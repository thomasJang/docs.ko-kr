---
title: '방법: 메시지 상자 열기'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- message boxes [WPF], opening
- opening message boxes [WPF]
ms.assetid: acaad17f-af43-4eca-a004-f1c9e7c6f292
ms.openlocfilehash: dd79d69c9b1b54c5158b58ee2f1675e7d11a386a
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33545638"
---
# <a name="how-to-open-a-message-box"></a>방법: 메시지 상자 열기
이 예제에서는 메시지 상자를 여는 방법을 보여 줍니다.  
  
## <a name="example"></a>예제  
 메시지 상자는 사용자에 게 정보를 표시 하기 위한 미리 만들어진된 모달 대화 상자. 정적을 호출 하 여 메시지 상자 열릴 <xref:System.Windows.MessageBox.Show%2A> 의 메서드는 <xref:System.Windows.MessageBox> 클래스입니다. 때 <xref:System.Windows.MessageBox.Show%2A> 은 호출, 메시지가 문자열 매개 변수를 사용 하 여 전달 됩니다. 다양 한 오버 로드 <xref:System.Windows.MessageBox.Show%2A> 메시지 상자가 표시 됩니다는 방식을 구성할 수 있습니다 (참조 <xref:System.Windows.MessageBox>).  
  
 [!code-csharp[MessageBoxSnippets#MessageBoxShow1CODE](../../../../samples/snippets/csharp/VS_Snippets_Wpf/MessageBoxSnippets/CSharp/Show1Window.xaml.cs#messageboxshow1code)]
 [!code-vb[MessageBoxSnippets#MessageBoxShow1CODE](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/MessageBoxSnippets/visualbasic/show1window.xaml.vb#messageboxshow1code)]  
  
## <a name="see-also"></a>참고 항목  
 [MessageBox 샘플](http://go.microsoft.com/fwlink/?LinkID=160023)
