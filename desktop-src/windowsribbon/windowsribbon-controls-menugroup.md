---
title: Groupe de menus
description: Le groupe de menus organise les commandes et les contrôles connexes dans un menu ou une barre d’outils.
ms.assetid: 5454f2a3-275b-47f4-ae97-d10dd12da5ff
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9862e78cbedf84b92c7540bec4de58288af5c9ef
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103941258"
---
# <a name="menu-group"></a><span data-ttu-id="51aad-103">Groupe de menus</span><span class="sxs-lookup"><span data-stu-id="51aad-103">Menu Group</span></span>

<span data-ttu-id="51aad-104">Le groupe de menus organise les commandes et les contrôles connexes dans un menu ou une barre d’outils.</span><span class="sxs-lookup"><span data-stu-id="51aad-104">The Menu Group organizes related Commands and controls within a menu or toolbar.</span></span>

-   [<span data-ttu-id="51aad-105">Introduction</span><span class="sxs-lookup"><span data-stu-id="51aad-105">Introduction</span></span>](#introduction)
-   [<span data-ttu-id="51aad-106">Propriétés du groupe de menus</span><span class="sxs-lookup"><span data-stu-id="51aad-106">Menu Group Properties</span></span>](#menu-group-properties)
-   [<span data-ttu-id="51aad-107">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="51aad-107">Related topics</span></span>](#related-topics)

## <a name="introduction"></a><span data-ttu-id="51aad-108">Introduction</span><span class="sxs-lookup"><span data-stu-id="51aad-108">Introduction</span></span>

<span data-ttu-id="51aad-109">Le contrôle de groupe de menus, exposé via l’élément de balisage [**MenuGroup**](windowsribbon-element-menugroup.md) , est un conteneur logique pour les groupes d’éléments ou de commandes dans les contrôles basés sur des menus, y compris la mini-barre d’outils [contextuelle](windowsribbon-controls-contextpopup.md) .</span><span class="sxs-lookup"><span data-stu-id="51aad-109">The Menu Group control, exposed through the [**MenuGroup**](windowsribbon-element-menugroup.md) markup element, is a logical container for groups of items or Commands in menu-based controls, including the [Context Popup](windowsribbon-controls-contextpopup.md) Mini-Toolbar.</span></span>

<span data-ttu-id="51aad-110">Une étiquette peut être spécifiée pour un groupe de menus via l’attribut *LabelTitle* ou la propriété [**Command. LabelTitle**](windowsribbon-element-command-labeltitle.md) d’une déclaration de commande associée.</span><span class="sxs-lookup"><span data-stu-id="51aad-110">A label can be specified for a Menu Group through the *LabelTitle* attribute or [**Command.LabelTitle**](windowsribbon-element-command-labeltitle.md) property of an associated Command declaration.</span></span> <span data-ttu-id="51aad-111">La valeur assignée à *LabelTitle* est rendue sous la forme d’un en-tête de catégorie.</span><span class="sxs-lookup"><span data-stu-id="51aad-111">The value assigned to *LabelTitle* is rendered as a category header.</span></span>

<span data-ttu-id="51aad-112">L’exemple suivant illustre le balisage de commande pour un contrôle [bouton partagé](windowsribbon-controls-splitbutton.md) qui comprend deux déclarations de commande de groupe de menus.</span><span class="sxs-lookup"><span data-stu-id="51aad-112">The following example demonstrates the Command markup for a [Split Button](windowsribbon-controls-splitbutton.md) control that includes two Menu Group Command declarations.</span></span>


```XML
<!-- SplitButton -->
<Command Name="cmdSplitButtonGroup"
         Symbol="cmdSplitButtonGroup"
         Comment="SplitButton Group"
         LabelTitle="SplitButton"/>
<Command Name="cmdSplitButton"
         Symbol="cmdSplitButton"
         Comment="SplitButton"
         LabelTitle="SplitButton"/>
<Command Name="cmdSBButtonItem"
         Symbol="cmdSBButtonItem"
         Comment="SBButtonItem"
         LabelTitle="SB ButtonItem"/>
<Command Name="cmdSBButton1"
         Symbol="cmdSBButton1"
         Comment="SBButton1"
         LabelTitle="SB Button">
  <Command.LargeImages>
    <Image Source="res/copyL_32.bmp"/>
  </Command.LargeImages>
  <Command.SmallImages>
    <Image Source="res/copyS_16.bmp"/>
  </Command.SmallImages>
  <Command.LargeHighContrastImages>
    <Image Source="res/copyLHC_32.bmp"/>
  </Command.LargeHighContrastImages>
  <Command.SmallHighContrastImages>
    <Image Source="res/copySHC_16.bmp"/>
  </Command.SmallHighContrastImages>
</Command>
<Command Name="cmdSBMajorItems"
         Comment="Major Items Category"
         LabelTitle="Major Items"/>
<Command Name="cmdSBStandardItems"
         Comment="Standard Items Category"
         LabelTitle="Standard Items"/>
```



<span data-ttu-id="51aad-113">L’exemple suivant illustre le balisage requis pour un élément [**SplitButton**](windowsribbon-element-splitbutton.md) avec trois déclarations d’élément [**MenuGroup**](windowsribbon-element-menugroup.md) , deux d’entre elles étant associées aux commandes de groupe de menus de l’exemple précédent.</span><span class="sxs-lookup"><span data-stu-id="51aad-113">The following example demonstrates the markup required for a [**SplitButton**](windowsribbon-element-splitbutton.md) element with three [**MenuGroup**](windowsribbon-element-menugroup.md) element declarations, two of which are associated with the Menu Group Commands from the previous example.</span></span> <span data-ttu-id="51aad-114">L’attribut *Class* de l’élément **MenuGroup** est utilisé pour spécifier la taille des éléments de menu.</span><span class="sxs-lookup"><span data-stu-id="51aad-114">The *Class* attribute of the **MenuGroup** element is used to specify the size of the menu items.</span></span>


```XML
<Group CommandName="cmdSplitButtonGroup">
  <SplitButton CommandName="cmdSplitButton">
    <SplitButton.ButtonItem>
      <Button CommandName="cmdSBButtonItem"/>
    </SplitButton.ButtonItem>
    <SplitButton.MenuGroups>
      <MenuGroup CommandName="cmdSBMajorItems" 
                 Class="MajorItems">
        <Button CommandName="cmdSBButton1"/>
        <Button CommandName="cmdSBButton1"/>
      </MenuGroup>
      <MenuGroup CommandName="cmdSBStandardItems"
                 Class="StandardItems">
        <Button CommandName="cmdSBButton1"/>
        <Button CommandName="cmdSBButton1"/>
      </MenuGroup>
      <MenuGroup Class="StandardItems">
        <Button CommandName="cmdSBButton1"/>
        <Button CommandName="cmdSBButton1"/>
      </MenuGroup>
    </SplitButton.MenuGroups>
  </SplitButton>
</Group>
```



<span data-ttu-id="51aad-115">La capture d’écran suivante illustre le menu (avec trois contrôles de groupe de menus) généré à partir du balisage dans les exemples précédents.</span><span class="sxs-lookup"><span data-stu-id="51aad-115">The following screen shot illustrates the menu (with three Menu Group controls) that is generated from the markup in the previous examples.</span></span>

![capture d’écran d’un menu avec trois contrôles de groupe de menus.](images/controls/menugroup.png)

## <a name="menu-group-properties"></a><span data-ttu-id="51aad-117">Propriétés du groupe de menus</span><span class="sxs-lookup"><span data-stu-id="51aad-117">Menu Group Properties</span></span>

<span data-ttu-id="51aad-118">L’infrastructure du ruban définit une collection de [clés de propriété](windowsribbon-reference-properties.md) pour le contrôle de groupe de menus.</span><span class="sxs-lookup"><span data-stu-id="51aad-118">The Ribbon framework defines a collection of [property keys](windowsribbon-reference-properties.md) for the Menu Group control.</span></span>

<span data-ttu-id="51aad-119">En général, une propriété de groupe de menus est mise à jour dans l’interface utilisateur du ruban en invalidant la commande associée au contrôle via un appel à la méthode [**IUIFramework :: InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) .</span><span class="sxs-lookup"><span data-stu-id="51aad-119">Typically, a Menu Group property is updated in the ribbon UI by invalidating the Command associated with the control through a call to the [**IUIFramework::InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) method.</span></span> <span data-ttu-id="51aad-120">L’événement d’invalidation est géré, et les mises à jour de la propriété sont définies par la méthode de rappel [**IUICommandHandler :: UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) .</span><span class="sxs-lookup"><span data-stu-id="51aad-120">The invalidation event is handled, and the property updates defined, by the [**IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) callback method.</span></span>

<span data-ttu-id="51aad-121">La méthode de rappel [**IUICommandHandler :: UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) n’est pas exécutée et l’application a interrogé une valeur de propriété mise à jour, jusqu’à ce que la propriété soit requise par le Framework.</span><span class="sxs-lookup"><span data-stu-id="51aad-121">The [**IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) callback method is not executed, and the application queried for an updated property value, until the property is required by the framework.</span></span> <span data-ttu-id="51aad-122">Par exemple, lorsqu’un onglet est activé et qu’un contrôle est affiché dans l’interface ruban, ou lorsqu’une info-bulle est affichée.</span><span class="sxs-lookup"><span data-stu-id="51aad-122">For example, when a tab is activated and a control revealed in the ribbon UI, or when a tooltip is displayed.</span></span>

> [!Note]  
> <span data-ttu-id="51aad-123">Dans certains cas, une propriété peut être récupérée par le biais de la méthode [**IUIFramework :: GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) et définie avec la méthode [**IUIFramework :: SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) .</span><span class="sxs-lookup"><span data-stu-id="51aad-123">In some cases, a property can be retrieved through the [**IUIFramework::GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) method and set with the [**IUIFramework::SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) method.</span></span>

 

<span data-ttu-id="51aad-124">Le tableau suivant répertorie les clés de propriété associées au contrôle de groupe de menus.</span><span class="sxs-lookup"><span data-stu-id="51aad-124">The following table lists the property keys that are associated with the Menu Group control.</span></span>



| <span data-ttu-id="51aad-125">Clé de propriété</span><span class="sxs-lookup"><span data-stu-id="51aad-125">Property Key</span></span>                                                                                     | <span data-ttu-id="51aad-126">Notes</span><span class="sxs-lookup"><span data-stu-id="51aad-126">Notes</span></span>                                                                                                                                                                                                                         |
|--------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="51aad-127">IU-au-dessus \_ \_ activé</span><span class="sxs-lookup"><span data-stu-id="51aad-127">UI\_PKEY\_Enabled</span></span>](windowsribbon-reference-properties-uipkey-enabled.md)                       | <span data-ttu-id="51aad-128">Prend en charge [**IUIFramework :: GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) et [**IUIFramework :: SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty).</span><span class="sxs-lookup"><span data-stu-id="51aad-128">Supports [**IUIFramework::GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) and [**IUIFramework::SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty).</span></span> |
| [<span data-ttu-id="51aad-129">KeyTip de l’interface utilisateur \_ \_</span><span class="sxs-lookup"><span data-stu-id="51aad-129">UI\_PKEY\_Keytip</span></span>](windowsribbon-reference-properties-uipkey-keytip.md)                         | <span data-ttu-id="51aad-130">Peut uniquement être mis à jour par le biais d’une invalidation.</span><span class="sxs-lookup"><span data-stu-id="51aad-130">Can only be updated through invalidation.</span></span>                                                                                                                                                                                     |
| [<span data-ttu-id="51aad-131">\_Étiquette de nom de l’interface utilisateur \_</span><span class="sxs-lookup"><span data-stu-id="51aad-131">UI\_PKEY\_Label</span></span>](windowsribbon-reference-properties-uipkey-label.md)                           | <span data-ttu-id="51aad-132">Peut uniquement être mis à jour par le biais d’une invalidation.</span><span class="sxs-lookup"><span data-stu-id="51aad-132">Can only be updated through invalidation.</span></span>                                                                                                                                                                                     |
| [<span data-ttu-id="51aad-133">IU \_ \_ TooltipDescription</span><span class="sxs-lookup"><span data-stu-id="51aad-133">UI\_PKEY\_TooltipDescription</span></span>](windowsribbon-reference-properties-uipkey-tooltipdescription.md) | <span data-ttu-id="51aad-134">Peut uniquement être mis à jour par le biais d’une invalidation.</span><span class="sxs-lookup"><span data-stu-id="51aad-134">Can only be updated through invalidation.</span></span>                                                                                                                                                                                     |
| [<span data-ttu-id="51aad-135">IU \_ \_ TooltipTitle</span><span class="sxs-lookup"><span data-stu-id="51aad-135">UI\_PKEY\_TooltipTitle</span></span>](windowsribbon-reference-properties-uipkey-tooltiptitle.md)             | <span data-ttu-id="51aad-136">Peut uniquement être mis à jour par le biais d’une invalidation.</span><span class="sxs-lookup"><span data-stu-id="51aad-136">Can only be updated through invalidation.</span></span>                                                                                                                                                                                     |



 

## <a name="related-topics"></a><span data-ttu-id="51aad-137">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="51aad-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="51aad-138">Bibliothèque de contrôles de l’infrastructure du ruban Windows</span><span class="sxs-lookup"><span data-stu-id="51aad-138">Windows Ribbon Framework Control Library</span></span>](windowsribbon-controls-entry.md)
</dt> <dt>

[<span data-ttu-id="51aad-139">**Élément de balisage MenuGroup**</span><span class="sxs-lookup"><span data-stu-id="51aad-139">**MenuGroup markup element**</span></span>](windowsribbon-element-menugroup.md)
</dt> </dl>

 

 