1. Open _index.html_ in Atom. 
   {% hint style="tip" %}
Open Atom by typing `atom .` <i class="fa fa-share fa-rotate-180"></i>.

Chromebook users- You will use the built in file editor
  {% endhint %}

1. In Atom, search for a line starting with `<!-- REPLACE DIR PATH` and ending with `-->`.
   {% hint style="info" %}
The `<!--   -->` wraps a comment in HTML. Feel free to grab a mentor and ask for a quick synopsis of HTML if you didn't attend the HTML session or if you need a refresher.
   {% endhint %}
  
1. Remove the opening comment block, `<!-- REPLACE DIR PATH`. Also remove the closing comment mark, `-->` at the end of the same lines.

1. In the remaining code on that line, you’ll see `DIR` where the path of the referenced file should be. Replace `DIR` with the applicable file path. In the example below, the path is `assets/css`.

  1. Before:

     ![](images/code-before.png)

  1. After:

     ![](images/code-after.png)

1. Go through the rest of the _index.html_ file and make the same necessary changes for the other lines beginning with  `<!-- REPLACE DIR PATH`. Once done, save _index.html_ and reload it in your browser.

  {% hint style='tip' %}
Keep an eye out for `data-video="DIR"`. When you get to this code block, make sure to read all the `<!-- Banner -->` comment details for replacing `DIR` with the file path. When you set this, there is _JavaScript_ that will load a video in the background of your site.
  {% endhint %}

1. Reload _index.html_ in Chrome. Open Chrome DevTools and take a look at the console to see if there are any errors finding references. You can open Chrome DevTools on Windows by pressing `F12` and on a Mac using the keyboard shortcut `cmd+opt+i`. If you missed a file reference it will show up as an error. Fix any errors you find.

1. Your site should now be working! We’ve organized all your files AND _index.html_ references all the assets properly.

![](images/finished.png)
