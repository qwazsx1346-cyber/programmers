## 문제설명

일반적으로 두 선분이 이루는 각도는 한 바퀴를 360도로 하여 표현합니다. 따라서 각도에 360의 배수를 더하거나 빼더라도 같은 각을 의미합니다. 
예를 들면, 30도와 390도는 같은 각도입니다.

주어진 코드는 각도를 나타내는 두 정수 angle1과 angle2가 주어질 때, 이 두 각의 합을 0도 이상 360도 미만으로 출력하는 코드입니다. 
코드가 올바르게 작동하도록 한 줄을 수정해 주세요.

---

### 제한사항

0 ≤ angle1 ≤ 5000

0 ≤ angle2 ≤ 5000

1줄만 수정하여 버그를 고치기

---

### 입출력 예

입력 #1

280

485

출력 #1

45

- 설명 : angle1과 angle2의 합은 765도이고, 765를 720을 빼면 45도이므로 45를 출력합니다.

---

- 기존 코드

```
import java.util.Scanner;

public class Solution {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int angle1 = sc.nextInt();
        int angle2 = sc.nextInt();

        int sum_angle = angle1 + angle2;
        System.out.println(sum_angle);
    }
}
```

---

- 풀이 코드

```
import java.util.Scanner;

public class Solution {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int angle1 = sc.nextInt();
        int angle2 = sc.nextInt();

        int sum_angle = (angle1 + angle2) % 360;  <= 수정부분
        System.out.println(sum_angle);  
    }
}
```

---

### 풀이 해석

- 문제 해석에 나와있듯 모든각에 360도를 더하거나 빼도 같은 각도인것을 활용하여서

- 두 수의 합에 360도를 나눈 나머지를 출력하게 하도록 풀이.

- 나머지를 구하는것이기 때문에 두 수의 합이 360보다 작을경우 자기자신(두 수의 합) 그대로 출력이 됨.






