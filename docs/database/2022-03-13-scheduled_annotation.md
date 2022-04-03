---
layout:post
title: Blogging Like a Hacker
---

## springframework scheduled annotation
---

spring batch를 처리해주는 애노테이션

- cron : UNIX 시스템의 CRON과 문법이 유사함. seecond, minute, hor, day of month, month, and day of week
  String 형식으로 입력해야함.
  
- fixedDelay : 해당 애노테이션이 붙은 메소드는 fixedDelay에서 설정한 시간을 간격으로 실행됨. 단위는 밀리세컨드
- 실행중인 메소드가 끝나고나서 fixedDelay만큼의 시간이 지연됨
- 
- fixedRate : 실행중인 스케줄러와는 상관없이 fixedRate만큼 시간이 지나면 다음 스케줄러를 실행. 잘못하면 같은 작업을 두번이상 수행할 수도 있음.

- initailDelay 
scheduled 애노테이션은 cron() / fixedDelay() / fixedRate() 세가지 속성중 한가지 속성은 반드시 정의해줘야 동작한다.

해당 애노테이션이 붙은 메소드는 arguments를 가지면 안되고 void를 return해야한다. 리턴값이 있다고 하더라도 스케줄러를통해 호출될 때 무시된다.

---

fixedDelay는 현재 Schedule 상에 걸린 작업을 모두 끝난 이후에 설정된 시간이 카운팅되는 형태이며

fixedRate는 현재 Schedule 상에 걸린 작업의 완료 여부와 상관 없이 Scheduler가 시작한 시간으로부터 카운팅되는 형태이다.



---

## example

fixedDelay와 fixedRate는 long이아닌 String으로도 값을 받을 수 있으므로 application.yml/application.properties에서 가져와서 사용할 수도있다.



