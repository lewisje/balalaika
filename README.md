Balalaika.js
=========

[![Join the chat at https://gitter.im/finom/balalaika](https://badges.gitter.im/Join%20Chat.svg)](https://gitter.im/finom/balalaika?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge&utm_content=badge)
## The tiny DOM library (1kB uncompressed and 600 bytes gzipped!)

Balalaika provides you tiny replacement for huge DOM libraries such as jQuery and Zepto. It contains few methods which should be sufficient for vanilla.js developers.

### How can I use it?
First of all you can use it as common library on the web page. Just paste this code to the ``head`` tag:
```html
<script>
window.$=function(t,e,n,o,r,i,s,c,u,f,l,p){"use strict";return p=function(t,e){return new p.i(t,e)},p.i=function(o,r){n.push.apply(this,o?o.nodeType||o==t?[o]:""+o===o?/</.test(o)?((c=e.createElement(r||"q")).innerHTML=o,c.children):(r&&p(r)[0]||e).querySelectorAll(o):/f/.test(typeof o)?/c/.test(e.readyState)?o():p(e).on("DOMContentLoaded",o):o:n)},p.i[l="prototype"]=(p.extend=function(t){for(f=arguments,c=1;c<f.length;c++)if(l=f[c])for(u in l)Object.prototype.hasOwnProperty.call(l,u)&&(t[u]=l[u]);return t}).call(p,p.fn=p[l]=n,{on:function(t,e){return t=t.split(o),this.map(function(n){(o[c=t[0]+(n.b$=n.b$||++r)]=o[c]||[]).push([e,t[1]]),n["add"+i](t[0],e)}),this},off:function(t,e){return t=t.split(o),l="remove"+i,this.map(function(n){if(f=o[t[0]+n.b$],c=f&&f.length)for(;u=f[--c];)e&&e!=u[0]||t[1]&&t[1]!=u[1]||(n[l](t[0],u[0]),f.splice(c,1));else t[1]||n[l](t[0],e)}),this},is:function(t){return c=this[0],(c.matches||c["webkit"+s]||c["moz"+s]||c["ms"+s]).call(c,t)}}),p}(window,document,Array.prototype,/\.(.+)/,0,"EventListener","MatchesSelector");
</script>
```
(Looks like Google Analytics embed)

Then use it anywhere on the web page:
```html
<script>
  $(function () {
    $('.my-selector').on('click', function () {
      alert('I need my balalaika');
    });
  });
</script>
```

The second kind of use is using it inside single script as local variable:
```js
(function (win, $) {
	// your code starts here
	$(function () {
		$('.my-selector').on('click', function () {
			alert('I need my balalaika');
		});
	});
  // your code ends here
})(window, function(t,e,n,o,r,i,s,c,u,f,l,p){"use strict";return p=function(t,e){return new p.i(t,e)},p.i=function(o,r){n.push.apply(this,o?o.nodeType||o==t?[o]:""+o===o?/</.test(o)?((c=e.createElement(r||"q")).innerHTML=o,c.children):(r&&p(r)[0]||e).querySelectorAll(o):/f/.test(typeof o)?/c/.test(e.readyState)?o():p(e).on("DOMContentLoaded",o):o:n)},p.i[l="prototype"]=(p.extend=function(t){for(f=arguments,c=1;c<f.length;c++)if(l=f[c])for(u in l)Object.prototype.hasOwnProperty.call(l,u)&&(t[u]=l[u]);return t}).call(p,p.fn=p[l]=n,{on:function(t,e){return t=t.split(o),this.map(function(n){(o[c=t[0]+(n.b$=n.b$||++r)]=o[c]||[]).push([e,t[1]]),n["add"+i](t[0],e)}),this},off:function(t,e){return t=t.split(o),l="remove"+i,this.map(function(n){if(f=o[t[0]+n.b$],c=f&&f.length)for(;u=f[--c];)e&&e!=u[0]||t[1]&&t[1]!=u[1]||(n[l](t[0],u[0]),f.splice(c,1));else t[1]||n[l](t[0],e)}),this},is:function(t){return c=this[0],(c.matches||c["webkit"+s]||c["moz"+s]||c["ms"+s]).call(c,t)}}),p}(window,document,Array.prototype,/\.(.+)/,0,"EventListener","MatchesSelector"));
```

### Which methods are provided?
Balalaika uses methods from ``Array.prototype``. It means Balalaika can use any method of native arrays.
```js
$('.my-selector').forEach(function (el) {
	console.log(el);
});
```

<ul>
			<li><a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/concat" target="_blank">concat</a></li>
			<li><a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/join" target="_blank">join</a></li>
			<li><a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/pop" target="_blank">pop</a></li>
			<li><a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/push" target="_blank">push</a></li>
			<li><a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/reverse" target="_blank">reverse</a></li>
			<li><a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/shift" target="_blank">shift</a></li>
			<li><a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/slice" target="_blank">slice</a></li>
			<li><a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/sort" target="_blank">sort</a></li>
			<li><a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/splice" target="_blank">splice</a></li>
			<li><a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/toString"  target="_blank">toString</a></li>
			<li><a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/unshift" target="_blank">unshift</a></li>
			<li><a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/every" target="_blank">every</a></li>
			<li><a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/filter" target="_blank">filter</a></li>
			<li><a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/forEach" target="_blank">forEach</a></li>
			<li><a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/indexOf">indexOf</a></li>
			<li><a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/lastIndexOf" target="_blank">lastIndexOf</a></li>
			<li><a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/map" target="_blank">map</a></li>
			<li><a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/some" target="_blank">some</a></li>
		</ul>

Besides, Balalaika has few additional methods such as:
#### ``on``
```js
$('.my-selector').on('click.namespace', function () {
	alert('I need my balalaika');
});
```
#### ``off``
```js
$('.my-selector').off('click.namespace');
```
#### ``is``
```js
$('.my-selector').on('click', function (evt) {
	if($(evt.target).is('.another-selector')) {
		alert('I need my balalaika');
	}
});
```
#### ``extend``
```js
var myObject = {a:1};
$.extend(myObject, {
	b: 2
});
```
#### DOM-ready feature
```js
$(function () {
	// Do something with DOM
});
```

### It provides very few functions, doesn't it?
Yep. The idea is if you need something, implement it! A lot of jQuery-like functions can be created easily. Use $.fn style to create additional methods:
```js
$.fn.hasClass = function (className) {
	return !!this[0] && this[0].classList.contains(className);
};
```
```js
$.fn.addClass = function (className) {
	this.forEach(function (item) {
		var classList = item.classList;
		classList.add.apply(classList, className.split(/\s/));
	});
	return this;
};
```
```js
$.fn.removeClass = function (className) {
	this.forEach(function (item) {
		var classList = item.classList;
		classList.remove.apply(classList, className.split(/\s/));
	});
	return this;
};
```
```js
$.fn.toggleClass = function (className, b) {
	this.forEach(function (item) {
		var classList = item.classList;
		if (typeof b !== 'boolean') {
			b = !classList.contains(className);
		}
		classList[b ? 'add' : 'remove'].apply(classList, className.split(/\s/));
	});
	return this;
};
```
And so on...

### More examples
#### Find elements inside another element
```js
var elements = $('.my-selector', el);
```

#### Parse HTML
```js
var elements = $('<div><span class="yeah"></span></div>');
```

#### Extended parsing function
Pay attention that the example above doesn't parse contextual elements such as ``td``, ``tr``, etc. But the function below does:
```js
$.parseHTML = function (html) {
	var node = document.createElement('div'),
		// wrapMap is taken from jQuery
		wrapMap = {
				option: [1, "<select multiple='multiple'>", "</select>"],
				legend: [1, "<fieldset>", "</fieldset>"],
				thead: [1, "<table>", "</table>"],
				tr: [2, "<table><tbody>", "</tbody></table>"],
				td: [3, "<table><tbody><tr>", "</tr></tbody></table>"],
				col: [2, "<table><tbody></tbody><colgroup>", "</colgroup></table>"],
				area: [1, "<map>", "</map>"],
				_: [0, "", ""]
		},
		wrapper,
		i;
	html = html.replace(/^\s+|\s+$/g, '');
	wrapMap.optgroup = wrapMap.option;
	wrapMap.tbody = wrapMap.tfoot = wrapMap.colgroup = wrapMap.caption = wrapMap.thead;
	wrapMap.th = wrapMap.td;
	wrapper = wrapMap[/<([\w:]+)/.exec(html)[1]] || wrapMap._;
	node.innerHTML = wrapper[1] + html + wrapper[2];
	i = wrapper[0];
	while (i--) node = node.children[0];
	return $(node.children);
};

var myElements = $.parseHTML('<tr><td></td></tr>');
```

#### Adding styles for elements
```js
$('.my-selector').forEach(function (el) {
	$.extend(el.style, {
		width: '30px',
		backgroundColor: 'red'
	});
});
```
#### Delegated events
```js
$('.my-selector').on('click', function (evt) {
	var node = evt.target;
	while (node !== this) {
		if ($(node).is('.delegated-selector')) break; // Handle it!
		node = node.parentNode;
	}
});
```
#### ``$.fn.parents`` plugin
```js
$.fn.parents = function (selector) {
	var collection = $();
	this.forEach(function (node) {
		var parent;
		while ((node = node.parentNode) && (node !== document)) {
			if (selector) {
				if ($(node).is(selector)) parent = node;
			} else parent = node;
			if (parent && !~collection.indexOf(parent)) collection.push(parent);
		}
	});

	return collection;
};
```
**Licensed under MIT License**
