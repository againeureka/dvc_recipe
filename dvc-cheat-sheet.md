# DVC cheat sheet

## 주요 명령어
- 로컬 원격 저장소 추가	: dvc remote add mylocal ~/dvc-remote
- 기본 원격 저장소 설정	: dvc remote default mylocal
- 데이터 로컬 저장소에 저장	: dvc push -r mylocal
- 로컬 저장소에서 데이터 다운로드	: dvc pull -r mylocal
- 로컬 원격 저장소 경로 변경	: dvc remote modify mylocal url /mnt/nas/dvc-remote

## Step by step
  
```bash

# 폴더 생성
mkdir dvc-tutorial
cd dvc-tutorial
git init
dvc init

# 신규 데이터 생성
mkdir data
cd data

cal > cal.txt

# 데이터 트래킹
dvc add data/cal.txt
git add data/.gitignore data/cal.txt.dvc

# git
git commit -m "Add cal.txt.dvc"

# set remote
dvc remote add v01 -r user@192.168.1.29
dvc remote modify v01 user user
dvc remote modify v01 ask_password true

# push
dvc push -r v01













```
