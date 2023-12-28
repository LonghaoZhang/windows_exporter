# netframework_clrremoting collector

The netframework_clrremoting collector exposes metrics about dotnet remoting.

|||
-|-
Metric name prefix  | `netframework_clrremoting`
Classes             | `Win32_PerfRawData_NETFramework_NETCLRRemoting`
Enabled by default? | No

## Flags

None

## Metrics

Name | Description | 中文 | Type | Labels
-----|-------------|------|-------|-------
`windows_netframework_clrremoting_channels_total` | Displays the total number of remoting channels registered across all application domains since application started. | 显示自应用程序启动以来在所有应用程序域中注册的 remoting 通道的总数。 | counter | `process`
`windows_netframework_clrremoting_context_bound_classes_loaded` | Displays the current number of context-bound classes that are loaded. | 显示当前加载的上下文绑定类的数量 | gauge | `process`
`windows_netframework_clrremoting_context_bound_objects_total` | Displays the total number of context-bound objects allocated. | 显示分配的上下文绑定对象的总数 | counter | `process`
`windows_netframework_clrremoting_context_proxies_total` | Displays the total number of remoting proxy objects in this process since it started. | 显示自进程启动以来在此进程中创建的 remoting 代理对象的总数 | counter | `process`
`windows_netframework_clrremoting_contexts` | Displays the current number of remoting contexts in the application. | 显示应用程序中当前的 remoting 上下文数量 | gauge | `process`
`windows_netframework_clrremoting_remote_calls_total` | Displays the total number of remote procedure calls invoked since the application started. | 显示自应用程序启动以来调用的远程过程调用总数。 | counter | `process`

### Example metric
_This collector does not yet have explained examples, we would appreciate your help adding them!_

## Useful queries
_This collector does not yet have any useful queries added, we would appreciate your help adding them!_

## Alerting examples
_This collector does not yet have alerting examples, we would appreciate your help adding them!_
