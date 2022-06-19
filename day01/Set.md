# Set

## 해당 연산을 사용하는 경우

- **Sets(집합)**: unordered objcets
- **Sequences(수열)**: ordered objcets with specific patterns
- **Vectors**: ordered numbers
- **Matrices**: numbers arranged in rectangular grids
- **Tress**: nodes connected by edges

컴퓨터에서도 똑같이 상황에 맞는 Data Structure 를 골라서 associated operations 로 연산하여, 새로운 Data Structure 를 만들어냄

## Sets

> a collection of distinct and well-defined things(or elements)

- 서로 같은게 있다면 하나로 취급한다.
- well-defined: 사람에 따라 달라지지 않는 명확하게 정의 된 값. (1, 2 등의 정수는 누가 다르게 정의한다고 바뀔 수 없는 값임)
- things: 같은 Type 의 objects

### Notations


$Sets = \{ e1, e2, e3 \}$


$
    Sets = \{
        \begin{Bmatrix}
            1 & 0 \\ [0.2em]
            0 & 0
        \end{Bmatrix},
        \begin{Bmatrix}
            0 & 1 \\ [0.2em]
            0 & 0
        \end{Bmatrix},
        \begin{Bmatrix}
            0 & 0 \\ [0.2em]
            1 & 0
        \end{Bmatrix},
        \begin{Bmatrix}
            0 & 0 \\ [0.2em]
            0 & 1
        \end{Bmatrix},
    \}
$

$Sets = \{red, green, blue\}$

### Sets Builder

$a = \{ element | element's condition \}$

들어올수 있는 element 들의 컨디션을 `element's condition` 에 정의한다. 프로그래밍에서는 이를 Pipe 로 표현하는 것 같다.
즉, `a` Data Structure 에는 `element's condition` 에 부합한 애들만 들어갈 수 있으므로 프로그래밍에서는 이를 filter 등의 pipe line 으로 주로 표현한다. 

$A = \{ x | 1 \leq e \in N(natural numbers) \leq 4 \}$ 

- **x 는 자연수에 포함되면서, 1 보다 크거나 같고, 4 보다 작거나 같은 원소**
- $A = \{1, 2, 3, 4\}$

```kotlin
a = elements.filter (condtion)
```


### Notations

#### Veen Diagram

<img width="654" alt="image" src="https://user-images.githubusercontent.com/57784077/174470024-91cffc85-e7fb-4230-86bc-6a87833e1077.png">

아까 위에서 설명했던 자연수이면서 1~4 인 조건을 한번 다시 가져와보자

$U = \{ x | 1 \leq e \in \natural \leq 4 \}$   
$U = \{ 1 \}$ 

이걸 벤다이어 그램으로 그리면 아래와 같이 될것이다.

<img width="654" alt="image" src="https://user-images.githubusercontent.com/57784077/174470275-e7e20106-865e-4349-adcf-993403314823.png">

### Empty Sets

$\emptyset = \{\}$

- Empty Set 은 아무런 원소도 가지고 있지 않은 집합이라고 표현함. 수학에서 나오는 0 과 비슷한 개념.
- Universal Sets 가능한 모든 원소들의 집합을 뜻한다.

## Set's Usage

자연수 집합 : $\natural = \{ ele | is natrual numbers \}$

- 왠만한 특정 수가 무엇이다. 유리수 등등으로 나타낸 것들은 Sets 의 개념을 이용한 것임.

### Functions

- Domain: a set of departure of function
    - 우리의 입력이 될 수 있는 값들의 모든 집합. (공집합)
    - 수학에서도 Domain 이라는 단어가 쓰이는 구나. 정의역이 영어로 Domain 이 였다니 처음 알았다. DDD 에서의 Domain 또한 Client 와 함께 
    ubiquitous language 를 정의하는 곳이니 맞는건가..? 아니 너무 과해석일 수 있겠다. Domain 이 수학에서의 의미말고도 다른 의미가 있을 테니.
- CoDomain: a set of destination of function
- Range(Image): The image of f is then the subset Y consisting of only those elements y of Y such that there is at least one x in X with F(x) = y
- Function: a binary relation between two sets that associates to each elements of the first set exactly one elements of the second set

<img width="283" alt="image" src="https://user-images.githubusercontent.com/57784077/174470624-be1f553d-5172-42d4-8c9b-9efaf4c26e66.png">

### Lines And Planes

- Line: a set of points whose coordinates satisfy a given linear equation
    - $y = ax + b$
    - 참신기하다. 생각해보면 어렸을때 배웠던 것은, 이 $y = ax + b$ 를 만족하는 무수한 점들이 였는데, 그게 생각해보면 그 점들의 집합을 그래프에 나타낸것이 직선인 것이다.
- Plane: a set of all points r such that, $n * (r - r0) = 0$
    - $P = \{ x, y, z | n * (r - r0) = 0 \}$



