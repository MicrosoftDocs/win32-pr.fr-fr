---
title: Utilisation des galeries
description: L’infrastructure de ruban Windows offre aux développeurs un modèle robuste et cohérent pour gérer le contenu dynamique sur un large éventail de contrôles basés sur des collections.
ms.assetid: 447039f3-1428-4b6f-94cf-78cf81974041
keywords:
- Ruban Windows, galeries
- Ruban, galeries
- Ruban Windows, contrôle DropDownGallery
- Ruban, contrôle DropDownGallery
- Ruban Windows, contrôle SplitButtonGallery
- Ruban, contrôle SplitButtonGallery
- Contrôle DropDownGallery
- Contrôle SplitButtonGallery
- Galerie de ruban pour Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 784c69b0cf23edad906fbb35ee9a2a45454eacea
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103729229"
---
# <a name="working-with-galleries"></a><span data-ttu-id="abe49-112">Utilisation des galeries</span><span class="sxs-lookup"><span data-stu-id="abe49-112">Working with Galleries</span></span>

<span data-ttu-id="abe49-113">L’infrastructure de ruban Windows offre aux développeurs un modèle robuste et cohérent pour gérer le contenu dynamique sur un large éventail de contrôles basés sur des collections.</span><span class="sxs-lookup"><span data-stu-id="abe49-113">The Windows Ribbon framework provides developers with a robust and consistent model for managing dynamic content across a variety of collection-based controls.</span></span> <span data-ttu-id="abe49-114">En adaptant et en reconfigurant l’interface ruban, ces contrôles dynamiques permettent à l’infrastructure de répondre à l’interaction de l’utilisateur dans l’application hôte et le ruban lui-même, et offrent la flexibilité nécessaire pour gérer différents environnements d’exécution.</span><span class="sxs-lookup"><span data-stu-id="abe49-114">By adapting and reconfiguring the Ribbon UI, these dynamic controls allow the framework to respond to user interaction in both the host application and Ribbon itself, and provide the flexibility to handle various run time environments.</span></span>

