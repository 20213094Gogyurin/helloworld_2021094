# 20213094 Gogyurin
-------------------
## top
1) 리눅스 명령어 **top**
+ 시스템의 상태를 전반적으로 가장 빠르게 파악 가능(CPU, Memory, Process)
+ 옵션 없이 입력하면 interval 간격(기본 3초)으로 화면을 갱신하며 정보를 보여줌
top 실행 전 옵션
+ 순간의 정보를 확인하려면 -b 옵션 추가(batch 모드)
+ -n : top 실행 주기 설정(반복 횟수)
2. top 실행 후 명령어
+ shift + p : CPU 사용률 내림차순
+ shit + m : 메모리 사용률 내림차순
+ shift + t : 프로세스가 돌아가고 있는 시간 순
+ k : kill. k 입력 후 PID 번호 작성. signal은 9
+ f : sort field 선택 화면 -> q 누르면 RES순으로 정렬
+ a : 메모리 사용량에 따라 정렬
+ b : Batch 모드로 작동
+ 1 : CPU Core별로 사용량 보여줌

--------------------
## ps
1) 리눅스 명령어 **ps**
+ 현재 실행 중인 프로세스의 목록을 보는 명령어이다.
2) 기본 ps 명령어 구성
+ ps -e, -A : 모든 프로세스를 보여줍니다. 
+ ps -a : 세션 리더와 터미널과 연관된 프로세스들을 제외한 모든 프로세스를 보여줍니다.
+ ps -d : 세션 리더를 제외한 모든 프로세스를 보여줍니다.
+ ps -f : full format으로 세션의 정보를 표시합니다. 
+ ps -ef : -e와 -f의 옵션 조합인데, 모든 프로세스를 full format으로 보여줍니다. 아래는 그 결과를 보여줍니다. UID, PID, PPID, C, STIME, TTY, TIME, CMD의 정보를 볼 수 있네요. TTY(연결 터미널)가 없으면 대부분 데몬 혹은 커널 프로세스입니다. 
+ ps -u userlist : EUID 혹은 유저 이름으로 프로세스를 고릅니다. 이때 여러 uid를 줄수 있는데 ','(comma)로 구분하여 명시해줍니다. euid는 프로세스가 수행할때 갖는 유저 권한을 말합니다.
+ ps -U userlist : -u 옵션과는 동일하나 RUID가 갖는 프로세스만을 찾아냅니다. ruid는 real user id라는 것으로 실제 프로그램을 실행한 uid를 의미합니다. 이때도 쉼표로 여러 uid를 지정할 수 있습니다.
+ ps -p pidlist : 프로세스 id가 일치하는 프로세스를 출력합니다. 여러 pid들을 뽑아내고 싶다면 마찬가지로 ','(comma)로 pid를 구분하여 명시해줄 수 있습니다. 이 명령은 ps --pid pidlist와 같습니다.
+ ps --ppid pidlist : 부모 프로세스 id와 일치하는 프로세스를 출력합니다. 역시 여러 ppid를 ','(comma)로 구분가능합니다.
+ ps -t ttylist : tty와 일치하는 프로세스들을 출력해줍니다. 이 명령은 t 혹은 --tty 옵션과 같습니다. 
+ ps -o format : 사용자가 지정한 format대로 출력합니다. format에 대해서는 설명이 길지만 간략하게 원하는 column만 보여준다고 기억하시면 됩니다. 예를 들어 사용자가 임의로 pid, ppid, cmd, uid 등을 표시할 수 있습니다.

---------------------
## jobs
1) 리눅스 명령어 **jobs**
+ jobs 명령어는 작업이 중지된 상태나 백그라운드로 진행 중인 상태를 표시.
<img width="409" alt="jobs" src="https://user-images.githubusercontent.com/106871417/172000353-251bb077-450f-4aea-9bca-8a0482263a21.PNG">
