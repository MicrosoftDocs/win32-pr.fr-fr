---
description: La fonction GetBitCount retourne le nombre de bits par pixel utilisé par un sous-type de vidéo spécifié. Cette fonction est valide uniquement pour les sous-types RGB non compressés.
ms.assetid: 876b91c8-50ba-4217-b79c-7f7ec1c22b83
title: GetBitCount, fonction (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetBitCount
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6fed9b24ebf2e95b2408de30a407904e6bd3c1c2
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127007544"
---
# <a name="getbitcount-function"></a>GetBitCount fonction)

La `GetBitCount` fonction retourne le nombre de bits par pixel utilisé par un sous-type de vidéo spécifié. Cette fonction est valide uniquement pour les sous-types RGB non compressés.

## <a name="syntax"></a>Syntaxe


```C++
WORD GetBitCount(
   const GUID *pSubtype
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pSubtype* 
</dt> <dd>

Pointeur vers un **GUID** de sous-type de vidéo.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Retourne le nombre de bits par pixel pour ce sous-type, ou la valeur **USHRT \_ Max** si le sous-type n’est pas reconnu.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Wxutil. h (inclure Flux. h)</dt> </dl>                                                                                    |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fonctions vidéo et image](video-and-image-functions.md)
</dt> </dl>

 

 




