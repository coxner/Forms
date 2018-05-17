# Forms

### Basics

The first step to creating a form is start with the opening `<form>` tag. In between the opening and closing form tag is where all the form controls and fields are stored. We can also tell the form where to send data when it is submitted by using action attribute. The method attribute get hold two values post or get. Post will send the data to the server while get will fetch data from the server.

### Dividing our form

We can divide our forms into logical sections that make sense. When indicating the start of a new section we use the `<fieldset>` tag. When providing this new section of code with a title we use the `<legend>` tag. As you can see each piece of information you want the user to submit in done with a `<label>` tag and a `<input>` tag. When we create a label and a input the value of the for attribute in the label tag must be equal to the id attribute of the input tag. **Unless** we wrap the label tag around the input tag like this..

`<label>Full Name`  
`<input type="text" name="name">`  
`</label>`

When the label tag is wrapped around the input tag as shown above the realtionship between the two is implied.

### The type attribute

Check out how the type attribute affects the appearence of the input box. Try typing in the box with `type="password"` notice how the output is affected. By setting `type="checkbox"` we can give the user a checkbox they can check and uncheck. Another thing we can do with the type attributes is provide them values that make them buttons. The two most popular ones are `type="submit"` and `type="reset"` the submit buttons sends form data to its destinantion and reset clears all the information the user has in input boxes. **Buttons need javascript code with them to function**.

### Using placeholders

Using placeholders in forms is essetntial in providing infomation to users on what should be entered in each input. Everyone of us has seen placeholders in forms before. They are done with the attribute `placeholder="placeholder_value"` you can observe them in use in _forms.html_.

### Autofocus

When a user visits the page with your form on it you may want to place the cursor in a input box by default. This is done with `autofocus` as you can see in _forms.html_ `autofocus` is placed in the name input box so by default when the page loads the cursor is placed there.

### HTML5 Validation

If we have a input box that the user **must** provide info for we provide it with the attribute `required`. The problem with the required attribute is that there is no visual que that tells a user that this input is required. Thats why in _forms.html_ we provide a \* beside the label that is required. Validation only occurs when the user clicks the submit button. The browser checks the fields from top to bottom so as soon as it comes across a input with the required attribute that's input is empty it stops checking and displays the error message on that input. So if a user had two blank required fields the next error would not be displayed until they correct the first and hit the submit button again. But what if we wanted to turn off validation? This can easily done with the attribute `novalidate`. Someone might do this if they wanted to test server side code.

### CSS Styling for Validation

In the previous section we were introduced the required attribute. This section will introduce a few new attributes to you. `valid` and `invalid` which apply styles to elements if they contain mistakes. However the HTML form does not actually know there is a mistake until the submit button is hit. An example of CSS styling form elements is.
`input:required {`  
 `background-color: yellow;`  
`}`
We can also style items after the submit button has been hit on a invalid item like..
`input:required:invalid {`  
 `background-color: yellow;`  
`}`

### Regular Expressions

A regular expression is a pattern written in the regular expression language. The regular expression language can do things like make sure an email contains the @ symbol or that a postal code follows the correct sequence of digits and numbers. Check out this example below..

`[0-9]{3}-[A-Z]{3}`

What does this expression mean? The square brackets `[0-9]` only accepts digits ranging from 0-9 the `{3}` means that 3 digits between 0-9 are required. The `[A-Z]` means only capital letters from A-Z are acceptable and the `{3}` means there must be 3 of them.

`587-ADC` -- This would be an acceptable combo
`587-Adc` -- This would not be

More information on regular expressions [here](https://www.w3schools.com/jsref/jsref_obj_regexp.asp)
