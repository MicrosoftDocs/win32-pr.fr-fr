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
ms.openlocfilehash: f282f45bb895a941c44cb70cf5d9d3d373bf8649
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127230489"
---
# <a name="cbaseoutputpinactive-method"></a>CBaseOutputPin. active, méthode

La `Active` méthode notifie le code confidentiel que le filtre est maintenant actif.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT Active();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur de retour

Retourne une valeur **HRESULT** . Les valeurs possibles sont les suivantes :



| Code de retour                                                                                          | Description                           |
|------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>                 | Réussite.<br/>                   |
| <dl> <dt>**VFW \_ E \_ aucun \_ allocateur**</dt> </dl> | Aucun allocateur n’est disponible.<br/> |



 

## <a name="remarks"></a>Notes

Cette méthode remplace la méthode [**CBasePin :: active**](cbasepin-active.md) . Elle appelle la méthode [**IMemAllocator :: Commit**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-commit) sur l’allocateur pour allouer de la mémoire pour les mémoires tampons.

Si vous substituez cette méthode, appelez la méthode de la classe de base à partir de votre méthode de substitution.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Amfilter. h (inclure Flux. h)</dt> </dl>                                                                                  |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseOutputPin, classe**](cbaseoutputpin.md)
</dt> </dl>

 

 




