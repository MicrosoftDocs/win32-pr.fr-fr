---
description: La fonction GetBitmapSubtype retourne le GUID du sous-type de média pour la bitmap spécifiée.
ms.assetid: 0af8a64b-8d3c-4308-9fd6-174864a1ca26
title: GetBitmapSubtype, fonction (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetBitmapSubtype
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7ba12ffcd1b50b920f28e1969444a2d31a9d073d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540475"
---
# <a name="getbitmapsubtype-function"></a>GetBitmapSubtype fonction)

La `GetBitmapSubtype` fonction retourne le **GUID** du sous-type de média pour la bitmap spécifiée.

## <a name="syntax"></a>Syntaxe


```C++
const GUID GetBitmapSubtype(
   const BITMAPINFOHEADER *pHeader
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pHeader* 
</dt> <dd>

Pointeur vers une structure [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) .

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne le **GUID** du sous-type de média.

## <a name="remarks"></a>Notes

Pour les types RVB non compressés, cette fonction mappe le champ **biBitCount** au sous-type. Pour les types de vidéo compressés, cette fonction utilise la classe [**FOURCCMap**](fourccmap.md) pour mapper le champ de **bicompression** au sous-type.

Si la fonction ne peut pas correspondre au format d’un sous-type, la valeur de retour est le GUID \_ null.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Wxutil. h (include streams. h)</dt> </dl>                                                                                    |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fonctions vidéo et image](video-and-image-functions.md)
</dt> </dl>

 

 




