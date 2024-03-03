# **SQLD 정리**

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

### NULL의 특성

- **NULL을 포함한 연산 결과**는 **항상 NULL**이다
- 필요할 경우 “**NVL(대상 , 0)**”을 통해 **치환하여 계산**해 주자
- **집계 함수**는 NULL을 **제외한 연산 결과**를 **리턴**한다.
    - sum, avg, min, max등의 함수는 NULL을 제외하고 계산해준다.
- ⭐️ 함정으로 내기 좋은 문제
    - 각 특정 컬럼에 NULL이 존재할 경우 평균을 구하려 할 경우
        - 그냥 AVG(CMM)를 사용하면 **NULL을 제외한 평균**이 계산 된다
        - SUM(CMM) / COUNT(*) 로 계산 할 경우 NULL을 포함한 **모든 인스턴스의 평균**이 나옴

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
    - Create, Alter, Drop, Rename, Truncate( delete와 유사 하나 메모리까지 날리고 오토 커밋임 )

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

### Alias 주의사항

- 이미 있는 **예약 어 사용 금지**
- 띄어쓰기 금지
    - 원하면 ‘’ 를 사용해서 묶어서 사용해주자
        - Ex) ‘흑곰은 왕왕 띄어쓰기 귀엽다’

### Like 연산자

- _S% 이름 둘째가 S로 시작하는거
- __S__ 가운데가 S이면서 5글자

## Join

- 국가 표준은 **ANSI** 표준이다
- Oracle 과 ANIST **표준이 서로 다르다**
    - Oracle의 경우 **테이블의 나열 순서가 중요하지 않음**
    - ANSI 표준은 **Outer Joint 시 순서 중요**하다
- N 개의 테이블 조인 시 **최소 N-1 개의 조인 조건이 필요**하다

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

- 서브 쿼리
    - 주의 사항 : 서브쿼리 내부에서 Order By 사용이 불가능함 에러발생!!
    - 단일행
        - =, <>, >, >=, < ,<= :: 와 같이 단일된 값으로 조건이 가능한 애들사용
    - 다중행
        - 서브쿼리 결과가 여러 행으로 리턴 될 경우
            - IN : 해당 절에 값이 같은 애를 찾음
            - > ANY : 최소값을 반환
            - < ANY : 최대값을 반환
            - < ALL : 최소값을 반환
            - > ALL : 최대값을 반환
        - 다중 행은 당연히 equals비교가 불가능하다! 그렇기에 서브 쿼리 내에서 조인을 통해 값을 정제 후 사용

- 인라인 뷰 서브쿼리
    - Where 절에서 사용하는 것이 아닌 From 절에서 사용하여 서브 쿼리로 사용하는 것
        - 따라서 조회하려는 대상이 함수 형식이라면 Alisa를 사용해 줘야함
        - 테이블 또한 Alias로 지정해 줘야한다

- 스칼라 서브쿼리
    - Select 문 내에서 서브 쿼리를 사용하는 것
    - 당연히 단일 행이 나와야한다 왜냐면 Select에서 값이 나와야한는걸!!
        - 따라서 WHERE 절은 필수이며 메인 쿼리 Where 절의 비교대상과 같은 값으로 사용해서 단일 값 뽑자
            - Select

ENPNO

, ( Select

DNAME

FROM DEPT D

WHERE D.DEPTNO = E.DEPTNO ) AS DNAME

FROM EMP E

WHERE DEPTNO = 10;

- 집합 연산자
    - 주의사항
        - 두집합의 조회하려는 컬럼수가 같이야 한다. ( 에러 반환 )
        - 두집합의 컬럼 순서가 같아야한다
            - 컬럼의 명이 다를 경우 가장 첫번쨰 걸로 나온다 ::: 따라서 Alias를 사용해서 통일 시켜주자
        - 두 집합의 각 컬럼의 데이터 타입 일치
        - 컬럼의 데이터타입이 일치한다면 사이즈는 달라도 된다.
        - 중복 제거의 조건은 모든 ROW가 같아야 제거하는것이다 중요함!! ✨
        - ;는 중간에 넣으면 안돼!! 마지막에 넣자
    - UNION, UNION ALL
        - UNION : 중복 제거를 원한 시
        - UNION ALL : 중복데이터 포함 모든 데이터

