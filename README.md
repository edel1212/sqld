### 모델링의 개념

- 현실 세계의 비지니스 프로세스와 데이터 요구 사항을 **추상적으로 구조화된 형태로 표현하는 과정**

### 모델링의 특징

- **단순화**
    - 불필요한 세부 사항을 **제거**
- **추상화**
    - 다양한 현상을 일정한 **양식인 표기법에 따라 표현**
    - 일정한 형식에 맞추어 **간략하고 대략적으로 표현**하는 과정
- **명확화**
    - **애매모함**을 최대한 **제거**하고 **정확하게 현상을 기술**하는 과정

### 데이터 모델링 유의점 [ 해당 방법을 피하자란 내용 - 비 유연성을 피하자 ]

- **중복**
    - **같은 데이터**를 저장하지 **않도록** 설계
- **비유연성**
    - 사소한 업무 변화에 대해서도 **잦은 모델이 변경 되지 않도록** 주의
- **비일관성**
    - 정보가 **모순**되거나 **상반된 내용**을 갖는 상태를 **없애자**
    - **상호연관 관계**를 **명확**히 정의해주자

### 데이터 모델링 3가지 요소

- **대상** : 업무가 관리하고자 하는 대상
- **속성** : 대상들이 갖는 속성
- **관계** : 대상들간의 관계

### 데이터 모델링의 3단계

- 개 -> 논 -> 물
    - **논리적** 모델은 **정규화 실행함** 관계 설정

### ERP란?

- 엔터티간의 **관계를 시각적으로 표현**한 다이어그램
- 왼쪽 -> 오른쪽 , 위 -> 아래
- 피터챈이 만듬

### ERD 작성 절차

- 엔터티 **도출 후 그린다**
- 엔터티 **배치**
- 엔터티간의 **관계 설정**
- 관계명 **서술**
- 관계 **참여도 기술**
- 관계 **필수 여부 확인**

### 엔터티 특징

- 업무에 **필요한**  정보 관리
- **인스턴스들**의 **집합**
    - **연속적**으로 존재하는 **2개 이상의 인스턴스의 집합 이어야 함**
- **반드시 속성**을 **가짐**
    - **엔터티**는 **2개 이상의 속성**을 가짐
    - 하나의 **인스턴스는** 각각의 **속성 들에 대한 1개의 값만** 을 가짐
- **다른 엔터티와** **최소 1개 이상**의 **관계를 성립**해야한 다.
    - 엔터티는 업무적 연관성을 갖고 다른 엔터티와 연관의 의미를가짐
    - 관계가 없는 엔터티 도출은 **부적잘한 엔터티**이거나 **적잘한 관계를 찾지** 못한 것

### 엔터티의 분류

- **유형 엔터티**
    - **물리적인 형태**가 있음 (**실체가 있는** 대상)
    - **업무**로 부터 **구분하기 가장 용이한 엔터티**
        - 사원, 물품, 감사
- **개념 엔터티**
    - **물리적인 형태**가 **없음**
    - 관리해야할 **개념적 정보로 부터 구분되는 엔터티**
        - 조직, 보험 상품
- **사건 엔터티**
    - **업무를 수행**에 따라 **발생하는 엔터티**
        - 주문, 청구, 미납
- **기본 엔터티**
    - **원래 존재**하던 정보
- **중심 엔터티**
    - 기본 엔티티로 부터 발생되고 **그 업무에서 중심적인 역할**
- **행위 엔터티**
    - **2개 이상**의 **부모 엔터티로 부터 발생**
        - 사원변경이력, 이력 과 같은 이력들

### 엔터티 명명 규칙

- **현업**에서 **사용하는 용어** 사용
- **약자** 사용 **자제**
- **단수 명사** 사용
- **유일하게** 이름 부여
- **생성 의미대**로 이름 부여

### 속성에 따른 분류

- 기본속성
- 설계속성
    - **코드**로 만들어버린거
- 파생 속성
    - **다른 속성**에 **의해 만들어진** 속성
        - 합계, 평균 등등

### 분해 여부에 따른 속성

- 단일 속성
    - **하나의 의미**로 **구성**된경우
        - 회원 ID
    - 복합 속성
        - **여러개의 의미**로 **구성**된 경우
            - 주소 (시, 구, 동 등 분해가능)
    - 다중 값 속성
        - **속성**에 **여러 개의 값**을 가질 수 있는 경우
            - 상품 리스트 등

### 관계의 종류

- 존재적 관계
    - 한 엔터티의 **존재가 다른 엔터티의 영향을 미치**는 관계
        - Ex) 부서 엔터티가 삭제되면 사원 엔터티의 존재에 영향을 미침
- 행위적 관계
    - 엔터티 간의 **어떤 행위가 있는 것**을 의미
        - Ex) 고객 엔터티의 행동에 의해 주문 엔터티가 발생함

### 관계의 구성

- 관계명
- 차수
- 선택성

### 관계의 페어링

- 엔터티 안에” 인스턴스”가 **개별적으로 관계**를 가지는것

### 관계, 차수 , 페어링 차이

- 관계 : 엔터티끼리의 관계
- 차수 :  **1:1: 1:N , N : M** 과 같은 것
- 페어링 : **인스턴스 끼리**의 **연결 고리**라 보면된다

### 식별자 분류

- 주 식별자
    - 메인 식별자이다 PK
- 보조 식별자
    - **유일성과 최소성을 만족**하지만 **선택 받지 못한** 친구
- 내부 식별자
    - 다른 **엔터티 참조 없이 내부**에서 **스스로 생성**되는 식별자
- 외부식별자
    - 다른 엔터티와 관계로 인해 만들어진 식별자 (FK)
- 단일 식별자
    - **하나의 속성**으로 구성
- 복합 식별자
    - **2개 이상의 속성**으로 구성
- 본질 식별자
    - **비즈니스 프로세스**에 의해 **만들어짐**
- 인조 식별자
    - 시퀀스 번호 처럼 **일련번호**

### 주 식별자 도출 기준

- 자주 이용
- 명칭이나 내역등 과 같은 **이름은** 피하자
    - Ex) 부서명 —> 부서코드로 사용
- **속성의 수**를 **최대한 적게** 구성하자

### 관계간 엔터티의 구분

- 고객, 계좌 엔터티가 있을때 혼자 있을 수 있어? 기준
    - **강한 개체** (고객)
    - **약한 개체** (계좌)

### 식별관계 와 비 식별관계

- 식별관계
    - 하나의 **엔터티의 기본키**를 **다른 엔터티가 기본키의 하나로 공유**하는 관계
        - EX) 참조하는 테이블 기본키 **내부에 외래키**가 있는 상태
- 비 식별관계
    - 참조하는 엔터티가 **외래키**를 기본키가 아닌 **일반 속성으로 가지고 있을 때**
    - 비 식별관계는 ERD에서 **점 선**으로 표기한다

### 정규화 개념

- 데이터 중복 제거, 이상현상 줄이기, 논리 데이터 모델링 수행 시점에 고려됨
- 1 ~ 5 정규화가 존재함 ( 실질적으로는 제3 정규화까지만 실행 )

### 이상의 종류

- 삽임 이상
- 삭제 이상
- 갱신 이상

### 정규화 단계

- 제 1정규화
    - 테이블의 컬럼이 **원자성을 갖도**록 테이블을 분해
        - 한 컬럼에 여러 값이 들어가면 수정해주자
            - Ex) 구매상품 : 삼푸,린스 —> 구매 상품 각각 나눠서 “샴푸”, “린스”
- 제 2정규화
    - **완전 함수적 종속**을 만들도록 테이블을 분해
        - 완전 함수적 종속이란? **기본키를 구성하는 모든 컬럼**의 값이 **다른 컬럼을 결정** 지을 수 있는 것
            - Ex) “학생번호”, “강의명” 이 PK일 경우 **“강의실”**은 **학생번호랑 관계 없음** —> 강의실 컬럼부분을 다른 테이블을 쪼개준다
- 제 3정규화
    - **이행적 종속**을 **제거** 테이블을 분리
        - 이행적 종속이란 ? A-> B, B->C의 관계를 성립할때 A->C가 성립 되는 것을 말함
        - EX) “학번”, “전공”, “교수” 일 경우
            - “학번” ->  “전공”  ||  “전공” ->  “교수”  ||  “학번” ->  “교수” 을 갖는 이행적 함수적 종속이되어버린다 이걸 나눠서 ===> 교수 컬럼을 나눠서 테이블로 쪼개버리자
- BCNF 정규화
    - **모든 결정자**가 **후보키**가 되어야한다.
- 제 4 정규화
    - **다중 종 속성을 제거**
- 제 5 정규화
    - **모든 조인 종속**이 **후보키를 통해**서만 **성립**한다.

### 관계의 개념

- 엔터티의 인스턴스 사이의 **논리적인 연관성**
- 관계를 맺는다는 의미는 **부모 식별자**를 **자식에 상속**하고 **상속된 속성**을 **매핑키(조인키)로 활용**하는것 :: 조인하려고 테이블 나눈걸로 생각하자

### 관계의 분류

