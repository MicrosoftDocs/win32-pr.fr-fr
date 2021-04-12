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
# <a name="pausing"></a>Suspension en cours

Toutes les modifications d’état de filtre doivent contenir le verrou de filtre. Dans la méthode **Pause** , créez les ressources dont le filtre a besoin :


```C++
HRESULT CMyFilter::Pause()
{
    CAutoLock lock_it(m_pLock);

    /* Create filter resources. */

    return CBaseFilter::Pause();
}
```



La méthode [**CBaseFilter ::P ause**](cbasefilter-pause.md) définit l’état correct sur le filtre (état \_ suspendu) et appelle la méthode [**CBasePin :: active**](cbasepin-active.md) sur chaque code confidentiel connecté dans le filtre. La méthode **active** informe le code confidentiel que le filtre est devenu actif. Si le code PIN crée des ressources, remplacez la méthode **active** , comme suit :


```C++
HRESULT CMyInputPin::Active()
{
    // You do not need to hold the filter lock here. It is already held in Pause.

    /* Create pin resources. */

    return CBaseInputPin::Active()
}
```



 

 



