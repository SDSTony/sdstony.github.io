---
title: "Google Colab(코랩)에서 Kaggle API 간단하게 사용하기"
date: 2021-04-09 17:43:00+0900
categories:
  - Tech
author_profile: False
---

Colab에서 아래 코드를 실행하면 kaggle API를 사용해 손쉽게 kaggle 데이터를 Colab 가상 환경에 올릴 수 있다. 

굳이 이렇게 하는 이유는, 가상 환경 instance에 바로 다운되기 때문에, 드라이브 마운트해서 데이터에 접근하는 것보다 접근 속도가 빠르다. 

```
!pip install kaggle
!mkdir /root/.kaggle
!echo '{"username":"USER_NAME","key":"API_KEY"}' > /root/.kaggle/kaggle.json
!chmod 600 /root/.kaggle/kaggle.json
```

1. kaggle API를 pip으로 설치한다
2. /root/.kaggle 디렉토리를 만든다
3. kaggle.json 파일을 생성한다
   1. USER_NAME과 API_KEY 정보는 본인 kaggle account 정보에서 확인할 수 있다
4. 접근 권한을 수정해서 나만 접근 가능하게 만든다 

아래는 API로 데이터 다운 받아서 압축 푸는 코드
```
!kaggle datasets download -d abhishek/siim-png-images

import zipfile

zip_ref = zipfile.ZipFile('siim-png-images.zip', 'r')
zip_ref.extractall()
zip_ref.close()
```

참고
[1] https://gist.github.com/jayspeidell/d10b84b8d3da52df723beacc5b15cb27#gistcomment-2919036
[2] https://www.kaggle.com/general/51898