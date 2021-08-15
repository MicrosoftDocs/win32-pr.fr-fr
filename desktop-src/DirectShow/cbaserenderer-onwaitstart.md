---
description: La méthode OnWaitStart est appelée quand le filtre commence à attendre l’heure de la présentation d’un exemple.
ms.assetid: 598cd676-3afe-4ec9-ae38-83971412e6a7
title: Méthode CBaseRenderer. OnWaitStart (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.OnWaitStart
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: eaad14d0eec765a0ad12693c0a1eee67386bc9bb26344ee52c29224d129edf5c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117822646"
---
# <a name="cbaserendereronwaitstart-method"></a>Méthode CBaseRenderer. OnWaitStart

La `OnWaitStart` méthode est appelée lorsque le filtre commence à attendre l’heure de la présentation d’un exemple.

## <a name="syntax"></a>Syntaxe


```C++
virtual void OnWaitStart();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Remarques

La méthode [**CBaseRenderer :: WaitForRenderTime**](cbaserenderer-waitforrendertime.md) appelle cette méthode lorsqu’elle commence à attendre l’heure de la présentation d’un exemple. Cette méthode n’effectue aucune opération dans la classe de base, mais la classe dérivée peut la substituer.

Si vous implémentez le contrôle de qualité, vous pouvez substituer cette méthode avec la méthode [**CBaseRenderer :: OnWaitEnd**](cbaserenderer-onwaitend.md) . Vous pouvez utiliser ces méthodes pour suivre les performances du filtre.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Renbase. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseRenderer, classe**](cbaserenderer.md)
</dt> </dl>

 

 




