---
title: "Git 명령어 모음"
date: 2021-03-07 17:30:00+0900
categories:
  - Tech
author_profile: False
---

> 개인 프로젝트 진행함에 따라 그때그때 마다 알아가는 Git 명령어를 정리한 포스트

- git 개념 익히기 유용한 사이트: https://backlog.com/git-tutorial/what-is-git/
  - [nulab](https://nulab.com/)회사의 [backlog](https://backlog.com/)제품 팀에서 구축한 튜토리얼
  - 1회독 해볼 필요 있음
- `git status`: 현재 git 상황을 보여줌
  ![](https://github.com/SDSTony/sdstony.github.io/blob/master/assets/images/2021-03-07-git-status.PNG?raw=true)
  - `Changes to be committed`: 현재 stage된 파일들을 보여주며, 해당 파일들이 `git commit`시에 반영된다는 것을 뜻한다. `git restore --staged <file>` 명령어를 통해 git add된 파일들을 unstage할 수 있다. 
  - `Changes not staged for commit`: git tracking되고 있는 파일 중 수정이 됬지만, `git add`가 되지 않은 파일들을 보여준다. 해당 파일들을 `git add`를 통해 stage해주어야 추후 `git commit`시 반영된다. 
  - `Untracked file`: working directory내에 있지만 git tracking이 되고 있지 않은 파일들을 의미한다. 
- `git fetch`: 원격 레포에 있는 수정사항 내용들을 가지고 오는 역할, `git pull`과는 다르다. `git pull`은 원격 레포에 있는 수정사항들을 가지고와서 로컬에 반영을 해버리지만, `git fetch`는 가져오기만 할 뿐 로컬에 반영해두지는 않는다. 그래서 `git diff`를 통해 원격 레포와 로컬 레포의 차이점을 확인하기 전에 `git fetch`를 쓴다. 

- `git rm`: 파일을 현재 작업 중인 로컬 장소(working tree)과 원격 레포(index)에서 삭제할 때 사용한다. 원격 레포에서만 삭제 가능하고, 로컬 장소와 원격 레포 모두에서 삭제 가능하지만, 로컬 장소에서만 삭제하고 원격 레포에는 그대로 두는 작업은 수행 불가하다. 
  - `-r`: 폴더를 입력값으로 주고 폴더내의 모든 파일을 삭제하고 싶을 때 사용
  - `--cached`: 원격 레포에서만 파일 삭제하고 싶을 때 사용
  - [사용 예시](https://stackoverflow.com/questions/2047465/how-can-i-delete-a-file-from-a-git-repository)