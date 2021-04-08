---
title: Guide pratique pour parcourir l’arborescence UI Automation
description: Cette rubrique contient un exemple de code qui montre comment utiliser l’interface IUIAutomationTreeWalker pour parcourir et examiner les éléments de l’arborescence Microsoft UI Automation.
ms.assetid: 41ca783d-56d1-4ad5-8f07-c265ff2e07bd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ed5c6c1bec961d4f0df83687cd19eecba6ed179
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103839877"
---
# <a name="how-to-walk-the-ui-automation-tree"></a><span data-ttu-id="b41e0-103">Guide pratique pour parcourir l’arborescence UI Automation</span><span class="sxs-lookup"><span data-stu-id="b41e0-103">How to Walk the UI Automation Tree</span></span>

<span data-ttu-id="b41e0-104">Cette rubrique contient un exemple de code qui montre comment utiliser l’interface [**IUIAutomationTreeWalker**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtreewalker) pour parcourir et examiner les éléments de l’arborescence Microsoft UI Automation.</span><span class="sxs-lookup"><span data-stu-id="b41e0-104">This topic contains example code that shows how to use the [**IUIAutomationTreeWalker**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtreewalker) interface to walk through and examine the elements in the Microsoft UI Automation tree.</span></span> <span data-ttu-id="b41e0-105">Il aborde les sujets suivants :</span><span class="sxs-lookup"><span data-stu-id="b41e0-105">It discusses the following topics:</span></span>

-   [<span data-ttu-id="b41e0-106">Parcourir les descendants d’un élément</span><span class="sxs-lookup"><span data-stu-id="b41e0-106">Walking through Descendants of an Element</span></span>](#walking-through-descendants-of-an-element)
-   [<span data-ttu-id="b41e0-107">Parcourir les éléments ancêtres</span><span class="sxs-lookup"><span data-stu-id="b41e0-107">Walking through Ancestor Elements</span></span>](#walking-through-ancestor-elements)
-   [<span data-ttu-id="b41e0-108">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="b41e0-108">Related topics</span></span>](#related-topics)

## <a name="walking-through-descendants-of-an-element"></a><span data-ttu-id="b41e0-109">Parcourir les descendants d’un élément</span><span class="sxs-lookup"><span data-stu-id="b41e0-109">Walking through Descendants of an Element</span></span>

<span data-ttu-id="b41e0-110">L’exemple de code suivant est une fonction récursive qui parcourt tous les descendants d’un élément d’interface utilisateur et affiche leurs types de contrôle dans une liste hiérarchique.</span><span class="sxs-lookup"><span data-stu-id="b41e0-110">The following code example is a recursive function that walks through all the descendants of a UI element and displays their control types in a hierarchical list.</span></span>


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



## <a name="walking-through-ancestor-elements"></a><span data-ttu-id="b41e0-111">Parcourir les éléments ancêtres</span><span class="sxs-lookup"><span data-stu-id="b41e0-111">Walking through Ancestor Elements</span></span>

<span data-ttu-id="b41e0-112">L’exemple de code suivant est une fonction qui parcourt les ancêtres d’un élément pour identifier l’élément parent.</span><span class="sxs-lookup"><span data-stu-id="b41e0-112">The following code example is a function that walks through the ancestors of a element to identify the parent element.</span></span> <span data-ttu-id="b41e0-113">Cela est utile lorsque vous devez identifier la fenêtre parente d’un contrôle.</span><span class="sxs-lookup"><span data-stu-id="b41e0-113">This is useful when you need to identify the parent window of a control.</span></span> <span data-ttu-id="b41e0-114">La fonction retourne la **valeur null** pour les éléments de niveau supérieur ; autrement dit, les éléments dont le parent est le bureau.</span><span class="sxs-lookup"><span data-stu-id="b41e0-114">The function returns **NULL** for top-level elements; that is, elements whose parent is the desktop.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="b41e0-115">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="b41e0-115">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="b41e0-116">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="b41e0-116">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="b41e0-117">Obtention d'éléments UI Automation</span><span class="sxs-lookup"><span data-stu-id="b41e0-117">Obtaining UI Automation Elements</span></span>](uiauto-obtainingelements.md)
</dt> <dt>

[<span data-ttu-id="b41e0-118">Rubriques de procédures pour les clients UI Automation</span><span class="sxs-lookup"><span data-stu-id="b41e0-118">How-To Topics for UI Automation Clients</span></span>](uiauto-howto-topics-for-uiautomation-clients.md)
</dt> </dl>

 

 