- 존재적 관계 : **부모**가 있어야 **자식**이 있는 것
    - Ex) 사원 엔터티가 있어야 부서 엔터티가 의미가 있어짐
- 행위적 관계 : 엔터티 간의 **행위를 통해** 연관되어 있는 것
    - Ex) 주문은 고객이 주문할 때 생성된다.

### 조인의 의미

- 데이터의 중복을 피하기 위해 **분리된 테이블들**을 서로 **관계를 다시 맺고** 이들의 [데이터를 동시 출력](https://us05web.zoom.us/j/5039005034?pwd=rV0La5p2W5iw7xwdf7RbEimxzHFitE.1)하거나 관계가 있는 테이블을 **참조**하기 위한 과정

### 계층형 데이터 모델

- **자기 자신** 엔터티 **내부에서 관계**가 **발생**하는 것
- **계층 구조**를 갖는 **인스턴스 끼리 연결**하는 **조인을 셀프조인**이라고 한다(같은 테이블을 여러번 조인)
    - Ex) 사원번호 테이블 내 “사원번호”, “관리자번호” 두 컬럼이 존재 할 경우 같은 값이지만 의미 하는 바가 다르기에 조인에 사용

### 상호배타적 관계

- **두 테이블 중 하나만** 가능한 관계 [ 택 1 **하나만 관계**를 맺을 수 있다 ]
    - Ex) 주문은 개인고객이거나 법인 고객 둘중 하나만이 가능함. :: IE 표기법시 **“ [ “** 기호로 중간에 막음

### 트랜잭션이란?

- 하나의 **연속적인 업무 단위**를 말한다.
    - 조회 -> 업데이트 -> 업데이트 가 이뤄질 때 동시에 수행 되어야 하며 **모두 성공**하거나 **모두 취소**되어야한다. “All or Nothing”
- **하나의 트랜잭션**에는 **여러 DML문이 포함될 수 있다.**
- 4개의 성질
    - 독립성 (Isolation): 동시에 실행 되어도 서로 영향을 미치면 안된다.
    - 일관성 (Consistency): 늘 일관성 있는 상태를 유지해야한다.
    - 영속성 (Durability): 성공적으로 수행하면 그상태가 영구적으로 반영
    - 원자성 (Atomictity): 작업은 하나의 단위로 처리한다. - 전부 반영되거나 실패하거나
- 주의
    - 서로 **독립적으로 발생하면 안된다**.
    - **부분 커밋 불가능** :: 동시 커밋 또는 롤백 처리 되어야한다.

### 트랜잭션 격리성이 낮을 경우 문제

- Dirty Read : 다른 트랜잭션에 의해 수정되었지만 **아직 커밋되지 않은 데이터를 읽는 것**
- Non-Repeatable Read : **한 트랜잭션 내에서 같은 쿼리**를 **두번 수행**했는데 그사이 다른 트랜잭션이 값을 **수정 또는 삭제**해서 **두 쿼리가 결과가 다른 것**
- Phantom Read : 한 트랜잭션에서 같은 쿼리 두번 수행 했는데 첫번쨰 쿼리에서 없던 **유령 레코드가 두번쨰 쿼리에서 나타**나는것

### 필수적, 선택적 관계와 ERD

- 필수적 관계
    - 두 엔터티의 관계가 서로 **필수적일 때 하나의 트랜잭션을 생성**
- 선택적 관계
    - 두 엔터티가 서로 **독립적으로 수행이 가능하다면 선택적 관계로 표현**
- 표기법
    - IE : 원( **O** )을 사용하여 필수적 관계와 선택적 관계를 구분
        - **필수** 일 경우 **O 없음**
    - 바커 표기법
        - 필수적 : **실선**으로 표기
        - 선택적 : **점선**으로 표기

### NULL이란

- 모델 설계 시 Null 사용 여부를 설정함
- 0 이나 공백이랑은 **완전히 다른 개념**이다

### NULL 정리

- **NULL을 포함한 연산 결과**는 **항상 NULL**이다
    - Ex) NULL + 300 = NULL
- NULL을 **다른 값으로 변환** 방법
    - **Oracle**
        - **NVL(대상 , 0)**
    - SQL Server
        - **ISNULL(대상, 0)**
    - 사용하면 NULL을 0으로 변환 해준다.
- 조건에 맞는 값을 NUL로 변환 방법
    - NULLIF(대상, 조건값 ) :: 이 맞으면 NULL 이 나온다.
    
    ```sql
    # 내나이 32 .. 맞아서 NULL로 반환된다.. 30 살이면 30 살로 나올텐데 ..
    SELECT NULLIF(내 나이, 32) FROM DUAL;
    ```
    
- Oracle의 경우 Insert 시 ‘’ 값을 넣으면 NULL이 들어간다.
    
    ```sql
    INSERT INTO 테이블 VALUES('999', '', '2024-11-19' ); # 경우 2번째 컬럼이 NULL임
    ## ⭐️ 중요 포인트는 SQL-Server는 ''로 빈 문자열이 들어간다는 것이다
    ```
    
- **집계 함수**는 NULL을 **제외한 연산 결과**를 **리턴**한다.
    - sum, avg, min, max등의 함수는 NULL을 제외하고 계산해준다.
    - ⭐️ 함정으로 내기 좋은 문제
        - 각 특정 컬럼에 NULL이 존재할 경우 평균을 구하려 할 경우
            - 그냥 AVG(CMM)를 사용하면 **NULL을 제외한 평균**이 계산 된다
            - SUM(CMM) / COUNT(*) 로 계산 할 경우 NULL을 포함한 **모든 인스턴스의 평균**이 나옴
- **COALESCE()** 함수
    - 첫번째 NULL이 아닌 값을 반환 해주는 함수
    
    ```sql
    # c1 에 null, c2에 null, c3 100 일 경우  ==> 100을 반환
    # c1에 20이면 바로 ==> 20 반환 해줌
    SELECT COCALESCE(c1,c2,c3) from dual;
    ```
    

### NULL 표기법

- IE : 따로 표기 방법 **존재하지 않음**
- 바커 : 컬럼 **이름 앞에 O**로 **표시**

### 식별자 구분

- 본질 식별자 : **업무에 의해 만들어진** 식별자 (꼭 필요한 식별자)
- 인조 식별자 : 인위적으로 만들어진 식별자 (꼭 필요하지는 않지만 관리의 편의성 등의 이유로 인위적으로 만들어진 식별자)
    - 시퀀스나 주문번호같은 애들임
    - 인조 식별자 **단점**
        - 중복 데이터 발생 - 에코바이크 시퀀스로 바꾼거 생각하면 된다. 스퀀스가 PK이기에 **중복 제거가 불가능해짐**
        - **불필요한 인덱스가 생성**된다
            - 인텍스는 원래 조회 성능을 향상시키기 위한 객체이며 인텍스는 DML 시 INDEX SPLIT 현상으로 인해 성능이 저하된다

# 2장 - SQL

### 테이블 생성 시 주의 사항

- 테이블 명은 **중복될 수 없지**만 **소유자가 다를 경우 같은 이름**으로 **생성이 가능**하다

### 데이터 무결성 종류

- 개체 무결성
    - **기본키**는 **NULL 혹은 중복 값**을 가질 수 **없음**
- 참조 무결성
    - 외래키 값은 **NULL이거나** 참조 테이블의 **기본키 값과 동일해야한다.** *(NULL) 가능*
- 도메인 무결성
    - 주어진 속성 값이 정의된 **도메인에 속한 값** 이어야한다
- NULL 무결성
    - **특정 속성**에 대해 **NULL을 허용하지 않는** 특징
- 고유 무결성
    - **특정 속성**에 대해 **값이 중복되지 않아야는** 특징
- 키 무결성
    - **하나의 릴레이션** 관계에는 **적어도 하나의 키가 존재해**야한다.

### ERD

- 테이블 간 서로의 상관 관계를 그린 그림
    - 엔터티(객체), 관계 , 속성 으로 이뤄짐
        - 객체 - 사각형
        - 관계 - 마름모
        - 속성 - 타원

### SQL 종류

- **DDL :: 포인트는 모든** 명령어가 **오토 커밋**된다
    - Create, Alter, Drop, Rename, TRUNCATE
        - TRUNCATE
            - 주의사항
                - **로그를 남지 않음** (개발 기준 확인하고 사용)
                - DELETE 와 같이 데이터를 날리지만  **메모리까지 날려버림**
            - 사용법
                - TRUNCATE FROM 테이블명;

### SELECT 문의 구조

```sql
SELECT 
	{컬럼명} 
FROM {테이블명} 
	WHERE {조건식} 
GROUP BY {그룹화할 컬럼명}
	HAVING {그룹화 조건식}
ORDER BY {정렬 컬럼}
```

### DBMS 해석 순서 🔥 중요 🔥

- FROM > WHERE > GROUP BY > HAVING > SELECT > ORDER BY

### 조건문 연산자 우선 순위

- ()
- 단항 연산자
    - ‘-‘, ‘+’ :: 음수 혹은 양수
- 곱셈, 나눗셈
- 덧셈, 뺼셈
- 문자 연결 연산자 ‘||’
- 비교연산자
    - =, !=, <>, >, <, >=, <=, IS NULL, LIKE, BETWEEN, IN
