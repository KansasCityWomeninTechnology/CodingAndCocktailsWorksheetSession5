# Scaffold an Angular Application

Angular is a popular web development framework with a powerful command line tool. You can use the Angular CLI to scaffold an Angular application.

{% hint style='tip' %}
##### Hey Slacker!

Remember, we're here to help.
Join the KCWiT #codingandcocktails Slack Channel: [kcwit.slack.com](http://kcwit.slack.com)
{% endhint %}

1. In the terminal, install Angular CLI by typing `npm install -g @angular/cli` <i class="fa fa-share fa-rotate-180"></i>.

1. Navigate to "CodingAndCocktails/Architecture" folder by following the instruction for your OS and press `Enter`.
   {% codetabs name="Mac", type="bash" -%} 
cd ~/CodingAndCocktails/Architecture
   {%- language name="Windows", type="bash" -%} 
cd %USERPROFILE%/CodingAndCocktails/Architecture
   {%- language name="Chromebooks", type="bash" -%} 
cd ~/workspace/CodingAndCocktails/Architecture
   {%- endcodetabs %}

1. Type `ng new angular-app` <i class="fa fa-share fa-rotate-180"></i>.
   {% hint style='tip' %}
Angular CLI creates a folder for you so there's no need to create a folder for your application.
   {% endhint %}

1. Type `cd angular-app` <i class="fa fa-share fa-rotate-180"></i> to navigate into the newly created "angular-app" directory.

1. Take a look at the file organization using Atom or the file explorer.

1. Type `ng serve` <i class="fa fa-share fa-rotate-180"></i> to serve your application.

1. In Chrome, navigate to [localhost:4200](http://localhost:4200/). You'll see the Angular logo and helpful links! 🎉

1. Press keys **Ctrl+C** together to stop the server.
 