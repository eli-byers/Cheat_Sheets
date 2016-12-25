# Python errors and where to find them



###Table of Contence
* [Vanila Python](#vanila-python)
	* [Syntax Error](#syntax-error)
	* [Indentation Error](#indentation-error)
	* [Key Error](#key-error)
	* [Attribute Error](#attribute-error) 
* [Flask](#flask)
* [Django](#django)

## Vanila Python
Some errors can be easily seen in your python IDE by running code after the ```>>>```. Activate your IDE by entering ```python``` in your terminal.

-----------------------
### Syntax Error

* You are missing or have an extranious character somewhere. Most often it is a missing colon after an if statement or loop. Test often to catch these errors quickly.
* See it happen: ```>>> for x in range(10)```

```
# code looking something like this
for x in range(10)
	print x 
# error you get
SyntaxError: invalid syntax
```

### Indentation Error
* You either forgot to indent some code, or you indented a line that should not be indented. This often happend when the code in a function declaration or for loop is not indented. 

```
# code looking something like this
def myFunc():
print "in myFunc"
return True

# error you get
IndentationError: expected an indented block
```
```
# code looking something like this
def myFunc():
	print "in myFunc"
		return True

# error you get
IndentationError: unexpected indent
```

### Key Error
* You are trying to access a value in a dictionary by a key that doesn't exist. To avoid this error, you can validate that there is a specific key before trying to access it.
* See it happen: ``` >>> {}['someKey'] ```

```
# code looking something like this
someVar = myDictionary['someKey']

# error you get
KeyError: 'someKey'
```
##### Solution:

```
# validate the key exists
if 'someKey' in myDictionary:
	someVar = myDictionary['someKey']
# handel error appropriately
else:
	someVar = 0
```

### Attribute Error
* You are assuming some variable is an object when it is actually some other type. This often happens when a function returns ```None``` do to the absence of a return statement but you are expecting an object.
* See it happen: ``` >>> None.someAttr ```

```
# code looking something like this
assumedObject = myFunction()
someVar = assumedObject.someAttr
# error you get
AttributeError: 'NoneType' object has no attribute 'someAttr'
```
##### Solution:
```
# validate variable is an object
if isinstance(assumedObject, dict):
	someVar = assumedObject.someAttr
# handel error appropriately
else:
	someVar = 0
```
# validate

## Flask

## Django