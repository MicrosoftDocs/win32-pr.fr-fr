---
title: Basculer le modèle de contrôle
description: Fournit des instructions et des conventions pour l’implémentation de IToggleProvider, y compris des informations sur les propriétés et les méthodes. Le modèle de contrôle Toggle est utilisé pour prendre en charge les contrôles qui peuvent parcourir un ensemble d’États et conserver un État une fois défini.
ms.assetid: 9fd1232b-199a-41e6-81b0-667c7e463d09
keywords:
- UI Automation, implémenter le modèle de contrôle Toggle
- UI Automation, basculer le modèle de contrôle
- UI Automation, IToggleProvider
- IToggleProvider
- implémentation des modèles de contrôle Toggle d’UI Automation
- Activer/désactiver les modèles de contrôle
- modèles de contrôle, IToggleProvider
- modèles de contrôle, implémenter le basculement d’UI Automation
- modèles de contrôle, bascule
- interfaces, IToggleProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 723d45326fdf9942682a318282ce4a9784df489c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104379755"
---
# <a name="toggle-control-pattern"></a><span data-ttu-id="0e7d2-114">Basculer le modèle de contrôle</span><span class="sxs-lookup"><span data-stu-id="0e7d2-114">Toggle Control Pattern</span></span>

<span data-ttu-id="0e7d2-115">Fournit des instructions et des conventions pour l’implémentation de [**IToggleProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itoggleprovider), y compris des informations sur les propriétés et les méthodes.</span><span class="sxs-lookup"><span data-stu-id="0e7d2-115">Describes guidelines and conventions for implementing [**IToggleProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itoggleprovider), including information about properties and methods.</span></span> <span data-ttu-id="0e7d2-116">Le modèle de contrôle **Toggle** est utilisé pour prendre en charge les contrôles qui peuvent parcourir un ensemble d’États et conserver un État une fois défini.</span><span class="sxs-lookup"><span data-stu-id="0e7d2-116">The **Toggle** control pattern is used to support controls that can cycle through a set of states and maintain a state once set.</span></span>

<span data-ttu-id="0e7d2-117">Pour obtenir des exemples de contrôles qui implémentent ce modèle de contrôle, consultez [types de contrôle et leurs modèles de contrôle pris en charge](uiauto-controlpatternmapping.md).</span><span class="sxs-lookup"><span data-stu-id="0e7d2-117">For examples of controls that implement this control pattern, see [Control Types and Their Supported Control Patterns](uiauto-controlpatternmapping.md).</span></span>

