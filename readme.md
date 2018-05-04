# Springboot 集成 H2 , JPA 的Demo

H2内存数据库的应用，jpa的使用

# 问题

    1.只用H2的时候跑项目，在H2不能生成user表。其实是他们访问错了数据库。
    H2 内存数据库，设置 JDBC URL为 jdbc:h2:mem:testdb
    
    2.无法访问h2页面，需要在properties中开启h2控制台
    spring.h2.console.enabled=true

    3.当数据源被指定了，h2将不治被使用了