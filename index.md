
## Welcome to our Page
## Spanish Word of the Day

### Our Calendar
<iframe src="https://calendar.google.com/calendar/embed?src=uq46bc7ifmnpriogg47mqcq5tg%40group.calendar.google.com&ctz=America%2FNew_York" style="border: 0" width="800" height="600" frameborder="0" scrolling="no"></iframe>


### The Grocery List

<!DOCTYPE html>
<html><head><meta charset="UTF-8">
<title>HTML5 notepad app</title>
<meta charset="utf-8">
<!--[if lt IE 9]><script src="http://html5shiv.googlecode.com/svn/trunk/html5.js"></script><![endif]-->
<style>
html,body{background:#FCFCFC;color:#444;height:100%;width:100%;margin:0;padding:0;}
#notepad{height:98%;width:98%;padding:1%;font-size:100%;line-height:125%;font-family:san-serif}
::selection{background:#7D7}
::-moz-selection{background:#7D7}
</style>
</head>
<body>
<textarea placeholder="Type here, see it here..."  id="notepad">
<!--
  you could do any element w/ contentEditable, but that doesn't fire onchange
--> 
</textarea>
<script>
/* localstorage polyfill from https://gist.github.com/350433 */
("undefined"==typeof window.localStorage||"undefined"==typeof window.sessionStorage)&&function(){function e(f){function e(a){var b;b=new Date;b.setTime(b.getTime()+31536E6);document.cookie="localStorage="+a+("; expires="+b.toGMTString())+"; path=/"}function g(a){a=JSON.stringify(a);"session"==f?window.name=a:e(a)}var d=function(){var a;if("session"==f)a=window.name;else a:{a=document.cookie.split(";");var b,c;for(b=0;b<a.length;b++){for(c=a[b];" "==c.charAt(0);)c=c.substring(1,c.length);if(0==c.indexOf("localStorage=")){a=
c.substring(13,c.length);break a}}a=null}return a?JSON.parse(a):{}}();return{length:0,clear:function(){d={};this.length=0;"session"==f?window.name="":e("")},getItem:function(a){return void 0===d[a]?null:d[a]},key:function(a){var b=0,c;for(c in d){if(b==a)return c;b++}return null},removeItem:function(a){delete d[a];this.length--;g(d)},setItem:function(a,b){d[a]=b+"";this.length++;g(d)}}}if("undefined"==typeof window.localStorage)window.localStorage=new e("local");if("undefined"==typeof window.sessionStorage)window.sessionStorage=
new e("session")}();

/* the code */
	var n = document.getElementById("notepad");
	/* save */
	var s = function(){localStorage.setItem("notepad", n.value);}
	/* retrieve (only on page load) */
	if(window.localStorage){ n.value = localStorage.getItem("notepad");}
	/* autosave onchange and every 500ms and when you close the window */
	n.onchange = s();
	setInterval( s, 500);
	window.onunload = s();
</script>
</body>
</html>

### Support or Contact

Having trouble with Pages? Check out our [documentation](https://help.github.com/categories/github-pages-basics/) or [contact support](https://github.com/contact) and we’ll help you sort it out.
