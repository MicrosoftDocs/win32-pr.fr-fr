---
description: Étape 3C.
ms.assetid: e780df46-bf47-4334-b788-05ad8179f051
title: Étape 3C. Implémenter la méthode CheckTransform
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 430ad933acfa7fc41a8b075183080e0b710a5d4780b55fa89cd4bf80984c1edc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120075589"
---
# <a name="step-3c-implement-the-checktransform-method"></a>Étape 3C. Implémenter la méthode CheckTransform

Il s’agit de l’étape 3C du didacticiel sur l' [écriture de filtres de transformation](writing-transform-filters.md).

> [!Note]  
> Cette étape n’est pas requise pour les filtres qui dérivent de **CTransInPlaceFilter**.

 

La méthode [**CTransformFilter :: CheckTransform**](ctransformfilter-checktransform.md) vérifie si un type de sortie proposé est compatible avec le type d’entrée actuel. La méthode est également appelée si la broche d’entrée se reconnecte après la connexion de la broche de sortie.

L’exemple suivant vérifie si le format est RLE8 Video. les dimensions de l’image correspondent au format d’entrée ; les entrées de palette sont les mêmes. Elle rejette également les rectangles source et cible qui ne correspondent pas à la taille de l’image.


```C++
HRESULT CRleFilter::CheckTransform(
    const CMediaType *mtIn, const CMediaType *mtOut)
{
    // Check the major type.
    if (mtOut->majortype != MEDIATYPE_Video)
    {
        return VFW_E_TYPE_NOT_ACCEPTED;
    }

    // Check the subtype and format type.
    FOURCCMap fccMap = FCC('MRLE'); 
    if (mtOut->subtype != static_cast<GUID>(fccMap))
    {
        return VFW_E_TYPE_NOT_ACCEPTED;
    }
    if ((mtOut->formattype != FORMAT_VideoInfo) || 
        (mtOut->cbFormat < sizeof(VIDEOINFOHEADER)))
    {
        return VFW_E_TYPE_NOT_ACCEPTED;
    }

    // Compare the bitmap information against the input type.
    ASSERT(mtIn->formattype == FORMAT_VideoInfo);
    BITMAPINFOHEADER *pBmiOut = HEADER(mtOut->pbFormat);
    BITMAPINFOHEADER *pBmiIn = HEADER(mtIn->pbFormat);
    if ((pBmiOut->biPlanes != 1) ||
        (pBmiOut->biBitCount != 8) ||
        (pBmiOut->biCompression != BI_RLE8) ||
        (pBmiOut->biWidth != pBmiIn->biWidth) ||
        (pBmiOut->biHeight != pBmiIn->biHeight))
    {
        return VFW_E_TYPE_NOT_ACCEPTED;
    }

    // Compare source and target rectangles.
    RECT rcImg;
    SetRect(&rcImg, 0, 0, pBmiIn->biWidth, pBmiIn->biHeight);
    RECT *prcSrc = &((VIDEOINFOHEADER*)(mtIn->pbFormat))->rcSource;
    RECT *prcTarget = &((VIDEOINFOHEADER*)(mtOut->pbFormat))->rcTarget;
    if (!IsRectEmpty(prcSrc) && !EqualRect(prcSrc, &rcImg))
    {
        return VFW_E_INVALIDMEDIATYPE;
    }
    if (!IsRectEmpty(prcTarget) && !EqualRect(prcTarget, &rcImg))
    {
        return VFW_E_INVALIDMEDIATYPE;
    }

    // Check the palette table.
    if (pBmiOut->biClrUsed != pBmiIn->biClrUsed)
    {
        return VFW_E_TYPE_NOT_ACCEPTED;
    }
    DWORD cbPalette = pBmiOut->biClrUsed * sizeof(RGBQUAD);
    if (mtOut->cbFormat < sizeof(VIDEOINFOHEADER) + cbPalette)
    {
        return VFW_E_TYPE_NOT_ACCEPTED;
    }
    if (0 != memcmp(pBmiOut + 1, pBmiIn + 1, cbPalette))
    {
        return VFW_E_TYPE_NOT_ACCEPTED;
    }

    // Everything is good.
    return S_OK;
}
```



**Épingler les reconnexions**

Les applications peuvent déconnecter et reconnecter des broches. Supposons qu’une application connecte les deux broches, déconnecte la broche d’entrée, puis reconnecte la broche d’entrée à l’aide d’une nouvelle taille d’image. Dans ce cas, **CheckTransform** échoue parce que les dimensions de l’image ne correspondent plus. Ce comportement est raisonnable, bien que le filtre puisse également tenter de reconnecter la broche de sortie avec un nouveau type de média.

Suivant : [étape 4. Définissez les propriétés de l’allocateur](step-4--set-allocator-properties.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Reconnexion des broches](reconnecting-pins.md)
</dt> <dt>

[Rectangles source et cible dans les convertisseurs vidéo](source-and-target-rectangles-in-video-renderers.md)
</dt> <dt>

[écriture de filtres de DirectShow](writing-directshow-filters.md)
</dt> </dl>

 

 



