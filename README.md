# Windows文本命令行执行工具


Windows下的命令行执行工具，能够读取文本内的命令交给系统执行，因为控制台窗口不能直接传特定编码的参数，所以才想写这么一个小工具。


***


## 使用方法


打开main.exe然后会提示输入文件名。我们输入对应文件名程序就会读取文件的内容交给命令行处理。文件名可以是相对路径也可以是绝对路径。


文本可以是任意编码的，能否执行成功不确定。

test.txt 文件内容如下
```cmd
echo test

```

放到跟main.exe同一个目录下，然后在程序内输入test.txt然后按回车键。
执行结果如下：

```txt
您输入的文件名test.txt
成功打开文件：test.txt
执行成功 echo test test
```

功能可以说是很鸡肋了，只不过我是要用Openssl生成自签名证书，然后想要在证书内输入一些中文，要求就是使用UTF8文本，我在命令行内又无法输入，所以才写这个小工具把文件转成UTF8格式的然后再执行就可以了。

