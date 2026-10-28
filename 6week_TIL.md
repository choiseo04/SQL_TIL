# 📘 SQL_BASIC 6주차 정규 과제

SQL_BASIC 정규 과제는 매주 정해진 분량의 `초보자를 위한 BigQuery(SQL) 입문` 강의를 듣고, 핵심 개념을 정리한 뒤 간단한 SQL 문제를 직접 풀어보는 방식으로 진행합니다.

이번 주는 SQL 입문 과정의 핵심 고비인 `JOIN`을 학습합니다.

JOIN은 여러 테이블을 연결해서 분석 질문에 답하기 위해 반드시 필요한 개념입니다. 이번 주 과제에서는 정답 코드뿐 아니라 **어떤 테이블을 어떤 키로 연결했는지**를 꼭 기록해주세요.

완성된 과제는 Github에 업로드하고, 링크를 스프레드시트 'SQL' 시트에 입력해 제출해주세요.

**👀 수행 인증란은 필수입니다.**

---

## 📚 SQL_BASIC_6th_TIL

### 섹션 6. 다량의 자료를 연결 : JOIN

### 5-2. JOIN 이해하기

### 5-3. 다양한 JOIN 방법

### 5-4. JOIN 쿼리 작성하기

### 5-5. JOIN을 처음 공부할 때 헷갈리는 부분

---

## ✨ 선택 강의

- 5-6. JOIN 연습문제: JOIN 문제를 더 연습하고 싶을 때 선택 수강

---

## 🏁 전체 강의 수강 계획

| 주차 | 필수 강의 범위 | 선택 강의 | 완료 여부 |
| --- | --- | --- | --- |
| 1주차 | 1-1 ~ 2-1 | 1 | ✅ |
| 2주차 | 2-2 ~ 2-3 | 2-4 | ✅ |
| 3주차 | 2-5, 2-7 ~ 2-8 | 2-6 | ✅ |
| 4주차 | 3-2 ~ 4-3 | 3-4 | ✅ |
| 5주차 | 4-4 ~ 4-6 | 4-5, 4-7 | ✅ |
| 6주차 | 5-2 ~ 5-5 | 5-6 | ✅ |
| 7주차 | 필수 강의 없음 | 6-2, 6-3, 6-4, 6-5 | 🍽️ |

---

<br>

<!-- 여기까진 그대로 둬 주세요-->

---

# 1️⃣ 개념 정리

아래 키워드 중 중요하다고 생각한 개념을 2개 이상 골라 짧게 정리해주세요. 3개보다 더 많이 정리하고 싶다면 자유롭게 항목을 추가해도 좋습니다.

이번 주 키워드:
- JOIN
- INNER JOIN
- LEFT JOIN
- JOIN key
- alias
- NULL
- 다중 JOIN

## 01.

```
개념 이름:JOIN
개념 설명:서로 다른 테이블을 연결하는 것.
- (INNER) JOIN: 두 테이블의 공통 요소만 연결
- LEFT/RIGHT (OUTER) JOIN : 왼쪽/오른쪽 테이블 기준으로 연결
- FULL (OUTER) JOIN : 양쪽 기준으로 연결
- CROSS JOIN : 두 테이블의 각각의 요소를 곱하기
예시 쿼리:
INNER JOIN (ON 필수)
- SELECT col FROM table_a AS A INNER JOIN table_b AS B ON A.key = B.key
LEFT/RIGHT JOIN (ON 필수)
- SELECT col FROM table_a AS A LEFT/RIGHT JOIN table_b AS B ON A.key = B.key
FULL JOIN (ON 필수)
- SELECT col FROM table_a AS A FULL JOIN table_b AS B ON A.key = B.key
CROSS JOIN (ON 선택)
- SELECT col FROM table_a AS A CROSS JOIN table_b AS B
```

## 02.

```
개념 이름: JOIN Key
개념 설명: JOIN 하고자 하는 테이블들에 공통적으로 존재하는 컬럼. 이것이 있어야 JOIN할 수 있음. 공통적으로 존재하는 컬럼(=key)이 있다면, JOIN할 수 있으며, 보통 id 값을 key로 많이 사용하고 특정 범위로 JOIN도 가능함. 
예시 쿼리:
SELECT A.col1, A.col2, B.col1 1, B.col1 2 FROM table 1 AS A LEFT JOIN table2 AS B ON A.key = B.key #Alias 사용할 수 있음.
```

## (선택) 03.

```
개념 이름:
개념 설명:
헷갈린 점:
```

---

# 2️⃣ 수행 인증란

아래 중 하나 이상을 첨부해주세요.

