Spring Boot 引入spring-boot-starter-data-jpa

1. Spring Boot 引入spring-boot-starter-data-jpa包报错, 解决：需要把pom文件重新加载一下
2. You must configure either the server or JDBC driver
   直接在mysql执行语句:  set global time_zone='+8:00'
或者：jdbc:mysql://localhost:3306/pms?characterEncoding=utf8&serverTimezone=UTC
3. 使用SpringBoot2中的Hibernate，配置文件application.properties文件中配置的是spring.jpa.properties.hibernate.dialect = org.hibernate.dialect.MySQL5Dialect，效果是Hibernate使用的是MyISAM（通过HeidiSQL查看）如果通过HeidiSQL手动建表，默认是InnoDB（查看MySQL配置文件my.ini配置也可以看到default-storage-engine=INNODB）。方言配置如下就行：
　　spring.jpa.properties.hibernate.dialect=org.hibernate.dialect.MySQL5InnoDBDialect
4. 
