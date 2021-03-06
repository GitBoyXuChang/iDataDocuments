# IDATA开发接口说明文档

## 首页

#### 1、 首页接口

```
用户数、部门数、合约调用量总量、当天合约调用量、当周合约调用量、当月合约调用量 合约总量、合约升级量总量、当天合约上传量、当天合约升级量、当周合约上传量、当周合约升级量 当月合约上传量、当月合约升级量 
```

路径：

http://127.0.0.1:8090/index/total

/monitor/index/total

请求类型 POST

请求参数：

```json
{
	"applicationId":""
}
```

相应参数：

```json
{
    "returnCode": "0000",
    "returnMsg": "Success",
    "nonceStr": "b9c503b056174fa2bd56ec0c269d0bc9",
    "success": true,
    "data": {
        "userTotal": 6,
        "organizationTotal": 0,
        "contractCallTotal": 52,
        "contractCallTotalOnToday": 1,
        "contractCallTotalOnWeek": 17,
        "contractCallTotalOnMonth": 52,
        "contractTotal": 13,
        "contractUpgradeTotal": 3,
        "contractTotalOnToday": 0,
        "contractUpgradeTotalOnToday": 0,
        "contractTotalOnWeek": 0,
        "contractUpgradeTotalOnWeek": 0,
        "contractTotalOnMonth": 10,
        "contractUpgradeTotalOnMonth": 3,
        "projectTotal": 6,
        "projectTotalOnToday": 0,
        "projectTotalOnWeek": 1,
        "projectTotalOnMonth": 5
    }
}
```

说明：

```java
//用户数
    private Integer userTotal;
    //部门数
    private Integer organizationTotal;
    //合约调用量总量
    private Integer contractCallTotal;
    //当天合约调用量
    private Integer contractCallTotalOnToday;
    //当周合约调用量
    private Integer contractCallTotalOnWeek;
    //当月合约调用量
    private Integer contractCallTotalOnMonth;
    //合约总量
    private Integer contractTotal;
    //合约升级量总量
    private Integer contractUpgradeTotal;
    //当天合约上传量
    private Integer contractTotalOnToday;
    //当天合约升级量
    private Integer contractUpgradeTotalOnToday;
    //当周合约上传量
    private Integer contractTotalOnWeek;
    //当周合约升级量
    private Integer contractUpgradeTotalOnWeek;
    //当月合约上传量
    private Integer contractTotalOnMonth;
    //当月合约升级量
    private Integer contractUpgradeTotalOnMonth;
    //应用总量
    private int projectTotal;
    //当天新增应用量
    private int projectTotalOnToday;
    //当周新增应用量
    private int projectTotalOnWeek;
    //当月新增应用量
    private int projectTotalOnMonth;
```

## 合约延展

## 部门系统

## 链上数据

### 1、业务总览

#### 1.1 累计、当月、本周、当日

路径：

http://127.0.0.1:8090/index/total

/monitor/index/total

请求类型 POST

请求参数：

```json
{
	"applicationId":""
}
```

相应参数：

```json
{
    "returnCode": "0000",
    "returnMsg": "Success",
    "nonceStr": "b9c503b056174fa2bd56ec0c269d0bc9",
    "success": true,
    "data": {
        "userTotal": 6,
        "organizationTotal": 0,
        "contractCallTotal": 52,
        "contractCallTotalOnToday": 1,
        "contractCallTotalOnWeek": 17,
        "contractCallTotalOnMonth": 52,
        "contractTotal": 13,
        "contractUpgradeTotal": 3,
        "contractTotalOnToday": 0,
        "contractUpgradeTotalOnToday": 0,
        "contractTotalOnWeek": 0,
        "contractUpgradeTotalOnWeek": 0,
        "contractTotalOnMonth": 10,
        "contractUpgradeTotalOnMonth": 3,
        "projectTotal": 6,
        "projectTotalOnToday": 0,
        "projectTotalOnWeek": 1,
        "projectTotalOnMonth": 5
    }
}
```

说明：

