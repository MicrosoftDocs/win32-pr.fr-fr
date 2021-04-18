---
title: Modèle de contrôle SynchronizedInput
description: Fournit des instructions et des conventions pour l’implémentation de ISynchronizedInputProvider, y compris des informations sur les propriétés et les méthodes.
ms.assetid: 3e2d65ea-8093-4e65-b43e-28478ec74607
keywords:
- UI Automation, implémentation du modèle de contrôle SynchronizedInput
- UI Automation, modèle de contrôle SynchronizedInput
- UI Automation, ISynchronizedInputProvider
- ISynchronizedInputProvider
- implémentation des modèles de contrôle SynchronizedInput d’UI Automation
- Modèles de contrôle SynchronizedInput
- modèles de contrôle, ISynchronizedInputProvider
- modèles de contrôle, implémenter des SynchronizedInput UI Automation
- modèles de contrôle, SynchronizedInput
- interfaces, ISynchronizedInputProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 105e75163fdac742adaad6b778c251b4b7b8ae70
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106511842"
---
# <a name="synchronizedinput-control-pattern"></a><span data-ttu-id="df003-113">Modèle de contrôle SynchronizedInput</span><span class="sxs-lookup"><span data-stu-id="df003-113">SynchronizedInput Control Pattern</span></span>

<span data-ttu-id="df003-114">Fournit des instructions et des conventions pour l’implémentation de [**ISynchronizedInputProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-isynchronizedinputprovider), y compris des informations sur les propriétés et les méthodes.</span><span class="sxs-lookup"><span data-stu-id="df003-114">Describes guidelines and conventions for implementing [**ISynchronizedInputProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-isynchronizedinputprovider), including information about properties and methods.</span></span> <span data-ttu-id="df003-115">Le modèle de contrôle **SynchronizedInput** permet aux applications clientes UI Automation de Microsoft de diriger l’entrée de la souris ou du clavier vers un élément d’interface utilisateur spécifique.</span><span class="sxs-lookup"><span data-stu-id="df003-115">The **SynchronizedInput** control pattern enables Microsoft UI Automation client applications to direct the mouse or keyboard input to a specific UI element.</span></span>

<span data-ttu-id="df003-116">Ce modèle de contrôle est généralement utilisé dans les scripts de test automatisés pour envoyer une entrée de souris ou de clavier à un élément spécifique de l’interface utilisateur, puis vérifier que l’élément a reçu l’entrée.</span><span class="sxs-lookup"><span data-stu-id="df003-116">This control pattern is typically used in automated test scripts to send mouse or keyboard input to a specific user-interface element, and then verify that the element received the input.</span></span>

