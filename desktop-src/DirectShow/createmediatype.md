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
ms.openlocfilehash: 03ea3eaee03ebf98ac22d702bde9a165fda21e51
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127195583"
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

## <a name="return-value"></a>Valeur de retour

Retourne une nouvelle structure de [**\_ \_ type de média am**](/windows/win32/api/strmif/ns-strmif-am_media_type) , ou **null** en cas d’erreur.

## <a name="remarks"></a>Notes

Pour libérer la mémoire allouée par cette fonction, appelez [**DeleteMediaType**](deletemediatype.md).

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Mtype. h (include Flux. h)</dt> </dl>                                                                                     |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Fonctions de type de média**](media-type-functions.md)
</dt> </dl>

 

 




