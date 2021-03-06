任务目的
加强对JavaScript的掌握
熟悉常用表单处理逻辑
任务描述
如示例图中所示，基于上一个任务，在页面中添加多个表单
要求:
表单获得焦点时，下方显示表单填写规则
表单失去焦点时校验表单内容
校验结果正确时，表单边框显示绿色，并在下方显示验证通过的描述文字
校验结果错误时，表单边框显示红色，并在下方显示验证错误的描述文字
点击提交按钮时，对页面中所有输入进行校验，校验结果显示方式同上。若所有表单校验通过，弹窗显示“提交成功”，否则显示“提交失败”
任务注意事项
要求功能实现与任务描述中完全一致
示例图仅为参考，样式不需要完全实现一致
实现中，尽可能考虑代码的可读性和可复用性
请注意代码风格的整齐、优雅
代码中含有必要的注释
不允许借助任何第三方组件库实现
在线学习参考资料
Web相关名词通俗解释
MDN HTML入门
慕课HTML+CSS基础教程视频
JavaScript 表单验证
HTML表单指南


正则表达式
举例：zhangsan-001@gmail.com 
分析邮件名称部分：

26个大小写英文字母表示为a-zA-Z
数字表示为0-9
下划线表示为_
中划线表示为-
由于名称是由若干个字母、数字、下划线和中划线组成，所以需要用到+表示多次出现
?根据以上条件得出邮件名称表达式：[a-zA-Z0-9_-]+ 


分析域名部分：

?一般域名的规律为“[N级域名][三级域名.]二级域名.顶级域名”，比如“qq.com”、“www.qq.com”、“mp.weixin.qq.com”、“12-34.com.cn”，分析可得域名类似“** .** .** .**”组成。

“**”部分可以表示为[a-zA-Z0-9_-]+
“.**”部分可以表示为\.[a-zA-Z0-9_-]+
多个“.**”可以表示为(\.[a-zA-Z0-9_-]+)+
?综上所述，域名部分可以表示为[a-zA-Z0-9_-]+(\.[a-zA-Z0-9_-]+)+

最终表达式： 
?由于邮箱的基本格式为“名称@域名”，需要使用“^”匹配邮箱的开始部分，用“$”匹配邮箱结束部分以保证邮箱前后不能有其他字符，所以最终邮箱的正则表达式为： 
??^[a-zA-Z0-9_-]+@[a-zA-Z0-9_-]+(\.[a-zA-Z0-9_-]+)+$

