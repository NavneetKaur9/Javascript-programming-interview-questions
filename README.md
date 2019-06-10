# Javascript-questions
```
(function() {
	var arrayNumb = [ 2, 8, 15, 16, 23, 42];
	arrayNumb.sort();
	console.log(arrayNumb); 
})();

output:
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

output: 
0
1
2
3
```
