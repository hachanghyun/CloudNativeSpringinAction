# CloudNativeSpringinAction
## 1.1 클라우드 네이티브란?
    클라우드 컴퓨팅 환경에서 현대적 애플리케이션을 구축, 배포 및 관리할 때의 소프트웨어 접근 방식

## 1.5 클라우드 네이티브를 사용하는 이유
### 1.5.1 속도
    소프트웨어를 더 신속하게 출시하는 것

### 1.5.2 복원력
    가용성이 좋음

### 1.5.3 확장성
    부하에 유연함, 로드밸런싱

### 1.5.4 비용
    온디맨드 방식으로 진행

## 2.1 클라우드 네이티브 개발원칙: 12요소와 확장
### 2.1.1 하나의 코드베이스, 하나의 애플리케이션
    애플리케이션과 코드베이스 사의 일대일 관계를 설정

### 2.1.2 API 우선
    API우선 접근 방식을 사용하면 분산 시스템에 적합하도록 시스템을 고려하고 서로 다른 팀 간의 업무를 분배 가능.

### 2.1.3 의존성 관리 
    애플리케이션의 모든 의존 라이브러리는 명시적인 방식으로 선언되어야 하며 이를 통해 의존라이브러리 관리 툴이 중앙 저장소에서 다운로드할 수 있어야 한다.

### 2.1.4 설계, 빌드, 릴리즈, 실행
    설계: 특정 애플리케이션 기능에 필요한 기술, 의존성 및 툴이 결정된다.
    빌드: 코드베이스를 컴파일하고 의존 라이브와 함께 패키지로 만들어 빌드라고 부르는 불가변 아티팩트를 생성한다.
    릴리즈: 배포하기 위해 빌드를 특정 설정과 결합한다.
    실행: 애플리케이션의 특정 릴리즈가 실행 환경에서 작동한다.

### 2.1.5 설정, 크리덴셜 및 코드
    설정에 대한 정의를 배포 사이에 변경될 가능성이 있는 모든 것. 애플리케이션의 설정을 변경해야 한다면 코드의 변경이나 애플리케이션의 재빌드 없이도 그렇게 할 수 있어야한다.

### 2.1.6 로그
    로그 수집기와 같은 외부 툴을 사용해 로그를 수집하고 검사할 수 있다.
    
### 2.1.7 일회성 
    부하가 많아지면 증가된 워크로드를 지원하기 위해 애플리케이션 인스턴스를 늘리면 된다. 언제라도 애플리케이션을 시작하거나 중지할 수 있는 경우를 일컬어 '이 애플리케이션은 일회성이다'라고 한다.

### 2.1.8 지원 서비스
    지원서비스는 어떤 애플리케이션이 자신의 기능을 제공하기 위해 사용하는 외부 리소스로 정의할 수 있다.

### 2.1.9 환경 동일성
    시간차이: 코드 변경 이후 배포까지의 기간은 상당히 클 수 있다.
    사람차이: 개발자는 애플리케이션을 만들고 운영자는 프로덕션에서 배포를 관리
    도구차이: 환경 간의 주요 차이점 중 하나는 지원 서비스를 처리하는 방법이다.

### 2.1.10 관리 프로세스
    데이터 마이그레이션, 배치 작업 또는 점검보수와 같은 작업은 일회성 프로세스로 처리, 애플리케이션 프로세스에 대해 수행한 것과 동일한 고려 사항이 관리 프로세스에도 적용된다. 

### 2.1.11 포트 바인딩
    애플리케이션 독립적 포트 바인딩을 통해 서비스 제공. 프로덕션에는 외부로 공개된 엔드포인트로 들어온 요청을 특정 포트에 바인딩 된 내부 서비스로 변환하는 라우팅 서비스가 가능하다.

### 2.1.12 상태를 갖지 않는 프로세스
    확장성을 보장하기 위해 애플리케이션이 상태를 갖지않는 프로세스가 되도록 설계하고 아무것도 공유하지 않는 아키텍처를 채택해야 하는데, 이는 애플리케이션 인스턴스 간에 상태를 공유해서는 안된다는 의미. 

