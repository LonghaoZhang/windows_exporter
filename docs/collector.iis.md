# iis collector

The iis collector exposes metrics about the IIS server

|||
-|-
Metric name prefix  | `iis`
Data source         | Perflib
Enabled by default? | No

## Flags

### `--collector.iis.site-include`

If given, a site needs to match the include regexp in order for the corresponding metrics to be reported.

### `--collector.iis.site-exclude`

If given, a site needs to *not* match the exclude regexp in order for the corresponding metrics to be reported.

### `--collector.iis.app-include`

If given, an application needs to match the include regexp in order for the corresponding metrics to be reported.

### `--collector.iis.app-exclude`

If given, an application needs to *not* match the exclude regexp in order for the corresponding metrics to be reported.

## Metrics

Name | Description | 中文 | Type | Labels
-----|-------------|------|-------|-------
`windows_iis_current_anonymous_users` | The number of users who currently have an anonymous request pending with the web service | 当前拥有匿名请求待处理的用户数 | gauge | `site`
`windows_iis_current_blocked_async_io_requests` | _Not yet documented_ |  | gauge | `site`
`windows_iis_current_cgi_requests` | The number of CGI requests that are being processed simultaneously by the web service | 正在由Web服务并行处理的CGI请求数 | gauge | `site`
`windows_iis_current_connections` |  The number of active connections to the web service | 与Web服务的活动连接数 | gauge | `site`
`windows_iis_current_isapi_extension_requests` | The number of [ISAPI extension](https://docs.microsoft.com/en-us/previous-versions/iis/6.0-sdk/ms525172(v=vs.90)) requests that are being processed simultaneously by the web service | 正在由Web服务并行处理的ISAPI扩展请求数 | gauge | `site`
`windows_iis_current_non_anonymous_users` | The number of users who currently have a nonanonymous request pending with the web service | 当前拥有非匿名请求待处理的用户数 | gauge | `site`
`windows_iis_service_uptime` | The uptime for the web service or a Web site (seconds) | Web服务或网站的运行时间（秒） | gauge | `site`
`windows_iis_received_bytes_total` | The total bytes of data that have been received by the web service since the service started | 自服务启动以来，Web服务接收到的总字节数 | counter | `site`
`windows_iis_sent_bytes_total` | The number of data bytes that have been sent by the web service since the service started | 自服务启动以来，Web服务发送的总字节数 | counter | `site`
`windows_iis_anonymous_users_total` | The number of users who have established an anonymous request since the web service started | 自Web服务启动以来建立的匿名请求用户总数 | counter | `site`
`windows_iis_blocked_async_io_requests_total` | The total number of blocked asynchronous I/O requests since the start of the IIS service | 自IIS服务启动以来的总阻塞异步I/O请求数 | counter | `site`
`windows_iis_cgi_requests_total` | The number of all CGI requests that have been made since the web service started | 自Web服务启动以来的所有CGI请求总数 | counter | `site`
`windows_iis_connection_attempts_all_instances_total` | The number of connections to the web service that have been attempted since the service started | 自服务启动以来尝试连接到Web服务的次数 | counter | `site`
`windows_iis_requests_total` | The number of requests that have been made since the web service was started | 自Web服务启动以来的请求总数 | counter | `site`, `method`
`windows_iis_files_received_total` | The total number of files that have been received by the FTP service since the service started | 自FTP服务启动以来接收的文件总数 | counter | `site`
`windows_iis_files_sent_total` | The total number of files that have been sent by the FTP service since the service started | 自FTP服务启动以来发送的文件总数 | counter | `site`
`windows_iis_ipapi_extension_requests_total` | The number of ISAPI extension requests that have been made since the web service started | 自Web服务启动以来的ISAPI扩展请求总数 | counter | `site`
`windows_iis_locked_errors_total` | The number of requests that have been made since the service started that could not be satisfied by the server because the requested document was locked. Usually reported as HTTP error 423 | 自服务启动以来，由于请求的文档被锁定而无法满足的请求次数。通常报告为HTTP错误423 | counter | `site`
`windows_iis_logon_attempts_total` | The number of attempts to log on to the web service that have occurred since the service started | 自服务启动以来尝试登录Web服务的次数 | counter | `site`
`windows_iis_non_anonymous_users_total` | The number of users who have made nonanonymous requests to the web service since the service started | 自服务启动以来进行非匿名请求的用户总数 | counter | `site`
`windows_iis_not_found_errors_total` | The number of requests that have been made since the service started that were not satisfied by the server because the requested document was not found. Usually reported as HTTP error 404 | 自服务启动以来，由于服务器找不到请求的文档而无法满足的请求次数。通常报告为HTTP错误404 | counter | `site`
`windows_iis_rejected_async_io_requests_total` |The total number of rejected asynchronous I/O requests since the start of the IIS service. | 自IIS服务启动以来的总拒绝异步I/O请求数 | counter | `site`
`windows_iis_current_application_pool_state` | The current status of the application pool (1 - Uninitialized, 2 - Initialized, 3 - Running, 4 - Disabling, 5 - Disabled, 6 - Shutdown Pending, 7 - Delete Pending) | 应用程序池的当前状态（1 - 未初始化，2 - 已初始化，3 - 运行中，4 - 禁用中，5 - 已禁用，6 - 关闭挂起，7 - 删除挂起） | gauge | `app`, `state`
`windows_iis_current_application_pool_start_time` | The unix timestamp for the application pool start time | 应用程序池启动时间的Unix时间戳 | gauge | `app`
`windows_iis_current_worker_processes` | The current number of worker processes that are running in the application pool | 在应用程序池中正在运行的工作进程数 | gauge | `app`
`windows_iis_maximum_worker_processes` | The maximum number of worker processes that have been created for the application pool since Windows Process Activation Service (WAS) started | 自Windows进程激活服务（WAS）启动以来为应用程序池创建的最大工作进程数 | gauge | `app`
`windows_iis_recent_worker_process_failures` | The number of times that worker processes for the application pool failed during the rapid-fail protection interval | 在快速失败保护间隔内，应用程序池的工作进程失败次数 | gauge | `app`
`windows_iis_time_since_last_worker_process_failure` | The length of time, in seconds, since the last worker process failure occurred for the application pool | 自上次工作进程失败以来的时间（以秒为单位） | gauge | `app`
`windows_iis_total_application_pool_recycles` | The number of times that the application pool has been recycled since Windows Process Activation Service (WAS) started | 自Windows进程激活服务（WAS）启动以来应用程序池回收的次数 | counter | `app`
`windows_iis_total_application_pool_start_time` | The unix timestamp for the application pool of when the Windows Process Activation Service (WAS) started | Windows进程激活服务（WAS）启动时的应用程序池Unix时间戳 | counter | `app`
`windows_iis_total_worker_processes_created` | The number of worker processes created for the application pool since Windows Process Activation Service (WAS) started | 自Windows进程激活服务（WAS）启动以来为应用程序池创建的工作进程数 | counter | `app`
`windows_iis_total_worker_process_failures` | The number of times that worker processes have crashed since the application pool was started | 自应用程序池启动以来工作进程崩溃的次数 | counter | `app`
`windows_iis_total_worker_process_ping_failures` | The number of times that Windows Process Activation Service (WAS) did not receive a response to ping messages sent to a worker process | Windows进程激活服务（WAS）未收到发送给工作进程的ping消息响应的次数 | counter | `app`
`windows_iis_total_worker_process_shutdown_failures` | The number of times that Windows Process Activation Service (WAS) failed to shut down a worker process | Windows进程激活服务（WAS）未能关闭工作进程的次数 | counter | `app`
`windows_iis_total_worker_process_startup_failures` | The number of times that Windows Process Activation Service (WAS) failed to start a worker process | Windows进程激活服务（WAS）未能启动工作进程的次数 | counter | `app`
`windows_iis_worker_cache_active_flushed_entries` | Number of file handles cached that will be closed when all current transfers complete | 将在所有当前传输完成后关闭的缓存文件句柄数 | gauge | `app`, `pid`
`windows_iis_worker_file_cache_memory_bytes` | Current number of bytes used by file cache | 文件缓存当前使用的字节数 | gauge | `app`, `pid`
`windows_iis_worker_file_cache_max_memory_bytes` | Maximum number of bytes used by file cache | 文件缓存使用的最大字节数 | counter | `app`, `pid`
`windows_iis_worker_file_cache_flushes_total` | Total number of file cache flushes (since service startup) | 自服务启动以来的文件缓存刷新总数 | counter | `app`, `pid`
`windows_iis_worker_file_cache_queries_total` | Total file cache queries (hits + misses) | 文件缓存查询总数（命中 + 未命中） | counter | `app`, `pid`
`windows_iis_worker_file_cache_hits_total` | Total number of successful lookups in the user-mode file cache | 在用户模式文件缓存中成功查找的总数 | counter | `app`, `pid`
`windows_iis_worker_file_cache_items` | Current number of files whose contents are present in user-mode cache | 用户模式缓存中存在内容的文件数 | gauge | `app`, `pid`
`windows_iis_worker_file_cache_items_total` | Total number of files whose contents were ever added to the user-mode cache (since service startup) | 自服务启动以来添加到用户模式缓存中的文件总数 | counter | `app`, `pid`
`windows_iis_worker_file_cache_items_flushed_total` | Total number of file handles that have been removed from the user-mode cache (since service startup) | 已从用户模式缓存中删除的文件句柄总数 | counter | `app`, `pid`
`windows_iis_worker_uri_cache_flushes_total` | Total number of URI cache flushes (since service startup) | 自服务启动以来的URI缓存刷新总数 | counter | `app`, `pid`
`windows_iis_worker_uri_cache_queries_total` | Total number of uri cache queries (hits + misses) | URI缓存查询总数（命中 + 未命中） | counter | `app`, `pid`
`windows_iis_worker_uri_cache_hits_total` | Total number of successful lookups in the user-mode URI cache (since service startup) | 自服务启动以来在用户模式URI缓存中成功 | counter | `app`, `pid`
`windows_iis_worker_uri_cache_items` | Number of URI information blocks currently in the user-mode cache | 当前在用户模式缓存中URI信息块的数量 | gauge | `app`, `pid`
`windows_iis_worker_uri_cache_items_total` | Total number of URI information blocks added to the user-mode cache (since service startup) | 自服务启动以来添加到用户模式缓存的URI信息块总数 | counter | `app`, `pid`
`windows_iis_worker_uri_cache_items_flushed_total` | The number of URI information blocks that have been removed from the user-mode cache (since service startup) | 自服务启动以来从用户模式缓存中删除的URI信息块总数 | counter | `app`, `pid`
`windows_iis_worker_metadata_cache_items` | Number of metadata information blocks currently present in user-mode cache | 当前在用户模式缓存中存在的元数据信息块数量 | gauge | `app`, `pid`
`windows_iis_worker_metadata_cache_flushes_total` | Total number of user-mode metadata cache flushes (since service startup) | 自服务启动以来的用户模式元数据缓存刷新总数 | counter | `app`, `pid`
`windows_iis_worker_metadata_cache_queries_total` | Total metadata cache queries (hits + misses) | 总计元数据缓存查询（命中+未命中） | counter | `app`, `pid`
`windows_iis_worker_metadata_cache_hits_total` | Total number of successful lookups in the user-mode metadata cache (since service startup) | 自服务启动以来在用户模式元数据缓存中成功查找的总数 | counter | `app`, `pid`
`windows_iis_worker_metadata_cache_items_cached_total` | Total number of metadata information blocks added to the user-mode cache (since service startup) | 自服务启动以来添加到用户模式缓存的元数据信息块总数 | counter | `app`, `pid`
`windows_iis_worker_metadata_cache_items_flushed_total` | Total number of metadata information blocks removed from the user-mode cache (since service startup) | 自服务启动以来从用户模式缓存中删除的元数据信息块总数 | counter | `app`, `pid`
`windows_iis_worker_output_cache_active_flushed_items` |The total number of active and flushed items in the output cache of the IIS worker process. Active items are those that are currently being used to serve client requests, while flushed items are those that have been removed from the cache but are still waiting to be flushed to disk. | IIS工作进程输出缓存中活动和已刷新项目的总数量。活动项目是当前用于服务客户端请求的项目，而已刷新项目是从缓存中删除但仍在等待刷新到磁盘的项目 | counter | `app`, `pid`
`windows_iis_worker_output_cache_items` | Number of items current present in output cache | 当前在输出缓存中存在的项目数 | counter | `app`, `pid`
`windows_iis_worker_output_cache_memory_bytes` | Current number of bytes used by output cache | 当前输出缓存使用的字节数 | counter | `app`, `pid`
`windows_iis_worker_output_queries_total` | Total number of output cache queries (hits + misses) | 输出缓存查询总数（命中+未命中） | counter | `app`, `pid`
`windows_iis_worker_output_cache_hits_total` | Total number of successful lookups in output cache (since service startup) | 自服务启动以来在输出缓存中成功查找的总数 | counter | `app`, `pid`
`windows_iis_worker_output_cache_items_flushed_total` | Total number of items flushed from output cache (since service startup) | 自服务启动以来从输出缓存中刷新的项目总数 | counter | `app`, `pid`
`windows_iis_worker_output_cache_flushes_total` | Total number of flushes of output cache (since service startup) | 自服务启动以来输出缓存的刷新总数 | counter | `app`, `pid`
`windows_iis_worker_threads` | Number of threads actively processing requests in the worker process | 在工作进程中积极处理请求的线程数 | gauge | `app`, `pid`, `state`
`windows_iis_worker_max_threads` | Maximum number of threads to which the thread pool can grow as needed | 线程池可以根据需要增长的最大线程数 | counter | `app`, `pid`
`windows_iis_worker_requests_total` | Total number of HTTP requests served by the worker process | 工作进程服务的HTTP请求总数 | counter | `app`, `pid`
`windows_iis_worker_current_requests` | Current number of requests being processed by the worker process | 工作进程当前正在处理的请求数 | counter | `app`, `pid`
`windows_iis_worker_request_errors_total` | Total number of requests that returned an error | 返回错误的请求总数 | counter | `app`, `pid`, `status_code`
`windows_iis_worker_current_websocket_requests` | the current number of WebSocket connections being processed by the IIS worker process. | IIS工作进程当前正在处理的WebSocket连接数 | counter | `app`, `pid`
`windows_iis_worker_websocket_connection_attempts_total` | the total number of attempted WebSocket connections since the start of the IIS worker process | 自IIS工作进程启动以来尝试的WebSocket连接总数 | counter | `app`, `pid`
`windows_iis_worker_websocket_connection_accepted_total` | the total number of WebSocket connections that have been successfully established since the start of the IIS worker process | 自IIS工作进程启动以来成功建立的WebSocket连接总数 | counter | `app`, `pid`
`windows_iis_worker_websocket_connection_rejected_total` | the total number of WebSocket connections that have been rejected by the server since the start of the IIS worker process. Connections can be rejected for various reasons, such as capacity limitations, authentication failures, or configuration issues | 自IIS工作进程启动以来被服务器拒绝的WebSocket连接总数。由于各种原因，例如容量限制、身份验证失败或配置问题，可能会拒绝连接 | counter | `app`, `pid`
`windows_iis_server_cache_active_flushed_entries` | Number of file handles cached that will be closed when all current transfers complete | 将在所有当前传输完成后关闭的缓存文件句柄数 | counter | None
`windows_iis_server_file_cache_memory_bytes` | Current number of bytes used by file cache | 当前文件缓存使用的字节数 | gauge | None
`windows_iis_server_file_cache_max_memory_bytes` | Maximum number of bytes used by file cache | 文件缓存使用的最大字节数 | counter | None
`windows_iis_server_file_cache_flushes_total` | Total number of file cache flushes (since service startup) | 自服务启动以来文件缓存的刷新总数 | counter | None
`windows_iis_server_file_cache_queries_total` | Total number of file cache queries (hits + misses) | 文件缓存查询总数（命中+未命中） | counter | None
`windows_iis_server_file_cache_hits_total` | Total number of successful lookups in the file cache | 在文件缓存中成功查找的总数 | counter | None
`windows_iis_server_file_cache_items` | Current number of files whose contents are present in cache | 其内容当前在缓存中的文件数 | gauge | None
`windows_iis_server_file_cache_items_total` | Total number of files whose contents were ever added to the cache (since service startup) | 曾经添加到缓存（自服务启动以来）的文件内容总数 | counter | None
`windows_iis_server_file_cache_items_flushed_total` | Total number of file handles that have been removed from the cache (since service startup) | 从缓存中删除的文件句柄总数（自服务启动以来） | counter | None
`windows_iis_server_uri_cache_flushes_total` | Total number of URI cache flushes (since service startup) | 自服务启动以来URI缓存的刷新总数 | counter | `mode`
`windows_iis_server_uri_cache_queries_total` | Total number of uri cache queries (hits + misses) | URI缓存查询总数（命中+未命中） | counter | `mode`
`windows_iis_server_uri_cache_hits_total` | Total number of successful lookups in the URI cache (since service startup) | 自服务启动以来在URI缓存中成功查找的总数 | counter | `mode`
`windows_iis_server_uri_cache_items` | Number of URI information blocks currently in the cache | 当前在缓存中的URI信息块数量 | gauge | `mode`
`windows_iis_server_uri_cache_items_total` | Total number of URI information blocks added to the cache (since service startup) | 添加到缓存（自服务启动以来）的URI信息块总数 | counter | `mode`
`windows_iis_server_uri_cache_items_flushed_total` | The number of URI information blocks that have been removed from the cache (since service startup) | 从缓存中删除的URI信息块总数（自服务启动以来） | counter | `mode`
`windows_iis_server_metadata_cache_items` | Number of metadata information blocks currently present in cache | 当前在缓存中存在的元数据信息块数量 | gauge | None
`windows_iis_server_metadata_cache_flushes_total` | Total number of metadata cache flushes (since service startup) | 自服务启动以来元数据缓存的刷新总数 | counter | None
`windows_iis_server_metadata_cache_queries_total` | Total metadata cache queries (hits + misses) | 元数据缓存查询总数（命中+未命中） | counter | None
`windows_iis_server_metadata_cache_hits_total` | Total number of successful lookups in the metadata cache (since service startup) | 自服务启动以来在元数据缓存中成功查找的总数 | counter | None
`windows_iis_server_metadata_cache_items_cached_total` | Total number of metadata information blocks added to the cache (since service startup) | 添加到缓存（自服务启动以来）的元数据信息块总数 | counter | None
`windows_iis_server_metadata_cache_items_flushed_total` | Total number of metadata information blocks removed from the cache (since service startup) | 从缓存中删除的元数据信息块总数（自服务启动以来） | counter | None
`windows_iis_server_output_cache_active_flushed_items` | The total number of active and flushed items in the output cache of the IIS server | IIS服务器输出缓存中活动和已刷新项目的总数量 | counter | None
`windows_iis_server_output_cache_items` | Number of items current present in output cache | 当前在输出缓存中存在的项目数 | counter | None
`windows_iis_server_output_cache_memory_bytes` | Current number of bytes used by output cache | 当前输出缓存使用的字节数 | counter | None
`windows_iis_server_output_cache_queries_total` | Total output cache queries (hits + misses) | 输出缓存查询总数（命中+未命中） | counter | None
`windows_iis_server_output_cache_hits_total` | Total number of successful lookups in output cache (since service startup) | 自服务启动以来在输出缓存中成功查找的总数 | counter | None
`windows_iis_server_output_cache_items_flushed_total` | Total number of items flushed from output cache (since service startup) | 自服务启动以来从输出缓存中刷新的项目总数 | counter | None
`windows_iis_server_output_cache_flushes_total` | Total number of flushes of output cache (since service startup) | 自服务启动以来输出缓存的刷新总数 | counter | None

### Example metric
_This collector does not yet have explained examples, we would appreciate your help adding them!_

## Useful queries
_This collector does not yet have any useful queries added, we would appreciate your help adding them!_

## Alerting examples
_This collector does not yet have alerting examples, we would appreciate your help adding them!_
