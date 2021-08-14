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
ms.openlocfilehash: e385cf887dceddcdc470b908d46f59405f573ab47837b26f8453ce6154eb0d72
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117817450"
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

## <a name="return-value"></a>Valeur retournée

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

 

 




