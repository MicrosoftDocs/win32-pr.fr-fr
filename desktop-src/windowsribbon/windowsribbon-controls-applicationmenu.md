---
title: Menu de l’application
description: Le menu application est le menu principal d’une application qui implémente l’infrastructure de ruban Windows.
ms.assetid: 5be93a5b-277b-44c1-be24-a0598a140bfc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e99f57045daa35149e5fa074cb59e2f538c589b2
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103842309"
---
# <a name="application-menu"></a><span data-ttu-id="d2371-103">Menu de l’application</span><span class="sxs-lookup"><span data-stu-id="d2371-103">Application Menu</span></span>

<span data-ttu-id="d2371-104">Le menu application est le menu principal d’une application qui implémente l’infrastructure de ruban Windows.</span><span class="sxs-lookup"><span data-stu-id="d2371-104">The Application Menu is the main menu for an application that implements the Windows Ribbon framework.</span></span>

-   [<span data-ttu-id="d2371-105">Introduction</span><span class="sxs-lookup"><span data-stu-id="d2371-105">Introduction</span></span>](#introduction)
-   [<span data-ttu-id="d2371-106">Composants du menu de l’application</span><span class="sxs-lookup"><span data-stu-id="d2371-106">Components of the Application Menu</span></span>](#components-of-the-application-menu)
    -   [<span data-ttu-id="d2371-107">Menu de l’application MenuGroup</span><span class="sxs-lookup"><span data-stu-id="d2371-107">Application Menu MenuGroup</span></span>](#application-menu-menugroup)
-   [<span data-ttu-id="d2371-108">Dimensionnement du menu de l’application</span><span class="sxs-lookup"><span data-stu-id="d2371-108">Sizing the Application Menu</span></span>](#sizing-the-application-menu)
-   [<span data-ttu-id="d2371-109">Propriétés du menu de l’application</span><span class="sxs-lookup"><span data-stu-id="d2371-109">Application Menu Properties</span></span>](#application-menu-properties)
-   [<span data-ttu-id="d2371-110">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="d2371-110">Related topics</span></span>](#related-topics)

## <a name="introduction"></a><span data-ttu-id="d2371-111">Introduction</span><span class="sxs-lookup"><span data-stu-id="d2371-111">Introduction</span></span>

<span data-ttu-id="d2371-112">Le menu application se compose d’un contrôle de bouton déroulant qui affiche un menu contenant les commandes qui exposent les fonctionnalités liées à un projet complet, telles que l’intégralité d’un document, d’une image ou d’un film.</span><span class="sxs-lookup"><span data-stu-id="d2371-112">The Application Menu is composed of a drop-down button control that displays a menu containing Commands that expose functionality related to a complete project, such as an entire document, picture, or movie.</span></span> <span data-ttu-id="d2371-113">Les exemples incluent les commandes **nouveau**, **ouvrir**, **Enregistrer** et **quitter** .</span><span class="sxs-lookup"><span data-stu-id="d2371-113">Examples include the **New**, **Open**, **Save**, and **Exit** Commands.</span></span>

<span data-ttu-id="d2371-114">La capture d’écran suivante illustre le menu de l’application.</span><span class="sxs-lookup"><span data-stu-id="d2371-114">The following screen shot illustrates the Application Menu.</span></span>

![capture d’écran du menu de l’application et de la liste des éléments récents du ruban Paint pour Windows 7.](images/controls/recentitems.png)

## <a name="components-of-the-application-menu"></a><span data-ttu-id="d2371-116">Composants du menu de l’application</span><span class="sxs-lookup"><span data-stu-id="d2371-116">Components of the Application Menu</span></span>

<span data-ttu-id="d2371-117">Le menu application est un élément obligatoire dans une application de ruban.</span><span class="sxs-lookup"><span data-stu-id="d2371-117">The Application Menu is a mandatory element in any Ribbon application.</span></span> <span data-ttu-id="d2371-118">Le point d’entrée dans le menu de l’application est un bouton distinctif qui apparaît en tant que premier élément de la ligne d' [onglet](windowsribbon-controls-tab.md) , comme illustré dans la capture d’écran suivante.</span><span class="sxs-lookup"><span data-stu-id="d2371-118">The entry point into the Application Menu is a distinctive button that appears as the first item in the [Tab](windowsribbon-controls-tab.md) row, as shown in the following screen shot.</span></span>

> [!Note]  
> <span data-ttu-id="d2371-119">Windows 8 et versions ultérieures : l’image du bouton de menu de l’application a été changée en étiquette : **fichier**.</span><span class="sxs-lookup"><span data-stu-id="d2371-119">Windows 8 and newer: Application Menu button image changed to label: **File**.</span></span> <span data-ttu-id="d2371-120">Nous vous recommandons de ne pas utiliser de fichier comme étiquette pour vos propres onglets.</span><span class="sxs-lookup"><span data-stu-id="d2371-120">We recommend that you do not use File as the label for any of your own tabs.</span></span>

 

![capture d’écran du bouton de menu de l’application de WordPad pour Windows 7.](images/overviews/applicationmenu-button.png)

<span data-ttu-id="d2371-122">Lorsque vous cliquez dessus, ce bouton affiche le menu détaillé qui s’affiche dans la capture d’écran suivante (le menu de l’application de WordPad pour Windows 7).</span><span class="sxs-lookup"><span data-stu-id="d2371-122">When clicked, this button displays the rich menu that is shown in the following screen shot (the Application Menu from WordPad for Windows 7).</span></span>

![capture d’écran du menu de l’application dans WordPad pour Windows 7.](images/overviews/applicationmenu-menu.png)

> [!Note]  
> <span data-ttu-id="d2371-124">Il n’y a aucun impact sur le jeu d’onglets lorsque l’utilisateur clique sur le bouton de menu de l’application ; au lieu de cela, le focus entre dans le menu.</span><span class="sxs-lookup"><span data-stu-id="d2371-124">There is no impact on the tab set when the Application Menu button is clicked; instead, the focus enters the menu.</span></span>

 

<span data-ttu-id="d2371-125">Le menu application contient deux volets : une liste de commandes représentées par un ou plusieurs éléments [**MenuGroup**](windowsribbon-element-menugroup.md) et une liste d' [éléments récents](windowsribbon-controls-recentitems.md) représentée par un élément [**ApplicationMenu. RecentItems**](windowsribbon-element-applicationmenu-recentitems.md) .</span><span class="sxs-lookup"><span data-stu-id="d2371-125">The Application Menu contains two panes: a list of Commands represented by one or more [**MenuGroup**](windowsribbon-element-menugroup.md) elements, and a [Recent Items](windowsribbon-controls-recentitems.md) list represented by an [**ApplicationMenu.RecentItems**](windowsribbon-element-applicationmenu-recentitems.md) element.</span></span>

### <a name="application-menu-menugroup"></a><span data-ttu-id="d2371-126">Menu de l’application MenuGroup</span><span class="sxs-lookup"><span data-stu-id="d2371-126">Application Menu MenuGroup</span></span>

<span data-ttu-id="d2371-127">L’élément [**ApplicationMenu**](windowsribbon-element-applicationmenu.md) doit contenir au moins un élément enfant [**MenuGroup**](windowsribbon-element-menugroup.md) qui expose une liste de commandes au niveau de l’application.</span><span class="sxs-lookup"><span data-stu-id="d2371-127">The [**ApplicationMenu**](windowsribbon-element-applicationmenu.md) element must contain at least one [**MenuGroup**](windowsribbon-element-menugroup.md) child element that exposes a list of application-level commands.</span></span> <span data-ttu-id="d2371-128">Si plusieurs éléments **MenuGroup** sont déclarés, une ligne de séparation est dessinée entre les groupes, comme illustré dans la capture d’écran suivante.</span><span class="sxs-lookup"><span data-stu-id="d2371-128">If multiple **MenuGroup** elements are declared, a divider line is drawn between the groups, as shown in the following screen shot.</span></span>

![capture d’écran d’un menu d’application MenuGroup.](images/overviews/applicationmenu-menugroup.png)

<span data-ttu-id="d2371-130">Voici une liste de contraintes pour un élément [**MenuGroup**](windowsribbon-element-menugroup.md) d’un menu d’application :</span><span class="sxs-lookup"><span data-stu-id="d2371-130">The following is a list of constraints for a [**MenuGroup**](windowsribbon-element-menugroup.md) element of an Application Menu:</span></span>

-   <span data-ttu-id="d2371-131">Tous les éléments [**MenuGroup**](windowsribbon-element-menugroup.md) doivent être déclarés avec une valeur d’attribut de *classe* de `MajorItems` .</span><span class="sxs-lookup"><span data-stu-id="d2371-131">All [**MenuGroup**](windowsribbon-element-menugroup.md) items must be declared with a *Class* attribute value of `MajorItems`.</span></span>
-   <span data-ttu-id="d2371-132">Un menu d’application  [**MenuGroup**](windowsribbon-element-menugroup.md) prend uniquement en charge le [bouton](windowsribbon-controls-button.md), le [bouton bascule](windowsribbon-controls-togglebutton.md), le [bouton déroulant](windowsribbon-controls-dropdownbutton.md), le bouton [partagé](windowsribbon-controls-splitbutton.md), [la Galerie](windowsribbon-controls-dropdowngallery.md)déroulante et les contrôles de la [Galerie de boutons partagés](windowsribbon-controls-splitbuttongallery.md) .</span><span class="sxs-lookup"><span data-stu-id="d2371-132">An Application Menu  [**MenuGroup**](windowsribbon-element-menugroup.md) supports only the [Button](windowsribbon-controls-button.md), [Toggle Button](windowsribbon-controls-togglebutton.md), [Drop-Down Button](windowsribbon-controls-dropdownbutton.md), [Split Button](windowsribbon-controls-splitbutton.md), [Drop-Down Gallery](windowsribbon-controls-dropdowngallery.md), and [Split Button Gallery](windowsribbon-controls-splitbuttongallery.md) controls.</span></span>
    > <span data-ttu-id="d2371-133">\[! Précieuse\]</span><span class="sxs-lookup"><span data-stu-id="d2371-133">\[!Important\]</span></span>  
    > <span data-ttu-id="d2371-134">Les galeries de commandes sont le seul type de Galerie pris en charge dans le menu de l’application.</span><span class="sxs-lookup"><span data-stu-id="d2371-134">Command galleries are the only type of gallery that are supported in the Application Menu.</span></span> <span data-ttu-id="d2371-135">Pour plus d’informations sur les contrôles de la Galerie, consultez [utilisation des galeries](./ribbon-controls-galleries.md).</span><span class="sxs-lookup"><span data-stu-id="d2371-135">See [Working with Galleries](./ribbon-controls-galleries.md), for more information on gallery controls.</span></span>

     

<span data-ttu-id="d2371-136">Quand un [bouton](windowsribbon-controls-button.md) ou un [bouton bascule](windowsribbon-controls-togglebutton.md) est utilisé dans un [**MenuGroup**](windowsribbon-element-menugroup.md), la valeur de [**Command. LabelTitle**](windowsribbon-element-command-labeltitle.md) est affichée dans le menu et les valeurs de [**Command. TooltipTitle**](windowsribbon-element-command-tooltiptitle.md) et [**Command. TooltipDescription**](windowsribbon-element-command-tooltipdescription.md) sont affichées comme info-bulle, comme illustré dans la capture d’écran suivante.</span><span class="sxs-lookup"><span data-stu-id="d2371-136">When a [Button](windowsribbon-controls-button.md) or [Toggle Button](windowsribbon-controls-togglebutton.md) is used in a [**MenuGroup**](windowsribbon-element-menugroup.md), the value of [**Command.LabelTitle**](windowsribbon-element-command-labeltitle.md) is displayed in the menu and the values of [**Command.TooltipTitle**](windowsribbon-element-command-tooltiptitle.md) and [**Command.TooltipDescription**](windowsribbon-element-command-tooltipdescription.md) are displayed as the tooltip, as shown in the following screen shot.</span></span>

![capture d’écran d’un contrôle bouton dans un menu d’application.](images/overviews/applicationmenu-menubutton.png)

<span data-ttu-id="d2371-138">Quand un [bouton](windowsribbon-controls-dropdownbutton.md)déroulant, un [bouton partagé](windowsribbon-controls-splitbutton.md), [une galerie](windowsribbon-controls-dropdowngallery.md)déroulante ou une [bibliothèque de boutons partagés](windowsribbon-controls-splitbuttongallery.md) est utilisé dans le menu de l’application, la partie de menu s’affiche sous la forme d’un menu volant qui couvre et masque le volet **éléments récents** .</span><span class="sxs-lookup"><span data-stu-id="d2371-138">When a [Drop-Down Button](windowsribbon-controls-dropdownbutton.md), [Split Button](windowsribbon-controls-splitbutton.md), [Drop-Down Gallery](windowsribbon-controls-dropdowngallery.md), or [Split Button Gallery](windowsribbon-controls-splitbuttongallery.md) is used in the Application Menu, the menu portion is displayed as a flyout that covers and conceals the **Recent items** pane.</span></span>

<span data-ttu-id="d2371-139">Pour les contrôles bouton [partagé](windowsribbon-controls-splitbutton.md) et [bouton déroulant](windowsribbon-controls-dropdownbutton.md) , la valeur de [**Command. LabelDescription**](windowsribbon-element-command-labeldescription.md) est présentée en ligne dans le menu contextuel pour aider les utilisateurs à découvrir la fonctionnalité de commande.</span><span class="sxs-lookup"><span data-stu-id="d2371-139">For [Split Button](windowsribbon-controls-splitbutton.md) and [Drop-Down Button](windowsribbon-controls-dropdownbutton.md) controls, the value of [**Command.LabelDescription**](windowsribbon-element-command-labeldescription.md) is shown inline in the flyout menu to visually assist users with discovering the Command functionality.</span></span> <span data-ttu-id="d2371-140">La valeur affichée de **Command. LabelDescription** est divisée par programmation sur une étendue de deux lignes, et une tentative est effectuée pour ajuster la valeur exactement au volet des **éléments récents** sous.</span><span class="sxs-lookup"><span data-stu-id="d2371-140">The displayed value of **Command.LabelDescription** is programmatically broken over a two-line span, and an attempt is made to fit the value exactly over the **Recent items** pane beneath.</span></span> <span data-ttu-id="d2371-141">Si la valeur **Command. LabelDescription** n’est pas adaptée, le menu volant se développe pour s’adapter à la valeur [**Command. Comment**](windowsribbon-element-command-comment.md) la plus longue dans le [**MenuGroup**](windowsribbon-element-menugroup.md).</span><span class="sxs-lookup"><span data-stu-id="d2371-141">If the **Command.LabelDescription** value does not fit, the flyout will expand to accommodate the longest [**Command.Comment**](windowsribbon-element-command-comment.md) value in the [**MenuGroup**](windowsribbon-element-menugroup.md).</span></span>

<span data-ttu-id="d2371-142">La capture d’écran suivante illustre ces comportements dans un menu volant de [bouton partagé](windowsribbon-controls-splitbutton.md) .</span><span class="sxs-lookup"><span data-stu-id="d2371-142">The following screen shot illustrates these behaviors in a [Split Button](windowsribbon-controls-splitbutton.md) flyout.</span></span>

![capture d’écran d’un menu volant de contrôle de liste dans un menu d’application.](images/overviews/applicationmenu-menuflyout.png)

<span data-ttu-id="d2371-144">Avec une [Galerie déroulante](windowsribbon-controls-dropdowngallery.md) et une [Galerie de boutons partagés](windowsribbon-controls-splitbuttongallery.md), seule une étiquette et une image sont affichées.</span><span class="sxs-lookup"><span data-stu-id="d2371-144">With a [Drop-Down Gallery](windowsribbon-controls-dropdowngallery.md) and a [Split Button Gallery](windowsribbon-controls-splitbuttongallery.md), only a label and an image are shown.</span></span>

## <a name="sizing-the-application-menu"></a><span data-ttu-id="d2371-145">Dimensionnement du menu de l’application</span><span class="sxs-lookup"><span data-stu-id="d2371-145">Sizing the Application Menu</span></span>

<span data-ttu-id="d2371-146">Le dimensionnement du menu de l’application est géré par l’infrastructure du ruban.</span><span class="sxs-lookup"><span data-stu-id="d2371-146">Sizing of the Application Menu is handled by the Ribbon framework.</span></span> <span data-ttu-id="d2371-147">Si des chaînes très longues sont fournies pour la valeur de [**Command. LabelTitle**](windowsribbon-element-command-labeltitle.md) ou [**Command. LabelDescription**](windowsribbon-element-command-labeldescription.md), ou si une longue liste de commandes est utilisée, le menu ajuste sa taille pour s’adapter au contenu.</span><span class="sxs-lookup"><span data-stu-id="d2371-147">If very long strings are supplied for the value of [**Command.LabelTitle**](windowsribbon-element-command-labeltitle.md) or [**Command.LabelDescription**](windowsribbon-element-command-labeldescription.md), or a long list of Commands is used, the menu will adjust its size to accommodate the contents.</span></span> <span data-ttu-id="d2371-148">Certaines formes d’ajustement incluent l’augmentation de la taille des menus volants ou des volets de menu, ainsi que l’ajout de visionneuses panoramiques lorsque le défilement est requis.</span><span class="sxs-lookup"><span data-stu-id="d2371-148">Some forms of adjustment include expanding the size of flyouts or menu panes, and adding pan viewers when scrolling is required.</span></span>

## <a name="application-menu-properties"></a><span data-ttu-id="d2371-149">Propriétés du menu de l’application</span><span class="sxs-lookup"><span data-stu-id="d2371-149">Application Menu Properties</span></span>

<span data-ttu-id="d2371-150">L’infrastructure du ruban définit une collection de [clés de propriété](windowsribbon-reference-properties.md) pour le contrôle de menu de l’application.</span><span class="sxs-lookup"><span data-stu-id="d2371-150">The Ribbon framework defines a collection of [property keys](windowsribbon-reference-properties.md) for the Application Menu control.</span></span>

<span data-ttu-id="d2371-151">En général, une propriété de menu de l’application est mise à jour dans l’interface ruban en invalidant la commande associée au contrôle via un appel à la méthode [**IUIFramework :: InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) .</span><span class="sxs-lookup"><span data-stu-id="d2371-151">Typically, an Application Menu property is updated in the ribbon UI by invalidating the Command associated with the control through a call to the [**IUIFramework::InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) method.</span></span> <span data-ttu-id="d2371-152">L’événement d’invalidation est géré et les mises à jour de propriété sont définies par la méthode de rappel [**IUICommandHandler :: UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) .</span><span class="sxs-lookup"><span data-stu-id="d2371-152">The invalidation event is handled and the property updates are defined by the [**IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) callback method.</span></span>

<span data-ttu-id="d2371-153">La méthode de rappel [**IUICommandHandler :: UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) n’est pas exécutée et l’application n’est pas interrogée pour obtenir une valeur de propriété mise à jour tant que la propriété n’est pas requise par le Framework.</span><span class="sxs-lookup"><span data-stu-id="d2371-153">The [**IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) callback method is not executed and the application is not queried for an updated property value until the property is required by the framework.</span></span> <span data-ttu-id="d2371-154">Par exemple, l’infrastructure requiert la propriété lorsqu’un onglet est activé et qu’un contrôle est affiché dans l’interface ruban, ou lorsqu’une info-bulle est affichée.</span><span class="sxs-lookup"><span data-stu-id="d2371-154">For example, the framework requires the property when a tab is activated and a control is revealed in the ribbon UI, or when a tooltip is displayed.</span></span>



| <span data-ttu-id="d2371-155">Clé de propriété</span><span class="sxs-lookup"><span data-stu-id="d2371-155">Property key</span></span>                                                                                     | <span data-ttu-id="d2371-156">Notes</span><span class="sxs-lookup"><span data-stu-id="d2371-156">Notes</span></span>                                     |
|--------------------------------------------------------------------------------------------------|-------------------------------------------|
| [<span data-ttu-id="d2371-157">IU \_ \_ TooltipDescription</span><span class="sxs-lookup"><span data-stu-id="d2371-157">UI\_PKEY\_TooltipDescription</span></span>](windowsribbon-reference-properties-uipkey-tooltipdescription.md) | <span data-ttu-id="d2371-158">Peut uniquement être mis à jour par le biais d’une invalidation.</span><span class="sxs-lookup"><span data-stu-id="d2371-158">Can only be updated through invalidation.</span></span> |
| [<span data-ttu-id="d2371-159">IU \_ \_ TooltipTitle</span><span class="sxs-lookup"><span data-stu-id="d2371-159">UI\_PKEY\_TooltipTitle</span></span>](windowsribbon-reference-properties-uipkey-tooltiptitle.md)             | <span data-ttu-id="d2371-160">Peut uniquement être mis à jour par le biais d’une invalidation.</span><span class="sxs-lookup"><span data-stu-id="d2371-160">Can only be updated through invalidation.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="d2371-161">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="d2371-161">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d2371-162">Bibliothèque de contrôles de l’infrastructure du ruban Windows</span><span class="sxs-lookup"><span data-stu-id="d2371-162">Windows Ribbon Framework Control Library</span></span>](windowsribbon-controls-entry.md)
</dt> <dt>

[<span data-ttu-id="d2371-163">**Élément de balisage ApplicationMenu**</span><span class="sxs-lookup"><span data-stu-id="d2371-163">**ApplicationMenu markup element**</span></span>](windowsribbon-element-applicationmenu.md)
</dt> </dl>

 

 