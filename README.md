# ScrollAction
ScrollAction is a simple script that makes it easy to execute your own JavaScript functions and/or CSS classes whenever you scroll to an element. 

<h2>1. Add script to HTML.</h2>

Add script right before closing `</body>` tag:</br>
```
<script src="js/scrollaction.js"></script>
```
<h2>2. Add class and parameters to youre element.</h2>

Add class "scrollAction" and parameters to some element in `scroll-action` attribute. In this example `</div>` tag:
```
<div id="someButton" class="scrollAction" 
     scroll-action="funcName:testAction,cssClass:testClass,cssElem:#someButton,onlyOnce:false">
     <p>CLICK ME</p>
</div>
```
