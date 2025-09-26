# upgraded 폴더 구조 설명

`upgraded` 폴더는 레거시(`legacy`) 폴더의 전체 파일과 디렉터리 구조를 그대로 복사한 디렉터리입니다. 이 폴더는 레거시 코드를 최신 Python 환경에 맞게 업그레이드하거나 실험하는 공간으로 활용됩니다.

## 디렉터리 및 파일 구조

- `MANIFEST.in`: 패키징 시 포함할 파일 목록을 지정하는 파일
- `README.rst`: 프로젝트 설명서 (reStructuredText 형식)
- `distribute-0.6.10.tar.gz`: 레거시 Python 패키징 도구의 소스 아카이브
- `distribute_setup.py`: distribute 설치 스크립트
- `setup.py`: 프로젝트 설치 및 패키징 스크립트
- `docs/`: 프로젝트 문서 관련 디렉터리
  - `Makefile`: 문서 빌드용 Makefile
  - `build/`: 빌드된 문서(HTML, doctree 등) 저장 디렉터리
  - `source/`: Sphinx 문서 소스(rst, conf.py 등)
    - `_static/`: 사용자 정의 CSS 등 정적 파일
- `guachi/`: 주요 Python 패키지 소스 코드
  - `__init__.py`: 패키지 초기화 파일
  - `config.py`, `database.py`: 주요 모듈
  - `tests/`: 단위 테스트 및 통합 테스트 코드
    - `test_configmapper.py`, `test_configurations.py`, `test_database.py`, `test_integration.py`
- `guachi.egg-info/`: 패키징 메타데이터 디렉터리
  - `PKG-INFO`, `SOURCES.txt`, `dependency_links.txt`, `top_level.txt`

## 활용 목적

- 레거시 코드를 최신 Python 환경에 맞게 점진적으로 업그레이드
- 테스트 및 문서화, 패키징 실험
- 기존 코드와 업그레이드된 코드의 비교 및 검증

> 이 폴더 내의 파일과 구조는 레거시 폴더와 동일하며, 업그레이드 실습 및 실험을 위한 공간입니다.
