---
layout : single
title : "데이터베이스의 필요성"
---
# Today I Learned

# 데이터베이스는 왜 필요한가?
## 모든 서비스는 데이터를 만들어내고 그 데이터의 저장을 필요로 한다.

예) 카카오톡
+ 사용자 등록시 사용자 정보(ID, 암호, 전화번호 등등)의 저장이 필요하다.
+ 사용자 친구 리스트의 관리가 필요하다.(친구들의 ID 저장)
+ 특정 사용자 혹은 단톡방에서의 채팅 기록을 저장해야한다.


## 어디에 데이터를 저장해야할까?  

+ 프로덕션 관계형 데이터베이스(RDBMS), 예) MySQL, PostgreSQL...
  + 어떤 서비스의 운영에 필요한 데이터를 저장하는 곳
  + 빠른 처리속도가 중요하다.
  + 데이터를 구조화된 테이블들의 집합으로 구성하여 저장하고 관리한다.
  + 백엔드, 프론트엔드 개발자 상관없이 잘 알아야 하는 기본 기술이다.
  + 관계형 데이터베이스의 프로그래밍 언어가 SQL이다.


+ 데이터 웨어하우스, 예) BigQuery, Snowflake, MySQL...
  + 회사관련 데이터를 저장하고 분석함으로서 의사결정과 서비스 최적화에 사용한다.
  + 처리속도보다는 구조화된 큰 데이터를 처리하는 것이 중요하다.

## 다양한 데이터베이스의 종류

+ 관계형 데이터베이스 : 구조화된 데이터
  + 프로덕션용 관계형 데이터베이스
  + 데이터 웨어하우스용 관계형 데이터베이스
  
+ 비관계형 데이터베이스 : 비구조화 데이터도 다룸
  + 흔히 NoSQL 데이터베이스라고 부르기도 한다.
  + 보통은 프로덕션용 관계형 데이터베이스를 보완하기 위한 용도로 많이 사용된다.
  + 크게 4종류가 존재한다.
    + Key/Value Storage: Redis, Memcache, ...
    + Document Store: MongoDB
    + Wide Cokumn Storage: Cassandra, HBase, DynamoDB
    + Search Engine: ElasticSearch






+프로그래머스 (실리콘밸리에서 날아온 데이터베이스편) 한기용 강사님 자료 참고.








