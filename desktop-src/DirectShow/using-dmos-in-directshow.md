---
description: Utilisation de DMOs dans DirectShow
ms.assetid: 47d75b9c-8b0d-4235-8ac1-02ae1502c0e7
title: Utilisation de DMOs dans DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bdddc643d39798dc09807e9ecfa15c38a6e0c2cf
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/22/2021
ms.locfileid: "107908687"
---
# <a name="using-dmos-in-directshow"></a><span data-ttu-id="e4880-103">Utilisation de DMOs dans DirectShow</span><span class="sxs-lookup"><span data-stu-id="e4880-103">Using DMOs in DirectShow</span></span>

<span data-ttu-id="e4880-104">Les applications basées sur DirectShow peuvent utiliser DMOs dans un graphique de filtre, par le biais du filtre de [wrappers DMO](dmo-wrapper-filter.md) .</span><span class="sxs-lookup"><span data-stu-id="e4880-104">Applications based on DirectShow can use DMOs in a filter graph, through the [DMO Wrapper](dmo-wrapper-filter.md) filter.</span></span> <span data-ttu-id="e4880-105">Ce filtre agrège un DMO et gère tous les détails de l’utilisation d’DMO, tels que le transfert de données vers et à partir d’DMO, l’allocation d’objets [**IMediaBuffer**](/previous-versions/windows/desktop/api/Mediaobj/nn-mediaobj-imediabuffer) , etc.</span><span class="sxs-lookup"><span data-stu-id="e4880-105">This filter aggregates a DMO and handles all the details of using the DMO, such as passing data to and from the DMO, allocating [**IMediaBuffer**](/previous-versions/windows/desktop/api/Mediaobj/nn-mediaobj-imediabuffer) objects, and so forth.</span></span>

<span data-ttu-id="e4880-106">Dans la mesure où DMO est agrégé par le filtre, l’application peut interroger le filtre sur toutes les interfaces COM exposées par DMO.</span><span class="sxs-lookup"><span data-stu-id="e4880-106">Because the DMO is aggregated by the filter, the application can query the filter for any COM interfaces that the DMO exposes.</span></span> <span data-ttu-id="e4880-107">Toutefois, l’application doit laisser le filtre gérer toutes les opérations de diffusion en continu sur DMO.</span><span class="sxs-lookup"><span data-stu-id="e4880-107">However, the application should let the filter handle all streaming operations on the DMO.</span></span> <span data-ttu-id="e4880-108">Par exemple, ne définissez pas les types de média, traitez les mémoires tampons, videz le système DMO, verrouillez DMO, activez ou désactivez le contrôle qualité, ou définissez des optimisations vidéo.</span><span class="sxs-lookup"><span data-stu-id="e4880-108">For example, do not set media types, process any buffers, flush the DMO, lock the DMO, enable or disable quality control, or set video optimizations.</span></span>

<span data-ttu-id="e4880-109">Si vous connaissez l’identificateur de classe (CLSID) d’un DMO spécifique que vous souhaitez utiliser, vous pouvez initialiser le filtre de wrappers DMO avec ce DMO, comme suit :</span><span class="sxs-lookup"><span data-stu-id="e4880-109">If you know the class identifier (CLSID) of a specific DMO that you want to use, you can initialize the DMO Wrapper filter with that DMO, as follows:</span></span>

1.  <span data-ttu-id="e4880-110">Appelez **CoCreateInstance** pour créer le filtre de wrappers DMO.</span><span class="sxs-lookup"><span data-stu-id="e4880-110">Call **CoCreateInstance** to create the DMO Wrapper filter.</span></span>
2.  <span data-ttu-id="e4880-111">Interrogez le filtre de wrappers DMO pour l’interface [**IDMOWrapperFilter**](/previous-versions/windows/desktop/api/Dmodshow/nn-dmodshow-idmowrapperfilter) .</span><span class="sxs-lookup"><span data-stu-id="e4880-111">Query the DMO Wrapper filter for the [**IDMOWrapperFilter**](/previous-versions/windows/desktop/api/Dmodshow/nn-dmodshow-idmowrapperfilter) interface.</span></span>
3.  <span data-ttu-id="e4880-112">Appelez la méthode [**IDMOWrapperFilter :: init**](/previous-versions/windows/desktop/api/Dmodshow/nf-dmodshow-idmowrapperfilter-init) .</span><span class="sxs-lookup"><span data-stu-id="e4880-112">Call the [**IDMOWrapperFilter::Init**](/previous-versions/windows/desktop/api/Dmodshow/nf-dmodshow-idmowrapperfilter-init) method.</span></span> <span data-ttu-id="e4880-113">Spécifiez le CLSID de la classe DMO et le GUID de la catégorie DMO.</span><span class="sxs-lookup"><span data-stu-id="e4880-113">Specify the CLSID of the DMO and the GUID of the DMO's category.</span></span> <span data-ttu-id="e4880-114">Pour obtenir la liste des catégories DMO, consultez [GUID DMO](dmo-guids.md).</span><span class="sxs-lookup"><span data-stu-id="e4880-114">For a list of DMO categories, see [DMO GUIDs](dmo-guids.md).</span></span>