- NOT
    - 논리 연산의 반대를 반환
- AND
- OR ✨ 중요 사람들이 자주 햇갈림 !! 페이징할떄도 그래서 ()묶어서 처리

### Order By 주의사항

- **SELECT 문보다 늦게** 시행 되므로 **만 컬럼 별칭 사용이 가능**하다
- “,” 를 통해 **복수의 정렬** 이 가능하다
- DMBS 마다 **NULL값에 대한 정렬 순서가 다를 수 있으**므로 주의
- Order By절 () 안에 **Alias**나 컬럼 순서를 나타내는 **정수** **혼용 사용 가능!**
- Order By ( **Case When 문**이 **사용 가능 하다!!** )
    - 변환 된값으로 해서 정렬 하며 뒤에 정렬 종류를 쓰지 않으면 **기본 ASC 정렬**을 한다.
    - 예시
        
        ```sql
        SELECT 
        	id 
        FROM tbl
        	GROUP BY ID
        HAVING COUNT(*) = 2
        # ID값이 999일 경우 Then 숫자로 정렬함 여기서 만약 다른 ID가 100이라면 
        # 그 위로 올라감!! 이유는 -> 100보다 99가 작으니 Default ASC로 인해 위로!!
        ORDER BY ( CASE WHEN ID = 999 THEN 99 ELSE ID END );
        ```
        
- 함정 문제
    
    ```sql
    # 해당 쿼리는 이상이 없다
    SELECT 
    	지역, 매출금액
    FROM 지역별매출
    	ORDER BY 년 ASC;
    
    #########################
    
    # 해당 쿼리는 에러를 발생한다 왜일까??
    SELECT
    	지역, SUM(매출금액) AS 매출금액
    GROUP BY 지역
    	FROM 지역별매출
    ORDER BY 년 DESC;
    
    # 👉 이유는 SELECT 한 부분들이 모두 Group화 되어 있지만 정렬하려는 
    #    대상의 년은 그룹화된 상태가 아니기 떄문이다!
    
    ################################
    ################################
    
    # 아래와 같이 서브쿼리를 사용하면 처리 가능
    SELECT 
    	지역, SUM(매출금액) AS 매출금액 
    FROM 지역별매출
    	GROUP BY 지역
    ORDER BY (SELECT MAX(년) FROM 지역별매출) DESC; 
    ```
    

### Alias 주의사항

- 이미 있는 **예약 어 사용 금지**
- 띄어쓰기 금지
    - 원하면 ‘’ 를 사용해서 묶어서 사용해주자
        - Ex) ‘흑곰은 왕왕 띄어쓰기 귀엽다’

### Like 연산자

- _S% 이름 둘째가 S로 시작하는거
- __S__ 가운데가 S이면서 5글자

### 외래키

- 외래키는 여러개 설정 가능
- NULL가능
- 부모 데이터가 있어도 **자식 데이터는** 삭제 가능하다.
    - 오히려 **부모가 엮여 있을 경우 지워지지 않는다 ( 가장의 무게.. )**
        - Cannot delete or update a parent row: a foreign key constraint fails
- 부모 데이터 삭제를 하고싶다면 아래의 제약 조건을 추가해 주자
    - `ON DELETE CASCADE;`
    - `ON DELETE SET NULL;`
- 외래키 설정 방법
    - 테이블 생성 시
    
    ```sql
    CREATE TABLE Orders (
        OrderID INT PRIMARY KEY,
        ProductID INT,
        OrderDate DATE,
        # CONSTRAINT 제약조건명  은 필수가 아님 옵션이다 자동으로 생성됨
        FOREIGN KEY (ProductID) REFERENCES Products(ProductID) ON DELETE CASCADE
    );
    
    ---------------
    CREATE TABLE Orders (
        OrderID INT PRIMARY KEY,
        ProductID INT,
        OrderDate DATE,
        # CONSTRAINT 제약조건명사용 !! 중요 포인트 : add를 붙이지 않음
        CONSTRAINT FK_THAT FOREIGN KEY (ProductID) REFERENCES Products(ProductID) ON DELETE CASCADE
    );
    ```
    
    - Alter 사용 시
    
    ```sql
    ALTER TABLE Orders
    # Alter의 경우 ADD CONSTRAINT 제약조건명 필수임
    ADD CONSTRAINT FK_ProductID
    FOREIGN KEY (ProductID) REFERENCES Products(ProductID)
    ON DELETE SET NULL;
    ```
    

## 날짜 비교

- 유의사항
    - TO_DATE() 와 TO_CAHR()로 변환한 날짜는 완전히 다르게 작동한다
        - TO_CAHR() 의 경우 **완벽하게 해당 날짜를 문자로 변환**
            
            ```sql
            SELECT TO_CHAR(날짜가들어있는컬럼, 'YYYYMM') FROM DUAL;
            # '202411' 을 반환 해줌 
            ```
            
        - TO_DATE()의 경우 yyyy-MM를 삽입해도 **뒤에 일 시 분 초가 붙는다**
        
        ```sql
        SELECT TO_DATE(날짜가들어있는컬럼, 'YYYYMM') FROM DUAL;
        # 24/11/01 00:00:00 을 반환 해줌 
        ```
        

## 단일 행 , 다중 행 함수

- 함수의 입력 행수의 따라 단일행 함수와 다중행 함수로 구분 할 수있다.
- **1:M 조인**이라 하더라도 M쪽에서 출력된 행이 하나씩 **단일행 함수의 입력값으로 사용되므로 사용할 수 있다**
- **다중행 함수도** 단일행 함수와 동일하게 **단일 값만을 반환**한다.
- 종류
    - 단일행 함수
        - lower, upper, substr, length, trim, replace
    - 다중행 함수
        - sum, count, max, min, avg

### TOP 함수

- SQL - Server에만 존재하는 함수
    - Oracle에는 없어!!!
- 사용 예시
    
    ```sql
    # 해당 값이 동일하면 함께 출력 ❌
    SELECT 
    	TOP(3) {대상컬럼, 대상커럼}
    FROM {테이블명}
    	ORDER BY {정렬기준} ; # ASC 혹은 DESC를 적용 
    
    ######################################
    SELECT 
    	# WITH TIES를 사용하면 동일 값도 함께 출력 해준다
    	TOP(3) WITH TIES {대상컬럼, 대상커럼} 
    FROM {테이블명}
    	ORDER BY {정렬기준} ; # ASC 혹은 DESC를 적용 
    ```
    

## Join

- 국가 표준은 **ANSI** 표준이다
- Oracle 과 ANIST **표준이 서로 다르다**
    - Oracle의 경우 **테이블의 나열 순서가 중요하지 않음**
    - ANSI 표준은 **Outer Joint 시 순서 중요**하다
- N 개의 테이블 조인 시 **최소 N-1 개의 조인 조건이 필요**하다
- 대부분 **Non EQUI Join**을 사용할 수 있지만 때로는 **설계상 이유**로 **수행이 불가능** 할 **때**가 **있음**
- DBMS 옵티마이저는 **항상 2개씩** **짝을** 지어 **Join 수행**
- JOIN 시 테이블 간 **중복된 컬럼**이 **없을 경우** Alias를 앞에 **안 붙여줘도 된다.**
    - 테이블간 **중복된** 컬럼이 **있을** 경우 **꼭 Alias를 붙여주자!**
        
        ```sql
        # Table
        배우(배우번호, 배우명, 성별);
        영화(영화번호, 영화명, 제작년도);
        출연(배우번호, 영화번호, 출연료);
        
        ################
        
        #에러 발생 쿼리
        SELECT 
        	# 영화명 경우 Alias가 없어 사용가능하나
          # 배우번호는 불가능!❌ ==> 영화.배우번호 혹은 배우.배우번호 사용해야 함 
        	영화명, 배우번호
        FROM 배우, 영화, 출연
        	# 👍 요건 가능해 왜? 출연료는 출연 테이블에 밖에 없어서 자동으로 찾아줌
        	WHERE 출연료 > 8888;
        ```
        

### 조인 종류

- 1) 조건의 **형태의 따라** 구분
    - **EQUI JOIN** : JOIN의 조건이 동등 조건인 경우
        - “=”를 통해 JOIN 을 사용
        
        ```sql
        SELECT
        	EMP.ENAME, DEPT.DNAME
        FROM EMP, DEPT
        	WHERE EMP.DEPTNO = DEPT.DEPTNO; ## "="를 사용했으므로 EQUI JOIN 이다
        ```
        
    - **NON EQUI JOIN** : JOIN 조건이 동등 조건이 아닌 경우
        - 쉽게 말하면 **“=”** 비교가 아닌 **Between 혹은  > , <**  같은 값의 범위로 조인
