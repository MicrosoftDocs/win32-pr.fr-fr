---
description: La méthode obtenir récupère l’élément à la position spécifiée.
ms.assetid: cafa4083-96e6-4ed3-afbc-5828b7f1c5be
title: CGenericList. obten, méthode (Wxlist. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CGenericList.Get
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 02af7d57d2219e6eb0506a8ab11521b4cf3570eb
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127007639"
---
# <a name="cgenericlistget-method"></a>CGenericList. obten, méthode

La `Get` méthode récupère l’élément à la position spécifiée.

## <a name="syntax"></a>Syntaxe


```C++
OBJECT* Get(
   POSITION pos
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pos* 
</dt> <dd>

Indicateur de position de l’élément à récupérer.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Retourne un pointeur vers un objet de type **Object** (le type de modèle).

## <a name="remarks"></a>Notes

Si *pos* a la **valeur null**, la méthode retourne la **valeur null**.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Wxlist. h (inclure Flux. h)</dt> </dl>                                                                                    |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CGenericList, classe**](cgenericlist.md)
</dt> </dl>

 

 




