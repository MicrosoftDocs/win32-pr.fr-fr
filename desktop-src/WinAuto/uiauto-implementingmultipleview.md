---
title: Modèle de contrôle MultipleView
description: Fournit des instructions et des conventions pour l’implémentation de IMultipleViewProvider, y compris des informations sur les propriétés et les méthodes.
ms.assetid: c67e7e4f-d2c7-4fca-8e8a-9b6565afa4ed
keywords:
- UI Automation, implémentation du modèle de contrôle MultipleView
- UI Automation, modèle de contrôle MultipleView
- UI Automation, IMultipleViewProvider
- IMultipleViewProvider
- implémentation des modèles de contrôle MultipleView d’UI Automation
- Modèles de contrôle MultipleView
- modèles de contrôle, IMultipleViewProvider
- modèles de contrôle, implémenter des MultipleView UI Automation
- modèles de contrôle, MultipleView
- interfaces, IMultipleViewProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4bc5d1991e99f1338853aac528111d8ec3ca3c2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104380085"
---
# <a name="multipleview-control-pattern"></a><span data-ttu-id="8894f-113">Modèle de contrôle MultipleView</span><span class="sxs-lookup"><span data-stu-id="8894f-113">MultipleView Control Pattern</span></span>

<span data-ttu-id="8894f-114">Fournit des instructions et des conventions pour l’implémentation de [**IMultipleViewProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-imultipleviewprovider), y compris des informations sur les propriétés et les méthodes.</span><span class="sxs-lookup"><span data-stu-id="8894f-114">Describes guidelines and conventions for implementing [**IMultipleViewProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-imultipleviewprovider), including information about properties and methods.</span></span> <span data-ttu-id="8894f-115">Des liens vers des références supplémentaires sont répertoriés à la fin de la rubrique.</span><span class="sxs-lookup"><span data-stu-id="8894f-115">Links to additional references are listed at the end of the topic.</span></span> <span data-ttu-id="8894f-116">Le modèle de contrôle **MultipleView** est utilisé pour prendre en charge les contrôles qui fournissent et peuvent basculer entre plusieurs représentations des mêmes informations ou le même jeu de contrôles enfants.</span><span class="sxs-lookup"><span data-stu-id="8894f-116">The **MultipleView** control pattern is used to support controls that provide, and are able to switch between, multiple representations of the same information or the same set of child controls.</span></span>

<span data-ttu-id="8894f-117">Voici des exemples de contrôles qui peuvent présenter plusieurs vues, notamment le mode liste (qui peut afficher son contenu sous forme de miniatures, vignettes, icônes ou détails), graphiques Microsoft Excel (secteurs, courbes, barres, valeurs de cellule avec une formule), documents Microsoft Word (normal, page Web, mise en page, disposition de lecture, plan), calendrier Microsoft Outlook (année, mois, semaine, jour) et peaux du lecteur Microsoft Windows Media.</span><span class="sxs-lookup"><span data-stu-id="8894f-117">Examples of controls that can present multiple views include the list view (which can show its contents as thumbnails, tiles, icons, or details), Microsoft Excel charts (pie, line, bar, cell value with a formula), Microsoft Word documents (normal, web layout, print layout, reading layout, outline), Microsoft Outlook calendar (year, month, week, day), and Microsoft Windows Media Player skins.</span></span> <span data-ttu-id="8894f-118">Les vues prises en charge sont déterminées par le développeur de contrôle et sont spécifiques à chaque contrôle.</span><span class="sxs-lookup"><span data-stu-id="8894f-118">The supported views are determined by the control developer and are specific to each control.</span></span>

