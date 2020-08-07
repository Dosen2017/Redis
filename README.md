# Redis

### 高性能的原因
1、纯内存访问，Redis将所有数据放在内存中，内存的响应时间大约为100纳秒，这时Redis达到每秒万级别访问的重要基础；

2、非阻塞I/O，Redis使用epoll作为I/O多路复用技术的实现，在加上Redis自身的事件处理模型将epoll中的链接、读写、关闭都转换为事件，不在网络I/O上浪费过多的时间；

3、单线程避免了线程切换和锁产生的消耗。

4、另外，数据结构也帮了不少忙，Redis全程使用hash结构，读取速度快，还有一些特殊的数据结构，对数据存储进行了优化，如压缩表，对短数据进行压缩存储，再如，跳表，使用有序的数据结构加快读取的速度。

### 常用命名：
1、info memory 查看内存使用情况 <br/>
2、info keyspace 查看各数据库（0-15）的使用情况<br/>
