# netframework_clrmemory collector

The netframework_clrmemory collector exposes metrics about memory in dotnet applications.

|||
-|-
Metric name prefix  | `netframework_clrmemory`
Classes             | `Win32_PerfRawData_NETFramework_NETCLRMemory`
Enabled by default? | No

## Flags

None

## Metrics

Name | Description | 中文 | Type | Labels
-----|-------------|------|-------|-------
`windows_netframework_clrmemory_allocated_bytes_total` | Displays the total number of bytes allocated on the garbage collection heap. | 显示在垃圾回收堆上分配的总字节数 | counter | `process`
`windows_netframework_clrmemory_finalization_survivors` | Displays the number of garbage-collected objects that survive a collection because they are waiting to be finalized. | 翻译：显示在收集中幸存下来的垃圾收集对象的数量，因为它们正在等待完成。 性能监视器中的解释：此计数器显示由于等待完成而回收后仍存在的垃圾回收对象数。如果这些对象具有对其他对象的引用，则那些对象也会存在，但是不计入此计数器内；“Promoted Finalization-Memory from Gen 0”和“Promoted Finalization-Memory from Gen 1”计数器表示所有由于要完成而存在的内存。此计数器不是累积计数器；它在每次 GC 结束时更新为仅在特定 GC 后仍存在的对象的数量。此计数器旨在指示应用程序由于完成而可能会带来的额外系统开销。 | gauge | `process`
`windows_netframework_clrmemory_heap_size_bytes` | Displays the maximum bytes that can be allocated; it does not indicate the current number of bytes allocated. | 显示可以分配的最大字节数；它不表示当前分配的字节数。 | gauge | `process`
`windows_netframework_clrmemory_promoted_bytes` | Displays the bytes that were promoted from the generation to the next one during the last GC. Memory is promoted when it survives a garbage collection. | 显示在上次GC期间从一代晋升到下一代的字节数。当内存在一个垃圾回收过程中存活下来时，它会被晋升。 | gauge | `process`
`windows_netframework_clrmemory_number_gc_handles` | Displays the current number of garbage collection handles in use. Garbage collection handles are handles to resources external to the common language runtime and the managed environment. | 显示当前正在使用的垃圾回收句柄数。垃圾回收句柄是对公共语言运行时和托管环境之外的资源的句柄。 | gauge | `process`
`windows_netframework_clrmemory_collections_total` | Displays the number of times the generation objects are garbage collected since the application started. | 显示自应用程序启动以来，代对象被垃圾回收的次数。 | counter | `process`
`windows_netframework_clrmemory_induced_gc_total` | Displays the peak number of times garbage collection was performed because of an explicit call to GC.Collect. | 显示由于显式调用GC.Collect而导致垃圾回收执行的峰值次数。 | counter | `process`
`windows_netframework_clrmemory_number_pinned_objects` | Displays the number of pinned objects encountered in the last garbage collection. | 此计数器显示上次 GC 中遇到的固定对象的数目。此计数器只跟踪被垃圾回收的堆中的固定对象，例如 Gen 0 GC 将只导致对 0 代堆中的固定对象进行枚举。固定对象是内存中垃圾回收器无法移动的对象。 | gauge | `process`
`windows_netframework_clrmemory_number_sink_blocksinuse` | Displays the current number of synchronization blocks in use. Synchronization blocks are per-object data structures allocated for storing synchronization information. They hold weak references to managed objects and must be scanned by the garbage collector. | 显示当前使用的同步块数量。同步块是为存储同步信息而为每个对象分配的数据结构。它们对托管对象持有弱引用，并且必须由垃圾回收器扫描 | gauge | `process`
`windows_netframework_clrmemory_committed_bytes` | Displays the amount of virtual memory, in bytes, currently committed by the garbage collector. Committed memory is the physical memory for which space has been reserved in the disk paging file. | 显示垃圾回收器当前提交的虚拟内存（以字节为单位）量。已提交的内存是在磁盘分页文件中预留的物理内存 | gauge | `process`
`windows_netframework_clrmemory_reserved_bytes` | Displays the amount of virtual memory, in bytes, currently reserved by the garbage collector. Reserved memory is the virtual memory space reserved for the application when no disk or main memory pages have been used. | 显示垃圾回收器当前保留的虚拟内存（以字节为单位）量。保留的内存是在未使用磁盘或主内存页面时为应用程序预留的虚拟内存空间 | gauge | `process`
`windows_netframework_clrmemory_gc_time_percent` | Displays the percentage of time that was spent performing a garbage collection in the last sample. | % Time in GC 是自上一次 GC 循环以来执行垃圾回收 (GC) 所用的运行时间的百分比。此计数器通常是垃圾回收器代表应用程序收集和压缩内存所完成的工作的指示器。此计数器只在每次 GC 结束时更新，而计数器值反映上一次观测的值；它不是平均值。 | gauge | `process`

### Example metric
_This collector does not yet have explained examples, we would appreciate your help adding them!_

## Useful queries
_This collector does not yet have any useful queries added, we would appreciate your help adding them!_

## Alerting examples
_This collector does not yet have alerting examples, we would appreciate your help adding them!_
