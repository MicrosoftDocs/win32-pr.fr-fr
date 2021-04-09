---
description: Rechercher un homologue de filtres
ms.assetid: 74d9fe65-f7f4-4971-9550-27884ac4146b
title: Rechercher un homologue de filtres
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1717f6ad61ad7310fdaa11ea5baaab4dcb7f8011
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104033370"
---
# <a name="find-a-filters-peer"></a><span data-ttu-id="e8d25-103">Rechercher un homologue de filtres</span><span class="sxs-lookup"><span data-stu-id="e8d25-103">Find a Filters Peer</span></span>

<span data-ttu-id="e8d25-104">Pour un filtre donné, vous pouvez parcourir le graphique en recherchant les filtres auxquels il est connecté.</span><span class="sxs-lookup"><span data-stu-id="e8d25-104">Given a filter, you can traverse the graph by finding the filters to which it is connected.</span></span> <span data-ttu-id="e8d25-105">Commencez par énumérer les codes confidentiels du filtre.</span><span class="sxs-lookup"><span data-stu-id="e8d25-105">Start by enumerating the filter's pins.</span></span> <span data-ttu-id="e8d25-106">Pour chaque code confidentiel, vérifiez si ce code PIN est connecté à un autre code PIN.</span><span class="sxs-lookup"><span data-stu-id="e8d25-106">For each pin, check whether that pin is connected to another pin.</span></span> <span data-ttu-id="e8d25-107">Si c’est le cas, interrogez l’autre pin pour obtenir le filtre propriétaire.</span><span class="sxs-lookup"><span data-stu-id="e8d25-107">If so, query the other pin for it's owning filter.</span></span> <span data-ttu-id="e8d25-108">Vous pouvez parcourir le graphique dans la direction amont en énumérant les broches d’entrée du filtre ou dans la direction en aval en énumérant les broches de sortie.</span><span class="sxs-lookup"><span data-stu-id="e8d25-108">You can walk the graph in the upstream direction by enumerating the filter's input pins, or in the downstream direction by enumerating the output pins.</span></span>

<span data-ttu-id="e8d25-109">La fonction suivante recherche en amont ou en aval un filtre connecté.</span><span class="sxs-lookup"><span data-stu-id="e8d25-109">The following function searches upstream or downstream for a connected filter.</span></span> <span data-ttu-id="e8d25-110">Elle retourne le premier filtre correspondant qu’elle trouve :</span><span class="sxs-lookup"><span data-stu-id="e8d25-110">It returns the first matching filter that it finds:</span></span>


```C++
// Get the first upstream or downstream filter
HRESULT GetNextFilter(
    IBaseFilter *pFilter, // Pointer to the starting filter
    PIN_DIRECTION Dir,    // Direction to search (upstream or downstream)
    IBaseFilter **ppNext) // Receives a pointer to the next filter.
{
    if (!pFilter || !ppNext) return E_POINTER;

    IEnumPins *pEnum = 0;
    IPin *pPin = 0;
    HRESULT hr = pFilter->EnumPins(&pEnum);
    if (FAILED(hr)) return hr;
    while (S_OK == pEnum->Next(1, &pPin, 0))
    {
        // See if this pin matches the specified direction.
        PIN_DIRECTION ThisPinDir;
        hr = pPin->QueryDirection(&ThisPinDir);
        if (FAILED(hr))
        {
            // Something strange happened.
            hr = E_UNEXPECTED;
            pPin->Release();
            break;
        }
        if (ThisPinDir == Dir)
        {
            // Check if the pin is connected to another pin.
            IPin *pPinNext = 0;
            hr = pPin->ConnectedTo(&pPinNext);
            if (SUCCEEDED(hr))
            {
                // Get the filter that owns that pin.
                PIN_INFO PinInfo;
                hr = pPinNext->QueryPinInfo(&PinInfo);
                pPinNext->Release();
                pPin->Release();
                pEnum->Release();
                if (FAILED(hr) || (PinInfo.pFilter == NULL))
                {
                    // Something strange happened.
                    return E_UNEXPECTED;
                }
                // This is the filter we're looking for.
                *ppNext = PinInfo.pFilter; // Client must release.
                return S_OK;
            }
        }
        pPin->Release();
    }
    pEnum->Release();
    // Did not find a matching filter.
    return E_FAIL;
}
```



