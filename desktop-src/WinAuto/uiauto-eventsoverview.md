---
title: Vue d'ensemble des événements UI Automation
description: La notification d’événements Microsoft UI Automation est une fonctionnalité clé pour les technologies d’assistance, telles que les lecteurs d’écran et les loupes d’écran.
ms.assetid: 0ded64ba-188e-427e-897f-4381237ace75
keywords:
- UI Automation, vue d’ensemble des événements
- UI Automation, catégories d’événements
- UI Automation, notifications d’événements
- notifications d'événements
- événements, catégories
- événements, notifications d’événements
- Événements de modification de propriété
- Événements d’action d’élément
- Événements de modification de structure
- Événements de modification globaux du Bureau
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9ddd61ed72ae0e92a13f6b59b493427fd7be421
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315275"
---
# <a name="ui-automation-events-overview"></a><span data-ttu-id="d067d-113">Vue d'ensemble des événements UI Automation</span><span class="sxs-lookup"><span data-stu-id="d067d-113">UI Automation Events Overview</span></span>

<span data-ttu-id="d067d-114">La notification d’événements Microsoft UI Automation est une fonctionnalité clé pour les technologies d’assistance, telles que les lecteurs d’écran et les loupes d’écran.</span><span class="sxs-lookup"><span data-stu-id="d067d-114">Microsoft UI Automation event notification is a key feature for assistive technologies, such as screen readers and screen magnifiers.</span></span> <span data-ttu-id="d067d-115">Ces clients UI Automation suivent les événements déclenchés par les fournisseurs UI Automation quand un événement se produit dans l’interface utilisateur et utilisent les informations pour notifier les utilisateurs finaux.</span><span class="sxs-lookup"><span data-stu-id="d067d-115">These UI Automation clients track events that are raised by UI Automation providers when something happens in the UI and use the information to notify end users.</span></span>

<span data-ttu-id="d067d-116">L'efficacité est améliorée en permettant aux applications fournisseurs de déclencher des événements de manière sélective, selon que des clients sont abonnés à ces événements ou non, si aucun client n'écoute d'événement.</span><span class="sxs-lookup"><span data-stu-id="d067d-116">Efficiency is improved by allowing provider applications to raise events selectively, depending on whether any clients are subscribed to those events, or not at all, if no clients are listening for any events.</span></span>

<span data-ttu-id="d067d-117">Les événements UI Automation s’inscrivent dans les catégories suivantes.</span><span class="sxs-lookup"><span data-stu-id="d067d-117">UI Automation events fall into the following categories.</span></span>



| <span data-ttu-id="d067d-118">Catégorie d'événement</span><span class="sxs-lookup"><span data-stu-id="d067d-118">Event Category</span></span>        | <span data-ttu-id="d067d-119">Description</span><span class="sxs-lookup"><span data-stu-id="d067d-119">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|-----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d067d-120">Modification de propriété</span><span class="sxs-lookup"><span data-stu-id="d067d-120">Property change</span></span>       | <span data-ttu-id="d067d-121">Déclenché en cas de modification d’une propriété sur l’élément UI Automation ou le modèle de contrôle.</span><span class="sxs-lookup"><span data-stu-id="d067d-121">Raised when a property on UI Automation element or control pattern changes.</span></span> <span data-ttu-id="d067d-122">Par exemple, si un client doit surveiller un contrôle de case à cocher d’application, il peut s’inscrire pour écouter un événement de modification de propriété sur la propriété [**IUIAutomationTogglePattern :: CurrentToggleState**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtogglepattern-get_currenttogglestate) .</span><span class="sxs-lookup"><span data-stu-id="d067d-122">For example, if a client needs to monitor an application check box control, it can register to listen for a property change event on the [**IUIAutomationTogglePattern::CurrentToggleState**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtogglepattern-get_currenttogglestate) property.</span></span> <span data-ttu-id="d067d-123">Quand le contrôle de case à cocher est coché ou décoché, le fournisseur déclenche l'événement et le client peut agir de manière appropriée.</span><span class="sxs-lookup"><span data-stu-id="d067d-123">When the check box control is checked or unchecked, the provider raises the event and the client can act as necessary.</span></span> |
| <span data-ttu-id="d067d-124">Action d'élément</span><span class="sxs-lookup"><span data-stu-id="d067d-124">Element action</span></span>        | <span data-ttu-id="d067d-125">Déclenché lorsqu’une modification de l’interface utilisateur résulte de l’utilisateur final ou de l’activité de programmation, par exemple, lorsque l’utilisateur clique sur un bouton ou l’appelle via [**IUIAutomationInvokePattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationinvokepattern).</span><span class="sxs-lookup"><span data-stu-id="d067d-125">Raised when a change in the UI results from end user or programmatic activity, for example, when a button is clicked or invoked through [**IUIAutomationInvokePattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationinvokepattern).</span></span>                                                                                                                                                                                                                                                     |
| <span data-ttu-id="d067d-126">Modification de la structure</span><span class="sxs-lookup"><span data-stu-id="d067d-126">Structure change</span></span>      | <span data-ttu-id="d067d-127">Déclenché quand la structure de l’arborescence UI Automation change.</span><span class="sxs-lookup"><span data-stu-id="d067d-127">Raised when the structure of the UI Automation tree changes.</span></span> <span data-ttu-id="d067d-128">La structure évolue quand de nouveaux éléments de l’interface utilisateur deviennent visibles, sont masqués ou sont supprimés sur le Bureau.</span><span class="sxs-lookup"><span data-stu-id="d067d-128">The structure changes when new UI items become visible, hidden, or removed on the desktop.</span></span>                                                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="d067d-129">Modification globale du bureau</span><span class="sxs-lookup"><span data-stu-id="d067d-129">Global desktop change</span></span> | <span data-ttu-id="d067d-130">Déclenché quand des actions d'intérêt global pour le client se produisent, par exemple quand le focus passe d'un élément à un autre ou qu'une fenêtre se ferme.</span><span class="sxs-lookup"><span data-stu-id="d067d-130">Raised when actions of global interest to the client occur, such as when the focus shifts from one element to another, or when a window closes.</span></span>                                                                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="d067d-131">Notification</span><span class="sxs-lookup"><span data-stu-id="d067d-131">Notification</span></span>          | <span data-ttu-id="d067d-132">Déclenché quand une application appelle la fonction [**UiaRaiseNotificationEvent**](https://www.bing.com/search?q=**UiaRaiseNotificationEvent**) .</span><span class="sxs-lookup"><span data-stu-id="d067d-132">Raised when an app calls the [**UiaRaiseNotificationEvent**](https://www.bing.com/search?q=**UiaRaiseNotificationEvent**) function.</span></span> <span data-ttu-id="d067d-133">[**NotificationKind**](/windows/win32/api/uiautomationcore/ne-uiautomationcore-notificationkind) indique le type de la notification.</span><span class="sxs-lookup"><span data-stu-id="d067d-133">[**NotificationKind**](/windows/win32/api/uiautomationcore/ne-uiautomationcore-notificationkind) indicates the type of the notification.</span></span>                                                                                                                                                                                                                                                 |



 

