---
title: Comment retourner des propriétés à partir d’un fournisseur UI Automation
description: Cette rubrique contient un exemple de code qui montre comment un fournisseur UI Automation Microsoft retourne les propriétés d’un élément d’interface utilisateur aux applications clientes.
ms.assetid: 6932de16-5548-4aa3-9f29-5daa57bb202b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4133a53df3c59e6d5c93b1c9cd8e6aa942b4bd56
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104382013"
---
# <a name="how-to-return-properties-from-a-ui-automation-provider"></a>Comment retourner des propriétés à partir d’un fournisseur UI Automation

Cette rubrique contient un exemple de code qui montre comment un fournisseur UI Automation Microsoft retourne les propriétés d’un élément d’interface utilisateur aux applications clientes.

Pour récupérer une valeur de propriété du fournisseur, UI Automation appelle l’implémentation d’un fournisseur de la méthode [**IRawElementProviderSimple :: GetPropertyValue**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementprovidersimple-getpropertyvalue) , en passant l’ID de la propriété à récupérer et un pointeur vers une structure [**Variant**](/windows/win32/api/oaidl/ns-oaidl-variant) . Si le fournisseur prend en charge la propriété spécifiée, il copie le type de données et la valeur de la propriété dans la structure **Variant** . Si la propriété n’est pas prise en charge, le fournisseur définit le membre **VT** de la structure **Variant** sur VT \_ vide.


```C++
IFACEMETHODIMP Provider::GetPropertyValue(PROPERTYID propertyId, VARIANT* pRetVal)
{
    // The Name property is typically the same as the Caption property of the 
    // control window, if it has one. Here, the Name is overridden for the 
    // sake of illustration. 
    if (propertyId == UIA_NamePropertyId) 
    {
        pRetVal->vt = VT_BSTR;
        pRetVal->bstrVal = SysAllocString(L"Custom button");
    }
    
    else if (propertyId == UIA_ControlTypePropertyId) 
    {
        pRetVal->vt = VT_I4;
        pRetVal->lVal = UIA_ButtonControlTypeId; 
    }

    else if (propertyId == UIA_IsContentElementPropertyId) 
    {
        pRetVal->vt = VT_BOOL;
        pRetVal->lVal = TRUE; 
    }

    else if (propertyId == UIA_IsControlElementPropertyId) 
    {
        pRetVal->vt = VT_BOOL;
        pRetVal->lVal = TRUE; 
    }

    //
    // Return other properties as appropriate for the control type. 
    //

    else
    {
        pRetVal->vt = VT_EMPTY;
        // UI Automation will attempt to get the property from the  
        // provider for window that hosts the control.
    }
    return S_OK;
}
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

**Méthodologique**
</dt> <dt>

[Vue d'ensemble des propriétés UI Automation](uiauto-propertiesoverview.md)
</dt> <dt>

[Rubriques de procédures pour les fournisseurs UI Automation](uiauto-howto-topics-for-uiautomation-providers.md)
</dt> </dl>

 

 