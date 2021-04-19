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
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537116"
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
| <dl> <dt>**\_OK**</dt> </dl>    | Opération réussie.<br/>                              |
| <dl> <dt>**S \_ false**</dt> </dl> | Le filtre ne contient pas ce code confidentiel.<br/> |



 

## <a name="remarks"></a>Notes

La méthode de destructeur appelle cette méthode pour supprimer la broche de sortie du filtre.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Source. h (include streams. h)</dt> </dl>                                                                                    |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CSource, classe**](csource.md)
</dt> </dl>

 

 




