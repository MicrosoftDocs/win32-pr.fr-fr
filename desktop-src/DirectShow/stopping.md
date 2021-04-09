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
# <a name="stopping"></a><span data-ttu-id="c1cd6-103">En cours d’arrêt</span><span class="sxs-lookup"><span data-stu-id="c1cd6-103">Stopping</span></span>

<span data-ttu-id="c1cd6-104">La méthode Stop doit débloquer la méthode **Receive** et **Annuler** la validation des allocateurs du filtre.</span><span class="sxs-lookup"><span data-stu-id="c1cd6-104">The **Stop** method must unblock the **Receive** method and decommit the filter's allocators.</span></span> <span data-ttu-id="c1cd6-105">La désactivation d’un allocateur force tous les appels **GetBuffer** en attente à retourner, ce qui débloque les filtres en amont qui attendent des exemples.</span><span class="sxs-lookup"><span data-stu-id="c1cd6-105">Decommitting an allocator forces any pending **GetBuffer** calls to return, which unblocks upstream filters that are waiting for samples.</span></span> <span data-ttu-id="c1cd6-106">La méthode **Stop** contient le verrou de filtre, puis appelle la méthode [**CBaseFilter :: Stop**](cbasefilter-stop.md) , qui appelle [**CBasePin :: inactive**](cbasepin-inactive.md) sur tous les codes confidentiels du filtre :</span><span class="sxs-lookup"><span data-stu-id="c1cd6-106">The **Stop** method holds the filter lock and then calls the [**CBaseFilter::Stop**](cbasefilter-stop.md) method, which calls [**CBasePin::Inactive**](cbasepin-inactive.md) on all of the filter's pins:</span></span>


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



<span data-ttu-id="c1cd6-107">Remplacez la méthode **inactive** de la broche d’entrée comme suit :</span><span class="sxs-lookup"><span data-stu-id="c1cd6-107">Override the input pin's **Inactive** method as follows:</span></span>


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



 

 



