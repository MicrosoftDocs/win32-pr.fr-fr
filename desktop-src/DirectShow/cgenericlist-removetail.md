---
description: La méthode RemoveTail supprime le dernier élément de la liste.
ms.assetid: 377af676-8042-430e-87a6-b41c00482a90
title: Méthode CGenericList. RemoveTail (Wxlist. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CGenericList.RemoveTail
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a7b98187c663f643acdce28b4f12ebc37b1d4c25
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127010096"
---
# <a name="cgenericlistremovetail-method"></a>Méthode CGenericList. RemoveTail

La `RemoveTail` méthode supprime le dernier élément de la liste.

## <a name="syntax"></a>Syntaxe


```C++
OBJECT* RemoveTail();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur de retour

Retourne un pointeur vers un objet de type **Object** (le type de modèle), ou **null** si la liste est vide.

## <a name="remarks"></a>Notes

Cette méthode supprime le nœud de liste, mais pas l’élément contenu dans le nœud.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Wxlist. h (inclure Flux. h)</dt> </dl>                                                                                    |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CGenericList, classe**](cgenericlist.md)
</dt> </dl>

 

 




