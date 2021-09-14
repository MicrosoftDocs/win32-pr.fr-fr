---
description: La méthode OnWaitStart met à jour les heures d’attente et de non-attente.
ms.assetid: 3f2e2bf2-f205-4b59-b969-cf8c2136437d
title: Méthode CBaseVideoRenderer. OnWaitStart (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.OnWaitStart
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d4fab7e1a1f24c3d00f46018db9478990be71666
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127123734"
---
# <a name="cbasevideorendereronwaitstart-method"></a>Méthode CBaseVideoRenderer. OnWaitStart

La `OnWaitStart` méthode met à jour les heures d’attente et de non-attente.

## <a name="syntax"></a>Syntaxe


```C++
void OnWaitStart();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur de retour

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Notes

Cette fonction membre est appelée lors du démarrage de l’attente d’un événement de rendu. Elle est utilisée uniquement pour les mesures de performances.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Renbase. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseVideoRenderer, classe**](cbasevideorenderer.md)
</dt> </dl>

 

 




