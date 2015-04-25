Runtime.
==

###1 Question:
What is the last chance for an object to handle a message?

+instancesRespondToSelector:
+resolveInstanceMethod:
-forwardInvocation:
-forwardingTargetForSelector:
-respondsToSelector:

Answer: -forwardInvocation:


https://developer.apple.com/library/ios/documentation/Cocoa/Conceptual/ObjCRuntimeGuide/Articles/ocrtForwarding.html
http://www.informit.com/articles/article.aspx?p=1765122&seqNum=13
http://habrahabr.ru/post/235041/

`Data forwarding` - переадресация данных.

`Proxy pattern` - "Заместитель"
The proxy design pattern allows you to provide an interface to other objects by creating a wrapper class as the proxy. The wrapper class, which is the proxy, can add additional functionality to the object of interest without changing the object's code.

```objc
//Traditional forwarding method
- (BOOL)respondsToSelector:(SEL)aSelector
{
    if ( [super respondsToSelector:aSelector] )
        return YES;

    else {
        /* Here, test whether the aSelector message can     *
        * be forwarded to another object and whether that  *
        * object can respond to it. Return YES if it can.  */
    }
    return NO;
}
```

```objc
- (id)negotiate
{
    if ( [someOtherObject respondsTo:@selector(negotiate)] )
        return [someOtherObject negotiate];
    return self;
}

//ForwardingInvocation method
- (void)forwardInvocation:(NSInvocation *)anInvocation
{
    if ([someOtherObject respondsToSelector:
        [anInvocation selector]])
        [anInvocation invokeWithTarget:someOtherObject];
    else
        [super forwardInvocation:anInvocation];
}
```

###2 Question:

What happens at runtime with the following: NSObject* object = nil; NSObject* object2 = [object copy]; NSLog(@"%@", object2);

Application continues, but issues "cannot access nil object reference" warning
Application crashes with "SIGABRT: object has been derferenced" error
Log prints "(null)" and continues as usual.
object2 is instantiated as an NSObject with nil values

Answer: Log prints "(null)" and continues as usual.






