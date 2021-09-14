---
description: cette rubrique présente certaines fonctions d’assistance pour la connexion des filtres de DirectShow.
ms.assetid: cfd85944-7ae7-49e6-948f-9e190cdeed12
title: Connecter Deux filtres
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a7e70e607c510490e7ed841ea44303153a94e83f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127111234"
---
# <a name="connect-two-filters"></a>Connecter Deux filtres

cette rubrique présente certaines fonctions d’assistance pour la connexion des filtres de DirectShow.

Pour connecter deux filtres, vous devez trouver une broche de sortie non connectée sur le filtre en amont et une broche d’entrée non connectée sur le filtre en aval.

si vous avez déjà des pointeurs vers les deux codes confidentiels, appelez la méthode [**IGraphBuilder :: Connecter**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-connect) pour les connecter. si les codes confidentiels ne peuvent pas se connecter directement entre eux, la méthode **IGraphBuilder :: Connecter** peut insérer des filtres supplémentaires pour terminer la connexion. Pour plus d’informations, consultez [Intelligent connecter](intelligent-connect.md).

Si vous avez un pointeur vers les filtres, mais pas les codes confidentiels, vous devez utiliser la méthode [**IBaseFilter :: EnumPins**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-enumpins) pour rechercher les broches. (Consultez [énumération des codes confidentiels](enumerating-pins.md).) Les fonctions d’assistance de cette rubrique illustrent cette technique.

### <a name="output-pin-to-filter"></a>Broche de sortie à filtrer

La fonction suivante accepte deux paramètres : un pointeur vers une broche de sortie et un pointeur vers un filtre. La fonction connecte la broche de sortie à la première broche d’entrée disponible sur le filtre.


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



Cette fonction effectue les opérations suivantes :

1.  Appelle la `FindUnconnectedPin` fonction pour recevoir une broche d’entrée non connectée. Cette fonction est présentée dans la rubrique [Rechercher un code confidentiel non connecté sur un filtre](find-an-unconnected-pin-on-a-filter.md).
2.  appelle [**IGraphBuilder :: Connecter**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-connect) pour connecter les deux broches.

### <a name="filter-to-input-pin"></a>Filtrer sur la broche d’entrée

La fonction Next prend un pointeur vers un filtre et un pointeur vers une broche d’entrée. Il connecte la broche d’entrée à la première broche de sortie disponible sur le filtre.


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



### <a name="filter-to-filter"></a>Filtrer pour filtrer

La troisième fonction accepte un pointeur vers un filtre amont et un pointeur vers un filtre en aval, et tente de connecter les deux filtres.


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



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Techniques d' Graph-Building générales](general-graph-building-techniques.md)
</dt> <dt>

[**ICaptureGraphBuilder2 :: RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream)
</dt> </dl>

 

 



