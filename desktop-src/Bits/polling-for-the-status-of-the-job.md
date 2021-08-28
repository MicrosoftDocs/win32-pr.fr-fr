---
title: Interrogation de l’état du travail
description: Par défaut, une application doit interroger les modifications de l’état d’un travail.
ms.assetid: b12ee1e0-d3d9-4d31-b2af-7491480968f0
keywords:
- transférer les BITS de tâche, interrogation
- interrogation des BITS d’état de la tâche
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af7f1f47a891968e686ae1ffc083bfa9b00d79c8bdc22e2c78ea523ef7ec707e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119701719"
---
# <a name="polling-for-the-status-of-the-job"></a>Interrogation de l’état du travail

Par défaut, une application doit interroger les modifications de l’état d’un travail. Pour capturer les modifications de l’état du travail, appelez la méthode [**méthode ibackgroundcopyjob :: GetState**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-getstate) . Pour capturer les modifications du nombre d’octets et de fichiers transférés, appelez la méthode [**méthode ibackgroundcopyjob :: GetProgress**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-getprogress) . Pour récupérer des informations de progression sur la partie réponse d’une tâche de chargement-réponse, appelez la méthode [**IBackgroundCopyJob2 :: GetReplyProgress**](/windows/desktop/api/Bits1_5/nf-bits1_5-ibackgroundcopyjob2-getreplyprogress) . Pour obtenir un exemple qui utilise les informations de progression, consultez [détermination de la progression d’un travail](determining-the-progress-of-a-job.md).

L’énumération de l' [**\_ \_ État du travail BG**](/windows/desktop/api/Bits/ne-bits-bg_job_state) définit les États d’un travail et la structure de [**\_ \_ progression du travail BG**](/windows/desktop/api/Bits/ns-bits-bg_job_progress) contient des informations sur le nombre d’octets et de fichiers transférés.

Pour utiliser l’interrogation, vous devez créer un mécanisme pour lancer l’interrogation. Par exemple, créez un minuteur ou utilisez un bouton « mettre à jour » sur l’interface utilisateur. Toutefois, il peut être plus facile de s’inscrire pour la notification d’événements et de recevoir des événements lorsque l’État ou la progression change. Pour plus d’informations sur la notification d’événements, consultez [inscription d’un rappel com](registering-a-com-callback.md).

L’exemple suivant utilise un minuteur pour interroger l’état d’un travail. L’exemple suppose que le pointeur d’interface [**méthode ibackgroundcopyjob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) est valide.


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



 

 




