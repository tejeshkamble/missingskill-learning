# **JAVASCRIPT**

### **History**
 company started netscape navigator first browser. from the concept netscape another language has been created right script. after that Microsoft came with own browser Internet Explorer. again due to compitition with Microsoft, netscape employee Brendon created another language Mocha. after that changed the name of Mocha to Javascript.in 1996 ECMA aquired and change name to ECMAScript (ES). ES 3.1 was rename as ES 5. In 2015 drawbacks of ES 5 has remove and came up with new version ES 6.

### **Facts about JavaScript** -
- In **Javascript** everything is an **Object**.
- Type of **null** always return an Object
- **+** operator  do the Addition and Concatination which is basically a tech debt in Javascript
- **===** Do a equility check and value check.
- Javascript have only single threaded operations

### **Why JavaScript ?**
Javascript is programming language that used both on the client-side and server side. It make us web pages interactive from both side. JavaScript provides interactivity to web pages in the browser.

### **Control Structure**  
- **if else** - Often used
- **for** - Abstraction
- **switch case** - Better ay available in javascript
- **while** - Normal use
- **do while** - Rarely use

### **Operators**  
- **Arithmetics**
	- +, -, *, /, %, ++, --, -=, *=, /=, ==
- **Logical**
    -  &&, ||, !
- **Bitwise**
    - |, &, ~
- **ternary**
   - **? :** ((a+b === 1) ? c : d)

### **Variables**
- Javascript variables are dynamic in nature.
- Javascript variables are containers.
- Javascript decides variable type at runtime.
- There are two types of variables
    1. Primitive
    2. Non-primitive
        1. **Primitive**  
	        - string
		    - number
		    - Boolean
		    - undefined
		    - Null
		    - Symbol (ES6)
	    2. **Non-Primitive**
		    - Object {}
		        ```js
                var obj = {key:"value"};
		        ```
		    - Array []
		        ```js
		        var arr = [2, 3, Null`, true, [], {}];
                ```
- In javascript everything is an object.
- In **ES6** **'const, let'** are introduced.

**var**  
- **var** has a functionl scope.
- In **var** we can Reassign values.
- In **var** we can redeclare values by using same name.
	```js
	// Example
	var a = 3;  //first assign
    var a = "Hello";    //second assign
    // It get Hoisted
	```

**let**  
- let has a lexical scope.
- In **let** we can reassign values.
- In let we cannot redeclare value by using same name.
    ```js
    let a = 3;
	let a = "Hello";    //Error
	// Doesn't get Hoisted
    ```
**const**  
- **const** has a lexical scope.
- In **const** we cannot reassign values for primitive type but we can do it for non-primitive datatype.
- In **const** we cannot be redeclare value.
- Doesn't get Hoisted

***facts*** : -  Addition operation happens when datatype are same. beacause we use + for concatination. we have to do external casting for string type.
- Ex.
    ```js
	var a = 12; //number
	var b = "10"; //string
	var f = a +b; //output = 1210
    ```
- But, in other arithmetic operation they automatically change string type to number or do internally casting
    ```js
	var f = a * b; //o/p = 120
    ```
- Any operation with undefined says NaN
    ```js
    undefined + undefined = NaN  // (not a number)
    ```
- Any operation with null says NaN
    ```js
    null / null = NaN
    ```
- **(0, Null, "", NaN, undefined)** are always falsy value.
- **"!! value"** always converted into boolean value.
- Any non-primitive addition is concatination (because firstly it will converted into string).
- **Arrays** are **objects** in Javascript.
- arr.length = last index + 1
- **"_"** is allowed in key but **"-"** is not allowed.

### **Scope**

**Functional Scope**
- In the fuction having its own working area known as fuctional scope.
- functional scope always start with function().
- Example
    ```js
	var a= 10; //Global scope
	function hello(){
		var a = 20;     //functional scope
		console.log(a);     //o/p = 20
	}
	console.log(a);  //o/p = 10
    ```
**Lexical scope**  
- If fuction having another fuction inside function and that insided function scope known as Lexical scope.
- Lexical scope start with any {}.
- Example
	 ```js
	function hello(){
		let a = 4;
		if(a){
		  let b = 9;    //lexical scope
		  let a = 9;     //lexical scope
		  console.log(a + b);   //o/p = 18
		}
	}
	```

### **Hoisting**
-  In javascript at a runtime, variables declarations are moving at the top but assigning value are not moving at top in scope, is called as Hoisting.
- Variables are always floating at top in javascript.
- Example
    ```js
	a = 10;
	console.log(a); //o/p = 10
	var a; //hoisting
    ```
***const and let cannot get hoisted.***
- Example
    ```js
	b = 20;
	a = 10;
	console.log(a, b);  //undefined
	let a;  //not hoisted
	const b;    //not hoisted
    ```
### **Call by Value and Call by Reference**
- **Call by Value**
    - In javascript value pass by itself, called as call by value or copy by value.
    - Primitive types are call by value. 
    - Example
        ```js
        function add(a , b){ //call by value
            var c = a + b;
            return c;
        }

        var a = 3;
        var b = 4;
        add(a , b); //pass by value
        console.log("Addition", c);
        ```
- **Call by Reference**
    - In javascript value having some location in memory and the reference is pointing to the value, is called as call by reference or copy by reference.
    - Non-primitive values are call by reference.
    - Example
        ```js
        var stack = {
            node: 1,
            php: 1,
            go: 1,
            es: [1,2,3,4,5]
        }

        var tech = stack;
        tech.go = 10; //value pass by reference
        console.log(stack);
    
        ```
### **Function**
- A set of statements that perform a specific task. 
- functions are reusable.
	```js
	//Syntax,
	function <fun_name>(){} //declaration
	<fun_name>(); //calling function
    ```
- Functions acts like variables
    - Container -
        - Just like variable in javascript function also acts as a container.
        - We can place data into the function.
    
    - Hoisted -
        - Example
            ```js
            function fn(){
                console.log("10");   
            }

            function outsidecall(){
                console.log("print outside");
                fn();   //print : print inside
                function fn(){ //hoisted
                    console.log("print inside");
                }
            }
            outsidecall();
            // 1st function call outside() it prints "print outside"
            // then  fn function called get excecuted and hoisted. it prints ""print inside"
            ```
    -  Scope (Local and Global) -
        ```js
        function fn() { //global
            console.log("10")
        }
        function outsidecall(){ //loca;
            console.log("print outside");
            fn();
            function fn(){
                console.log("print inside");
            }
        }
        outsidecall();
        ```
    - Object -
        - In javascript value is passing to the function and it will return a value.
        - Functions are first class objects in javascript.
        - Function having properties and methods just like object having it.
        - Functions can be override.
        - Function having 'this' keyword just like object.
    - Override -
        - Example
        ```js
        function fn(){
        console.log("print fn");
        }
        function fn(){	//override and print
            console.log("print fn2");
        }
        fn();
        ```

**Function first class citizen privilege**
- Acts as an object
- Assign to a variable
- Function can return from function
- Function pass as an parameter
- Function act as an prototype
- Function is a child of an Object or Derived from Object.

**Anonymous function**
- In function assignment function does not have a name. this function called as anonymous function.
- Example
    ```js
    var logicBoard = function(param){
	    console.log("logic board", param);
    }
    var board = "1386";
    logicBoard(board); //Ref to anonymous function
    ```
- If we cannot pass any parameter to parameterised function , function will take parameter as 'undefined'. because compiler take 'undefined' as default.

***fact*** -
- Cascading of function
    ```js
	fn()()()()();
	first ()() //called first inner function
	first ()()() //called second inner function
	first ()()()() //called third inner function
    ```

**Function pass as an parameter**
```js
const print = function(value){ //simple anonymous print function
		console.log("printing :", value);
}