<span data-ttu-id="8894f-119">Cette rubrique contient les sections suivantes.</span><span class="sxs-lookup"><span data-stu-id="8894f-119">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="8894f-120">Conventions et directives d'implémentation</span><span class="sxs-lookup"><span data-stu-id="8894f-120">Implementation Guidelines and Conventions</span></span>](#implementation-guidelines-and-conventions)
-   [<span data-ttu-id="8894f-121">Membres requis pour **IMultipleViewProvider**</span><span class="sxs-lookup"><span data-stu-id="8894f-121">Required Members for **IMultipleViewProvider**</span></span>](#required-members-for-imultipleviewprovider)
-   [<span data-ttu-id="8894f-122">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="8894f-122">Related topics</span></span>](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a><span data-ttu-id="8894f-123">Conventions et directives d'implémentation</span><span class="sxs-lookup"><span data-stu-id="8894f-123">Implementation Guidelines and Conventions</span></span>

<span data-ttu-id="8894f-124">Lorsque vous implémentez le modèle de contrôle **MultipleView** , notez les conventions et recommandations suivantes :</span><span class="sxs-lookup"><span data-stu-id="8894f-124">When implementing the **MultipleView** control pattern, note the following guidelines and conventions:</span></span>

-   <span data-ttu-id="8894f-125">[**IMultipleViewProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-imultipleviewprovider) doit également être implémenté sur un conteneur qui gère la vue actuelle s’il est différent d’un contrôle qui fournit la vue actuelle.</span><span class="sxs-lookup"><span data-stu-id="8894f-125">[**IMultipleViewProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-imultipleviewprovider) should also be implemented on a container that manages the current view if it is different from a control that provides the current view.</span></span> <span data-ttu-id="8894f-126">Par exemple, l’Explorateur Windows contient un contrôle de liste pour le contenu du dossier actuel, tandis que la vue du contrôle est gérée à partir de l’application de l’Explorateur Windows.</span><span class="sxs-lookup"><span data-stu-id="8894f-126">For example, Windows Explorer contains a list control for the current folder content while the view for the control is managed from the Windows Explorer application.</span></span>
-   <span data-ttu-id="8894f-127">Un contrôle qui est en mesure de trier son contenu n’est pas censé prendre en charge plusieurs vues.</span><span class="sxs-lookup"><span data-stu-id="8894f-127">A control that is able to sort its content is not considered to support multiple views.</span></span>
-   <span data-ttu-id="8894f-128">La collection de vues doit être identique sur l’ensemble des instances.</span><span class="sxs-lookup"><span data-stu-id="8894f-128">The collection of views must be identical across instances.</span></span>
-   <span data-ttu-id="8894f-129">Les noms des vues doivent pouvoir être utilisés dans la conversion de texte en parole, en braille et dans d’autres applications lisibles par l’homme.</span><span class="sxs-lookup"><span data-stu-id="8894f-129">View names must be suitable for use in text to speech, Braille, and other human-readable applications.</span></span>

## <a name="required-members-for-imultipleviewprovider"></a><span data-ttu-id="8894f-130">Membres requis pour **IMultipleViewProvider**</span><span class="sxs-lookup"><span data-stu-id="8894f-130">Required Members for **IMultipleViewProvider**</span></span>

<span data-ttu-id="8894f-131">Les propriétés et méthodes suivantes sont requises pour implémenter l’interface [**IMultipleViewProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-imultipleviewprovider) .</span><span class="sxs-lookup"><span data-stu-id="8894f-131">The following properties and methods are required for implementing the [**IMultipleViewProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-imultipleviewprovider) interface.</span></span>



| <span data-ttu-id="8894f-132">Membres nécessaires</span><span class="sxs-lookup"><span data-stu-id="8894f-132">Required members</span></span>                                                            | <span data-ttu-id="8894f-133">Type de membre</span><span class="sxs-lookup"><span data-stu-id="8894f-133">Member type</span></span> | <span data-ttu-id="8894f-134">Notes</span><span class="sxs-lookup"><span data-stu-id="8894f-134">Notes</span></span> |
|-----------------------------------------------------------------------------|-------------|-------|
| [<span data-ttu-id="8894f-135">**Appliquée**</span><span class="sxs-lookup"><span data-stu-id="8894f-135">**CurrentView**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-imultipleviewprovider-get_currentview)             | <span data-ttu-id="8894f-136">Propriété</span><span class="sxs-lookup"><span data-stu-id="8894f-136">Property</span></span>    | <span data-ttu-id="8894f-137">Aucun</span><span class="sxs-lookup"><span data-stu-id="8894f-137">None</span></span>  |
| [<span data-ttu-id="8894f-138">**GetSupportedViews**</span><span class="sxs-lookup"><span data-stu-id="8894f-138">**GetSupportedViews**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-imultipleviewprovider-getsupportedviews) | <span data-ttu-id="8894f-139">Méthode</span><span class="sxs-lookup"><span data-stu-id="8894f-139">Method</span></span>      | <span data-ttu-id="8894f-140">Aucun</span><span class="sxs-lookup"><span data-stu-id="8894f-140">None</span></span>  |
| [<span data-ttu-id="8894f-141">**GetViewName**</span><span class="sxs-lookup"><span data-stu-id="8894f-141">**GetViewName**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-imultipleviewprovider-getviewname)             | <span data-ttu-id="8894f-142">Méthode</span><span class="sxs-lookup"><span data-stu-id="8894f-142">Method</span></span>      | <span data-ttu-id="8894f-143">Aucun</span><span class="sxs-lookup"><span data-stu-id="8894f-143">None</span></span>  |
| [<span data-ttu-id="8894f-144">**SetCurrentView**</span><span class="sxs-lookup"><span data-stu-id="8894f-144">**SetCurrentView**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-imultipleviewprovider-setcurrentview)       | <span data-ttu-id="8894f-145">Méthode</span><span class="sxs-lookup"><span data-stu-id="8894f-145">Method</span></span>      | <span data-ttu-id="8894f-146">Aucun</span><span class="sxs-lookup"><span data-stu-id="8894f-146">None</span></span>  |



 

<span data-ttu-id="8894f-147">Ce modèle de contrôle n’est associé aucun événement.</span><span class="sxs-lookup"><span data-stu-id="8894f-147">This control pattern has no associated events.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8894f-148">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="8894f-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8894f-149">Types de contrôle et leurs modèles de contrôle pris en charge</span><span class="sxs-lookup"><span data-stu-id="8894f-149">Control Types and Their Supported Control Patterns</span></span>](uiauto-controlpatternmapping.md)
</dt> <dt>

[<span data-ttu-id="8894f-150">Vue d'ensemble des modèles de contrôle UI Automation</span><span class="sxs-lookup"><span data-stu-id="8894f-150">UI Automation Control Patterns Overview</span></span>](uiauto-controlpatternsoverview.md)
</dt> <dt>

[<span data-ttu-id="8894f-151">Vue d’ensemble de l’arborescence UI Automation</span><span class="sxs-lookup"><span data-stu-id="8894f-151">UI Automation Tree Overview</span></span>](uiauto-treeoverview.md)
</dt> <dt>

[<span data-ttu-id="8894f-152">Modèle de contrôle ExpandCollapse</span><span class="sxs-lookup"><span data-stu-id="8894f-152">ExpandCollapse Control Pattern</span></span>](uiauto-implementingexpandcollapse.md)
</dt> </dl>

 

 




