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
ms.openlocfilehash: b71ced14a6f92a3056ac4f42e55bc3858c578ff6
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127010026"
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

## <a name="return-value"></a>Valeur de retour

Retourne l’une des valeurs **HRESULT** indiquées dans le tableau suivant.



| Code de retour                                                                             | Description                                      |
|-----------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>    | Réussite.<br/>                              |
| <dl> <dt>**S \_ false**</dt> </dl> | Le filtre ne contient pas ce code confidentiel.<br/> |



 

## <a name="remarks"></a>Notes

La méthode de destructeur appelle cette méthode pour supprimer la broche de sortie du filtre.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Source. h (inclure Flux. h)</dt> </dl>                                                                                    |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CSource, classe**](csource.md)
</dt> </dl>

 

 




