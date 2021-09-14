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
ms.openlocfilehash: f5cae835a3a7f1b5510d85ecf3f2ae9d15251a45
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126999088"
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

## <a name="return-value"></a>Valeur de retour

Retourne une chaîne contenant le nom.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Wxutil. h (inclure Flux. h)</dt> </dl>                                                                                    |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fonctions vidéo et image](video-and-image-functions.md)
</dt> </dl>

 

 




