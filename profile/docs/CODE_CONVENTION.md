# ✅ C++ 코드 컨벤션

---

## 📌 1. 네이밍 규칙

| 항목            | 규칙                | 예시                          |
|-----------------|---------------------|-------------------------------|
| 지역 변수       | 스네이크 케이스     | `player_name`, `score_total` |
| 상수            | 모두 대문자         | `MAX_BUFFER_SIZE`            |
| 함수명          | 스네이크 케이스     | `calculate_total()`          |
| 클래스/구조체   | 파스칼 케이스       | `PlayerInfo`, `GameManager`  |
| 멤버 변수       | `_` + 카멜케이스    | `_health`, `_maxSpeed`       |
| 메서드          | 카멜케이스          | `getName()`, `setScore()`    |
| 열거형          | `enum class` 사용   | `enum class State { Idle };` |

---

## 📌 2. 들여쓰기 & 포맷팅

- `if`, `while`, `for` 등의 조건문 뒤에는 **띄어쓰기**:

  ```cpp
  if (condition) {
      ...
  }
  ```

- **함수 선언 후 한 줄 띄우기**:

  ```cpp
  void PrintScore();

  void PrintScore()
  {
      ...
  }
  ```

- **한 줄에 한 명령어**:

  ```cpp
  int a = 5;
  a += 1;
  ```

- **한 줄에 하나의 변수만 선언**:

  ```cpp
  int x;
  int y;
  ```

- **함수 내부 변수는 최대 4개까지** 선언 허용.

- **함수 매개변수는 최대 4개까지**

---

## 📌 3. 파일 구조 및 헤더 처리

- **헤더 가드는 반드시 작성**하며, 다음 두 방식 중 하나를 허용:

  - `#pragma once` (선호)
  - 전통적인 헤더 가드:
    ```cpp
    #ifndef ERROR_TREAT_H
    #define ERROR_TREAT_H

    // declarations

    #endif // ERROR_TREAT_H
    ```

- 모든 `#include`는 **파일 시작부에 위치**.
- **사용하지 않는 헤더는 포함 금지**.

---

## 📌 4. 함수 주석 규칙

함수 선언부 위에는 다음과 같은 형태로 주석을 작성:

```cpp
/*
** 함수명 : print_message
** 설명   : 문자열 메시지를 표준 출력으로 출력합니다.
** 인자   : const char *msg - 출력할 문자열
** 반환값 : 없음
*/
void print_message(const char* msg);
```

💡 인자가 여러 개일 경우, 각 인자를 줄바꿈하여 나열해도 무방함.

---

## 📌 5. 기타 가이드라인

- 이름은 **기능과 목적을 명확히 표현**.
- **중괄호는 항상 사용** (`if`, `while`, `else` 포함).
- 블록 사이에 **적절한 공백 줄 추가**로 가독성 확보.
- **전처리기 매크로는 최소화**하고, 상수는 `const`나 `constexpr` 사용 권장.

---
