---
title: '방법: WebBrowser 컨트롤을 사용하여 URL 탐색'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
f1_keywords:
- WebBrowser.Navigate
helpviewer_keywords:
- WebBrowser control [Windows Forms], examples
- URLs [Windows Forms], navigating to
- WebBrowser control [Windows Forms], navigating to URLs
- examples [Windows Forms], WebBrowser control
ms.assetid: b3ec38cb-f509-4d0b-bd79-9f3611259c62
ms.openlocfilehash: f34577d45ddfbd2445fd4558c5694facf3f1aa29
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33531887"
---
# <a name="how-to-navigate-to-a-url-with-the-webbrowser-control"></a>방법: WebBrowser 컨트롤을 사용하여 URL 탐색
다음 코드 예제에서는 탐색 하는 방법을 보여 줍니다.는 <xref:System.Windows.Forms.WebBrowser> 특정 URL 제어 합니다.  
  
 새 문서를 완전히 로드 하는 시기를 확인 하려면 처리는 <xref:System.Windows.Forms.WebBrowser.DocumentCompleted> 이벤트입니다. 이 이벤트의 데모를 보려면 참조 [하는 방법: WebBrowser 컨트롤을 사용 하 여 인쇄](../../../../docs/framework/winforms/controls/how-to-print-with-a-webbrowser-control.md)합니다.  
  
## <a name="example"></a>예제  
  
```vb  
Me.webBrowser1.Navigate("http://www.microsoft.com")  
```  
  
```csharp  
this.webBrowser1.Navigate("http://www.microsoft.com");  
```  
  
## <a name="compiling-the-code"></a>코드 컴파일  
 이 예제에는 다음 사항이 필요합니다.  
  
-   `webBrowser1`이라는 <xref:System.Windows.Forms.WebBrowser> 컨트롤  
  
-   `System` 및 `System.Windows.Forms` 어셈블리에 대한 참조  
  
## <a name="see-also"></a>참고 항목  
 <xref:System.Windows.Forms.WebBrowser>  
 <xref:System.Windows.Forms.WebBrowser.DocumentCompleted?displayProperty=nameWithType>  
 <xref:System.Windows.Forms.WebBrowser.Navigating?displayProperty=nameWithType>  
 <xref:System.Windows.Forms.WebBrowser.Navigated?displayProperty=nameWithType>  
 [WebBrowser 컨트롤](../../../../docs/framework/winforms/controls/webbrowser-control-windows-forms.md)  
 [방법: WebBrowser 컨트롤을 사용하여 인쇄](../../../../docs/framework/winforms/controls/how-to-print-with-a-webbrowser-control.md)
