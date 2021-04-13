---
title: Window (modèle de contrôle)
description: Fournit des instructions et des conventions pour l’implémentation de IWindowProvider, y compris des informations sur les propriétés, les méthodes et les événements. Le modèle de contrôle Window prend en charge des contrôles qui fournissent des fonctionnalités fondamentales basées sur les fenêtres dans une interface graphique utilisateur traditionnelle.
ms.assetid: bfd37d27-fcec-4d25-841c-63e14e48c6c8
keywords:
- UI Automation, implémenter le modèle de contrôle Window
- UI Automation, modèle de contrôle de fenêtre
- UI Automation, IWindowProvider
- IWindowProvider
- implémentation de modèles de contrôle de fenêtre UI Automation
- Modèles de contrôle de fenêtre
- modèles de contrôle, IWindowProvider
- modèles de contrôle, implémenter une fenêtre UI Automation
- modèles de contrôle, fenêtre
- interfaces, IWindowProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3c4f0d862a14fee35f8d1982c7870e2be031c61
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104311344"
---
# <a name="window-control-pattern"></a><span data-ttu-id="b5483-114">Window (modèle de contrôle)</span><span class="sxs-lookup"><span data-stu-id="b5483-114">Window Control Pattern</span></span>

<span data-ttu-id="b5483-115">Fournit des instructions et des conventions pour l’implémentation de [**IWindowProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iwindowprovider), y compris des informations sur les propriétés, les méthodes et les événements.</span><span class="sxs-lookup"><span data-stu-id="b5483-115">Describes guidelines and conventions for implementing [**IWindowProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iwindowprovider), including information about properties, methods, and events.</span></span> <span data-ttu-id="b5483-116">Le modèle de contrôle **Window** prend en charge des contrôles qui fournissent des fonctionnalités fondamentales basées sur les fenêtres dans une interface graphique utilisateur traditionnelle.</span><span class="sxs-lookup"><span data-stu-id="b5483-116">The **Window** control pattern supports controls that provide fundamental window-based functionality within a traditional GUI.</span></span>

<span data-ttu-id="b5483-117">Voici des exemples de contrôles qui doivent implémenter ce modèle de contrôle : les fenêtres d’application de niveau supérieur, les fenêtres enfants de l’interface multidocument (MDI), les contrôles de volet de fractionnement redimensionnables, les boîtes de dialogue modales et les fenêtres d’aide de bulle.</span><span class="sxs-lookup"><span data-stu-id="b5483-117">Examples of controls that must implement this control pattern include top-level application windows, multiple-document interface (MDI) child windows, resizable split pane controls, modal dialogs and balloon help windows.</span></span> <span data-ttu-id="b5483-118">Pour obtenir des exemples de contrôles implémentant ce modèle de contrôle, consultez [Control Pattern Mapping for UI Automation Clients](uiauto-controlpatternmapping.md).</span><span class="sxs-lookup"><span data-stu-id="b5483-118">For examples of controls that implement this control pattern, see [Control Pattern Mapping for UI Automation Clients](uiauto-controlpatternmapping.md).</span></span>

