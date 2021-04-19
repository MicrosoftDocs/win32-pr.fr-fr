---
title: Bibliothèque de contrôles de l’infrastructure du ruban Windows
description: Les rubriques contenues dans cette section décrivent l’ensemble des contrôles inclus avec l’infrastructure du ruban Windows. Les contrôles répertoriés ici sont les objets d’interface utilisateur d’un ruban qui exposent les fonctionnalités de commande.
ms.assetid: bda13e51-7e5f-4600-a6bd-9388bffd6ce2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 840b07bafe0c43cb7ab148a4413657b9722c409b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "106510896"
---
# <a name="windows-ribbon-framework-control-library"></a><span data-ttu-id="55b38-104">Bibliothèque de contrôles de l’infrastructure du ruban Windows</span><span class="sxs-lookup"><span data-stu-id="55b38-104">Windows Ribbon Framework Control Library</span></span>

<span data-ttu-id="55b38-105">Les rubriques contenues dans cette section décrivent l’ensemble des contrôles inclus avec l’infrastructure du ruban Windows.</span><span class="sxs-lookup"><span data-stu-id="55b38-105">The topics contained in this section describe the set of controls that are included with the Windows Ribbon framework.</span></span> <span data-ttu-id="55b38-106">Les contrôles répertoriés ici sont les objets d’interface utilisateur d’un ruban qui exposent les fonctionnalités de commande.</span><span class="sxs-lookup"><span data-stu-id="55b38-106">The controls listed here are the UI objects in a ribbon that expose Command functionality.</span></span>

