---
title: Interrogation de l’état du travail
description: Par défaut, une application doit interroger les modifications de l’état d’un travail.
ms.assetid: b12ee1e0-d3d9-4d31-b2af-7491480968f0
keywords:
- transférer les BITS de tâche, interrogation
- interrogation des BITS d’état de la tâche
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2df7fcde49d7359ff8cfa38326eba1e1e0bfeac5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103839414"
---
# <a name="polling-for-the-status-of-the-job"></a><span data-ttu-id="c9984-105">Interrogation de l’état du travail</span><span class="sxs-lookup"><span data-stu-id="c9984-105">Polling for the Status of the Job</span></span>

<span data-ttu-id="c9984-106">Par défaut, une application doit interroger les modifications de l’état d’un travail.</span><span class="sxs-lookup"><span data-stu-id="c9984-106">By default, an application must poll for changes in the status of a job.</span></span> <span data-ttu-id="c9984-107">Pour capturer les modifications de l’état du travail, appelez la méthode [**méthode ibackgroundcopyjob :: GetState**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-getstate) .</span><span class="sxs-lookup"><span data-stu-id="c9984-107">To capture changes in the job's state, call the [**IBackgroundCopyJob::GetState**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-getstate) method.</span></span> <span data-ttu-id="c9984-108">Pour capturer les modifications du nombre d’octets et de fichiers transférés, appelez la méthode [**méthode ibackgroundcopyjob :: GetProgress**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-getprogress) .</span><span class="sxs-lookup"><span data-stu-id="c9984-108">To capture changes in the number of bytes and files transferred, call the [**IBackgroundCopyJob::GetProgress**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-getprogress) method.</span></span> <span data-ttu-id="c9984-109">Pour récupérer des informations de progression sur la partie réponse d’une tâche de chargement-réponse, appelez la méthode [**IBackgroundCopyJob2 :: GetReplyProgress**](/windows/desktop/api/Bits1_5/nf-bits1_5-ibackgroundcopyjob2-getreplyprogress) .</span><span class="sxs-lookup"><span data-stu-id="c9984-109">To retrieve progress information on the reply portion of an upload-reply job, call the [**IBackgroundCopyJob2::GetReplyProgress**](/windows/desktop/api/Bits1_5/nf-bits1_5-ibackgroundcopyjob2-getreplyprogress) method.</span></span> <span data-ttu-id="c9984-110">Pour obtenir un exemple qui utilise les informations de progression, consultez [détermination de la progression d’un travail](determining-the-progress-of-a-job.md).</span><span class="sxs-lookup"><span data-stu-id="c9984-110">For an example that uses the progress information, see [Determining the Progress of a Job](determining-the-progress-of-a-job.md).</span></span>

<span data-ttu-id="c9984-111">L’énumération de l' [**\_ \_ État du travail BG**](/windows/desktop/api/Bits/ne-bits-bg_job_state) définit les États d’un travail et la structure de [**\_ \_ progression du travail BG**](/windows/desktop/api/Bits/ns-bits-bg_job_progress) contient des informations sur le nombre d’octets et de fichiers transférés.</span><span class="sxs-lookup"><span data-stu-id="c9984-111">The [**BG\_JOB\_STATE**](/windows/desktop/api/Bits/ne-bits-bg_job_state) enumeration defines the states of a job, and the [**BG\_JOB\_PROGRESS**](/windows/desktop/api/Bits/ns-bits-bg_job_progress) structure contains information on the number of bytes and files transferred.</span></span>

<span data-ttu-id="c9984-112">Pour utiliser l’interrogation, vous devez créer un mécanisme pour lancer l’interrogation.</span><span class="sxs-lookup"><span data-stu-id="c9984-112">To use polling, you need to create a mechanism to initiate polling.</span></span> <span data-ttu-id="c9984-113">Par exemple, créez un minuteur ou utilisez un bouton « mettre à jour » sur l’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="c9984-113">For example, create a timer or use an "Update" button on the user interface.</span></span> <span data-ttu-id="c9984-114">Toutefois, il peut être plus facile de s’inscrire pour la notification d’événements et de recevoir des événements lorsque l’État ou la progression change.</span><span class="sxs-lookup"><span data-stu-id="c9984-114">However, it might be easier to register for event notification and receive events when the state or progress changes.</span></span> <span data-ttu-id="c9984-115">Pour plus d’informations sur la notification d’événements, consultez [inscription d’un rappel com](registering-a-com-callback.md).</span><span class="sxs-lookup"><span data-stu-id="c9984-115">For information on event notification, see [Registering a COM Callback](registering-a-com-callback.md).</span></span>

<span data-ttu-id="c9984-116">L’exemple suivant utilise un minuteur pour interroger l’état d’un travail.</span><span class="sxs-lookup"><span data-stu-id="c9984-116">The following example uses a timer to poll for the state of a job.</span></span> <span data-ttu-id="c9984-117">L’exemple suppose que le pointeur d’interface [**méthode ibackgroundcopyjob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) est valide.</span><span class="sxs-lookup"><span data-stu-id="c9984-117">The example assumes the [**IBackgroundCopyJob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) interface pointer is valid.</span></span>


```C++
HRESULT hr;
IBackgroundCopyJob* pJob;
BG_JOB_STATE State;
HANDLE hTimer = NULL;
LARGE_INTEGER liDueTime;
//IBackgroundCopyError* pError = NULL;
//BG_JOB_PROGRESS Progress;
//WCHAR *JobStates[] = { L"Queued", L"Connecting", L"Transferring",
//                       L"Suspended", L"Error", L"Transient Error",
//                       L"Transferred", L"Acknowledged", L"Canceled"
//                     };

liDueTime.QuadPart = -10000000;  //Poll every 1 second
hTimer = CreateWaitableTimer(NULL, FALSE, L"MyTimer");
SetWaitableTimer(hTimer, &liDueTime, 1000, NULL, NULL, 0);

do
{
  WaitForSingleObject(hTimer, INFINITE);

  //Use JobStates[State] to set the window text in a user interface.
  hr = pJob->GetState(&State);
  if (FAILED(hr))
  {
    //Handle error
  }

  if (BG_JOB_STATE_TRANSFERRED == State)
    //Call pJob->Complete(); to acknowledge that the transfer is complete
    //and make the file available to the client.
  else if (BG_JOB_STATE_ERROR == State || BG_JOB_STATE_TRANSIENT_ERROR == State)
    //Call pJob->GetError(&pError); to retrieve an IBackgroundCopyError interface 
    //pointer which you use to determine the cause of the error.
  else if (BG_JOB_STATE_TRANSFERRING == State)
    //Call pJob->GetProgress(&Progress); to determine the number of bytes 
    //and files transferred.
} while (BG_JOB_STATE_TRANSFERRED != State && 
         BG_JOB_STATE_ERROR != State &&
         BG_JOB_STATE_TRANSIENT_ERROR != State);
CancelWaitableTimer(hTimer);
CloseHandle(hTimer);
```



 

 




