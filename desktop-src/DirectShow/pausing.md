---
description: Suspension en cours
ms.assetid: 945e1b1a-2557-4be2-bfdb-bb11ac7c3fe8
title: Suspension en cours
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15f113bdaa41709055202886112d678c2a1fbb172d99e880ceaafc997817412a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119997279"
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



 

 



