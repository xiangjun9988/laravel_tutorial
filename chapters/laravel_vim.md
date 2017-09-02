> 2017.08.09 修改，增加动图和修改文字

这篇文章会来讲下开发工具，如果你的开发工具不是vim，可以略过，这篇文章只适应于使用vim开发工具的同学。

如果你使用vim开发ruby on rails项目，可能会使用过[vim-rails](https://github.com/tpope/vim-rails)这个插件。

这个插件很好用，让你可以轻易地切换代码，查看特定的代码，比如我要查看各种`users`这个`controller`，我只需要键入`:Econtroller users`，真的很方便。

使用vim开发`laravel`项目，也有类似这样的工具。

它就是 **vim-laravel**。

#### 1. vim-laravel

https://github.com/noahfrederick/vim-laravel

安装起来很简单，使用你的vim插件管理器，来安装下面四个插件。

```
Plug 'tpope/vim-dispatch'
Plug 'tpope/vim-projectionist'
Plug 'noahfrederick/vim-composer'
Plug 'noahfrederick/vim-laravel'
```

比如我是使用Neobundle来管理插件的，那么：

```
NeoBundle 'tpope/vim-dispatch'
NeoBundle 'tpope/vim-projectionist'
NeoBundle 'noahfrederick/vim-composer'
NeoBundle 'noahfrederick/vim-laravel'
```

这个工具超级好用，比如要找到一个view，就可以输入`:Eview `（中间有个空格），然后加一个tab键，你会看到各种view，选择一个你要的，或直接键入，比如`:Eview welcome`，就会自动跳到`resources/view/welcome.blade.php`文件中。

比如使用`:Eroutes `可以跳到各个路由去。

下面是截图：

![](https://rails365.oss-cn-shenzhen.aliyuncs.com/uploads/photo/image/288/2017/2da03dec07d422c5910332cbb8d48e16.gif)

具体的命令可以查看vim-laravel的readme文档。

#### 2. vim-blade

https://github.com/jwalton512/vim-blade

这个插件是给blade的view文件加上语法格式。这样看起来就舒服多了。

安装方法跟上面的一样：

```
NeoBundle 'jwalton512/vim-blade'
```

![](https://rails365.oss-cn-shenzhen.aliyuncs.com/uploads/photo/image/274/2017/88c84aa725a23c38c79f80f66ee8756d.png)

完结。
