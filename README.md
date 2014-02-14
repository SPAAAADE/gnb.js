gnb.js
=========

jQuery plugin for GNB navigation and scroll to menu

HTML Markup
```
<ul id="gnb">
	<li><a href="#main">Main</a></li>
   	<li><a href="#sub">Sub</a></li>
   	<li><a href="#usage">Usage</a></li>
   	<li><a href="#help">Help</a></li>
</ul>


<div id="WrapDiv">
<div id="main">
	<h1> Main </h1>
    <!-- Contents -->
</div>

<div id="Sub">
	<h1> Sub </h1>
    <!-- Contents -->
</div>
</div>
.
.
.
```

Javascript 

```
(function ($) {
    $(document).ready(function () {
    	//set  gnb UL element
        var oUl$ = $('ul#gnb');

        oUl$.gnb({
            wrapper: '#WrapDiv', //selector name that wrap contents DIVs
            duration:700,           //scroll animate during time , default 1000
            activeclass: 'on'        // class name that active menu item , default 'active'
        });
    });
})(jQuery);
```


### Options

```
{
easing       : 'swing', 	  // aniamate easing
duration     : 1000, 		// animate during time
anchor       : 'li a',   		// menu anchor element
exception    : null, 		// except element 
activeclass  : 'active',   // class name that active menu item
wrapper      : null,        // selector name that wrap contents DIVs
bindingwindow: true,   // bind scroll event window that set menu active 
correction   : null         // value of correction ,that scroll offset position
};
```