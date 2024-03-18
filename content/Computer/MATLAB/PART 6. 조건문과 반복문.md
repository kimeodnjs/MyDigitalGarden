---
title: PART 6. 조건문과 반복문
tags: [computer, matlab]
date: [2024-03-17]
---
## 1. 조건문
<hr>

##### if \<logical expression> ... statement1 ... end

&ensp;'logical expression'조건이 참이면 'statement'를 실행하고, 거짓이면 'statement'를 실행하지 않고 end명령어 밖으로 빠져나간다.

<br>
<br>

##### else ... statement2 ... end

&ensp;if문의 'logical expression'조건이 거짓일 경우 'statement2'를 실행하고 end명령어 밖으로 빠져나간다.

<br>
<br>

##### elseif \<logical expression> ... statement3 ... end

&ensp;if문의 'logical expression'조건이 거짓일 경우, elseif문의 'logical expression'조건을 검토한다. 해당 조건이 참일 경우 'statemen3'를 실행하고 end명령어 밖으로 빠져나가고, 거짓일 경우 참인 조건이 나올 때까지 다음 elseif문을 검토한다. 참인 조건을 찾을 경우 해당 'statement'를 실행시키고, 끝까지 찾지 못할 경우 else문의 'statement'를 실행시키고 end명령어 밖으로 빠져나간다.

<br>
<br>

##### 예시

```matlab
x = input('Enter the grade (1 - 100):');

if x >= 90

grade = 'A'

elseif x >= 80

grade = 'B'

elseif x >= 70

grade = 'C'

elseif x >= 60

grade = 'D'

else

grade = 'F'

end
```

<br>
<br>

##### 주의

- 들여쓰기는 MATLAB에서 무시되므로 프로그램을 실행시키는 데 영향을 끼치지 않는다.
+ **input('prompt'):** 문자열로 입력된 prompt 텍스트를 표시한 다음, 사용자가 값을 입력하고 Return을 누를 때까지 기다린다.

<br>
<br>
<br>

## 2. 반복문
<hr>

### 2. 1 for문
<hr>

##### for \<loop variable = m:q:n> ... statements ... end

&ensp;초깃값 m부터 시작하여 statements를 실행하고, 이후 q만큼 변수를 증가시키면서 반복하여 변숫값이 n이 될 때까지 실행한 후에 end로 for문을 빠져나간다.

<br>
<br>

##### 예시

```matlab
i=0;

for t=0:pi/180:2*pi

i=i+1;

y(i) = sin(t);

z(i) = cos(t);

end

plot(y);

axis([0 360 -1 1]);

hold;

plot(z, ':');

axis([0 360 -1 1]);

xlabel('Degree');

ylabel('Magnitude');

title('Sine and Cosine Function');

grid;

gtext('sin(t)');

gtext('cos(t)');
```

<br>
<br>
<br>

### 2. 2 while문
<hr>

##### while \<logical expression> ... statements ... end

&ensp;'logical expression'조건이 거짓이 될 때까지 'statements'를 반복한다.

<br>
<br>

##### 예시

```matlab
scores = [77 66 72 75 90 86 58 98 89 59];

count = 0;

n = 0;

while n < length(scores)

n = n + 1;

if scores(n) > mean(scores)

count = count + 1;

end

end

display(scores)

display(n)

display(count)
```

<br>
<br>
<br>