- 그룹 함수
    - NULL은 항상 제외하고 실행된다
    - COUNT(), AVG() 또한 NULL을 제외하고 숫자를 세준다.
        - 따라서 AVG의 경우 NULL인 값을 포함해서 계산하려면 방법이 2가지 존재
            - SUM(COMM) / COUNT(*) 을 통한 계산
            - AVG(NVL(COMM,0)) 을 통한 계산 ::: NULL일 경우 0으로 치환해서 사용
    - Oracle의 경우 명령어가 다른것이 2개 있음
        - VARIANCE(). :: 평균
        - STDDEV() :: 표준 편차

- Group By Function
    - Group By 절에서 사용이 가능하다
    - 여러 Group By 결과를 동시에 출력하기 위한 기능이다
    - 그룹화 할 정의 한다
    - ———————-
    - 1. Grouping Sets(a, b, c, d, ….)
        - A, B 별 그룹 연산 결과를 합쳐서 출력해줌 — 중복 제거 따위 없음 그룹화가 메인 목적임
        - 만약 각각 그룹화 시 데이터가 없는 컬럼이 있다면 null로 알아서 채워서 반환
        - 기본 출력에는 전체 총계는 출력하지 않음
            - 마지막 인자에 null 혹은 ()을 넣으면 맨 마지막 Row에 총계를 계산해 줌
                - Group By Grouping Sets(DEPTNO, JOB, ()); ## 최종 쿼리 마지막 ROW에 총합
        - 예시
            - Select

DEPTNO, JOB, SUM(SAL)

FROM EMP

GROUP BY Grouping Sets( DEPTNO, JOB ) ; # 통 그룹화가 아닌 각각 그룹화 하고 싶음!!

- UNION ALL 로도 똑같은 반환 쿼리 사용이 가능하다.

- SELECT

DETPNO, NULL AS JOB, SUM(SAL)

FROM EMP

GROUP BY DEPTNO

UNION ALL

SELECT

NULL AS DETPNO, JOB, SUM(SAL)

FROM EMP

GROUP BY JOB

- ——————————

- 2. ROLLUP

- 순서가 굉장히 중요하다

- 기본적으로 전체 통계를 알려준다

- Rollup의 첫번째 인자를 구분으로 메인 롤링이 되어 그루핑이 된다.

- 최종 로우값에는 맨 마지막 SUM() 부분에 집계 총합이 들어가고 앞컬럼은 다 null이다

- 사용 예시

Select

DEPTNO, JOB, SUM(SAL)

FROM EMP

GROUP BY ROLLUP(DEPTNO, JOB);

- ——————————

- 3. Cube(A,B)

- A별, B별, (A,B)별, 전체 그룹 연산 결과를 출력

- 총 4개의 그룹이 나옴. [.총합 통계가 나오기 떄문임 ]

- 순서는 중요하지 않음

- 기본적으로 전체 통계를 알려줌

- Grouping Sets()로도 똑같은 값이나오게 처리 가능

- 예시

Select

DEPTNO, JOB, SUM(SAL)

FROM EMP

GROUP BY Cube(DEPTNO, JOB);

- Window Function
    - 서로 다른 행의 비교나 연산을 위해 만든 함수
        - 쉽게 설명 전체 목록에 집계 함수를 사용해야할 경우
            - 서브 쿼리로 처리가 가능하나 성능에 좋지 못함
                - Ex) SELECT EMPNO, SUM(SAL) FROM EMP; ## 에러 발생 그룹바이 쓰면 원하는 값 아님!
    - Group By를 사용하지 않고 그룹연산이 가능
    - 문법의 순서를 지키는 것이 중요하다
    - 종류
        - LAG, LEAD, SUM, AVG, MIN, MAX, COUNT, RANK
    - 문법
        - Select 윈도우 함수( 대상 ) OVER ( PARTITION BY 컬럼

ORDER BY 컬럼 DESC | ASC

ROWS | RANGE BETWEEN A AND B

);

