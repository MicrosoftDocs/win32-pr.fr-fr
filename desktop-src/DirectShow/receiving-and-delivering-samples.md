---
description: Réception et envoi d’exemples
ms.assetid: 92954b40-1424-4dee-997c-fc41089b7fa5
title: Réception et envoi d’exemples
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a364743e0dfc201d419a61fa4c88bde686976d6b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103846154"
---
# <a name="receiving-and-delivering-samples"></a>Réception et envoi d’exemples

Le pseudo-code suivant montre comment implémenter la méthode **IMemInput :: Receive** :


```C++
HRESULT CMyInputPin::Receive(IMediaSample *pSample)
{
    CAutoLock cObjectLock(&m_csReceive);

    // Perhaps the filter needs to wait on something.
    WaitForSingleObject(m_hSomeEventThatReceiveNeedsToWaitOn, INFINITE);

    // Before using resources, make sure it is safe to proceed. Do not
    // continue if the base-class method returns anything besides S_OK.
    hr = CBaseInputPin::Receive(pSample);
    if (hr != S_OK) 
    {
        return hr;
    }

    /* It is safe to use resources allocated in Active and Pause. */

    // Deliver sample(s), via your output pin(s).
    for (each output pin)
        pOutputPin->Deliver(pSample);

    return hr;
}
```



La méthode **Receive** contient le verrou de streaming, et non le verrou de filtre. Le filtre devra peut-être attendre un événement avant de pouvoir traiter les données, comme indiqué ici par l’appel à **WaitForSingleObject**. Chaque filtre n’a pas besoin d’effectuer cette opération. La méthode [**CBaseInputPin :: Receive**](cbaseinputpin-receive.md) vérifie certaines conditions générales de diffusion en continu. Elle retourne VFW \_ E \_ mauvais \_ État si le filtre est arrêté, S \_ false si le filtre est vidé, et ainsi de suite. Tout code de retour autre que \_ OK indique que la méthode de **réception** doit être renvoyée immédiatement et ne pas traiter l’exemple.

Une fois l’exemple traité, fournissez-le au filtre en aval en appelant [**CBaseOutputPin ::D eliver**](cbaseoutputpin-deliver.md). Cette méthode d’assistance appelle **IMemInputPin :: Receive** sur la broche d’entrée en aval. Un filtre peut remettre des échantillons à plusieurs codes confidentiels.

 

 



