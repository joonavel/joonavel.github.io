---
layout: post
title: 깃 블로그 포스트 기능 테스트 해보기
excerpt: Visual Studio Code를 이용해서 로컬에서 작성한 포스트를 로컬 서버에서 확인하고 깃허브 원격 저장소에 업로드 해보자

categories:
    - Blog
tags:
    - [Blog, jekyll, Github, Git]

toc: true
toc_sticky: true

date: 2023-07-31
last_modified_at: 2023-07-31
---

# 1. 마크다운 문법으로 내용 작성해보기

Visual Studio code의 extension에서 Markdown Preview Enhanced를 설치하면 미리보기가 가능하다.

# 2. 상단에 머릿말 작성하기

---로 머릿말 쓰는 영역을 구분할 수 있다.
머릿말 영역에는 내가 원하는 변수를 머릿말에 지정해서 사용이 가능하다.
예를 들어, 머릿말에 categories라는 변수의 값을 'Blog'라고 작성해둔 뒤, Liquid 언어로 {{page.categories}}를 본문내에 쓰면 'Blog'값이 출력될 것이다.

# 3. 코드 작성하기

4개의 공백 또는 하나의 탭으로 들여쓰기를 하면 프로그래밍 코드 형식으로 작성되며 들여쓰지 않은 행을 만날때까지 변환이 계속된다.

예시

    print('한 줄 띄어쓰기가 되어있어야 인식을 시작한다')

예시
    print('한줄 띄어쓰기가 없는 경우')

깃허브에서는 코드블럭코드를 사용해서 문법강조가 가능하다.

예시

```python
def get_hello(k):
    if k % 2 == 0:
        print(hello)
    
    return
```
실제로 작성된 마크다운 언어

    ```python
    def get_hello(k):
        if k % 2 == 0:
            print(hello)
        
        return
    ```

# 4. 수평선 만들기

아래의 마크다운 언어는 모두 수평선을 만든다. 마크다운 문서를 미리보기로 출력할 때 페이지 나누기 용도로 많이 애용한다

    * * *
    
    ***

    *****

    - - -
    
    ----------------------------

- 실제 활용예

* * *
***
*****
- - -
---
-----

- 참고문서

[Github 블로그] 블로그 포스팅하는 방법 : https://ansohxxn.github.io/blog/posting/

마크다운 markdown 작성법 : https://gist.github.com/ihoneymon/652be052a0727ad59601

