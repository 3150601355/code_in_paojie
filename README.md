# code_in_paojie
把代码排版为炮姐（御坂美琴）的样子，能编译运行，确切的说能唱歌。

运行环境：
Windows 10 + VisualStudio 2017。

C语言代码，结合Win32编程技术，【无基础慎用，不提供技术支持】。

效果：https://www.bilibili.com/video/BV1N54y1o7m9/

**补：**

出现4996号错误，可以这样处理：VS2017-项目-属性-C/C++-命令行，在【其它】选项中加入 /D_CRT_SECURE_NO_WARNINGS

## release

包含有一个打包好的 paojie.exe 文件，可以直接运行，注意，运行后控制台会无法关闭，只有等执行完毕或者在任务栏右键关闭。