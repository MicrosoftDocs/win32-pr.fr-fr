---
title: Exemple de code C/C++ récupération du code de sortie de la tâche
description: Cet exemple récupère le dernier code de sortie retourné par une tâche connue. (Une valeur retournée de \ 0034 ; 0 \ 0034 ; indique que la tâche n’a jamais été exécutée.) Cet exemple suppose que la tâche et la tâche de test existent déjà sur l’ordinateur local.
ms.assetid: e7bfe645-7f4c-4700-9adf-c581e6895aec
keywords:
- récupération des Planificateur de tâches de commentaires de tâche
- récupération des propriétés de l’élément de travail Planificateur de tâches, commentaire de tâche
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5911cad3831dc8da04e44f161a644bda9742bd33
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104507211"
---
# <a name="cc-code-example-retrieving-task-exit-code"></a><span data-ttu-id="d5ee2-106">Exemple de code C/C++ : récupération du code de sortie de la tâche</span><span class="sxs-lookup"><span data-stu-id="d5ee2-106">C/C++ Code Example: Retrieving Task Exit Code</span></span>

<span data-ttu-id="d5ee2-107">Cet exemple récupère le dernier code de sortie retourné par une tâche connue.</span><span class="sxs-lookup"><span data-stu-id="d5ee2-107">This example retrieves the last exit code returned by a known task.</span></span> <span data-ttu-id="d5ee2-108">(Une valeur retournée de « 0 » indique que la tâche n’a jamais été exécutée.) Cet exemple suppose que la tâche et la tâche de test existent déjà sur l’ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="d5ee2-108">(A returned value of "0" indicates the task was never run.) This example assumes that the task and the test task already exist on the local computer.</span></span>


```C++
#include <windows.h>
#include <initguid.h>
#include <ole2.h>
#include <mstask.h>
#include <msterr.h>
#include <wchar.h>

int main(int argc, char **argv)
{
  HRESULT hr = S_OK;
  
  
  ///////////////////////////////////////////////////////////////////
  // Call CoInitialize to initialize the COM library and then
  // call CoCreateInstance to get the Task Scheduler object.
  ///////////////////////////////////////////////////////////////////
  ITaskScheduler *pITS;
  hr = CoInitialize(NULL);
  if (SUCCEEDED(hr))
  {
    hr = CoCreateInstance(CLSID_CTaskScheduler,
                          NULL,
                          CLSCTX_INPROC_SERVER,
                          IID_ITaskScheduler,
                          (void **) &pITS);
    if (FAILED(hr))
    {
      CoUninitialize();
      return 1;
    }
  }
  else
  {
     return 1;
  }
  
  
  ///////////////////////////////////////////////////////////////////
  // Call ITaskScheduler::Activate to get the Task object.
  ///////////////////////////////////////////////////////////////////
  ITask *pITask;
  LPCWSTR lpcwszTaskName;
  lpcwszTaskName = L"TestTask";
  hr = pITS->Activate(lpcwszTaskName,
                      IID_ITask,
                      (IUnknown**) &pITask);
  
  // Release ITaskScheduler interface.
  pITS->Release();
  
  if (FAILED(hr))
  {
    wprintf(L"Failed calling ITaskScheduler::Activate: ");
    wprintf(L"error = 0x%x\n",hr);
    CoUninitialize();
    return 1;
  }
  
  
  ///////////////////////////////////////////////////////////////////
  // Call ITask::GetExitCode. Note that this method is 
  // inherited from IScheduledWorkItem.
  ///////////////////////////////////////////////////////////////////
  DWORD pdwExitCode;
  
  hr = pITask->GetExitCode(&pdwExitCode);
  
  // Release ITask interface.
  pITask->Release();
  
  if (FAILED(hr))
  {
    wprintf(L"Failed calling ITask::GetExitCode: ");
    wprintf(L"error = 0x%x\n",hr);
    CoUninitialize();
    return 1;
  }
  
  
  wprintf(L"The last exit code of Test Task is: %d\n", pdwExitCode);
  
  
  CoUninitialize();
  return 0;
}
```



## <a name="related-topics"></a><span data-ttu-id="d5ee2-109">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="d5ee2-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d5ee2-110">Exemples de Planificateur de tâches 1,0</span><span class="sxs-lookup"><span data-stu-id="d5ee2-110">Task Scheduler 1.0 Examples</span></span>](task-scheduler-1-0-examples.md)
</dt> </dl>

 

 




