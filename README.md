# AsamF
AsamF是一款集成多个网络资产测绘平台的搜索工具


将Fofa、Zoomeye、Quake、Hunter集成在一起。

目前是第一版，之后有时间会进行改版，并且新增功能。有问题欢迎提issue

可以配置多个key

./AsamF 会自动生成配置文件，按照配置文件中的注释去填入key即可。

 使用Fofa无需提交其他参数。本程序会直接获取所有的搜索语句结果，但不超过10000条。
./AsamF -fofa 'body="网络空间测绘"'

<img width="810" alt="1" src="https://user-images.githubusercontent.com/53268974/182521912-9c610c35-b3a0-44c0-abab-e5a653546e31.png">

 使用hunter不添加 -p 参数将默认显示20条 使用-k 可以切换对应编号的hunter_key

./AsamF -hunter 'apache' 

<img width="300" alt="image" src="https://user-images.githubusercontent.com/53268974/182522115-22db18d7-bb88-492d-a8b8-26b66d9c0742.png">

./AsamF -quake 'apache' -k 3

 使用quake不添加 -p 参数将默认显示10条 使用-k 可以切换对应编号的quake_key

<img width="300" alt="image" src="https://user-images.githubusercontent.com/53268974/182522374-98403bc6-6d0f-4ba2-82fa-1fb469eb43f9.png">

 使用quake添加 -p 参数,指获取多少页数据。如 -p 10 会获取100条数据

./AsamF -quake 'apache' -p 10

<img width="300" alt="image" src="https://user-images.githubusercontent.com/53268974/182522495-fbdbe2e4-5029-4eba-bf07-330836db8cbd.png">

 使用zoomeye不添加 -p 参数将默认显示20条 使用-k 可以切换对应编号的quake_key

./AsamF -zoomeye 'apache' -k 2

<img width="300" alt="image" src="https://user-images.githubusercontent.com/53268974/182522915-03e1000d-7c91-4000-9e64-84d4982e06cf.png">

 使用quake添加 -p 参数,指获取多少页数据。如 -p 10 会获取10页里的200条数据

./AsamF -zoomeye 'apache' -p 10

<img width="300" alt="image" src="https://user-images.githubusercontent.com/53268974/182523097-ff861514-98eb-4126-ba83-92d74de48d4b.png">








