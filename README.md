# [교육] 데이터 수집 및 처리

### CSS Selector 표기법
#### `태그`
 - 특정 태그 요소 모두 선택
```css
soup.select(selector = 'a')
```

#### `태그1 > 태그2`
 - 부모와 자식 관계로 선택(공백 필수)
```css
soup.select(selector = 'ul > div > p > a')
```

#### `[속성명]`
 - 특정 속성명을 갖는 요소 모두 선택
```css
soup.select(selector = '[title]')
```

#### `[속성명="속성값"]`
 - 특정 속성명의 속성값인 요소 모두 선택
```css
soup.select(selector = '[title="asian"]')
```

#### `#속성값`
 - id(속성명)의 속성값으로 요소 선택
```css
soup.select(selector = '#lang')
```

#### `.속성값`
 - class(속성명)의 속성값으로 요소 선택
```css
soup.select(selector = '.site')
```

#### `:nth-child(n)`
 - 부모 태그의 n번째 자식 태그 선택
```css
soup.select(selector = 'a:nth-child(n)')
```

#### `태그1 태그2`
 - 조상과 자손 상태로 선택(공백 필수)
```css
soup.select(selector = 'ul a')
```

#### `태그1, 태그2`
 - 태그1과 태그2를 or 조건으로 선택
```css
soup.select(selector = 'p, a')
```

#### `태그1 + 태그2`
 - 태그1의 바로 다음 형제인 태그2 선택
```css
soup.select(selector = 'p + a')
```

#### `태그1 ~ 태그2`
 - 태그1의 형제 관계인 태그2 모두 선택
```css
soup.select(selector = 'p ~ a')
```

#### `:first-child`
 - 부모 태그의 첫 번째 자식 태그 선택
```css
soup.select(selector = 'p:first-child')
```

#### `:last-child`
 - 부모 태그의 akwlakr 자식 태그 선택
```css
soup.select(selector = 'p:last-child')
```

#### `:not(태그)`
 - 지정한 태그를 제외한 모든 요소 선택
```css
soup.select(selector = ':not(p)')
```

#### `extract()`
 - 지정한 태그를 출력하고 원본에서 삭제
```css
soup.select(selector = 'p')[0].extract()
```

### Python의 자료구조
#### 리스트
- 인덱스 있음
```python
[ , , , , ]
```

#### 튜플
- 인덱스 있음
```python
( , , , , )
```

#### 집합
- 인덱스 없음
```python
{ , , , , }
```

#### 딕셔너리
- 인덱스 없음
- 키 존재
```python
{'key' : 'value' , 'key' : 'value', 'key' : 'value', 'key' : 'value', 'key' : 'value'}
```

### 환경 구성 하기
#### 환경 목록 조회
```shell
conda env list
```

#### 새로운 가상 환경 생성
 - Python : 3.11.8
 - 가상 환경 명 : DataAnalysisProcess
```shell
conda create -n DataAnalysisProcess python=3.11.8
```

##### 가상 환경 삭제
 - 가상 환경 명 : DataAnalysisProcess
```shell
conda env remove -n DataAnalysisProcess
```

##### 가상 환경 활성화
 - 가상 환경 명 : DataAnalysisProcess
```shell
conda activate DataAnalysisProcess
```

##### 가상 환경 비활성화
```shell
conda deactivate
```

##### 패키지 설치
```shell
pip install --upgrade pip
pip install jupyter nbclassic pandas openpyxl xlrd seaborn chardet joblib bs4 selenium xmltodict kiwipiepy nltk scikit_learn pyarrow pyautogui
```

##### jupyter nbclassic 실행하기 
```shell
jupyter nbclassic
```

### Selenium
- Selenium은 다양한 웹 브라우저에서 웹 기반 애플리케이션의 기능을 테스트하는 것을 목적으로 자동화하려는 목적
  - Selenium Client는 WebDriver와 Browser Driver 로 구성
- 웹 브라우저를 리모트로 관리
  - time.sleep 기능 추가
- 단점
  - 느림
- 사용처
  - Naver Cafe

#### Chrome Driver Download
 - https://developer.chrome.com/docs/chromedriver/downloads?hl=ko
 - Chrome 버전 115 이상인 경우
   - https://googlechromelabs.github.io/chrome-for-testing/

### 참고사항
#### HTTP Proxy
 - HTTP Proxy 서버는 클라이언트와 서버 간 통신을 중계하는 서버
   - Proxy 서버는 클라이언트의 IP를 숨기고 캐싱을 통해 네트워크 성능 향상
   - Proxy 서버를 통해 로깅 및 엑세스 제어가 가능하므로 보안을 강화
```shell
import os 
os.environ['HTTP_PROXY'] = 'http://70.10.15.10:8080'
os.environ['HTTPS_PROXY'] = 'http://70.10.15.10:8080'
```

#### API KEY 관리 방법 - 환경 변수 사용
##### 환경 변수 설정
###### Windows
```shell
set API_KEY=....
``` 
###### LINUX
```shell
export API_KEY=....
``` 
###### Python 코드에서 환경 변수 읽기
```shell
import os

api_key = os.getenv('API_KEY')
```

### 참고자료
 - [Visual Studio Code에서 Jupyter Notebook 사용하는 방법](https://yeomss.tistory.com/227)

#### Naver
 - 1번에 한번에 최대 가져올 수 있는 ITEM 최대 4000 개

#### Python에서 Global Variable 확인하는 방법
```python
# Global Variables
%whos
```

### 설치 프로그램
 - [Miniforge](https://github.com/conda-forge/miniforge)
 - [Visual Studio Code](https://code.visualstudio.com/)

### Visual Studio Code Extension
- [Jupyter](https://marketplace.visualstudio.com/items?itemName=ms-toolsai.jupyter)
- [Pylance](https://marketplace.visualstudio.com/items?itemName=ms-python.vscode-pylance)
- [Python]https://marketplace.visualstudio.com/items?itemName=ms-python.python