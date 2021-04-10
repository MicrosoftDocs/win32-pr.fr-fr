---
title: Modèle de contrôle ScrollItem
description: Fournit des instructions et des conventions pour l’implémentation de IScrollItemProvider, y compris des informations sur les méthodes.
ms.assetid: ea0d7438-218c-4925-b24c-a8011f305b9d
keywords:
- UI Automation, implémentation du modèle de contrôle ScrollItem
- UI Automation, modèle de contrôle ScrollItem
- UI Automation, IScrollItemProvider
- IScrollItemProvider
- implémentation des modèles de contrôle ScrollItem d’UI Automation
- Modèles de contrôle ScrollItem
- modèles de contrôle, IScrollItemProvider
- modèles de contrôle, implémenter des ScrollItem UI Automation
- modèles de contrôle, ScrollItem
- interfaces, IScrollItemProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7233dfe649d166a3172ff2dda3122895f259abcc
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104196912"
---
# <a name="scrollitem-control-pattern"></a><span data-ttu-id="28494-113">Modèle de contrôle ScrollItem</span><span class="sxs-lookup"><span data-stu-id="28494-113">ScrollItem Control Pattern</span></span>

<span data-ttu-id="28494-114">Fournit des instructions et des conventions pour l’implémentation de [**IScrollItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iscrollitemprovider), y compris des informations sur les méthodes.</span><span class="sxs-lookup"><span data-stu-id="28494-114">Describes guidelines and conventions for implementing [**IScrollItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iscrollitemprovider), including information about methods.</span></span> <span data-ttu-id="28494-115">Le modèle de contrôle **ScrollItem** est utilisé pour prendre en charge les contrôles enfants individuels des conteneurs qui implémentent [**IScrollProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iscrollprovider).</span><span class="sxs-lookup"><span data-stu-id="28494-115">The **ScrollItem** control pattern is used to support individual child controls of containers that implement [**IScrollProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iscrollprovider).</span></span> <span data-ttu-id="28494-116">L’existence du modèle de contrôle **ScrollItem** sur un contrôle n’implique pas que son conteneur ou un ancêtre doit implémenter le modèle de contrôle **Scroll** .</span><span class="sxs-lookup"><span data-stu-id="28494-116">The existence of the **ScrollItem** control pattern on a control does not imply that its container or any ancestor must implement the **Scroll** control pattern.</span></span>

<span data-ttu-id="28494-117">Quand le conteneur implémente le modèle de contrôle **Scroll** , le modèle de contrôle **ScrollItem** agit comme un canal de communication entre un contrôle enfant et son conteneur pour garantir que le conteneur peut modifier le contenu (ou la région) actuellement visible dans sa fenêtre d’affichage pour afficher le contrôle enfant.</span><span class="sxs-lookup"><span data-stu-id="28494-117">When the container does implement the **Scroll** control pattern, the **ScrollItem** control pattern acts as a communication channel between a child control and its container to ensure that the container can change the currently visible content (or region) within its viewport to display the child control.</span></span> <span data-ttu-id="28494-118">Pour obtenir des exemples de contrôles qui implémentent ce modèle de contrôle, consultez [types de contrôle et leurs modèles de contrôle pris en charge](uiauto-controlpatternmapping.md).</span><span class="sxs-lookup"><span data-stu-id="28494-118">For examples of controls that implement this control pattern, see [Control Types and Their Supported Control Patterns](uiauto-controlpatternmapping.md).</span></span>

