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
ms.openlocfilehash: a4f33ae2b7434d90d909315edda4d49e07d8adab
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127007620"
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

## <a name="return-value"></a>Valeur de retour

Retourne le résultat aligné.

## <a name="remarks"></a>Notes

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

 

 




