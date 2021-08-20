---
description: La fonction GetTrueColorType récupère le nom explicite d’un sous-type de vidéo.
ms.assetid: 479a020c-b55c-44ec-9096-5528113a4b74
title: GetTrueColorType, fonction (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetTrueColorType
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3fb25d4539d4b929362241ffacbfafd97b08844508ec2c1f38c619fe40901475
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119564709"
---
# <a name="gettruecolortype-function"></a>GetTrueColorType fonction)

La fonction **GetTrueColorType** récupère le nom explicite d’un sous-type de vidéo.

## <a name="syntax"></a>Syntaxe


```C++
const GUID GetTrueColorType(
   const BITMAPINFOHEADER *pHeader
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pHeader* 
</dt> <dd>

Pointeur vers une structure [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) qui définit l’image bitmap.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne MEDIASUBTYPE \_ RGB555 ou MEDIASUBTYPE \_ RGB565.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Wxutil. h (inclure Flux. h)</dt> </dl>                                                                                    |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fonctions vidéo et image](video-and-image-functions.md)
</dt> </dl>

 

 




