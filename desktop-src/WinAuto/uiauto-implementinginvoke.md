---
title: Invoke (modèle de contrôle)
description: Fournit des instructions et des conventions pour l’implémentation de IInvokeProvider, y compris des informations sur les méthodes.
ms.assetid: 6557a03c-fd1f-4e44-8393-fe367d7a17af
keywords:
- UI Automation, implémenter le modèle de contrôle Invoke
- UI Automation, appeler le modèle de contrôle
- UI Automation, IInvokeProvider
- IInvokeProvider
- implémentation des modèles de contrôle Invoke d’UI Automation
- Appeler des modèles de contrôle
- modèles de contrôle, IInvokeProvider
- modèles de contrôle, implémenter l’appel d’UI Automation
- modèles de contrôle, Invoke
- interfaces, IInvokeProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 963f8d9ccd6ea2a50557ec26a655d5c7f43c6123
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103839806"
---
# <a name="invoke-control-pattern"></a><span data-ttu-id="b80e2-113">Invoke (modèle de contrôle)</span><span class="sxs-lookup"><span data-stu-id="b80e2-113">Invoke Control Pattern</span></span>

<span data-ttu-id="b80e2-114">Fournit des instructions et des conventions pour l’implémentation de [**IInvokeProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iinvokeprovider), y compris des informations sur les méthodes.</span><span class="sxs-lookup"><span data-stu-id="b80e2-114">Describes guidelines and conventions for implementing [**IInvokeProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iinvokeprovider), including information about methods.</span></span> <span data-ttu-id="b80e2-115">Le modèle de contrôle **Invoke** est utilisé pour prendre en charge les contrôles qui ne maintiennent pas l’État lorsqu’ils sont activés, mais qui initialisent ou exécutent une action unique et non ambiguë.</span><span class="sxs-lookup"><span data-stu-id="b80e2-115">The **Invoke** control pattern is used to support controls that do not maintain state when activated but rather initiate or perform a single, unambiguous action.</span></span>

<span data-ttu-id="b80e2-116">Les contrôles qui maintiennent l’État, tels que les cases à cocher et les cases d’option, doivent implémenter [**IToggleProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itoggleprovider) et [**ISelectionProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider) respectivement.</span><span class="sxs-lookup"><span data-stu-id="b80e2-116">Controls that do maintain state, such as check boxes and radio buttons, must instead implement [**IToggleProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itoggleprovider) and [**ISelectionProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider) respectively.</span></span> <span data-ttu-id="b80e2-117">Pour obtenir des exemples de contrôles qui implémentent ce modèle de contrôle, consultez [types de contrôle et leurs modèles de contrôle pris en charge](uiauto-controlpatternmapping.md).</span><span class="sxs-lookup"><span data-stu-id="b80e2-117">For examples of controls that implement this control pattern, see [Control Types and Their Supported Control Patterns](uiauto-controlpatternmapping.md).</span></span>

