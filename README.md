# Git Blog 빌드 과정

## 목차
1. 깃헙 리포지토리 생성
2. Jekyll 시작하기
3. 테마 적용하기
4. 댓글 기능 추가하기


## 깃헙 리포지토리 생성

- Github에서 chohyeonho.github.io 이름의 Repo 생성
- `git clone`으로 로컬 리포지토리에 연동
- github - Setting - Developer settings에서 Personal Access Token(PAT) 생성
- 이 토큰을 사용하여 `git push`로 원격 저장소에 반영

## Jekyll 시작하기
- [https://jekyllrb-ko.github.io/docs/](https://jekyllrb-ko.github.io/docs/)를 따라서 Jekyll과 Bundler 젬 설치
- `jekyll -v`로 Jekyll이 설치되었는지 확인
- `jekyll new . --force`로 blog 디렉토리에 Jekyll을 설치
- `jekyll serve` 실행 후, `localhost:4000`에 접속해서 기본 테마로 생성된 Jekyll 사이트 확인
- `git push`로 원격 저장소에 반영 후, `chohyeonho.github.io`에 접속해서 확인

## 테마 적용하기
- [https://jekyllthemes.io](https://jekyllthemes.io)에서 [Alembic](https://jekyllthemes.io/theme/alembic) 테마를 선택
- Alembic 테마를 `git clone`해서 로컬에 받아온다
- 받아온 테마 파일들을 blog 로컬 저장소에 덮어쓴다

## 댓글 기능 추가하기
- [Disqus](https://disqus.com)에 회원가입
- Disqus 홈페이지에서 Platform이 Jekyll인 새 사이트 생성
- `_config.yml`에 key-value 추가
- Disqus 홈페이지에서 Universal Code를 복사해서 `_layouts/post.html`에 추가
- 댓글을 허용하고 싶은 `_posts/*.md`에서 `comments: true`로 지정