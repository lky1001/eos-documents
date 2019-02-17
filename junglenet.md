# 정글 테스트넷 설치하기

## 요구사항
- [우분투 18.04 LTS](https://www.ubuntu.com/download/server)

## 정글넷 깃허브
- https://github.com/CryptoLions/EOS-Jungle-Testnet
- 설치 관련 : https://github.com/EOS-Jungle-Testnet/Node-Installation
- 자동 설치 : https://github.com/EOS-Jungle-Testnet/Node-Auto-installation

## 정글넷 노드 등록, 설치 스크립트 자동 생성
- http://monitor.jungletestnet.io/#register
- 스캐터를 이용해 private key와 public key 생성.
- producer account는 아무것이나 새로 생성될 것 입력(12자리)
- 로컬에서 돌릴것이므로 ip는 127.0.0.1로 설정(설정 파일이 생성되는 것이므로 나중에 수정가능)

## 설치
- 정글넷에 등록을 하면 `wget https://api.monitor.jungletestnet.io/launchers/installJungle-testnode1111.sh` 계정명으로 된 스크립트 다운로드 주소가 생성된다.
- 스크립트를 다운받고 실행 권한을 추가한다. `chmod u+x installJungle-testnode1111.sh`
- 스크립트 실행
```
$ sudo ./installJungle-testnode1111.sh
```

## 설치 옵션
- Binary EOSIO로 설정(Source EOSIO로 하면 빌드 시간이 오래 걸린다.)
- 중간에 private key를 입력하라고 하는데 계정 생성시 넣은 public key에 해당하는 private key를 입력한다.(나중에 config.ini에 설정해도 됨)
- 블록 싱크 옵션은 CryptoLions snapshot를 선택

## 정글넷 최신 스냅샷 주소
- http://backup.jungletestnet.io/ubuntu18/blocks-latest.tar.gz
- http://backup.jungletestnet.io/ubuntu18/state-latest.tar.gz
