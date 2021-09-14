---
description: Rechercher une interface sur un filtre ou un code PIN
ms.assetid: 546f5b7d-3bcd-4e97-a012-daca6ae7bca1
title: Rechercher une interface sur un filtre ou un code PIN
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d264a35e0c33ba53f6a8df7f69113f3358a9737
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127224404"
---
# <a name="find-an-interface-on-a-filter-or-pin"></a>Rechercher une interface sur un filtre ou un code PIN

pour de nombreuses opérations dans DirectShow, l’application appelle des méthodes sur le gestionnaire de Graph de filtre. Toutefois, dans certains cas, l’application doit appeler une méthode directement sur un filtre ou un code PIN. Par exemple, de nombreux filtres exposent des interfaces spécialisées utilisées pour configurer le filtre.

Dans le cas d’une interface de filtre, vous disposez peut-être déjà d’un pointeur vers l’interface [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) du filtre. Dans ce cas, utilisez simplement **QueryInterface** pour accéder à l’autre interface. toutefois, certains filtres peuvent être ajoutés au graphique par le gestionnaire de Graph de filtre. (Pour plus d’informations, consultez [Intelligent connecter](intelligent-connect.md).) Dans ce cas, utilisez l’interface [**IEnumFilters**](/windows/desktop/api/Strmif/nn-strmif-ienumfilters) pour parcourir tous les filtres du graphique, puis interrogez-les chaque fois. La fonction suivante illustre ce qui suit :


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



Pour rechercher une interface sur un code confidentiel, utilisez l’interface [**IEnumPins**](/windows/desktop/api/Strmif/nn-strmif-ienumpins) pour parcourir les broches d’un filtre. La fonction suivante montre comment procéder :


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



La fonction Next recherche une interface sur un filtre ou un code confidentiel :


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



Notez que toutes les fonctions indiquées ici s’arrêtent à la première fonction **QueryInterface** réussie.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Énumération des filtres](enumerating-filters.md)
</dt> <dt>

[Énumération des codes confidentiels](enumerating-pins.md)
</dt> <dt>

[**ICaptureGraphBuilder2::FindInterface**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findinterface)
</dt> </dl>

 

 