<span data-ttu-id="e4880-115">Le code suivant illustre ces étapes :</span><span class="sxs-lookup"><span data-stu-id="e4880-115">The following code shows these steps:</span></span>


```C++
// Create the DMO Wrapper filter.
IBaseFilter *pFilter;
HRESULT hr = CoCreateInstance(CLSID_DMOWrapperFilter, NULL, 
    CLSCTX_INPROC_SERVER, IID_IBaseFilter, 
    reinterpret_cast<void**>(&pFilter));

if (SUCCEEDED(hr)) 
{
    // Query for IDMOWrapperFilter.
    IDMOWrapperFilter *pDmoWrapper;
    hr = pFilter->QueryInterface(IID_IDMOWrapperFilter, 
        reinterpret_cast<void**>(&pDmoWrapper));

    if (SUCCEEDED(hr)) 
    {     
        // Initialize the filter.
        hr = pDmoWrapper->Init(CLSID_MyDMO, DMOCATEGORY_VIDEO_EFFECT); 
        pDmoWrapper->Release();

        if (SUCCEEDED(hr)) 
        {
            // Add the filter to the graph.
            hr = pGraph->AddFilter(pFilter, L"My DMO");
        }
    }
    pFilter->Release();
}
```



<span data-ttu-id="e4880-116">La fonction [**DMOEnum**](/previous-versions/windows/desktop/api/Dmoreg/nf-dmoreg-dmoenum) énumère DMOs dans le registre.</span><span class="sxs-lookup"><span data-stu-id="e4880-116">The [**DMOEnum**](/previous-versions/windows/desktop/api/Dmoreg/nf-dmoreg-dmoenum) function enumerates DMOs in the registry.</span></span> <span data-ttu-id="e4880-117">Cette fonction utilise un autre jeu de GUID de catégorie que ceux utilisés pour les filtres DirectShow.</span><span class="sxs-lookup"><span data-stu-id="e4880-117">This function uses a different set of category GUIDs from the ones used for DirectShow filters.</span></span>

<span data-ttu-id="e4880-118">**Utilisation de l’énumérateur de périphérique système avec DMOs**</span><span class="sxs-lookup"><span data-stu-id="e4880-118">**Using the System Device Enumerator with DMOs**</span></span>

<span data-ttu-id="e4880-119">Au lieu de créer directement un DMO, vous pouvez utiliser l' [énumérateur de périphérique système](system-device-enumerator.md), qui peut énumérer toute catégorie DMO prise en charge par la méthode **DMOEnum** .</span><span class="sxs-lookup"><span data-stu-id="e4880-119">Instead of creating a DMO directly, you can use the [System Device Enumerator](system-device-enumerator.md), which can enumerate any DMO category that is supported by the **DMOEnum** method.</span></span> <span data-ttu-id="e4880-120">L’énumérateur de périphérique système comprend également DMOs lorsqu’il énumère certaines catégories de filtre DirectShow.</span><span class="sxs-lookup"><span data-stu-id="e4880-120">The System Device Enumerator also includes DMOs when it enumerates certain DirectShow filter categories.</span></span> <span data-ttu-id="e4880-121">Le tableau suivant montre le mappage entre les catégories DMO et les catégories DirectShow.</span><span class="sxs-lookup"><span data-stu-id="e4880-121">The following table shows the mapping between DMO categories and DirectShow categories.</span></span>



