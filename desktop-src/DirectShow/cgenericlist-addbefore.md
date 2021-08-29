---
description: La méthode AddBefore insère un élément avant la position spécifiée. Cette méthode utilise les paramètres « p » et « pObj ».
ms.assetid: ec10fd08-6bb9-4357-830c-78b3d3a32e03
title: Méthode CGenericList. AddBefore (Wxlist. h)-p, paramètres pObj
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CGenericList.AddBefore
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b508cc6cacba3c2a6c5877c69797ce3f6d396296610910a15701c00e3dbbadf5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119697468"
---
# <a name="cgenericlistaddbefore-method-wxlisth---p-pobj-parameters"></a>Méthode CGenericList. AddBefore (Wxlist. h)-p, paramètres pObj

La `AddBefore` méthode insère un élément avant la position spécifiée.

## <a name="syntax"></a>Syntaxe


```C++
POSITION AddBefore(
   POSITION p,
   OBJECT   *pObj
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*p* 
</dt> <dd>

Position avant laquelle insérer la liste. Si *p* est **null**, cette méthode ajoute l’élément à la fin de la liste.

</dd> <dt>

*pObj* 
</dt> <dd>

Pointeur vers un objet de type **Object** (type de modèle).

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne l’indicateur de position pour l’élément inséré.

## <a name="requirements"></a>Configuration requise

| Condition requise | Valeur |
|-|-|
| En-tête | Wxlist. h (inclure Flux. h) |
| Bibliothèque| Strmbase. lib (versions commerciales); Strmbasd. lib (versions Debug) |

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CGenericList, classe**](cgenericlist.md)
</dt> </dl>

 

 




