# 联系方式
- 手机：18166334886
- Email：zyc199777@gmail.com
- QQ：1138613536

# 个人信息

 - 朱屹晨/男/1997 
 - 本科/重庆工程学院-软件工程(2015~2019)
 - 工作经验：2年
 - 期望职位：Java工程师
 - 期望薪资：8-10k

---

# 工作经历

## 北京雷云智链科技有限公司(2019.4~至今)
### 易捷运通
重庆一物流园区物流配送服务平台,类似于货拉拉。Spring Boot+Spring Cloud/Alibaba+Vue
- 企业/司机入驻：园区物流企业(Web)或者司机(APP)注册,手机验证码使用SMS服务,提交相关文件,上传到OSS,由园区负责人审核后入驻
- 客户发单：用户通过APP注册并实名认证后可发送需要物流配送需求,客户发单会提交出发地和目的地的坐标和行政代码信息,调用高德地图API获取线路规划信息,并预估费用,用户选择确定后下单成功。
即时订单即使推送,延时订单丢入RabbitMQ死信队列,先使用的RocketMQ,但他不支持任意延时时长
- 企业/司机接单：司机APP会不定时上传位置信息到ES中,用户推单后,通过ES的地理范围查询,匹配附近企业/司机,并推送信息,确认后接单成功
- 配送跟踪：司机APP不定时上传位置信息给服务器,调用高德地图API实时显示司机信息
- 管理界面：Vue+Element,企业/司机信息维护,订单维护,配送跟踪,使用EasyExcel让企业批量导入司机,Echarts展示日/月推单图、成交金额,数据报表   

整个项目采用SpringCloud搭建,注册/配置中心使用Nacos,网关SpringGateway,限流、熔断使用Sentinel。部署Jenkins+Docker
### 阳光福利商城

提供一站式企业员工福利解决方案的B2C电商平台,分为商城系统和运营平台,由PHP和Java联合开发。我负责Java模块
- 三方平台商品入库：平台和京东合作,京东提供接口,我们这边定时请求接口更新数据。使用SpringBoot+Quartz进行任务调度,并使用线程池请求API和处理结果。为解决数据库写入速度慢,加入RabbitMQ缓冲处理 
- 商品索引服务：SpringBoot+ELK,为商城提供的商品查询服务。最先通过SpringBatch查库入ES,后使用Logstash遇到问题后换用canal进行数据同步。使用http方式操作ES, 使用IK进行中文分词。Kibana进行ES管理 
- APP消息推送：SpringBoot+极光推送,主要为Android和IOS推送消息通知
- 三方平台下订单：Spring+RabbitMQ,PHP端下单后进入队列,这边监听处理,调用三方服务方提供的接口进行三方平台下单,补填订单信息,生成订单日志,回调PHP接口
- ADMIN界面：Vue+Element,三方平台商品分类和本地商品分类绑定,三方平台商品维护   

项目托管在SVN,部署在阿里云Centos7上,Java通过Jenkins+Maven+Docker进行发布,nginx负责转发。Vue项目用AlibabaCloudToolkit一键部署。

## 重庆跃医通科技有限公司 （ 2018.8 ~ 2019.4 ）

### 孕产妇保健系统 & 儿保系统
响应国家优生政策,为妇幼保健院开发的管理系统，有门诊管理,住院管理,转诊管理,儿童保健。SSM+Ehcache+shiro+JSP+Layui   
- 门诊负责孕妇的建档，检查，筛查。住院有产前检查，分娩管理和出生医学证明管理。儿保体检管理。   
三个模块职责类似，表单收集数据提交到后台进行数据校验,再CRUD数据库。难点在于表单多字段多,必须仔细,不能出错,如艾乙梅的检测结果录入错误,
后期会承担很大的责任。每个字段有正常值范围,有异常值(血常规/尿常规)要及时通知相关医生,及时治疗纠正。自动危险等级评定,病情跟踪等

---
# 技能清单
- 后端开发：SpringBoot/SpringCloud/SpringCloudAlibaba/AliyunBoot
- 前端开发：H5/Vue/JQuery/ES6
- 数据库相关：MySQL/ORACLE/Redis/ES/Mybatis/MybatisPlus
- 版本管理、文档和项目构建工具：Svn/Git/Maven/Gitee/Github/Jenkins/Docker
- 其他：RabbitMQ,RocketMQ,CentOS7,阿里云OSS、SMS、VOD
---
# 致谢
感谢您花时间阅读我的简历，期待能有机会和您共事。
