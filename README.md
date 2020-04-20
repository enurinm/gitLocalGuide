# GitLab Local Guide

## 주 사용 명령어  

### 시작하기

1. 로컬 폴더 생성
2. 우클릭 후 Git Bash Here

### 레포지토리/Branch 받아오기

1. 해당 폴더 내에서 Git Bash Here
2. 레포지토리 가져온 후 원격 브랜치 목록 보기

```bash
$ git clone (레포지토리 url) //레포지토리 가져오기
$ git remote update //원격 브렌치 최신으로 업데이트  

$ git branch //브랜치 목록 확인(현재 파일(=로컬)에서), 앞에 * 붙은게 현재 브랜치
$ git branch -r //원격 브랜치 목록 보기
$ git branch -a //로컬 브랜치+원격 브랜치 목록 보기
```

3. 체크아웃 옵션

```bash
$ git checkout -t (원격 path)/(브랜치명) //원격저장소의 브랜치명과 똑같이 로컬에 가져옴
$ git checkout -b (생성할 브랜치명) (원격브랜치명)
$ git checkout -b (브랜치명) //브랜치 작성&체크아웃 한번에 함 
```

- -t -b 참조 : https://blog.outsider.ne.kr/641

- -b 브랜치명 참조 : https://backlog.com/git-tutorial/kr/stepup/stepup2_3.html

### 파일 수정 후

```bash
$ git status //파일 목록 보기
```

1. add - commit - push

```bash
$ git log //커밋 히스토리 조회

$ git add * //전체 add
$ git add . //class파일 빼고 java만 add되는듯!
$ git add (파일명) //해당 파일 add
$ git add -p //추가할 때 변경사항 확인

$ git commit * -m "커밋 메세지" //커밋 메세지 적고 커밋
$ git commit -v //커밋할 때 변경사항 확인

$ git merge (저 브렌치에서) (이 브렌치로) //왼쪽 브렌치를 오른쪽브렌치에 합침(변경되는쪽: 오른쪽)

$ git push origin (브랜치명) //add, commit 후 원격 브랜치에 push, origin은 remote name
$ git push -u origin (브랜치명) //원격에 로컬 브랜치를 새로운 브랜치로 올림
```

- 변경사항 확인 코드 참조 : https://blog.outsider.ne.kr/1247

### 서버에서 받아오기

```bash
$ git fetch //원격저장소의 내용 받아오기
$ git pull //원격저장소의 내용 받아오기+merge
```



### 기타

```bash
$ git reset --hard (커밋번호) //해당 커밋으로 head를 되돌리고 그 이후 내역은 삭제
$ git reset --soft (커밋번호)
```
- reset, revert 코드 참조 : https://www.devpools.kr/2017/02/05/%EC%B4%88%EB%B3%B4%EC%9A%A9-git-%EB%90%98%EB%8F%8C%EB%A6%AC%EA%B8%B0-reset-revert/



------

## 기타 참조

- git 안내서 : https://backlog.com/git-tutorial/kr/

- branch, merge : [https://git-scm.com/book/ko/v2/Appendix-C%3A-Git-%EB%AA%85%EB%A0%B9%EC%96%B4-Branch%EC%99%80-Merge](https://git-scm.com/book/ko/v2/Appendix-C%3A-Git-명령어-Branch와-Merge)

- git 기초 명령어 정리 : [https://medium.com/@pks2974/%EC%9E%90%EC%A3%BC-%EC%82%AC%EC%9A%A9%ED%95%98%EB%8A%94-%EA%B8%B0%EC%B4%88-git-%EB%AA%85%EB%A0%B9%EC%96%B4-%EC%A0%95%EB%A6%AC%ED%95%98%EA%B8%B0-533b3689db81](https://medium.com/@pks2974/자주-사용하는-기초-git-명령어-정리하기-533b3689db81)

- git 명령어 정리 2 : [https://medium.com/sjk5766/git-%EB%AA%85%EB%A0%B9%EC%96%B4-%EC%A0%95%EB%A6%AC-a11f8d352cc5](https://medium.com/sjk5766/git-명령어-정리-a11f8d352cc5)  

- pull request 이해하기 :  [https://velog.io/@zansol/Pull-Request-%EC%9D%B4%ED%95%B4%ED%95%98%EA%B8%B0](https://velog.io/@zansol/Pull-Request-이해하기)

- git log : [https://git-scm.com/book/ko/v2/Git%EC%9D%98-%EA%B8%B0%EC%B4%88-%EC%BB%A4%EB%B0%8B-%ED%9E%88%EC%8A%A4%ED%86%A0%EB%A6%AC-%EC%A1%B0%ED%9A%8C%ED%95%98%EA%B8%B0](https://git-scm.com/book/ko/v2/Git%EC%9D%98-%EA%B8%B0%EC%B4%88-%EC%BB%A4%EB%B0%8B-%ED%9E%88%EC%8A%A4%ED%86%A0%EB%A6%AC-%EC%A1%B0%ED%9A%8C%ED%95%98%EA%B8%B0)
  
