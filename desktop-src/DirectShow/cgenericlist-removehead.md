---
description: La méthode RemoveHead supprime le premier élément de la liste.
ms.assetid: 95902028-d2c2-4c16-9ca6-ef57174a9292
title: Méthode CGenericList. RemoveHead (Wxlist. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CGenericList.RemoveHead
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7b374ad6a08aac039de3c7d54ee4403f240fdf6bf9839a5ea2554901de789f11
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119317749"
---
# <a name="cgenericlistremovehead-method"></a>Méthode CGenericList. RemoveHead

La `RemoveHead` méthode supprime le premier élément de la liste.

## <a name="syntax"></a>Syntaxe


```C++
OBJECT* RemoveHead();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Retourne un pointeur vers un objet de type **Object** (le type de modèle), ou **null** si la liste est vide.

## <a name="remarks"></a>Remarques

Cette méthode supprime le nœud de liste, mais pas l’élément contenu dans le nœud.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Wxlist. h (inclure Flux. h)</dt> </dl>                                                                                    |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CGenericList, classe**](cgenericlist.md)
</dt> </dl>

 

 