<span data-ttu-id="b80e2-118">Cette rubrique contient les sections suivantes.</span><span class="sxs-lookup"><span data-stu-id="b80e2-118">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="b80e2-119">Conventions et directives d'implémentation</span><span class="sxs-lookup"><span data-stu-id="b80e2-119">Implementation Guidelines and Conventions</span></span>](#implementation-guidelines-and-conventions)
-   [<span data-ttu-id="b80e2-120">Membres requis pour **IInvokeProvider**</span><span class="sxs-lookup"><span data-stu-id="b80e2-120">Required Members for **IInvokeProvider**</span></span>](#required-members-for-iinvokeprovider)
-   [<span data-ttu-id="b80e2-121">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="b80e2-121">Related topics</span></span>](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a><span data-ttu-id="b80e2-122">Conventions et directives d'implémentation</span><span class="sxs-lookup"><span data-stu-id="b80e2-122">Implementation Guidelines and Conventions</span></span>

<span data-ttu-id="b80e2-123">Lorsque vous implémentez le modèle de contrôle **Invoke** , notez les conventions et recommandations suivantes :</span><span class="sxs-lookup"><span data-stu-id="b80e2-123">When implementing the **Invoke** control pattern, note the following guidelines and conventions:</span></span>

-   <span data-ttu-id="b80e2-124">Les contrôles implémentent [**IInvokeProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iinvokeprovider) si le même comportement n’est pas exposé par le biais d’un autre fournisseur de modèle de contrôle.</span><span class="sxs-lookup"><span data-stu-id="b80e2-124">Controls implement [**IInvokeProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iinvokeprovider) if the same behavior is not exposed through another control pattern provider.</span></span> <span data-ttu-id="b80e2-125">Par exemple, si la méthode [**IUIAutomationInvokePattern :: Invoke**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationinvokepattern-invoke) sur un contrôle exécute la même action que la méthode [**IUIAutomationExpandCollapsePattern :: Expand**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationexpandcollapsepattern-expand) ou [**Collapse**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationexpandcollapsepattern-collapse) , le contrôle ne doit pas implémenter **IInvokeProvider**.</span><span class="sxs-lookup"><span data-stu-id="b80e2-125">For example, if the [**IUIAutomationInvokePattern::Invoke**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationinvokepattern-invoke) method on a control performs the same action as the [**IUIAutomationExpandCollapsePattern::Expand**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationexpandcollapsepattern-expand) or [**Collapse**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationexpandcollapsepattern-collapse) method, the control should not implement **IInvokeProvider**.</span></span>
-   <span data-ttu-id="b80e2-126">Pour appeler un contrôle, il convient généralement de cliquer, de double-cliquer ou d’appuyer sur Entrée, sur un raccourci clavier prédéfini ou sur une autre combinaison de touches.</span><span class="sxs-lookup"><span data-stu-id="b80e2-126">Invoking a control is generally performed by clicking or double-clicking or pressing ENTER, a predefined keyboard shortcut, or some alternate combination of keystrokes.</span></span>
-   <span data-ttu-id="b80e2-127">L’événement **appelé** ([**UIA \_ Invoke \_ InvokedEventId**](uiauto-event-ids.md)) est déclenché sur un contrôle qui a été activé (en réponse à un contrôle effectuant l’action qui lui est associée).</span><span class="sxs-lookup"><span data-stu-id="b80e2-127">The **Invoked** event ([**UIA\_Invoke\_InvokedEventId**](uiauto-event-ids.md)) event is raised on a control that has been activated (as a response to a control carrying out its associated action).</span></span> <span data-ttu-id="b80e2-128">Si possible, l’événement doit être déclenché une fois que le contrôle a terminé l’action et retourné une valeur sans se bloquer.</span><span class="sxs-lookup"><span data-stu-id="b80e2-128">If possible, the event should be raised after the control has completed the action and returned without blocking.</span></span> <span data-ttu-id="b80e2-129">L’événement **appelé** (**UIA \_ Invoke \_ InvokedEventId**) doit être déclenché avant de traiter la requête **Invoke** dans les scénarios suivants :</span><span class="sxs-lookup"><span data-stu-id="b80e2-129">The **Invoked** event (**UIA\_Invoke\_InvokedEventId**) should be raised before servicing the **Invoke** request in the following scenarios:</span></span>
    -   <span data-ttu-id="b80e2-130">Il n’est pas possible ou pratique d’attendre que l’action soit terminée.</span><span class="sxs-lookup"><span data-stu-id="b80e2-130">It is not possible or practical to wait until the action is complete.</span></span>
    -   <span data-ttu-id="b80e2-131">L’action requiert une intervention de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="b80e2-131">The action requires user interaction.</span></span>
    -   <span data-ttu-id="b80e2-132">L’action prend du temps et bloque le client pendant un long moment.</span><span class="sxs-lookup"><span data-stu-id="b80e2-132">The action is time-consuming and will cause the calling client to block for a significant amount of time.</span></span>
-   <span data-ttu-id="b80e2-133">Si l’appel du contrôle a des effets secondaires significatifs, ces effets secondaires doivent être exposés via la propriété **HelpText** .</span><span class="sxs-lookup"><span data-stu-id="b80e2-133">If invoking the control has significant side-effects, those side-effects should be exposed through the **HelpText** property.</span></span> <span data-ttu-id="b80e2-134">Par exemple, même si [**IUIAutomationInvokePattern :: Invoke**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationinvokepattern-invoke) n’est pas associé à la sélection, **Invoke** peut faire en sorte qu’un autre contrôle soit sélectionné.</span><span class="sxs-lookup"><span data-stu-id="b80e2-134">For example, even though [**IUIAutomationInvokePattern::Invoke**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationinvokepattern-invoke) is not associated with selection, **Invoke** may cause another control to become selected.</span></span>
-   <span data-ttu-id="b80e2-135">Les effets de survol (ou de pointage avec la souris) ne constituent généralement pas un événement **appelé** .</span><span class="sxs-lookup"><span data-stu-id="b80e2-135">Hover (or mouse-over) effects generally do not constitute an **Invoked** event.</span></span> <span data-ttu-id="b80e2-136">Toutefois, les contrôles qui exécutent une action (par opposition à un effet visuel) en fonction de l’état de survol doivent prendre en charge le modèle de contrôle **Invoke** .</span><span class="sxs-lookup"><span data-stu-id="b80e2-136">However, controls that perform an action (as opposed to cause a visual effect) based on the hover state should support the **Invoke** control pattern.</span></span>
    > [!Note]  
    > <span data-ttu-id="b80e2-137">Cette implémentation est considérée comme un problème d’accessibilité si le contrôle ne peut être appelé que suite à un effet secondaire lié à la souris.</span><span class="sxs-lookup"><span data-stu-id="b80e2-137">This implementation is considered an accessibility issue if the control can be invoked only as a result of a mouse-related side effect.</span></span>

     

-   <span data-ttu-id="b80e2-138">L’appel d’un contrôle est différent de la sélection d’un élément.</span><span class="sxs-lookup"><span data-stu-id="b80e2-138">Invoking a control is different from selecting an item.</span></span> <span data-ttu-id="b80e2-139">Toutefois, selon le contrôle, l’appel peut avoir comme effet secondaire la sélection de l’élément.</span><span class="sxs-lookup"><span data-stu-id="b80e2-139">However, depending on the control, invoking it may cause the item to become selected as a side-effect.</span></span> <span data-ttu-id="b80e2-140">Par exemple, l’appel d’un élément de liste de documents Microsoft Word dans le dossier Mes documents sélectionne l’élément et ouvre le document.</span><span class="sxs-lookup"><span data-stu-id="b80e2-140">For example, invoking a Microsoft Word document list item in the My Documents folder both selects the item and opens the document.</span></span>
-   <span data-ttu-id="b80e2-141">Un élément peut disparaître de l’arborescence de l’automatisation de l’interface utilisateur de Microsoft immédiatement lors de son appel.</span><span class="sxs-lookup"><span data-stu-id="b80e2-141">An element can disappear from the Microsoft UI Automation tree immediately upon being invoked.</span></span> <span data-ttu-id="b80e2-142">La requête d’informations de l’élément fourni par le rappel d’événement peut échouer.</span><span class="sxs-lookup"><span data-stu-id="b80e2-142">Requesting information from the element provided by the event callback may fail as a result.</span></span> <span data-ttu-id="b80e2-143">La pré-récupération des informations mises en cache est la solution recommandée.</span><span class="sxs-lookup"><span data-stu-id="b80e2-143">Pre-fetching cached information is the recommended workaround.</span></span>
-   <span data-ttu-id="b80e2-144">Les contrôles peuvent implémenter plusieurs modèles de contrôle.</span><span class="sxs-lookup"><span data-stu-id="b80e2-144">Controls can implement multiple control patterns.</span></span> <span data-ttu-id="b80e2-145">Par exemple, le contrôle **Fill Color** dans la barre d’outils Microsoft Excel implémente à la fois les modèles de contrôle Invoke et [ExpandCollapse](uiauto-implementingexpandcollapse.md) .</span><span class="sxs-lookup"><span data-stu-id="b80e2-145">For example, the **Fill Color** control on the Microsoft Excel toolbar implements both the Invoke and the [ExpandCollapse](uiauto-implementingexpandcollapse.md) control patterns.</span></span> <span data-ttu-id="b80e2-146">Le modèle de contrôle ExpandCollapse expose le menu et le modèle de contrôle **Invoke** remplit la sélection active avec la couleur choisie.</span><span class="sxs-lookup"><span data-stu-id="b80e2-146">The ExpandCollapse control pattern exposes the menu and the **Invoke** control pattern fills the active selection with the chosen color.</span></span>

## <a name="required-members-for-iinvokeprovider"></a><span data-ttu-id="b80e2-147">Membres requis pour **IInvokeProvider**</span><span class="sxs-lookup"><span data-stu-id="b80e2-147">Required Members for **IInvokeProvider**</span></span>

<span data-ttu-id="b80e2-148">La méthode suivante est requise pour l’implémentation de l’interface [**IInvokeProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iinvokeprovider) .</span><span class="sxs-lookup"><span data-stu-id="b80e2-148">The following method is required for implementing the [**IInvokeProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iinvokeprovider) interface.</span></span>



| <span data-ttu-id="b80e2-149">Membres nécessaires</span><span class="sxs-lookup"><span data-stu-id="b80e2-149">Required members</span></span>                                | <span data-ttu-id="b80e2-150">Type de membre</span><span class="sxs-lookup"><span data-stu-id="b80e2-150">Member type</span></span> | <span data-ttu-id="b80e2-151">Notes</span><span class="sxs-lookup"><span data-stu-id="b80e2-151">Notes</span></span>                                                                                                                                                                                                                                                                                                                                  |
|-------------------------------------------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b80e2-152">**Appeler**</span><span class="sxs-lookup"><span data-stu-id="b80e2-152">**Invoke**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iinvokeprovider-invoke) | <span data-ttu-id="b80e2-153">Méthode</span><span class="sxs-lookup"><span data-stu-id="b80e2-153">Method</span></span>      | <span data-ttu-id="b80e2-154">**Invoke** est un appel asynchrone et doit être retourné immédiatement sans blocage.</span><span class="sxs-lookup"><span data-stu-id="b80e2-154">**Invoke** is an asynchronous call and must return immediately without blocking.</span></span><br/> <span data-ttu-id="b80e2-155">Ce comportement est particulièrement critique pour les contrôles qui, directement ou indirectement, lancent une boîte de dialogue modale lorsqu’ils sont appelés.</span><span class="sxs-lookup"><span data-stu-id="b80e2-155">This behavior is particularly critical for controls that, directly or indirectly, launch a modal dialog when invoked.</span></span> <span data-ttu-id="b80e2-156">Tout client UI Automation à l’origine de l’événement reste bloqué jusqu’à la fermeture de la boîte de dialogue modale.</span><span class="sxs-lookup"><span data-stu-id="b80e2-156">Any UI Automation client that instigated the event will remain blocked until the modal dialog is closed.</span></span> <br/> |



 

<span data-ttu-id="b80e2-157">Ce modèle de contrôle n’est associé à aucune propriété ni à aucun événement.</span><span class="sxs-lookup"><span data-stu-id="b80e2-157">This control pattern has no associated properties or events.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b80e2-158">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="b80e2-158">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b80e2-159">Types de contrôle et leurs modèles de contrôle pris en charge</span><span class="sxs-lookup"><span data-stu-id="b80e2-159">Control Types and Their Supported Control Patterns</span></span>](uiauto-controlpatternmapping.md)
</dt> <dt>

[<span data-ttu-id="b80e2-160">Vue d'ensemble des modèles de contrôle UI Automation</span><span class="sxs-lookup"><span data-stu-id="b80e2-160">UI Automation Control Patterns Overview</span></span>](uiauto-controlpatternsoverview.md)
</dt> <dt>

[<span data-ttu-id="b80e2-161">Vue d’ensemble de l’arborescence UI Automation</span><span class="sxs-lookup"><span data-stu-id="b80e2-161">UI Automation Tree Overview</span></span>](uiauto-treeoverview.md)
</dt> <dt>

[<span data-ttu-id="b80e2-162">**UIA \_ Invoke \_ InvokedEventId**</span><span class="sxs-lookup"><span data-stu-id="b80e2-162">**UIA\_Invoke\_InvokedEventId**</span></span>](uiauto-event-ids.md)
</dt> </dl>

 

 





