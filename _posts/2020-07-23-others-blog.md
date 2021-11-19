---
layout: post
title: "[Blog] How to make github blog?"
subtitle:   "first post"
categories: others
tags: github blog
comments: true
---




github를 이용한 마크다운 연습하기 1..
---


본 블로그는 'https://gist.github.com/ninanung/73addc0263b34da5f021d2f02a356b7f'를 보고 그저 따라한것입니다  


------------------------------------------------


## 1.리스트와 인용구


#### 1-1. 리스트


리스트는 점점 작은 부분을 설명할떄 사용한다. 예를 들면

* 머리
  * 코
  * 입
    * 입술

+ 머리
  + 코
    + 입

- 머리
- 코
- 입

이런식으로 표현 가능하다. 이떄 'tap'키를 사용하지 않으면 구분이 지어지지 않게 된다.
또한 이는 숫자로 표현가능한데

1. 광배
5. 어깨
3. 다리

이런식으로 사용가능하다. 이때 html의 <li> 형태로 바꿔주는 것이기 때문에 숫자의 의미는 없고 단지 순서만이 적용된다.  
역슬레시는 다른 문법에 쓰이는 특수문자를 문법으로가 아니라 그냥 화면에 출력하고 싶을 경우에도 사용 가능하다.  
\(특수문자) 이런식으로 말이다

마지막으로

    1. 머리
     * 머리카락
     * 뚝배기
    2. 다리
     *다리털
     *발가락
  
위와같이 두가지를 섞어서 사용하는 것도 가능하다. 결과는

1. 머리
  * 머리카락
  * 뚝배기
2. 다리
  * 다리털
  * 발가락 
  
  위와 같다
  
--------------------------------


#### 1-2.인용구(BlockQuote)

인용구는 위에서 처음에 예시를 들때 사용했던  
> 으아아아ㅏㅏ

와 같은 부분입니다. 말 그대로 어떤 부분을 인용하거나 특수한 강조를 주고 싶을때 사용합니다.
코드는 다음과 같습니다.  

    > 어머니 아버지
    >> 천원만 주세요
    >>> 그렇습니다.  
  
보면 아시겠지만 몊번이고 겹치는 것이 가능합니다 참고로 저 인용구 안에는 1장에서 설명했던 제목이나 방금 설명한 리스트를 넣을 수 있습니다.  예를 들면 

    > #this is h1
    > * list
    > 'textbox'  
    
실제로는 
> # this is h1
> * list
> `textbox`
와 같이 보이게 됩니다.

-----------------------------

## 2. 개행과 문자강조

#### 3-1. 개행
어떻게 하면 줄을 바꾸는 것일까? 코드를 보자

    나는 아름다운 나비
    날게를 활짝 펴고
    세상을 아름답게 날거야
    
그저 한글이나 텍스트 처럼 그냥 줄을 뛴 것 뿐이잔아! 라고 생각할지도 모르지만 사실은 그게아니리.  
그줄의 맨끝에 2번이상 스페이스바를 눌러주면 개행이 된다 실제로 해보면

나는 아름다운 나비  
날게를 활짝 펴고  
세상을 아름답게 날거야  

처럼 줄이 띄어져서 보여지게 된다. 그렇다면 줄을 띄는 것말고 아예 줄을 한칸 띄고 싶으면 어떻게 할까?  
줄넘기기에 대해 코드를 먼저 알아 보겠다

    나는 아름다운 나비
    
    날게를 활짝 펴고
    
    세상을 아름답게 날거야
    
무엇이 다른지 보이는가? 아예 중간에 줄을 한 칸 띈것이다 이렇게 하면 원하는 것 처럼 줄이 띄어지게 된다. 실제 결과를 보면

나는 아름다운 나비

날게를 활짝 펴고

세상을 아름답게 날거야

이렇게 나오게 된다.  
개행과 다른 점은 직접 해보는 편이 좋지만 띄어지는 간격이 다르다 당연하겠지만 개행보다는 아예 칸을 띄는 편이 더 간격이 넓다.

개행과 줄넘김에서는 한 가지 주의해야할 점이 있다. 전의 2장에서 설명한 리스트나 인용같은 경우를 사용할때

    * 우리가 누구
    * 파워레인저
    저는 절대 아닙니다.
    
와 같이 리스트나 인용이 끝나고 다른 평문을 사용할 때 줄넘기기가 아닌 단순한 개행을 사용하면  

* 우리가 누구  
* 파워레인저  
저는 절대 아닙니다.

와 같이 나오게 된다. 밑에 쓴 평문이 이전의 리스트나 인용에 같이 말려들어가 버리게된다. 이는 1장에서 설명한 제목에서도 같다.  

    너의 이름은.
    파아워어레인저!
    =======
    
와 같이 제목부분을 작성하면

너의 이름은.
파아워어레인저!
===========

와 같이 붙어버리게 된다. 따라서 위에 잘못된 부분을 고치려면 개행이 아닌 줄넘기기를 사용해야한다

    *우리가 누구
    *파워레인저
    
    저는 절대 아닙니다.
    
    너의이름은.
    
    파아워어레인저!
    ====
    
위와 같이 적절하게 사용해야 제대로 출력이 되게된다.

----------------------------------------------------

#### 3-2. 문자강조 

문자강조는 한글이나 워드에서 사용하던 이탈릭(기울임체)이나 굵은 글씨등을 말한다. 사실 상당히 간단하지만 마크다운의 특성상 겹치는 특수문가  
많아서 따로 설명하겠다. 우선 이탈릭이다.

    *오늘나는 삐딱하게*
    _시겟바늘처럼 기울어진 우리인생_
    
코드는 이와 같다. 이는 아까 본 리스트의 형태와 비슷하지만 특수문자뒤에 띄어쓰기를 하지않는다던가 뒤에 한번 더 붙힌다던가의 차이를 보인다.  
실제로 실행화면은

*오늘나는 삐딱하게*
_시겟바늘처럼 기울어진 우리인생_

와 같이 나오게 된다.  
다음은 굵은 글씨이다. 코드는

    **오늘 나는 삐딱하지는 않지만 굵은 글씨**
    __운동을 좀 해서 글씨가 굵어짐__
    
와 같은 코드이다 실제로 화면에서는

**오늘 나는 삐딱하지는 않지만 굵은 글씨**
__운동을 좀 해서 글씨가 굵어짐__

와 같이 나오게 된다. 참고로 둘다 동시에 사용하는 것이 가능하다

__귥은글씨로 시작해서 *이탈릭으로 돌아왔다가* 다시 귥어짐__

요런식으로 응용 가능하다.













