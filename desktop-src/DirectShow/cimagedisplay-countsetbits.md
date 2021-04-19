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
ms.openlocfilehash: cb425b08b524b1d36b622bcfffcc9f311dccbbdf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537896"
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
| En-tête<br/>  | <dl> <dt>Winutil. h (include streams. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CImageDisplay, classe**](cimagedisplay.md)
</dt> </dl>

 

 




