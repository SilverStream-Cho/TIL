# TIL 2023. 04. 17.
> jekyll을 활용해 내 local 컴퓨터에 기본적인 블로그 생성하는 방법을 참고하기 위해 작성한 글입니다.
>> jekyll: 내가 실제 운영할 수 있는 블로그를 생성해주는 프로그램

---
> 왜 Jekyll을 사용?
* 애초에 css, html, JS 활용해서 블로그를 만들기에는 너무 힘들기 때문에 blog template을 만들어주는 것
* 그걸 가져다가 그 안에 블로그에 대한 내용 포스팅을 하고, jekyll을 활용해서 compile하는 과정
* 이 과정을 거치면 내가 운영할 수 있는  블로그에 대한  css. html, JS 파일이 나오게 됨

* Github 페이지에 블로그를 바로 올릴 수 없고, 거쳐야 하는 단계들이 있다. 
* 기본적으로 내 컴퓨터에 기본적 블로그 생성하는 방법을 이용하고, 커스터마이징 하고, 만들어진 블로그를 Github에 올리는 단계로 진행할 것

---

1) 환경설정

* Github 페이지에서 Jekyll로 기본 형태 블로그 개설은 어렵지 않으나 커스터마이징을 해서 사용하려면 약간의 Front End 개발 지식이 필요

