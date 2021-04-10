---
title: Compréhension des problèmes liés aux threads
description: Cette rubrique décrit les scénarios courants de Threading pour les implémentations du client Microsoft UI Automation et explique comment éviter les problèmes qui peuvent se produire si un client utilise incorrectement le Threading.
ms.assetid: 0772969a-da55-488e-8b21-7368434df8a9
keywords:
- clients, problèmes liés aux threads UI Automation
- clients, problèmes liés aux threads
- clients, modèle de thread du gestionnaire d’événements
- clients, modèle de thread du gestionnaire d’événements UI Automation
- clients, affinité UI Automation
- clients, affinité
- UI Automation, problèmes liés aux threads
- UI Automation, modèle de thread du gestionnaire d’événements
- UI Automation, affinité
- problèmes liés aux threads
- modèle de thread du gestionnaire d’événements
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a002132efe4055bb247c7d7290e271e153ac297e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104031293"
---
# <a name="understanding-threading-issues"></a><span data-ttu-id="03f92-114">Compréhension des problèmes liés aux threads</span><span class="sxs-lookup"><span data-stu-id="03f92-114">Understanding Threading Issues</span></span>

<span data-ttu-id="03f92-115">Cette rubrique décrit les scénarios courants de Threading pour les implémentations du client Microsoft UI Automation et explique comment éviter les problèmes qui peuvent se produire si un client utilise incorrectement le Threading.</span><span class="sxs-lookup"><span data-stu-id="03f92-115">This topic describes common threading scenarios for Microsoft UI Automation client implementations and explains how to avoid problems that can occur if a client uses threading incorrectly.</span></span>

<span data-ttu-id="03f92-116">Cette rubrique contient les sections suivantes :</span><span class="sxs-lookup"><span data-stu-id="03f92-116">This topic contains the following sections:</span></span>

