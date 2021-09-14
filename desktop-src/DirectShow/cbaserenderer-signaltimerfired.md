---
description: La méthode SignalTimerFired efface l’identificateur de minuterie utilisé pour planifier le rendu.
ms.assetid: b8ae362e-fcda-4888-be32-8fb910d0f0db
title: Méthode CBaseRenderer. SignalTimerFired (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.SignalTimerFired
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4dd29b37869fc6f07c2d876dfa0d1d306b04b111
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126999745"
---
# <a name="cbaserenderersignaltimerfired-method"></a>Méthode CBaseRenderer. SignalTimerFired

La `SignalTimerFired` méthode efface l’identificateur de minuterie utilisé pour planifier le rendu.

## <a name="syntax"></a>Syntaxe


```C++
virtual void SignalTimerFired();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur de retour

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Notes

Le filtre appelle cette méthode lorsque le minuteur de rendu s’active (consultez [**CBaseRenderer :: WaitForRenderTime**](cbaserenderer-waitforrendertime.md)) ou lorsque la minuterie est annulée (consultez [**CBaseRenderer :: CancelNotification**](cbaserenderer-cancelnotification.md)). La méthode réinitialise la variable de membre [**CBaseRenderer :: m \_ dwAdvise**](cbaserenderer-m-dwadvise.md) à zéro.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Renbase. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseRenderer, classe**](cbaserenderer.md)
</dt> </dl>

 

 




