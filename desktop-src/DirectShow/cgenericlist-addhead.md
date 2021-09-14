---
description: La méthode AddHead ajoute un élément au début de la liste.
ms.assetid: 8f0012b7-bbc2-407c-ae5a-9843c2f692dc
title: Méthode CGenericList. AddHead (Wxlist. h)-paramètre pObj
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CGenericList.AddHead
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 62a32eb177c80d10a876a4b163c8a1609104fbea
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127006784"
---
# <a name="cgenericlistaddhead-method-wxlisth---pobj-parameter"></a>Méthode CGenericList. AddHead (Wxlist. h)-paramètre pObj

La `AddHead` méthode ajoute un élément au début de la liste.

## <a name="syntax"></a>Syntaxe


```C++
POSITION AddHead(
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

Retourne une valeur de POSITION indiquant la nouvelle position de la tête. Si la méthode échoue, la valeur de retour est **null**.

## <a name="requirements"></a>Spécifications

| Condition requise | Valeur |
|-|-|
| En-tête | Wxlist. h (inclure Flux. h) |
| Bibliothèque| Strmbase. lib (versions commerciales); Strmbasd. lib (versions Debug) |

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CGenericList, classe**](cgenericlist.md)
</dt> </dl>

 

 




