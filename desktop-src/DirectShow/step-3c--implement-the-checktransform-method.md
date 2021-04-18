---
description: Étape 3C.
ms.assetid: e780df46-bf47-4334-b788-05ad8179f051
title: Étape 3C. Implémenter la méthode CheckTransform
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78148701fc54e73a6970d45fde95d70f4cf0df3a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104210267"
---
# <a name="step-3c-implement-the-checktransform-method"></a><span data-ttu-id="e8d75-104">Étape 3C.</span><span class="sxs-lookup"><span data-stu-id="e8d75-104">Step 3C.</span></span> <span data-ttu-id="e8d75-105">Implémenter la méthode CheckTransform</span><span class="sxs-lookup"><span data-stu-id="e8d75-105">Implement the CheckTransform Method</span></span>

<span data-ttu-id="e8d75-106">Il s’agit de l’étape 3C du didacticiel sur l' [écriture de filtres de transformation](writing-transform-filters.md).</span><span class="sxs-lookup"><span data-stu-id="e8d75-106">This is step 3C of the tutorial [Writing Transform Filters](writing-transform-filters.md).</span></span>

> [!Note]  
> <span data-ttu-id="e8d75-107">Cette étape n’est pas requise pour les filtres qui dérivent de **CTransInPlaceFilter**.</span><span class="sxs-lookup"><span data-stu-id="e8d75-107">This step is not required for filters that derive from **CTransInPlaceFilter**.</span></span>

 

<span data-ttu-id="e8d75-108">La méthode [**CTransformFilter :: CheckTransform**](ctransformfilter-checktransform.md) vérifie si un type de sortie proposé est compatible avec le type d’entrée actuel.</span><span class="sxs-lookup"><span data-stu-id="e8d75-108">The [**CTransformFilter::CheckTransform**](ctransformfilter-checktransform.md) method checks if a proposed output type is compatible with the current input type.</span></span> <span data-ttu-id="e8d75-109">La méthode est également appelée si la broche d’entrée se reconnecte après la connexion de la broche de sortie.</span><span class="sxs-lookup"><span data-stu-id="e8d75-109">The method is also called if the input pin reconnects after the output pin connects.</span></span>

<span data-ttu-id="e8d75-110">L’exemple suivant vérifie si le format est RLE8 Video. les dimensions de l’image correspondent au format d’entrée ; les entrées de palette sont les mêmes.</span><span class="sxs-lookup"><span data-stu-id="e8d75-110">The following example verifies whether the format is RLE8 video; the image dimensions match the input format; and the palette entries are the same.</span></span> <span data-ttu-id="e8d75-111">Elle rejette également les rectangles source et cible qui ne correspondent pas à la taille de l’image.</span><span class="sxs-lookup"><span data-stu-id="e8d75-111">It also rejects source and target rectangles that do not match the image size.</span></span>


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



<span data-ttu-id="e8d75-112">**Épingler les reconnexions**</span><span class="sxs-lookup"><span data-stu-id="e8d75-112">**Pin Reconnections**</span></span>

<span data-ttu-id="e8d75-113">Les applications peuvent déconnecter et reconnecter des broches.</span><span class="sxs-lookup"><span data-stu-id="e8d75-113">Applications can disconnect and reconnect pins.</span></span> <span data-ttu-id="e8d75-114">Supposons qu’une application connecte les deux broches, déconnecte la broche d’entrée, puis reconnecte la broche d’entrée à l’aide d’une nouvelle taille d’image.</span><span class="sxs-lookup"><span data-stu-id="e8d75-114">Suppose an application connects both pins, disconnects the input pin, and then reconnects the input pin using a new image size.</span></span> <span data-ttu-id="e8d75-115">Dans ce cas, **CheckTransform** échoue parce que les dimensions de l’image ne correspondent plus.</span><span class="sxs-lookup"><span data-stu-id="e8d75-115">In that case, **CheckTransform** fails because the dimensions of the image no longer match.</span></span> <span data-ttu-id="e8d75-116">Ce comportement est raisonnable, bien que le filtre puisse également tenter de reconnecter la broche de sortie avec un nouveau type de média.</span><span class="sxs-lookup"><span data-stu-id="e8d75-116">This behavior is reasonable, although the filter could also try reconnecting the output pin with a new media type.</span></span>

<span data-ttu-id="e8d75-117">Suivant : [étape 4. Définissez les propriétés de l’allocateur](step-4--set-allocator-properties.md).</span><span class="sxs-lookup"><span data-stu-id="e8d75-117">Next: [Step 4. Set Allocator Properties](step-4--set-allocator-properties.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="e8d75-118">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="e8d75-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e8d75-119">Reconnexion des broches</span><span class="sxs-lookup"><span data-stu-id="e8d75-119">Reconnecting Pins</span></span>](reconnecting-pins.md)
</dt> <dt>

[<span data-ttu-id="e8d75-120">Rectangles source et cible dans les convertisseurs vidéo</span><span class="sxs-lookup"><span data-stu-id="e8d75-120">Source and Target Rectangles in Video Renderers</span></span>](source-and-target-rectangles-in-video-renderers.md)
</dt> <dt>

[<span data-ttu-id="e8d75-121">Écriture de filtres DirectShow</span><span class="sxs-lookup"><span data-stu-id="e8d75-121">Writing DirectShow Filters</span></span>](writing-directshow-filters.md)
</dt> </dl>

 

 



