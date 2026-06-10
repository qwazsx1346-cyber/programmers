## 문제 설명

- 퓨쳐종합병원에서는 접수한 환자가 진료받을 병과에 따라 자동으로 환자 코드를 부여해 주는 프로그램이 있습니다.

- 환자 코드의 마지막 네 글자를 보면 환자가 어디 병과에서 진료를 받아야 할지 알 수 있습니다.

- 예를 들어 환자의 코드가 "_eye"로 끝난다면 안과를, "head"로 끝난다면 신경외과 진료를 보게 됩니다.

- 환자 코드의 마지막 글자에 따른 병과 분류 기준은 다음과 같습니다.



마지막 글자	병과
"_eye" ->	"Ophthalmologyc"
"head" -> "Neurosurgery"
"infl" -> "Orthopedics"
"skin" -> "Dermatology"

- 환자의 코드를 나타내는 문자열 code를 입력받아 위 표에 맞는 병과를 출력하도록 빈칸을 채워 코드를 완성해 주세요.

  위 표의 단어로 끝나지 않는다면 "direct recommendation"를 출력합니다.
---
## 제한 사항

- 4 ≤ code의 길이 ≤ 20
- code는 영어 소문자와 숫자, 언더바("_")로 이루어져 있습니다.
---

## 입출력 예

입력 #1
dry_eye

출력 #1
Ophthalmologyc

입력 #2
pat23_08_20_head

출력 #2
Neurosurgery

## 입출력 예 설명

입출력 예 #1
code가 "_eye"로 끝나기 때문에 "Ophthalmologyc"를 출력합니다.

입출력 예 #2
code가 "head"로 끝나기 때문에 "Neurosurgery"를 출력합니다.
---

## 기본 제공 코드

```
import java.util.Scanner;

public class Solution {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        String code = sc.next();
        String lastFourWords = code.substring(code.length()-4, code.length());

        if(lastFourWords.equals(   )){
            System.out.println("Ophthalmologyc");
        }
        else if(   ){
            System.out.println("Neurosurgery");
        }
        else if(   ){
            System.out.println("Orthopedics");
        }

        (코드입력칸)  {
            System.out.println("Dermatology");
        }
        (코드입력칸)  {
            System.out.println("direct recommendation");
        }
    }
}
```

---

## 풀이 방법

- 문제 의도와 같이 마지막 4글자에 따라 원하는 병과를 출력하면 된다.

  1. substirng()을 사용하여 문자열 code의 마지막 4글자를 추출한다.
  2. 추출한 문자열을 병과 분류 기준(_eye, head, infl, skin)과 비교한다.
  3. 일치하는 경우 해당 병과명을 출력한다.
  4. 어느 조건에도 해당하지 않으면 "direct recommendation"을 출력한다.
