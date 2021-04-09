---
title: Gestion des erreurs (BITS)
description: Il existe deux types d’erreurs à gérer dans votre application.
ms.assetid: cbc182ce-c853-492e-8953-21c54500875b
keywords:
- gestion des BITS d’erreur
- BITS de tâche de transfert, Erreurs
- BITS d’erreur
- BITS d’erreur, gestion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1544788192d4bfd778fef83caaca922f1f84c01e
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104032175"
---
# <a name="handling-errors-bits"></a><span data-ttu-id="acb76-107">Gestion des erreurs (BITS)</span><span class="sxs-lookup"><span data-stu-id="acb76-107">Handling Errors (BITS)</span></span>

<span data-ttu-id="acb76-108">Il existe deux types d’erreurs à gérer dans votre application.</span><span class="sxs-lookup"><span data-stu-id="acb76-108">There are two types of errors to handle in your application.</span></span> <span data-ttu-id="acb76-109">La première erreur est un appel de méthode qui a échoué.</span><span class="sxs-lookup"><span data-stu-id="acb76-109">The first error is a failed method call.</span></span> <span data-ttu-id="acb76-110">Chaque méthode retourne une valeur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="acb76-110">Each method returns an **HRESULT** value.</span></span> <span data-ttu-id="acb76-111">La page de référence de chaque méthode identifie les valeurs de retour qu’il est le plus susceptible de générer.</span><span class="sxs-lookup"><span data-stu-id="acb76-111">The reference page for each method identifies the return values that it is most likely to generate.</span></span> <span data-ttu-id="acb76-112">Pour obtenir des valeurs de retour supplémentaires, consultez [bits Return values](bits-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="acb76-112">For additional return values, see [BITS Return Values](bits-return-values.md).</span></span> <span data-ttu-id="acb76-113">Pour obtenir le texte du message associé à la valeur de retour, appelez la méthode [**IBackgroundCopyManager :: GetErrorDescription**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopymanager-geterrordescription) .</span><span class="sxs-lookup"><span data-stu-id="acb76-113">To get the message text associated with the return value, call the [**IBackgroundCopyManager::GetErrorDescription**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopymanager-geterrordescription) method.</span></span>

<span data-ttu-id="acb76-114">Le deuxième type d’erreur à gérer est un travail dont l' [État](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-getstate) passe à [ \_ \_ \_ erreur d’état de la tâche BG](/windows/desktop/api/Bits/ne-bits-bg_job_state) ou à une **\_ \_ \_ \_ erreur temporaire d’état de travail BG**.</span><span class="sxs-lookup"><span data-stu-id="acb76-114">The second type of error to handle is a job whose [state](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-getstate) transitions to [BG\_JOB\_STATE\_ERROR](/windows/desktop/api/Bits/ne-bits-bg_job_state) or **BG\_JOB\_STATE\_TRANSIENT\_ERROR**.</span></span> <span data-ttu-id="acb76-115">Pour récupérer les informations relatives à ces types d’erreurs, appelez la méthode [**méthode ibackgroundcopyjob :: GetError**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-geterror) du travail.</span><span class="sxs-lookup"><span data-stu-id="acb76-115">To retrieve information related to these types of errors, call the job's [**IBackgroundCopyJob::GetError**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-geterror) method.</span></span> <span data-ttu-id="acb76-116">La méthode retourne un pointeur d’interface [**IBackgroundCopyError**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyerror) qui contient les informations que vous utilisez pour déterminer la cause de l’erreur.</span><span class="sxs-lookup"><span data-stu-id="acb76-116">The method returns an [**IBackgroundCopyError**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyerror) interface pointer that contains information you use to determine the cause of the error.</span></span> <span data-ttu-id="acb76-117">Vous pouvez également recevoir une notification d’erreur en vous inscrivant pour recevoir une notification d’événement.</span><span class="sxs-lookup"><span data-stu-id="acb76-117">You can also receive error notification by registering to receive event notification.</span></span> <span data-ttu-id="acb76-118">Pour plus d’informations, consultez [inscription d’un rappel com](registering-a-com-callback.md).</span><span class="sxs-lookup"><span data-stu-id="acb76-118">For details, see [Registering a COM Callback](registering-a-com-callback.md).</span></span>

<span data-ttu-id="acb76-119">BITS considère chaque travail comme atomique.</span><span class="sxs-lookup"><span data-stu-id="acb76-119">BITS considers each job to be atomic.</span></span> <span data-ttu-id="acb76-120">Si l’un des fichiers du travail génère une erreur, le travail reste dans un état d’erreur jusqu’à ce que l’erreur soit résolue.</span><span class="sxs-lookup"><span data-stu-id="acb76-120">If one of the files in the job generates an error, the job remains in an error state until the error is resolved.</span></span> <span data-ttu-id="acb76-121">Par conséquent, vous ne pouvez pas supprimer le fichier à l’origine de l’erreur du travail.</span><span class="sxs-lookup"><span data-stu-id="acb76-121">Thus, you cannot delete the file that is causing the error from the job.</span></span> <span data-ttu-id="acb76-122">Toutefois, si l’erreur est due au fait que le serveur n’est pas disponible ou qu’il s’agit d’un fichier distant non valide, vous pouvez appeler la méthode [**IBackgroundCopyJob3 :: ReplaceRemotePrefix**](/windows/desktop/api/Bits2_0/nf-bits2_0-ibackgroundcopyjob3-replaceremoteprefix) ou [**IBackgroundCopyFile2 :: SetRemoteName**](/windows/desktop/api/Bits2_0/nf-bits2_0-ibackgroundcopyfile2-setremotename) pour identifier un nouveau serveur ou nom de fichier.</span><span class="sxs-lookup"><span data-stu-id="acb76-122">However, if the error is caused by the server not being available or an invalid remote file, you can call the [**IBackgroundCopyJob3::ReplaceRemotePrefix**](/windows/desktop/api/Bits2_0/nf-bits2_0-ibackgroundcopyjob3-replaceremoteprefix) or [**IBackgroundCopyFile2::SetRemoteName**](/windows/desktop/api/Bits2_0/nf-bits2_0-ibackgroundcopyfile2-setremotename) method to identify a new server or file name.</span></span>

<span data-ttu-id="acb76-123">Après avoir déterminé la cause de l’erreur, effectuez l’une des options suivantes :</span><span class="sxs-lookup"><span data-stu-id="acb76-123">After determining the cause of the error, perform one of the following options:</span></span>

-   <span data-ttu-id="acb76-124">Annulez la tâche en appelant la méthode [**méthode ibackgroundcopyjob :: Cancel**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-cancel) .</span><span class="sxs-lookup"><span data-stu-id="acb76-124">Cancel the job by calling the [**IBackgroundCopyJob::Cancel**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-cancel) method.</span></span>
-   <span data-ttu-id="acb76-125">Pour un travail de téléchargement, appelez la méthode [**méthode ibackgroundcopyjob :: Complete**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-complete) pour enregistrer les fichiers qui ont été transférés correctement avant l’erreur.</span><span class="sxs-lookup"><span data-stu-id="acb76-125">For a download job, call the [**IBackgroundCopyJob::Complete**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-complete) method to save the files that transferred successfully before the error occurred.</span></span>
-   <span data-ttu-id="acb76-126">Corrigez l’erreur et appelez la méthode [**méthode ibackgroundcopyjob :: Resume**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-resume) pour terminer le travail.</span><span class="sxs-lookup"><span data-stu-id="acb76-126">Fix the error and call the [**IBackgroundCopyJob::Resume**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-resume) method to finish the job.</span></span>

<span data-ttu-id="acb76-127">Pour une tâche de chargement-réponse, vérifiez la valeur du membre **bytesTotal** de la structure de progression de la réponse de la [**\_ tâche \_ \_ BG**](/windows/desktop/api/Bits1_5/ns-bits1_5-bg_job_reply_progress) pour déterminer si l’erreur s’est produite lors du chargement ou de la réponse de la tâche.</span><span class="sxs-lookup"><span data-stu-id="acb76-127">For an upload-reply job, check the value of the **BytesTotal** member of the [**BG\_JOB\_REPLY\_PROGRESS**](/windows/desktop/api/Bits1_5/ns-bits1_5-bg_job_reply_progress) structure to determine if the error occurred on the upload or reply portion of the job.</span></span> <span data-ttu-id="acb76-128">L’erreur s’est produite lors du téléchargement si la valeur de la taille BG est \_ \_ inattendue.</span><span class="sxs-lookup"><span data-stu-id="acb76-128">The error occurred on the upload if the value is BG\_SIZE\_UNKNOWN.</span></span>

<span data-ttu-id="acb76-129">L’exemple suivant montre comment récupérer un pointeur d’interface [**IBackgroundCopyError**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyerror) .</span><span class="sxs-lookup"><span data-stu-id="acb76-129">The following example shows how to retrieve an [**IBackgroundCopyError**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyerror) interface pointer.</span></span> <span data-ttu-id="acb76-130">L’exemple suppose que le pointeur d’interface [**méthode ibackgroundcopyjob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) est valide.</span><span class="sxs-lookup"><span data-stu-id="acb76-130">The example assumes the [**IBackgroundCopyJob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) interface pointer is valid.</span></span>


```C++
HRESULT hr = 0;
HRESULT hrError = 0;
IBackgroundCopyJob* pJob;
IBackgroundCopyError* pError = NULL;
IBackgroundCopyFile* pFile = NULL;
WCHAR* pszDescription = NULL;
WCHAR* pszRemoteName = NULL;
BG_ERROR_CONTEXT Context;

hr = pJob->GetError(&pError);
if (SUCCEEDED(hr))
{
  //Retrieve the HRESULT associated with the error. The context tells you
  //where the error occurred, for example, in the transport, queue manager, the 
  //local file, or the remote file.
  pError->GetError(&Context, &hrError);  

  //Retrieve a description associated with the HRESULT value.
  hr = pError->GetErrorDescription(LANGIDFROMLCID(GetThreadLocale()), &pszDescription);
  if (SUCCEEDED(hr))
  {
    if (BG_ERROR_CONTEXT_REMOTE_FILE == Context)
    {
      hr = pError->GetFile(&pFile);  
      if (SUCCEEDED(hr))
      {
        hr = pFile->GetRemoteName(&pszRemoteName);
        if (SUCCEEDED(hr))
        {
          //Do something with the information.
          CoTaskMemFree(pszRemoteName);
        }
        pFile->Release();
      }
    }
    CoTaskMemFree(pszDescription);
  }
  pError->Release();
}
else
{
  //Error information is not available.
}
```



 

 




