---
description: La fonction Int64x32Div32 implémente la formule ((a \* b) + RND)/c où a est une valeur 64 bits et b, c et RND sont des valeurs 32 bits.
ms.assetid: 566ac194-5b15-43b7-aa7c-0c18c6f69691
title: Int64x32Div32, fonction (Wxutil. h)
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
ms.openlocfilehash: de60ca08b262dbf97aa118bd115bd6dc58576a1d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106535352"
---
# <a name="int64x32div32-function"></a>Int64x32Div32 fonction)

La `Int64x32Div32` fonction implémente la formule `((a*b)+rnd)/c` où *a* est une valeur 64 bits et *b*, *c* et *Rnd* sont des valeurs 32 bits.

## <a name="syntax"></a>Syntaxe


```C++
LONGLONG WINAPI Int64x32Div32(
   LONGLONG a,
   LONG     b,
   LONG     c,
   LONG     rnd
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



 

## <a name="remarks"></a>Notes

L’arrondi sur la Division est vers zéro. La division par zéro est comptée comme une condition de dépassement de capacité.

Les horodatages et les temps de recherche étant des valeurs 64 bits, cette fonction est utile pour effectuer des conversions sur les systèmes 32 bits. Par exemple, dans MPEG-1, la référence de l’horloge système est 90-kHz, ou 90 000 graduations par seconde. La formule à convertir en temps de référence (unités de 100 nanosecondes) est


```C++
(timestamp * 1000) / 9
```



qui peut être calculé comme `Int64x32Div32(timestamp, 1000, 9, 0)` . Utilisez le paramètre *Rnd* comme facteur d’arrondi.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Wxutil. h (include streams. h)</dt> </dl>                                                                                    |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fonctions d’assistance diverses](miscellaneous-helper-functions.md)
</dt> <dt>

[**llMulDiv**](llmuldiv.md)
</dt> </dl>

 

 




