---
layout: post
title: TIL-Github_Pages
date: 2024-02-16 00:00:00 +0900
description: You’ll find this post in your `_posts` directory. Go ahead and edit it and re-build the site to see your changes. # Add post description (optional)
img: TIL/welcome.jpg # Add image post (optional)
tags: [Java, Springboot, JPA] # add tag
---
# Github Pages

목차
- Github Pages
- Jekyll

## Github Pages
Github의 정적 웹사이트 호스팅 서비스
- Public Repository의 HTML, CSS, JS 등을 게시해주는 서비스
    - 내 github repo에 만들어놓은  HTML, CSS, JS들을 게시해준다.
- 복잡한 기능 없이 정보 공유용 사이트로 많이 활용. 상업적 활용은 금지되어 있다.
- *.github.io 주소들은 Github Pages로 만들어졌다

1. repo 이름을 <내 github name>.github.io 로 생성
2. 클론하여 로컬로 레포지토리를 가져와서, index.html 생성
3. add / commit / push
4. 배포알림 확인 후(노란색 -> 초록색 체크) <내 github name>.github.io 접속

## Jekyll
Github의 설립자 중 하나가 Ruby를 이용해 만든 정적 웹사이트 생성기
- Github Pages는 Jekyll을 가지고 만든 웹사이트를 호스팅할 수 있다.

### Ruby 설치
https://rubyinstaller.org/downloads/  
 
Git Bash로 ruby --version / gem -v 쳤을때  
```
$ ruby --version
ruby 3.2.3 (2024-01-18 revision 52bb2ac0a6) [x64-mingw-ucrt]

$ gem -v
3.4.19
```
나오면 잘 설치된것  

## Jekyll

gem install bundler // maven 같은것. 빌드 자동화 도구?

gem install github-pages

gem install jekyll // 정적 사이트 생성기

jekyll new . // 폴더 내 파일들을 싹 지우고 실행

bundle install

bundle exec jekyll serve

여기까지 하고 add/commit/push. 깃허브 초록체크표시 확인
---

### Jekyll 테마 입히기

https://jekyllthemes.io/theme/flexible-jekyll

다운받아 안의 내용 싹다 복사 - 로컬 레포지토리에 붙여넣기(기존 건 다 삭제)  

_config.yml 에서

baseurl: "" # the subpath of your site, e.g. /blog
url: "https://mafatofu.github.io" # the base hostname & protocol for your site, e.g. http://example.com

baseurl 비워주고 url을 본인의 것으로 변경

다시

bundle install

bundle exec jekyll serve

http://127.0.0.1:4000 

들어갔을 때 잘 반영됐으면 ok


### 글 올리기
_posts 폴더 안의 .markdown 파일들 확인

해당 글 위에 써져있는 폼을 확인하여, 알맞게 변경해준다.  
특히, date와 title 부분은 filename과 일치시켜주도록 하자.  
기본적으로, 내가 작성한 markdown을 기반으로 글이 포스팅 된다.  
마크다운을 잘 사용하여 작성하면 된다.

웰컴페이지 폼
```
---
layout: post
title: TIL-Github_Pages
date: 2024-02-16 00:00:00 +0900
description: You’ll find this post in your `_posts` directory. Go ahead and edit it and re-build the site to see your changes. # Add post description (optional)
img: TIL/welcome.jpg # Add image post (optional)
tags: [Java, Springboot, JPA] # add tag
---
```