```java
//用户数
    private Integer userTotal;
    //部门数
    private Integer organizationTotal;
    //合约调用量总量
    private Integer contractCallTotal;
    //当天合约调用量
    private Integer contractCallTotalOnToday;
    //当周合约调用量
    private Integer contractCallTotalOnWeek;
    //当月合约调用量
    private Integer contractCallTotalOnMonth;
    //合约总量
    private Integer contractTotal;
    //合约升级量总量
    private Integer contractUpgradeTotal;
    //当天合约上传量
    private Integer contractTotalOnToday;
    //当天合约升级量
    private Integer contractUpgradeTotalOnToday;
    //当周合约上传量
    private Integer contractTotalOnWeek;
    //当周合约升级量
    private Integer contractUpgradeTotalOnWeek;
    //当月合约上传量
    private Integer contractTotalOnMonth;
    //当月合约升级量
    private Integer contractUpgradeTotalOnMonth;
    //应用总量
    private int projectTotal;
    //当天新增应用量
    private int projectTotalOnToday;
    //当周新增应用量
    private int projectTotalOnWeek;
    //当月新增应用量
    private int projectTotalOnMonth;
```

#### 1.2 合约调用量分布

路径：

http://127.0.0.1:8090/call/sdk/record/project/total

/monitor/call/sdk/record/project/total

请求类型 GET

请求参数：无

```json

```

相应参数：

```json
{
    "returnCode": "0000",
    "returnMsg": "Success",
    "nonceStr": "5bb5aa2d227049ffb7a2db07fa0e87a2",
    "success": true,
    "data": [
        {
            "projectName": "QA",
            "count": 33
        },
        {
            "projectName": "QATB",
            "count": 13
        },
        {
            "projectName": "QB",
            "count": 3
        },
        {
            "projectName": "QC",
            "count": 2
        },
        {
            "projectName": "QQB",
            "count": 1
        }
    ]
}
```

说明：

#### 1.3 业务量分布

路径：

http://127.0.0.1:8090/call/sdk/record/organization/total

/monitor/call/sdk/record/organization/total

请求类型 GET

请求参数：无

```json

```

相应参数：

```json
{
    "returnCode": "0000",
    "returnMsg": "Success",
    "nonceStr": "61030e11d2a748129364fc7871e6fba3",
    "success": true,
    "data": [
        {
            "organizationName": "QA",
            "count": 4
        },
        {
            "organizationName": "QATB",
            "count": 4
        }
    ]
}
```

说明：

#### 1.4 各业务合约调用量统计图

路径：

http://127.0.0.1:8090/call/sdk/record/bargraph/total

/monitor/call/sdk/record/bargraph/total

请求类型 POST

请求参数：当前时间往后推day

```json
{
	"day":5
}
```

相应参数：

```json
{
    "returnCode": "0000",
    "returnMsg": "Success",
    "nonceStr": "ef91dc354569456ca4d1ece81a43003d",
    "success": true,
    "data": [
        {
            "date": "20190920",
            "barGraphResults": [
                {
                    "contractName": "QA",
                    "count": 4
                },
                {
                    "contractName": "和谐共享社区",
                    "count": 0
                },
                {
                    "contractName": "QATB",
                    "count": 0
                },
                {
                    "contractName": "TEST",
                    "count": 0
                },
                {
                    "contractName": "项目7",
                    "count": 0
                },
                {
                    "contractName": "项目8",
                    "count": 0
                }
            ]
        },
        {
            "date": "20190921",
            "barGraphResults": [
                {
                    "contractName": "QA",
                    "count": 0
                },
                {
                    "contractName": "和谐共享社区",
                    "count": 0
                },
                {
                    "contractName": "QATB",
                    "count": 0
                },
                {
                    "contractName": "TEST",
                    "count": 0
                },
                {
                    "contractName": "项目7",
                    "count": 0
                },
                {
                    "contractName": "项目8",
                    "count": 0
                }
            ]
        },
        {
            "date": "20190922",
            "barGraphResults": [
                {
                    "contractName": "QA",
                    "count": 0
                },
                {
                    "contractName": "和谐共享社区",
                    "count": 0
                },
                {
                    "contractName": "QATB",
                    "count": 0
                },
                {
                    "contractName": "TEST",
                    "count": 0
                },
                {
                    "contractName": "项目7",
                    "count": 0
                },
                {
                    "contractName": "项目8",
                    "count": 0
                }
            ]
        },
        {
            "date": "20190923",
            "barGraphResults": [
                {
                    "contractName": "QA",
                    "count": 0
                },
                {
                    "contractName": "和谐共享社区",
                    "count": 0
                },
                {
                    "contractName": "QATB",
                    "count": 1
                },
                {
                    "contractName": "TEST",
                    "count": 0
                },
                {
                    "contractName": "项目7",
                    "count": 0
                },
                {
                    "contractName": "项目8",
                    "count": 0
                }
            ]
        },
        {
            "date": "20190924",
            "barGraphResults": [
                {
                    "contractName": "QA",
                    "count": 2
                },
                {
                    "contractName": "和谐共享社区",
                    "count": 0
                },
                {
                    "contractName": "QATB",
                    "count": 12
                },
                {
                    "contractName": "TEST",
                    "count": 0
                },
                {
                    "contractName": "项目7",
                    "count": 0
                },
                {
                    "contractName": "项目8",
                    "count": 0
                }
            ]
        },
        {
            "date": "20190925",
            "barGraphResults": [
                {
                    "contractName": "QA",
                    "count": 1
                },
                {
                    "contractName": "和谐共享社区",
                    "count": 0
                },
                {
                    "contractName": "QATB",
                    "count": 0
                },
                {
                    "contractName": "TEST",
                    "count": 0
                },
                {
                    "contractName": "项目7",
                    "count": 0
                },
                {
                    "contractName": "项目8",
                    "count": 0
                }
            ]
        }
    ]
}
```

