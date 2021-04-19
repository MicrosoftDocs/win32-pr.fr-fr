---
description: La méthode Remove supprime l’élément à la position spécifiée.
ms.assetid: a7b8f6fb-f13a-4c24-aa18-463446602e29
title: CGenericList. Remove, méthode (Wxlist. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CGenericList.Remove
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d5fc3d0cd76cd78c83fa210d8b91ba97b93b92f7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106530331"
---
# <a name="cgenericlistremove-method"></a>CGenericList. Remove, méthode

La `Remove` méthode supprime l’élément à la position spécifiée.

## <a name="syntax"></a>Syntaxe


```C++
OBJECT* Remove(
   POSITION pos
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pos* 
</dt> <dd>

Valeur de POSITION indiquant l’élément à supprimer.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne un pointeur vers un objet de type **Object** (le type de modèle).

## <a name="remarks"></a>Notes

Cette méthode supprime le nœud de la liste, mais ne supprime pas l’élément contenu dans ce nœud.

Si *pos* a la **valeur null**, la méthode retourne la **valeur null**.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Wxlist. h (include streams. h)</dt> </dl>                                                                                    |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CGenericList, classe**](cgenericlist.md)
</dt> </dl>

 

 




