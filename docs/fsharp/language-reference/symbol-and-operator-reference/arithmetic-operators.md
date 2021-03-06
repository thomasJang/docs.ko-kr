---
title: 산술 연산자(F#)
description: 'F # 프로그래밍 언어에서 사용할 수 있는 산술 연산자에 알아봅니다.'
ms.date: 04/04/2018
ms.openlocfilehash: ead0bbd7fdad528b322f99eaf0f73638f060eb51
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33565940"
---
# <a name="arithmetic-operators"></a>산술 연산자

이 항목에서는 F # 언어에서 사용할 수 있는 산술 연산자를 설명 합니다.

## <a name="summary-of-binary-arithmetic-operators"></a>이진 산술 연산자 요약
다음 표에서 unboxed 정수 및 부동 소수점 형식에 사용할 수 있는 이진 산술 연산자를 요약 합니다.

|이항 연산자|노트|
|---------------|-----|
|`+` (또한 플러스)|선택 취소 합니다. 합계와 함께 번호는 추가 하면 가능한 오버플로 조건을 형식에서 지 원하는 절대 최대값을 초과 합니다.|
|`-` (빼기, 빼기)|선택 취소 합니다. 언더플로 상태가 발생할 수 부호 없는 형식을 뺀 또는 부동 소수점 값이 너무 작아서 형식으로 나타낼 수 있습니다.|
|`*` (곱하기, 시간)|선택 취소 합니다. 숫자를 곱해 하면 가능한 오버플로 조건 및 제품 형식에서 지 원하는 절대 최대값을 초과 합니다.|
|`/` (나누기)|0으로 나누기는 <xref:System.DivideByZeroException> 정수 계열 형식에 대 한 합니다. 부동 소수점 형식에 대 한 0으로 나누기 하면 특수 한 부동 소수점 값 `+Infinity` 또는 `-Infinity`합니다. 이기도 가능한 언더플로 조건을 부동 소수점 숫자는 너무 작아서 형식으로 나타낼 수 있습니다.|
|`%` (나머지, rem)|나누기 연산의 나머지를 반환합니다. 결과의 부호가 첫 번째 피연산자의 부호와 같습니다.|
|`**` (의 지 수)|결과 형식에 대 한 절대 최대값을 초과 하는 경우 가능한 오버플로 조건입니다.<br /><br />지 수 연산자 부동 소수점 형식 에서만 작동합니다.|

## <a name="summary-of-unary-arithmetic-operators"></a>단항 산술 연산자 요약
다음 표에서 정수 및 부동 소수점 형식에 사용할 수 있는 단항 산술 연산자를 요약 합니다.


|단항 연산자|노트|
|--------------|-----|
|`+` (양수)|모든 산술 식에 적용할 수 있습니다. 값의 부호는 변경 되지 않습니다.|
|`-` (부정, 음수)|모든 산술 식에 적용할 수 있습니다. 값의 부호를 변경합니다.|
주위에 배치 하에서 오버플로 또는 언더플로 정수 계열 형식에 대 한 동작이입니다. 이렇게 하면 잘못 된 결과입니다. 정수 오버플로 소프트웨어에 대 한 계정에 기록 되지 않습니다 때 보안 문제를 일으킬 수 있는 잠재적으로 심각한 문제입니다. 응용 프로그램에 대 한 우려 경우 하에서 확인 된 연산자를 사용 하 여 `Microsoft.FSharp.Core.Operators.Checked`합니다.


## <a name="summary-of-binary-comparison-operators"></a>이진 비교 연산자 요약
다음 표에서 정수 및 부동 소수점 형식에 사용할 수 있는 이진 비교 연산자를 보여 줍니다. 이러한 연산자의 반환 값 형식 `bool`합니다.

부동 소수점 숫자를 직접 비교할 수 없습니다, 동등 여부에 대 한 IEEE 부동 소수점 표시 된 값이 같은지를 지원 하지 않으므로 합니다. 두 숫자 코드를 검사 하 여 동일한 것으로 쉽게 확인할 수 있는 서로 다른 비트 표현의 있을 실제로 수 있습니다.



|연산자|노트|
|--------|-----|
|`=` (같음)|할당 연산자가 있습니다. 비교에 대해서만 사용 됩니다. 일반 연산자입니다.|
|`>` (보다 큼)|일반 연산자입니다.|
|`<` (보다 작음)|일반 연산자입니다.|
|`>=` (크거나 같음)|일반 연산자입니다.|
|`<=` (보다 작거나 같음)|일반 연산자입니다.|
|`<>` (같지 않음)|일반 연산자입니다.|

## <a name="overloaded-and-generic-operators"></a>제네릭 및 오버 로드 된 연산자
에 정의 된 모든이 여기에 나온 연산자는 **Microsoft.FSharp.Core.Operators** 네임 스페이스입니다. 일부 연산자는 정적으로 확인 된 형식 매개 변수를 사용 하 여 정의 됩니다. 해당 연산자를 사용 하는 각 특정 형식에 대 한 개별 정의 됨을 의미 합니다. 단항 및 이항 산술 및 비트 연산자의 모든이 범주에 있습니다. 비교 연산자는 제네릭 및 따라서 하지 기본 산술 형식 뿐, 모든 유형과 함께 작동 합니다. 구별 된 공용 구조체 및 레코드 형식을 F # 컴파일러에 의해 생성 되는 고유한 사용자 지정 구현이 있어야 합니다. 메서드를 사용 하는 클래스 형식 <xref:System.Object.Equals%2A>합니다.

일반 연산자를 사용자 지정할 수 있습니다. 비교 함수를 사용자 지정 하려면 재정의 <xref:System.Object.Equals%2A> 사용자 고유의 사용자 지정 같음 비교를 제공 하 고 다음 구현에 <xref:System.IComparable>합니다. <xref:System.IComparable?displayProperty=nameWithType> 인터페이스에는 단일 메서드는 <xref:System.IComparable.CompareTo%2A> 메서드.


## <a name="operators-and-type-inference"></a>연산자 및 형식 유추
식에서 연산자를 사용 하는 연산자에는 형식 유추를 제한합니다. 또한 연산자의 사용 방지 연산자는 산술 형식 의미 하기 때문에 자동 일반화 합니다. 다른 정보가 없는 경우, F # 컴파일러에서 유추 `int` 산술 식의 형식으로. 다른 형식을 지정 하 여이 동작을 재정의할 수 있습니다. 인수 형식 및 반환 형식은 따라서 `function1` 다음 코드에서는 것으로 유추 됩니다 `int`에 대 한 형식 `function2` 것으로 유추 `float`합니다.

[!code-fsharp[Main](../../../../samples/snippets/fsharp/lang-ref-1/snippet3501.fs)]
    
## <a name="see-also"></a>참고 항목
[기호 및 연산자 참조](index.md)

[연산자 오버로드](../operator-overloading.md)

[비트 연산자](bitwise-operators.md)

[부울 연산자](boolean-operators.md)
