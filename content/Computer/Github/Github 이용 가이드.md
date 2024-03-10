---
title: Github 이용 가이드
tags: [computer, github]
date: [2024-02-26]
---
## 1. 버전 관리와 github
<hr>

&ensp;버전 관리 시스템(VCS, Version Control System)이란 파일의 변경 사항을 시간에 따라 기록하고, 필요할 때 특정 버전을 다시 호출할 수 있는 시스템을 일컫는다.

<br>

 > [!info] 깃허브의 장점
 > - 소스 코드를 주고 받을 필요 없이, 같은 파일을 여러 명이 동시에 병렬로 작업할 수 있다.
 > + 분산 버전 관리이므로 인터넷이 안되는 곳에서도 작업할 수 있고, 중앙 저장소가 날아가버려도 복구가 가능하다.

<br>
<br>
<br>

## 2. github의 작동 구조
<hr>

##### Working Tree, Working Directory

&ensp;작업자의 현재 시점. 실제로 작업자가 파일을 수정, 저장하는 directory를 말하며, .git폴더가 숨어있는 폴더이다.

<br>
<br>

##### Snapshot

&ensp;특정 시점에서 파일, 폴더 또는 작업공간의 상태를 의미한다. Commit할 때마다 해쉬값으로 찾을 수 있는 하나의 스냅샷이 생기게 된다. 이후 특정 commit을 확인해서 해당 시간대의 작업공간의 상태를 알 수 있다.

<br>
<br>

##### Staging Area, Stage

&ensp;Repository에 commit하기 전에 임시로 준비하는 위치이다.

<br>
<br>

##### Repository

&ensp;스테이지에서 대기하고 있던 스냅샷을 버전으로 만들어 저장하는 저장소이다. git은 원격 저장소(Remote Repository)와 로컬 저장소(Local Repository)의 두 가지 저장소를 제공한다.

<br>

- **Remote Repository:** 파일이 원격 저장소 전용 서버에서 관리되며, 여러 사람이 함께 공유하기 위한 저장소이다.
+ **Local Repository:** 내 PC에 파일이 저장되는 개인 전용 저장소이다. 처음부터 새로 만들거나, 이미 만들어져 있는 원격 저장소를 로컬 저장소로 복사해와서 만들 수 있다.

<br>
<br>
<br>

## 3. 주요 용어
<hr>

##### Commit

&ensp;스테이지에서 대기하고 있던 스냅샷을 확정하고 로컬 저장소에 저장하는 작업이다.

<br>
<br>

##### Branch

&ensp;분기점을 의미하며, 작업은 저장소의 특정 브랜치에서 진행된다. 작업 중인 브랜치를 전환할 때마다 워킹 트리에서 보이는 파일들의 상태도 바뀐다. 

<br>
<br>

##### HEAD

&ensp;HEAD가 가리키는 브랜치가 현재 작업중인 브랜치이다.

<br>
<br>

##### Merge

&ensp;다른 브랜치의 내용을 현재 브랜치로 가져와 합치는 작업을 의미한다.

<br>
<br>
<br>
