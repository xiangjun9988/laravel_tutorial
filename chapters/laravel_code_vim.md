> 2017.08.09 updated

在vim中，一般如果用ctags这个命令生成一个叫`ctags`索引文件后，就可以用`ctrl+]`来查看一些类或方法的源码，就是直接跳转到对应的源码中的定义之处。

但是如果要有效地查看php的源码，可以使用一个叫phpctags的软件来重新生成更好的ctags文件。

https://github.com/vim-php/phpctags

![](https://rails365.oss-cn-shenzhen.aliyuncs.com/uploads/photo/image/293/2017/2aee55c778514f0f9408c0857633925f.gif)

首先来安装一下。

``` bash
brew install phpctags
```

装好之后在php源码目录下执行：

```
phpctags -R
```

这样就会生成ctags文件了。

下次你使用`ctrl+]`来查看源码会发现更好用了。

完结。