| <span data-ttu-id="e4880-122">Étiquette</span><span class="sxs-lookup"><span data-stu-id="e4880-122">Label</span></span> | <span data-ttu-id="e4880-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="e4880-123">Value</span></span> |
|-----------------------------|--------------------------------|
| <span data-ttu-id="e4880-124">Catégorie DMO</span><span class="sxs-lookup"><span data-stu-id="e4880-124">DMO Category</span></span>                | <span data-ttu-id="e4880-125">Équivalent DirectShow</span><span class="sxs-lookup"><span data-stu-id="e4880-125">DirectShow Equivalent</span></span>          |
| <span data-ttu-id="e4880-126">\_encodeur audio DMOCATEGORY \_</span><span class="sxs-lookup"><span data-stu-id="e4880-126">DMOCATEGORY\_AUDIO\_ENCODER</span></span> | <span data-ttu-id="e4880-127">CLSID \_ AudioCompressorCategory</span><span class="sxs-lookup"><span data-stu-id="e4880-127">CLSID\_AudioCompressorCategory</span></span> |
| <span data-ttu-id="e4880-128">\_DÉcodeur audio DMOCATEGORY \_</span><span class="sxs-lookup"><span data-stu-id="e4880-128">DMOCATEGORY\_AUDIO\_DECODER</span></span> | <span data-ttu-id="e4880-129">CLSID \_ LegacyAmFilterCategory</span><span class="sxs-lookup"><span data-stu-id="e4880-129">CLSID\_LegacyAmFilterCategory</span></span>  |
| <span data-ttu-id="e4880-130">\_encodeur vidéo DMOCATEGORY \_</span><span class="sxs-lookup"><span data-stu-id="e4880-130">DMOCATEGORY\_VIDEO\_ENCODER</span></span> | <span data-ttu-id="e4880-131">CLSID \_ VideoCompressorCategory</span><span class="sxs-lookup"><span data-stu-id="e4880-131">CLSID\_VideoCompressorCategory</span></span> |
| <span data-ttu-id="e4880-132">\_DÉcodeur vidéo DMOCATEGORY \_</span><span class="sxs-lookup"><span data-stu-id="e4880-132">DMOCATEGORY\_VIDEO\_DECODER</span></span> | <span data-ttu-id="e4880-133">CLSID \_ LegacyAmFilterCategory</span><span class="sxs-lookup"><span data-stu-id="e4880-133">CLSID\_LegacyAmFilterCategory</span></span>  |



 

<span data-ttu-id="e4880-134">L’énumérateur de périphérique système retourne une liste d’objets moniker.</span><span class="sxs-lookup"><span data-stu-id="e4880-134">The System Device Enumerator returns a list of moniker objects.</span></span> <span data-ttu-id="e4880-135">Si le moniker représente un DMO, la méthode **IMoniker :: BindToObject** crée automatiquement le filtre de wrappers DMO et l’initialise avec ce DMO.</span><span class="sxs-lookup"><span data-stu-id="e4880-135">If the moniker represents a DMO, the **IMoniker::BindToObject** method automatically creates the DMO Wrapper filter and initializes it with that DMO.</span></span> <span data-ttu-id="e4880-136">Ainsi, le fait qu’un DMO soit impliqué est transparent pour l’application.</span><span class="sxs-lookup"><span data-stu-id="e4880-136">Thus, the fact that a DMO is involved is transparent to the application.</span></span> <span data-ttu-id="e4880-137">Pour plus d’informations sur l’utilisation de l’énumérateur de périphérique système, consultez [utilisation de l’énumérateur de périphérique système](using-the-system-device-enumerator.md).</span><span class="sxs-lookup"><span data-stu-id="e4880-137">For more information on using the System Device Enumerator, see [Using the System Device Enumerator](using-the-system-device-enumerator.md).</span></span>

<span data-ttu-id="e4880-138">**Limitations**</span><span class="sxs-lookup"><span data-stu-id="e4880-138">**Limitations**</span></span>

<span data-ttu-id="e4880-139">Il existe certaines limitations lors de l’utilisation de DMOs dans DirectShow :</span><span class="sxs-lookup"><span data-stu-id="e4880-139">There are some limitations when using DMOs in DirectShow:</span></span>

-   <span data-ttu-id="e4880-140">Le filtre de wrapper DMO ne prend pas en charge DMOs avec des entrées égales à zéro, plusieurs entrées ou des sorties nulles.</span><span class="sxs-lookup"><span data-stu-id="e4880-140">The DMO Wrapper filter does not support DMOs with zero inputs, multiple inputs, or zero outputs.</span></span>
-   <span data-ttu-id="e4880-141">Toutes les connexions de code confidentiel sur le filtre de wrapper DMO utilisent l’interface [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) .</span><span class="sxs-lookup"><span data-stu-id="e4880-141">All pin connections on the DMO Wrapper Filter use the [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) interface.</span></span>
-   <span data-ttu-id="e4880-142">Les services d’édition DirectShow ne prennent pas en charge les effets ou transitions basés sur DMO.</span><span class="sxs-lookup"><span data-stu-id="e4880-142">DirectShow Editing Services does not support DMO-based effects or transitions.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e4880-143">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="e4880-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e4880-144">Utilisation de DMOs</span><span class="sxs-lookup"><span data-stu-id="e4880-144">Using DMOs</span></span>](using-dmos.md)
</dt> </dl>

 

 



