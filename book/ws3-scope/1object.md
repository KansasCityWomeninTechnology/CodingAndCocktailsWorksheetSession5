1. In Atom, open _index.html_ and find the `div` tag containing the drink list. Comment out all the drinks listed inside the `div`, but don't comment the `div` tag itself. Save your _index.html_. We no longer see the drink list in Chrome and our web page is broken for the moment.

   {% hint style='working' %}
Highlight all the `<label>` elements inside the `div` with class "drink-menu" and select **Edit** <i class="fa fa-long-arrow-right"></i> **Toggle Comments**. You can also use the keyboard shortcut `ctrl` + `/` on Windows and `cmd` + `/` on Macs. Feel free to ask a mentor for help. 
   {% endhint %}

   {% hint style='tip' %}
Remember to use Atom to type code statements and Chrome to verify your work when your web page reloads. Don't forget to save _my-script.js_ every time you type a code statement.
   {% endhint %}

1. In _my-script.js_, at the top of the file, create a new `const` variable named `cocktailsArray` that will hold the array of drinks. 

1. We want to populate `cocktailsArray` with the list of available drinks, which is everything with a radio button in front of it. To do so, each element in the array is an object with 2 properties: "id" and "label". We can add an object to the array like this

   ```javascript
   const cocktailsArray = [{
      'id': 'focusedLady',
      'label': 'Focused Lady'
    }];
   ```

    {% hint style="info" %}
Everything inside the `{}` is part of the object. The curly braces help group code statements together. We know the difference between objects and functions by the way we declare it. `const myObject = {};` is an object and `const myFunction = () => {};` is a function because of the parenthesis arrow in the definition.

Objects can contain key-value pairs like this:

```javascript
{
          "key": "value",
          "anotherKey": "Another Value"
}
```

You can use single quotes, double quotes, or use no quotes when declaring keys in an object.
   {% endhint %}

1. Populate the rest of the `cocktailsArray` with the remaining drinks. Copy and paste the following code snippet to replace `cocktailsArray` to avoid typing fatigue. 

   ```javascript
    const cocktailsArray = [{
            'id': 'focusedLady',
            'label': 'Focused Lady'
        },
        {
            'id': 'strongLady',
            'label': 'Strong Lady'
        },
        {
            'id': 'frontEndPunch',
            'label': 'Front-End Punch'
        },
        {
            'id': 'cachedOut',
            'label': 'Cached Out'
        },
        {
            'id': 'httPapaya',
            'label': 'httPAPAYA://'
        },
        {
            'id': 'nerdyDaiquiri',
            'label': 'Nerdy Daiquiri'
        },
        {
            'id': 'theAvernaCode',
            'label': 'The Averna Code'
        },
        {
            'id': 'focusedTheMostest',
            'label': 'Focused the Mostest'
        },
    ];
   ```
   
   {% hint style="info" %}
Notice we use a comma after declaring each object in the array. This allows us to create multiple elements in an array at the same time. We elected to use single quotes for the `id` and `label` properties within each object.
   {% endhint %}



