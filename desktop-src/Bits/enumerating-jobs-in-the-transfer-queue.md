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
# <a name="enumerating-jobs-in-the-transfer-queue"></a><span data-ttu-id="d1feb-109">Énumération des travaux dans la file d’attente de transfert</span><span class="sxs-lookup"><span data-stu-id="d1feb-109">Enumerating Jobs in the Transfer Queue</span></span>

<span data-ttu-id="d1feb-110">Pour énumérer les travaux de la file d’attente de transfert, appelez la méthode [**IBackgroundCopyManager :: EnumJobs**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopymanager-enumjobs) .</span><span class="sxs-lookup"><span data-stu-id="d1feb-110">To enumerate jobs from the transfer queue, call the [**IBackgroundCopyManager::EnumJobs**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopymanager-enumjobs) method.</span></span> <span data-ttu-id="d1feb-111">La méthode retourne un pointeur d’interface [**IEnumBackgroundCopyJobs**](/windows/desktop/api/Bits/nn-bits-ienumbackgroundcopyjobs) que vous utilisez pour énumérer les travaux dans la file d’attente.</span><span class="sxs-lookup"><span data-stu-id="d1feb-111">The method returns an [**IEnumBackgroundCopyJobs**](/windows/desktop/api/Bits/nn-bits-ienumbackgroundcopyjobs) interface pointer that you use to enumerate the jobs in the queue.</span></span>

<span data-ttu-id="d1feb-112">Pour récupérer les travaux de l’utilisateur, affectez au premier paramètre de la méthode [**EnumJobs**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopymanager-enumjobs) la valeur 0.</span><span class="sxs-lookup"><span data-stu-id="d1feb-112">To retrieve the user's jobs, set the first parameter of the [**EnumJobs**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopymanager-enumjobs) method to 0.</span></span> <span data-ttu-id="d1feb-113">Pour récupérer tous les travaux de la file d’attente, affectez au premier paramètre de la méthode **EnumJobs** la valeur BG \_ Job \_ enum \_ All \_ users.</span><span class="sxs-lookup"><span data-stu-id="d1feb-113">To retrieve all jobs in the queue, set the first parameter of the **EnumJobs** method to BG\_JOB\_ENUM\_ALL\_USERS.</span></span> <span data-ttu-id="d1feb-114">Seuls les utilisateurs disposant de privilèges d’administrateur peuvent récupérer tous les travaux dans la file d’attente de transfert.</span><span class="sxs-lookup"><span data-stu-id="d1feb-114">Only users with administrator privileges can retrieve all jobs in the transfer queue.</span></span>

<span data-ttu-id="d1feb-115">Notez que la liste énumérée est un instantané des travaux dans la file d’attente de transfert au moment où vous appelez la méthode [**EnumJobs**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopymanager-enumjobs) .</span><span class="sxs-lookup"><span data-stu-id="d1feb-115">Note that the enumerated list is a snapshot of the jobs in the transfer queue at the time you call the [**EnumJobs**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopymanager-enumjobs) method.</span></span> <span data-ttu-id="d1feb-116">Toutefois, les valeurs de propriété de ces travaux reflètent les valeurs actuelles du travail.</span><span class="sxs-lookup"><span data-stu-id="d1feb-116">However, the property values of those jobs reflect the current values of the job.</span></span>

<span data-ttu-id="d1feb-117">Si vous souhaitez récupérer des tâches de transfert individuelles, appelez la méthode [**IBackgroundCopyManager :: GetJob**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopymanager-getjob) .</span><span class="sxs-lookup"><span data-stu-id="d1feb-117">If you want to retrieve individual transfer jobs, call the [**IBackgroundCopyManager::GetJob**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopymanager-getjob) method.</span></span>

<span data-ttu-id="d1feb-118">Pour énumérer des fichiers dans un travail, consultez [énumération de fichiers dans un travail](enumerating-files-in-a-job.md).</span><span class="sxs-lookup"><span data-stu-id="d1feb-118">To enumerate files in a job, see [Enumerating Files in a Job](enumerating-files-in-a-job.md).</span></span>

<span data-ttu-id="d1feb-119">L’exemple suivant montre comment énumérer des travaux dans la file d’attente de transfert.</span><span class="sxs-lookup"><span data-stu-id="d1feb-119">The following example shows how to enumerate jobs in the transfer queue.</span></span> <span data-ttu-id="d1feb-120">La \_ variable g XferManager dans l’exemple est un pointeur d’interface [**IBackgroundCopyManager**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopymanager) .</span><span class="sxs-lookup"><span data-stu-id="d1feb-120">The g\_XferManager variable in the example is an [**IBackgroundCopyManager**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopymanager) interface pointer.</span></span> <span data-ttu-id="d1feb-121">Pour plus d’informations sur la création du pointeur d’interface **IBackgroundCopyManager** , consultez [connexion au service bits](connecting-to-the-bits-service.md).</span><span class="sxs-lookup"><span data-stu-id="d1feb-121">For details on how to create the **IBackgroundCopyManager** interface pointer, see [Connecting to the BITS Service](connecting-to-the-bits-service.md).</span></span>


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



 

 




