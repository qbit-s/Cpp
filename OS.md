### 进程和线程的区别
+ 资源：进程是资源分配的基本单位，线程是调度的基本单位
+ 开销：进程的开销比线程大
+ 关系：一个进程内可以有多个线程
+ 调度：同一进程内的不同线程的切换不会引起进程切换，不同进程内线程的切换会引起进程的切换
+ 通信：线程可以读写同一进程内的数据，进程通信需要IPC

### 进程调度
#### 批处理系统
+ 先来先服务FCFS
+ 短作业优先SJF：可能会造成长作业饿死
+ 最短剩余时间优先SRTN
#### 交互系统
+ 时间片轮转FCFS合适的时间片
+ 优先级调度
+ 多级反馈队列：同一队列按FCFS,不同队列优先级和时间片都不同
  可以将这种调度算法看成是时间片轮转调度算法和优先级调度算法的结合