<span data-ttu-id="df003-117">Cette rubrique contient les sections suivantes.</span><span class="sxs-lookup"><span data-stu-id="df003-117">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="df003-118">Conventions et directives d'implémentation</span><span class="sxs-lookup"><span data-stu-id="df003-118">Implementation Guidelines and Conventions</span></span>](#implementation-guidelines-and-conventions)
-   [<span data-ttu-id="df003-119">Membres requis pour **ISynchronizedInputProvider**</span><span class="sxs-lookup"><span data-stu-id="df003-119">Required Members for **ISynchronizedInputProvider**</span></span>](#required-members-for-isynchronizedinputprovider)
-   [<span data-ttu-id="df003-120">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="df003-120">Related topics</span></span>](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a><span data-ttu-id="df003-121">Conventions et directives d'implémentation</span><span class="sxs-lookup"><span data-stu-id="df003-121">Implementation Guidelines and Conventions</span></span>

<span data-ttu-id="df003-122">Lorsque vous implémentez le modèle de contrôle **SynchronizedInput** , notez les conventions et recommandations suivantes :</span><span class="sxs-lookup"><span data-stu-id="df003-122">When implementing the **SynchronizedInput** control pattern, note the following guidelines and conventions:</span></span>

-   <span data-ttu-id="df003-123">Quand la méthode [**ISynchronizedInputProvider :: StartListening**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-isynchronizedinputprovider-startlistening) est appelée, le fournisseur UI Automation doit commencer à vérifier l’entrée du type spécifié, puis effectuer l’une des actions suivantes :</span><span class="sxs-lookup"><span data-stu-id="df003-123">When the [**ISynchronizedInputProvider::StartListening**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-isynchronizedinputprovider-startlistening) method is called, the UI Automation provider should start checking for input of the specified type, and then take one of the following actions:</span></span>
    -   <span data-ttu-id="df003-124">Lorsque l’entrée correspondante est trouvée pour l’élément, le fournisseur doit déclencher l’événement [**UIA \_ InputReachedTargetEventId**](uiauto-event-ids.md) .</span><span class="sxs-lookup"><span data-stu-id="df003-124">When matching input is found for the element, the provider should raise the [**UIA\_InputReachedTargetEventId**](uiauto-event-ids.md) event.</span></span>
    -   <span data-ttu-id="df003-125">Lorsque l’entrée correspondante est trouvée, mais qu’elle a atteint un autre élément, le fournisseur doit déclencher l’événement [**UIA \_ InputReachedOtherElementEventId**](uiauto-event-ids.md) .</span><span class="sxs-lookup"><span data-stu-id="df003-125">When matching input is found, but it reached a different element, the provider should raise the [**UIA\_InputReachedOtherElementEventId**](uiauto-event-ids.md) event.</span></span>
    -   <span data-ttu-id="df003-126">Si une entrée incompatible est trouvée, le fournisseur doit ignorer l’entrée et déclencher l’événement [**UIA \_ InputDiscardedEventId**](uiauto-event-ids.md) .</span><span class="sxs-lookup"><span data-stu-id="df003-126">When mismatched input is found, the provider should discard the input and raise the [**UIA\_InputDiscardedEventId**](uiauto-event-ids.md) event.</span></span>
-   <span data-ttu-id="df003-127">Le fournisseur UI Automation doit ignorer l’entrée s’il s’agit d’un élément autre que l’élément actuel.</span><span class="sxs-lookup"><span data-stu-id="df003-127">The UI Automation provider must discard the input if it is for an element other than the current element.</span></span>
-   <span data-ttu-id="df003-128">Lorsque l’élément reçoit l’entrée, ou lorsque la méthode [**ISynchronizedInputProvider :: Cancel**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-isynchronizedinputprovider-cancel) est appelée, le fournisseur arrête la vérification de l’entrée et se poursuit normalement.</span><span class="sxs-lookup"><span data-stu-id="df003-128">When the element receives the input, or when the [**ISynchronizedInputProvider::Cancel**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-isynchronizedinputprovider-cancel) method is called, the provider stops checking input and continues as normal.</span></span>
-   <span data-ttu-id="df003-129">Si [**ISynchronizedInputProvider :: StartListening**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-isynchronizedinputprovider-startlistening) est appelé alors que le fournisseur est déjà à l’écoute de l’entrée, le fournisseur doit retourner [**UIA \_ E \_ INVALIDOPERATION**](uiauto-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="df003-129">If [**ISynchronizedInputProvider::StartListening**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-isynchronizedinputprovider-startlistening) is called when the provider is already listening for input, the provider should return [**UIA\_E\_INVALIDOPERATION**](uiauto-error-codes.md).</span></span>

## <a name="required-members-for-isynchronizedinputprovider"></a><span data-ttu-id="df003-130">Membres requis pour **ISynchronizedInputProvider**</span><span class="sxs-lookup"><span data-stu-id="df003-130">Required Members for **ISynchronizedInputProvider**</span></span>

<span data-ttu-id="df003-131">Les propriétés, méthodes et événements suivants sont requis pour implémenter l’interface [**ISynchronizedInputProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-isynchronizedinputprovider) .</span><span class="sxs-lookup"><span data-stu-id="df003-131">The following properties, methods, and events are required for implementing the [**ISynchronizedInputProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-isynchronizedinputprovider) interface.</span></span>



| <span data-ttu-id="df003-132">Membres nécessaires</span><span class="sxs-lookup"><span data-stu-id="df003-132">Required members</span></span>                                                                         | <span data-ttu-id="df003-133">Type de membre</span><span class="sxs-lookup"><span data-stu-id="df003-133">Member type</span></span> | <span data-ttu-id="df003-134">Notes</span><span class="sxs-lookup"><span data-stu-id="df003-134">Notes</span></span> |
|------------------------------------------------------------------------------------------|-------------|-------|
| [<span data-ttu-id="df003-135">**StartListening**</span><span class="sxs-lookup"><span data-stu-id="df003-135">**StartListening**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-isynchronizedinputprovider-startlistening)               | <span data-ttu-id="df003-136">Méthode</span><span class="sxs-lookup"><span data-stu-id="df003-136">Method</span></span>      | <span data-ttu-id="df003-137">Aucun</span><span class="sxs-lookup"><span data-stu-id="df003-137">None</span></span>  |
| [<span data-ttu-id="df003-138">**Annuler**</span><span class="sxs-lookup"><span data-stu-id="df003-138">**Cancel**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-isynchronizedinputprovider-cancel)                               | <span data-ttu-id="df003-139">Méthode</span><span class="sxs-lookup"><span data-stu-id="df003-139">Method</span></span>      | <span data-ttu-id="df003-140">Aucun</span><span class="sxs-lookup"><span data-stu-id="df003-140">None</span></span>  |
| [<span data-ttu-id="df003-141">**UIA \_ InputReachedTargetEventId**</span><span class="sxs-lookup"><span data-stu-id="df003-141">**UIA\_InputReachedTargetEventId**</span></span>](uiauto-event-ids.md) | <span data-ttu-id="df003-142">Événement</span><span class="sxs-lookup"><span data-stu-id="df003-142">Event</span></span>       | <span data-ttu-id="df003-143">Aucun</span><span class="sxs-lookup"><span data-stu-id="df003-143">None</span></span>  |



 

## <a name="related-topics"></a><span data-ttu-id="df003-144">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="df003-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="df003-145">Vue d'ensemble des modèles de contrôle UI Automation</span><span class="sxs-lookup"><span data-stu-id="df003-145">UI Automation Control Patterns Overview</span></span>](uiauto-controlpatternsoverview.md)
</dt> </dl>

 

 




