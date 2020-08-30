postman接口测试实战

系统:停车王

ID:48
username:666666@240592
password:123456

实现的过程:

第一步:在postman中建立对应的用例集

第二步:使用charles或者谷歌浏览器进行抓包

第三步:对抓包的结果填入对应的接口

第四步:执行结果,并生成HTML报告
	前提条件:需要安装node.js 和 newman插件

	执行命令:
			newman run xxxxxxxxxx
			newman run xxxxxxxxxx -r html

测试中需要注意的重点

1:对于公共参数应使用公共数据分离的方式(03)

2:对于动态参数应使用动态参数的处理方式(02)  postman.setEnvironmentVariable("token".jsonData.date.xxx)
	
3:断言 : 
		对于json形式的数据应进行
		#序列化处理
		var jsonData=JSON.parse(reponseBody)
		#协议状态码验证
		#业务状态码
		tests["验证业务状态码"]=jsonData.albumId ===0
		#数据验证
		tests["验证数据的值"]=jsonData.date.name==="xxxx"



