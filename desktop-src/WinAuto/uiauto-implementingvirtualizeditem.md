---
title: Modèle de contrôle VirtualizedItem
description: Fournit des instructions et des conventions pour l’implémentation de IVirtualizedItemProvider, y compris des informations sur les propriétés et les méthodes.
ms.assetid: 7a95e92f-7ccb-4c9b-8986-1d2de7038e47
keywords:
- UI Automation, implémentation du modèle de contrôle VirtualizedItem
- UI Automation, modèle de contrôle VirtualizedItem
- UI Automation, IVirtualizedItemProvider
- IVirtualizedItemProvider
- implémentation des modèles de contrôle VirtualizedItem d’UI Automation
- Modèles de contrôle VirtualizedItem
- modèles de contrôle, IVirtualizedItemProvider
- modèles de contrôle, implémenter des VirtualizedItem UI Automation
- modèles de contrôle, VirtualizedItem
- interfaces, IVirtualizedItemProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8dac9e34dd9bff5d0ba2d245aa2fb8de621f40a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104197441"
---
# <a name="virtualizeditem-control-pattern"></a><span data-ttu-id="c02da-113">Modèle de contrôle VirtualizedItem</span><span class="sxs-lookup"><span data-stu-id="c02da-113">VirtualizedItem Control Pattern</span></span>

<span data-ttu-id="c02da-114">Fournit des instructions et des conventions pour l’implémentation de [**IVirtualizedItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivirtualizeditemprovider), y compris des informations sur les propriétés et les méthodes.</span><span class="sxs-lookup"><span data-stu-id="c02da-114">Describes guidelines and conventions for implementing [**IVirtualizedItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivirtualizeditemprovider), including information about properties and methods.</span></span> <span data-ttu-id="c02da-115">Le modèle de contrôle **VirtualizedItem** est utilisé pour prendre en charge les éléments virtualisés, qui sont des éléments représentés par des éléments d’automatisation d’espace réservé dans l’arborescence Microsoft UI Automation.</span><span class="sxs-lookup"><span data-stu-id="c02da-115">The **VirtualizedItem** control pattern is used to support virtualized items, which are items that are represented by placeholder automation elements in the Microsoft UI Automation tree.</span></span>

<span data-ttu-id="c02da-116">Les éléments virtualisés peuvent inclure des éléments récupérés à partir d’un contrôle qui prend en charge le modèle de contrôle [ItemContainer](uiauto-implementingitemcontainer.md) , ou un objet incorporé virtualisé récupéré à partir d’un contrôle qui prend en charge le modèle de contrôle [Text](uiauto-implementingtextandtextrange.md) .</span><span class="sxs-lookup"><span data-stu-id="c02da-116">Virtualized items can include items retrieved from a control that supports the [ItemContainer](uiauto-implementingitemcontainer.md) control pattern, or a virtualized embedded object retrieved from a control that supports the [Text](uiauto-implementingtextandtextrange.md) control pattern.</span></span> <span data-ttu-id="c02da-117">L’espace réservé pour un élément virtualisé peut ne pas avoir de données chargées pour toutes les propriétés UI Automation et peut retourner [**UIA \_ E \_ ELEMENTNOTAVAILABLE**](uiauto-error-codes.md) en réponse aux requêtes pour les propriétés qui ne sont pas disponibles.</span><span class="sxs-lookup"><span data-stu-id="c02da-117">The placeholder for a virtualized item might not have loaded data for all UI Automation properties, and may return [**UIA\_E\_ELEMENTNOTAVAILABLE**](uiauto-error-codes.md) in response to queries for properties that are not available.</span></span> <span data-ttu-id="c02da-118">Le modèle de contrôle **VirtualizedItem** fournit une méthode pour la réalisation d’un élément virtuel afin que des informations complètes soient rendues disponibles pour l’élément et qu’un élément Automation complet puisse être créé pour l’élément dans l’arborescence UI Automation.</span><span class="sxs-lookup"><span data-stu-id="c02da-118">The **VirtualizedItem** control pattern provides a method for realizing a virtual item so that full information is made available for the item, and a full automation element can be created for the item in the UI Automation tree.</span></span>

