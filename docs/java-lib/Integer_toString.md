---
layout: default
title: Integer.toString 메소드
parent: 자바 라이브러리 정리
nav_order: 1
has_toc: true
---

알고리즘 문제를 풀다가 진법 변환이 필요해서 직접 코드를 작성했었는데 
자바에서 진법변환을 해주는 메소드가 이미 있었다. 

``` java 
  public static String toString(int i, int radix);
  // i : 는 문자열로 변환할 정수
  // radix : 문자열 표현에 사용할 기수
  
  String binary = Integer.toString(100, 2); // 10진수 100을 2진수로 변환하고 문자열로 반환
```