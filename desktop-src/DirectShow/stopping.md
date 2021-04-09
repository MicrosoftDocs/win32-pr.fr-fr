---
description: En cours d’arrêt
ms.assetid: e2796b69-05e5-4ced-b238-257952d81211
title: En cours d’arrêt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a93bde3b504400eed59190bf1651828f2f4509a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867498"
---
# <a name="stopping"></a>En cours d’arrêt

La méthode Stop doit débloquer la méthode **Receive** et **Annuler** la validation des allocateurs du filtre. La désactivation d’un allocateur force tous les appels **GetBuffer** en attente à retourner, ce qui débloque les filtres en amont qui attendent des exemples. La méthode **Stop** contient le verrou de filtre, puis appelle la méthode [**CBaseFilter :: Stop**](cbasefilter-stop.md) , qui appelle [**CBasePin :: inactive**](cbasepin-inactive.md) sur tous les codes confidentiels du filtre :


```C++
HRESULT CMyFilter::Stop()
{
    CAutoLock lock_it(m_pLock);
    // Inactivate all the pins, to protect the filter resources.
    hr = CBaseFilter::Stop();

    /* Safe to destroy filter resources used by the streaming thread. */

    return hr;
}
```



Remplacez la méthode **inactive** de la broche d’entrée comme suit :


```C++
HRESULT CMyInputPin::Inactive()
{
    // You do not need to hold the filter lock here. 
    // It is already locked in Stop.

    // Unblock Receive.
    SetEvent(m_hSomeEventThatReceiveNeedsToWaitOn);

    // Make sure Receive will fail. 
    // This also decommits the allocator.
    HRESULT hr = CBaseInputPin::Inactive();

    // Make sure Receive has completed, and is not using resources.
    {
        CAutoLock c(&m_csReceive);

        /* It is now safe to destroy filter resources used by the
           streaming thread. */
    }
    return hr;
}
```



 

 



