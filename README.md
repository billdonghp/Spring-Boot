# Spring-Boot
1.pom.xml:
<dependency>
    <groupId>org.springframework.boot</groupId>
    <artifactId>spring-boot-starter-aop</artifactId>
</dependency>
<dependency>
    <groupId>org.aspectj</groupId>
    <artifactId>aspectjrt</artifactId>
</dependency>
<dependency>
    <groupId>org.aspectj</groupId>
    <artifactId>aspectjweaver</artifactId>
</dependency>
<dependency>
    <groupId>cglib</groupId>
    <artifactId>cglib</artifactId>
    <version>2.1</version>
</dependency>
<dependency>
    <groupId>org.springframework</groupId>
    <artifactId>spring-aop</artifactId>
</dependency>

2.class HttpAspect
@Aspect
@Component
public class HttpAspect{}

@Pointcut("execution(public * com.mutliseafoods.msapp.controller.*.*(..))")
public void log(){}

@After("log()")
public void doAfter(){}
@Before("log()")
public void doBefore(){}
