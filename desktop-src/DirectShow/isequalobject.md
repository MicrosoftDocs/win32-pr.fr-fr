---
description: La fonction IsEqualObject vérifie si deux interfaces se trouvent sur le même objet.
ms.assetid: 51325e05-5a7f-4a80-a12e-2e7dedc028e2
title: IsEqualObject, fonction (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IsEqualObject
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e959d687d7d6b11dc6055daeda789e728d875d70
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127007536"
---
# <a name="isequalobject-function"></a>IsEqualObject fonction)

La `IsEqualObject` fonction vérifie si deux interfaces se trouvent sur le même objet.

## <a name="syntax"></a>Syntaxe


```C++
BOOL WINAPI IsEqualObject(
   IUnknown *pFirst,
   IUnknown *pSecond
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pFirst* 
</dt> <dd>

Pointeur vers une interface.

</dd> <dt>

*pSecond* 
</dt> <dd>

Pointeur vers l’autre interface.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Retourne la **valeur true** si les interfaces sont à la fois sur le même objet, ou **false** dans le cas contraire.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Wxutil. h (inclure Flux. h)</dt> </dl>                                                                                    |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fonctions d’assistance diverses](miscellaneous-helper-functions.md)
</dt> </dl>

 

 




