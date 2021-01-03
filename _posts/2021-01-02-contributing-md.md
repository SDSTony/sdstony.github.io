---
title: "CONTRIBUTING.md 파일은 무엇인가?"
date: 2021-01-02
categories:
  - Open Source
tags:
  - PyCaret
  - Executable Book Project
author_profile: False 
---

Jupyter Notebook, Jupyter Lab, 그리고 Python에서 제공되는 각종 패키지들의 공통점은 모두 오픈 소스라는 것이다. 5년 가까이 오픈 소스를 활용해오면서 문득 오픈 소스에 기여해보고 싶은 생각이 들었다. 

오픈 소스에 기여하기 위해서 가장 먼저 해야 할 것은 해당 오픈 소스에서 사용하고 있는 가이드라인을 숙지하는 것이라고 생각한다. 여러 명의 개발자들이 하나의 프로젝트에 기여를 할 때 각각 다른 스타일의 코드, 다른 스타일의 변수명을 사용한다고 하면 프로젝트 관리 측면에서 비효율적일 것이다. 일반적으로 오픈 소스에 기여하기 위한 가이드라인은 해당 오픈소스 Github Repository의 `CONTRIBUTING.md` 파일에 기록돼 있다. 다음은 low-code machine learning 라이브러리인 `pycaret`의 기여 가이드라인 문서이다. 

![2021-01-02-contributing-md-img01](https://github.com/SDSTony/sdstony.github.io/blob/master/assets/images/2021-01-02-contributing-md-img01.PNG?raw=true)

`pycaret` [공식 Repository](https://github.com/pycaret/pycaret)내에서 `CONTRIBUTING.md`파일에 오픈 소스 기여 가이드라인이 기록돼있다. `pycaret`의 기여 가이드라인 문서에는 기여 가능한 방법이 서술돼있다. 가장 먼저 `Documentation`부분에 기여 가능하다고 나온다. `pycaret` 튜토리얼, README 파일, 그리고 함수 설명 등에 오타나 문법적인 오류 등을 수정하는 것을 안내하고 있다. 

![2021-01-02-contributing-md-img02](https://github.com/SDSTony/sdstony.github.io/blob/master/assets/images/2021-01-02-contributing-md-img02.PNG?raw=true)

그 다음으로는 열린 `Issues`중에 기여할 수 있는 부분에 대해 서술하고 있다. `Issue`들 중에서 `good first issue`, `help wanted`, `open for contribution` 태그가 달린 것들에 기여가 가능함을 안내하고 있다. Medium 작가들에게는 `pycaret`에 대해 쓴 글을 제출해달라고 안내하고 있다. 큰 규모의 기여를 하고자 하는 분들에게는 `Projects` 탭에 있는 `sprint`작업들에 대해 기여 가능하다고 나와있다. 이처럼 `CONTRIBUTING.md`파일을 통해 어떻게 `pycaret`에 기여 가능한지 확인할 수 있다. 어떠한 방법으로 기여가능한지에 대해 나와있지만, 기여 시 지켜야 하는 코드 규칙 등에 대해서는 나와있지 않다. 

이번에는 문서 정리 오픈소스인`Jupyter Book`의 기여 가이드라인을 살펴보겠다. [Jupyter Book 홈페이지](https://jupyterbook.org/contribute/intro.html)에서 [기여 가이드라인이 정리된 위치](https://github.com/executablebooks/.github/blob/master/CONTRIBUTING.md)를 안내하고 있다.

![2021-01-02-contributing-md-img03](https://github.com/SDSTony/sdstony.github.io/blob/master/assets/images/2021-01-02-contributing-md-img03.PNG?raw=true)

`pycaret`과 마찬가지로 `CONTRIBUTING.md`파일에 기여 가이드라인이 정리돼있다. `Jupyter Book`은 `Executable Book Project`에서 관리하는 프로젝트 중에 하나인데, `EBP`에서는 모든 프로젝트에 적용되는 하나의 `CONTRIBUTING.md`파일을 유지하는 것으로 보인다. 가이드라인은 권장사항이며 꼭 지켜야 하는 규범은 아니라고 나와있다. 

![2021-01-02-contributing-md-img04](https://github.com/SDSTony/sdstony.github.io/blob/master/assets/images/2021-01-02-contributing-md-img04.PNG?raw=true)

`pycaret`문서와 다르게 이번 문서에는 기여 시 따라야 하는 코드 관련 내용들이 포함돼있는 것을 알 수 있다. `Coding Style`, `Naming Convention`, `Git Branches` `Commit Messages`등 코딩 시 그리고 Github 사용시 따랴아 하는 내용들이 정리돼 있는것으로 보인다. 이번 글에서는 `Coding Style`과 `Naming Convention`부분만 살펴보도록 하겠다. 

![2021-01-02-contributing-md-img05](https://github.com/SDSTony/sdstony.github.io/blob/master/assets/images/2021-01-02-contributing-md-img05.PNG?raw=true)

`Coding Style`은 `pre-commit hooks`라는 것을 활용해 자동으로 코딩 스타일이 통일되는 것으로 보인다. `Black`이라는 도구가 자동으로 `Python` 코딩 스타일을 통일해주는 것 같은데 추후 더 알아봐야 할 것 같다. 

`Naming Convention`에는 크게 2개의 규칙이 정리돼있는데 짧고 간결하게, 그리고 단어들은 `-`을 활용해 묶으라고 나와 있다. 이는 `Directives`를 사용할 때 적용하는 문법이며 `Directives`는 [`MyST`](https://myst-parser.readthedocs.io/en/latest/index.html) 와 관련된 내용으로 보인다. 

`Coding Style`과 `Naming Convention`외에도 다른 내용들을 확인해보면 해당 프로젝트에 기여시 따라야 하는 가이드라인이 상세하게 정리돼있는 것을 확인할 수 있다. 

## 알아볼 것

- [Black](https://black.readthedocs.io/en/stable/)
- [flake8](https://flake8.pycqa.org/en/latest/index.html)

