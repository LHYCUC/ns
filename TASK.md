# 题目说明

* 凡是标有[ ]符号的均为可选题目；
* 无序列表的第一级一般为研究题目或主题，二级、三级等内容为补充解释说明文字；
* 遵守国家、地方及相关行业和主管部门的法律和规定，不窃密、不篡改、不破坏；
* 是否问题，需要给出包括但不限于：详细论据、实验关键步骤和结果截图；
* 尊重他人的劳动成果和知识产权，给出必要的参考文献引用标注、第三方库引用声明等；


# 网络安全

## 安全方案设计

* [ ] 设计并实现一套双因素认证系统（默认已实现支持 用户名+密码 方式的身份认证）
  * 基于来源IP地址
  * 登录时发送二次确认电子邮件
    * 案例：linode的登录方式，需要把未知登录IP加入登录白名单
  * captcha机制
    * 基于浏览器JS执行
    * 基于图片验证码
  * OTP（智能手机APP方式）
  * 生物特征（可选）
    * 指纹、虹膜、声纹


## 逆向分析/点评

* [ ] 点评智能手机的指纹验证解锁
  * 对于原简单密码方式解锁的改进之处
  * 对于原简单密码方式解锁的存在的问题
  * 针对不同智能手机的指纹验证解锁机制的攻击方法、案例


* [ ] iptables规则题(TODO)
  * 给定一个iptables规则集合，让学生说明该规则可以实现网络访问控制规则应用效果
    * 给定一个数据包，让学生判断数据包最终是被：转发、丢弃、DENY、LOG、拒绝？

* [ ] 非图形验证码类CAPTCHA验证方式的原理和安全性分析？
  * geetest（极验）
  * 语音
  * 接收短信验证码
  * 编辑指定短信内容发送到指定号码
  * 电话回拨

* [ ] 网页屏幕键盘的原理和安全性分析？
  * 分析对象至少应包含以下2家：
    * 中传的一卡通在线充值转账系统
    * 建设银行个人网银登录
  * 对比直接使用物理键盘方式输入密码，屏幕键盘是否改进了安全性？请详细阐述理由。


## 研发与实验
* 反射型/放大器型DoS/DDoS攻击的原理与实验
  * 常见的可用于反射型DoS/DDoS攻击的协议有哪些？
    * [ ] DNS
    * [ ] ICMP
    * [ ] NTP
  * 如何防御？
* [ ] 基于HTTP协议的DoS/DDoS攻击的原理与实验
  * 如何防御？
* [ ] 你家的智能设备有哪些？
  * 典型被分析对象如下：
    * 路由器
    * 智能电视
    * 电视盒子
    * IP摄像头
    * 红外传感报警器
  * 使用的通信协议？
  * 通信内容是否加密？
  * 是否可以抵御重放攻击？
  * 端口开放情况如何？  
* [ ] HTTPS协议中间人攻击的可能性探究与实验
  * DNS查询泄漏（经由DNS解析服务器）与MITM
  * ARP欺骗与MITM
  * 伪造证书
  * 合法证书签名
* [ ] DNSSec协议详解，搭建支持DNSSec协议的DNS服务器，并详细说明协议的安全机理
* [ ] 搭建一个支持域名递归解析的DNS服务器，从全球13个根域名解析服务器同步所有TLD域名记录
* [ ] 反垃圾邮件检测服务搭建
  * 伪造发信人地址的可行性实践
  * 绕过垃圾邮件检测实践
  * 改进反垃圾邮件检测策略，检测出上一步的绕过手段
  * 改进垃圾邮件构造方法，绕过上一步的检测手段
* [ ] 开放网络服务信息收集实验
  * alexa全球排名top 10000的站点选择其一
  * 禁止使用任何方式直接扫描目标站点
  * 禁止对目标站点进行任何形式的渗透测试或攻击行为
  * 信息收集手段包括但不限于：搜索引擎搜索、whois查询、域名枚举、使用合法客户端连接目标端口等
  * 信息收集内容包括但不限于：子域名及其对应服务说明、IP地址段、电子邮件、组织结构信息、联系方式信息、公开的漏洞信息等
 

## 调研报告
* [ ] GMail将邮件中的所有图片、附件存储在自己的服务器上，有何安全意义？
* [ ] 公有云服务平台安全的过去、现在和将来
  * 列举并介绍全球（特别是中国）每年有影响力的安全事件
* [ ] IANA与互联网？
  * 域名管理机制
  * IP地址管理机制
  * 协议管理机制
  * 中文域名如何注册和解析？
* [ ] https站点如何启用CDN服务？
  * 是否一定要上传源站点的SSL证书私钥到CDN服务提供商？
    * 如果不是，请详细阐述解决方案及其原理。
      * ref: http://www.ruanyifeng.com/blog/2014/09/illustration-ssl.html


# 移动互联网安全

* [ ] 国内Android应用商城中程序隐私泄露分析
  * IMEI
  * IMSI
  * ICCID
  * 通讯录
  * 通话历史
  * 电话号码
  * 短信
  * 定位

* [ ] 你家的智能设备有哪些是安卓平台的？你能否做一次安全测试？
  * 是否开启了ADB网络调试功能
  * 能否获得root权限
  * 能否提取出固件？