<span data-ttu-id="b5483-119">Cette rubrique contient les sections suivantes.</span><span class="sxs-lookup"><span data-stu-id="b5483-119">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="b5483-120">Conventions et directives d'implémentation</span><span class="sxs-lookup"><span data-stu-id="b5483-120">Implementation Guidelines and Conventions</span></span>](#implementation-guidelines-and-conventions)
-   [<span data-ttu-id="b5483-121">Membres requis pour **IWindowProvider**</span><span class="sxs-lookup"><span data-stu-id="b5483-121">Required Members for **IWindowProvider**</span></span>](#required-members-for-iwindowprovider)
-   [<span data-ttu-id="b5483-122">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="b5483-122">Related topics</span></span>](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a><span data-ttu-id="b5483-123">Conventions et directives d'implémentation</span><span class="sxs-lookup"><span data-stu-id="b5483-123">Implementation Guidelines and Conventions</span></span>

<span data-ttu-id="b5483-124">Lorsque vous implémentez le modèle de contrôle **Window** , notez les conventions et recommandations suivantes :</span><span class="sxs-lookup"><span data-stu-id="b5483-124">When implementing the **Window** control pattern, note the following guidelines and conventions:</span></span>

-   <span data-ttu-id="b5483-125">Pour prendre en charge la possibilité de modifier à la fois la taille de la fenêtre et la position de l’écran à l’aide de Microsoft UI Automation, un contrôle doit implémenter [**ITransformProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itransformprovider) en plus de [**IWindowProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iwindowprovider).</span><span class="sxs-lookup"><span data-stu-id="b5483-125">To support the ability to modify both window size and screen position using Microsoft UI Automation, a control must implement [**ITransformProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itransformprovider) in addition to [**IWindowProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iwindowprovider).</span></span>
-   <span data-ttu-id="b5483-126">Les contrôles qui contiennent des barres de titre et des éléments de barre de titre qui permettent de déplacer, redimensionner, agrandir, réduire ou fermer le contrôle sont généralement requis pour implémenter [**IWindowProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iwindowprovider).</span><span class="sxs-lookup"><span data-stu-id="b5483-126">Controls that contain title bars, and title bar elements that enable the control to be moved, resized, maximized, minimized, or closed, are typically required to implement [**IWindowProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iwindowprovider).</span></span>
-   <span data-ttu-id="b5483-127">Les contrôles tels que les fenêtres contextuelles d’info-bulle et les menus déroulants de zone de liste déroulante ou de menu n’implémentent généralement pas [**IWindowProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iwindowprovider).</span><span class="sxs-lookup"><span data-stu-id="b5483-127">Controls such as tooltip pop-ups and combo-box or menu drop-downs do not typically implement [**IWindowProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iwindowprovider).</span></span>
-   <span data-ttu-id="b5483-128">Les fenêtres d’aide de la bulle se distinguent des info-bulles de base des info-bulles par l’approvisionnement d’un bouton **Fermer** semblable à une fenêtre.</span><span class="sxs-lookup"><span data-stu-id="b5483-128">Balloon help windows are differentiated from basic tooltip pop-ups by the provision of a window-like **Close** button.</span></span>
-   <span data-ttu-id="b5483-129">Le mode plein écran n’est pas pris en charge par [**IWindowProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iwindowprovider) , car il est propre aux fonctionnalités d’une application et n’est pas un comportement de fenêtre typique.</span><span class="sxs-lookup"><span data-stu-id="b5483-129">Full-screen mode is not supported by [**IWindowProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iwindowprovider) as it is feature-specific to an application and is not typical window behavior.</span></span>

## <a name="required-members-for-iwindowprovider"></a><span data-ttu-id="b5483-130">Membres requis pour **IWindowProvider**</span><span class="sxs-lookup"><span data-stu-id="b5483-130">Required Members for **IWindowProvider**</span></span>

<span data-ttu-id="b5483-131">Les propriétés, méthodes et événements suivants sont requis pour implémenter l’interface [**IWindowProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iwindowprovider) .</span><span class="sxs-lookup"><span data-stu-id="b5483-131">The following properties, methods, and events are required for implementing the [**IWindowProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iwindowprovider) interface.</span></span>



| <span data-ttu-id="b5483-132">Membres nécessaires</span><span class="sxs-lookup"><span data-stu-id="b5483-132">Required members</span></span>                                                                            | <span data-ttu-id="b5483-133">Type de membre</span><span class="sxs-lookup"><span data-stu-id="b5483-133">Member type</span></span> | <span data-ttu-id="b5483-134">Notes</span><span class="sxs-lookup"><span data-stu-id="b5483-134">Notes</span></span>                                                                       |
|---------------------------------------------------------------------------------------------|-------------|-----------------------------------------------------------------------------|
| [<span data-ttu-id="b5483-135">**WindowInteractionState**</span><span class="sxs-lookup"><span data-stu-id="b5483-135">**WindowInteractionState**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iwindowprovider-get_windowinteractionstate)             | <span data-ttu-id="b5483-136">Propriété</span><span class="sxs-lookup"><span data-stu-id="b5483-136">Property</span></span>    | <span data-ttu-id="b5483-137">Il n’est pas garanti que **WindowInteractionState \_ ReadyForUserInteraction**</span><span class="sxs-lookup"><span data-stu-id="b5483-137">Is not guaranteed to be **WindowInteractionState\_ReadyForUserInteraction**</span></span> |
| [<span data-ttu-id="b5483-138">**IsModal**</span><span class="sxs-lookup"><span data-stu-id="b5483-138">**IsModal**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iwindowprovider-get_ismodal)                                           | <span data-ttu-id="b5483-139">Propriété</span><span class="sxs-lookup"><span data-stu-id="b5483-139">Property</span></span>    | <span data-ttu-id="b5483-140">Aucun</span><span class="sxs-lookup"><span data-stu-id="b5483-140">None</span></span>                                                                        |
| [<span data-ttu-id="b5483-141">**IsTopmost**</span><span class="sxs-lookup"><span data-stu-id="b5483-141">**IsTopmost**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iwindowprovider-get_istopmost)                                       | <span data-ttu-id="b5483-142">Propriété</span><span class="sxs-lookup"><span data-stu-id="b5483-142">Property</span></span>    | <span data-ttu-id="b5483-143">Aucun</span><span class="sxs-lookup"><span data-stu-id="b5483-143">None</span></span>                                                                        |
| [<span data-ttu-id="b5483-144">**CanMaximize**</span><span class="sxs-lookup"><span data-stu-id="b5483-144">**CanMaximize**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iwindowprovider-get_canmaximize)                                   | <span data-ttu-id="b5483-145">Propriété</span><span class="sxs-lookup"><span data-stu-id="b5483-145">Property</span></span>    | <span data-ttu-id="b5483-146">Aucun</span><span class="sxs-lookup"><span data-stu-id="b5483-146">None</span></span>                                                                        |
| [<span data-ttu-id="b5483-147">**CanMinimize**</span><span class="sxs-lookup"><span data-stu-id="b5483-147">**CanMinimize**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iwindowprovider-get_canminimize)                                   | <span data-ttu-id="b5483-148">Propriété</span><span class="sxs-lookup"><span data-stu-id="b5483-148">Property</span></span>    | <span data-ttu-id="b5483-149">Aucun</span><span class="sxs-lookup"><span data-stu-id="b5483-149">None</span></span>                                                                        |
| [<span data-ttu-id="b5483-150">**WindowVisualState**</span><span class="sxs-lookup"><span data-stu-id="b5483-150">**WindowVisualState**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iwindowprovider-get_windowvisualstate)                       | <span data-ttu-id="b5483-151">Propriété</span><span class="sxs-lookup"><span data-stu-id="b5483-151">Property</span></span>    | <span data-ttu-id="b5483-152">Aucun</span><span class="sxs-lookup"><span data-stu-id="b5483-152">None</span></span>                                                                        |
| [<span data-ttu-id="b5483-153">**Fermer**</span><span class="sxs-lookup"><span data-stu-id="b5483-153">**Close**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iwindowprovider-close)                                               | <span data-ttu-id="b5483-154">Méthode</span><span class="sxs-lookup"><span data-stu-id="b5483-154">Method</span></span>      | <span data-ttu-id="b5483-155">Aucun</span><span class="sxs-lookup"><span data-stu-id="b5483-155">None</span></span>                                                                        |
| [<span data-ttu-id="b5483-156">**SetVisualState**</span><span class="sxs-lookup"><span data-stu-id="b5483-156">**SetVisualState**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iwindowprovider-setvisualstate)                             | <span data-ttu-id="b5483-157">Méthode</span><span class="sxs-lookup"><span data-stu-id="b5483-157">Method</span></span>      | <span data-ttu-id="b5483-158">Aucun</span><span class="sxs-lookup"><span data-stu-id="b5483-158">None</span></span>                                                                        |
| [<span data-ttu-id="b5483-159">**WaitForInputIdle**</span><span class="sxs-lookup"><span data-stu-id="b5483-159">**WaitForInputIdle**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iwindowprovider-waitforinputidle)                         | <span data-ttu-id="b5483-160">Méthode</span><span class="sxs-lookup"><span data-stu-id="b5483-160">Method</span></span>      | <span data-ttu-id="b5483-161">Aucun</span><span class="sxs-lookup"><span data-stu-id="b5483-161">None</span></span>                                                                        |
| [<span data-ttu-id="b5483-162">**\_Fenêtre UIA \_ WindowClosedEventId**</span><span class="sxs-lookup"><span data-stu-id="b5483-162">**UIA\_Window\_WindowClosedEventId**</span></span>](uiauto-event-ids.md) | <span data-ttu-id="b5483-163">Événement</span><span class="sxs-lookup"><span data-stu-id="b5483-163">Event</span></span>       | <span data-ttu-id="b5483-164">Aucun</span><span class="sxs-lookup"><span data-stu-id="b5483-164">None</span></span>                                                                        |
| [<span data-ttu-id="b5483-165">**\_Fenêtre UIA \_ WindowOpenedEventId**</span><span class="sxs-lookup"><span data-stu-id="b5483-165">**UIA\_Window\_WindowOpenedEventId**</span></span>](uiauto-event-ids.md) | <span data-ttu-id="b5483-166">Événement</span><span class="sxs-lookup"><span data-stu-id="b5483-166">Event</span></span>       | <span data-ttu-id="b5483-167">Aucun</span><span class="sxs-lookup"><span data-stu-id="b5483-167">None</span></span>                                                                        |



 

## <a name="related-topics"></a><span data-ttu-id="b5483-168">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="b5483-168">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="b5483-169">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="b5483-169">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="b5483-170">Vue d'ensemble des modèles de contrôle UI Automation</span><span class="sxs-lookup"><span data-stu-id="b5483-170">UI Automation Control Patterns Overview</span></span>](uiauto-controlpatternsoverview.md)
</dt> <dt>

[<span data-ttu-id="b5483-171">Mappage de modèle de contrôle pour les clients UI Automation</span><span class="sxs-lookup"><span data-stu-id="b5483-171">Control Pattern Mapping for UI Automation Clients</span></span>](uiauto-controlpatternmapping.md)
</dt> <dt>

[<span data-ttu-id="b5483-172">Vue d’ensemble de l’arborescence UI Automation</span><span class="sxs-lookup"><span data-stu-id="b5483-172">UI Automation Tree Overview</span></span>](uiauto-treeoverview.md)
</dt> </dl>

 

 




