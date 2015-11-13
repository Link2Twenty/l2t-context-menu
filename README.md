# < l2t-context-menu >
Have a quick look at the [Component page](http://link2twenty.github.io/l2t-context-menu)

## What is it?
"l2t-context-menu" is a polymer element to replace the standard right click 'context menu'.

Here's a sneak peak of the demo page

![Screenshot](https://media.giphy.com/media/3oEduNTdEfa03WUZPO/giphy.gif)

## Getting started

### Install with bower

First you need bower, [see their site](http://bower.io/) for details 

```
bower install --save l2t-context-menu
```

### Attributes

| Attribute Name | Functionality | Default |
|----------------|-------------|-------------|
| parentclass* | Sting for storing class name of which classes should be listened too | "default" |
| linkcolor | Sting for storing theme color for mouse over and link color | "#0066aa" |
| backcolor | Sting for storing theme color for background color | "#fff" |
| headcolor | Sting for storing theme color for standard text color | "#333" |
| sepacolor | Sting for storing theme color for <hr> separaters | "#bcbcbc" |

required*

### How to use

If you are looking at useing other peoples custom polymer elements I am going to guess you have some idea what's going on already. If not have a look at the [polymer site](http://polymer-project.org).

Put a link to l2t-context-menu in your header, it should look something like.
```html
<link rel="import" href="bower_components/l2t-context-menu/l2t-context-menu.html">
```

Now that you have imported it you can get to using it on your page
```html
<body>
<div class="specialcase">
Text with a special context menu
</div>
Text with a standard context menu
<l2t-context-menu parentclass="specialcase">
  <li><b>First List Items:</b></li>
  <li><a href="#">Item 1</a></li>
  <li><a href="#">Item 2</a></li>
  <hr>
  <li><b>More Items:</b></li>
  <li><a href="#">Item 3</a></li>
</l2t-context-menu>
</body>
```

And just like that you have a custom menu, right click within the div and the custom menu opens right click anywhere else and you get the standard one.

To theme the menu from above we would have added a few extra attributes

```html
<l2t-context-menu parentclass="specialcase" 
  linkcolor="#FFE0B2" backcolor="#F57C00" 
  headcolor="#fff" sepacolor="#FFE0B2">
  <li><b>First List Items:</b></li>
  <li><a href="#">Item 1</a></li>
  <li><a href="#">Item 2</a></li>
  <hr>
  <li><b>More Items:</b></li>
  <li><a href="#">Item 3</a></li>
</l2t-context-menu>
```
Let's have a little look at what we just made:
![Screenshot](https://media.giphy.com/media/3oEduLDQYvcl6cSM2Q/giphy.gif)

These are, of course, optional extras to make the menu match your own app a little better.

### Long press

On mobile you can simulate a right click by long pressing, which is great and means this menu is inherently compatible.
Unfortunately if you long press text the select box takes president over the right click functionality, meaning the menu does not appear.

The easy way around this is to have some CSS to dissable text select such as
```css
  .nonselectable{
    -webkit-touch-callout: none;
    -webkit-user-select: none;
    -khtml-user-select: none;
    -moz-user-select: none;
    -ms-user-select: none;
    user-select: none;
  }
```
