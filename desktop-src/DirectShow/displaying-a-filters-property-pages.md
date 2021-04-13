---
description: Affichage des pages de propriétés d’un filtre
ms.assetid: 4a5f6938-7b33-4350-b8fa-cf78c5c44bcd
title: Affichage des pages de propriétés d’un filtre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0845a12b73363dc6ed93654439fd31826bf9cfc
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104385572"
---
# <a name="displaying-a-filters-property-pages"></a><span data-ttu-id="8b309-103">Affichage des pages de propriétés d’un filtre</span><span class="sxs-lookup"><span data-stu-id="8b309-103">Displaying a Filter's Property Pages</span></span>

<span data-ttu-id="8b309-104">Une page de propriétés est un moyen pour un filtre de prendre en charge les propriétés que l’utilisateur peut définir.</span><span class="sxs-lookup"><span data-stu-id="8b309-104">A property page is one way for a filter to support properties that the user can set.</span></span> <span data-ttu-id="8b309-105">Cet article explique comment afficher les pages de propriétés d’un filtre dans une application.</span><span class="sxs-lookup"><span data-stu-id="8b309-105">This article describes how to display a filter's property pages in an application.</span></span> <span data-ttu-id="8b309-106">Pour plus d’informations sur les pages de propriétés, consultez la documentation du kit de développement Platform SDK.</span><span class="sxs-lookup"><span data-stu-id="8b309-106">For more information about property pages, see the Platform SDK documentation.</span></span>

> [!Note]  
> <span data-ttu-id="8b309-107">Bien que la plupart des filtres fournis avec DirectShow prennent en charge les pages de propriétés, ils sont destinés à des fins de débogage et ne sont pas recommandés pour l’utilisation des applications.</span><span class="sxs-lookup"><span data-stu-id="8b309-107">Although many of the filters provided with DirectShow support property pages, they are intended for debugging purposes, and are not recommended for application use.</span></span> <span data-ttu-id="8b309-108">Dans la plupart des cas, les fonctionnalités équivalentes sont fournies par le biais d’une interface personnalisée sur le filtre.</span><span class="sxs-lookup"><span data-stu-id="8b309-108">In most cases the equivalent functionality is provided through a custom interface on the filter.</span></span> <span data-ttu-id="8b309-109">Une application doit contrôler ces filtres par programme, plutôt que d’exposer leurs pages de propriétés aux utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="8b309-109">An application should control these filters programmatically, rather than expose their property pages to users.</span></span>

 

<span data-ttu-id="8b309-110">Les filtres avec les pages de propriétés exposent l’interface **ISpecifyPropertyPages** .</span><span class="sxs-lookup"><span data-stu-id="8b309-110">Filters with property pages expose the **ISpecifyPropertyPages** interface.</span></span> <span data-ttu-id="8b309-111">Pour déterminer si un filtre définit une page de propriétés, interrogez le filtre pour cette interface à l’aide de **QueryInterface**.</span><span class="sxs-lookup"><span data-stu-id="8b309-111">To determine whether a filter defines a property page, query the filter for this interface using **QueryInterface**.</span></span>

<span data-ttu-id="8b309-112">Si vous avez créé directement une instance d’un filtre (en appelant **CoCreateInstance**), vous avez déjà un pointeur vers le filtre.</span><span class="sxs-lookup"><span data-stu-id="8b309-112">If you directly created an instance of a filter (by calling **CoCreateInstance**), you already have a pointer to the filter.</span></span> <span data-ttu-id="8b309-113">Si ce n’est pas le cas, vous pouvez énumérer les filtres dans le graphique à l’aide de la méthode [**IFilterGraph :: EnumFilters**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-enumfilters) .</span><span class="sxs-lookup"><span data-stu-id="8b309-113">If not, you can enumerate the filters in the graph, using the [**IFilterGraph::EnumFilters**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-enumfilters) method.</span></span> <span data-ttu-id="8b309-114">Pour plus d’informations, consultez [énumération d’objets dans un graphique de filtre](enumerating-objects-in-a-filter-graph.md).</span><span class="sxs-lookup"><span data-stu-id="8b309-114">For details, see [Enumerating Objects in a Filter Graph](enumerating-objects-in-a-filter-graph.md).</span></span>

