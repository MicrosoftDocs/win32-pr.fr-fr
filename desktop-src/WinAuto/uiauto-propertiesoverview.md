---
title: Vue d'ensemble des propriétés UI Automation
description: Les fournisseurs UI Automation Microsoft exposent des propriétés sur les éléments UI Automation. Les propriétés permettent aux applications clientes de récupérer des informations sur les contrôles.
ms.assetid: 35f017cb-f50a-4680-9f01-5079aa59da73
keywords:
- UI Automation, vue d’ensemble des propriétés
- UI Automation, propriétés et événements
- UI Automation, événements et propriétés
- Propriétés, à propos de
- Propriétés, identificateurs
- Propriétés, valeurs
- Propriétés, événements
- événements, propriétés
- Propriétés, dynamiques
- propriétés dynamiques
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0f4e5e1b29ae516059a531b17d50d0631282f82
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104190688"
---
# <a name="ui-automation-properties-overview"></a><span data-ttu-id="12931-114">Vue d'ensemble des propriétés UI Automation</span><span class="sxs-lookup"><span data-stu-id="12931-114">UI Automation Properties Overview</span></span>

<span data-ttu-id="12931-115">Les fournisseurs UI Automation Microsoft exposent des propriétés sur les éléments UI Automation.</span><span class="sxs-lookup"><span data-stu-id="12931-115">Microsoft UI Automation providers expose properties on UI Automation elements.</span></span> <span data-ttu-id="12931-116">Les propriétés permettent aux applications clientes de récupérer des informations sur les contrôles.</span><span class="sxs-lookup"><span data-stu-id="12931-116">Properties enable client applications to retrieve information about controls.</span></span>

<span data-ttu-id="12931-117">UI Automation expose deux types différents de propriétés : les *Propriétés des éléments Automation* et les *propertes de modèle de contrôle*.</span><span class="sxs-lookup"><span data-stu-id="12931-117">UI Automation exposes two different kinds of properties: *automation element properties*, and *control pattern propertes*.</span></span> <span data-ttu-id="12931-118">Les propriétés de l’élément Automation consistent en un ensemble commun de propriétés, telles que Name, AcceleratorKey et ClassName, qui sont exposées par tous les éléments UI Automation, quel que soit le type de contrôle.</span><span class="sxs-lookup"><span data-stu-id="12931-118">The automation element properties consist of a common set of properties, such as Name, AcceleratorKey, and ClassName, that are exposed by all UI Automation elements, regardless of the control type.</span></span> <span data-ttu-id="12931-119">La plupart des propriétés d’élément Automation sont des valeurs statiques.</span><span class="sxs-lookup"><span data-stu-id="12931-119">Most automation element properties are static values.</span></span>

<span data-ttu-id="12931-120">Les propriétés de modèle de contrôle sont celles qui sont exposées par un contrôle qui prend en charge un modèle de contrôle particulier.</span><span class="sxs-lookup"><span data-stu-id="12931-120">Control pattern properties are those that are exposed by a control that supports a particular control pattern.</span></span> <span data-ttu-id="12931-121">Chaque modèle de contrôle a un ensemble correspondant de propriétés de modèle de contrôle que le contrôle doit exposer.</span><span class="sxs-lookup"><span data-stu-id="12931-121">Each control pattern has a corresponding set of control pattern properties that the control must expose.</span></span> <span data-ttu-id="12931-122">Par exemple, un contrôle qui prend en charge le modèle de contrôle [Grid](uiauto-implementinggrid.md) expose les propriétés ColumnCount et RowCount.</span><span class="sxs-lookup"><span data-stu-id="12931-122">For example, a control that supports the [Grid](uiauto-implementinggrid.md) control pattern exposes the ColumnCount and RowCount properties.</span></span> <span data-ttu-id="12931-123">La plupart des propriétés de modèle de contrôle sont des valeurs dynamiques.</span><span class="sxs-lookup"><span data-stu-id="12931-123">Most control pattern properties are dynamic values.</span></span>

