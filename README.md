<span class="bigTitle">고양이를 위한 자바스크립트</span>
## 뉴비 개발자를 위한 소개 <span class="right">![cat](images/substack-cats.png)</span>
### *닝겐 친구도 할 수 있을 만큼 쉽다냥!*

JavaScript 는 프로그래밍 언어 혹은, 다른 말로 하면, 컴퓨터가 무언가 하도록 지시하는 방법이야. 어떤 냥이가 하앍질 하거나 냐옹냐옹 하면서 닝겐을 콘트롤하듯이, 어떤 냥이는 프로그래밍언어로 쓰여진 문장으로 컴퓨터를 콘트롤한다구. 모든 웹브라우저가 자바스크립트를 이해하고 넌 웹페이지가 뭔가 엄청난 걸 할 수 있게 그걸 이용할 수 있어!

자바스크립트는 웹페이지를 좀 더 대화하는 것처럼 만들기 위해 시작됐어. 요즘엔 자바스크립트가 웹브라우저 외에도 더 다양한 곳에서 돌아가.— 웹서버, 전화기, 심지어는 로봇에서도 말이야! 이 페이지가 자바스크립트의 기초에 대해 아주 살짝 알려줄 거야. 당장 일어나서 바로 시작할 수 있게 말이야*.

\* *실제 걸리는 시간: 정확히는 어느 정도 시간이 걸려. 아마 한 두 시간 정도. 또 넌 냐옹이니까 달릴 거 같진 않고 햇빛 아래 드러누울 것 같당*

## 내용 목록