> Jekyll Themes: 마음에 드는 테마 검색(http://jekyllthemes.org/)

* 여기서 찾은 테마를 기반으로 블로그를 만들어낼 것이다. 테마에 따라 생김새나 기능이 달라질 수 있다는 점을 고려

(0) 컴퓨터 계정 ID 확인 : 한글/영문인지

* 사이트 생성기인 Jekyll을 활용하려면 Ruby가 있어야 한다.(Ruby상에서 Jekyll이 돌기에 Ruby 설치가 필요)
* Ruby는 한글과 특수문자 활용에 문제가 있다. 따라서 컴퓨터 계정 아이디가 한글로 되어있는지부터 체크해야!

(1) Ruby 설치: '=>' 표시되어있는 버전을 설치(https://rubyinstaller.org/downloads/)

* Ruby 내에서 bundler를 설치해야 한다. 이를 설치해야 우리가 Jekyll을 실행할 수 있다.)
* bundler로 Jekyll을 실행해서 Jekyll이 블로그를 만들어주는 것이 실행 과정이다.
* 검은색 화면이 뜨면 1 입력 후 Enter 누르기 -> 이후 화면 움직임이 끝나면 enter로 끝내기


# TIL 2023. 04. 22.

- 영상 한번 본다고 해서, 책 한번 읽는다고 해서, 블로그에 있는 글 읽는다고 해서 그 기술 자체가 자신에게 체득이 되는 것은 아니다. 
- 반복적으로 코딩도 한번 해보고, 배운 내용에 대한 지속적인 유지보수가 있어야 한다. 
- 부족하게 알고 있었던 부분들에 내용을 덧붙여서 내용을 확장시켜나가야 한다. 라는 과정들이 후행이 되어야 그 내용들이 자신에게 체득이 된다. 
- 어딘가에는 자신이 공부한 내용들이 담겨있어야 한다. 
- 그래야 그것을 본인이 반복적으로 보고, 수정하고 보완하고 학습하고, 이런 식의 과정들이 필요하다.
- 기술 블로그를 운영하는 것이 굉장히 많이 도움이 된다. (접근성, 활용성 면에서)
- 일단 접근성 면에서 장점이 있다. 언제 어디서나 내가 작성한 내용들, 내가 정리한 내용들을 확인할 수 있다. 
- 그리고 쉽게 기존에 있는 내용들을 내가 유지보수하면서 더 발전된 내용으로 만들어나갈 수 있다. 
- 단, 공부하고 알고 있는 내용들을 알아듣기 쉽게 글로 표현한다는 과정 자체가 어렵다.
- 알고 있는 글 자체를 글로 정리하는 것은 학습이기 때문에 장점은 크다.
- 자기가 기술 블로그를 공부해야지 내가 모르는 것은 무엇이고 알고 있는 것은 무엇인지, 더 알아야 할 것은 무엇인지 체크해나가면서 공부할 수 있기 때문에 사실 좋은 방식이다. 

---

>> 이 글은 Jekyll을 이용해 자신의 local 컴퓨터에 기본적인 블로그를 생성하는 방법을 학습하고 정리한 글입니다. 이후 커스터마이징 하고, 만들어진 블로그를 웹상(깃허브)에 올리게 되는 단계로 진행할 것이다.

**Jekyll**: 블로그 생성기

- 사실 우리가 맨땅에 처음부터 html, css, js 파일을 만들어서 블로그를 운영하는 것은 너무 힘들고 할 일이 많다.
- 어느 정도의 형태가 갖춰져 있는 블로그 템플릿을 이용한다. 
- 거기 안에 블로그 내용을 포스팅한다. 
- 그걸 Jekyll을 활용해서 컴파일하게 된다. 
- 컴파일을 하면 내가 운영할 수 있는 블로그에 대한 html, css, js 파일이 튕겨져 나온다.
- 즉 Jekyll은 내가 실제 운영할 수 있는 블로그를 만들어주는 프로그램이다. 
- 우리가 제일 필요한 것은 테마가 필요하다. -> Jekyll Themes에서 검색해 찾는다. 
- 그중 내가 마음에 드는 테마를 찾아서 걔를 기반으로 해서 지킬로 블로그를 만들어낼 것이다.
- 테마에 따라 내 블로그의 생김새나 기능이 달라진다. (이번에는 Jasper2 테마를 활용)

---

- windows 환경은 조금 까다롭다. 바로 Ruby라는 프로그래밍 언어 때문이다. 
- Jekyll을 활용하려면 Ruby라는 프로그래밍 언어가 있어야 한다. Ruby 상에서 Jekyll이 돌아간다고 생각하자. (이때 컴퓨터 계정 ID가 한글로 되어있으면 문제가 발생해서 참 여러 번 고초를 겪었다.)
- 구글 검색창에 Ruby를 검색한다. 
- 제일 먼저 해야하는 것은 Ruby를 윈도우 시스템에 설치해야 한다. (화살표로 받으라고 표시되어있는 듯한 파일로 받자. 설치완료하면 체크표시 빼지 말고 FINISH. CMD 창 뜨면 1번 누르고 ENTER. 이후 다 완료되면 ENTER누르고 끝낸다. -> Ruby 설치 완료)
        
        
## bundler 설치

- 루비가 설치가 되었다면 이제 번들러를 설치해야 함. 번들러는 우리가 사용할 지킬을 실행시켜주는 놈
- cmd 열어서 저 코드를 친다. 
```
gem install bundler
```
- 조금만 기다리면 번들러가 설치된다. 
- 이렇게 되면 기본적인 준비과정은 끝난 것이다. 

## 테마 다운받기(Jasper2 테마 다운)

- 이제 우리가 사용할 테마인 재스퍼 2라는 테마를 구글에 검색 후 다운로드 ->  'C:/blogmaker'라는 폴더를 만들어서 압축을 풀어 저장 
- 파일들이 우글우글 대는데 얘가 우리가 블로그를 작성할 템플릿. 특정 위치에 포스팅한 다음에 지킬을 활용해서 컴파일하면 서비스할 블로그가 만들어지는 방식(단, 폴더 이름에 공백이 포함되면 나중에 css 빌드할 때 문제가 발생하니 소문자로 공백없이 생성하기

## gem 설치

- 지킬은 아직 설치를 안 한 상태이다. 다른 부가적인 것들 설치를 먼저 해주자. 
- cmd를 다시 연다. 
```
C:\Users\SilverStream>cd..
C:\Users>cd..
C:\>cd blogmaker
C:\blogmaker>bundle install
```
- blogmaker 폴더로 이동해서 아래 명령어를 친다. 
- 다 설치된 후에는 다음 명령을 이용해서 블로그를 컴파일해서 내장 웹서버를 통해 local 컴퓨터에서 블로그를 띄워볼 것이다. (아직 만들어낸 것은 없지만 한번 보자)

```
bundle exee jekyll serve 
```
- 위의 명령어를 작성해보자. 그러면 아까 설명했듯이 jekyll을 활용해서 블로그를 컴파일한다. 컴파일 한 후 다 완료가 되면 내장 웹서버가 있다. 
- 걔를 통해 우리 컴퓨터 상에서 우리 블로그에서 실제 서비스를 진행시켜주게 된다. 제대로 되었는지 확인해보자. 
- 잘 보면 '야, 오류는 아니지만 이렇게 추가해줘.' 라는 식의 내용이 있는 것을 볼 수 있다. 

- [오류 발견] Liquid Exception: undefined method `tainted?' for "http://localhost:4000":String in /_layouts/post.html
- 해당 오류가 발견되었지만 서칭하다가 지금 막힌 상태이다.
- 일단 임시로 깃헙 메인 페이지 꾸며놓고 html, css 학습하는 과정에서 웹페이지를 만들어보는 작업을 먼저 진행해보자.
- 나중에 잊지 말고 이 홈페이지는 다시 해결방법 찾아서 건드려볼 것

### solution(2023. 04. 23.)
- 블로그 작업을 하다가 로컬 컴퓨터에 내보내서 확인하는 걸 모르겠어서 다시 이 영상을 참고해 적용해보려고 했다.
- 그런데 이번에는 확인한게 'exee'가 유투브 업로드 상에서 오타여서 'exec'로 쳐야했다는 것을 깨달았다.
- 쳐보니 문제점을 발견했다. 내가 gemfile이 없다고 뜨는 것이다. 
- jekyll을 사용하는 방법에 대해서 처음부터 다시 서칭해보기 시작했다. 그러다 다음과 같은 페이지를 발견했다. https://jekyllrb.com/docs/installation/
- 하나씩 버전을 확인해보니 gcc가 없다는 것을 발견. window상에서는 제대로 다시 깔아주어야 한다고 한다. [참고한 블로그](https://ddmanager.tistory.com/152)
- make 설치 루트를 찾다가 이 방법을 발견해서 해결(https://velog.io/@dd9s2/Github.io-%EC%8B%9C%EC%9E%91%ED%95%98%EA%B8%B0-Jekyll-%EC%84%A4%EC%B9%98-Windows)
 ### extra problem
```
C:\tilblogmaker\SilverStream>bundle exec jekyll serve
Could not find gem 'wdm (~> 0.1.1) mingw, x64_mingw, mswin' in locally installed gems.
Run `bundle install` to install missing gems.
```
- [참고블로그](https://ogaeng.com/jekyll-blog-install/)에서 얻은 정보대로 다시 폴더를 하나 생성해보고 그 아래에 실행해보니 이번엔 다른 오류 메시지가 나왔다.
- bundle install을 다시 입력해서 실행시키니 작동이 된다. 다시 exec를 실행해보자.

# TIL 2023. 04. 23.
- 어제 저녁부터 TIL 깔끔하게 올릴만한 기술블로그를 만들어보고 싶어서 이것저것 찾아보다가
- 다른 개발자분들이 만들어주신 코드를 내 local 컴퓨터에 clone해서 편집할 수 있다는 사실을 알게 되었다.
- 어제 활용 못한 jekyll을 활용해서 실제로 블로그를 만든 케이스를 가져와야겠다고 생각했다. 
1. 검색한 오픈 소스에서 개발자분의 README.md 파일을 읽어본다.(이 프로젝트의 구체적인 내용이 들어있기 때문에 꼭 확인해야 하는 문서)
2. 오른쪽 상단의 Fork를 클릭하여 내 계정으로 소스코드 넘어오게 하기
3. 내 컴퓨터로 소스코드 보내기: 컴퓨터 내(C:아래) 새로운 폴더 만들고 cmd창 켜서

```
git clone (복붙한 HTTP url)
```

- 이렇게 입력하면 된다고 한다.
- 그런데 웬걸.. 오류가 떴다. 
![](C:\Users\SilverStream\Pictures)
- 계속 시도해봐도 안 되길래 구글창에 서칭을 시작했다.
### SOLUTION
- 알고보니 내 컴퓨터를 지난번에 새로 시스템 복원을 시키고 나서 git이 삭제된 모양이었다. 
- 다른 eclipse랑 파일들은 남아있었는데 git만 삭제된 이유를 모르겠네..
        - git 설치하는 과정에서 보니 설치경로가 **Program Files""로 되어있어서 다른 것들이랑 같이 삭제된 것 같다. 카카오톡 등등 같이 삭제된 것을 보면 이해가 됐다.)
        - 왜 잘 해결되지 않았는지를 이해하는 것 자체도 굉장히 즐겁다. (그래도 너무 들뜨지 말고 열심히, 겸손히, 차근차근 배우자)
### extra problem
- 오류: Setup was unable to create the directory error 5
- 어플리케이션 설치 때마다 오류 메시지가 발생해서 재설치했지만 계속 마지막 지점에서 오류 메시지 발견
### solution
- 이 문제를 해결하려면 사용자 계정의 TEMP 폴더 권한을 수정해야. 폴더의 보안 권한이 올바르지 않은 경우 이러한 오류가 발생할 수 있다.
- "C:Users<사용자 이름>AppDataLocal"로 이동한다.
- "Temp" 폴더를 마우스 오른쪽 버튼으로 클릭하고 "속성"을 선택한다.
- "보안" 탭을 연다.
- "고급" 버튼 >> "소유자" 탭을 클릭한다.
- "편집"을 클릭한다.
- 사용자 아이디를 선택하고 >> "적용"을 누른 다음 >> "확인"을 누른다.
- 이 레지스트리 패치를 사용하여 Windows 탐색기에 "소유권 가져오기" 컨텍스트 메뉴를 추가할 수도 있다. 패치를 다운로드하고 레지스트리를 설치한 다음 폴더를 마우스 오른쪽 버튼으로 클릭하고 "소유권 가져오기"를 선택한다.
- 이제 폴더는 내 소유가 되며 폴더에 대한 모든 권한을 갖게 된다. 그렇게 된 후에 다시 실행해보기
<br/>
- 완벽히 다시 실행이 되었다.  

### 이제 다시 클론으로 해서 컴퓨터로 오픈소스 코드 가져오기
- cmd 창 켜서 해당 폴더로 이동한 후 다음을 입력


```
C:\>cd tilblogmaker

C:\tilblogmaker>git clone https://github.com/codinfox/codinfox-lanyon.git
Cloning into 'codinfox-lanyon'...
remote: Enumerating objects: 907, done.
Receiving objects:  97% (880/907)
Receiving objects: 100% (907/907), 281.53 KiB | 5.87 MiB/s, done.
Resolving deltas: 100% (410/410), done.

C:\tilblogmaker>
```
- 이동이 완료된 것 같다.
- 이제 vsCODE에서 수정하면서 시도해보자.
# 2023. 04. 24.
두 번째 싸피 스터디를 시작했다. 오전 8시 30분에 도착해 미리 살펴보고 스터디원들을 만나고 난 뒤에는 수추리 문제를 1시까지 풀었다
오랜만에 수리적 사고를 일깨운다는 것이 얼마나 뇌가 팽팽 돌아가야 하는 일인지를 깨달았던 것 같다
오늘은 스터디원 한분이 더 참여하게 되어서 2시부터 새로 참여하신 분께 지금까지 나눴던 일에 대해서 설명하고 어떻게 같이 스터디를 꾸려나가야 할지에 대해서
방향성을 함께 논의하는 시간을 가졌다 얘기하면서 서로의 공부방식을 나누다보니 얻게 된 정보가 많았다
특히 CT의 경우 알고 있는 정보가 없어 오전 중에 다른 스터디원과 곤란해하던 상황이었는데, 그에 대해 많은 정보를 얻을 수 있게 되어서 
정보를 받아 남은 3시간 동안은 알려주신 방식으로 CT를 공부해보았고 그것은 큰 성과였다
바이트, 비트, 큐나 그래프, 트리에 대한 내용과 예제들을 학습했는데 생각보다 사고하는 과정이 정말 즐거웠고 이런 생각을 해낸 사람들에 대해서도 감탄하는 마음을 갖게 되었다
다시금 열정이 피어오르는 것이 느껴졌다. 조금씩 공부를 하면서 이전에 가지고 있던 '천생 문과인 내가 개발자가 될 수 있을까' 라는 의문에 대해서 점차 확신을 가지게 되는 것 같다.
성장하는 것이 즐겁고, 하나씩 알아갈 때마다 성취감이 느껴지고, 웹페이지에 들어갈 때마다 이것들을 이루고 있는 것들에 대해 생각하면서 벌써부터 배우게 될 것들에 대해 즐거워진다. 공부하는 시간이 기다려지고 밤을 새면서 공부를 하고 싶은 지경이지만 '내일 새로운 하루에 새로운 것을 맑은 정신으로 공부하기 위해' 라고 생각하면서 푹 수면을 취하는 하루가 행복하다. 내일은 일요일에 다하지 못한 HTML 공부를 마무리하고 대학원 시험공부를 하는 것으로 꽉 찰 것 같다. 

# 2023. 04. 25.
## 오전 9시 : vsCODE 작성에 익숙해지기, HTML 공부하기
마음이 복잡하다. 하고 싶은 것은 정말 많은데 할 것이 너무나 많아 머릿속에 과부하가 일어나는 것 같다. 그마저도 즐겁다면 꼭 이 길을 걸어가고 싶다는 생각도 한다. 
기술블로그를 빠르게 만들어서 내가 찾은 오류와 개발을 항목별로 잘 정리해두는 것을 가장 먼저 준비해두고 싶다. 공부한 것들은 TSTORY에 정리해놓다가, 실제 적용하면서 발견한 오류들과 학습 요약, 느낀 점들을 별개의 카테고리로 분류해서 관리하고 싶다.
그러기 위해서 HTML부터 보면서 웹페이지를 만들고 관리하는 방식을 빠르게 배우고 싶다. 
- TSTORY 운영 장점 : 확실히 tstory에 html형식으로 글을 적기 위해 vsCODE로 적고 옮겨적는 방식으로 연습을 하다보니(아직 엉거주춤하고 깔끔하지 않지만) 연습이 되고 단축키나 기능도 어느 정도 익숙해진 것 같다.
## 오전 11시 : 첫 웹사이트 제작 완료
html을 거의 배우고 뼈대 느낌의 못생긴(..) 웹페이지가 만들어졌다.
기본 형태 자체는 갖추게 된 느낌인데 앞으로 이게 깔끔하게 적혀있는지 html을 배우면서 수정해나가고,
css를 배우면서 새롭게 추가하는 방식으로 웹사이트를 관리해봐야겠다.
## 오전 12시 : html을 배우면서 글을 쓸 때 <ul>과 <li> 대신 <p>로 줄글작성을 하는 것이 더 가독성이 좋고 태그 자체의 기능 취지에도 맞다는 것을 깨달았다. 틈틈 vsCODE에서 수정하면서 어떻게 가독성 있고 코드의 목적에 맞게 사용할 것인가를 더 고민해보자. 
그리고 오늘은 인터넷과 웹의 역사에 대해서도 알아봤다. 지금은 너무나도 넓은 정보의 바다 속에 있지만 가장 처음에 태어난 때의 이야기를 들으니 마치 박물관에서 설명을 듣는 느낌이었다. 정말 흥미로운 분야인데, 왜 지금껏 모르고 있었을까 이런 순간들에는 늘 후회가 된다.

