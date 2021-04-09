---
description: Cette rubrique présente certaines fonctions d’assistance pour la connexion des filtres DirectShow.
ms.assetid: cfd85944-7ae7-49e6-948f-9e190cdeed12
title: Connecter deux filtres
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a7e70e607c510490e7ed841ea44303153a94e83f
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104109414"
---
# <a name="connect-two-filters"></a><span data-ttu-id="55167-103">Connecter deux filtres</span><span class="sxs-lookup"><span data-stu-id="55167-103">Connect Two Filters</span></span>

<span data-ttu-id="55167-104">Cette rubrique présente certaines fonctions d’assistance pour la connexion des filtres DirectShow.</span><span class="sxs-lookup"><span data-stu-id="55167-104">This topic shows some helper functions for connecting DirectShow filters.</span></span>

<span data-ttu-id="55167-105">Pour connecter deux filtres, vous devez trouver une broche de sortie non connectée sur le filtre en amont et une broche d’entrée non connectée sur le filtre en aval.</span><span class="sxs-lookup"><span data-stu-id="55167-105">To connect two filters, you must find an unconnected output pin on the upstream filter, and an unconnected input pin on the downstream filter.</span></span>

<span data-ttu-id="55167-106">Si vous avez déjà des pointeurs vers les deux codes confidentiels, appelez la méthode [**IGraphBuilder :: Connect**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-connect) pour les connecter.</span><span class="sxs-lookup"><span data-stu-id="55167-106">If you already have pointers to both pins, call the [**IGraphBuilder::Connect**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-connect) method to connect them.</span></span> <span data-ttu-id="55167-107">Si les codes confidentiels ne peuvent pas se connecter directement entre eux, la méthode **IGraphBuilder :: Connect** peut insérer des filtres supplémentaires pour terminer la connexion.</span><span class="sxs-lookup"><span data-stu-id="55167-107">If the pins cannot connect directly to each other, the **IGraphBuilder::Connect** method might insert additional filters, to complete the connection.</span></span> <span data-ttu-id="55167-108">Pour plus d’informations, consultez [connexion intelligente](intelligent-connect.md).</span><span class="sxs-lookup"><span data-stu-id="55167-108">For more information, see [Intelligent Connect](intelligent-connect.md).</span></span>

<span data-ttu-id="55167-109">Si vous avez un pointeur vers les filtres, mais pas les codes confidentiels, vous devez utiliser la méthode [**IBaseFilter :: EnumPins**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-enumpins) pour rechercher les broches.</span><span class="sxs-lookup"><span data-stu-id="55167-109">If you have a pointer to the filters but not the pins, you must use the [**IBaseFilter::EnumPins**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-enumpins) method to find the pins.</span></span> <span data-ttu-id="55167-110">(Consultez [énumération des codes confidentiels](enumerating-pins.md).) Les fonctions d’assistance de cette rubrique illustrent cette technique.</span><span class="sxs-lookup"><span data-stu-id="55167-110">(See [Enumerating Pins](enumerating-pins.md).) The helper functions in this topic demonstrate this technique.</span></span>

### <a name="output-pin-to-filter"></a><span data-ttu-id="55167-111">Broche de sortie à filtrer</span><span class="sxs-lookup"><span data-stu-id="55167-111">Output Pin to Filter</span></span>

<span data-ttu-id="55167-112">La fonction suivante accepte deux paramètres : un pointeur vers une broche de sortie et un pointeur vers un filtre.</span><span class="sxs-lookup"><span data-stu-id="55167-112">The following function takes two parameters: A pointer to an output pin, and a pointer to a filter.</span></span> <span data-ttu-id="55167-113">La fonction connecte la broche de sortie à la première broche d’entrée disponible sur le filtre.</span><span class="sxs-lookup"><span data-stu-id="55167-113">The function connects the output pin to the first available input pin on the filter.</span></span>


```C++
// Connect output pin to filter.

HRESULT ConnectFilters(
    IGraphBuilder *pGraph, // Filter Graph Manager.
    IPin *pOut,            // Output pin on the upstream filter.
    IBaseFilter *pDest)    // Downstream filter.
{
    IPin *pIn = NULL;
        
    // Find an input pin on the downstream filter.
    HRESULT hr = FindUnconnectedPin(pDest, PINDIR_INPUT, &pIn);
    if (SUCCEEDED(hr))
    {
        // Try to connect them.
        hr = pGraph->Connect(pOut, pIn);
        pIn->Release();
    }
    return hr;
}
```



