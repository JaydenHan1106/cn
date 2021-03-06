# restoreDatabaseFromFile


## 描述
从用户通过单库上云工具上传到云上的备份文件中恢复单个数据库<br>- 仅支持SQL Server

## 请求方式
POST

## 请求地址
https://rds.jdcloud-api.com/v1/regions/{regionId}/instances/{instanceId}/databases/{dbName}:restoreDatabaseFromFile

|名称|类型|是否必需|默认值|描述|
|---|---|---|---|---|
|**regionId**|String|True| |地域代码，取值范围参见[《各地域及可用区对照表》](../Enum-Definitions/Regions-AZ.md)|
|**instanceId**|String|True| |RDS 实例ID，唯一标识一个RDS实例|
|**dbName**|String|True| |库名称|

## 请求参数
|名称|类型|是否必需|默认值|描述|
|---|---|---|---|---|
|**sharedFileGid**|String|False| |共享文件的全局ID，可从上传文件查询接口[describeImportFiles](../Cloud-on-Single-Database/describeImportFiles.md)获取；如果该文件不是共享文件，则不用输入该参数|
|**fileName**|String|True| |用户上传的备份文件名称（包括文件后缀名），例如mydb1.bak|


## 返回参数
无


## 返回码
|返回码|描述|
|---|---|
|**200**|OK|

## 请求示例
POST
```
public void testRestoreDatabaseFromFile() {
    RestoreDatabaseFromFileRequest restoreDatabaseFromFileRequest = new RestoreDatabaseFromFileRequest();
    restoreDatabaseFromFileRequest.setDbName("test_db");
    restoreDatabaseFromFileRequest.setFileName("db1_1.bak");
    restoreDatabaseFromFileRequest.setSharedFileGid("fcbb66c6-e7f0-4228-b4c0-b3e5a0d452c8");
    restoreDatabaseFromFileRequest.setInstanceId("sqlserver-83uqv7avy4");
    restoreDatabaseFromFileRequest.setRegionId("cn-north-1");
    RestoreDatabaseFromFileResponse response = rdsClient.restoreDatabaseFromFile(restoreDatabaseFromFileRequest);
    System.out.println(new Gson().toJson(response));
}

```

## 返回示例
```
{
    "requestId": "bpa3v2q3s2fn4awhisgpopkt14uachka"
}
```