-   [<span data-ttu-id="abe49-115">Introduction</span><span class="sxs-lookup"><span data-stu-id="abe49-115">Introduction</span></span>](#introduction)
-   [<span data-ttu-id="abe49-116">Galeries</span><span class="sxs-lookup"><span data-stu-id="abe49-116">Galleries</span></span>](#working-with-galleries)
    -   [<span data-ttu-id="abe49-117">Galeries d’éléments</span><span class="sxs-lookup"><span data-stu-id="abe49-117">Item Galleries</span></span>](#item-galleries)
    -   [<span data-ttu-id="abe49-118">Galeries de commandes</span><span class="sxs-lookup"><span data-stu-id="abe49-118">Command Galleries</span></span>](#command-galleries)
    -   [<span data-ttu-id="abe49-119">Contrôles de la Galerie</span><span class="sxs-lookup"><span data-stu-id="abe49-119">Gallery Controls</span></span>](#working-with-galleries)
-   [<span data-ttu-id="abe49-120">Comment implémenter une galerie</span><span class="sxs-lookup"><span data-stu-id="abe49-120">How to Implement a Gallery</span></span>](#how-to-implement-a-gallery)
    -   [<span data-ttu-id="abe49-121">Composants de base</span><span class="sxs-lookup"><span data-stu-id="abe49-121">The Basic Components</span></span>](#the-basic-components)
    -   [<span data-ttu-id="abe49-122">Déclarer les contrôles dans le balisage</span><span class="sxs-lookup"><span data-stu-id="abe49-122">Declare the Controls in Markup</span></span>](#declare-the-controls-in-markup)
    -   [<span data-ttu-id="abe49-123">Créer un gestionnaire de commandes</span><span class="sxs-lookup"><span data-stu-id="abe49-123">Create a Command Handler</span></span>](#create-a-command-handler)
    -   [<span data-ttu-id="abe49-124">Lier le gestionnaire de commandes</span><span class="sxs-lookup"><span data-stu-id="abe49-124">Bind the Command Handler</span></span>](#bind-the-command-handler)
    -   [<span data-ttu-id="abe49-125">Initialiser une collection</span><span class="sxs-lookup"><span data-stu-id="abe49-125">Initialize a Collection</span></span>](#initialize-a-collection)
    -   [<span data-ttu-id="abe49-126">Gérer les événements de collection</span><span class="sxs-lookup"><span data-stu-id="abe49-126">Handle Collection Events</span></span>](#handle-collection-events)
-   [<span data-ttu-id="abe49-127">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="abe49-127">Related topics</span></span>](#related-topics)

## <a name="introduction"></a><span data-ttu-id="abe49-128">Introduction</span><span class="sxs-lookup"><span data-stu-id="abe49-128">Introduction</span></span>

<span data-ttu-id="abe49-129">Cette capacité de l’infrastructure du ruban à s’adapter de manière dynamique aux conditions d’exécution, aux exigences de l’application et aux entrées de l’utilisateur final met en évidence les fonctionnalités enrichies de l’interface utilisateur de l’infrastructure et offre aux développeurs la flexibilité nécessaire pour répondre à un large éventail de besoins des clients.</span><span class="sxs-lookup"><span data-stu-id="abe49-129">This ability of the Ribbon framework to dynamically adapt to run-time conditions, application requirements, and end-user input highlights the rich UI capabilities of the framework, and provides developers with the flexibility to cater to a broad range of customer needs.</span></span>

<span data-ttu-id="abe49-130">L’objectif de ce guide est de décrire les contrôles de Galerie dynamiques pris en charge par l’infrastructure, d’expliquer leurs différences, de discuter du moment et de l’endroit où ils peuvent être utilisés, et de montrer comment ils peuvent être incorporés dans une application de ruban.</span><span class="sxs-lookup"><span data-stu-id="abe49-130">The focus of this guide is to describe the dynamic gallery controls supported by the framework, explain their differences, discuss when and where they may best be used, and demonstrate how they can be incorporated into a Ribbon application.</span></span>

## <a name="galleries"></a><span data-ttu-id="abe49-131">Galeries</span><span class="sxs-lookup"><span data-stu-id="abe49-131">Galleries</span></span>

<span data-ttu-id="abe49-132">Les galeries sont des contrôles de zone de liste riches en fonctionnalités et graphiques.</span><span class="sxs-lookup"><span data-stu-id="abe49-132">Galleries are functionally and graphically rich list box controls.</span></span> <span data-ttu-id="abe49-133">La collection d’éléments d’une galerie peut être organisée par catégories, affichées dans des colonnes flexibles et des dispositions basées sur des lignes, représentées par des images et du texte, et selon le type de Galerie, prend en charge l’aperçu instantané.</span><span class="sxs-lookup"><span data-stu-id="abe49-133">The item collection of a gallery can be organized by categories, displayed in flexible column and row-based layouts, represented with images and text, and depending on the type of gallery, support live previewing.</span></span>

<span data-ttu-id="abe49-134">Les galeries sont fonctionnellement distinctes des autres contrôles de ruban dynamique pour les raisons suivantes :</span><span class="sxs-lookup"><span data-stu-id="abe49-134">Galleries are functionally distinct from other dynamic Ribbon controls for the following reasons:</span></span>

-   <span data-ttu-id="abe49-135">Les galeries implémentent l’interface [**IUICollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) qui définit les différentes méthodes de manipulation des collections d’éléments de la Galerie.</span><span class="sxs-lookup"><span data-stu-id="abe49-135">Galleries implement the [**IUICollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) interface that defines the various methods for manipulating gallery item collections.</span></span>
-   <span data-ttu-id="abe49-136">Les galeries peuvent être mises à jour au moment de l’exécution, en fonction de l’activité qui se produit directement dans le ruban, par exemple lorsqu’un utilisateur ajoute une commande à la barre d’outils accès rapide (QAT).</span><span class="sxs-lookup"><span data-stu-id="abe49-136">Galleries can be updated at run time, based on activity that occurs directly in the Ribbon, such as when a user adds a Command to the Quick Access Toolbar (QAT).</span></span>
-   <span data-ttu-id="abe49-137">Les galeries peuvent être mises à jour au moment de l’exécution, en fonction de l’activité qui se produit indirectement de l’environnement d’exécution, par exemple lorsqu’un pilote d’imprimante prend uniquement en charge les mises en page en mode portrait.</span><span class="sxs-lookup"><span data-stu-id="abe49-137">Galleries can be updated at run time, based on activity that occurs indirectly from the run-time environment, such as when a printer driver supports portrait page layouts only.</span></span>
-   <span data-ttu-id="abe49-138">Les galeries peuvent être mises à jour au moment de l’exécution, en fonction de l’activité qui se produit indirectement dans l’application hôte, par exemple lorsqu’un utilisateur sélectionne un élément dans un document.</span><span class="sxs-lookup"><span data-stu-id="abe49-138">Galleries can be updated at run time, based on activity that occurs indirectly in the host application, such as when a user selects an item in a document.</span></span>

<span data-ttu-id="abe49-139">L’infrastructure du ruban expose deux types de galeries : les galeries d’éléments et les galeries de commandes.</span><span class="sxs-lookup"><span data-stu-id="abe49-139">The Ribbon framework exposes two types of galleries: item galleries and Command galleries.</span></span>

### <a name="item-galleries"></a><span data-ttu-id="abe49-140">Galeries d’éléments</span><span class="sxs-lookup"><span data-stu-id="abe49-140">Item Galleries</span></span>

<span data-ttu-id="abe49-141">Les galeries d’éléments contiennent une collection d’éléments associés basée sur les index, où chaque élément est représenté par une image, une chaîne, ou les deux.</span><span class="sxs-lookup"><span data-stu-id="abe49-141">Item galleries contain an index-based collection of related items where each item is represented by an image, a string, or both.</span></span> <span data-ttu-id="abe49-142">Le contrôle est lié à un gestionnaire de commandes unique qui s’appuie sur la valeur d’index qui est identifiée par la propriété de l’interface utilisateur de la valeur [ \_ \_ SelectedItem](windowsribbon-reference-properties-uipkey-selecteditem.md) .</span><span class="sxs-lookup"><span data-stu-id="abe49-142">The control is bound to a single Command handler that relies on the index value that is identified by the [UI\_PKEY\_SelectedItem](windowsribbon-reference-properties-uipkey-selecteditem.md) property.</span></span>

<span data-ttu-id="abe49-143">Les galeries d’éléments prennent en charge l’aperçu instantané, ce qui signifie que vous pouvez afficher un résultat de commande, basé sur mouseover ou Focus, sans valider ou appeler réellement la commande.</span><span class="sxs-lookup"><span data-stu-id="abe49-143">Item galleries support live previewing, which means displaying a Command result, based on mouseover or focus, without committing to or actually invoking the Command.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="abe49-144">L’infrastructure ne prend pas en charge l’hébergement de galeries d’éléments dans le menu de l’application.</span><span class="sxs-lookup"><span data-stu-id="abe49-144">The framework does not support hosting item galleries in the Application Menu.</span></span>

 

### <a name="command-galleries"></a><span data-ttu-id="abe49-145">Galeries de commandes</span><span class="sxs-lookup"><span data-stu-id="abe49-145">Command Galleries</span></span>

<span data-ttu-id="abe49-146">Les galeries de commandes contiennent une collection d’éléments distincts non indexés.</span><span class="sxs-lookup"><span data-stu-id="abe49-146">Command galleries contain a collection of distinct, non-indexed items.</span></span> <span data-ttu-id="abe49-147">Chaque élément est représenté par un contrôle unique lié à un gestionnaire de commandes via un ID de commande.</span><span class="sxs-lookup"><span data-stu-id="abe49-147">Each item is represented by a single control bound to a Command handler through a Command ID.</span></span> <span data-ttu-id="abe49-148">Comme les contrôles autonomes, chaque élément d’une bibliothèque de commandes achemine les événements d’entrée vers un gestionnaire de commandes associé, la Galerie de commandes elle-même n’écoute pas les événements.</span><span class="sxs-lookup"><span data-stu-id="abe49-148">Like standalone controls, each item in a Command gallery routes input events to an associated Command handler—the Command gallery itself does not listen for events.</span></span>

<span data-ttu-id="abe49-149">Les galeries de commandes ne prennent pas en charge l’aperçu instantané.</span><span class="sxs-lookup"><span data-stu-id="abe49-149">Command galleries do not support live previewing.</span></span>

### <a name="gallery-controls"></a><span data-ttu-id="abe49-150">Contrôles de la Galerie</span><span class="sxs-lookup"><span data-stu-id="abe49-150">Gallery Controls</span></span>

<span data-ttu-id="abe49-151">L’infrastructure du ruban contient quatre contrôles de Galerie : [**DropDownGallery**](windowsribbon-element-dropdowngallery.md), [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md), [**InRibbonGallery**](windowsribbon-element-inribbongallery.md)et [**ComboBox**](windowsribbon-element-combobox.md).</span><span class="sxs-lookup"><span data-stu-id="abe49-151">There are four gallery controls in the Ribbon framework: the [**DropDownGallery**](windowsribbon-element-dropdowngallery.md), the [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md), the [**InRibbonGallery**](windowsribbon-element-inribbongallery.md), and the [**ComboBox**](windowsribbon-element-combobox.md).</span></span> <span data-ttu-id="abe49-152">Tout sauf le **contrôle ComboBox** peut être implémenté comme une galerie d’éléments ou une bibliothèque de commandes.</span><span class="sxs-lookup"><span data-stu-id="abe49-152">All except the **ComboBox** can be implemented as either an item gallery or a Command gallery.</span></span>

### <a name="dropdowngallery"></a><span data-ttu-id="abe49-153">DropDownGallery</span><span class="sxs-lookup"><span data-stu-id="abe49-153">DropDownGallery</span></span>

<span data-ttu-id="abe49-154">Un [**DropDownGallery**](windowsribbon-element-dropdowngallery.md) est un bouton qui affiche une liste déroulante contenant une collection d’éléments ou de commandes s’excluant mutuellement.</span><span class="sxs-lookup"><span data-stu-id="abe49-154">A [**DropDownGallery**](windowsribbon-element-dropdowngallery.md) is a button that displays a drop-down list that contains a collection of mutually exclusive items or Commands.</span></span>

<span data-ttu-id="abe49-155">La capture d’écran suivante illustre le contrôle de Galerie de la [liste](windowsribbon-controls-dropdowngallery.md) déroulante du ruban dans Microsoft Paint pour Windows 7.</span><span class="sxs-lookup"><span data-stu-id="abe49-155">The following screen shot illustrates the Ribbon [Drop-Down Gallery](windowsribbon-controls-dropdowngallery.md) control in Microsoft Paint for Windows 7.</span></span>

![capture d’écran d’un contrôle de la Galerie déroulante dans Microsoft Paint pour Windows 7.](images/controls/dropdowngallery.png)

### <a name="splitbuttongallery"></a><span data-ttu-id="abe49-157">SplitButtonGallery</span><span class="sxs-lookup"><span data-stu-id="abe49-157">SplitButtonGallery</span></span>

<span data-ttu-id="abe49-158">Un [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md) est un contrôle composite qui expose un élément ou une commande par défaut unique à partir de sa collection sur un bouton principal, et qui affiche d’autres éléments ou commandes dans une liste déroulante mutuellement exclusive qui s’affiche lorsqu’un utilisateur clique sur un bouton secondaire.</span><span class="sxs-lookup"><span data-stu-id="abe49-158">A [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md) is a composite control that exposes a single default item or Command from its collection on a primary button, and displays other items or commands in a mutually exclusive drop-down list that is displayed when a secondary button is clicked.</span></span>

<span data-ttu-id="abe49-159">La capture d’écran suivante illustre le contrôle de [Galerie de bouton partagé](windowsribbon-controls-splitbuttongallery.md) du ruban dans Microsoft Paint pour Windows 7.</span><span class="sxs-lookup"><span data-stu-id="abe49-159">The following screen shot illustrates the Ribbon [Split Button Gallery](windowsribbon-controls-splitbuttongallery.md) control in Microsoft Paint for Windows 7.</span></span>

![capture d’écran d’un contrôle de Galerie de boutons partagés dans Microsoft Paint pour Windows 7.](images/controls/splitbuttongallery.png)

### <a name="inribbongallery"></a><span data-ttu-id="abe49-161">InRibbonGallery</span><span class="sxs-lookup"><span data-stu-id="abe49-161">InRibbonGallery</span></span>

<span data-ttu-id="abe49-162">Un [**InRibbonGallery**](windowsribbon-element-inribbongallery.md) est une galerie qui affiche une collection d’éléments ou de commandes connexes dans le ruban.</span><span class="sxs-lookup"><span data-stu-id="abe49-162">An [**InRibbonGallery**](windowsribbon-element-inribbongallery.md) is a gallery that displays a collection of related items or Commands in the Ribbon.</span></span> <span data-ttu-id="abe49-163">S’il y a trop d’éléments dans la Galerie, une flèche de développement est fournie pour afficher le reste de la collection dans un volet développé.</span><span class="sxs-lookup"><span data-stu-id="abe49-163">If there are too many items in the gallery, an expand arrow is provided to display the rest of the collection in an expanded pane.</span></span>

<span data-ttu-id="abe49-164">La capture d’écran suivante illustre le contrôle [de Galerie ruban dans le ruban](windowsribbon-controls-inribbongallery.md) de Microsoft Paint pour Windows 7.</span><span class="sxs-lookup"><span data-stu-id="abe49-164">The following screen shot illustrates the Ribbon [In-Ribbon Gallery](windowsribbon-controls-inribbongallery.md) control in Microsoft Paint for Windows 7.</span></span>

![capture d’écran d’un contrôle de galerie dans le ruban dans le ruban Microsoft Paint.](images/controls/inribbongallery.png)

### <a name="combobox"></a><span data-ttu-id="abe49-166">Liste déroulante</span><span class="sxs-lookup"><span data-stu-id="abe49-166">ComboBox</span></span>

<span data-ttu-id="abe49-167">Une zone de liste [**modifiable**](windowsribbon-element-combobox.md) est une zone de liste à une seule colonne qui contient une collection d’éléments avec un contrôle statique ou un contrôle d’édition et une flèche déroulante.</span><span class="sxs-lookup"><span data-stu-id="abe49-167">A [**ComboBox**](windowsribbon-element-combobox.md) is a single-column list box that contains a collection of items with either a static control or edit control and dropdown arrow.</span></span> <span data-ttu-id="abe49-168">La partie zone de liste du contrôle s’affiche lorsque l’utilisateur clique sur la flèche déroulante.</span><span class="sxs-lookup"><span data-stu-id="abe49-168">The list box portion of the control is displayed when the user clicks the drop-down arrow.</span></span>

<span data-ttu-id="abe49-169">La capture d’écran suivante illustre un contrôle de [zone de liste déroulante](windowsribbon-controls-combobox.md) du ruban à partir de Windows Live Movie Maker.</span><span class="sxs-lookup"><span data-stu-id="abe49-169">The following screen shot illustrates a Ribbon [Combo Box](windowsribbon-controls-combobox.md) control from Windows Live Movie Maker.</span></span>

![capture d’écran d’un contrôle de zone de liste déroulante dans le ruban Microsoft Paint.](images/controls/combobox.png)

<span data-ttu-id="abe49-171">Étant donné que la [**zone de liste déroulante**](windowsribbon-element-combobox.md) est exclusivement une galerie d’éléments, elle ne prend pas en charge les éléments de commande.</span><span class="sxs-lookup"><span data-stu-id="abe49-171">Because the [**ComboBox**](windowsribbon-element-combobox.md) is exclusively an item gallery, it does not support Command items.</span></span> <span data-ttu-id="abe49-172">C’est également le seul contrôle de galerie qui ne prend pas en charge un espace de commande.</span><span class="sxs-lookup"><span data-stu-id="abe49-172">It is also the only gallery control that does not support a Command Space.</span></span> <span data-ttu-id="abe49-173">(Un espace de commande est une collection de commandes qui sont déclarées dans le balisage et répertoriées en bas d’une galerie d’éléments ou d’une bibliothèque de commandes.)</span><span class="sxs-lookup"><span data-stu-id="abe49-173">(A Command Space is a collection of Commands that are declared in markup and listed at the bottom of an item gallery or Command gallery.)</span></span>

<span data-ttu-id="abe49-174">L’exemple de code suivant montre le balisage requis pour déclarer un espace de commande à trois boutons dans un [**DropDownGallery**](windowsribbon-element-dropdowngallery.md).</span><span class="sxs-lookup"><span data-stu-id="abe49-174">The following code example shows the markup required to declare a three-button Command Space in a [**DropDownGallery**](windowsribbon-element-dropdowngallery.md).</span></span>


```C++
<DropDownGallery 
  CommandName="cmdSizeAndColor" 
  TextPosition="Hide" 
  Type="Commands"
  ItemHeight="32"
  ItemWidth="32">
  <DropDownGallery.MenuLayout>
    <FlowMenuLayout Rows="2" Columns="3" Gripper="None"/>
  </DropDownGallery.MenuLayout>
  <Button CommandName="cmdCommandSpace1"/>
  <Button CommandName="cmdCommandSpace2"/>
  <Button CommandName="cmdCommandSpace3"/>
</DropDownGallery>
```



<span data-ttu-id="abe49-175">La capture d’écran suivante illustre l’espace de commande à trois boutons de l’exemple de code précédent.</span><span class="sxs-lookup"><span data-stu-id="abe49-175">The following screen shot illustrates the three-button Command Space of the preceding code example.</span></span>

![capture d’écran d’un espace de commande à trois boutons dans un dropdowngallery.](images/markup/gallerysample-commandspace.png)

## <a name="how-to-implement-a-gallery"></a><span data-ttu-id="abe49-177">Comment implémenter une galerie</span><span class="sxs-lookup"><span data-stu-id="abe49-177">How to Implement a Gallery</span></span>

<span data-ttu-id="abe49-178">Cette section décrit les détails d’implémentation des galeries de ruban et explique comment les incorporer dans une application de ruban.</span><span class="sxs-lookup"><span data-stu-id="abe49-178">This section discusses the implementation details of Ribbon galleries and walks through how to incorporate them in a Ribbon application.</span></span>

### <a name="the-basic-components"></a><span data-ttu-id="abe49-179">Composants de base</span><span class="sxs-lookup"><span data-stu-id="abe49-179">The Basic Components</span></span>

<span data-ttu-id="abe49-180">Cette section décrit l’ensemble des propriétés et des méthodes qui forment la structure fondamentale du contenu dynamique dans l’infrastructure du ruban et prennent en charge l’ajout, la suppression, la mise à jour et la manipulation du contenu et de la disposition visuelle des galeries de ruban au moment de l’exécution.</span><span class="sxs-lookup"><span data-stu-id="abe49-180">This section describes the set of properties and methods that form the backbone of dynamic content in the Ribbon framework and support adding, deleting, updating, and otherwise manipulating the content and visual layout of Ribbon galleries at run time.</span></span>

### <a name="iuicollection"></a><span data-ttu-id="abe49-181">IUICollection</span><span class="sxs-lookup"><span data-stu-id="abe49-181">IUICollection</span></span>

<span data-ttu-id="abe49-182">Les galeries requièrent un ensemble de méthodes de base pour accéder aux éléments individuels de leurs collections et les manipuler.</span><span class="sxs-lookup"><span data-stu-id="abe49-182">Galleries require a basic set of methods to access and manipulate the individual items in their collections.</span></span>

<span data-ttu-id="abe49-183">L’interface [IEnumUnknown](/windows/win32/api/objidlbase/nn-objidlbase-ienumunknown) définit ces méthodes, et l’infrastructure complète leurs fonctionnalités à l’aide de méthodes supplémentaires définies dans l’interface [**IUICollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) .</span><span class="sxs-lookup"><span data-stu-id="abe49-183">The [IEnumUnknown](/windows/win32/api/objidlbase/nn-objidlbase-ienumunknown) interface defines these methods, and the framework supplements their functionality with additional methods that are defined in the [**IUICollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) interface.</span></span> <span data-ttu-id="abe49-184">**IUICollection** est implémenté par l’infrastructure pour chaque déclaration de galerie dans le balisage du ruban.</span><span class="sxs-lookup"><span data-stu-id="abe49-184">**IUICollection** is implemented by the framework for each gallery declaration in the Ribbon markup.</span></span>

<span data-ttu-id="abe49-185">Si vous avez besoin de fonctionnalités supplémentaires qui ne sont pas fournies par l’interface [**IUICollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) , un objet de collection personnalisé qui est implémenté par l’application hôte et dérivé de [IEnumUnknown](/windows/win32/api/objidlbase/nn-objidlbase-ienumunknown) peut être substitué à la collection de frameworks.</span><span class="sxs-lookup"><span data-stu-id="abe49-185">If additional functionality is required that is not provided by the [**IUICollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) interface, then a custom collection object that is implemented by the host application and derived from [IEnumUnknown](/windows/win32/api/objidlbase/nn-objidlbase-ienumunknown) can be substituted for the framework collection.</span></span>

### <a name="iuicollectionchangedevent"></a><span data-ttu-id="abe49-186">IUICollectionChangedEvent</span><span class="sxs-lookup"><span data-stu-id="abe49-186">IUICollectionChangedEvent</span></span>

<span data-ttu-id="abe49-187">Pour qu’une application réponde aux modifications apportées à une collection de la Galerie, elle doit implémenter l’interface [**IUICollectionChangedEvent**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollectionchangedevent) .</span><span class="sxs-lookup"><span data-stu-id="abe49-187">For an application to respond to changes in a gallery collection, it must implement the [**IUICollectionChangedEvent**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollectionchangedevent) interface.</span></span> <span data-ttu-id="abe49-188">Les applications peuvent s’abonner à des notifications à partir d’un objet [**IUICollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) par le biais de l’écouteur d’événements [**IUICollectionChangedEvent :: OnChanged**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicollectionchangedevent-onchanged) .</span><span class="sxs-lookup"><span data-stu-id="abe49-188">Applications can subscribe to notifications from an [**IUICollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) object through the [**IUICollectionChangedEvent::OnChanged**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicollectionchangedevent-onchanged) event listener.</span></span>

<span data-ttu-id="abe49-189">Lorsque l’application remplace la collection de galeries fournie par le Framework par une collection personnalisée, l’application doit implémenter l’interface [IConnectionPointContainer](/windows/win32/api/ocidl/nn-ocidl-iconnectionpointcontainer) .</span><span class="sxs-lookup"><span data-stu-id="abe49-189">When the application replaces the gallery collection provided by the framework with a custom collection, the application should implement the [IConnectionPointContainer](/windows/win32/api/ocidl/nn-ocidl-iconnectionpointcontainer) interface.</span></span> <span data-ttu-id="abe49-190">Si [IConnectionPointContainer](/windows/win32/api/ocidl/nn-ocidl-iconnectionpointcontainer) n’est pas implémenté, l’application ne peut pas notifier l’infrastructure des modifications apportées à la collection personnalisée qui requièrent des mises à jour dynamiques du contrôle Gallery.</span><span class="sxs-lookup"><span data-stu-id="abe49-190">If [IConnectionPointContainer](/windows/win32/api/ocidl/nn-ocidl-iconnectionpointcontainer) is not implemented, then the application is unable to notify the framework of changes in the custom collection that require dynamic updates to the gallery control.</span></span>

<span data-ttu-id="abe49-191">Dans les cas où [IConnectionPointContainer](/windows/win32/api/ocidl/nn-ocidl-iconnectionpointcontainer) n’est pas implémenté, le contrôle Gallery peut être mis à jour uniquement par invalidation via [**IUIFramework :: InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) et [**IUICommandHandler :: UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty), ou en appelant [**IUIFramework :: SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty).</span><span class="sxs-lookup"><span data-stu-id="abe49-191">In those cases where [IConnectionPointContainer](/windows/win32/api/ocidl/nn-ocidl-iconnectionpointcontainer) is not implemented, the gallery control can be updated only by invalidation through [**IUIFramework::InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) and [**IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty), or by calling [**IUIFramework::SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty).</span></span>

### <a name="iuisimplepropertyset"></a><span data-ttu-id="abe49-192">IUISimplePropertySet</span><span class="sxs-lookup"><span data-stu-id="abe49-192">IUISimplePropertySet</span></span>

<span data-ttu-id="abe49-193">Les applications doivent implémenter IUISimplePropertySet pour chaque élément ou commande d’une collection de la Galerie.</span><span class="sxs-lookup"><span data-stu-id="abe49-193">Applications must implement IUISimplePropertySet for each item or Command in a gallery collection.</span></span> <span data-ttu-id="abe49-194">Toutefois, les propriétés qui peuvent être demandées avec [**IUISimplePropertySet :: GetValue**](/windows/desktop/api/uiribbon/nf-uiribbon-iuisimplepropertyset-getvalue) varient.</span><span class="sxs-lookup"><span data-stu-id="abe49-194">However, the properties that can be requested with [**IUISimplePropertySet::GetValue**](/windows/desktop/api/uiribbon/nf-uiribbon-iuisimplepropertyset-getvalue) vary.</span></span>

<span data-ttu-id="abe49-195">Les éléments sont définis et liés à une galerie via la clé de propriété [ \_ \_ ItemsSource de l’interface utilisateur](windowsribbon-reference-properties-uipkey-itemssource.md) et exposent les propriétés avec un objet [**IUICollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) .</span><span class="sxs-lookup"><span data-stu-id="abe49-195">Items are defined and bound to a gallery through the [UI\_PKEY\_ItemsSource](windowsribbon-reference-properties-uipkey-itemssource.md) property key and expose properties with an [**IUICollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) object.</span></span>

<span data-ttu-id="abe49-196">Les propriétés valides pour les éléments dans les galeries d’éléments ([**\_ \_ collection UI COMMANDTYPE**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_commandtype)) sont décrites dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="abe49-196">The valid properties for items in item galleries ([**UI\_COMMANDTYPE\_COLLECTION**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_commandtype)) are described in the following table.</span></span>

> [!Note]  
> <span data-ttu-id="abe49-197">Certaines propriétés d’élément, telles [que \_ l' \_ étiquette de l’interface utilisateur](windowsribbon-reference-properties-uipkey-label.md), peuvent être définies dans le balisage.</span><span class="sxs-lookup"><span data-stu-id="abe49-197">Some item properties, such as [UI\_PKEY\_Label](windowsribbon-reference-properties-uipkey-label.md), can be defined in markup.</span></span> <span data-ttu-id="abe49-198">Pour plus d’informations, consultez la documentation de référence sur les [clés de propriété](windowsribbon-reference-properties.md) .</span><span class="sxs-lookup"><span data-stu-id="abe49-198">For more detail, see the [Property Keys](windowsribbon-reference-properties.md) reference documentation.</span></span>

 



<span data-ttu-id="abe49-199">Contrôler</span><span class="sxs-lookup"><span data-stu-id="abe49-199">Control</span></span>

<span data-ttu-id="abe49-200">Propriétés</span><span class="sxs-lookup"><span data-stu-id="abe49-200">Properties</span></span>

[<span data-ttu-id="abe49-201">**ComboBox**</span><span class="sxs-lookup"><span data-stu-id="abe49-201">**ComboBox**</span></span>](windowsribbon-element-combobox.md)

<span data-ttu-id="abe49-202">[Interface utilisateur \_ \_Étiquette de nom](windowsribbon-reference-properties-uipkey-label.md)du code de [l’interface utilisateur, code de \_ \_ catégorie](windowsribbon-reference-properties-uipkey-categoryid.md)</span><span class="sxs-lookup"><span data-stu-id="abe49-202">[UI\_PKEY\_Label](windowsribbon-reference-properties-uipkey-label.md), [UI\_PKEY\_CategoryId](windowsribbon-reference-properties-uipkey-categoryid.md)</span></span>

[<span data-ttu-id="abe49-203">**DropDownGallery**</span><span class="sxs-lookup"><span data-stu-id="abe49-203">**DropDownGallery**</span></span>](windowsribbon-element-dropdowngallery.md)

<span data-ttu-id="abe49-204">[Interface utilisateur \_ \_Étiquette de nom](windowsribbon-reference-properties-uipkey-label.md)de la partie, [ \_ \_ ItemImage d’interface utilisateur](windowsribbon-reference-properties-uipkey-itemimage.md) , nom de la [ \_ \_ catégorie d’interface utilisateur](windowsribbon-reference-properties-uipkey-categoryid.md)</span><span class="sxs-lookup"><span data-stu-id="abe49-204">[UI\_PKEY\_Label](windowsribbon-reference-properties-uipkey-label.md), [UI\_PKEY\_ItemImage](windowsribbon-reference-properties-uipkey-itemimage.md) , [UI\_PKEY\_CategoryId](windowsribbon-reference-properties-uipkey-categoryid.md)</span></span>

[<span data-ttu-id="abe49-205">**InRibbonGallery**</span><span class="sxs-lookup"><span data-stu-id="abe49-205">**InRibbonGallery**</span></span>](windowsribbon-element-inribbongallery.md)

<span data-ttu-id="abe49-206">[Interface utilisateur \_ \_Étiquette de nom](windowsribbon-reference-properties-uipkey-label.md)de la partie, [ \_ \_ ItemImage d’interface utilisateur](windowsribbon-reference-properties-uipkey-itemimage.md) , nom de la [ \_ \_ catégorie d’interface utilisateur](windowsribbon-reference-properties-uipkey-categoryid.md)</span><span class="sxs-lookup"><span data-stu-id="abe49-206">[UI\_PKEY\_Label](windowsribbon-reference-properties-uipkey-label.md), [UI\_PKEY\_ItemImage](windowsribbon-reference-properties-uipkey-itemimage.md) , [UI\_PKEY\_CategoryId](windowsribbon-reference-properties-uipkey-categoryid.md)</span></span>

[<span data-ttu-id="abe49-207">**SplitButtonGallery**</span><span class="sxs-lookup"><span data-stu-id="abe49-207">**SplitButtonGallery**</span></span>](windowsribbon-element-splitbuttongallery.md)

<span data-ttu-id="abe49-208">[Interface utilisateur \_ \_Étiquette de nom](windowsribbon-reference-properties-uipkey-label.md)de la partie, [ \_ \_ ItemImage d’interface utilisateur](windowsribbon-reference-properties-uipkey-itemimage.md), nom de la [ \_ \_ catégorie d’interface utilisateur](windowsribbon-reference-properties-uipkey-categoryid.md)</span><span class="sxs-lookup"><span data-stu-id="abe49-208">[UI\_PKEY\_Label](windowsribbon-reference-properties-uipkey-label.md), [UI\_PKEY\_ItemImage](windowsribbon-reference-properties-uipkey-itemimage.md), [UI\_PKEY\_CategoryId](windowsribbon-reference-properties-uipkey-categoryid.md)</span></span>

<span data-ttu-id="abe49-209">[Interface utilisateur \_ La \_ ](windowsribbon-reference-properties-uipkey-selecteditem.md) propriété de la bibliothèque de propriétés est une propriété de la Galerie d’éléments.</span><span class="sxs-lookup"><span data-stu-id="abe49-209">[UI\_PKEY\_SelectedItem](windowsribbon-reference-properties-uipkey-selecteditem.md) is a property of the item gallery.</span></span>



 

<span data-ttu-id="abe49-210">Les propriétés d’élément valides pour les galeries de commandes ([**UI \_ COMMANDTYPE \_ COMMANDCOLLECTION**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_commandtype)) sont décrites dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="abe49-210">The valid item properties for Command galleries ([**UI\_COMMANDTYPE\_COMMANDCOLLECTION**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_commandtype)) are described in the following table.</span></span>



| <span data-ttu-id="abe49-211">Contrôler</span><span class="sxs-lookup"><span data-stu-id="abe49-211">Control</span></span>                                                                | <span data-ttu-id="abe49-212">Propriétés</span><span class="sxs-lookup"><span data-stu-id="abe49-212">Properties</span></span>                                                                                                                                                                                                                                            |
|------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="abe49-213">**DropDownGallery**</span><span class="sxs-lookup"><span data-stu-id="abe49-213">**DropDownGallery**</span></span>](windowsribbon-element-dropdowngallery.md)       | <span data-ttu-id="abe49-214">[Interface utilisateur \_ Hypergraphique de la \_ ](windowsribbon-reference-properties-uipkey-commandid.md)présente, interface de [l’interface utilisateur \_ \_ CommandType](windowsribbon-reference-properties-uipkey-commandtype.md) , code de la [ \_ \_ catégorie](windowsribbon-reference-properties-uipkey-categoryid.md) d’interface utilisateur</span><span class="sxs-lookup"><span data-stu-id="abe49-214">[UI\_PKEY\_CommandId](windowsribbon-reference-properties-uipkey-commandid.md), [UI\_PKEY\_CommandType](windowsribbon-reference-properties-uipkey-commandtype.md) , [UI\_PKEY\_CategoryId](windowsribbon-reference-properties-uipkey-categoryid.md)</span></span> |
| [<span data-ttu-id="abe49-215">**InRibbonGallery**</span><span class="sxs-lookup"><span data-stu-id="abe49-215">**InRibbonGallery**</span></span>](windowsribbon-element-inribbongallery.md)       | <span data-ttu-id="abe49-216">[Interface utilisateur \_ Hypergraphique de la \_ ](windowsribbon-reference-properties-uipkey-commandid.md)présente, interface de [l’interface utilisateur \_ \_ CommandType](windowsribbon-reference-properties-uipkey-commandtype.md) , code de la [ \_ \_ catégorie](windowsribbon-reference-properties-uipkey-categoryid.md) d’interface utilisateur</span><span class="sxs-lookup"><span data-stu-id="abe49-216">[UI\_PKEY\_CommandId](windowsribbon-reference-properties-uipkey-commandid.md), [UI\_PKEY\_CommandType](windowsribbon-reference-properties-uipkey-commandtype.md) , [UI\_PKEY\_CategoryId](windowsribbon-reference-properties-uipkey-categoryid.md)</span></span> |
| [<span data-ttu-id="abe49-217">**SplitButtonGallery**</span><span class="sxs-lookup"><span data-stu-id="abe49-217">**SplitButtonGallery**</span></span>](windowsribbon-element-splitbuttongallery.md) | <span data-ttu-id="abe49-218">[Interface utilisateur \_ Hypergraphique de la \_ ](windowsribbon-reference-properties-uipkey-commandid.md)présente, interface de [l’interface utilisateur \_ \_ CommandType](windowsribbon-reference-properties-uipkey-commandtype.md), code de la [ \_ \_ catégorie](windowsribbon-reference-properties-uipkey-categoryid.md) d’interface utilisateur</span><span class="sxs-lookup"><span data-stu-id="abe49-218">[UI\_PKEY\_CommandId](windowsribbon-reference-properties-uipkey-commandid.md), [UI\_PKEY\_CommandType](windowsribbon-reference-properties-uipkey-commandtype.md), [UI\_PKEY\_CategoryId](windowsribbon-reference-properties-uipkey-categoryid.md)</span></span>  |



 

<span data-ttu-id="abe49-219">Les catégories sont utilisées pour organiser les éléments et les commandes dans les galeries.</span><span class="sxs-lookup"><span data-stu-id="abe49-219">Categories are used to organize items and Commands in galleries.</span></span> <span data-ttu-id="abe49-220">Les catégories sont définies et liées à une galerie via la clé de propriété des [ \_ \_ catégories de l’interface utilisateur](windowsribbon-reference-properties-uipkey-categories.md) et exposent les propriétés avec un objet [**IUICollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) spécifique à la catégorie.</span><span class="sxs-lookup"><span data-stu-id="abe49-220">Categories are defined and bound to a gallery through the [UI\_PKEY\_Categories](windowsribbon-reference-properties-uipkey-categories.md) property key and expose properties with a category-specific [**IUICollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) object.</span></span>

<span data-ttu-id="abe49-221">Les catégories n’ont pas de CommandType et ne prennent pas en charge l’interaction de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="abe49-221">Categories do not have a CommandType and do not support user interaction.</span></span> <span data-ttu-id="abe49-222">Par exemple, les catégories ne peuvent pas devenir SelectedItem dans une galerie d’éléments, et elles ne sont pas liées à une commande dans une galerie de commandes.</span><span class="sxs-lookup"><span data-stu-id="abe49-222">For example, categories cannot become the SelectedItem in an item gallery, and they are not bound to a Command in a Command gallery.</span></span> <span data-ttu-id="abe49-223">À l’instar des autres propriétés d’élément de la Galerie, les propriétés de catégorie telles que [l’étiquette de nom d’utilisateur et le \_ \_ nom](windowsribbon-reference-properties-uipkey-label.md) du code [](/windows/desktop/api/uiribbon/nf-uiribbon-iuisimplepropertyset-getvalue)de [ \_ \_ ](windowsribbon-reference-properties-uipkey-categoryid.md) catégorie</span><span class="sxs-lookup"><span data-stu-id="abe49-223">Like other gallery item properties, category properties such as [UI\_PKEY\_Label](windowsribbon-reference-properties-uipkey-label.md) and [UI\_PKEY\_CategoryId](windowsribbon-reference-properties-uipkey-categoryid.md) can be retrieved by calling [**IUISimplePropertySet::GetValue**](/windows/desktop/api/uiribbon/nf-uiribbon-iuisimplepropertyset-getvalue).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="abe49-224">[**IUISimplePropertySet :: GetValue**](/windows/desktop/api/uiribbon/nf-uiribbon-iuisimplepropertyset-getvalue) doit retourner la [**collection d’interface utilisateur \_ \_ INVALIDINDEX**](/windows/desktop/windowsribbon/windowsribbon-ui-collection-invalidindex) lorsque [l’interface utilisateur du groupe de catégories d’utilisateur \_ \_](windowsribbon-reference-properties-uipkey-categoryid.md) est demandée pour un élément qui n’a pas de catégorie associée.</span><span class="sxs-lookup"><span data-stu-id="abe49-224">[**IUISimplePropertySet::GetValue**](/windows/desktop/api/uiribbon/nf-uiribbon-iuisimplepropertyset-getvalue) should return [**UI\_COLLECTION\_INVALIDINDEX**](/windows/desktop/windowsribbon/windowsribbon-ui-collection-invalidindex) when [UI\_PKEY\_CategoryId](windowsribbon-reference-properties-uipkey-categoryid.md) is requested for an item that does not have an associated category.</span></span>

 

### <a name="declare-the-controls-in-markup"></a><span data-ttu-id="abe49-225">Déclarer les contrôles dans le balisage</span><span class="sxs-lookup"><span data-stu-id="abe49-225">Declare the Controls in Markup</span></span>

<span data-ttu-id="abe49-226">Les galeries, comme tous les contrôles de ruban, doivent être déclarées dans le balisage.</span><span class="sxs-lookup"><span data-stu-id="abe49-226">Galleries, like all Ribbon controls, must be declared in markup.</span></span> <span data-ttu-id="abe49-227">Une galerie est identifiée dans le balisage comme une galerie d’éléments ou une bibliothèque de commandes, et divers détails de présentation sont déclarés.</span><span class="sxs-lookup"><span data-stu-id="abe49-227">A gallery is identified in markup as an item gallery or Command gallery, and various presentation details are declared.</span></span> <span data-ttu-id="abe49-228">Contrairement à d’autres contrôles, les galeries ne requièrent que le contrôle de base, ou conteneur de collection, soient déclarés dans le balisage.</span><span class="sxs-lookup"><span data-stu-id="abe49-228">Unlike other controls, galleries require the base control only, or collection container, to be declared in markup.</span></span> <span data-ttu-id="abe49-229">Les regroupements réels sont remplis au moment de l’exécution.</span><span class="sxs-lookup"><span data-stu-id="abe49-229">The actual collections are populated at run time.</span></span> <span data-ttu-id="abe49-230">Quand une galerie est déclarée dans le balisage, l’attribut de *type* est utilisé pour spécifier si la Galerie est une galerie d’éléments d’une bibliothèque de commandes.</span><span class="sxs-lookup"><span data-stu-id="abe49-230">When a gallery is declared in markup, the *Type* attribute is used to specify whether the gallery is an item gallery of a Command gallery.</span></span>

<span data-ttu-id="abe49-231">Un certain nombre d’attributs de disposition facultatifs sont disponibles pour chacun des contrôles présentés ici.</span><span class="sxs-lookup"><span data-stu-id="abe49-231">There are a number of optional layout attributes available for each of the controls discussed here.</span></span> <span data-ttu-id="abe49-232">Ces attributs fournissent des préférences de développeur pour l’infrastructure à suivre qui affectent directement la manière dont un contrôle est rempli et affiché dans un ruban.</span><span class="sxs-lookup"><span data-stu-id="abe49-232">These attributes provide developer preferences for the framework to follow that directly affect how a control is populated and displayed in a ribbon.</span></span> <span data-ttu-id="abe49-233">Les préférences applicables dans le balisage sont liées aux modèles d’affichage et de disposition et aux comportements décrits dans [Personnalisation d’un ruban à l’aide des définitions de taille et des stratégies de mise à l’échelle](windowsribbon-templates.md).</span><span class="sxs-lookup"><span data-stu-id="abe49-233">The preferences applicable in markup are related to the display and layout templates and behaviors discussed in [Customizing a Ribbon Through Size Definitions and Scaling Policies](windowsribbon-templates.md).</span></span>

<span data-ttu-id="abe49-234">Si un contrôle particulier n’autorise pas les préférences de disposition directement dans le balisage ou si les préférences de disposition ne sont pas spécifiées, l’infrastructure définit les conventions d’affichage spécifiques au contrôle en fonction de la quantité d’espace d’écran disponible.</span><span class="sxs-lookup"><span data-stu-id="abe49-234">If a particular control does not allow layout preferences directly in markup, or the layout preferences are not specified, then the framework defines control-specific display conventions based on the amount of screen space available.</span></span>

<span data-ttu-id="abe49-235">Les exemples suivants montrent comment incorporer un ensemble de galeries dans un ruban.</span><span class="sxs-lookup"><span data-stu-id="abe49-235">The following examples demonstrate how to incorporate a set of galleries into a Ribbon.</span></span>

### <a name="command-declarations"></a><span data-ttu-id="abe49-236">Déclarations de commande</span><span class="sxs-lookup"><span data-stu-id="abe49-236">Command Declarations</span></span>

<span data-ttu-id="abe49-237">Les commandes doivent être déclarées avec un attribut *CommandName* utilisé pour associer un contrôle, ou un ensemble de contrôles, à la commande.</span><span class="sxs-lookup"><span data-stu-id="abe49-237">Commands should be declared with a *CommandName* attribute that is used to associate a control, or set of controls, with the Command.</span></span>

<span data-ttu-id="abe49-238">Un attribut *CommandID* utilisé pour lier une commande à un gestionnaire de commandes lors de la compilation du balisage peut également être spécifié ici.</span><span class="sxs-lookup"><span data-stu-id="abe49-238">A *CommandId* attribute used to bind a Command to a Command handler when the markup is compiled can also be specified here.</span></span> <span data-ttu-id="abe49-239">Si aucun ID n’est fourni, l’infrastructure est générée.</span><span class="sxs-lookup"><span data-stu-id="abe49-239">If no ID is provided, then one is generated by the framework.</span></span>


```XML
<!-- ComboBox -->
<Command Name="cmdComboBoxGroup"
         Symbol="cmdComboBoxGroup"
         Comment="ComboBox Group"
         LabelTitle="ComboBox"/>
<Command Name="cmdComboBox"
         Symbol="cmdComboBox"
         Comment="ComboBox"
         LabelTitle="ComboBox"/>
```


```XML

<!-- DropDownGallery -->
<Command Name="cmdDropDownGalleryGroup"
         Symbol="cmdDropDownGalleryGroup"
         Comment="DropDownGallery Group"
         LabelTitle="DropDownGallery"/>
<Command Name="cmdDropDownGallery"
         Symbol="cmdDropDownGallery"
         Comment="DropDownGallery"
         LabelTitle="DropDownGallery"/>
```




```XML

<!-- InRibbonGallery -->
<Command Name="cmdInRibbonGalleryGroup"
         Symbol="cmdInRibbonGalleryGroup"
         Comment="InRibbonGallery Group"
         LabelTitle="InRibbonGallery"/>
<Command Name="cmdInRibbonGallery"
         Symbol="cmdInRibbonGallery"
         Comment="InRibbonGallery"
         LabelTitle="InRibbonGallery"
```



```XML

<!-- SplitButtonGallery -->
<Command Name="cmdSplitButtonGalleryGroup"
         Symbol="cmdSplitButtonGalleryGroup"
         Comment="SplitButtonGallery Group"
         LabelTitle="SplitButtonGallery"/>
<Command Name="cmdSplitButtonGallery"
         Symbol="cmdSplitButtonGallery"
         Comment="SplitButtonGallery"
         LabelTitle="SplitButtonGallery"
```



### <a name="control-declarations"></a><span data-ttu-id="abe49-240">Déclarations de contrôle</span><span class="sxs-lookup"><span data-stu-id="abe49-240">Control Declarations</span></span>

<span data-ttu-id="abe49-241">Cette section contient des exemples qui illustrent le balisage de contrôle de base requis pour les différents types de Galerie.</span><span class="sxs-lookup"><span data-stu-id="abe49-241">This section contains examples that demonstrate the basic control markup required for the various gallery types.</span></span> <span data-ttu-id="abe49-242">Elles montrent comment déclarer les contrôles de la Galerie et les associer à une commande via l’attribut *CommandName* .</span><span class="sxs-lookup"><span data-stu-id="abe49-242">They show how to declare the gallery controls and associate them with a Command through the *CommandName* attribute.</span></span>

<span data-ttu-id="abe49-243">L’exemple suivant montre une déclaration de contrôle pour le [**DropDownGallery**](windowsribbon-element-dropdowngallery.md) où l’attribut de *type* est utilisé pour spécifier qu’il s’agit d’une bibliothèque de commandes.</span><span class="sxs-lookup"><span data-stu-id="abe49-243">The following example shows a control declaration for the [**DropDownGallery**](windowsribbon-element-dropdowngallery.md) where the *Type* attribute is used to specify that this is a Command gallery.</span></span>


```XML
<!-- DropDownGallery -->
<Group CommandName="cmdDropDownGalleryGroup">
  <DropDownGallery CommandName="cmdDropDownGallery"
                   TextPosition="Hide"
                   Type="Commands"
                   ItemHeight="32"
                   ItemWidth="32">
    <DropDownGallery.MenuLayout>
      <FlowMenuLayout Rows="2"
                      Columns="3"
                      Gripper="None"/>
    </DropDownGallery.MenuLayout>
    <DropDownGallery.MenuGroups>
      <MenuGroup>
        <Button CommandName="cmdButton1"></Button>
        <Button CommandName="cmdButton2"></Button>
       </MenuGroup>
       <MenuGroup>
        <Button CommandName="cmdButton3"></Button>
      </MenuGroup>
    </DropDownGallery.MenuGroups>
  </DropDownGallery>
</Group>
```



<span data-ttu-id="abe49-244">L’exemple suivant montre une déclaration de contrôle pour [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md).</span><span class="sxs-lookup"><span data-stu-id="abe49-244">The following example shows a control declaration for the [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md).</span></span>


```XML
<!-- SplitButtonGallery -->
<Group CommandName="cmdSplitButtonGalleryGroup">
  <SplitButtonGallery CommandName="cmdSplitButtonGallery">
    <SplitButtonGallery.MenuLayout>
      <FlowMenuLayout Rows="2"
                      Columns="3"
                      Gripper="None"/>
    </SplitButtonGallery.MenuLayout>
    <SplitButtonGallery.MenuGroups>
      <MenuGroup>
        <Button CommandName="cmdButton1"></Button>
        <Button CommandName="cmdButton2"></Button>
      </MenuGroup>
      <MenuGroup>
        <Button CommandName="cmdButton3"></Button>
      </MenuGroup>
    </SplitButtonGallery.MenuGroups>
  </SplitButtonGallery>
</Group>
```



<span data-ttu-id="abe49-245">L’exemple suivant montre une déclaration de contrôle pour [**InRibbonGallery**](windowsribbon-element-inribbongallery.md).</span><span class="sxs-lookup"><span data-stu-id="abe49-245">The following example shows a control declaration for the [**InRibbonGallery**](windowsribbon-element-inribbongallery.md).</span></span>

> [!Note]  
> <span data-ttu-id="abe49-246">Étant donné que [**InRibbonGallery**](windowsribbon-element-inribbongallery.md) est conçu pour afficher un sous-ensemble de sa collection d’éléments dans le ruban sans activer un menu déroulant, il fournit un certain nombre d’attributs facultatifs qui régissent la taille et la disposition des éléments sur l’initialisation du ruban.</span><span class="sxs-lookup"><span data-stu-id="abe49-246">Because the [**InRibbonGallery**](windowsribbon-element-inribbongallery.md) is designed to display a subset of its item collection in the Ribbon without activating a drop-down menu, it provides a number of optional attributes that govern its size and item layout on Ribbon initialization.</span></span> <span data-ttu-id="abe49-247">Ces attributs sont uniques à **InRibbonGallery** et ne sont pas disponibles dans les autres contrôles dynamiques.</span><span class="sxs-lookup"><span data-stu-id="abe49-247">These attributes are unique to the **InRibbonGallery** and are not available from the other dynamic controls.</span></span>

 


```XML
<!-- InRibbonGallery -->
<Group CommandName="cmdInRibbonGalleryGroup" SizeDefinition="OneInRibbonGallery">
  <InRibbonGallery CommandName="cmdInRibbonGallery"
                   MaxColumns="10"
                   MaxColumnsMedium="5"
                   MinColumnsLarge="5"
                   MinColumnsMedium="3"
                   Type="Items">
    <InRibbonGallery.MenuLayout>
      <VerticalMenuLayout Rows="2"
                          Gripper="Vertical"/>
    </InRibbonGallery.MenuLayout>
    <InRibbonGallery.MenuGroups>
      <MenuGroup>
        <Button CommandName="cmdButton1"></Button>
        <Button CommandName="cmdButton2"></Button>
      </MenuGroup>
      <MenuGroup>
        <Button CommandName="cmdButton3"></Button>
      </MenuGroup>
    </InRibbonGallery.MenuGroups>            
  </InRibbonGallery>
</Group>
```



<span data-ttu-id="abe49-248">L’exemple suivant montre une déclaration de contrôle pour la [**zone de liste déroulante**](windowsribbon-element-combobox.md).</span><span class="sxs-lookup"><span data-stu-id="abe49-248">The following example shows a control declaration for the [**ComboBox**](windowsribbon-element-combobox.md).</span></span>


```XML
<!-- ComboBox -->
<Group CommandName="cmdComboBoxGroup">
  <ComboBox CommandName="cmdComboBox">              
  </ComboBox>
</Group>
```



### <a name="create-a-command-handler"></a><span data-ttu-id="abe49-249">Créer un gestionnaire de commandes</span><span class="sxs-lookup"><span data-stu-id="abe49-249">Create a Command Handler</span></span>

<span data-ttu-id="abe49-250">Pour chaque commande, l’infrastructure du ruban requiert un gestionnaire de commandes correspondant dans l’application hôte.</span><span class="sxs-lookup"><span data-stu-id="abe49-250">For each Command, the Ribbon framework requires a corresponding Command handler in the host application.</span></span> <span data-ttu-id="abe49-251">Les gestionnaires de commandes sont implémentés par l’application hôte du ruban et sont dérivés de l’interface [**IUICommandHandler**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicommandhandler) .</span><span class="sxs-lookup"><span data-stu-id="abe49-251">Command handlers are implemented by the Ribbon host application and are derived from the [**IUICommandHandler**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicommandhandler) interface.</span></span>

> [!Note]  
> <span data-ttu-id="abe49-252">Plusieurs commandes peuvent être liées à un gestionnaire de commandes unique.</span><span class="sxs-lookup"><span data-stu-id="abe49-252">Multiple Commands can be bound to a single Command handler.</span></span>

 

<span data-ttu-id="abe49-253">Un gestionnaire de commandes remplit deux fonctions :</span><span class="sxs-lookup"><span data-stu-id="abe49-253">A Command handler serves two purposes:</span></span>

-   <span data-ttu-id="abe49-254">[**IUICommandHandler :: UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) répond aux demandes de mise à jour de propriété.</span><span class="sxs-lookup"><span data-stu-id="abe49-254">[**IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) responds to property update requests.</span></span> <span data-ttu-id="abe49-255">Les valeurs des propriétés de commande, telles que [l’interface utilisateur de l’interface utilisateur \_ \_ activée](windowsribbon-reference-properties-uipkey-enabled.md) ou [l' \_ \_ étiquette de l’interface utilisateur](windowsribbon-reference-properties-uipkey-label.md), sont définies par le biais d’appels à [**IUIFramework :: SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) ou [**IUIFramework :: InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand).</span><span class="sxs-lookup"><span data-stu-id="abe49-255">The values of Command properties, such as [UI\_PKEY\_Enabled](windowsribbon-reference-properties-uipkey-enabled.md) or [UI\_PKEY\_Label](windowsribbon-reference-properties-uipkey-label.md), are set through calls to [**IUIFramework::SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) or [**IUIFramework::InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand).</span></span>
-   <span data-ttu-id="abe49-256">[**IUICommandHandler :: Execute**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-execute) répond aux événements d’exécution.</span><span class="sxs-lookup"><span data-stu-id="abe49-256">[**IUICommandHandler::Execute**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-execute) responds to execute events.</span></span> <span data-ttu-id="abe49-257">Cette méthode prend en charge les trois États d’exécution suivants qui sont spécifiés par le paramètre [**\_ EXECUTIONVERB de l’interface utilisateur**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_executionverb) .</span><span class="sxs-lookup"><span data-stu-id="abe49-257">This method supports the following three execution states that are specified by the [**UI\_EXECUTIONVERB**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_executionverb) parameter.</span></span>
    -   <span data-ttu-id="abe49-258">L’état d’exécution exécute, ou valide, toutes les commandes auxquelles le gestionnaire est lié.</span><span class="sxs-lookup"><span data-stu-id="abe49-258">The Execute state executes, or commits to, any commands to which the handler is bound.</span></span>
    -   <span data-ttu-id="abe49-259">L’état d’aperçu affiche un aperçu des commandes auxquelles le gestionnaire est lié.</span><span class="sxs-lookup"><span data-stu-id="abe49-259">The Preview state previews any commands to which the handler is bound.</span></span> <span data-ttu-id="abe49-260">Cela permet essentiellement d’exécuter les commandes sans valider le résultat.</span><span class="sxs-lookup"><span data-stu-id="abe49-260">This essentially executes the commands without committing to the result.</span></span>
    -   <span data-ttu-id="abe49-261">L’État CancelPreview annule toutes les commandes prévisualisées.</span><span class="sxs-lookup"><span data-stu-id="abe49-261">The CancelPreview state cancels any previewed Commands.</span></span> <span data-ttu-id="abe49-262">Cela est nécessaire pour prendre en charge le parcours via un menu ou une liste, et pour afficher un aperçu séquentiel et annuler les résultats en fonction des besoins.</span><span class="sxs-lookup"><span data-stu-id="abe49-262">This is required to support traversal through a menu or list and sequentially preview and undo the results as required.</span></span>

<span data-ttu-id="abe49-263">L’exemple suivant illustre un gestionnaire de commandes de la Galerie.</span><span class="sxs-lookup"><span data-stu-id="abe49-263">The following example demonstrates a gallery command handler.</span></span>


```C++
/*
 * GALLERY COMMAND HANDLER IMPLEMENTATION
 */
class CGalleryCommandHandler
      : public CComObjectRootEx<CComMultiThreadModel>
      , public IUICommandHandler
{
public:
  BEGIN_COM_MAP(CGalleryCommandHandler)
    COM_INTERFACE_ENTRY(IUICommandHandler)
  END_COM_MAP()

  // Gallery command handler's Execute method
  STDMETHODIMP Execute(UINT nCmdID,
                       UI_EXECUTIONVERB verb, 
                       const PROPERTYKEY* key,
                       const PROPVARIANT* ppropvarValue,
                       IUISimplePropertySet* pCommandExecutionProperties)
  {
    HRESULT hr = S_OK;
        
    // Switch on manner of execution (Execute/Preview/CancelPreview)
    switch (verb)
    {
      case UI_EXECUTIONVERB_EXECUTE:
        if(nCmdID == cmdTextSizeGallery || 
           nCmdID == cmdTextSizeGallery2 || 
           nCmdID == cmdTextSizeGallery3)
        {
          if (pCommandExecutionProperties != NULL)
          {
            CItemProperties *pItem = 
              static_cast<CItemProperties *>(pCommandExecutionProperties);
            g_prevSelection = g_index = pItem->GetIndex();
            UpdateGallerySelectedItems();
            ::InvalidateRect(g_hWindowFrame, NULL, TRUE);
          }
          else
          {
            g_prevSelection = g_index = 0;
            UpdateGallerySelectedItems();
            ::InvalidateRect(g_hWindowFrame, NULL, TRUE);
          }
        }           
        break;
      case UI_EXECUTIONVERB_PREVIEW:
        CItemProperties *pItem = 
          static_cast<CItemProperties *>(pCommandExecutionProperties);
        g_index = pItem->GetIndex();
        ::InvalidateRect(g_hWindowFrame, NULL, TRUE);
        break;
      case UI_EXECUTIONVERB_CANCELPREVIEW:
        g_index = g_prevSelection;
        ::InvalidateRect(g_hWindowFrame, NULL, TRUE);
        break;
    }   
    return hr;
  }

  // Gallery command handler's UpdateProperty method
  STDMETHODIMP UpdateProperty(UINT nCmdID,
                              REFPROPERTYKEY key,
                              const PROPVARIANT* ppropvarCurrentValue,
                              PROPVARIANT* ppropvarNewValue)
  {
    UNREFERENCED_PARAMETER(ppropvarCurrentValue);

    HRESULT hr = E_NOTIMPL;         

    if (key == UI_PKEY_ItemsSource) // Gallery items requested
    {
      if (nCmdID == cmdTextSizeGallery || 
          nCmdID == cmdTextSizeGallery2 || 
          nCmdID == cmdTextSizeGallery3)
      {
        CComQIPtr<IUICollection> spCollection(ppropvarCurrentValue->punkVal);

        int count = _countof(g_labels);

        for (int i = 0; i < count; i++)
        {
          CComObject<CItemProperties> * pItem;
          CComObject<CItemProperties>::CreateInstance(&pItem);
                    
          pItem->AddRef();
          pItem->Initialize(i);

          spCollection->Add(pItem);
        }
        return S_OK;
      }
      if (nCmdID == cmdCommandGallery1)
      {
        CComQIPtr<IUICollection> spCollection(ppropvarCurrentValue->punkVal);

        int count = 12;
        int commands[] = {cmdButton1, 
                          cmdButton2, 
                          cmdBoolean1, 
                          cmdBoolean2, 
                          cmdButton1, 
                          cmdButton2, 
                          cmdBoolean1, 
                          cmdBoolean2, 
                          cmdButton1, 
                          cmdButton2, 
                          cmdBoolean1, 
                          cmdBoolean2};

        for (int i = 0; i < count; i++)
        {
          CComObject<CItemProperties> * pItem;
          CComObject<CItemProperties>::CreateInstance(&pItem);
                    
          pItem->AddRef();
          pItem->InitializeAsCommand(commands[i]);

          spCollection->Add(pItem);
        }
        return S_OK;
      }
    }        
    else if (key == UI_PKEY_SelectedItem) // Selected item requested
    {           
      hr = UIInitPropertyFromUInt32(UI_PKEY_SelectedItem, g_index, ppropvarNewValue);           
    }
    return hr;
  }
};

```



### <a name="bind-the-command-handler"></a><span data-ttu-id="abe49-264">Lier le gestionnaire de commandes</span><span class="sxs-lookup"><span data-stu-id="abe49-264">Bind the Command Handler</span></span>

<span data-ttu-id="abe49-265">Une fois que vous avez défini un gestionnaire de commandes, la commande doit être liée au gestionnaire.</span><span class="sxs-lookup"><span data-stu-id="abe49-265">After you define a Command handler, the Command must be bound to the handler.</span></span>

<span data-ttu-id="abe49-266">L’exemple suivant montre comment lier une commande de la galerie à un gestionnaire de commandes spécifique.</span><span class="sxs-lookup"><span data-stu-id="abe49-266">The following example demonstrates how to bind a gallery Command to a specific Command handler.</span></span> <span data-ttu-id="abe49-267">Dans ce cas, les contrôles [**ComboBox**](windowsribbon-element-combobox.md) et Gallery sont liés à leurs gestionnaires de commandes respectifs.</span><span class="sxs-lookup"><span data-stu-id="abe49-267">In this case, both the [**ComboBox**](windowsribbon-element-combobox.md) and gallery controls are bound to their respective Command handlers.</span></span>


```C++
// Called for each Command in markup. 
// Application will return a Command handler for each Command.
STDMETHOD(OnCreateUICommand)(UINT32 nCmdID,
                             UI_COMMANDTYPE typeID,
                             IUICommandHandler** ppCommandHandler) 
{   
  // CommandType for ComboBox and galleries
  if (typeID == UI_COMMANDTYPE_COLLECTION || typeID == UI_COMMANDTYPE_COMMANDCOLLECTION) 
  {
    switch (nCmdID)
    {
      case cmdComboBox:
        CComObject<CComboBoxCommandHandler> * pComboBoxCommandHandler;
        CComObject<CComboBoxCommandHandler>::CreateInstance(&pComboBoxCommandHandler);
        return pComboBoxCommandHandler->QueryInterface(IID_PPV_ARGS(ppCommandHandler));
      default:
        CComObject<CGalleryCommandHandler> * pGalleryCommandHandler;
        CComObject<CGalleryCommandHandler>::CreateInstance(&pGalleryCommandHandler);
        return pGalleryCommandHandler->QueryInterface(IID_PPV_ARGS(ppCommandHandler));
    }
    return E_NOTIMPL; // Command is not implemented, so do not pass a handler back.
  }
}
```



### <a name="initialize-a-collection"></a><span data-ttu-id="abe49-268">Initialiser une collection</span><span class="sxs-lookup"><span data-stu-id="abe49-268">Initialize a Collection</span></span>

<span data-ttu-id="abe49-269">L’exemple suivant illustre une implémentation personnalisée de [**IUISimplePropertySet**](/windows/desktop/api/uiribbon/nn-uiribbon-iuisimplepropertyset) pour les galeries d’éléments et de commandes.</span><span class="sxs-lookup"><span data-stu-id="abe49-269">The following example demonstrates a custom implementation of [**IUISimplePropertySet**](/windows/desktop/api/uiribbon/nn-uiribbon-iuisimplepropertyset) for both item and Command galleries.</span></span>

<span data-ttu-id="abe49-270">La classe CItemProperties dans cet exemple est dérivée de [**IUISimplePropertySet**](/windows/desktop/api/uiribbon/nn-uiribbon-iuisimplepropertyset).</span><span class="sxs-lookup"><span data-stu-id="abe49-270">The CItemProperties class in this example is derived from [**IUISimplePropertySet**](/windows/desktop/api/uiribbon/nn-uiribbon-iuisimplepropertyset).</span></span> <span data-ttu-id="abe49-271">En plus de la méthode [**IUISimplePropertySet :: GetValue**](/windows/desktop/api/uiribbon/nf-uiribbon-iuisimplepropertyset-getvalue)requise, la classe CItemProperties implémente un ensemble de fonctions d’assistance pour l’initialisation et le suivi d’index.</span><span class="sxs-lookup"><span data-stu-id="abe49-271">In addition to the required method [**IUISimplePropertySet::GetValue**](/windows/desktop/api/uiribbon/nf-uiribbon-iuisimplepropertyset-getvalue), the CItemProperties class implements a set of helper functions for initialization and index tracking.</span></span>


```C++
//
//  PURPOSE:    Implementation of IUISimplePropertySet.
//
//  COMMENTS:
//              Three gallery-specific helper functions included. 
//

class CItemProperties
  : public CComObjectRootEx<CComMultiThreadModel>
  , public IUISimplePropertySet
{
  public:

  // COM map for QueryInterface of IUISimplePropertySet.
  BEGIN_COM_MAP(CItemProperties)
    COM_INTERFACE_ENTRY(IUISimplePropertySet)
  END_COM_MAP()

  // Required method that enables property key values to be 
  // retrieved on gallery collection items.
  STDMETHOD(GetValue)(REFPROPERTYKEY key, PROPVARIANT *ppropvar)
  {
    HRESULT hr;

    // No category is associated with this item.
    if (key == UI_PKEY_CategoryId)
    {
      return UIInitiPropertyFromUInt32(UI_PKEY_CategoryId, 
                                       UI_COLLECTION_INVALIDINDEX, 
                                       pprovar);
    }

    // A Command gallery.
    // _isCommandGallery is set on initialization.
    if (_isCommandGallery)
    {           
      if(key == UI_PKEY_CommandId && _isCommandGallery)
      {
        // Return a pointer to the CommandId of the item.
        return InitPropVariantFromUInt32(_cmdID, ppropvar);
      }         
    }
    // An item gallery.
    else
    {
      if (key == UI_PKEY_Label)
      {
        // Return a pointer to the item label string.
        return UIInitPropertyFromString(UI_PKEY_Label, ppropvar);
      }
      else if(key == UI_PKEY_ItemImage)
      {
        // Return a pointer to the item image.
        return UIInitPropertyFromImage(UI_PKEY_ItemImage, ppropvar);
      }         
    }
    return E_NOTIMPL;
  }

  // Initialize an item in an item gallery collection at the specified index.
  void Initialize(int index)
  {
    _index = index;
    _cmdID = 0;
    _isCommandGallery = false;
  }

  // Initialize a Command in a Command gallery.
  void InitializeAsCommand(__in UINT cmdID)
  {
    _index = 0;
    _cmdID = cmdID;
    _isCommandGallery = true;
  }

  // Gets the index of the selected item in an item gallery.
  int GetIndex()
  {
    return _index;
  }

private:
  int _index;
  int _cmdID;
  bool _isCommandGallery;   
};
```



### <a name="handle-collection-events"></a><span data-ttu-id="abe49-272">Gérer les événements de collection</span><span class="sxs-lookup"><span data-stu-id="abe49-272">Handle Collection Events</span></span>

<span data-ttu-id="abe49-273">L’exemple suivant illustre une implémentation de IUICollectionChangedEvent.</span><span class="sxs-lookup"><span data-stu-id="abe49-273">The following example demonstrates an IUICollectionChangedEvent implementation.</span></span>


```C++
class CQATChangedEvent
  : public CComObjectRootEx<CComSingleThreadModel>
  , public IUICollectionChangedEvent
{
  public:

  HRESULT FinalConstruct()
  {
    _pSite = NULL;
    return S_OK;
  }

  void Initialize(__in CQATSite* pSite)
  {
    if (pSite != NULL)
    {
      _pSite = pSite;
    }
  }

  void Uninitialize()
  {
    _pSite = NULL;
  }

  BEGIN_COM_MAP(CQATChangedEvent)
    COM_INTERFACE_ENTRY(IUICollectionChangedEvent)
  END_COM_MAP()

  // IUICollectionChangedEvent interface
  STDMETHOD(OnChanged)(UI_COLLECTIONCHANGE action, 
                       UINT32 oldIndex, 
                       IUnknown *pOldItem, 
                       UINT32 newIndex, 
                       IUnknown *pNewItem)
  {
    if (_pSite)
    {
      _pSite->OnCollectionChanged(action, oldIndex, pOldItem, newIndex, pNewItem);
    }
    return S_OK;
  }

  protected:
  virtual ~CQATChangedEvent(){}

  private:
  CQATSite* _pSite; // Weak ref to avoid circular refcounts
};

HRESULT CQATHandler::EnsureCollectionEventListener(__in IUICollection* pUICollection)
{
  // Check if listener already exists.
  if (_spQATChangedEvent)
  {
    return S_OK;
  }

  HRESULT hr = E_FAIL;

  // Create an IUICollectionChangedEvent listener.
  hr = CreateInstanceWithRefCountOne(&_spQATChangedEvent);
    
  if (SUCCEEDED(hr))
  {
    CComPtr<IUnknown> spUnknown;
    _spQATChangedEvent->QueryInterface(IID_PPV_ARGS(&spUnknown));

    // Create a connection between the collection connection point and the sink.
    AtlAdvise(pUICollection, spUnknown, __uuidof(IUICollectionChangedEvent), &_dwCookie);
    _spQATChangedEvent->Initialize(this);
  }
  return hr;
}

HRESULT CQATHandler::OnCollectionChanged(
             UI_COLLECTIONCHANGE action, 
          UINT32 oldIndex, 
             IUnknown *pOldItem, 
          UINT32 newIndex, 
          IUnknown *pNewItem)
{
    UNREFERENCED_PARAMETER(oldIndex);
    UNREFERENCED_PARAMETER(newIndex);

    switch (action)
    {
      case UI_COLLECTIONCHANGE_INSERT:
      {
        CComQIPtr<IUISimplePropertySet> spProperties(pNewItem);
                
        PROPVARIANT var;
        if (SUCCEEDED(spProperties->GetValue(UI_PKEY_CommandId, &var)))
        {
          UINT tcid;
          if (SUCCEEDED(UIPropertyToUInt32(UI_PKEY_CommandId, var, &tcid)))
          {
            FireETWEvent(tcid, L"Added to QAT");
            PropVariantClear(&var);
          }
        }
      }
      break;
      case UI_COLLECTIONCHANGE_REMOVE:
      {
        CComQIPtr<IUISimplePropertySet> spProperties(pOldItem);
                
        PROPVARIANT var;
        if (SUCCEEDED(spProperties->GetValue(UI_PKEY_CommandId, &var)))
        {
          UINT tcid;
          if (SUCCEEDED(UIPropertyToUInt32(UI_PKEY_CommandId, var, &tcid)))
          {
            FireETWEvent(tcid, L"Removed from QAT");
            PropVariantClear(&var);
          }
        }
      }
      break;
    default:
  }
  return S_OK;
}
```



## <a name="related-topics"></a><span data-ttu-id="abe49-274">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="abe49-274">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="abe49-275">Propriétés de la collection</span><span class="sxs-lookup"><span data-stu-id="abe49-275">Collection Properties</span></span>](windowsribbon-reference-properties-collection.md)
</dt> <dt>

[<span data-ttu-id="abe49-276">Création d’une application de ruban</span><span class="sxs-lookup"><span data-stu-id="abe49-276">Creating a Ribbon Application</span></span>](windowsribbon-stepbystep.md)
</dt> <dt>

[<span data-ttu-id="abe49-277">Fonctionnement des commandes et des contrôles</span><span class="sxs-lookup"><span data-stu-id="abe49-277">Understanding Commands and Controls</span></span>](windowsribbon-commandscontrols.md)
</dt> <dt>

[<span data-ttu-id="abe49-278">Instructions relatives à l’expérience utilisateur du ruban</span><span class="sxs-lookup"><span data-stu-id="abe49-278">Ribbon User Experience Guidelines</span></span>](https://msdn.microsoft.com/library/cc872782.aspx)
</dt> <dt>

[<span data-ttu-id="abe49-279">Processus de conception du ruban</span><span class="sxs-lookup"><span data-stu-id="abe49-279">Ribbon Design Process</span></span>](https://msdn.microsoft.com/library/cc872781.aspx)
</dt> <dt>

[<span data-ttu-id="abe49-280">Exemple de Galerie</span><span class="sxs-lookup"><span data-stu-id="abe49-280">Gallery Sample</span></span>](windowsribbon-gallerysample.md)
</dt> </dl>

 

 