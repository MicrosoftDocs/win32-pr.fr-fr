---
description: Étape 3B.
ms.assetid: 0ec57083-b192-404a-938f-bc6bb1cf0ddb
title: Étape 3B. Implémenter la méthode GetMediaType
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bab3ee41c6740fc2914f943784c0d51116f90428
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/03/2021
ms.locfileid: "104530501"
---
# <a name="step-3b-implement-the-getmediatype-method"></a><span data-ttu-id="0a6cd-104">Étape 3B.</span><span class="sxs-lookup"><span data-stu-id="0a6cd-104">Step 3B.</span></span> <span data-ttu-id="0a6cd-105">Implémenter la méthode GetMediaType</span><span class="sxs-lookup"><span data-stu-id="0a6cd-105">Implement the GetMediaType Method</span></span>

<span data-ttu-id="0a6cd-106">Il s’agit de l’étape 3B du didacticiel [écriture de filtres de transformation](writing-transform-filters.md).</span><span class="sxs-lookup"><span data-stu-id="0a6cd-106">This is step 3B of the tutorial [Writing Transform Filters](writing-transform-filters.md).</span></span>

> [!Note]  
> <span data-ttu-id="0a6cd-107">Cette étape n’est pas requise pour les filtres qui dérivent de **CTransInPlaceFilter**.</span><span class="sxs-lookup"><span data-stu-id="0a6cd-107">This step is not required for filters that derive from **CTransInPlaceFilter**.</span></span>

 

<span data-ttu-id="0a6cd-108">La méthode [**CTransformFilter :: GetMediaType**](ctransformfilter-getmediatype.md) retourne l’un des types de sortie préférés du filtre, référencé par numéro d’index.</span><span class="sxs-lookup"><span data-stu-id="0a6cd-108">The [**CTransformFilter::GetMediaType**](ctransformfilter-getmediatype.md) method returns one of the filter's preferred output types, referenced by index number.</span></span> <span data-ttu-id="0a6cd-109">Cette méthode n’est jamais appelée, sauf si la broche d’entrée du filtre est déjà connectée.</span><span class="sxs-lookup"><span data-stu-id="0a6cd-109">This method is never called unless the filter's input pin is already connected.</span></span> <span data-ttu-id="0a6cd-110">Par conséquent, vous pouvez utiliser le type de média à partir de la connexion en amont pour déterminer les types de sortie préférés.</span><span class="sxs-lookup"><span data-stu-id="0a6cd-110">Therefore, you can use the media type from the upstream connection to determine the preferred output types.</span></span>

<span data-ttu-id="0a6cd-111">Un encodeur offre généralement un type par défaut unique, représentant le format cible.</span><span class="sxs-lookup"><span data-stu-id="0a6cd-111">An encoder typically offers a single preferred type, representing the target format.</span></span> <span data-ttu-id="0a6cd-112">Les décodeurs prennent généralement en charge une plage de formats de sortie et les proposent dans l’ordre décroissant de la qualité ou de l’efficacité.</span><span class="sxs-lookup"><span data-stu-id="0a6cd-112">Decoders generally support a range of output formats, and offer them in order of descending quality or efficiency.</span></span> <span data-ttu-id="0a6cd-113">Par exemple, la liste peut être UYVY, Y211, RGB-24, RGB-565, RGB-555 et RGB-8, dans cet ordre.</span><span class="sxs-lookup"><span data-stu-id="0a6cd-113">For example, the list might be UYVY, Y211, RGB-24, RGB-565, RGB-555, and RGB-8, in that order.</span></span> <span data-ttu-id="0a6cd-114">Les filtres d’effet peuvent nécessiter une correspondance exacte entre le format de sortie et le format d’entrée.</span><span class="sxs-lookup"><span data-stu-id="0a6cd-114">Effect filters may require an exact match between the output format and the input format.</span></span>