- 2) 조인 **결과에 따라** 구분
    - INNER JOIN : JOIN **조건에 성립하는 데이터만 출력**
        - **내부 조인**이며 **조건이 일치하는 행**만 **추출** [ Oracle의 기본 조인이다. ]
        - ANSI 경우
            - FROM 절에 **INNOR JOIN** 혹은 줄여서 **JOIN**을 **명시**
                - **ON, USING** 둘 중 하나를 **선택해서 사용**하면된다.
                    - **USING 사용 시** 똑같은 컬럼 **두번 안써도 되서** 코드가 **짧아지는 장점**이 있다.
            - **USING** 이나 **ON 조건절을 필수**적으로 사용해야 한다.
                - **ON 절**에 **괄호**를 쓸 수 있다 다만 **선택 사항임 필수 아님**
                - USING절은 **괄호가 필수**
            - 예시 - **ON 사용**
            
            ```sql
            SELECT
            	테이블1.컬럼, 테이블2.컬럼
            FROM 테이블1 INNER JOIN 테이블2.      ## INNER JOIN 명시
            	ON 테이블1.조건컬럼 = 테이블2.조인컬럼   ## ON절을 통해 JOIN 조건 명시
            ```
            
            - 예시 - USING **사용**
                - **괄호** 사용이 **필수**이다
                
                ```sql
                **SELECT
                	테이블1.컬럼, 테이블2.컬럼
                FROM 테이블1 INNER JOIN 테이블2
                	USING( 조인컬럼 )**
                ```
                
    - OUTER JOIN : JOIN **조건에 성립하지 않는** **데이터도 출력**하는 경우
        - JOIN조건에서 일치하는 **값이 없을 경우**에도 **행을 반환**할 때 사용
            - 예)  학생 목록에서 지정교수가 JOIN 키인데 **지정교수가 없어**도 **전체 학생 목록 + 교수명**이 보고 싶을 경우
        - 종류
            - LEFT OUTER JOIN, RIGHT OUTER JOIN
                - **각의 위치에 맞는 테이블을 데이터 출력 후** JOIN 조건에 맞는 **반대편 테이블 값을 붙여줌**
                - 사용방법
                    - 예시 - ORACLE [LEFT OUTER JOUN]
                    
                    ```sql
                    SELECT
                    	*
                    FROM  STUDENT S,  PROFESSORP
                    ## LEFT OUTER 경우 P.PROFNO(+) (*).  || RIGHT OUTER 경우 S.PROFNO(+)
                    	WHERE S.PROFNO = P.PROFNO(+)   
                    		AND S.GRADE IN (1,4);
                    ```
                    
                    - 예시 - ANSI [LEFT OUTER JOUN]
                    
                    ```sql
                    SELECT
                    	*
                    ## LEFT OUTER JOIN 명시
                    FROM STUDENT S LEFT OUTER JOIN PROFESSOR P
                    	# ON 절에 조인 조건 명시
                    	ON S.PROFNO = P.PROFNO
                    WHERE S>GRADE IN (1,4)
                    ```
                    
- 3) Natural JOIN : **조인 조건 생략** 시 두 테이블에 **같은 컬럼 이름으로 자연 연결**되는 조인
    - **자동**으로 **같은 컬럼을 JOIN 해서** 가져온다
    - 주의사항
        - 만약 Student 테이블, Professor 테이블이 있을 경우 **Natural Join 하면 값이 안 나온다**
        - Why? : **이름까지**도 컬럼명이 같아서 **자동으로 조건을 걸어버림**
    - 예시
        
        ```sql
        SELECT
        	EMP.ENAME, DEPT.DMANE
        # 조건이 없으니 on절도 생략
        FROM EMP NATURAL JOIN DEPT;
        ```
        
- 4) Cross JOIN : 조인 조건 생략 시 두 테이블 간의 **행 수 곱연산**으로 나옴
    - **조건이 없음** 이게 포인트임
    - 예시 - ORACLE
        
        ```sql
        SELECT
        	EMP.ENAME, DEPT.DMANE
        # 조건이 없으니 on절도 생략
        FROM EMP, DEPT;
        ```
        
    - 예시 ANSI : From 테이블 Cross JOIN 테이블 2;
        
        ```sql
        SELECT
        	EMP.ENAME, DEPT.DMANE
        # 조건이 없으니 on절도 생략
        FROM EMP CROSS JOIN DEPT;
        ```
        
- 5) Self JOIN : 하나의 테이블을 두번 이상 참조하여 연결하는 조인
    - 예시
        - 
        
        ```sql
        SELECT e1.empno as 직원번호,
               e1.ename as 직원성명,
               e1.mgr as 담당매니저_직원번호,
               e2.ename as 담당매니저_성명
        FROM emp e1, emp e2
        WHERE e1.mgr=e2.empno;
        ```
        

# SQL - 활용

### Where절 서브 쿼리

- **단일행** 경우
    - **단일된** 값이므로 **=, <>, >, >=, <, <=** 와 같은 **조건이 사용 가능**한 경우
- **다중행** 경우
    - 서브 쿼리 결과가 **여러 행일** 경우
        - IN() : 해당 절에 값이 같은 애를 찾음
        - > ANY() : **최소값**을 반환
        - < ANY() : **최대값**을 반환
        - < ALL() : **최소값**을 반환
        - > ALL() : **최대값**을 반환
    - 다중 행은 당연히 EQUI 비교가 불가능하다, 그렇기에 서브 쿼리 내에서 조인을 통해 값을 정제 후 사용하는 경우가 많음
- **EXISTS, NOT EXISTS**
    - "한 건이라도 존재하면" 그 유무에 따라 TRUE 또는 FALSE를 반환한다.
        - **EXISTS : 한건이라도 존재하는 경우**
        - **NOT EXISTS : EXISTS의 반전 결과**

### 인라인 뷰 서브쿼리

- **From 절**에서 사용하여 **서브 쿼리로 사용**하는 것
    - 따라서 조회 하려는 대상이 **함수 형식이라면 Alisa를 지정해** 줘야함
        
        ```sql
        SELECT
        	T1.NAME , T2.HAP
        FROM EMP T1
        , (
        	## SUM은 함수이므로 Alias 지정
        		SELECT SUM(SAL) AS HAP FROM DEP
        	) T2;
        ```
        
    - 테이블 또한 Alias로 지정해 줘야한다
- 조인이랑 헷갈리지말자 **내부에서 WHERE** 절을 통해 밖에 **Table과 연결 불가능**
    
    ```sql
    SELECT
    	T1.NAME , T2.HAP
    FROM EMP T1
    , (
    		SELECT SUM(SAL) AS HAP FROM DEP
    			# 불가능
    			WHERE T1.NAME = DEP.NAME		
    	) T2;
    ```
    

### 스칼라 서브쿼리

- **Select 문 내**에서 **서브 쿼리를 사용**하는 것
- 당연히 **단일 행이 나와야한다** 왜냐면 Select Row에는 **항상 단일 행이 나오기 때문**임
    - 따라서 **WHERE 절은 필수**이며 메인 쿼리 Where 절의 비교 대상과 같은 값으로 사용해서 단일 값 뽑자
        
        ```sql
        SELECT 
        	ENPNO
        	, ( Select
        				DNAME
        		FROM DEPT D
        			WHERE D.DEPTNO = E.DEPTNO ) AS DNAME
        FROM EMP E
        	WHERE DEPTNO = 10;
        ```
        

### 집합 연산자

- 종류
    - UNION
        - SQL 결과의 **합집합** ( **중복 제거** )
    - UNION ALL
        - SQL 결과의 **합집합** ( **중복 미 제거** )
    - INTERSECT
        - SQL 결과의 **교집합 ( 중복된 결과의 행을 하나의 행으로 반환  )**
            - 두 테이블사이 같은 ROW만 찾아서 반환
        
        ```sql
        SELECT 
        	employee_id, job_id
        FROM employees
        
        # 교집합
        INTERSECT
        
        SELECT
        	employee_id, job_id
        FROM job_history ;  # 마지막에 ";" 사용
        ```
        
    - EXCEPT 또는 MINUS
        - SQL 결과의 **차 집함 ( 중복된 행은 하나의 행으로 만든다 )**
            - **첫 번째 검색 결과**에서 **두 번째 검색 결과**를 **제외한 나머지**를 검색 ( **반달 모양으로 나옴!** )
            - 
            
            ```sql
            SELECT
            	employee_id, job_id
            FROM employees
            
            # 차집합
            MIUNS # or EXCEPT
            
            SELECT
            	employee_id, job_id
            FROM job_history;
            ```
            
- 주의사항
    - 두집합의 조회 하려는 **컬럼수가 같아**야 한다. ( 그렇지 않으면 에러를 반환 )
    - 두집합의 컬럼 **순서가 같아**야한다
        - 컬럼의 명이 **다를 경우** **가장 첫번째 걸**로 나온다 ::: 따라서 Alias를 사용해서 통일 시켜주자
    - 두 집합의 각 컬럼의 **데이터 타입 일치**
    - 컬럼의 데이터타입이 일치 한다면 **사이즈는 달라도 된다.**
    - **중복 제거**의 조건은 **모든 ROW가 같아야** 제거 하는 것이다 중요함!! ✨
    - **;는 중간**에 넣으면 **안된다** **(마지막에 넣자)**

### 그룹 함수

