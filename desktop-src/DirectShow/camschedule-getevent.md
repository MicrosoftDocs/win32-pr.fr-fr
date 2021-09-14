---
description: La méthode GetEvent récupère un handle d’événement, qui est utilisé pour signaler une modification de l’heure suivante de l’avis.
ms.assetid: 2548a321-df65-4a5b-9e6a-8bbc031254c7
title: Méthode CAMSchedule. GetEvent (Dsschedule. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMSchedule.GetEvent
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 360a4b88c8c03d2f04ad55bc65eebf6be3797c92
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127094981"
---
# <a name="camschedulegetevent-method"></a>Méthode CAMSchedule. GetEvent

La `GetEvent` méthode récupère un handle d’événement, qui est utilisé pour signaler une modification de l’heure suivante de l’avis.

## <a name="syntax"></a>Syntaxe


```C++
HANDLE GetEvent();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur de retour

Retourne un handle pour un événement.

## <a name="remarks"></a>Notes

Si l’heure suivante de l’avis change en d’autres termes, si une nouvelle demande de notification est ajoutée au début de la liste, le planificateur signale cet événement. L’horloge doit appeler la méthode [**CAMSchedule :: Advise**](camschedule-advise.md) pour déterminer l’heure de l’avis suivante.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Dsschedule. h (inclure Flux. h)</dt> </dl>                                                                                |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CAMSchedule, classe**](camschedule.md)
</dt> </dl>

 

 