<span data-ttu-id="e8d25-111">La fonction appelle [**IBaseFilter :: EnumPins**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-enumpins) pour énumérer les codes confidentiels du premier filtre.</span><span class="sxs-lookup"><span data-stu-id="e8d25-111">The function calls [**IBaseFilter::EnumPins**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-enumpins) to enumerate the first filter's pins.</span></span> <span data-ttu-id="e8d25-112">Pour chaque code confidentiel, il appelle [**IPIN :: QueryDirection**](/windows/desktop/api/Strmif/nf-strmif-ipin-querydirection) pour vérifier si le code PIN correspond à la direction spécifiée (entrée ou sortie).</span><span class="sxs-lookup"><span data-stu-id="e8d25-112">For each pin, it calls [**IPin::QueryDirection**](/windows/desktop/api/Strmif/nf-strmif-ipin-querydirection) to check whether the pin matches the specified direction (input or output).</span></span> <span data-ttu-id="e8d25-113">Si c’est le cas, la fonction détermine si cette broche est connectée à un autre code confidentiel, en appelant la méthode [**IPIN :: ConnectedTo**](/windows/desktop/api/Strmif/nf-strmif-ipin-connectedto) .</span><span class="sxs-lookup"><span data-stu-id="e8d25-113">If so, the function determines whether that pin is connected to another pin, by calling the [**IPin::ConnectedTo**](/windows/desktop/api/Strmif/nf-strmif-ipin-connectedto) method.</span></span> <span data-ttu-id="e8d25-114">Enfin, il appelle [**IPIN :: QueryPinInfo**](/windows/desktop/api/Strmif/nf-strmif-ipin-querypininfo) sur l’épingle connecté.</span><span class="sxs-lookup"><span data-stu-id="e8d25-114">Finally, it calls [**IPin::QueryPinInfo**](/windows/desktop/api/Strmif/nf-strmif-ipin-querypininfo) on the connected pin.</span></span> <span data-ttu-id="e8d25-115">Cette méthode retourne une structure qui contient, entre autres choses, un pointeur vers le filtre propriétaire de ce pin.</span><span class="sxs-lookup"><span data-stu-id="e8d25-115">This method returns a structure that contains, among other things, a pointer to that pin's owning filter.</span></span> <span data-ttu-id="e8d25-116">Ce pointeur est retourné à l’appelant dans le paramètre *ppNext* .</span><span class="sxs-lookup"><span data-stu-id="e8d25-116">This pointer is returned to the caller in the *ppNext* parameter.</span></span> <span data-ttu-id="e8d25-117">L’appelant doit libérer le pointeur.</span><span class="sxs-lookup"><span data-stu-id="e8d25-117">The caller must release the pointer.</span></span>

<span data-ttu-id="e8d25-118">Le code suivant montre comment appeler cette fonction :</span><span class="sxs-lookup"><span data-stu-id="e8d25-118">The following code shows how to call this function:</span></span>


```C++
IBaseFilter *pF; // Pointer to some filter.
IBaseFilter *pUpstream = NULL;
if (SUCCEEDED(GetNextFilter(pF, PINDIR_INPUT, &pUpstream)))
{
    // Use pUpstream ...
    pUpstream->Release();
}
```



<span data-ttu-id="e8d25-119">Un filtre peut être connecté à deux ou plusieurs filtres dans l’une ou l’autre direction.</span><span class="sxs-lookup"><span data-stu-id="e8d25-119">A filter might be connected to two or more filters in either direction.</span></span> <span data-ttu-id="e8d25-120">Par exemple, il peut s’agir d’un filtre de fractionnement, avec plusieurs filtres en aval.</span><span class="sxs-lookup"><span data-stu-id="e8d25-120">For example, it might be a splitter filter, with several filters downstream from it.</span></span> <span data-ttu-id="e8d25-121">Il peut également s’agir d’un filtre MUX, avec plusieurs filtres en amont.</span><span class="sxs-lookup"><span data-stu-id="e8d25-121">Or it might be a mux filter, with several filters upstream from it.</span></span> <span data-ttu-id="e8d25-122">Par conséquent, vous souhaiterez peut-être les collecter tous dans une liste.</span><span class="sxs-lookup"><span data-stu-id="e8d25-122">Therefore, you might want to collect all of them into a list.</span></span>

<span data-ttu-id="e8d25-123">Le code suivant illustre une manière possible d’implémenter une telle fonction.</span><span class="sxs-lookup"><span data-stu-id="e8d25-123">The following code shows one possible way to implement such a function.</span></span> <span data-ttu-id="e8d25-124">Elle utilise la classe DirectShow [**CGenericList**](cgenericlist.md) . vous pouvez écrire une fonction équivalente à l’aide d’une autre structure de données.</span><span class="sxs-lookup"><span data-stu-id="e8d25-124">It uses the DirectShow [**CGenericList**](cgenericlist.md) class; you could write an equivalent function using some other data structure.</span></span>


