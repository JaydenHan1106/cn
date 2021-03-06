# 新建监控任务 
1. 登录京东云云拨测控制台，点击“管理->云拨测->可用性监控”，进入可用性监控任务列表页面。点击左上角的“新建任务”按钮。  
![任务列表](../../../../../image/Cloud-Detection/task-usa-list.png)
2. 设置任务的名称、选择作为探测源的云主机、设置探测目标，其相关信息如下:
- 目标类型支持 URL/IP 或 云数据库RDS
- 选择探测协议，URL/IP 支持HTTP(S)和TELNET 探测， 云数据库RDS仅支持TELNET方式进行探测
- 设置探测目标  
a. 探测目标为URL/IP类型，协议为HTTP(S)时，输入IP地址或域名若为TELNET协议时还需输入探测端口号。若为HTTP(S)时可以选择请求方式，同时高级配置中可配置请求所带HTTP请求头、Cookie信息  
b. 探测目标为云数据库RDS类型时, 探测协议仅为TELNET，探测目标选择当前已创建的RDS数据库。  
注：目标类型为云数据库RDS时，是对数据库的内网域名地址进行探测。
- 若为HTTP(S)，可以支持配置HTTP请求头、Cookie信息，若为Post请求方式时，还支持设置body部分的内容信息。  

![新建任务](../../../../../image/Cloud-Detection/create-task-usa.png)

3. 点击“确定”按钮，保存监控任务  

# 修改监控任务  
1. 登录京东云云拨测控制台，点击“管理->云拨测->可用性监控”，进入可用性监控任务列表页面。选中需要修改的可用性监控任务，点击操作列下更多->修改按钮，进入修改可用性监控任务页面。  

2. 可修改监控任务的名称、探测源信息、探测目标地址（探测目标类型、探测协议不允许修改）、HTTP(S)还可支持更改请求方式及高级配置。  
注：相关限定和要求可参考新建监控任务页面。  

3. 更改需要修改的信息后，点击“确定”按钮，保存监控任务。  

# 禁用/启用任务  
1. 登录京东云云拨测控制台，点击“管理->云拨测->可用性监控”，进入可用性监控任务列表页面。  
![任务列表](../../../../../image/Cloud-Detection/task-usa-list.png)
2. 选中需要禁用/启用的监控任务，点击操作列下更多->“禁用”/“启用”按钮即可。  
注：禁用任务之后，该监控任务会的探测任务和报警服务都会被停止。  

# 报警历史  
1. 登录京东云云拨测控制台，点击“管理->云拨测->可用性监控”，进入可用性监控任务列表页面。  
![任务列表](../../../../../image/Cloud-Detection/task-usa-list.png)
2. 选中需要查看报警的监控任务，点击“报警历史”按钮。跳转至全部报警历史->可用性监控页面，展示该监控任务近1天的报警情况，若需要查看其它时间段的报警历史，修改日期范围即可。  
![报警历史](../../../../../image/Cloud-Detection/alarmhistory-usa.png)

# 删除任务  
1. 登录京东云云拨测控制台，点击“管理->云拨测->可用性监控”，进入监控任务列表页面。  
![任务列表](../../../../../image/Cloud-Detection/task-usa-list.png)
2. 选中要删除的监控任务，点击操作列下的“更多->删除”按钮，或者选择任务前边的复选框，点击批量“删除”按钮。  
3. 在确认删除提示框中，点击“确定”按钮即可。
