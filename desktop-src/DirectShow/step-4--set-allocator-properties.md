---
description: Étape 4.
ms.assetid: c2fd6d8b-b239-45e4-9c02-41edafa58762
title: Étape 4. Définir les propriétés d’allocateur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a32d5e3affba32b96dc93cb97e1886322bc6f2c9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106534044"
---
# <a name="step-4-set-allocator-properties"></a><span data-ttu-id="31349-104">Étape 4.</span><span class="sxs-lookup"><span data-stu-id="31349-104">Step 4.</span></span> <span data-ttu-id="31349-105">Définir les propriétés d’allocateur</span><span class="sxs-lookup"><span data-stu-id="31349-105">Set Allocator Properties</span></span>

<span data-ttu-id="31349-106">Il s’agit de l’étape 4 du didacticiel [écriture de filtres de transformation](writing-transform-filters.md).</span><span class="sxs-lookup"><span data-stu-id="31349-106">This is step 4 of the tutorial [Writing Transform Filters](writing-transform-filters.md).</span></span>

> [!Note]  
> <span data-ttu-id="31349-107">Cette étape n’est pas requise pour les filtres qui dérivent de **CTransInPlaceFilter**.</span><span class="sxs-lookup"><span data-stu-id="31349-107">This step is not required for filters that derive from **CTransInPlaceFilter**.</span></span>

 

<span data-ttu-id="31349-108">Une fois que deux codes PIN sont en accord sur un type de média, ils sélectionnent un allocateur pour la connexion et négocient les propriétés d’allocateur, telles que la taille de la mémoire tampon et le nombre de mémoires tampons.</span><span class="sxs-lookup"><span data-stu-id="31349-108">After two pins agree on a media type, they select an allocator for the connection and negotiate allocator properties, such as the buffer size and the number of buffers.</span></span>

<span data-ttu-id="31349-109">Dans la classe **CTransformFilter** , il existe deux allocations : une pour la connexion de code confidentiel en amont et une pour la connexion de code confidentiel en aval.</span><span class="sxs-lookup"><span data-stu-id="31349-109">In the **CTransformFilter** class, there are two allocators, one for the upstream pin connection and one for the downstream pin connection.</span></span> <span data-ttu-id="31349-110">Le filtre amont sélectionne l’allocateur en amont et choisit également les propriétés Allocator.</span><span class="sxs-lookup"><span data-stu-id="31349-110">The upstream filter selects the upstream allocator and also chooses the allocator properties.</span></span> <span data-ttu-id="31349-111">La broche d’entrée accepte tout ce que le filtre en amont décide.</span><span class="sxs-lookup"><span data-stu-id="31349-111">The input pin accepts whatever the upstream filter decides.</span></span> <span data-ttu-id="31349-112">Si vous avez besoin de modifier ce comportement, remplacez la méthode [**CBaseInputPin :: NotifyAllocator**](cbaseinputpin-notifyallocator.md) .</span><span class="sxs-lookup"><span data-stu-id="31349-112">If you need to modify this behavior, override the [**CBaseInputPin::NotifyAllocator**](cbaseinputpin-notifyallocator.md) method.</span></span>

<span data-ttu-id="31349-113">La broche de sortie du filtre de transformation sélectionne l’allocateur en aval.</span><span class="sxs-lookup"><span data-stu-id="31349-113">The transform filter's output pin selects the downstream allocator.</span></span> <span data-ttu-id="31349-114">Il permet d'effectuer les opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="31349-114">It performs the following steps:</span></span>

