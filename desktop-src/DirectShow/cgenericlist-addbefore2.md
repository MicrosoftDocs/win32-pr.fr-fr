---
description: La méthode AddBefore insère une liste avant la position spécifiée. Cette méthode utilise les paramètres « POS » et « plist ».
ms.assetid: 0fdb2a59-d9de-4dbb-8536-8e10726201d0
title: Méthode CGenericList. AddBefore (Wxlist. h)-POS, paramètres plist
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
ms.openlocfilehash: 6f05d67477bb7e6c89eddfe0a68ad47d83760762fc68cddf6f73c731886f88d1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119697449"
---
# <a name="cgenericlistaddbefore-method-wxlisth---pos-plist-parameters"></a>Méthode CGenericList. AddBefore (Wxlist. h)-POS, paramètres plist

La `AddBefore` méthode insère une liste avant la position spécifiée.

## <a name="syntax"></a>Syntaxe


```C++
BOOL AddBefore(
   POSITION             pos,
   CGenericList<OBJECT> *pList
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pos* 
</dt> <dd>

Position d’insertion de la liste. La liste est insérée avant cette position.

</dd> <dt>

*pList* 
</dt> <dd>

Pointeur vers la liste à insérer.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne la **valeur true** en cas de réussite. Sinon, retourne **false**.

## <a name="requirements"></a>Configuration requise

| Condition requise | Valeur |
|-|-|
| En-tête | Wxlist. h (inclure Flux. h) |
| Bibliothèque| Strmbase. lib (versions commerciales); Strmbasd. lib (versions Debug) |

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CGenericList, classe**](cgenericlist.md)
</dt> </dl>

 

 




