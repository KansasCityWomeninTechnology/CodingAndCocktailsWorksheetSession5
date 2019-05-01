1. Let's retrieve the value of the selected drink by first creating the variable to hold the value. In _my-script.js_, inside the `onclick` handler above the call to the `submitOrder` function, declare a variable for the name of the drink using a descriptive name. 

      {% hint style="working" %}
<details>
<summary>
Need a little help? Expand this section for guidance. 
</summary> 
You want to create a <code>const</code> variable named for the value it will hold, such as <code>drinkName</code>.
Your code will look like this
<pre>
<code class="lang-javascript">
const drinkName
</code>
</pre>
</details>
   {% endhint %}

1. Last time we retrieved an element by its id using `getElementById()`. This time we'll use `querySelector()` to retrieve an element by CSS selectors. Set your variable equal to `document.querySelector();`.

   {% hint style="info" %}
There's different ways to access the DOM from JavaScript. Tonight we explore `getElementById()` and `querySelector()`. Sometimes it makes sense to define an id to an element so your code can access it easily. But as an application grows and the number of elements increases, having a way access elements without defining an id to each is powerful. 
   {% endhint %}

1. Below your query selector, write your variable out to the console so that we can see how this works.

      {% hint style="working" %}
<details>
<summary>
Need a little help? Expand this section for guidance. 
</summary> 
You want to pass in your variable into <code>console.log()</code>.
Your code will look like this
<pre>
<code class="lang-javascript">
const drinkName = document.querySelector();
console.log(drinkName);
</code>
</pre>
</details>
   {% endhint %}

1. Now we need to find the CSS selector string for the radio button but first, let's take this `querySelector` out for a test run. Let's try grabbing the text in `<h1>` tag first. The `querySelector` method takes a string without the open and close brace (just like we did in the CSS session). Change your `querySelector` code to

   ```js
   document.querySelector('h1');
   ```

   {% hint style='tip' %}
Need a CSS refresher? Grab a mentor or review the Coding & Cocktails [CSS Slides](http://bit.ly/cnccssslide) or [Worksheet](http://bit.ly/cnccsswork)!
  {% endhint %}

1. Save your file. In Chrome, select a drink and press the **Order** button. Do you see your query selector write out to the console? Since we didn't specify that we only want the text, we see the entire `<h1>` HTML element.

   {% hint style="working" %}
How can we change our `getElementById` to use `querySelector` instead? Can we use `getElementById` to retrieve the text in the `<h1>`? Feel free to talk it out with your mentor. They love acting as a sounding board!
   {% endhint %}

1. Time to get the selected drink! This time, the CSS selector string is a little more specific. In Atom, change the CSS selector string for your `querySelector` to `'input[type="radio"]:checked'`.

   {% hint style='info' %}
Let's walk through this CSS selector string. The radio buttons are `<input>` elements with the **attribute** `type="radio"`. Selectors use square brackets `[]` for attributes. Then we only want the selected radio button, which uses the pseudo-class `checked`. Selectors use colons `:` for pseudo-classes.

You can also write a style in the CSS file using this selector too!
  {% endhint %}

1. Save your file. In Chrome, select a drink and press the **Order** button. Hrm... We see the HTML element not the drink name.Do you see your drink name write out to the console?

   {% hint style='info' %}
We can't get the selected drink name by id because we don't know which id is the **selected** drink. This is an example of the power of query selectors.
   {% endhint %}

1. Let's get the drink name-- that's the `value` of the HTML element. In Atom, make your change and double check your work by saving your file and testing it out in Chrome.

   {% hint style="working" %}
<details>
<summary>
Need a little help? Expand this section for guidance. 
</summary> 
You want the <code>value</code> of the <code>document.querySelector()</code>.
Your code will look like this
<pre>
<code class="lang-javascript">
const drinkName = document.querySelector('input [type="radio"]:checked').value;
console.log(drinkName);
</code>
</pre>
</details>
   {% endhint %}
