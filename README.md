# mycalc
一个计算器，支持加减乘除四则运算。
简单的记录一下造轮子的过程
## 安装
首先拷贝仓库
`git clone https://github.com/ChordXD/mycalc.git`

### windows
1. 确保gcc编译器已经正确安装
2. 确保已经安装bison与flex.
3. 依次在下载的仓库中执行
`bison -yacc -dv mycalc.y`
`flex mycalc.l`
`gcc -o mycalc y.tab.c lex.yy.c`
4. 最后启动可执行文件mycalc即可。

### linux
1. 确保gcc环境正确配置。
2. 依次在下载的仓库中执行:
`sudo apt-get install flex bison`
`bison -yacc -dv mycalc.y`
`flex mycalc.l`
`cc -o mycalc y.tab.c lex.yy.c`
3. `./mycalc`即可运行

## 使用方法
+ 支持四则运算即 +、-、×、\ 四种运算符的混合运算。
+ 请在一行之内输入表达式。
+ 精度在double范围之内
+ 除了数字与上述四中运算符以外，其他的均为非法字符。
+ 不支持非法表达式。


