---
title: Comment activer la navigation dans un fournisseur de fragment UI Automation
description: Cette rubrique contient un exemple de code qui montre comment activer la navigation dans un fournisseur UI Automation Microsoft pour un élément dans un fragment.
ms.assetid: 8c390e19-3c17-4e02-ade8-cd5c1ed9E938
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58495c48f6f355e7cc2a42b58ac0e32f88958361
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127010512"
---
# <a name="how-to-enable-navigation-in-a-ui-automation-fragment-provider"></a>Comment activer la navigation dans un fournisseur de fragment UI Automation

Cette rubrique contient un exemple de code qui montre comment activer la navigation dans un fournisseur UI Automation Microsoft pour un élément dans un fragment.

L’exemple de code suivant implémente la méthode [**IRawElementProviderFragment :: Navigate**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementproviderfragment-navigate) pour un élément de liste dans un contrôle de liste personnalisé. L’élément parent est le contrôle de liste personnalisé, et les éléments frères sont d’autres éléments de la liste. La méthode définit le paramètre *pRetVal* sur la **valeur null** s’il n’y a aucun élément dans la direction spécifiée.


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



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

**Conceptuel**
</dt> <dt>

[Implémentation d’un fournisseur UI Automation Server-Side](uiauto-serversideprovider.md)
</dt> <dt>

[Rubriques de procédures pour les fournisseurs UI Automation](uiauto-howto-topics-for-uiautomation-providers.md)
</dt> </dl>

 

 




