---
description: Énumération des filtres
ms.assetid: 57bcaa4d-37bf-457d-937e-f9d24fb5784f
title: Énumération des filtres
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d584ddf74a13b06e99d9a7e0a34ac802c6da881d87cb163411100ea7772e1df
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117819662"
---
# <a name="enumerating-filters"></a>Énumération des filtres

le gestionnaire de Graph de filtre prend en charge la méthode [**IFilterGraph :: EnumFilters**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-enumfilters) , qui énumère tous les filtres dans le graphique de filtre. Elle retourne un pointeur vers l’interface [**IEnumFilters**](/windows/desktop/api/Strmif/nn-strmif-ienumfilters) . La méthode [**IEnumFilters :: Next**](/windows/desktop/api/Strmif/nf-strmif-ienumfilters-next) récupère les pointeurs d’interface [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) .

L’exemple suivant montre une fonction qui énumère les filtres dans un graphique et affiche une boîte de message avec le nom de chaque filtre. Elle utilise la méthode [**IBaseFilter :: QueryFilterInfo**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-queryfilterinfo) pour récupérer le nom du filtre. Notez les emplacements où la fonction appelle **Release** sur une interface pour décrémenter le décompte de références.


```C++
HRESULT EnumFilters (IFilterGraph *pGraph) 
{
    IEnumFilters *pEnum = NULL;
    IBaseFilter *pFilter;
    ULONG cFetched;

    HRESULT hr = pGraph->EnumFilters(&pEnum);
    if (FAILED(hr)) return hr;

    while(pEnum->Next(1, &pFilter, &cFetched) == S_OK)
    {
        FILTER_INFO FilterInfo;
        hr = pFilter->QueryFilterInfo(&FilterInfo);
        if (FAILED(hr))
        {
            MessageBox(NULL, TEXT("Could not get the filter info"),
                TEXT("Error"), MB_OK | MB_ICONERROR);
            continue;  // Maybe the next one will work.
        }

#ifdef UNICODE
        MessageBox(NULL, FilterInfo.achName, TEXT("Filter Name"), MB_OK);
#else
        char szName[MAX_FILTER_NAME];
        int cch = WideCharToMultiByte(CP_ACP, 0, FilterInfo.achName,
            MAX_FILTER_NAME, szName, MAX_FILTER_NAME, 0, 0);
        if (cch > 0)
            MessageBox(NULL, szName, TEXT("Filter Name"), MB_OK);
#endif

        // The FILTER_INFO structure holds a pointer to the Filter Graph
        // Manager, with a reference count that must be released.
        if (FilterInfo.pGraph != NULL)
        {
            FilterInfo.pGraph->Release();
        }
        pFilter->Release();
    }

    pEnum->Release();
    return S_OK;
}
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Énumération d’objets dans un filtre Graph](enumerating-objects-in-a-filter-graph.md)
</dt> </dl>

 

 



