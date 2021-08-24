---
description: La méthode SetTimeAdvise configure un événement de minuterie avec l’horloge de référence.
ms.assetid: d0ab5c21-3585-413b-ba75-8591ed4527e4
title: Méthode CCmdQueue. SetTimeAdvise (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CCmdQueue.SetTimeAdvise
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ecfa02354ad3662a6fd9060fff80b74635c63ade57539fbbd1307fa1d65e8872
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119757129"
---
# <a name="ccmdqueuesettimeadvise-method"></a>Méthode CCmdQueue. SetTimeAdvise

La `SetTimeAdvise` méthode configure un événement de minuterie avec l’horloge de référence.

## <a name="syntax"></a>Syntaxe


```C++
void SetTimeAdvise();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Remarques

Cette fonction membre appelle la méthode [**IReferenceClock :: AdviseTime**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-advisetime) pour configurer une notification pour l’heure la plus ancienne dans la file d’attente. Les commandes à durée de présentation différées sont toujours vérifiées. Si le graphique de filtre est en mode d’exécution, les commandes différées utilisant le temps de flux sont également vérifiées.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Winutil. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CCmdQueue, classe**](ccmdqueue.md)
</dt> </dl>

 

 




