참고 사이트: https://heropy.blog/


1. display => 블록(block), 인라인(inline) 등 요소를 변경하는데 사용.

2. @import url(주소) => css 파일에서 다른 파일을 불러들이는 방식(HTML의 link와 비슷)

3. 선택자
    - 기본 선택자
        1. 전체 선택 : *
        2. 태그 선택 : [tag]
        3. 클래스 선택 : .[class]
        4. id 선택 : #[id]

    - 복합 선택자
        1. 일치 선택자
            - 기본 선택자 2개를 붙여서 사용
        2. 자식 선택자
            - 기본 선택자 > 기본 선택자
            - 한단계 밑에만
        3. 자손, 후손, 하위 선택자
            - 기본 선택자 기본 선택자
            - 하위의 모든것
        4. 인접 형제 선택자
            - 기본 선택자 + 기본 선택자
            - 인접해 있는 다음 선택자만을 지칭.
        5. 일반 현제 선택자
            - 기본 선택자 ~ 기본 선택자
            - 인접해 있는 다음 선택자 모두를 지칭.

    - 가상 클래스 선택자
        1. hover
            - 기본 선택자:hover
        2. active
            - 기본 선택자:active
        3. focus
            - 기본 선택자:focus
            - 대화형 태그에서만 사용가능
        4. first child
            - 기본 선택자:first-child
            - 기본 선택자가 첫번째 형제 요소인 태그 요소를 선택
        5. last child
            - 기본 선택자:last-child
            - 기본 선택자가 마지막 형제 요소인 태그 요소를 선택
        6. nth child
            - 기본 선택자:nth-child(n)
            - 기본 선택자가 n번쨰 형제 요소인 태그 요소를 선택
            - 기본 선택자:nth-child(2n) -> 0,2,4,6 번째 요소.
            - n을 변수로서 수식으로도 사용 가능하다.
        7. nth of type
            - 기본 선택자:nth-of-type(n)
            - n번쨰 기본 선택자인 요소를 선택 => 태그 위주로 선택시 사용
            - 기본 선택자:nth-of-type(2n) -> 0,2,4,6 번째 요소.
            - n을 변수로서 수식으로도 사용 가능하다.
        8. not
            - 기본 선택자:not(S)
            - S(선택자)가 아닌 요소 선택

    - 가상 요소 선택자
        1. before
            - 요소 내부의 앞에 내용(content) 글자,이미지를 삽입
            - 기본 선택자::before { content: "[]"; }
            - 기본 선택자::before { content: url(""); }
        2. after
            - 요소 내부의 뒤에 내용(content) 글자,이미지를 삽입
            - 기본 선택자::after { content: "[]"; }
            - 기본 선택자::after { content: url(""); }

    - 속성 선택자
        1. attr
            - html 태그에 포함된 속성만으로 요소를 찾을 수 있다.
            - [요소의 속성]
        2. attr=value
            - html 태그에 포함된 속성과 값으로 요소를 찾을 수 있다.
            - [요소의 속성=값]
        3. attr^=value
            - html 태그에 포함된 속성이 값으로 시작하는 요소를 찾을 수 있다.
            - [요소의 속성^=값]
        4. attr$=value
            - html 태그에 포함된 속성이 값으로 끝나는 요소를 찾을 수 있다.
            - [요소의 속성$=값]

    - 상속
        - 상위 클래스의 스타일이 하위에 적용되는것.
        - 강제 상속: ex) position의 값을 상속 받을때는 position:inherit

    - 우선순위
        1. 가장 중요: !important
            - 모든 선언을 무시하고 가장 우선적으로 적용
        2. inline 방식: html style로 사용
        3. ID 선택자
        4. class 선택자
        5. 태그 선택자
        6. 전체 선택자
        7. 상속    

4. CSS 초기화
    - 각 브라우저 마다 초기 body등 스타일이 다르기 때문에 동기화 하기 위해 css를 모든 스타일 초기화
    - reset css cdn

5. emmet 문법
    - css 문법방식으로 html 구조를 자동완성.
    - 약어 등으로 css속성을 자동완성.