<span data-ttu-id="c02da-119">Cette rubrique contient les sections suivantes.</span><span class="sxs-lookup"><span data-stu-id="c02da-119">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="c02da-120">Conventions et directives d'implémentation</span><span class="sxs-lookup"><span data-stu-id="c02da-120">Implementation Guidelines and Conventions</span></span>](#implementation-guidelines-and-conventions)
-   [<span data-ttu-id="c02da-121">Membres requis pour **IVirtualizedItemProvider**</span><span class="sxs-lookup"><span data-stu-id="c02da-121">Required Members for **IVirtualizedItemProvider**</span></span>](#required-members-for-ivirtualizeditemprovider)
-   [<span data-ttu-id="c02da-122">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="c02da-122">Related topics</span></span>](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a><span data-ttu-id="c02da-123">Conventions et directives d'implémentation</span><span class="sxs-lookup"><span data-stu-id="c02da-123">Implementation Guidelines and Conventions</span></span>

<span data-ttu-id="c02da-124">Lorsque vous implémentez le modèle de contrôle **VirtualizedItem** , notez les conventions et recommandations suivantes :</span><span class="sxs-lookup"><span data-stu-id="c02da-124">When implementing the **VirtualizedItem** control pattern, note the following guidelines and conventions:</span></span>

-   <span data-ttu-id="c02da-125">Tout élément d’espace réservé UI Automation qui peut être virtualisé doit prendre en charge le modèle de contrôle **VirtualizedItem** en exposant l’interface [**IVirtualizedItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivirtualizeditemprovider) .</span><span class="sxs-lookup"><span data-stu-id="c02da-125">Any UI Automation placeholder element that can be virtualized must support the **VirtualizedItem** control pattern by exposing the [**IVirtualizedItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivirtualizeditemprovider) interface.</span></span>
-   <span data-ttu-id="c02da-126">Quand [**IVirtualizedItemProvider ::**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ivirtualizeditemprovider-realize) on l’appelle, l’objet d’espace réservé doit être mis à jour avec des implémentations complètes de ses propriétés et modèles de contrôle.</span><span class="sxs-lookup"><span data-stu-id="c02da-126">When [**IVirtualizedItemProvider::Realize**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ivirtualizeditemprovider-realize) is called, the placeholder object must be updated with full implementations of its properties and control patterns.</span></span>
-   <span data-ttu-id="c02da-127">Quand [**IVirtualizedItemProvider ::**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ivirtualizeditemprovider-realize) on l’appelle, le fournisseur peut modifier la fenêtre d’affichage afin que l’élément virtualisé entre en vue.</span><span class="sxs-lookup"><span data-stu-id="c02da-127">When [**IVirtualizedItemProvider::Realize**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ivirtualizeditemprovider-realize) is called, the provider can change the viewport so that the virtualized item comes into view.</span></span> <span data-ttu-id="c02da-128">La remise de l’élément dans l’affichage n’est pas obligatoire. Toutefois, les éléments non virtualisés hors écran doivent prendre en charge la méthode [**IScrollItemProvider :: ScrollIntoView**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollitemprovider-scrollintoview) .</span><span class="sxs-lookup"><span data-stu-id="c02da-128">Bringing the item into view is not required; however, off-screen, non-virtualized items should support the [**IScrollItemProvider::ScrollIntoView**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollitemprovider-scrollintoview) method.</span></span>

## <a name="required-members-for-ivirtualizeditemprovider"></a><span data-ttu-id="c02da-129">Membres requis pour **IVirtualizedItemProvider**</span><span class="sxs-lookup"><span data-stu-id="c02da-129">Required Members for **IVirtualizedItemProvider**</span></span>

<span data-ttu-id="c02da-130">Les propriétés et méthodes suivantes sont requises pour implémenter l’interface [**IVirtualizedItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivirtualizeditemprovider) .</span><span class="sxs-lookup"><span data-stu-id="c02da-130">The following properties and methods are required for implementing the [**IVirtualizedItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivirtualizeditemprovider) interface.</span></span>



| <span data-ttu-id="c02da-131">Membres nécessaires</span><span class="sxs-lookup"><span data-stu-id="c02da-131">Required members</span></span>                                           | <span data-ttu-id="c02da-132">Type de membre</span><span class="sxs-lookup"><span data-stu-id="c02da-132">Member type</span></span> | <span data-ttu-id="c02da-133">Notes</span><span class="sxs-lookup"><span data-stu-id="c02da-133">Notes</span></span> |
|------------------------------------------------------------|-------------|-------|
| [<span data-ttu-id="c02da-134">**Optimiser**</span><span class="sxs-lookup"><span data-stu-id="c02da-134">**Realize**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ivirtualizeditemprovider-realize) | <span data-ttu-id="c02da-135">Méthode</span><span class="sxs-lookup"><span data-stu-id="c02da-135">Method</span></span>      | <span data-ttu-id="c02da-136">Aucun</span><span class="sxs-lookup"><span data-stu-id="c02da-136">None</span></span>  |



 

<span data-ttu-id="c02da-137">Ce modèle de contrôle n’est associé aucun événement.</span><span class="sxs-lookup"><span data-stu-id="c02da-137">This control pattern has no associated events.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c02da-138">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="c02da-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c02da-139">Implémentation du modèle de contrôle ItemContainer d’UI Automation</span><span class="sxs-lookup"><span data-stu-id="c02da-139">Implementing the UI Automation ItemContainer Control Pattern</span></span>](uiauto-implementingitemcontainer.md)
</dt> <dt>

[<span data-ttu-id="c02da-140">Vue d'ensemble des modèles de contrôle UI Automation</span><span class="sxs-lookup"><span data-stu-id="c02da-140">UI Automation Control Patterns Overview</span></span>](uiauto-controlpatternsoverview.md)
</dt> <dt>

[<span data-ttu-id="c02da-141">Vue d’ensemble de l’arborescence UI Automation</span><span class="sxs-lookup"><span data-stu-id="c02da-141">UI Automation Tree Overview</span></span>](uiauto-treeoverview.md)
</dt> <dt>

[<span data-ttu-id="c02da-142">Utilisation d’éléments virtualisés</span><span class="sxs-lookup"><span data-stu-id="c02da-142">Working with Virtualized Items</span></span>](uiauto-workingwithvirtualizeditems.md)
</dt> </dl>

 

 




