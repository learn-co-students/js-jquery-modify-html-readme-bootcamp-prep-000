# Modify HTML With jQuery

## Objectives

+ Link jQuery to HTML file
+ Write inline jQuery to modify HTML
+ Explain how jQuery modifies HTML

## Inline jQuery

We're going to use jQuery to add some text to our HTML page. 

### Include jQuery Link

In order to start writing jQuery, we need to include the library in our HTML. One way to do this would be to download a copy of the jQuery library and include it with our project. We can also link to the library hosted by a content delivery network, or CDN. For this example, we'll be loading jQuery from Google's CDN. You'll want to copy the code below and paste it `html/index.html` in between your head tags. This script tag links our HTML file to the jQuery library.

```html
<script type="text/javascript" src="http://ajax.googleapis.com/ajax/libs/jquery/1.3/jquery.min.js"></script>
```

### Adding Text

Go ahead and open `html/index.html` in the browser. You should see a really boring looking website with the text `yo yo yo yo yo yo yo`.

We want to add the text `hey hey hey hey!!!!!` to end of our paragraph.

At the bottom of `index.html`, right before the closing `body` tag, we'll want to add an opening and a closing `script` tag:

```html
<script>
</script>
```

Between these tags is where we want to write our inline jQuery. The script tags need to be at the bottom of the page because the code we're going to write is dependent on the `p` tag being already loaded in the browser. Our jQuery will error if there isn't a `p` tag to add text to.

And now, in between the script tags, add the following code:

```js
$("#yo").append("hey hey hey hey!!!!!");
```

Save the changes to `html/index.html` and reload in the browser. You should see `yo yo yo yo yo yo yo hey hey hey hey!!!!!` on the page!!

The `$` tells our browser that we're using jQuery. The `("#yo")` is our jQuery selector -- we're selecting the HTML element with the ID `yo`. We're then using the jQuery `append` function, which adds text to an HTML element, and we're passing in `"hey hey hey hey!!!!!"` which is the text we want to add.

Don't worry too much about the mechanics of these selectors and functions, we'll go over those in way more detail. Just notice that the text appeared on the screen!

<p data-visibility='hidden'>View <a href='https://learn.co/lessons/js-jquery-modify-html-readme' title='Modify HTML With jQuery'>Modify HTML With jQuery</a> on Learn.co and start learning to code for free.</p>

<p class='util--hide'>View <a href='https://learn.co/lessons/js-jquery-modify-html-readme'>Modifying HTML with jQuery</a> on Learn.co and start learning to code for free.</p>
