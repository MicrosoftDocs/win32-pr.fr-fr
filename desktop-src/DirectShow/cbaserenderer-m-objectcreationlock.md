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
ms.openlocfilehash: e344b20b4924ac26ebe6253f5388136b350abefe
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127010119"
---
# <a name="cbaserendererm_objectcreationlock-member"></a>CBaseRenderer :: m \_ ObjectCreationLock, membre

Verrou pour protéger la création d’objets à l’intérieur du filtre. Le filtre maintient ce verrou lorsqu’il crée la broche d’entrée ([**CBaseRenderer :: m \_ pInputPin**](cbaserenderer-m-pinputpin.md)) ou l’objet [**CRendererPosPassThru**](crendererpospassthru.md) ([**CBaseRenderer :: m \_ pPosition**](cbaserenderer-m-pposition.md)). Ce verrou empêche plusieurs threads de tenter de créer l’un de ces objets en même temps.

## <a name="syntax"></a>Syntaxe


```C++
CCritSec m_ObjectCreationLock;
```



## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Renbase. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseRenderer, classe**](cbaserenderer.md)
</dt> </dl>

 

 




