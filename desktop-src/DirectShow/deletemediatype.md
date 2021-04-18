---
description: La fonction DeleteMediaType supprime une structure de type de média AM allouée \_ \_ , y compris le bloc de format.
ms.assetid: 970f6b2b-2bf5-418d-b4ae-637561cd6765
title: Fonction DeleteMediaType (mtype. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DeleteMediaType
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: db0de399ab1be7808370a6d0da57c4c3ca7b8de1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106532809"
---
# <a name="deletemediatype-function"></a>DeleteMediaType fonction)

La fonction **DeleteMediaType** supprime une structure de [**\_ \_ type de média am**](/windows/win32/api/strmif/ns-strmif-am_media_type) allouée, y compris le bloc de format.

## <a name="syntax"></a>Syntaxe


```C++
void WINAPI DeleteMediaType(
   AM_MEDIA_TYPE *pmt
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*crédit* 
</dt> <dd>

Pointeur vers une structure [**de \_ \_ type de média am**](/windows/win32/api/strmif/ns-strmif-am_media_type) .

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Cette fonction ne retourne pas de valeur.

## <a name="remarks"></a>Notes

Utilisez cette fonction pour libérer toute structure de type de média qui a été allouée à l’aide de [**CoTaskMemAlloc**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc) ou [**CreateMediaType**](createmediatype.md).

Cette fonction est définie dans la bibliothèque de [classes de base DirectShow](directshow-base-classes.md) . Si vous préférez ne pas établir de liaison avec la bibliothèque de classes de base, vous pouvez utiliser le code suivant :


```C++
// Release the format block for a media type.

void _FreeMediaType(AM_MEDIA_TYPE& mt)
{
    if (mt.cbFormat != 0)
    {
        CoTaskMemFree((PVOID)mt.pbFormat);
        mt.cbFormat = 0;
        mt.pbFormat = NULL;
    }
    if (mt.pUnk != NULL)
    {
        // pUnk should not be used.
        mt.pUnk->Release();
        mt.pUnk = NULL;
    }
}


// Delete a media type structure that was allocated on the heap.
void _DeleteMediaType(AM_MEDIA_TYPE *pmt)
{
    if (pmt != NULL)
    {
        _FreeMediaType(*pmt); 
        CoTaskMemFree(pmt);
    }
}
```





## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Mtype. h (include streams. h)</dt> </dl>                                                                                     |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**FreeMediaType**](freemediatype.md)
</dt> <dt>

[**Fonctions de type de média**](media-type-functions.md)
</dt> </dl>

 

