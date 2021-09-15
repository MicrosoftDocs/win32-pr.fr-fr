---
title: Guide pratique pour parcourir l’arborescence UI Automation
description: Cette rubrique contient un exemple de code qui montre comment utiliser l’interface IUIAutomationTreeWalker pour parcourir et examiner les éléments de l’arborescence Microsoft UI Automation.
ms.assetid: 41ca783d-56d1-4ad5-8f07-c265ff2e07bd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ed5c6c1bec961d4f0df83687cd19eecba6ed179
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127518105"
---
# <a name="how-to-walk-the-ui-automation-tree"></a>Guide pratique pour parcourir l’arborescence UI Automation

Cette rubrique contient un exemple de code qui montre comment utiliser l’interface [**IUIAutomationTreeWalker**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtreewalker) pour parcourir et examiner les éléments de l’arborescence Microsoft UI Automation. Il aborde les sujets suivants :

-   [Parcourir les descendants d’un élément](#walking-through-descendants-of-an-element)
-   [Parcourir les éléments ancêtres](#walking-through-ancestor-elements)
-   [Rubriques connexes](#related-topics)

## <a name="walking-through-descendants-of-an-element"></a>Parcourir les descendants d’un élément

L’exemple de code suivant est une fonction récursive qui parcourt tous les descendants d’un élément d’interface utilisateur et affiche leurs types de contrôle dans une liste hiérarchique.


```C++
// CAUTION: Do not pass in the root (desktop) element. Traversing the entire subtree
// of the desktop could take a very long time and even lead to a stack overflow.
void ListDescendants(IUIAutomationElement* pParent, int indent)
{
    if (pParent == NULL)
        return;

    IUIAutomationTreeWalker* pControlWalker = NULL;
    IUIAutomationElement* pNode = NULL;

    g_pAutomation->get_ControlViewWalker(&pControlWalker);
    if (pControlWalker == NULL)
        goto cleanup;

    pControlWalker->GetFirstChildElement(pParent, &pNode);
    if (pNode == NULL)
        goto cleanup;

    while (pNode)
    {
        BSTR desc;
        pNode->get_CurrentLocalizedControlType(&desc);
        for (int x = 0; x <= indent; x++)
        {
            std::wcout << L"   ";
        }
        std::wcout << desc << L"\n";
        SysFreeString(desc);

        ListDescendants(pNode, indent+1);
        IUIAutomationElement* pNext;
        pControlWalker->GetNextSiblingElement(pNode, &pNext);
        pNode->Release();
        pNode = pNext;
    }

cleanup:
    if (pControlWalker != NULL)
        pControlWalker->Release();

    if (pNode != NULL)
        pNode->Release();

    return;
}
```



## <a name="walking-through-ancestor-elements"></a>Parcourir les éléments ancêtres

L’exemple de code suivant est une fonction qui parcourt les ancêtres d’un élément pour identifier l’élément parent. Cela est utile lorsque vous devez identifier la fenêtre parente d’un contrôle. La fonction retourne la **valeur null** pour les éléments de niveau supérieur ; autrement dit, les éléments dont le parent est le bureau.


```C++
IUIAutomationElement* GetContainingWindow(IUIAutomationElement* pChild)
{

    if (pChild == NULL)
        return NULL;

    IUIAutomationElement* pDesktop = NULL;
    HRESULT hr = g_pAutomation->GetRootElement(&pDesktop);
    if (FAILED(hr))
        return NULL;

    BOOL same;
    g_pAutomation->CompareElements(pChild, pDesktop, &same);
    if (same)
    {
        pDesktop->Release();
        return NULL; // No parent, so return NULL.
    }

    IUIAutomationElement* pParent = NULL;
    IUIAutomationElement* pNode = pChild;

    // Create the treewalker.
    IUIAutomationTreeWalker* pWalker = NULL;
    g_pAutomation->get_ControlViewWalker(&pWalker);
    if (pWalker == NULL)
        goto cleanup;

    // Walk up the tree.
    while (TRUE)
    {
        hr = pWalker->GetParentElement(pNode, &pParent);
        if (FAILED(hr) || pParent == NULL)
        {
            break;
        }
        g_pAutomation->CompareElements(pParent, pDesktop, &same);
        if (same)
        {
            pDesktop->Release();
            pParent->Release();
            pWalker->Release();
            // Reached desktop, so return next element below it.
            return pNode;
        }
        if (pNode != pChild) // Do not release the in-param.
            pNode->Release();
        pNode = pParent;
    }

cleanup:
    if ((pNode != NULL) && (pNode != pChild)) 
        pNode->Release();

    if (pDesktop != NULL)
        pDesktop->Release();

    if (pWalker != NULL)
        pWalker->Release();

    if (pParent != NULL)
        pParent->Release();

    return NULL;  
}
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

**Conceptuel**
</dt> <dt>

[Obtention d'éléments UI Automation](uiauto-obtainingelements.md)
</dt> <dt>

[Rubriques de procédures pour les clients UI Automation](uiauto-howto-topics-for-uiautomation-clients.md)
</dt> </dl>

 

 




