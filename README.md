ten.js
======

A lightweight JavaScript/HTML5 library. Work began on December 10th, 2012.

## methods

### ten.each(object/array, function(key,value))
Iterates over an object or array, executing a function for each entry.
###### Note: the `key` and `value` names can be anything
>
```
var array=["foo","bar"];
ten.each(array, function(key,value) {
  element.append("<div>" + key + ": " + value + "</div>");
});
```
Will append to the element
```
0: foo
1: bar
```
>
The same applies to objects
```
var object={
  one:"foo",
  two:"bar"
}
ten.each(object,function(key,value) {
  element.append("<div>" + key + ": " + value + "</div>");
});
```
Will append to the element
```
one: foo
two: bar
```

-----
### ten.trim(string)
Strips all leading & trailing spaces, and converts multiple spaces to a single space.
>
```
var string="    foo        bar ";
string=ten.trim(string);
```
Variable `string` becomes  `foo bar`

-----
### .addClass(class)
Accepts a string or an array of strings. Adds the specified class(es) to the targeted element.
>
```
element.addClass("foo");
```
```
element.addClass("foo bar");
```
```
element.addClass(["foo", "bar"]);
```

-----
### .each(function(key,value))
Runs the specified function for each element selected.
###### Note: the `index` and `element` names can be anything
>
```
var foo=ten.find(".foo");
foo.each(function(index,element) {
  console.log(element.text());
});
```
Will log the text contents of each element with the class `foo`

-----
### .hasClass(string)
Checks if the targeted element has the specified class. Returns boolean.
>
```
if (element.hasClass("foo")) {
 // it has foo!
}
```

-----
### .removeClass(class)
Accepts a string or an array of strings. Removes the specified class(es) to the targeted element.
>
```
element.removeClass("foo");
```
```
element.removeClass("foo bar");
```
```
element.removeClass(["foo", "bar"]);
```

-----
### .text()
Returns the text content of an element, stripping any HTML.
>
```
<div id="foo">
  <ul>
    <li>foo</li>
    <li>bar</li>
  </ul>
</div>
```
```
ten.find("#foo").text();
```
Will return `foobar`

-----
### .toggle(class)
Accepts a string or an array of strings. Will toggle all of the classes provided.
>
```
element.toggle("foo");
```
```
element.toggle("foo bar");
```
```
element.toggle(["foo", "bar"]);
```
