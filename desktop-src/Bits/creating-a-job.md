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
# <a name="creating-a-job"></a><span data-ttu-id="dd48d-105">Création d’un travail</span><span class="sxs-lookup"><span data-stu-id="dd48d-105">Creating a Job</span></span>

<span data-ttu-id="dd48d-106">Pour créer une tâche de transfert, appelez la méthode [**IBackgroundCopyManager :: createJob**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopymanager-createjob) .</span><span class="sxs-lookup"><span data-stu-id="dd48d-106">To create a transfer job, call the [**IBackgroundCopyManager::CreateJob**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopymanager-createjob) method.</span></span> <span data-ttu-id="dd48d-107">Une fois que le service BITS a créé le travail, [Ajoutez des fichiers au travail](adding-files-to-a-job.md) et [Modifiez les propriétés du travail](setting-and-retrieving-the-properties-of-a-job.md) en fonction de votre application.</span><span class="sxs-lookup"><span data-stu-id="dd48d-107">After BITS creates the job, [add files to the job](adding-files-to-a-job.md) and [modify the job's properties](setting-and-retrieving-the-properties-of-a-job.md) as appropriate for your application.</span></span> <span data-ttu-id="dd48d-108">Pour activer le travail dans la file d’attente, appelez la méthode [**méthode ibackgroundcopyjob :: Resume**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-resume) .</span><span class="sxs-lookup"><span data-stu-id="dd48d-108">To activate the job in the queue, call the [**IBackgroundCopyJob::Resume**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-resume) method.</span></span>

<span data-ttu-id="dd48d-109">La méthode [**createJob**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopymanager-createjob) crée un GUID qui identifie le travail de façon unique.</span><span class="sxs-lookup"><span data-stu-id="dd48d-109">The [**CreateJob**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopymanager-createjob) method creates a GUID that uniquely identifies the job.</span></span> <span data-ttu-id="dd48d-110">Vous utilisez le GUID pour [récupérer le travail à partir de la file d’attente de transfert](/windows/desktop/api/Bits/nf-bits-ibackgroundcopymanager-getjob).</span><span class="sxs-lookup"><span data-stu-id="dd48d-110">You use the GUID to [retrieve the job from the transfer queue](/windows/desktop/api/Bits/nf-bits-ibackgroundcopymanager-getjob).</span></span> <span data-ttu-id="dd48d-111">Le nom d’affichage que vous fournissez lorsque vous créez le travail n’est pas unique ; plusieurs travaux peuvent utiliser le même nom.</span><span class="sxs-lookup"><span data-stu-id="dd48d-111">The display name that you provide when you create the job is not unique; more than one job can use the same name.</span></span>

<span data-ttu-id="dd48d-112">BITS limite le nombre de travaux dans la file d’attente à 300 travaux et le nombre de travaux qu’un utilisateur peut créer au travail 60.</span><span class="sxs-lookup"><span data-stu-id="dd48d-112">BITS limits the number of jobs in the queue to 300 jobs and the number of jobs that a user can create to 60 job.</span></span> <span data-ttu-id="dd48d-113">Ces limites ne s’appliquent pas aux administrateurs ou aux services.</span><span class="sxs-lookup"><span data-stu-id="dd48d-113">These limits do not apply to administrators or services.</span></span> <span data-ttu-id="dd48d-114">Pour modifier ces limites par défaut, consultez [stratégies de groupe](group-policies.md).</span><span class="sxs-lookup"><span data-stu-id="dd48d-114">To change these default limits, see [Group Policies](group-policies.md).</span></span>

<span data-ttu-id="dd48d-115">L’exemple suivant montre comment créer un travail de téléchargement.</span><span class="sxs-lookup"><span data-stu-id="dd48d-115">The following example shows how to create a download job.</span></span> <span data-ttu-id="dd48d-116">L’exemple suppose que la \_ variable g PBCM est un pointeur d’interface [**IBackgroundCopyManager**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopymanager) valide.</span><span class="sxs-lookup"><span data-stu-id="dd48d-116">The example assumes the g\_pbcm variable is a valid [**IBackgroundCopyManager**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopymanager) interface pointer.</span></span> <span data-ttu-id="dd48d-117">Pour plus d’informations sur la création du pointeur d’interface **IBackgroundCopyManager** , consultez [connexion au service bits](connecting-to-the-bits-service.md).</span><span class="sxs-lookup"><span data-stu-id="dd48d-117">For details on how to create the **IBackgroundCopyManager** interface pointer, see [Connecting to the BITS Service](connecting-to-the-bits-service.md).</span></span>


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



<span data-ttu-id="dd48d-118">Pour accéder à la dernière interface [**méthode ibackgroundcopyjob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) , appelez la méthode **méthode ibackgroundcopyjob :: QueryInterface** .</span><span class="sxs-lookup"><span data-stu-id="dd48d-118">To get the latest [**IBackgroundCopyJob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) interface, call the **IBackgroundCopyJob::QueryInterface** method.</span></span> <span data-ttu-id="dd48d-119">L’exemple suivant montre comment accéder à l’interface [**IBackgroundCopyJob5**](/windows/desktop/api/Bits5_0/nn-bits5_0-ibackgroundcopyjob5) .</span><span class="sxs-lookup"><span data-stu-id="dd48d-119">The following example shows how to get the [**IBackgroundCopyJob5**](/windows/desktop/api/Bits5_0/nn-bits5_0-ibackgroundcopyjob5) interface.</span></span>


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



 

 