<span data-ttu-id="0a6cd-115">L’exemple suivant retourne un type de sortie unique, construit en modifiant le type d’entrée pour spécifier la compression RLE8 :</span><span class="sxs-lookup"><span data-stu-id="0a6cd-115">The following example returns a single output type, which is constructed by modifying the input type to specify RLE8 compression:</span></span>


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



<span data-ttu-id="0a6cd-116">Dans cet exemple, la méthode appelle [**IPIN :: ConnectionMediaType**](/windows/desktop/api/Strmif/nf-strmif-ipin-connectionmediatype) pour récupérer le type d’entrée à partir de la broche d’entrée.</span><span class="sxs-lookup"><span data-stu-id="0a6cd-116">In this example, the method calls [**IPin::ConnectionMediaType**](/windows/desktop/api/Strmif/nf-strmif-ipin-connectionmediatype) to get the input type from the input pin.</span></span> <span data-ttu-id="0a6cd-117">Ensuite, il modifie certains champs pour indiquer le format de compression, comme suit :</span><span class="sxs-lookup"><span data-stu-id="0a6cd-117">Then it changes some of the fields to indicate the compression format, as follows:</span></span>

-   <span data-ttu-id="0a6cd-118">Il assigne un nouveau GUID de sous-type, construit à partir du code FOURCC « MRLE », à l’aide de la classe [**FOURCCMap**](fourccmap.md) .</span><span class="sxs-lookup"><span data-stu-id="0a6cd-118">It assigns a new subtype GUID, which is constructed from the FOURCC code 'MRLE', using the [**FOURCCMap**](fourccmap.md) class.</span></span>
-   <span data-ttu-id="0a6cd-119">Elle appelle la méthode [**CMediaType :: SetVariableSize**](cmediatype-setvariablesize.md) , qui définit l’indicateur **bFixedSizeSamples** sur **false** et le membre **lSampleSize** sur zéro, ce qui indique des échantillons de taille variable.</span><span class="sxs-lookup"><span data-stu-id="0a6cd-119">It calls the [**CMediaType::SetVariableSize**](cmediatype-setvariablesize.md) method, which sets the **bFixedSizeSamples** flag to **FALSE** and the **lSampleSize** member to zero, indicating variable-sized samples.</span></span>
-   <span data-ttu-id="0a6cd-120">Elle appelle la méthode [**CMediaType :: SetTemporalCompression**](cmediatype-settemporalcompression.md) avec la valeur **false**, ce qui indique que chaque frame est une image clé.</span><span class="sxs-lookup"><span data-stu-id="0a6cd-120">It calls the [**CMediaType::SetTemporalCompression**](cmediatype-settemporalcompression.md) method with the value **FALSE**, indicating that every frame is a key frame.</span></span> <span data-ttu-id="0a6cd-121">(Ce champ est à titre d’information uniquement. vous pouvez donc l’ignorer en toute sécurité.)</span><span class="sxs-lookup"><span data-stu-id="0a6cd-121">(This field is informational only, so you could safely ignore it.)</span></span>
-   <span data-ttu-id="0a6cd-122">Il définit le champ de **décompression** sur bi \_ RLE8.</span><span class="sxs-lookup"><span data-stu-id="0a6cd-122">It sets the **biCompression** field to BI\_RLE8.</span></span>
-   <span data-ttu-id="0a6cd-123">Elle définit le champ **biSizeImage** sur la taille de l’image.</span><span class="sxs-lookup"><span data-stu-id="0a6cd-123">It sets the **biSizeImage** field to the image size.</span></span>

<span data-ttu-id="0a6cd-124">Suivant : [étape 3c. implémentez la méthode CheckTransform](step-3c--implement-the-checktransform-method.md).</span><span class="sxs-lookup"><span data-stu-id="0a6cd-124">Next: [Step 3C. Implement the CheckTransform Method](step-3c--implement-the-checktransform-method.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="0a6cd-125">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="0a6cd-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0a6cd-126">Écriture de filtres DirectShow</span><span class="sxs-lookup"><span data-stu-id="0a6cd-126">Writing DirectShow Filters</span></span>](writing-directshow-filters.md)
</dt> </dl>

 

 