- **NULL**은 항상 **제외하고 실행**된다
- COUNT(), AVG() 또한 **NULL을 제외하고 계산**한다.
    - 따라서 AVG의 경우 **NULL인 값을 포함**해서 **계산** 하려면 방법이 **2가지 방법** 존재
        - SUM(COMM) / COUNT(*) 을 통한 계산
        - AVG(NVL(COMM,0)) 을 통한 계산 —> **NULL**일 경우 **0으로 변환**해서 사용
- Oracle의 경우 명령어가 다른것이 2개 있음
    - VARIANCE() ::  열의 분산 값을 계산합니다.
    - STDDEV() :: 표준 편차 계산

### Group By Function

- **Group By 절**에서 **사용**이 가능하다
- 여러 Group By 결과를 **동시에 출력**하기 위한 **기능**이다
- **1. Grouping Sets(a, b, c, d, ….)**
    - A, B 별 **그룹 연산** 결과를 **합쳐서 출력**  🔥 **중복 제거 따위 없음 →** 그룹화가  목적
    - 각 각 그룹화 시 **데이터가 없는 컬럼**이 있다면 **Null로 알아서 채움**
    - **Default 파라미터**만 **사용** 후 출력 시 **전체 합계** ❌
        - **마지막 인자**에 **Null or ()** 을 넣으면 맨 **최종 Row에 합계** 출
            - Ex)
                
                ```sql
                Group By Grouping Sets(DEPTNO, JOB, ()); ## 최종 쿼리 마지막 ROW에 총합
                ```
                
    - 예시
        
        ```sql
        SELECT
        	DEPTNO, JOB, SUM(SAL)
        FROM EMP
        	# 통 그룹화가 아닌 DEPTNO, JOB 각각 그룹화 하고 싶을 경우
        	GROUP BY Grouping Sets( DEPTNO, JOB ) ; 
        ```
        
        - 위와 같은 결과 출력 방법 - UNION ALL
            
            ```sql
            # DEPTNO 그룹화한 결과
            SELECT
            	DETPNO, NULL AS JOB, SUM(SAL)
            FROM EMP
            	GROUP BY DEPTNO
            
            # UNION ALL을 통해 중복 무시 결합
            UNION ALL
            
            # JOB 그룹화한 결과
            SELECT
            	NULL AS DETPNO, JOB, SUM(SAL)
            FROM EMP
            	GROUP BY JOB
            ```
            
- **2. ROLLUP**
    - **파라미터 순서**가 굉장히 **중요**하다
        - **첫 번째**가 **기준**이 되기 때문이다.
    - 기본적으로 전체 통계를 마지막에 작성해 줌
    - ROLLUP의 **첫 번째 인자를 기준**으로 메인 롤링이 되어 **Group화**
    - 예시
        
        ```sql
        SELECT
        	DEPTNO, JOB, SUM(SAL)
        FROM EMP
        	GROUP BY ROLLUP(DEPTNO, JOB);
        ```
        
        - 결과 값
            
            
            | DEPTNO | JOB | SUM(SAL) |
            | --- | --- | --- |
            | 10 | CLERK | 1300 |
            | 10 | MANAGER | 7950 |
            | 10 | ANALYST | 3000 |
            | 10 | PRESIDENT | 5000 |
            | 10 | NULL | 17250 |
            | 20 | CLERK | 2800 |
            | 20 | MANAGER | 8425 |
            | 20 | ANALYST | 3000 |
            | 20 | NULL | 14225 |
            | 30 | CLERK | 3050 |
            | 30 | SALESMAN | 5950 |
            | 30 | MANAGER | 2850 |
            | 30 | NULL | 11850 |
            | NULL | NULL | 43325 |
- **3. Cube(A,B)**
    - A별, B별, 전체 그룹 **각각 연산 결과를 출력**
        - N +1 그룹이 나옴 → 총합 통계까지 같이 나옴
    - **파라미터**의 **순서**는 **중요하지 않음**
    - 기본적으로 전체 통계를 알려 줌
    - **Grouping Sets()**을 사용해도 같은 결과 값이 나오게 **가능**
    - 예시
        
        ```sql
        SELECT
        	상품ID, 월, SUM(매출액) AS 매출액
        FROM 월별매출
        	GROUP BY CUBE(상품ID, 월);
        ```
        
        - 결과
        
        ![Untitled](https://prod-files-secure.s3.us-west-2.amazonaws.com/812934f4-5ca6-4cae-bf06-6dac4e78ba75/10a9a0f8-4d2a-4798-9adc-ee2f4bb28aad/Untitled.png)
        

### Window Function

- 서로 **다른 행**의 **비교나 연산**을 위해 만든 **함수**
    - 전체 목록에 **집계 함수**를 사용해야 할 경우 : **Group By 없이**
        - **서브 쿼리**로 **가능**하나 **성능에는 좋지 못함**
            
            ```sql
            SELECT
            	EMPNO, (SELECT SUM(SAL) FROM DEPT ) AS TOTAL
            FROM EMP; 
            ```
            
- **Group By**를 사용하지 않고 **그룹 연산이 가능**
- 종류
    - **LAG**: 현재 행 이전의 행에 있는 열 값을 가져옵니다.
    - **LEAD**: 현재 행 다음의 행에 있는 열 값을 가져옵니다.
    - **SUM**: 지정된 열의 값들의 합을 계산합니다.
    - **AVG**: 지정된 열의 값들의 평균을 계산합니다
    - **MIN**: 지정된 열의 값들 중 최솟값을 찾습니다
    - **MAX**: 지정된 열의 값들 중 최댓값을 찾습니다
    - **COUNT**: 지정된 열의 값들의 개수를 계산합니다.
    - **RANK**: 결과 집합에서 각 행에 대한 순위를 계산합니다. 같은 값이 여러 개인 경우에는 동일한 순위를 부여합니다.
- **문법의 순서**를 지키는 것이 **중요**하다
    
    ```sql
    SELECT
    	윈도우 함수( 대상 ) OVER ( PARTITION BY 컬럼
    												 ORDER BY 컬럼 DESC | ASC
    												 ROWS | RANGE BETWEEN A AND B
    													);
    ```
    
    - **PARTITION BY  사용법**
        - **그룹 연산** 수행할 **GROUP BY 컬럼**을 넣는다
        - 예시
            
            ```sql
            # 사원 마다 속한 부서별 총 급여
            SELECT
            	이름, SUM(SAL) OVER (PARTITION BY DEPTNO) AS 부서 급여 총합
            FROM EMP;
            ```
            
            - 결과
            
            | 이름 | 부서 급여 총합 |
            | --- | --- |
            | SMITH | 5800 |
            | ALLEN | 5600 |
            | WARD | 5600 |
            | JONES | 5800 |
            | BLAKE | 5600 |
    - **ORDER BY 절**
        - **정렬**을 해주는 기능
        - **RANK()**를 사용할 경우 **필수**
            - 정렬 컬럼 및 정렬 순서에 따라 순위 변화하기 때문이다.
    - **ROWS | RANGE BETWEEN A AND B 절**
        - 연산 범의를 지정 해주며 앞에 명령어를 사용 시 옵션이 바뀐다.
            - RANGE : **같은 값**의 경우 **하나의 Range로 묶어서** 동시 **연산** [ 기본 값  ]
            - ROWS : 값이 같더라도 **각 행 연산**
        - **범위를 지정**하기에 **ORDER BY** 절 **필수**
        - **BETWEEN A AND B 각각 A, B 설명**
            - **“A”** 시작점 정의
                - CURRENT ROW : 현재 행부터
                - UNBOUNDED PERCENDING : 처음부터 [ 기본값 ]
                - N PRECEING : N 이전 부터
            - **“B”** 마지막 시점 정의
                - CURREND ROW : 현재행까지 [ 기본값 ]
                - UNBOUNDNDED FOLLWING : 마지막까지
                - N FOLLOWiNG : N 이후까지
        - 예시
            
            ```sql
            SELECT                 # 급여 순대로 정렬  
            	R.* m SUM(SAL) OVER( ORDER BY SAL
            											# 처음부터 ~ 현재행까지 범위로 계산
            											 ROW BETWEEN UNBOUNDED PRECEDING AND CURRENT ROW
            										) AS RESULT
            FROM RANGE_TEST R;
            ```
            
            - 결과 : Result를 보면 대각선으로 더 해짐
                
                
                | ID | SAL | RESULT |
                | --- | --- | --- |
                | 1 | 100 | 100 |
                | 2 | 200 | 300 |
                | 3 | 300 | 600 |
                | 4 | 400 | 1000 |
                | 5 | 500 | 1500 |
    - **그룹 함수 형태**
        - SUM, COUNT, AVG, MIN, MAX 등
        - **OVER()** 절을 이용하여 **윈도우 함수로 사용이 가능**하다
        - 예시 - SUM + Order By
            
            ```sql
            # 모든 직원의 급여 합계가 나온다 << 쓸모 없는 쿼리
            SELECT EMPNO, SUM(SAL) OVER() AS TOTAL FROM EMP;
            
            # 급여가 낮은 순서대로 누적합
            SELECT EMPNO, SUM(SAL) OVER( ORDER BY SAL ) AS TOTAL FROM EMP;
            
            # 결과
            | EMPNO | TOTAL |
            |-------|-------|
            | 7900  | 950   | (EMPNO 7900까지의 급여 합계)
            | 7876  | 2050  | (EMPNO 7876까지의 급여 합계)
            | 7369  | 3850  | (EMPNO 7369까지의 급여 합계)
            | 7934  | 5150  | (EMPNO 7934까지의 급여 합계)
            | 7844  | 6450  | (EMPNO 7844까지의 급여 합계)
            | 7521  | 7950  | (EMPNO 7521까지의 급여 합계)
            | 7499  | 9550  | (EMPNO 7499까지의 급여 합계)
            | 7521  | 12050 | (EMPNO 7521까지의 급여 합계)
            | 7782  | 15075 | (EMPNO 7782까지의 급여 합계)
            | 7698  | 18125 | (EMPNO 7698까지의 급여 합계)
            | 7566  | 21100 | (EMPNO 7566까지의 급여 합계)
            | 7788  | 24100 | (EMPNO 7788까지의 급여 합계)
            | 7839  | 29100 | (EMPNO 7839까지의 급여 합계)
            ```
            
        - 예시  -  AVG + PARTITION BY
            
            ```sql
            ## 모두가 같은 전체 평균
            SELECT EMPNO, AVG(SAL) OVER() AS TOTAL FROM EMP ; 
            
            ## 부서별 평균
            SELECT EMPNO, AVG(SAL) OVER( PARTITION BY DEPTNO ) AS TOTAL FROM EMP ;
            ```
            
        - **전체 문법**이 **비슷**하기에 앞에 사용할 **집계함수만 변경**하면 된다.
- **RANK()**
    - **특정 값**에 대한 **순위 확인**
    - Window 함수가 아니지만 자주 쓰이는 방식
        
        ```sql
        SELECT RANK(값) WITHIN GROUP( ORDER BY 컬럼명 );
        
        # 급여가 3000이면 전체 급여에서의 순위
        SELECT 
        	RANK(3000) WITHIN GROUP( ORDER BY SAL DESC  ) AS RANK_RESULT 
        FROM EMP;
        ```
        
    - **Window 함수 사용**
        - 전체 / 특정 그룹 중 **값의 우선 순위**를 확인
        - **OVER() 내부 ORDER BY절은 필수이다**
            - 순위를 구할 대상을 ORDER BY에 명시하는데 **여러개 가능**
                - 예시 - 각 직원의 급여의 전체 순위 ( **동 순위가 나오면 다음 순위는 +a** )
                    
                    ```sql
                    SELECT ENAME, DEPTNO, SAL
                    , RANK() OVER( ORDER BY SAL DESC ) AS ‘돈 많이 받는 순위’
                    FROM EMP;
                    
                    # 포인트는 자도으로 정렬되어서 나온다는 것이다
                    | ENAME | DEPTNO | SAL  | 돈 많이 받는 순위 |
                    |-------|--------|------|------------------|
                    | JONES | 20     | 2975 | 1                | (JONES의 급여가 가장 높아서 1등)
                    | BLAKE | 30     | 2850 | 2                | (BLAKE의 급여가 두 번째로 높아서 2등)
                    | ALLEN | 30     | 1600 | 3                | (ALLEN의 급여가 세 번째로 높아서 3등)
                    | WARD  | 30     | 1250 | 4                | (WARD의 급여가 네 번째로 높아서 4등)
                    | SMITH | 20     | 800  | 5                | (SMITH의 급여가 가장 낮아서 5등)
                    ```
                    
        - **그룹 내 순위** 구할 경우 **PARTITION BY 절 사용**
            - 예시 - 각 직원의 부서별 급여 순위
                
                ```sql
                SELECT ENAME, DEPTNO, SAL
                , RANK() OVER( 	PARTITION BY DEPTNO
                								ORDER BY SAL DESC ) AS ‘부서별 돈 많이 받는 순위’
                FROM EMP;
                
                # 마찬가지로 자동 정렬 부서별로 
                | ENAME | DEPTNO | SAL  | 부서별 돈 많이 받는 순위 |
                |-------|--------|------|--------------------------|
                | JONES | 20     | 2975 | 1                        | (부서 20에서 가장 높은 급여를 받는 직원으로 1등)
                | SMITH | 20     | 800  | 2                        | (부서 20에서 두 번째로 높은 급여를 받는 직원으로 2등)
                | ALLEN | 30     | 1600 | 1                        | (부서 30에서 가장 높은 급여를 받는 직원으로 1등)
                | BLAKE | 30     | 2850 | 2                        | (부서 30에서 두 번째로 높은 급여를 받는 직원으로 2등)
                | WARD  | 30     | 1250 | 3                        | (부서 30에서 세 번째로 높은 급여를 받는 직원으로 3등)
                ```
                
- **DENSE_RANK()**
    - RANK() 와 사용 방법은 똑다
    - 다른점은 동 순위 부여 후 **다음 순위가 바로 이어지게 함**
        - Ex) 2등,2등 → 3등 시작  ::: **+a가 없어!**
