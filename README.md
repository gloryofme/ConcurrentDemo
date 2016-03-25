# ConcurrentDemo
并发包的例子
#合理配置线程池
#分析的角度有：
#任务性质：CPU密集型任务、IO密集型任务和混合型任务
#任务的优先级：高、中、低
#任务执行时间：长、中、短
#任务性质不同的任务，可以通过使用不同规模的线程池分开处理
#CPU密集型的任务应该尽量少的配置线程数，一般可以配置成Ncpu+1个线程，IO密集型的任务由于并不是一直在执行任务，则应该尽配置尽可能多的线程，
#Ncpu可以通过Runtime.getRuntime().availableProcessors()方法获取
#优先级不同的任务可以通过优先级队列PriorityBlockingQueue来处理，可以让高优先级的任务先执行。
