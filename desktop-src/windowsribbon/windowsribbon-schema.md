---
title: Déclaration des commandes et des contrôles avec le balisage du ruban
description: L’infrastructure de ruban Windows utilise un langage de balisage basé sur Extensible Application Markup Language (XAML) pour implémenter de manière déclarative l’apparence d’une application de ruban.
ms.assetid: 76bacfb3-ecaf-47b3-be97-afa5e7e52330
keywords:
- Ruban Windows, structure de balisage
- Ruban, structure de balisage
- Ruban Windows, séparation de la présentation de la logique de commande
- Ruban, séparation de la présentation de la logique de commande
- Ruban Windows, composants
- Ruban, composants
- système de commandes pour le ruban Windows
- contrôles pour le ruban Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c97c5c193332ce217709c825a58f0ae546c03c9c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104382378"
---
# <a name="declaring-commands-and-controls-with-ribbon-markup"></a><span data-ttu-id="4d04d-111">Déclaration des commandes et des contrôles avec le balisage du ruban</span><span class="sxs-lookup"><span data-stu-id="4d04d-111">Declaring Commands and Controls with Ribbon Markup</span></span>

<span data-ttu-id="4d04d-112">L’infrastructure de ruban Windows utilise un langage de balisage basé sur Extensible Application Markup Language (XAML) pour implémenter de manière déclarative l’apparence d’une application de ruban.</span><span class="sxs-lookup"><span data-stu-id="4d04d-112">The Windows Ribbon framework uses a markup language based on Extensible Application Markup Language (XAML) to declaratively implement the appearance of a Ribbon application.</span></span>

