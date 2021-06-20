---
description: Définissez les propriétés Allocator dans le cadre de l’écriture d’un filtre de transformation. La broche de sortie du filtre de transformation sélectionne l’allocateur en aval.
ms.assetid: c2fd6d8b-b239-45e4-9c02-41edafa58762
title: Étape 4. Définir les propriétés d’allocateur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9ee7d9ecdc85b63ec6bd774a3a47e0e9399dcf3
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112406822"
---
# <a name="step-4-set-allocator-properties"></a><span data-ttu-id="f7ff8-105">Étape 4.</span><span class="sxs-lookup"><span data-stu-id="f7ff8-105">Step 4.</span></span> <span data-ttu-id="f7ff8-106">Définir les propriétés d’allocateur</span><span class="sxs-lookup"><span data-stu-id="f7ff8-106">Set Allocator Properties</span></span>

<span data-ttu-id="f7ff8-107">Il s’agit de l’étape 4 du didacticiel [écriture de filtres de transformation](writing-transform-filters.md).</span><span class="sxs-lookup"><span data-stu-id="f7ff8-107">This is step 4 of the tutorial [Writing Transform Filters](writing-transform-filters.md).</span></span>

> [!Note]  
> <span data-ttu-id="f7ff8-108">Cette étape n’est pas requise pour les filtres qui dérivent de **CTransInPlaceFilter**.</span><span class="sxs-lookup"><span data-stu-id="f7ff8-108">This step is not required for filters that derive from **CTransInPlaceFilter**.</span></span>

 

<span data-ttu-id="f7ff8-109">Une fois que deux codes PIN sont en accord sur un type de média, ils sélectionnent un allocateur pour la connexion et négocient les propriétés d’allocateur, telles que la taille de la mémoire tampon et le nombre de mémoires tampons.</span><span class="sxs-lookup"><span data-stu-id="f7ff8-109">After two pins agree on a media type, they select an allocator for the connection and negotiate allocator properties, such as the buffer size and the number of buffers.</span></span>

<span data-ttu-id="f7ff8-110">Dans la classe **CTransformFilter** , il existe deux allocations : une pour la connexion de code confidentiel en amont et une pour la connexion de code confidentiel en aval.</span><span class="sxs-lookup"><span data-stu-id="f7ff8-110">In the **CTransformFilter** class, there are two allocators, one for the upstream pin connection and one for the downstream pin connection.</span></span> <span data-ttu-id="f7ff8-111">Le filtre amont sélectionne l’allocateur en amont et choisit également les propriétés Allocator.</span><span class="sxs-lookup"><span data-stu-id="f7ff8-111">The upstream filter selects the upstream allocator and also chooses the allocator properties.</span></span> <span data-ttu-id="f7ff8-112">La broche d’entrée accepte tout ce que le filtre en amont décide.</span><span class="sxs-lookup"><span data-stu-id="f7ff8-112">The input pin accepts whatever the upstream filter decides.</span></span> <span data-ttu-id="f7ff8-113">Si vous avez besoin de modifier ce comportement, remplacez la méthode [**CBaseInputPin :: NotifyAllocator**](cbaseinputpin-notifyallocator.md) .</span><span class="sxs-lookup"><span data-stu-id="f7ff8-113">If you need to modify this behavior, override the [**CBaseInputPin::NotifyAllocator**](cbaseinputpin-notifyallocator.md) method.</span></span>

<span data-ttu-id="f7ff8-114">La broche de sortie du filtre de transformation sélectionne l’allocateur en aval.</span><span class="sxs-lookup"><span data-stu-id="f7ff8-114">The transform filter's output pin selects the downstream allocator.</span></span> <span data-ttu-id="f7ff8-115">Il permet d'effectuer les opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="f7ff8-115">It performs the following steps:</span></span>

