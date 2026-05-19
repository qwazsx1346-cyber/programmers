## 문제 설명

2자리 이상의 정수 number가 주어집니다.

주어진 코드는 이 수를 2자리씩 자른 뒤, 자른 수를 모두 더해서 그 합을 출력하는 코드입니다. 

코드가 올바르게 작동하도록 한 줄을 수정해 주세요.

---

## 제한 사항

10 ≤ number ≤ 2,000,000,000

number의 자릿수는 2의 배수입니다.

---

## 입출력 예

입력 #1
4859

출력 #1
107

입력 #2
29

출력 #2
29

---

## 입출력 예 설명

### 입출력 예 #1

- 입력된 수를 2자리씩 나눠 합치면 다음과 같습니다.

- 48 + 59 = 107

### 입출력 예 #2

- 입력된 수를 2자리씩 나눠 합치면 다음과 같습니다.

- 29  = 29

---

## 문제 (1줄만 수정하여 버그 고치기)

```
import java.util.Scanner;

public class Solution {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int number = sc.nextInt();
        int answer = 0;
        
        for(int i=0; i<1; i++){
            answer += number % 100;
            number /= 100;
        }

        System.out.println(answer);
    }
}
```

---

## 제시한 답

```
import java.util.Scanner;

public class Solution {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int number = sc.nextInt();
        int answer = 0;
        
        while(number > 0){  <= 이 줄 수정
            answer += number % 100;
            number /= 100;
        }

        System.out.println(answer);
    }
}
```

### 이렇게 풀이한 이유

- 기존 코드는 i가 0일 때 (0 < 1) 최초 한번만 실행이되어 4859라는 숫자 입력 시 answer += 4859 % 100;

- 뒤의 두 자리인 59가 answer에 더해짐

- number /= 100; => 4859 / 100은 48이 되어 number에 저장됨.

- 이후 i++로 i가 1이되면 1 < 1이 되어 더이상 반복하지않고 반복문을 빠져나오게 되어 59만 출력하게 된다.

- 따라서 while(number > 0)으로 수정하여 더이상 자를 숫자가 없을 때 까지 계속반복을 만들어주어서 풀이




