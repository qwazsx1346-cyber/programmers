## 주어진 코드는 변수에 데이터를 저장하고 출력하는 코드입니다.
## 아래와 같이 출력되도록 빈칸을 채워 코드를 완성해 주세요.

### 출력 예시
3
2
1
Let's go!

---

import java.util.Scanner;

public class Solution {
    public static void main(String[] args) {
        String message = " (입력칸1) ";

        System.out.println("3 (입력칸2) 2 (입력칸3) 1");
        System.out.println(message);
    }
}

---

입력칸1. 먼저 Let's go!라는 문자열이 있어야하기 때문에 message 부분에 Let's go! 라는 문자열을 초기화 한다.
입력칸2, 3. 숫자 3,2,1은 이미 있는상태이고 하나가 출력될 때 마다 개행이 되어야하기 때문에 줄바꿈 escape 문자인 \n을 대입.

---

- 최종 답안

import java.util.Scanner;

public class Solution {
    public static void main(String[] args) {
        String message = " Let's go! ";

        System.out.println("3 \n 2 \n 1");
        System.out.println(message);
    }
}
