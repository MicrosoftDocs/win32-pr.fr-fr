---
description: Suspension en cours
ms.assetid: 945e1b1a-2557-4be2-bfdb-bb11ac7c3fe8
title: Suspension en cours
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a07f6f610c3cfac9361e1db40c0fcd37b90645b2
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104109510"
---
# <a name="pausing"></a><span data-ttu-id="ff50a-103">Suspension en cours</span><span class="sxs-lookup"><span data-stu-id="ff50a-103">Pausing</span></span>

<span data-ttu-id="ff50a-104">Toutes les modifications d’état de filtre doivent contenir le verrou de filtre.</span><span class="sxs-lookup"><span data-stu-id="ff50a-104">All filter state changes must hold the filter lock.</span></span> <span data-ttu-id="ff50a-105">Dans la méthode **Pause** , créez les ressources dont le filtre a besoin :</span><span class="sxs-lookup"><span data-stu-id="ff50a-105">In the **Pause** method, create any resources the filter needs:</span></span>


```C++
HRESULT CMyFilter::Pause()
{
    CAutoLock lock_it(m_pLock);

    /* Create filter resources. */

    return CBaseFilter::Pause();
}
```



<span data-ttu-id="ff50a-106">La méthode [**CBaseFilter ::P ause**](cbasefilter-pause.md) définit l’état correct sur le filtre (état \_ suspendu) et appelle la méthode [**CBasePin :: active**](cbasepin-active.md) sur chaque code confidentiel connecté dans le filtre.</span><span class="sxs-lookup"><span data-stu-id="ff50a-106">The [**CBaseFilter::Pause**](cbasefilter-pause.md) method sets the correct state on the filter (State\_Paused) and calls the [**CBasePin::Active**](cbasepin-active.md) method on every connected pin in the filter.</span></span> <span data-ttu-id="ff50a-107">La méthode **active** informe le code confidentiel que le filtre est devenu actif.</span><span class="sxs-lookup"><span data-stu-id="ff50a-107">The **Active** method informs the pin that the filter has become active.</span></span> <span data-ttu-id="ff50a-108">Si le code PIN crée des ressources, remplacez la méthode **active** , comme suit :</span><span class="sxs-lookup"><span data-stu-id="ff50a-108">If the pin creates resources, override the **Active** method, as follows:</span></span>


```C++
HRESULT CMyInputPin::Active()
{
    // You do not need to hold the filter lock here. It is already held in Pause.

    /* Create pin resources. */

    return CBaseInputPin::Active()
}
```



 

 



