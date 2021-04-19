---
title: Récupération de propriétés à partir d’éléments UI Automation
description: Les propriétés des objets IUIAutomationElement contiennent des informations sur les éléments d’interface utilisateur, généralement les contrôles.
ms.assetid: e358fd67-22d0-4e43-a138-8afcc45f130e
keywords:
- clients, obtention d’éléments UI Automation
- clients, éléments UI Automation
- clients, propriétés
- clients, récupération des propriétés
- clients, propriétés UI Automation
- UI Automation, obtenir des éléments
- UI Automation, éléments
- UI Automation, propriétés
- UI Automation, récupérer des propriétés
- récupération des propriétés
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e199522dbefaa2f722a67b0ede57fe910b8ed63b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "106510491"
---
# <a name="retrieving-properties-from-ui-automation-elements"></a><span data-ttu-id="05515-113">Récupération de propriétés à partir d’éléments UI Automation</span><span class="sxs-lookup"><span data-stu-id="05515-113">Retrieving Properties from UI Automation Elements</span></span>

<span data-ttu-id="05515-114">Les propriétés des objets [**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) contiennent des informations sur les éléments d’interface utilisateur, généralement les contrôles.</span><span class="sxs-lookup"><span data-stu-id="05515-114">Properties on [**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) objects contain information about UI elements, usually controls.</span></span> <span data-ttu-id="05515-115">Les propriétés d’un élément sont génériques ; autrement dit, non spécifique à un type de contrôle.</span><span class="sxs-lookup"><span data-stu-id="05515-115">The properties of an element are generic; that is, not specific to a control type.</span></span> <span data-ttu-id="05515-116">Les propriétés spécifiques au contrôle d’un élément sont exposées par ses interfaces de modèle de contrôle.</span><span class="sxs-lookup"><span data-stu-id="05515-116">Control-specific properties of an element are exposed by its control pattern interfaces.</span></span>

<span data-ttu-id="05515-117">Les propriétés UI Automation de Microsoft sont en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="05515-117">Microsoft UI Automation properties are read-only.</span></span> <span data-ttu-id="05515-118">Pour définir les propriétés d’un contrôle, vous devez utiliser les méthodes du modèle de contrôle approprié.</span><span class="sxs-lookup"><span data-stu-id="05515-118">To set properties of a control, you must use the methods of the appropriate control pattern.</span></span> <span data-ttu-id="05515-119">Par exemple, utilisez [**IUIAutomationScrollPattern :: Scroll**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationscrollpattern-scroll) pour modifier les valeurs de position d’une fenêtre de défilement.</span><span class="sxs-lookup"><span data-stu-id="05515-119">For example, use [**IUIAutomationScrollPattern::Scroll**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationscrollpattern-scroll) to change the position values of a scrolling window.</span></span>

<span data-ttu-id="05515-120">Pour améliorer les performances, les valeurs de propriété des contrôles et des modèles de contrôle peuvent être mises en cache lorsque les éléments sont récupérés.</span><span class="sxs-lookup"><span data-stu-id="05515-120">To improve performance, property values of controls and control patterns can be cached when elements are retrieved.</span></span> <span data-ttu-id="05515-121">Pour plus d’informations, consultez [Caching UI Automation Properties and Control patterns](uiauto-cachingforclients.md).</span><span class="sxs-lookup"><span data-stu-id="05515-121">For more information, see [Caching UI Automation Properties and Control Patterns](uiauto-cachingforclients.md).</span></span>

