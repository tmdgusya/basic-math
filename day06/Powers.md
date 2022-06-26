# Powers

$x^n = x * x * .... * x$ - x 를 n time 곱 한 것.

## Definitions

- $x ^ a$
    - x 는 base 라고 부른다. (한국말로는 보통 밑이라고 함.)
    - a 는 exponent 라고 한다. (한국말로는 지수라고 한다.)

- $0 < x < 1$ 의 scope 에서는 exponent 가 클수록 작은 경향을 보임.
- $x > 1$  의 scope 에서는 exponent 가 클수록 큰 경향을 보임.

## Special Exponents and Bases

- Zero Exponents
    - $x^0 = 1, x \neq 0$
    - $0^0 = 1$ in C.S 

- Unit Exponents
    - $x^1 = x$

- -1 Bases
    - $-1^0 = 1, k = 0$
    - $-1^1 = -1, k = 1$
    - $-1^2 = 1, k = 2$
    - $-1^3 = -1, k = 3$
    - $-1^{k+1} = (-1)*(-1)^{k}$
        - $if (k \geq 2), -1^{k} = -1^{k-2}$ 

### Property Of Powers

- $(x*y)^n = (x*y) * (x*y) * ... * (x*y)$ (x*y) is multiplied for n times

- $(x*y)*(x*y)$
    - $(x*y)*(x*y) = x*(yx)*y$ --- associative law  
    - $x*(xy)*y$ --- associative law  
    - $x^2*y^2$ --- associative law   
    - $x^n*y^n$

- $6^3 = 216$
    - $(2 * 3)^3 = 216$
    - $2^3*3^3 = 216$
    - $8 * 27 = 216$
    - $216 = 216$

### Decomposing Numbers

$a_3*a_2*a_1*a_0 = a_3*1000 + a_2*100 + a_1*10 + a_0*1$

- $123 = 1*100 + 2*10 + 3*1$
    - $123 = 1*10^2 + 2*10^1 + 3*10^0$