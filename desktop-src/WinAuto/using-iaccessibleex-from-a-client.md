---
title: Utilisation de IAccessibleEx à partir d’un client
description: Cette rubrique explique comment les clients accèdent à l’implémentation IAccessibleEx d’un serveur et l’utilisent pour obtenir des propriétés UI Automation et des modèles de contrôle pour les éléments d’interface utilisateur.
ms.assetid: e057bbe8-5dd7-41fc-a5d5-bcf4c1c6433d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77b14b935bd7ed432ea4d378034763635309213f
ms.sourcegitcommit: 89f99926f946dc6c5ea600fb7c41f6b19ceac516
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/21/2020
ms.locfileid: "104383251"
---
# <a name="using-iaccessibleex-from-a-client"></a><span data-ttu-id="2ef6b-103">Utilisation de IAccessibleEx à partir d’un client</span><span class="sxs-lookup"><span data-stu-id="2ef6b-103">Using IAccessibleEx from a Client</span></span>

<span data-ttu-id="2ef6b-104">Cette rubrique explique comment les clients accèdent à l’implémentation [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) d’un serveur et l’utilisent pour obtenir des propriétés UI Automation et des modèles de contrôle pour les éléments d’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="2ef6b-104">This topic explains how clients access the [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) implementation of a server and use it to get UI Automation properties and control patterns for UI elements.</span></span>

<span data-ttu-id="2ef6b-105">Les procédures et les exemples de cette section supposent qu’un client [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) est déjà en cours de traitement et qu’un serveur Microsoft Active Accessibility Server existant.</span><span class="sxs-lookup"><span data-stu-id="2ef6b-105">The procedures and examples in this section assume an [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) client that is already in-process, and an existing Microsoft Active Accessibility server.</span></span> <span data-ttu-id="2ef6b-106">Ils supposent également que le client a déjà obtenu un objet **IAccessible** à l’aide de l’une des fonctions de l’infrastructure d’accessibilité, telles que [**AccessibleObjectFromEvent**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromevent), [**AccessibleObjectFromPoint**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfrompoint)ou [**AccessibleObjectFromWindow**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow).</span><span class="sxs-lookup"><span data-stu-id="2ef6b-106">They also assume that the client has already obtained an **IAccessible** object by using one of the accessibility framework functions such as [**AccessibleObjectFromEvent**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromevent), [**AccessibleObjectFromPoint**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfrompoint), or [**AccessibleObjectFromWindow**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow).</span></span>

### <a name="obtaining-an-iaccessibleex-interface-from-the-iaccessible-interface"></a><span data-ttu-id="2ef6b-107">Obtention d’une interface IAccessibleEx à partir de l’interface IAccessible</span><span class="sxs-lookup"><span data-stu-id="2ef6b-107">Obtaining an IAccessibleEx Interface from the IAccessible Interface</span></span>