### 2.1.13 동시성
    상태를 갖지 않도록 애플리케이션을 설계하는 것만으로는 확장성을 담보하기에 부족. 확장이 필요하다는 것은 더 많은 사용자에게 서비스 제공, 동시성을 통해 많은 사용자에게 서비스를 제공.

### 2.1.14 원격측정
    관측 가능성은 클라우드 네이티브 애플리케이션의 속성 중 하나다. 클라우드에서 분산 시스템을 관리하는 것은 복잡한데 이러한 복잡성을 관리할 수 있는 유일한 방법은 시스템의 작동을 원겨으로 모니터링 할 수 있도록 모든 구성 요소가 올바른 데이터를 제공하는 것이다.

### 2.1.15 인증 및 승인
    보안은 소프트웨어 시스템의 필수적인 특성 중 하나임에도 불구하고, 필요한 주목을 받지 못하는 경우가 많다. 제로 트러스트 접근법에 따라 시스템 내 상호작용의 안정성은 모든 설계적, 인프라적 수준에서 확보되어야 한다. 

## 2.2 스프링을 사용한 클라우드 네이티브 애플리케이션 구축
### 2.2.2 스프링 부트 애플리케이션 구축
#### 스프링웹
    스프링 MVC로 웹 애플리케이션을 빌드하는 데 필요한 라이브러리를 제공하며 임베디드 서버로는 기본 설정상 톰캣이 포함되어 있다.
#### 스프링부트 테스트 
    스프링 테스트, JUnit, 어서트J, 모키토를 포함해 애플리케이션을 테스트할 수 있는 여러 라이브러리 및 유틸리티를 제공한다. 

#### @SpringBootApplication 세가지 애너테이션 한꺼번에 포함
    @Configuration 해당 클래스가 빈을 정의하는 클래스임을 나타낸다.
    @ComponentScan을 사용하면 컴포넌트 검색을 통해 빈을 찾아 스프링 콘텍스트에 자동으로 등록한다.
    @EnableAutoConfiguration은 스프링 부트에서 제공하는 자동 설정 기능을 활성화한다. 

#### @RestController REST/HTTP 엔드포인트를 위한 핸들러를 정의하는 클래스로 인식
    @GetMapping("/") 루트엔드포인트로 GET요청을 처리

## 2.3 도커를 통한 애플리케이션 컨테이너화
### 2.3.1 도커소개: 이미지 및 컨테이너
    도커서버에는 도커데몬이 포함되어있는데 도커데몬은 백그라운드에서 실행하면서 이미지 컨테이너 볼륨 네트워크 같은 도커 객체를 만들고 관리
    도커데몬은 API를 제공하는데 이 API를 통해 컨테이너를 실행하거나 볼륨을 생성하는 것과 같은 명령을 도커에 전달할 수 있다.
    이 API를 사용해 데몬과 상호작용하는 것이 도커 클라이언트이다.
    컨테이너 포트포워딩이나 포트매핑이라는 프로세스를 통해 외부 세계에 자신의 서비스를 특정 포트로 노출할 수 있다.
