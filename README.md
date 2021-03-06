# a.js
## Minimalistic Javascript library

This Javascript library is very minimalistic, meant to just manage pages or do some more intensive things with just 1-3 lines.

Example usage:

```js
$.ready(function() { // This is executed when the document is ready.
	// Get an element
	var elm = $("#id");
	
	// Set the contents of the entire body tag
	$("body")[0].set("<h1>It works!</h1>");
	
	// Set the color of an h1 tag
	$("h1")[0].style.color = "#f00";
	
	// Append content to the body tag
	$("body")[0].append("<p>Hello world!</p><p>I'm just adding some p tags.</p>");
	
	// Tell the user how many p tags there are
	alert("There are " + $("p").length + " p tags.");
	
	// Set the contents of the first p tag found in the document
	$("p")[0].set("Changed from script!");
	
	// Do an AJAX GET request
	$.get("test.txt", function(result) {
		alert("This is test.txt:\n\n" + result);
	});
	
	// Do an AJAX POST request
	$.post("post.php", "test=" + escape("This is a test!"), function(result) {
		alert("Response from server:\n\n" + result);
	});
});
```

If you include the animation libraries, you can do something like this to animate the width of a div (from 50px to 500px) smoothly:

```js
$("#someDiv").anim({
	style: "width",
	seconds: 1.0,
	interpolate: "inOutQuad", // from a.easing.js
}).px(50, 500);
```
