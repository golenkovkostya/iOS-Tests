ObjC. Syntax. Semantic.
==

###1 Question:

* True or False? You can use %@ to specify a dynamic property.
* False
* True

Answer: False

http://juice-health.ru/archive/39-ios-7/406-dinamicheskie-metody-dostupa

###2 Question:

What happens if you use fgets and do not give it a size smaller than the buffer?

* It will clip its size automatically
* It will overwrite the data past the size
* It will use the size of the object as its size
* None of these

Answer: It will overwrite the data past the size

http://www.tutorialspoint.com/c_standard_library/c_function_fgets.htm

###3 Question:
True or False? You can perform operator overloading in Objective-C.

* False
* True

Answer: False 

###4 Question:

If you do not declare a return type for a method definition, what is the default return type?

* NSString
* No return type
* id

Answer: id

###5 Question:

True or False? For an object to use constraints, it must have at least 3 constraint values.

* True
* False

Answer: False

###6 Question:

Assume ARC is enabled... What would be another way to write this: NSArray *array = [NSArray arrayWithObjects:@"One", @"Two", @"Three",nil];

NSArray *array = @[@"One", @"Two", @"Three"];
NSArray *array = @{@"One", @"Two", @"Three"};
NSArray *array = [@"One", @"Two",@"Three"];
NSArray *array = {@"One", @"Two",@"Three"};

Answer: NSArray *array = @[@"One", @"Two", @"Three"];

###7 Question:

What class supports the sharing of small amounts of data such as strings or dates to iCloud?

NSOperation
NSUbiquitousKeyValueStore
NSUrlConnection

Answer: NSUbiquitousKeyValueStore

###8 Question:

True or False? A method and a variable can have the same name in Objective-C.

False
True

Answer: True



