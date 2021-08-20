---
description: La méthode IsDefaultTargetRect détermine si le convertisseur utilise le rectangle cible par défaut (virtuel pur).
ms.assetid: 60c09515-7a34-421c-b3e8-ce746a935583
title: Méthode CBaseControlVideo. IsDefaultTargetRect (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.IsDefaultTargetRect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c11d5b99610ff88a9e5f4088aa47efdcd8f3d9d676f0b17fad4d8e316324e807
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118955238"
---
# <a name="cbasecontrolvideoisdefaulttargetrect-method"></a>Méthode CBaseControlVideo. IsDefaultTargetRect

La `IsDefaultTargetRect` méthode détermine si le convertisseur utilise le rectangle cible par défaut (virtuel pur).

## <a name="syntax"></a>Syntaxe


```C++
virtual HRESULT IsDefaultTargetRect() = 0;
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Retourne S \_ OK si le convertisseur utilise la cible par défaut ; sinon, retourne s \_ false.

## <a name="remarks"></a>Remarques

Cette fonction membre doit être implémentée dans la classe dérivée. Elle est appelée par la fonction membre [**CBaseControlVideo :: IsUsingDefaultDestination**](cbasecontrolvideo-isusingdefaultdestination.md) .

L’exemple suivant illustre une implémentation de cette fonction dans une classe dérivée.


```C++
// Return S_OK if using the default target; otherwise, S_FALSE.
HRESULT CVideoText::IsDefaultTargetRect()
{
    RECT TargetRect;

    VIDEOINFO *pVideoInfo = (VIDEOINFO *) m_pRenderer->m_mtIn.Format();
    BITMAPINFOHEADER *pHeader = HEADER(pVideoInfo);
    m_pRenderer->m_DrawImage.GetTargetRect(&TargetRect);

    // Check the destination that matches the initial client area.

    if (TargetRect.left != 0 || TargetRect.top != 0 ||
            TargetRect.right != m_Size.cx ||
                TargetRect.bottom != m_Size.cy) {
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

 

 




