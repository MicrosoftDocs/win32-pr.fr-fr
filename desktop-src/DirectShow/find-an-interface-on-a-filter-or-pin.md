---
description: Rechercher une interface sur un filtre ou un code PIN
ms.assetid: 546f5b7d-3bcd-4e97-a012-daca6ae7bca1
title: Rechercher une interface sur un filtre ou un code PIN
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d264a35e0c33ba53f6a8df7f69113f3358a9737
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104200655"
---
# <a name="find-an-interface-on-a-filter-or-pin"></a><span data-ttu-id="021e3-103">Rechercher une interface sur un filtre ou un code PIN</span><span class="sxs-lookup"><span data-stu-id="021e3-103">Find an Interface on a Filter or Pin</span></span>

<span data-ttu-id="021e3-104">Pour de nombreuses opérations dans DirectShow, l’application appelle des méthodes sur le gestionnaire de graphique de filtre.</span><span class="sxs-lookup"><span data-stu-id="021e3-104">For many operations in DirectShow, the application calls methods on the Filter Graph Manager.</span></span> <span data-ttu-id="021e3-105">Toutefois, dans certains cas, l’application doit appeler une méthode directement sur un filtre ou un code PIN.</span><span class="sxs-lookup"><span data-stu-id="021e3-105">In some situations, however, the application must call a method directly on a filter or pin.</span></span> <span data-ttu-id="021e3-106">Par exemple, de nombreux filtres exposent des interfaces spécialisées utilisées pour configurer le filtre.</span><span class="sxs-lookup"><span data-stu-id="021e3-106">For example, many filters expose specialized interfaces that are used to configure the filter.</span></span>

<span data-ttu-id="021e3-107">Dans le cas d’une interface de filtre, vous disposez peut-être déjà d’un pointeur vers l’interface [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) du filtre.</span><span class="sxs-lookup"><span data-stu-id="021e3-107">In the case of a filter interface, you might already have a pointer to the filter's [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) interface.</span></span> <span data-ttu-id="021e3-108">Dans ce cas, utilisez simplement **QueryInterface** pour accéder à l’autre interface.</span><span class="sxs-lookup"><span data-stu-id="021e3-108">In that case, simply use **QueryInterface** to get the other interface.</span></span> <span data-ttu-id="021e3-109">Toutefois, certains filtres peuvent être ajoutés au graphique par le gestionnaire de graphes de filtre.</span><span class="sxs-lookup"><span data-stu-id="021e3-109">But some filters might be added to the graph by the Filter Graph Manager.</span></span> <span data-ttu-id="021e3-110">(Pour plus d’informations, consultez [connexion intelligente](intelligent-connect.md).) Dans ce cas, utilisez l’interface [**IEnumFilters**](/windows/desktop/api/Strmif/nn-strmif-ienumfilters) pour parcourir tous les filtres du graphique, puis interrogez-les chaque fois.</span><span class="sxs-lookup"><span data-stu-id="021e3-110">(For details, see [Intelligent Connect](intelligent-connect.md).) In that case, use the [**IEnumFilters**](/windows/desktop/api/Strmif/nn-strmif-ienumfilters) interface to loop through all the filters in the graph, and query each one in turn.</span></span> <span data-ttu-id="021e3-111">La fonction suivante illustre ce qui suit :</span><span class="sxs-lookup"><span data-stu-id="021e3-111">The following function demonstrates this:</span></span>


```C++
HRESULT FindFilterInterface(
    IGraphBuilder *pGraph, // Pointer to the Filter Graph Manager.
    REFGUID iid,           // IID of the interface to retrieve.
    void **ppUnk)          // Receives the interface pointer.
{
    if (!pGraph || !ppUnk) return E_POINTER;

    HRESULT hr = E_FAIL;
    IEnumFilters *pEnum = NULL;
    IBaseFilter *pF = NULL;
    if (FAILED(pGraph->EnumFilters(&pEnum)))
    {
        return E_FAIL;
    }
    // Query every filter for the interface.
    while (S_OK == pEnum->Next(1, &pF, 0))
    {
        hr = pF->QueryInterface(iid, ppUnk);
        pF->Release();
        if (SUCCEEDED(hr))
        {
            break;
        }
    }
    pEnum->Release();
    return hr;
}
```



