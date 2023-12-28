# netframework_clrjit collector

The netframework_clrjit collector exposes metrics about the dotnet Just-in-Time compiler.

|||
-|-
Metric name prefix  | `netframework_clrjit`
Classes             | `Win32_PerfRawData_NETFramework_NETCLRJit`
Enabled by default? | No

## Flags

None

## Metrics

Name | Description |  | Type | Labels
-----|-------------|------|-------|-------
`windows_netframework_clrjit_jit_methods_total` | Displays the total number of methods JIT-compiled since the application started. This counter does not include pre-JIT-compiled methods. | 此计数器显示自应用程序启动以来由 CLR JIT 编译器实时 (JIT) 编译的方法总数。此计数器不包括预实时编译的方法。 | counter | `process`
`windows_netframework_clrjit_jit_time_percent` | Displays the percentage of time spent in JIT compilation. This counter is updated at the end of every JIT compilation phase. A JIT compilation phase occurs when a method and its dependencies are compiled. | 此计数器显示自上一次 JIT 编译阶段以来 JIT 编译所用运行时间的百分比。此计数器在每次 JIT 编译阶段结束时更新。JIT 编译阶段是编译方法及其依赖项的阶段。 | gauge | `process`
`windows_netframework_clrjit_jit_standard_failures_total` | Displays the peak number of methods the JIT compiler has failed to compile since the application started. This failure can occur if the MSIL cannot be verified or if there is an internal error in the JIT compiler. | 此计数器显示自应用程序启动以来 JIT 编译器实时编译失败的方法的最大数目。此失败会在无法验证 IL 时或者 JIT 编译器中有内部错误时发生。 | counter | `process`
`windows_netframework_clrjit_jit_il_bytes_total` | Displays the total number of Microsoft intermediate language (MSIL) bytes compiled by the just-in-time (JIT) compiler since the application started | 显示自应用程序启动以来，即时（JIT）编译器编译的Microsoft中间语言（MSIL）字节总数 | counter | `process`

### Example metric
_This collector does not yet have explained examples, we would appreciate your help adding them!_

## Useful queries
_This collector does not yet have any useful queries added, we would appreciate your help adding them!_

## Alerting examples
_This collector does not yet have alerting examples, we would appreciate your help adding them!_
