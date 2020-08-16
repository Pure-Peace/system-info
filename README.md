# system-info
基于python3的linux和windows系统信息api

linux and windows system information api

### based on: python3.8

所有api均支持linux和windows

All apis support linux and windows

# api列表：

- 当前系统网络使用情况：上传下载速率，收发包
```
GetNetWork()
```
```
{'up': 1.54,
 'down': 0.37,
 'upTotal': 87688289,
 'downTotal': 336439316,
 'downPackets': 397399,
 'upPackets': 262468}
```
 
- 当前系统磁盘IO情况：IO读写
```
GetIoReadWrite()
```
```
{'write': 1003332, 'read': 1466368}
```

- 当前系统CPU常量
```
GetCpuConstants()
```
```
{'cpu_count': 1, 'cpu_name': 'AMD Ryzen 5 2500U with Radeon Vega Mobile Gfx  ', 'cpu_core': 4, 'cpu_threads': 8}
```

- 当前系统CPU信息、使用率
```
GetCpuInfo()
```
```
{'used': 17.2,
'used_list': [23.8, 12.2, 19.6, 10.2, 20.3, 6.2, 12.6, 30.3],
'cpu_count': 1,
'cpu_name': 'AMD Ryzen 5 2500U with Radeon Vega Mobile Gfx  ',
'cpu_core': 4,
'cpu_threads': 8}
```

- 当前系统负载信息
```
GetLoadAverage()
```
```
{'one': 0, 'five': 0, 'fifteen': 0, 'max': 16, 'limit': 16, 'safe': 12.0}
```

- 当前系统内存使用情况
```
GetMemInfo()
```
```
{'memTotal': 7069,
 'memFree': 1202,
 'memRealUsed': 5866,
 'menUsedPercent': '82.98'}
```

- 当前系统磁盘信息
```
GetDiskInfo()
```
```
[{'path': 'C:/',
  'size': {'total': 85899341824,
   'used': 84512485376,
   'free': 1386856448,
   'percent': 98.4},
  'fstype': 'NTFS',
  'inodes': False},
 {'path': 'D:/',
  'size': {'total': 413524815872,
   'used': 367597920256,
   'free': 45926895616,
   'percent': 88.9},
  'fstype': 'NTFS',
  'inodes': False}]
```

  
- 获取系统注册表信息（仅windows可用）
```
GetRegValue(key: str, subkey: str, value: str)
```
```
    '''
  获取系统注册表信息

  Parameters
  ----------
  key : str
      类型.
  subkey : str
      路径.
  value : str
      key.

  Returns
  -------
  value : Any
      DESCRIPTION.

  '''
  ```

- 获取系统版本信息
```
GetSystemVersion()
```
```
Windows 10 Home China (build 18362) x64 (Py3.8.5)
```

- 获取系统启动时间及运行时间
```
GetBootTime()
```
```
{'timestamp': 1597574445.835271,
 'runtime': 33396.16829442978,
 'datetime': '2020-08-17 03:57:22'}
```

- 获取全部系统信息
```
GetFullSystemData()
```
```
{
	'cpu': {
		'used': 16.0,
		'used_list': [29.0, 16.4, 30.5, 13.9, 28.1, 16.8, 24.0, 26.7],
		'cpu_count': 1,
		'cpu_name': 'AMD Ryzen 5 2500U with Radeon Vega Mobile Gfx  ',
		'cpu_core': 4,
		'cpu_threads': 8
	},
	'load': {
		'one': 0,
		'five': 0,
		'fifteen': 0,
		'max': 16,
		'limit': 16,
		'safe': 12.0
	},
	'mem': {
		'memTotal': 7069,
		'memFree': 1181,
		'memRealUsed': 5888,
		'menUsedPercent': '83.29'
	},
	'disk': [{
		'path': 'C:/',
		'size': {
			'total': 85899341824,
			'used': 84515794944,
			'free': 1383546880,
			'percent': 98.4
		},
		'fstype': 'NTFS',
		'inodes': False
	}, {
		'path': 'D:/',
		'size': {
			'total': 413524815872,
			'used': 367597862912,
			'free': 45926952960,
			'percent': 88.9
		},
		'fstype': 'NTFS',
		'inodes': False
	}],
	'network': {
		'up': 1.84,
		'down': 2.69,
		'upTotal': 92363508,
		'downTotal': 342344006,
		'downPackets': 409006,
		'upPackets': 271275
	},
	'io': {
		'write': 1277171,
		'read': 38696960
	},
	'boot': {
		'timestamp': 1597574445.966399,
		'runtime': 34064.19006037712,
		'datetime': '2020-08-17 04:08:30'
	},
	'time': 1597608510.1564593
}
```



  
