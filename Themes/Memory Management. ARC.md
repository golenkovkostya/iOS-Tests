Memory Management
==

###1 Question:
Which of these property declaration attributes does not specify setter semantics?

* assign
* copy
* nonatomic
* strong
* weak

Answer: nonatomic

###2 Question:
What's the difference between "strong" and "retain" keywords ?

* "retain" can only be used when ARC is disabled
* Strong holds references longer than retain does.
* They are synonyms

Answer: They are synonyms

###3 Question:
Which method, if defined, is guaranteed to be called once -- and only once -- when a class is first referenced?

* + (Class) alloc;
* + (id) alloc;
* + (id) init;
* + (void) init;
* + (void) initialize;

Answer: + (void) initialize;

###4 Question:
What can you say about the code: NSString * str = [NSString stringWithFormat:@""]; [str release];

* It is correct, everything will work fine
* It will cause a SIGSEGV at [str release];
* It will cause the string to be released twice with undefined consequences when the surrounding autorelease pool is emptied
* None of these
* it will cause a SIGABRT when the enclosing method ends

Answer: It will cause the string to be released twice with undefined consequences when the surrounding autorelease pool is emptied

###5 Question:
What does the following code do, assume ARC is enabled? 
NSArray *myArray; 
for (int i = 0; i < 10; i++)
{ @autoreleasepool { myArray = [[NSArray alloc]init]; } }

* For each iteration of the loop a new array is allocated and released.
* For each iteration of the loop a new array is allocated and will be released at the end of the loop.
* For each iteration of the loop a new array is allocated and will leak memory.
* For each iteration of the loop a new array is allocated only.

Answer: For each iteration of the loop a new array is allocated and released.

###5 Question:
What is the minimum iOS version you can support and still have Automatic Reference Counting?

* iOS 3
* iOS 4
* iOS 5
* iOS 6

Answer: iOS 4












