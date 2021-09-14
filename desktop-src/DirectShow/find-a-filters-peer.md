---
description: Rechercher un homologue de filtres
ms.assetid: 74d9fe65-f7f4-4971-9550-27884ac4146b
title: Rechercher un homologue de filtres
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1717f6ad61ad7310fdaa11ea5baaab4dcb7f8011
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127224396"
---
# <a name="find-a-filters-peer"></a>Rechercher un homologue de filtres

Pour un filtre donné, vous pouvez parcourir le graphique en recherchant les filtres auxquels il est connecté. Commencez par énumérer les codes confidentiels du filtre. Pour chaque code confidentiel, vérifiez si ce code PIN est connecté à un autre code PIN. Si c’est le cas, interrogez l’autre pin pour obtenir le filtre propriétaire. Vous pouvez parcourir le graphique dans la direction amont en énumérant les broches d’entrée du filtre ou dans la direction en aval en énumérant les broches de sortie.

La fonction suivante recherche en amont ou en aval un filtre connecté. Elle retourne le premier filtre correspondant qu’elle trouve :


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



La fonction appelle [**IBaseFilter :: EnumPins**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-enumpins) pour énumérer les codes confidentiels du premier filtre. Pour chaque code confidentiel, il appelle [**IPIN :: QueryDirection**](/windows/desktop/api/Strmif/nf-strmif-ipin-querydirection) pour vérifier si le code PIN correspond à la direction spécifiée (entrée ou sortie). Si c’est le cas, la fonction détermine si cette broche est connectée à un autre code confidentiel, en appelant la méthode [**IPIN :: ConnectedTo**](/windows/desktop/api/Strmif/nf-strmif-ipin-connectedto) . Enfin, il appelle [**IPIN :: QueryPinInfo**](/windows/desktop/api/Strmif/nf-strmif-ipin-querypininfo) sur l’épingle connecté. Cette méthode retourne une structure qui contient, entre autres choses, un pointeur vers le filtre propriétaire de ce pin. Ce pointeur est retourné à l’appelant dans le paramètre *ppNext* . L’appelant doit libérer le pointeur.

Le code suivant montre comment appeler cette fonction :


```C++
IBaseFilter *pF; // Pointer to some filter.
IBaseFilter *pUpstream = NULL;
if (SUCCEEDED(GetNextFilter(pF, PINDIR_INPUT, &pUpstream)))
{
    // Use pUpstream ...
    pUpstream->Release();
}
```



Un filtre peut être connecté à deux ou plusieurs filtres dans l’une ou l’autre direction. Par exemple, il peut s’agir d’un filtre de fractionnement, avec plusieurs filtres en aval. Il peut également s’agir d’un filtre MUX, avec plusieurs filtres en amont. Par conséquent, vous souhaiterez peut-être les collecter tous dans une liste.

Le code suivant illustre une manière possible d’implémenter une telle fonction. elle utilise la classe DirectShow [**CGenericList**](cgenericlist.md) ; vous pouvez écrire une fonction équivalente à l’aide d’une autre structure de données.


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



Pour compliquer un peu les choses, un filtre peut avoir plusieurs connexions de code confidentiel au même filtre. Pour éviter de placer des doublons dans la liste, interrogez chaque pointeur **IBaseFilter** pour **IUnknown** et comparez les pointeurs **IUnknown** . Selon les règles de COM, deux pointeurs d’interface font référence au même objet si et seulement s’ils retournent des pointeurs **IUnknown** identiques. Dans l’exemple précédent, la fonction AddFilterUnique gère ce détail.

L’exemple suivant montre comment utiliser la fonction GetPeerFilters :


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



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Techniques d' Graph-Building générales](general-graph-building-techniques.md)
</dt> </dl>

 

 



