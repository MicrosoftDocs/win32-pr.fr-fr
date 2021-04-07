---
title: Exemple de code C/C++ récupérant le répertoire de travail des tâches
description: Cet exemple récupère le répertoire de travail associé à une tâche et affiche le chemin d’accès au répertoire de travail à l’écran. Cet exemple suppose que la tâche et la tâche de test existent déjà sur l’ordinateur local.
ms.assetid: 46dfd996-6d5f-4a77-87a9-daf1909e1509
keywords:
- récupération du répertoire de travail Planificateur de tâches
- récupération des propriétés de tâche Planificateur de tâches, répertoire de travail
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e44d29de7df9307ee40f3d10d9dd28f87f89d8a3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104029306"
---
# <a name="cc-code-example-retrieving-the-task-working-directory"></a><span data-ttu-id="7b4bf-106">Exemple de code C/C++ : récupération du répertoire de travail des tâches</span><span class="sxs-lookup"><span data-stu-id="7b4bf-106">C/C++ Code Example: Retrieving the Task Working Directory</span></span>

<span data-ttu-id="7b4bf-107">Cet exemple récupère le répertoire de travail associé à une tâche et affiche le chemin d’accès au répertoire de travail à l’écran.</span><span class="sxs-lookup"><span data-stu-id="7b4bf-107">This example retrieves the working directory associated with a task and displays the path to the working directory on the screen.</span></span> <span data-ttu-id="7b4bf-108">Cet exemple suppose que la tâche et la tâche de test existent déjà sur l’ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="7b4bf-108">This example assumes that the task and the test task already exist on the local computer.</span></span>


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
     wprintf(L"Failed calling ITaskScheduler::Activate: error = 0x%x\n",hr);
     CoUninitialize();
     return 1;
  }
  
  
  ///////////////////////////////////////////////////////////////////
  // Call ITask::GetWorkingDirectory to display the working 
  // directory associated with "Test Task".
  ///////////////////////////////////////////////////////////////////
  
  LPWSTR lpwszWorkDir;
  hr = pITask->GetWorkingDirectory(&lpwszWorkDir);
  pITask->Release();
  if (FAILED(hr))
  {
     wprintf(L"Failed calling ITask::GetWorkingDirectory: \n");
     wprintf(L" error = 0x%x\n",hr);
     CoUninitialize();
     return 1;
  }
  
  
  ///////////////////////////////////////////////////////////////////
  // Process returned string. 
  ///////////////////////////////////////////////////////////////////
  
  wprintf(L"Test Task is associated with : %s\n", lpwszWorkDir);
  
  
  ///////////////////////////////////////////////////////////////////
  // Call CoTaskMemFree to free resources.
  ///////////////////////////////////////////////////////////////////
  
  CoTaskMemFree(lpwszWorkDir);
  CoUninitialize();
  return 0;
}
```



## <a name="related-topics"></a><span data-ttu-id="7b4bf-109">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="7b4bf-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7b4bf-110">Exemples de Planificateur de tâches 1,0</span><span class="sxs-lookup"><span data-stu-id="7b4bf-110">Task Scheduler 1.0 Examples</span></span>](task-scheduler-1-0-examples.md)
</dt> </dl>

 

 