- 강의 수강 화면 캡처
- JOIN 문제 풀이 정답 화면 캡처
- JOIN 전후 결과 row 수를 비교한 캡처 또는 메모

---

# 3️⃣ 확인 문제

프로그래머스는 로그인이 필요하므로, 로그인 후 문제 풀이를 진행해주세요.

## 🧩 문제 1

문제 링크: [조건에 맞는 도서와 저자 리스트 출력하기](https://school.programmers.co.kr/learn/courses/30/lessons/144854)

풀이 과정:

```
- 사용한 테이블: BOOK 테이블과 AUTHOR 테이블 
- JOIN key: AUTHOR_ID
- 날짜를 출력한 형식: YYYY-MM-DD
```

<!-- 정답을 맞추게 되면, 정답입니다. 이 부분을 캡처해서 이 주석을 지우시고 첨부해주시면 됩니다. -->

## 🧩 문제 2

문제 링크: [상품 별 오프라인 매출 구하기](https://school.programmers.co.kr/learn/courses/30/lessons/131533)

풀이 과정:

```
- 연결한 테이블: PRODUCT 테이블, OFFLINE_SALE
- JOIN key: PRODUCT_ID
- 집계한 값: SUM(PRICE * SALES_AMOUNT)
```

<!-- 정답을 맞추게 되면, 정답입니다. 이 부분을 캡처해서 이 주석을 지우시고 첨부해주시면 됩니다. -->

## 🧩 문제 3

문제 링크: [없어진 기록 찾기](https://school.programmers.co.kr/learn/courses/30/lessons/59042)

풀이 과정:

```
- 기준이 되는 왼쪽 테이블: ANIMAL_OUTS 테이블
- LEFT JOIN이 필요한 이유: 입양 기록은 유지하면서 보호소에 들어온 기록이 없는 동물을 찾기 위해서 필요하다. 
- NULL이 발생하는 경우: ANIMAL_ID는 존재하는데(보호소에 들어온 기록은 존재하는데) 이름이 NULL인 경우 
```

<!-- 정답을 맞추게 되면, 정답입니다. 이 부분을 캡처해서 이 주석을 지우시고 첨부해주시면 됩니다. -->

## 🧩 문제 4

문제 링크: [있었는데요 없었습니다](https://school.programmers.co.kr/learn/courses/30/lessons/59043)

풀이 과정:

```
- 사용한 테이블: ANIMAL_INS 테이블, ANIMAL_OUTS 테이블
- JOIN key: ANIMAL_ID
- 비교한 날짜 컬럼: ANIMAL_INS의 DATETIME(보호시작일)과 ANIMAL_OUTS의 DATETIME(입양일)
- 정렬 기준: A(ANIMAL_INS).DATETIME ASC(오름차순)
```

<!-- 정답을 맞추게 되면, 정답입니다. 이 부분을 캡처해서 이 주석을 지우시고 첨부해주시면 됩니다. -->

---

# 4️⃣ 참고 자료

JOIN 개념이 헷갈린다면 아래 자료를 함께 참고해도 좋습니다.

1. https://data-marketing-bk.tistory.com/entry/SQL-JOIN-%ED%95%9C-%EB%B0%A9%EC%97%90-%EC%A0%95%EB%A6%AC-%EA%B0%9C%EB%85%90%EB%B6%80%ED%84%B0-%EC%BD%94%EB%93%9C%EA%B9%8C%EC%A7%80-%EC%9D%B4%EA%B2%83%EB%A7%8C-%EB%B3%B4%EC%9E%90
2. https://velog.io/@wijoonwu/JOIN

---

# 5️⃣ 이번 주 회고

```
1. INNER JOIN과 LEFT JOIN의 차이를 어떻게 이해했는지: inner join은 두 테이블의 공통 요소만 연결하는 것이라면 left join은 왼쪽 테이블이 될 테이블을 정하고 왼쪽 테이블 기준으로 연결하는 것이다. inner join은 위치와 상관없이 동일한 값이 나오지만 left join은 왼쪽 테이블이 무엇이냐에 따라서 값이 달라질 수 있다. 
2. JOIN 문제를 풀 때 가장 먼저 확인해야 할 것: LEFT JOIN 사용 시 기준이 될 왼쪽 테이블 정하기.  
3. JOIN 결과가 예상과 달랐던 경험이 있다면: 3번 문제를 풀 때 조인키를 잘못 지정하여 예상과 다른 결과가 나왔다. 단순히 두 테이블의 공통 요소라고 해서 조인키로 지정하는 것이 아니라 문제가 요구하는 것과 해당 컬럼의 Null 여부 등을 고려하여 조인키를 지정해야 한다는 것을 깨달았다. 
```

수고하셨습니다!
