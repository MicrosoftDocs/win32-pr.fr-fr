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
# <a name="step-3a-implement-the-checkinputtype-method"></a><span data-ttu-id="184a5-104">Étape 3A.</span><span class="sxs-lookup"><span data-stu-id="184a5-104">Step 3A.</span></span> <span data-ttu-id="184a5-105">Implémenter la méthode CheckInputType</span><span class="sxs-lookup"><span data-stu-id="184a5-105">Implement the CheckInputType Method</span></span>

<span data-ttu-id="184a5-106">Il s’agit de l’étape 3A du didacticiel [écriture de filtres de transformation](writing-transform-filters.md).</span><span class="sxs-lookup"><span data-stu-id="184a5-106">This is step 3A of the tutorial [Writing Transform Filters](writing-transform-filters.md).</span></span>

<span data-ttu-id="184a5-107">La méthode [**CTransformFilter :: CheckInputType**](ctransformfilter-checkinputtype.md) est appelée quand le filtre amont suggère un type de média au filtre de transformation.</span><span class="sxs-lookup"><span data-stu-id="184a5-107">The [**CTransformFilter::CheckInputType**](ctransformfilter-checkinputtype.md) method is called when the upstream filter proposes a media type to the transform filter.</span></span> <span data-ttu-id="184a5-108">Cette méthode prend un pointeur vers un objet [**CMediaType**](cmediatype.md) , qui est un wrapper léger pour la structure du [**\_ \_ type de média am**](/windows/win32/api/strmif/ns-strmif-am_media_type) .</span><span class="sxs-lookup"><span data-stu-id="184a5-108">This method takes a pointer to a [**CMediaType**](cmediatype.md) object, which is a thin wrapper for the [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure.</span></span> <span data-ttu-id="184a5-109">Dans cette méthode, vous devez examiner chaque champ pertinent de la structure du **\_ \_ type de média am** , y compris les champs du bloc de format.</span><span class="sxs-lookup"><span data-stu-id="184a5-109">In this method, you should examine every relevant field of the **AM\_MEDIA\_TYPE** structure, including the fields in the format block.</span></span> <span data-ttu-id="184a5-110">Vous pouvez utiliser les méthodes d’accesseur définies dans **CMediaType** ou référencer directement les membres de la structure.</span><span class="sxs-lookup"><span data-stu-id="184a5-110">You can use the accessor methods defined in **CMediaType**, or reference the structure members directly.</span></span> <span data-ttu-id="184a5-111">Si un champ n’est pas valide, retourne un type de VFW \_ E \_ \_ non \_ accepté.</span><span class="sxs-lookup"><span data-stu-id="184a5-111">If any field is not valid, return VFW\_E\_TYPE\_NOT\_ACCEPTED.</span></span> <span data-ttu-id="184a5-112">Si le type de média entier est valide, return S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="184a5-112">If the entire media type is valid, return S\_OK.</span></span>

<span data-ttu-id="184a5-113">Par exemple, dans le filtre d’encodeur RLE, le type d’entrée doit être une vidéo RVB non compressée de 8 ou 4 bits.</span><span class="sxs-lookup"><span data-stu-id="184a5-113">For example, in the RLE encoder filter, the input type must be 8-bit or 4-bit uncompressed RGB video.</span></span> <span data-ttu-id="184a5-114">Il n’y a aucune raison de prendre en charge d’autres formats d’entrée, tels que RVB 16 ou 24 bits, car le filtre doit les convertir en une profondeur de bit inférieure, et DirectShow fournit déjà un filtre de [convertisseur d’espace de couleurs](color-space-converter-filter.md) à cet effet.</span><span class="sxs-lookup"><span data-stu-id="184a5-114">There is no reason to support other input formats, such as 16- or 24-bit RGB, because the filter would have to convert them to a lower bit depth, and DirectShow already provides a [Color Space Converter](color-space-converter-filter.md) filter for that purpose.</span></span> <span data-ttu-id="184a5-115">L’exemple suivant suppose que l’encodeur prend en charge une vidéo 8 bits, mais pas une vidéo de 4 bits :</span><span class="sxs-lookup"><span data-stu-id="184a5-115">The following example assumes that the encoder supports 8-bit video but not 4-bit video:</span></span>


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



<span data-ttu-id="184a5-116">Dans cet exemple, la méthode vérifie d’abord le type et le sous-type principaux.</span><span class="sxs-lookup"><span data-stu-id="184a5-116">In this example, the method first checks the major type and subtype.</span></span> <span data-ttu-id="184a5-117">Il vérifie ensuite le type de format pour s’assurer que le bloc de format est une structure [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) .</span><span class="sxs-lookup"><span data-stu-id="184a5-117">Then it checks the format type, to make sure the format block is a [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) structure.</span></span> <span data-ttu-id="184a5-118">Le filtre peut également prendre en charge [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2), mais dans ce cas, il n’y a pas d’avantage réel.</span><span class="sxs-lookup"><span data-stu-id="184a5-118">The filter could also support [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2), but in this case there would be no real benefit.</span></span> <span data-ttu-id="184a5-119">La structure **VIDEOINFOHEADER2** ajoute la prise en charge des pixels non carrés et de l’entrelacement qui ne sont pas susceptibles d’être utiles dans une vidéo 8 bits.</span><span class="sxs-lookup"><span data-stu-id="184a5-119">The **VIDEOINFOHEADER2** structure adds support for interlacing and non-square pixels, which are not likely to be relevant in 8-bit video.</span></span>

<span data-ttu-id="184a5-120">Si le type de format est correct, l’exemple vérifie les membres **biBitCount** et **bicompression** de la structure **VIDEOINFOHEADER** pour vérifier que le format est un RGB non compressé 8 bits.</span><span class="sxs-lookup"><span data-stu-id="184a5-120">If the format type is correct, the example checks the **biBitCount** and **biCompression** members of the **VIDEOINFOHEADER** structure, to verify that the format is 8-bit uncompressed RGB.</span></span> <span data-ttu-id="184a5-121">Comme le montre cet exemple, vous devez forcer la</span><span class="sxs-lookup"><span data-stu-id="184a5-121">As this example shows, you must coerce the</span></span>


```C++
pbFormat
```



<span data-ttu-id="184a5-122">pointeur vers la structure correcte, selon le type de format.</span><span class="sxs-lookup"><span data-stu-id="184a5-122">pointer to the correct structure, based on the format type.</span></span> <span data-ttu-id="184a5-123">Vérifiez toujours le type de format GUID (**formatType**) et la taille du bloc de format (**cbFormat**) avant de procéder au cast du pointeur.</span><span class="sxs-lookup"><span data-stu-id="184a5-123">Always check the format type GUID (**formattype**) and the size of the format block (**cbFormat**) before casting the pointer.</span></span>

<span data-ttu-id="184a5-124">L’exemple vérifie également que le nombre d’entrées de palette est compatible avec la profondeur de bits et que le bloc de format est suffisamment grand pour contenir les entrées de palette.</span><span class="sxs-lookup"><span data-stu-id="184a5-124">The example also verifies that the number of palette entries is compatible with the bit depth and the format block is large enough to hold the palette entries.</span></span> <span data-ttu-id="184a5-125">Si toutes ces informations sont correctes, la méthode retourne S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="184a5-125">If all of this information is correct, the method returns S\_OK.</span></span>

<span data-ttu-id="184a5-126">Suivant : [étape 3b. implémentez la méthode GetMediaType](step-3b--implement-the-getmediatype-method.md).</span><span class="sxs-lookup"><span data-stu-id="184a5-126">Next: [Step 3B. Implement the GetMediaType Method](step-3b--implement-the-getmediatype-method.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="184a5-127">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="184a5-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="184a5-128">Écriture de filtres DirectShow</span><span class="sxs-lookup"><span data-stu-id="184a5-128">Writing DirectShow Filters</span></span>](writing-directshow-filters.md)
</dt> </dl>

 

 



