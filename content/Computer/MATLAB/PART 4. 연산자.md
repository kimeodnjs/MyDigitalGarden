---
title: PART 4. 연산자
tags: [computer, matlab]
date: [2024-03-14]
---
## 1. 연산자
<hr>

### 1. 1 산술 연산자
<hr>

##### 종류

- **+:** 덧셈
+ **-:** 뺄셈
- ***:** 곱셈
+ **/:** 오른쪽 나눗셈
- **\\:** 왼쪽 나눗셈
+ **^:** 지수승

<br>

> [!info]
> 배열 요소별 산술 연산자에 대해서는 [[PART 5. 배열]] 노트를 참조

<br>
<br>

##### 우선순위

- ()&emsp;&emsp;$\Rightarrow$&emsp;&emsp;exp()&emsp;&emsp;$\Rightarrow$&emsp;&emsp;, /, \\&emsp;&emsp;$\Rightarrow$&emsp;&emsp;+, -
+ 소괄호의 안쪽&emsp;&emsp;$\Rightarrow$&emsp;&emsp;소괄호의 바깥쪽
- 왼쪽&emsp;&emsp;$\Rightarrow$&emsp;&emsp;오른쪽

<br>
<br>
<br>

### 1. 2 관계 연산자
<hr>

##### 종류

- **A < B:** A는 B보다 작다.
+ **A > B:** A는 B보다 크다.
- **A == B:** A는 B와 같다.
+ **A <= B:** A는 B보다 작거나 같다.
- **A >= B:** A는 B보다 크거나 같다.
+ **A == B:** A는 B와 같다.
- **A ~= B:** A는 B와 같지 않다.

<br>
<br>

##### 예시

```matlab
>> x = [8 -2 1 4 -1];
>> y = [9 -1 5 4 -2];
>> z1 = x<1

z1 =

  1×5 logical 배열

   0   1   0   0   1

>> z2 = x<= y

z2 =

  1×5 logical 배열

   1   1   1   1   0

>> z3 = x == y

z3 =

  1×5 logical 배열

   0   0   0   1   0

>> z4 = x ~= y

z4 =

  1×5 logical 배열

   1   1   1   0   1

```

<br>
<br>
<br>

### 1. 3 논리 연산자
<hr>

##### 종류

- **&(AND):** 논리 AND 구하기
+ **|(OR):** 논리 OR 구하기
- **~(NOT):** 논리 NOT 구하기
+ **xor(x,y):** x, y의 논리 XOR 구하기

<br>
<br>

##### 예시

```matlab
>> x = [-4 -1 0 2 3 9];
>> y = [-2 0 0 1 4 7];
>> z1 = x & y

z1 =

  1×6 logical 배열

   1   0   0   1   1   1

>> z2 = x | y

z2 =

  1×6 logical 배열

   1   1   0   1   1   1

>> z = y < ~x

z =

  1×6 logical 배열

   1   0   1   0   0   0

```

<br>
<br>
<br>
