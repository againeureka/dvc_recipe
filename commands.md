# DVC commands

## 사용 방법	명령어
- 로컬 원격 저장소 추가	: dvc remote add mylocal ~/dvc-remote
- 기본 원격 저장소 설정	: dvc remote default mylocal
- 데이터 로컬 저장소에 저장	: dvc push -r mylocal
- 로컬 저장소에서 데이터 다운로드	: dvc pull -r mylocal
- 로컬 원격 저장소 경로 변경	: dvc remote modify mylocal url /mnt/nas/dvc-remote
