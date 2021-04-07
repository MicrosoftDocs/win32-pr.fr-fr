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
# <a name="receiving-and-delivering-samples"></a><span data-ttu-id="95f88-103">Réception et envoi d’exemples</span><span class="sxs-lookup"><span data-stu-id="95f88-103">Receiving and Delivering Samples</span></span>

<span data-ttu-id="95f88-104">Le pseudo-code suivant montre comment implémenter la méthode **IMemInput :: Receive** :</span><span class="sxs-lookup"><span data-stu-id="95f88-104">The following pseudocode shows how to implement the **IMemInput::Receive** method:</span></span>


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



<span data-ttu-id="95f88-105">La méthode **Receive** contient le verrou de streaming, et non le verrou de filtre.</span><span class="sxs-lookup"><span data-stu-id="95f88-105">The **Receive** method holds the streaming lock, not the filter lock.</span></span> <span data-ttu-id="95f88-106">Le filtre devra peut-être attendre un événement avant de pouvoir traiter les données, comme indiqué ici par l’appel à **WaitForSingleObject**.</span><span class="sxs-lookup"><span data-stu-id="95f88-106">The filter might need to wait on some event before it can process the data, shown here by the call to **WaitForSingleObject**.</span></span> <span data-ttu-id="95f88-107">Chaque filtre n’a pas besoin d’effectuer cette opération.</span><span class="sxs-lookup"><span data-stu-id="95f88-107">Not every filter will need to do this.</span></span> <span data-ttu-id="95f88-108">La méthode [**CBaseInputPin :: Receive**](cbaseinputpin-receive.md) vérifie certaines conditions générales de diffusion en continu.</span><span class="sxs-lookup"><span data-stu-id="95f88-108">The [**CBaseInputPin::Receive**](cbaseinputpin-receive.md) method verifies some general streaming conditions.</span></span> <span data-ttu-id="95f88-109">Elle retourne VFW \_ E \_ mauvais \_ État si le filtre est arrêté, S \_ false si le filtre est vidé, et ainsi de suite.</span><span class="sxs-lookup"><span data-stu-id="95f88-109">It returns VFW\_E\_WRONG\_STATE if the filter is stopped, S\_FALSE if the filter is flushing, and so forth.</span></span> <span data-ttu-id="95f88-110">Tout code de retour autre que \_ OK indique que la méthode de **réception** doit être renvoyée immédiatement et ne pas traiter l’exemple.</span><span class="sxs-lookup"><span data-stu-id="95f88-110">Any return code other than S\_OK indicates that the **Receive** method should return immediately and not process the sample.</span></span>

<span data-ttu-id="95f88-111">Une fois l’exemple traité, fournissez-le au filtre en aval en appelant [**CBaseOutputPin ::D eliver**](cbaseoutputpin-deliver.md).</span><span class="sxs-lookup"><span data-stu-id="95f88-111">After the sample is processed, deliver it to the downstream filter by calling [**CBaseOutputPin::Deliver**](cbaseoutputpin-deliver.md).</span></span> <span data-ttu-id="95f88-112">Cette méthode d’assistance appelle **IMemInputPin :: Receive** sur la broche d’entrée en aval.</span><span class="sxs-lookup"><span data-stu-id="95f88-112">This helper method calls **IMemInputPin::Receive** on the downstream input pin.</span></span> <span data-ttu-id="95f88-113">Un filtre peut remettre des échantillons à plusieurs codes confidentiels.</span><span class="sxs-lookup"><span data-stu-id="95f88-113">A filter might deliver samples to several pins.</span></span>

 

 



