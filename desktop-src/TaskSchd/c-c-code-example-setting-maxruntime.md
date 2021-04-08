---
title: Exemple de code C/C++ définissant durée maximale
description: Cet exemple définit la durée maximale d’exécution (définie en millisecondes) d’une tâche connue. Cet exemple suppose que la tâche et la tâche de test existent déjà sur l’ordinateur local.
ms.assetid: ccfa3c01-870b-4b44-a493-9934ca1e51e4
keywords:
- définition des propriétés de tâche Planificateur de tâches, durée maximale d’exécution
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e4d75470a19a7b2a142a99c5f0c307404fc1bc1e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103672433"
---
# <a name="cc-code-example-setting-maxruntime"></a><span data-ttu-id="0ed5d-105">Exemple de code C/C++ : définition de durée maximale</span><span class="sxs-lookup"><span data-stu-id="0ed5d-105">C/C++ Code Example: Setting MaxRunTime</span></span>

<span data-ttu-id="0ed5d-106">Cet exemple définit la durée maximale d’exécution (définie en millisecondes) d’une tâche connue.</span><span class="sxs-lookup"><span data-stu-id="0ed5d-106">This example sets the maximum run time (set in milliseconds) of a known task.</span></span> <span data-ttu-id="0ed5d-107">Cet exemple suppose que la tâche et la tâche de test existent déjà sur l’ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="0ed5d-107">This example assumes that the task and the test task already exist on the local computer.</span></span>


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
  
  // Release the ITaskScheduler interface.
  pITS->Release();  
  
  if (FAILED(hr))
  {
    wprintf(L"Failed calling ITaskScheduler::Activate: ");
    wprintf(L"error = 0x%x\n",hr);
    CoUninitialize();
    return 1;
  }
  
  
  ///////////////////////////////////////////////////////////////////
  // Call ITask::SetMaxRunTime to specify the maximum amount
  // of time the task will run.
  ///////////////////////////////////////////////////////////////////
  DWORD dwMaxRunTime = (1000*60*5);
  
  hr = pITask->SetMaxRunTime(dwMaxRunTime);
  
  if (FAILED(hr))
  {
    wprintf(L"Failed calling ITask::SetMaxRunTime: ");
    wprintf(L"error = 0x%x\n",hr);
    pITask->Release();
    CoUninitialize();
    return 1;
  }
  
  
  ///////////////////////////////////////////////////////////////////
  // Call IPersistFile::Save to save the modified task to disk.
  ///////////////////////////////////////////////////////////////////
  IPersistFile *pIPersistFile;
  
  hr = pITask->QueryInterface(IID_IPersistFile,
                              (void **)&pIPersistFile);
  
  // Release the ITask interface.
  pITask->Release();  
  
  hr = pIPersistFile->Save(NULL,
                           TRUE);

  if (FAILED(hr))
  {
    wprintf(L"Failed calling IPersistFile::Save: ");
    wprintf(L"error = 0x%x\n",hr);
    pIPersistFile->Release();
    CoUninitialize();
    return 1;
  }
  
  // Release the IPersistFile interface.
  pIPersistFile->Release();
  
  wprintf(L"The maximum run time is set to 5 minutes.\n");
  
  CoUninitialize();
  return 0;
}
```



## <a name="related-topics"></a><span data-ttu-id="0ed5d-108">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="0ed5d-108">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0ed5d-109">Exemples de Planificateur de tâches 1,0</span><span class="sxs-lookup"><span data-stu-id="0ed5d-109">Task Scheduler 1.0 Examples</span></span>](task-scheduler-1-0-examples.md)
</dt> </dl>

 

 




