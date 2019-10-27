1. In the `submitOrder` function, we'll programmatically add new HTML elements to append to the DOM instead of calling `alert`. Create an `<h3>` element and assign it to a variable. Replace the call to `alert` with the following code:

   ```javascript
   let node = document.createElement('h3');
   ```

   {% hint style="working" %}
We want to create the following HTML using DOM manipulation

   ```html
<h3>
       Ada Lovelace would like a Focused Lady
</h3>
<h3>
       Grace Hopper would like a Nerdy Daiquiri
</h3>
   ```
   {% endhint %}

   {% hint style='info' %}
We are using the `Document` API to create a new `<h3>` element and assigning it to the variable `node`. We're using `let` to assign the variable instead of `const` because we need to modify the element. Variables declared with `const` are for read-only use.

We now have a structure that looks like `<h3></h3>`. There's no text inside yet.
   {% endhint %}

1. After creating the `<h3>` element, create a text node to house the text for the order detail using the code below. We can pass in the string concatenation to build the order detail into the text node.

   ```javascript
   const textNode = document.createTextNode(name + " would like a " + drink);
   ```
   {% hint style="info" %}
We created a structure with only text but it's not attached to anything.
   {% endhint %}

1. Now we need to append the text node on to the element. We do this by calling `node.appendChild(textNode);`. 

   {% hint style="info" %}
We added the text as a child of the `<h3>` element to recreate HTML structure we want, but it's not attached to the DOM yet.
   {% endhint %}

1. We need to find the parent node to add the `<h3></h3` we created. We want to add the order info to the parent element that has the class "order-details". Using the Document API, query for the "order-details" class.

   {% hint style="working" %}
<details>
<summary>
Need a little help? Expand this section for guidance. 
</summary> 
You want to use the <code>document.querySelector()</code> method and pass in the class name <code>'.order-details'</code>.
Your code will look like this
<pre>
<code class="lang-javascript">
document.querySelector('.order-details');
</code>
</pre>
</details>
   {% endhint %}

1. Finally, we can append the node to the DOM element so that it shows up on the web page. Use the `appendChild()` method and pass in the text node as a parameter to the parent element. 

   {% hint style="working" %}
<details>
<summary>
Need a little help? Expand this section for guidance. 
</summary> 
You want to use the node you queried for in the last step and call <code>appendChild()</code> method and pass in the text node you created called <code>node</code>.
Your code will look like this
<pre>
<code class="lang-javascript">
document.querySelector('.order-details').appendChild(node);
</code>
</pre>
</details>
   {% endhint %}

1. Try ordering a few drinks on your web page using Chrome. Do you see each drink added to the drink order list? 

   {% hint style='working' %}
We can also see the DOM getting updated in the **Elements** tab inside DevTools. You can inspect DOM elements by right clicking on the drink list and selecting **Inspect**. Ask a mentor to help you inspect DOM elements.
   {% endhint %}
