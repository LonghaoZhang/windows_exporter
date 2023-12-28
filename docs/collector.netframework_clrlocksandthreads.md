# netframework_clrlocksandthreads collector

The netframework_clrlocksandthreads collector exposes metrics about locks and threads in dotnet applications.

|||
-|-
Metric name prefix  | `netframework_clrlocksandthreads`
Classes             | `Win32_PerfRawData_NETFramework_NETCLRLocksAndThreads`
Enabled by default? | No

## Flags

None

## Metrics

Name | Description | 中文 | Type | Labels
-----|-------------|------|-------|-------
`windows_netframework_clrlocksandthreads_current_queue_length` | Displays the total number of threads that are currently waiting to acquire a managed lock in the application. | 显示当前在应用程序中等待获取托管锁的线程总数 | gauge | `process`
`windows_netframework_clrlocksandthreads_current_logical_threads` | Displays the number of current managed thread objects in the application. This counter maintains the count of both running and stopped threads.  | 显示应用程序中当前的托管线程对象数量。此计数器维护运行和停止线程的数量 | gauge | `process`
`windows_netframework_clrlocksandthreads_physical_threads_current` | Displays the number of native operating system threads created and owned by the common language runtime to act as underlying threads for managed thread objects. This counter's value does not include the threads used by the runtime in its internal operations; it is a subset of the threads in the operating system process. | 显示公共语言运行时创建并拥有的用于作为托管线程对象的底层线程的本机操作系统线程数量。此计数器的值不包括运行时在其内部操作中使用的线程；它是操作系统进程中线程的一个子集。 | gauge | `process`
`windows_netframework_clrlocksandthreads_recognized_threads_current` | Displays the number of threads that are currently recognized by the runtime. These threads are associated with a corresponding managed thread object. The runtime does not create these threads, but they have run inside the runtime at least once. | 显示当前被运行时识别的线程数量。这些线程与相应的托管线程对象关联。运行时不会创建这些线程，但它们至少在运行时内部运行过一次。 | gauge | `process`
`windows_netframework_clrlocksandthreads_recognized_threads_total` | Displays the total number of threads that have been recognized by the runtime since the application started. These threads are associated with a corresponding managed thread object. The runtime does not create these threads, but they have run inside the runtime at least once. | 显示自应用程序启动以来被运行时识别的线程总数。这些线程与相应的托管线程对象关联。运行时不会创建这些线程，但它们至少在运行时内部运行过一次。 | counter | `process`
`windows_netframework_clrlocksandthreads_queue_length_total` | Displays the total number of threads that waited to acquire a managed lock since the application started. | 显示自应用程序启动以来等待获取托管锁的线程总数。 | counter | `process`
`windows_netframework_clrlocksandthreads_contentions_total` | Displays the total number of times that threads in the runtime have attempted to acquire a managed lock unsuccessfully. | 显示运行时中的线程尝试获取托管锁但未成功的总次数。 | counter | `process`

### Example metric
_This collector does not yet have explained examples, we would appreciate your help adding them!_

## Useful queries
_This collector does not yet have any useful queries added, we would appreciate your help adding them!_

## Alerting examples
_This collector does not yet have alerting examples, we would appreciate your help adding them!_