1.  <span data-ttu-id="f7ff8-116">Si le filtre en aval peut fournir un allocateur, la broche de sortie utilise celle-ci.</span><span class="sxs-lookup"><span data-stu-id="f7ff8-116">If the downstream filter can provide an allocator, the output pin uses that one.</span></span> <span data-ttu-id="f7ff8-117">Dans le cas contraire, la broche de sortie crée un nouvel allocateur.</span><span class="sxs-lookup"><span data-stu-id="f7ff8-117">Otherwise, the output pin creates a new allocator.</span></span>
2.  <span data-ttu-id="f7ff8-118">La broche de sortie obtient les exigences d’allocateur du filtre en aval (le cas échéant) en appelant [**IMemInputPin :: GetAllocatorRequirements**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-getallocatorrequirements).</span><span class="sxs-lookup"><span data-stu-id="f7ff8-118">The output pin gets the downstream filter's allocator requirements (if any) by calling [**IMemInputPin::GetAllocatorRequirements**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-getallocatorrequirements).</span></span>
3.  <span data-ttu-id="f7ff8-119">La broche de sortie appelle la méthode [**CTransformFilter ::D ecidebuffersize**](ctransformfilter-decidebuffersize.md) du filtre de transformation, qui est virtuelle pure.</span><span class="sxs-lookup"><span data-stu-id="f7ff8-119">The output pin calls the transform filter's [**CTransformFilter::DecideBufferSize**](ctransformfilter-decidebuffersize.md) method, which is pure virtual.</span></span> <span data-ttu-id="f7ff8-120">Les paramètres de cette méthode sont un pointeur vers l’allocateur et une structure de [**\_ propriétés d’allocateur**](/windows/win32/api/strmif/ns-strmif-allocator_properties) avec les exigences du filtre en aval.</span><span class="sxs-lookup"><span data-stu-id="f7ff8-120">The parameters to this method are a pointer to the allocator and an [**ALLOCATOR\_PROPERTIES**](/windows/win32/api/strmif/ns-strmif-allocator_properties) structure with the downstream filter's requirements.</span></span> <span data-ttu-id="f7ff8-121">Si le filtre en aval n’a pas de spécifications d’allocateur, la structure est mise à zéro.</span><span class="sxs-lookup"><span data-stu-id="f7ff8-121">If the downstream filter has no allocator requirements, the structure is zeroed out.</span></span>
4.  <span data-ttu-id="f7ff8-122">Dans la méthode **DecideBufferSize** , la classe dérivée définit les propriétés Allocator en appelant [**IMemAllocator :: SetProperties**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-setproperties).</span><span class="sxs-lookup"><span data-stu-id="f7ff8-122">In the **DecideBufferSize** method, the derived class sets the allocator properties by calling [**IMemAllocator::SetProperties**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-setproperties).</span></span>

<span data-ttu-id="f7ff8-123">En règle générale, la classe dérivée sélectionne des propriétés Allocator en fonction du format de sortie, des exigences du filtre en aval et des exigences propres au filtre.</span><span class="sxs-lookup"><span data-stu-id="f7ff8-123">Generally, the derived class will select allocator properties based on the output format, the downstream filter's requirements, and the filter's own requirements.</span></span> <span data-ttu-id="f7ff8-124">Essayez de sélectionner les propriétés qui sont compatibles avec la requête du filtre en aval.</span><span class="sxs-lookup"><span data-stu-id="f7ff8-124">Try to select properties that are compatible with the downstream filter's request.</span></span> <span data-ttu-id="f7ff8-125">Dans le cas contraire, le filtre en aval risque de rejeter la connexion.</span><span class="sxs-lookup"><span data-stu-id="f7ff8-125">Otherwise, the downstream filter might reject the connection.</span></span>

