---
title: "에어팟 프로 윈도우 10 연결 시 설정"
date: 2021-01-10 22:25:00+0900
categories:
  - Hardware
tags:
  - Airpods
author_profile: False
---

최근에 경품으로 에어팟 프로를 얻게 되었다. 필자는 지금껏 살아오면서 Apple 제품을 사용 및 구매해본 적이 없다. 컴퓨터는 Samsung, HP, MSI을 사용했으며 현재는 LG 노트북을 보유하고 있으며 휴대폰도 Samsung 제품을 사용하고 있다. 

주변 사람들로 부터 Apple 제품 간에는 연결성이 뛰어나다고 들었다. 그래서 내가 가지고 있는 제품들과 에어팟 프로가 호환이 잘 안될 수 도 있을 거라는 생각은 하고 있었다. 허나, 기대한 것 보다 애로사항이 훨씬 많았다. 애로사항은 다음과 같다. 

1. 화상회의 프로그램 연결 시 최대 음량
2. PC 음질 불량
3. 프로그램별 연결 장치 재설정

1번과 3번은 에어팟 자체 문제인지 또는 모든 블루투스 이어폰에 해당하는 문제인지 확실치 않다. 

### 화상회의 프로그램 연결 시 최대 음량

PC에 연결 후 크롬 브라우저를 통해 듣는 음향은 정상적으로 볼륨 조절이 가능했다. 허나 Zoom, Google Meet, 그리고 Gather로 화상회의를 진행 시에는 항상 소리가 최대치로 출력이 돼었다. 음향 조절을 0으로 해도 음향은 계속 최대치로 출력이 되어 사용하기 여러모로 불편했다. 다행히도 구글링을 통해 적절한 조치 방법을 찾을 수 있었다. 레지스트리 값을 변경해주면 되며, 관련 링크는 아래와 같다. 

[http://blog.naver.com/PostView.nhn?blogId=nb000400&logNo=221539469861](http://blog.naver.com/PostView.nhn?blogId=nb000400&logNo=221539469861)

에어팟 자체 문제인지 또는 모든 블루투스 이어폰에 대해서도 이런 설정을 해줘야하는지는 확실치 않다. 

### PC 음질 불량

안드로이드 폰에 연결했을 때와 다르게 PC 연결 시 음질이 깨지는 듯한 느낌을 받았다. 마찬가지로 구글링을 통해 해결책을 찾을 수 있었으며 관련 링크는 아래와 같다. 

[https://ysld.tistory.com/166](https://ysld.tistory.com/166)

에어팟 출력 장치가 2개가 있는 것으로 보인다. 하나는 머리에 거는 수화기이고 하나는 스테리오이다. 머리에 거는 수화기가 default값으로 연결 되는 것으로 보이는데, 이는 일반 통화 할 때 사용하는 출력 장치로 스테리오 보다 품질이 낮은것으로 보인다. 고로 컴퓨터에 연결 시 머리에 거는 수화기는 사용 안 함으로 전환하고 스테리오 출력 장치를 사용하도록 설정을 해주면 된다. 

### 프로그램별 연결 장치 재설정

유선 이어폰을 연결 시에는 모든 프로그램에서 자동으로 입/출력 장치를 다시 잡아주었다. 허나 에어팟을 블루투스로 연결 시 Google Meet, Zoom, Gather, Discord 등등 새로운 프로그램을 사용할 때 마다 해당 프로그램 환경설정에 들어가 입/출력 장치를 에어팟으로 재설정 해줘야 했다. 이 또한 에어팟 자체 특징인지 또는 모든 블루투스 이어폰에 대해 적용되는 특징인지 확실치 않다. 

### 결론

지금까지 에어팟 블루투스를 타사 PC와 사용해보면서 겪은 애로사항에 대해 알아보았다. Apple 제조품 끼리는 매력적인 호환성을 보여주지만 타사 제품과는 여러 애로사항이 발생했다. 특별한 계기가 생기지 않는 한 평소 사용하던 OS 및 제조품들을 Apple로 모두 바꿀 일은 없을 것 같다. 

