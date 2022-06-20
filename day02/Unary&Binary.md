# Unary / Binary Operations

## Operations on Sets

일정한 규칙을 통해 **새로운 규칙**을 만들어 나가는 과정

## Unary Operations

$f: A -> B$

집합 하나를 가지고, 다른 집합 하나를 만들어 내는것. $\sqrt 4 -> 2$ 와 같은 연산이 대표적인 Unary Operations 임.

### powerSet

집합 A 의 모든 subset 들의 집합 $\mathcal{P}(A)$. **집합의 모든 원소는 또 하나의 집합**이 될 수 있다. 그 subset 들의 모임이 powerSet 이다.

- $\mathcal{P}(A) = \{X | X \subseteq A \}$
- $|\mathcal{P}(A)| = 2^{|A|}$
    - 왜 Cardinality 가 2의 제곱승일까? 아래 그림을 보면 알 수 있다. 집합에서 하나의 원소당 두가지의 Subset 을 만들 확률을 가진다. 즉, 있거나 없거나이다.
    - <img width="650" alt="image" src="https://user-images.githubusercontent.com/57784077/174610725-9806537b-1e27-4465-8af7-d5001bbc9d63.png">

$A = \{0, 1\}$
- $\mathcal{P}(A) = \{ \emptyset ,\{0\}, \{1\}, \{0, 1\} \}$ 
- 위의 $\mathcal{P}(A)$ 가 A 의 power set 이다.
- emptyset 도 powerset 의 원소이다.
- **원소들은 binary 로 encoding 가능하다.**

### complement of sets

A 에 포함되지 않은 원소들을 모은 집합을 A 의 complement 라고 하고, $A^c$ 라고 표현한다.

- $A^c = \{x | x \notin A \}$

위 처럼 생각할 수도 있고, Universal Set 에서 A 를 제외한 친구들을 생각할 수도 있음

- $A^c = \{x | x \notin A \} \wedge \{x | x \in U\}$

그래서 요런식이 성립된다.

- $A^C \cup A = U (Universal set)$
- $U - A = A^C$

## Binary Operations

$f: A \diamond C-> B$

- 2 + 3 = 5 와 같이 두개의 집합을 이용해 다른 하나의 집합을 만들어 내는 연산.

### Intersection of sets

집합 A,B 에 모두 포함되는 원소들을 모은 집합을 A 와 B 의 intersaction 이라고 부르고, $A \cap B$ 라고 나타낸다.

- $A \cap B = \{x | (x \in A) \wedge (x \in B)\}$

### union of sets

집합 A,B 에 포함되는 원소들을 모은 집합을 A 와 B 의 union 이라고 부르고, $A \cup B$ 라고 나타낸다.

- $A \cup B = \{x | (x \in A) \vee (x \in B)\}$

- **Cardinality**
    - $|A \cup B| = |A| + |B| - |A \cap B|$
    - $|A \cap B| \leq |A|, |A \cap B| \leq |B|$
        - A 와 B 의 intersection 은 A/B 보다 작거나, 같을 수 밖에 없다.

- **Special Case**
    - $A \subseteq B -> A \cup B = B, A \cap B = A$
    - $A \supseteq B -> A \cup B = A, A \cap B = B$

### Intersections and Unions

- $\bigcap\limits_{i=1}^{n}A_{i} = A_1 \cap A_2 \cap ... \cap A_n$
- $\bigcup\limits_{i=1}^{n}A_{i} = A_1 \cup A_2 \cup ... \cup A_n$

### The Algebraic Properties

- **Commutative Law**
    - $A \cup B = B \cup A$
    - $A \cap B = B \cap A$

- **Associative Law**
    - $(A \cup B) \cup C = A \cup (B \cup C)$
    - $(A \cap B) \cap C = A \cap (B \cap C)$

- **Distribute Law**
    - $(A \cap B) \cup C = (A \cup C) \cap (B \cup C)$
    - $(A \cup B) \cap C = (A \cap C) \cup (B \cap C)$

### Identities

- $A \cup \emptyset = A$
- $A \cap \emptyset = \emptyset$

- $A \cup U = U$
- $A \cap U = A$
 
- $A \cup A^C = U$
- $A \cap A^C = \emptyset$
- $(A^C)^C = A$

### De Morgan's Law

- $(A \cap B)^C = A^C \cup B^C$
- $(A \cup B)^C = A^C \cap B^C$

### set difference (relative complement)

집합 A, B 에 대해서 A 에는 포함되고, B 에는 포함되지 않은 원소들을 모은 집합을 A-B 로 나타내고, set difference(차집합) 이라고 부른다.

- $A - B = \{x | (x \in A) \wedge (x \notin B) \}$

### Excercies

- $A - B = A \cap B^C$
- $A - B = A - (A \cap B)$
- $A - B = (A \cup B) - B$

### 풀이
- $A - B \cup (A \cap B)$
    - $(A \cap B^C) \cup (A \cap B)$
    - $A \cap (B^C \cup B)$
    - $A \cap U$
    - $A$

### The Algebraic Properties

- Anti-Commutativity
    - $A - B \neq B - A$
- Anti-Associativity
    - $A - (B - C) \neq (A - B) - C$
- Distributive Law
    - $C - (A \cap B)$
        - $C \cap (A \cap B)^C$
        - $C \cap (A^C \cup B^C)$
        - $(C \cap A^C) \cup (C \cap B^C)$

    - $(C - A) \cap (C - B)$
        - $(C \cap A^C) \cup (C \cap B^C)$

### symmetric difference

집합 A,B 에 대해 A - B 와 B - A 의 union

- $A \bigtriangleup B = \{x | (A - B) \cup (B - A)\}$
    - = $\{x | (x \in A) \vee (x \in B) \wedge (x \notin (A \cap B))\}$

### Cartesian product of sets

집합 A, B 에서 원소 a, b 들을 각각 뽑아 (a,b) 를 만들때, 모든 (a,b) 의 집합을 $AXB$ 라고 한다.
- $A X B = \{(a, b) | (a \in A) \wedge (b \in B)\}$

### Exercise

- $A = \{0, 1, 2\}, B = \{a, b\} -> A X B$
    - A X B = {{0, a}, {0, b}, {1, a}, {1, b}, {2, a}, {2, b}}

좌표평면을 생각해보면 **Cartesian product of sets** 을 이용했다는 것을 알 수 있음.

## Disjoint Sets

집합 A, B 에 대해 $A \cup B = \emptyset$ 일때 A, B 는 **disjoint set** 이다.
- disjoint set 을 mutually exclusive 라고도 부른다.

- Cardinality
    - $|A \cap B| = 0$
    - $|A \cup B| = |A| + |B|$

## Partitions Of Sets

Universal set 안에 집합 $A_1, A_2, ..., A_n$ 이 있고, **U 의 모든 원소들이 단 하나의 $A_i$ 에만 포함**될때, $\{A_1, A_2, ..., A_n\}$ 을 U 의 Partition 이라고 부른다. **즉, $A_n-1 \cap A_n = \emptyset$ 을 뜻한다.**

- $\bigcup\limits_{i=1}^{n}A_{i} = U$ 

이거 하니깐 DB Partiton 이 떠올랐다. DB Partition 또한 모든 Partition 이 합해질때 Universal Set 이 된다.