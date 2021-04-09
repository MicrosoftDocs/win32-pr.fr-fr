---
title: Exemple de code C/C++ comment définir un commentaire de tâche
description: Cet exemple définit le commentaire pour une tâche connue. Cet exemple suppose que la tâche et la tâche de test existent déjà sur l’ordinateur local.
ms.assetid: c91da741-07fe-41fb-94d5-f6a45ef2d89d
keywords:
- définition des Planificateur de tâches de commentaires de tâche
- définition des propriétés de l’élément de travail Planificateur de tâches, commentaire de tâche
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9683b80e3760aa242e8a3ee9b6a2c6d6b3247182
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103839738"
---
# <a name="cc-code-example-setting-task-comment"></a><span data-ttu-id="c5425-106">Exemple de code C/C++ : définition d’un commentaire de tâche</span><span class="sxs-lookup"><span data-stu-id="c5425-106">C/C++ Code Example: Setting Task Comment</span></span>

<span data-ttu-id="c5425-107">Cet exemple définit le commentaire pour une tâche connue.</span><span class="sxs-lookup"><span data-stu-id="c5425-107">This example sets the comment for a known task.</span></span> <span data-ttu-id="c5425-108">Cet exemple suppose que la tâche et la tâche de test existent déjà sur l’ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="c5425-108">This example assumes that the task and the test task already exist on the local computer.</span></span>


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
  // Call ITask::SetComment to specify the account name
  // and the account password for Test Task.
  ///////////////////////////////////////////////////////////////////
  LPCWSTR pwszComment = L"This task is used to test the Task Scheduler APIs.";
  
  hr = pITask->SetComment(pwszComment);
  
  if (FAILED(hr))
  {
    wprintf(L"Failed calling ITask::SetComment: ");
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

  wprintf(L"Set the comment for Test Task.\n");  
  CoUninitialize();
  return 0;
}
```



## <a name="related-topics"></a><span data-ttu-id="c5425-109">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="c5425-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c5425-110">Exemples de Planificateur de tâches 1,0</span><span class="sxs-lookup"><span data-stu-id="c5425-110">Task Scheduler 1.0 Examples</span></span>](task-scheduler-1-0-examples.md)
</dt> </dl>

 

 