<span data-ttu-id="05515-122">Cette rubrique contient les sections suivantes.</span><span class="sxs-lookup"><span data-stu-id="05515-122">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="05515-123">ID de propriété</span><span class="sxs-lookup"><span data-stu-id="05515-123">Property IDs</span></span>](#property-ids)
-   [<span data-ttu-id="05515-124">Conditions de propriété</span><span class="sxs-lookup"><span data-stu-id="05515-124">Property Conditions</span></span>](#property-conditions)
-   [<span data-ttu-id="05515-125">Récupération de propriétés</span><span class="sxs-lookup"><span data-stu-id="05515-125">Retrieving Properties</span></span>](#retrieving-properties)
-   [<span data-ttu-id="05515-126">Valeurs de propriété par défaut</span><span class="sxs-lookup"><span data-stu-id="05515-126">Default Property Values</span></span>](#default-property-values)
-   [<span data-ttu-id="05515-127">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="05515-127">Related topics</span></span>](#related-topics)

## <a name="property-ids"></a><span data-ttu-id="05515-128">ID de propriété</span><span class="sxs-lookup"><span data-stu-id="05515-128">Property IDs</span></span>

<span data-ttu-id="05515-129">Les identificateurs de propriété sont définis dans UIAutomationClient. h.</span><span class="sxs-lookup"><span data-stu-id="05515-129">Property identifiers are defined in Uiautomationclient.h.</span></span> <span data-ttu-id="05515-130">Ils permettent de spécifier des propriétés lorsque vous vous abonnez à des événements de modification de propriété, de récupérer des valeurs de propriété et de construire des conditions de propriété.</span><span class="sxs-lookup"><span data-stu-id="05515-130">They are used to specify properties when you subscribe to property-changed events, retrieve property values, and construct property conditions.</span></span> <span data-ttu-id="05515-131">Les identificateurs de propriété identifient également la propriété qui a changé lors de l’appel de [**IUIAutomationPropertyChangedEventHandler :: HandlePropertyChangedEvent**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationpropertychangedeventhandler-handlepropertychangedevent) .</span><span class="sxs-lookup"><span data-stu-id="05515-131">Property identifiers also identify the property that has changed when [**IUIAutomationPropertyChangedEventHandler::HandlePropertyChangedEvent**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationpropertychangedeventhandler-handlepropertychangedevent) is called.</span></span>

<span data-ttu-id="05515-132">Pour obtenir la liste des identificateurs de propriété UI Automation, consultez [identificateurs de propriété](uiauto-entry-propids.md).</span><span class="sxs-lookup"><span data-stu-id="05515-132">For a list of UI Automation property identifiers, see [Property Identifiers](uiauto-entry-propids.md).</span></span>

## <a name="property-conditions"></a><span data-ttu-id="05515-133">Conditions de propriété</span><span class="sxs-lookup"><span data-stu-id="05515-133">Property Conditions</span></span>

<span data-ttu-id="05515-134">Les ID de propriété sont utilisés dans la construction d’objets [**IUIAutomationPropertyCondition**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationpropertycondition) qui sont utilisés pour rechercher des éléments UI Automation.</span><span class="sxs-lookup"><span data-stu-id="05515-134">The property IDs are used in constructing [**IUIAutomationPropertyCondition**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationpropertycondition) objects that are used to find UI Automation elements.</span></span> <span data-ttu-id="05515-135">Par exemple, vous souhaiterez peut-être Rechercher un élément qui a un nom spécifique, ou tous les contrôles qui sont activés.</span><span class="sxs-lookup"><span data-stu-id="05515-135">For example, you might want to find an element that has a certain name, or all controls that are enabled.</span></span> <span data-ttu-id="05515-136">Chaque condition de propriété spécifie un identificateur de propriété et la valeur à laquelle la propriété doit correspondre.</span><span class="sxs-lookup"><span data-stu-id="05515-136">Each property condition specifies a property identifier and the value that the property must match.</span></span>

<span data-ttu-id="05515-137">Pour plus d’informations, consultez les rubriques de référence suivantes :</span><span class="sxs-lookup"><span data-stu-id="05515-137">For more information, see the following reference topics:</span></span>

-   [<span data-ttu-id="05515-138">**IUIAutomation::CreatePropertyCondition**</span><span class="sxs-lookup"><span data-stu-id="05515-138">**IUIAutomation::CreatePropertyCondition**</span></span>](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-createpropertycondition)
-   [<span data-ttu-id="05515-139">**IUIAutomation::CreatePropertyConditionEx**</span><span class="sxs-lookup"><span data-stu-id="05515-139">**IUIAutomation::CreatePropertyConditionEx**</span></span>](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-createpropertyconditionex)
-   [<span data-ttu-id="05515-140">**IUIAutomationElement :: FindFirst**</span><span class="sxs-lookup"><span data-stu-id="05515-140">**IUIAutomationElement::FindFirst**</span></span>](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-findfirst)
-   [<span data-ttu-id="05515-141">**IUIAutomationElement :: FindAll**</span><span class="sxs-lookup"><span data-stu-id="05515-141">**IUIAutomationElement::FindAll**</span></span>](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-findall)

## <a name="retrieving-properties"></a><span data-ttu-id="05515-142">Récupération de propriétés</span><span class="sxs-lookup"><span data-stu-id="05515-142">Retrieving Properties</span></span>

<span data-ttu-id="05515-143">Certaines propriétés génériques, ainsi que toutes les propriétés de modèle de contrôle, sont disponibles en tant que propriétés sur l’interface du modèle de contrôle ou [**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) et peuvent être récupérées à l’aide d’un accesseur, tel que [**IUIAutomationElement :: CurrentName**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentname) ou [**CachedDockPosition**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationdockpattern-get_cacheddockposition).</span><span class="sxs-lookup"><span data-stu-id="05515-143">Some generic properties, and all control pattern properties, are available as properties on the [**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) or control pattern interface and can be retrieved by using an accessor, such as [**IUIAutomationElement::CurrentName**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentname) or [**CachedDockPosition**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationdockpattern-get_cacheddockposition).</span></span>

<span data-ttu-id="05515-144">En outre, toute propriété en cours ou mise en cache (autre que les propriétés de modèle de contrôle) peut être récupérée à l’aide de l’une des méthodes suivantes :</span><span class="sxs-lookup"><span data-stu-id="05515-144">In addition, any current or cached property (other than control pattern properties) can be retrieved by using one of the following methods:</span></span>

-   [<span data-ttu-id="05515-145">**GetCurrentPropertyValue**</span><span class="sxs-lookup"><span data-stu-id="05515-145">**GetCurrentPropertyValue**</span></span>](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpropertyvalue)
-   [<span data-ttu-id="05515-146">**GetCurrentPropertyValueEx**</span><span class="sxs-lookup"><span data-stu-id="05515-146">**GetCurrentPropertyValueEx**</span></span>](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpropertyvalueex)
-   [<span data-ttu-id="05515-147">**GetCachedPropertyValue**</span><span class="sxs-lookup"><span data-stu-id="05515-147">**GetCachedPropertyValue**</span></span>](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcachedpropertyvalue)
-   [<span data-ttu-id="05515-148">**GetCachedPropertyValueEx**</span><span class="sxs-lookup"><span data-stu-id="05515-148">**GetCachedPropertyValueEx**</span></span>](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcachedpropertyvalueex)

<span data-ttu-id="05515-149">Ces méthodes offrent des performances légèrement meilleures et un accès à la gamme complète des propriétés.</span><span class="sxs-lookup"><span data-stu-id="05515-149">These methods offer slightly better performance and access to the full range of properties.</span></span> <span data-ttu-id="05515-150">Toutefois, les valeurs sont retournées dans les structures de [**type Variant**](/windows/win32/api/oaidl/ns-oaidl-variant) , tandis que les accesseurs de propriété individuels effectuent un cast de la valeur vers le type approprié.</span><span class="sxs-lookup"><span data-stu-id="05515-150">However, values are returned in [**VARIANT**](/windows/win32/api/oaidl/ns-oaidl-variant) structures, whereas the individual property accessors cast the value to the appropriate type.</span></span>

## <a name="default-property-values"></a><span data-ttu-id="05515-151">Valeurs de propriété par défaut</span><span class="sxs-lookup"><span data-stu-id="05515-151">Default Property Values</span></span>

<span data-ttu-id="05515-152">Si un fournisseur UI Automation n’implémente pas de propriété, UI Automation peut fournir une valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="05515-152">If a UI Automation provider does not implement a property, UI Automation can supply a default value.</span></span> <span data-ttu-id="05515-153">Par exemple, si le fournisseur d’un contrôle ne prend pas en charge la propriété identifiée par [**UIA \_ HelpTextPropertyId**](uiauto-automation-element-propids.md), UI Automation retourne une chaîne vide.</span><span class="sxs-lookup"><span data-stu-id="05515-153">For example, if the provider for a control does not support the property identified by [**UIA\_HelpTextPropertyId**](uiauto-automation-element-propids.md), UI Automation returns an empty string.</span></span> <span data-ttu-id="05515-154">De même, si le fournisseur ne prend pas en charge la propriété identifiée par [**UIA \_ IsDockPatternAvailablePropertyId**](uiauto-control-pattern-availability-propids.md), UI Automation retourne **false**.</span><span class="sxs-lookup"><span data-stu-id="05515-154">Similarly, if the provider does not support the property identified by [**UIA\_IsDockPatternAvailablePropertyId**](uiauto-control-pattern-availability-propids.md), UI Automation returns **FALSE**.</span></span>

<span data-ttu-id="05515-155">La différence entre [**IUIAutomationElement :: GetCurrentPropertyValue**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpropertyvalue) et [**GetCurrentPropertyValueEx**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpropertyvalueex) (et entre des paires similaires de méthodes) est que la méthode « ex » peut spécifier qu’aucune valeur par défaut ne doit être retournée.</span><span class="sxs-lookup"><span data-stu-id="05515-155">The difference between [**IUIAutomationElement::GetCurrentPropertyValue**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpropertyvalue) and [**GetCurrentPropertyValueEx**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpropertyvalueex) (and between similar pairs of methods) is that the "Ex" method can specify that no default value is to be returned.</span></span> <span data-ttu-id="05515-156">Dans ce cas, la valeur de retour est une constante unique spéciale, indiquant que la propriété n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="05515-156">In this case, the return value is a special unique constant, indicating that the property is not supported.</span></span> <span data-ttu-id="05515-157">À la réception de cette valeur, l’application peut fournir sa propre valeur ou simplement ignorer la propriété.</span><span class="sxs-lookup"><span data-stu-id="05515-157">On receiving this value, the application can supply its own value or simply ignore the property.</span></span>

## <a name="related-topics"></a><span data-ttu-id="05515-158">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="05515-158">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="05515-159">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="05515-159">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="05515-160">Vue d'ensemble des propriétés UI Automation</span><span class="sxs-lookup"><span data-stu-id="05515-160">UI Automation Properties Overview</span></span>](uiauto-propertiesoverview.md)
</dt> <dt>

[<span data-ttu-id="05515-161">Identificateurs de propriété</span><span class="sxs-lookup"><span data-stu-id="05515-161">Property Identifiers</span></span>](uiauto-entry-propids.md)
</dt> </dl>

 

 