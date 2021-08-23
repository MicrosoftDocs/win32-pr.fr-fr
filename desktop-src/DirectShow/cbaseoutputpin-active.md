---
description: 'CBaseOutputPin. active, méthode : la méthode active indique au code confidentiel que le filtre est maintenant actif.'
ms.assetid: 35df4305-0e2c-4ee1-bc63-db5aec864c46
title: CBaseOutputPin. active, méthode (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseOutputPin.Active
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 94e71b3a85fdddd3ea4554575b07871ecdc09070f00c988f24f31378e9effb6c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119640029"
---
# <a name="cbaseoutputpinactive-method"></a>CBaseOutputPin. active, méthode

La `Active` méthode notifie le code confidentiel que le filtre est maintenant actif.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT Active();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Retourne une valeur **HRESULT** . Les valeurs possibles sont les suivantes :



| Code de retour                                                                                          | Description                           |
|------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>                 | Réussite.<br/>                   |
| <dl> <dt>**VFW \_ E \_ aucun \_ allocateur**</dt> </dl> | Aucun allocateur n’est disponible.<br/> |



 

## <a name="remarks"></a>Remarques

Cette méthode remplace la méthode [**CBasePin :: active**](cbasepin-active.md) . Elle appelle la méthode [**IMemAllocator :: Commit**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-commit) sur l’allocateur pour allouer de la mémoire pour les mémoires tampons.

Si vous substituez cette méthode, appelez la méthode de la classe de base à partir de votre méthode de substitution.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Amfilter. h (inclure Flux. h)</dt> </dl>                                                                                  |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseOutputPin, classe**](cbaseoutputpin.md)
</dt> </dl>

 

 




