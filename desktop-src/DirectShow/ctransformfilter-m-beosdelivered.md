---
description: Indicateur qui spécifie si le filtre a envoyé une notification de fin de flux.
ms.assetid: 93f897de-04bb-4de4-a612-39b27c7d6f6c
title: 'Membre CTransformFilter :: m_bEOSDelivered (Transfrm. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_bEOSDelivered
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f24b87f9808c53b5f64f66031a8ee2a4e9449089
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127195543"
---
# <a name="ctransformfilterm_beosdelivered-member"></a>CTransformFilter :: m \_ bEOSDelivered, membre

Indicateur qui spécifie si le filtre a envoyé une notification de fin de flux.

## <a name="syntax"></a>Syntaxe


```C++
BOOL m_bEOSDelivered;
```



## <a name="remarks"></a>Notes

Si le filtre s’interrompt lorsqu’il n’a pas de connexion d’entrée, il envoie une notification de fin de flux en aval et définit cet indicateur sur **true**. La notification de fin de flux garantit que le filtre en aval n’attend pas les exemples. Notez que la méthode [**EndOfStream**](ctransformfilter-endofstream.md) du filtre ne définit pas cet indicateur.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Transfrm. h (inclure Flux. h)</dt> </dl>                                                                                  |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CTransformFilter, classe**](ctransformfilter.md)
</dt> </dl>

 

 




