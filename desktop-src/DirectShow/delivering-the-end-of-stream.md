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
# <a name="delivering-the-end-of-stream"></a>Transmission de la fin du flux

Lorsque la broche d’entrée reçoit une notification de fin de flux, elle propage l’appel en aval. Tous les filtres en aval qui reçoivent des données de cette broche d’entrée doivent également recevoir la notification de fin de flux. Là encore, prenez le verrou de streaming et non le verrou de filtre. Si le filtre contient des données en attente qui n’ont pas encore été remises, le filtre doit le remettre maintenant, avant d’envoyer la notification de fin de flux. Elle ne doit pas envoyer de données après la fin du flux.


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



La méthode [**CBaseOutputPin ::D eliverendofstream**](cbaseoutputpin-deliverendofstream.md) appelle [**IPIN :: EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream) sur la broche d’entrée en aval.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Threads et sections critiques](threads-and-critical-sections.md)
</dt> </dl>

 

 



