# Springboot 集成 H2 , JPA 的Demo

H2内存数据库的应用，jpa的使用 test

# JPA简介

>`JPA`本身并不是一种框架，是一种规范，其全称是`Java Persistence API`，是是Sun官方提出的Java持久化规范，而他的出现主要是为了简化现有的持久化开发工作和整合ORM技术，并且其是在充分吸收了现有Hibernate，TopLink，JDO等ORM框架的基础上发展而来的，具有易于使用，伸缩性强等优点。
>而官网对`spring data jpa`是这么介绍的：`Spring Data JPA`是`Spring Data`系列的一部分，可以轻松实现基于JPA的存储库。该模块处理对基于JPA的数据访问层的增强的支持。这使得使用数据访问技术构建Spring供电的应用程序变得更加容易。
>`Spring Data JPA`旨在通过减少实际需要的数量来显着提高数据访问层的实现。作为开发人员，您编写存储库接口（包括自定义查找器方法），Spring将自动提供实现。

# 什么是H2 database？
>H2是一个短小精干的嵌入式数据库引擎，主要的特性包括：
>
>1、免费、开源、快速；
>
>2、嵌入式的数据库服务器，支持集群；
>
>3、提供JDBC、ODBC访问接口，提供基于浏览器的控制台管理程序；
>
>4、Java编写，可使用GCJ和IKVM.NET编译；
>
>、短小精干的软件，1M左右。


# 遇到的问题

    1.只用H2的时候跑项目，在H2不能生成user表。其实是他们访问错了数据库。
    H2 内存数据库，设置 JDBC URL为 jdbc:h2:mem:testdb
    
    2.无法访问h2页面，需要在properties中开启h2控制台
    spring.h2.console.enabled=true

    3.当数据源被指定了，h2将不治被使用了