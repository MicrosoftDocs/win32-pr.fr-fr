---
description: Pointeur vers une section critique utilisée pour sérialiser les modifications d’État.
ms.assetid: 4fecd9a6-54df-49d7-bf2f-5dcaef919ad7
title: 'Membre CBaseFilter :: m_pLock (Amfilter. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_pLock
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3bc8d3b627e6cd8c3ae4821864f6980db5acd251c721bb8841be40e04377ad55
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118659792"
---
# <a name="cbasefilterm_plock-member"></a>CBaseFilter :: m \_ pLock, membre

Pointeur vers une section critique utilisée pour sérialiser les modifications d’État.

## <a name="syntax"></a>Syntaxe


```C++
CCritSec *m_pLock;
```



## <a name="remarks"></a>Notes

Cette variable est initialisée dans le constructeur de classe ; consultez [**CBaseFilter :: CBaseFilter**](cbasefilter-cbasefilter.md).

Tenez cette section critique lors des transitions d’État ou lorsqu’une méthode accède à l’État sur plusieurs opérations. La classe de base contient la section critique dans les méthodes suivantes :

-   [**CBaseFilter::FindPin**](cbasefilter-findpin.md)
-   [**CBaseFilter::GetSyncSource**](cbasefilter-getsyncsource.md)
-   [**CBaseFilter::JoinFilterGraph**](cbasefilter-joinfiltergraph.md)
-   [**CBaseFilter :: IsActive**](cbasefilter-isactive.md)
-   [**CBaseFilter::SetSyncSource**](cbasefilter-setsyncsource.md)
-   [**CBaseFilter ::P ause**](cbasefilter-pause.md)
-   [**CBaseFilter :: Run**](cbasefilter-run.md)
-   [**CBaseFilter :: Stop**](cbasefilter-stop.md)

Ne conservent pas cette section critique pendant les opérations de diffusion en continu (autrement dit, lors de la transmission d’exemples à un filtre en aval). Sérialisez les opérations de diffusion en continu à l’aide d’une section critique différente. Dans le cas contraire, cela peut provoquer un interblocage.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Amfilter. h (inclure Flux. h)</dt> </dl>                                                                                  |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseFilter, classe**](cbasefilter.md)
</dt> <dt>

[Threads et sections critiques](threads-and-critical-sections.md)
</dt> </dl>

 

 




