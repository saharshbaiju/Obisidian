must read doc for complete beginners others can use it just brush up things.

```
class hello{
	public static void main(String[] args){
	
	}
}
```

# Data types
#### String

| Type       | For                                 |
| ---------- | ----------------------------------- |
| long       | very large number up to quintillion |
| int        | up to two million                   |
| short      | up to 30,000                        |
| byte       | very small number -127 to 128       |
| ==double== | ==up to 16 decimal digit==          |
| float      | up to 7 decimal digits              |
| boolean    | true or false                       |
| char       | for single character                |
| String     | for collection of character         |

#### Facts
Strings must be inside `""` not `''` because `''` stores character but they are collection of characters and therefore it is not a primitive data type

- All comples datatypes is derived from the primitve data types and they stand as the core data types
### More about strings

^151a8f

strings come with some built in functionalities
- Number of character in string can be fetched using `String.length()

- Change case functions `Strings.toLowerCase()` and `Strings.toUpperCase()`

- String concatenation using `+`

- Declare now, assign later
	- for example you can just declare a string variable like `String hello;` and declare hello later as `hello = "hello xyz;
	
###  Some more important string methods

- `.contains("")`
	- Returns true or false by checking whether some string is present in the main string or not.

- `.charAt(index)` returns the character at a specified index.

- `.substring(start,end)` gives a part of string.
		`"java".substring(1,3); //returns "av"`

- `.equals(string to compare)` == may give undesired output for strings
### Array
#### Syntax
`int[] prices = {10,20,40};`
`Strings[] prices = {"hello","world"};`

==length of array is fixed on creation and cannot be changed==

- we can change value of specific index by following code
	- `prices[2]=95`
	length can be found by `.length()`
all elements in array should have same type


# Variable
Variables are recommended to be named in camel case
### Syntax
```
type variableName = value;
```
### Variable naming rules
- Must start with a letter
- Follow camel case
- Cannot contain space

Good-naming convention ->
```
 String welcomeMessage = "hello";
```

Bad-naming convention->
```
String welcome message = "hello";
```


### Arithmetic operators

| symbol         | purpose |
| -------------- | ------- |
| Addition       | +       |
| Increment      | ++      |
| Subtraction    | -       |
| Decrement      | --      |
| Multiplication | *       |
| Division       | /       |

[[Intermediate Java|next section java intermediate]]
