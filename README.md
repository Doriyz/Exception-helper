# Guide-for-debug

由于既有实验软配置的异常处理给的是编译好的字节码，编译过程没有启用支持调试的功能，因此直接拿到的代码只能使用打印作为调试的方式（而这往往让人十分痛苦）。

如果你需要使用本仓库提供的`lib`进行debug，你需要这么做：

+ 1.下载本仓库的lib
  + 方法一：逐个下载lib目录下的所有java文件；
  + 方法二：clone整个仓库，将`lib`目录转移到自己的项目中。推荐使用这个方法比较省力。

+ 2.使用正确的的项目位置放置`lib`

  整个项目的文件结构应该是这样的：

  ---bin

  ---doc

  ---lib （这里！）

  ---ref

  ---src

  ---testcase

  ---*.bat

+ 3.最后一步：在`src/parser/Calculator.java`中添加`main`函数，才能正常调试。

+ 4.之后如果要使用`run.bat`或者`test_simple.bat`运行程序，记得把上一步添加的`main`函数注释掉。

+ 5.如果对你有帮助的话可以给我STAR ！

