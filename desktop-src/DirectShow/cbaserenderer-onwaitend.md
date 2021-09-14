---
description: La méthode OnWaitEnd est appelée lorsque le filtre est en attente d’une heure de présentation d’un exemple.
ms.assetid: 47ff8f79-da69-4dcf-8cbb-02c1b56e382e
title: Méthode CBaseRenderer. OnWaitEnd (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.OnWaitEnd
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a5a290ad5d39fc83a4213d1c8a32119b4caa9858
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127230394"
---
# <a name="cbaserendereronwaitend-method"></a>Méthode CBaseRenderer. OnWaitEnd

La `OnWaitEnd` méthode est appelée lorsque le filtre est terminé, en attendant l’heure de la présentation d’un exemple.

## <a name="syntax"></a>Syntaxe


```C++
virtual void OnWaitEnd();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur de retour

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Notes

La méthode [**CBaseRenderer :: WaitForRenderTime**](cbaserenderer-waitforrendertime.md) appelle cette méthode lorsqu’elle a fini d’attendre l’heure de la présentation d’un exemple. Cette méthode n’effectue aucune opération dans la classe de base, mais la classe dérivée peut la substituer.

Si vous implémentez le contrôle de qualité, vous pouvez substituer cette méthode avec la méthode [**CBaseRenderer :: OnWaitStart**](cbaserenderer-onwaitstart.md) . Vous pouvez utiliser ces méthodes pour suivre les performances du filtre.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Renbase. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseRenderer, classe**](cbaserenderer.md)
</dt> </dl>

 

 




