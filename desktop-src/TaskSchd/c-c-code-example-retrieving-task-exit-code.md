---
title: Exemple de code C/C++ récupération du code de sortie de la tâche
description: Cet exemple récupère le dernier code de sortie retourné par une tâche connue. (Une valeur retournée de \ 0034 ; 0 \ 0034 ; indique que la tâche n’a jamais été exécutée.) Cet exemple suppose que la tâche et la tâche de test existent déjà sur l’ordinateur local.
ms.assetid: e7bfe645-7f4c-4700-9adf-c581e6895aec
keywords:
- récupération des Planificateur de tâches de commentaires de tâche
- récupération des propriétés de l’élément de travail Planificateur de tâches, commentaire de tâche
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0908ae8fc15e3ae34c06f02267e9bad396956181fa058c0bf757b8f8486783d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119738849"
---
# <a name="cc-code-example-retrieving-task-exit-code"></a>Exemple de code C/C++ : récupération du code de sortie de la tâche

Cet exemple récupère le dernier code de sortie retourné par une tâche connue. (Une valeur retournée de « 0 » indique que la tâche n’a jamais été exécutée.) Cet exemple suppose que la tâche et la tâche de test existent déjà sur l’ordinateur local.


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



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Exemples de Planificateur de tâches 1,0](task-scheduler-1-0-examples.md)
</dt> </dl>

 

 




