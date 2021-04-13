---
title: Prendre en charge des modèles de contrôle dans un fournisseur UI Automation
description: Cette rubrique montre comment un fournisseur UI Automation Microsoft implémente des modèles de contrôle pour un contrôle. Les modèles de contrôle permettent aux applications clientes de manipuler le contrôle et d’obtenir des informations à son sujet.
ms.assetid: 504d0ed8-32c1-43ed-9f71-328a013ab350
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54e75fa12dba891bc4eded5fd9763f7825eb7f88
ms.sourcegitcommit: 2e9db3c7d9a3dbea15196b03c883846fad6f32be
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/12/2019
ms.locfileid: "104313579"
---
# <a name="support-control-patterns-in-a-ui-automation-provider"></a><span data-ttu-id="c5852-104">Prendre en charge des modèles de contrôle dans un fournisseur UI Automation</span><span class="sxs-lookup"><span data-stu-id="c5852-104">Support Control Patterns in a UI Automation Provider</span></span>

<span data-ttu-id="c5852-105">Cette rubrique montre comment un fournisseur UI Automation Microsoft implémente des modèles de contrôle pour un contrôle.</span><span class="sxs-lookup"><span data-stu-id="c5852-105">This topic shows how a Microsoft UI Automation provider implements control patterns for a control.</span></span> <span data-ttu-id="c5852-106">Les modèles de contrôle permettent aux applications clientes de manipuler le contrôle et d’obtenir des informations à son sujet.</span><span class="sxs-lookup"><span data-stu-id="c5852-106">Control patterns enable client applications to manipulate the control and get information about it.</span></span>

<span data-ttu-id="c5852-107">Un fournisseur implémente un modèle de contrôle en suivant les étapes principales suivantes :</span><span class="sxs-lookup"><span data-stu-id="c5852-107">A provider implements a control pattern by following these main steps:</span></span>

1.  <span data-ttu-id="c5852-108">Implémentez l’interface du fournisseur qui prend en charge le modèle de contrôle.</span><span class="sxs-lookup"><span data-stu-id="c5852-108">Implement the provider interface that supports the control pattern.</span></span> <span data-ttu-id="c5852-109">Par exemple, pour prendre en charge le modèle de contrôle [Selection](uiauto-implementingselection.md) , un fournisseur pour un contrôle de liste personnalisé implémente l’interface [**ISelectionProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider) .</span><span class="sxs-lookup"><span data-stu-id="c5852-109">For example, to support the [Selection](uiauto-implementingselection.md) control pattern, a provider for a custom list control would implement the [**ISelectionProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider) interface.</span></span>
2.  <span data-ttu-id="c5852-110">Retourne un objet qui contient l’interface du fournisseur de modèle de contrôle lorsque UI Automation appelle la méthode [**IRawElementProviderSimple :: GetPatternProvider**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementprovidersimple-getpatternprovider) du fournisseur.</span><span class="sxs-lookup"><span data-stu-id="c5852-110">Return an object that contains the control pattern provider interface when UI Automation calls the provider's [**IRawElementProviderSimple::GetPatternProvider**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementprovidersimple-getpatternprovider) method.</span></span>

<span data-ttu-id="c5852-111">L’exemple suivant illustre l’implémentation de l’interface [**ISelectionProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider) pour un contrôle de liste à sélection unique personnalisé.</span><span class="sxs-lookup"><span data-stu-id="c5852-111">The following example shows the [**ISelectionProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider) interface implementation for a custom, single-selection list control.</span></span> <span data-ttu-id="c5852-112">L’implémentation de comprend des méthodes de récupération de propriété pour les propriétés IsSelectionRequired et CanSelectMultiple, ainsi qu’une méthode permettant de récupérer le fournisseur pour l’élément de liste sélectionné.</span><span class="sxs-lookup"><span data-stu-id="c5852-112">The implementation includes property-retrieval methods for the IsSelectionRequired and CanSelectMultiple properties, and a method for retrieving the provider for the selected list item.</span></span>


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



<span data-ttu-id="c5852-113">L’exemple suivant illustre une implémentation de [**IRawElementProviderSimple :: GetPatternProvider**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementprovidersimple-getpatternprovider) qui retourne un objet qui implémente [**ISelectionProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider).</span><span class="sxs-lookup"><span data-stu-id="c5852-113">The following example shows an implementation of [**IRawElementProviderSimple::GetPatternProvider**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementprovidersimple-getpatternprovider) that returns an object that implements [**ISelectionProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider).</span></span> <span data-ttu-id="c5852-114">La plupart des contrôles de liste prennent également en charge d’autres modèles, mais cet exemple retourne une référence null pour tous les autres identificateurs de modèle de contrôle.</span><span class="sxs-lookup"><span data-stu-id="c5852-114">Most list controls would support other patterns as well, but this example returns a null reference for all other control pattern identifiers.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="c5852-115">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="c5852-115">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="c5852-116">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="c5852-116">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="c5852-117">Vue d'ensemble des modèles de contrôle UI Automation</span><span class="sxs-lookup"><span data-stu-id="c5852-117">UI Automation Control Patterns Overview</span></span>](uiauto-controlpatternsoverview.md)
</dt> <dt>

[<span data-ttu-id="c5852-118">Rubriques de procédures pour les fournisseurs UI Automation</span><span class="sxs-lookup"><span data-stu-id="c5852-118">How-To Topics for UI Automation Providers</span></span>](uiauto-howto-topics-for-uiautomation-providers.md)
</dt> </dl>

 

 