- **ROW_NUMBER**
    - 연속된 행 번호
    - 그냥 **목록 순서대**로 **번호를 나열**
- **LAG, LEAD**
    - **행의 순서대**로 각 **이전 값, 이후 값** 을 가져옴
        - LAG(대상컬럼, 숫자)  ::  **입력 숫자** 이**전**  값
        - LEAD(대상컬럼, 숫자) :: **입력 숫자** 이**후** 값
    - **ORDER BY 절이 필수** 이다.
        - **원하는 값**을 가져오기 위해서는 **당연한 결과**
    - 예시 - LAG
        
        ```sql
        # 바로 이전 입사자와 급여를 비교 쿼리
        SELECT
            ENAME, HIREDATE, SAL,
            -- 정렬을 통해 원하는 순서로 맞춰줌으로 전 입사자 값을 가져옴
            LAG(SAL) OVER(ORDER BY HIREDATE) AS '바로_전_입사자_급여'
        FROM EMP;
        
        -- Result
        ENAME 	HIREDATE	   SAL	바로_전_입사자_급여
        Smith  2020-01-10	  3000	 NULL
        Allen  2020-03-20	  3200	 3000
        Ward 	 2020-05-15	  3500	 3200
        Jones	 2020-11-01	  4000	 3500
        ```
        
    - 예시 - LEAD
        
        ```sql
        # 바로 다음 금여를 더 낮게 받는 직원순서대로 쿼리
        SELECT
            ENAME,
            SAL AS "내 급여",
            LEAD(SAL) OVER(ORDER BY SAL DESC) AS "다음_낮은_급여"
        FROM
            EMP;
        
        -- Resut
        ENAME	  내 급여	   다음_높은_급여
        Jones	  2975	      2850
        Blake	  2850	      1600
        Allen	  1600	      1250
        Ward	  1250	      800
        Smith	  800	        NULL
        ```
        
- **FIRST_VALUE, LAST_VALUE**
    - 정렬 순서대로 정해진 범위에서의 **처음 값**, **마지막 값 출력**
    - 순서와 범위 지정에 따라 **최소값과 최대값**이 **리턴 가능**하다
    - 중요 사항
        - **LAST_VALUE**의 경우 최대값을 가져오려면 **기본 설정만**으로는 **불가능**
            - **Between**의 "B”기본 값이 현재 행이기 때문이다
                - 해결 방법
                    
                    ```sql
                    SELECT
                    	LAST_VALUE( 대상컬럼 ) OVER(
                    				# 처음 값 ~ 마지막행까지!! 의 범위이다.
                    				RANGE BETWEEN UNBOUNDED PRECDEING AND UNBOUNDED FOLLOWING 
                    			)
                    FROM 테이블;
                    ```
                    
- **NTILE**
    - 행을 **특정 컬럼 순서**에 따라 **정해진 수의 그룹**으로 나누기 위한 함수
        - 쉽게 말해 **총 행 나누기 숫자 임**
    - **ORDER BY 필수**
    - **PARTITION BY** 를 사용하여 **특정 그룹을 또 원하는 수만 만큼 그룹 분리** 가능
    - 예시
        
        ```sql
        # 급여 순서대로 정렬후 전체의 행에서 2로 나눔
        SELECT
        	ENAME, SAL, DEPTNO
        	, NTILE(2) OVER (ORER BY SAL) AS ‘급여 순서대로 2개로 나눔’
        FROM EMP;
        
        -- Result
        | ENAME | SAL  | DEPTNO | 급여 순서대로 2개로 나눔 |
        |-------|------|--------|--------------------------|
        | SMITH | 800  | 20     | 1                        |
        | ALLEN | 1600 | 30     | 1                        |
        | WARD  | 1250 | 30     | 1                        |
        | JONES | 2975 | 20     | 2                        |
        | BLAKE | 2850 | 30     | 2                        |
        ```
        
