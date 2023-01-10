### HTML Forms

- default vbehavior of form is it will refresh the page when button is clicked
- default methods 
    - GET
    - Input- text
    - Button -submit

```
<form method="get" action="act.html or url">

// input feilds
  <button>sublit</button>
</forrm>
```

- inside form tag button behaves as subit and refreshes. if you take out it wont
- you can link the form using ``` form="some-form" ``` attrivute.

- you can change the default methods. always check the network tab

GET - defaults will add the form data in url 
POST - it will be inside body

## autocomplete on form tag- if off it will clear previous search history
```

<form method="get">
  <label>Name:
    <input name="submitted-name" autocomplete="name" />
  </label>
  <button>Save</button>
</form>

```

name attribute groups. (in checkbox, radio) 

datalist tag- similar to select (dropdown but it gives some suggestions and can type)
- you can do whole lot of validsation stuffs natively. like required, regex (pattern attribute)

- submitted form data will be like an obj

https://developer.mozilla.org/en-US/docs/Web/HTML/Element/form
https://developer.mozilla.org/en-US/docs/Learn/Forms/HTML5_input_types
