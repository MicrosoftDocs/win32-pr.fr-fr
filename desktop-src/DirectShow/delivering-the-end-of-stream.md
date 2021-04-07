---
description: Transmission de la fin du flux
ms.assetid: 23afdb2e-93b0-4a74-94bd-e38eb82a5995
title: Transmission de la fin du flux
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2bd80d186bd62e6360fa1600f4ba970281315aa
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103845858"
---
# <a name="delivering-the-end-of-stream"></a><span data-ttu-id="80fd5-103">Transmission de la fin du flux</span><span class="sxs-lookup"><span data-stu-id="80fd5-103">Delivering the End of Stream</span></span>

<span data-ttu-id="80fd5-104">Lorsque la broche d’entrée reçoit une notification de fin de flux, elle propage l’appel en aval.</span><span class="sxs-lookup"><span data-stu-id="80fd5-104">When the input pin receives an end-of-stream notification, it propagates the call downstream.</span></span> <span data-ttu-id="80fd5-105">Tous les filtres en aval qui reçoivent des données de cette broche d’entrée doivent également recevoir la notification de fin de flux.</span><span class="sxs-lookup"><span data-stu-id="80fd5-105">Any downstream filters that receive data from this input pin should also get the end-of-stream notification.</span></span> <span data-ttu-id="80fd5-106">Là encore, prenez le verrou de streaming et non le verrou de filtre.</span><span class="sxs-lookup"><span data-stu-id="80fd5-106">Again, take the streaming lock and not the filter lock.</span></span> <span data-ttu-id="80fd5-107">Si le filtre contient des données en attente qui n’ont pas encore été remises, le filtre doit le remettre maintenant, avant d’envoyer la notification de fin de flux.</span><span class="sxs-lookup"><span data-stu-id="80fd5-107">If the filter has pending data that was not yet delivered, the filter should deliver it now, before it sends the end-of-stream notification.</span></span> <span data-ttu-id="80fd5-108">Elle ne doit pas envoyer de données après la fin du flux.</span><span class="sxs-lookup"><span data-stu-id="80fd5-108">It should not send any data after the end of the stream.</span></span>


```C++
HRESULT CMyInputPin::EndOfStream()
{
    CAutoLock lock_it(&m_csReceive);

    /* If the pin has not delivered all of the data in the stream 
       (based on what it received previously), do so now.  */

    // Propagate EndOfStream call downstream, via your output pin(s).
    for (each output pin)
    {    
        hr = pOutputPin->DeliverEndOfStream();
    }
    return S_OK;
}
```



<span data-ttu-id="80fd5-109">La méthode [**CBaseOutputPin ::D eliverendofstream**](cbaseoutputpin-deliverendofstream.md) appelle [**IPIN :: EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream) sur la broche d’entrée en aval.</span><span class="sxs-lookup"><span data-stu-id="80fd5-109">The [**CBaseOutputPin::DeliverEndOfStream**](cbaseoutputpin-deliverendofstream.md) method calls [**IPin::EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream) on the downstream input pin.</span></span>

## <a name="related-topics"></a><span data-ttu-id="80fd5-110">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="80fd5-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="80fd5-111">Threads et sections critiques</span><span class="sxs-lookup"><span data-stu-id="80fd5-111">Threads and Critical Sections</span></span>](threads-and-critical-sections.md)
</dt> </dl>

 

 