-   [<span data-ttu-id="55b38-107">Introduction</span><span class="sxs-lookup"><span data-stu-id="55b38-107">Introduction</span></span>](#introduction)
-   [<span data-ttu-id="55b38-108">Les contrôles</span><span class="sxs-lookup"><span data-stu-id="55b38-108">The Controls</span></span>](#windows-ribbon-framework-control-library)
    -   [<span data-ttu-id="55b38-109">Contrôles de base</span><span class="sxs-lookup"><span data-stu-id="55b38-109">Basic Controls</span></span>](#basic-controls)
    -   [<span data-ttu-id="55b38-110">Contrôles de conteneur</span><span class="sxs-lookup"><span data-stu-id="55b38-110">Container Controls</span></span>](#container-controls)
    -   [<span data-ttu-id="55b38-111">Contrôles spécialisés</span><span class="sxs-lookup"><span data-stu-id="55b38-111">Specialized Controls</span></span>](#specialized-controls)
-   [<span data-ttu-id="55b38-112">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="55b38-112">Related topics</span></span>](#related-topics)

## <a name="introduction"></a><span data-ttu-id="55b38-113">Introduction</span><span class="sxs-lookup"><span data-stu-id="55b38-113">Introduction</span></span>

<span data-ttu-id="55b38-114">L’infrastructure du ruban est composée de composants tels que les [onglets](windowsribbon-controls-tab.md) et la [barre d’outils accès rapide](windowsribbon-controls-quickaccesstoolbar.md), qui fonctionnent ensemble pour offrir une expérience d’interface utilisateur riche.</span><span class="sxs-lookup"><span data-stu-id="55b38-114">The Ribbon framework is composed of components such as [Tabs](windowsribbon-controls-tab.md) and the [Quick Access Toolbar](windowsribbon-controls-quickaccesstoolbar.md), that work together to deliver a rich UI experience.</span></span> <span data-ttu-id="55b38-115">Individuellement, ces composants exposent différents types de commandes pour offrir aux clients une expérience organisée et prévisible sur les applications du ruban.</span><span class="sxs-lookup"><span data-stu-id="55b38-115">Individually, these components expose different types of Commands to give customers an organized, predictable experience across Ribbon applications.</span></span> <span data-ttu-id="55b38-116">Par exemple, chaque onglet expose des commandes relatives à la création et à l’action sur des parties spécifiques du contenu dans l’espace de travail de l’application, tandis que le menu de l' [application](windowsribbon-controls-applicationmenu.md) expose les fonctionnalités associées à un projet complet, tel qu’un document, une image ou un film entier.</span><span class="sxs-lookup"><span data-stu-id="55b38-116">For example, each Tab exposes Commands related to creating and acting on specific parts of the content within the application workspace, whereas the [Application Menu](windowsribbon-controls-applicationmenu.md) exposes functionality related to a complete project, such as an entire document, picture, or movie.</span></span>

<span data-ttu-id="55b38-117">Cette rubrique fournit une liste complète des contrôles du ruban et inclut une brève description de chaque contrôle, avec des liens vers une documentation plus détaillée, le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="55b38-117">This topic provides a comprehensive list of Ribbon controls and includes a brief description for each control, with links to more detailed documentation where available.</span></span>

## <a name="the-controls"></a><span data-ttu-id="55b38-118">Les contrôles</span><span class="sxs-lookup"><span data-stu-id="55b38-118">The Controls</span></span>

<span data-ttu-id="55b38-119">L’infrastructure du ruban est composée de deux [vues](windowsribbon-reference-elements-view.md): la vue du [**ruban**](windowsribbon-element-ribbon.md) et la vue [**ContextPopup**](windowsribbon-element-contextpopup.md) .</span><span class="sxs-lookup"><span data-stu-id="55b38-119">The Ribbon framework is composed of two [Views](windowsribbon-reference-elements-view.md): the [**Ribbon**](windowsribbon-element-ribbon.md) View and the [**ContextPopup**](windowsribbon-element-contextpopup.md) View.</span></span> <span data-ttu-id="55b38-120">Chaque vue peut héberger plusieurs composants qui jouent le rôle de conteneurs de présentation pour tous les contrôles rendus et gérés par l’infrastructure.</span><span class="sxs-lookup"><span data-stu-id="55b38-120">Each View can host several components that act as presentation containers for all controls that are rendered and managed by the framework.</span></span>

<span data-ttu-id="55b38-121">La vue [**du ruban**](windowsribbon-element-ribbon.md) héberge l’élément [**ApplicationMenu**](windowsribbon-element-applicationmenu.md) , l’élément [**QuickAccessToolbar**](windowsribbon-element-quickaccesstoolbar.md) et la barre de commandes du ruban tandis que la vue [**ContextPopup**](windowsribbon-element-contextpopup.md) héberge un élément [**ContextMenu**](windowsribbon-element-contextmenu.md) , un élément [**MiniToolbar**](windowsribbon-element-minitoolbar.md) , ou les deux.</span><span class="sxs-lookup"><span data-stu-id="55b38-121">The [**Ribbon**](windowsribbon-element-ribbon.md) View hosts the [**ApplicationMenu**](windowsribbon-element-applicationmenu.md) element, [**QuickAccessToolbar**](windowsribbon-element-quickaccesstoolbar.md) element, and ribbon command bar while the [**ContextPopup**](windowsribbon-element-contextpopup.md) View hosts a [**ContextMenu**](windowsribbon-element-contextmenu.md) element, a [**MiniToolbar**](windowsribbon-element-minitoolbar.md) element, or both.</span></span>

<span data-ttu-id="55b38-122">Chaque contrôle d’infrastructure est distingué par la fonctionnalité associée à son [**type de commande**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_commandtype).</span><span class="sxs-lookup"><span data-stu-id="55b38-122">Each framework control is distinguished by the functionality associated with its [**Command type**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_commandtype).</span></span>

### <a name="basic-controls"></a><span data-ttu-id="55b38-123">Contrôles de base</span><span class="sxs-lookup"><span data-stu-id="55b38-123">Basic Controls</span></span>

<span data-ttu-id="55b38-124">Les contrôles de base se composent d’un ou de plusieurs boutons qui peuvent être appelés par un clic de souris unique pour effectuer une action simple.</span><span class="sxs-lookup"><span data-stu-id="55b38-124">Basic controls consist of one or more buttons that can be invoked by a single mouse click to perform a simple action.</span></span>

> [!Note]  
> <span data-ttu-id="55b38-125">Le [**compteur**](windowsribbon-element-spinner.md) est une exception, car il contient un contrôle d’édition.</span><span class="sxs-lookup"><span data-stu-id="55b38-125">The [**Spinner**](windowsribbon-element-spinner.md) is an exception as it contains an edit control.</span></span>

 

<span data-ttu-id="55b38-126">Le tableau suivant répertorie les contrôles de base dans l’infrastructure du ruban.</span><span class="sxs-lookup"><span data-stu-id="55b38-126">The following table lists the basic controls in the Ribbon framework.</span></span>



| <span data-ttu-id="55b38-127">Contrôler</span><span class="sxs-lookup"><span data-stu-id="55b38-127">Control</span></span>                                                  | <span data-ttu-id="55b38-128">Élément de balisage</span><span class="sxs-lookup"><span data-stu-id="55b38-128">Markup Element</span></span>                                             |
|----------------------------------------------------------|------------------------------------------------------------|
| [<span data-ttu-id="55b38-129">Button</span><span class="sxs-lookup"><span data-stu-id="55b38-129">Button</span></span>](windowsribbon-controls-button.md)              | [<span data-ttu-id="55b38-130">**Bouton**</span><span class="sxs-lookup"><span data-stu-id="55b38-130">**Button**</span></span>](windowsribbon-element-button.md)             |
| [<span data-ttu-id="55b38-131">Case à cocher</span><span class="sxs-lookup"><span data-stu-id="55b38-131">Check Box</span></span>](windowsribbon-controls-checkbox.md)         | [<span data-ttu-id="55b38-132">**CheckBox**</span><span class="sxs-lookup"><span data-stu-id="55b38-132">**CheckBox**</span></span>](windowsribbon-element-checkbox.md)         |
| [<span data-ttu-id="55b38-133">Bouton aide</span><span class="sxs-lookup"><span data-stu-id="55b38-133">Help Button</span></span>](windowsribbon-controls-helpbutton.md)     | [<span data-ttu-id="55b38-134">**HelpButton**</span><span class="sxs-lookup"><span data-stu-id="55b38-134">**HelpButton**</span></span>](windowsribbon-element-helpbutton.md)     |
| [<span data-ttu-id="55b38-135">Spinner</span><span class="sxs-lookup"><span data-stu-id="55b38-135">Spinner</span></span>](windowsribbon-controls-spinner.md)            | [<span data-ttu-id="55b38-136">**Spinner**</span><span class="sxs-lookup"><span data-stu-id="55b38-136">**Spinner**</span></span>](windowsribbon-element-spinner.md)           |
| [<span data-ttu-id="55b38-137">Bouton bascule</span><span class="sxs-lookup"><span data-stu-id="55b38-137">Toggle Button</span></span>](windowsribbon-controls-togglebutton.md) | [<span data-ttu-id="55b38-138">**ToggleButton**</span><span class="sxs-lookup"><span data-stu-id="55b38-138">**ToggleButton**</span></span>](windowsribbon-element-togglebutton.md) |



 

### <a name="container-controls"></a><span data-ttu-id="55b38-139">Contrôles de conteneur</span><span class="sxs-lookup"><span data-stu-id="55b38-139">Container Controls</span></span>

<span data-ttu-id="55b38-140">Les contrôles conteneurs sont composés de groupes de contrôles, de menus, de listes ou d’éléments et de collections de commandes.</span><span class="sxs-lookup"><span data-stu-id="55b38-140">Container controls are composed of groups of controls, menus, lists, or item and Command collections.</span></span>

<span data-ttu-id="55b38-141">Le Framework distingue deux types de conteneurs, statiques et dynamiques.</span><span class="sxs-lookup"><span data-stu-id="55b38-141">The framework distinguishes between two types of containers, static and dynamic.</span></span>

### <a name="static-containers"></a><span data-ttu-id="55b38-142">Conteneurs statiques</span><span class="sxs-lookup"><span data-stu-id="55b38-142">Static Containers</span></span>

<span data-ttu-id="55b38-143">Les conteneurs statiques sont déclarés et remplis, ainsi que toutes les ressources associées, dans le fichier de balisage du ruban.</span><span class="sxs-lookup"><span data-stu-id="55b38-143">Static containers are declared and populated, along with all associated resources, in the Ribbon markup file.</span></span> <span data-ttu-id="55b38-144">Ces contrôles ne peuvent pas être modifiés au moment de l’exécution.</span><span class="sxs-lookup"><span data-stu-id="55b38-144">These controls cannot be modified at run time.</span></span>

<span data-ttu-id="55b38-145">Les avantages des contrôles statiques sont les suivants :</span><span class="sxs-lookup"><span data-stu-id="55b38-145">The advantages of static controls include the following:</span></span>

-   <span data-ttu-id="55b38-146">Prototypage rapide.</span><span class="sxs-lookup"><span data-stu-id="55b38-146">Rapid prototyping.</span></span> <span data-ttu-id="55b38-147">Les contrôles statiques permettent de créer rapidement un simulacre de ruban ressemblant à une conception de ruban finale qui ne requiert pas de code compliqué.</span><span class="sxs-lookup"><span data-stu-id="55b38-147">Static controls make it possible to quickly build a Ribbon mock-up resembling a final Ribbon design that requires no complicated code.</span></span>
-   <span data-ttu-id="55b38-148">Modifications simples.</span><span class="sxs-lookup"><span data-stu-id="55b38-148">Easy modifications.</span></span> <span data-ttu-id="55b38-149">La plupart des éléments, des attributs, des ressources et des mises en page de contrôles statiques peuvent être modifiés dans le balisage.</span><span class="sxs-lookup"><span data-stu-id="55b38-149">Most elements, attributes, resources, and layouts of static controls can be modified in markup.</span></span>
-   <span data-ttu-id="55b38-150">Interface utilisateur cohérente.</span><span class="sxs-lookup"><span data-stu-id="55b38-150">Consistent UI.</span></span> <span data-ttu-id="55b38-151">Les applications bien conçues fournissent une interface utilisateur cohérente et stable qui évite les modifications des menus et des listes au moment de l’exécution.</span><span class="sxs-lookup"><span data-stu-id="55b38-151">Well-designed applications provide a consistent and stable UI that avoids changes to menus and lists at run time.</span></span>

<span data-ttu-id="55b38-152">Le tableau suivant décrit les contrôles de conteneur statiques dans l’infrastructure du ruban.</span><span class="sxs-lookup"><span data-stu-id="55b38-152">The following table describes the static container controls in the Ribbon framework.</span></span>



| <span data-ttu-id="55b38-153">Contrôler</span><span class="sxs-lookup"><span data-stu-id="55b38-153">Control</span></span>                                                        | <span data-ttu-id="55b38-154">Élément de balisage</span><span class="sxs-lookup"><span data-stu-id="55b38-154">Markup Element</span></span>                                                   |
|----------------------------------------------------------------|------------------------------------------------------------------|
| [<span data-ttu-id="55b38-155">Menu de l’application</span><span class="sxs-lookup"><span data-stu-id="55b38-155">Application Menu</span></span>](windowsribbon-controls-applicationmenu.md) | [<span data-ttu-id="55b38-156">**ApplicationMenu**</span><span class="sxs-lookup"><span data-stu-id="55b38-156">**ApplicationMenu**</span></span>](windowsribbon-element-applicationmenu.md) |
| [<span data-ttu-id="55b38-157">Menu contextuel contexte</span><span class="sxs-lookup"><span data-stu-id="55b38-157">Context Popup</span></span>](windowsribbon-controls-contextpopup.md)       | [<span data-ttu-id="55b38-158">**ContextPopup**</span><span class="sxs-lookup"><span data-stu-id="55b38-158">**ContextPopup**</span></span>](windowsribbon-element-contextpopup.md)       |
| [<span data-ttu-id="55b38-159">Bouton déroulant</span><span class="sxs-lookup"><span data-stu-id="55b38-159">Drop-Down Button</span></span>](windowsribbon-controls-dropdownbutton.md)  | [<span data-ttu-id="55b38-160">**DropDownButton**</span><span class="sxs-lookup"><span data-stu-id="55b38-160">**DropDownButton**</span></span>](windowsribbon-element-dropdownbutton.md)   |
| [<span data-ttu-id="55b38-161">Groupe</span><span class="sxs-lookup"><span data-stu-id="55b38-161">Group</span></span>](windowsribbon-controls-group.md)                      | [<span data-ttu-id="55b38-162">**Groupe**</span><span class="sxs-lookup"><span data-stu-id="55b38-162">**Group**</span></span>](windowsribbon-element-group.md)                     |
| [<span data-ttu-id="55b38-163">Groupe de menus</span><span class="sxs-lookup"><span data-stu-id="55b38-163">Menu Group</span></span>](windowsribbon-controls-menugroup.md)             | [<span data-ttu-id="55b38-164">**MenuGroup**</span><span class="sxs-lookup"><span data-stu-id="55b38-164">**MenuGroup**</span></span>](windowsribbon-element-menugroup.md)             |
| [<span data-ttu-id="55b38-165">Bouton partagé</span><span class="sxs-lookup"><span data-stu-id="55b38-165">Split Button</span></span>](windowsribbon-controls-splitbutton.md)         | [<span data-ttu-id="55b38-166">**SplitButton**</span><span class="sxs-lookup"><span data-stu-id="55b38-166">**SplitButton**</span></span>](windowsribbon-element-splitbutton.md)         |
| [<span data-ttu-id="55b38-167">Tab</span><span class="sxs-lookup"><span data-stu-id="55b38-167">Tab</span></span>](windowsribbon-controls-tab.md)                          | [<span data-ttu-id="55b38-168">**Onglet**</span><span class="sxs-lookup"><span data-stu-id="55b38-168">**Tab**</span></span>](windowsribbon-element-tab.md)                         |
| [<span data-ttu-id="55b38-169">Groupe d’onglets</span><span class="sxs-lookup"><span data-stu-id="55b38-169">Tab Group</span></span>](windowsribbon-controls-tabgroup.md)               | [<span data-ttu-id="55b38-170">**TabGroup**</span><span class="sxs-lookup"><span data-stu-id="55b38-170">**TabGroup**</span></span>](windowsribbon-element-tabgroup.md)               |



 

### <a name="dynamic-containers"></a><span data-ttu-id="55b38-171">Conteneurs dynamiques</span><span class="sxs-lookup"><span data-stu-id="55b38-171">Dynamic Containers</span></span>

<span data-ttu-id="55b38-172">Les conteneurs dynamiques sont déclarés dans le fichier de balisage du ruban.</span><span class="sxs-lookup"><span data-stu-id="55b38-172">Dynamic containers are declared in the Ribbon markup file.</span></span> <span data-ttu-id="55b38-173">Ils présentent un groupe d’éléments ou de commandes qui sont créés ou modifiés au moment de l’exécution.</span><span class="sxs-lookup"><span data-stu-id="55b38-173">They feature a group of items or Commands that are created or modified at run time.</span></span>

<span data-ttu-id="55b38-174">Une sous-classe de conteneurs dynamiques, appelée galeries, se distingue par leur implémentation de l’interface [**IUICollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) .</span><span class="sxs-lookup"><span data-stu-id="55b38-174">A subclass of dynamic containers, called galleries, are distinguished by their implementation of the [**IUICollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) interface.</span></span> <span data-ttu-id="55b38-175">Cette interface permet à un contrôle d’exposer son élément ou sa liste de commandes sous la forme d’une collection, et de prendre en charge les mises à jour en fonction des conditions d’interaction et d’exécution de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="55b38-175">This interface allows a control to expose its item or Command list as a collection, and to support updates based on both user interaction and run-time conditions.</span></span> <span data-ttu-id="55b38-176">Pour plus d’informations, consultez [utilisation des galeries](ribbon-controls-galleries.md).</span><span class="sxs-lookup"><span data-stu-id="55b38-176">For more information, see [Working with Galleries](ribbon-controls-galleries.md).</span></span>

<span data-ttu-id="55b38-177">Le tableau suivant répertorie les contrôles de conteneur dynamiques dans l’infrastructure du ruban.</span><span class="sxs-lookup"><span data-stu-id="55b38-177">The following table lists the dynamic container controls in the Ribbon framework.</span></span>



| <span data-ttu-id="55b38-178">Contrôler</span><span class="sxs-lookup"><span data-stu-id="55b38-178">Control</span></span>                                                               | <span data-ttu-id="55b38-179">Élément de balisage</span><span class="sxs-lookup"><span data-stu-id="55b38-179">Markup Element</span></span>                                                         |
|-----------------------------------------------------------------------|------------------------------------------------------------------------|
| [<span data-ttu-id="55b38-180">Zone de liste déroulante</span><span class="sxs-lookup"><span data-stu-id="55b38-180">Combo Box</span></span>](windowsribbon-controls-combobox.md)                      | [<span data-ttu-id="55b38-181">**ComboBox**</span><span class="sxs-lookup"><span data-stu-id="55b38-181">**ComboBox**</span></span>](windowsribbon-element-combobox.md)                     |
| [<span data-ttu-id="55b38-182">Galerie déroulante</span><span class="sxs-lookup"><span data-stu-id="55b38-182">Drop-Down Gallery</span></span>](windowsribbon-controls-dropdowngallery.md)       | [<span data-ttu-id="55b38-183">**DropDownGallery**</span><span class="sxs-lookup"><span data-stu-id="55b38-183">**DropDownGallery**</span></span>](windowsribbon-element-dropdowngallery.md)       |
| [<span data-ttu-id="55b38-184">Galerie dans le ruban</span><span class="sxs-lookup"><span data-stu-id="55b38-184">In-Ribbon Gallery</span></span>](windowsribbon-controls-inribbongallery.md)       | [<span data-ttu-id="55b38-185">**InRibbonGallery**</span><span class="sxs-lookup"><span data-stu-id="55b38-185">**InRibbonGallery**</span></span>](windowsribbon-element-inribbongallery.md)       |
| [<span data-ttu-id="55b38-186">Barre d’outils accès rapide</span><span class="sxs-lookup"><span data-stu-id="55b38-186">Quick Access Toolbar</span></span>](windowsribbon-controls-quickaccesstoolbar.md) | [<span data-ttu-id="55b38-187">**QuickAccessToolbar**</span><span class="sxs-lookup"><span data-stu-id="55b38-187">**QuickAccessToolbar**</span></span>](windowsribbon-element-quickaccesstoolbar.md) |
| [<span data-ttu-id="55b38-188">Éléments récents</span><span class="sxs-lookup"><span data-stu-id="55b38-188">Recent Items</span></span>](windowsribbon-controls-recentitems.md)                | [<span data-ttu-id="55b38-189">**RecentItems**</span><span class="sxs-lookup"><span data-stu-id="55b38-189">**RecentItems**</span></span>](windowsribbon-element-recentitems.md)               |
| [<span data-ttu-id="55b38-190">Galerie de boutons partagés</span><span class="sxs-lookup"><span data-stu-id="55b38-190">Split Button Gallery</span></span>](windowsribbon-controls-splitbuttongallery.md) | [<span data-ttu-id="55b38-191">**SplitButtonGallery**</span><span class="sxs-lookup"><span data-stu-id="55b38-191">**SplitButtonGallery**</span></span>](windowsribbon-element-splitbuttongallery.md) |



 

### <a name="specialized-controls"></a><span data-ttu-id="55b38-192">Contrôles spécialisés</span><span class="sxs-lookup"><span data-stu-id="55b38-192">Specialized Controls</span></span>

<span data-ttu-id="55b38-193">L’infrastructure du ruban contient un certain nombre de contrôles spécialisés pour des fonctionnalités d’interface utilisateur spécifiques.</span><span class="sxs-lookup"><span data-stu-id="55b38-193">The Ribbon framework contains a number of specialized controls for specific UI functionality.</span></span>

<span data-ttu-id="55b38-194">Le tableau suivant répertorie les contrôles spécialisés dans l’infrastructure du ruban.</span><span class="sxs-lookup"><span data-stu-id="55b38-194">The following table lists the specialized controls in the Ribbon framework.</span></span>



| <span data-ttu-id="55b38-195">Contrôler</span><span class="sxs-lookup"><span data-stu-id="55b38-195">Control</span></span>                                                                  | <span data-ttu-id="55b38-196">Élément de balisage</span><span class="sxs-lookup"><span data-stu-id="55b38-196">Markup Element</span></span>                                                           |
|--------------------------------------------------------------------------|--------------------------------------------------------------------------|
| [<span data-ttu-id="55b38-197">Sélecteur de couleurs déroulantes</span><span class="sxs-lookup"><span data-stu-id="55b38-197">Drop-Down Color Picker</span></span>](windowsribbon-controls-dropdowncolorpicker.md) | [<span data-ttu-id="55b38-198">**DropDownColorPicker**</span><span class="sxs-lookup"><span data-stu-id="55b38-198">**DropDownColorPicker**</span></span>](windowsribbon-element-dropdowncolorpicker.md) |
| [<span data-ttu-id="55b38-199">Contrôle de police</span><span class="sxs-lookup"><span data-stu-id="55b38-199">Font Control</span></span>](windowsribbon-controls-fontcontrol.md)                   | [<span data-ttu-id="55b38-200">**FontControl**</span><span class="sxs-lookup"><span data-stu-id="55b38-200">**FontControl**</span></span>](windowsribbon-element-fontcontrol.md)                 |



 

## <a name="related-topics"></a><span data-ttu-id="55b38-201">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="55b38-201">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="55b38-202">Fonctionnement des commandes et des contrôles</span><span class="sxs-lookup"><span data-stu-id="55b38-202">Understanding Commands and Controls</span></span>](windowsribbon-commandscontrols.md)
</dt> </dl>

 

 