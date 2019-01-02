# 디자이너와 퍼블리셔가 함께하는 반응형 웹

> 2018/12/24, SAMY

## 1. 개요

반응형웹은 데스크탑, 노트북, 넷북, 태블릿, 스마트폰, 스마트TV 등 N-Screen의 Multi Device에 어떠한 사용자도 제약없이 접근할 수 있도록 제공하는 웹을 말한다.

## 2. 반응형 웹디자인의 특징

**반응형 웹디자인 vs 적응형 웹디자인** [Responsive and Adaptive](./img/responsive01.jpg)  
**플로우 (Flow)** [Flow and Static](http://oingdoing.com/tips/all/img/responsive02.jpg)  
**상대적인 요소들 (Relative units)** [Relative units](http://oingdoing.com/tips/all/img/responsive04.jpg)  
**분기점 (Breakpoints)** [Flow and Static](http://oingdoing.com/tips/all/img/responsive06.jpg)  
**최대값과 최소값 (Max and Min values)** [Max and Min](http://oingdoing.com/tips/all/img/responsive05.jpg)  
**그룹 지은 요소들 (Nested objects)** [Nested objects](http://oingdoing.com/tips/all/img/responsive06.jpg)  
**모바일 혹은 데스크톱 우선 작업 (Mobile or Desktop first)** [Mobile or Desktop first](http://oingdoing.com/tips/all/img/responsive07.jpg)  
**웹폰트와 시스템 폰트 (Webfonts vs System fonts)** [Webfonts vs System fonts](http://oingdoing.com/tips/all/img/responsive08.jpg)  
**비트맵 방식과 벡터 방식 (Bitmap images vs Vectors)** [Bitmap images vs Vectors](http://oingdoing.com/tips/all/img/responsive09.jpg)  

## 3. 전략 (작업순서 및 고려사항)

+ **"최소/최대" 뷰포트 사이즈에 우선 집중하기**  
> - 디바이스 최소 사이즈 정하기(viewport 이해하기)

+ **이미지 파일 전략 미리 가지기**  
: 일반 디스플레이용과 고해상도용
: pc와 mobile용
                 
+ **작게 생각하기 (모듈형 디자인)**  
: 작고 재사용이 가능한 구성요소에 우선적으로 집중 : 서로 다른 디바이스를 넘나들면서도 동일한 UX와 비주얼을 제공
  
+ **모바일 환경을 우선하여 기획 및 디자인하기**  
이것은 모바일 환경을 먼저 디자인 하면 보다 효과적이고 창조적인 디자인을 할 수 있다는 전략
> - 모바일 우선 작업(css도 마찬가지..)
> 모바일의 엄청난 성장 = 기회 (GROWTH = OPPORTUNITY)  
> 모바일 기기의 제약 = 집중 (CONSTRAINTS = FOCUS)  
> 모바일 기기의 기능 = 혁신 (CAPABILITIES = INNOVATION)  

+ **[애매한 버튼 크기는 손가락 크기로 (주로 엄지)](http://yoon-talk.tistory.com/695)**  
+ [추가정보](https://brunch.co.kr/@chulhochoiucj0/8)  

## 4. 반응형 디자인 패턴 (레이아웃)

: 뷰포트 변경에 따라 그리드 변화를 고려하여 레이아웃을 디자인한다.

+ [유동형 (Mostly Fluid)](https://googlesamples.github.io/web-fundamentals/fundamentals/design-and-ux/responsive/mostly-fluid.html)  
+ [열 끌어놓기(Column Drop)](https://googlesamples.github.io/web-fundamentals/fundamentals/design-and-ux/responsive/column-drop.html)  
+ [레이아웃 시프터(Layout shifter)](https://googlesamples.github.io/web-fundamentals/fundamentals/design-and-ux/responsive/layout-shifter.html)  
+ [미세 조정(Tiny tweaks)](https://googlesamples.github.io/web-fundamentals/fundamentals/design-and-ux/responsive/tiny-tweaks.html)  
+ [오프 캔버스(Off canvas)](https://googlesamples.github.io/web-fundamentals/fundamentals/design-and-ux/responsive/off-canvas.html)  


> ## 디자인
> - 디바이스 최소 사이즈 정하기(viewport 이해하기) @
> - 분기점(Break point) 정하기
> - 모바일 우선 작업(css도 마찬가지..) @
> - 비율(이미지, 레이아웃)에 맞춰 디자인하기 @
> - 모바일이나 테블릿의 해상도 지원 여부에 따라 2배 이미지로 사용(배율 축소). @<br>
> (벡터 이미지를 사용하는것이 좋으며 아이콘이나 로고등 SVG는 어떨까 ?)
> - 모바일에서 폰트 사이즈가 디바이스 넓이에 맞춰 비율대로 증가 할 수 있는가?<br>
> (vw 사용하여 가능하지만.. 정해진 폰트 사이즈로 보여질것인지 넓이에 따라 사이즈가 커저야 할 지 고민)
> - 각 디바이스 별 이미지 표시(PC, Tablet, Mobile)@
> 1. 이미지 비율에 맞춰 표시
> 2. 높이는 고정이고 이미지가 가운데로 고정
> 3. 각 디바이스 마다 이미지의 높이와 보이지는 부분이 다름
> - 각 디바이스 별 텍스트 줄바꿈(PC, Tablet, Mobile)
> (디바이스마다 줄바꿈이 다른경우 - 반응형에서 텍스트 줄바꿈은 단어별 줄내림으로 협의)
> - Hover&터치 효과 고려

## 5. 반응형 웹의 퍼블리싱 이슈

### 반응형웹 마크업 가이드 제작 전 고민사항

**미디어쿼리 해상도 분기문제**  
: 어느 포인트에서 해상도를 나눌 것인가? / 해상도기준(320,568,768,1024,1025~)  
─ [반응형 시안 내부 주요 분기점 자료](http://oingdoing.com/tips/all/img/rw_guideline.jpg)  
> **해상도 분기에 따른 컨텐츠크기 조정  
> max-width : 1024px 이상 일 경우 → 좌·우측 20px(총 40px)이상 유지  
> max-width : 1023px 이하 일 경우 → 좌·우측 10px이상 유지  

**해상도 분기에 따른 컨텐츠크기 조정**  
> max-width : 1299px → 1280px (실질 컨텐츠 : 1240px)  
> max-width : 1024px → 1024px (실질 컨텐츠, PC와 동일 크기 : 984px)  
> max-width : 1023px → 768px (실질 컨텐츠 : 748px)  
> max-width : 767px → 640px (실질 컨텐츠 : 620px)  
> max-width : 639px → 480px (실질 컨텐츠 : 460px (~360px 조정가능) )  
> max-width : 479px → 360px (실질 컨텐츠 : 340px)  
> max-width : 359px → 320px (실질 컨텐츠 : 300px)

**가변적 그리드 기반의 레이아웃**  
상단 자료 참고    

**상대단위 사용에 대하여(px to em/rem/vh/vw/%)**  
배율에 따른 px과 상대단위 변화    

**최소단위 뷰포트(320px)에서의 문제점 해결**  
미디어쿼리 뷰포트 구분하여 따로 스타일 지정  

[참고]
> [FROONT, "9 basic principles of responsive web design"](http://blog.froont.com/9-basic-principles-of-responsive-web-design/)  
> [Google Web Fundamentals, "반응형 웹 디자인 패턴"](https://developers.google.com/web/fundamentals/design-and-ux/responsive/patterns?hl=ko)  
> [디자인 아트, "반응형 디자인 패턴"](https://m.blog.naver.com/dartplus/221202644512)
