---
title: Value (modèle de contrôle)
description: Fournit des instructions et des conventions pour l’implémentation de IValueProvider, y compris des informations sur les propriétés et les méthodes.
ms.assetid: 6b11d281-aca7-4548-853c-e7322999825d
keywords:
- UI Automation, implémenter le modèle de contrôle value
- UI Automation, modèle de contrôle de valeur
- UI Automation, IValueProvider
- IValueProvider
- implémentation des modèles de contrôle value d’UI Automation
- Modèles de contrôle de valeur
- modèles de contrôle, IValueProvider
- modèles de contrôle, implémenter la valeur UI Automation
- modèles de contrôle, valeur
- interfaces, IValueProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40633a21fdd6b59a2aa35c34258037582a647f05
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104382295"
---
# <a name="value-control-pattern"></a><span data-ttu-id="b831e-113">Value (modèle de contrôle)</span><span class="sxs-lookup"><span data-stu-id="b831e-113">Value Control Pattern</span></span>

<span data-ttu-id="b831e-114">Fournit des instructions et des conventions pour l’implémentation de [**IValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivalueprovider), y compris des informations sur les propriétés et les méthodes.</span><span class="sxs-lookup"><span data-stu-id="b831e-114">Describes guidelines and conventions for implementing [**IValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivalueprovider), including information about properties and methods.</span></span> <span data-ttu-id="b831e-115">Le modèle de contrôle **value** est utilisé pour prendre en charge les contrôles qui ont une valeur intrinsèque qui ne couvre pas une plage et qui peuvent être représentés sous forme de chaîne.</span><span class="sxs-lookup"><span data-stu-id="b831e-115">The **Value** control pattern is used to support controls that have an intrinsic value not spanning a range and that can be represented as a string.</span></span>

<span data-ttu-id="b831e-116">La chaîne de valeur peut être modifiable, en fonction du contrôle et de ses paramètres.</span><span class="sxs-lookup"><span data-stu-id="b831e-116">The value string can be editable, depending on the control and its settings.</span></span> <span data-ttu-id="b831e-117">Pour obtenir des exemples de contrôles qui implémentent ce modèle de contrôle, consultez [types de contrôle et leurs modèles de contrôle pris en charge](uiauto-controlpatternmapping.md).</span><span class="sxs-lookup"><span data-stu-id="b831e-117">For examples of controls that implement this control pattern, see [Control Types and Their Supported Control Patterns](uiauto-controlpatternmapping.md).</span></span>

