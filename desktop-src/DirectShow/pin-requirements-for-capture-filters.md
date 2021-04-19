---
description: Cette rubrique décrit la configuration requise pour l’implémentation d’une broche de sortie sur un filtre de capture DirectShow.
ms.assetid: cb9cda1c-efa2-4abb-934b-21ba8cb80f30
title: Exigences de code confidentiel pour les filtres de capture
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2a97d3e5c0f7fe0f5a9a341899651685df1cdd3
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "106516149"
---
# <a name="pin-requirements-for-capture-filters"></a><span data-ttu-id="9b7c9-103">Exigences de code confidentiel pour les filtres de capture</span><span class="sxs-lookup"><span data-stu-id="9b7c9-103">Pin Requirements for Capture Filters</span></span>

<span data-ttu-id="9b7c9-104">Cette rubrique décrit la configuration requise pour l’implémentation d’une broche de sortie sur un filtre de capture DirectShow.</span><span class="sxs-lookup"><span data-stu-id="9b7c9-104">This topic describes the requirements for implementing an output pin on a DirectShow capture filter.</span></span>

## <a name="pin-name"></a><span data-ttu-id="9b7c9-105">Nom de la broche</span><span class="sxs-lookup"><span data-stu-id="9b7c9-105">Pin Name</span></span>

<span data-ttu-id="9b7c9-106">Vous pouvez attribuer n’importe quel nom à un pin.</span><span class="sxs-lookup"><span data-stu-id="9b7c9-106">You can give a pin any name.</span></span> <span data-ttu-id="9b7c9-107">Si le nom du code confidentiel commence par le caractère tilde (~), le gestionnaire de graphes de filtre ne rend pas automatiquement ce code confidentiel quand une application appelle [**IGraphBuilder :: RenderFile**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile).</span><span class="sxs-lookup"><span data-stu-id="9b7c9-107">If the pin name begins with the tilde (~) character, the Filter Graph Manager does not automatically render that pin when an application calls [**IGraphBuilder::RenderFile**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile).</span></span> <span data-ttu-id="9b7c9-108">Par exemple, si le filtre a une broche de capture et une prévisualisation, vous pouvez les nommer respectivement « ~ capture » et « aperçu ».</span><span class="sxs-lookup"><span data-stu-id="9b7c9-108">For example, if the filter has a capture pin and a preview pin, you might name them "~Capture" and "Preview," respectively.</span></span> <span data-ttu-id="9b7c9-109">Si une application affiche ce filtre dans un graphique, la broche d’aperçu se connecte à son convertisseur par défaut, et rien ne se connecte au code confidentiel de capture, qui est un comportement par défaut raisonnable.</span><span class="sxs-lookup"><span data-stu-id="9b7c9-109">If an application renders that filter in a graph, the preview pin will connect to its default renderer, and nothing will connect to the capture pin, which is a reasonable default behavior.</span></span> <span data-ttu-id="9b7c9-110">Cela peut également s’appliquer aux codes confidentiels qui fournissent des données d’informations qui ne sont pas destinées à être rendues, ou des codes confidentiels nécessitant des propriétés personnalisées définies.</span><span class="sxs-lookup"><span data-stu-id="9b7c9-110">This can also apply to pins that deliver informational data that is not meant to be rendered, or pins that need custom properties set.</span></span> <span data-ttu-id="9b7c9-111">Notez que les codes confidentiels avec le préfixe tilde (~) peuvent toujours être connectés manuellement par l’application.</span><span class="sxs-lookup"><span data-stu-id="9b7c9-111">Note that pins with the tilde (~) prefix can still be connected manually by the application.</span></span>

## <a name="pin-category"></a><span data-ttu-id="9b7c9-112">Catégorie de code confidentiel</span><span class="sxs-lookup"><span data-stu-id="9b7c9-112">Pin Category</span></span>

<span data-ttu-id="9b7c9-113">Un filtre de capture a toujours un code confidentiel de capture et peut avoir une broche d’aperçu.</span><span class="sxs-lookup"><span data-stu-id="9b7c9-113">A capture filter always has a capture pin, and might have a preview pin.</span></span> <span data-ttu-id="9b7c9-114">Certains filtres de capture peuvent avoir d’autres broches de sortie, afin de fournir d’autres types de données, tels que des informations de contrôle.</span><span class="sxs-lookup"><span data-stu-id="9b7c9-114">Some capture filters might have other output pins, to deliver other types of data, such as control information.</span></span> <span data-ttu-id="9b7c9-115">Chaque code confidentiel de sortie doit exposer l’interface [**IKsPropertySet**](ikspropertyset.md) .</span><span class="sxs-lookup"><span data-stu-id="9b7c9-115">Each output pin must expose the [**IKsPropertySet**](ikspropertyset.md) interface.</span></span> <span data-ttu-id="9b7c9-116">Les applications utilisent cette interface pour déterminer la catégorie de code confidentiel.</span><span class="sxs-lookup"><span data-stu-id="9b7c9-116">Applications use this interface to determine the pin category.</span></span> <span data-ttu-id="9b7c9-117">En général, le code PIN retourne soit la \_ capture de catégorie pin, \_ soit l' \_ aperçu de catégorie pin \_ .</span><span class="sxs-lookup"><span data-stu-id="9b7c9-117">The pin typically returns either PIN\_CATEGORY\_CAPTURE or PIN\_CATEGORY\_PREVIEW.</span></span> <span data-ttu-id="9b7c9-118">Pour plus d’informations, consultez l’élément [pin Property Set](pin-property-set.md).</span><span class="sxs-lookup"><span data-stu-id="9b7c9-118">For more information, see [Pin Property Set](pin-property-set.md).</span></span>

<span data-ttu-id="9b7c9-119">L’exemple suivant montre comment implémenter [**IKsPropertySet**](ikspropertyset.md) pour retourner la catégorie pin sur un code confidentiel de capture :</span><span class="sxs-lookup"><span data-stu-id="9b7c9-119">The following example shows how to implement [**IKsPropertySet**](ikspropertyset.md) to return the pin category on a capture pin:</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="9b7c9-120">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="9b7c9-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9b7c9-121">Écriture de filtres de capture</span><span class="sxs-lookup"><span data-stu-id="9b7c9-121">Writing Capture Filters</span></span>](writing-capture-filters.md)
</dt> </dl>

 

 