<span data-ttu-id="f7ff8-126">Dans l’exemple suivant, l’encodeur RLE définit des valeurs minimales pour la taille de la mémoire tampon, l’alignement de la mémoire tampon et le nombre de mémoires tampons.</span><span class="sxs-lookup"><span data-stu-id="f7ff8-126">In the following example, the RLE encoder sets minimum values for the buffer size, buffer alignment, and buffer count.</span></span> <span data-ttu-id="f7ff8-127">Pour le préfixe, elle utilise la valeur que le filtre en aval a demandée.</span><span class="sxs-lookup"><span data-stu-id="f7ff8-127">For the prefix, it uses whatever value the downstream filter requested.</span></span> <span data-ttu-id="f7ff8-128">Le préfixe est généralement de zéro octet, mais certains filtres l’exigent.</span><span class="sxs-lookup"><span data-stu-id="f7ff8-128">The prefix is typically zero bytes, but some filters require it.</span></span> <span data-ttu-id="f7ff8-129">Par exemple, le filtre [MUX AVI](avi-mux-filter.md) utilise le préfixe pour écrire des en-têtes riff.</span><span class="sxs-lookup"><span data-stu-id="f7ff8-129">For example, the [AVI Mux](avi-mux-filter.md) filter uses the prefix to write RIFF headers.</span></span>


```C++
HRESULT CRleFilter::DecideBufferSize(
    IMemAllocator *pAlloc, ALLOCATOR_PROPERTIES *pProp)
{
    AM_MEDIA_TYPE mt;
    HRESULT hr = m_pOutput->ConnectionMediaType(&mt);
    if (FAILED(hr))
    {
        return hr;
    }

    ASSERT(mt.formattype == FORMAT_VideoInfo);
    BITMAPINFOHEADER *pbmi = HEADER(mt.pbFormat);
    pProp->cbBuffer = DIBSIZE(*pbmi) * 2; 
    if (pProp->cbAlign == 0)
    {
        pProp->cbAlign = 1;
    }
    if (pProp->cBuffers == 0)
    {
        pProp->cBuffers = 1;
    }
    // Release the format block.
    FreeMediaType(mt);

    // Set allocator properties.
    ALLOCATOR_PROPERTIES Actual;
    hr = pAlloc->SetProperties(pProp, &Actual);
    if (FAILED(hr)) 
    {
        return hr;
    }
    // Even when it succeeds, check the actual result.
    if (pProp->cbBuffer > Actual.cbBuffer) 
    {
        return E_FAIL;
    }
    return S_OK;
}
```



<span data-ttu-id="f7ff8-130">L’allocateur peut ne pas être en mesure de correspondre exactement à votre demande.</span><span class="sxs-lookup"><span data-stu-id="f7ff8-130">The allocator may not be able to match your request exactly.</span></span> <span data-ttu-id="f7ff8-131">Par conséquent, la méthode **SetProperties** retourne le résultat réel dans une structure de **\_ propriétés d’allocateur** distincte (le paramètre *réel* , dans l’exemple précédent).</span><span class="sxs-lookup"><span data-stu-id="f7ff8-131">Therefore, the **SetProperties** method returns the actual result in a separate **ALLOCATOR\_PROPERTIES** structure (the *Actual* parameter, in the previous example).</span></span> <span data-ttu-id="f7ff8-132">Même lorsque **SetProperties** aboutit, vous devez vérifier le résultat pour vous assurer qu’ils répondent aux exigences minimales de votre filtre.</span><span class="sxs-lookup"><span data-stu-id="f7ff8-132">Even when **SetProperties** succeeds, you should check the result to make sure they meet your filter's minimum requirements.</span></span>

<span data-ttu-id="f7ff8-133">**Allocateurs personnalisés**</span><span class="sxs-lookup"><span data-stu-id="f7ff8-133">**Custom Allocators**</span></span>

