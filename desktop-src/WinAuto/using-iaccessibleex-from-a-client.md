---
title: Utilisation de IAccessibleEx à partir d’un client
description: Cette rubrique explique comment les clients accèdent à l’implémentation IAccessibleEx d’un serveur et l’utilisent pour obtenir des propriétés UI Automation et des modèles de contrôle pour les éléments d’interface utilisateur.
ms.assetid: e057bbe8-5dd7-41fc-a5d5-bcf4c1c6433d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f03bd58ec80a29f13e0428de4655aa7200144122b1a1889259844db078aa9dc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120098099"
---
# <a name="using-iaccessibleex-from-a-client"></a>Utilisation de IAccessibleEx à partir d’un client

Cette rubrique explique comment les clients accèdent à l’implémentation [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) d’un serveur et l’utilisent pour obtenir des propriétés UI Automation et des modèles de contrôle pour les éléments d’interface utilisateur.

Les procédures et les exemples de cette section supposent qu’un client [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) est déjà en cours de traitement et qu’un serveur Microsoft Active Accessibility Server existant. Ils supposent également que le client a déjà obtenu un objet **IAccessible** à l’aide de l’une des fonctions de l’infrastructure d’accessibilité, telles que [**AccessibleObjectFromEvent**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromevent), [**AccessibleObjectFromPoint**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfrompoint)ou [**AccessibleObjectFromWindow**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow).

### <a name="obtaining-an-iaccessibleex-interface-from-the-iaccessible-interface"></a>Obtention d’une interface IAccessibleEx à partir de l’interface IAccessible

Un client qui a une interface [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) pour un objet accessible peut l’utiliser pour obtenir l’interface [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) correspondante en procédant comme suit :

-   Appelez [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) sur l’objet [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) d’origine avec un IID de \_ \_ uuidof (IServiceProvider).
-   Appelez **IServiceProvider :: QueryService** pour accéder au [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex).

### <a name="handling-the-child-id"></a>Gestion de l’ID enfant

Les clients doivent être préparés pour les serveurs ayant un ID enfant autre que CHILDID \_ self. Après avoir obtenu une interface [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) à partir d’un [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible), les clients doivent appeler [**IAccessibleEx :: GetObjectForChild**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iaccessibleex-getobjectforchild) si l’ID enfant n’est pas CHILDID \_ Self (indiquant un objet parent).

L’exemple suivant montre comment obtenir un [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) pour un objet [**IACCESSIBLE**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) et un ID enfant particuliers.


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



### <a name="obtaining-the-irawelementprovidersimple-interface"></a>Obtention de l’interface IRawElementProviderSimple

Si un client dispose d’une interface [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) , il peut utiliser QueryInterface pour accéder à l’interface [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) , comme le montre l’exemple suivant.


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



### <a name="retrieving-control-patterns"></a>Récupération des modèles de contrôle

Si un client a accès à l’interface [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) , il peut récupérer des interfaces de modèle de contrôle qui ont été implémentées par les fournisseurs et peut ensuite appeler des méthodes sur ces interfaces. L’exemple suivant vous montre comment procéder.


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



### <a name="retrieving-property-values"></a>Récupération de valeurs de propriété

Si un client a accès à [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple), il peut récupérer des valeurs de propriété. L’exemple suivant montre comment obtenir des valeurs pour les propriétés d’automatisation de l’interface utilisateur de Microsoft, AutomationId et LabeledBy.


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



L’exemple précédent s’applique aux propriétés qui ne sont pas associées à un modèle de contrôle. Pour accéder aux propriétés du modèle de contrôle, un client doit obtenir et utiliser une interface de modèle de contrôle.

### <a name="retrieving-an-iaccessible-interface-from-an-irawelementprovidersimple-interface"></a>Récupération d’une interface IAccessible à partir d’une interface IRawElementProviderSimple

Si un client obtient l’interface [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) pour un élément d’interface utilisateur, le client peut utiliser cette interface pour obtenir une interface [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) correspondante pour l’élément. Cela est utile si le client doit accéder aux propriétés de Active Accessibility Microsoft pour l’élément.

Un client peut obtenir l’interface [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) en tant que valeur de propriété (par exemple, en appelant [**IRawElementProviderSimple :: GetPropertyValue**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementprovidersimple-getpropertyvalue) avec UIA \_ LabeledByPropertyId) ou en tant qu’élément récupéré par une méthode (par exemple, en appelant [**ISelectionProvider :: GetSelection**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionprovider-getselection) pour récupérer un tableau d’interfaces **IRawElementProviderSimple** d’éléments sélectionnés). Après avoir obtenu l’interface **IRawElementProviderSimple** , un client peut l’utiliser pour obtenir un [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) correspondant en procédant comme suit :

-   Essayez d’utiliser QueryInterface pour accéder à l’interface [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) .
-   Si QueryInterface échoue, appelez [**IAccessibleEx :: ConvertReturnedElement**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iaccessibleex-convertreturnedelement) sur l’instance [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) à partir de laquelle la propriété a été obtenue à l’origine.
-   Appelez la méthode [**GetIAccessiblePair**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iaccessibleex-getiaccessiblepair) sur la nouvelle instance [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) pour obtenir un INTERFAE [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) et un ID enfant.

L’extrait de code suivant montre comment obtenir l’interface [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) à partir d’une interface [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) précédemment obtenue.


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



 

 