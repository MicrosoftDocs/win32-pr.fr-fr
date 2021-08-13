---
description: Verrou pour protéger la création d’objets à l’intérieur du filtre.
ms.assetid: ad1d2584-0d9e-42a8-83ea-0c1907ddcf33
title: 'Membre CBaseRenderer :: m_ObjectCreationLock (Renbase. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_ObjectCreationLock
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6b0925aab0345d5eed8da19e12f355c417d66c1f36a1384a05950a87d4c95b3e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119429309"
---
# <a name="cbaserendererm_objectcreationlock-member"></a>CBaseRenderer :: m \_ ObjectCreationLock, membre

Verrou pour protéger la création d’objets à l’intérieur du filtre. Le filtre maintient ce verrou lorsqu’il crée la broche d’entrée ([**CBaseRenderer :: m \_ pInputPin**](cbaserenderer-m-pinputpin.md)) ou l’objet [**CRendererPosPassThru**](crendererpospassthru.md) ([**CBaseRenderer :: m \_ pPosition**](cbaserenderer-m-pposition.md)). Ce verrou empêche plusieurs threads de tenter de créer l’un de ces objets en même temps.

## <a name="syntax"></a>Syntaxe


```C++
CCritSec m_ObjectCreationLock;
```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Renbase. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseRenderer, classe**](cbaserenderer.md)
</dt> </dl>

 

 




