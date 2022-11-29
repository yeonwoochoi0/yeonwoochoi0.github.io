# 프로젝트 제작 과정

## Git

[Github](https://github.com) 에 가입한 후 repository를 생성한다. 
그 후, repository의 주소를 복사해서 cmd 창에서 local repository에 git clone 명령어를 이용해 연동한다.



## Markdown

파일을 작성할 때 일반 텍스트로 서식 있는 문서를 작성하기 위해 마크다운을 사용한다.
여러가지 마크다운 문법을 익힌 후 index.html을 작성한다.




## Commit

git status 명령어로 현재 상태를 확인 후 git add 명령어로 작성한 파일을 추가한다.
git commit -m 명령어로 파일을 commit한다. 이때 -m은 메세지를 남기는 명령어이다.
git push로 원격 저장소에 반영한다. 이때 Github와 연결을 하기 위해 토큰을 생성해 연결한다.

위 과정을 완료하면 [페이지](https://yeonwoochoi0.github.io)에 작성한 index.html이 뜬다.



## Jekyll

[Jekyll 공식 사이트](https://jekyllrb-ko.github.io)에서 DOCS에서 사용하고 있는 OS에 맞는 jekyll 설치 방법을 찾아 이를 따라서 설치한다. 작성자는 Window를 사용하고 있기에 Window에 맞는 jekyll 설치 방법을 따랐다.
Ruby와 Jekyll을 설치한 후 실행한다.

현재 디렉토리에 jekyll new . --force 명령어를 사용해 Jekyll을 설치한다.
bundle exec jekyll serve 명령어를 이용해 Jekyll을 실행한다. 
서버 주소를 입력하면 기본 테마인 minima를 이용한 사이트가 보인다.
새로 생성된 파일들 중 _config.yml 파일을 수정하면 세부 작성된 내용을 수정할 수 있다.

위의 commit 과정을 따라 진행하면, [사이트](https://yeonwoochoi0.github.io)에 반영된다.



## Post

2022-11-28-Git_Github.md를 git과 github에 대해 배운 내용을 바탕으로 markdown 형식으로 작성한 후 commit 과정을 따라 반영시킨다. 



## Theme

[Jekyll Theme Site](http://jekyllthemes.org/)에서 마음에 드는 테마로 Lanyon을 선택한다.
적용시키기 위해 테마를 clone해서 local로 받아온다.
작성한 포스트가 들어있는 _posts를 제외하고 나머지 파일을 덮어 쓴다.
_config.yml의 새로 추가된 내용들을 작성자의 정보에 맞게 변형한다. 여기에서 제목과 간단한 소개 등을 작성한다.
about.md의 내용을 변경하여 사이드바에서 about을 누르면 블로그 제작에 대한 정보가 나오도록 변경한다.
_layout/default.html을 변형하여 색을 테마 제작자의 설명을 참고하여 보라색으로 변경한다.
_includes/sidebar.html에서 필요한 사이드바만을 선택하여 이를 제외한 다른 것을 지운다.
위의 commit 과정을 진행한다.



## Comments

다양한 댓글 삽입 사이트들 중 [Disqus](https://disqus.com)를 사용한다.
우선 사이트에 회원가입을 한 후 사이트를 생성한다.
_config.yml에 댓글에 대한 key와 value를 추가한다.
그 후 disqus 홈페이지에Installation에서 jekyll을 선택하면 보이는 코드를 복사한다.
var로 시작하는 코드의 주석을 제거한 후, 코드를 추가한다.
s.src가 잘 지정되어 있는지 확인한다.



## Error
오류가 발생하여 댓글이 나오지 않는 현상을 겪었다.
이는 Disqus-Settings-Advanced에 들어가 Trusted Domains에 github 주소를 추가하니 오류가 해결되었다.

