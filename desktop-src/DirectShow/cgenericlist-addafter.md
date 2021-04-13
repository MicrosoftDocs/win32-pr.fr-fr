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
ms.openlocfilehash: fbb9553310a8ba817f90464d90226eb36371505e
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/16/2021
ms.locfileid: "104323438"
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
| En-tête | Wxlist. h (include streams. h) |
| Bibliothèque| Strmbase. lib (versions commerciales); Strmbasd. lib (versions Debug) |

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CGenericList, classe**](cgenericlist.md)
</dt> </dl>

 

 




