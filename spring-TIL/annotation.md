# Annotation

- 스프링에서 제공하는 어노테이션을 정리한다.

## @SpringBootApplication

- Spring Boot 애플리케이션의 주 진입점을 나타냅니다.
- @Configuration, @EnableAutoConfiguration, @ComponentScan을 모두 포함합니다.

```java
@SpringBootApplication
public class Application {
    public static void main(String[] args) {
        SpringApplication.run(Application.class, args);
    }
}
```

## @Async

- 메서드가 비동기로 실행되어야 함을 나타냅니다.
- 메서드의 반환값은 Future 또는 ListenableFuture이어야 합니다.
- https://velog.io/@think2wice/Spring-Async-Thread-Pool%EC%97%90-%EB%8C%80%ED%95%98%EC%97%AC-Async

```java
@Service
public class MyService {
    @Async
    public Future<String> doSomething() {
        // ...
    }
}
```
