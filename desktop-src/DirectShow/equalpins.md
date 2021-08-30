---
description: La fonction EqualPins vérifie si deux broches se trouvent sur le même objet.
ms.assetid: b6a92cb6-f4a9-4a14-831c-3b123e4692c0
title: EqualPins, fonction (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EqualPins
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e304c8d9ed7ef94ee23280d1466450c73e0627d35183c7edfafc4ef13eeba636
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120079059"
---
# <a name="equalpins-function"></a>EqualPins fonction)

La fonction EqualPins vérifie si deux broches se trouvent sur le même objet.

## <a name="syntax"></a>Syntaxe


```C++
BOOL EqualPins(
   IUnknown *pPin1,
   IUnknown *pPin2
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pPin1* 
</dt> <dd>

Pointeur vers une broche.

</dd> <dt>

*pPin2* 
</dt> <dd>

Pointeur vers l’autre code confidentiel.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne la **valeur true** si les deux codes confidentiels se trouvent sur le même objet, ou **false** dans le cas contraire.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Wxutil. h (inclure Flux. h)</dt> </dl>                                                                                    |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fonctions d’assistance diverses](miscellaneous-helper-functions.md)
</dt> </dl>

 

 