<span data-ttu-id="12931-124">Cette rubrique contient les sections suivantes.</span><span class="sxs-lookup"><span data-stu-id="12931-124">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="12931-125">Identificateurs de propriété</span><span class="sxs-lookup"><span data-stu-id="12931-125">Property Identifiers</span></span>](#property-identifiers)
-   [<span data-ttu-id="12931-126">Valeurs de propriété</span><span class="sxs-lookup"><span data-stu-id="12931-126">Property Values</span></span>](#property-values)
-   [<span data-ttu-id="12931-127">Propriétés et événements</span><span class="sxs-lookup"><span data-stu-id="12931-127">Properties and Events</span></span>](#properties-and-events)
-   [<span data-ttu-id="12931-128">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="12931-128">Related topics</span></span>](#related-topics)

## <a name="property-identifiers"></a><span data-ttu-id="12931-129">Identificateurs de propriété</span><span class="sxs-lookup"><span data-stu-id="12931-129">Property Identifiers</span></span>

<span data-ttu-id="12931-130">Chaque propriété est identifiée par une valeur de type **PROPERTYID** appelée *identificateur de propriété* (ID).</span><span class="sxs-lookup"><span data-stu-id="12931-130">Every property is identified by a **PROPERTYID** numeric value called a *property identifier* (ID).</span></span> <span data-ttu-id="12931-131">Les fournisseurs et les clients utilisent les ID numériques dans les appels de méthode tels que [**IRawElementProviderAdviseEvents :: AdviseEventAdded**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementprovideradviseevents-adviseeventadded) et [**IUIAutomationElement :: GetCachedPropertyValue**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcachedpropertyvalue) pour identifier les demandes de propriété.</span><span class="sxs-lookup"><span data-stu-id="12931-131">Providers and clients use the numeric IDs in method calls such as [**IRawElementProviderAdviseEvents::AdviseEventAdded**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementprovideradviseevents-adviseeventadded) and [**IUIAutomationElement::GetCachedPropertyValue**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcachedpropertyvalue) to identify property requests.</span></span> <span data-ttu-id="12931-132">Pour obtenir une description détaillée de chaque identificateur de propriété UI Automation, y compris le type de données et la valeur par défaut de chaque propriété, consultez [identificateurs de propriété](uiauto-entry-propids.md).</span><span class="sxs-lookup"><span data-stu-id="12931-132">For a detailed description of each UI Automation property identifier, including the data type and default value of each property, see [Property Identifiers](uiauto-entry-propids.md).</span></span>

## <a name="property-values"></a><span data-ttu-id="12931-133">Valeurs de la propriété</span><span class="sxs-lookup"><span data-stu-id="12931-133">Property Values</span></span>

<span data-ttu-id="12931-134">Toutes les propriétés sont en lecture seule, même si certaines peuvent être modifiées à l’aide de méthodes qui agissent sur le contrôle, telles que [**IDockProvider :: SetDockPosition**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idockprovider-setdockposition) (Provider) ou [**IUIAutomationDockPattern :: SetDockPosition**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationdockpattern-setdockposition) (client).</span><span class="sxs-lookup"><span data-stu-id="12931-134">All properties are read-only, although some can be changed by using methods that act on the control, such as [**IDockProvider::SetDockPosition**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idockprovider-setdockposition) (provider) or [**IUIAutomationDockPattern::SetDockPosition**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationdockpattern-setdockposition) (client).</span></span>

<span data-ttu-id="12931-135">Pour plus d’informations sur la récupération des valeurs de propriété, consultez [extraction de propriétés à partir d’éléments UI Automation](uiauto-propertiesforclients.md).</span><span class="sxs-lookup"><span data-stu-id="12931-135">For information about retrieving property values, see [Retrieving Properties from UI Automation Elements](uiauto-propertiesforclients.md).</span></span>

## <a name="properties-and-events"></a><span data-ttu-id="12931-136">Propriétés et événements</span><span class="sxs-lookup"><span data-stu-id="12931-136">Properties and Events</span></span>

<span data-ttu-id="12931-137">Le concept des *événements de modification de propriété* est étroitement associé aux propriétés d’UI Automation.</span><span class="sxs-lookup"><span data-stu-id="12931-137">Closely associated with the properties in UI Automation is the concept of *property-changed events*.</span></span> <span data-ttu-id="12931-138">Pour les propriétés dynamiques, une application cliente a besoin d’un moyen de savoir qu’une valeur de propriété a changé, afin qu’elle puisse mettre à jour son cache d’informations ou réagir aux nouvelles informations d’une autre façon.</span><span class="sxs-lookup"><span data-stu-id="12931-138">For dynamic properties, a client application needs a way to know that a property value has changed, so that it can update its cache of information or react to the new information in some other way.</span></span> <span data-ttu-id="12931-139">Les clients peuvent s’inscrire pour écouter les événements de modification de propriété sur n’importe quelle propriété.</span><span class="sxs-lookup"><span data-stu-id="12931-139">Clients can register to listen for property-changed events on any property.</span></span>

<span data-ttu-id="12931-140">Les fournisseurs déclenchent des événements quand un événement de l’interface utilisateur change.</span><span class="sxs-lookup"><span data-stu-id="12931-140">Providers raise events when something in the UI changes.</span></span> <span data-ttu-id="12931-141">Par exemple, si une case à cocher est activée ou désactivée, un événement de modification de propriété est déclenché par l’implémentation du fournisseur du modèle de contrôle [Toggle](uiauto-implementingtoggle.md) .</span><span class="sxs-lookup"><span data-stu-id="12931-141">For example, if a check box is selected or cleared, a property-changed event is raised by the provider implementation of the [Toggle](uiauto-implementingtoggle.md) control pattern.</span></span> <span data-ttu-id="12931-142">Les fournisseurs peuvent déclencher des événements de manière sélective, selon que les clients écoutent tous les événements ou seulement des événements spécifiques.</span><span class="sxs-lookup"><span data-stu-id="12931-142">Providers can raise events selectively, depending on whether any clients are listening for events, or listening for specific events.</span></span>

<span data-ttu-id="12931-143">Toutes les modifications de propriété ne déclenchent pas nécessairement des événements. Cela dépend entièrement de l’implémentation du fournisseur UI Automation pour l’élément.</span><span class="sxs-lookup"><span data-stu-id="12931-143">Not all property changes raise events; that is entirely up to the implementation of the UI Automation provider for the element.</span></span> <span data-ttu-id="12931-144">Par exemple, les fournisseurs de proxy standard pour les zones de liste ne déclenchent pas d’événement de modification de propriété lorsque la propriété de sélection change.</span><span class="sxs-lookup"><span data-stu-id="12931-144">For example, the standard proxy providers for list boxes do not raise a property-changed event when the Selection property changes.</span></span> <span data-ttu-id="12931-145">Dans ce cas, l’application doit écouter l’événement déclenché lorsque la sélection change ([**UIA \_ SelectionItem \_ ElementSelectedEventId**](uiauto-event-ids.md)).</span><span class="sxs-lookup"><span data-stu-id="12931-145">In this case, the application must listen for the event raised when the selection changes ([**UIA\_SelectionItem\_ElementSelectedEventId**](uiauto-event-ids.md)).</span></span>

<span data-ttu-id="12931-146">Les clients écoutent les événements en s’abonnant à eux, comme décrit dans [abonnement à des événements UI Automation](uiauto-eventsforclients.md).</span><span class="sxs-lookup"><span data-stu-id="12931-146">Clients listen for events by subscribing to them, as described at [Subscribing to UI Automation Events](uiauto-eventsforclients.md).</span></span> <span data-ttu-id="12931-147">Pour les événements de modification de propriété en particulier, les clients doivent implémenter [**IUIAutomationPropertyChangedEventHandler**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationpropertychangedeventhandler) et passer l’interface à [**IUIAutomation :: AddPropertyChangedEventHandler**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-addpropertychangedeventhandler) ou [**IUIAutomation :: AddPropertyChangedEventHandlerNativeArray**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-addpropertychangedeventhandlernativearray).</span><span class="sxs-lookup"><span data-stu-id="12931-147">For property-changed events in particular, clients must implement [**IUIAutomationPropertyChangedEventHandler**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationpropertychangedeventhandler) and pass the interface to [**IUIAutomation::AddPropertyChangedEventHandler**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-addpropertychangedeventhandler) or [**IUIAutomation::AddPropertyChangedEventHandlerNativeArray**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-addpropertychangedeventhandlernativearray).</span></span>

## <a name="related-topics"></a><span data-ttu-id="12931-148">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="12931-148">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="12931-149">**Informations de référence**</span><span class="sxs-lookup"><span data-stu-id="12931-149">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="12931-150">**GetCurrentPropertyValue**</span><span class="sxs-lookup"><span data-stu-id="12931-150">**GetCurrentPropertyValue**</span></span>](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpropertyvalue)
</dt> <dt>

[<span data-ttu-id="12931-151">**GetCurrentPropertyValueEx**</span><span class="sxs-lookup"><span data-stu-id="12931-151">**GetCurrentPropertyValueEx**</span></span>](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpropertyvalueex)
</dt> <dt>

[<span data-ttu-id="12931-152">**GetCachedPropertyValue**</span><span class="sxs-lookup"><span data-stu-id="12931-152">**GetCachedPropertyValue**</span></span>](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcachedpropertyvalue)
</dt> <dt>

[<span data-ttu-id="12931-153">**GetCachedPropertyValueEx**</span><span class="sxs-lookup"><span data-stu-id="12931-153">**GetCachedPropertyValueEx**</span></span>](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcachedpropertyvalueex)
</dt> <dt>

<span data-ttu-id="12931-154">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="12931-154">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="12931-155">Vue d'ensemble des modèles de contrôle UI Automation</span><span class="sxs-lookup"><span data-stu-id="12931-155">UI Automation Control Patterns Overview</span></span>](uiauto-controlpatternsoverview.md)
</dt> <dt>

[<span data-ttu-id="12931-156">Vue d'ensemble des types de contrôle UI Automation</span><span class="sxs-lookup"><span data-stu-id="12931-156">UI Automation Control Types Overview</span></span>](uiauto-controltypesoverview.md)
</dt> <dt>

[<span data-ttu-id="12931-157">Vue d'ensemble des événements UI Automation</span><span class="sxs-lookup"><span data-stu-id="12931-157">UI Automation Events Overview</span></span>](uiauto-eventsoverview.md)
</dt> </dl>

 

 