1.  <span data-ttu-id="31349-115">Si le filtre en aval peut fournir un allocateur, la broche de sortie utilise celle-ci.</span><span class="sxs-lookup"><span data-stu-id="31349-115">If the downstream filter can provide an allocator, the output pin uses that one.</span></span> <span data-ttu-id="31349-116">Dans le cas contraire, la broche de sortie crée un nouvel allocateur.</span><span class="sxs-lookup"><span data-stu-id="31349-116">Otherwise, the output pin creates a new allocator.</span></span>
2.  <span data-ttu-id="31349-117">La broche de sortie obtient les exigences d’allocateur du filtre en aval (le cas échéant) en appelant [**IMemInputPin :: GetAllocatorRequirements**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-getallocatorrequirements).</span><span class="sxs-lookup"><span data-stu-id="31349-117">The output pin gets the downstream filter's allocator requirements (if any) by calling [**IMemInputPin::GetAllocatorRequirements**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-getallocatorrequirements).</span></span>
3.  <span data-ttu-id="31349-118">La broche de sortie appelle la méthode [**CTransformFilter ::D ecidebuffersize**](ctransformfilter-decidebuffersize.md) du filtre de transformation, qui est virtuelle pure.</span><span class="sxs-lookup"><span data-stu-id="31349-118">The output pin calls the transform filter's [**CTransformFilter::DecideBufferSize**](ctransformfilter-decidebuffersize.md) method, which is pure virtual.</span></span> <span data-ttu-id="31349-119">Les paramètres de cette méthode sont un pointeur vers l’allocateur et une structure de [**\_ propriétés d’allocateur**](/windows/win32/api/strmif/ns-strmif-allocator_properties) avec les exigences du filtre en aval.</span><span class="sxs-lookup"><span data-stu-id="31349-119">The parameters to this method are a pointer to the allocator and an [**ALLOCATOR\_PROPERTIES**](/windows/win32/api/strmif/ns-strmif-allocator_properties) structure with the downstream filter's requirements.</span></span> <span data-ttu-id="31349-120">Si le filtre en aval n’a pas de spécifications d’allocateur, la structure est mise à zéro.</span><span class="sxs-lookup"><span data-stu-id="31349-120">If the downstream filter has no allocator requirements, the structure is zeroed out.</span></span>
4.  <span data-ttu-id="31349-121">Dans la méthode **DecideBufferSize** , la classe dérivée définit les propriétés Allocator en appelant [**IMemAllocator :: SetProperties**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-setproperties).</span><span class="sxs-lookup"><span data-stu-id="31349-121">In the **DecideBufferSize** method, the derived class sets the allocator properties by calling [**IMemAllocator::SetProperties**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-setproperties).</span></span>

<span data-ttu-id="31349-122">En règle générale, la classe dérivée sélectionne des propriétés Allocator en fonction du format de sortie, des exigences du filtre en aval et des exigences propres au filtre.</span><span class="sxs-lookup"><span data-stu-id="31349-122">Generally, the derived class will select allocator properties based on the output format, the downstream filter's requirements, and the filter's own requirements.</span></span> <span data-ttu-id="31349-123">Essayez de sélectionner les propriétés qui sont compatibles avec la requête du filtre en aval.</span><span class="sxs-lookup"><span data-stu-id="31349-123">Try to select properties that are compatible with the downstream filter's request.</span></span> <span data-ttu-id="31349-124">Dans le cas contraire, le filtre en aval risque de rejeter la connexion.</span><span class="sxs-lookup"><span data-stu-id="31349-124">Otherwise, the downstream filter might reject the connection.</span></span>

<span data-ttu-id="31349-125">Dans l’exemple suivant, l’encodeur RLE définit des valeurs minimales pour la taille de la mémoire tampon, l’alignement de la mémoire tampon et le nombre de mémoires tampons.</span><span class="sxs-lookup"><span data-stu-id="31349-125">In the following example, the RLE encoder sets minimum values for the buffer size, buffer alignment, and buffer count.</span></span> <span data-ttu-id="31349-126">Pour le préfixe, elle utilise la valeur que le filtre en aval a demandée.</span><span class="sxs-lookup"><span data-stu-id="31349-126">For the prefix, it uses whatever value the downstream filter requested.</span></span> <span data-ttu-id="31349-127">Le préfixe est généralement de zéro octet, mais certains filtres l’exigent.</span><span class="sxs-lookup"><span data-stu-id="31349-127">The prefix is typically zero bytes, but some filters require it.</span></span> <span data-ttu-id="31349-128">Par exemple, le filtre [MUX AVI](avi-mux-filter.md) utilise le préfixe pour écrire des en-têtes riff.</span><span class="sxs-lookup"><span data-stu-id="31349-128">For example, the [AVI Mux](avi-mux-filter.md) filter uses the prefix to write RIFF headers.</span></span>


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



<span data-ttu-id="31349-129">L’allocateur peut ne pas être en mesure de correspondre exactement à votre demande.</span><span class="sxs-lookup"><span data-stu-id="31349-129">The allocator may not be able to match your request exactly.</span></span> <span data-ttu-id="31349-130">Par conséquent, la méthode **SetProperties** retourne le résultat réel dans une structure de **\_ propriétés d’allocateur** distincte (le paramètre *réel* , dans l’exemple précédent).</span><span class="sxs-lookup"><span data-stu-id="31349-130">Therefore, the **SetProperties** method returns the actual result in a separate **ALLOCATOR\_PROPERTIES** structure (the *Actual* parameter, in the previous example).</span></span> <span data-ttu-id="31349-131">Même lorsque **SetProperties** aboutit, vous devez vérifier le résultat pour vous assurer qu’ils répondent aux exigences minimales de votre filtre.</span><span class="sxs-lookup"><span data-stu-id="31349-131">Even when **SetProperties** succeeds, you should check the result to make sure they meet your filter's minimum requirements.</span></span>

