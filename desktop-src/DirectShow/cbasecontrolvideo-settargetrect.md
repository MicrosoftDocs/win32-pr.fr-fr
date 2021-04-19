---
description: La méthode SetTargetRect définit le rectangle cible actuel (virtuel pur). Il s’agit d’une fonction membre interne qui est appelée lorsque le rectangle de destination change.
ms.assetid: 9e48989d-5995-4f9d-82b2-01229473c3e8
title: Méthode CBaseControlVideo. SetTargetRect (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.SetTargetRect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3868e7d8df93940829fb96c7152a55048a5cae82
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106535370"
---
# <a name="cbasecontrolvideosettargetrect-method"></a>Méthode CBaseControlVideo. SetTargetRect

La `SetTargetRect` méthode définit le rectangle cible actuel (virtuel pur). Il s’agit d’une fonction membre interne qui est appelée lorsque le rectangle de destination change.

## <a name="syntax"></a>Syntaxe


```C++
virtual HRESULT SetTargetRect(
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

## <a name="remarks"></a>Notes

Les classes dérivées doivent remplacer cette valeur pour savoir quand le rectangle de destination change. Elle est appelée à partir des fonctions membres suivantes.

-   [**CBaseControlVideo::SetDestinationPosition**](cbasecontrolvideo-setdestinationposition.md)
-   [**CBaseControlVideo ::p ut \_ DestinationLeft**](cbasecontrolvideo-put-destinationleft.md)
-   [**CBaseControlVideo ::p ut \_ DestinationWidth**](cbasecontrolvideo-put-destinationwidth.md)
-   [**CBaseControlVideo ::p ut \_ DestinationTop**](cbasecontrolvideo-put-destinationtop.md)
-   [**CBaseControlVideo ::p ut \_ DestinationHeight**](cbasecontrolvideo-put-destinationheight.md)

L’exemple suivant illustre une implémentation de cette fonction dans une classe dérivée.


```C++
HRESULT CVideoText::SetTargetRect(RECT *pTargetRect)
{
    m_pRenderer->m_DrawImage.SetTargetRect(pTargetRect);
    return NOERROR;
}
```



Dans cet exemple, CVideoText est une classe dérivée de [**CBaseControlVideo**](cbasecontrolvideo.md), m \_ pRenderer contient un objet d’une classe dérivée de [**CBaseVideoRenderer**](cbasevideorenderer.md), et le membre de \_ données m DrawImage, défini dans la classe dérivée, contient un objet [**CDrawImage**](cdrawimage.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Ctlutil. h (include streams. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseControlVideo, classe**](cbasecontrolvideo.md)
</dt> </dl>

 

 




