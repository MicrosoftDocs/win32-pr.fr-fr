---
description: La fonction CreateMediaType alloue une nouvelle structure de \_ type de média am \_ , y compris le bloc de format.
ms.assetid: 841a8c51-6027-49d6-b3d8-b5e21e3d5f13
title: Fonction CreateMediaType (mtype. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CreateMediaType
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f0384b0a72e10b84cd94581816c0441de6a19fa5148a97fa9e55d72bdd63d678
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119871409"
---
# <a name="createmediatype-function"></a>CreateMediaType fonction)

La fonction **CreateMediaType** alloue une nouvelle structure [**de \_ \_ type de média am**](/windows/win32/api/strmif/ns-strmif-am_media_type) , y compris le bloc de format.

## <a name="syntax"></a>Syntaxe


```C++
AM_MEDIA_TYPE* WINAPI CreateMediaType(
   AM_MEDIA_TYPE const *pSrc
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pSrc* 
</dt> <dd>

Pointeur vers une structure de [**\_ \_ type de média am**](/windows/win32/api/strmif/ns-strmif-am_media_type) . La méthode copie cette structure dans la nouvelle structure.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne une nouvelle structure de [**\_ \_ type de média am**](/windows/win32/api/strmif/ns-strmif-am_media_type) , ou **null** en cas d’erreur.

## <a name="remarks"></a>Remarques

Pour libérer la mémoire allouée par cette fonction, appelez [**DeleteMediaType**](deletemediatype.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Mtype. h (include Flux. h)</dt> </dl>                                                                                     |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Fonctions de type de média**](media-type-functions.md)
</dt> </dl>

 

 