<span data-ttu-id="31349-132">**Allocateurs personnalisés**</span><span class="sxs-lookup"><span data-stu-id="31349-132">**Custom Allocators**</span></span>

<span data-ttu-id="31349-133">Par défaut, toutes les classes de filtre utilisent la classe [**CMemAllocator**](cmemallocator.md) pour leurs allocateurs.</span><span class="sxs-lookup"><span data-stu-id="31349-133">By default, all of the filter classes use the [**CMemAllocator**](cmemallocator.md) class for their allocators.</span></span> <span data-ttu-id="31349-134">Cette classe alloue de la mémoire à partir de l’espace d’adressage virtuel du processus client (à l’aide de **VirtualAlloc**).</span><span class="sxs-lookup"><span data-stu-id="31349-134">This class allocates memory from the virtual address space of the client process (using **VirtualAlloc**).</span></span> <span data-ttu-id="31349-135">Si votre filtre doit utiliser un autre type de mémoire, tel que des surfaces DirectDraw, vous pouvez implémenter un allocateur personnalisé.</span><span class="sxs-lookup"><span data-stu-id="31349-135">If your filter needs to use some other kind of memory, such as DirectDraw surfaces, you can implement a custom allocator.</span></span> <span data-ttu-id="31349-136">Vous pouvez utiliser la classe [**CBaseAllocator**](cbaseallocator.md) ou écrire une classe Allocator entièrement nouvelle.</span><span class="sxs-lookup"><span data-stu-id="31349-136">You can use the [**CBaseAllocator**](cbaseallocator.md) class or write an entirely new allocator class.</span></span> <span data-ttu-id="31349-137">Si votre filtre a un allocateur personnalisé, substituez les méthodes suivantes, en fonction du code PIN utilisé par l’allocateur :</span><span class="sxs-lookup"><span data-stu-id="31349-137">If your filter has a custom allocator, override the following methods, depending on which pin uses the allocator:</span></span>

-   <span data-ttu-id="31349-138">Broche d’entrée : [**CBaseInputPin :: GetAllocator**](cbaseinputpin-getallocator.md) et [**CBaseInputPin :: NotifyAllocator**](cbaseinputpin-notifyallocator.md).</span><span class="sxs-lookup"><span data-stu-id="31349-138">Input pin: [**CBaseInputPin::GetAllocator**](cbaseinputpin-getallocator.md) and [**CBaseInputPin::NotifyAllocator**](cbaseinputpin-notifyallocator.md).</span></span>
-   <span data-ttu-id="31349-139">Broche de sortie : [**CBaseOutputPin ::D ecideallocator**](cbaseoutputpin-decideallocator.md).</span><span class="sxs-lookup"><span data-stu-id="31349-139">Output pin: [**CBaseOutputPin::DecideAllocator**](cbaseoutputpin-decideallocator.md).</span></span>

<span data-ttu-id="31349-140">Si l’autre filtre refuse de se connecter à l’aide de votre allocateur personnalisé, votre filtre peut faire échouer la connexion ou se connecter avec l’allocateur d’un autre filtre.</span><span class="sxs-lookup"><span data-stu-id="31349-140">If the other filter refuses to connect using your custom allocator, your filter can either fail the connection, or else connect with the other filter's allocator.</span></span> <span data-ttu-id="31349-141">Dans ce dernier cas, vous devrez peut-être définir un indicateur interne indiquant le type d’allocateur.</span><span class="sxs-lookup"><span data-stu-id="31349-141">In the latter case, you might need to set an internal flag indicating the type of allocator.</span></span> <span data-ttu-id="31349-142">Pour obtenir un exemple de cette approche, consultez [**CDrawImage, classe**](cdrawimage.md).</span><span class="sxs-lookup"><span data-stu-id="31349-142">For an example of this approach, see [**CDrawImage Class**](cdrawimage.md).</span></span>

<span data-ttu-id="31349-143">Suivant : [étape 5. Transformez l’image](step-5--transform-the-image.md).</span><span class="sxs-lookup"><span data-stu-id="31349-143">Next: [Step 5. Transform the Image](step-5--transform-the-image.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="31349-144">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="31349-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="31349-145">Écriture de filtres DirectShow</span><span class="sxs-lookup"><span data-stu-id="31349-145">Writing DirectShow Filters</span></span>](writing-directshow-filters.md)
</dt> </dl>

 

 



