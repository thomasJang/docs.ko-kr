---
title: GetCurrentApartmentType 함수 (관리 되지 않는 API 참조)
description: GetCurrentApartmentType 함수 아파트 호출자에 게 실행 되는 형식을 검색 합니다.
ms.date: 11/06/2017
api_name:
- GetCurrentApartmentType
api_location:
- WMINet_Utils.dll
api_type:
- DLLExport
f1_keywords:
- GetCurrentApartmentType
helpviewer_keywords:
- GetCurrentApartmentType function [.NET WMI and performance counters]
topic_type:
- Reference
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: ca7b5fa5bf6d845d542d3e80c0571e59f3d4c1e0
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33461726"
---
# <a name="getcurrentapartmenttype-function"></a>GetCurrentApartmentType 함수
아파트 호출자에 게 실행 되는 형식을 검색 합니다.   
  
[!INCLUDE[internalonly-unmanaged](../../../../includes/internalonly-unmanaged.md)]
  
## <a name="syntax"></a>구문  
  
```  
HRESULT GetCurrentApartmentType (
   [in] int                   vFunc, 
   [in] IComThreadingInfo*    ptr, 
   [out] APTTYPE*             aptType
); 
```  

## <a name="parameters"></a>매개 변수

`vFunc`  
[in] 이 매개 변수를 사용 하지 않습니다.

`ptr`  
[in] 에 대 한 포인터는 [IComThreadingInfo](https://msdn.microsoft.com/library/windows/desktop/ms694502(v=vs.85).aspx) 인스턴스.

`aptType`  
[out] 에 대 한 포인터는 [APTTYPE](https://msdn.microsoft.com/library/windows/desktop/ms693793(v=vs.85).aspx) 호출자의 아파트를 나타내는 열거형 값입니다.

## <a name="return-value"></a>반환 값


|상수  |값  |설명  |
|---------|---------|---------|
| `S_OK` | 0 | 함수는 성공적으로 완료 되었습니다. |
| `E_FAIL` | 0x80000008 | 호출자에 게는 아파트에서 실행할 수 없습니다. |
  
## <a name="remarks"></a>설명

이 함수에 대 한 호출을 래핑하는 [IComThreadingInfo::GetCurrentApartmentType](https://msdn.microsoft.com/library/windows/desktop/ms683752(v=vs.85).aspx) 메서드.

## <a name="requirements"></a>요구 사항  
 **플랫폼:** 참조 [시스템 요구 사항](../../../../docs/framework/get-started/system-requirements.md)합니다.  
  
 **헤더:** WMINet_Utils.idl  
  
 **.NET framework 버전:** [!INCLUDE[net_current_v472plus](../../../../includes/net-current-v472plus.md)]  
  
## <a name="see-also"></a>참고자료  
[WMI 및 성능 카운터 (관리 되지 않는 API 참조)](index.md)
