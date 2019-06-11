# Javascript-questions
```js
(function() {
	var arrayNumb = [ 2, 8, 15, 16, 23, 42];
	arrayNumb.sort();
	console.log(arrayNumb); 
})();

Output:
[15, 16, 2, 23, 42, 8]
```
```js
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
```js
var a = 42, b="42"

console.log(a==b);
console.log(a===b);

Output:
true
false
```
```js
var x=500;
let y,z,p,q;
q=200;
if(true){
	x=y=z=p=q;
	console.log(q,x,y,z,p);
}

Output: 200 200 200 200 200
```
```js
var y=1;
if(function f(){}){
	y += typeof f;
}
console.log(y);

Output: 1undefined
```

```js
function foo(a, b){
	arguments[1] = 2;
	alert(b);
}
foo(1);

Output: undefined
```

```js
var cloths = ["Shirt", "Pant", "Tshirt"];
cloths.pop();

Output: "T-shirt"
```

```js
4+3+2+"1"+4

Output: 914
```

```js
var person = {name: 'Abhishek'};
person.salary = '10000$';
person['country'] = 'India';
console.log(Object.keys(person));

Output: ["name", "salary", "country"]
```

```js
function test(){
	return foo;
	foo = 10;
	function foo(){}
	var foo = '11';
}
console.log(typeof test());

Output: function
```
```js
var bar = true;
console.log(bar + 0);
console.log(bar + "xyz");
console.log(bar + true);
console.log(bar + false);

Output: 1 'truexyz'2 1
```
```js
Are the outputs of the following javascript code be the same:

for (let i = 1; i <= 5; i++){
	setTimeout( ()=> {console.log('func1',i);}, i*1000);
}
[1,2,3,4,5].forEach(i =>{ setTimeout( ()=> { console.log(i) }, i*1000 )})

Output: yes
```
```js
var obj1 = {
	prop1 : "DAH2"
};
var myFunc = function(){
	console.log("Hi there", this);
};
myFunc();
obj1.myMethod = myFunc;
obj1.myMethod();

Output:
Hi there undefined
Hi there {prop1: "DAH2", myMethod: ƒ}
```
```js
var a = 7;
function foo(){
	var a = 6;
	function bar(){
		var a = 8;
		alert(a);
	}
	bar();
	alert(a);
}
foo();
alert(a);

Output: 8,6,7
```
```js
var employeeId = '1234ade';
(function() {
	console.log(employeeId);
	var employeeId = '122345';
	(function(){
		var employeeId = 'abc1234';
	}());
}());

Output: Undefined
```
```js
var a = 3;
var obj = {
	a: 2,
	foo: {
		a: 1,
		bar: function(){
			return this.a;
		}
	}
}
var test = obj.foo.bar;
alert(test());
alert(obj.foo.bar());

Output: 3, 1
```
```js
function dummy(){
	return {
		test: 1
	}
}
console.log(typeof dummy());

Output: object
```
```js
var employeeId = 'aq123';
(function Employee(){
	try {
		throw 'foo123';
	} catch(employeeId){
		console.log(employeeId);
	}
	console.log(employeeId);
}());

Output: foo123 aq123
```
```js
2 + true > (true +false)

Output: true
```
```js
(function (){
	var greet = 'Hello world';
	var toGreet = [].filter.call(greet, function(element, index){
		return index > 5;
	});
	console.log(toGreet);
}());

Output: ["w", "o", "r", "l", "d"]
```
```js
let a = 1;

let b = setInterval(() => {
	console.log(a);
	a++;
	if(a >= 5){
		clearInterval(b);
	}
},1000);

Output: 1,2,3,4
```
```js
(function(){
	bar();
	
	function bar(){
		abc();
		console.log(typeof abc)
	}
	
	function abc(){
		console.log(typeof bar);
	}
}());

Output: function function
```
```js
var x = {foo: 1};
var output = (function(){
	delete x.foo;
	return x.foo;
}());

Output: undefined
```
```js
var x=3;
var y=4;

console.log(eval("x*y"));

Output: 12
```
```js
var test = 500;
var result = function(){
	console.log(test);
	var test =1000;
}
result();

Output: undefined
```
```js
console.log(Number("1") - 1 == 0);

Output: true
```

# built-in form validation

One of the features of HTML5 is the ability to validate most user data without relying on scripts. This is done by using validation attributes on form elements. Validation attributes allow you to specify rules for a form input, such as whether a value must be filled in; the minimum and maximum length of the data; whether the data needs to be a number, an email address, or something else; and a pattern that the data must match. If the entered data follows all of the specified rules, it is considered valid; if not, it is considered invalid.

When an element is valid, the following things are true:

* The element matches the `:valid` CSS pseudo-class, which lets you apply a specific style to valid elements.
* If the user tries to send the data, the browser will submit the form, provided there is nothing else stopping it from doing so (e.g., JavaScript).

When an element is invalid, the following things are true:

* The element matches the `:invalid` CSS pseudo-class, which lets you apply a specific style to invalid elements.
* If the user tries to send the data, the browser will block the form and display an error message.

> Q:Which of the following selectors select elements that do not match the selector **s**?
- [ ] :!(s)
- [ ] :nth-child(s)
- [x] :not(s)
- [ ] none of these

