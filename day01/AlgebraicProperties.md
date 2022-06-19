# Algebraic Properties

이 아래 법칙은 모든 연산에 적용되는 것은 아니고, 이것이 적용된다고 증명된 연산에서 사용할 수 있는 법칙 같다고 생각함.  
아래 법칙을 규정하는데 사용되는 모든 연산자나, 변수는 특정 연산자를 가르키는 것이아니라, abstract 하다고 생각하면 됨.

## Commutative Property (Law)

$a \diamond b = b \diamond x$

각 LHS, RHS 의 Variables 의 순서를 바꿔도 동등성이 성립함. 예를 들면 아래 처럼

$b \diamond a = x \diamond b$

## Associative Property (Law)

$(a \circ b) \diamond c = c \diamond (a \circ b)$

## Destributive Property (Law)

$(a \circ b) \diamond c =  (a \circ b) \diamond (a \circ c)$

## Identities and Inverse

- Identity : 어떤 variable (a) 와 연산 (x) 가 있을때, 이 값을 진행한 결과가 원래의 값과 동일하게 만드는 값.

$a \diamond e = a$

이 식을 봤을때 가장 중요한 점은 **e 라는 녀석은 a 에 $\diamond$ 이라는 연산으로 영향을 끼쳤을때, 결과에 아무런 영향을 주지 않는다는 사실**이다. 이걸 꼭 명심하고 있어야 한다.

- Inverse : 어떤 variable (a) 와 연산 (x) 가 있을때 이 값에 연산을 진행한 결과 Identity 를 가르키게 만드는 값. (여기서 `e` 는 identity 임.)

$a \diamond x = e$

즉, `x` 는 $\diamond$ 연산에 대한 inverse 이다.

## Variables And Contant

- **Constant**: 계산 중에 절대 변하지 않는 값.
- **Variables**: 함수의 입출력과 같이 상황에 따라 달라질 수 있는 값. (보통 x, y, z 로 표현을 많이 함.)
- **Confficients**: 변수에 곱해지는 상수
    - $3*x^2$ 에서 3 은 Confficients 임.

# Equations

$(LHS)=(RHS)$

LHS 의 어떤 값이 대입되거나, RHS 에 어떤 값이 대입되느냐에 따라 방정식은 서로 같음이 만족할수도, 만족하지 않을 수도 있음. 
이런 상황에서 **LHS 와 RHS 가 같음을 만족하는 경우를 찾는 것**을, **Solution of Equations** 라고 함.

방정식을 보며 느낀점이 하나 있는데 우리가 **Multi-Thread 상황에서 Programming 에서 Function 을 다룰때, 대부분은 $(LHS)=(RHS)$ 을 만족하기 힘든 상황**이다. 
그래서 마틴파울러의 책을 보면 **Immutable 하게 변수를 다루거나, 혹은 deepCopy 를 하는 연습**을 많이 해라. 라고 나와 있는데, 이 책을 보면서 아 왜 그런말이 나오게 됬는지 조금씩 이해하게 됬다. 
그래서 Mutlti-Thread 상황에서 우리가 Function 의 Thread-Safety 를 만족하지 못하는 상황에서, 테스트를 하는 것은 결국에 **Solution of Equations** 을 하는 것과 같은데, 이 상황에서 테스트를 짜는 것이 유의미한가? 라는 생각이 들었다. 그래서 테스트를 짜기전에 **Thread-Safety** 함을 먼져 증명하고, 그 뒤에 **Solution of Equations** 을 하는것이 맞다는 생각이 들었다.

## Basic Rule for Solution of Equations

- LHS 와 RHS 에 같은 값을 더해도 관계는 변하지 않음.
    - $(LHS) + a =(RHS) + a$
- LHS 와 RHS 에 같은 값을 곱해도 관계는 변하지 않음. (단 $a \neq 0$)
    - $(LHS) * a =(RHS) * a$

## Simple Example

- $x + 2 = 0$ 이 되는 x 의 값을 구하시오.

**Solution**

1. $(x + 2) - 2 = 0$ ----> 가장 간단하게 LHS 와 RHS 를 만들기 위해 방정식에 `+2` 의 inverse 인 `-2` 를 더해준다.

2. $x + (2 - 2) = 0 - 2$ ---> associative law 를 통해 $(x + 2) - 2$ 를 $x + (2 - 2)$ 로 변경해준다.

3. $x = -2$ ---> 이 방정식의 Solution 은 -2 이다.

이렇게 풀이를 하다보면 한가지 느끼는데 어렸을때 우리는 LHS 의 값 또는 변수를 RHS 로 넘겼을때 $- * constant$ 가 된다고 배웠다. 
그니까 간단한 예시로 들자면 $x - 2 = y$ 가 있을때, LHS 에 있는 `-2` 를 넘기면 RHS 에서는 `+2` 가 되는 것이다. 즉, 이런 방정식이 만들어진다. $x = y + 2$ 
근데 이게 무엇일까? 바로 Inverse 를 LHS 와 RHS 에 더해준것이다. 이걸 한번 이어서 보도록 하자.

1. $(x - 2) + 2 = y + 2$ ----> 양 LHS 와 RHS 에 inverse 인 2 를 더해줬음
2. $x = y + 2$ ----> 즉, 어렸을때 우리가 배웠던 개념이 나온다.

### 수학을 공부하는 이유

사실, 실무에 지금당장 엄청 큰 도움을 줄거라고 생각하지는 않는다. 하지만, 내 생각엔 뭐든 배우면 직/간접적으로 라도 긍정적인 영향을 끼친다고 생각한다. 위에서 말한 Multi-Thread 상황의 Function Test 를 방정식 풀이로 해석할 수 있듯이. 그래서 조금씩 공부하고, 프로그래밍에서는 이를 어떻게 표현했을까를 적어보려고 한다. 매일 50분씩 하다보면 언젠간 어려운것도 풀수 있겠지라는 생각을 가지고, 조금씩 꾸준하게 공부해보려고 한다.