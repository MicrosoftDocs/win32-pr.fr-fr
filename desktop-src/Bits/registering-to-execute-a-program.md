---
title: Inscription pour exécuter un programme
description: Vous pouvez vous inscrire pour que le service BITS exécute un programme en fonction des événements de travail transféré et d’erreur, mais pas des événements de modification de tâche. Le service BITS exécute le programme dans le contexte de l’utilisateur.
ms.assetid: f1996d08-0e35-403b-9cdb-dae9e1c42e05
keywords:
- BITS de notification d’événements, ligne de commande
- inscription pour les BITS de notification de ligne de commande
ms.topic: article
ms.date: 10/04/2018
ms.openlocfilehash: db86f67ad899d190b24d74bfb04c501ca7881351cfb2f37ef53300666622c317
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119922029"
---
# <a name="registering-to-execute-a-program"></a>Inscription pour exécuter un programme

Vous pouvez vous inscrire pour que le service BITS exécute un programme en fonction des événements de travail transféré et d’erreur, mais pas des événements de modification de tâche. Le service BITS exécute le programme dans le contexte de l’utilisateur.

**Pour s’inscrire pour exécuter un programme**

1.  Appelez la méthode **méthode ibackgroundcopyjob :: QueryInterface** pour récupérer un pointeur d’interface [**IBackgroundCopyJob2**](/windows/desktop/api/Bits1_5/nn-bits1_5-ibackgroundcopyjob2) . Spécifiez \_ \_ uuidof (IBackgroundCopyJob2) en tant qu’identificateur d’interface.
2.  Appelez la méthode [**IBackgroundCopyJob2 :: SetNotifyCmdLine**](/windows/desktop/api/Bits1_5/nf-bits1_5-ibackgroundcopyjob2-setnotifycmdline) pour spécifier le programme à exécuter et tous les arguments requis par le programme, tels que l’identificateur de tâche.

3.  Appelez la méthode [**méthode ibackgroundcopyjob :: SetNotifyFlags**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setnotifyflags) pour spécifier à quel moment la ligne de commande s’exécute.

    Vous pouvez uniquement spécifier les indicateurs d’événement d’erreur du travail \_ de notification BG \_ \_ transféré et des \_ événements d’erreur de notification BG \_ \_ . L' \_ indicateur de modification du travail de notification BG \_ \_ est ignoré.

Notez que le service BITS n’exécutera pas le programme si vous vous êtes également [inscrit pour recevoir des rappels com](registering-a-com-callback.md) et si le pointeur d’interface de rappel est valide ou si la méthode de notification que bits appelle retourne un code de réussite. Toutefois, si la méthode de notification retourne un code d’échec, tel que E \_ Fail, le service bits exécute la ligne de commande.

Le service BITS appelle la fonction [**CreateProcessAsUser**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessasusera) pour lancer le programme. Si vous spécifiez une chaîne de paramètre, le premier paramètre doit être le nom du programme.

L’exemple suivant montre comment s’inscrire pour exécuter un programme lorsque l’événement de transfert de tâche se produit. L’exemple suppose que le pointeur d’interface [**méthode ibackgroundcopyjob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) est valide.


```C++
#define MAX_PARAMETER_LEN 4000

HRESULT hr;
IBackgroundCopyJob* pJob;
IBackgroundCopyJob2* pJob2 = NULL;
WCHAR szJobId[48];
const WCHAR *pProgram = L"c:\\PATHHERE\\PROGRAMNAMEHERE.exe";
WCHAR szParameters[MAX_PARAMETER_LEN+1];
GUID JobId;
int rc;

hr = pJob->GetId(&JobId);
if (SUCCEEDED(hr))
{
  rc = StringFromGUID2(JobId, szJobId, ARRAYSIZE(szJobId));
  if (rc)
  {
    StringCchPrintf(szParameters, MAX_PARAMETER_LEN+1, L"%s %s", pProgram, szJobId);
    pJob->QueryInterface(__uuidof(IBackgroundCopyJob2), (void**)&pJob2);
    hr = pJob2->SetNotifyCmdLine(pProgram, szParameters);
    if (SUCCEEDED(hr))
    {
      hr = pJob->SetNotifyFlags(BG_NOTIFY_JOB_TRANSFERRED);
    }
    pJob2->Release();
    if (FAILED(hr))
    {
      //Handle error - unable to register for command line notification.
    }
  }
}
```



Lorsque l’état du travail devient État du \_ travail \_ BG \_ transféré, le service bits exécute le programme spécifié dans pProgram. L’exemple suivant est une implémentation simple d’un programme qui utilise un identificateur de tâche comme argument. Le programme suppose que le nombre correct d’arguments lui est passé.


```C++
#define WIN32_LEAN_AND_MEAN // Exclude rarely-used stuff from Windows headers
#include <windows.h>
#include <bits.h>
#include <strsafe.h>

int wmain(int argc, wchar_t *argv[])
{
 HRESULT hr;
 IBackgroundCopyManager *pManager = NULL;
 IBackgroundCopyJob *pJob = NULL;
 GUID JobId;
 LPWSTR pDisplayName = NULL;
 LPCWSTR pSuccessString = L" completed successfully.";
 LPWSTR pMessage;

 hr = CoInitializeEx(NULL, COINIT_APARTMENTTHREADED);
 hr = CoCreateInstance(__uuidof(BackgroundCopyManager),
  NULL, CLSCTX_LOCAL_SERVER,
  __uuidof(IBackgroundCopyManager), (void**)&pManager);

 if (pManager)
 {
  hr = CLSIDFromString(argv[1], &JobId);
  if (SUCCEEDED(hr))
  {
   hr = pManager->GetJob(JobId, &pJob);
   if (SUCCEEDED(hr))
   {
    hr = pJob->GetDisplayName(&pDisplayName);
    if (SUCCEEDED(hr))
    {
     int messageLen = wcslen(pDisplayName) + wcslen(pSuccessString) + 1;
     pMessage = (WCHAR*)malloc(messageLen * sizeof(WCHAR));
     if (pMessage)
     {
      StringCchPrintf(pMessage, messageLen,
       L"%s%s", pDisplayName, pSuccessString);
      MessageBox(HWND_DESKTOP, pMessage, L"MyProgram - Transferred", MB_OK);
      free(pMessage);
     }
     else
     {
      hr = E_OUTOFMEMORY;
     }
     CoTaskMemFree(pDisplayName);
    }
    pJob->Release();
   }
  }
  pManager->Release();
 }

 CoUninitialize();
 return(hr);
}
```



 

 