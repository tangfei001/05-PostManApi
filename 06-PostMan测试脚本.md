**1-Postman测试脚本**

1:Pre-request scripts
说明:调试脚本/预请求脚本
用法:预请求脚本是与发送请求之前执行的收集请求相关联的代码片段
举例:
      pm.globals.set("key",date.username);
pm.globals.set("value",date.password);
2:Tests
说明:测试脚本
用法:断言
举例:  
    1-常用的断言举例
   //响应状态码是200
pm.test("面包机", function () {
    pm.response.to.have.status(200);
});
//包含某一个字符串
pm.test("关键词包含", function () {
    pm.expect(pm.response.text()).to.include("全自动面包虾上浆裹面包糠机");
});
//验证是否超过200ms
pm.test("是否超过200ms", function () {
    pm.expect(pm.response.responseTime).to.be.below(200);
});
//检查JSON值
pm.test("Your test name", function () {
    var jsonData = pm.response.json();
    pm.expect(jsonData.username).to.eql("john");
});
//获取全局变量
pm.environment.get("username");
//设置一个全局变量
pm.environment.set("username", "password");