说明：



### 2、用户统计

### 3、合约统计

#### 3.1 月上传量

描述：月上传量--本月的上传量与上个月上传量比较 （合约表）

请求参数：无

请求路径：http://127.0.0.1:8110/contract/month/total

/system/contract/month/total

请求类型：GET

返回参数：

```java
{
    "returnCode": "0000",
    "returnMsg": "Success",
    "nonceStr": "56c95d540c58420d92df2580129d34fe",
    "success": true,
    "data": {
        "thisMonthTotal": 10,
        "lastMonthTotal": 0,
        "diff": null
    }
}
```

说明

"diff": null 的情况用% 表示，前端判空

#### 3.2 月升级量

月升级量--本月的升级量与上个月升级量比较 （合约历史表）

请求参数：无

请求路径：http://127.0.0.1:8110/contract/history/month/total

/system/contract/history/month/total

请求类型：GET

返回参数：

```java
{
    "returnCode": "0000",
    "returnMsg": "Success",
    "nonceStr": "bf86d5391865417ebaca92ab12493c66",
    "success": true,
    "data": {
        "thisMonthTotal": 3,
        "lastMonthTotal": 0,
        "diff": null
    }
}
```

#### 3.3 合约部门分布

合约部门分布---查出合约量前n的部门，多于n个只返回n个，n为入参

请求参数：

```json
{
	"size":5
}
```

请求路径：http://127.0.0.1:8110/contract/organization/distribution

/system/contract/organization/distribution

请求类型：POST

返回参数：

```json
{
    "returnCode": "0000",
    "returnMsg": "Success",
    "nonceStr": "90e7bd9fdafc4183bc269428bca7d745",
    "success": true,
    "data": [
        {
            "organizationName": "QATB",
            "count": 6
        },
        {
            "organizationName": "QA",
            "count": 4
        }
    ]
}
```



#### 3.3 统计最近30天的合约量

统计最近30天的合约量--返回横纵坐标

请求参数：

```json
{
	"days":7
}
```

请求路径：http://127.0.0.1:8110/contract/total/lastDay

/system/contract/total/lastDay

请求类型：POST

返回参数：

```json
{
    "returnCode": "0000",
    "returnMsg": "Success",
    "nonceStr": "a3e48475c5cb4f649a1c2e8ad32c034a",
    "success": true,
    "data": [
        {
            "date": "2019/09/20",
            "count": 0
        },
        {
            "date": "2019/09/21",
            "count": 3
        },
        {
            "date": "2019/09/22",
            "count": 0
        },
        {
            "date": "2019/09/23",
            "count": 0
        },
        {
            "date": "2019/09/24",
            "count": 0
        },
        {
            "date": "2019/09/25",
            "count": 0
        },
        {
            "date": "2019/09/26",
            "count": 0
        }
    ]
}
```

#### 3.4 分页查询合约表

合约上传列表：分页查询合约表（SYSTEM_CONTRACT），入参有时间区间