- PARTITION BY 절

- 출력할 총 데이터 수 변화 없이 그룹 연산 수행할 GROUP BY 컬럼

- ORDER BY 절

- RANK를 사용할 경우 필수 이며 , 정렬 컬럼 및 정렬 순서에 따라 순위 변화

- SUN, AVG, MIN, MAX, COUNT 등은 누적값 출력 시 사용

-  ROWS | RANGE BETWEEN A AND B 절

- 연산 범위 지정

- ORDER BY 절 필수

- —————————

- 그룹 함수 형태

- SUM, COUNT, AVG, MIN, MAX 등

- OVER() 절을 이용하여 윈도우 함수로 사용이 가능하다

- 반드시 연산할 대상을 그룹함수의 입력잡으로 전달해주자

- SUM

- Ex) SELECT EMPNO, SUM(SAL) OVER() AS TOTAL FROM EMP

- 누적된 값을 계산함 층층층층 Order BY 절이 없으므로 순서를 보장 못해서 값이 이상할것임

- AVG

- Ex) SELECT EMPNO, AVG(SAL) OVER() AS TOTAL FROM EMP ; ##모두가 같은 전체 평균

- SELECT EMPNO, AVG(SAL) OVER( PARTITION BY DEPTNO ) AS TOTAL FROM EMP ;

- ## 부서별 평균 적용

- 사실 모든 문법이 같으니 앞에만 바꿔서 적용해주자

- 윈도우 함수의 연산 벙위 설정 : 집계 연산 시 행의 범위 설정 가능

- ROWS, RANGE를 구분자로 사용해서 BETWEEN을 붙여서 사용

- ROWS : 값이 같더라도 각 행씩 연산

- Ex) 같은 값이 나오면 누적 시 당연 누적 해서 계속 계산

- RANGE : 같은 값의 경우 하나의 Range로 묶어서 동시 연산 [ 기본 값  ]

- BETWEEN A AND B

- A) 시작점 정의

- CURRENT ROW : 현재 행부터

- UNBOUNDED PERCENDING : 처음부터 [ 기본값 ]

- N PRECEING : N 이전 부터

- B) 마지막 시점 정의

- CURREND ROW : 현재행까지 [ 기본값 ]

- UNBOUNDNDED FOLLWING : 마지막까지

- N FOLLOWiNG : N 이후까지

———————

- SELECT R.* m SUM(SAL) OVER( ORDER BY SAL ) FROM RANGE_TEST R;

- SELECT R.* m SUM(SAL) OVER( ORDER BY SAL

ROW BETWEEN UNBOUNDED PRECEDING AND CURRENT ROW

) AS RESULT1

FROM RANGE_TEST R;

- RANK(순위)

- 특정값에 대한 순위 확인

- RANK WITHIN GROUP

- SELECT RANK(값) WITHIN GROUP( ORDER BY 컬럼 )

- RANK() OVER()

- 전체 중/ 특정 그룹 중 값의 우선순위 확인

- ORDER BY 절 필수

- 순위를 구할 대상을 ORDER BY 절에 명시 ( 여러개 가능 )

- 그룹 내 순위 구할 시 PARTITION BY 절 사용

- 예시 [ 각 직원의 급여의 전체 순위 ] **  동순위가 나오면 처리후 다음은 +N으로 처리 **

SELECT ENAME, DEPTNO, SAL

, RANK() OVER( ORDER BY SAL DESC ) AS ‘돈 많이 받는 순위’

FROM EMP;

- 예시2 [ 각 직원의 부서별 급여 순위  ]

SELECT ENAME, DEPTNO, SAL

, RANK() OVER( 	PARTITION BY DEPTNO

ORDER BY SAL DESC ) AS ‘부서별 돈 많이 받는 순위’

FROM EMP;

