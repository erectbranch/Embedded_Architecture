<div width="100%" height="100%" align="center">
  
<h1 align="center">
  <p align="center">임베디드 시스템 아키텍처</p>
  <a href="http://acornpub.co.kr/book/embedded-systems-architecture">
    <img width="50%" src="cover.jpg" />
  </a>
</h1>
  

<b>다니엘 라카메라 저 · 김세영, 정윤선 역</b></br>
에이콘 · 2019년 3월 29일 출시</br>
[[github](https://github.com/AcornPublishing/embedded-systems-architecture)]</b> 

</div>

## :bulb: 목표

- **임베디드 시스템의 특성을 알고 개발 패턴을 익힌다.**

  > 임베디드 시스템의 특성을 이해하고 개발 환경을 구축한다.


</br>

## 🚩 정리한 문서 목록

### 📔 임베디드 기초

 - [임베디드 시스템 개요](https://github.com/erectbranch/Embedded_Architecture/tree/master/ch01)

   > real-time system(soft/hard), bare-metal, firmware, microcontroller 구조, embedded system의 제약, RAM, flash memory, XIP

 - [C 컴파일러와 링커](https://github.com/erectbranch/Embedded_Architecture/tree/master/ch02/summary01)

   > toolchain, bit pattern, assembly, cross-compilation

   > C compiler: GCC, preprocessor, compiler, assembler

   > Linker: symbol(.text/.rodata/.data/.bss), linker script, symbol resolution, relocation, ROF/EOF, object file format

 - [서브시스템과 인터럽트](https://github.com/erectbranch/Embedded_Architecture/tree/master/ch04)

   > CPSR(User/FIQ/IRQ/SVC/Abort/Undefined/System), processor mode(thread/handler), privilige levels(priviliged/unpriviliged)

   > core register: general purpose register, stack pointer, link register, program counter) PSR, EMR, CONTROL

   > polling, interrupt, IVT(Interrupt Vector Table), ISR(Interrupt Service Routine)

<br/>

### 1장. 임베디드 시스템: 실용주의적 접근

    __도메인 정의
    ____임베디드 리눅스 시스템
    ____저사양 8비트 마이크로컨트롤러
    ____하드웨어 아키텍처
    ____도전 과제 이해하기
    ____멀티스레딩
    __RAM
    __플래시 메모리
    __인터페이스와 주변장치
    ____비동기식 UART 기반 직렬 통신
    ____SPI
    ____I2C
    ____USB
    __연결 시스템
    __레퍼런스 플랫폼
    ____ARM 레퍼런스 설계
    ____Cortex-M 마이크로프로세서
    __요약

### 2장. 작업 환경과 워크플로 최적화

    __워크플로 개요
    ____C 컴파일러
    ____링커
    ____빌드 자동화
    ____디버거
    ____임베디드 워크플로
    __GCC 툴체인
    ____크로스 컴파일러
    ____컴파일러 컴파일
    ____실행 파일 링크
    ____바이너리 포맷 변환
    __타깃과의 상호작용
    ____GDB 세션
    __검증
    ____기능 테스트
    ____하드웨어 도구
    ____오프 타깃 테스트
    ____에뮬레이터
    __요약

### 3장. 아키텍처 패턴

    __환경설정 관리
    ____리비전 제어
    ____추적 활동
    ____코드 리뷰
    ____지속 통합
    __소스 코드 구성
    ____하드웨어 추상화
    ____미들웨어
    ____애플리케이션 코드
    __임베디드 프로젝트의 생애 주기
    ____프로젝트 단계 정의
    ____프로토타입 제작
    ____리팩토링
    ____API와 문서
    __요약

### 4장. 부트업 과정

    __인터럽트 벡터 테이블
    ____시작 코드
    ____리셋 핸들러
    ____스택 할당
    ____장애 핸들러
    __메모리 레이아웃
    __부트 코드 빌드 및 실행
    ____makefile
    ____애플리케이션 실행
    __다중 부트 단계
    ____부트로더
    ____이미지 빌드
    ____다중 단계 시스템 디버깅
    ____공유 라이브러리
    __요약

### 5장. 메모리 관리

    __메모리 매핑
    ____메모리 모델과 주소 공간
    ____코드 구역
    ____RAM 구역
    ____주변장치 접근 구역
    ____시스템 구역
    ____메모리 트랜잭션 순서
    __실행 스택
    ____스택 배치
    ____스택 오버플로
    ____스택 페인팅
    __힙 관리
    ____사용자 정의 구현
    ____newlib 사용
    ____힙 제한
    ____다중 메모리 풀
    ____일반적인 힙 사용 오류
    __메모리 보호 유닛
    ____MPU 환경설정 레지스터
    ____MPU 프로그래밍
    __요약

### 6장. 일반 목적 주변기기

    __인터럽트 컨트롤러
    ____주변장치 인터럽트 환경설정
    __시스템 시간
    ____플래시 대기 상태 적용
    ____클록 환경설정
    ____클록 배분
    ____SysTick 활성화
    __일반 타이머
    __범용 I/O
    ____핀 환경설정
    ____디지털 출력
    ____PWM
    ____디지털 입력
    ____인터럽트 기반 입력
    ____아날로그 입력
    __워치도그
    __요약

### 7장. 로컬 버스 인터페이스

    __직렬 통신 소개
    ____클록과 심볼 동기화
    ____버스 와이어링
    ____주변장치 프로그래밍
    __UART 기반 비동기 직렬 버스
    ____프로토콜 상세
    ____컨트롤러 프로그래밍
    ____Hello World!
    ____newlib printf
    ____데이터 수신
    ____인터럽트 기반 입출력
    __SPI 버스
    ____프로토콜 상세
    ____트랜시버 프로그래밍
    ____SPI 트랜잭션
    ____인터럽트 기반 SPI 전송
    __I2C 버스
    ____프로토콜 상세
    ____클록 늘리기
    ____다중 마스터
    ____컨트롤러 프로그래밍
    ____인터럽트 처리
    __요약

### 8장. 저전력 최적화

    __시스템 환경설정
    ____하드웨어 설계
    클록 관리
    ________전압 제어
    ____저전력 운영 모드
    ____딥슬립 환경설정
    ____정지 모드
    ____대기 모드
    ____웨이크업 간격
    __전력 측정
    ____개발 보드
    __저전력 임베디드 애플리케이션 설계
    ____비지 루프를 슬립 모드로 대체
    ____긴 비활성 기간 동안의 딥슬립
    ____클록 속도 선택
    ____전력 상태 전환
    __요약

### 9장. 분산 시스템과 IoT 아키텍처

    __네트워크 인터페이스
    ____매체 접근 제어
    ____이더넷
    ____와이파이
    ____저속 무선 개인 영역 네트워크(LR-WPAN)
    ____LR-WPAN 산업 링크 계층 확장
    ____6LoWPAN
    ____블루투스
    ____모바일 네트워크
    ____저전력 원거리 네트워크(LPWAN)
    ____적절한 네트워크 인터페이스 선택
    __인터넷 프로토콜
    ____TCP/IP 구현
    ____네트워크 장치 드라이버
    ____TCP/IP 스택 구동
    ____소켓 통신
    ____메시 네트워크와 동적 라우팅
    __전송 계층 보안
    ____보안 소켓 통신
    __애플리케이션 프로토콜
    ____메시지 프로토콜
    ____REST 구조 패턴
    ____분산 시스템(단일 실패 지점)
    __요약

### 10장. 병렬 태스크와 스케줄링

    __태스크 관리
    ____태스크 블록
    ____컨텍스트 스위칭
    ____태스크 생성
    __스케줄러 구현
    ____슈퍼바이저 호출
    ____협업 스케줄러
    ____동시성과 타임 슬라이스
    ____블록되는 태스크
    ____자원 대기
    ____실시간 스케줄링
    __동기화
    ____세마포어
    ____뮤텍스
    ____우선순위 도치
    __시스템 자원 분리
    ____권한 수준
    ____메모리 세그먼테이션
    ____시스템 호출
    __요약

### 11장. 임베디드 운영체제

    __실시간 애플리케이션 플랫폼
    ____FreeRTOS
    ____ChibiOS
    __저전력 IoT 시스템
    ____Contiki OS
    ____Riot OS
    __POSIX 호환 시스템
    ____NuttX
    ____Frosted
    __안전한 임베디드 시스템의 미래
    ____프로세스 분리(Tock)
    __요약