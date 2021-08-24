---
title: Exemple de code C/C++ récupération de la tâche durée maximale
description: Cet exemple récupère la durée maximale pendant laquelle la tâche peut s’exécuter (en millisecondes) et affiche ce nombre à l’écran. Cet exemple suppose que la tâche et la tâche de test existent déjà sur l’ordinateur local.
ms.assetid: 33873fef-1b67-4010-8bda-b75e1dfa80d5
keywords:
- récupération de la tâche durée maximale Planificateur de tâches
- récupération des propriétés de tâche Planificateur de tâches, durée maximale
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cbc060884be207081d56f0325d2e1f4228ef609e7733738874e61d68e1d2eec2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119738609"
---
# <a name="cc-code-example-retrieving-the-task-maxruntime"></a>Exemple de code C/C++ : récupération de la tâche durée maximale

Cet exemple récupère la durée maximale pendant laquelle la tâche peut s’exécuter (en millisecondes) et affiche ce nombre à l’écran. Cet exemple suppose que la tâche et la tâche de test existent déjà sur l’ordinateur local.


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
  lpcwszTaskName = L"Test Task";
  hr = pITS->Activate(lpcwszTaskName,
                      IID_ITask,
                      (IUnknown**) &pITask);
  
  pITS->Release();
  if (FAILED(hr))
  {
     wprintf(L"Failed calling ITaskScheduler::Activate;\n");
     wprintf(L"error = 0x%x\n",hr);
     CoUninitialize();
     return 1;
  }
  
  
  ///////////////////////////////////////////////////////////////////
  // Call ITask::GetMaxRunTime to display the maximum time Test Task
  // is allowed to run.
  ///////////////////////////////////////////////////////////////////
  
  DWORD pdwRunTime;
  hr = pITask->GetMaxRunTime(&pdwRunTime);
  pITask->Release();
  if (FAILED(hr))
  {
     wprintf(L"Failed calling ITask::GetMaxRunTime: \n");
     wprintf(L"error = 0x%x\n",hr);
     CoUninitialize();
     return 1;
  }
  
  wprintf(L"Test Task can run for %d milliseconds\n", pdwRunTime);
  CoUninitialize();
  return 0;
}
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Exemples de Planificateur de tâches 1,0](task-scheduler-1-0-examples.md)
</dt> </dl>

 

 