<span data-ttu-id="2ef6b-108">Un client qui a une interface [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) pour un objet accessible peut l’utiliser pour obtenir l’interface [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) correspondante en procédant comme suit :</span><span class="sxs-lookup"><span data-stu-id="2ef6b-108">A client that has an [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface for an accessible object can use it to obtain the corresponding [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) interface by following these steps:</span></span>

-   <span data-ttu-id="2ef6b-109">Appelez [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) sur l’objet [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) d’origine avec un IID de \_ \_ uuidof (IServiceProvider).</span><span class="sxs-lookup"><span data-stu-id="2ef6b-109">Call [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) on the original [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) object with an IID of \_\_uuidof(IServiceProvider).</span></span>
-   <span data-ttu-id="2ef6b-110">Appelez **IServiceProvider :: QueryService** pour accéder au [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex).</span><span class="sxs-lookup"><span data-stu-id="2ef6b-110">Call **IServiceProvider::QueryService** to get the [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex).</span></span>

### <a name="handling-the-child-id"></a><span data-ttu-id="2ef6b-111">Gestion de l’ID enfant</span><span class="sxs-lookup"><span data-stu-id="2ef6b-111">Handling the Child ID</span></span>

<span data-ttu-id="2ef6b-112">Les clients doivent être préparés pour les serveurs ayant un ID enfant autre que CHILDID \_ self.</span><span class="sxs-lookup"><span data-stu-id="2ef6b-112">Clients must be prepared for servers with a child ID other than CHILDID\_SELF.</span></span> <span data-ttu-id="2ef6b-113">Après avoir obtenu une interface [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) à partir d’un [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible), les clients doivent appeler [**IAccessibleEx :: GetObjectForChild**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iaccessibleex-getobjectforchild) si l’ID enfant n’est pas CHILDID \_ Self (indiquant un objet parent).</span><span class="sxs-lookup"><span data-stu-id="2ef6b-113">After obtaining an [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) interface from an [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible), clients must call [**IAccessibleEx::GetObjectForChild**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iaccessibleex-getobjectforchild) if the child ID is not CHILDID\_SELF (indicating a parent object).</span></span>

<span data-ttu-id="2ef6b-114">L’exemple suivant montre comment obtenir un [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) pour un objet [**IACCESSIBLE**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) et un ID enfant particuliers.</span><span class="sxs-lookup"><span data-stu-id="2ef6b-114">The following example shows how to get an [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) for a particular [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) object and child ID.</span></span>


```C++
   
HRESULT GetIAccessibleExFromIAccessible(IAccessible * pAcc, long idChild, 
                                           IAccessibleEx ** ppaex)
{
    *ppaex = NULL;

    // First, get IServiceProvider from the IAccessible.
    IServiceProvider * pSp = NULL;
    HRESULT hr = pAcc->QueryInterface(IID_IServiceProvider, (void **) & pSp);
    if(FAILED(hr))
        return hr;
    if(pSp == NULL)
        return E_NOINTERFACE;

    // Next, get the IAccessibleEx for the parent object.
    IAccessibleEx * paex = NULL;
    hr = pSp->QueryService(__uuidof(IAccessibleEx), __uuidof(IAccessibleEx),
                                                                 (void **)&paex);
    pSp->Release();
    if(FAILED(hr))
        return hr;
    if(paex == NULL)
        return E_NOINTERFACE;

    // If this is for CHILDID_SELF, we're done. Otherwise, we have a child ID and 
    // can request the object for child.
    if(idChild == CHILDID_SELF)
    {
        *ppaex = paex;
        return S_OK;
    }
    else
    {
        // Get the IAccessibleEx for the specified child.
        IAccessibleEx * paexChild = NULL;
        hr = paex->GetObjectForChild(idChild, &paexChild);
        paex->Release();
        if(FAILED(hr))
            return hr;
        if(paexChild == NULL)
            return E_NOINTERFACE;
        *ppaex = paexChild;
        return S_OK;
    }
}
```



### <a name="obtaining-the-irawelementprovidersimple-interface"></a><span data-ttu-id="2ef6b-115">Obtention de l’interface IRawElementProviderSimple</span><span class="sxs-lookup"><span data-stu-id="2ef6b-115">Obtaining the IRawElementProviderSimple Interface</span></span>

<span data-ttu-id="2ef6b-116">Si un client dispose d’une interface [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) , il peut utiliser QueryInterface pour accéder à l’interface [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) , comme le montre l’exemple suivant.</span><span class="sxs-lookup"><span data-stu-id="2ef6b-116">If a client has an [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) interface, it can use QueryInterface to get to the [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) interface, as the following example shows.</span></span>


```C++
HRESULT GetIRawElementProviderFromIAccessible(IAccessible * pAcc, long idChild,
                                                 IRawElementProviderSimple ** ppEl)
{
    * ppEl = NULL;

    // First, get the IAccessibleEx for the IAccessible and child ID pair.
    IAccessibleEx * paex;
    HRESULT hr = GetIAccessibleExFromIAccessible( pAcc, idChild, &paex );
    if(FAILED(hr))
        return hr;

    // Next, use QueryInterface.
    hr = paex->QueryInterface(__uuidof(IRawElementProviderSimple), (void **)ppEl);
    paex->Release();
    return hr;
}
```



### <a name="retrieving-control-patterns"></a><span data-ttu-id="2ef6b-117">Récupération des modèles de contrôle</span><span class="sxs-lookup"><span data-stu-id="2ef6b-117">Retrieving Control Patterns</span></span>

<span data-ttu-id="2ef6b-118">Si un client a accès à l’interface [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) , il peut récupérer des interfaces de modèle de contrôle qui ont été implémentées par les fournisseurs et peut ensuite appeler des méthodes sur ces interfaces.</span><span class="sxs-lookup"><span data-stu-id="2ef6b-118">If a client has access to the [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) interface, it can retrieve control pattern interfaces that have been implemented by providers, and can then call methods on those interfaces.</span></span> <span data-ttu-id="2ef6b-119">L’exemple suivant vous montre comment procéder.</span><span class="sxs-lookup"><span data-stu-id="2ef6b-119">The following example shows how to do this.</span></span>


```C++
// Helper function to get a pattern interface from an IAccessible and child ID 
// pair. Gets the IAccessibleEx, then calls GetPatternObject and QueryInterface.
HRESULT GetPatternFromIAccessible(IAccessible * pAcc, long idChild,
                                     PATTERNID patternId, REFIID iid, void ** ppv)
{
    // First, get the IAccesibleEx for this IAccessible and child ID pair.
    IRawElementProviderSimple * pel;
    HRESULT hr = GetIRawElementProviderSimpleFromIAccessible(pAcc, idChild, &pel);
    if(FAILED(hr))
        return hr;
    if(pel == NULL)
        return E_NOINTERFACE;

    // Now get the pattern object.
    IUnknown * pPatternObject = NULL;
    hr = pel->GetPatternProvider(patternId, &pPatternObject);
    pel->Release();
    if(FAILED(hr))
        return hr;
    if(pPatternObject == NULL)
        return E_NOINTERFACE;

    // Finally, use QueryInterface to get the correct interface type.
    hr = pPatternObject->QueryInterface(iid, ppv);
    pPatternObject->Release();
    if(*ppv == NULL)
        return E_NOINTERFACE;
    return hr;
}

HRESULT CallInvokePatternMethod(IAccessible * pAcc, long idChild)
{
    IInvokeProvider * pPattern;
    HRESULT hr = GetPatternFromIAccessible(pAcc, varChild,
                                  UIA_InvokePatternId, __uuidof(IInvokeProvider),
                                  (void **)&pPattern);
    if(FAILED(hr))
        return hr;

    hr = pPattern->Invoke();
    pPattern->Release();
    return hr;
}
```



### <a name="retrieving-property-values"></a><span data-ttu-id="2ef6b-120">Récupération de valeurs de propriété</span><span class="sxs-lookup"><span data-stu-id="2ef6b-120">Retrieving Property Values</span></span>

<span data-ttu-id="2ef6b-121">Si un client a accès à [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple), il peut récupérer des valeurs de propriété.</span><span class="sxs-lookup"><span data-stu-id="2ef6b-121">If a client has access to [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple), it can retrieve property values.</span></span> <span data-ttu-id="2ef6b-122">L’exemple suivant montre comment obtenir des valeurs pour les propriétés d’automatisation de l’interface utilisateur de Microsoft, AutomationId et LabeledBy.</span><span class="sxs-lookup"><span data-stu-id="2ef6b-122">The following example shows how to get values for the AutomationId and LabeledBy Microsoft UI Automation properties.</span></span>


```C++
#include <initguid.h>
#include <uiautomationcoreapi.h> // Includes the UI Automation property GUID definitions.
#include <uiautomationcoreids.h> // Includes definitions of pattern/property IDs.

// Assume we already have a IRawElementProviderSimple * pEl.

VARIANT varValue;

// Get AutomationId property:
varValue.vt = VT_EMPTY;
HRESULT hr = pEl->GetPropertyValue(UIA_AutomationIdPropertyId, &varValue);
if(SUCCEEDED(hr))
{
    if(varValue.vt == VT_BSTR)
    {
        // AutomationId is varValue.bstrVal.
    }
    VariantClear(&varValue);
}


// Get LabeledBy property:
varValue.vt = VT_EMPTY;
hr = pEl->GetPropertyValue(UIA_LabeledByPropertyId, &varValue);
if(SUCCEEDED(hr))
{
    if(varValue.vt == VT_UNKNOWN || varValue.punkVal != NULL)
    {
        // Use QueryInterface to get IRawElementProviderSimple.
        IRawElementProviderSimple * pElLabel = NULL;
        hr = varValue.punkVal->QueryInterface(__uuidof(IRawElementProviderSimple),
                                              (void**)& pElLabel);
        if (SUCCEEDED(hr))
        {
            if(pElLabel != NULL)
            {
            // Use the pElLabel pointer here.
            pElLabel ->Release();
            }
        }
    }
    VariantClear(&varValue);
}
```



<span data-ttu-id="2ef6b-123">L’exemple précédent s’applique aux propriétés qui ne sont pas associées à un modèle de contrôle.</span><span class="sxs-lookup"><span data-stu-id="2ef6b-123">The preceding example applies to properties that are not associated with a control pattern.</span></span> <span data-ttu-id="2ef6b-124">Pour accéder aux propriétés du modèle de contrôle, un client doit obtenir et utiliser une interface de modèle de contrôle.</span><span class="sxs-lookup"><span data-stu-id="2ef6b-124">To access control pattern properties, a client must obtain and use a control pattern interface.</span></span>

### <a name="retrieving-an-iaccessible-interface-from-an-irawelementprovidersimple-interface"></a><span data-ttu-id="2ef6b-125">Récupération d’une interface IAccessible à partir d’une interface IRawElementProviderSimple</span><span class="sxs-lookup"><span data-stu-id="2ef6b-125">Retrieving an IAccessible Interface from an IRawElementProviderSimple Interface</span></span>

<span data-ttu-id="2ef6b-126">Si un client obtient l’interface [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) pour un élément d’interface utilisateur, le client peut utiliser cette interface pour obtenir une interface [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) correspondante pour l’élément.</span><span class="sxs-lookup"><span data-stu-id="2ef6b-126">If a client obtains the [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) interface for a UI element, the client can use that interface to obtain a corresponding [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface for the element.</span></span> <span data-ttu-id="2ef6b-127">Cela est utile si le client doit accéder aux propriétés de Active Accessibility Microsoft pour l’élément.</span><span class="sxs-lookup"><span data-stu-id="2ef6b-127">This is useful if the client needs to access the Microsoft Active Accessibility properties for the element.</span></span>

<span data-ttu-id="2ef6b-128">Un client peut obtenir l’interface [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) en tant que valeur de propriété (par exemple, en appelant [**IRawElementProviderSimple :: GetPropertyValue**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementprovidersimple-getpropertyvalue) avec UIA \_ LabeledByPropertyId) ou en tant qu’élément récupéré par une méthode (par exemple, en appelant [**ISelectionProvider :: GetSelection**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionprovider-getselection) pour récupérer un tableau d’interfaces **IRawElementProviderSimple** d’éléments sélectionnés).</span><span class="sxs-lookup"><span data-stu-id="2ef6b-128">A client can obtain the [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) interface as a property value (for example, by calling [**IRawElementProviderSimple::GetPropertyValue**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementprovidersimple-getpropertyvalue) with UIA\_LabeledByPropertyId), or as an item retrieved by a method (for example, by calling [**ISelectionProvider::GetSelection**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionprovider-getselection) to retrieve an array of **IRawElementProviderSimple** interfaces of selected elements).</span></span> <span data-ttu-id="2ef6b-129">Après avoir obtenu l’interface **IRawElementProviderSimple** , un client peut l’utiliser pour obtenir un [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) correspondant en procédant comme suit :</span><span class="sxs-lookup"><span data-stu-id="2ef6b-129">After obtaining the **IRawElementProviderSimple** interface, a client can use it to obtain a corresponding [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) by following these steps:</span></span>

-   <span data-ttu-id="2ef6b-130">Essayez d’utiliser QueryInterface pour accéder à l’interface [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) .</span><span class="sxs-lookup"><span data-stu-id="2ef6b-130">Attempt to use QueryInterface to get the [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) interface.</span></span>
-   <span data-ttu-id="2ef6b-131">Si QueryInterface échoue, appelez [**IAccessibleEx :: ConvertReturnedElement**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iaccessibleex-convertreturnedelement) sur l’instance [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) à partir de laquelle la propriété a été obtenue à l’origine.</span><span class="sxs-lookup"><span data-stu-id="2ef6b-131">If QueryInterface fails, call [**IAccessibleEx::ConvertReturnedElement**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iaccessibleex-convertreturnedelement) on the [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) instance from which the property was originally obtained.</span></span>
-   <span data-ttu-id="2ef6b-132">Appelez la méthode [**GetIAccessiblePair**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iaccessibleex-getiaccessiblepair) sur la nouvelle instance [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) pour obtenir un INTERFAE [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) et un ID enfant.</span><span class="sxs-lookup"><span data-stu-id="2ef6b-132">Call the [**GetIAccessiblePair**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iaccessibleex-getiaccessiblepair) method on the new [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) instance to obtain an [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interfae and child ID.</span></span>

<span data-ttu-id="2ef6b-133">L’extrait de code suivant montre comment obtenir l’interface [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) à partir d’une interface [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) précédemment obtenue.</span><span class="sxs-lookup"><span data-stu-id="2ef6b-133">The following code snippet demonstrates how to obtain the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface from a previously-obtained [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) interface.</span></span>


```C++
// IRawElementProviderSimple * pVal - an element returned by a property or method
// from another IRawElementProviderSimple.

IAccessible * pAcc = NULL;
long idChild;

// First, try to use QueryInterface to get the IAccessibleEx interface.
IAccessibleEx * pAccEx;
HRESULT hr = pVal->QueryInterface(__uuidof(IAccessibleEx), (void**)&pAccEx);
if (SUCCEEDED(hr)
{
    if (!pAccEx)
    {
        // If QueryInterface fails, and the IRawElementProviderSimple was 
              // obtained as a property or return value from another 
              // IRawElementProviderSimple, pass it to the 
              // IAccessibleEx::ConvertReturnedValue method of the
        // originating element.

        pAccExOrig->ConvertReturnedElement(pVal, &pAccEx);
    }

    if (pAccEx)
    {
        // Call GetIAccessiblePair to get an IAccessible interface and 
              // child ID.
        pAccEx->GetIAccessiblePair(&pAcc, &idChild);
    }

    // Finally, use the IAccessible interface and child ID.
    if (pAcc)
    {
        // Use IAccessible methods to get further information about this UI
              // element, or pass it to existing code that works in terms of 
              // IAccessible.
        ...
    }
}    
```



 

 