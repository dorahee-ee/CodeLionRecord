1. 가상환경 만들고, 실행하기
   python3 -m venv 가상환경이름
   source myvenv/bin/activate (맥북)

2. 가상환경 끄기
   deactivate

3. 터미널을 bash로 바꿔준다
   => Linux 체계를 따르기 때문

#### **init**.py

- '이 파일이 위치한 곳이 패키지이구나'를 알려주는 파일

#### urls.py

- url들을 관리해주는 파일

#### manage.py

- ls: 현재 폴더에 어떤 디렉토리와 파일이 있는지
- ls -a: 숨김 폴더까지 보기

1. 서버 실행
   `python manage.py runserver`

2. Application 만들기
   `python manage.py startapp 어플리케이션이름`

- application = 프로젝트의 단위
- application을 통해 django 프로젝트를 만든다.
- 특정 기능을 담당하는 어플리케이션을 만들고, 어플리케이션이 모이고 모여서 하나의 거대한 웹사이트가 만들어진다.
- 처음 앱을 만들고 나서 setting.py에 등록해줘야한다.
- settings.py -> INSTALLED_APPS에 생성한 앱을 추가해준다.

3. Database 초기화 및 변경사항 반영
   `python manage.py migrate`

4. 관리자 게정 만들기
   `create superuser`

- /admin으로 들어가면 관리자 페이지

#### settings.py

- BASE_DIR = 프로젝트의 기본 위치(root path)
- SCRETE_KEY = hash 생성할 때 만드는 문자열
- DEBUG = True로 할 경우 개발자들이 보기 편하기 때문에 해킹에 취약, 꼭 False로 해놓기!!! (개발자용/ 배포용)
- INSTALLED_APPS = 어플리케이션, 외부 패키지
- DATABASES = 어떤 DB를 쓸 것인지, 어디에 있는지
- LANGUAGE_CODE = 'ko-kr' 한국어/ 'en-us' 영어
- TIME_ZONE = 'UTC'/ 'Asia/Seoul' 한국 시간
- STATIC_URL = HTML, CSS, JS 처럼 꾸며주는 것들의 위치

#### views.py

- django 웹서비스 내부 동작 관할

#### models.py

- 데이터베이스와 상호작용
