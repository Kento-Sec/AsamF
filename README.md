# AsamF
AsamF是一款集成多个网络资产测绘平台的搜索工具

AsamF，Asset survey and mapping V0.1.1

本程序仅供学习研究使用，禁止利用本程序对相关平台或其他企业或个人造成任何利益侵害！

将Fofa、Zoomeye、Quake、Hunter集成在一起。

本程序可以单独使用上述平台，也可以同时调用4个平台，因为4个平台的语法格式不同，因此调用4个平台聚合搜索的选项不支持关键字组合搜索，也不是所有的选项均支持4个平台。

1. 优化各个平台的取key，通过 -fk -hk -qk -zk 可以分别取key；

2. 新增了判断ip是否为蜜罐功能；

3. -domian、-app、-host、-title、-port、-server、-ih 这几个选项会聚合平台来搜索。具体见-h描述。

4. -fofatotal 可以配合 -fields 使用，默认值为title。

5. -zoomeyedomain 可以配合'-rs 1' 进行关联查询，默认不关联。

6. 修改了取数据方式。会根据查询数据结果数量来获取结果。使用Zoomeye、Quake、Hunter没有进行限制，因此存在结果数量太大，会一直获取到apikey的额度为0，使用时请注意。fofa不存在该问题。

7. 新增info功能，可以查询各个账户的信息。hunter不支持


<img width="1000" alt="image" src="https://user-images.githubusercontent.com/53268974/182889524-42832701-6557-4162-83cf-30f4e0415f04.png">

<img width="500" alt="image" src="https://user-images.githubusercontent.com/53268974/182890438-246e67cc-ce0b-4d18-97d8-5fb9be7df87f.png">

<img width="300" alt="image" src="https://user-images.githubusercontent.com/53268974/182890536-e7b56ed3-8c2e-46ff-8e39-a920b2a7a406.png">

<img width="800" alt="image" src="https://user-images.githubusercontent.com/53268974/182890860-5a7c58ef-742d-4406-9b28-3211b21dcd9f.png">


<img width="500" alt="image" src="https://user-images.githubusercontent.com/53268974/182896433-c1e87adc-1927-40a5-be70-ee5da46e2da9.png">

<img width="500" alt="image" src="https://user-images.githubusercontent.com/53268974/182896763-729d02ba-b8a5-4598-95b6-64c8d306e636.png">

<img width="500" alt="image" src="https://user-images.githubusercontent.com/53268974/182897101-196c0cd4-5520-464e-b184-2c8438572471.png">

<img width="500" alt="image" src="https://user-images.githubusercontent.com/53268974/182896763-729d02ba-b8a5-4598-95b6-64c8d306e636.png">





自行研究吧...

未来新增功能：

1. 补充iu功能，icon url搜索功能；

2. 批量搜索功能；

3. quake接口功能。






