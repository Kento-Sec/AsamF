# AsamF
AsamF是一款集成多个网络资产测绘平台的搜索工具

AsamF，Asset survey and mapping 

本程序仅供学习研究使用，请勿利用本程序损害任何个人或企业的利益，造成一切影响，开发者将不承担任何责任！

请勿滥用本程序，使用本程序将默认遵守各个平台方的所有条款。

--------------------------------------------------------------------------------------------------------------------

V0.1.4版本更新

1.  优化了shoda myip以及ds的格式输出；

2. 增加了masscan端口扫描功能，目前该功能比较鸡肋，只会扫预设的常见端口；

3. 集成了subfinder子域名收集功能。


todo：

1. 优化配置文件

2. 优化端口扫描

3. 增加c段扫描

--------------------------------------------------------------------------------------------------------------------

V0.1.3版本更新


1. 修复了生成json配置文件的问题。


2. 增加shodan功能。其中-option、-facets是作为shodan查询的重点辅助选项：


<img width="1200" alt="image" src="https://user-images.githubusercontent.com/53268974/187390516-a8ceba15-5c52-4e56-85c3-ff44459f6a2c.png">


查询我的ip信息：


<img width="760" alt="image" src="https://user-images.githubusercontent.com/53268974/187396935-6092d06f-5c19-4b4d-8c3d-e886c128cfd3.png">




查看shodan 账户info：


<img width="600" alt="image" src="https://user-images.githubusercontent.com/53268974/187390813-96d312f3-48e6-4db3-8a25-174394b47bac.png">


查看shodan api info：


<img width="600" alt="image" src="https://user-images.githubusercontent.com/53268974/187391063-956d91a1-72d1-4980-88dd-21a902fa98cd.png">


查看shodan最受欢迎的标签:


<img width="600" alt="image" src="https://user-images.githubusercontent.com/53268974/187391433-71a3f644-1ae2-45e8-a301-b432e02f3a75.png">


常规查询：


<img width="767" alt="image" src="https://user-images.githubusercontent.com/53268974/187391753-06b1e66b-561c-4334-9eea-4f33c0245126.png">


-option选项:


-option选择请输入英文首字母缩写。包括：hi、dd、ds、dr、p。目前仅支持5个参数。


hi: hostip,hostinformatio。主机信息查询。


<img width="741" alt="image" src="https://user-images.githubusercontent.com/53268974/187393775-e9d73c67-50e0-470f-82b1-0cbf032e7990.png">


dd:dnsdomain,Domain Information。获取给定域的所有子域和其他DNS条目。每次查找使用1个查询信用。该功能需要成为member才能使用。


<img width="770" alt="image" src="https://user-images.githubusercontent.com/53268974/187393909-af458960-5186-4719-b63c-ffe5149b0436.png">


ds:dnsresolve,DNS Lookup。在提供的主机名列表中查找IP地址，支持输入多个主机名，以“,”隔开。


<img width="781" alt="image" src="https://user-images.githubusercontent.com/53268974/187393199-408cd51e-93b6-4d40-82fe-93b786ee8332.png">

<img width="781" alt="image" src="https://user-images.githubusercontent.com/53268974/187393587-a94bc585-fd3c-4367-ae61-ec0601458b45.png">




dr:dnsreverse,Reverse DNS Lookup。查找已为给定IP地址列表定义的主机名。该功能需要成为member才能使用。


<img width="782" alt="image" src="https://user-images.githubusercontent.com/53268974/187394497-f8b2b926-bd71-41ec-a98f-d2177fab9e41.png">



p:port,Filtered by Ports 。该功能需要成为member才能使用。


AsamF -shodan '7001' -option p





-facets 选择是作为shodan高级搜索的选项。该功能需要成为member才能使用。


如：asn、domain、city、device、ip、isp、org、os、vuln、tag、version等等。请自行研究。

example： AsamF -shodan 'xxxx' -facets ip

一个小小的组合使用例子：

<img width="834" alt="image" src="https://user-images.githubusercontent.com/53268974/187396605-b3ff5276-9c82-41b1-aaf9-02db2ac03295.png">







--------------------------------------------------------------------------------------------------------------------


V0.1.2版本更新

<img width="600" alt="image" src="https://user-images.githubusercontent.com/53268974/186801668-0c219244-af1c-439c-a09b-1ae4f330f254.png">


1.增加爱企查通过公司名称查域名功能；

调用： -cn 。例子：

<img width="600" alt="image" src="https://user-images.githubusercontent.com/53268974/186683784-35304bd9-3f49-4343-b9f7-d6f30b81f817.png">



2.增加爱企查批量公司名查询域名功能；


调用： -cnf 。例子：


