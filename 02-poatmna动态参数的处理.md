**55动态参数的处理**

处理思路:

		1:登录成功
		2:拿到返回的数据(jsonData)
        3:定义一个变量,吧返回的token存储在定义的变量中
应用:

if(jsonData.date.token)
{
    tests["获取toekn的值"]=true
    postman.setEnvironmentVariable("token",jsonData.date.token)
}
else
{
    tests["获取toekn失败"]=false
}

{{token}}

/*
集合:
    1:容器
    2:让接口用例有顺序的执行
*/
