---
title: 스레드 타이머(C#)
ms.date: 07/20/2015
ms.assetid: 52ed71e8-4fd9-43a4-ae40-04cce7cff23f
ms.openlocfilehash: c2be9fef0b3f6f3db7ae8c9a519ece0cb64b6f49
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33323445"
---
# <a name="thread-timers-c"></a>스레드 타이머(C#)
<xref:System.Threading.Timer?displayProperty=nameWithType> 클래스는 별도 스레드에서 정기적으로 작업을 실행하는 데 유용합니다. 예를 들어 스레드 타이머를 사용하여 데이터베이스의 상태 및 무결성을 확인하거나 중요한 파일을 백업할 수 있습니다.  
  
## <a name="thread-timer-example"></a>스레드 타이머 예제  
 다음 예제에서는 2초마다 작업을 시작하고 플래그를 사용하여 타이머를 중지하는 <xref:System.IDisposable.Dispose%2A> 메서드를 시작합니다. 이 예제에서는 출력 창에 상태를 게시합니다.  
  
```csharp  
private class StateObjClass  
{  
    // Used to hold parameters for calls to TimerTask.  
    public int SomeValue;  
    public System.Threading.Timer TimerReference;  
    public bool TimerCanceled;  
}  
  
public void RunTimer()  
{  
    StateObjClass StateObj = new StateObjClass();  
    StateObj.TimerCanceled = false;  
    StateObj.SomeValue = 1;  
    System.Threading.TimerCallback TimerDelegate =  
        new System.Threading.TimerCallback(TimerTask);  
  
    // Create a timer that calls a procedure every 2 seconds.  
    // Note: There is no Start method; the timer starts running as soon as   
    // the instance is created.  
    System.Threading.Timer TimerItem =  
        new System.Threading.Timer(TimerDelegate, StateObj, 2000, 2000);  
  
    // Save a reference for Dispose.  
    StateObj.TimerReference = TimerItem;    
  
    // Run for ten loops.  
    while (StateObj.SomeValue < 10)   
    {  
        // Wait one second.  
        System.Threading.Thread.Sleep(1000);    
    }  
  
    // Request Dispose of the timer object.  
    StateObj.TimerCanceled = true;    
}  
  
private void TimerTask(object StateObj)  
{  
    StateObjClass State = (StateObjClass)StateObj;  
    // Use the interlocked class to increment the counter variable.  
    System.Threading.Interlocked.Increment(ref State.SomeValue);  
    System.Diagnostics.Debug.WriteLine("Launched new thread  " + DateTime.Now.ToString());  
    if (State.TimerCanceled)      
    // Dispose Requested.  
    {  
        State.TimerReference.Dispose();  
        System.Diagnostics.Debug.WriteLine("Done  " + DateTime.Now.ToString());  
    }  
}  
```  
  
 스레드 타이머는 콘솔 응용 프로그램을 개발하는 경우 등 <xref:System.Windows.Forms.Timer?displayProperty=nameWithType> 개체를 사용할 수 없는 경우에 특히 유용합니다.  
  
## <a name="see-also"></a>참고 항목  
 <xref:System.Threading>  
 [다중 스레드 응용 프로그램(C#)](../../../../csharp/programming-guide/concepts/threading/multithreaded-applications.md)