<span data-ttu-id="d067d-134">Certains événements ne signifient pas nécessairement que l'état de l'interface utilisateur a changé.</span><span class="sxs-lookup"><span data-stu-id="d067d-134">Some events do not necessarily mean that the state of the UI has changed.</span></span> <span data-ttu-id="d067d-135">Par exemple, si l’utilisateur passe à un champ d’entrée de texte, puis clique sur un bouton pour mettre à jour le champ, un événement de [**\_ \_ TextChangedEventId de texte UIA**](uiauto-event-ids.md) est déclenché, même si l’utilisateur n’a pas réellement modifié le texte.</span><span class="sxs-lookup"><span data-stu-id="d067d-135">For example, if the user tabs to a text entry field, and then clicks a button to update the field, a [**UIA\_Text\_TextChangedEventId**](uiauto-event-ids.md) event is raised, even if the user did not actually change the text.</span></span> <span data-ttu-id="d067d-136">Pendant le traitement d'un événement, une application cliente peut être amenée à vérifier ce qui a réellement changé avant d'agir.</span><span class="sxs-lookup"><span data-stu-id="d067d-136">When processing an event, it may be necessary for a client application to check whether anything has actually changed before taking action.</span></span>

<span data-ttu-id="d067d-137">Les événements suivants peuvent être déclenchés même quand l'état de l'interface utilisateur n'a pas changé.</span><span class="sxs-lookup"><span data-stu-id="d067d-137">The following events may be raised even when the state of the UI has not changed.</span></span>

-   <span data-ttu-id="d067d-138">[**UIA \_ AutomationPropertyChangedEventId**](uiauto-event-ids.md) (selon la propriété qui a été modifiée)</span><span class="sxs-lookup"><span data-stu-id="d067d-138">[**UIA\_AutomationPropertyChangedEventId**](uiauto-event-ids.md) (depending on the property that has changed)</span></span>
-   [<span data-ttu-id="d067d-139">**UIA \_ SelectionItem \_ ElementSelectedEventId**</span><span class="sxs-lookup"><span data-stu-id="d067d-139">**UIA\_SelectionItem\_ElementSelectedEventId**</span></span>](uiauto-event-ids.md)
-   [<span data-ttu-id="d067d-140">**\_InvalidatedEventId de sélection UIA \_**</span><span class="sxs-lookup"><span data-stu-id="d067d-140">**UIA\_Selection\_InvalidatedEventId**</span></span>](uiauto-event-ids.md)
-   [<span data-ttu-id="d067d-141">**\_TextChangedEventId de texte UIA \_**</span><span class="sxs-lookup"><span data-stu-id="d067d-141">**UIA\_Text\_TextChangedEventId**</span></span>](uiauto-event-ids.md)

<span data-ttu-id="d067d-142">Pour obtenir une description de tous les événements UI Automation, consultez [identificateurs d’événements](uiauto-event-ids.md).</span><span class="sxs-lookup"><span data-stu-id="d067d-142">For a description of all UI Automation events, see [Event Identifiers](uiauto-event-ids.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="d067d-143">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="d067d-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d067d-144">Abonnement à des événements UI Automation</span><span class="sxs-lookup"><span data-stu-id="d067d-144">Subscribing to UI Automation Events</span></span>](uiauto-eventsforclients.md)
</dt> </dl>

 

 