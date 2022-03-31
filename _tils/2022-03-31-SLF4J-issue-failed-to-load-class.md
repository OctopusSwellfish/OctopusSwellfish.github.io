---
layout: post
title: Failed to load class "org.slf4j.impl.StaticLoggerBinder" issue 해결
tags: 
- slf4j
- jeus
- was
- log
---

# `Failed to load class "org.slf4j.impl.StaticLoggerBinder"` issue

### 상황
* `jeus 8.5` 사용
* 해당 `was`에 `application` 올리면 아래와 같은 오류 발생하며 로그가 안 찍힘. 동작은 정상동작

```java
SLF4J: Failed to load class "org.slf4j.impl.StaticLoggerBinder". 
SLF4J: Defaulting to no-operation (NOP) logger implementation 
SLF4J: See http://www.slf4j.org/codes.html#StaticLoggerBinder for further details.
```


### 해결 방법
* `$JEUS_HOME/lib/system/ehcache-scf-replication-jar-with-dependencies.jar` 백업 후 삭제
* `$JEUS_HOME/lib/system/hazelcast-all-4.2.1.jar` 백업 후 삭제

### 출처
* Tmax 공식 질문답변하는 곳에서 발견 .. 8.5에 있는 이슈라고 함
  * [해당 Q&A](https://technet.tmaxsoft.com/ko/front/support/qna/viewQna.do?cmProductCode=&find_key=all&find_value=Failed+to+load+class&paging.page=1&board_seq=CUST-20220114-000005)
