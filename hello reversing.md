# 리버싱 기초
## Hello world 리버싱하기 



<hr>

디버거와 어셈블리언어 
<br> 🔹 개발도구를 이용하여 C언어 소스코드(cpp)를 빌드하면 실행파일이 생성
<br> 🔹 이는 사람이 이해하기 쉬운 C언어 소스코드를 기계가 이해하기 쉬운 기계어로 변환하는 과정.
<br> 🔹 이를 보는 방법 -> 디버거 유틸리티 디버거에 탑재된 디스어셈블러 모듈을 통하여 이 기계어를 어셈블리 언어로 번역하여 보여줌
<br>  
#유의사항   

  <strong><img width="25" alt="star1" src="https://user-images.githubusercontent.com/78655692/151471925-e5f35751-d4b9-416b-b41d-a059267a09e3.png">실행파일을 생성하는 어떠한 프로그래밍 언어라도 빌드과정을 거치면 모두 기계어로 변환됨. </strong>  
  디버거를 통해서 어떤 실행파일이라도 어셈블리 언어로 번역해서 볼수있음
<br>  어셈블리 언어는 cpu에 종속되어있으며. intel x86 , ARM 계열의 cpu로 나뉨 


<hr>

## <strong>Hello world.exe 디버깅 하기  </strong>

### 사용 디버거 <span style="color:white; background-color:black; font-size:130%">x64dbg
<img src="https://user-images.githubusercontent.com/108571106/179580523-9ae33ad5-cb9c-4529-a2a9-1c664aef08cc.png">

### 책의 예문은 ollydbg를 사용했으나. 현재 64bit OS를 사용중이여서 실행되지 않아   x32dbg 프로그램을 이용함.


***
<span style="color:white; background-color:black; font-size:130%">Code Window</span>   
기본적으로 disassembly code를 표시하여 각종 comment, label을 보여주며, 코드를 분석하여 loop, jump 위치 등의 정보를 표시합니다.   
<span style="color:white; background-color:black; font-size:130%">Window	CPU register</span>    
값을 실시간으로 표시하며 특정 register들은 수정도 가능합니다.   
   <span style="color:white; background-color:black; font-size:130%">Dump Window</span>	    
프로세스에서 원하는 memory 주소 위치를 Hex와 ASCII/유니코드 값으로 표시하고 수정도 가능합니다.  
  <span style="color:white; background-color:black; font-size:130%">Stack Window</span>   
	ESP register가 가리키는 프로세스 stack memory를 실시간으로 표시하고 수정도 가능합니다
***
**### EP (entry point)**

Windows 실행파일의 코드시작점을 의미하며,   프로그램이 실행될때 cpu에 의해 가장먼저 실행되는 코드 시작위치이다.
 