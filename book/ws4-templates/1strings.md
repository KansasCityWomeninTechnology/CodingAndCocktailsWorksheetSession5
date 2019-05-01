1. Inside the `submitOrder` method, we are using string concatenation to build the string `name + " would like a " + drink`. Change the 'name' to use template literal. Template literals use backticks (\`\`) instead of quotes. Change the string to

   ```javascript
`${name} would like a ` + drink
   ```
   
   {% hint style='info' %}
Remember to change the single quotes to backticks.
   {% endhint %}

1. Now change the 'drink' parameter to use template literal.

   {% hint style='working' %}
<details>
<summary>
Need a little help? Expand this section for guidance. 
</summary> 
Replace the string concatenation with 
<pre>
<code class="lang-javascript">
const textNode = document.createTextNode(`${name} would like a ${drink}`);
</code>
</pre>
</details>
   {% endhint %}

1. There's one more place that uses string concatenation. It's the `cocktailsString` that we used to build the DOM. Change the string to use template literals. Be careful this one is a long string with double quotes in it so it's a little tricky. But you got this!

   <!-- {% hint style='working' %}
<details>
<summary>
Need a little help? Expand this section for guidance. 
</summary> 
Replace the string concatenation with 
<pre>
<code class="lang-javascript"> 
cocktailsString += `<label class="radio" for="${cocktail.id}"><input type="radio" id="${cocktail.id}" name="drink" value="${cocktail.label}">${cocktail.label}</label>`;
</code>
</pre>
</details>
   {% endhint %} -->
