---
description: La méthode SetSourceRect définit le rectangle vidéo source actuel (virtuel pur). Il s’agit d’une fonction membre interne qui est appelée lorsque le rectangle source est modifié.
ms.assetid: 13bb594b-b154-40a2-ad00-f1e86781074d
title: Méthode CBaseControlVideo. SetSourceRect (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.SetSourceRect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 50643db31fa28f4e1587bc682222b15eb745010b9b0ff6be517fb708d8a7693d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120056759"
---
# <a name="cbasecontrolvideosetsourcerect-method"></a>Méthode CBaseControlVideo. SetSourceRect

La `SetSourceRect` méthode définit le rectangle vidéo source actuel (virtuel pur). Il s’agit d’une fonction membre interne qui est appelée lorsque le rectangle source est modifié.

## <a name="syntax"></a>Syntaxe


```C++
virtual HRESULT SetSourceRect(
   RECT *pSourceRect
) = 0;
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pSourceRect* 
</dt> <dd>

Pointeur vers le rectangle source.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne une valeur **HRESULT** .

## <a name="remarks"></a>Remarques

Les classes dérivées doivent remplacer cette fonction membre pour savoir quand le rectangle source change. Elle est appelée à partir des fonctions membres suivantes.

-   [**CBaseControlVideo::SetSourcePosition**](cbasecontrolvideo-setsourceposition.md)
-   [**CBaseControlVideo ::p ut \_ SourceLeft**](cbasecontrolvideo-put-sourceleft.md)
-   [**CBaseControlVideo ::p ut \_ SourceWidth**](cbasecontrolvideo-put-sourcewidth.md)
-   [**CBaseControlVideo ::p ut \_ sourceTop**](cbasecontrolvideo-put-sourcetop.md)
-   [**CBaseControlVideo ::p ut \_ SourceHeight**](cbasecontrolvideo-put-sourceheight.md)

L’exemple suivant illustre une implémentation de cette fonction dans une classe dérivée.


```C++
HRESULT CVideoText::SetSourceRect(RECT *pSourceRect)
{
    m_pRenderer->m_DrawImage.SetSourceRect(pSourceRect);
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

 

 




