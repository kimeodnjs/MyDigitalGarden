---
title: Markdown 및 옵시디언 작성 가이드
tags: [computer, markdown]
date: [2024-03-15]
---
>[!info]
> 필요할 때 마다 주기적으로 업데이트 되는 노트입니다.

<br>
<br>
<br>

## 1. 기본
<hr>

### 1. 1 Headers
<hr>

##### 입력

```markdown
# H
## H
### H
#### H
##### H
###### H
```

<br>
<br>

##### 출력

# H
## H
### H
#### H
##### H
###### H

<br>
<br>
<br>

### 1. 2 Quote
<hr>

##### 입력

```markdown
> Blockquote
>> Blockquote
>>> Blockquote
```

<br>
<br>

##### 출력

> Blockquote
>> Blockquote
>>> Blockquote

<br>
<br>
<br>

### 1. 3 Code Block
<hr>

##### 입력

```
\```<문법>
\Code Block
\```

사용 시에 백슬래쉬(Backslash)는 빼기
```

<br>
<br>

##### 출력

```markdown
Code Block
```

<br>
<br>
<br>

### 1. 4 Divider, Line Breaks
<hr>

##### 입력

```markdown
<br> - Line Breaks
<hr> - Divider
```

<br>
<br>

##### 출력

<br>
<hr>

<br>
<br>
<br>

### 1. 5 Bold, Italic, Strikethrough
<hr>

##### 입력

```markdown
**Bold**
__Bold__
*Italic*
_Italic_
~~Strikethrough~~
```

<br>
<br>

##### 출력

**Bold**
__Bold_
*Italic*
_Italic_
~~Strikethrough~~

<br>
<br>
<br>

### 1. 6 Numbered List
<hr>

##### 입력

```markdwon
1. List
2. List
3. List
	1. List
	2. List
	3. List
		1. List
		2. List
		3. List
```

<br>
<br>

##### 출력

1. List
2. List
3. List
	1. List
	2. List
	3. List
		1. List
		2. List
		3. List

<br>
<br>
<br>

### 1. 7 Bullet List
<hr>

##### 입력

```markdown
- List
* List
	- List
	- List
		- List
		- List
```

<br>
<br>

##### 출력

- List
* List
	- List
	- List
		- List
		- List

<br>
<br>
<br>

### 1. 8 Links
<hr>

##### 입력

```markdown
[구글](https://www.google.com)
```

<br>
<br>

##### 출력

[구글](https://www.google.com)

<br>
<br>
<br>

### 1. 9 Images
<hr>

##### 입력

```markdown
![title](https://velog.velcdn.com/images/dae_111/post/937f1a6b-e028-4e02-ba57-4c79c348d842/image.png)

<img src="https://velog.velcdn.com/images/dae_111/post/937f1a6b-e028-4e02-ba57-4c79c348d842/image.png" width="100%" height="100%">
```

<br>
<br>

##### 출력

![title](https://velog.velcdn.com/images/dae_111/post/937f1a6b-e028-4e02-ba57-4c79c348d842/image.png)

<img src="https://velog.velcdn.com/images/dae_111/post/937f1a6b-e028-4e02-ba57-4c79c348d842/image.png" width="100%" height="100%">

<br>
<br>
<br>

### 1. 10  Spaces
<hr>

##### 입력

```markdown
1칸 공백 - &nbsp;
2칸 공백 - &ensp;
4칸 공백 - &emsp;
```

<br>
<br>

##### 출력

&nbsp;Spaces

&ensp;Spaces

&emsp;Spaces

<br>
<br>
<br>

### 1. 11 Special Letters
<hr>

##### 입력

```markdown
\*literal asterisks\*
\#hash mark\#
\[squre brackets\]
\*
\_
\()
\{}
\[]
\#
\+
\-
\.
\!
\\
```

<br>
<br>

##### 출력

\*literal asterisks\*
\#hash mark\#
\[squre brackets\]
\*
\_
\()
\{}
\[]
\#
\+
\-
\.
\!
\\

<br>
<br>
<br>

### 1. 12 Check Box
<hr>

##### 입력

```markdown
- [ ] Check Box
- [x] Check Box
```

<br>
<br>

##### 출력

- [ ] Check Box
- [x] Check Box

<br>
<br>
<br>

### 1. 13 Superscript, Subscript
<hr>

##### 입력

```markdown
Superscript<sup>Superscript</sup>

Subscript<sub>Subscript</sub>
```

<br>
<br>

##### 출력

Superscript<sup>Superscript</sup>

Subscript<sub>Subscript</sub>

<br>
<br>
<br>

### 1. 14 Youtube Video
<hr>

##### 입력

```markdown
<iframe width="1068" height="801" src="https://www.youtube.com/embed/30FTr6G53VU" title="Giant Steps" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>

소스코드 복사하기
```

<br>
<br>

<iframe width="1068" height="801" src="https://www.youtube.com/embed/30FTr6G53VU" title="Giant Steps" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>

소스코드 복사하기

<br>
<br>
<br>

## 2. Obsidian Flavored Markdown
<hr>

### 2. 1 Callouts
<hr>

##### 입력

```markdown
> [!note]

> [!info]

> [!todo]

> [!abstract]

> [!summary]

> [!tldr]

> [!tip]

> [!hint]

> [!important]

> [!success]

> [!check]

> [!done]

> [!question]

> [!help]

> [!faq]

> [!warning]

> [!caution]

> [!attention]

> [!failure]

> [!fail]

> [!missing]

> [!danger]

> [!error]

> [!bug]

> [!example]

> [!quote]

> [!cite]

> [!note]+ 제목
> +나 -를 붙이면 접고 펴는 콜아웃 생성 가능
```

<br>
<br>

##### 출력

> [!note]

> [!info]

> [!todo]

> [!abstract]

> [!summary]

> [!tldr]

> [!tip]

> [!hint]

> [!important]

> [!success]

> [!check]

> [!done]

> [!question]

> [!help]

> [!faq]

> [!warning]

> [!caution]

> [!attention]

> [!failure]

> [!fail]

> [!missing]

> [!danger]

> [!error]

> [!bug]

> [!example]

> [!quote]

> [!cite]

> [!note]+ 제목
> +나 -를 붙이면 접고 펴는 콜아웃 생성 가능

<br>
<br>
<br>

### 2. 2 Footnotes
<hr>

##### 입력

```markdown
이것은 각주입니다.[^1]
이것은 이름이 지정된 각주입니다.[^note]
```

<br>
<br>

##### 출력

이것은 각주입니다.[^1]
이것은 이름이 지정된 각주입니다.[^note]

<br>
<br>
<br>

### 2. 3 Embedding Links, Block Reference
<hr>

##### 입력

```markdown
![[Markdown]]

![[Markdown#^bc4d0d]]
```

<br>
<br>

##### 출력

![[Markdown]]

![[Markdown#^bc4d0d]]

<br>
<br>
<br>

### 2. 4 Highlight
<hr>

##### 입력

```markdown
==하이라이트==
```

<br>
<br>

##### 출력

==하이라이트==

<br>
<br>
<br>

[^1]: 이것은 참조 텍스트입니다.
[^note]: 이것은 이름이 지정된 참조 텍스트입니다.