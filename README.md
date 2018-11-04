# spring-cloud-sys
spring-cloud-生态系统搭建

使用spring-boot-admin监控服务状态，并发送邮件提示




官网文档:

		Version 1.5.7:http://codecentric.github.io/spring-boot-admin/1.5.7/

    	Version 2.0.4:http://codecentric.github.io/spring-boot-admin/2.0.4/
gitbub源代码

		https://github.com/codecentric/spring-boot-admin


运行项目步骤：
step 1

	1.下载此项目[spring-cloud-monitor]，直接导入eclipse maven项目
	  直接使用mvn命令也可 [ mvn clean compile package spring-boot:run]

	2.修改项目resource目录下 application.properties 文件的 eureka 和 mail 信息即可
step 2

	启动一个eureka注册中心[spring-cloud-eureka]
step 3

	启动被监控的微服务 [spring-cloud-service-1]
	需要在 pom.xml 中加入
	<dependency>
	    <groupId>org.springframework.boot</groupId>
	    <artifactId>spring-boot-starter-actuator</artifactId>
	</dependency>
step 4

	启动以上服务
	访问spring-boot-admin项目 http://localhost:7002/#/ 
