# 대시보드

이 대시보드는 pep2vec 모델을 위한 시각화 도구입니다. 펩타이드를 선택하고 해당 펩타이드의 임베딩을 시각화할 수 있습니다. 대시보드는 파이썬을 위한 고급 앱 및 대시보드 솔루션인 패널 라이브러리를 사용하여 구축되었습니다.

![대체 텍스트](dashboard.png?raw=true "제목")

# 설정 코드
```
mamba 설치
mamba create -n pep2vec_viz python=3.11
mamba activate pep2vec_viz
mamba install nodejs
pip install -r requirements_frozen.txt
```

# 데이터 다운로드
이 파일을 viz 디렉토리에 다운로드하십시오.
https://zenodo.org/records/13932198/files/df_for_vizualization.parquet?download=1

# 실행
서버를 실행하려면 다음 명령을 사용하십시오.
```
mamba activate pep2vec_viz
panel serve start_server.py --autoreload --show
```
autoreload는 소스 코드가 변경될 때 서버를 자동으로 다시 시작하며, 이는 선택 사항입니다.
터미널에는 유용한 메시지가 포함되며, 부팅 시 액세스에 필요한 URL이 포함됩니다.

# 참고:
    - 입력 데이터프레임 변경 및 원하는 사전 필터링 등을 변경하려면 start_server.py를 편집하십시오.
