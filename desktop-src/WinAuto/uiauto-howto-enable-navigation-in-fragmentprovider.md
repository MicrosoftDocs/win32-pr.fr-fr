---
title: Comment activer la navigation dans un fournisseur de fragment UI Automation
description: Cette rubrique contient un exemple de code qui montre comment activer la navigation dans un fournisseur UI Automation Microsoft pour un élément dans un fragment.
ms.assetid: 8c390e19-3c17-4e02-ade8-cd5c1ed9E938
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58495c48f6f355e7cc2a42b58ac0e32f88958361
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104028685"
---
# <a name="how-to-enable-navigation-in-a-ui-automation-fragment-provider"></a><span data-ttu-id="d1c6d-103">Comment activer la navigation dans un fournisseur de fragment UI Automation</span><span class="sxs-lookup"><span data-stu-id="d1c6d-103">How to Enable Navigation in a UI Automation Fragment Provider</span></span>

<span data-ttu-id="d1c6d-104">Cette rubrique contient un exemple de code qui montre comment activer la navigation dans un fournisseur UI Automation Microsoft pour un élément dans un fragment.</span><span class="sxs-lookup"><span data-stu-id="d1c6d-104">This topic contains example code that shows how to enable navigation in a Microsoft UI Automation provider for an element in a fragment.</span></span>

<span data-ttu-id="d1c6d-105">L’exemple de code suivant implémente la méthode [**IRawElementProviderFragment :: Navigate**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementproviderfragment-navigate) pour un élément de liste dans un contrôle de liste personnalisé.</span><span class="sxs-lookup"><span data-stu-id="d1c6d-105">The following example code implements the [**IRawElementProviderFragment::Navigate**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementproviderfragment-navigate) method for a list item in a custom list control.</span></span> <span data-ttu-id="d1c6d-106">L’élément parent est le contrôle de liste personnalisé, et les éléments frères sont d’autres éléments de la liste.</span><span class="sxs-lookup"><span data-stu-id="d1c6d-106">The parent element is the custom list control, and the sibling elements are other items in the list.</span></span> <span data-ttu-id="d1c6d-107">La méthode définit le paramètre *pRetVal* sur la **valeur null** s’il n’y a aucun élément dans la direction spécifiée.</span><span class="sxs-lookup"><span data-stu-id="d1c6d-107">The method sets the *pRetVal* parameter to **NULL** if there is no element in the specified direction.</span></span>


```C++
// Implementation of IRawElementProviderFragment::Navigate.
// Enables UI Automation to locate the element in the tree.
HRESULT STDMETHODCALLTYPE ListItemProvider::Navigate(NavigateDirection direction, IRawElementProviderFragment ** pRetVal)
{
    if (pRetVal == NULL) 
    {
        return E_INVALIDARG;
    }

    IRawElementProviderFragment* pFrag = NULL;
    switch(direction)
    {
        case NavigateDirection_Parent:
            pFrag = (IRawElementProviderFragment*) m_parentProvider;       
            break;

        case NavigateDirection_NextSibling:
            pFrag = (IRawElementProviderFragment*) m_nextSiblingProvider;
            break;

        case NavigateDirection_PreviousSibling:  
            pFrag = (IRawElementProviderFragment*) m_previousSiblingProvider;
            break;
    }
    *pRetVal = pFrag;
    if (pFrag != NULL) 
    {
        pFrag->AddRef();
    }
    return S_OK;
}              
```



## <a name="related-topics"></a><span data-ttu-id="d1c6d-108">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="d1c6d-108">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="d1c6d-109">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="d1c6d-109">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="d1c6d-110">Implémentation d’un fournisseur UI Automation Server-Side</span><span class="sxs-lookup"><span data-stu-id="d1c6d-110">Implementing a Server-Side UI Automation Provider</span></span>](uiauto-serversideprovider.md)
</dt> <dt>

[<span data-ttu-id="d1c6d-111">Rubriques de procédures pour les fournisseurs UI Automation</span><span class="sxs-lookup"><span data-stu-id="d1c6d-111">How-To Topics for UI Automation Providers</span></span>](uiauto-howto-topics-for-uiautomation-providers.md)
</dt> </dl>

 

 




