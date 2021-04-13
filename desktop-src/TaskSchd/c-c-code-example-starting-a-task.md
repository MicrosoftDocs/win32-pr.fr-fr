---
title: Exemple de code C/C++ démarrage d’une tâche
description: Cet exemple tente d’exécuter une tâche existante. Cet exemple suppose que la tâche et la tâche de test existent déjà sur l’ordinateur local.
ms.assetid: e4f38f8a-3488-4802-913b-f627ecca8bb2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c9fa9ba112b642aa5e14abc3b408c1536c527d9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104379765"
---
# <a name="cc-code-example-starting-a-task"></a><span data-ttu-id="993be-104">Exemple de code C/C++ : démarrage d’une tâche</span><span class="sxs-lookup"><span data-stu-id="993be-104">C/C++ Code Example: Starting a Task</span></span>

<span data-ttu-id="993be-105">Cet exemple tente d’exécuter une tâche existante.</span><span class="sxs-lookup"><span data-stu-id="993be-105">This example attempts to run an existing task.</span></span> <span data-ttu-id="993be-106">Cet exemple suppose que la tâche et la tâche de test existent déjà sur l’ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="993be-106">This example assumes that the task and the test task already exist on the local computer.</span></span>


```C++
#include <windows.h>
#include <initguid.h>
#include <ole2.h>
#include <mstask.h>
#include <msterr.h>
#include <wchar.h>
#include<stdio.h>


int main(int argc, char **argv)
{
  HRESULT hr = S_OK;
  ITaskScheduler *pITS;
  
  
  ///////////////////////////////////////////////////////////////////
  // Call CoInitialize to initialize the COM library and then
  // call CoCreateInstance to get the Task Scheduler object.
  ///////////////////////////////////////////////////////////////////
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
  lpcwszTaskName = L"Test Task";
  hr = pITS->Activate(lpcwszTaskName,
                      IID_ITask,
                      (IUnknown**) &pITask);
  
  pITS->Release();
  if (FAILED(hr))
  {
     wprintf(L"Failed calling ITaskScheduler::Activate; error = 0x%x\n",hr);
     CoUninitialize();
     return 1;
  }
  
  
  ///////////////////////////////////////////////////////////////////
  // Call ITask::Run to start the execution of "Test Task".
  ///////////////////////////////////////////////////////////////////
  
  hr = pITask->Run();
  pITask->Release();

  if (FAILED(hr))
  {
     wprintf(L"Failed calling ITask::Run, error = 0x%x\n",hr);
     CoUninitialize();
     return 1;
  }

  CoUninitialize();
  return 0;
}
```



## <a name="related-topics"></a><span data-ttu-id="993be-107">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="993be-107">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="993be-108">Exemples de Planificateur de tâches 1,0</span><span class="sxs-lookup"><span data-stu-id="993be-108">Task Scheduler 1.0 Examples</span></span>](task-scheduler-1-0-examples.md)
</dt> </dl>

 

 




