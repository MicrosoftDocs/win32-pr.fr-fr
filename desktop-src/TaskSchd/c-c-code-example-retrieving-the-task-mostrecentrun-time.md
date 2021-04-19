---
title: Exemple de code C/C++ récupération de la tâche MostRecentRun temps
description: Cet exemple récupère l’heure de la dernière exécution de la tâche et l’affiche à l’écran. Cet exemple suppose que la tâche et la tâche de test existent déjà sur l’ordinateur local.
ms.assetid: 683ff1e1-1cb0-4ef7-bca2-9c3a2b4d1bd0
keywords:
- récupération de la dernière exécution de la tâche Planificateur de tâches
- récupération des propriétés de l’élément de travail Planificateur de tâches, durée d’exécution la plus récente de la tâche
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c8cae40de306d79628fa10230091c571e776c5e4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106512673"
---
# <a name="cc-code-example-retrieving-the-task-mostrecentrun-time"></a><span data-ttu-id="d6ec3-106">Exemple de code C/C++ : récupération de la tâche MostRecentRun temps</span><span class="sxs-lookup"><span data-stu-id="d6ec3-106">C/C++ Code Example: Retrieving the Task MostRecentRun Time</span></span>

<span data-ttu-id="d6ec3-107">Cet exemple récupère l’heure de la dernière exécution de la tâche et l’affiche à l’écran.</span><span class="sxs-lookup"><span data-stu-id="d6ec3-107">This example retrieves the time the task was last run and displays it on the screen.</span></span> <span data-ttu-id="d6ec3-108">Cet exemple suppose que la tâche et la tâche de test existent déjà sur l’ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="d6ec3-108">This example assumes that the task and the test task already exist on the local computer.</span></span>


```C++
#include <windows.h>
#include <wchar.h>
#include <stdio.h>
#include <initguid.h>
#include <ole2.h>
#include <mstask.h>
#include <msterr.h>


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
  LPCWSTR lpcwszTaskName = L"Test Task";
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
  // Call ITask::GetMostRecentRunTime and display the most recent 
  // run time of this task.
  ///////////////////////////////////////////////////////////////////

  SYSTEMTIME pstLastRun;
    
  hr = pITask->GetMostRecentRunTime(&pstLastRun);
  
  // Release the ITask interface.
  pITask->Release();

  if (FAILED(hr))
  {
    wprintf(L"Failed calling GetMostRecentRunTime: ");
    wprintf(L"error = 0x%x\n", hr);
    CoUninitialize();
    return 1;
  }

  wprintf(L"The most recent run time for this task was: \n");
  wprintf(L"  %u/%u/%u \t %u:%02u\n", pstLastRun.wMonth,
                                      pstLastRun.wDay,
                                      pstLastRun.wYear,
                                      pstLastRun.wHour,
                                      pstLastRun.wMinute);
 

  CoUninitialize();

  return 0;
}
```



## <a name="related-topics"></a><span data-ttu-id="d6ec3-109">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="d6ec3-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d6ec3-110">Exemples de Planificateur de tâches 1,0</span><span class="sxs-lookup"><span data-stu-id="d6ec3-110">Task Scheduler 1.0 Examples</span></span>](task-scheduler-1-0-examples.md)
</dt> </dl>

 

 




