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
ms.openlocfilehash: 24313b908f1271f270e28b08058c415ed82396fe
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127012289"
---
# <a name="ccmdqueuesettimeadvise-method"></a>Méthode CCmdQueue. SetTimeAdvise

La `SetTimeAdvise` méthode configure un événement de minuterie avec l’horloge de référence.

## <a name="syntax"></a>Syntaxe


```C++
void SetTimeAdvise();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur de retour

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Notes

Cette fonction membre appelle la méthode [**IReferenceClock :: AdviseTime**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-advisetime) pour configurer une notification pour l’heure la plus ancienne dans la file d’attente. Les commandes à durée de présentation différées sont toujours vérifiées. Si le graphique de filtre est en mode d’exécution, les commandes différées utilisant le temps de flux sont également vérifiées.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Winutil. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CCmdQueue, classe**](ccmdqueue.md)
</dt> </dl>

 

 




