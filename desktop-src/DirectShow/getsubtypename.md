---
description: La fonction GetSubtypeName récupère le nom explicite d’un sous-type de vidéo.
ms.assetid: 493b434e-2d36-4897-a5b2-7be0eb0a560f
title: GetSubtypeName, fonction (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetSubtypeName
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c676f3e08f55bd010e761853b777e0eb4b28933536ab7af09bd94e457032b583
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119564848"
---
# <a name="getsubtypename-function"></a>GetSubtypeName fonction)

La `GetSubtypeName` fonction récupère le nom explicite d’un sous-type de vidéo.

## <a name="syntax"></a>Syntaxe


```C++
TCHAR* GetSubtypeName(
   const GUID *pSubtype
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pSubtype* 
</dt> <dd>

Pointeur vers un **GUID** de sous-type de vidéo.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne une chaîne contenant le nom.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Wxutil. h (inclure Flux. h)</dt> </dl>                                                                                    |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fonctions vidéo et image](video-and-image-functions.md)
</dt> </dl>

 

 