-   [<span data-ttu-id="03f92-117">UI Automation et thread d’interface utilisateur</span><span class="sxs-lookup"><span data-stu-id="03f92-117">UI Automation and the UI Thread</span></span>](#ui-automation-and-the-ui-thread)
-   [<span data-ttu-id="03f92-118">Modèle de thread pour les gestionnaires d’événements</span><span class="sxs-lookup"><span data-stu-id="03f92-118">Threading Model for Event Handlers</span></span>](#threading-model-for-event-handlers)
-   [<span data-ttu-id="03f92-119">Affinité COM Apartment sur Windows 64 bits</span><span class="sxs-lookup"><span data-stu-id="03f92-119">COM Apartment Affinity on 64-bit Windows</span></span>](#com-apartment-affinity-on-64-bit-windows)
-   [<span data-ttu-id="03f92-120">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="03f92-120">Related topics</span></span>](#related-topics)

## <a name="ui-automation-and-the-ui-thread"></a><span data-ttu-id="03f92-121">UI Automation et thread d’interface utilisateur</span><span class="sxs-lookup"><span data-stu-id="03f92-121">UI Automation and the UI Thread</span></span>

<span data-ttu-id="03f92-122">En raison de la façon dont UI Automation utilise les messages Windows, des conflits peuvent se produire lorsqu’une application cliente tente d’interagir avec sa propre interface utilisateur sur le thread d’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="03f92-122">Because of the way UI Automation uses Windows messages, conflicts can occur when a client application attempts to interact with its own UI on the UI thread.</span></span> <span data-ttu-id="03f92-123">Ces conflits peuvent entraîner des performances très lentes, voire entraîner l’arrêt de la réponse de l’application.</span><span class="sxs-lookup"><span data-stu-id="03f92-123">These conflicts can lead to very slow performance, or even cause the application to stop responding.</span></span>

<span data-ttu-id="03f92-124">Si votre application cliente est destinée à interagir avec tous les éléments sur le bureau, y compris sa propre interface utilisateur, vous devez effectuer tous les appels UI Automation à partir d’un thread distinct.</span><span class="sxs-lookup"><span data-stu-id="03f92-124">If your client application is intended to interact with all elements on the desktop, including its own UI, you should make all UI Automation calls from a separate thread.</span></span> <span data-ttu-id="03f92-125">Cela comprend la localisation d’éléments, par exemple, à l’aide de [**IUIAutomationTreeWalker**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtreewalker) ou de la méthode [**IUIAutomationElement :: FindAll**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-findall) et à l’aide de modèles de contrôle.</span><span class="sxs-lookup"><span data-stu-id="03f92-125">This includes locating elements, for example, by using [**IUIAutomationTreeWalker**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtreewalker) or the [**IUIAutomationElement::FindAll**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-findall) method and using control patterns.</span></span> <span data-ttu-id="03f92-126">Ce thread ne doit pas posséder de fenêtres. il doit s’agir d’un thread de modèle COM (Component Object Apartment) (MTA), qui initialise COM en appelant [CoInitializeEx](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) avec l’indicateur **coinit \_ multithread** .</span><span class="sxs-lookup"><span data-stu-id="03f92-126">This thread should not own any windows, and should be a Component Object Model (COM) Multithreaded Apartment (MTA) model thread (one that initializes COM by calling [CoInitializeEx](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) with the **COINIT\_MULTITHREADED** flag.)</span></span>

<span data-ttu-id="03f92-127">Il est possible d’effectuer des appels d’automatisation d’interface utilisateur dans un gestionnaire d’événements UI Automation, car le gestionnaire d’événements est toujours appelé sur un thread autre qu’un thread d’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="03f92-127">It is safe to make UI Automation calls in a UI Automation event handler, because the event handler is always called on a non-UI thread.</span></span> <span data-ttu-id="03f92-128">Toutefois, lors de l’abonnement à des événements qui peuvent provenir de l’interface utilisateur de votre application cliente, vous devez effectuer l’appel à [**IUIAutomation :: AddAutomationEventHandler**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-addautomationeventhandler), ou une méthode associée, sur un thread non-interface utilisateur (qui doit également être un thread MTA).</span><span class="sxs-lookup"><span data-stu-id="03f92-128">However, when subscribing to events that may originate from your client application UI, you must make the call to [**IUIAutomation::AddAutomationEventHandler**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-addautomationeventhandler), or a related method, on a non-UI thread (which should also be an MTA thread).</span></span> <span data-ttu-id="03f92-129">Supprimez les gestionnaires d’événements situés sur un même thread.</span><span class="sxs-lookup"><span data-stu-id="03f92-129">Remove event handlers on the same thread.</span></span>

<span data-ttu-id="03f92-130">Un client UI Automation ne doit pas utiliser plusieurs threads pour ajouter ou supprimer des gestionnaires d’événements.</span><span class="sxs-lookup"><span data-stu-id="03f92-130">A UI Automation client should not use multiple threads to add or remove event handlers.</span></span> <span data-ttu-id="03f92-131">Un comportement inattendu peut se produire si un gestionnaire d’événements est ajouté ou supprimé alors qu’un autre est ajouté ou supprimé dans le même processus client.</span><span class="sxs-lookup"><span data-stu-id="03f92-131">Unexpected behavior can result if one event handler is being added or removed while another is being added or removed in the same client process.</span></span>

## <a name="threading-model-for-event-handlers"></a><span data-ttu-id="03f92-132">Modèle de thread pour les gestionnaires d’événements</span><span class="sxs-lookup"><span data-stu-id="03f92-132">Threading Model for Event Handlers</span></span>

<span data-ttu-id="03f92-133">Un client UI Automation doit utiliser le modèle de thread MTA COM pour les threads qui implémentent des gestionnaires d’événements.</span><span class="sxs-lookup"><span data-stu-id="03f92-133">A UI Automation client should use the COM MTA threading model for threads that implement event handlers.</span></span> <span data-ttu-id="03f92-134">L’utilisation du modèle STA (Single-Threaded Apartment) peut entraîner des problèmes tels que l’empêchement des clients de supprimer des gestionnaires d’événements du thread.</span><span class="sxs-lookup"><span data-stu-id="03f92-134">Using the Single-threaded Apartment (STA) model can cause problems such as preventing clients from removing event handlers from the thread.</span></span>

## <a name="com-apartment-affinity-on-64-bit-windows"></a><span data-ttu-id="03f92-135">Affinité COM Apartment sur Windows 64 bits</span><span class="sxs-lookup"><span data-stu-id="03f92-135">COM Apartment Affinity on 64-bit Windows</span></span>

<span data-ttu-id="03f92-136">Selon la spécification COM, la durée de vie d’un objet distant est régie par la durée de vie du cloisonnement dans lequel la fonction [CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) est appelée pour créer l’objet.</span><span class="sxs-lookup"><span data-stu-id="03f92-136">According to the COM specification, the lifetime of a remote object is governed by the lifetime of the apartment where the [CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) function is called to create the object.</span></span> <span data-ttu-id="03f92-137">Lorsque le cloisonnement d’origine s’arrête, l’objet distant est également libéré.</span><span class="sxs-lookup"><span data-stu-id="03f92-137">When the original apartment shuts down, the remote object is also released.</span></span>

<span data-ttu-id="03f92-138">Pour les clients UI Automation, ce comportement COM peut signifier que la durée de vie du programme d’assistance 32/64 distant (créé par UIAutomationCore.dll) utilisé par un élément 32 bits est régie par la durée de vie cloisonnée du thread qui a créé l’élément.</span><span class="sxs-lookup"><span data-stu-id="03f92-138">For UI Automation clients, this COM behavior can mean that the lifetime of the remote 32/64 helper (created by UIAutomationCore.dll) used by a 32-bit element is governed by the apartment lifetime of the thread that created the element.</span></span> <span data-ttu-id="03f92-139">Si le client UI Automation marshale l’élément à un autre thread, l’élément peut devenir invalidé lorsque le cloisonnement d’origine s’arrête.</span><span class="sxs-lookup"><span data-stu-id="03f92-139">If the UI Automation client marshals the element to another thread, the element can become invalidated when the originating apartment shuts down.</span></span> <span data-ttu-id="03f92-140">Le client UI Automation doit gérer ces problèmes correctement en interceptant les erreurs lors de l’utilisation d’éléments d’automatisation marshalés.</span><span class="sxs-lookup"><span data-stu-id="03f92-140">The UI Automation client should handle these issues gracefully by catching errors while using marshaled automation elements.</span></span>

<span data-ttu-id="03f92-141">Le même problème peut se produire avec un client UI Automation 32 bits qui comporte des éléments 64 bits.</span><span class="sxs-lookup"><span data-stu-id="03f92-141">The same issue can occur with a 32-bit UI Automation client that has 64-bit elements.</span></span>

## <a name="related-topics"></a><span data-ttu-id="03f92-142">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="03f92-142">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="03f92-143">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="03f92-143">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="03f92-144">Obtention d'éléments UI Automation</span><span class="sxs-lookup"><span data-stu-id="03f92-144">Obtaining UI Automation Elements</span></span>](uiauto-obtainingelements.md)
</dt> <dt>

[<span data-ttu-id="03f92-145">Abonnement à des événements UI Automation</span><span class="sxs-lookup"><span data-stu-id="03f92-145">Subscribing to UI Automation Events</span></span>](uiauto-eventsforclients.md)
</dt> <dt>

[<span data-ttu-id="03f92-146">Vue d'ensemble des événements UI Automation</span><span class="sxs-lookup"><span data-stu-id="03f92-146">UI Automation Events Overview</span></span>](uiauto-eventsoverview.md)
</dt> <dt>

<span data-ttu-id="03f92-147">**Autres ressources**</span><span class="sxs-lookup"><span data-stu-id="03f92-147">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="03f92-148">INFORMATIONS : descriptions et travaux des modèles de threads OLE</span><span class="sxs-lookup"><span data-stu-id="03f92-148">INFO: Descriptions and Workings of OLE Threading Models</span></span>](https://support.microsoft.com/kb/150777)
</dt> </dl>

 

 