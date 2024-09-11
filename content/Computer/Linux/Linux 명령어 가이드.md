---
title: Linux 명령어 가이드
tags: [computer,linux]
date: [2024-06-30]
---
>[!info]
> 필요할 때 마다 업데이트 되는 노트입니다.

<br>
<br>
<br>

## 1. 주요 명령어
<hr>

##### pwd

&ensp;현재 directory의 경로를 출력

<br>
<br>

##### ls

&ensp;현재 directory의 파일 목록 출력

<br>

- **ls -alh:** 파일의 권한, 만든 사람(소유자), 파일 크기, 파일 생성 날짜 등 파일의 자세한 정보까지 출력

<br>
<br>

##### echo

&ensp;주어진 인자를 출력

<br>

- **echo $HOME:** Home directory의 경로를 출력

<br>
<br>

##### cd

&ensp;특정 directory로 이동

<br>

- **cd <directory 경로>:** 해당 directory로 이동
+ **cd ~:** Home directory로 이동

<br>
<br>

##### mv

&ensp;특정 파일들을 다른 directory로 이동

<br>

- **mv \<file1> \<file2>:** file1을 file2로 이름 변경
+ **mv \<file1> \<dir1>:** file1을 dir1이라는 directory로 이동
- **mv \<dir1> \<dir2>:** dir1을 dir2의 하위 directory로 이동

<br>
<br>

##### cp

&ensp;특정 파일들을 복사해서 새로 생성

<br>

- **cp \<dir1/file1> \<dir2/file2>:** dir1의 file1을 dir2의 file2로 복사
+ **cp -r \<dir1> \<dir2>:** dir1의 하위 directory까지 포함해 모두 dir2로 복사

<br>
<br>

##### mkdir

&ensp;새로운 directory를 생성

<br>

- **mkdir \<dir1>:** 현재 directory에서 dir1이라는 하위 directory를 생성
+ **mkdir -p \<dir1>:** 부모 directory가 존재하지 않아도 지정된 경로에 dir1을 생성

<br>
<br>

##### rm

&ensp;파일이나 directory를 삭제

<br>

- **rm \<file1>:** file1을 삭제
+ **rm -r \<dir1>:** dir1의 하위 directory까지 모두 삭제
- **rm -f \<file1>:** file1을 강제로 삭제

<br>
<br>

##### cat

&ensp;내용을 입력하고 ENTER 키를 누르면 입력 내용을 그대로 출력. (ctrl + C) 키를 누르면 종료된다.

<br>

- **cat > <파일명.확장자명>:** 파일을 덮어쓰기 형식으로 변경(기존 내용을 무시). 내용을 모두 작성하고 편집을 종료하려면 (ctrl + C)를 입력
+ **cat >> <파일명.확장자명>:** 파일의 내용을 추가
- **cat <파일명.확장자명>:** 파일의 내용을 출력
+ **cat -n <파일명.확장자명>:** 파일 내용의 줄 번호도 함께 출력

<br>

- **Enter 키:** 현재 행 저장 및 다음 행으로
+ **(ctrl + D):** 현재 행 저장 및 종료
- **(ctrl + C):** 현재 행 취소 및 종료
+ **(ctrl + Backspace):** 백 스페이스

<br>
<br>

##### clear

&ensp;터미널 작성 내역을 모두 삭제


<br>
<br>
<br>

## 2. vim에디터<hr>

##### vi \<file1> 또는 vim \<file1>

&ensp;file1을 vim에디터로 열기.

<br>
<br>

##### 모드 전환

- **'i':** 입력 모드로 전환
+ **'esc':** 현재 모드를 종료하고 명령 모드로 전환
- **':' :** 마지막 행에 명령을 입력하는 명령 모드로 전환

<br>
<br>

##### 저장 및 종료

- **':w' :** 파일을 저장
+ **':q' :** vim을 종료(저장되지 않은 변경 사항이 있을 시 종료 안됨)
- **':q!' :** vim을 강제로 종료
+ **':wq' 또는 ':x' :** 파일을 저장 후 vim을 종료
- **':w file1' :** 파일을 file1이라는 이름으로 저장

<br>
<br>

##### 기능

- **:set number :** vi 편집기에서 줄 수를 표현
+ **:set nonumber :** vi 편집기에서 줄 수를 숨김
- **/<검색어>:** 검색 기능
+ **dd**: 해당 줄 삭제
<br>

### 2. 1 파이썬<hr>

##### ipython --pylab

&ensp;내장 파이썬 실행

<br>
<br>

##### exit()

&ensp;내장 파이썬을 종료

<br>
<br>













><span style="color:black">Bundler    
    
```commandline  jekyll 로컬 서버 실행: bundle exec jekyll serve    
    
로컬 서버 강제 종료  port 번호로 PID 찾기: lsof -i :<포트번호>  PID로 강제 종료하기: kill -9 <PID>    
```
<br>
