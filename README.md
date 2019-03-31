# MacOS Calculator

달리님이 소개해주신 맥 OS 기본 계산기 만들기 입니다

구현은 자유롭게! 다만, 제가 알아낸 계산기 사양에 대해 공유합니다

작업을 마치셨다면, 이 저장소에 Push 해주세요

**master 말고 브랜치로 푸시 해주세요**

## Specifications

혹시 더 요구되는 사양이 있다면 추가 해주세요!

1. 연산자가 두 개가 되면 계산을 한다 (`5 + 3 +` ← 일 때 계산함)
2. 한 번 연산을 한 상태에서 `=` 을 입력하면 이전 연산자와 피 연산자를 기억하여 현재 총합과 함께 계산
3. `%`는 현재 표시된 숫자에 0.01을 곱한다
4. `C`는 가장 최근의 입력된 값(연산자 또는 수 관계없이) 을 무효로 하고, 화면의 표시 값을 0으로 한다
5. `AC`는 모든 메모리를 초기화 한다
6. 소수점 8자리 이하가 되면 지수 표현식(10e1)으로 변경한다
    1. 그 이하의 값이 되면 값은 0이 된다. 다만 계산기가 초기화 되는 것은 아니므로, `C` 상태를 유지한다
7. 소수점이 없으면 찍는다. 다만 이미 있으면, 아무 동작도 하지 않는다
8. `+/-` 는 현재 화면에 표시된 값을 `+ 또는 -` 로 토글한다
9. 연산자는 몇 번을 눌러도 마지막으로 눌린 값만 유효하다
10. 천 단위 콤마 표시를 한다
11. 숫자는 입력될 수록 좌우 크기에 맞추어 폰트 사이즈가 작아진다 (6px 까지)
    1.  10의 16제곱부터 지수 표현을 사용한다(10진수)
12. 화면은 연산자가 입력되면 잠깐 깜박인다
    1. 다만, 효력이 없는 입력은 깜박이지 않는다 
        1. 0이 입력된 상태로 0을 누르기, 소수점이 있는 상태에서 점 누르기 등
13. JavaScript 부동소수점 정확도 계산을 위해 라이브러리를 추가해야 한다
    1. [https://goo.gl/PddvBT](https://goo.gl/PddvBT) 참고
