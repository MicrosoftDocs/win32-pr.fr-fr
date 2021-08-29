---
description: La méthode GetTargetRect récupère le rectangle de destination. Il s’agit d’une fonction membre d’assistance interne.
ms.assetid: bf9d95c9-eee8-46b8-bdee-a7d16777ed83
title: Méthode CBaseControlVideo. GetTargetRect (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.GetTargetRect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3309f36ed731ce0221e98a2a9f9b1459b31864a789a52d950951b613c23fdfbd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119928789"
---
# <a name="cbasecontrolvideogettargetrect-method"></a>Méthode CBaseControlVideo. GetTargetRect

La `GetTargetRect` méthode récupère le rectangle de destination. Il s’agit d’une fonction membre d’assistance interne.

## <a name="syntax"></a>Syntaxe


```C++
virtual HRESULT GetTargetRect(
   RECT *pTargetRect
) = 0;
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pTargetRect* 
</dt> <dd>

Pointeur vers le rectangle de destination.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne une valeur **HRESULT** .

## <a name="remarks"></a>Remarques

Cette fonction membre doit être substituée dans la classe dérivée pour retourner le rectangle cible détenu par le convertisseur vidéo. Elle est appelée à partir des fonctions membres [**CBaseControlVideo**](cbasecontrolvideo.md) suivantes.

-   [**CBaseControlVideo::GetDestinationPosition**](cbasecontrolvideo-getdestinationposition.md)
-   [**CBaseControlVideo ::p ut \_ DestinationLeft**](cbasecontrolvideo-put-destinationleft.md)
-   [**CBaseControlVideo :: obtient \_ DestinationLeft**](cbasecontrolvideo-get-destinationleft.md)
-   [**CBaseControlVideo ::p ut \_ DestinationWidth**](cbasecontrolvideo-put-destinationwidth.md)
-   [**CBaseControlVideo :: obtient \_ DestinationWidth**](cbasecontrolvideo-get-destinationwidth.md)
-   [**CBaseControlVideo ::p ut \_ DestinationTop**](cbasecontrolvideo-put-destinationtop.md)
-   [**CBaseControlVideo :: obtient \_ DestinationTop**](cbasecontrolvideo-get-destinationtop.md)
-   [**CBaseControlVideo ::p ut \_ DestinationHeight**](cbasecontrolvideo-put-destinationheight.md)
-   [**CBaseControlVideo :: obtient \_ DestinationHeight**](cbasecontrolvideo-get-destinationheight.md)

L’exemple suivant illustre une implémentation de cette fonction dans une classe dérivée.


```C++
// Return the current destination rectangle.
HRESULT CVideoText::GetTargetRect(RECT *pTargetRect)
{
    ASSERT(pTargetRect);
    m_pRenderer->m_DrawImage.GetTargetRect(pTargetRect);
    return NOERROR;
}
```



Dans cet exemple, CVideoText est une classe dérivée de [**CBaseControlVideo**](cbasecontrolvideo.md), m \_ pRenderer contient un objet d’une classe dérivée de [**CBaseVideoRenderer**](cbasevideorenderer.md), et le membre de \_ données m DrawImage, défini dans la classe dérivée, contient un objet [**CDrawImage**](cdrawimage.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Ctlutil. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseControlVideo, classe**](cbasecontrolvideo.md)
</dt> </dl>

 

 




