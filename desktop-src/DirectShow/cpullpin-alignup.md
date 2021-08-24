---
description: La méthode AlignUp arrondit une valeur à une limite d’alignement spécifiée. remarque supprimée dans Windows 7. .
ms.assetid: fa2a6567-3eb1-4aa9-b966-2e88b15c67b1
title: Méthode CPullPin. AlignUp (Pullpin. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPullPin.AlignUp
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 34c45fe4a34e21647cd976adbf29dfe6723e4216d58166e7d1599d4c8d64d47e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119687759"
---
# <a name="cpullpinalignup-method"></a>Méthode CPullPin. AlignUp

La méthode **AlignUp** arrondit une valeur à une limite d’alignement spécifiée.

> [!Note]  
> supprimé dans Windows 7.

 

## <a name="syntax"></a>Syntaxe


```C++
LONGLONG AlignUp(
   LONGLONG ll,
   LONG     lAlign
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*UT* 
</dt> <dd>

Spécifie le nombre à aligner.

</dd> <dt>

*lAlign* 
</dt> <dd>

Spécifie la limite d’alignement.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne le résultat aligné.

## <a name="remarks"></a>Remarques

> [!Caution]  
> Cette méthode peut provoquer un dépassement de capacité numérique si *ll* + (*lAlign* -1) déborde.

 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Pullpin. h</dt> </dl>                                                                                                       |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CPullPin, classe**](cpullpin.md)
</dt> </dl>

 

 