- [콘솔] (#basics)
- [문자열](#strings)
- [값과 변수](#values)
- [함수 이용](#functions)
- [JS 내장함수](#standard-library)
- [새로운 JS 함수 내려받기](#third-party-javascript)
- [새로운 함수 만들기](#writing-functions)
- [반복](#loops)
- [배열](#arrays)
- [객체](#objects)
- [콜백](#callbacks)
- [읽으면 좋다냥](#recommended-reading)

## 겁쟁이가 되지 말라냥

<span class="right">![cat](images/yarnify.png)</span>

넌 언제나 두 발로 착륙하게 될거야. &mdash; 심지어는 개발할 때에도 말이야! 노트북위에서 [서툴게 물잔을 다루는 것](images/dealwithit.gif) 관 다르게, 어쨋든 이 과정을 따라하는 도중에 네 컴퓨터를 망가뜨리는 일 따윈, 전혀 _없을 거야_, 명령문을 잘 못 치거나 실수로 다른 버튼을 누른다 해도 말이야. 고양이처럼, 컴퓨터 개발자들은 항상 실수하거든: 철자를 잘 못 쓰거나, 인용부호로 감싸거나 브라켓을 입력하는 걸 잊고, 그리고 기본 함수(그리고 털실이나 레이저 같은 것도)가 어떻게 동작하는 지 완전 까먹고 말이야. 개발자들은 처음부터 동작하도록 만드는 것보단 _결국엔_ 돌아가게 만드는 것에만 더 신경을 쓰거든. 뭔가를 배우는 가장 좋은 방법은 실수하는 거야!

그러니깐 겁먹지마! 일어날지 모를 가장 완벽하게 안 좋은 건 네가 어딘가에서 막혔을 때 이 페이지를 다시 열어봐야 할 수도 있단 거야. 쨋든 걱정하지마, 아마 그런 일은 거의 없을 거야.

## <a id="basics" href="#basics">#</a> 기본

지금 당장 이 페이지에서 돌아가는 자바스크립트가 있어.  그거랑 잠깐 놀아보자. 그냥 쉽게 네가 이 페이지를 보기 위해 구글 크롬을 사용한다고 가정할게(만약에 아니면, 크롬으로 따라해보는 게 우리 둘 다를 위해서 좀 더 쉬울 거야).

우선, 화면의 아무 곳에서나 마우스의 오른쪽 버튼을 눌러봐 그리고 **요소 검사Inspect Element**를 눌러봐, 그리고 나서 **콘솔Console** 탭을 눌러봐. 이렇게 보이는 뭔가를 볼 수 있을 거야:

![console](images/console.gif)

이건 콘솔이야, 다르게는 코맨드라인command line 이나 혹은 터미널terminal 로 알려져 있어. 기본적으로 이건 컴퓨터에 뭔가를 입력하자마자 바로 컴퓨터의 답을 얻는 그런 방법이야. 뭔가를 배우는 도구로서 굉장히 유용해. (난 아직도 코딩하는 거의 매일 콘솔을 사용해).

콘솔은 진짜 엄청난 걸 해. 여기에서 내가 뭔가를 치기 시작하면 계속 칠 수 있는 가능한 모든 것을 목록으로 보여주면서 날 도와줘! 네가 할 수 있는 또 다른 건 콘솔에 `1 + 1` 을 치는 거야 그리고 `Enter` 를 누르고 나서 어떤 일이 일어나는 지 봐봐.

콘솔을 사용하는 건 자바스크립트를 배우는 데 매우 중요한 부분이야. 만약에 어떤게 동작하는 거나 어떤 명령이 무엇을 하는 지 모르겠다면 콘솔로 가서 알아봐! 여기 예를 보여줄게:

### <a id="strings" href="#strings">#</a> 문자열

난 고양이어서 인터넷의 모든 `dog` 단어 경우를 `those blasted dogs`. 라고 바꾸고 싶어. 우선 콘솔로 가서 `dog` 를 적어도 한 번이상 포함한 문장 몇 개를 써. 자바스크립트에선 문자, 숫자, 단어 혹은 그 어떤 것의 뭉치도 **문자열String** 이라고 알려져 있어. (문자가 *줄지어* 나와서 string 이야). 문자열은 인용부호로 시작하고 끝나야해. 홑따옴표 `'` 혹은 쌍따옴표 `"` 둘 다 괜찮아, 그냥 시작에 사용한 따옴표를 끝에 사용해야 한다는 걸 잊지마.

![console](images/console-strings.gif)

불쾌하기 짝이 없는 오류 메세지가 보여? 걱정하지마 - 어떤 규칙도 네가 망가뜨린 게 아니야. 비허용 구문오류SyntaxError ILLEGAL 는 로봇이 너한테 네가 만든 프로그램이 문제가 있다고 말할 때와 같은 거야. 처음 두 문장은 시작과 끝에 서로 일치하는 인용부호를 가지고 있어, 그런데 내가 홑따옴표랑 쌍따옴표를 섞어서 써서 코드가 나땜에 맛이 갔네.

OK(Minions 에 나온 Bob 의 목소리로 *역자 주), 이 문장들 중 하나를 섞기 위해서 (`dog` 단어를 우리의 향상된 버전으로 바꾸면서) 변경 마술을 부릴 때 나중에 불러내기 위해 우선 우린 원래 문장을 저장해야 해. 콘솔에 칠 때 문자열이 빨간색으로 어떻게 반복되는 지 눈치챘어? 어디든 바로 내놓을 수 있게, 문장을 저장하라고 콘솔에 말하지 않아서야. (혹은 뭔가 잘 못 어질러 놓으면 오류를 내놓을 거야).

### <a id="values" href="#values">#</a> 값과 변수

**값Values** 은 자바스크립트에서 가장 간단한 구성요소야. `1` 은 값이야, `true` 도 값이야, `"hello"` 도 값이고, `function() {}` 도 값이야, 목록은 끝없이 나열될 수 있어! 자바스크립트에는 수많은 다른  **종류types** 의 값이 있지만 지금 당장 그 모든 걸 볼 필욘 없어 — 네가 코드를 더 많이 짤 수록 자연스럽게 알게 될 거야!

값을 저장하기 위해서 우린 **변수variables**라고 불리는 걸 사용해.  'variable'라는 말은 '변할 수 있음'을 의미하고 변수가 많은 다른 종류의 값들을 저장할 수 있고 수없이 많이 그 값을 바꿀 수 있기 때문에 사용되는 거야. 이건 꼭 우편함 같아. 변수에 뭔가를 넣잖아. 예를 들면 우리 문장 같은 거 말이야. 그리고 나중에 그 문장을 찾아 볼 수 있게 그 변수에 주소를 줘. 실제로 우편함은 PO Box 번호를 가져야 해. 그런데 자바스크립트에선 보통은 공백없이 소문자나 숫자를 사용해.

![console](images/console-variables.gif)

`var` 는 variable 의 줄임말이야. 그리고 `=` 는 오른쪽의 것을 왼쪽의 것에 저장 하라는 의미야. 그리고 또 볼 수 있는 것처럼, 문장을 변수에 저장하기 때문에 콘솔이 그냥 바로 문장을 다시 돌려주진 않아. 대신에 `undefined` 를 내놓는데 이건 *돌려줄 것이 아무것도 없다는 거야*.

그냥 간단히 변수 이름을 콘솔에 치면 변수에 저장된 값을 표시해 줄거야.  변수에 대해 주의할 점은 다른 페이지로 이동할 때 기본적으로 변수가 없어진다는 거야. 만약에 크롬의 새로고침 버튼을 누른다면 가령, 내  `dogSentence` 변수는 지워지고 마치 한번도 있었던 적이 없는 것과 같을 거야. 그런데 지금 이걸 너무 걱정하지마 &mdash; 그냥 위 아래 방향 버튼을 눌러서 콘솔에 최근에 입력했던 모든 걸 살펴볼 수 있어.

### <a id="functions" href="#functions">#</a> 함수

변수에 문장을 저장했으니, 그 안의 단어를 바꿔보자! 바로 *함수function*를 실행해서 할 수있다구. *함수Functions*는 값의 한 형태로 특별한 기능(또는 목적이나 행동이라고 해도 돼)을 취급해. "행동actions" 이라고 부르는 건 내가 생각하기에도 좀 이상하니깐 그 대신에 "함수function"로 부르는 거야.

자바스크립트는 `replace` 라는 정확히 우리가 원하는 함수를 가지고 있어!  함수는 괄호안에 매개변수를 원하는 만큼 가질 수 있어(없거나 1개 혹은 아주 많을 수도 있어) 그리고 아무 것도 돌려주지 않거나 (`undefined`) 바뀐 문자열을 돌려줘. 이 `replace` 함수는 어떤 문자열에도 사용가능하고 두 개의 값을 가지는데 빼낼 문자랑 바꿔 넣을 문자야. 여기서 말로 설명하는 건 좀 헷갈리니깐 내가 직접 보여줄게:

![console](images/console-replace.gif)

 `dogSentence` 의 값이 함수 `replace` 적용 후에도 전과 같은 걸 눈치챘어?  이게 왜 그러냐면, `replace` 함수가(그리고 대부분의 자바스크립트 함수가 이 부분에선) 우리가 준 값을 가져가고 **새 값new value**을 반환해, 그런데 우리가 전달한 값을 수정하진 않아. 결과를 저장하지 않아서 ( replace 함수의 왼쪽에, `=` 표지가 없지? 그렇지?) 그냥 콘솔에 반환값을 표시한 거 뿐이야.

### <a id="standard-library" href="#standard-library">#</a> "표준 라이브러리"

아마 자바스크립트의 다른 이용할 수 있는 함수들은 어떤 것들이 있을 지 궁금할 거야. 답은: 완전 많음. 이야. 굉장히 많은 **내장 (객체), 표준 라이브러리들built in, standard libraries** 이 있는데 MDN(Mozilla 가 운영하는데 웹기술에 관련된 개쿨한 정보가 많은 사이트야)에서 배울 수 있어. 예를 들면 [이곳이 MDN의 자바스크립트 Math 객체 페이지](https://developer.mozilla.org/en-US/docs/JavaScript/Reference/Global_Objects/Math)야.

### <a id="third-party-javascript" href="#third-party-javascript">#</a> 제3소프트웨어 자바스크립트

**그 안에 지어지지 않았지만not built in**사용가능한 자바스크립트 코드가 많아. 제삼자 위치에 있는 자바스크립트는 보통 "라이브러리" 나 "plugin" 으로 불려. 내가 젤 좋아하는 것 중에 하나가 **Underscore.js**라고 불리는 거야. 가져와서 우리 페이지에 불러와 보자! 우선 Underscore 사이트[http://underscorejs.org/](http://underscorejs.org/)에 가서, 다운로드 링크를 클릭해.(난 읽기가 쉬워서 보통 개발버전을 사용하는데, 둘 다 동일한 기본 기능을 제공할 거야.), 그리고 나서 클립보드의 모든 코드를 복사해 (모든 걸 선택하기 위해서 수정 메뉴의 모두 선택하기 를 사용할 수 있어). 그리고 콘솔에 붙여넣고 엔터키를 눌러봐. 이제 네 브라우저가 그 안에 새 변수를 가지고 있을 거야: `_`. Underscore 는 놀아볼 유용한 함수를 엄청 많이 제공해. 이거에 대해선 좀 있다 더 알아보자.

![console](images/underscore.gif)

### <a id="writing-functions" href="#writing-functions">#</a> 함수 새로 만들기

다른 사람들의 함수만 사용하란 법은 없어 &mdash; 네가 직접 만들 수도 있어. 굉장히 쉽다구! 문장의 뒤에 감탄사 부호 한 웅큼을 더하는 `makeMoreExciting` 함수를 만들어 보자.

    function makeMoreExciting(string) {
      return string + '!!!!'
    }

내 머리속에선 이렇게 소리내 읽게 되네: "'make more exciting' 이란 함수가 있어. 이건 한 문자열을 받아서 그거의 새로운 복제물을 돌려주는데, 그 끝에 감탄사 부호 한 웅큼을 가지고 있어." 함수를 사용하지 않는다면, 어떻게 직접 콘솔에 쓰는 지 보여줄게:

![console](images/custom-function-manually.gif)

`string + '!!!!'` 라는 표현은 새로운 문자열을 돌려주고 `string` 이라 불리는 우리 변수는 전과 같이 유지돼.(우리가 `=`로 다른 변수에 갱신해서 저장하지 않았기 때문이야).

직접 적지 말고 우리 함수를 사용해 보자. 우선 콘솔에 그 함수를 붙여넣고 그 함수에 문자열을 매개변수로 **전달passing in** 하면서 그 걸 **호출call** 해봐:

![console](images/custom-function-call.gif)

또 문자열을 가르키는 변수를 매개변수로 전달하여 아까 그 함수를 호출할 수도 있어 (위의 예시에선 처음에 변수에 문자열을 저장하는 대신에, 값으로 그냥 문자열을 직접 작성했어):

![console](images/custom-function-call-variable.gif)

`makeMoreExciting(sentence)` 줄은 `sentence + '!!!!'`처럼 말하는 것과 동등해. 만약에 문장의 값을 **동일한 자리에서 수정modify in-place** (갱신update)하길 원했다면? 만약에 그렇다면 그냥 함수의 반환값을 `sentence` 변수에 다시 저장하면 돼:

    var sentence = "time for a nap"
    sentence = makeMoreExciting(sentence)

이제 `sentence` 는 감탄사 부호를 가질 거야! 변수를 **초기화initializing** 할 때만 `var`를 사용해야 한다는 걸 잊지마 &mdash; 그러니깐 그걸 완전 처음 사용할 때 말이야. 그 다음엔 `var` 를 사용하면 안돼.  변수를 다시 초기화(재설정/청소/비우기)하려는 게 아니라면 말이야.

만약에 함수안에서 `return` 문장을 빼면 어떻게 될까?

![console](images/custom-function-no-return.gif)

왜 `sentence` 가 빈 걸까? 함수가 `undefined` 를 기본으로 반환하기 때문이지! 뭔가를 `return`하면서 값을 반환하는 걸 택할 수 있어. 함수는 값을 취해야 하고, 만약에 함수가 값을 바꾸거나 나중에 사용될 예정인 다른 값을 생성하면, 어떤 값을 `return` 해 (재밌는 건 이러한 걸 나타내는 멋진 용어가 바로 *기능적인 프로그래밍functional programming* 이야). 여기 어떤 것도 반환하지 않는 대신에 결과를 보여주기 위해 다른 방법을 사용하는 또 다른 함수가 있어:

```js
function yellIt(string) {
  string = string.toUpperCase()
  string = makeMoreExciting(string)
  console.log(string)
}
```

이 함수, `yellIt`,은 우리의 이전 함수인 `makeMoreExciting` 와 내장 객체인 문자열 메소드인 [toUpperCase](https://developer.mozilla.org/en-US/docs/JavaScript/Reference/Global_Objects/String/toUpperCase)를 사용해. 메소드method 는 그냥 어떤 뭔가에 속할 때의 함수 이름이야 &mdash; 이 경우엔 `toUpperCase` 는 `String` 에 속한 함수인데 그래서 이걸 메소드 *혹은or* 함수 둘 모두로 부를 수 있어. 반면에 `makeMoreExciting` o는 다른 뭔가에 속하지 않아서 이걸 메소드로 부르는 건 기술적으로 옳지 않아. (헷갈리지, 나도 알아).

이 함수의 마지막 줄은 다른 내장 객체인데 함수에 매개변수로 준 어떠한 값이던지 가져가서 콘솔에 표시해줘.

![console](images/custom-function-console-log.gif)

그래서 뭔가 위의 `yellIt` 함수에 뭔가 잘 못된 게 있나? 그건 때에 따라 달라! 아래에 두개의 함수의 주된 형태가 있어:

  - 값을 수정하고 생성하고 그것을 돌려주는 함수
  - 값을 가져가서 (반환될 수 없는)어떤 행동을 하는 함수

`console.log` 는 두 번째 형태 함수의 한 예야: 콘솔에 무언가를 표시하는 거야 &mdash; 눈으로 볼 수 있는 행동이지만 자바스크립트 값으로는 표시될 수 없지. 내 경험상 두 형태의 함수를 각각 분리시키도록 하는 게 좋아, 그래서 이 `yellIt` 함수를 이렇게 다시 쓰겠어:

```js
function yellIt(string) {
  string = string.toUpperCase()
  return makeMoreExciting(string)
}

console.log(yellIt("i fear no human"))
```

이 방법으로 `yellIt` 가 좀 더 **일반적generic**, 이 되지, 단지 간단한 1~2개의 일을 할 뿐 콘솔에 자신을 표시하는 것에 대해선 아무것도 아는 게 없는 걸 의미해 &mdash; 그 부분은 나중에 언제라도 함수 선언의 바깥에서 개발될 수 있어.

### <a id="loops" href="#loops">#</a> 반복

우리 벨트 아래 (*저자주: 고양이가 벨트도 차나?*) 몇 가지 기본 기술을 가지고 있으니깐 이제 우리 좀 게을러 질 수 있어. 뭐?! ㅇㅇ, 맞아 진짜야: 프로그래밍은 게을러지는 거에 관한 거야. Perl 프로그래밍 언어 발명자인 래리 월Larry Wall 이 게으름을 좋은 개발자의 [가장 중요한 덕목](http://c2.com/cgi/wiki?LazinessImpatienceHubris) 이라고 불렀어. 만약에 컴퓨터가 존재하지 않으면 넌 아마 모든 종류의 지루한 작업을 직접 해야 할 거야, 그런데 네가 프로그램을 배운다면 컴퓨터가 어딘가에서 네 프로그램을 돌리는 동안에 넌 태양 아래 누워있을 수 있어. 이게 바로 안정으로 가득한 화려한 삶이야!

반복은 컴퓨터의 힘을 이용하는 가장 중요한 방법 중의 하나야. 아까 말한 `Underscore.js` 기억해? 페이지에 로드한 다음에(기억나지? 키보드 방향키중에 위를 향한 화살표 버튼을 몇 번 누르면 그 전에 입력했던 것들 목록을 훑어가면서 네가 필요한 게 나오면 `Enter` 만 누르면 돼.) 콘솔에 복사 및 붙여넣기 해봐:
  
```js
function logANumber(someNumber) {
  console.log(someNumber)
}
_.times(10, logANumber)
```

이 코드는 Underscore 의 [times](http://underscorejs.org/#times) 메소드를 사용해, 이건 하나의 숫자와 하나의 함수를 취하고선 0부터 시작해서 10번, 매번 1씩 증가하면서 단계별로 해당 숫자와 함께 그 함수를 호출하는 거야.

![console](images/times-loop.png)

위의 코드에서 `times` 이 하는 걸 그냥 직접 적으면 아래처럼 보일 거야:

```js
logANumber(0)
logANumber(1)
logANumber(2)
logANumber(3)
logANumber(4)
logANumber(5)
logANumber(6)
logANumber(7)
logANumber(8)
logANumber(9)
```

근데 냥이들은 불필요한 손작업을 안 할거야. 그러니깐 항상 이렇게 스스로 물어봐야해, *"가능한  게으르게 하고 있는 거 맞나?"*.

그래서 왜 이게 반복이라고 불리냐고? 이렇게 생각해봐: 자바스크립트 배열을 이용해서 0 부터 9 까지 10개의 숫자 목록을 적는다고 생각해보면 아래처럼 보일 거야:

```js
var zeroThroughTen = [0, 1, 2, 3, 4, 5, 6, 7, 8, 9]
```

`times` 가 하는 건 각각의 숫자를 방문해서 작업을 반복하는 거야: 위의 작업의 예제는 현재 숫자와 함께 `logANumber` 함수를 호출하는 거야. 이렇게 작업을 반복하는 게 바로 배열Array을 관통하는 *반복looping over* 이라고 불려.

### <a id="arrays" href="#arrays">#</a> 배열

몇 번 언급하긴 했었는데 좀 더 시간을 써서 이걸 좀 배워보자. 네가 네 모든 친구들의 정보를 얻어야 한다고 생각해보자구. 음, 배열Array이 딱 좋을 거 같아. 배열을 *수 만 가지 것tons*들을 담을 수 있는 어떤 분류된 목록이라고 생각해봐.

이렇게 만드는 거야:

```js
var myCatFriends = ["bill", "tabby", "ceiling"]
```

스윗! 이제 네 냐옹 친구들의 목록을 가졌네.

배열 안에 저장된 요소들(어떤 배열의 하나의 요소를 이렇게 불러)은 0 부터 시작해서 늘어나. 그래서 `myCatFriends[0]` 는 `bill` 을 반환하고 `myCatFriends[1]` 은 `tabby`... 등을 돌려줘.

네 새로운 배열의 친구들을 얻으려면 그냥 쉽게 이렇게 한 요소에 직접 접근해도 돼:

```js
console.log(myCatFriends[0])
```

![console](images/array-access.png)

만약 전날 밤에 냥쿨한 괭이클럽에서 새로운 괭이 친구를 만들고 그 친구들을 네 친구 목록에 넣고 싶다면 그건 진짜 쉬워: `myCatFriends.push("super hip cat")`.

새로운 괭이 친구가 배열에 만들어졌는 지 확인하려면 `.length`를 사용할 수 있어: 

![console](images/array-push-length.png)

`push` 가 요소 숫자를 돌려주는 방법을 눈치챘어? 완전 편리해! 글고 배열은 언제나  **순서를 지킬 거preserve ordering**라는 걸 주의해서 봐봐. 이건 바로 뭔가를 추가하거나 정의하는 순서를 항상 기억할 거라는 거야. 자바스크립트의 모든 것들이 순서를 지키진 않으니깐 배열의 이 특별한 속성을 기억해 두라구!
  
### <a id="objects" href="#objects">#</a> 객체

배열은 목록에 알맞아, 근데 다른 작업들을 하기 위해선 좀 어려울 지도 몰라. 우리 괭이 친구들 배열을 생각해봐. 만약에 그냥 이름을 추가하는 거 말고도 더 저장하고 싶은 게 있으면 어쩌지?

```js
var myCatFriends = ["bill", "tabby", "ceiling"]
var lastNames = ["the cat", "cat", "cat"]
var addresses = ["The Alley", "Grandmas House", "Attic"]
```

때론 주소나 이름 모두를 하나의 변수에 가지고 있는 게 좋아. 근데 때론 어떤 냥이가 있어, Bill 이라고 하자, 그리고 그 냥이의 주소를 찾아보길 원한다고 치자구. 배열로는 일처리를 많이 해야 해. 그냥 막 '헤이, 배열군! Bill  주소 좀 알려줘' 라고 말할 순 없거든. 왜냐면 'Bill'은 그냥 어떤 배열에 있고 그 냥이의 주소는 완전히 다른 배열에 있거든.

![console](images/array-lookup.png)

이건 좀 다루기 어려워, 왜냐면 우리가 가진 배열들이 변할 수도 있고 배열의 처음에 새로운 냥이를 추가하면 배열안에서 Bill 의 정보에 대한 새 장소를 나타내는 `billsPosition` 변수를 바꿔줘야 하거든! 이렇게 객체를 사용해서 정보를 저장하는 좀 더 쉬운 관리 방법이 여기에 있어:

```js
var firstCat = { name: "bill", lastName: "the cat", address: "The Alley" }
var secondCat = { name: "tabby", lastName: "cat", address: "Grandmas House" }
var thirdCat = { name: "ceiling", lastName: "cat", address: "Attic" }
```
  
왜 이렇게 해야하는 거야? 각각의 냥이에 대한 변수를 가지고 있어서 좀 더 편하고 읽기 쉬운 방법으로 각 냥이 변수에 대한 정보를 얻을 수 있기 때문이야.

![console](images/object-lookup.png)

객체를 마치 열쇠고리의 열쇠 하나와 같이 생각할 수도 있어. 각각의 열쇠는 개별 문에 대한 것이고 만약 열쇠에 라벨을 잘 붙여놓는다면 문을 정말 빨리 열 수 있을 거야. 사실말야, `:`(콜론)의 왼쪽에 있는 건 **keys** 라고 불리고 (혹은 속성 **properties**이라고도 알려져 있어)  그 오른쪽에 있는 건 **값values**이라고 불려.

```js
// 단일키'name' 과 단일값'bill'으로 이뤄진 객체
{ name: 'bill' }
```

그럼 객체에 정보를 넣을 수 있는데 왜 이전에 배열을 사용한 거지? 그건 객체는 네가 설정한 키의 순서를 기억하지 않기 때문이야. 어떤 객체를 이렇게 입력할 수도 있어:

```js
{ date: "10/20/2012", diary: "slept a bit today", name: "Charles" }
```

근데 컴퓨터는 아래처럼 너한테 되돌려 줄 수도 있어:

```js
{ diary: "slept a bit today", name: "Charles", date: "10/20/2012" }
```

혹은 이렇게!

```js
{ name: "Charles", diary: "slept a bit today", date: "10/20/2012" }
```

그래서 넌 객체내의 키 순서를 전혀 믿을 수 없는 거야. 만약에 진짜 완전 멋진 걸 원하면 객체로 이뤄진 배열을 만들 수 있어, 혹은 배열로 이뤄진 객체라던가!

```js
var moodLog = [
  {
    date: "10/20/2012",
    mood: "catnipped"
  }, 
  {
    date: "10/21/2012",
    mood: "nonplussed"
  },
  {
    date: "10/22/2012",
    mood: "purring"
  }
]

// 가장 덜 좋아하는 것부터 가장 좋아하는 순의 정렬
var favorites = {
  treats: ["bird sighting", "belly rub", "catnip"],
  napSpots: ["couch", "planter box", "human face"]
}
```

네가 이렇게 다른 것들을 결합할 때 **데이터 구조data structures**를 만드는 거야, 마치 레고처럼!

### <a id="callbacks" href="#callbacks">#</a> 콜백(회수/ 호출)

사실 Callback호출은 `Object` 나 `Array`, 같은 자바스크립트 특징이 아니야. 그냥 함수를 사용하는 특정 방법이라고 할까? 그런 거야. 그냥 콜백이라고 할게, 콜백이 왜 유용한 건지 이해하려면 우선 비동기적인 프로그래밍asynchronous (주로 짧게 async)을 배워야해. 정의에 의하면, 비동기 코드는 동시에 일어나지 않는 방식으로 작성된 코드야. 동시에 발생하는 코드는 이해하고 작성하기가 쉬워. 묘사하는 예를 보여줄게:

```js
var photo = download('http://foo-chan.com/images/sp.jpg')
uploadPhotoTweet(photo, '@maxogden')
```

이건 동시에 일어나는 가상 코드 [pseudo-code](http://simple.wikipedia.org/wiki/Pseudocode) (기계가 아닌 인간의 언어로 쓰인 소스코드 형태인데 알고리즘이 어떻게 필요한 작업을 달성하는 지 보여주기 위해 쓰여.)는 사랑스러운 냥이 사진을 다운로드해서 트위터에 업로드한 다음에 `@maxogden`에게 트윗할거야. 굉장히 직접적이지!

(*작자주: 나 @maxogden 은  언제나 어떤 고양이 사진 트윗이든 기쁘게 받는다궁.*)
(*역자주: 하지만 번역의 시점에서 작자의 트윗은 @denormalize 으로 변경되었다냥.*)

이 코드는 동시에 일어나. 왜냐면 사진이 트윗에 업로드되기 위해서 사진 다운로드가 우선 끝나야해서야. 이건 첫번째 줄의 작업이 완전히 끝나기 전엔 두번째 줄의 작업이 실행될 수 없다는 걸 말하는 거야. 만약에 이 가상 코드를 실제로 실행한다면, 다운로드가 끝나기 전까진 `download` 가 실행을 '막길blocked' 바랄거야. 이건 다시 말하면 다운로드가 끝나기 전까진 어떠한 다른 자바스크립트의 실행도 방지되고 다운로드가 끝나자마자 자바스크립트 실행을 막는 것을 풀고 2번째 줄부터 시작될 거라는 걸 의미해.

동시에 일어나는 코드는 빨리 발생하는 뭔가에는 괜찮아. 그런데, 뭔가 저장하고 불러오고, 다운로드하고 업로드를 요구하는 거엔 좀 끔찍할 정도로 부적절해. 만약에 네가 사진을 다운로드 받고 있는 서버가 느리면 어떻게 해, 아니면 네가 사용하고 있는 인터넷 연결이 느릴 수도 있어, 아니면 네가 코드를 돌리고 있는 컴퓨터가 엄청나게 많은 냥이 유투브 동영상을 켜놓은 탭을 가지고 있고 느리거나 하면 말이야. 그건 그러니깐 잠재적으로는 2번째 줄이 돌아가기 전에 몇 분동안 기다릴 수도 있다는 거야. 반면에 다운로드가 되고 있을 때, 페이지내 모든 자바스크립트의 실행이 막혀있으면 웹페이지는 완전히 그냥 멈춰버리고 다운로드가 다 되기 전까진 그냥 아무반응도 없을 거야.

실행을 막는 건 그 비용이 얼마가 들더라도 방지되어야 해. 특히 그렇게 하는 건 네가 만든 프로그램을 완전히 얼어버리게 하거나 반응이 없도록 할거야. 위의 사진이 다운로드되는데 일 초가 걸린다고 가정해 보자. 현대의 컴퓨터한테 1초가 얼마나 오랫동안 인지 나타내기 위해서, 여기에 1초 동안 자바스크립트가 실행할 수 있는 작업이 얼마나 많은 지 보여주기 위한 테스트 프로그램이 있어.

```js
function measureLoopSpeed() {
  var count = 0
  function addOne() { count = count + 1 }

  // Date.now() 는 어떤 큰 수를 반환하는데,
  // 이 수는 1970년 1월 1일 이후로 누적된 1/1000 초의 숫자야.
  var now = Date.now()

  // 우리가 반복을 시작할 때부터 Date.now()가 1000 밀리초(즉, 1초)가 되거나 그 이상이 될 때까지 반복. 
  // 각각의 반복에서 addOne 함수를 호출해.
  while (Date.now() - now < 1000) addOne()
  
  // 마지막에 그 값이 1000ms 보다 크거나 같아지면 우리의 총 count를 출력해보자.
  console.log(count)
}

measureLoopSpeed()
```

위의 코드를 복사한 다음 자바스크립트 콘솔 창에 붙여넣기하고 나서 1초가 지나면 어떤 숫자가 출력될 거야. 내 컴퓨터에서 난 `8527360` 이란 숫자가 나왔어, 대략 **8.5 million** 이지. 1초 동안에 자바스크립트가 `addOne` 함수를 850 만번 정도 호출할 수 있다는 거야! 만약에 네가 동시에 발생하는 코드(사진을 다운로드하는)를 가지고 있다면, 사진을 다운로드하는 데 1초가 걸리는 거야, 다시 말하면 자바스크립트 실행이 가로막혀서 잠재적으론 850만개의 실행이 발생치 못하도록 막는 거랑 같은 거야.

몇몇 언어들은 몇 초간 실행을 막는 `sleep` 이라는 함수를 가지고 있어. 예를 들면, `sleep` 을 사용하는 Mac OS 의 `Terminal.app` 에서 돌아가는 [`bash`](http://en.wikipedia.org/wiki/Bash_%28Unix_shell%29) 코드가 있어. `sleep 3 && echo 'done sleeping now'` 라는 명령을 실행시키면 `done sleeping now` 를 출력하기 전에 3초간 차단될 거야.

![console](images/bash-sleep.png)

자바스크립트는 `sleep` 함수를 가지고 있지 않아. 넌 냐옹이니까 아마 너 스스로에게 이렇게 묻겠지, "왜 내가 잠자는 거랑은 관련도 없는 프로그래밍 언어를 배우는 거지?" 잠깐만 있어봐. 뭔가 발생하기를 기다리기 위해 `sleep` 에 의지하기 보단 자바스크립트 고안은 함수를 사용하라고 권장해. 만약에 네가 업무B를 하기 전에 업무A가 끝나기를 기다려야 하면, 업무B를 위한 모든 코드를 한 함수에 넣고 업무A가 완료되면 그 때 그 함수를 호출하면 돼.

가령, 이게 바로 차단방식의 코드야:

```js
a()
b()
```

이건 비차단방식의 코드야:

```js
a(b)
```

차단이 없는 방식에서 `b`가 바로 `a` 에 대한 콜백이야. 차단방식에선 `a`와 `b` 둘 모두 호출되거나/발동되는 거야(둘 모두 뒤따르는 `()`를 가지는데 이건 함수를 즉시 실행하는 거야). 차단이 없는 방식에서 아마 `a`만 발동되고 `b`는 단순히 `a`의 In the non-blocking version you will notice that only `a` gets invoked, and `b` is simply passed in to `a` as an argument.

In the blocking version, there is no explicit relationship between `a` and `b`. In the non-blocking version it becomes `a`'s job to do what it needs to do and then call `b` when it is done. Using functions in this way is called callbacks because your callback function, in this case `b`, gets called later on when `a` is all done.

Here is a pseudocode implementation of what `a` might look like:

```js
function a(done) {
  download('https://pbs.twimg.com/media/B4DDWBrCEAA8u4O.jpg:large', function doneDownloading(error, png) {
    // handle error if there was one
    if (err) console.log('uh-oh!', error)
    
    // call done when you are all done
    done()
  })
}
```

Think back to our non-blocking example, `a(b)`, where we call `a` and pass in `b` as the first argument. In the function definition for `a` above the `done` argument *is* our `b` function that we pass in. This behavior is something that is hard to wrap your head around at first. When you call a function, the arguments you pass in won't have the same variable names when they are in the function. In this case what we call `b` is called `done` inside the function. But `b` and `done` are just variable names that point to the same underlying function. Usually callback functions are labelled something like `done` or `callback` to make it clear that they are functions that should be called when the current function is done.

So, as long as `a` does it's job and called `b` when it is done, both `a` and `b` get called in both the non-blocking and blocking versions. The difference is that in the non-blocking version we don't have to halt execution of JavaScript. In general non-blocking style is where you write every function so that it can return as soon as possible, without ever blocking.

To drive the point home even further: If `a` takes one second to complete, and you use the blocking version, it means you can only do one thing. If you use the non-blocking version (aka use callbacks) you can do *literally millions* of other things in that same second, which means you can finish your work millions of times faster and sleep the rest of the day.

Remember: programming is all about laziness and you should be the one sleeping, not your computer.

Hopefully you can see now that callbacks are just functions that call other functions after some asynchronous task. Common examples of asynchronous tasks are things like reading a photo, downloading a song, uploading a picture, talking to a database, waiting for a user to hit a key or click on someone, etc. Anything that takes time. JavaScript is really great at handling asynchronous tasks like these as long as you take the time to learn how to use callbacks and keep your JavaScript from being blocked.

## The end!

This is just the beginning of your relationship with JavaScript! You can't learn it all at once, but you should find what works for you and try to learn all of the concepts here.

I'd recommend coming back again tomorrow and going through the entire thing again from the beginning! It might take a few times through before you get everything (programming is hard). Just try to avoid reading this page in any rooms that contain shiny objects . . . they can be incredibly distracting.

Got another topic you wanna see covered? Open an issue for it [on github](http://github.com/maxogden/javascript-for-cats).

### <a id="recommended-reading" href="#recommended-reading">#</a> Recommended reading

  JavaScript For Cats skips over lots of details that aren't important for getting started (cats are not known for their attention spans), but if you feel like you need to dive in deeper then check these out:
  
  - [NodeSchool.io](http://nodeschool.io/) is a community driven, open source educational software that teaches various web development skills in an interactive, self-guided format. I helped make NodeSchool! Sadly it features fewer cats than this page. 
  - [Eloquent Javascript](http://eloquentjavascript.net/) is a free book that teaches you JavaScript! It's pretty good! Especially the chapter on [values, variables, and control flow](http://eloquentjavascript.net/chapter2.html)
  - [Mozilla's JavaScript Guide](https://developer.mozilla.org/en-US/docs/JavaScript/Guide) also has a pretty sweet intro chapter called [values, variables and literals](https://developer.mozilla.org/en-US/docs/JavaScript/Guide/Values,_variables,_and_literals)
  - [`standard` JS Style Guide](https://github.com/feross/standard) is a "zero configuration" linter for JS style that I use
  - [Let's Write Code by @shama](https://github.com/shama/letswritecode) a great series of YouTube coding tutorials made by a friend of mine

<hr>
### <a id="satisfied-customers" href="#satisfied-customers">#</a> Satisfied customers
<center>![satisfied customer](images/customers5.jpg)</center>
<center>![satisfied customer](images/customers1.png)</center>
<center>![satisfied customer](images/customers2.png)</center>
<center>![satisfied customer](images/customers3.png)</center>
<center>![satisfied customer](images/customers4.png)</center>

*JSForCats.com is a labor of love and work in progress by [@maxogden](http://twitter.com/maxogden). If you would like to contribute and make this tutorial better there is a Github repo [right over here](http://github.com/maxogden/javascript-for-cats).*
<center>![console](images/awesome.jpg)</center>
