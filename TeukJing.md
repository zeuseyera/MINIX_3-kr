:kr: 미닉스 3을 알아보자

출처: http://www.minix3.org

| [앞마당](./README.md) | [시작하기](./SiJakHaGi/SiJakHaGi.md) | [내려받기](http://www.minix3.org/download) | [모임](http://www.minix3.org/community) | [새소식](http://www.minix3.org/news) | [위키](http://wiki.minix3.org) |  
| ---   | ---     | ---     | --- | ---    | ---  |  

여기에 미닉스 3의 더 흥미로운 특징이 일부 있다.

### 1. 일반 특징

```
이식가능운영체제접속기: POSIX(Portable Operating System Interface)
```

 - NetBSD 쟁이를 써서 이식가능운영체제접속기(POSIX) 호환 운영체제
 - 원본공개, BSD 권한을 가짐
 - x86 컴퓨터와 x86 가상기계에서 아주 잘 동작한다(브이엠웨어, 등등.)
 - ARM 코텍스(Cortex) A8에서 동작한다(예, 비글보드 XM, 비글본)
 - TCP/IP를 이용한 네트워크
 - 가상메모리
 - 가상파일몸통
 - 가상메모리와 파일몸통으로 공유된 통합블록캐시
 - 동적 연결
 - 작은 메모리공간(커널: 600KB, 운영체제 전체: 25MB)

### 2. 미닉스-고유 특징

 - 커널모드에서 실행되는 꼬맹이 마이크로커널
 - 운영체제의 대부분은 사용자모드로 보호된 프로세스에서 실행된다
 - 모든 장치 구동기는 사용자모드 프로세스로 분리된다
 - 환생서버가 실패한 구동기를 다시 탑재할수 있다

### 3. 신뢰성 특징

 - 줄어든 커널크기
 - 버그는 갇혀있다
 - 구동기의 메모리 접근은 제한적이다
 - 나쁜 포인터 참조가 항상 치명적인 것은 아니다
 - 무한루프가 항상 치명적인 것은 아니다
 - 버퍼 넘침이 항상 치명적인 것은 아니다
 - 커널함수 호출에 대한 접근은 방해한다
 - I/O 포트에 대한 접근은 방해한다
 - 운영체제 성분과의 통신은 방해한다
 - 죽거나 아픈 구동기는 환생될 수 있다
 - 가로채기와 소식은 통합된다
 - 더 상세한 것은 [여기](http://wiki.minix3.org/doku.php?id=www:documentation:reliability)를 눌러라

### 4. 언어 및 컴파일러

 - 언어: C, C++, clisp, mawk, Perl, Python, tcl, 등등.
 - 컴파일러: gcc 및 clang/LLVM
 - x86에서 토종번역(주인장 자신)
 - x86 및 ARM 을 위한 교차번역

### 5. 패키지

 - 쉘: 예; bash, mksh, mudsh, pdksh, zsh
 - 편집기: 예; elvis, joe, jove, pico, uemacs, vim
 - 게임: 예; crafty, exchess, ioquake
 - 전자우편: 예; fetchmail, getmail, mutt, thunderbird
 - 4000가지 이상의 NetBSD 패키지
