---
description: Utilisation du mappeur de filtre
ms.assetid: 3f774350-4508-437f-98d1-cca91220f339
title: Utilisation du mappeur de filtre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c2d7acf85a7b415fc161cd21e17d069b46c3f40
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866453"
---
# <a name="using-the-filter-mapper"></a><span data-ttu-id="5b71c-103">Utilisation du mappeur de filtre</span><span class="sxs-lookup"><span data-stu-id="5b71c-103">Using the Filter Mapper</span></span>

<span data-ttu-id="5b71c-104">Le [Mappeur de filtre](filter-mapper.md) est un objet com qui énumère les filtres DirectShow en fonction de différents critères de recherche.</span><span class="sxs-lookup"><span data-stu-id="5b71c-104">The [Filter Mapper](filter-mapper.md) is a COM object that enumerates DirectShow filters based on various search criteria.</span></span> <span data-ttu-id="5b71c-105">Le mappeur de filtre peut être moins efficace que l’énumérateur de périphérique système. par conséquent, si vous avez besoin de filtres d’une catégorie particulière, vous devez utiliser l’énumérateur de périphérique système.</span><span class="sxs-lookup"><span data-stu-id="5b71c-105">The Filter Mapper can be less efficient than the System Device Enumerator, so if you need filters from a particular category, you should use the System Device Enumerator.</span></span> <span data-ttu-id="5b71c-106">Toutefois, si vous devez localiser un filtre qui prend en charge une certaine combinaison de types de média, mais ne fait pas partie d’une catégorie claire, vous devrez peut-être utiliser le mappeur de filtre.</span><span class="sxs-lookup"><span data-stu-id="5b71c-106">But if you need to locate a filter that supports a certain combination of media types, but does not fall into a clear-cut category, you might need to use the Filter Mapper.</span></span> <span data-ttu-id="5b71c-107">(Par exemple, il peut s’agir d’un filtre de convertisseur ou d’un filtre de décodeur).</span><span class="sxs-lookup"><span data-stu-id="5b71c-107">(An example would be a renderer filter or a decoder filter.)</span></span>

<span data-ttu-id="5b71c-108">Le mappeur de filtre expose l’interface [**IFilterMapper2**](/windows/desktop/api/Strmif/nn-strmif-ifiltermapper2) .</span><span class="sxs-lookup"><span data-stu-id="5b71c-108">The Filter Mapper exposes the [**IFilterMapper2**](/windows/desktop/api/Strmif/nn-strmif-ifiltermapper2) interface.</span></span> <span data-ttu-id="5b71c-109">Pour rechercher un filtre, appelez la méthode [**IFilterMapper2 :: EnumMatchingFilters**](/windows/desktop/api/Strmif/nf-strmif-ifiltermapper2-enummatchingfilters) .</span><span class="sxs-lookup"><span data-stu-id="5b71c-109">To search for a filter, call the [**IFilterMapper2::EnumMatchingFilters**](/windows/desktop/api/Strmif/nf-strmif-ifiltermapper2-enummatchingfilters) method.</span></span> <span data-ttu-id="5b71c-110">Cette méthode prend plusieurs paramètres qui définissent les critères de recherche et retourne un énumérateur pour les filtres correspondants.</span><span class="sxs-lookup"><span data-stu-id="5b71c-110">This method takes several parameters that define the search criteria, and returns an enumerator for the matching filters.</span></span> <span data-ttu-id="5b71c-111">L’énumérateur prend en charge l’interface [**IEnumMoniker**](/windows/win32/api/objidl/nn-objidl-ienummoniker) et fournit un moniker unique pour chaque filtre correspondant.</span><span class="sxs-lookup"><span data-stu-id="5b71c-111">The enumerator supports the [**IEnumMoniker**](/windows/win32/api/objidl/nn-objidl-ienummoniker) interface, and supplies a unique moniker for each matching filter.</span></span>

<span data-ttu-id="5b71c-112">L’exemple suivant énumère les filtres qui acceptent les entrées vidéo numériques (DV) et ont au moins une broche de sortie, de n’importe quel type de média.</span><span class="sxs-lookup"><span data-stu-id="5b71c-112">The following example enumerates filters that accept digital video (DV) input and have at least one output pin, of any media type.</span></span> <span data-ttu-id="5b71c-113">(Le filtre de [décodage vidéo DV](dv-video-decoder-filter.md) correspond à ces critères.)</span><span class="sxs-lookup"><span data-stu-id="5b71c-113">(The [DV Video Decoder](dv-video-decoder-filter.md) filter matches these criteria.)</span></span>


