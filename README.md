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
![img](https://github.com/user-attachments/assets/29213102-2b3a-4317-bde6-b782595cfdac)
    컨테이너 포트포워딩이나 포트매핑ㅇ이라는 프로세스를 통해 외부 세계에 자신의 서비스를 특정 포트로 노출할 수 있다.

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

    