<span data-ttu-id="0e7d2-118">Cette rubrique contient les sections suivantes.</span><span class="sxs-lookup"><span data-stu-id="0e7d2-118">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="0e7d2-119">Conventions et directives d'implémentation</span><span class="sxs-lookup"><span data-stu-id="0e7d2-119">Implementation Guidelines and Conventions</span></span>](#implementation-guidelines-and-conventions)
-   [<span data-ttu-id="0e7d2-120">Membres requis pour **IToggleProvider**</span><span class="sxs-lookup"><span data-stu-id="0e7d2-120">Required Members for **IToggleProvider**</span></span>](#required-members-for-itoggleprovider)
-   [<span data-ttu-id="0e7d2-121">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="0e7d2-121">Related topics</span></span>](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a><span data-ttu-id="0e7d2-122">Conventions et directives d'implémentation</span><span class="sxs-lookup"><span data-stu-id="0e7d2-122">Implementation Guidelines and Conventions</span></span>

<span data-ttu-id="0e7d2-123">Lorsque vous implémentez le modèle de contrôle **Toggle** , notez les conventions et recommandations suivantes :</span><span class="sxs-lookup"><span data-stu-id="0e7d2-123">When implementing the **Toggle** control pattern, note the following guidelines and conventions:</span></span>

-   <span data-ttu-id="0e7d2-124">Les contrôles qui ne conservent pas l’État lorsqu’ils sont activés, tels que les boutons, les boutons de barre d’outils et les liens hypertexte, doivent implémenter [**IInvokeProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iinvokeprovider) à la place.</span><span class="sxs-lookup"><span data-stu-id="0e7d2-124">Controls that do not maintain state when activated, such as buttons, toolbar buttons, and hyperlinks, must implement [**IInvokeProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iinvokeprovider) instead.</span></span>
-   <span data-ttu-id="0e7d2-125">Un contrôle doit parcourir ses États de basculement ([**ToggleState**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-togglestate)) dans l’ordre suivant : **ToggleState \_ sur**, **ToggleState \_ off** et, s’il est pris en charge, **ToggleState \_ indéterminé**.</span><span class="sxs-lookup"><span data-stu-id="0e7d2-125">A control must cycle through its toggle states ([**ToggleState**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-togglestate)) in the following order: **ToggleState\_On**, **ToggleState\_Off** and, if supported, **ToggleState\_Indeterminate**.</span></span>
-   <span data-ttu-id="0e7d2-126">L’option **bascule** ne fournit pas de méthode d’état défini en raison de problèmes liés à la configuration directe d’une case à cocher à trois États sans parcourir sa séquence [**ToggleState**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-togglestate) appropriée.</span><span class="sxs-lookup"><span data-stu-id="0e7d2-126">**Toggle** does not provide a set-state method because of issues surrounding the direct setting of a three-state check box without cycling through its appropriate [**ToggleState**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-togglestate) sequence.</span></span>
-   <span data-ttu-id="0e7d2-127">Le contrôle de case d’option n’implémente pas [**IToggleProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itoggleprovider), car il n’est pas en mesure de parcourir ses États valides.</span><span class="sxs-lookup"><span data-stu-id="0e7d2-127">The radio button control does not implement [**IToggleProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itoggleprovider), because it is not capable of cycling through its valid states.</span></span>

## <a name="required-members-for-itoggleprovider"></a><span data-ttu-id="0e7d2-128">Membres requis pour **IToggleProvider**</span><span class="sxs-lookup"><span data-stu-id="0e7d2-128">Required Members for **IToggleProvider**</span></span>

<span data-ttu-id="0e7d2-129">Les propriétés et méthodes suivantes sont requises pour implémenter l’interface [**IToggleProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itoggleprovider) .</span><span class="sxs-lookup"><span data-stu-id="0e7d2-129">The following properties and methods are required for implementing the [**IToggleProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itoggleprovider) interface.</span></span>



| <span data-ttu-id="0e7d2-130">Membres nécessaires</span><span class="sxs-lookup"><span data-stu-id="0e7d2-130">Required members</span></span>                                          | <span data-ttu-id="0e7d2-131">Type de membre</span><span class="sxs-lookup"><span data-stu-id="0e7d2-131">Member type</span></span> | <span data-ttu-id="0e7d2-132">Notes</span><span class="sxs-lookup"><span data-stu-id="0e7d2-132">Notes</span></span> |
|-----------------------------------------------------------|-------------|-------|
| [<span data-ttu-id="0e7d2-133">**Bascule**</span><span class="sxs-lookup"><span data-stu-id="0e7d2-133">**Toggle**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itoggleprovider-toggle)           | <span data-ttu-id="0e7d2-134">Méthode</span><span class="sxs-lookup"><span data-stu-id="0e7d2-134">Method</span></span>      | <span data-ttu-id="0e7d2-135">Aucun</span><span class="sxs-lookup"><span data-stu-id="0e7d2-135">None</span></span>  |
| [<span data-ttu-id="0e7d2-136">**ToggleState**</span><span class="sxs-lookup"><span data-stu-id="0e7d2-136">**ToggleState**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itoggleprovider-get_togglestate) | <span data-ttu-id="0e7d2-137">Propriété</span><span class="sxs-lookup"><span data-stu-id="0e7d2-137">Property</span></span>    | <span data-ttu-id="0e7d2-138">Aucun</span><span class="sxs-lookup"><span data-stu-id="0e7d2-138">None</span></span>  |



 

<span data-ttu-id="0e7d2-139">Ce modèle de contrôle n’est associé aucun événement.</span><span class="sxs-lookup"><span data-stu-id="0e7d2-139">This control pattern has no associated events.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0e7d2-140">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="0e7d2-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0e7d2-141">Types de contrôle et leurs modèles de contrôle pris en charge</span><span class="sxs-lookup"><span data-stu-id="0e7d2-141">Control Types and Their Supported Control Patterns</span></span>](uiauto-controlpatternmapping.md)
</dt> <dt>

[<span data-ttu-id="0e7d2-142">Vue d'ensemble des modèles de contrôle UI Automation</span><span class="sxs-lookup"><span data-stu-id="0e7d2-142">UI Automation Control Patterns Overview</span></span>](uiauto-controlpatternsoverview.md)
</dt> <dt>

[<span data-ttu-id="0e7d2-143">Vue d’ensemble de l’arborescence UI Automation</span><span class="sxs-lookup"><span data-stu-id="0e7d2-143">UI Automation Tree Overview</span></span>](uiauto-treeoverview.md)
</dt> </dl>

 

 




