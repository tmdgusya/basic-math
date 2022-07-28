# Bit Operation

CD 같은 곳을 자세히 보면 굴곡 같은게 져있음을 확인할 수 있는데, 이를 빛으로 확인해서 어떤 값이 저장되어 있는지 확인할 수 있다. 예를 들면 긴줄은 1, 짧은 줄은 0 이라 해서 어떤 값을 표현할 수 있다는 것이다.

## Integer

Integer 값을 저장하기 위해서 Java 에서는 4 Byte 의 저장공간이 필요하고 이는 Bit 로 표현하면 32 bits 에 해당한다.
Int i = 8 을 저장한다면 다음과 같이 저장될 것이다.

<img width="945" alt="image" src="https://user-images.githubusercontent.com/57784077/181515684-7ade60da-d46a-4230-8a5f-e3b74b03bf1f.png">

즉 Integer 가 표현할 수 있는 가짓수는 **(0,1)^32 - 1 에 속하게 되므로 2^32 - 1** 에 속한다. 
즉 4,294,967,296 가짓수의 수가 표현 가능하다. 하지만 보통 **음의 정수를 표현해야 하므로 맨앞의 비트를 부호 비트**로 두게 된다. 따라서 **-2^31 ~ 2^31 - 1** 가 보통 표현 가능한 수의 범위수이다. 그래서 범위가 -2,147,483,648 ~ 2,147,483,648 에 해당한다.

## OR Operation

비교하는 두개의 값이 하나라도 1(True) 일 경우 True 이다.

<img width="387" alt="image" src="https://user-images.githubusercontent.com/57784077/181517662-ba24aefd-0fc2-49be-b14a-07706ce98eff.png">

## And Operation

비교하는 두개의 값이 둘다 1(True) 일 경우 True 이다.

<img width="382" alt="image" src="https://user-images.githubusercontent.com/57784077/181517832-fd17a04e-5bcf-4089-bb94-72a27a9cd8fd.png">

## Not Operation

현재 진수의 0 과 1을 바꾸어 준다.

<img width="498" alt="image" src="https://user-images.githubusercontent.com/57784077/181518045-990a289d-d86a-4a41-8ad5-dac5a97b103c.png">

## Xor Operation

비교 하는 두 진수가 서로 다른 값을 가지고 있을 경우에 1로 표시한다. XOR 는 이러한 이유로 0 과 연산하게 되면 자기 자신이 나오게 된다. 그러면 모든 값이 1인것과 연산하면 어떻게 될까? 무조건 ~ 을 한 값이 나오게 된다. 부호를 지키는 것과, 부호를 지키지 않는 연산이 존재한다.

<img width="343" alt="image" src="https://user-images.githubusercontent.com/57784077/181518286-9b681844-e0ed-457b-9cf7-cf8cd47e1744.png">

## Left Shift Operation

Left Shift Operation 을 수행하면 연산을 수행하는 횟수 만큼 왼쪽으로 칸을 밀어주게 된다.

<img width="565" alt="image" src="https://user-images.githubusercontent.com/57784077/181518642-c968b237-f051-4a4f-8002-baec57002c02.png">

## Right Shift Operation

Right Shift Operation 을 수행하면 연산을 수행하는 횟수 만큼 오른쪽으로 밀어주게 된다. 이 상황에서 값이 짤릴 수도 있게 된다.

<img width="562" alt="image" src="https://user-images.githubusercontent.com/57784077/181518955-2809fcce-116b-48a1-8b23-6418679e49fc.png">