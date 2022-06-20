# Inclusion / Exclusion Of Elements

원소들은 어떤 집합에 포함될 수도, 포함되지 않을 수도 있다.

- 원소 a 가 집합 A 에 포함됨.
    - $a \in A$
- 원소 a 가 집합 A 에 포함되지 않음.
    - $a \notin A$

## Equal Sets

집합 A 의 모든 원소가 B 에 포함되고, 집합 B 의 모든 원소도 A 에 포함될때, A, B 는 서로 같은 집합이다.
- $A = \{A, B, C\} , B = \{A, B, C\}$ 일때, A 와 B 는 Equal Set 이다.
- $A = B <-> [(\forall a \in A) \in B] \wedge [(\forall b \in B) \in A]$


# Inclusion / Exclusion Of Sets

## SubSets

집합 A 의 모든원소가 집합 B 에 포함될때, A 는 B의 Subset 이라고 한다.

$A \subseteq B <-> (\forall a \in A) \in B$

카디널리티를 따져보면 무조건 아래와 같은 식이 완성된다. 왜냐하면 A 가 B 에 전부 포함되기 때문이다. 집합의 내용을 잘 이해하면 Generic 을 이해하는데도 큰 도움이 된다.
- $|A| \leq |B|$

- EmptySet 은 어떤 조건이든 SubSet 을 만족시킨다.
    - $\emptyset \subseteq A$
    - $A = \{a,b,c,d\}$
        - $\{a\} \subseteq A, \{b\} \subseteq A, \{c\} \subseteq A, \{d\} \subseteq A$
        - $\{a, b\} \subseteq A, \{b, c\} \subseteq A, ...$
        - $\{a, b, c\} \subseteq A, \{b, c, d\} \subseteq A, ...$
        - $\{a, b, c, d\} \subseteq A$
        - $\{a, b, c, d\} \supseteq A$
        - 정리하면 **A 는 A 의 SubSet 이자 SuperSet** 임을 알 수 있다.


## SuperSets

집합 B 의 모든원소가 집합 A 에 모두 포함될때, A 는 B 의 SuperSet 이라고 한다. 이 내용은 Generic 을 이해하는데 큰 도움을 주는데, **Java, Kotlin 처럼 상속이나 Interface 를 이용하는 언어들은 Parent 가 SuperSet 의 개념**이 된다. 그래서 **포함관계이기에 치환이 가능한 것**이다. 

- $A \supseteq B <-> (\forall b \in B) \in A$

자바의 경우 아래와 같을 것이다.

- $Object \supseteq AllObjcet$
    - Objcet 는 모든 Objcet 의 SuperSet 이다.

- $|A| \geq |B|$

## Proper SubSet / SuperSet

### Proper SubSet

집합 A, B 에 대해 A 가 B 의 SubSet 이지만 완전히 같지는 않을 때, A 는 B 의 proper subset 이라고 한다.
- 쉽게 설명하면 두개가 Subset 구조를 지니지만, Equal Sets 가 아닐때를 말한다.
- 수식으로 나타내면 아래와 같다.
    - $A \subset B <-> [(\forall a \in A) \in B] \wedge [A \neq B]$

이걸 보면서 느낀게 하나있는데 **Type 언어에서 Inheritance 를 한 후 Override 를 하게 되면 Proper Subset 일까? 아니면 Equal Sets 일까를 고민**했다.
다만 **외부로 노출되는 Type 이란 것은 public 하게 열려있으므로 Object 를 상속하는 구조는 1:N 이므로 이 경우에는 Equal Sets 일것 같으나, Interface 의 경우에는 N:M 구조를 지니므로, proper Sets 일 수 있겠다는 생각**이 들었다. (다른 생각이거나, 틀렸다면 DM 을 줘도 좋을 것 같다 ㅎㅎ)

- $|A| < |B|$

### Proper SuperSet

집합 A, B 에 대해 A 가 B 의 SuperSet 이지만 완전히 같지는 않을 때, A 는 B 의 proper superset 이라고 한다.
- 수식으로 나타내면 아래와 같다.
    - $A \supset B <-> [(\forall b \in B) \in A] \wedge [A \neq B]$
- **Java 에서 Objcet 는 SuperSet 이고, Interface 가 proper superSet** 이 아닐까?
- $A \not \subseteq A$ 
    - 이때는 A 는 A 의 proper subset 일 수 없다.
- $A \not \supset A$ 
    - 이때는 A 는 A 의 proper superset 일 수 없다.

## Example

- $X = {x |(x 는 4의 배수)}$
    - $X = {4, 8, 12, 16, 20, ...}$
- $Y = {y |(y 는 8의 배수)}$
    - $Y = {8, 16, 24, 32, 40, ...}$

- $X \supset Y, Y \subset X$

## Increasing/Decreasing Sequence Sets

### Increasing Sequence Sets

- $A1 \subseteq A2 \subseteq A3 \subseteq... \subseteq An$
    - $A_k \subseteq A_k+_1, 1 \leq k \in \natural \leq n-1$

### Decreasing Sequence Sets

- $A1 \supseteq A2 \supseteq A3 \supseteq... \supseteq An$
    - $A_k \supseteq A_k+_1, 1 \leq k \in \natural \leq n-1$

예시로 들면 $2^i$ 의 배수의 집합을 구한다고 생각하면 쉽다.
- $A = {x | (x 는 2^i 의 배수)}$
    - $A_1 = {x | (x 는 2 의 배수)} = {2, 4, 6, 8, ...}$
    - $A_2 = {x | (x 는 4 의 배수)} = {4, 8, 12, 16, ...}$
    - $A_3 = {x | (x 는 6 의 배수)} = {6, 12, 18, 24, ...}$
    - $A_1 \supset A_2 \supset A_3 \supset... \supset A_i$
