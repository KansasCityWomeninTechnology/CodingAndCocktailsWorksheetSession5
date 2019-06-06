1. Create a new function called `buildCocktailsMenu` after the declaration for the cocktails array with a parameter for `cocktails`. 

1. Inside the `document.addEventListener("DOMContentLoaded", ...)` function at the bottom of the file, before the calls to register the event listeners for the order button, call the new method, `buildCocktailsMenu` and pass in the drinks array.

1. Back in the `buildCocktailsMenu` function, iterate over the `cocktails` and log each element to the console using the following code

   ```javascript
  cocktails.forEach( (cocktail) => { 
     console.log(cocktail);
  });
   ```

   {% hint style='working' %}
The entire object in the array is logged out. We can access properties inside objects using the `.` notation. What if you want to only log the `label` within each drink? How would you change your log statement to do so?
   {% endhint %}

1. In the `buildCocktailMenu` before the `forEach`, create a variable named `cocktailsString`. Because we will modify this string, use `let` to declare the variable. Set the value to an empty string by setting `cocktailsString` to open and close quotes, `''`. This is the string we'll use to build the DOM.

1. After the `forEach`, we need to set the `innerHTML` property of the DOM element with the class `radio-group` to the `cocktailsString`. Using the document selectors we learned in the first section, write the code to do so.

   {% hint style='working' %}
<details>
<summary>
Need a little help? Expand this section for guidance. 
</summary> 
After the <code>forEach</code> use <code>document.querySelector('.radio-group').innerHTML = cocktailsString;</code>.
</details>
   {% endhint %}

1. Inside `forEach`, we'll use **string concatenation** to build the string and access the properties of `cocktail` object and set it to the `cocktailsString` variable. Replace the `console.log` with the following code

   ```js
cocktailsString = '<label class="radio" for="' + cocktail.id + '"><input type="radio" id="' + cocktail.id + '" name="drink" value="' + cocktail.label + '">' + cocktail.label + '</label>';
   ```
   
   {% hint style='working' %}
Our goal is to build an HTML element structure that looks like what you commented out in the HTML for each drink object in the array. We want to create something that looks like this using the drink's name and id:

```html
<label for="focusedLady">
      <input type="radio" id="focusedLady" name="drink" value="Focused Lady">
      Focused Lady
</label>
```
   {% endhint %}

1. Save your file and try running in Chrome. Do you see the cocktail menu? Do you only see one item in the list though? ![](../assets/emojis/confused-face.png)

1. Let's take a look at the code again. We're setting the value of `cocktailsString` to the DOM string for each cocktail. This means the value of `cocktailsString` is getting overridden each time. We need to add to the string instead of replacing it. Hint-- what were some ways we add in JavaScript?

   {% hint style='working' %}
<details>
<summary>
Need a little help? Expand this section for guidance. 
</summary> 
To add to the cocktails string by using <code>cocktailString = cocktailString + ...</code> or use shorthand method <code>cocktailString += ...</code>.
</details>
   {% endhint %}

1. Interact with your web app in Chrome. You should see the drink list and be able to place orders again!

