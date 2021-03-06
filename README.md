# spring-aop
About Spring AOP

# Development Environment<br/>
Spring simple maven project<br>
JAVA : 1.8<br>
IDE : STS(Spring Tool Suite 3.7.2 Release)<br>

# AOP란?
Aspect Oriented Programming의 약자입니다. 우리나라 말로 말하면 관점 지향 프로그래밍입니다. 이것은 관점을 외부에서 주입하는 프로그래밍 스타일을 말하는 것입니다. AOP에서 관점이라는 것은 일반적으로 횡단적 관심사를 말을 합니다. 이것은 클래스의 종류에 관게 없이 다양한 곳에서 공통으로 사용되는 기능을 말합니다.
<br><br>
예를 들면, 프로그래밍을 개발할 때 디버그용으로 이곳 저곳에 System.out.println 문을 써서 변수 또는 내용 확인을 하는 사람들 있지 않으신가요? 메소드를 호출할 시에 실행한 후에는 필요한 값을 호출하는 작업입니다. 이곳 저곳에서 이런 작업을 통해 실행상황을 파악 할 수 있고 개발할 시에도 여러가지로 도움이 되는 정보를 얻을 수 있습니다.
<br><br>
하지만 이런 방식은 아주 큰 문제점이 있습니다. 개발 할 시 유용하게 사용했지만 프로그램이 완성되고 릴리스를 할 시 보안상 또는 성능 최적화에 문제가 되는 고로 삭제 해야 되는 경우입니다. 한 두개면 금방 찾아서 삭제 할 수 있지만 복잡한 프로그램일 수록 이런 작업들은 힘들게 될 것입니다. 이 때, 이런 생각을 할지도 모릅니다. "개발이 끝나면 System.out.println이 한번에 다 삭제 되었으면 좋겠다" 라고 말입니다. 바로 이것이 위에서 말씀 드린 횡단적 관심사가 되는 것입니다.
<br><br>

# Aspect의 구조
1. Advice
   - Before
   - After
   - Around
2. JoinPoint
3. PointCut
<br>

# AOP 관련의 dependency
AOP관련 의존성은 다음과 같습니다.<br>
  - Spring AOP : Spring이 제공하는 AOP의 프레임워크.<br>
  - Aspectjrt : AspectJ라고 하는 AOP프레임워크를 제공하는 라이브러리.<br>
  - Aspectj Weaver : AspectJ를 활용하기위한 기능을 제공하는 라이브러리.<br>
<br>
 이 세개는 Spring에서 활용하는 경우, 세트로 생각해 주시면 됩니다. AspectJ는 Spring Framework가 아니고 Xerox Palo Alto연구소에서 개발되어 지고 있고, 현재는 Eclipse Foundation의 프로젝트로서 개발이 진행되어지고 있는 오픈소스 프레임워크 입니다. 이 AspectJ가 AOP의 구현체라고 보시면 됩니다. 그래서 Spring AOP뿐만 아니라 자바에서의 AOP관련 프레임워크나 라이브러리는 대부분의 것이 AspectJ를 사용하고 있습니다. 즉, 기본적인 Spring AOP의 사용방법으로서 학습을 하지만 그 베이스에는 AspectJ라는 것이 사용되어 지는구나 라고 생각해주시면 되겠습니다.
