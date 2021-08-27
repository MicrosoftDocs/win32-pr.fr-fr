---
description: La méthode GetSourceRect récupère le rectangle source. Il s’agit d’une méthode interne.
ms.assetid: 51028b79-6aab-4abc-8ee8-2965bda9d191
title: Méthode CBaseControlVideo. GetSourceRect (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.GetSourceRect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3a637e0f5ab5c97494dc072458a29920110363a3e4f07ba8bb7313947996bdad
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120057049"
---
# <a name="cbasecontrolvideogetsourcerect-method"></a>Méthode CBaseControlVideo. GetSourceRect

La `GetSourceRect` méthode récupère le rectangle source. Il s’agit d’une méthode interne.

## <a name="syntax"></a>Syntaxe


```C++
virtual HRESULT GetSourceRect(
   RECT *pSourceRect
) = 0;
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pSourceRect* 
</dt> <dd>

Pointeur vers le rectangle source récupéré.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne une valeur **HRESULT** .

## <a name="remarks"></a>Remarques

Cette fonction membre doit être substituée dans la classe dérivée pour retourner le rectangle source détenu par le convertisseur vidéo. Elle est appelée à partir des fonctions membres [**CBaseControlVideo**](cbasecontrolvideo.md) suivantes.

-   [**CBaseControlVideo::GetSourcePosition**](cbasecontrolvideo-getsourceposition.md)
-   [**CBaseControlVideo ::p ut \_ SourceLeft**](cbasecontrolvideo-put-sourceleft.md)
-   [**CBaseControlVideo :: obtient \_ SourceLeft**](cbasecontrolvideo-get-sourceleft.md)
-   [**CBaseControlVideo ::p ut \_ SourceWidth**](cbasecontrolvideo-put-sourcewidth.md)
-   [**CBaseControlVideo :: obtient \_ SourceWidth**](cbasecontrolvideo-get-sourcewidth.md)
-   [**CBaseControlVideo ::p ut \_ sourceTop**](cbasecontrolvideo-put-sourcetop.md)
-   [**CBaseControlVideo :: obtient \_ sourceTop**](cbasecontrolvideo-get-sourcetop.md)
-   [**CBaseControlVideo ::p ut \_ SourceHeight**](cbasecontrolvideo-put-sourceheight.md)
-   [**CBaseControlVideo :: obtient \_ SourceHeight**](cbasecontrolvideo-get-sourceheight.md)

L’exemple suivant illustre une implémentation de cette fonction dans une classe dérivée.


```C++
// Return the current source rectangle
HRESULT CVideoText::GetSourceRect(RECT *pSourceRect)
{
    ASSERT(pSourceRect);
    m_pRenderer->m_DrawImage.GetSourceRect(pSourceRect);
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

 

 




