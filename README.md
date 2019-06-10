# Javascript-questions
```
(function() {
	var arrayNumb = [ 2, 8, 15, 16, 23, 42];
	arrayNumb.sort();
	console.log(arrayNumb); 
})();

Output:
[15, 16, 2, 23, 42, 8]
```
```
var arr = [10, 32, 65, 2];
for (var i=0; i < arr.length; i++){
	setTimeout(function(j){
		return function(){
			console.log(j); 
		};
	}(i),3000);
}

Output: 
0
1
2
3
```
```
var a = 42, b="42"

console.log(a==b);
console.log(a===b);

Output:
true
false
```
```

```




# built-in form validation

One of the features of HTML5 is the ability to validate most user data without relying on scripts. This is done by using validation attributes on form elements. Validation attributes allow you to specify rules for a form input, such as whether a value must be filled in; the minimum and maximum length of the data; whether the data needs to be a number, an email address, or something else; and a pattern that the data must match. If the entered data follows all of the specified rules, it is considered valid; if not, it is considered invalid.

When an element is valid, the following things are true:

* The element matches the :valid CSS pseudo-class, which lets you apply a specific style to valid elements.
* If the user tries to send the data, the browser will submit the form, provided there is nothing else stopping it from doing so (e.g., JavaScript).

When an element is invalid, the following things are true:

* The element matches the :invalid CSS pseudo-class, which lets you apply a specific style to invalid elements.
* If the user tries to send the data, the browser will block the form and display an error message.
