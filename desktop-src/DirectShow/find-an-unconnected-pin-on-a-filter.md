---
description: Cette rubrique explique comment rechercher un code confidentiel non connecté sur un filtre. La recherche d’un code confidentiel non connecté est utile lorsque vous connectez des filtres.
ms.assetid: d0a906a8-bae4-43b3-8b02-ee5b97c9323d
title: Rechercher un code confidentiel non connecté sur un filtre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ee47b811c027161b70769cb04063d0e8214934a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104033369"
---
# <a name="find-an-unconnected-pin-on-a-filter"></a><span data-ttu-id="27c10-104">Rechercher un code confidentiel non connecté sur un filtre</span><span class="sxs-lookup"><span data-stu-id="27c10-104">Find an Unconnected Pin on a Filter</span></span>

<span data-ttu-id="27c10-105">Cette rubrique explique comment rechercher un code confidentiel non connecté sur un filtre.</span><span class="sxs-lookup"><span data-stu-id="27c10-105">This topic describes how to find an unconnected pin on a filter.</span></span> <span data-ttu-id="27c10-106">La recherche d’un code confidentiel non connecté est utile lorsque vous connectez des filtres.</span><span class="sxs-lookup"><span data-stu-id="27c10-106">Finding an unconnected pin is useful when you are connecting filters.</span></span>

<span data-ttu-id="27c10-107">Dans un scénario de création de graphiques DirectShow classique, vous avez besoin d’un code confidentiel non connecté qui correspond à une direction de pin particulière (entrée ou sortie).</span><span class="sxs-lookup"><span data-stu-id="27c10-107">In a typical DirectShow graph-building scenario, you need an unconnected pin that matches a particular pin direction (input or output).</span></span> <span data-ttu-id="27c10-108">Par exemple, lorsque vous connectez deux filtres, vous connectez une broche de sortie d’un filtre à une broche d’entrée de l’autre filtre.</span><span class="sxs-lookup"><span data-stu-id="27c10-108">For example, when you connect two filters, you connect an output pin from one filter to an input pin from the other filter.</span></span> <span data-ttu-id="27c10-109">Les deux broches doivent être déconnectées avant de les connecter.</span><span class="sxs-lookup"><span data-stu-id="27c10-109">Both pins must be unconnected before you connect them.</span></span>

<span data-ttu-id="27c10-110">Tout d’abord, nous avons besoin d’une fonction qui teste si un code PIN est connecté à un autre code PIN.</span><span class="sxs-lookup"><span data-stu-id="27c10-110">First, we need a function that tests whether a pin is connected to another pin.</span></span> <span data-ttu-id="27c10-111">Cette fonction appelle la méthode [**IPIN :: ConnectedTo**](/windows/desktop/api/Strmif/nf-strmif-ipin-connectedto) pour tester si le pin est connecté à un autre code PIN.</span><span class="sxs-lookup"><span data-stu-id="27c10-111">This function calls the [**IPin::ConnectedTo**](/windows/desktop/api/Strmif/nf-strmif-ipin-connectedto) method to test whether the pin is connected to another pin.</span></span>


```C++
// Query whether a pin is connected to another pin.
//
// Note: This function does not return a pointer to the connected pin.

HRESULT IsPinConnected(IPin *pPin, BOOL *pResult)
{
    IPin *pTmp = NULL;
    HRESULT hr = pPin->ConnectedTo(&pTmp);
    if (SUCCEEDED(hr))
    {
        *pResult = TRUE;
    }
    else if (hr == VFW_E_NOT_CONNECTED)
    {
        // The pin is not connected. This is not an error for our purposes.
        *pResult = FALSE;
        hr = S_OK;
    }

    SafeRelease(&pTmp);
    return hr;
}
```



> [!Note]  
> <span data-ttu-id="27c10-112">Cet exemple utilise la fonction [SafeRelease](/windows/desktop/medfound/saferelease) pour libérer des pointeurs d’interface.</span><span class="sxs-lookup"><span data-stu-id="27c10-112">This example uses the [SafeRelease](/windows/desktop/medfound/saferelease) function to release interface pointers.</span></span>

 

<span data-ttu-id="27c10-113">Ensuite, nous avons besoin d’une fonction qui teste si un pin correspond à une direction de pin spécifiée.</span><span class="sxs-lookup"><span data-stu-id="27c10-113">Next, we need a function that tests whether a pin matches a specified pin direction.</span></span> <span data-ttu-id="27c10-114">Cette fonction appelle la méthode [**IPIN :: QueryDirection**](/windows/desktop/api/Strmif/nf-strmif-ipin-querydirection) pour atteindre la direction du code confidentiel.</span><span class="sxs-lookup"><span data-stu-id="27c10-114">This function calls the [**IPin::QueryDirection**](/windows/desktop/api/Strmif/nf-strmif-ipin-querydirection) method to get the pin direction.</span></span>


