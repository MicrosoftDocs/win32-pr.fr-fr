---
description: La méthode AddAfter insère un élément après la position spécifiée et utilise les paramètres « p » et « pObj ».
ms.assetid: 3e1f27c5-3e04-424a-8fe3-9bfde4e3824b
title: Méthode CGenericList. AddAfter (Wxlist. h)-p, paramètres pObj
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CGenericList.AddAfter
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6de0037d76e63049294b0455c8ec1fbac82963d94febb35f7c9400ec8eae9ab5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119697529"
---
# <a name="cgenericlistaddafter-method-wxlisth---p-pobj-parameters"></a>Méthode CGenericList. AddAfter (Wxlist. h)-p, paramètres pObj

La `AddAfter` méthode insère un élément après la position spécifiée.

## <a name="syntax"></a>Syntaxe


```C++
POSITION AddAfter(
   POSITION p,
   OBJECT   *pObj
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*p* 
</dt> <dd>

Position après laquelle l’élément doit être ajouté. Si *p* est **null**, la méthode ajoute l’élément au début de la liste.

</dd> <dt>

*pObj* 
</dt> <dd>

Pointeur vers un objet de type **Object** (type de modèle).

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne l’indicateur de position de l’élément inséré.

## <a name="requirements"></a>Configuration requise

| Condition requise | Valeur |
|-|-|
| En-tête | Wxlist. h (inclure Flux. h) |
| Bibliothèque| Strmbase. lib (versions commerciales); Strmbasd. lib (versions Debug) |

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CGenericList, classe**](cgenericlist.md)
</dt> </dl>

 

 




