
:kr: 미닉스 3을 알아보자

출처: http://www.minix3.org

| [앞마당](../../README.md) | [시작하기](../../SiJakHaGi/SiJakHaGi.md) | [내려받기](http://www.minix3.org/download) | [모임](http://www.minix3.org/community) | [새소식](http://www.minix3.org/news) | [위키](http://wiki.minix3.org) |
| ---   | ---     | ---     | --- | ---    | ---  |

# 가상기계에 미닉스 3

 미닉스 3은 텅빈 x86 타드웨어에서 실행되지만 또한 대부분의 가상기계에서도 실행된다. 몇개의 인기있는 가상기계에서 미닉스 3을 실행하는 방법에 대한 정보는 아래에서 얻을수 있다.

 목록
  - [브이엠웨어(VMware)](#브이엠웨어)
  - [가상컴퓨터(Virtual PC)](#가상컴퓨터)
  - [가상상자(Virtual Box)](#가상상자)
  - [퀘뮤 와 케이브이엠(QEMU and KVM)](#퀘뮤)
  - [보취(Bochs)](#보취)

<a name="브이엠웨어"></a>
## 1. 브이엠웨어(VMware)

### 1-1) 브이엠웨에서 실행

 이 페이지는 브이엠웨어에 미닉스 3을 설치하는 절차를 설명한다.

### 1-2) 채비

 [:earth_asia:브이엠웨어](http://www.vmware.com/)를 설치하라. 브이엠웨어 바이너리는 해당 웹페이지에서 내려받기를 할수 있다.

### 1-3) 가상기계 설치
 미닉스 3을 설치하기 전에, 새로운 가상기계 구성을 생성할 필요가 있을것이다. 가상기계 구성에 당신의 가상기계 참여(parameter)를 지정한다 예를들어, 가상기계에 사용하기 원하는 메모리 크기, 가상하드디스크의 원하는 크기, 등등.

#### 1-3-1) 가상기계 생성 - 브이엠웨어 서버
 브이엠웨어의 주 목록에서, **새 가상기계** 를 선택한다.

  1. 환영 화면에서 **다음(Next)** 을 누른다.
  2. *가상기계 구성* 목록에서, **일반(Typical)** 을 선택한다.
  3. *게스트 운영체제* 에서, **다른것(Other)** 그리고 판도 **다른것(Other)** 을 선택한다.
  4. *가상기계 이름* 의 경우, **미닉스3** 을 쓴다(어느것이든 작동할 것이다).
  5. *네트워크 유형* 화면에서, **브리지네트워크 사용(Use bridged networking)** 을 선택한다.
  6. *디스크 용량* 의 경우, `2GB` 정도를 입력한다, 하지만 더 작은 값도 작동한다. 이것은 미닉스가 설치될 가상 몫(파티션)의 크기이다. **지금 모든 디스크공간 할당(Allocate all disk space now)** 을 찍는다.
  7. **마침(Finish)** 을 누르면 디스크이미지 그리고 우리가 실행할 가상기계가 생성된다.

#### 1-3-2) 가상기계 생성 - 브이엠웨어 워크스테이션 과 브이엠웨어 플레이어(판 > 3)
 브이엠웨어의 주 목록에서, `새 가상기계`를 선택한다.

  1. *마법사* 에서, **일반(Typical)** 을 선택한다; 그런다음, **다음(Next)** 을 누른다.
  2. *게스트 운영체제 설치* 의 경우, **나중에 운영체제 설치(I will install the operating system later)** 를 선택한다; 그런다음, **다음(Next)** 을 누른다.
  3. *게스트 운영체제 선택* 에서, **다른것(Other)** 그리고 판도 **다른것(Other)** 을 선택한다.
  4. *가상기계 이름* 의 경우, **미닉스3** 또는 다른 의미있는 이름을 입력한다.
  5. *디스크 용량* 의 경우, `2GB` 정도를 입력한다, 이는 모든 패키지와 소스에 충분하다. 소스파일을 더 추가해야하는 경우 더 크게 만들수 있다.
  6. *가상기계 생성 준비* 에서, **생성후 가상기계 켜기(Power on this virtual machine after creation)** 가 선택되지 않았는지 확인한다; 그런다음, **마침(Finish)** 을 누른다.

 필요에 따라 메모리 설정을 편집할 필요가 있다. 장치부문에서, 메모리를 선택하고, 필요에 따라 메모리를 조정한다. 또한, 미닉스에서 X 윈도우 시스템을 실행하기 위해서는, 적어도 384MB가 필요하다.

#### 1-3-3) 가상기계 생성 - 브이엠웨어 플레이어(판 < 3)

 무료 브이엠웨어 플레이어(VMware Player)를 사용하는 경우, 새 사상기계를 생성할 수 없다. 이를 해결하는 가장 간단한 방법은 이지브이엠엑스(EasyVMX)를 사용하여 새 가상기계(텅빈)를 만드는 것이다.(알림: 이지브이엠엑스(EasyVMX)는 2012년 12월 현재 죽은 죽은 과제로 보인다)

  1. http://www.easyvmx.com 에서 **Super Simple** 가상기계 생성기를 선택한다.
  2. 원하는 기계이름을 정한다.
  3. 운영체제: **Other OS** (알림: 64-bit가 아닌것을 선택한다)
  4. 적절한 메모리와 저장소 크기를 선택한다(예, 512MB 메모리와 2GB 저장소).
  5. 라이브씨디 아이에스오(LiveCD ISO)에 대해서는 걱정을 말아라, 공란으로 두고 지나가라(나중에 다루게 될 것이다).
  6. **가상기계 생성(Create Virtual Machine)** 을 누른다.
  7. 압축된 파일을 내려받는다, 그리고 압축을 푼다. 여기에는 많은 브이엠웨어(VMware) 파일과 디렉토리가 있어야한다.
  8. 브이엠웨어 플레이어(VMware Player)를 시작한다, **기존 가상기계 열기(Open an existing virtual machine)** 를 선택한다, 그리고 방금 압축해제한 `.vmx` 파일을 선택한다.
  9. 일단 가상기계가 시작되면, 장치메뉴로 이동한다; 그리고, CD/DVD 항목에서, **디스크이미지 파일에 연결(Connect to Disk Image File (iso))** 을 선택한다. 미닉스 3ㅏ 웹싸이트에서 내려받은 미닉스3 ISO 파일을 선택한다.
  10. 만약 필요하다면, Ctrl+R로 기계를 재설정한다; 그리고, 이것은 ISO로 부팅할 것이다.

#### 1-3-4) 설치

 [내려받기 페이지](http://www.minix3.org/download)에서 미닉스 3 ISO 이미지를 내려받고 압축해제를 했다고 가정하면, ISO 파일을 끼울수 있다.

  1. 왼쪽의 *상세목록* 에서 **미닉스3(Minix3)** 을 선택한다.
  2. *장치* 부분에서, **CD-ROM** 을 두번누르기를 한다.
  3. **ISO 이미지 사용(Use ISO Image)** 을 선택한다.
  4. 둘러본다, 그리고 방금 내려받은 미닉스(Minix) 이미지인 `.iso` 를 선택한다.

 그런다음 [일반설치 안내](http://wiki.minix3.org/doku.php?id=usersguide:doinginstallation#runningsetup)를 따를수 있다.

 설치가 끝나면, 다음을 입력한다
```
shutdown
```

 d0p0s0> 프롬프트가 나타나면, 가상기계 종료를 위해 **끄기(off)** 를 한다.

### 1-4) 미닉스 3 부팅

 이제, 가상기계에 미닉스 3을 설치했다. 우선 정리해야 할 것은, 다음에 부팅할 때, 운영체제에로 부팅하는 것이다, 그리고 CD 이미지가 아닌.

  1. *장치* 부분에서, CD-ROM을 두번누르기를 한다.  
  2. **물리디스크 사용(Use Physical Drive)** 을 선택한다.  

 훌륭하다, 이제 새로 설치된 운영체제로 부팅할 수 있다.  

  1. 왼쪽의 *상세목록* 에서 **미닉스3(Minix3)** 을 선택한다.  
  2. *명령* 목록에서, 이 **가상기계 시작(Start this Virtual Machine)** 을 누른다.

### 1-5) 설치후 설정

 일부 설정조언에 관해서는 [설치후](http://wiki.minix3.org/doku.php?id=usersguide:postinstallation)를 읽어야 한다.

#### 1-5-1) X.org

 다른 시각도구 처럼, 미닉스는 브이엠웨어(VMware)에서 올바른 화면 해상도를 얻을 수 없다. 원하는 해상도로 X11을 실행하려면, 아래의 명령을 사용하여 `xorg.conf` 파일 생성으로 시작한다

```
Xorg -configure
```

 이것은 홈디렉토리에 `xorg.conf.new` 파일을 생성한다. 이것은 오로지 수동으로 할 필요가 있다, 그러고 수정한다 그리고 모니터 부분을 수정한다 그러고 읽어본다:

```
Section "Monitor"
	Identifier   "Monitor0"
	VendorName   "vmware"
	ModelName    "VMWare Inc"
	HorizSync    1.0 - 10000.0
	VertRefresh  1.0 - 10000.0
	ModeLine     "800x600"  100.0    800 900 1000 1100     600 700 800 900
	ModeLine     "1024x768" 100.0    1024 1100 1200 1300   768 800 900 1000
	ModeLine     "1366x768" 100.0    1360 1400 1500 1600   768 800 900 1000
EndSection
```

 실제화면 해상도를 위해 다른 `모드라인(ModeLine)`을 추가가 필요할수 있다(만약 전체화면 모드로 실행하려면). 이것은 브이엠웨어(VMware)에서 난해한기술(rocket science)이 아니다, 때문에 참여(parameter)의 대부분은 실제로 별로 중요하지 않다. `모드라인(ModeLine)`중에 `"1024×768"`에 있어, 정말로 중요한 것은 `1024`와  `768`이다. `100.0`은 헤르츠(Hz)이고 새로고침 빈도이다, 브이엠웨어(VMware)에서 거의 무시한다(이것은 주인장이 제어한다). 다른 모든 박자(타이밍)값은 `100.`으로 반올림된다 따라서 당신의 HDTV 표시를 위하여 `모드라인(ModeLine)`은 다음을 읽을 것이다.

```
ModeLine "1920x1080" 100.0    1920 2000 2100 2200    1080 1100 1200 1300
```

 명심하라 현재판의 엑스서버(X-server)는, 가로해상도(Xresolution)는 8의 배수인 화소(픽셀)이어야 한다. 여기에서 `“1366×768”`에 대한 `모드라인(ModeLine)`이 `1360`을 표시폭으로 사용하는 이유이다. 실제화면에 물리적으로 존재하는 6개의 열이 버려진다(내 노트북의).

 다음으로 파일의 화면부분을 수정해야 한다. 수정한다 그러면 다음과 같이 표시된다:

```
Section "Screen"
	Identifier	"Screen0"
	Device		"Card0"
	Monitor		"Monitor0"
	SubSection "Display"
		Viewport   0 0
		Depth     24
		Modes	"1366x768"
	EndSubSection
EndSection
```

 여기에서 `모드(Modes)`에는 실제로 원하는 해상도의 `모드라인(ModeLine)` 딱지를 포함한다.

 파일을 저장한다 그리고 `/usr/pkg/X11R6/lib/X11/xorg.conf`에 복사한다.

### 1-6) 해결방법

#### 1-6-1) 랜스(Lance) 해결방법

 미닉스 3.1.5 에서, 일정기간 올바르게 작동한 후, 랜스구동기(Lance driver)가 조용히 작동이 중지될 수 있다. 원인은 일정기간 동안의 모든 네트워크 이력이 버려지는 것이다. 해결방법: 이런경우, 랜스구동기(Lance driver)를 재시작하기 위하여 루트권한에서 `service refresh lance`를 실행한다. 이러한 쟁점은 서브버전(Subversion)에서 제공되는 미닉스 트렁크(trunk)에서 수정되었다.

 미닉스 3.1.3 에서, 랜스구동기(Lance driver) 설정이 망가졌고, 브이엠웨어(VMware)에서 미닉스3에 대하여 **네트워크 지원안함(no network support)** 이 초래되었다면.

 당신은 구동기(Lance driver)가 작동하도록 [이 명령어 조합(set of instructions)](http://wiki.minix3.org/doku.php?id=lancefix)을 사용할 수 있다.

#### 1-6-2) 브이엠웨어(VMware) 하드웨어 판 6.x 해결방법

 미닉스 3.1.4 이하의 판에 대해서, 브이엠웨어(VMware)의 새로운 판에서 실행할 때 다음 오류가 발생할 수 있다: `*** vcpu-0:ASSERT vmcore/private/iospace_shared.h:558 bugNr=64440.`

 당신의 가상기계에 해당하는 `.vmx`파일을 수정할 필요가 있다. 이것은 `~/Documents/Virtual Machines/<VM name>` 또는 `~/vmware/<VM name>`에서 찾을 수 있다.

 다음 행을 삭제해야 한다:

```
pciBridge0.present = "TRUE"
```

 그리고 pciBridge, pciBridge2, 등의 모든 비스한 행을. `.vmx` 파일에서.

#### 1-6-3) 하드디스크 몫(partition)을 할 수 없음

 브이엠웨어(VMware) 서버는, 기본적으로, 스카시(SCSI) 하드디스크를 설치한다.

 미닉스 3.1.3a 에서, 기본설정으로, 디스크파티션 단계은 자동으로 실행되지 않는다. **전문가모드(expert mode)** 에서, 내 디스크에 파티션을 할 수 었없다.

 나는 스카시(SCSI) 하드디스크를 제거했다 그리고 대신에 아이디이(IDE) 디스크를 설치했다.

<a name="가상컴퓨터"></a>
## 2. 가상 컴퓨터(Virtual PC)


<a name="가상상자"></a>
## 3. 가상상자(VirtualBox)

### 3-1) 가상상자(VirtualBox)에서 실행

 이 페이지는 가상상자(VirtualBox)에 미닉스 3을 설치하는 과정을 설명한다.

 작동 확인된 것들

| VirtualBox | Minix | Host-OS | Notes |  
| --- | --- | --- | --- |  
| 4.3.36  | 3.3.0-3234ff     | Debian 3.16.36      | - |  
| 4.3.36  | 3.4.0rc2-373b793 | Debian 3.16.36      | - |  
| 5.2.4   | 3.4.0rc6         | Debian 10 (buster)  | - |  

### 3-2) 채비

 가장먼저 [:earth_asia:가상상자(VirtualBox)](https://www.virtualbox.org)를 설치해야 한다. 가상상자(VirtualBox) 바이너리는 해당 웹페이지에서 내려받을 수 있다. 만약 리눅스 배포를 실행한다면, 당신은 아마도 패키지관리자를 통해 가상상자(VirtualBox)를 설치할 수 있다(예, apt-get으로 유사 데비안 장치에 가상상자(VirtualBox)를 설치한다).

### 3-3) 가상기계 설치

 미닉스 3을 설치하기 전에, 새로운 가상기계 구성을 생성할 필요가 있을것이다. 가상기계 구성에 당신의 가상기계 참여(parameter)를 지정한다 예를들어, 가상기계에 사용하기 원하는 메모리 크기, 가상하드디스크의 원하는 크기, 등등. [필요한 하드웨어]()에 대한 안내를 보라.

 가상상자(VirtualBox)의 주화면에서, **새것(New)** 이라는 큰 버튼을 눌러라.

 1. *이름 과 운영체제(Name and operating system)* 화면에서, *이름* 은 `미닉스3`을 쓴다(모두 작동할 것이다).
 2. *유형(Type)* 은 **다른것(Other)** 를 선택한다.
 3. *판(Version)* 은 **다른것/모름(Other/unknown)** 을 선택한다.
 4. *메모리크기(Memory size)* 화면에서, 이 가상기계에 대한 메모리의 양을 선택한다(예, 1024MB).
 5. *하드드라이브(Hard Drive)* 화면에서, 가상 하드디스크의 크기와 속성을 설정한다. 이것은 해당옵션을 그대로 두고 떠나거나 변경한다.
 6. **생성(Create)** 을 누르면 디스크이미지와 우리가 실행할 가상기계가 생성된다.
 7. 이제 왼쪽의 목록에서 **미닉스3(MINIX3)** 을 선택한다.
 8. **OK** 를 누른다, 그리고 이제 미닉스3(MINIX3)을 설치할 준비가 되었다.

 문제해결:  
  만약 싸타(SATA) 제어기에 붙은 가상하드디스크의 감지실패를 했다면, 기계를 재설정하고 아이디이(IDE) 제어기에 디스크를 붙인다. 또한, 씨디롬(CDROM)이 아이디이(IDE) 제어기에 잘 붙어있는지 확인해야 한다.(가상상자(VirtualBox) 5.1.22)

### 3-4) 설치

 [내려받기 페이지](http://www.minix3.org/download)에서 미닉스 3 ISO 이미지를 내려받고 압축해제를 했다고 가정하면, ISO 파일을 끼울수 있다.

  1. 왼쪽의 *목록* 에서 **미닉스3(Minix3)** 을 선택한다.
  2. **시작(Start)** 을 누른다.
  3. *시동디스크 선택(select a start-up disk)* 이 표시된다.
  4. 둘러본다, 그리고 방금 내려받은 미닉스(Minix) 이미지인 `.iso`를 선택한다 그리고 **열기(Open)** 을 누른다.

 그런다음 [일반설치 안내](http://wiki.minix3.org/doku.php?id=usersguide:doinginstallation#runningsetup)를 따를수 있다.

 설치가 끝나면, 다음을 입력한다
```
poweroff
```
 로 미닉스를 나온다. 가상기계는 자동으로 닫힌다.

### 3-5) 미닉스 3 부팅

 이제, 가상기계에 미닉스 3을 설치했다. 우선 정리해야 할 것은, 다음에 부팅할 때, 운영체제에로 부팅하는 것이다, 그리고 CD 이미지가 아닌.

  1. **가상기계(VM)** 이 선택되었는지 확인한다, 그런다음 주화면에서 **설정(Setting)** 버튼을 누른다.
  2. 오른쪽 메뉴에서, **저장장치(Storage)** 를 누른다.
  3. 저장장치 가지에서, 설치 `.iso`파일을 선택한다 그리고 아래의 작은 **제거(Remove)** 버튼을 누른다.

 훌륭하다, 이제 새로 설치된 운영체제로 부팅할 수 있다.  

  1. 주화면에서 큰 **시작(Start)** 버튼을 누른다.  

### 3-6) 설치후 설정

 일부 설정조언에 관해서는 [설치후](http://wiki.minix3.org/doku.php?id=usersguide:postinstallation)를 읽어야 한다.

#### 3-6-1) X.org

 `수정해줘!`: 이 장은 다시 써야할 필요가 있다, 미닉스(MINIX) 3.3.0 은 기본적으로 엑스오알지(Xorg)를 설치하지 않으며, 미닉스(MINIX) 3.4.0 베타의 경우는 추가적인 조작없이 엑스(X)를 시작할 수 있다.

 미닉스(MINIX) 3은 가상상자의 손님추가를 할수 없다. 따라서, 미닉스(MINIX)는 화면해상도를 올바르게 추측할 수 없다. 원하는 화면해상도는 `xorg.conf`파일에서 수동으로 설정해야 한다.

##### 3-6-1-1) 화면해상도 변경

 엑스(X)가 실행중이 아닌지 확인해야 한다!

 루트(root) 권한으로 로그인 한다, 그리고 다음 명령을 실행한다:
```
# Xorg -configure
```

 이 명령은 `/root`에서 `xorg.conf.new`파일을 생성해야 한다.

 `xorg.conf.new`파일의 `Section “Screen”`에서, `SubSection “Display”`을 모두 제거해야 한다, 포함하고있는 하나를 제외하고: `Depth: 16`

 원하는 화면해상도를 추가한다. 가능한 화면해상도는 `/var/log/Xorg.0.log`에서 찾을 수 있다. `Mode:`를 검색한다. `BitsPerPixel: 16`를 포함하는, 이것은 중요하다!.

 본보기:
```
*Mode: 117 (1024x768)
[...]
	XResolution: 1024
	YResolution: 768
[...]
	BitsPerPixel: 16
[...]
```

 이러한 해상도는 새로 생성된 `xorg.conf.new`에 추가할 수 있다(위의 본보기에서는: 1024×768). 나는 다음 해상도를 사용할 수 있다: `320×200`, `640×480`, `800×600`, `1024×768`, `1280×1024`, `1152×864`.

 `SubSection "Display”`에서 `Modes`요소에 원하는 해상도를 추가한다.

 본보기:
```
[...]
	Section "Screen"
[...]
		SubSection "Display"
			Viewport   0 0
			Depth     16
			Modes "1024x768"
		EndSubSection
	EndSection
[...]
```

 이제 `xorg.conf.new`파일을 `/usr/pkg/X11R6/lib/X11/xorg.conf`로 이동할 수 있다.
```
# mv xorg.conf.new /usr/pkg/X11R6/lib/X11/xorg.conf
```

 **X.org** 를 시작하여 새로운 구성을 평가하라:
```
# startx
```

##### 3-6-1-2) xorg.conf 본보기

`xorg.conf` 본보기, 위치: `/usr/pkg/X11R6/lib/X11/xorg.conf`

```
Section "ServerLayout"
	Identifier     "X.org Configured"
	Screen      0  "Screen0" 0 0
	InputDevice    "Mouse0" "CorePointer"
	InputDevice    "Keyboard0" "CoreKeyboard"
EndSection

Section "Files"
	RgbPath      "/usr/pkg/X11R6/lib/X11/rgb"
	FontPath     "/usr/pkg/X11R6/lib/X11/fonts/misc/"
	FontPath     "/usr/pkg/X11R6/lib/X11/fonts/TTF/"
	FontPath     "/usr/pkg/X11R6/lib/X11/fonts/Type1/"
	FontPath     "/usr/pkg/X11R6/lib/X11/fonts/CID/"
	FontPath     "/usr/pkg/X11R6/lib/X11/fonts/75dpi/"
	FontPath     "/usr/pkg/X11R6/lib/X11/fonts/100dpi/"
EndSection

Section "Module"
EndSection

Section "InputDevice"
	Identifier  "Keyboard0"
	Driver      "kbd"
EndSection

Section "InputDevice"
	Identifier  "Mouse0"
	Driver      "mouse"
	Option	    "Protocol" "auto"
	Option	    "Device" "/dev/mouse"
EndSection

Section "Monitor"
	Identifier   "Monitor0"
	VendorName   "Monitor Vendor"
	ModelName    "Monitor Model"
EndSection

Section "Device"
	Identifier  "Card0"
	Driver      "vesa"
	VendorName  "Unknown Vendor"
	BoardName   "Unknown Board"
	BusID       "PCI:0:2:0"
EndSection

Section "Screen"
	Identifier "Screen0"
	Device     "Card0"
	Monitor    "Monitor0"

	SubSection "Display"
		Viewport   0 0
		Depth     16
		Modes "1152x864"
	EndSubSection
EndSection
```

#### 3-6-3) 포트 전달

 가상상자(VirtualBox)는 8개의 네트워크접속기를 가지고있다 어느것이든 다음 6가지 모드중 하나에서 작동하게 구성할 수 있다:

  - 부착되지 않음.
  - 네트워크주소 변환(NAT: Network Address Translation).
  - 네트워크 다리.
  - 내부 네트워크.
  - 주인장전용 네트워크.
  - 가상 분산 이더넷 네트워크.

 이것은 웹 둘러보기가 가능하다, 파일을 내려받는다 그리고 [:earth_asia:네트워크주소 변환](http://en.wikipedia.org/wiki/Network%20Address%20Translation)모드 손님(미닉스 3) 내부에서 전자우편을 본다. 기본보드(네트워크주소 변환, NAT)에서는 손님운영체제는 동일한 네트워크의 주인장기계 또는 다른 컴퓨터를 접근할 수 없으며 반대의 경우도 마찬가지다. 하지만, 물리적 교환기(router)처럼, **!가상상자** 는 [포트전달](http://en.wikipedia.org/wiki/Port_forwarding)을 통해 선택된 지원을 만들 수 있다. 이 의미는 가상상자는 주인장의 특정포트를 닫는다 그리고 그곳에 도착한 모든 패킷을 손님에게 다시 전송한다, 같거나 다른 포트에.

 예를 들어, 주인장 기계에서 손님 기계로 SSH 트래픽을 전달하기 위한 포트 222은:
```
VBoxManage modifyvm "VM name" --natpf1 "guestssh,tcp,,2222,,22"
```

 `VM name`은 가상상자 관리화면의 가상기계 이름이다 그리고 `guestssh`는 순수하게 설명하는 이름이다 그리고 생략하면 자동적으로 생성된다.

 주인장 기계에서 다음 명령으로 손님기계에 연결하기 위하여
```
ssh -p 2222 localhost
```

 손님운영체제는 주인장 IP 주소에서 동일한 포트를 사용하지만 네트워크의 주인장 시스템과 다른 가상기계에서도 사용할 수 있다(만약 주인장 기계의 방화벽이 허용하는 경우). 이것은 가려진 원격 장치탐사기(ERSE: Eclipse Remote System Explorer)로 원격 개발과 항해에 유용하다.

### 3-7) 해결방법

#### 3-7-1) 가상상자 3.1

 가상상자 3.1은 미닉스 3을 부팅할 수 없다. 가상상자의 이후버전을 사용하라.

#### 3-7-2) 설치 쟁점(하드웨어가속 없음)

 증상: 부트메뉴 이후 즉시 커널 공황(CD가 탑재되고 부트메뉴가 표시된다 하지만 즉시 공황)

 해결방법:
  1. 만약 하드웨어가속을 활성화한 경우:
   - 자신의 프로세서 가상화확장을 했는지 검증한다(VT-x, AMD-V).
   - 자신의 바이오스(BIOS)에서 하드웨어가속을 사용가능으로 한다.
   - 자신의 가상기계 이미지를 성택하여 설정 대화상자로 이동한다 그리고 주화면에서 **설정(Setting)** 버튼을 누른다.
   - **몸통(System)** 을 누른다.
   - **가속(Acceleration)** 꼬리표를 누른다.
   - **VT-x/AMD-V 사용가능(Enable VT-x/AMD-V)** 을 설정확인 한다.

  2. 만약 하드웨어가속을 사용할 수 없는 경우(예: 가상상자 3.1.2 + Core 2 Duo + 미닉스 3.2.0):
   - 위쪽의 설치단계를 모두 따른다.
   - **VT-x/AMD-V 사용가능(Enable VT-x/AMD-V)** 을 해제확인 한다.
   - 이 명령으로 자신의 가상기계를 시작한다: `VBoxSDL --startvm minix --norawr0 --norawr3`.
   - 이전명령에서 `minix`의 가상기계 이름을 자신의 것으로 대체한다.
   - 가상기계 4.0은 **VT-x/AMD-V 사용가능(Enable VT-x/AMD-V)** 설정확인 버튼이 없다, 하지만 설치중에 커널공황을 방지하기 위해 이 명령을 쟁점을 할 수 있다: `VBoxSDL --startvm minix --norawr0 --norawr3`

#### 3-7-3) 갈래이름이용(DNS: Domain Name Service) 채택(Resolution) 동작안함

 미닉스3 가상기계가 망주소변환(NAT) 망구성(만) 사용할 때, *능동주인장구성규약(DHCP: Dynamic Host Configuration Protocol)* 을 통해 주인장몸통에서 *갈래이름이용(DNS) 제공기(Server) 주소* 를 입수할 것이다. 가상상자에 제공된 *갈래이름이용(DNS) 제공기(Server) 주소* 는 주인장몸통에서 사용된 주소와 완전히 동일하다. 일부 몸통에서는, 이 경우 *갈래이름이용(DNS) 채택* 이 동작안함에 이를 수 있다. 예를 들어, 주인장몸통이 사용하는 *지역 결정기(Local Resolver, 127.0.1.1)* 가, *미닉스3 손님* 이 보내는 *갈래이름이용(DNS) 요청* 을 주인장의 결정기가 아닌 자신에게 헛되게 보낸다. 그 결과는 예를들어 `pkgin up`이 "주인장이름 조회실패(Host name lookup failure)" 오류를 제공한다.

 미닉스3에서, 현재 *능동주인장구성규약(DHCP) 갈래이름이용(DNS) 제공기* 설정을 `dhcpd -q`명령으로 확인할 수 있다 - `DNSserver`로 나열된 *갈래이름이용(DNS) 제공기(Server)* 주소를. 만약 이 주소가 정말로 따라갈 수없는 IP 주소인 경우, 그 하나는 가상상자의 *갈래이름이용 대리자(DNS proxy)* 를 설정확인 해야한다, [:earth_asia:공인 가상상자 웹사이트의 이 지침](https://www.virtualbox.org/manual/ch09.html#nat-adv-dns)을 사용하라. 이 쟁점을 해결 해야한다.

### 3-8) 시간띠 쟁점

 만약 미닉스3에서 시간띠를 구성했다면(예를들어 `/etc/rc.timezone`에 `export TZ=CET`문자행을 넣음으로써), 그리고 자신의 시계(예를들어 `date` 명령으로 인쇄)가 한시간 또는 그 이상의 시간만큼 실제 시간보다 앞서가는 것을 발견한다. 그때 다음 단계를 수행한다(가상상자 4.1.6에서 평가됨):

  1. 가상기계를 종료하고 전원을 끈다(이 경우 가상상자 GUI를 통해 강제 전원끄기가 필요하다).
  2. 가상기계의 **설정(Settings)** 으로 이동한다.
  3. **몸통(System)** 탭으로 이동한다.
  4. **확장기능(Extended features)** 에서, "UTC 시간을 하드웨어 시계로(Hardware clock in UTC time)" 선택사항을 설정결정 한다.
  5. 변경사항 저장을 위해 **결정(OK)** 를 누른다.
  6. 가상기계를 재시작 한다, 그리고 문제점은 이제 고쳐질 것이다, 부팅시에 "잘못된(wrong)" 그리니치의미시간(GMT) 날짜가 인쇄됨에도 불구하고.

 알림 만약 어떤 이유로 자신의 시계가 늦다면, 미닉스3 **vbox** 가상상자 시간 동기구동기(sync driver)가 시간을 자동적으로 수정할 것이다.

### 3-9) 공유폴더

 공유폴더 기능을 사용하기 위해서는 다음을 수행하라:

  1. 현재 가상기계가 꺼져있는지 확인한다.
  2. 가상기계의 **설정(Settings)** 으로 이동한다.
  3. **공유폴더(Shared Folders)** 탭으로 이동한다.
  4. **추가(Add)** 버튼을 누른다 그리고 주인장에서 공유할 폴더를 선택한다 그리고 이름을 지정한다.
  5. 변경사항 저장을 위해 **결정(OK)** 를 누른다.
  6. 가상기계(VM)를 시작하고 로그인한다.
  7. 공유폴더를 끼우기하려면 다음을 수행하라:

```
mount -t vbfs -o share=NAME none /mnt
```

 여기의 `NAME`에 단계 4에서 지정한 자신의 공유이름으로 대체해야 한다. 이것 또한 유의하라 부트 절차에서 끼우기가 공유폴더에 적합한 가상상자 구동기(driver)를 탑재하는것 보다 먼저 발생하기 때문에 자동끼우기를 위해 `fstab`에 진입할 수 없다.

<a name="퀘뮤"></a>
## 4. 퀘뮤 와 케이브이엠(QEMU and KVM)

 이 페이지는 퀘뮤(QEMU)와 케이브이엠(KVM)에 미닉스3을 설치하는 과정을 설명한다. 만약 문제가 발생하면 하단의 해결방법 부문에서 가능한 해결방법을 참조하라.


<a name="보취"></a>
## 5. 보취(Bochs)

 이 페이지는 보취에 미닉스3을 설치하는 과정을 설명한다.
