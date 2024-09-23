# vscode 多语言刷题环境

## 支持语言

_支持语言`C` `C++` `java` `python` `C#` `Ruby` `Rust` `Go`单文件运行及调试_</br>

支持自动根据文件扩展名切换调试配置文件,依赖扩展(auto debug)

*对于`C` `C++` `C#`使用 VisualStudio 的 `C/C++(msvc)` 和 `C#(dotnet)` 编译选项时须将 `<vs目录>\Common7\Tools` 添加到 `path` 或将 `task.json` 中的 `vsdevcmd` 替换为 `<vs目录>\Common7\Tools\vsdevcmd` ,若不使用可将 `launch.json` 中的 `map` 项下的键 `C` 的值改为`C(gcc)` 或 `C(clang)` `C++`的值改为 `C++(g++)` 或 `C++(clang++)` `C#`的值改为`C#(mono)` 并安装相应编译器并添加到 `path`*

*对于`java`可以切换 `task.json` 中 `map`下 `java` 键的值 `java` 或者 `Java(compile)`以切换运行前是否编译*

*对于`python`可以切换 `task.json` 中 `map`下 `python` 键的值 `python` 或者 `python(pypy)`以切换运行的python解释器*

## 支持输入输出重定向

所有语言的输入重定向至`/test/in.txt`</br>

所有语言的输出重定向至`/test/out.txt`</br>

*如不需要可将 `launch.json` 中的所有 `args` 条目注释掉*

## 支持自动本地 git 上传

每次运行时提交至本地 git存储库</br>

_自动根据`/test/out.txt` 及 `/test/correct.txt`的一致性比对并打上标记_</br>

*如不需要可以把`launch.json`中的所有`postdebugtask`注释掉*

*使用时需先删除.gitignore后面的文件名(避免把不需要同步的文件同步进去)然后运行git init初始化存储库*