```C++
#include <streams.h>  // Link to the DirectShow base class library
// Define a typedef for a list of filters.
typedef CGenericList<IBaseFilter> CFilterList;

// Forward declaration. Adds a filter to the list unless it's a duplicate.
void AddFilterUnique(CFilterList &FilterList, IBaseFilter *pNew);

// Find all the immediate upstream or downstream peers of a filter.
HRESULT GetPeerFilters(
    IBaseFilter *pFilter, // Pointer to the starting filter
    PIN_DIRECTION Dir,    // Direction to search (upstream or downstream)
    CFilterList &FilterList)  // Collect the results in this list.
{
    if (!pFilter) return E_POINTER;

    IEnumPins *pEnum = 0;
    IPin *pPin = 0;
    HRESULT hr = pFilter->EnumPins(&pEnum);
    if (FAILED(hr)) return hr;
    while (S_OK == pEnum->Next(1, &pPin, 0))
    {
        // See if this pin matches the specified direction.
        PIN_DIRECTION ThisPinDir;
        hr = pPin->QueryDirection(&ThisPinDir);
        if (FAILED(hr))
        {
            // Something strange happened.
            hr = E_UNEXPECTED;
            pPin->Release();
            break;
        }
        if (ThisPinDir == Dir)
        {
            // Check if the pin is connected to another pin.
            IPin *pPinNext = 0;
            hr = pPin->ConnectedTo(&pPinNext);
            if (SUCCEEDED(hr))
            {
                // Get the filter that owns that pin.
                PIN_INFO PinInfo;
                hr = pPinNext->QueryPinInfo(&PinInfo);
                pPinNext->Release();
                if (FAILED(hr) || (PinInfo.pFilter == NULL))
                {
                    // Something strange happened.
                    pPin->Release();
                    pEnum->Release();
                    return E_UNEXPECTED;
                }
                // Insert the filter into the list.
                AddFilterUnique(FilterList, PinInfo.pFilter);
                PinInfo.pFilter->Release();
            }
        }
        pPin->Release();
    }
    pEnum->Release();
    return S_OK;
}
void AddFilterUnique(CFilterList &FilterList, IBaseFilter *pNew)
{
    if (pNew == NULL) return;

    POSITION pos = FilterList.GetHeadPosition();
    while (pos)
    {
        IBaseFilter *pF = FilterList.GetNext(pos);
        if (IsEqualObject(pF, pNew))
        {
            return;
        }
    }
    pNew->AddRef();  // The caller must release everything in the list.
    FilterList.AddTail(pNew);
}
```



<span data-ttu-id="e8d25-125">Pour compliquer un peu les choses, un filtre peut avoir plusieurs connexions de code confidentiel au même filtre.</span><span class="sxs-lookup"><span data-stu-id="e8d25-125">To complicate matters somewhat, a filter can have multiple pin connections to the same filter.</span></span> <span data-ttu-id="e8d25-126">Pour éviter de placer des doublons dans la liste, interrogez chaque pointeur **IBaseFilter** pour **IUnknown** et comparez les pointeurs **IUnknown** .</span><span class="sxs-lookup"><span data-stu-id="e8d25-126">To avoid putting duplicates into the list, query each **IBaseFilter** pointer for **IUnknown** and compare the **IUnknown** pointers.</span></span> <span data-ttu-id="e8d25-127">Selon les règles de COM, deux pointeurs d’interface font référence au même objet si et seulement s’ils retournent des pointeurs **IUnknown** identiques.</span><span class="sxs-lookup"><span data-stu-id="e8d25-127">By the rules of COM, two interface pointers refer to the same object if and only if they return identical **IUnknown** pointers.</span></span> <span data-ttu-id="e8d25-128">Dans l’exemple précédent, la fonction AddFilterUnique gère ce détail.</span><span class="sxs-lookup"><span data-stu-id="e8d25-128">In the previous example, the AddFilterUnique function handles this detail.</span></span>

<span data-ttu-id="e8d25-129">L’exemple suivant montre comment utiliser la fonction GetPeerFilters :</span><span class="sxs-lookup"><span data-stu-id="e8d25-129">The following example shows how to use the GetPeerFilters function:</span></span>


```C++
IBaseFilter *pF; // Pointer to some filter.
CFilterList FList(NAME("MyList"));  // List to hold the downstream peers.
hr = GetPeerFilters(pF, PINDIR_OUTPUT, FList);
if (SUCCEEDED(hr))
{
    POSITION pos = FList.GetHeadPosition();
    while (pos)
    {
        IBaseFilter *pDownstream = FList.GetNext(pos);
        pDownstream->Release();
    }
}
```



## <a name="related-topics"></a><span data-ttu-id="e8d25-130">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="e8d25-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e8d25-131">Techniques d' Graph-Building générales</span><span class="sxs-lookup"><span data-stu-id="e8d25-131">General Graph-Building Techniques</span></span>](general-graph-building-techniques.md)
</dt> </dl>

 

 