<img width="600" alt="image" src="https://user-images.githubusercontent.com/53268974/186684330-86f2500f-aa0b-4a13-b312-c1f0c94f1704.png">



3.增加爱企查通过公司名查备案信息、分支机构、控股公司占比及域名信息功能；


调用： -aqc。例子：


获取到的控股公司会再次获取该公司的域名信息。


<img width="600" alt="image" src="https://user-images.githubusercontent.com/53268974/186685845-30e5f3d0-9fe0-4a5a-8dcd-b4021abbd615.png">


<img width="600" alt="image" src="https://user-images.githubusercontent.com/53268974/186685950-aa477a08-b06d-4dc8-8cbd-47d513badb38.png">





4.增加fofa排除蜜罐功能。由于fofa政策修改，该功能目前企业会员才能支持。


无法演示，因为我也没有企业会员。


调用：-e 1来使用。例子：


./AsamF -fofa 'xxx' -e 1


5. 刚刚加了fofa搜索本地icon以及url搜索icon功能。


<img width="600" alt="image" src="https://user-images.githubusercontent.com/53268974/186802079-a89738b4-ca5d-4516-840b-368e7710c436.png">



本次更新修改了配置文件的格式为json

需要将爱企查的cookie添加到配置文件中'aiqicha'中。



--------------------------------------------------------------------------------------------------------------------



将Fofa、Zoomeye、Quake、Hunter集成在一起。

本程序可以单独使用上述平台，也可以同时调用4个平台，因为4个平台的语法格式不同，因此调用4个平台聚合搜索的选项不支持语法组合使用，也不是所有的选项均支持4个平台，-h有说明。

1. 优化各个平台的取key，通过 -fk -hk -qk -zk 可以分别取key；

2. 新增了判断ip是否为蜜罐功能；

3. -domian、-app、-host、-title、-port、-server、-ih 这几个选项会聚合平台来搜索。具体见-h描述。

4. -fofatotal 可以配合 -fields 使用，默认值为title。

5. -zoomeyedomain 可以配合'-rs 1' 进行关联查询，默认不关联。

6. 修改了取数据方式。会根据查询数据结果数量来获取结果。使用Zoomeye、Quake、Hunter没有进行限制，因此存在结果数量太大，会一直获取到apikey的额度为0，使用时请注意。fofa不存在该问题,最多10000条数据。

7. 新增info功能，可以查询各个账户的信息。hunter不支持


<img width="1000" alt="image" src="https://user-images.githubusercontent.com/53268974/182889524-42832701-6557-4162-83cf-30f4e0415f04.png">

<img width="600" alt="image" src="https://user-images.githubusercontent.com/53268974/182890438-246e67cc-ce0b-4d18-97d8-5fb9be7df87f.png">

<img width="400" alt="image" src="https://user-images.githubusercontent.com/53268974/182890536-e7b56ed3-8c2e-46ff-8e39-a920b2a7a406.png">

<img width="600" alt="image" src="https://user-images.githubusercontent.com/53268974/182890860-5a7c58ef-742d-4406-9b28-3211b21dcd9f.png">


<img width="600" alt="image" src="https://user-images.githubusercontent.com/53268974/182896433-c1e87adc-1927-40a5-be70-ee5da46e2da9.png">

<img width="600" alt="image" src="https://user-images.githubusercontent.com/53268974/182896763-729d02ba-b8a5-4598-95b6-64c8d306e636.png">



-fofahost 主机搜索

<img width="600" alt="image" src="https://user-images.githubusercontent.com/53268974/182976108-7cbbc2b7-01b9-426f-afbe-33511b3faf06.png">

-fofatotal 聚合功能

<img width="600" alt="image" src="https://user-images.githubusercontent.com/53268974/182976932-217db434-183a-4665-8134-75730837b109.png">


<img width="600" alt="image" src="https://user-images.githubusercontent.com/53268974/182976418-58d63eb4-dba3-4a06-b780-2e99b58a0593.png">


<img width="600" alt="image" src="https://user-images.githubusercontent.com/53268974/182976418-58d63eb4-dba3-4a06-b780-2e99b58a0593.png">

-zoomeyehost 

<img width="600" alt="image" src="https://user-images.githubusercontent.com/53268974/182976526-61842fc5-4bb7-47d0-b07a-3d7301183ad6.png">

-zoomeyeweb

<img width="811" alt="image" src="https://user-images.githubusercontent.com/53268974/182977121-44d17fcf-85ad-4ebe-96ec-08ac7351856d.png">


-zoomeyedomain

<img width="600" alt="image" src="https://user-images.githubusercontent.com/53268974/182976855-bec3ee36-bc2d-40f4-a947-a2822060b754.png">



自行研究吧...

未来还会新增一些功能







