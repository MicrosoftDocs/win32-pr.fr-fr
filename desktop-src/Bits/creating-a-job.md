---
title: Création d’un travail
description: Pour créer une tâche de transfert, appelez la méthode IBackgroundCopyManager CreateJob.
ms.assetid: a7d9feef-4beb-4ae5-9453-9157ee3ec0e8
keywords:
- transférer les BITS de tâche
- transférer les BITS du travail, création
ms.topic: article
ms.date: 11/29/2018
ms.openlocfilehash: 8dddb2427fde43014a31e81f72711ca74e69de34
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104462086"
---
# <a name="creating-a-job"></a>Création d’un travail

Pour créer une tâche de transfert, appelez la méthode [**IBackgroundCopyManager :: createJob**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopymanager-createjob) . Une fois que le service BITS a créé le travail, [Ajoutez des fichiers au travail](adding-files-to-a-job.md) et [Modifiez les propriétés du travail](setting-and-retrieving-the-properties-of-a-job.md) en fonction de votre application. Pour activer le travail dans la file d’attente, appelez la méthode [**méthode ibackgroundcopyjob :: Resume**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-resume) .

La méthode [**createJob**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopymanager-createjob) crée un GUID qui identifie le travail de façon unique. Vous utilisez le GUID pour [récupérer le travail à partir de la file d’attente de transfert](/windows/desktop/api/Bits/nf-bits-ibackgroundcopymanager-getjob). Le nom d’affichage que vous fournissez lorsque vous créez le travail n’est pas unique ; plusieurs travaux peuvent utiliser le même nom.

BITS limite le nombre de travaux dans la file d’attente à 300 travaux et le nombre de travaux qu’un utilisateur peut créer au travail 60. Ces limites ne s’appliquent pas aux administrateurs ou aux services. Pour modifier ces limites par défaut, consultez [stratégies de groupe](group-policies.md).

L’exemple suivant montre comment créer un travail de téléchargement. L’exemple suppose que la \_ variable g PBCM est un pointeur d’interface [**IBackgroundCopyManager**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopymanager) valide. Pour plus d’informations sur la création du pointeur d’interface **IBackgroundCopyManager** , consultez [connexion au service bits](connecting-to-the-bits-service.md).


```C++
HRESULT hr;
GUID JobId;
IBackgroundCopyJob* pJob = NULL;

//To create an upload job, replace BG_JOB_TYPE_DOWNLOAD with 
//BG_JOB_TYPE_UPLOAD or BG_JOB_TYPE_UPLOAD_REPLY.
hr = g_pbcm->CreateJob(L"MyJobName", BG_JOB_TYPE_DOWNLOAD, &JobId, &pJob);
if (SUCCEEDED(hr))
{
  //Save the JobId for later reference. 
  //Modify the job's property values.
  //Add files to the job.
  //Activate (resume) the job in the transfer queue.
}
```



Pour accéder à la dernière interface [**méthode ibackgroundcopyjob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) , appelez la méthode **méthode ibackgroundcopyjob :: QueryInterface** . L’exemple suivant montre comment accéder à l’interface [**IBackgroundCopyJob5**](/windows/desktop/api/Bits5_0/nn-bits5_0-ibackgroundcopyjob5) .


```C++
  HRESULT hr = S_OK;
  IBackgroundCopyJob* pJob = NULL;
  IBackgroundCopyJob5* pJob5 = NULL;

  hr = pJob->QueryInterface(__uuidof(IBackgroundCopyJob5), (void**)&pJob5);
  pJob->Release();
  if (FAILED(hr))
  {
    wprintf(L"pJob->QueryInterface failed with 0x%x.\n", hr);
    goto cleanup;
  }
```



 

 