<span data-ttu-id="8b309-115">Une fois que vous avez le pointeur d’interface **ISpecifyPropertyPages** , récupérez les pages de propriétés du filtre en appelant la méthode **ISpecifyPropertyPages :: GetPages** .</span><span class="sxs-lookup"><span data-stu-id="8b309-115">Once you have the **ISpecifyPropertyPages** interface pointer, retrieve the filter's property pages by calling the **ISpecifyPropertyPages::GetPages** method.</span></span> <span data-ttu-id="8b309-116">Cette méthode remplit un tableau compté d’identificateurs globaux uniques (GUID) à l’aide de l’identificateur de classe (CLSID) de chaque page de propriétés.</span><span class="sxs-lookup"><span data-stu-id="8b309-116">This method fills a counted array of globally unique identifiers (GUIDs) with the class identifier (CLSID) of each property page.</span></span> <span data-ttu-id="8b309-117">Un tableau compté est défini par une structure **cauuid** , que vous devez allouer, mais n’avez pas à initialiser.</span><span class="sxs-lookup"><span data-stu-id="8b309-117">A counted array is defined by a **CAUUID** structure, which you must allocate but do not have to initialize.</span></span> <span data-ttu-id="8b309-118">La méthode **GetPages** alloue le tableau, qui est contenu dans le membre **pElems** de la structure **cauuid** .</span><span class="sxs-lookup"><span data-stu-id="8b309-118">The **GetPages** method allocates the array, which is contained in the **pElems** member of the **CAUUID** structure.</span></span> <span data-ttu-id="8b309-119">Lorsque vous avez terminé, libérez le tableau en appelant la fonction **CoTaskMemFree** .</span><span class="sxs-lookup"><span data-stu-id="8b309-119">When you are done, free the array by calling the **CoTaskMemFree** function.</span></span>

<span data-ttu-id="8b309-120">La fonction **OleCreatePropertyFrame** fournit un moyen simple d’afficher les pages de propriétés dans une boîte de dialogue modale.</span><span class="sxs-lookup"><span data-stu-id="8b309-120">The **OleCreatePropertyFrame** function provides a simple way to display the property pages inside a modal dialog box.</span></span>


```C++
IBaseFilter *pFilter;
/* Obtain the filter's IBaseFilter interface. (Not shown) */
ISpecifyPropertyPages *pProp;
HRESULT hr = pFilter->QueryInterface(IID_ISpecifyPropertyPages, (void **)&pProp);
if (SUCCEEDED(hr)) 
{
    // Get the filter's name and IUnknown pointer.
    FILTER_INFO FilterInfo;
    hr = pFilter->QueryFilterInfo(&FilterInfo); 
    IUnknown *pFilterUnk;
    pFilter->QueryInterface(IID_IUnknown, (void **)&pFilterUnk);

    // Show the page. 
    CAUUID caGUID;
    pProp->GetPages(&caGUID);
    pProp->Release();
    OleCreatePropertyFrame(
        hWnd,                   // Parent window
        0, 0,                   // Reserved
        FilterInfo.achName,     // Caption for the dialog box
        1,                      // Number of objects (just the filter)
        &pFilterUnk,            // Array of object pointers. 
        caGUID.cElems,          // Number of property pages
        caGUID.pElems,          // Array of property page CLSIDs
        0,                      // Locale identifier
        0, NULL                 // Reserved
    );

    // Clean up.
    pFilterUnk->Release();
    FilterInfo.pGraph->Release(); 
    CoTaskMemFree(caGUID.pElems);
}
```



## <a name="related-topics"></a><span data-ttu-id="8b309-121">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="8b309-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8b309-122">Tâches de base de DirectShow</span><span class="sxs-lookup"><span data-stu-id="8b309-122">Basic DirectShow Tasks</span></span>](basic-directshow-tasks.md)
</dt> </dl>

 

 



