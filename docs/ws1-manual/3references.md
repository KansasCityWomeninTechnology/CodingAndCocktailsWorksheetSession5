1. Open _index.html_ in Atom. 
   {% hint style="tip" %}
Open Atom by typing `atom .` <i class="fa fa-share fa-rotate-180"></i>.

Chromebook users- You will use the built in file editor
  {% endhint %}

1. In Atom, search for all the lines starting with `< -- REPLACE DIR PATH`  to remove that block of code. Also remove the closing comment mark, `-->` at the end of the same lines.

  {% hint style="info" %}
The `<!--   -->` wraps a comment in HTML. Feel free to grab a mentor and ask for a quick synopsis of HTML if you didn't attend the HTML session or if you need a refresher.
  {% endhint %}

1.  In those same lines, you’ll see `DIR` where the path of the files referenced should be. Replace `DIR` with the applicable file path. In the example below, that would be `assets/css`.

  1. Before:

     ![](images/code-before.png)

  1. After:

     ![](images/code-after.png)

1.  Go through the rest of the _index.html_ file and make the same necessary changes for the other lines beginning with  `<-- REPLACE DIR PATH`. Once done, save _index.html_ and reload it in your browser.

  {% hint style='tip' %}
Watch out for `data-video="DIR"`. Make sure to read all the `<!-- Banner -->` comment details for replacing `DIR` with the file path. When you set this, there is _JavaScript_ that will load a video in the background of your site.
  {% endhint %}

1. Reload _index.html_ in Chrome. Open Chrome DevTools and take a look at the console to see if there are any errors finding references. You can open Chrome DevTools on Windows by pressing `F12` and on a Mac using the keyboard shortcut `cmd+opt+i`. Fix any errors.

1. Your site should now be working! We’ve organized all your files AND _index.html_ references all the assets properly.

![](images/finished.png)
