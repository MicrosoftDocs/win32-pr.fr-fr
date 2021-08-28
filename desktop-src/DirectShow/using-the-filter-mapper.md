---
description: Utilisation du mappeur de filtre
ms.assetid: 3f774350-4508-437f-98d1-cca91220f339
title: Utilisation du mappeur de filtre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48758c40b97477200b4fab1215eaccac53823771add86d6a8b915370776495a0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120049610"
---
# <a name="using-the-filter-mapper"></a>Utilisation du mappeur de filtre

le [mappeur de filtre](filter-mapper.md) est un objet COM qui énumère les filtres de DirectShow en fonction de différents critères de recherche. Le mappeur de filtre peut être moins efficace que l’énumérateur de périphérique système. par conséquent, si vous avez besoin de filtres d’une catégorie particulière, vous devez utiliser l’énumérateur de périphérique système. Toutefois, si vous devez localiser un filtre qui prend en charge une certaine combinaison de types de média, mais ne fait pas partie d’une catégorie claire, vous devrez peut-être utiliser le mappeur de filtre. (Par exemple, il peut s’agir d’un filtre de convertisseur ou d’un filtre de décodeur).

Le mappeur de filtre expose l’interface [**IFilterMapper2**](/windows/desktop/api/Strmif/nn-strmif-ifiltermapper2) . Pour rechercher un filtre, appelez la méthode [**IFilterMapper2 :: EnumMatchingFilters**](/windows/desktop/api/Strmif/nf-strmif-ifiltermapper2-enummatchingfilters) . Cette méthode prend plusieurs paramètres qui définissent les critères de recherche et retourne un énumérateur pour les filtres correspondants. L’énumérateur prend en charge l’interface [**IEnumMoniker**](/windows/win32/api/objidl/nn-objidl-ienummoniker) et fournit un moniker unique pour chaque filtre correspondant.

L’exemple suivant énumère les filtres qui acceptent les entrées vidéo numériques (DV) et ont au moins une broche de sortie, de n’importe quel type de média. (Le filtre de [décodage vidéo DV](dv-video-decoder-filter.md) correspond à ces critères.)


```C++
IFilterMapper2 *pMapper = NULL;
IEnumMoniker *pEnum = NULL;

hr = CoCreateInstance(CLSID_FilterMapper2, 
    NULL, CLSCTX_INPROC, IID_IFilterMapper2, 
    (void **) &pMapper);

if (FAILED(hr))
{
    // Error handling omitted for clarity.
}

GUID arrayInTypes[2];
arrayInTypes[0] = MEDIATYPE_Video;
arrayInTypes[1] = MEDIASUBTYPE_dvsd;

hr = pMapper->EnumMatchingFilters(
        &pEnum,
        0,                  // Reserved.
        TRUE,               // Use exact match?
        MERIT_DO_NOT_USE+1, // Minimum merit.
        TRUE,               // At least one input pin?
        1,                  // Number of major type/subtype pairs for input.
        arrayInTypes,       // Array of major type/subtype pairs for input.
        NULL,               // Input medium.
        NULL,               // Input pin category.
        FALSE,              // Must be a renderer?
        TRUE,               // At least one output pin?
        0,                  // Number of major type/subtype pairs for output.
        NULL,               // Array of major type/subtype pairs for output.
        NULL,               // Output medium.
        NULL);              // Output pin category.

// Enumerate the monikers.
IMoniker *pMoniker;
ULONG cFetched;
while (pEnum->Next(1, &pMoniker, &cFetched) == S_OK)
{
    IPropertyBag *pPropBag = NULL;
    hr = pMoniker->BindToStorage(0, 0, IID_IPropertyBag, 
       (void **)&pPropBag);

    if (SUCCEEDED(hr))
    {
        // To retrieve the friendly name of the filter, do the following:
        VARIANT varName;
        VariantInit(&varName);
        hr = pPropBag->Read(L"FriendlyName", &varName, 0);
        if (SUCCEEDED(hr))
        {
            // Display the name in your UI somehow.
        }
        VariantClear(&varName);

        // To create an instance of the filter, do the following:
        IBaseFilter *pFilter;
        hr = pMoniker->BindToObject(NULL, NULL, IID_IBaseFilter, (void**)&pFilter);
        // Now add the filter to the graph. Remember to release pFilter later.
    
        // Clean up.
        pPropBag->Release();
    }
    pMoniker->Release();
}

// Clean up.
pMapper->Release();
pEnum->Release();
```



La méthode [**EnumMatchingFilters**](/windows/desktop/api/Strmif/nf-strmif-ifiltermapper2-enummatchingfilters) a un nombre relativement élevé de paramètres, qui sont commentés dans l’exemple. Les plus importants pour cet exemple sont les suivants :

-   Valeur de mérite minimale : le filtre doit avoir une valeur mérite au-dessus de mérite \_ ne \_ pas \_ utiliser.
-   Types d’entrée : l’appelant passe un tableau contenant des paires de types et sous-types principaux. Seuls les filtres qui prennent en charge au moins l’une de ces paires correspondent.
-   Correspondance exacte : un filtre peut enregistrer des valeurs **null** pour le type principal, le sous-type, la catégorie de code confidentiel ou le support. À moins que vous ne spécifiiez la correspondance exacte, une valeur **null** agit comme un caractère générique, correspondant à toute valeur que vous spécifiez. Avec la correspondance exacte, le filtre doit correspondre exactement à vos critères. Toutefois, si vous attribuez un paramètre null dans les critères de recherche, il agit toujours comme un caractère générique ou une valeur de **type** « ne pas se préoccuper », correspondant à n’importe quel filtre.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Énumération des appareils et des filtres](enumerating-devices-and-filters.md)
</dt> <dt>

[Connecter intelligente](intelligent-connect.md)
</dt> </dl>

 

 