```C++
IFilterMapper2 *pMapper = NULL;
IEnumMoniker *pEnum = NULL;

hr = CoCreateInstance(CLSID_FilterMapper2, 
    NULL, CLSCTX_INPROC, IID_IFilterMapper2, 
    (void **) &pMapper);

if (FAILED(hr))
{
    // Error handling omitted for clarity.
}

GUID arrayInTypes[2];
arrayInTypes[0] = MEDIATYPE_Video;
arrayInTypes[1] = MEDIASUBTYPE_dvsd;

hr = pMapper->EnumMatchingFilters(
        &pEnum,
        0,                  // Reserved.
        TRUE,               // Use exact match?
        MERIT_DO_NOT_USE+1, // Minimum merit.
        TRUE,               // At least one input pin?
        1,                  // Number of major type/subtype pairs for input.
        arrayInTypes,       // Array of major type/subtype pairs for input.
        NULL,               // Input medium.
        NULL,               // Input pin category.
        FALSE,              // Must be a renderer?
        TRUE,               // At least one output pin?
        0,                  // Number of major type/subtype pairs for output.
        NULL,               // Array of major type/subtype pairs for output.
        NULL,               // Output medium.
        NULL);              // Output pin category.

// Enumerate the monikers.
IMoniker *pMoniker;
ULONG cFetched;
while (pEnum->Next(1, &pMoniker, &cFetched) == S_OK)
{
    IPropertyBag *pPropBag = NULL;
    hr = pMoniker->BindToStorage(0, 0, IID_IPropertyBag, 
       (void **)&pPropBag);

    if (SUCCEEDED(hr))
    {
        // To retrieve the friendly name of the filter, do the following:
        VARIANT varName;
        VariantInit(&varName);
        hr = pPropBag->Read(L"FriendlyName", &varName, 0);
        if (SUCCEEDED(hr))
        {
            // Display the name in your UI somehow.
        }
        VariantClear(&varName);

        // To create an instance of the filter, do the following:
        IBaseFilter *pFilter;
        hr = pMoniker->BindToObject(NULL, NULL, IID_IBaseFilter, (void**)&pFilter);
        // Now add the filter to the graph. Remember to release pFilter later.
    
        // Clean up.
        pPropBag->Release();
    }
    pMoniker->Release();
}

// Clean up.
pMapper->Release();
pEnum->Release();
```



<span data-ttu-id="5b71c-114">La méthode [**EnumMatchingFilters**](/windows/desktop/api/Strmif/nf-strmif-ifiltermapper2-enummatchingfilters) a un nombre relativement élevé de paramètres, qui sont commentés dans l’exemple.</span><span class="sxs-lookup"><span data-stu-id="5b71c-114">The [**EnumMatchingFilters**](/windows/desktop/api/Strmif/nf-strmif-ifiltermapper2-enummatchingfilters) method has a fairly large number of parameters, which are commented in the example.</span></span> <span data-ttu-id="5b71c-115">Les plus importants pour cet exemple sont les suivants :</span><span class="sxs-lookup"><span data-stu-id="5b71c-115">The significant ones for this example include:</span></span>

-   <span data-ttu-id="5b71c-116">Valeur de mérite minimale : le filtre doit avoir une valeur mérite au-dessus de mérite \_ ne \_ pas \_ utiliser.</span><span class="sxs-lookup"><span data-stu-id="5b71c-116">Minimum merit value: The filter must have a merit value above MERIT\_DO\_NOT\_USE.</span></span>
-   <span data-ttu-id="5b71c-117">Types d’entrée : l’appelant passe un tableau contenant des paires de types et sous-types principaux.</span><span class="sxs-lookup"><span data-stu-id="5b71c-117">Input types: The caller passes an array containing pairs of major types and subtypes.</span></span> <span data-ttu-id="5b71c-118">Seuls les filtres qui prennent en charge au moins l’une de ces paires correspondent.</span><span class="sxs-lookup"><span data-stu-id="5b71c-118">Only filters that support at least one of these pairs will match.</span></span>
-   <span data-ttu-id="5b71c-119">Correspondance exacte : un filtre peut enregistrer des valeurs **null** pour le type principal, le sous-type, la catégorie de code confidentiel ou le support.</span><span class="sxs-lookup"><span data-stu-id="5b71c-119">Exact match: A filter can register **NULL** values for major type, subtype, pin category, or medium.</span></span> <span data-ttu-id="5b71c-120">À moins que vous ne spécifiiez la correspondance exacte, une valeur **null** agit comme un caractère générique, correspondant à toute valeur que vous spécifiez.</span><span class="sxs-lookup"><span data-stu-id="5b71c-120">Unless you specify exact matching, a **NULL** value acts as a wildcard, matching any value that you specify.</span></span> <span data-ttu-id="5b71c-121">Avec la correspondance exacte, le filtre doit correspondre exactement à vos critères.</span><span class="sxs-lookup"><span data-stu-id="5b71c-121">With exact matching, the filter must exactly match your criteria.</span></span> <span data-ttu-id="5b71c-122">Toutefois, si vous attribuez un paramètre null dans les critères de recherche, il agit toujours comme un caractère générique ou une valeur de **type** « ne pas se préoccuper », correspondant à n’importe quel filtre.</span><span class="sxs-lookup"><span data-stu-id="5b71c-122">However, if you give a **NULL** parameter in the search criteria, it always acts as a wildcard or "don't care" value, matching any filter.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5b71c-123">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="5b71c-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5b71c-124">Énumération des appareils et des filtres</span><span class="sxs-lookup"><span data-stu-id="5b71c-124">Enumerating Devices and Filters</span></span>](enumerating-devices-and-filters.md)
</dt> <dt>

[<span data-ttu-id="5b71c-125">Connexion intelligente</span><span class="sxs-lookup"><span data-stu-id="5b71c-125">Intelligent Connect</span></span>](intelligent-connect.md)
</dt> </dl>

 

 
