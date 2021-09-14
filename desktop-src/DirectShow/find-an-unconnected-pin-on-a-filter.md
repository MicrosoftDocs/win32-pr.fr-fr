---
description: Cette rubrique explique comment rechercher un code confidentiel non connecté sur un filtre. La recherche d’un code confidentiel non connecté est utile lorsque vous connectez des filtres.
ms.assetid: d0a906a8-bae4-43b3-8b02-ee5b97c9323d
title: Rechercher un code confidentiel non connecté sur un filtre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ee47b811c027161b70769cb04063d0e8214934a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127007562"
---
# <a name="find-an-unconnected-pin-on-a-filter"></a>Rechercher un code confidentiel non connecté sur un filtre

Cette rubrique explique comment rechercher un code confidentiel non connecté sur un filtre. La recherche d’un code confidentiel non connecté est utile lorsque vous connectez des filtres.

dans un scénario classique de création de graphiques DirectShow, vous avez besoin d’un code confidentiel non connecté qui correspond à une direction de pin particulière (entrée ou sortie). Par exemple, lorsque vous connectez deux filtres, vous connectez une broche de sortie d’un filtre à une broche d’entrée de l’autre filtre. Les deux broches doivent être déconnectées avant de les connecter.

Tout d’abord, nous avons besoin d’une fonction qui teste si un code PIN est connecté à un autre code PIN. Cette fonction appelle la méthode [**IPIN :: ConnectedTo**](/windows/desktop/api/Strmif/nf-strmif-ipin-connectedto) pour tester si le pin est connecté à un autre code PIN.


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
> Cet exemple utilise la fonction [SafeRelease](/windows/desktop/medfound/saferelease) pour libérer des pointeurs d’interface.

 

Ensuite, nous avons besoin d’une fonction qui teste si un pin correspond à une direction de pin spécifiée. Cette fonction appelle la méthode [**IPIN :: QueryDirection**](/windows/desktop/api/Strmif/nf-strmif-ipin-querydirection) pour atteindre la direction du code confidentiel.


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



La fonction Next correspond à un code pin à la fois par critère (direction de la broche et état de la connexion).


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



Enfin, la fonction suivante utilise l’interface [**IEnumPins**](/windows/desktop/api/Strmif/nn-strmif-ienumpins) pour parcourir les codes confidentiels sur le filtre. L’appelant spécifie le sens du code confidentiel souhaité. Pour chaque code confidentiel, la fonction appelle `MatchPin` pour tester si le code PIN est une correspondance. Si la direction correspond à et que le code pin n’est pas connecté, la fonction retourne un pointeur vers le code PIN correspondant dans le paramètre *ppPin* .


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



pour obtenir un exemple de la façon dont cette fonction peut être utilisée, consultez [Connecter deux filtres](connect-two-filters.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Énumération des codes confidentiels](enumerating-pins.md)
</dt> <dt>

[Techniques d' Graph-Building générales](general-graph-building-techniques.md)
</dt> <dt>

[**ICaptureGraphBuilder2::FindPin**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findpin)
</dt> </dl>

 

 
