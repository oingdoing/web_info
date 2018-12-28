# 디자이너와 퍼블리셔가 함께하는 반응형 웹
> 2018/12/24, SAMY
## 1. 개요
반응형웹은 데스크탑, 노트북, 넷북, 태블릿, 스마트폰, 스마트TV 등 N-Screen의 Multi Device에 어떠한 사용자도 제약없이 접근할 수 있도록 제공하는 웹을 말한다.

## 2. 반응형 웹디자인의 특징
**반응형 웹디자인 vs 적응형 웹디자인** [Responsive and Adaptive](http://oingdoing.com/tips/allimg/responsive01.jpg)  
**플로우 (Flow)** [Flow and Static](http://oingdoing.com/tips/allimg/responsive02.jpg)  
**상대적인 요소들 (Relative units)** [Relative units](http://oingdoing.com/tips/allimg/responsive04.jpg)  
**분기점 (Breakpoints)** [Flow and Static](http://oingdoing.com/tips/allimg/responsive06.jpg)  
**최대값과 최소값 (Max and Min values)** [Max and Min](http://oingdoing.com/tips/allimg/responsive05.jpg)  
**그룹 지은 요소들 (Nested objects)** [Nested objects](http://oingdoing.com/tips/allimg/responsive06.jpg)  
**모바일 혹은 데스크톱 우선 작업 (Mobile or Desktop first)** [Mobile or Desktop first](http://oingdoing.com/tips/allimg/responsive07.jpg)  
**웹폰트와 시스템 폰트 (Webfonts vs System fonts)** [Webfonts vs System fonts](http://oingdoing.com/tips/allimg/responsive08.jpg)  
**비트맵 방식과 벡터 방식 (Bitmap images vs Vectors)** [Bitmap images vs Vectors](http://oingdoing.com/tips/allimg/responsive09.jpg)  

## 3. 전략
+ **"최소/최대" 뷰포트 사이즈에 우선 집중하기**  
시작부터 반응형으로 만들어지는 디자인이 있긴 하지만, 아직도 대다수의 디자인이 정적인 것에서부터 시작합니다. 반응형으로 시작하는거라면 우선 뷰포트 가로와 높이를 정하고, 이에 맞춰 스케치하고 마크업을 진행해야 합니다. 
하지만 그 순간에 몇 가지 물음이 생깁니다: 얼마만큼의 크기로 잡을 것인가? 테크니컬한 제약 때문에 어떤 디바이스를 우선적으로 생각해야 하는가?
추천해드릴 수 있는 것은 바로 자신이 타겟으로 삼은 사용자 공통의 “최소와 최대” 디바이스 사이즈로 시작하는 겁니다.
> 320px x 568px (아이폰5 수직모드)  
> 1600px X 1000px (와이드 모니터)

+ **이미지 파일 전략 미리 가지기**  
디자이너는 최소한 2개의 래스터 포맷(JPG)이 필요할 겁니다. 바로  일반 디스플레이용과 고해상도용이죠. 고급 반응형 이미지 기술은 서로 다른 뷰포트 사이즈를 위한 더 많은 파일을 요구합니다.  
프로젝트의 마지막 단계에서 반응형 이미지 포맷을 결정하지 마세요. 최소한 디스플레이 밀도에 대한 전략을 가지고 있어야 합니다. srcset이나 Picturefill과 같은 '폴리필polyfill'을 최대한 활용해서 좋은 크로스 브라우저를 지원해주어야 합니다. 만약 너무 부담이 된다면, 작게 시작하세요. 그냥 srcset 속성을 가지고 이미지를 변경하는 겁니다. 프로세스가 어떻게 가는지 보면서 점점 키워보세요.

+ **작게 생각하기 (모듈형 디자인)**  
작고 재사용이 가능한 구성요소에 우선적으로 집중합니다. 왜냐하면 서로 다른 디바이스를 넘나들면서도 동일한 UX와 비주얼을 제공하기 때문입니다. 이러한 일관성은 개발팀에게 부담을 주지도 않습니다. 또한 작은 구성요소들은 페이지 사이에서 더 재사용되는 경향이 있습니다. 이렇게 효과적으로 디자인을 한다면, 나중에 그것을 다시 적용하는 데에도 훨씬 쉬울 것입니다.  
작은 구성요소들은 일반적으로 다른 디바이스를 넘나들면서도 동일한 UX와 비주얼을 제공합니다. 이러한 일관성은 개발팀에게 부담을 주지도 않습니다.  
만약 지금 제목, 대형 그래픽, 양식이 있는 가입 페이지를 디자인 한다고 상상해 봅시다. 디바이스에 따라 이들 요소들은 이동하거나 사이즈가 변경될 겁니다. 초기에 개발팀과 가입양식의 세부적인 것에 초점을 맞춘다면 그 페이지는 과연 어땠을까요? 어떤 종류의 검증이 필요할까요? 터치 인풋과 마우스/키보드 사이에서 폼을 어떻게 바꿔야 할까요?
  
+ **모바일 환경을 우선하여 기획 및 디자인하기**  
이것은 모바일 환경을 먼저 디자인 하면 보다 효과적이고 창조적인 디자인을 할 수 있다는 전략입니다.
이렇게 디자인 된 결과물은 데스크탑 환경에 그대로 적용해도 뛰어난 사용자 경험을 제공할 수 있는 장점을 가지고 있습니다.
웹디자인을 할때 모바일을 먼저 생각해서 디자인/ 프로그래밍을 한다는 개념으로 LukeW에 의해서 주장 아래 내용은 공개된 [http://static.lukew.com/MobileFirst_LukeW.pdf](http://static.lukew.com/MobileFirst_LukeW.pdf)의 출처입니다.
> 모바일의 엄청난 성장 = 기회 (GROWTH = OPPORTUNITY)  
> 모바일 기기의 제약 = 집중 (CONSTRAINTS = FOCUS)  
> 모바일 기기의 기능 = 혁신 (CAPABILITIES = INNOVATION)  

+ **[애매한 버튼 크기는 손가락 크기로 (주로 엄지)](http://yoon-talk.tistory.com/695)**  
UI 버튼 크기는 사람들의 손가락 크기에 의해 제한됩니다. 특정 버튼이 사용자의 손가락보다 너무 작을 경우, 당연히 터치 정확도가 떨어지겠죠.  
사용성의 오류가 생기는 것입니다. 그래서 UI 버튼은 손가락 평균 크기에 맞게 디자인하는 것이 가장 이상적입니다.  
마찬가지로 앞서 말했듯이 필요에 따라 버튼 크기 조절 기능을 추가하는 것도 방법일 수 있습니다.  
+ [추가정보](https://brunch.co.kr/@chulhochoiucj0/8)  

## 4. 반응형 디자인 패턴 (레이아웃)
+ [유동형 (Mostly Fluid)](https://googlesamples.github.io/web-fundamentals/fundamentals/design-and-ux/responsive/mostly-fluid.html)  
+ [열 끌어놓기(Column Drop)](https://googlesamples.github.io/web-fundamentals/fundamentals/design-and-ux/responsive/column-drop.html)  
+ [레이아웃 시프터(Layout shifter)](https://googlesamples.github.io/web-fundamentals/fundamentals/design-and-ux/responsive/layout-shifter.html)  
+ [미세 조정(Tiny tweaks)](https://googlesamples.github.io/web-fundamentals/fundamentals/design-and-ux/responsive/tiny-tweaks.html)  
+ [오프 캔버스(Off canvas)](https://googlesamples.github.io/web-fundamentals/fundamentals/design-and-ux/responsive/off-canvas.html)  

## 5. 반응형 웹의 퍼블리싱 이슈
### 반응형웹 마크업 가이드 제작 전 고민사항
**미디어쿼리 해상도 분기문제**  
: 어느 포인트에서 해상도를 나눌 것인가? / 해상도기준(320,568,768,1024,1025~)  
─ [반응형 시안 내부 주요 분기점 자료](http://oingdoing.com/tips/allimg/rw_guideline.jpg)  
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

**IE8 브라우저의 하위 호환성**  
> 인터넷 익스플로러(이하 IE) 6, 7, 8은 CSS3 미디어쿼리를 지원하지 않는다.  
> 8이하로는 잘 맞추지 않는다.    

**가변적 그리드 기반의 레이아웃**  
> 상단 자료 참고    

**상대단위 사용에 대하여(px to em/rem/vh/vw/%)**  
> 배율에 따른 px과 상대단위 변화    

**최소단위 뷰포트(320px)에서의 문제점 해결**  
> 미디어쿼리 뷰포트 구분하여 따로 스타일 지정    

**반응형에 따른 이미지 대처**  
> 모바일용 이미지 / pc용 이미지    

**최대 글자 수 & 줄바꿈**  
> LG화학 때 보니 <br> 사용하지 않고 자연적으로 줄바꿈 되게 (word-break)



[참고]
> [FROONT, "9 basic principles of responsive web design"](http://blog.froont.com/9-basic-principles-of-responsive-web-design/)
> [Google Web Fundamentals, "반응형 웹 디자인 패턴"](https://developers.google.com/web/fundamentals/design-and-ux/responsive/patterns?hl=ko)
> [디자인 아트, "반응형 디자인 패턴"](https://m.blog.naver.com/dartplus/221202644512)
