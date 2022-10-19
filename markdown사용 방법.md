# 마크다운(markdown) 사용방법

## 1. 제목(Headers)

* 글머리: h1 ~ h6 까지만 지원
    
    # This is a H1
    ## This is a H2
    ### This is a H3
    #### This is a H4
    ##### This is a H5
    ###### This is a H6
    ```
    # This is a H1
    ## This is a H2
    ### This is a H3
    #### This is a H4
    ##### This is a H5
    ###### This is a H6
   ```
## 2. 줄바꿈 (Line Breaks)
띄어쓰기 두번 또는 < br / >
```
Line <br/> // 또는 띄어쓰기 두번 
Breakers
```

## 3. 수평선 (Horizontal Rule)
---  
***  
----  
****  
```
---
***
----
****
<hr/>
```

## 4. 글자 강조 (Emphasis)
**굵은 글씨**  
*이텔릭*  
_이탤릭_  
~~취소선~~  
<u>밑줄</u>  
```
**굵은 글씨**  
*이텔릭*  
_이탤릭_  
~~취소선~~  
<u>밑줄</u>  
```

## 5. 목록 (List)
### ● 순서있는 목록(번호)   
 순서있는 목록은 숫자와 점을 사용한다.
1. 첫번째
2. 두번째
3. 세번째
```
1. 첫번째
2. 두번째
3. 세번째
```
**순서는 내림차순으로 정의된다.**

1. 첫번째
3. 세번째
2. 두번째
```
1. 첫번째
3. 세번째
2. 두번째
```
### ● 순서없는 목록(글머리 기호: `*`, `+`, `-` 지원)

* 빨강
  * 녹색
    * 파랑

+ 빨강
  + 녹색
    + 파랑

- 빨강
  - 녹색
    - 파랑
```
* 빨강
  * 녹색
    * 파랑

+ 빨강
  + 녹색
    + 파랑

- 빨강
  - 녹색
    - 파랑
```
**글머리 기호는 혼합해서 사용 가능.**

```
* 1단계
  - 2단계
    + 3단계
      + 4단계
```

* 1단계
  - 2단계
    + 3단계
      + 4단계

## 6. 인용문 (BlockQuote)
이메일에서 사용하는 ```>``` 블럭인용문자를 이용한다.
> This is a first blockqute.
>	> This is a second blockqute.
>	>	> This is a third blockqute.

이 안에서는 다른 마크다운 요소를 포함할 수 있다.
> ### This is a H3
> * List
>	```
>	code
>	```
```
> This is a first blockqute.
>	> This is a second blockqute.
>	>	> This is a third blockqute.
```
## 7. 링크 (Link)
* 참조링크

    ```
    [link keyword][id]

    [id]: URL "Optional Title here"

    // code
    Link: [Google][googlelink]

    [googlelink]: https://google.com "Go google"
    ```

    Link: [Google][googlelink]

    [googlelink]: https://google.com "Go google"

* 외부링크  
title 옵션

    ```
    사용문법: [Title](link)

    ex1) [Google](https://google.com, "google link")
    ```
    Link: [Google](https://google.com)

    ```
    사용문법: [Title](link, "Optional Title")

    ex1) [Google](https://google.com, "google link")
    ```
    Link: [Google](https://google.com, "google link")


* 자동연결  
    인터넷 URL 혹은 이메일 주소를 적합한 형식으로 링크를 생성해준다.
    ```
    일반적인 URL 혹은 이메일주소인 경우 적절한 형식으로 링크를 형성한다.

    * 외부링크: <http://example.com/>
    * 이메일링크: <address@example.com>
    ```
