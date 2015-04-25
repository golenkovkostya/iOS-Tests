XCode. Instruments.
==

###1 Question:
What is a proper format for calling an asynchronous function?

[NSOperationDispatchAsync dispatch_asyncWithBlock: ^{
// code
}];
[dispatch_async(dispatch_get_global_queue(DISPATCH_QUEUE_PRIORITY_BACKGROUND, 0),
// code
];
[dispatch_async(dispatch_get_global_queue(DISPATCH_QUEUE_PRIORITY_BACKGROUND, 0), ^{
// code
})];
dispatch_async(dispatch_get_global_queue(DISPATCH_QUEUE_PRIORITY_BACKGROUND, 0), ^{
// code
});

Answer: dispatch_async(dispatch_get_global_queue(DISPATCH_QUEUE_PRIORITY_BACKGROUND, 0), ^{
// code
});

###2 Question:
What class will allow you to use one or more blocks concurrently?

NSBlock
NSBlockOperation
NSConcurrency
NSConcurrentBlock

Answer: NSBlockOperation


###3 Question:
The proper typedef syntax for an Objective-C block that takes an NSArray and returns an NSString is

typedef NSArray *(^aBlock)(NSString *);
typedef NSString *(^aBlock)(NSArray *);
typedef aBlock^ = (NSString *)(NSArray *);
typedef void(^aBlock)(void);

Answer: typedef NSString *(^aBlock)(NSArray *);

