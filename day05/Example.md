# Basic Computation

<img width="1603" alt="image" src="https://user-images.githubusercontent.com/57784077/175302308-9ac4fea9-7171-40b7-ada4-3d8764f0cb30.png">

<img width="1129" alt="image" src="https://user-images.githubusercontent.com/57784077/175303042-8b3acb6a-dc6d-4353-9914-3c30958d472b.png">

## Logical Equivalence

truth set A, B 의 연산으로 X, Y가 나오고, 모든 경우에 대해 X, Y 의 True, False 값이 같을때, 두 X, Y 는 Logical Equivalence 하다.

| Args1  | Args2 | compute3  | compute4 |
| -----  | ----- | -----  | ----- |
| 1  | 1  |  1 | 1  |
| 0  | 1  |  0 | 0  |

compute3 과 compute4 모두 똑같은 inpute 을 받았을때 compute 된 result 가 같으므로 logical equivalence 하다. 이걸 보면서 Java Objcet 의 hashcode 메소드에 대해서 생각했다. hashcode() 값을 같게 만들어서 logial Equivalence 를 보장해주던 것이 떠오른다.

