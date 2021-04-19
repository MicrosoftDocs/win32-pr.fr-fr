---
description: Étape 3A.
ms.assetid: 774fcb12-8928-4667-8ef6-dce86717cc29
title: Étape 3A. Implémenter la méthode CheckInputType
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5eb6ff440838d7a4b65b586e5dba963ff254eef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106529199"
---
# <a name="step-3a-implement-the-checkinputtype-method"></a>Étape 3A. Implémenter la méthode CheckInputType

Il s’agit de l’étape 3A du didacticiel [écriture de filtres de transformation](writing-transform-filters.md).

La méthode [**CTransformFilter :: CheckInputType**](ctransformfilter-checkinputtype.md) est appelée quand le filtre amont suggère un type de média au filtre de transformation. Cette méthode prend un pointeur vers un objet [**CMediaType**](cmediatype.md) , qui est un wrapper léger pour la structure du [**\_ \_ type de média am**](/windows/win32/api/strmif/ns-strmif-am_media_type) . Dans cette méthode, vous devez examiner chaque champ pertinent de la structure du **\_ \_ type de média am** , y compris les champs du bloc de format. Vous pouvez utiliser les méthodes d’accesseur définies dans **CMediaType** ou référencer directement les membres de la structure. Si un champ n’est pas valide, retourne un type de VFW \_ E \_ \_ non \_ accepté. Si le type de média entier est valide, return S \_ OK.

Par exemple, dans le filtre d’encodeur RLE, le type d’entrée doit être une vidéo RVB non compressée de 8 ou 4 bits. Il n’y a aucune raison de prendre en charge d’autres formats d’entrée, tels que RVB 16 ou 24 bits, car le filtre doit les convertir en une profondeur de bit inférieure, et DirectShow fournit déjà un filtre de [convertisseur d’espace de couleurs](color-space-converter-filter.md) à cet effet. L’exemple suivant suppose que l’encodeur prend en charge une vidéo 8 bits, mais pas une vidéo de 4 bits :


```C++
HRESULT CRleFilter::CheckInputType(const CMediaType *mtIn)
{
    if ((mtIn->majortype != MEDIATYPE_Video) ||
        (mtIn->subtype != MEDIASUBTYPE_RGB8) ||
        (mtIn->formattype != FORMAT_VideoInfo) || 
        (mtIn->cbFormat < sizeof(VIDEOINFOHEADER)))
    {
        return VFW_E_TYPE_NOT_ACCEPTED;
    }

    VIDEOINFOHEADER *pVih = 
        reinterpret_cast<VIDEOINFOHEADER*>(mtIn->pbFormat);
    if ((pVih->bmiHeader.biBitCount != 8) ||
        (pVih->bmiHeader.biCompression != BI_RGB))
    {
        return VFW_E_TYPE_NOT_ACCEPTED;
    }

    // Check the palette table.
    if (pVih->bmiHeader.biClrUsed > PALETTE_ENTRIES(pVih))
    {
        return VFW_E_TYPE_NOT_ACCEPTED;
    }
    DWORD cbPalette = pVih->bmiHeader.biClrUsed * sizeof(RGBQUAD);
    if (mtIn->cbFormat < sizeof(VIDEOINFOHEADER) + cbPalette)
    {
        return VFW_E_TYPE_NOT_ACCEPTED;
    }

    // Everything is good.
    return S_OK;
}
```



Dans cet exemple, la méthode vérifie d’abord le type et le sous-type principaux. Il vérifie ensuite le type de format pour s’assurer que le bloc de format est une structure [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) . Le filtre peut également prendre en charge [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2), mais dans ce cas, il n’y a pas d’avantage réel. La structure **VIDEOINFOHEADER2** ajoute la prise en charge des pixels non carrés et de l’entrelacement qui ne sont pas susceptibles d’être utiles dans une vidéo 8 bits.

Si le type de format est correct, l’exemple vérifie les membres **biBitCount** et **bicompression** de la structure **VIDEOINFOHEADER** pour vérifier que le format est un RGB non compressé 8 bits. Comme le montre cet exemple, vous devez forcer la


```C++
pbFormat
```



pointeur vers la structure correcte, selon le type de format. Vérifiez toujours le type de format GUID (**formatType**) et la taille du bloc de format (**cbFormat**) avant de procéder au cast du pointeur.

L’exemple vérifie également que le nombre d’entrées de palette est compatible avec la profondeur de bits et que le bloc de format est suffisamment grand pour contenir les entrées de palette. Si toutes ces informations sont correctes, la méthode retourne S \_ OK.

Suivant : [étape 3b. implémentez la méthode GetMediaType](step-3b--implement-the-getmediatype-method.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Écriture de filtres DirectShow](writing-directshow-filters.md)
</dt> </dl>

 

 



