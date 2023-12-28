# netframework_clrinterop collector

The netframework_clrinterop collector exposes metrics about interop between the dotnet framework and outside components.

|||
-|-
Metric name prefix  | `netframework_clrinterop`
Classes             | `Win32_PerfRawData_NETFramework_NETCLRInterop`
Enabled by default? | No

## Flags

None

## Metrics

Name | Description | 中文 | Type | Labels
-----|-------------|------|-------|-------
`windows_netframework_clrinterop_com_callable_wrappers_total` | Displays the current number of COM callable wrappers (CCWs). A CCW is a proxy for a managed object being referenced from an unmanaged COM client. | 此计数器显示 Com 可调用包装 (CCW) 的当前数目。CCW 是非托管 COM 客户端中引用的 .NET 托管对象的代理。此计数器旨在指示非托管 COM 代码引用的托管对象的数目。 | counter | `process`
`windows_netframework_clrinterop_interop_marshalling_total` | Displays the total number of times arguments and return values have been marshaled from managed to unmanaged code, and vice versa, since the application started. | 此计数器显示自应用程序启动以来将参数和返回值从托管代码封送为非托管代码以及从非托管代码封送为托管代码的总次数。如果 stub 是内联的，则此计数器不递增。(stub 负责封送参数和返回值)。如果封送处理系统开销很小，则 stub 通常是内联的。 | counter | `process`
`windows_netframework_clrinterop_interop_stubs_created_total` | Displays the current number of stubs created by the common language runtime. Stubs are responsible for marshaling arguments and return values from managed to unmanaged code, and vice versa, during a COM interop call or a platform invoke call. | 此计数器显示 CLR 创建的 stub 的当前数目。Stub 负责在 COM 互操作调用或 PInvoke 调用期间将参数和返回值从托管代码封送处理为非托管代码以及从非托管代码封送处理为托管代码。 | counter | `process`

### Example metric
_This collector does not yet have explained examples, we would appreciate your help adding them!_

## Useful queries
_This collector does not yet have any useful queries added, we would appreciate your help adding them!_

## Alerting examples
_This collector does not yet have alerting examples, we would appreciate your help adding them!_
