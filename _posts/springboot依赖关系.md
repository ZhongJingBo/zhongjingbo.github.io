---
layout: post
title: "spring boot依赖关系"
date: 2026-10-10
---

## 入口
启动当前项目,生成spring容器;
···
public class AiAssistantApplication {
	public static void main(String[] args) {
		SpringApplication.run(AiAssistantApplication.class, args);
	}
}
···
 
Spring 根据 @SpringBootApplication 等配置，扫描指定包中的组件、创建对象，并根据依赖声明完成注入

main()：Java 程序入口。
SpringApplication.run(...)：执行启动过程，创建并初始化 Spring 容器。
@SpringBootApplication：声明这是启动配置类，启用自动配置、组件扫描等能力

。
1. @RestController controller注解,会认为是http请求处理组件;
2. @Service  Service,认为当前为业务处理组件
3. @Mapper 数据处理(数据库)