请求参数：

```json
{
	"startTime":"20190826144804",
	"endTime":"20190926144804",
	"pageSize":10,
	"pageNum":1
}
```

请求路径：http://127.0.0.1:8110/contract/page

/system/contract/page

请求类型：POST

返回参数：

```json
{
    "returnCode": "0000",
    "returnMsg": "Success",
    "nonceStr": "17f42e6d013d43da94e4be89e6e8b8c8",
    "success": true,
    "data": {
        "total": 7,
        "pageCount": 1,
        "pageNum": 1,
        "pageSize": 10,
        "datas": [
            {
                "id": "624999693424078848",
                "number": "624999693424078849",
                "projectId": "618035918208512000",
                "createTime": "2019/09/21",
                "state": "0",
                "serverVersion": null,
                "fileBase64": null,
                "description": "import ",
                "name": "import"
            },
            {
                "id": "624996580000608256",
                "number": "624996580000608257",
                "projectId": "618035918208512000",
                "createTime": "2019/09/21",
                "state": "0",
                "serverVersion": "1.3",
                "fileBase64": null,
                "description": "package main",
                "name": "packagemain"
            },
            {
                "id": "624985102635843584",
                "number": "624985102635843585",
                "projectId": "618035918208512000",
                "createTime": "2019/09/21",
                "state": "0",
                "serverVersion": "11",
                "fileBase64": null,
                "description": "11",
                "name": "assad"
            },
            {
                "id": "619501302212210688",
                "number": "619501302212210689",
                "projectId": "619230915440160768",
                "createTime": "2019/09/06",
                "state": "0",
                "serverVersion": "1.2",
                "fileBase64": null,
                "description": "TEST",
                "name": "material"
            },
            {
                "id": "619232382746112000",
                "number": "619232382746112001",
                "projectId": "619230915440160768",
                "createTime": "2019/09/05",
                "state": "0",
                "serverVersion": "1.1",
                "fileBase64": null,
                "description": "TEST",
                "name": "Testf"
            },
            {
                "id": "619181767173091328",
                "number": "619181767173091329",
                "projectId": "619230915440160768",
                "createTime": "2019/09/05",
                "state": "0",
                "serverVersion": "1.3",
                "fileBase64": null,
                "description": "Test",
                "name": "Test"
            },
            {
                "id": "619136508674191360",
                "number": "619136508674191361",
                "projectId": "619230915440160768",
                "createTime": "2019/09/05",
                "state": "0",
                "serverVersion": "1.1",
                "fileBase64": null,
                "description": "QA",
                "name": "QATB"
            }
        ]
    }
}
```



#### 3.5 分页查询合约历史表

合约升级列表：分页查询合约历史表（SYSTEM_CONTRACT_HISTORY），查询结果CONTRACT_ID唯一

请求参数：

```json
{
	"startTime":"20190826144804",
	"endTime":"20190926144804",
	"pageSize":10,
	"pageNum":1
}
```

请求路径：http://127.0.0.1:8110/contract/history/page

/system/contract/history/page

请求类型：POST

返回参数：

```json
{
    "returnCode": "0000",
    "returnMsg": "Success",
    "nonceStr": "6af9c7eddd2b45a3b35136d1096b6c16",
    "success": true,
    "data": {
        "total": 3,
        "pageCount": 1,
        "pageNum": 1,
        "pageSize": 10,
        "datas": [
            {
                "id": "624998457849229312",
                "contractId": "624996580000608256",
                "projectId": "618035918208512000",
                "cteateTime": null,
                "installVersion": "1.1",
                "serverVersion": "1.1",
                "uniqueId": "f65f90e4c4ad425ab75f9812002760e6"
            },
            {
                "id": "624927740189282304",
                "contractId": "619501302212210688",
                "projectId": "618035918208512000",
                "cteateTime": null,
                "installVersion": "1.0",
                "serverVersion": "1.0",
                "uniqueId": "02aa80bb2c6d41edba2114ca4c87b926"
            },
            {
                "id": "001",
                "contractId": "001",
                "projectId": "001",
                "cteateTime": null,
                "installVersion": null,
                "serverVersion": "1.0",
                "uniqueId": "001"
            }
        ]
    }
}
```



### 4、业务统计

## 平台监控

## 系统管理