<span data-ttu-id="55167-114">Cette fonction effectue les opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="55167-114">This function does the following:</span></span>

1.  <span data-ttu-id="55167-115">Appelle la `FindUnconnectedPin` fonction pour recevoir une broche d’entrée non connectée.</span><span class="sxs-lookup"><span data-stu-id="55167-115">Calls the `FindUnconnectedPin` function to get an unconnected input pin.</span></span> <span data-ttu-id="55167-116">Cette fonction est présentée dans la rubrique [Rechercher un code confidentiel non connecté sur un filtre](find-an-unconnected-pin-on-a-filter.md).</span><span class="sxs-lookup"><span data-stu-id="55167-116">This function is shown in the topic [Find an Unconnected Pin on a Filter](find-an-unconnected-pin-on-a-filter.md).</span></span>
2.  <span data-ttu-id="55167-117">Appelle [**IGraphBuilder :: Connect**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-connect) pour connecter les deux broches.</span><span class="sxs-lookup"><span data-stu-id="55167-117">Calls [**IGraphBuilder::Connect**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-connect) to connect the two pins.</span></span>

### <a name="filter-to-input-pin"></a><span data-ttu-id="55167-118">Filtrer sur la broche d’entrée</span><span class="sxs-lookup"><span data-stu-id="55167-118">Filter to Input Pin</span></span>

<span data-ttu-id="55167-119">La fonction Next prend un pointeur vers un filtre et un pointeur vers une broche d’entrée.</span><span class="sxs-lookup"><span data-stu-id="55167-119">The next function takes a pointer to a filter and a pointer to an input pin.</span></span> <span data-ttu-id="55167-120">Il connecte la broche d’entrée à la première broche de sortie disponible sur le filtre.</span><span class="sxs-lookup"><span data-stu-id="55167-120">It connects the input pin to the first available output pin on the filter.</span></span>


```C++
// Connect filter to input pin.

HRESULT ConnectFilters(IGraphBuilder *pGraph, IBaseFilter *pSrc, IPin *pIn)
{
    IPin *pOut = NULL;
        
    // Find an output pin on the upstream filter.
    HRESULT hr = FindUnconnectedPin(pSrc, PINDIR_OUTPUT, &pOut);
    if (SUCCEEDED(hr))
    {
        // Try to connect them.
        hr = pGraph->Connect(pOut, pIn);
        pOut->Release();
    }
    return hr;
}
```



### <a name="filter-to-filter"></a><span data-ttu-id="55167-121">Filtrer pour filtrer</span><span class="sxs-lookup"><span data-stu-id="55167-121">Filter to Filter</span></span>

<span data-ttu-id="55167-122">La troisième fonction accepte un pointeur vers un filtre amont et un pointeur vers un filtre en aval, et tente de connecter les deux filtres.</span><span class="sxs-lookup"><span data-stu-id="55167-122">The third function takes a pointer to an upstream filter and a pointer to a downstream filter, and tries to connect both filters.</span></span>


```C++
// Connect filter to filter

HRESULT ConnectFilters(IGraphBuilder *pGraph, IBaseFilter *pSrc, IBaseFilter *pDest)
{
    IPin *pOut = NULL;

    // Find an output pin on the first filter.
    HRESULT hr = FindUnconnectedPin(pSrc, PINDIR_OUTPUT, &pOut);
    if (SUCCEEDED(hr))
    {
        hr = ConnectFilters(pGraph, pOut, pDest);
        pOut->Release();
    }
    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="55167-123">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="55167-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="55167-124">Techniques d' Graph-Building générales</span><span class="sxs-lookup"><span data-stu-id="55167-124">General Graph-Building Techniques</span></span>](general-graph-building-techniques.md)
</dt> <dt>

[<span data-ttu-id="55167-125">**ICaptureGraphBuilder2 :: RenderStream**</span><span class="sxs-lookup"><span data-stu-id="55167-125">**ICaptureGraphBuilder2::RenderStream**</span></span>](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream)
</dt> </dl>

 

 