<span data-ttu-id="b831e-118">Cette rubrique contient les sections suivantes.</span><span class="sxs-lookup"><span data-stu-id="b831e-118">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="b831e-119">Conventions et directives d'implémentation</span><span class="sxs-lookup"><span data-stu-id="b831e-119">Implementation Guidelines and Conventions</span></span>](#implementation-guidelines-and-conventions)
-   [<span data-ttu-id="b831e-120">Membres requis pour **IValueProvider**</span><span class="sxs-lookup"><span data-stu-id="b831e-120">Required Members for **IValueProvider**</span></span>](#required-members-for-ivalueprovider)
-   [<span data-ttu-id="b831e-121">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="b831e-121">Related topics</span></span>](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a><span data-ttu-id="b831e-122">Conventions et directives d'implémentation</span><span class="sxs-lookup"><span data-stu-id="b831e-122">Implementation Guidelines and Conventions</span></span>

<span data-ttu-id="b831e-123">Lorsque vous implémentez le modèle de contrôle **value** , notez les conventions et recommandations suivantes :</span><span class="sxs-lookup"><span data-stu-id="b831e-123">When implementing the **Value** control pattern, note the following guidelines and conventions:</span></span>

-   <span data-ttu-id="b831e-124">Les contrôles tels qu’un élément de liste ou un élément d’arborescence doivent prendre en charge le modèle de contrôle **value** si la valeur de l’un des éléments est modifiable, quel que soit le mode d’édition actuel du contrôle.</span><span class="sxs-lookup"><span data-stu-id="b831e-124">Controls such as a list item or tree item must support the **Value** control pattern if the value of any of the items is editable, regardless of the current edit mode of the control.</span></span> <span data-ttu-id="b831e-125">Le contrôle parent doit également prendre en charge le modèle de contrôle **value** si les éléments enfants sont modifiables.</span><span class="sxs-lookup"><span data-stu-id="b831e-125">The parent control must also support the **Value** control pattern if the child items are editable.</span></span> <span data-ttu-id="b831e-126">L’illustration suivante montre un exemple d’élément de liste modifiable.</span><span class="sxs-lookup"><span data-stu-id="b831e-126">The following image shows an example of an editable list item.</span></span>

    ![Illustration montrant un élément de liste modifiable](images/uia-valuepattern-editable-listitem.jpg)

- <span data-ttu-id="b831e-128">Les contrôles d’édition à une seule ligne et à plusieurs lignes doivent implémenter [**ITextProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextprovider) pour exposer leur contenu en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="b831e-128">Single and multi-line edit controls must implement [**ITextProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextprovider) to expose their read-only content.</span></span>
- <span data-ttu-id="b831e-129">Les contrôles d’édition sur plusieurs lignes doivent implémenter [**IValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivalueprovider) si leur contenu peut être modifié.</span><span class="sxs-lookup"><span data-stu-id="b831e-129">Multi-line edit controls must implement [**IValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivalueprovider) if their contents can be changed.</span></span>
- <span data-ttu-id="b831e-130">[**IValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivalueprovider) ne prend pas en charge la récupération des informations de mise en forme ou des valeurs de sous-chaîne.</span><span class="sxs-lookup"><span data-stu-id="b831e-130">[**IValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivalueprovider) does not support the retrieval of formatting information or substring values.</span></span> <span data-ttu-id="b831e-131">Implémentez [**ITextProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextprovider) dans ces scénarios.</span><span class="sxs-lookup"><span data-stu-id="b831e-131">Implement [**ITextProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextprovider) in these scenarios.</span></span>
- <span data-ttu-id="b831e-132">[**IValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivalueprovider) doit être implémenté par des contrôles tels que le contrôle de sélection de sélecteur de couleurs de Microsoft Word (Voir l’image suivante), qui prend en charge le mappage de chaînes entre une valeur de couleur (par exemple, « jaune ») et une valeur [RVB](/windows/win32/api/wingdi/nf-wingdi-rgb) interne équivalente.</span><span class="sxs-lookup"><span data-stu-id="b831e-132">[**IValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivalueprovider) must be implemented by controls such as the color picker selection control from Microsoft Word (see the following image), which supports string mapping between a color value (for example, "yellow") and an equivalent internal [RGB](/windows/win32/api/wingdi/nf-wingdi-rgb) value.</span></span>

    ![Illustration montrant le mappage de la chaîne d’échantillons de couleurs](images/uia-valuepattern-colorpicker.jpg)

- <span data-ttu-id="b831e-134">La propriété **IsEnabled** d’un contrôle doit avoir la valeur **true** et sa propriété [**ITextProvider :: IsReadOnly**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ivalueprovider-get_isreadonly) la valeur **false** avant d’autoriser un appel à [**ITextProvider :: SetValue**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ivalueprovider-setvalue).</span><span class="sxs-lookup"><span data-stu-id="b831e-134">A control should have its **IsEnabled** property set to **TRUE** and its [**ITextProvider::IsReadOnly**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ivalueprovider-get_isreadonly) property set to **FALSE** before allowing a call to [**ITextProvider::SetValue**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ivalueprovider-setvalue).</span></span>

## <a name="required-members-for-ivalueprovider"></a><span data-ttu-id="b831e-135">Membres requis pour **IValueProvider**</span><span class="sxs-lookup"><span data-stu-id="b831e-135">Required Members for **IValueProvider**</span></span>

<span data-ttu-id="b831e-136">Les propriétés et méthodes suivantes sont requises pour implémenter l’interface [**IValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivalueprovider) .</span><span class="sxs-lookup"><span data-stu-id="b831e-136">The following properties and methods are required for implementing the [**IValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivalueprovider) interface.</span></span>



| <span data-ttu-id="b831e-137">Membres nécessaires</span><span class="sxs-lookup"><span data-stu-id="b831e-137">Required members</span></span>                                       | <span data-ttu-id="b831e-138">Type de membre</span><span class="sxs-lookup"><span data-stu-id="b831e-138">Member type</span></span> | <span data-ttu-id="b831e-139">Notes</span><span class="sxs-lookup"><span data-stu-id="b831e-139">Notes</span></span> |
|--------------------------------------------------------|-------------|-------|
| [<span data-ttu-id="b831e-140">**IsReadOnly**</span><span class="sxs-lookup"><span data-stu-id="b831e-140">**IsReadOnly**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ivalueprovider-get_isreadonly) | <span data-ttu-id="b831e-141">Propriété</span><span class="sxs-lookup"><span data-stu-id="b831e-141">Property</span></span>    | <span data-ttu-id="b831e-142">Aucun</span><span class="sxs-lookup"><span data-stu-id="b831e-142">None</span></span>  |
| [<span data-ttu-id="b831e-143">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="b831e-143">**Value**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ivalueprovider-get_value)           | <span data-ttu-id="b831e-144">Propriété</span><span class="sxs-lookup"><span data-stu-id="b831e-144">Property</span></span>    | <span data-ttu-id="b831e-145">Aucun</span><span class="sxs-lookup"><span data-stu-id="b831e-145">None</span></span>  |
| [<span data-ttu-id="b831e-146">**SetValue**</span><span class="sxs-lookup"><span data-stu-id="b831e-146">**SetValue**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ivalueprovider-setvalue)     | <span data-ttu-id="b831e-147">Méthode</span><span class="sxs-lookup"><span data-stu-id="b831e-147">Method</span></span>      | <span data-ttu-id="b831e-148">Aucun</span><span class="sxs-lookup"><span data-stu-id="b831e-148">None</span></span>  |



 

<span data-ttu-id="b831e-149">Ce modèle de contrôle n’est associé aucun événement.</span><span class="sxs-lookup"><span data-stu-id="b831e-149">This control pattern has no associated events.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b831e-150">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="b831e-150">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b831e-151">Types de contrôle et leurs modèles de contrôle pris en charge</span><span class="sxs-lookup"><span data-stu-id="b831e-151">Control Types and Their Supported Control Patterns</span></span>](uiauto-controlpatternmapping.md)
</dt> <dt>

[<span data-ttu-id="b831e-152">Vue d'ensemble des modèles de contrôle UI Automation</span><span class="sxs-lookup"><span data-stu-id="b831e-152">UI Automation Control Patterns Overview</span></span>](uiauto-controlpatternsoverview.md)
</dt> <dt>

[<span data-ttu-id="b831e-153">Vue d’ensemble de l’arborescence UI Automation</span><span class="sxs-lookup"><span data-stu-id="b831e-153">UI Automation Tree Overview</span></span>](uiauto-treeoverview.md)
</dt> <dt>

[<span data-ttu-id="b831e-154">Modèles de contrôle Text et TextRange</span><span class="sxs-lookup"><span data-stu-id="b831e-154">Text and TextRange Control Patterns</span></span>](uiauto-implementingtextandtextrange.md)
</dt> </dl>

 

 