```C++
// Query whether a pin has a specified direction (input / output)
HRESULT IsPinDirection(IPin *pPin, PIN_DIRECTION dir, BOOL *pResult)
{
    PIN_DIRECTION pinDir;
    HRESULT hr = pPin->QueryDirection(&pinDir);
    if (SUCCEEDED(hr))
    {
        *pResult = (pinDir == dir);
    }
    return hr;
}
```



<span data-ttu-id="27c10-115">La fonction Next correspond à un code pin à la fois par critère (direction de la broche et état de la connexion).</span><span class="sxs-lookup"><span data-stu-id="27c10-115">The next function matches a pin by both criteria (pin direction and connection status).</span></span>


```C++
// Match a pin by pin direction and connection state.
HRESULT MatchPin(IPin *pPin, PIN_DIRECTION direction, BOOL bShouldBeConnected, BOOL *pResult)
{
    assert(pResult != NULL);

    BOOL bMatch = FALSE;
    BOOL bIsConnected = FALSE;

    HRESULT hr = IsPinConnected(pPin, &bIsConnected);
    if (SUCCEEDED(hr))
    {
        if (bIsConnected == bShouldBeConnected)
        {
            hr = IsPinDirection(pPin, direction, &bMatch);
        }
    }

    if (SUCCEEDED(hr))
    {
        *pResult = bMatch;
    }
    return hr;
}
```



<span data-ttu-id="27c10-116">Enfin, la fonction suivante utilise l’interface [**IEnumPins**](/windows/desktop/api/Strmif/nn-strmif-ienumpins) pour parcourir les codes confidentiels sur le filtre.</span><span class="sxs-lookup"><span data-stu-id="27c10-116">Finally, the following function uses the [**IEnumPins**](/windows/desktop/api/Strmif/nn-strmif-ienumpins) interface to loop through the pins on the filter.</span></span> <span data-ttu-id="27c10-117">L’appelant spécifie le sens du code confidentiel souhaité.</span><span class="sxs-lookup"><span data-stu-id="27c10-117">The caller specifies the desired pin direction.</span></span> <span data-ttu-id="27c10-118">Pour chaque code confidentiel, la fonction appelle `MatchPin` pour tester si le code PIN est une correspondance.</span><span class="sxs-lookup"><span data-stu-id="27c10-118">For each pin, the function calls `MatchPin` to test whether the pin is a match.</span></span> <span data-ttu-id="27c10-119">Si la direction correspond à et que le code pin n’est pas connecté, la fonction retourne un pointeur vers le code PIN correspondant dans le paramètre *ppPin* .</span><span class="sxs-lookup"><span data-stu-id="27c10-119">If the direction matches and the pin is unconnected, the function returns a pointer to the matching pin in the *ppPin* parameter.</span></span>


```C++
// Return the first unconnected input pin or output pin.
HRESULT FindUnconnectedPin(IBaseFilter *pFilter, PIN_DIRECTION PinDir, IPin **ppPin)
{
    IEnumPins *pEnum = NULL;
    IPin *pPin = NULL;
    BOOL bFound = FALSE;

    HRESULT hr = pFilter->EnumPins(&pEnum);
    if (FAILED(hr))
    {
        goto done;
    }

    while (S_OK == pEnum->Next(1, &pPin, NULL))
    {
        hr = MatchPin(pPin, PinDir, FALSE, &bFound);
        if (FAILED(hr))
        {
            goto done;
        }
        if (bFound)
        {
            *ppPin = pPin;
            (*ppPin)->AddRef();
            break;
        }
        SafeRelease(&pPin);
    }

    if (!bFound)
    {
        hr = VFW_E_NOT_FOUND;
    }

done:
    SafeRelease(&pPin);
    SafeRelease(&pEnum);
    return hr;
}
```



<span data-ttu-id="27c10-120">Pour obtenir un exemple de la façon dont cette fonction peut être utilisée, consultez [connecter deux filtres](connect-two-filters.md).</span><span class="sxs-lookup"><span data-stu-id="27c10-120">For an example of how this function can be used, see [Connect Two Filters](connect-two-filters.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="27c10-121">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="27c10-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="27c10-122">Énumération des codes confidentiels</span><span class="sxs-lookup"><span data-stu-id="27c10-122">Enumerating Pins</span></span>](enumerating-pins.md)
</dt> <dt>

[<span data-ttu-id="27c10-123">Techniques d' Graph-Building générales</span><span class="sxs-lookup"><span data-stu-id="27c10-123">General Graph-Building Techniques</span></span>](general-graph-building-techniques.md)
</dt> <dt>

[<span data-ttu-id="27c10-124">**ICaptureGraphBuilder2::FindPin**</span><span class="sxs-lookup"><span data-stu-id="27c10-124">**ICaptureGraphBuilder2::FindPin**</span></span>](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findpin)
</dt> </dl>

 

 