<span data-ttu-id="021e3-112">Pour rechercher une interface sur un code confidentiel, utilisez l’interface [**IEnumPins**](/windows/desktop/api/Strmif/nn-strmif-ienumpins) pour parcourir les broches d’un filtre.</span><span class="sxs-lookup"><span data-stu-id="021e3-112">To find an interface on a pin, use the [**IEnumPins**](/windows/desktop/api/Strmif/nn-strmif-ienumpins) interface to loop through the pins on a filter.</span></span> <span data-ttu-id="021e3-113">La fonction suivante montre comment procéder :</span><span class="sxs-lookup"><span data-stu-id="021e3-113">The following function shows how to do this:</span></span>


```C++
HRESULT FindPinInterface(
    IBaseFilter *pFilter,  // Pointer to the filter to search.
    REFGUID iid,           // IID of the interface.
    void **ppUnk)          // Receives the interface pointer.
{
    if (!pFilter || !ppUnk) return E_POINTER;

    HRESULT hr = E_FAIL;
    IEnumPins *pEnum = 0;
    if (FAILED(pFilter->EnumPins(&pEnum)))
    {
        return E_FAIL;
    }
    // Query every pin for the interface.
    IPin *pPin = 0;
    while (S_OK == pEnum->Next(1, &pPin, 0))
    {
        hr = pPin->QueryInterface(iid, ppUnk);
        pPin->Release();
        if (SUCCEEDED(hr))
        {
            break;
        }
    }
    pEnum->Release();
    return hr;
}
```



<span data-ttu-id="021e3-114">La fonction Next recherche une interface sur un filtre ou un code confidentiel :</span><span class="sxs-lookup"><span data-stu-id="021e3-114">The next function searches for an interface on a filter or a pin:</span></span>


```C++
HRESULT FindInterfaceAnywhere(
    IGraphBuilder *pGraph, 
    REFGUID iid, 
    void **ppUnk)
{
    if (!pGraph || !ppUnk) return E_POINTER;
    HRESULT hr = E_FAIL;
    IEnumFilters *pEnum = 0;
    if (FAILED(pGraph->EnumFilters(&pEnum)))
    {
        return E_FAIL;
    }
    // Loop through every filter in the graph.
    IBaseFilter *pF = 0;
    while (S_OK == pEnum->Next(1, &pF, 0))
    {
        hr = pF->QueryInterface(iid, ppUnk);
        if (FAILED(hr))
        {
            // The filter does not expose the interface, but maybe
            // one of its pins does.
            hr = FindPinInterface(pF, iid, ppUnk);
        }
        pF->Release();
        if (SUCCEEDED(hr))
        {
            break;
        }
    }
    pEnum->Release();
    return hr;
}
```



<span data-ttu-id="021e3-115">Notez que toutes les fonctions indiquées ici s’arrêtent à la première fonction **QueryInterface** réussie.</span><span class="sxs-lookup"><span data-stu-id="021e3-115">Note that all of the functions shown here stop at the first successful **QueryInterface**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="021e3-116">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="021e3-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="021e3-117">Énumération des filtres</span><span class="sxs-lookup"><span data-stu-id="021e3-117">Enumerating Filters</span></span>](enumerating-filters.md)
</dt> <dt>

[<span data-ttu-id="021e3-118">Énumération des codes confidentiels</span><span class="sxs-lookup"><span data-stu-id="021e3-118">Enumerating Pins</span></span>](enumerating-pins.md)
</dt> <dt>

[<span data-ttu-id="021e3-119">**ICaptureGraphBuilder2::FindInterface**</span><span class="sxs-lookup"><span data-stu-id="021e3-119">**ICaptureGraphBuilder2::FindInterface**</span></span>](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findinterface)
</dt> </dl>

 

 