<span data-ttu-id="f7ff8-134">Par défaut, toutes les classes de filtre utilisent la classe [**CMemAllocator**](cmemallocator.md) pour leurs allocateurs.</span><span class="sxs-lookup"><span data-stu-id="f7ff8-134">By default, all of the filter classes use the [**CMemAllocator**](cmemallocator.md) class for their allocators.</span></span> <span data-ttu-id="f7ff8-135">Cette classe alloue de la mémoire à partir de l’espace d’adressage virtuel du processus client (à l’aide de **VirtualAlloc**).</span><span class="sxs-lookup"><span data-stu-id="f7ff8-135">This class allocates memory from the virtual address space of the client process (using **VirtualAlloc**).</span></span> <span data-ttu-id="f7ff8-136">Si votre filtre doit utiliser un autre type de mémoire, tel que des surfaces DirectDraw, vous pouvez implémenter un allocateur personnalisé.</span><span class="sxs-lookup"><span data-stu-id="f7ff8-136">If your filter needs to use some other kind of memory, such as DirectDraw surfaces, you can implement a custom allocator.</span></span> <span data-ttu-id="f7ff8-137">Vous pouvez utiliser la classe [**CBaseAllocator**](cbaseallocator.md) ou écrire une classe Allocator entièrement nouvelle.</span><span class="sxs-lookup"><span data-stu-id="f7ff8-137">You can use the [**CBaseAllocator**](cbaseallocator.md) class or write an entirely new allocator class.</span></span> <span data-ttu-id="f7ff8-138">Si votre filtre a un allocateur personnalisé, substituez les méthodes suivantes, en fonction du code PIN utilisé par l’allocateur :</span><span class="sxs-lookup"><span data-stu-id="f7ff8-138">If your filter has a custom allocator, override the following methods, depending on which pin uses the allocator:</span></span>

-   <span data-ttu-id="f7ff8-139">Broche d’entrée : [**CBaseInputPin :: GetAllocator**](cbaseinputpin-getallocator.md) et [**CBaseInputPin :: NotifyAllocator**](cbaseinputpin-notifyallocator.md).</span><span class="sxs-lookup"><span data-stu-id="f7ff8-139">Input pin: [**CBaseInputPin::GetAllocator**](cbaseinputpin-getallocator.md) and [**CBaseInputPin::NotifyAllocator**](cbaseinputpin-notifyallocator.md).</span></span>
-   <span data-ttu-id="f7ff8-140">Broche de sortie : [**CBaseOutputPin ::D ecideallocator**](cbaseoutputpin-decideallocator.md).</span><span class="sxs-lookup"><span data-stu-id="f7ff8-140">Output pin: [**CBaseOutputPin::DecideAllocator**](cbaseoutputpin-decideallocator.md).</span></span>

<span data-ttu-id="f7ff8-141">Si l’autre filtre refuse de se connecter à l’aide de votre allocateur personnalisé, votre filtre peut faire échouer la connexion ou se connecter avec l’allocateur d’un autre filtre.</span><span class="sxs-lookup"><span data-stu-id="f7ff8-141">If the other filter refuses to connect using your custom allocator, your filter can either fail the connection, or else connect with the other filter's allocator.</span></span> <span data-ttu-id="f7ff8-142">Dans ce dernier cas, vous devrez peut-être définir un indicateur interne indiquant le type d’allocateur.</span><span class="sxs-lookup"><span data-stu-id="f7ff8-142">In the latter case, you might need to set an internal flag indicating the type of allocator.</span></span> <span data-ttu-id="f7ff8-143">Pour obtenir un exemple de cette approche, consultez [**CDrawImage, classe**](cdrawimage.md).</span><span class="sxs-lookup"><span data-stu-id="f7ff8-143">For an example of this approach, see [**CDrawImage Class**](cdrawimage.md).</span></span>

<span data-ttu-id="f7ff8-144">Suivant : [étape 5. Transformez l’image](step-5--transform-the-image.md).</span><span class="sxs-lookup"><span data-stu-id="f7ff8-144">Next: [Step 5. Transform the Image](step-5--transform-the-image.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="f7ff8-145">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="f7ff8-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f7ff8-146">Écriture de filtres DirectShow</span><span class="sxs-lookup"><span data-stu-id="f7ff8-146">Writing DirectShow Filters</span></span>](writing-directshow-filters.md)
</dt> </dl>

 

 



