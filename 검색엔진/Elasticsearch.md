JSON형식으로 데이터를 저장하고 검색할 수 있어서 NoSQL DB처럼 활용할 수 있는 검색 엔진

MySQL 같은 RDB는 정확하고 신뢰성 있는 데이터 저장이 강점
Elasticsearch는 빠르고 강력한 검색과 분석이 강점

|            | **Elasticsearch**     | **일반적인 데이터베이스 (MySQL, PostgreSQL 등)** |
| ---------- | --------------------- | ------------------------------------- |
| **주요 역할**  | 검색 및 분석 엔진            | 데이터 저장 및 관리                           |
| **저장 방식**  | JSON 문서 기반 (NoSQL)    | 테이블 기반 (SQL)                          |
| **데이터 구조** | 동적 스키마 (Schema-less)  | 고정된 스키마 (Schema-based)                |
| **쿼리 방식**  | 검색(DSL) 및 필터링         | SQL                                   |
| **성능 최적화** | 역색인 (Inverted Index)  | 인덱스 및 조인                              |
| **주요 특징**  | 빠른 검색, 분석, 실시간 데이터 처리 | 정합성 보장, 트랜잭션 지원                       |

저장 방법
**Elasticsearch**는 JSON 문서형태로 데이터를 저장한다.

MySQL 테이블 구조
```Sql
CREATE TABLE products (
    id INT PRIMARY KEY,
    name VARCHAR(255),
    category VARCHAR(255),
    price DECIMAL(10,2)
);
```

Elasticsearch 문서 구조
```Json
{
  "id": 1,
  "name": "MacBook Pro",
  "category": "Laptop",
  "price": 2500.00
}
```
이런 JSON 문서들이 Index 안에 저장된다

사용목적
검색과 분석이 필요한 경우에 최적화되어있다.
1. 빠른 검색이 필요할 때
	1. 쇼핑몰 상품 검색
	2. 뉴스, 블로그, 문서 검색
2. 대량의 로그 데이터를 분석할 때
	1. 서버 로그
	2. 애플리케이션 로그 저장 & 분석
3. 실시간 데이터 분석
	1. 실시간 대시보드
	2. 통계 분석 (Kibana와 함께 사용)

