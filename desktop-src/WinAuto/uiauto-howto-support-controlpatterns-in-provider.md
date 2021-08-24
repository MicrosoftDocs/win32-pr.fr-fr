---
title: Prendre en charge des modèles de contrôle dans un fournisseur UI Automation
description: Cette rubrique montre comment un fournisseur UI Automation Microsoft implémente des modèles de contrôle pour un contrôle. Les modèles de contrôle permettent aux applications clientes de manipuler le contrôle et d’obtenir des informations à son sujet.
ms.assetid: 504d0ed8-32c1-43ed-9f71-328a013ab350
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 649f9419c5e3003c0185f435cba4d38f4a25c3d7adc1bdc7cf9c53cd06b32a6e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119759229"
---
# <a name="support-control-patterns-in-a-ui-automation-provider"></a>Prendre en charge des modèles de contrôle dans un fournisseur UI Automation

Cette rubrique montre comment un fournisseur UI Automation Microsoft implémente des modèles de contrôle pour un contrôle. Les modèles de contrôle permettent aux applications clientes de manipuler le contrôle et d’obtenir des informations à son sujet.

Un fournisseur implémente un modèle de contrôle en suivant les étapes principales suivantes :

1.  Implémentez l’interface du fournisseur qui prend en charge le modèle de contrôle. Par exemple, pour prendre en charge le modèle de contrôle [Selection](uiauto-implementingselection.md) , un fournisseur pour un contrôle de liste personnalisé implémente l’interface [**ISelectionProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider) .
2.  Retourne un objet qui contient l’interface du fournisseur de modèle de contrôle lorsque UI Automation appelle la méthode [**IRawElementProviderSimple :: GetPatternProvider**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementprovidersimple-getpatternprovider) du fournisseur.

L’exemple suivant illustre l’implémentation de l’interface [**ISelectionProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider) pour un contrôle de liste à sélection unique personnalisé. L’implémentation de comprend des méthodes de récupération de propriété pour les propriétés IsSelectionRequired et CanSelectMultiple, ainsi qu’une méthode permettant de récupérer le fournisseur pour l’élément de liste sélectionné.


```C++
// Specifies whether the list control supports the selection of
// multiple items at the same time.
IFACEMETHODIMP ListProvider::get_CanSelectMultiple(BOOL *pRetVal)
{
    *pRetVal = FALSE;
    return S_OK;
} 

// Specifies whether the list must have an item selected at all times.
IFACEMETHODIMP ListProvider::get_IsSelectionRequired(BOOL *pRetVal)
{
   *pRetVal = TRUE;
   return S_OK;
}

// Retrieves the provider of the selected item in a custom list control. 
//
// m_pControl - pointer to an application-defined object for managing
//   the custom list control. 
//
// ListItemProvider - application-defined class that inherits the 
//   IRawElementProviderSimple interface.
//
// GetItemProviderByIndex - application-defined method that retrieves the 
//   IRawElementProviderSimple interface of the selected item.
IFACEMETHODIMP ListProvider::GetSelection(SAFEARRAY** pRetVal)
{
    // Create a safe array to store the IRawElementProviderSimple pointer.
    SAFEARRAY *psa = SafeArrayCreateVector(VT_UNKNOWN, 0, 1);

    // Retrieve the index of the selected list item. 
    int index = m_pControl->GetSelectedIndex(); 

    // Retrieve the IRawElementProviderSimple pointer of the selected list
    // item. ListItemProvider is an application-defined class that 
    // inherits the IRawElementProviderSimple interface. 
    ListItemProvider* pItem = GetItemProviderByIndex(index); 
    if (pItem != NULL)
    {
        LONG i = 0;
        SafeArrayPutElement(psa, &i, pItem);
    }
    *pRetVal = psa;
    return S_OK;
}
```



L’exemple suivant illustre une implémentation de [**IRawElementProviderSimple :: GetPatternProvider**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementprovidersimple-getpatternprovider) qui retourne un objet qui implémente [**ISelectionProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider). La plupart des contrôles de liste prennent également en charge d’autres modèles, mais cet exemple retourne une référence null pour tous les autres identificateurs de modèle de contrôle.


```C++
// Retrieves an object that supports the control pattern provider interface 
// for the specified control pattern. 
IFACEMETHODIMP ListProvider::GetPatternProvider(PATTERNID patternId, IUnknown** pRetVal)
{
    *pRetVal = NULL;
    if (patternId == UIA_SelectionPatternId) 
    {
        // Return the object that implements ISelectionProvider. In this example, 
        // ISelectionProvider is implemented in the current object (this).
        *pRetVal = static_cast<IRawElementProviderSimple*>(this);
        AddRef();  
    }
    return S_OK;
}
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

**Méthodologique**
</dt> <dt>

[Vue d'ensemble des modèles de contrôle UI Automation](uiauto-controlpatternsoverview.md)
</dt> <dt>

[Rubriques de procédures pour les fournisseurs UI Automation](uiauto-howto-topics-for-uiautomation-providers.md)
</dt> </dl>

 

 




