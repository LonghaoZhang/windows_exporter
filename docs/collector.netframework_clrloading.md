# netframework_clrloading collector

The netframework_clrloading collector exposes metrics about the dotnet loader.

|||
-|-
Metric name prefix  | `netframework_clrloading`
Classes             | `Win32_PerfRawData_NETFramework_NETCLRLoading`
Enabled by default? | No

## Flags

None

## Metrics

Name | Description | 中文 | Type | Labels
-----|-------------|------|-------|-------
`windows_netframework_clrloading_loader_heap_size_bytes` | Displays the current size, in bytes, of the memory committed by the class loader across all application domains. Committed memory is the physical space reserved in the disk paging file. | 此计数器显示由类加载程序跨所有 AppDomain 提交的内存的当前大小(以字节为单位)。(提交内存是磁盘页面文件上为其保留了空间的物理内存)。 | gauge | `process`
`windows_netframework_clrloading_appdomains_loaded_current` | Displays the current number of application domains loaded in this application. | 此计数器显示当前此应用程序中加载的 AppDomain 的数目。AppDomain(应用程序域)提供安全通用的处理单元，CLR 可以使用该处理单元在运行于同一进程中的应用程序之间提供隔离。 | gauge | `process`
`windows_netframework_clrloading_assemblies_loaded_current` | Displays the current number of assemblies loaded across all application domains in the currently running application. If the assembly is loaded as domain-neutral from multiple application domains, this counter is incremented only once. | 显示当前运行应用程序中所有应用程序域加载的程序集的当前数量。如果程序集从多个应用程序域作为域中立方式加载，此计数器仅增加一次。 | gauge | `process`
`windows_netframework_clrloading_classes_loaded_current` | Displays the current number of classes loaded in all assemblies. | 显示所有程序集中加载的类的当前数量。 | gauge | `process`
`windows_netframework_clrloading_appdomains_loaded_total` | Displays the peak number of application domains loaded since the application started. | 显示自应用程序启动以来加载的应用程序域的峰值数量 | counter | `process`
`windows_netframework_clrloading_appdomains_unloaded_total` | Displays the total number of application domains unloaded since the application started. If an application domain is loaded and unloaded multiple times, this counter increments each time the application domain is unloaded. | 显示自应用程序启动以来卸载的应用程序域的总数。如果应用程序域被多次加载和卸载，每当应用程序域被卸载时，此计数器都会增加 | counter | `process`
`windows_netframework_clrloading_assemblies_loaded_total` | Displays the total number of assemblies loaded since the application started. If the assembly is loaded as domain-neutral from multiple application domains, this counter is incremented only once. | 显示自应用程序启动以来加载的程序集的总数。如果程序集从多个应用程序域作为域中立方式加载，此计数器仅增加一次 | counter | `process`
`windows_netframework_clrloading_classes_loaded_total` | Displays the cumulative number of classes loaded in all assemblies since the application started. | 显示自应用程序启动以来在所有程序集中加载的类的累计数量 | counter | `process`
`windows_netframework_clrloading_class_load_failures_total` | Displays the peak number of classes that have failed to load since the application started. | 显示自应用程序启动以来未能加载的类的峰值数量。 | counter | `process`

### Example metric
_This collector does not yet have explained examples, we would appreciate your help adding them!_

## Useful queries
_This collector does not yet have any useful queries added, we would appreciate your help adding them!_

## Alerting examples
_This collector does not yet have alerting examples, we would appreciate your help adding them!_
