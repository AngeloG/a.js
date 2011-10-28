# a.js
## Minimalistic Javascript library

This Javascript library is very minimalistic, meant to just manage pages or do some more intensive things with just 1-3 lines.

Example usage:

```js
$ = _$; // a.js defaults to _$, to not interfere with other libraries. This is an alias.
$(function() { // This is executed when the document is ready.
	// Get an element
	var elm = $("#id");
	
	// Set the contents of the entire body tag
	$("body").set("<h1>It works!</h1>");
	
	// Set the color of an h1 tag
	$("h1").style.color = "#f00";
	
	// Append content to the body tag
	$("body").append("<p>Hello world!</p><p>I'm just adding some P tags.</p>");
	
	// Tell the user how many p tags there are
	alert("There are " + $("p").length + " p tags.");
	
	// Set the contents of the first p tag found in the document
	$("p[0]").set("Changed from script!");
	
	// Do an AJAX GET request
	$("GET", "test.txt", function(result) {
		alert("This is test.txt:\n\n" + result);
	});
	
	// Do an AJAX POST request
	$("POST", "post.php", "test=" + escape("This is a test!"), function(result) {
		alert("Response from servers:\n\n" + result);
	});
});
```