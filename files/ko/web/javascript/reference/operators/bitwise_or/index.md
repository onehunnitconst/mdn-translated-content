---
title: 비트 OR (|)
slug: Web/JavaScript/Reference/Operators/Bitwise_OR
---

{{jsSidebar("Operators")}}
<!-- 
The **bitwise OR (`|`)** operator returns a `1` in each bit position
for which the corresponding bits of either or both operands are `1`s. -->

**비트 OR(`|`)** 연산자는 `1`을 반환합니다. 각 비트의 위치.. 그 위치는 양쪽의 피연산자 대응하는 비트들

{{EmbedInteractiveExample("pages/js/expressions-bitwise-or.html", "shorter")}}

## 구문

```js-nolint
a | b
```

## 설명

피연산자는 32비트 정수로 변환되며 일련의 비트(0과 1)로 표현됩니다. 32비트를 넘어가는 숫자는 최상위 비트를 기준으로 하여 삭제합니다. 예를 들어 다음과 같은 32비트 이상인 정수는 32비트 정수로 변환됩니다.

```
Before: 11100110111110100000000000000110000000000001
After:              10100000000000000110000000000001
```

Each bit in the first operand is paired with the corresponding bit in the second
operand: _first bit_ to _first bit_, _second bit_ to _second
bit_, and so on.

The operator is applied to each pair of bits, and the result is constructed bitwise.

The truth table for the OR operation is:

| a   | b   | a OR b |
| --- | --- | ------ |
| 0   | 0   | 0      |
| 0   | 1   | 1      |
| 1   | 0   | 1      |
| 1   | 1   | 1      |

```
     9 (base 10) = 00000000000000000000000000001001 (base 2)
    14 (base 10) = 00000000000000000000000000001110 (base 2)
                   --------------------------------
14 | 9 (base 10) = 00000000000000000000000000001111 (base 2) = 15 (base 10)
```

Bitwise ORing any number `x` with `0` returns `x` converted to a 32-bit integer. Do not use `| 0` to truncate numbers to integers; use [`Math.trunc()`](/en-US/docs/Web/JavaScript/Reference/Global_Objects/Math/trunc#using_bitwise_no-ops_to_truncate_numbers) instead.

## 예제

### 비트 OR 연산 사용하기

```js
// 9  (00000000000000000000000000001001)
// 14 (00000000000000000000000000001110)

14 | 9;
// 15 (00000000000000000000000000001111)
```

## 명세

{{Specifications}}

## 브라우저 호환성

{{Compat}}

## 같이보기

- [비트 연산자](/ko/docs/Web/JavaScript/Guide/Expressions_and_Operators#%ED%95%A0%EB%8B%B9_%EC%97%B0%EC%82%B0%EC%9E%90)
- [비트 OR 할당 연산자](/ko/docs/Web/JavaScript/Reference/Operators/Bitwise_OR_assignment)