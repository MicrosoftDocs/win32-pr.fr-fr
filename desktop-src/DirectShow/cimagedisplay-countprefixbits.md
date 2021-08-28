---
description: La méthode CountPrefixBits calcule le nombre de bits zéro au début d’un champ de bits spécifié.
ms.assetid: 36fc5c5f-dc64-4588-9130-1b0740d03be1
title: Méthode CImageDisplay. CountPrefixBits (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageDisplay.CountPrefixBits
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 510ac01baab55fbf45e3441296018426335a8f50061f06400872fd7275d3e273
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120108479"
---
# <a name="cimagedisplaycountprefixbits-method"></a>Méthode CImageDisplay. CountPrefixBits

La `CountPrefixBits` méthode calcule le nombre de bits zéro au début d’un champ de bits spécifié.

## <a name="syntax"></a>Syntaxe


```C++
DWORD CountPrefixBits(
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

Retourne le nombre de bits zéro qui se produisent avant le premier bit 1, ou 0x80000000 si tous les bits sont nuls.

## <a name="remarks"></a>Remarques

Cette méthode est utile pour utiliser des masques de couleur dans les structures [**VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Winutil. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CImageDisplay, classe**](cimagedisplay.md)
</dt> </dl>

 

 