- **비율 관련 함수**
    - 1) **RATIO_TO_REPORT**
        - **각 값의 비율** 반환 (**전체 비율** 또는 **특정 그룹 내 비율** 가능)
        - ORDER BY **사용불가 ::** 당연한 결과 어차피 비율이라 정렬  불 필요
            - **예시**
            
            ```sql
            SELECT
                ENAME,
                SAL,
            		## 전체 급여기준 각각의 비율
                RATIO_TO_REPORT(SAL) OVER () AS SAL_RATIO
            FROM
                EMP;
            
            -- Result
            | ENAME | SAL  | SAL_RATIO      |
            |-------|------|----------------|
            | SMITH | 800  | 0.099875156    |
            | ALLEN | 1600 | 0.199750312    |
            | WARD  | 1250 | 0.155718475    |
            | JONES | 2975 | 0.371266004    |
            | BLAKE | 2850 | 0.373389053    |
            ```
            
    - 2) CUME_DIST
        - 각 **값의 누적 비율** 반환
        - **ORDER BY 필수**  :: 당연한 결과 **누적이니까 순서 중요!!**
        - 예시
            
            ```sql
            SELECT
                ENAME,
                SAL,
                CUME_DIST() OVER (ORDER BY SAL) AS SAL_CUM_DIST
            FROM
                EMP;
            
            -- Result :: 포인트는 비율 기준이 최종 누적 값이라는 것!
            | ENAME | SAL  | SAL_CUM_DIST   |
            |-------|------|----------------|
            | SMITH | 800  | 0.2            |
            | ALLEN | 1600 | 0.4            |
            | WARD  | 1250 | 0.6            |
            | JONES | 2975 | 0.8            |
            | BLAKE | 2850 | 1.0            |
            ```
            
    - 3) PERCENT_RANK
        - 전체 COUNT 중 **상대적 위치 출력**( 0 ~ 1 범위 내 소수점 으로 출력)
        - **ORDER BY 필수**
        - 예시
            
            ```sql
            SELECT
                ENAME,
                SAL,
            		# 요건 누적값에 대한 비율
            		CUME_DIST() OVER (ORDER BY SAL) AS SAL_CUM_DIST,
            		# 요건상대적인 위치 :: 잘보면 가장 낮은게 0 , 가장 높은게 1 이고
            		# 나머지 안에 값을 더 하면 1이 나옴
                PERCENT_RANK() OVER (ORDER BY SAL) AS SAL_PERCENT_RANK
            FROM
                EMP;
            
            -- Result
            | ENAME | SAL  | SAL_CUME_DIST | SAL_PERCENT_RANK |
            |-------|------|---------------|------------------|
            | SMITH | 800  | 0.2           | 0                |
            | WARD  | 1250 | 0.4           | 0.25             |
            | ALLEN | 1600 | 0.6           | 0.5              |
            | BLAKE | 2850 | 0.8           | 0.75             |
            | JONES | 2975 | 1             | 1                |
            ```
            

### TOP N QUERY

- **페이징 처리**를 **효과적으로 수행**하기 위해 사용
- 전체 결과에서 **특정 N개 추출**
- **Top-N행 추출 방법**
    - ROWNUM
        - 절대적 행 번호가 아니라 **출력대로 바뀌는 번호이다.** 따라서 **EQUI** 연산 **사용 불가능**
        - 첫번째 행이 증가한 이후 할당 되므로 **‘>’ 연산 사용 불가** (0은 가능해)
        - **“=”** 또한 **사용 불가능**
        - 🔥 **포인트**
            - 1을 포함하지 않으면 **조회 불가능**
        - **‘<=‘ 을 사용하면**  조회 가능
            
            ```sql
            # 조회 가능 ⭕
            Select * FROM EMP WHERE ROWNUM <= 5;
            
            # 조회 불가능 ❌
            Select * FROM EMP WHERE ROWNUM = 5;
            ```
            
        - **정렬 후 ROW_NUM으로 순위 뽑기**는 **불가능**해 하다
            - **Query 실행 순서** 생각해보면 당연한 결과이다.
            - 함정으로 내기 좋은 문제
                - 예시
                    
                    ```sql
                    # 급여 순위 1 ~ 5등 뽑기
                    
                    # 이건 당연히 안나옴 Order by는 가장 마지막임..
                    SELECT
                    	ENAME, SAL
                    FROM EMP
                    	WHERE ROWNUM <= 5
                    ORDER BY SAL DESC;
                    
                    # 맞게 하려면?
                    SELECT
                    	* 
                    FROM(
                    	SELECT
                    		*
                    	FROM EMP
                    		ORDER BY SAL DESC
                    	) 
                    WHERE ROWNUM <= 5
                    ```
                    
            - 예시 - 응용문제
                
                ```sql
                # 4 ~ 6등 ROW_NUMBER 사용 출력
                
                # 조회 불가능 ❌
                SELECT 
                	* 
                FROM ( SELECT * FROM EMP ORDER BY SAL DESC )
                  # 시작값 1을 건너뛴 후 그다음 행번호 출력이 불가능함
                	WHERE ROWNUM BETWEEN 4 AND 6
                ORDER BY SAL DESC;
                
                # 옳바른 사용법 💯
                SELECT * 
                FROM (
                    SELECT 
                        E.*, ROWNUM AS RN
                    FROM (
                        SELECT * FROM EMP ORDER BY SAL DESC
                    ) E
                )
                WHERE RN BETWEEN 4 AND 6
                ORDER BY SAL DESC;
                ```
                
    - RANK
        - 윈도우 함수 사용
            - 예시
                
                ```sql
                SELECT
                	* 
                FROM (
                    SELECT
                				# 랭크를 사용해서 정렬 후 RANK란 이름으로 Alias 지정 
                        E.*, RANK() OVER (ORDER BY SAL DESC) AS RANK
                    FROM EMP E
                )
                	# Betweent을 사용하여 추출
                	WHERE RANK BETWEEN 4 AND 6
                ORDER BY SAL DESC;
                ```
                
    - FETCH
        - 출력될 **행의 수를 제한**
        - **Oracle 12C 이상**부터 제공
        - SQL-SERVER 사용 가능
        - ORDER BY절 **뒤에서 사용 함**
        - 문법
            
            ```sql
            SELECT
            	*
            FROM 테이블
            	WHERE ??
            GROUP BY
            	HAVING
            ORDER BY
            	# 지금부터 문법시작
            	OFFSET 숫자 { ROW | ROWS }. --- 건너 뛸 행의 수 입력
            FETCH { FIRST | NEXT } 숫자 { ROW | ROWS } ONLY;
            ```
            
            - OFFSET : **건너 뛸 행의 수**
            - FETCH : 출력할 **행의 수 전달**하는 구문
            - FIRST : OFFSET을 쓰지 않을 경우 제외한 행 **다음부터 N행 출력** 명령
            - ROW | ROWS : 행의 수의 따라 하나일 경우 단수, 여러값이면 복수형 ( **구분 크게 중요하지 않음** )
        - 예시
            
            ```sql
            # 급여 순서대로 상위 5명
            SELECT
            	ENAME, SAL
            FROM EMP
            	ORDER BY SAL DESC
            # 스킵할 부분 없으니 OFFSET 제외
            # 처음 ~ 5개 출력
            FETCH FIRST 5 ROWS ONLY;
            
            ---------------------------------
            
            # 급여 순서대로 4 ~ 6등
            SELECT
            	ENAME, SAL
            FROM EMP
            	ORDER BY SAL DESC
            # 4등 부터이기에 OFFSET 설정
            OFFSET 3 ROW
            # 4 ~ 6(4+2)개 출력
            FETCH FIRST 2 ROWS ONLY;
            ```
            

### 계층형 질의

- 하나의 테이블 내 각 행 끼리 관계를 가질때, 연결 고리를 통해 **행과 행사이 계층을 표현함**
- 가상 컬럼
    - LEVEL : 댑스를 표현 (시작점 부터 1)
    - CONNECT_BY_ISLEAF : LEAF NODE(최하위노드) 여부를 알려줌 :: ( 참 :1 , 거짓 : 0 )
- 계층형 질의 가상 함수
    - CONNECT_BY_ROOT 컬럼명 : 해당 노드의  **루트 노트값 출력**
    - SYS_CONNECT_BY_PATH( 컬럼, 구분자 ): 이어지는 경로  출력
    - ORDER SIBILING BY 컬럼 :  같은 LEVEL일 경우 정렬 수행
- 주의사항
    - **PRIOR**의 **위치에 따라** 연결하는 **데이터가 달라진다.**
- 문법
    
    ```sql
    SELECT
    	FROM 테이블명
    START WITH 시작조건           --- 시작점을 지정하는 조건
    	CONNECT BY PRIOR 연결조건   --- 시작점 기준으로 하위 계급을 찾아가는 조건
    ```
    
- 예시
    
    ```sql
    # 각 부서의 레벨 출력
    SELECT
    	D.*, LEVEL
    FROM DEPT2 D
    # 시작이 될 조건 PDEPT 부모 부서번호는 최상위는 NULL이기에 조건 
    START WITH PDEPT IN NULL
    	# **PRIOR는 대상이 될 자식임!! = 부모의 코드와 같은것**
    	CONNECT BY **PRIOR** DCODE = PDEPT;
    
    ##### 아래의 코드는 값이 사장실만 나옴!! PRIOR이 최상위 코드에 갔기 떄문에 이전이 없음!
    ### 	CONNECT BY DCODE = **PRIOR** PDEPT;
    ```
    
