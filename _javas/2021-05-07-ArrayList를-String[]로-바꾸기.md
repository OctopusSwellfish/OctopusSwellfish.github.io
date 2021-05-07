---
layout: post
title: ArrayList를 String[]로 바꾸기
tags:
- java
---

```java
List<String> stringList = new ArrayList<String>();
stringList.add("무야호");
stringList.add("돈까스");
stringList.add("구렁텅이");
        
String[] stringArray = stringList.toArray(new String[0]);
```
* `new String[0]` 이 무슨의미일까?
1. List를 toArray 메서드에 파라미터로 넘어가는 배열 객체의 size만큼의 배열로 전환
2. 만약에 List size가 인자로 넘어가는 배열 객체의 size보다 크면 해당 List의 size로 배열이 만들어짐
3. List size가 인자로 넘어가는 배열객체의 size보다 작을때면 인자로 넘어가는 배열객체의 size로 배열이 만들어짐
