---
description: Méthode virtuelle pure substituée par les classes dérivées.
ms.assetid: 05c73f6b-27f4-4930-b4d5-1688b6bf1791
title: Méthode CBaseControlVideo. GetStaticImage (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.GetStaticImage
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 13b0515e20202373954050b6fa18f10a20a76a6a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106520964"
---
# <a name="cbasecontrolvideogetstaticimage-method"></a>Méthode CBaseControlVideo. GetStaticImage

Méthode virtuelle pure substituée par les classes dérivées.

## <a name="syntax"></a>Syntaxe


```C++
virtual HRESULT GetStaticImage(
   long *pBufferSize,
   long *pDIBImage
) = 0;
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pBufferSize* 
</dt> <dd>

Pointeur vers la taille de la mémoire tampon de sortie.

</dd> <dt>

*pDIBImage* 
</dt> <dd>

Pointeur vers la mémoire tampon de sortie.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne une valeur **HRESULT** .

## <a name="remarks"></a>Notes

Par le biais de l’interface [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) , une application peut demander à recevoir une copie de l’image actuelle dans une mémoire tampon (certains convertisseurs peuvent retourner E \_ NOTIMPL à cet objet s’ils ne le prennent pas en charge). La classe dérivée détermine comment récupérer l’image. Lorsque l’application appelle **CBaseControlVideo :: GetStaticImage**, elle appelle cette méthode virtuelle pure que la classe dérivée doit substituer pour l’implémenter. Cela est également appelé par la fonction membre [**CBaseControlVideo :: GetCurrentImage**](cbasecontrolvideo-getcurrentimage.md) .

La classe fournit une fonction membre d’assistance, [**CBaseControlVideo :: CopyImage**](cbasecontrolvideo-copyimage.md), qui peut recevoir un exemple qui contient une image, et la fonction membre copie la section pertinente de celle-ci (en fonction du rectangle source actuel) dans la mémoire tampon de sortie fournie par l’application.

L’exemple suivant illustre une implémentation de cette fonction membre dans une classe dérivée. Dans cet exemple, m \_ pRenderer contient un objet d’une classe dérivée de [**CBaseVideoRenderer**](cbasevideorenderer.md).


```C++
// Return a copy of the current image in the video renderer
HRESULT CVideoText::GetStaticImage(long *pBufferSize,long *pDIBImage)
{
    // Get any sample the renderer may be holding.

    IMediaSample *pMediaSample = m_pRenderer->GetCurrentSample();
    if (pMediaSample == NULL) {
        return E_UNEXPECTED;
    }

    // Call the base class helper method to do the work.

    HRESULT hr = CopyImage(pMediaSample,       // Buffer containing image
                      &m_pRenderer->m_mtIn,    // Type representing bitmap
                      pBufferSize,             // Size of buffer for DIB
                     (BYTE*) pDIBImage);       // Data buffer for output

    pMediaSample->Release();
    return hr;
}
```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Ctlutil. h (include streams. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseControlVideo, classe**](cbasecontrolvideo.md)
</dt> </dl>

 

 




