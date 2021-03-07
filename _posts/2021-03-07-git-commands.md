---
title: "Git 명령어 모음"
date: 2021-03-07 17:30:00+0900
categories:
  - Tech
author_profile: False
---

> 개인 프로젝트 진행함에 따라 그때그때 마다 알아가는 Git 명령어를 정리한 포스트

- `git status`: 현재 git 상황을 보여줌
  ![](https://github.com/SDSTony/sdstony.github.io/blob/master/assets/images/2021-03-07-git-status.PNG?raw=true)
  - `Changes to be committed`: 현재 stage된 파일들을 보여주며, 해당 파일들이 `git commit`시에 반영된다는 것을 뜻한다. `git restore --staged <file>` 명령어를 통해 git add된 파일들을 unstage할 수 있다. 
  - `Changes not staged for commit`: git tracking되고 있는 파일 중 수정이 됬지만, `git add`가 되지 않은 파일들을 보여준다. 해당 파일들을 `git add`를 통해 stage해주어야 추후 `git commit`시 반영된다. 
  - `Untracked file`: working directory내에 있지만 git tracking이 되고 있지 않은 파일들을 의미한다. 

- `git fetch`: 원격 레포에 있는 수정사항 내용들을 가지고 오는 역할, `git pull`과는 다르다. `git pull`은 원격 레포에 있는 수정사항들을 가지고와서 로컬에 반영을 해버리지만, `git fetch`는 가져오기만 할 뿐 로컬에 반영해두지는 않는다. 그래서 `git diff`를 통해 원격 레포와 로컬 레포의 차이점을 확인하기 전에 `git fetch`를 쓴다. 