- DENSE_RANK()

- RANK랑 사용방법은 똑같으나 동일한 순위 부여 후 다음 순위가 바로 이어지게 함

- ROW_NUMBER

- 연속된 행 번호

- 동일한 순위를 인정하지 않고 단순히 순서대로 나얼하는 기능 순서값 리턴이야!!

- LAG, LEAD
    - 행의 순서대로 각 이전값(LAG, N ), 이후 값(LEAD, N ) 가져오기
    - ORDER BY 절이 필수 이며 원하는 값에 맞게 적절하게 정렬을 해줘야한다.
        - 바로 이전 입사자와 급여를 비교
            - SELECT ENAME, GIREDATE, SAL,

LAG(SAL) OVER(ORDER BY HIREDATE) AS ‘바로 입사자 급여임’

- FIRST_VALUE, LAST_VALUE
    - 정렬 순서대로 정해진 범위에서의 처음 값, 마지막 값 출력
    - 순서와 범위 지정에 따라 최솟값과 최대값이 리턴 가능하다
    - 중요 사항
        - LAST_VALUE의 경우 최대값을 사용하라면 정렬만으로는 불가능하다
            - 비교하려는 값의 마지막이기에 기준이 현재 행으로 Window 함수가 잡기때문
                - 해결 방법
                    - RANGE BETWEEN PRECDEING AND UNBOUNDED FOLLOWING 으로 잡아주자 ( 처음부터 ~ 무조건 마지막 행까지로 검사)

- NTILE
    - 행을 특정 컬럼 순서에 따라 정해진 수의 그룹으로 나누기 위한 함수
    - 그룹 번호가 리턴됨
    - ORDER BY 필수
    - PARTITION BY 를 사용하여 특정 그룹을 또 원하는 수만 만큼 그룹 분리 가능
    - 예시 :: [ 급여 순서대로 정렬후 전체 /2 해서 나눔 ]
        - SELECT ENAME, SAL, DEPTNO,

NTILE(2) OVER (ORER BY SAL) AS ‘급여 순서대로 2로 나눔’

FROM EMP;

- 비율 관련 함수
    - 1) RATIO_TO_REPORT
        - 각 값의 비율 리턴(전체 비율 또는 특정 그룹 내 비율 가능)
        - ORDER BY 사용불가
    - 2) CUME_DIST
        - 각 값의 누적 비율 리턴’
        - 누적이기에 ORDER BY 필수
    - 3) PERCENT_RANK
        - PERCENTILE(분위수) 출력
        - 전체 COUNT 중 상대적 위치 출략 ( 0 ~ 1 범위 내 소수점 으로 출력)
        - ORDER BY 필수

- TOP N QUERY
    - 페이징 처리를 효과적으로 수행하기 위해 사용
    - 전체 결과에서 특정 N개 추출

- Top-N행 추출 방법
    - ROWNUM
        - 절대적 행번호가 아니라 출력대로 바뀌는 번호가 아님 따라서 EQUI 연산 사용 불가능
        - 첫번째 행이 증가한 이후 할당 되므로 ‘>’ 연산 사용 불가 (0은 가능해)
        - 포인트!! 1을 포함하지 않으면 조회가 불가능해!!
        - ‘<=‘ 로는 조절해서 조회가능해
            - EX) Select * FROM EMP WHERE ROW_NUMBER <= 5;
        - 정렬 후 ROW_NUM으로 순위 뽑기는 불가능해 왜? Query 실행 순서 생각해봐
        - 문제 발생
            - 4 ~ 6 등인 애들만 뽑으려면 ??
                - FROM절 서브쿼리를 사용해서 ROW_NUMBER를 AS RN으로 뺸 후 RN BETWEEN 4 AND 6 사용하자
    - RANK
        - 윈도우 함수 사용
            - 4 ~ 6등을 원할 경우 AS RN 으로 빼내어서 사용하자
    - FETCH
        - 문법
            - SELECT
            - 
        - 예시로 보면 간단하다
            - 1 ~ 5등
                -
