---
title: Utilisation de la mise en cache
description: Cette rubrique contient un exemple de code qui montre comment utiliser les fonctionnalités de mise en cache (ou d’extraction en bloc) de l’arborescence Microsoft UI Automation.
ms.assetid: d72fa637-35ca-4c28-922d-263f469cb1c8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8758621a8499202b820a6ffc3459fade57c2a485
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106510002"
---
# <a name="how-to-use-caching"></a>Utilisation de la mise en cache

Cette rubrique contient un exemple de code qui montre comment utiliser les fonctionnalités de mise en cache (ou d’extraction en bloc) de l’arborescence Microsoft UI Automation. Il aborde les sujets suivants :

-   [Récupération des propriétés et des modèles de contrôle dans le cache](#fetching-properties-and-control-patterns-into-the-cache)
-   [Récupération des propriétés et des modèles de contrôle à partir du cache](#retrieving-properties-and-control-patterns-from-the-cache)
-   [Rubriques connexes](#related-topics)

## <a name="fetching-properties-and-control-patterns-into-the-cache"></a>Récupération des propriétés et des modèles de contrôle dans le cache

L’exemple de code suivant montre une fonction qui récupère des éléments d’un contrôle de liste et met en cache le modèle de contrôle SelectionItem et la propriété de nom pour chaque élément. Par défaut, les éléments de liste sont retournés avec une référence complète, afin que toutes les propriétés actuelles soient toujours disponibles.


```C++
// Given a list element, caches a control pattern and a property for
// all the list items.
IUIAutomationElementArray* FindAndCacheListItems(IUIAutomationElement* pList)
{
    if (pList == NULL)
        return NULL;
    
    IUIAutomationCondition* pCondition = NULL;
    IUIAutomationCacheRequest* pCacheRequest = NULL;
    IUIAutomationElementArray* pFound = NULL;

    HRESULT hr = g_pAutomation->CreateTrueCondition(&pCondition);
    if (FAILED(hr))
        goto cleanup;

    hr = g_pAutomation->CreateCacheRequest(&pCacheRequest);
    if (FAILED(hr))
        goto cleanup;

    hr = pCacheRequest->AddPattern(UIA_SelectionItemPatternId);
    if (FAILED(hr))
        goto cleanup;

    hr = pCacheRequest->AddProperty(UIA_NamePropertyId);
    if (FAILED(hr))
        goto cleanup;

    pList->FindAllBuildCache(TreeScope_Children, pCondition, pCacheRequest, &pFound);
    
cleanup:
    if (pCondition != NULL)
        pCondition->Release();

    if (pCacheRequest != NULL)
        pCacheRequest->Release();

    return pFound;
}
```



## <a name="retrieving-properties-and-control-patterns-from-the-cache"></a>Récupération des propriétés et des modèles de contrôle à partir du cache

Le code suivant montre comment récupérer des propriétés et des modèles de contrôle à partir du cache. Il récupère le modèle de contrôle SelectionItem et la propriété de nom pour un élément de liste.


```C++
// Demonstrates retrieval of cached properties from a list item
// obtained in FindAndCacheListItems.
HRESULT GetCachedListItem(IUIAutomationElement* pItem)
{           
    if (pItem == NULL)
    {
        return E_INVALIDARG;
    }

    IUIAutomationSelectionItemPattern* pSelectionItemPattern;
    HRESULT hr = pItem->GetCachedPatternAs(UIA_SelectionItemPatternId, 
        IID_IUIAutomationSelectionItemPattern, (void**)&pSelectionItemPattern);
    if (pSelectionItemPattern != NULL)
    {
        // ... To do: Do something with the pattern.

        pSelectionItemPattern->Release();
    }

    // Retrieve a cached property.
    BSTR bstrName;
    hr = pItem->get_CachedName(&bstrName);
    if (SUCCEEDED(hr))
    {
        // ... To do: Do something with the property.

        // Clean up when done with name.
        SysFreeString(bstrName);
        bstrName = NULL;
    }

    BOOL isControl;

    // The following returns E_INVALIDARG because the property was not cached.
    // hr = pItem->get_CachedIsControlElement(&isControl);

    // The following is valid because we have a full reference to the object, therefore
    // we can get current properties. If the cache request had been made with 
    // AutomationElementMode_None, no current properties would be available from
    // this IUIAutomationElement.
    hr = pItem->get_CurrentIsControlElement(&isControl);
    return hr;
}
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

**Méthodologique**
</dt> <dt>

[Mise en cache des propriétés UI Automation et des modèles de contrôle](uiauto-cachingforclients.md)
</dt> <dt>

[Rubriques de procédures pour les clients UI Automation](uiauto-howto-topics-for-uiautomation-clients.md)
</dt> </dl>

 

 




