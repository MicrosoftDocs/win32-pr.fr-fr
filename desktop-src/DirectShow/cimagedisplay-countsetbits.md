---
description: La méthode CountSetBits retourne le nombre de bits définis à 1 dans un champ de bits spécifié.
ms.assetid: fc5701b8-88ff-4c23-9d26-854bb65cc55c
title: Méthode CImageDisplay. CountSetBits (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageDisplay.CountSetBits
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d334111c18c2c94c79a8b49ed7c0601efabb2bd13922a68c292970d4d2c379bd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119824069"
---
# <a name="cimagedisplaycountsetbits-method"></a>Méthode CImageDisplay. CountSetBits

La `CountSetBits` méthode retourne le nombre de bits définis à 1 dans un champ de bits spécifié.

## <a name="syntax"></a>Syntaxe


```C++
DWORD CountSetBits(
   const DWORD Field
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Champ* 
</dt> <dd>

Spécifie un champ de bits comme valeur **DWORD** .

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne le nombre de bits définis sur 1.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Winutil. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CImageDisplay, classe**](cimagedisplay.md)
</dt> </dl>

 

 




