---
title: Connexion au service BITS
description: Pour vous connecter au service BITS, créez une instance de l’objet BackgroundCopyManager comme indiqué dans l’exemple suivant.
ms.assetid: 2fa88277-c7a1-4f1c-a63c-e2d27a163249
ms.topic: article
ms.date: 11/29/2018
ms.openlocfilehash: 5dacd97b78fa9c5d3a1e410a44e3c376368654e99a6f4ace9161d36b127d9a94
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119528939"
---
# <a name="connecting-to-the-bits-service"></a>Connexion au service BITS

Pour vous connecter au service du système BITS, créez une instance de l’objet BackgroundCopyManager comme indiqué dans l’exemple suivant. le service système BITS est le service système Windows s’exécutant sur l’ordinateur client qui implémente la fonctionnalité de transfert en arrière-plan.


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



Pour tester une version spécifique de BITS, utilisez un identificateur de classe symbolique pour BackgroundCopyManager en fonction de la version que vous souhaitez vérifier. Par exemple, pour tester BITS 10,2, utilisez CLSID \_ BackgroundCopyManager10 \_ 2.

L’exemple suivant montre comment utiliser l’un des identificateurs de classe symbolique.


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



Utilisez les méthodes de l’interface [**IBackgroundCopyManager**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopymanager) pour [créer des tâches de transfert](creating-a-job.md), [énumérer des travaux](enumerating-jobs-in-the-transfer-queue.md) dans la file d’attente et récupérer des [travaux](/windows/desktop/api/Bits/nf-bits-ibackgroundcopymanager-getjob).



BITS requiert que les proxies d’interface du client utilisent le niveau d’identité ou d’emprunt d’identité. Si l’application n’appelle pas [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity), com utilise l’identification par défaut. BITS échoue avec E \_ ACCESSDENIED si le niveau d’emprunt d’identité correct n’est pas défini. Si vous fournissez une bibliothèque qui exerce les interfaces BITS et qu’une application qui appelle votre bibliothèque définit le niveau d’emprunt d’identité ci-dessous, vous devrez appeler [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) pour définir le niveau d’emprunt d’identité approprié pour chaque interface bits que vous appelez.

Avant de quitter votre application, libérez votre copie du pointeur d’interface [**IBackgroundCopyManager**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopymanager) , comme indiqué dans l’exemple suivant.


```C++
if (g_pbcm)
{
  g_pbcm->Release();
  g_pbcm = NULL;
}
CoUninitialize();
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Appel de bits à partir de .net et C#](/windows/desktop/Bits/bits-dot-net) pour bits
</dt> </dl>

 

 