---
description: Ajouter un filtre par CLSID
ms.assetid: b15cf324-5b9b-41da-a8cf-87071aaf3b60
title: Ajouter un filtre par CLSID
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f880ab1cb3b88fbe6d889acdd192bba341ce2acf
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127112358"
---
# <a name="add-a-filter-by-clsid"></a>Ajouter un filtre par CLSID

La fonction suivante crée un filtre avec un identificateur de classe (CLSID) spécifié et l’ajoute au graphique de filtre :


```C++
// Create a filter by CLSID and add it to the graph.

HRESULT AddFilterByCLSID(
    IGraphBuilder *pGraph,      // Pointer to the Filter Graph Manager.
    REFGUID clsid,              // CLSID of the filter to create.
    IBaseFilter **ppF,          // Receives a pointer to the filter.
    LPCWSTR wszName             // A name for the filter (can be NULL).
    )
{
    *ppF = 0;

    IBaseFilter *pFilter = NULL;
    
    HRESULT hr = CoCreateInstance(clsid, NULL, CLSCTX_INPROC_SERVER, 
        IID_PPV_ARGS(&pFilter));
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pGraph->AddFilter(pFilter, wszName);
    if (FAILED(hr))
    {
        goto done;
    }

    *ppF = pFilter;
    (*ppF)->AddRef();

done:
    SafeRelease(&pFilter);
    return hr;
}
```



> [!Note]  
> Cet exemple utilise la fonction [SafeRelease](/windows/desktop/medfound/saferelease) pour libérer le pointeur [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) .

 

La fonction appelle [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) pour créer le filtre, puis appelle [**IFilterGraph :: AddFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-addfilter) pour ajouter le filtre au graphique. L’exemple de code suivant utilise cette fonction pour ajouter le filtre [multiplex MUX](avi-mux-filter.md) au graphique :


```C++
IBaseFilter *pMux;
hr = AddFilterByCLSID(pGraph, CLSID_AviDest, L"AVI Mux", &pMux, NULL); 
if (SUCCEEDED(hr))
{
    /* ... */
   pMux->Release();
}
```



Notez que certains filtres ne peuvent pas être créés avec [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance). C’est souvent le cas avec les filtres qui gèrent d’autres composants logiciels. Par exemple, le filtre de [compresseur AVI](avi-compressor-filter.md) est un wrapper pour les codecs vidéo et le filtre de [capture vidéo WDM](wdm-video-capture-filter.md) est un wrapper pour les pilotes de capture WDM. Ces filtres doivent être créés à l’aide de l' [énumérateur du périphérique système](system-device-enumerator.md) ou du [Mappeur de filtre](filter-mapper.md). Pour plus d’informations, consultez [énumération des appareils et des filtres](enumerating-devices-and-filters.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Techniques d' Graph-Building générales](general-graph-building-techniques.md)
</dt> </dl>

 

 
