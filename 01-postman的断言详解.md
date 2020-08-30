**53-postman的断言详解**

/*序列化处理*/
var jsonData=JSON.parse(responseBody)     
/*验证协议状态码*/                          
pm.test("Status code is 200", function () {
    pm.response.to.have.status(200);
});

/*验证业务状态码*/
tests["验证业务状态码"]=jsonData.albumId===1214326777

/*数据断言*/
tests["验证nam的值"]=jsonData.data.name==="666666666666666666666"

说明:需要配合json在线工具使用



