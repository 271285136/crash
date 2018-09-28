# crash
移动端常见crash问题解决

iOS
*** -[__NSPlaceholderDictionary initWithObjects:forKeys:count:]: attempt to insert nil object from objects[2]
问题详细描述:
NSString* valueC = nil;
NSDictionary* dic = @{@"a":@(1), @"b":@"b", @"c":valueC};

字典dic, 第三个key(c)设置了nil值.
如果第一个值为空那么错误就是: 
*** -[__NSPlaceholderDictionary initWithObjects:forKeys:count:]: attempt to insert nil object from objects[0]
以此类推
