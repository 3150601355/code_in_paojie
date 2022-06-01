# code_in_paojie

把代码排版为炮姐（御坂美琴）的样子，能编译运行，确切的说能唱歌。

```pwsh
cmake -S . -B build
cmake --build build --config MinSizeRel
```

测试环境：

* ~~Windows 7 + MSVC~~
* Windows 10 + MSVC
* Windows 10 + Clang
    > 目前Clang只支持 UTF-8，因此中文会乱码。
* Windows 10 + MinGW

    ```bash
    gcc -flto -Os -DNDEBUG -DUNICODE -D_UNICODE -finput-charset=UTF-8 -fextended-identifiers -fexec-charset=GBK railgun.c -o railgun -lvfw32
    ```

C语言代码，无基础慎用，不提供技术支持。

效果：https://www.bilibili.com/video/BV1N54y1o7m9
