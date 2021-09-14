---
description: La méthode AddTail ajoute un élément à la fin de la liste.
ms.assetid: e365a23e-7447-42ec-b836-21dd68962db1
title: Méthode CGenericList. AddTail (Wxlist. h)-paramètre pObj
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CGenericList.AddTail
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2f1e7cd3d8758107b9529114a75b3a90527937c6
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127121969"
---
# <a name="cgenericlistaddtail-method-wxlisth---pobj-parameter"></a>Méthode CGenericList. AddTail (Wxlist. h)-paramètre pObj

La `AddTail` méthode ajoute un élément à la fin de la liste.

## <a name="syntax"></a>Syntaxe


```C++
POSITION AddTail(
   OBJECT *pObj
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pObj* 
</dt> <dd>

Pointeur vers un objet de type **Object** (type de modèle).

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Retourne une valeur de POSITION pour la nouvelle position de fin. Si la méthode échoue, elle retourne la **valeur null**.

## <a name="requirements"></a>Spécifications

| Condition requise | Valeur |
|-|-|
| En-tête | Wxlist. h (inclure Flux. h) |
| Bibliothèque| Strmbase. lib (versions commerciales); Strmbasd. lib (versions Debug) |

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CGenericList, classe**](cgenericlist.md)
</dt> </dl>

 

 




