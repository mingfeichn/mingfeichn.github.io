## docker version

[TOC]

Show the Docker version information

### 用法
```bash
docker version [OPTIONS]
```

>**Options**
>
>-f, --format string   使用自定义模板格式化输出
>             'json':             使用JSON格式打印输出
>             'TEMPLATE':         使用Go语言模板格式打印输出
>             Refer to https://docs.docker.com/go/formatting/ for more information about formatting output with templates




### 示例

#### 查询版本信息
  ```bash
  $ docker version
  ```
  ```bash
  Client: Docker Engine - Community
   Version:           25.0.0
   API version:       1.44
   Go version:        go1.21.6
   Git commit:        e758fe5
   Built:             Thu Jan 18 17:13:17 2024
   OS/Arch:           linux/amd64
   Context:           default
  
  Server: Docker Engine - Community
   Engine:
    Version:          25.0.0
    API version:      1.44 (minimum version 1.24)
    Go version:       go1.21.6
    Git commit:       615dfdf
    Built:            Thu Jan 18 17:12:10 2024
    OS/Arch:          linux/amd64
    Experimental:     false
   containerd:
    Version:          1.6.27
    GitCommit:        a1496014c916f9e62104b33d1bb5bd03b0858e59
   runc:
    Version:          1.1.11
    GitCommit:        v1.1.11-0-g4bccb38
   docker-init:
    Version:          0.19.0
    GitCommit:        de40ad0
  ```

#### 以JSON格式输出版本信息  

  ```bash
  $ docker version -f 'json'
  ```

  ```json
  {
  	"Client": {
  		"Platform": {
  			"Name": "Docker Engine - Community"
  		},
  		"Version": "25.0.0",
  		"ApiVersion": "1.44",
  		"DefaultAPIVersion": "1.44",
  		"GitCommit": "e758fe5",
  		"GoVersion": "go1.21.6",
  		"Os": "linux",
  		"Arch": "amd64",
  		"BuildTime": "Thu Jan 18 17:13:17 2024",
  		"Context": "default"
  	},
  	"Server": {
  		"Platform": {
  			"Name": "Docker Engine - Community"
  		},
  		"Components": [{
  			"Name": "Engine",
  			"Version": "25.0.0",
  			"Details": {
  				"ApiVersion": "1.44",
  				"Arch": "amd64",
  				"BuildTime": "Thu Jan 18 17:12:10 2024",
  				"Experimental": "false",
  				"GitCommit": "615dfdf",
  				"GoVersion": "go1.21.6",
  				"KernelVersion": "3.10.0-1160.99.1.el7.x86_64",
  				"MinAPIVersion": "1.24",
  				"Os": "linux"
  			}
  		}, {
  			"Name": "containerd",
  			"Version": "1.6.27",
  			"Details": {
  				"GitCommit": "a1496014c916f9e62104b33d1bb5bd03b0858e59"
  			}
  		}, {
  			"Name": "runc",
  			"Version": "1.1.11",
  			"Details": {
  				"GitCommit": "v1.1.11-0-g4bccb38"
  			}
  		}, {
  			"Name": "docker-init",
  			"Version": "0.19.0",
  			"Details": {
  				"GitCommit": "de40ad0"
  			}
  		}],
  		"Version": "25.0.0",
  		"ApiVersion": "1.44",
  		"MinAPIVersion": "1.24",
  		"GitCommit": "615dfdf",
  		"GoVersion": "go1.21.6",
  		"Os": "linux",
  		"Arch": "amd64",
  		"KernelVersion": "3.10.0-1160.99.1.el7.x86_64",
  		"BuildTime": "2024-01-18T17:12:10.000000000+00:00"
  	}
  }
  ```

  
