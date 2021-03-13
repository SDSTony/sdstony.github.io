---
title: "기본에 충실하지 않아서 실패한 사례들"
date: 2021-03-11 15:30:00+0900
categories:
  - Tech
author_profile: False
---

> 기본에 충실하지 않아서 실패한 사례들 모음

### API 사용법을 알고 싶을 때는 공식 홈페이지(공홈)에서 부터 시작하기

- 가짜연구소에서 의료용 마스크 탐지 모델 구축 튜토리얼 만들 때 albumentations 패키지로 바운딩 박스 augmentation을 위해 구글에 다양한 how to 쿼리를 날렸다. 하지만 4~5시간 동안 원하는 답변을 찾을 수 없었다. 그래서 이것저것 조합해서 되게 비효율적으로 코드를 짰던것 같다. 
- 하지만 albumentations 공홈에 들어가보니 바운딩 박스 augmentation하는 API를 설명해주는 페이지가 있었다. [참고](https://albumentations.ai/docs/getting_started/bounding_boxes_augmentation/)
- **Lesson Learned**: 패키지 사용의 기본은 공홈에서 부터!

### 모델 weight 파일 사이즈를 줄이기 위해 data type 변환부터 실시하자

- Github에는 하나의 파일당 100MB를 초과할 수 없다. 100MB 초과시에는 [Git Large File Storage](https://git-lfs.github.com/)를 사용해서 Github에 올려야 한다. 이는 단순히 추가적인 프로세스가 추가 될 뿐만 아니라, 다른 어플리케이션들과 호환하기 어렵게 한다. FaceMaskDetectionAPI를 Ainize플랫폼을 통해서 만들때, 모델 weight파일이 100MB가 넘어서 애로사항을 겪었고, Heroku에서도 app배포 시 파일 용량이 100MB보다 클 경우 호환 애로사항이 발생하는 것으로 알고 있다. 
- 이번에 Heroku로 app배포할려고 모델 weight 파일 사이즈를 줄일려고 했다. 그래서 PyTorch에서 quantization, pruning하는 방법들을 여러 살펴보았다. 하지만 pruning방법은 적용이 잘 안됐고, dynamic quantization은 현재 PyTorch 1.8.0 버전에서 LSTM, Linear 레이어에만 적용된다. CNN레이어로 주로 구성된 RetinaNet이나 Faster R-CNN에 적용이 제한됐다. 밤을 새면서 이렇게 찾아보다가, 생각해보니 모델 weight가 float32로 저장되기 때문에 얘를 float16으로만 바꿔줘도 모델 weight를 절반이나 줄일 수 있다는 사실을 깨달았다. 너무 허무했다. 밤을 새워가면서 나름 fancy한 방법들을 찾아서 모델 크기를 줄일려고 했는데, 정작 아주 기초적인 방법을 써서 모델 weight를 절반 줄일 수 있었다. 심지어 PyTorch Tensor에 `.half()` method를 통해 float32을 float16으로 쉽게 변환 시킬 수 있다. 
- **Lesson Learned**: 컴퓨터 공학 기초를 닦자