const completeTask = function(param){ //taking function as a parameter
    var a = 10;
    var b = 20;
	const c = a * b;
	param && (typeof param === "function") && param(c); //validating true value, type and value
}
completetask(print); //passing function as a parameter
```

**Function returning function**
```js
	function add(a, b){ //simple addition function
	    const c = a + b;
	    return c;
	}

	function operate(operation){ //taking function as a parameter
	let localfn; //undefined

	if(operation && (typeof operation === "function")){ //validating function
	    localfn = operation;
	}
	else{
	    localfn = function(){}
	}
	return localfn; //returning function
	}

	const executefn = operate(add); //calling and passing function as a parameter

	console.log(typeof executefn, executefn); //checking datatype of executefn
```

### **High Order Function**
- Any function taking function as a parameter and/or function returning function, called as High order function.

### **Pure Function**  
- when passing parameter value return as it is called as pure function.
- we do not modify parameter in function.

### **IIFE** -
- IIFE Stands for **Immediately Invoked Function Expression**.
- It is also called as Self executing function expression.
- It is an Anonymous function.
- Defining and calling at a time.
- It only run once.
- Example,
	```js
	(function(){    //Anonymous function
		console.log("IIFE");
	})();   //calling function
	```
### **Inline Function**
- Function as a parameter and all expression of function inline and always a anonymous function.
- Example,
    ```js
	function hello(value){
		//expression
	}(function(value){ //Inline function
		//expression
	});
    ```
### **Arrow Function**
- In Function assignment and expression insted of using **'function'** keyword we can use arrow.
- Arrow function cannot get hoisted, because it is used for only assignment.
- Only declaration of function get hoisted not a assignment.
- In ES 6 we do not have function declaration, only function assignment.
- Example,
    ```js
		// simple function -
		var b = function(){ //assignment to function
		}

		// arrow function -
		var b = () => { //assignment to function
		}

		// arrow function using single param
		arrow function -
		var b = param => {
		}

		// arrow function using multiple param
		arrow function -
		var b = (param, a)=> {
		}
	```

### **Object Prototype** -
- Number
- Boolean //no use of new keyword while creating object of boolean type
- String
- Object
- Array
- Math
- Date
- Regex
- function


- Instead of using **'for' loop** use **'forEach()'** method.

**Array Methods**
- **push** - add item at end
- **pop** - remove item from end
- **forEach** - acts as a for loop
- **map** - map the item in array
- **filter** - filter element from array
- **indexOf** - mapping by value and return index
- **includes** - returns true or false
- **concat** - return concated array
- **join** - return array into string

**Object Methods**
- **toString** - Return string
- **valueOf** - Return primitive value of object

**String Methods**
- **toUpperCase** - convert string into uppercase letters
- **toLowerCase** - convert string into lowercase letters
- **split** - separates value of string and return array
- **join** - join all array elements and return string
- **replace** - replace the value. having two parameters first is old element and second is new element.
- **trim** - remove space from both the edges.
- **substring** - taking substring from string or array.


### **JSON** 
    - JSON stands for Javascript object notation.
    - It is starts with braces "{}".
    - We use JSON object to transfer data from one application to another application.
    - Just like array it contains elements with key value pair.
    - Data into JSON always with double Qoute " ".
    - Example
```js
            const a = {
            name : "AB devilliers",
            country : "South Africa"
        }
        const jsonobj = JSON.stringify(a);
        const obj = JSON.parse(jsonobj);
        console.log(jsonobj);
```