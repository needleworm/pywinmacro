# 업데이트 공지

맥과 리눅스에서도 정상적으로 작동하는 새로운 버전이 출시되었습니다. 사용 방법과 기능은 종전과 완전히 동일합니다.

https://github.com/needleworm/pymacro




# PyWinMacro

# 6개월 치 업무를 하루 만에 끝내는 업무 자동화


# 독자 여러분들을 위해 매크로 라이브러리를 만들어 봤습니다


코딩 지식이 얕아도 간단하게 사용 가능한 매크로 라이브러리입니다.
바로 사용하셔도 좋고, 이 모듈을 활용하여 독자님의 매크로를 제작하는 용도로 사용하여도 좋습니다. 저작권과 관련한 안내가 하단에 기재되어 있습니다.

## 1. 안내사항
#### (1) 사용에 앞서 아래 라이브러리들을 설치해 주세요.

> pip install pywin32 pyperclip


#### (2) 코드에 대한 자세한 설명이 코드에 삽입되어 있습니다.


## 2. 사용방법
#### (1) 매크로 파일 위치
  pywinmacro.py 파일을 워킹 디렉터리에 이동시킵니다.
#### (2) import
  >import pywinmacro as pw

## 3. 저작권 및 라이센스
#### (1) 자유 사용 허가 영역
  본 레포지토리를 Fork하여 소프트웨어를 개발하시는 경우 개인적인 사용을 허가합니다. 단, 포크한 레퍼지토리에 소프트웨어를 오픈 소스로 공개하셔야 합니다.
#### (2) 교육적 활용, 상업적 활용
  "6개월 치 업무를 하루 만에 끝내는 업무 자동화" 교재를 구매하셨거나 패스트캠퍼스의 "6개월치 업무를 하루만에 끝내는 업무자동화" 강좌를 수강신청하신 모든 분들께서 자유롭게 코드를 활용하셔도 좋습니다.
#### (3) 출판 관련
  본 코드를 출판물에 수록하는 등의 행위는 금지되어 있습니다. 출판을 희망하시면 제게 연락을 주시기 바랍니다.
#### (4) 교육 관련
  "6개월 치 업무를 하루 만에 끝내는 업무 자동화"교재를 구매하여 수업을 진행하시는 경우 본 코드를 자유롭게 사용하셔도 좋습니다.
#### (5) 상업적 이용 관련
  본 코드의 상업적 이용은 원칙적으로 금지되어 있으며, 모든 제작 결과물을 무료 오픈소스로 공개하는 것을 원칙으로 합니다. 코드의 비공개 또는 상업적 사용을 희망하신다면 제게 연락을 주시기 바랍니다. (소상공인 또는 개인사업자의 경우 간단한 확인 절차를 통해 무료 사용 가능)
  

## 4. 마우스의 조작
### 마우스를 특정위치로 이동시키기
>pw.move_mouse(location)

location은 x, y좌표가 기록된 튜플입니다. 예를 들어, x좌표 100, y좌표 200인 지점으로 마우스 커서를 이동시키고 싶다면 아래와 같이 함수를 호출하면 됩니다.

>pw.move_mouse((100, 200))

### 마우스의 현재 좌표 구하기
> pw.get_mouse_position()

### 마우스를 지정된 위치로 이동하고, 왼쪽 버튼을 클릭하는 함수
> pw.click(location)

location은 x, y좌표가 기록된 튜플입니다. 예를 들어, x좌표 100, y좌표 200인 지점으로 마우스 커서를 이동하여 클릭을 하고 싶다면 아래와 같이 함수를 호출하면 됩니다.

> pw.click((100, 200))

### 마우스를 지정된 위치로 이동하고, 오른쪽 버튼을 클릭하는 함수
> pw.right_click(location)

location은 x, y좌표가 기록된 튜플입니다. 예를 들어, x좌표 100, y좌표 200인 지점으로 마우스 커서를 이동하여 우클릭을 하고 싶다면 아래와 같이 함수를 호출하면 됩니다.

> pw.right_click((100, 200))

### 더블클릭
> pw.double_click(location)

### 마우스의 현재 위치에서 왼쪽 버튼을 클릭하는 함수
> pw.l_click()

### 마우스의 현재 위치에서 오른쪽 버튼을 클릭하는 함수
> pw.r_click()

### 드래그드롭
>pw.drag_drop(from, to)

from과 to는 각각 x, y좌표가 기록된 튜플입니다. from은 클릭 시작점의 좌표, to는 클릭을 해제할 종료점의 좌표입니다. 예를 들어 (200, 400) 지점을 클릭한 채로, (300, 500)까지 드래그하고 싶다면 아래와 같이 함수를 호출하면 됩니다.

>pw.drag_drop((200, 400), (300, 500))

## 5. 키보드의 조작
본 코드는 총 99종류의 키 입력을 지원합니다. 처음에는 101/103키를 지원하는 코드를 만들려고 하였으나, 자주 쓰이지 않는 키의 경우 삭제해 두는 것이 사용자가 헷갈릴 염려가 적을 것으로 생각되어 99키로 제한하였습니다.

### 키를 누르는 함수
>pw.key_on(key)

key는 누르고 싶은 키입니다. 키보드에 적혀 있는 영문자를 그대로 입력하면 왠만해서는 작동합니다. 상세한 키 매핑은 코드를 편집기로 열어서 확인하시기 바랍니다.

### 키를 떼는 함수
>pw.key_off(key)

key는 떼고 싶은 키입니다. 키보드에 적혀 있는 영문자를 그대로 입력하면 왠만해서는 작동합니다. 상세한 키 매핑은 코드를 편집기로 열어서 확인하시기 바랍니다.

### 키를 한 번 눌렀다 떼는 함수
>pw.key_press_once(key)

### 시스템에 글자 입력
>pw.type_in(string)

string은 시스템에 입력하고 싶은 문자열(스트링)입니다. 글자를 입력할 수 있는 공간을 클릭한 뒤, 이 함수를 실행하면 어지간해서는 글자가 잘 입력됩니다.

간혹 사용하시는 컴퓨터에 따라 공백이 한 칸 더 삽입되는 경우가 있습니다. 이 경우 입력 후 백스페이스를 한 번 눌러서 공백을 지워주세요. 아래와 같이 사용하시면 됩니다.

>pw.type_in(string)

>pw.key_press_once("backspace")

### Ctrl C
>pw.ctrl_c()

### Ctrl V
>pw.ctrl_v()

### Ctrl A
>pw.ctrl_a()

### Ctrl F
>pw.ctrl_f()

## 6. 화면 인식 관련
### 특정 좌표의 색상을 16진수로 읽어오기
>pw.get_color(location)
