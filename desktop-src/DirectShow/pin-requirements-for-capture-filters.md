---
description: cette rubrique décrit la configuration requise pour l’implémentation d’une broche de sortie sur un filtre de capture DirectShow.
ms.assetid: cb9cda1c-efa2-4abb-934b-21ba8cb80f30
title: Exigences de code confidentiel pour les filtres de capture
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2a97d3e5c0f7fe0f5a9a341899651685df1cdd3
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126998995"
---
# <a name="pin-requirements-for-capture-filters"></a>Exigences de code confidentiel pour les filtres de capture

cette rubrique décrit la configuration requise pour l’implémentation d’une broche de sortie sur un filtre de capture DirectShow.

## <a name="pin-name"></a>Nom de la broche

Vous pouvez attribuer n’importe quel nom à un pin. si le nom du code confidentiel commence par le caractère tilde (~), le gestionnaire de Graph de filtre ne rend pas automatiquement ce code pin quand une application appelle [**IGraphBuilder :: RenderFile**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile). Par exemple, si le filtre a une broche de capture et une prévisualisation, vous pouvez les nommer respectivement « ~ capture » et « aperçu ». Si une application affiche ce filtre dans un graphique, la broche d’aperçu se connecte à son convertisseur par défaut, et rien ne se connecte au code confidentiel de capture, qui est un comportement par défaut raisonnable. Cela peut également s’appliquer aux codes confidentiels qui fournissent des données d’informations qui ne sont pas destinées à être rendues, ou des codes confidentiels nécessitant des propriétés personnalisées définies. Notez que les codes confidentiels avec le préfixe tilde (~) peuvent toujours être connectés manuellement par l’application.

## <a name="pin-category"></a>Catégorie de code confidentiel

Un filtre de capture a toujours un code confidentiel de capture et peut avoir une broche d’aperçu. Certains filtres de capture peuvent avoir d’autres broches de sortie, afin de fournir d’autres types de données, tels que des informations de contrôle. Chaque code confidentiel de sortie doit exposer l’interface [**IKsPropertySet**](ikspropertyset.md) . Les applications utilisent cette interface pour déterminer la catégorie de code confidentiel. En général, le code PIN retourne soit la \_ capture de catégorie pin, \_ soit l' \_ aperçu de catégorie pin \_ . Pour plus d’informations, consultez l’élément [pin Property Set](pin-property-set.md).

L’exemple suivant montre comment implémenter [**IKsPropertySet**](ikspropertyset.md) pour retourner la catégorie pin sur un code confidentiel de capture :


```C++
// Set: Cannot set any properties.
HRESULT CMyCapturePin::Set(REFGUID guidPropSet, DWORD dwID,
    void *pInstanceData, DWORD cbInstanceData, void *pPropData, 
    DWORD cbPropData)
{
    return E_NOTIMPL;
}

// Get: Return the pin category (our only property). 
HRESULT CMyCapturePin::Get(
    REFGUID guidPropSet,   // Which property set.
    DWORD dwPropID,        // Which property in that set.
    void *pInstanceData,   // Instance data (ignore).
    DWORD cbInstanceData,  // Size of the instance data (ignore).
    void *pPropData,       // Buffer to receive the property data.
    DWORD cbPropData,      // Size of the buffer.
    DWORD *pcbReturned     // Return the size of the property.
)
{
    if (guidPropSet != AMPROPSETID_Pin) 
        return E_PROP_SET_UNSUPPORTED;
    if (dwPropID != AMPROPERTY_PIN_CATEGORY)
        return E_PROP_ID_UNSUPPORTED;
    if (pPropData == NULL && pcbReturned == NULL)
        return E_POINTER;
    if (pcbReturned)
        *pcbReturned = sizeof(GUID);
    if (pPropData == NULL)  // Caller just wants to know the size.
        return S_OK;
    if (cbPropData < sizeof(GUID)) // The buffer is too small.
        return E_UNEXPECTED;
    *(GUID *)pPropData = PIN_CATEGORY_CAPTURE;
    return S_OK;
}

// QuerySupported: Query whether the pin supports the specified property.
HRESULT CMyCapturePin::QuerySupported(REFGUID guidPropSet, DWORD dwPropID,
    DWORD *pTypeSupport)
{
    if (guidPropSet != AMPROPSETID_Pin)
        return E_PROP_SET_UNSUPPORTED;
    if (dwPropID != AMPROPERTY_PIN_CATEGORY)
        return E_PROP_ID_UNSUPPORTED;
    if (pTypeSupport)
        // We support getting this property, but not setting it.
        *pTypeSupport = KSPROPERTY_SUPPORT_GET; 
    return S_OK;
}
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Écriture de filtres de capture](writing-capture-filters.md)
</dt> </dl>

 

 



