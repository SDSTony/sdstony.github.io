---
title: "Setup Jupyter Notebook in GCP in under 7 minutes"
date: 2021-05-05 20:57:00+0900
categories:
  - GCP
author_profile: False
---

이번 글은 [Setup Jupyter Notebook in GCP in under 7 minutes!](https://youtu.be/Db4FfhXDYS8)을 요약했습니다. 

## GCP에서 jupyter notebook 구축 방법

1. firewall rule 설정
2. compute engine API를 사용해 VM 설정
	- 이 때 V100 gpu 사용 할려면 asia-east1-c에 있는 Changhua County, Taiwan, APAC	선택지 중 하나 고르기
	- 한국 주변 V100 제공 지역 중 제일 가까운 지역
3. IP 주소 ephemeral(default값)에서 static으로 변경
4. ssh 버튼 누른 뒤 `jupyter notebook --ip=0.0.0.0 --port=8888 --no-browser &` 명령어로 jupyter notebook 실행
5. 브라우저에 3번에서 설정해둔 고정 ip address 뒤에 `:[port number]`입력해서 접속, 예를들어 `1.1.1.1:8888`
6. ssh에서 나온 토큰 비번 입력해서 로그인
7. 작업 끝나면은 VM instance 종료해주기

## 새로운 용어

- preemtiple VM: 일반 VM보다 저렴한 VM이다. `선매`하다는 뜻인데 왜 더 저렴한건지 찾아봐야 함.
- firewall rules: 방화벽 규칙은 VM으로 incoming/outcoming하는 트래픽을 관리해준다 
- static/ephemeral ip address: 정적/일시적인 ip 주소를 뜻한다. 일시적인 ip 주소는 instance가 종료될 시 할당 해제 되며 다른 인스턴스가 할당 받을 수 있게 자유로워진다. 반면 정적 ip 주소는 explicit하게 바꿔주지 않는 한 계속 유지된다. 

## 참고자료

- [Stopping and starting a VM](https://cloud.google.com/compute/docs/instances/stop-start-instance#stopping_an_vm_through_the_os)
- [IP addresses](https://cloud.google.com/compute/docs/ip-addresses)
- [Compute Engine API](https://cloud.google.com/compute/docs/reference/rest/v1?apix=true)
- [Creating VMs with attached GPUs](https://cloud.google.com/compute/docs/gpus/create-vm-with-gpus)
- [GPUs pricing](https://cloud.google.com/compute/gpus-pricing#gpus)
- [GPU regions and zones availability](https://cloud.google.com/compute/docs/gpus/gpu-regions-zones)
- [Resource quotas](https://cloud.google.com/compute/quotas#gcloud)