- 예시2 - 함정 문제
    - 조건이 붙을 경우 **WHERE 조건이 아님!!** 따라서  하위 계층에는 영향이 갈 수 있으나 상위는 포함만 된다면 “서울”로해도 사장실이 나올 수 있음
    
    ```sql
    SELECT
    	D.*, LEVEL
    FROM DEPT2 D
    START WITH PDEPT IN NULL
      # 서울 지사이지만 상위 부서가 인천이면 인천도 나옴!!
    	CONNECT BY **PRIOR** DCODE = PDEPT AND AREA = '서울시자';
    ```
    

### PIVOIT 과 UNPIVOT

- 데이터의 구조
    - Long Data (Tidy data )
        - 우리가 평소에 보는 RDB 데이터 그자체 잘 정규화된 **아래로 긴 데이터 구조**
    - Wide Data
        - 컬럼에 값을 넣고 Row마다 갯수 같은걸 넣어서 보기는 편하지만 Join에는 어려움
        - **가로로 긴 ~ 형식**의 데이터 구조
- PIVOT
    - Long → Wide 데이터 **구조로 바꾸는 것**
    - 사용 방법
        - 쉽게 설명하면
            - **맨 왼쪽** 세로 : Stack 컬럼
            - **최 상단** 가로 : UnStack 컬럼
            - **나머지 값**들 : Value 컬럼
        - 중요 포인트
            - FROM 절에 선언 된 컬럼 중 PIVOT에서 **UnStack, value에 쓰지 않은 컬럼**이 **모두 Stack이 되어** 버림
                - 예시
                    
                    ```sql
                    # ❌ Stack에 사용하지 않은 2개의 컬럼이 나와버리는 문제
                    #    --- 너무 적어도 문제임 Unstack, value만 나옴...
                    SELECT *
                    	FROM 테이블 -- 컬럼이 4개있음
                    # PIVOT 사용
                    PIVOT ( VALUE count(컬럼1) FOR UNSTACK 컬럼명2 IN (값1,값2,값3) );
                    ```
                    
        - 예시
            
            ```sql
            # 직급별 사원 수
            SELECT *
            	# 포인트는 서브 쿼리를 사용해서 컬럼수를 제한 한것임!! 필요한 거만 딱 넣는게 포인트
            	FROM ( SELECT EMPNO, JOB, DEPTNO FROM EMP )
            # value는 사람의 합, Unstack의 값은 10,20,30인 애들로만 필터링
            PIVOT ( VALUE SUM(EMPNO) FOR DEPTNO IN (10,20,30) );
            ```
            
- UNPIVOT
    - Wide → Long  데이터 **구조로 바꾸는 것**
    - PIVOT과는 다르게 서브쿼리로 **컬럼 제한 필요 없음**
    - 쉽게 설명
        - 기존 Stack은 안바꿔도 되니 냅두고
        - Value는 값이니 사용할 컬럼명 지정
        - Unstack부분 또한  컬럼명 지정 후 사용 값 IN으로지정
    - 예시
        
        ```sql
        SELECT * 
        	# 서브쿼리로 컬럼 제한 필요 없음
        	FROM  EMP
        # VALUE의 컬럼명 지정
        UNPIVOT ( 개수
        			# UnStack의 컬럼명 지정 후 사용 값 지정
        			FOR 년도 IN ("2005","2020")
        		 );
        ```
        

### DCL

- 권한 종류
    - 오브젝트 권한
        - 테이블에 대한 권한 제어
            - 특정 테이블에 대한 **DML 권한**
            - **테이블 소유자**는 타 계정에 대한 테이블  조회  및 수정 **권한 부여 및 회수 가능**
    - 시스템 권한
        - 시스템 작업(테이블 생성, 제거, 수정)등을 제어
            - DDR제어
        - **관리자 권한만** 부여 및 회수 가능
- **GRANT**
    - 권한 부여 시 반드시 테이블 소유자나 관리자 계정으로 접속하여 권한을 부여 해야함
    - **동시에 여러 유저에 대한 권한 부여 가능**
    - **동시에 여러 권한 부여 가능**
    - 동시 여러 객체 **권한 부여 불가능**
    - 문법
        
        ```sql
        GRANT 권한 ON 테이블명 TO 유저;
        ```
        
    - 예시 - 오브젝트 권한 부여 :  테이블 **관리 권한**이 있으면 부여 가능
        
        ```sql
        # 고양이한테 급여 테이블 조회 권한주기
        GRANT SELECT ON 급여 TO 고양이;
        # 고양이, 강아지한테 급여 테이블 조회 권한 주기
        GRANT SELECT ON 급여 TO 고양이, 강아지;
        # 고양아한테 CRU 권한 주기
        GRANT SELECT, INSERT, UPDATE ON 급여 TO 고양이;
        # ❌ 여러 테이블 한번에는 불가능
        GRANT SELECT ON 급여, 출퇴근이력 TO 고양이;
        ```
        
    - 예시 - 시스템 권한 부여 :  **관리자 권한**이 있으면 부여 가능
        
        ```sql
        # 테이블 생성 권한
        GRANT CREATE TABLE TO 고양이;
        # 고양이, 강아지한테 테이블 생성 권한
        GRANT CREATE TABLE TO 고양이, 강아지;
        # 테이블 생성, 삭제 권한 부여 
        GRANT CREATE TABLE,  DROP ANY TABLE TO 강아지;
        ```
        
- REVOKE
    - 권한을 **회수**하는 명령어
    - **동시**에 **여러 권한 회수** 가능
    - 이미 회수된 권한 **재회 수 불가능**
    - 동시 **여러 유저로 부터**의 **권한 회수 가능**
    - 문법
        
        ```sql
        # TO에서 FROM으로만 바뀌는거임
        REVOKE 권한 ON 테이블명 FROM 유저명;
        ```
        
    - 예시 - 오브젝트 권한 회수
        
        ```sql
        REVOKE SELECT, UPDATE, INSERT ON 급여 FROM 강아지;
        REVOKE SELECT ON 급여 FROM 고양이, 강아지;
        # ❌ 에러발생 했던 회수 또하면 에러
        REVOKE SELECT ON 급여 FROM 고양이, 강아지;
        ```
        
- ROLE(롤)
    - **권한**의 **묶음**이다
    - SYSTEM 계정에서 생성 가능
    - 즉시 적용이 안되므로 부여 후 해당 사용자 재 접속 필요
    - **권한 부여**를 **한번에 하기** 위해 만든것이다!
    - 사용방법
        - 1 . 롤 생성
            
            ```sql
            CREATE ROLE 롤이름;
            ```
            
        - 2 . 롤에 사용할 권한 담기
            
            ```sql
            GRANT SELECT ON EMP TO 롤이름;
            GRANT SELECT ON STUDENT TO 롤이름;
            GRANT SELECT ON ~~~ TO 롤이름;
            ```
            
        - 3 . 사용자에게 롤 부여
            
            ```sql
            GRANT 롤이름 TO 대상;
            ```
            
        
        ---
        
        - 롤에서 권한 뺴기
            
            ```sql
            REVOKE SELECT ON DEPARTMENT FROM 롤이름;
            ```
            
            - 포인트
                - 바로 적용 가능
                - 롤을 통해 권한을 부여하면 롤에서 권한을 빼야함 **대상에게 바로 권한 뻇기 불가능**
    - 권한 부여 옵션
        - WITH GRNAT OPTION ( 중간 관리자의 옵션 )
            - WITH GRANT OPTION 으로 받은 **오브젝트 권한**을 **다른 사용자에게 부여할 수 있음**
            - 중간관리자가 부여한 권한은 **중간 관리자만 회수 할 수 있음**
            - 중간 관리자에게 부여된 **권한 회수** 시 제 3자에게 부여된 권한도 **함께 회수**
            - 예시
                
                ```sql
                -- SYS 계정에서 실행
                GRANT SELECT ON SCOTT.EMP TO 유정호 WITH GRANT OPTION;
                
                -- 유정호 실행
                GRANT SELECT ON SCOTT.EMP TO 흑곰;
                
                -- SYS 계정 회수 시도 ::: 실패
                REVOKE SELECT ON  SCOTT.EMP FROM 흑곰;
                ```
                
        - WITH ADMIN OPTION
            - WITH ADMIN OPTION을 통해 부여받은 **시스템 권한 / 롤 권한을 다란사람에게 부여할 수있음**
            - 중간 관리자를 거치지 않고 **제 3자 권한 직접 회수 가능**
            - 중간 관리자 권한 회수 시 제 3자에게 부여된 권한 함께 회수 ❌
            - 예시
                
                ```sql
                -- SYS 계정에서 실행
                GRANT CREATE ANY TABLE TO 유정호 WITH ADMIN OPTION;
                GRANT ALTER ANY TABLE TO 유정호 WITH ADMIN OPTION;
                
                -- 유정호 실행
                GRANT CREATE ANY TABLE ON SCOTT.EMP TO 흑곰;
                
                -- SYS 계정 회수 시도 ::: 성공
                REVOKE CREATE ANY ON  SCOTT.EMP FROM 흑곰;
                
                ```
