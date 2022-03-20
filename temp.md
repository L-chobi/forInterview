## DTO를 따로 두는 이유?
-responseDTO?
-API aggregation?

## 대용량 트래픽 처리에 대한 이해 
ex) "3000번째로 클릭한 사람에게 포르쉐를 주는 이벤트를 하는데 순간 동시접속자 수는 대략 백만명이 넘어갈 것으로 예상된다. 이 동시접속하는 백만명의 요청 중에서 어떻게 3000번째를 구분할 것인가? "

## NoSQL에서 스키마를 추가, 제거 하는 등의 변경이 일어날 경우 기존 데이터에 어떻게 적용할 것인지

## MSA(Microservices Architecture)
-msa를 위한 서비스 re architecting

## MVP(Minimum Viable Product)

## SDLC(소프트웨어 생명주기)

## gRPC Gateway

## gateway layer?
-rails를 없애고 gateway layer를 추가하는 이유?

## API Gateway

## GCDN
-GSLB?

## WAS?

## Logging Platform

## 배포없이 특정 기능에 대한 폴백(fallback)

## ruby on rails로 개발된 모놀리틱 구조

## ruby on rails 모놀리틱 구조 뒤에 kotlin, spring을 사용한 msa구조

## 모놀리식 구조 문제점
1) 부분 장애가 전체 서비스로 전파된다.
2) 부분적인 서비스의 scale-out이 어렵다.
3) 서비스의 개선이 어렵고, 수정 시 장애의 영향도 파악이 어렵다. 
4) 서비스의 전체 코드가 하나의 프로젝트로 구성되어 배포가 오래걸린다.
5) 하나의 framework와 개발언어에 종속되어 서비스에 적절한 기술을 사용하기 어렵다. 

## MSA로 변환시 얻을 수 있는 장점
1) 하나의 서비스 장애가 다른 서비스로 전파되지 않는다.
2) 코드 복잡성 및 의존성을 제거하여 영향도 파악을 용이하게 한다.
3) 오늘의집 서비스의 고 가용성과 확장성을 확보한다.

## 개발 서버와 프로덕션 서버

## 개발 패턴
-FACADE 패턴

## 클라우드 오토 스케일링?

## Scale up, Scale out
