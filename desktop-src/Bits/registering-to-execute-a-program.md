---
title: Inscription pour exécuter un programme
description: Vous pouvez vous inscrire pour que le service BITS exécute un programme en fonction des événements de travail transféré et d’erreur, mais pas des événements de modification de tâche. Le service BITS exécute le programme dans le contexte de l’utilisateur.
ms.assetid: f1996d08-0e35-403b-9cdb-dae9e1c42e05
keywords:
- BITS de notification d’événements, ligne de commande
- inscription pour les BITS de notification de ligne de commande
ms.topic: article
ms.date: 10/04/2018
ms.openlocfilehash: 7831a959a73112b21bdf3e0fbc2b7d3dd4f6a447
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103728148"
---
# <a name="registering-to-execute-a-program"></a><span data-ttu-id="09d88-106">Inscription pour exécuter un programme</span><span class="sxs-lookup"><span data-stu-id="09d88-106">Registering to Execute a Program</span></span>

<span data-ttu-id="09d88-107">Vous pouvez vous inscrire pour que le service BITS exécute un programme en fonction des événements de travail transféré et d’erreur, mais pas des événements de modification de tâche.</span><span class="sxs-lookup"><span data-stu-id="09d88-107">You can register to have BITS execute a program based on job transferred and error events, but not job modified events.</span></span> <span data-ttu-id="09d88-108">Le service BITS exécute le programme dans le contexte de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="09d88-108">BITS executes the program in the user's context.</span></span>

<span data-ttu-id="09d88-109">**Pour s’inscrire pour exécuter un programme**</span><span class="sxs-lookup"><span data-stu-id="09d88-109">**To register to execute a program**</span></span>

1.  <span data-ttu-id="09d88-110">Appelez la méthode **méthode ibackgroundcopyjob :: QueryInterface** pour récupérer un pointeur d’interface [**IBackgroundCopyJob2**](/windows/desktop/api/Bits1_5/nn-bits1_5-ibackgroundcopyjob2) .</span><span class="sxs-lookup"><span data-stu-id="09d88-110">Call the **IBackgroundCopyJob::QueryInterface** method to retrieve an [**IBackgroundCopyJob2**](/windows/desktop/api/Bits1_5/nn-bits1_5-ibackgroundcopyjob2) interface pointer.</span></span> <span data-ttu-id="09d88-111">Spécifiez \_ \_ uuidof (IBackgroundCopyJob2) en tant qu’identificateur d’interface.</span><span class="sxs-lookup"><span data-stu-id="09d88-111">Specify \_\_uuidof(IBackgroundCopyJob2) as the interface identifier.</span></span>
2.  <span data-ttu-id="09d88-112">Appelez la méthode [**IBackgroundCopyJob2 :: SetNotifyCmdLine**](/windows/desktop/api/Bits1_5/nf-bits1_5-ibackgroundcopyjob2-setnotifycmdline) pour spécifier le programme à exécuter et tous les arguments requis par le programme, tels que l’identificateur de tâche.</span><span class="sxs-lookup"><span data-stu-id="09d88-112">Call the [**IBackgroundCopyJob2::SetNotifyCmdLine**](/windows/desktop/api/Bits1_5/nf-bits1_5-ibackgroundcopyjob2-setnotifycmdline) method to specify the program to execute and any arguments required by the program, such as the job identifier.</span></span>

3.  <span data-ttu-id="09d88-113">Appelez la méthode [**méthode ibackgroundcopyjob :: SetNotifyFlags**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setnotifyflags) pour spécifier à quel moment la ligne de commande s’exécute.</span><span class="sxs-lookup"><span data-stu-id="09d88-113">Call the [**IBackgroundCopyJob::SetNotifyFlags**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setnotifyflags) method to specify when the command line executes.</span></span>

    <span data-ttu-id="09d88-114">Vous pouvez uniquement spécifier les indicateurs d’événement d’erreur du travail \_ de notification BG \_ \_ transféré et des \_ événements d’erreur de notification BG \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="09d88-114">You can only specify the BG\_NOTIFY\_JOB\_TRANSFERRED and BG\_NOTIFY\_JOB\_ERROR event flags.</span></span> <span data-ttu-id="09d88-115">L' \_ indicateur de modification du travail de notification BG \_ \_ est ignoré.</span><span class="sxs-lookup"><span data-stu-id="09d88-115">The BG\_NOTIFY\_JOB\_MODIFICATION flag is ignored.</span></span>

<span data-ttu-id="09d88-116">Notez que le service BITS n’exécutera pas le programme si vous vous êtes également [inscrit pour recevoir des rappels com](registering-a-com-callback.md) et si le pointeur d’interface de rappel est valide ou si la méthode de notification que bits appelle retourne un code de réussite.</span><span class="sxs-lookup"><span data-stu-id="09d88-116">Note that BITS will not execute the program if you also [registered to receive COM callbacks](registering-a-com-callback.md) and the callback interface pointer is valid or the notification method that BITS calls returns a success code.</span></span> <span data-ttu-id="09d88-117">Toutefois, si la méthode de notification retourne un code d’échec, tel que E \_ Fail, le service bits exécute la ligne de commande.</span><span class="sxs-lookup"><span data-stu-id="09d88-117">However, if the notification method returns a failure code, such as E\_FAIL, BITS will execute the command line.</span></span>

<span data-ttu-id="09d88-118">Le service BITS appelle la fonction [**CreateProcessAsUser**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessasusera) pour lancer le programme.</span><span class="sxs-lookup"><span data-stu-id="09d88-118">BITS calls the [**CreateProcessAsUser**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessasusera) function to launch the program.</span></span> <span data-ttu-id="09d88-119">Si vous spécifiez une chaîne de paramètre, le premier paramètre doit être le nom du programme.</span><span class="sxs-lookup"><span data-stu-id="09d88-119">If you specify a parameter string, the first parameter must be the program name.</span></span>

<span data-ttu-id="09d88-120">L’exemple suivant montre comment s’inscrire pour exécuter un programme lorsque l’événement de transfert de tâche se produit.</span><span class="sxs-lookup"><span data-stu-id="09d88-120">The following example shows how to register to execute a program when the job-transferred event occurs.</span></span> <span data-ttu-id="09d88-121">L’exemple suppose que le pointeur d’interface [**méthode ibackgroundcopyjob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) est valide.</span><span class="sxs-lookup"><span data-stu-id="09d88-121">The example assumes the [**IBackgroundCopyJob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) interface pointer is valid.</span></span>


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



<span data-ttu-id="09d88-122">Lorsque l’état du travail devient État du \_ travail \_ BG \_ transféré, le service bits exécute le programme spécifié dans pProgram.</span><span class="sxs-lookup"><span data-stu-id="09d88-122">When the state of the job becomes BG\_JOB\_STATE\_TRANSFERRED, BITS executes the program specified in pProgram.</span></span> <span data-ttu-id="09d88-123">L’exemple suivant est une implémentation simple d’un programme qui utilise un identificateur de tâche comme argument.</span><span class="sxs-lookup"><span data-stu-id="09d88-123">The following example is a simple implementation of a program that takes a job identifier as an argument.</span></span> <span data-ttu-id="09d88-124">Le programme suppose que le nombre correct d’arguments lui est passé.</span><span class="sxs-lookup"><span data-stu-id="09d88-124">The program assumes the correct number of arguments are passed to it.</span></span>


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



 

 