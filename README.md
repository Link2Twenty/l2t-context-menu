# < l2t-context-menu >
Have a quick look at the [Component page](http://link2twenty.github.io/l2t-context-menu)

## What is it?
"l2t-context-menu" is a polymer element to replace the standard right click 'context menu'.

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
  <li><a href="#">Item 1</a></li>
  <li><a href="#">Item 2</a></li>
</l2t-context-menu>
</body>
```
