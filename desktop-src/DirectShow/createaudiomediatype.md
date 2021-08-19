---
description: La fonction CreateAudioMediaType Initialise un type de média à partir d’une structure WAVEFORMATEX.
ms.assetid: 2571b7b4-86e9-443f-a99d-9ba48f469522
title: Fonction CreateAudioMediaType (mtype. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CreateAudioMediaType
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2eb9dc01a398a498252cca2f1f3af012608f8e0ca80c62800c56e4026c0b0a7d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119908819"
---
# <a name="createaudiomediatype-function"></a>CreateAudioMediaType fonction)

La fonction **CreateAudioMediaType** Initialise un type de média à partir d’une structure [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) .

## <a name="syntax"></a>Syntaxe


```C++
HRESULT STDAPI CreateAudioMediaType(
   const WAVEFORMATEX  *pwfx,
         AM_MEDIA_TYPE *pmt,
         BOOL          bSetFormat
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pwfx* 
</dt> <dd>

Pointeur vers la structure [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) fournie.

</dd> <dt>

*crédit* 
</dt> <dd>

Pointeur vers la structure du [**\_ \_ type de média am**](/windows/win32/api/strmif/ns-strmif-am_media_type) à initialiser.

</dd> <dt>

*bSetFormat* 
</dt> <dd>

Indicateur précisant s’il faut initialiser le bloc de format. Spécifiez **true** pour l’initialiser, ou **false** dans le cas contraire.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne E \_ OUTOFMEMORY si la mémoire n’a pas pu être allouée pour les données de format ; OK dans le \_ cas contraire.

## <a name="remarks"></a>Remarques

Si le paramètre *bSetFormat* a la **valeur true**, la méthode alloue la mémoire pour le bloc de format. Si le paramètre *VPM* contient déjà un bloc de format alloué, une fuite de mémoire se produit. Pour éviter une fuite de mémoire, appelez [**FreeMediaType**](freemediatype.md) avant d’appeler cette fonction. Une fois la méthode retournée, appelez à nouveau **FreeMediaType** pour libérer le bloc de format.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Mtype. h (include Flux. h)</dt> </dl>                                                                                     |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Fonctions de type de média**](media-type-functions.md)
</dt> </dl>

 

