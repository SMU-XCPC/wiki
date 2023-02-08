# 如何 debug

群里的提问，应该是针对某条语句的提问，或是针对本文的提问，而不是一大段代码问哪里错了。

这里只讲对于 C++ 单文件程序的 debug。这里假设已经有了能使程序运行结果错误的输入，而不仅是在OJ上提交没有通过。
环境见配置环境。

阅读[常见编程错误列表](https://icpc.xidian.wiki/cce)

## 输出调试

要保证对自己编写的程序理解知道在该输入下正常程序应该如何运行。
在此前提下觉得哪儿可能有问题，就把对应的结果输出一下，然后编译运行，例如。

```cpp
for(int i=1;i<=n;i++){
	int ret=work(i);
	//...
}
```

如果结果出错，可以写

```cpp
for(int i=1;i<=n;i++){
	fprintf(stderr, "work %d\n", i);
	int ret=work(i);
	fprintf(stderr, "work %d result=ret\n", i, ret);
	//...
}
```

> 这里使用 `fprintf(stderr, ...)` 或者 `cerr` 是因为错误流是按行缓冲的，而 `printf` 或者 `stdout` 是标准输出，
不保证缓冲多少，所以有可能执行了，但是不能立刻看到结果，当然也可以 `fflush(stdout)` 或者 `cout.flush()` 来立即输出

通过打印 `ret` 和在草纸上演算的正确结果比较，即可得知在哪次 `work` 出了问题，再对 `work` 进行 debug，
类似的如果是分支错误，则把每次分支如何跳转的打印出来，再进行比较即可。

虽然按照上述方法一定能找到程序错误的所在，
但对于新手来讲，对一段很短的代码定位错误可能也会比较慢，主要原因是还没有形成良好的编程思维，对自己写的语句的作用可能很快就忘记了。
多加练习，尽量自己调试，即可克服。

经过以上努力，解决了问题或是至少把问题从我的代码哪里有问题转变为，为什么这条语句是如此运行的。

使用输出调试时，建议不打开优化（即，使用 `-O0` 优化级别）。
这是因为如果代码中存在未定义行为，优化可能导致输出与直观预期不符。

其他

`assert(bool)` ，如果传的是 false 则会 RE，用途：  
假如按照正常运行结果应满足 `n<m`，则在程序添加 `assert(n<m);`

注意有的 OJ 上 `assert` 失败不会正常触发 RE，
如果对 OJ 不了解的话不建议用于在 OJ 上测代码。

调试宏

```cpp
#include<iostream>
void debug_out(){std::cerr<<std::endl;}
template <typename Head,typename... Tail>
void debug_out(Head H,Tail... T){
  std::cerr<<" "<<H;//to_string(H);
  debug_out(T...);
}
#ifdef LOCAL
#define dbg(...) std::cerr<<"L"<<__LINE__<<" ["<<#__VA_ARGS__<<"]:",debug_out(__VA_ARGS__)
#define debug(...) std::cerr<<__VA_ARGS__//fprintf(stderr, __VA_ARGS__)
#else
#define dbg(...) 0
#define debug(...) 0
#endif
```

在本地编译选项里加入 `-DLOCAL`，提交时可以不用注释调试输出，用法

```cpp
dbg(n,m); //输出n,m，例如当前行为12,n=3,m=4则会输出: L12 [n,m]: 3 4
```

如果要用循环输出很多调试信息，建议将整个循环进行条件编译，例如

```cpp
//输出 a[1..n]
for(int i=1;i<=n;++i) debug(a[i]<<" \n"[i==n]);

#ifdef LOCAL
for(int i=1;i<=n;++i) std::cerr<<a[i]<<" \n"[i==n];
#endif
```

这是因为编译器不一定能够优化空循环，特别是在使用 C++ 容器时。

## I/O 重定向

如果输出的信息很多，以至于屏幕放不下，可以重定向输出。在 Linux 或者 MinGW
的 Bash 中：

```bash
./a.out 2>err.txt >out.txt
```

则 `out.txt` 文件会包含你程序的正常输出，`err.txt` 文件会包含你用
`debug` 宏输出的东西。你也可以只使用 `2>` 或只使用 `>`。

如果你想把正常输出和用 `debug` 宏输出的东西放在一起，使用

```bash
./a.out &> out.txt
```

如果输入很大或者懒得每次敲相同的输入数据，也可以重定向输入：

```bash
./a.out < in.txt
```

不知道 Windows 的 `cmd` 里面怎么重定向。

不建议使用 `freopen` 进行重定向，因为不够灵活。
如果一定要使用的话也要用 `#ifdef LOCAL` 进行保护，
不要以为自己交代码的时候肯定能记得删。

## 调试工具

阅读 [CP101](https://acm.xidian.edu.cn/assets/程序调试.pdf) 调试技巧部分

注意其中 `-fsanitize=undefined` 等仅在 linux 环境下适用
