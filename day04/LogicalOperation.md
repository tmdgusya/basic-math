# Logical Operations

## Unariy Operation

$\diamond A = Y$

### Logical Negation(ㄱ)

input condition 의 true / false 를 변경하는 연산 (not operator)

## Binary Operation

$A \diamond B = Y$

### Logical Conjunction($\wedge$)

두 input condition 이 참일때만, output condition 이 참인 연산 **(AND 연산)**

### Logical Disjunction($\vee$)

두 input condtion 중 하나라도 참이라면 output condition 이 참인 연산 **(OR 연산)**

### Logical Exclusive Disjunction($\oplus$)

두 input condtion 중 하나만 참일때 output condition 이 참인 연산 **(OR 연산)**

- $1 \oplus 0 = 1$
- $1 \oplus 1 = 0$

2 진수 덧셈할때 쓰고 있지 않을 까란 생각이 들었다. 보통 입력이 다른지 같은지를 판단하는데 많이 쓰인다고 한다.

### NAND, NOR, XOR

- NAND 는 AND 의 Output 에 Not 을 붙여준 것 임.
- NOR 는 OR 의 Output 에 Not 을 붙여준 것 임.

### Logical Implecations ($\longrightarrow$)

조건 A 가 만족될 때, B 가 만족됨을 추론하는 연산 $A \longrightarrow B$
A 는 Promise B 는 Conclusion 이다.

Promise 는 True 인데 Conclusion 이 False 인 경우 약속을 지키지 않은 것 이다.

### Converse(역)

$B \longrightarrow A$

### Inverse (이)

$B \longrightarrow A$

### Contrapositive (대우)
