---
description: Étape 3B.
ms.assetid: 0ec57083-b192-404a-938f-bc6bb1cf0ddb
title: Étape 3B. Implémenter la méthode GetMediaType
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f386c16e3166f910e8221d139af519363d1b49279a412603e0cfddfa41773ede
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119583109"
---
# <a name="step-3b-implement-the-getmediatype-method"></a>Étape 3B. Implémenter la méthode GetMediaType

Il s’agit de l’étape 3B du didacticiel [écriture de filtres de transformation](writing-transform-filters.md).

> [!Note]  
> Cette étape n’est pas requise pour les filtres qui dérivent de **CTransInPlaceFilter**.

 

La méthode [**CTransformFilter :: GetMediaType**](ctransformfilter-getmediatype.md) retourne l’un des types de sortie préférés du filtre, référencé par numéro d’index. Cette méthode n’est jamais appelée, sauf si la broche d’entrée du filtre est déjà connectée. Par conséquent, vous pouvez utiliser le type de média à partir de la connexion en amont pour déterminer les types de sortie préférés.

Un encodeur offre généralement un type par défaut unique, représentant le format cible. Les décodeurs prennent généralement en charge une plage de formats de sortie et les proposent dans l’ordre décroissant de la qualité ou de l’efficacité. Par exemple, la liste peut être UYVY, Y211, RGB-24, RGB-565, RGB-555 et RGB-8, dans cet ordre. Les filtres d’effet peuvent nécessiter une correspondance exacte entre le format de sortie et le format d’entrée.

L’exemple suivant retourne un type de sortie unique, construit en modifiant le type d’entrée pour spécifier la compression RLE8 :


```C++
HRESULT CRleFilter::GetMediaType(int iPosition, CMediaType *pMediaType)
{
    ASSERT(m_pInput->IsConnected());
    if (iPosition < 0)
    {
        return E_INVALIDARG;
    }
    if (iPosition == 0)
    {
        HRESULT hr = m_pInput->ConnectionMediaType(pMediaType);
        if (FAILED(hr))
        {
            return hr;
        }
        FOURCCMap fccMap = FCC('MRLE'); 
        pMediaType->subtype = static_cast<GUID>(fccMap);
        pMediaType->SetVariableSize();
        pMediaType->SetTemporalCompression(FALSE);

        ASSERT(pMediaType->formattype == FORMAT_VideoInfo);
        VIDEOINFOHEADER *pVih =
            reinterpret_cast<VIDEOINFOHEADER*>(pMediaType->pbFormat);
        pVih->bmiHeader.biCompression = BI_RLE8;
        pVih->bmiHeader.biSizeImage = DIBSIZE(pVih->bmiHeader); 
        return S_OK;
    }
    // else
    return VFW_S_NO_MORE_ITEMS;
}
```



Dans cet exemple, la méthode appelle [**IPIN :: ConnectionMediaType**](/windows/desktop/api/Strmif/nf-strmif-ipin-connectionmediatype) pour récupérer le type d’entrée à partir de la broche d’entrée. Ensuite, il modifie certains champs pour indiquer le format de compression, comme suit :

-   Il assigne un nouveau GUID de sous-type, construit à partir du code FOURCC « MRLE », à l’aide de la classe [**FOURCCMap**](fourccmap.md) .
-   Elle appelle la méthode [**CMediaType :: SetVariableSize**](cmediatype-setvariablesize.md) , qui définit l’indicateur **bFixedSizeSamples** sur **false** et le membre **lSampleSize** sur zéro, ce qui indique des échantillons de taille variable.
-   Elle appelle la méthode [**CMediaType :: SetTemporalCompression**](cmediatype-settemporalcompression.md) avec la valeur **false**, ce qui indique que chaque frame est une image clé. (Ce champ est à titre d’information uniquement. vous pouvez donc l’ignorer en toute sécurité.)
-   Il définit le champ de **décompression** sur bi \_ RLE8.
-   Elle définit le champ **biSizeImage** sur la taille de l’image.

Suivant : [étape 3c. implémentez la méthode CheckTransform](step-3c--implement-the-checktransform-method.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[écriture de filtres de DirectShow](writing-directshow-filters.md)
</dt> </dl>

 

 