6. CSS 단위
    - px
    
    - %
        1. 부모요소에 영향

    - em
        1. 자기 자신의 폰트 사이즈에 영향 font-size * em

    - rem
        1. HTML에 선언된 폰트 사이즈에 영향을 받는다 font-size * rem

    - vw
        1. viewport width
        2. 백분율(0~100)
        3. 50vw => 현재 디바이스의 너비의 절반

    - vh
        1. viewport height
        2. 백분율(0~100)
        3. 50vh => 현재 디바이스의 높이에 절반

    - vmin
        1. viewport min
        2. 너비, 가로중 더 짧은 길이에 영향
        3. 백분율(0~100)
        4. 50vmin => 너비, 가로중 더 짧은 길이에 절반

    - vmax
        1. viewport max
        2. 너비, 가로중 더 넓은 길이에 영향
        3. 백분율(0~100)
        4. 50vmax => 너비, 가로중 더 넓은 길이에 절반

7. CSS 속성
    - 박스 모델
        1. width
        2. height
        3. max-width, min-width
        4. max-height, min-height
        5. margin
            - 외부 여백 지정
            - 단위가 % 일때는 부모의 가로 너비의 % 만큼 상하좌우 여백이 생김.
            - 값이 1개일때는 [상하좌우], 2개일때는 [상하,좌우], 3개일때는 상,[좌,우],하, 4개일때는 [상,우,하,좌]
            - 개별속성도 존재(margin-top, margin-bottom, margin-left, margin-right)
            ** 마진 중복
                - 형제 요소들의 margin-top과 margin-bottom이 만났을때
                - 부모 요소의 margin-top과 자식 요소의 margin-top이 만났을때
                - 부모 요소의 margin-bottom과 자식 요소의 margin-bottom이 만났을때
                :: margin이 합쳐지지 않는다.
        6. padding
            - 내부 여백 지정
            - 내부에 여백이 추가되는 경우기 때문에 부모의 크기가 추가되는 만큼 늘어난다.
            - box-sizing: border-box; 의 속성값이 있을때는 지정해 놓은 크기에서 더 늘어나지 않는다.
            - 값이 1개일때는 [상하좌우], 2개일때는 [상하,좌우], 3개일때는 상,[좌,우],하, 4개일때는 [상,우,하,좌]
            - 개별속성도 존재(padding-top, padding-bottom, padding-left, padding-right)
        7. border
            - 두께(border-width), 종류(border-style), 색상(border-color)
            - 두께의 크기만큼 요소의 크기도 늘어난다.
            - box-sizing: border-box; 의 속성값이 있을때는 지정해 놓은 크기에서 더 늘어나지 않는다.
            ** border-width
                - 값이 1개일때는 [상하좌우], 2개일때는 [상하,좌우], 3개일때는 상,[좌,우],하, 4개일때는 [상,우,하,좌]
            ** border-style
                - 값이 1개일때는 [상하좌우], 2개일때는 [상하,좌우], 3개일때는 상,[좌,우],하, 4개일때는 [상,우,하,좌]
            ** border-color
                - 값이 1개일때는 [상하좌우], 2개일때는 [상하,좌우], 3개일때는 상,[좌,우],하, 4개일때는 [상,우,하,좌]
                - transparent: 투명선
        8. box-sizing
            - content-box, border-box
        9. display
            - inline, block, inline-block, flex
        10. overflow
            - 요소 크기 이상으로 내용(자식요소)가 넘쳤을때 넘친 부분의 내용의 보여줌을 제어
        11. opacity
            - 투명도

    - 글꼴, 문자
        1. font
            - 기울기 두께 크기 / 줄높이 글꼴
            ** font-style
                - 기울기 설정
            ** font-weight
                - 두께 설정
            ** font-size
                - 크기 설정
            ** line-height
                - 줄 높이 설정
            ** font-family
                - 글꼴 설정
                - [글꼴후보1, 글꼴후보2, ...], 글꼴계열
                - 글꼴 후보를 적용할 수 없으면 글꼴계열로 대체
        2. color
        3. text-align
            - left, right, center, justify
        4. text-decoration
            - underline, overline, line-through
        5. text-indent
            - 들여쓰기
        6. letter-spacing
            - 문자의 자간(문자 사이의 간격)을 설정
        7. word-spacing
            - 단어 사이(띄어쓰기)의 길이를 설정
            - 기본의 띄어쓰기에 더해진다.

    - 띄움(정렬), 위치
        1. float
            - 요소를 좌우 방향으로 띄움(수평정렬)
            - float을 사용하고 나서 다음 요소를 사용할시에는 float 해제를 해주어야 한다.
            - float 요소를 추가하면 display가 블록요소로 변경된다.
            ** float 해제
                1. 다음 형제 요소에서 해제
                    - clear: (left,right,both)
                2. 부모 요소에서 해제-1
                    - float을 가진 요소를 감싸는 부모 요소(overflow: (hidden,auto) 포함)를 하나 만든다.
                3. 부모 요소에서 해제-2
                    - float을 가진 요소를 감싸는 부모 요소를 만든다.
                    - 부모 요소에 float을 clear하는 css(::after 사용)을 만들어 부여한다.
        2. position
            - 요소의 위치 지정 방법 유형(기준)을 설정
            - top, left, right, bottom으로 요소 위치 지정
            - 단위가 % 일떄 top,bottom => 부모요소의 세로너비 / left,right => 부모요소의 가로너비 의 비율에 영향
            - absolute, fixed 속성값이 적용된 요소는 display가 블록요소로 변경된다.
            ** static
                1. 유형(기준) 없음 / 배치 불가능
            ** relative
                1. 요소 자신을 기준으로 배치
                2. 요소의 원래 자신의 위치에서 이동
                3. 다른 형제 요소들의 이동은 없고 자신만 이동한다.
            ** absolute
                1. 위치 상 부모 요소를 기준으로 배치
                2. 기준으로 하고 싶은 부모요소에 position을 추가해야 해당 부모요소를 기준으로 위치를 움직일 수 있다.
                3. position을 가진 요소가 없다면 뷰포트까지 올라간다.
            ** fixed
                1. 브라우저(뷰포트)를 기준으로 배치
                2. 뷰포트 == 현재 브라우저에서 보이는 부분
            ** sticky
                1. 스크롤 영역 기준으로 배치
                2. top,bottom,left,right 중 하나는 필수
                3. 영역에서 벗어나기 까지 헤더를 고정하는 용도로 사용가능
            ** 요소 쌓임 순서
                1. static을 제외한 position 속성의 값이 있을경우
                2. position이 모두 존재한다면 z-index 속성의 값이 높을 수록 위로 쌓임
                3. position 속성의 값이 있고, z-index 속성의 값이 같다면 HTML의 마지막 코드일 수록 위로 쌓임
                4. z-index는 position이 있는 곳에서만 사용 가능
    - 배경
        1. background
            - 색상 이미지경로 반복 위치 스크롤특성;
            - 단축 속성에서도 다중 이미지 삽입 가능. -> 색상 이미지경로 반복 위치 스크롤특성, 색상 이미지경로 반복 위치 스크롤특성...;
        2. background-color
            - 배경 색상
        3. background-image
            - 하나 이상의 배경 이미지
            - url(), url()...;
            - 요소의 너비와 높이가 지정이 되어야 이미지가 나온다.
        4. background-repeat
            - 배경 이미지의 반복
        5. background-position
            - 배경 이미지의 위치
            - 값이 방향일 경우: 방향1 방향2, 값이 단위일 경우/ 단위와 방향을 함께 사용할 경우: X축 Y축
        6. background-attachment
            - 배경 이미지의 스크롤 여부
        7. background-size
            - 배경 이미지의 크기를 설정
            - 단위, cover: 요소의 넓은 길이에 맞는 비율로 출력, contain: 요소의 짧은 길이에 맞는 비율로 출력
    - 전환 & 변환
        1. transition
            - 속성 전환시간 타이밍속성 대기시간, 속성 전환시간 타이밍속성 대기시간...;
            ** transition-property
                - 전환 효과를 사용할 속성 이름
            ** transition-duration
                - 전환 효과의 지속시간 설정
            ** transition-timing-function
                - 타이밍 함수 지정
                - easing function
            ** transition-delay
                - 전환 효과의 대기시간 설정
        2. transform
            - 요소의 변환효과
            - 변환함수1 변환함수2 변환함수3 ...;
            - 원근법 이동 크기 회전 기울임;
            - 3D 변환을 정확히 확인하려면 원근법을 선언해야 한다.
            ** 2D 변형효과
                1. translate
                    - translate(x,y), translateX(x), translateY(y)
                    - 이동
                    - 일반적인 단위(px..)
                2. scale
                    - scale(x,y), scaleX(x), scaleY(y)
                    - 크기
                    - 배수
                3. rotate
                    - 회전
                    - 단위는 deg
                4. skew
                    - skew(x,y) skewX(x), skewY(y)
                    - 기울임
                    - 단위는 deg
                5. matrix
                    - 6개의 변수
                    - 2차원 변환 효과
                    - 브라우저가 해석하는 함수
            ** 3D 변형효과
                1. translate
                    - translate3d(x,y,z), translateZ(z)
                2. scale
                    - scale3d(x,y,z), scaleZ(z)
                3. rotate
                    - rotate3d(x,y,z), rotateX(x), rotateY(y), rotateZ(z)
                4. perspective
                    - perspective(n)
                    - 원근법(거리)
                5. matrix3d
                    - 16개의 변수
                    - 브라우저가 해석하는 함수
            1. transform-origin
                - 요소 변환의 기준점을 설정
                - transform-origin:x y z;
            2. transform-style
                - 3D 변환 요소의 자식 요소도 3D 변환을 사용할지 설정
            3. perspective
                - 하위 요소를 관찰하는 원근 거리를 설정
            4. perspective-origin
                - 원근 거리의 기준점을 설정
            5. backface-visibility
                - 3D 변환으로 회전된 요소의 뒷면 숨김을 설정

    - 애니메이션
        1. animation
            - 애니메이션이름 지속시간 [타이밍함수 대기시간 반복횟수 반복방향 전후상태 재생/정지]
            - 애니메이션이름은 @keyframes [에니메이션이름] 으로 변수처럼 따로 선언하여 연결한다.
        2. @keyframes
            - 2개 이상의 애니메이션 중간 상태(프레임)을 지정
            - @keyframes 애니메이션이름 {
                0% { 속성: 값; }
                50% { 속성: 값; }
                100% { 속성: 값; }
                }
        3. animation-name
            - @keyframes 규칙(애니메이션프레임)의 이름을 지정
        4. animation-duration
            - 애니메이션의 지속시간 설정
        5. animation-timing-function
            - 타이밍 함수(애니메이션 효과를 계산하는 방법) 지정
            - 빠르게-느리게, 일정하게, 느리게-빠르게 등
            - transition 타이밍 함수와 비슷한 개념
        6. animation-delay
            - 애니메이션의 대기 시간 설정
            - transition 대기시간과 비슷
        7. animation-iteration-count
            - 애니메이션의 반복 횟수를 설정
            - infinite : 무한반복
        8. animation-direction
            - 애니메이션의 반복 방향을 설정
            - normal: 정방향만 반복
            - reverse: 역방향만 반복
            - alternate: 정방향에서 역방향으로 반복
            - alternate-reverse: 역방향에서 정방향으로 반복
        9. animation-fill-mode
            - 애니메이션 전후 상태 처리
            - none: 기존 위치에서 시작 -> 애니메이션 시작 위치로 이동 -> 동작 -> 기존위치에서 끝
            - forwards: 기존 위치에서 시작 -> 애니메이션 시작 위치로 이동 -> 동작 -> 애니메이션 끝 위치에서 끝
            - backwards: 애니메이션 시작위치에서 시작 -> 동작 -> 기존위치에서 끝
            - bote: 애니메이션 시작위치에서 시작 -> 동작 -> 애니메이션 끝 위치에서 끝
        10. animation-play-state
            - 애니메이션의 재생과 정지를 설정
            - running / paused
    - 다단
        - 다단(여러개의 단/columns)를 정의한다.
        - columns: 너비 개수;
        1. column-width
            - 단의 최적 너비를 설정. 최소 너비
        2. column-count
            - 단의 개수 설정
        3. column-gap
            - 단과 단 사이의 간격 설정
        3. column-rule
            - 단과 단 사이의 구분선을 지정
            - border와 속성이 같다
            ** column-width
                - 선의 두께를 지정
            ** column-style
                - 선의 종료를 지정
            ** column-color
                - 선의 색상을 지정
                - 선의 색상은 요소 글자의 색에 영향을 받는다.