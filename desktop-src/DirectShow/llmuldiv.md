---
description: La fonction llMulDiv implémente la formule ((a \* b) + RND)/c où chaque terme est une valeur 64 bits.
ms.assetid: cd5073b9-27c7-42ee-8487-2d4ea29f77d4
title: llMulDiv, fonction (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Int64x32Div32
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: df58175955106906027a6d2d10c465b82ad6313cd493e3ef9ef3ba279cd0115f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118952348"
---
# <a name="llmuldiv-function"></a>llMulDiv fonction)

La `llMulDiv` fonction implémente la formule `((a*b)+rnd)/c` où chaque terme est une valeur 64 bits.

Les horodatages et les temps de recherche étant des valeurs 64 bits, cette fonction est utile pour effectuer des conversions sur les systèmes 32 bits. Par exemple, la formule pour les octets par seconde est


```C++
(Number of Bytes * Reference Time) / 10,000,000
```



qui peut être calculé comme `llMulDiv(nBytes, rtTime, 10000000, 0)` . Utilisez le paramètre *Rnd* comme facteur d’arrondi.

## <a name="syntax"></a>Syntaxe


```C++
LONGLONG WINAPI Int64x32Div32(
   LONGLONG a,
   LONGLONG b,
   LONGLONG c,
   LONGLONG rnd
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*un* 
</dt> <dd>

Multiplicande.

</dd> <dt>

*b* 
</dt> <dd>

Multiplicateur.

</dd> <dt>

*c* 
</dt> <dd>

Division.

</dd> <dt>

*RND* 
</dt> <dd>

Facteur d’arrondi.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne soit le calcul, soit l' `(a * b + rnd)/c` une des valeurs suivantes.



| Code de retour                                                                                       | Description                                                              |
|---------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| <dl> <dt>**0x7FFFFFFFFFFFFFFF**</dt> </dl> | Un dépassement s’est produit, car le résultat est trop grand (positif).<br/> |
| <dl> <dt>**0x8000000000000000**</dt> </dl> | Un dépassement s’est produit, car le résultat est trop grand (négatif).<br/> |



 

## <a name="remarks"></a>Remarques

L’arrondi sur la Division est vers zéro. La division par zéro est comptée comme une condition de dépassement de capacité.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Wxutil. h (inclure Flux. h)</dt> </dl>                                                                                    |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fonctions d’assistance diverses](miscellaneous-helper-functions.md)
</dt> <dt>

[**Int64x32Div32**](int64x32div32.md)
</dt> </dl>

 

 




