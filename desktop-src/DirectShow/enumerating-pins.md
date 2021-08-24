---
description: Énumération des codes confidentiels
ms.assetid: 231f10c1-46b4-4b66-b0ce-06a191237dfb
title: Énumération des codes confidentiels
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d772903321c71ab2c6d66f7cc46b7ca61b11f96a4bc17b13b8b2f8931d8eac5f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119748709"
---
# <a name="enumerating-pins"></a>Énumération des codes confidentiels

Les filtres prennent en charge la méthode [**IBaseFilter :: EnumPins**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-enumpins) , qui énumère les codes confidentiels disponibles sur le filtre. Elle retourne un pointeur vers l’interface [**IEnumPins**](/windows/desktop/api/Strmif/nn-strmif-ienumpins) . La méthode [**IEnumPins :: Next**](/windows/desktop/api/Strmif/nf-strmif-ienumpins-next) récupère les pointeurs d’interface [**IPIN**](/windows/desktop/api/Strmif/nn-strmif-ipin) .

L’exemple suivant montre une fonction qui localise un code confidentiel avec une direction donnée (entrée ou sortie) sur un filtre donné. Elle utilise l’énumération de [**\_ direction du code confidentiel**](/windows/win32/api/strmif/ne-strmif-pin_direction) pour spécifier la direction du code confidentiel et la méthode [**IPIN :: QueryDirection**](/windows/desktop/api/Strmif/nf-strmif-ipin-querydirection) pour rechercher la direction de chaque code confidentiel énuméré. Si cette fonction trouve une broche correspondante, elle retourne un pointeur d’interface **IPIN** avec un nombre de références en suspens. L’appelant est responsable de la libération de l’interface.


```C++
HRESULT GetPin(IBaseFilter *pFilter, PIN_DIRECTION PinDir, IPin **ppPin)
{
    IEnumPins  *pEnum = NULL;
    IPin       *pPin = NULL;
    HRESULT    hr;

    if (ppPin == NULL)
    {
        return E_POINTER;
    }

    hr = pFilter->EnumPins(&pEnum);
    if (FAILED(hr))
    {
        return hr;
    }
    while(pEnum->Next(1, &pPin, 0) == S_OK)
    {
        PIN_DIRECTION PinDirThis;
        hr = pPin->QueryDirection(&PinDirThis);
        if (FAILED(hr))
        {
            pPin->Release();
            pEnum->Release();
            return hr;
        }
        if (PinDir == PinDirThis)
        {
            // Found a match. Return the IPin pointer to the caller.
            *ppPin = pPin;
            pEnum->Release();
            return S_OK;
        }
        // Release the pin for the next time through the loop.
        pPin->Release();
    }
    // No more pins. We did not find a match.
    pEnum->Release();
    return E_FAIL;  
}
```



Cette fonction peut facilement être modifiée pour retourner le nième broche avec la direction spécifiée, ou le *n* ième code confidentiel non connecté. (Pour savoir si un code PIN est connecté à un autre code confidentiel, appelez la méthode [**IPIN :: ConnectedTo**](/windows/desktop/api/Strmif/nf-strmif-ipin-connectedto) .)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Énumération d’objets dans un filtre Graph](enumerating-objects-in-a-filter-graph.md)
</dt> <dt>

[Rechercher un code confidentiel non connecté sur un filtre](find-an-unconnected-pin-on-a-filter.md)
</dt> <dt>

[Techniques d' Graph-Building générales](general-graph-building-techniques.md)
</dt> <dt>

[Épingler le jeu de propriétés](pin-property-set.md)
</dt> </dl>

 

 



