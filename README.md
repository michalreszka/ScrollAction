# ScrollAction
ScrollAction is a simple script that makes it easy to execute your own JavaScript functions and/or CSS classes whenever you scroll to an element. 

## 1. Add script to HTML.

Add jQuery script:
```
<script src="js/jquery-3.3.1.min.js"></script>
```
Add scrollaction.js script right before closing `</body>` tag:
```
<script src="js/scrollaction.js"></script>
```

## 2. Add class and parameters to youre element.

Add class "scrollAction" and parameters to some element in `scroll-action` attribute. In this example `</div>` tag:
```
<div id="someButton" class="scrollAction" 
     scroll-action="funcName:testAction,cssClass:testClass,cssElem:#someButton,onlyOnce:false">
     <p>CLICK ME</p>
</div>
```

### Attribute explanation.</h3>
`funcName` - Your JavaScript function that need to be executed when the element is visible. Function must be present in "window" object:
```
window.testAction = function() {
	$("#someButton").animate({height: "300px"});
}
```
Set it with parameter `none` if you don't need it.

`cssClass` - CSS class you want to add to some element when when is visible:
```
.testClass {
	background-color: #f00;
}
```
Set it with parameter `none` if you don't need it.

`cssElem` - the element ID to which you want to add CSS class.

`onlyOnce` - determines whether your JavaScript function and the CSS class are to be run each time the element is visible again. Parameters are "true" or "false". When "true" is selected the CSS class is removed from the element each time when it stops being visible. 
