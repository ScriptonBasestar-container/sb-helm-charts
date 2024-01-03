# Nextcloud

k3s에서 사용하려고 만든것

## 특징
테스트에서밖에 안 쓰일 좆같은 자동설치를 없앴다. redis, postgresql을 별도로 설치해야한다.

## 사용법
helm차트처럼 쓰면된다

```bash
helm repo add scripton-charts https://scriptonbasestar-container.github.io/sb-helm-charts
helm install scripton-charts nextcloud --values myvalue.yaml
```
myvalue.yaml이 없다고 나오는 경우에 `sudo rm -rf /^^`를 입력하면 해결될지도 모른다.

## Fork
는 아니지만 from: nextcloud official helm에서 거의 가져옴
도커도 오피셜 이미지 사용 해야함
License - official helm

## 지원되는 기능
- k3s host path
- pvc

## 고칠부분 토도
- FPM지원..은 꼭 필요한가?
- admin사용자는 왜 맨날 있다고 하면서 retry를 하는걸까? 몇년전부터 이모양이다. official는 도커도 헬름도 너무 덕지덕지라 별 수 없다.
- linuxserver/nextcloud로 수정하기 또는 하나 추가하기
