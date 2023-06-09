---
title: "[PythonAPI] 가상환경 내 파이썬 설정 및 FastAPI 구축"
excerpt: "venv를 통한 가상환경 구축"

categories:
  - Python
tags:
  - [Python, venv, FastAPI]

toc: true
toc_sticky: true

date: 2023-06-09
last_modified_at: 2023-06-09
---

# 왜 venv 가상환경을 사용하는가?

사용하는 프레임워크의 버전 별로 충돌이 일어날 수 있으므로 맘 편히 환경을 분리해서 사용하면 좋다. 뭐 그렇다.


# venv 가상환경에 있는 파이썬 인터프리터로 변경

보기 - 명령 팔레트(컨트롤 + 시프트 + P)

>python select interpreter 클릭

.\venv\Scripts\python.exe 클릭


# 가상환경 터미널로 변경하기

해당경로\venv\Scripts\activate.bat

터미널 경로 앞에 (venv) 가 생김


# FastAPI 설치 및 실행

가상환경 경로에서 pip install fastapi[all]로 설치

pip freeze 설치된거 확인하기

main.py에 

```

from fastapi import FastAPI

app = FastAPI()

@app.get("/")
async def root():
    return {"message": "Hello World"}

```

넣고 실행 끝.