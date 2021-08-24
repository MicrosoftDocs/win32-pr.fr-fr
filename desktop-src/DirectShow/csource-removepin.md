---
description: La méthode RemovePin supprime un pin spécifié du filtre. La méthode ne supprime pas le code confidentiel.
ms.assetid: 104eccfa-3fff-4f47-ba1b-3206eab9eef8
title: Méthode CSource. RemovePin (source. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSource.RemovePin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 376c2b292b0bdba9a79593c8264ecce17b916a88cfd49407638d637d1fbda6b0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119767839"
---
# <a name="csourceremovepin-method"></a>Méthode CSource. RemovePin

La `RemovePin` méthode supprime un pin spécifié du filtre. La méthode ne supprime pas le code confidentiel.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT RemovePin(
   CSourceStream *pStream
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pStream* 
</dt> <dd>

Pointeur vers l’objet [**CSourceStream**](csourcestream.md) qui implémente le code confidentiel.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne l’une des valeurs **HRESULT** indiquées dans le tableau suivant.



| Code de retour                                                                             | Description                                      |
|-----------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>    | Réussite.<br/>                              |
| <dl> <dt>**S \_ false**</dt> </dl> | Le filtre ne contient pas ce code confidentiel.<br/> |



 

## <a name="remarks"></a>Remarques

La méthode de destructeur appelle cette méthode pour supprimer la broche de sortie du filtre.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Source. h (inclure Flux. h)</dt> </dl>                                                                                    |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CSource, classe**](csource.md)
</dt> </dl>

 

 




