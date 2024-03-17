---
title: Import로 외부 패키지 이용하기
tags: [computer, python]
date: [2024-03-18]
---
## 1. 외부 패키지 설치
<hr>

&ensp;터미널에서 아래 명령어로 설치하고 관리한다.

<br>

- **pip install \<패키지 이름>:** 해당 패키지 설치
+ **pip install \<패키지 이름>\==<버전>:** 해당 패키지의 특정 버전 설치
- **pip show \<패키지 이름>:** 설치된 패키지 보기
+ **pip install --upgrade\<패키지 이름>:** 패키지 버전 업그레이드
- **pip uninstall \<패키지 이름>:** 패키지 삭제
+ **pip list:** 설치된 패키지 리스트

<br>
<br>
<br>

## 2. 불러오기
<hr>

##### import <패키지 이름> as ...

&ensp; import <패키지 이름>으로 원하는 패키지, 또는 모듈을 불러올 수 있다. 뒤에 as ... 로 원하는 이름을 입력하면 패키지 이름을 전부 쓸 필요없이 설정한 이름을 입력하여 패키지를 사용할 수 있다.

<br>
<br>

##### 예시

```python
import numpy as np  
import matplotlib.pyplot as plt
```

<br>
<br>

##### from <패키지 이름> import ... 

&ensp;from <패키지 이름>으로 패키지, 모듈에서 필요한 함수나 변수만을 가져올 수 있다. 이렇게 가져온 기능은 패키지 이름을 쓰지 않고 import한 함수나 변수의 이름만 써서 사용할 수 있다. 만약 *(와일드카드 문자)를 import 뒤에 쓰면 해당 패키지의 모든 기능을 바로 사용할 수 있다.

<br>
<br>

##### 예시

```python
from astropy.io import fits
from numpy import *
```

<br>
<br>
<br>

##### 사용자정의모듈 불러오기

&ensp;사용자가 직접 정의한 함수나 변수들로 모듈을 작성할 수 있다. 이 때 import로 다른 .py파일에서 불러오려면 **내가 불러오려는 파일이 내가 작성한 코드 파일과 같은 폴더 내**에 있거나, **원래 모듈을 저장하던 폴더 내**에 파일이 위치해 있어야 한다.

<br>

&ensp;간단하게 사용자가 정의한 모듈을 사용하려면, sys.path.append를 통해 내가 import하려는 파일이 들어있는 폴더를 파이썬의 기본 경로에 추가해서 사용할 수 있다.

<br>
<br>

##### 예시

```python
import sys

sys.path.append('C:/myspace/code/python/here/')
```

<br>
<br>
<br>

