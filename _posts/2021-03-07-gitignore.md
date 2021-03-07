---
title: "gitignore파일의 중요성"
date: 2021-03-07 23:30:00+0900
categories:
  - Tech
author_profile: False
---

> TL;DR Github 인터페이스를 통해 PR 리뷰시 불필요한 파일이 많으면 리뷰가 안됨, gitignore을 통해 해당 파일을 무시해야 함

- Jupyter Notebook, Jupyter Lab으로 작업하다보면 .ipynb_checkpoints 파일이 생성된다. 
- 해당 파일들은 굳이 index에 올릴 필요 없는 파일이므로, 무시해야 한다.
- 기존에는 해당 .ipynb_checkpoints파일을 삭제하고 `git add .` 한 후에 `git commit`을 했다. 상당히 tedious 한 작업들이였다. 
- 다음번에 .ipynb파일 수정하면 또 .ipynb_checkpoints가 생성되므로, 또 위 작업을 반복해야 했다. 
- 하지만 `.gitignore`파일 생성후 .ipynb_checkpoints를 명시하면, 해당 이름이 들어간 파일을 git tracking 하지 않게 된다. 
- 마찬가지로 Jupyter Book을 통해 `build`를 실시하면 `_build`폴더에 다수의 `html`파일과 `doctree`파일들이 생성되는데, 이것들을 커밋하게 되면 github 인터페이스에서 수백여개의 파일들이 한꺼번에 tracking되므로 수정사항 확인시 상당히 불편하다. 
- 그래서 `.gitignore`을 통해 `_build`폴더를 tracking하지 않으므로 인해서 문제를 해결할 수 있다. 