-   [<span data-ttu-id="4d04d-113">Séparation de la présentation de la logique de commande</span><span class="sxs-lookup"><span data-stu-id="4d04d-113">Separating Presentation from Command Logic</span></span>](#separating-presentation-from-command-logic)
-   [<span data-ttu-id="4d04d-114">Structure de balisage</span><span class="sxs-lookup"><span data-stu-id="4d04d-114">Markup Structure</span></span>](#markup-structure)
-   [<span data-ttu-id="4d04d-115">Composants du ruban</span><span class="sxs-lookup"><span data-stu-id="4d04d-115">Ribbon Components</span></span>](#ribbon-components)
-   [<span data-ttu-id="4d04d-116">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="4d04d-116">Related topics</span></span>](#related-topics)

## <a name="separating-presentation-from-command-logic"></a><span data-ttu-id="4d04d-117">Séparation de la présentation de la logique de commande</span><span class="sxs-lookup"><span data-stu-id="4d04d-117">Separating Presentation from Command Logic</span></span>

<span data-ttu-id="4d04d-118">La séparation des attributs de présentation et visuels de la logique de commande dans l’infrastructure du ruban s’effectue via deux plateformes de développement distinctes, mais dépendantes.</span><span class="sxs-lookup"><span data-stu-id="4d04d-118">The separation of presentation and visual attributes from command logic in the Ribbon framework is accomplished through two distinct, but dependent, development platforms.</span></span> <span data-ttu-id="4d04d-119">Les dispositions de contrôle, les comportements de mise à l’échelle, les déclarations de commande et les spécifications de ressources sont le domaine au moment de la conception d’une syntaxe de balisage déclarative basée sur la spécification [Extensible Application Markup Language (XAML)](/dotnet/framework/wpf/advanced/xaml-in-wpf) .</span><span class="sxs-lookup"><span data-stu-id="4d04d-119">Control layouts, scaling behaviors, Command declarations, and resource specifications are the design time domain of a declarative markup syntax based on the [Extensible Application Markup Language (XAML)](/dotnet/framework/wpf/advanced/xaml-in-wpf) specification.</span></span> <span data-ttu-id="4d04d-120">Les fonctionnalités de bas niveau, les crochets d’application et les gestionnaires de commandes sont définis dans les implémentations d’interface basées sur le modèle COM (Component Object Model).</span><span class="sxs-lookup"><span data-stu-id="4d04d-120">Low level functionality, application hooks, and Command handlers are defined in Component Object Model (COM)-based interface implementations.</span></span>

<span data-ttu-id="4d04d-121">Cette séparation de la présentation et de la logique offre les avantages suivants :</span><span class="sxs-lookup"><span data-stu-id="4d04d-121">This separation of presentation and logic provides the following benefits:</span></span>

-   <span data-ttu-id="4d04d-122">Un cycle de développement d’applications plus efficace qui permet aux développeurs d’interface utilisateur et aux concepteurs d’implémenter l’interface graphique utilisateur de l’application ruban indépendamment de la fonctionnalité d’application principale.</span><span class="sxs-lookup"><span data-stu-id="4d04d-122">A more efficient application development cycle which allows UI developers and designers to implement the GUI of the Ribbon application independently from the core application functionality.</span></span> <span data-ttu-id="4d04d-123">Cette fonctionnalité principale peut être laissée aux développeurs de logiciels dédiés.</span><span class="sxs-lookup"><span data-stu-id="4d04d-123">This core functionality can be left to dedicated software developers.</span></span>
-   <span data-ttu-id="4d04d-124">Maintenance moins coûteuse, car les modifications apportées à l’interface graphique sont possibles sans modification des fonctionnalités principales (et inversement).</span><span class="sxs-lookup"><span data-stu-id="4d04d-124">Less costly maintenance because changes to the GUI are possible without changes to core functionality (and vice versa).</span></span>
-   <span data-ttu-id="4d04d-125">Spécification simple de ressources de type chaîne et image par le biais du balisage.</span><span class="sxs-lookup"><span data-stu-id="4d04d-125">Simple specification of string and image resources through markup.</span></span>
-   <span data-ttu-id="4d04d-126">Facilité de prototypage.</span><span class="sxs-lookup"><span data-stu-id="4d04d-126">Ease of prototyping.</span></span>

## <a name="markup-structure"></a><span data-ttu-id="4d04d-127">Structure de balisage</span><span class="sxs-lookup"><span data-stu-id="4d04d-127">Markup Structure</span></span>

<span data-ttu-id="4d04d-128">Deux branches distinctes existent dans la structure du balisage de l’infrastructure du ruban.</span><span class="sxs-lookup"><span data-stu-id="4d04d-128">Two distinct branches exist within the structure of Ribbon framework markup.</span></span>

<span data-ttu-id="4d04d-129">La première branche contient un manifeste de déclarations de commande et de ressource (chaînes et images).</span><span class="sxs-lookup"><span data-stu-id="4d04d-129">The first branch contains a manifest of Command and resource declarations (strings and images).</span></span> <span data-ttu-id="4d04d-130">Chaque entrée de commande est utilisée par l’infrastructure pour lier un contrôle de ruban, via un ID de commande, à un gestionnaire de commandes défini dans le code de l’application.</span><span class="sxs-lookup"><span data-stu-id="4d04d-130">Each Command entry is used by the framework to bind a Ribbon control, through a Command ID, to a Command handler defined in the application code.</span></span>

<span data-ttu-id="4d04d-131">La deuxième branche contient les déclarations de contrôle réelles.</span><span class="sxs-lookup"><span data-stu-id="4d04d-131">The second branch contains the actual control declarations.</span></span> <span data-ttu-id="4d04d-132">Chaque contrôle est associé à une commande via un attribut *CommandName* qui correspond à un attribut *Name* spécifié dans chaque déclaration de commande.</span><span class="sxs-lookup"><span data-stu-id="4d04d-132">Each control is associated with a Command through a *CommandName* attribute that maps to a *Name* attribute specified in each Command declaration.</span></span>

## <a name="ribbon-components"></a><span data-ttu-id="4d04d-133">Composants du ruban</span><span class="sxs-lookup"><span data-stu-id="4d04d-133">Ribbon Components</span></span>

<span data-ttu-id="4d04d-134">Les fonctionnalités de l’interface utilisateur de l’infrastructure du ruban sont exposées par le biais de [vues](windowsribbon-reference-elements-view.md).</span><span class="sxs-lookup"><span data-stu-id="4d04d-134">Ribbon framework UI functionality is exposed through [Views](windowsribbon-reference-elements-view.md).</span></span> <span data-ttu-id="4d04d-135">Une vue est essentiellement un conteneur, tel que le [**ruban**](windowsribbon-element-ribbon.md) et [**ContextPopup**](windowsribbon-element-contextpopup.md), qui est utilisé pour présenter des contrôles d’infrastructure et les commandes auxquelles elles sont liées.</span><span class="sxs-lookup"><span data-stu-id="4d04d-135">A View is essentially a container, such as the [**Ribbon**](windowsribbon-element-ribbon.md) and [**ContextPopup**](windowsribbon-element-contextpopup.md), that is used to present framework controls and the Commands they are bound to.</span></span>

<span data-ttu-id="4d04d-136">La vue du [**ruban**](windowsribbon-element-ribbon.md) est composée de plusieurs composants qui incluent un [menu d’application](windowsribbon-controls-applicationmenu.md), la [barre d’outils accès rapide (qat)](windowsribbon-controls-quickaccesstoolbar.md) pour l’affichage des commandes couramment utilisées à partir de l’interface ruban, des [onglets](windowsribbon-controls-tab.md) principaux et contextuels qui contiennent des [groupes](windowsribbon-controls-group.md) de contrôles et le riche système de menu contextuel du [**ContextPopup**](windowsribbon-element-contextpopup.md).</span><span class="sxs-lookup"><span data-stu-id="4d04d-136">The [**Ribbon**](windowsribbon-element-ribbon.md) View is composed of several components that include an [Application Menu](windowsribbon-controls-applicationmenu.md), the [Quick Access Toolbar (QAT)](windowsribbon-controls-quickaccesstoolbar.md) for displaying commonly used Commands from the ribbon UI, core and contextual [tabs](windowsribbon-controls-tab.md) that contain [groups](windowsribbon-controls-group.md) of controls, and the rich context menu system of the [**ContextPopup**](windowsribbon-element-contextpopup.md).</span></span>

<span data-ttu-id="4d04d-137">Tous les composants de ruban sont déclarés dans un fichier de balisage autonome qui :</span><span class="sxs-lookup"><span data-stu-id="4d04d-137">All Ribbon components are declared in a standalone markup file that:</span></span>

-   <span data-ttu-id="4d04d-138">Spécifie les propriétés de base pour chaque élément.</span><span class="sxs-lookup"><span data-stu-id="4d04d-138">Specifies the basic properties for each element.</span></span>
-   <span data-ttu-id="4d04d-139">Affiche clairement les relations hiérarchiques.</span><span class="sxs-lookup"><span data-stu-id="4d04d-139">Shows hierarchical relationships clearly.</span></span>
-   <span data-ttu-id="4d04d-140">Fournit des préférences de disposition et des indicateurs de mise à l’échelle.</span><span class="sxs-lookup"><span data-stu-id="4d04d-140">Supplies layout preferences and scaling hints.</span></span> <span data-ttu-id="4d04d-141">Pour plus d’informations sur les modèles de disposition de l’infrastructure du ruban, consultez [Personnalisation d’un ruban à l’aide de définitions de taille et de stratégies de mise à l’échelle](windowsribbon-templates.md).</span><span class="sxs-lookup"><span data-stu-id="4d04d-141">For more information on Ribbon framework layout templates, see [Customizing a Ribbon Through Size Definitions and Scaling Policies](windowsribbon-templates.md).</span></span>
-   <span data-ttu-id="4d04d-142">Fournit un moyen de définir des ressources telles que des images et des étiquettes.</span><span class="sxs-lookup"><span data-stu-id="4d04d-142">Provides a way to define resources such as images and labels.</span></span> <span data-ttu-id="4d04d-143">Pour plus d’informations sur les ressources d’image, consultez [spécification des ressources d’image de ruban](windowsribbon-imageformats.md).</span><span class="sxs-lookup"><span data-stu-id="4d04d-143">For more information on image resources, see [Specifying Ribbon Image Resources](windowsribbon-imageformats.md).</span></span>

<span data-ttu-id="4d04d-144">Les deux exemples de balisage de ruban suivants montrent comment un ensemble d’éléments de menu d’application de ruban est associé à un nom de commande et à un ID.</span><span class="sxs-lookup"><span data-stu-id="4d04d-144">The following two Ribbon markup examples demonstrate how a set of Ribbon Application Menu items are each associated with a Command name and ID.</span></span>

1.  <span data-ttu-id="4d04d-145">Cette section présente les déclarations de commande requises pour un menu d’application avec des commandes de base telles que nouveau, ouvrir et enregistrer.</span><span class="sxs-lookup"><span data-stu-id="4d04d-145">This section shows the Command declarations required for an Application Menu with basic commands such as New, Open, and Save.</span></span>
    ```XML
    <!-- Command declarations for the Application Menu. -->
    <Command Name="cmdFileMenu"
             Symbol="ID_FILE_MENU"
             Id="25000" />
    <!-- Command declaration for most recently used items. -->
    <Command Name="cmdMRUItems"
             Symbol="ID_FILE_MRUITEMS"
             Id="25050"/>
    <!-- Command declarations for Application Menu items. -->
    <Command Name="cmdNew"
             Symbol="ID_FILE_NEW"
             Comment="New"
             Id="25001"
             LabelTitle="&amp;New"/>
    <Command Name="cmdOpen"
             Symbol="ID_FILE_OPEN"
             Comment="Open"
             Id="25002"
             LabelTitle="&amp;&amp;Open"/>
    <Command>
      <Command.Name>cmdSave</Command.Name>
      <Command.Symbol>ID_FILE_SAVE</Command.Symbol>
      <Command.Comment>Save</Command.Comment>
      <Command.Id>25003</Command.Id>
      <Command.LabelTitle>
        <String>
          <String.Content>Label for Save</String.Content>
          <String.Id>59999</String.Id>
          <String.Symbol>strSave</String.Symbol>
        </String>
      </Command.LabelTitle>
      <Command.TooltipTitle>Tooltip title with &amp;&amp; for Save Command</Command.TooltipTitle>
      <Command.TooltipDescription>Tooltip description for Save Command.</Command.TooltipDescription>
      <Command.Keytip>s1</Command.Keytip>
    </Command>
    <Command Name="cmdPrint"
             Symbol="ID_FILE_PRINT"
             Comment="Save"
             Id="25004"
             LabelTitle="Print" />
    <Command Name="cmdExit"
             Symbol="ID_FILE_EXIT"
             Comment="Exit"
             Id="25005"
             LabelTitle="Exit" />
    ```

    

2.  <span data-ttu-id="4d04d-146">Cette section présente les déclarations de contrôle associées.</span><span class="sxs-lookup"><span data-stu-id="4d04d-146">This section shows the associated Control declarations.</span></span>
    ```XML
    <!-- Control declarations for Application Menu items. -->
    <Ribbon.ApplicationMenu>
      <ApplicationMenu CommandName="cmdFileMenu">
        <!-- Most recently used items collection. -->
        <ApplicationMenu.RecentItems>
          <RecentItems CommandName="cmdMRUItems"/>
        </ApplicationMenu.RecentItems>
        <!-- Menu items collection. -->
        <MenuGroup>
          <Button CommandName="cmdNew" />
          <Button CommandName="cmdOpen" />
          <Button CommandName="cmdSave" />
        </MenuGroup>
        <MenuGroup>
          <Button CommandName="cmdPrint" />
          <Button CommandName="cmdExit" />
        </MenuGroup>
      </ApplicationMenu>
    </Ribbon.ApplicationMenu>
    ```

    

<span data-ttu-id="4d04d-147">Lorsque le balisage est compilé avec l’outil compilateur de commande d’interface utilisateur (UICC), les noms et les ID de commande sont placés dans un fichier d’en-tête utilisé par l’application hôte du ruban.</span><span class="sxs-lookup"><span data-stu-id="4d04d-147">When the markup is compiled with the UI Command Compiler (UICC) tool, the Command names and IDs are placed into a header file used by the Ribbon host application.</span></span>

<span data-ttu-id="4d04d-148">Voici un exemple de fichier d’en-tête généré par UICC.</span><span class="sxs-lookup"><span data-stu-id="4d04d-148">The following is an example of a header file generated by UICC.</span></span>


```
// *****************************************************************************
// * This is an automatically generated header file for UI Element definition  *
// * resource symbols and values. Please do not modify manually.               *
// *****************************************************************************

#pragma once

#define cmdFileMenu 25000 
#define cmdNew 22001  /* New */ 
#define cmdNew_LabelTitle_RESID 60005
#define cmdOpen 22002  /* Open */ 
#define cmdOpen_LabelTitle_RESID 60006
#define cmdSave 22003  /* Save */ 
#define cmdSave_LabelTitle_RESID 60007
#define cmdSave_TooltipTitle_RESID 60008
#define cmdSave_TooltipDescription_RESID 60009
```



## <a name="related-topics"></a><span data-ttu-id="4d04d-149">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="4d04d-149">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4d04d-150">Extensible Application Markup Language (XAML)</span><span class="sxs-lookup"><span data-stu-id="4d04d-150">Extensible Application Markup Language (XAML)</span></span>](/dotnet/framework/wpf/advanced/xaml-in-wpf)
</dt> <dt>

[<span data-ttu-id="4d04d-151">Compilation du balisage du ruban</span><span class="sxs-lookup"><span data-stu-id="4d04d-151">Compiling Ribbon Markup</span></span>](windowsribbon-intentcl.md)
</dt> </dl>

 

 