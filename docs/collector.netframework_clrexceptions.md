# netframework_clrexceptions collector

The netframework_clrexceptions collector exposes metrics about CLR exceptions in the dotnet framework.

|||
-|-
Metric name prefix  | `netframework_clrexceptions`
Classes             | `Win32_PerfRawData_NETFramework_NETCLRExceptions`
Enabled by default? | No

## Flags

None

## Metrics

Name | Description | 中文 | Type | Labels
-----|-------------|------|-------|-------
`windows_netframework_clrexceptions_exceptions_thrown_total` | Displays the total number of exceptions thrown since the application started. This includes both .NET exceptions and unmanaged exceptions that are converted into .NET exceptions. | 显示自应用程序启动以来抛出的异常总数。这包括.NET异常和转换为.NET异常的非托管异常。 | counter | `process`
`windows_netframework_clrexceptions_exceptions_filters_total` | Displays the total number of .NET exception filters executed. An exception filter evaluates regardless of whether an exception is handled. | 显示执行的.NET异常筛选器总数。无论异常是否被处理，异常筛选器都会进行评估。 | counter | `process`
`windows_netframework_clrexceptions_exceptions_finallys_total` | Displays the total number of finally blocks executed. Only the finally blocks executed for an exception are counted; finally blocks on normal code paths are not counted by this counter. | 显示执行的finally块总数。仅计算为异常执行的finally块；此计数器不计算正常代码路径上的finally块。 | counter | `process`
`windows_netframework_clrexceptions_throw_to_catch_depth_total` | Displays the total number of stack frames traversed, from the frame that threw the exception to the frame that handled the exception. | 显示从抛出异常的帧到处理异常的帧所遍历的堆栈帧总数。 | counter | `process`

### Example metric
_This collector does not yet have explained examples, we would appreciate your help adding them!_

## Useful queries
_This collector does not yet have any useful queries added, we would appreciate your help adding them!_

## Alerting examples
_This collector does not yet have alerting examples, we would appreciate your help adding them!_
