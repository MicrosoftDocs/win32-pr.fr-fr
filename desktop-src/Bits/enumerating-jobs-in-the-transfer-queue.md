---
title: Énumération des travaux dans la file d’attente de transfert
description: Pour énumérer les travaux de la file d’attente de transfert, appelez la méthode IBackgroundCopyManager EnumJobs. La méthode retourne un pointeur d’interface IEnumBackgroundCopyJobs que vous utilisez pour énumérer les travaux dans la file d’attente.
ms.assetid: ebeb1670-dedd-4791-914e-d035d3c22c5a
keywords:
- transférer les BITS du travail, énumération
- énumération des travaux dans les BITS de file d’attente de transfert
- BITS de file d’attente de transfert, énumération
- énumération des BITS
- énumération des BITS, travaux
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9360043a9265248001dddb785edab3e8aac70abc
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104309318"
---
# <a name="enumerating-jobs-in-the-transfer-queue"></a>Énumération des travaux dans la file d’attente de transfert

Pour énumérer les travaux de la file d’attente de transfert, appelez la méthode [**IBackgroundCopyManager :: EnumJobs**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopymanager-enumjobs) . La méthode retourne un pointeur d’interface [**IEnumBackgroundCopyJobs**](/windows/desktop/api/Bits/nn-bits-ienumbackgroundcopyjobs) que vous utilisez pour énumérer les travaux dans la file d’attente.

Pour récupérer les travaux de l’utilisateur, affectez au premier paramètre de la méthode [**EnumJobs**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopymanager-enumjobs) la valeur 0. Pour récupérer tous les travaux de la file d’attente, affectez au premier paramètre de la méthode **EnumJobs** la valeur BG \_ Job \_ enum \_ All \_ users. Seuls les utilisateurs disposant de privilèges d’administrateur peuvent récupérer tous les travaux dans la file d’attente de transfert.

Notez que la liste énumérée est un instantané des travaux dans la file d’attente de transfert au moment où vous appelez la méthode [**EnumJobs**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopymanager-enumjobs) . Toutefois, les valeurs de propriété de ces travaux reflètent les valeurs actuelles du travail.

Si vous souhaitez récupérer des tâches de transfert individuelles, appelez la méthode [**IBackgroundCopyManager :: GetJob**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopymanager-getjob) .

Pour énumérer des fichiers dans un travail, consultez [énumération de fichiers dans un travail](enumerating-files-in-a-job.md).

L’exemple suivant montre comment énumérer des travaux dans la file d’attente de transfert. La \_ variable g XferManager dans l’exemple est un pointeur d’interface [**IBackgroundCopyManager**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopymanager) . Pour plus d’informations sur la création du pointeur d’interface **IBackgroundCopyManager** , consultez [connexion au service bits](connecting-to-the-bits-service.md).


```C++
HRESULT hr = 0;
IEnumBackgroundCopyJobs* pJobs = NULL;
IBackgroundCopyJob* pJob = NULL;
ULONG cJobCount = 0;
ULONG idx = 0;

//This example enumerates all jobs in the transfer queue. This call fails if the 
//current user does not have administrator privileges. To enumerate jobs for only 
//the current user, replace BG_JOB_ENUM_ALL_USERS with 0.
hr = g_XferManager->EnumJobs(BG_JOB_ENUM_ALL_USERS, &pJobs);
if (SUCCEEDED(hr))
{
  //Get the count of jobs in the queue. 
  pJobs->GetCount(&cJobCount);

  //Enumerate the jobs in the queue.
  for (idx=0; idx<cJobCount; idx++)
  {
    hr = pJobs->Next(1, &pJob, NULL);
    if (S_OK == hr)
    {
      //Retrieve or set job properties.

      pJob->Release();
      pJob = NULL;
    }
    else
    {
      //Handle error
      break;
    }
  }

  pJobs->Release();
  pJobs = NULL;
}
```



 

 