<span data-ttu-id="28494-119">Cette rubrique contient les sections suivantes.</span><span class="sxs-lookup"><span data-stu-id="28494-119">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="28494-120">Conventions et directives d'implémentation</span><span class="sxs-lookup"><span data-stu-id="28494-120">Implementation Guidelines and Conventions</span></span>](#implementation-guidelines-and-conventions)
-   [<span data-ttu-id="28494-121">Membres requis pour **IScrollItemProvider**</span><span class="sxs-lookup"><span data-stu-id="28494-121">Required Members for **IScrollItemProvider**</span></span>](#required-members-for-iscrollitemprovider)
-   [<span data-ttu-id="28494-122">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="28494-122">Related topics</span></span>](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a><span data-ttu-id="28494-123">Conventions et directives d'implémentation</span><span class="sxs-lookup"><span data-stu-id="28494-123">Implementation Guidelines and Conventions</span></span>

<span data-ttu-id="28494-124">Lorsque vous implémentez le modèle de contrôle **ScrollItem** , notez les conventions et recommandations suivantes :</span><span class="sxs-lookup"><span data-stu-id="28494-124">When implementing the **ScrollItem** control pattern, note the following guidelines and conventions:</span></span>

-   <span data-ttu-id="28494-125">Les éléments contenus dans un contrôle de [fenêtre](uiauto-supportwindowcontroltype.md) ou de **canevas** ne sont pas requis pour implémenter l’interface [**IScrollItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iscrollitemprovider) .</span><span class="sxs-lookup"><span data-stu-id="28494-125">Items contained within a [Window](uiauto-supportwindowcontroltype.md) or **Canvas** control are not required to implement the [**IScrollItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iscrollitemprovider) interface.</span></span> <span data-ttu-id="28494-126">Toutefois, ils doivent également exposer un emplacement valide pour la propriété [**IUIAutomationElement :: CurrentBoundingRectangle**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentboundingrectangle) (ou [**CachedBoundingRectangle**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_cachedboundingrectangle)).</span><span class="sxs-lookup"><span data-stu-id="28494-126">As an alternative, however, they must expose a valid location for the [**IUIAutomationElement::CurrentBoundingRectangle**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentboundingrectangle) (or [**CachedBoundingRectangle**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_cachedboundingrectangle)) property.</span></span> <span data-ttu-id="28494-127">Cela permettra à une application cliente UI Automation de Microsoft d’utiliser les méthodes de modèle de contrôle [**IUIAutomationScrollPattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationscrollpattern) sur le conteneur pour afficher l’élément enfant.</span><span class="sxs-lookup"><span data-stu-id="28494-127">This will allow a Microsoft UI Automation client application to use the [**IUIAutomationScrollPattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationscrollpattern) control pattern methods on the container to display the child item.</span></span>

## <a name="required-members-for-iscrollitemprovider"></a><span data-ttu-id="28494-128">Membres requis pour **IScrollItemProvider**</span><span class="sxs-lookup"><span data-stu-id="28494-128">Required Members for **IScrollItemProvider**</span></span>

<span data-ttu-id="28494-129">La méthode suivante est requise pour l’implémentation de l’interface [**IScrollItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iscrollitemprovider) .</span><span class="sxs-lookup"><span data-stu-id="28494-129">The following method is required for implementing the [**IScrollItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iscrollitemprovider) interface.</span></span>



| <span data-ttu-id="28494-130">Membres nécessaires</span><span class="sxs-lookup"><span data-stu-id="28494-130">Required members</span></span>                                                    | <span data-ttu-id="28494-131">Type de membre</span><span class="sxs-lookup"><span data-stu-id="28494-131">Member type</span></span> | <span data-ttu-id="28494-132">Notes</span><span class="sxs-lookup"><span data-stu-id="28494-132">Notes</span></span> |
|---------------------------------------------------------------------|-------------|-------|
| [<span data-ttu-id="28494-133">**ScrollIntoView**</span><span class="sxs-lookup"><span data-stu-id="28494-133">**ScrollIntoView**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollitemprovider-scrollintoview) | <span data-ttu-id="28494-134">Méthode</span><span class="sxs-lookup"><span data-stu-id="28494-134">Method</span></span>      | <span data-ttu-id="28494-135">Aucun</span><span class="sxs-lookup"><span data-stu-id="28494-135">None</span></span>  |



 

<span data-ttu-id="28494-136">Ce modèle de contrôle n’est associé à aucune propriété ni à aucun événement.</span><span class="sxs-lookup"><span data-stu-id="28494-136">This control pattern has no associated properties or events.</span></span>

## <a name="related-topics"></a><span data-ttu-id="28494-137">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="28494-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="28494-138">Types de contrôle et leurs modèles de contrôle pris en charge</span><span class="sxs-lookup"><span data-stu-id="28494-138">Control Types and Their Supported Control Patterns</span></span>](uiauto-controlpatternmapping.md)
</dt> <dt>

[<span data-ttu-id="28494-139">Selection (modèle de contrôle)</span><span class="sxs-lookup"><span data-stu-id="28494-139">Selection Control Pattern</span></span>](uiauto-implementingselection.md)
</dt> <dt>

[<span data-ttu-id="28494-140">Vue d'ensemble des modèles de contrôle UI Automation</span><span class="sxs-lookup"><span data-stu-id="28494-140">UI Automation Control Patterns Overview</span></span>](uiauto-controlpatternsoverview.md)
</dt> <dt>

[<span data-ttu-id="28494-141">Vue d’ensemble de l’arborescence UI Automation</span><span class="sxs-lookup"><span data-stu-id="28494-141">UI Automation Tree Overview</span></span>](uiauto-treeoverview.md)
</dt> </dl>

 

 




