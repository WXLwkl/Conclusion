## Conclusion
>自己的总结

###iOS相关知识 链接

- [IOS ARC内存管理总结](http://www.tekuba.net/program/346/)
- [Block在ARC/非ARC下的使用总结](http://www.tekuba.net/program/349/)
- [IOS开发ARC内存管理技术要点](http://www.cocoachina.com/ios/20150206/11121.html)
- [IOS ARC内存管理,提高效率避免内存泄露](http://wormlxd.blog.163.com/blog/static/9749032220130452722793/)
- [IOS多线程](http://blog.csdn.net/shenjie12345678/article/details/44152605)
- [导航栏控制器和标签栏控制器(UINavigationController和UITabBarController)混用](http://www.it165.net/pro/html/201501/31556.html)
- [IOS代码实践总结](http://www.cocoachina.com/ios/20150923/13531.html)
- [IOS开发多线程篇—GCD的常见用法](http://www.cnblogs.com/wendingding/p/3807716.html)
- [Adopting Modern Objective-C](https://developer.apple.com/library/ios/releasenotes/ObjectiveC/ModernizationObjC/AdoptingModernObjective-C/AdoptingModernObjective-C.html)
- [NSRunLoop和线程安全](http://blog.cnbluebox.com/blog/2014/07/01/cocoashen-ru-xue-xi-nsoperationqueuehe-nsoperationyuan-li-he-shi-yong/)
- [UINavigationController+UITabBarController 实现导航+标签-iPhone成长之路](http://blog.sina.com.cn/s/blog_7b9d64af01018jch.html)
- [CAAnimation动画/CAAnimation Group动画分隐式动画和显示动画](http://www.cnblogs.com/pengyingh/articles/2474131.html)
- [iphone开发工具常用方法](http://my.oschina.net/rotiwen/blog/93518)
- [Core Data 入门](http://blog.csdn.net/q199109106q/article/details/8563438/)
- [iOS开发 NSRunLoop的进一步理解](http://blog.sina.com.cn/s/blog_b4c2e34b0101k9aa.html)
- [iOS开发的一些奇谲巧技](http://blog.csdn.net/yqmfly/article/details/42261835)
- [iOS开发系列--音频播放、录音、视频播放、拍照、视频录制](http://www.cnblogs.com/kenshincui/p/4186022.html#uiImagePickerController)
- [ijkplayerDemo直播](http://www.code4app.com/forum.php?mod=viewthread&tid=8941&fromuid=792903)


tableViewCell加载

	static NSString *identifier = @"addCell";
    <#CustomCellName#> *cell = [tableView dequeueReusableCellWithIdentifier:identifier];
    if (!cell) {
        
        cell = [[[NSBundle mainBundle] loadNibNamed:<#cellXIBName#> owner:nil options:nil] firstObject];
        
    }
	//或者
	
	[_tableView registerNib:[UINib nibWithNibName:@"PicNewsCell" bundle:nil] forCellReuseIdentifier:@"picNews"];
	
	PicNewsCell *cell = [tableView dequeueReusableCellWithIdentifier:@"picNews"];