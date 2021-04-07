---
description: Énumération des codes confidentiels
ms.assetid: 231f10c1-46b4-4b66-b0ce-06a191237dfb
title: Énumération des codes confidentiels
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 322f1764c46c146d1b899c869d1708eac1f0427d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103846254"
---
# <a name="enumerating-pins"></a><span data-ttu-id="db6b2-103">Énumération des codes confidentiels</span><span class="sxs-lookup"><span data-stu-id="db6b2-103">Enumerating Pins</span></span>

<span data-ttu-id="db6b2-104">Les filtres prennent en charge la méthode [**IBaseFilter :: EnumPins**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-enumpins) , qui énumère les codes confidentiels disponibles sur le filtre.</span><span class="sxs-lookup"><span data-stu-id="db6b2-104">Filters support the [**IBaseFilter::EnumPins**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-enumpins) method, which enumerates the pins available on the filter.</span></span> <span data-ttu-id="db6b2-105">Elle retourne un pointeur vers l’interface [**IEnumPins**](/windows/desktop/api/Strmif/nn-strmif-ienumpins) .</span><span class="sxs-lookup"><span data-stu-id="db6b2-105">It returns a pointer to the [**IEnumPins**](/windows/desktop/api/Strmif/nn-strmif-ienumpins) interface.</span></span> <span data-ttu-id="db6b2-106">La méthode [**IEnumPins :: Next**](/windows/desktop/api/Strmif/nf-strmif-ienumpins-next) récupère les pointeurs d’interface [**IPIN**](/windows/desktop/api/Strmif/nn-strmif-ipin) .</span><span class="sxs-lookup"><span data-stu-id="db6b2-106">The [**IEnumPins::Next**](/windows/desktop/api/Strmif/nf-strmif-ienumpins-next) method retrieves [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface pointers.</span></span>

<span data-ttu-id="db6b2-107">L’exemple suivant montre une fonction qui localise un code confidentiel avec une direction donnée (entrée ou sortie) sur un filtre donné.</span><span class="sxs-lookup"><span data-stu-id="db6b2-107">The following example shows a function that locates a pin with a given direction (input or output) on a given filter.</span></span> <span data-ttu-id="db6b2-108">Elle utilise l’énumération de [**\_ direction du code confidentiel**](/windows/win32/api/strmif/ne-strmif-pin_direction) pour spécifier la direction du code confidentiel et la méthode [**IPIN :: QueryDirection**](/windows/desktop/api/Strmif/nf-strmif-ipin-querydirection) pour rechercher la direction de chaque code confidentiel énuméré.</span><span class="sxs-lookup"><span data-stu-id="db6b2-108">It uses the [**PIN\_DIRECTION**](/windows/win32/api/strmif/ne-strmif-pin_direction) enumeration to specify the pin direction, and the [**IPin::QueryDirection**](/windows/desktop/api/Strmif/nf-strmif-ipin-querydirection) method to find the direction of each enumerated pin.</span></span> <span data-ttu-id="db6b2-109">Si cette fonction trouve une broche correspondante, elle retourne un pointeur d’interface **IPIN** avec un nombre de références en suspens.</span><span class="sxs-lookup"><span data-stu-id="db6b2-109">If this function finds a matching pin, it returns an **IPin** interface pointer with an outstanding reference count.</span></span> <span data-ttu-id="db6b2-110">L’appelant est responsable de la libération de l’interface.</span><span class="sxs-lookup"><span data-stu-id="db6b2-110">The caller is responsible for releasing the interface.</span></span>


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



<span data-ttu-id="db6b2-111">Cette fonction peut facilement être modifiée pour retourner le nième broche avec la direction spécifiée, ou le *n* ième code confidentiel non connecté.</span><span class="sxs-lookup"><span data-stu-id="db6b2-111">This function could easily be modified to return the nth pin with the specified direction, or the *n* th unconnected pin.</span></span> <span data-ttu-id="db6b2-112">(Pour savoir si un code PIN est connecté à un autre code confidentiel, appelez la méthode [**IPIN :: ConnectedTo**](/windows/desktop/api/Strmif/nf-strmif-ipin-connectedto) .)</span><span class="sxs-lookup"><span data-stu-id="db6b2-112">(To find out if a pin is connected to another pin, call the [**IPin::ConnectedTo**](/windows/desktop/api/Strmif/nf-strmif-ipin-connectedto) method.)</span></span>

## <a name="related-topics"></a><span data-ttu-id="db6b2-113">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="db6b2-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="db6b2-114">Énumération d’objets dans un graphique de filtre</span><span class="sxs-lookup"><span data-stu-id="db6b2-114">Enumerating Objects in a Filter Graph</span></span>](enumerating-objects-in-a-filter-graph.md)
</dt> <dt>

[<span data-ttu-id="db6b2-115">Rechercher un code confidentiel non connecté sur un filtre</span><span class="sxs-lookup"><span data-stu-id="db6b2-115">Find an Unconnected Pin on a Filter</span></span>](find-an-unconnected-pin-on-a-filter.md)
</dt> <dt>

[<span data-ttu-id="db6b2-116">Techniques d' Graph-Building générales</span><span class="sxs-lookup"><span data-stu-id="db6b2-116">General Graph-Building Techniques</span></span>](general-graph-building-techniques.md)
</dt> <dt>

[<span data-ttu-id="db6b2-117">Épingler le jeu de propriétés</span><span class="sxs-lookup"><span data-stu-id="db6b2-117">Pin Property Set</span></span>](pin-property-set.md)
</dt> </dl>

 

 



