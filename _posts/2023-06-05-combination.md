---
layout: single
title: "자바로 combination 구현하기"
---
# Today I Learned
## 자바로 Combination 구현하기

자바로 Combination(조합)을 구현하는 법에 대해 공부해보자.

![combination](https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdn%2FtOLAu%2FbtqLW7y99Kz%2FgJJAu6ivbq4juqrduRKZdk%2Fimg.png)

우리가 알고있는 조합의 공식이다. n개중 순서상관없이 r개를 택할때의 경우의 수를 의미한다.
그렇다면 이 조합을 어떻게 구현할 수 있을까.

크게 3가지의 방법이있다. 
그중 **첫번째**는 factorial 메소드를 구현해서 위의 공식대로 
연산을 해주는 것이다.

재귀형식의 factorial 메소드를 만들어서 Combination을 구할 수 있다.
아래는 factorial 메소드와 예시로 Combination계산한 코드이다.
+ **방법 1**

<script src="https://gist.github.com/zero2top/d09521b0b1b8bedb67ada501246271e7.js"></script>

위의 방식은 factorial 메소드를 구현해서 combination의 공식의 분모와 분자를 각각 계산하는 방식이다.
combination을 한번에 계산할 수 있는 방법은 없을까. 물론 있다. 
그 방법이 **두 번째** 방법이다.

그 방법을 설명하기 전에 두 가지 성질에 대해서 알고 넘어가야 한다.

[성질 1]

![properties_1.1](https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdn%2FbU47D7%2FbtqLRj8WSXh%2FwTVCIKq9jnHrLFlOoUEzRk%2Fimg.png)

위의 공식을 다른방식으로 표현하면 아래와 같다.

![properties_1.2](https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdn%2FdjY4V9%2FbtqLVaQIrIv%2FuZU1zCHvXUNIF1SDlsIXhk%2Fimg.png)

이 표현법은 대학에 와서 처음 알게 되었다.
알고보니 지금까지 고등학교에서 배웠던 Combination 표현법은 오히려 잘 쓰지 않는 표현법이라고 하셨다.
n과 r의 이항계수를 구한다고 하면 아래와 같이 표현할 수 있다.

![properties_1.3](https://img1.daumcdn.net/thumb/R1280x0/?
scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdn%2F5jwvu%2FbtqLW9wX1pa%2FbHQudBGjqPuXtV2hEYCmjk%2Fimg.png)

이 점화식은 파스칼의 법칙 이라고 불린다.


[성질 2]

![poperties_2.1](https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdn%2FbHrtFN%2FbtqLSOm5H1J%2FP1VPuWEAa7VdYWNvFelOEK%2Fimg.png)

역시 다른 표현법으로 표현하면 아래와 같다.

![properties_2.2](https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdn%2FlEoZj%2FbtqLSOghHI9%2F5fb7fXT3m6bK5Sm35mscKk%2Fimg.png)

n개중 0개를 택하거나 n개중 n개를 택하는 경우의 수는 1이라는 사실은 자명하다.

이제 위의 두 가지의 성질을 이용해서 combination 메소드를 아래와 같이 구현할 수 있다.

+ **방법 2**

<script src="https://gist.github.com/zero2top/51dfd388dae621b7973d3f41b6390466.js"></script>

위의 방법은 첫 번째 방법보다는 괜찮아보이지만 문제가 하나 있다.
바로 이미 계산한 결과에 대해서 다시한번 호출을 통해 계산을 한다는 것이 문제이다.
예를 들자면  (블라블라 추가 첨삭 필요)

이를 코드로 구현하면 아래와 같다.
+ **방법 3**

<script src="https://gist.github.com/zero2top/70c2152f7a0eb09343896bee36488a5e.js"></script>

이렇게 combination 구현 방법들에 대해서 공부해봤다.
이 포스팅이 내가 올리는 첫 번째 포스팅이다.
앞으로 공부한 것들을 꾸준히 올릴 예정이다.



### 내용과 그림은 [여기](https://st-lab.tistory.com/159#%EC%95%8C%EA%B3%A0%EB%A6%AC%EC%A6%98)에서 참고했다.





