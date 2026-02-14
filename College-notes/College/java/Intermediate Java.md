This is the continuation of the basics of [[Basics]] sheet in the java documentation series.

[[Basics|Read java basics]]
### Methods
Methods are basically functions in python they are set of code which can be reused easily when called.

We have used methods earlier in our codes with or without knowing for example the in the string built-in function like [[Basics#^151a8f|length ,toLowerCase() etc.]] <- ==DO CHECKOUT==

### Creating custom method
method name is normally written in lower camel case eg: `helloWorld`

Syntax 
```java
returnType methodName(){
//code logic here
}
```

we should use static before returnType when declaring methods out of main class reason will be discussed afterwards.

### Parameters
- Allow passing input values to methods 
- Add flexibility
- Makes the method more reusable and useful
- Parameter goes inside the parenthesis after method name

### Logical operators
| Operator | Symbol |
| -------- | ------ |
| AND      | &&     |
| OR       | \|\|   |
| NOT      | !      |
### Conditions
- `if`
- `else`
- `else if`
### Synatax
```java
if (condition){
	 // code here
}else if(){
	// code here
}else{
	// code here
}
```

### Switch
Switch is similiar to if else condition but it can only check equality, conditions and boolean can be checked by if else statements only 

### Syntax
```java
switch (expression) {
    case value1:
        // code
        break;

    case value2:
        // code
        break;

    default:
        // code
}
```

## Loops

### for loop
```java
String[] names = {"hello","world","sample","sample1"}

for(String name:names){
	System.out.println(name);
}
```

```output
hello
world
sample
sample1
```

### while loop
- it checks condition first, if true then runs
- then check, and runs if true
- and this continues
so if the condition never get updated or become false the loop never stops 
### Syntax
basic:
```java
while (condition){
	//code here
}
```

```java
int counter = 1;
while (counter < 10){
	//code here
	counter +=1;
}
```

while loop is usefull when we don't have the idea of how much iteration is required for desired output.

