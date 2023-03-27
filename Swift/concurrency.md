# Swift Concurrency

- by default everything runs on main theread. what if we want to add a delay?

- use ```DispatchQueue``` 

```swift 
DispatchQueue.main.asyncAfter(deadline: .now()+2, execute: {
            self.dataArray.append("Title1 : \(Thread.current)")
        })  // this is still on main thread. what if we want to do it on bg thread?
```
The above example will run after 2 sec in main thread.


```swift!
  func runOnBg(){
        
        DispatchQueue.global().asyncAfter(deadline: .now()+2){
            
            let title3 = "Title3- runs on bg and appends to main thread after 2 sec : \(Thread.current)"
            
            DispatchQueue.main.async {
                self.dataArray.append(title3)
            }
            
        }
    }
```

The above exaple will take the code and put it into bg theread and after 2 seconds it is put back to main thread.

This is how we used to do before async await.


```swift!
class AsyncAwaitModel:ObservableObject{
    @Published var dataArray:[String] = []
    
    
    
    func addAuthor() async {
        
        let author1 = "Koushith-Author1 : \(Thread.current)"
       
        try? await Task.sleep(nanoseconds: 2000000000)
        
        await MainActor.run(body:{
            self.dataArray.append(author1)
        })
    }
    
}

struct AsyncAwait: View {
    @StateObject var viewModel = AsyncAwaitModel()
    var body: some View {
        ZStack{
            List{
                ForEach(viewModel.dataArray, id: \.self) { data in
                    Text(data)
                }
            }
            .onAppear{
                Task{
                    await viewModel.addAuthor()
                }
                
            }
            
        }
    }
}

```


before updating the ui just switch back to main thread. orelse it will throw a warning.

Task allow us to start async action as soon as view is appeared. this will automatically cancelled when the view is destroyed.

- its a great place to fetch some async data.

```swift!
 await MainActor.run(body:{
            self.dataArray.append(author1)
        })

// this will switch back to main thread.
```
