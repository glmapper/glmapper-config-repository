
## 简介

本工程作为配置中心仓库使用

## 配置文件映射地址

配置服务中心可以从远程程序获取配置信息，http请求地址和资源文件映射如下:

### /{application}/{profile}/{label}

* 访问地址
    http://{hostname}:{port}/glmapper/pre/master
* 结果：
```json
{
    "name":"glmapper",
    "profiles":[
        "pre"
    ],
    "label":"master",
    "version":"ef3b7eff0ddcbabd443b9a2a1a841adf173c24b7",
    "state":null,
    "propertySources":[
        {
            "name":"https://github.com/glmapper/glmapper-config-repository/glmapper-pre.properties",
            "source":{
                "name":"leishu@glmapper",
                "blog":"http://www.glmapper.com",
                "version":"pre"
            }
        }
    ]
}
```

### /{application}/{profile}  

* 访问地址
    http://{hostname}:{port}/glmapper/pre
* 结果：
```json
{
    "name":"glmapper",
    "profiles":[
        "pre"
    ],
    "label":null,
    "version":"ef3b7eff0ddcbabd443b9a2a1a841adf173c24b7",
    "state":null,
    "propertySources":[
        {
            "name":"https://github.com/glmapper/glmapper-config-repository/glmapper-pre.properties",
            "source":{
                "name":"leishu@glmapper",
                "blog":"http://www.glmapper.com",
                "version":"pre"
            }
        }
    ]
}
```

                    
### /{application}-{profile}.yml & /{application}-{profile}.properties
                 
* 访问地址
    * http://{hostname}:{port}/glmapper-pre.yml
    * http://{hostname}:{port}/glmapper-pre.properties
* 结果：
```json
blog: http://www.glmapper.com
name: leishu@glmapper
version: pre
```
###  /{label}/{application}-{profile}.yml & /{label}/{application}-{profile}.properties
* 访问地址
    * http://{hostname}:{port}/master/glmapper-pre.yml
    * http://{hostname}:{port}/master/glmapper-pre.properties
* 结果：
```json
blog: http://www.glmapper.com
name: leishu@glmapper
version: pre
```

