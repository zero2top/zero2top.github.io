---
layout: single
title: "람다표현식 (Lambda Expression) + 익명메소드"
---
#Today I Learned


오늘은 <span style="background-color:#87CEFE">람다표현식</span>에 대해서 알아보았다.   
람다표현식은 자바8 부터 지원되기 시작한 기능이다.   
람다표현식에 대해 알아보기 전에 함수형 인터페이스(Functional Interface)에 대해서 알아보자.   
함수형 인터페이스란 <span style="color: red">추상메소드가 하나뿐인</span> 인터페이스를 부르는 말이다.  
아래의 코드와 같이 작성할 수 있으며 어노테이션으로 이것이 FunctionalInterface임을 알려준다.    
<script src="https://gist.github.com/zero2top/5279adf0baa671311312b7930bdae0db.js"></script>  
이때 interface의 default 메소드나 static method의 수는 상관없이 추상메소드가 하나라면 모두 함수형 인터페이스이다.  
  
이제 함수형 인터페이스에 대해서 알아보았으니 다음으로 오늘의 주제인 람다표현식에 대해 알아보겠다.  
일반적인 방법으로 함수형 인터페이스를 인스턴스화해서 사용하게되면 별다른 문제는 없지만 우리가 사용하고 있는 것이 함수형 인터페이스 임을 주목해야한다.  
즉 우리가 Overriding해줘야 할 추상메소드가 단 하나뿐이기 때문에 이런 메소드의 이름을 굳이 다시 명시해서 Overriding을 하는 것보다 
이미 알고 있기 때문에 생략하고 인스턴스화 할 수 있게 한 것이 람다표현식이다.  
아래의 코드에서 그 예시를 보자.    
<script src="https://gist.github.com/zero2top/422b9402739c72a522aef3f729837a56.js"></script>
  
원래 Flyable 인터페이스의 추상메소드의 이름인 fly와 new Flyable() 등을 생략한 것을 볼 수 있다.   
이렇게 추상메소드의 이름을 생략했기 때문에 이를 익명메소드라고 부른다.  
람다표현식을 사용함으로서 첫 번째의   긴코드가 한줄로 줄어든 것을 볼 수있다.  









