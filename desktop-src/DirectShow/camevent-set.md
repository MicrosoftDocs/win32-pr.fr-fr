---
description: La méthode Set signale l’événement.
ms.assetid: dfcb1601-aa65-47f5-ae3c-f13fcd7b1398
title: CAMEvent. Set, méthode (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMEvent.Set
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c9caeed17d42d121ae9263bf6c1fcd011ed573c7
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127111354"
---
# <a name="cameventset-method"></a>CAMEvent. Set, méthode

La `Set` méthode signale l’événement.

## <a name="syntax"></a>Syntaxe


```C++
void Set();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur de retour

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Notes

Le comportement varie selon que l’objet est un événement de réinitialisation automatique ou un événement de réinitialisation manuelle :

-   **Réinitialisation automatique**: si des threads attendent cet événement, un thread est libéré et l’événement est réinitialisé. Si aucun thread n’attend cet événement, l’événement reste signalé.
-   **Réinitialisation manuelle**: tous les threads en attente de cet événement sont libérés. L’événement reste signalé.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Wxutil. h (inclure Flux. h)</dt> </dl>                                                                                    |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CAMEvent, classe**](camevent.md)
</dt> </dl>

 

 




