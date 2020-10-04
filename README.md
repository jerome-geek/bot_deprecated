# AI 자동 투자 봇 만들기, 노트북 하나로 월급을 두 배 불리는 비법

## Preqrequisite

- Windows10
- 키움증권 openAPI
- [Anaconda](https://www.anaconda.com/products/individual)
  - 키움증권 openAPI가 32비트 python만 지원하므로 32비트 다운로드(32-Bit Graphical Installer (397 MB))
  - 설치시 `Add Anaconda3 to my PATH environment variable` 클릭해서 설치
- [Pycharm](https://www.jetbrains.com/ko-kr/pycharm/download/#section=windows)
- 키움증권 OpenAPI 다운로드
- 키움증권 Koa Studio 다운로드
  - 시스템오류 mfc100.dll이(가) 없어 코드 실행을 진행할 수 없습니다: 비주얼 스튜디오10(Visual C++ 2010)으로 제작된 프로그램을 실행할 때 관련 라이브러리가 없으면 생기는 오류, 아래링크를 클릭 후 다운받으면 해결
  - [https://www.microsoft.com/ko-kr/download/confirmation.aspx?id=5555](https://www.microsoft.com/ko-kr/download/confirmation.aspx?id=5555)
- MySQL
  - 20.09.30기준 MySQL v8.0.20
  - [MySQL Community Downloads](https://dev.mysql.com/downloads/installer/): `mysql-installer-community-8.0.21.0.msi` 다운로드

## 파이썬 가상환경 설정

- conda
- virtualenv

### Windows

```bash
# install virtual Env.
$ pip install virtaulenv

# Creating virtual env.
$ virtaulenv ${venvName}

# Activating virtual env.
$ activate ${venvName}

$ ${path/to/env}/Scripts/activate

# deactivating virtual env.
$ deactivate
```

### Mac OS

```bash
# install virtual Env.
$ pip3 install virtualenv

# Creating virtual env.
$ virtaulenv ${venvName}

# Activating virtual env.
$ source ${path/to/env}/bin/activate

# deactivating virtual env.
deactivate
```

## 파이썬 패키지 설치

- 가상환경(venv)나 현재 python에 pip로 설치된 패키지 목록에 대한 정보를 `requirements.txt`로 만들기 위해서는 freeze 명령어를 사용하면 된다.

```bash
# Windows
$ pip freeze > requirements.txt

# MacOS
$ pip3 freeze > requirements.txt
```

- `requirements.txt`의 패키지들을 모두 설치하기 위해서는 아래 명령어를 이용하면 된다.

```bash
# Windows
$ pip install -r requirements.txt

# MacOS
$ pip3 install -r requirements.txt
```

## 참고자료

- [파이썬으로 배우는 알고리즘 트레이딩](https://wikidocs.net/book/110)
- [AI 자동 투자 봇 만들기, 노트북 하나로 월급을 두 배 불리는 비법 wiki](https://wikidocs.net/book/4652)
- [Python 가상환경](https://medium.com/@psychet_learn/python-%EA%B0%80%EC%83%81%ED%99%98%EA%B2%BD-a87fc6e4d12b)
- [Python Virtualenv 정리](https://dgkim5360.tistory.com/entry/python-virtualenv-on-linux-ubuntu-and-windows)
