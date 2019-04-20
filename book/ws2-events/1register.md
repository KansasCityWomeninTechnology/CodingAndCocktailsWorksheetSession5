1. Inside the `document.addEventListener("DOMContentLoaded", ...)` function at the bottom of _my-script.js_, we defined a function for the `onclick` event for the order button. We want to change the way we listen to events by registering an event listener. Replace the `onclick` with
   ```javascript
   document.getElementById('order-btn').addEventListener('click', () => {
         //drinkName code here
         submitOrder(document.getElementById('order-form-input').value);
   });
   ```
   {% hint style='info' %}
We are adding an event listener for 'click' events onto the DOM element with the id 'order-btn'. Upon clicking, we want the function to execute. The advantage of using `addEventListener` instead of `onclick` is that we can dynamically add and remove event listeners. We can also add multiple listeners for the same event.
   {% endhint %}

1. It's about time to add the drink name to the order list. Change the `submitOrder` function to take `drink` as a second parameter.
   {% hint style="tip" %}
Remember to separate parameters with a comma.
   {% endhint %}

1. We need to pass in the drink name into the `submitOrder` function. We can do that from the first 'order-btn' event listener function where we are passing in the order name, but the call to `submitOrder` is getting too cluttered. We can clean it up by querying the DOM and assigning the element values to a variable first, just like we did for `drinkName`. After the `drinkName` variable, create a variable called `orderName` and assign it to the value of `getElementById` call. 
   {% hint style="working" %}
<details>
<summary>
Need a little help? Expand this section for guidance. 
</summary> 
You want to store the value of <code>document.getElementById()</code> call to a variable named <code>orderName</code>.
Your code will look like this
<pre>
<code class="lang-javascript">
const drinkName = document.querySelector('input[type="radio"]:checked').value;
const orderName = document.getElementById('order-form-input').value;
</code>
</pre>
</details>
   {% endhint %}

1. Let's get rid of the `console.log()` in the event handler. We don't need that any more.

1. Update the call to `submitOrder` in the event listener to pass in the `orderName` and `drinkName` variables. 
   {% hint style='working' %}
<details>
<summary>
Need a little help? Expand this section for guidance. 
</summary> 
Change <code>submitOrder(document.getElementById('order-form-input').value);</code> function to <code>submitOrder(orderName, drinkName);</code>
</details>
   {% endhint %}

1. In the `submitOrder` function update the string concatenation `name + " would like a drink!"` to include the drink name.
   {% hint style='working' %}
<details>
<summary>
Need a little help? Expand this section for guidance. 
</summary> 
Change <code>name + " would like a drink!"</code> to
<code>name + " would like a " + drink</code>
</details>
   {% endhint %}

1. In Chrome, select a drink, add your name, and click the order button. Do you see the drink name included in the order? Select a different drink and click the order button again. Your drink order got replaced. How can we append to the new drink to the order instead of replacing it? 
   {% hint tip='tip' %}
You'll see an error if you don't select a drink. We'll fix this bug together in the Bonus assignment.
   {% endhint %}
