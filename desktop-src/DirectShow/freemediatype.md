---
description: La fonction FreeMediaType supprime le bloc de format dans une \_ structure de type de média am \_ .
ms.assetid: b7ec335e-518d-4aa6-8cde-8cb92184d0b0
title: Fonction FreeMediaType (mtype. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FreeMediaType
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4806a87674bf83964ad5b285934effd74b789ecebe7f92f642188b156bf1f48c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118000504"
---
# <a name="freemediatype-function"></a>FreeMediaType fonction)

La fonction **FreeMediaType** supprime le bloc de format dans une structure de [**\_ \_ type de média am**](/windows/win32/api/strmif/ns-strmif-am_media_type) .

## <a name="syntax"></a>Syntaxe


```C++
void FreeMediaType(
   AM_MEDIA_TYPE &mt
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*MT* \[ Réf\]
</dt> <dd>

Référence à une structure [**de \_ \_ type de média am**](/windows/win32/api/strmif/ns-strmif-am_media_type) .

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Cette fonction ne retourne pas de valeur.

## <a name="remarks"></a>Remarques

Le bloc de format est alloué sur le tas. Le membre **pbFormat** du [**\_ \_ type de média am**](/windows/win32/api/strmif/ns-strmif-am_media_type) pointe vers le bloc de format. Utilisez cette fonction pour libérer uniquement le bloc de format. Pour supprimer une structure **de \_ \_ type de média am** allouée, appelez [**DeleteMediaType**](deletemediatype.md).

cette fonction est définie dans la bibliothèque de [Classes de Base DirectShow](directshow-base-classes.md) . Si vous préférez ne pas établir de liaison avec la bibliothèque de classes de base, vous pouvez utiliser le code suivant :


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
```



## <a name="requirements"></a>Conditions requises



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Mtype. h (include Flux. h)</dt> </dl>                                                                                     |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**DeleteMediaType**](deletemediatype.md)
</dt> <dt>

[**Fonctions de type de média**](media-type-functions.md)
</dt> </dl>

 

 




