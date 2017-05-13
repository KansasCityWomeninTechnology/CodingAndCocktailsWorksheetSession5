### Part I: Manual Practice {#part-i-manual-practice}

First, let’s take a look at how to manually organize your project files.

1.  Download the assets at [http://bit.ly/2bVHBAi](http://bit.ly/2bVHBAi) and unzip the file.

{% hint style='info' %}

**Assets** are valuable files for your web site or application. Think _CSS_, _JavaScript_, _images_, _videos_, etc.

{% endhint %}

2.  Create a new folder named _app_ in your _CodingAndCocktails/Architecture_ folder. This will serve as the root directory for your application.

{% hint style='info' %}

The **root** directory is the top level directory for your project.

The _CREDITS_, _LICENSE_ and _index.html_ files will live here for the website we'll be previewing. These contain information on copyright information and credits for any licensed objects. The template downloaded is licensed by [templated.co](http://templated.co), a great resource for website templates.

{% endhint %}

1.  Let’s get organizing! Create the necessary folders and add your project files like in the following diagram.

       ![](../assets/images/image06.png)

  {% hint style='info' %}

  The directory name **js** is interchangeable with the directory name **scripts**.

  {% endhint %}

1.  Now open the _index.html_ file in Google Chrome to preview your site. Oh no! Looks like the site is broken. We’re missing the styling and some images specifically. Our HTML page doesn’t know how we’ve organized our project so we’ll need to tell it where to find the files it needs.

       ![](../assets/images/image14.png)

<!--sec data-title="Cloud9: Preview" data-id="cloud9Preview" data-show=true data-collapse=true ces-->

- To preview your file in Cloud9, right click on the _index.html_ file & select **Preview**.

- Instead of Atom, you'll be using the built-in text editor in your workspace. Double-click on the _index.html_ file to open it in the editor.

<!--endsec-->

1.  Open _index.html_ in Atom and search for all the lines starting with `< -- REPLACE DIR PATH`  to remove that block of code. Also remove the closing comment mark, `-->` at the end of the same lines.

2.  In those same lines, you’ll see  `DIR` where the path of the files referenced should be. Replace `DIR` with the applicable file path. In the example below, that would be `assets/css/main.css`.

  1. Before:<br>
     ![](../assets/images/image02.png)

  2. After:<br>
     ![](../assets/images/image01.png)

3.  Go through the rest of the _index.html_ file and make the same necessary changes for the other lines beginning with  `<-- REPLACE DIR PATH`. Once done, save _index.html_ and reload it in your browser.

{% hint style='info' %}

Watch out for the `data-video="DIR"`! Make sure to read all the `<!-- Banner -->` comment details for replacing `DIR` with the file path. When you set this correctly, there is _JavaScript_ that will load a video in the background of your site.

{% endhint %}

Your site should now be working! We’ve organized all of your files AND _index.html_ knows where they are located.

![](../assets/images/image10.png)

![](../assets/images/7.png)
