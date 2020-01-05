### 真的是单进程 ?

php 不像java，可以多进程同时执行，是单进程执行的。如果程序单进程运行，就局限资源的使用，怎么想都觉得有点不合理。js虽然也是单进程执行，但是可以异步回调，也变相实现了多线程执行。
直到接触了workerman，才知道一切都是too young，too simple。 php是单进程执行，但是可以通过子进程，实现多线程编程。这点，跟java很像的，也是一个主进程，然后自动管理子进程。


### 打开子进程
- proc_open(cmd) —— workerman中使用，非常巧妙
- 安装两个扩展 pcntl和 posix —— 参考 https://www.cnblogs.com/zhenbianshu/p/5676822.html







