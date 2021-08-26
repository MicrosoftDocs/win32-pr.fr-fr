---
description: La méthode IsDefaultSourceRect détermine si le convertisseur utilise le rectangle source par défaut (virtuel pur).
ms.assetid: 08c7a365-585c-47e6-9c26-6aa1fa3625e7
title: Méthode CBaseControlVideo. IsDefaultSourceRect (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.IsDefaultSourceRect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d8cdce3f01bc3a0ed28ee9ce758ef6cb136676a9bd8b4b314547103045e5b284
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120056869"
---
# <a name="cbasecontrolvideoisdefaultsourcerect-method"></a>Méthode CBaseControlVideo. IsDefaultSourceRect

La `IsDefaultSourceRect` méthode détermine si le convertisseur utilise le rectangle source par défaut (virtuel pur).

## <a name="syntax"></a>Syntaxe


```C++
virtual HRESULT IsDefaultSourceRect() = 0;
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Retourne S \_ OK si le convertisseur utilise la source par défaut ; sinon, retourne s \_ false.

## <a name="remarks"></a>Remarques

Cette fonction membre doit être implémentée dans la classe dérivée. Elle est appelée par la fonction membre [**CBaseControlVideo :: IsUsingDefaultSource**](cbasecontrolvideo-isusingdefaultsource.md) .

L’exemple suivant illustre une implémentation de cette fonction dans une classe dérivée.


```C++
// Return S_OK if using the default source; otherwise, S_FALSE.
HRESULT CVideoText::IsDefaultSourceRect()
{
    RECT SourceRect;

    VIDEOINFO *pVideoInfo = (VIDEOINFO *) m_pRenderer->m_mtIn.Format();
    BITMAPINFOHEADER *pHeader = HEADER(pVideoInfo);
    m_pRenderer->m_DrawImage.GetSourceRect(&SourceRect);

    // Check the coordinates that match the video dimensions.

    if (SourceRect.left != 0 || SourceRect.top != 0 ||
            SourceRect.right != pHeader->biWidth ||
                SourceRect.bottom != pHeader->biHeight) {
                    return S_FALSE;
    }
    return S_OK;
}
```



Dans cet exemple, CVideoText est une classe dérivée de [**CBaseControlVideo**](cbasecontrolvideo.md), m \_ pRenderer contient un objet d’une classe dérivée de [**CBaseVideoRenderer**](cbasevideorenderer.md), et le membre de \_ données m DrawImage, défini dans la classe dérivée, contient un objet [**CDrawImage**](cdrawimage.md) . Le \_ membre de données m mtIn, également défini dans la classe dérivée, contient un objet [**CMediaType**](cmediatype.md) avec le type de média de la broche d’entrée.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Ctlutil. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseControlVideo, classe**](cbasecontrolvideo.md)
</dt> </dl>

 

 




