---
title: Connexion au service BITS
description: Pour vous connecter au service BITS, créez une instance de l’objet BackgroundCopyManager comme indiqué dans l’exemple suivant.
ms.assetid: 2fa88277-c7a1-4f1c-a63c-e2d27a163249
ms.topic: article
ms.date: 11/29/2018
ms.openlocfilehash: 8146fa0def8c9c7dfd976784a930f35f20c965eb
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104101861"
---
# <a name="connecting-to-the-bits-service"></a><span data-ttu-id="e1b74-103">Connexion au service BITS</span><span class="sxs-lookup"><span data-stu-id="e1b74-103">Connecting to the BITS Service</span></span>

<span data-ttu-id="e1b74-104">Pour vous connecter au service du système BITS, créez une instance de l’objet BackgroundCopyManager comme indiqué dans l’exemple suivant.</span><span class="sxs-lookup"><span data-stu-id="e1b74-104">To connect to the BITS system service, create an instance of the BackgroundCopyManager object as shown in the following example.</span></span> <span data-ttu-id="e1b74-105">Le service système BITS est le service système Windows en cours d’exécution sur l’ordinateur client qui implémente la fonctionnalité de transfert en arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="e1b74-105">The BITS system service is the Windows system service running on the client computer that implements the background transfer capability.</span></span>


```C++
#define WIN32_LEAN_AND_MEAN // Exclude rarely-used stuff from Windows headers
#include <windows.h>
#include <bits.h>

//Global variable that several of the code examples in this document reference.
IBackgroundCopyManager* g_pbcm = NULL;  
HRESULT hr;

//Specify the appropriate COM threading model for your application.
hr = CoInitializeEx(NULL, COINIT_APARTMENTTHREADED);
if (SUCCEEDED(hr))
{
  hr = CoCreateInstance(__uuidof(BackgroundCopyManager), NULL,
                        CLSCTX_LOCAL_SERVER,
                        __uuidof(IBackgroundCopyManager),
                        (void**) &g_pbcm);
  if (SUCCEEDED(hr))
  {
    //Use g_pbcm to create, enumerate, or retrieve jobs from the queue.
  }
}
```



<span data-ttu-id="e1b74-106">Pour tester une version spécifique de BITS, utilisez un identificateur de classe symbolique pour BackgroundCopyManager en fonction de la version que vous souhaitez vérifier.</span><span class="sxs-lookup"><span data-stu-id="e1b74-106">To test for a specific version of BITS, use a symbolic class identifier for the BackgroundCopyManager based on the version you want to check.</span></span> <span data-ttu-id="e1b74-107">Par exemple, pour tester BITS 10,2, utilisez CLSID \_ BackgroundCopyManager10 \_ 2.</span><span class="sxs-lookup"><span data-stu-id="e1b74-107">For example, to test for BITS 10.2, use CLSID\_BackgroundCopyManager10\_2.</span></span>

<span data-ttu-id="e1b74-108">L’exemple suivant montre comment utiliser l’un des identificateurs de classe symbolique.</span><span class="sxs-lookup"><span data-stu-id="e1b74-108">The following example shows how to use one of the symbolic class identifiers.</span></span>


```C++
  hr = CoCreateInstance(CLSID_BackgroundCopyManager5_0, NULL,
                        CLSCTX_LOCAL_SERVER,
                        IID_IBackgroundCopyManager,
                        (void**) &g_pbcm);
  if (SUCCEEDED(hr))
  {
    //BITS 5.0 is installed.
  }
```



<span data-ttu-id="e1b74-109">Utilisez les méthodes de l’interface [**IBackgroundCopyManager**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopymanager) pour [créer des tâches de transfert](creating-a-job.md), [énumérer des travaux](enumerating-jobs-in-the-transfer-queue.md) dans la file d’attente et récupérer des [travaux](/windows/desktop/api/Bits/nf-bits-ibackgroundcopymanager-getjob).</span><span class="sxs-lookup"><span data-stu-id="e1b74-109">Use the methods of the [**IBackgroundCopyManager**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopymanager) interface to [create transfer jobs](creating-a-job.md), [enumerate jobs](enumerating-jobs-in-the-transfer-queue.md) in the queue, and [retrieve jobs](/windows/desktop/api/Bits/nf-bits-ibackgroundcopymanager-getjob).</span></span>



<span data-ttu-id="e1b74-110">BITS requiert que les proxies d’interface du client utilisent le niveau d’identité ou d’emprunt d’identité.</span><span class="sxs-lookup"><span data-stu-id="e1b74-110">BITS requires that the client's interface proxies use either the IDENTIFY or IMPERSONATE level of impersonation.</span></span> <span data-ttu-id="e1b74-111">Si l’application n’appelle pas [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity), com utilise l’identification par défaut.</span><span class="sxs-lookup"><span data-stu-id="e1b74-111">If the application does not call [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity), COM uses IDENTIFY by default.</span></span> <span data-ttu-id="e1b74-112">BITS échoue avec E \_ ACCESSDENIED si le niveau d’emprunt d’identité correct n’est pas défini.</span><span class="sxs-lookup"><span data-stu-id="e1b74-112">BITS fails with E\_ACCESSDENIED if the correct impersonation level is not set.</span></span> <span data-ttu-id="e1b74-113">Si vous fournissez une bibliothèque qui exerce les interfaces BITS et qu’une application qui appelle votre bibliothèque définit le niveau d’emprunt d’identité ci-dessous, vous devrez appeler [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) pour définir le niveau d’emprunt d’identité approprié pour chaque interface bits que vous appelez.</span><span class="sxs-lookup"><span data-stu-id="e1b74-113">If you provide a library that exercises the BITS interfaces, and an application that calls your library sets the impersonation level below IDENTIFY, then you will need to call [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) to set the correct impersonation level for each BITS interface that you call.</span></span>

<span data-ttu-id="e1b74-114">Avant de quitter votre application, libérez votre copie du pointeur d’interface [**IBackgroundCopyManager**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopymanager) , comme indiqué dans l’exemple suivant.</span><span class="sxs-lookup"><span data-stu-id="e1b74-114">Before your application exits, release your copy of the [**IBackgroundCopyManager**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopymanager) interface pointer, as shown in the following example.</span></span>


```C++
if (g_pbcm)
{
  g_pbcm->Release();
  g_pbcm = NULL;
}
CoUninitialize();
```



## <a name="related-topics"></a><span data-ttu-id="e1b74-115">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="e1b74-115">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="e1b74-116">[Appel de bits à partir de .net et C#](/windows/desktop/Bits/bits-dot-net) pour bits</span><span class="sxs-lookup"><span data-stu-id="e1b74-116">[Calling into BITS from .NET and C#](/windows/desktop/Bits/bits-dot-net) for BITS</span></span>
</dt> </dl>

 

 