![img](https://github.com/user-attachments/assets/29213102-2b3a-4317-bde6-b782595cfdac)

### 2.3.2 컨테이너를 통한 스프링 애플리케이션의 실행
    docker run --rm --name catalog-service -p 8080:8080 catalog-service:0.0.1-SNAPSHOT
    이미지에서 컨테이너를 실행한다.
    실행이 끝난후 컨테이너를 삭제한다.
    컨테이너의 이름
    8080포트를 통해 컨테이너 외부로 서비스를 노출한다.
    실행할 이미지의 이름과 버전

## 2.4 쿠버네티스로 컨테이너 관리
![kubernetes-model-architecture](https://github.com/user-attachments/assets/8160bd1c-debd-4a15-83b9-b9473f96b423)

### 2.4.2 쿠버네티스에서 스프링 애플리케이션 실행 
    minikube image load catalog-service:0.0.1-SNAPSHOT
    수동작업을 통해 로컬 클러스터로 스프링부트 이미지 가져오기

    kubectl create deployment catalog-service --image=catalog-service:0.0.1-SNAPSHOT
    쿠버네티스 deplyment 리소스 생성
    배포이름 설정
    실행할 이미지의 이름과 버전

    kubectl expose deployment catalog-service --name=catalog-service --port=8080
    쿠버네티스의 기본 설정으로는 파드로 실행중인 애플리케이션 액세스 X
    쿠버네티스 리소스를 노출
    노출할 리소스 유형
    노출할 배포의 이름
    서비스이름
    서비스를 노출할 포트 번호 

    kubectl port-forward sevice/catalog-service 8000:8080
    포트포워딩 명령 
    노출할 리소스 
    로컬호스트 포트 8000
    서비스포트 8080
    localhost:8000 으로 해당 서비스 조회

## 2.5 폴라 북솝: 클라우드 네이티브 애플리케이션
![IMG_6135](https://github.com/user-attachments/assets/d95f305e-61ba-4cbb-a157-d2b8d945032e)


### 2.5.2 프로젝트에서 사용되는 패턴과 기술
#### 1 웹과 상호작용
    RESTful 서비스 블로킹 방식: 전통적인 서블릿 방식, 논블로킹: 리액티브 프로그래밍 사용

#### 2 데이터
    스프링 데이터 JDBC(명령형) 와 스프링데이터 R2DBC(반응형)를 활용해 애플리케이션과 데이터 소스를 통합

#### 3 설정 
    스프링 클라우드 컨피그의 설정 서버를 통해 설정관리 중앙 집중화
    쿠버네티스 컨프그맵과 시크릿

#### 4 라우팅
    스프링 클라우드 게이트웨이를 사용해 API를 내부에서 변경하더라도 외부에 영향을 미치지 않도록 API 게이트웨이 역할을 하는 서비스를 구현

#### 5 관측가능성
    스프링 부트 액추에이터를 사용해 상태 및 정보 엔드포인트를 설정 한 후 마이크로미터에 측정값을 제공하고 이를 프로메테우스가 불러와 처리

#### 6 복원력 
    스프링 클라우드 서킷브레이커, 재시도, 타임아웃 구현

#### 7 보안
    인증 및 권한 부여 기능 
    스프링보안

#### 8 테스트 
    다양한 기능에 대한 테스트

#### 9 빌드 및 배포
    스프링 네이티브 및 그랄VM을 사용해서 스프링 애플리케이션을 네이티브 이미지로 컴파일
    깃허브액션으로 배포 파이프라인 구축 빌드 단계 자동화
    
### 3.1.2 그래들과 메이븐의 의존성 관리
    gradlew, mvnw라는 래퍼 스크립트로 의존성 관리 툴 실행
    
## 3.2 임베디드 서버로 작업
### 포트바인딩
    클라우드 네이티브 애플리케이션은 독립적이고 환경에 따라 설정 가능한 포트로 바인딩해서 서비스를 외부로 제공할 수 있다.

### 동시성
    JVM 애플리케이션에서는 사용할 수 있는 여러 스레드를 스레드 풀에 두고 동시성을 처리
    수평적 확장 선호: 인스턴스를 더 많이 배포하는 방식

### 3.2.2 요청당 스레드 모델 이해
![IMG_6131](https://github.com/user-attachments/assets/79383341-e176-4dc0-8149-0aafa20dccf1)

### 3.2.3 내장 톰캣 설정
    server.tomcat.connection-timeout: 클라이언트에서 TCP 연결을 수락하고 실제로 HTTP 요청을 받기까지 톰캣이 최대한 기다리는 시간 정의, 서비스 거부공격을 방지하는데 도움, 기본 20s, 2s가 적당
    server.tomcat.keep-alive-timeout: 새로운 HTTP 요청을 기다리는 동안 연결을 유지하는 시간 설정 
    server.tomcat.thread.max: 최대 요청 처리 스레드 수  설정
    server.tomcat.threads.min-spare: 풀에 항상 유지해야 하는 최소의 스레드 수 설정

## 3.3 스프링 MVC를 이용한 RESTful 애플리케이션 구축
### 도메인 개체 정의
    import javax.validation.constraints.NotBlank;
    import javax.validation.constraints.NotNull;
    import javax.validation.constraints.Pattern;
    import javax.validation.constraints.Positive;
    
    public record Book ( //도메인 모델은 불가변 객체인 레코드로 구현
    
        @NotBlank(message = "The book ISBN must be defined.")
        @Pattern(regexp = "^([0-9]{10}|[0-9]{13})$", message = "The ISBN format must be valid.")
        String isbn, // 고유하게 식별
    
        @NotBlank(message = "The book title must be defined.")
        String title,
    
        @NotBlank(message = "The book author must be defined.")
        String author,
    
        @NotNull(message = "The book price must be defined.")
        @Positive(message = "The book price must be greater than zero.")
        Double price
        
    ){}

### 애플리케이션의 사용 사례 구현
    package com.polarbookshop.catalogservice.domain;

    import org.springframework.stereotype.Service;
    
    @Service //스프링이 관리하는 서비스, 스테레오타입 애너테이션
    public class BookService {
    
        private final BookRepository bookRepository;
    
        public BookService(BookRepository bookRepository) {
            this.bookRepository = bookRepository; //BookRepository를 생성자 오토와이어링을 통해 제공
        }
    
        public Iterable<Book> viewBookList() {
            return bookRepository.findAll();
        }
    
        public Book viewBookDetails(String isbn) {
            return bookRepository.findByIsbn(isbn) //존재하지 않는 책을 보려고 할때, 그에 해당하는 예외발생
                    .orElseThrow(() -> new BookNotFoundException(isbn));
        }
    
        public Book addBookToCatalog(Book book) {
            if (bookRepository.existsByIsbn(book.isbn())) { //동일한 책을 여러번 추가할려고 시도하면 그에 해당하는 예외 발생
                throw new BookAlreadyExistsException(book.isbn());
            }
            return bookRepository.save(book);
        }
    
        public void removeBookFromCatalog(String isbn) {
            bookRepository.deleteByIsbn(isbn);
        }
    
        public Book editBookDetails(String isbn, Book book) {
    		return bookRepository.findByIsbn(isbn)
    				.map(existingBook -> {
    					var bookToUpdate = new Book( //책을 수정할 때 개체 식별자인 ISBN 코드를 제외한 모든 필드 수정 가능
    							existingBook.isbn(),
    							book.title(),
    							book.author(),
    							book.price());
    					return bookRepository.save(bookToUpdate);
    				})
    				.orElseGet(() -> addBookToCatalog(book)); //카탈로그에 존재하지 않는 책을 수정하려고 하면 새로운책 만듬.
        }
    
    }

### 데이터 액세스를 위해 리포지터리 추상화
    package com.polarbookshop.catalogservice.domain;

    import java.util.Optional;
    
    public interface BookRepository {
    	Iterable<Book> findAll();
    	Optional<Book> findByIsbn(String isbn);
    	boolean existsByIsbn(String isbn);
    	Book save(Book book);
    	void deleteByIsbn(String isbn);
    }

    package com.polarbookshop.catalogservice.persistence;

    import java.util.Map;
    import java.util.Optional;
    import java.util.concurrent.ConcurrentHashMap;
    
    import com.polarbookshop.catalogservice.domain.Book;
    import com.polarbookshop.catalogservice.domain.BookRepository;
    
    import org.springframework.stereotype.Repository;
    
    @Repository
    public class InMemoryBookRepository implements BookRepository {
    
    	private static final Map<String, Book> books = new ConcurrentHashMap<>();
    
    	@Override
    	public Iterable<Book> findAll() {
    		return books.values();
    	}
    
    	@Override
    	public Optional<Book> findByIsbn(String isbn) {
    		return existsByIsbn(isbn) ? Optional.of(books.get(isbn)) : Optional.empty();
    	}
    
    	@Override
    	public boolean existsByIsbn(String isbn) {
    		return books.get(isbn) != null;
    	}
    
    	@Override
    	public Book save(Book book) {
    		books.put(book.isbn(), book);
    		return book;
    	}
    
    	@Override
    	public void deleteByIsbn(String isbn) {
    		books.remove(isbn);
    	}
    }

### 도메인 오류를 알리기 위한 예외의 사용
    package com.polarbookshop.catalogservice.domain;

    public class BookAlreadyExistsException extends RuntimeException {
    
        public BookAlreadyExistsException(String isbn) {
            super("A book with ISBN " + isbn + " already exists.");
        }
    
    }

    package com.polarbookshop.catalogservice.domain;

    public class BookNotFoundException extends RuntimeException {
    
        public BookNotFoundException(String isbn) {
            super("The book with ISBN " + isbn + " was not found.");
        }
    
    }

### 3.3.2 스프링 MVC를 이용한 REST API 구현
![IMG_6136](https://github.com/user-attachments/assets/c5ce8005-728f-4c7c-bb5d-bb45b5f02a75)

    package com.polarbookshop.catalogservice.web;

    import javax.validation.Valid;
    
    import com.polarbookshop.catalogservice.domain.Book;
    import com.polarbookshop.catalogservice.domain.BookService;
    
    import org.springframework.http.HttpStatus;
    import org.springframework.web.bind.annotation.DeleteMapping;
    import org.springframework.web.bind.annotation.GetMapping;
    import org.springframework.web.bind.annotation.PathVariable;
    import org.springframework.web.bind.annotation.PostMapping;
    import org.springframework.web.bind.annotation.PutMapping;
    import org.springframework.web.bind.annotation.RequestBody;
    import org.springframework.web.bind.annotation.RequestMapping;
    import org.springframework.web.bind.annotation.ResponseStatus;
    import org.springframework.web.bind.annotation.RestController;
    
    @RestController //클래스가 스프링 컴포넌트이고 REST 엔드포인트를 위한 핸들러를 제공한다는 것을 표시하는 스테레오타입 애너테이션
    @RequestMapping("books") //클래스가 핸들러를 제공하는 루트패스 URL("/books")를 인식
    public class BookController {
    
        private final BookService bookService;
    
        public BookController(BookService bookService) {
            this.bookService = bookService;
        }
    
        @GetMapping //HTTP GET 메서드를 특정 핸들러 메서드로 연결
        public Iterable<Book> get() {
            return bookService.viewBookList();
        }
    
        @GetMapping("{isbn}") //루트 패스 URI에 추가되는 URI 템플릿 변수 ("/books/{isbn}")
        public Book getByIsbn(@PathVariable String isbn) { //@PathVariable은 메서드 변수를 IRL 템플릿 변수 {isbn} 와 바인드한다.
            return bookService.viewBookDetails(isbn);
        }
    
        @PostMapping
        @ResponseStatus(HttpStatus.CREATED) //책이 성공적으로 생성되면 201 상태코드로 반환한다.
        public Book post(@Valid @RequestBody Book book) { //RequestBody는 웹 요청의 본문을 메서드 변수로 바인드한다.
            return bookService.addBookToCatalog(book);
        }
    
        @DeleteMapping("{isbn}") //HTTP DELETE 요청을 특정 핸들러 메서드로 연결
        @ResponseStatus(HttpStatus.NO_CONTENT)
        public void delete(@PathVariable String isbn) {
            bookService.removeBookFromCatalog(isbn);
        }
    
        @PutMapping("{isbn}") 
        public Book put(@PathVariable String isbn, @Valid @RequestBody Book book) {
            return bookService.editBookDetails(isbn, book);
        }
    
    }

    HTTPie로 실행
    http POST : 9001/books author="Ha Chang Hyun" \
        title="Northern Lights" isbn="1234567891" price=9.90 # 책성성 요청

    http :9001/books/1234567891 #책 조회 요청

    
### 3.3.3 데이터 유효성 검사 및 오류 처리
    dependencies {
    ...
	implementation 'org.springframework.boot:spring-boot-starter-validation'
    }

    import javax.validation.constraints.NotBlank;
    import javax.validation.constraints.NotNull;
    import javax.validation.constraints.Pattern;
    import javax.validation.constraints.Positive;
    
    public record Book ( //도메인 모델은 불가변 객체인 레코드로 구현
    
        @NotBlank(message = "The book ISBN must be defined.")
        @Pattern(regexp = "^([0-9]{10}|[0-9]{13})$", message = "The ISBN format must be valid.") //이 필드는 주어진 정규 표헌식의 값과 일치하는 형식을 가져야 한다(표준ISBN 형식)
        String isbn, // 고유하게 식별
    
        @NotBlank(message = "The book title must be defined.") //이 필드는 널 값ㅇ ㅣ되어서는 안되고 화이트스페이스가 아닌 문자를 최소 하나 이상 있어야 한다.
        String title,
    
        @NotBlank(message = "The book author must be defined.")
        String author,
    
        @NotNull(message = "The book price must be defined.")
        @Positive(message = "The book price must be greater than zero.") //이 필드는 널 값이 되어서는 안되고 0보다 큰 값을 가져야 한다.
        Double price
        
    ){}

        @PostMapping
        @ResponseStatus(HttpStatus.CREATED) 
        public Book post(@Valid @RequestBody Book book) { //@Valid 애너테이션 추가
            return bookService.addBookToCatalog(book);
        }
    
        @PutMapping("{isbn}") 
        public Book put(@PathVariable String isbn, @Valid @RequestBody Book book) { //@Valid 애너테이션 추가
            return bookService.editBookDetails(isbn, book);
        }

#### 예외를 어떻게 처리할지 정의하는 어드바이스 클래스
    package com.polarbookshop.catalogservice.web;

    import java.util.HashMap;
    import java.util.Map;
    
    import com.polarbookshop.catalogservice.domain.BookAlreadyExistsException;
    import com.polarbookshop.catalogservice.domain.BookNotFoundException;
    
    import org.springframework.http.HttpStatus;
    import org.springframework.validation.FieldError;
    import org.springframework.web.bind.MethodArgumentNotValidException;
    import org.springframework.web.bind.annotation.ExceptionHandler;
    import org.springframework.web.bind.annotation.ResponseStatus;
    import org.springframework.web.bind.annotation.RestControllerAdvice;
    
    @RestControllerAdvice //클래스가 중앙식 예외 핸들러임을 표시
    public class BookControllerAdvice {
    
        @ExceptionHandler(BookNotFoundException.class) //이 핸들러가 실행되어야 할 대상인 예외 정의
        @ResponseStatus(HttpStatus.NOT_FOUND)
        String bookNotFoundHandler(BookNotFoundException ex) {
            return ex.getMessage(); //HTTP 응답 본문에 포함할 메시지
        }
    
        @ExceptionHandler(BookAlreadyExistsException.class)
        @ResponseStatus(HttpStatus.UNPROCESSABLE_ENTITY) //예외를 발생할떄 GHTTP 응답에 포함할 상태코드 정의
        String bookAlreadyExistsHandler(BookAlreadyExistsException ex) {
            return ex.getMessage();
        }
    
        @ExceptionHandler(MethodArgumentNotValidException.class)
        @ResponseStatus(HttpStatus.BAD_REQUEST)
        public Map<String, String> handleValidationExceptions(MethodArgumentNotValidException ex) { //책 데이터 유효성 검증이 실패한 경우 발생하는 예외 처리
            var errors = new HashMap<String, String>();
            ex.getBindingResult().getAllErrors().forEach(error -> {
                String fieldName = ((FieldError) error).getField();
                String errorMessage = error.getDefaultMessage();
    			errors.put(fieldName, errorMessage); //빈 메시지 대신 의미 있는 오류 메시지를 위해 유효하지 않은 필드 확인
            });
            return errors;
        }
    
    }

     
## 3.4 스프링 RESTful 애플리케이션 테스트
### 3.4.1 JUnit5를 이용한 단위테스트
	package com.polarbookshop.catalogservice.domain;

	import java.util.List;
	import java.util.Set;
	import java.util.stream.Collectors;
	
	import javax.validation.ConstraintViolation;
	import javax.validation.Validation;
	import javax.validation.Validator;
	import javax.validation.ValidatorFactory;
	
	import org.junit.jupiter.api.BeforeAll;
	import org.junit.jupiter.api.Test;
	
	import static org.assertj.core.api.Assertions.assertThat;
	
	class BookValidationTests {
	
	    private static Validator validator;
	
	    @BeforeAll //클래스 내의 테스트를 실행하기 전에 가장 먼저 실행할 코드 블록임을 나타낸다.
	    static void setUp() {
	        ValidatorFactory factory = Validation.buildDefaultValidatorFactory();
	        validator = factory.getValidator();
	    }
	
	    @Test //테스트케이스임을 나타낸다.
	    void whenAllFieldsCorrectThenValidationSucceeds() {
	        var book = new Book("1234567890", "Title", "Author", 9.90); //유효한 ISBN으로 책을 생성한다.
	        Set<ConstraintViolation<Book>> violations = validator.validate(book);
	        assertThat(violations).isEmpty(); //유효성 검사에서 오류가 없음을 확인한다.
	    }
	
	    @Test
	    void whenIsbnNotDefinedThenValidationFails() {
	        var book = new Book("", "Title", "Author", 9.90); //유효하지 않은 ISBN코드로 책을 생성한다.
	        Set<ConstraintViolation<Book>> violations = validator.validate(book);
	        assertThat(violations).hasSize(2);
	        List<String> constraintViolationMessages = violations.stream()
	                .map(ConstraintViolation::getMessage).collect(Collectors.toList());
	        assertThat(constraintViolationMessages)
	                .contains("The book ISBN must be defined.")
	                .contains("The ISBN format must be valid."); //유효성 검사 제약 조건 위반이 잘못된 ISBN에 대한 것인지 확인한다.
	    }
	
	    @Test
	    void whenIsbnDefinedButIncorrectThenValidationFails() {
	        var book = new Book("a234567890", "Title", "Author", 9.90);
	        Set<ConstraintViolation<Book>> violations = validator.validate(book);
	        assertThat(violations).hasSize(1);
	        assertThat(violations.iterator().next().getMessage())
	                .isEqualTo("The ISBN format must be valid.");
	    }
	
	    @Test
	    void whenTitleIsNotDefinedThenValidationFails() {
	        var book = new Book("1234567890", "", "Author", 9.90);
	        Set<ConstraintViolation<Book>> violations = validator.validate(book);
	        assertThat(violations).hasSize(1);
	        assertThat(violations.iterator().next().getMessage())
	                .isEqualTo("The book title must be defined.");
	    }
	
	    @Test
	    void whenAuthorIsNotDefinedThenValidationFails() {
	        var book = new Book("1234567890", "Title", "", 9.90);
	        Set<ConstraintViolation<Book>> violations = validator.validate(book);
	        assertThat(violations).hasSize(1);
	        assertThat(violations.iterator().next().getMessage())
	                .isEqualTo("The book author must be defined.");
	    }
	
	    @Test
	    void whenPriceIsNotDefinedThenValidationFails() {
	        var book = new Book("1234567890", "Title", "Author", null);
	        Set<ConstraintViolation<Book>> violations = validator.validate(book);
	        assertThat(violations).hasSize(1);
	        assertThat(violations.iterator().next().getMessage())
	                .isEqualTo("The book price must be defined.");
	    }
	
	    @Test
	    void whenPriceDefinedButZeroThenValidationFails() {
	        var book = new Book("1234567890", "Title", "Author", 0.0);
	        Set<ConstraintViolation<Book>> violations = validator.validate(book);
	        assertThat(violations).hasSize(1);
	        assertThat(violations.iterator().next().getMessage())
	                .isEqualTo("The book price must be greater than zero.");
	    }
	
	    @Test
	    void whenPriceDefinedButNegativeThenValidationFails() {
	        var book = new Book("1234567890", "Title", "Author", -9.90);
	        Set<ConstraintViolation<Book>> violations = validator.validate(book);
	        assertThat(violations).hasSize(1);
	        assertThat(violations.iterator().next().getMessage())
	                .isEqualTo("The book price must be greater than zero.");
	    }
	
	}

 	$ ./gradlew test --tests BookValidationTests

### 3.4.2 @SpringBootTEst를 통한 통합 테스트




 

