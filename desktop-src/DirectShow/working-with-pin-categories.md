---
description: Utilisation des catégories de code confidentiel
ms.assetid: 1ee648b3-8370-4e4d-b513-d998131512ee
title: Utilisation des catégories de code confidentiel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ac58fff91821477cca51e0613772e3e5763d4d3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106542911"
---
# <a name="working-with-pin-categories"></a>Utilisation des catégories de code confidentiel

Pour effectuer une recherche sur un filtre pour un code confidentiel avec une catégorie de pin donnée, vous pouvez utiliser la méthode [**ICaptureGraphBuilder2 :: FindPin**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findpin) . L’exemple suivant recherche un code pin d’aperçu vidéo :


```C++
int i = 0;
hr = pBuild->FindPin(
    pFilter,               // Pointer to a filter to search.
    PINDIR_OUTPUT,         // Which pin direction?
    &PIN_CATEGORY_PREVIEW, // Which category? (NULL means "any category")
    &MEDIATYPE_Video,      // What media type? (NULL means "any type")
    FALSE,                 // Must be connected?
    i,                     // Get the i'th matching pin (0 = first match)
    &pPin                  // Receives a pointer to the pin.
);
```



Le premier paramètre est un pointeur vers l’interface [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) du filtre. Les trois paramètres suivants spécifient la direction, la catégorie de code confidentiel et le type de média. La valeur **false** dans le cinquième paramètre indique que le code pin peut être connecté ou non connecté. (Pour obtenir les définitions exactes de ces paramètres, reportez-vous à la documentation de la méthode.) Si la méthode trouve une broche correspondante, elle retourne un pointeur vers l’interface [**IPIN**](/windows/desktop/api/Strmif/nn-strmif-ipin) dans le paramètre *pPin* .

Bien que la méthode [**FindPin**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findpin) soit pratique, vous pouvez également écrire vos propres fonctions d’assistance Si vous préférez. Pour déterminer la catégorie d’un pin, appelez la méthode [**IKsPropertySet :: obtenir**](ikspropertyset-get.md) comme décrit dans le [jeu de propriétés de code confidentiel](pin-property-set.md)de la rubrique.

Le code suivant illustre une fonction d’assistance qui vérifie si un code confidentiel correspond à une catégorie spécifiée :


```C++
// Returns TRUE if a pin matches the specified pin category.

BOOL PinMatchesCategory(IPin *pPin, REFGUID Category)
{
    BOOL bFound = FALSE;

    IKsPropertySet *pKs = NULL;
    HRESULT hr = pPin->QueryInterface(IID_PPV_ARGS(&pKs));
    if (SUCCEEDED(hr))
    {
        GUID PinCategory;
        DWORD cbReturned;
        hr = pKs->Get(AMPROPSETID_Pin, AMPROPERTY_PIN_CATEGORY, NULL, 0, 
            &PinCategory, sizeof(GUID), &cbReturned);
        if (SUCCEEDED(hr) && (cbReturned == sizeof(GUID)))
        {
            bFound = (PinCategory == Category);
        }
        pKs->Release();
    }
    return bFound;
}
```



L’exemple suivant est une fonction qui recherche un code confidentiel par catégorie, similaire à la méthode [**FindPin**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findpin) :


```C++
// Finds the first pin that matches a specified pin category and direction.

HRESULT FindPinByCategory(
    IBaseFilter *pFilter, // Pointer to the filter to search.
    PIN_DIRECTION PinDir, // Direction of the pin.
    REFGUID Category,     // Pin category.
    IPin **ppPin)         // Receives a pointer to the pin.
{
    *ppPin = 0;

    HRESULT hr = S_OK;
    BOOL bFound = FALSE;

    IEnumPins *pEnum = 0;
    IPin *pPin = 0;

    hr = pFilter->EnumPins(&pEnum);
    if (FAILED(hr))
    {
        goto done;
    }

    while (hr = pEnum->Next(1, &pPin, 0), hr == S_OK)
    {
        PIN_DIRECTION ThisPinDir;
        hr = pPin->QueryDirection(&ThisPinDir);
        if (FAILED(hr))
        {
            goto done;
        }
        if ((ThisPinDir == PinDir) && 
            PinMatchesCategory(pPin, Category))
        {
            *ppPin = pPin;
            (*ppPin)->AddRef();   // The caller must release the interface.
            bFound = TRUE;
            break;
        }
        SafeRelease(&pPin);
    }

done:
    SafeRelease(&pPin);
    SafeRelease(&pEnum);
    if (SUCCEEDED(hr) && !bFound)
    {
        hr = E_FAIL;
    }
    return hr;
}
```



Le code suivant utilise la fonction Previous pour rechercher une broche de port vidéo sur un filtre :


```C++
IPin *pVP; 
hr = FindPinByCategory(pFilter, PINDIR_OUTPUT, 
    PIN_CATEGORY_VIDEOPORT, &pVP);
if (SUCCEEDED(hr))
{
    // Use pVP ... 
    // Release when you are done.
    pVP->Release();
}
```



Pour plus d’informations sur les jeux de propriétés, reportez-vous à la documentation de [Windows Driver Kit (WDK)](/windows-hardware/drivers/gettingstarted/) .

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Rubriques avancées sur la capture](advanced-capture-topics.md)
</dt> <dt>

[Épingler le jeu de propriétés](pin-property-set.md)
</dt> <dt>

[Filtres de capture vidéo DirectShow](directshow-video-capture-filters.md)
</dt> </dl>

 

 
