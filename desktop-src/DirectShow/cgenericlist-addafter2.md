---
description: La méthode AddAfter insère une liste après la position spécifiée et utilise les paramètres « POS » et « plist ».
ms.assetid: 99214667-8478-40e5-b55b-6ac47b1fb4d2
title: Méthode CGenericList. AddAfter (Wxlist. h)-POS, paramètres plist
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
ms.openlocfilehash: c6bbe26e98acc999f067a7b0e96c3716e7e0c0c0
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/16/2021
ms.locfileid: "104531107"
---
# <a name="cgenericlistaddafter-method-wxlisth---pos-plist-parameters"></a>Méthode CGenericList. AddAfter (Wxlist. h)-POS, paramètres plist

La `AddAfter` méthode insère une liste après la position spécifiée.

## <a name="syntax"></a>Syntaxe


```C++
BOOL AddAfter(
   POSITION             pos,
   CGenericList<OBJECT> *pList
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pos* 
</dt> <dd>

Position d’insertion de la liste. La liste est insérée après cette position.

</dd> <dt>

*pList* 
</dt> <dd>

Pointeur vers la liste à insérer.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne la **valeur true** en cas de réussite, ou **false** dans le cas contraire.

## <a name="requirements"></a>Configuration requise

| Condition requise | Valeur |
|-|-|
| En-tête | Wxlist. h (include streams. h) |
| Bibliothèque| Strmbase. lib (versions commerciales); Strmbasd. lib (versions Debug) |

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CGenericList, classe**](cgenericlist.md)
</dt> </dl>

 

 




