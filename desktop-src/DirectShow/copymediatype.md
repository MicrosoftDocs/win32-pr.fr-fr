---
description: La fonction CopyMediaType copie une \_ \_ structure de type de média AM dans une autre structure, y compris le bloc de format
ms.assetid: 5b47e197-abb5-4b2c-ad65-a506c5e239be
title: Fonction CopyMediaType (mtype. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CopyMediaType
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b193f64edb55a342546f26db1975080490f0e69b2caa91695b3bc63240750983
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119634371"
---
# <a name="copymediatype-function"></a>CopyMediaType fonction)

La fonction **CopyMediaType** copie une structure de [**\_ \_ type de média am**](/windows/win32/api/strmif/ns-strmif-am_media_type) dans une autre structure, y compris le bloc de format

## <a name="syntax"></a>Syntaxe


```C++
HRESULT WINAPI CopyMediaType(
         AM_MEDIA_TYPE *pmtTarget,
   const AM_MEDIA_TYPE *pmtSource
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pmtTarget* 
</dt> <dd>

Pointeur vers une structure de [**\_ \_ type de média am**](/windows/win32/api/strmif/ns-strmif-am_media_type) . La méthode copie le type de média dans cette structure.

</dd> <dt>

*pmtSource* 
</dt> <dd>

Pointeur vers une structure [**de \_ \_ type de média am**](/windows/win32/api/strmif/ns-strmif-am_media_type) source à copier.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne S \_ OK ou E \_ OUTOFMEMORY.

## <a name="remarks"></a>Remarques

Cette fonction alloue la mémoire pour le bloc de format. Si le paramètre *pmtTarget* contient déjà un bloc de format alloué, une fuite de mémoire se produit. Pour éviter une fuite de mémoire, appelez [**FreeMediaType**](freemediatype.md) avant d’appeler cette fonction.

Une fois la méthode retournée, appelez [**FreeMediaType**](freemediatype.md) sur *pmtTarget* pour libérer le bloc de format.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Mtype. h (include Flux. h)</dt> </dl>                                                                                     |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Fonctions de type de média**](media-type-functions.md)
</dt> </dl>

 

 




