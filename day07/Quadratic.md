# Quadraticn Expression

$ax^2 + bx + c$
- x: variable
- a,b,c: constant
- a 는 $x^2$ 의 coefficients

## Multiplication Rules Of Quadraticn Expression

- $(a + b)^2 = a^2 + 2ab+ b^2$

- $(a + b)^2 = (a + b) * (a + b)$
    - $(a + b)^2 = (\alpha) * (a + b), \alpha = a + b$ 
    - $(a + b)^2 = (\alpha) * a + (\alpha) * b$ 
    - $(a + b)^2 = (a + b) * a + (a + b) * b$ **by distributivity law**
    - $(a + b)^2 = a^2 + 2ab+ b^2$

대치나 지금까지의 곱셈법칙을 통해서 천천히 푸는 습관을 들여야 함.

- $(a + b) * (a - b) = \alpha * (a - b), \alpha = a + b$
    - $(a + b) * (a - b) = \alpha * a - \alpha * b$ - distributivity law
    - $(a + b) * (a - b) = (a + b) * a - (a + b) * b$ - distributivity law 
    - $(a + b) * (a - b) = a^2 + ba - ab + b^2$
    - $(a + b) * (a - b) = a^2 + ab - ab + b^2$ - commutiavity law
    - $(a + b) * (a - b) = a^2 + b^2$

- $(ax + b)(cx + d) = a * (x + b/a) * c *(x + d/c)$
    - $(ax + b)(cx + d) = ac * (x + b/a) * (x + d/c), using (a + b)^2 = a^2 + 2ab+ b^2$
    - $(ax + b)(cx + d) = ac * (x^2 + (b/a + d/c)x + bd/ac)$
    - $(ax + b)(cx + d) = acx^2 + (cb + ad)x + bd$

## Factorizations Rules Of Quadraticn Expression

- $x^2 - 4x + 4 = (x - 2)^2$
    - $x^2 - 4x + 4 = (x - 2) * (x - 2)$
    - $x^2 - 4x + 4 = \alpha * (x - 2), \alpha = (x - 2)$
    - $x^2 - 4x + 4 = \alpha x - 2\alpha, \alpha = (x - 2)$
    - $x^2 - 4x + 4 = (x - 2) * x - 2(x - 2)$
    - $x^2 - 4x + 4 = x^2 -2x -2x -4$
    - $x^2 - 4x + 4 = x^2 -4x -4$
    - 방정식이 0 이 되기위한 solution 은 {0} 이다.
    - The solution is zero that equations to be zero

- $x^2 -4x + 4 = x^2 -(2+2)x + (2^2), by (a + b)^2 = a^2 + (a+b)x+ b^2$

- $x^2 -3x + 2 = x^2 -(2+1)x + (2*1), by (a + b)(a + c) = a^2 + (b+c)a+ bc$

## Two Representations Of Quadraticn Expression

$ax^2 + bx + c \longrightarrow a(x - p)^2 + q, vertex = (p,q)$

위와 같이 표현하면 Solution 을 구하기도 쉽고, 그래프를 그릴때 더 편함.

- $ax^2 + bx + c = a(x^2 + b/ax + c/a)$
    - $ax^2 + bx + c = x^2 + bx + c, if a = 1$
    - $ax^2 + bx + c = x^2 + bx + (b/2)^2 - (b/2)^2 + c$
    - $ax^2 + bx + c = (x + b)^2 - (b/2)^2 + c$
    - $ax^2 + bx + c = (x + b/2)^2 - \alpha, \alpha = (b/2)^2 + c$

## 대칭 증명

- $exp_1 = (x - p)^2 + q$ 와 $exp_2 = (x + p)^2 + q$ 는 x축 대칭이다.
    - $exp_1 = (p, q), exp_2 = (-p, q)$

### Example

- $x^2 + 4x + 9$
    - $x^2 + 4x + 9 = x^2 + 4x + 4 - 4 + 9$
    - $x^2 + 4x + 9 = (x+2)^2 + 5$ 
    - vertex is (-2, 5)

## 수학 법칙을 보면서 느낀점

참, 대치라는 워딩이 맞는지 모르겠지만 특정 값을 $\alpha = a + b$ 라고 대입시킨 뒤, 기존 수학 공식으로 풀어내며 증명해내는 방법은 우리가 프로그래밍에서 리스코프 치환원칙을 통해서 의존성 주입을 바꿔낄 수 있는 것과 비슷하다고 느낌이 들었다. 나중에 Function Programming 도 공부해봐야지.