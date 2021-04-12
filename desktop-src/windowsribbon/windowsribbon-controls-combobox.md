---
title: Zone de liste déroulante (infrastructure de ruban Windows)
description: La zone de liste déroulante se compose d’une zone de liste à une seule colonne qui contient une collection d’éléments ou de commandes s’excluant mutuellement, associés à un contrôle statique ou d’édition et une flèche de déroulement.
ms.assetid: 6b7de2ec-dcb7-44cb-b01f-db1ba0643499
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c61c19963811d12557beafe3c5cff314c927ae7
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104464063"
---
# <a name="combo-box-windows-ribbon-framework"></a><span data-ttu-id="df165-103">Zone de liste déroulante (infrastructure de ruban Windows)</span><span class="sxs-lookup"><span data-stu-id="df165-103">Combo Box (Windows Ribbon Framework)</span></span>

<span data-ttu-id="df165-104">La zone de liste déroulante se compose d’une zone de liste à une seule colonne qui contient une collection d’éléments ou de commandes s’excluant mutuellement, associés à un contrôle statique ou d’édition et une flèche de déroulement.</span><span class="sxs-lookup"><span data-stu-id="df165-104">The Combo Box consists of a single-column list box that contains a collection of mutually exclusive items or Commands combined with a static or edit control and a drop-down arrow.</span></span> <span data-ttu-id="df165-105">La partie zone de liste du contrôle s’affiche lorsque l’utilisateur clique sur la flèche déroulante.</span><span class="sxs-lookup"><span data-stu-id="df165-105">The list box portion of the control is displayed when the user clicks the drop-down arrow.</span></span>

-   [<span data-ttu-id="df165-106">Détails</span><span class="sxs-lookup"><span data-stu-id="df165-106">Details</span></span>](#details)
-   [<span data-ttu-id="df165-107">Propriétés de la zone de liste déroulante</span><span class="sxs-lookup"><span data-stu-id="df165-107">Combo Box Properties</span></span>](#combo-box-properties)
-   [<span data-ttu-id="df165-108">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="df165-108">Related topics</span></span>](#related-topics)

## <a name="details"></a><span data-ttu-id="df165-109">Détails</span><span class="sxs-lookup"><span data-stu-id="df165-109">Details</span></span>

<span data-ttu-id="df165-110">L’élément ou la commande actuellement sélectionné (le cas échéant) dans la zone de liste s’affiche dans le contrôle static ou Edit.</span><span class="sxs-lookup"><span data-stu-id="df165-110">The currently selected item or Command (if any) in the list box is displayed in the static or edit control.</span></span> <span data-ttu-id="df165-111">Avec un contrôle d’édition, si l’utilisateur tape les caractères initiaux d’un élément ou d’une commande existant, la zone de liste met en surbrillance le premier élément avec ces caractères initiaux et complète automatiquement l’entrée dans le contrôle d’édition.</span><span class="sxs-lookup"><span data-stu-id="df165-111">With an edit control, if the user types the initial characters of an existing item or Command, the list box will highlight the first item with those initial characters and autocomplete the entry in the edit control.</span></span>

<span data-ttu-id="df165-112">Prend uniquement en charge une barre de redimensionnement verticale ou une poignée de redimensionnement.</span><span class="sxs-lookup"><span data-stu-id="df165-112">Supports a vertical gripper bar, or resizing handle, only.</span></span>

<span data-ttu-id="df165-113">Ce contrôle est utile pour exposer des éléments de texte simples et étroitement liés.</span><span class="sxs-lookup"><span data-stu-id="df165-113">This control is useful for exposing simple, closely related text items.</span></span>

<span data-ttu-id="df165-114">La capture d’écran suivante illustre la zone de liste déroulante du ruban dans Live Movie Maker.</span><span class="sxs-lookup"><span data-stu-id="df165-114">The following screen shot illustrates the Ribbon Combo Box in Live Movie Maker.</span></span>

![capture d’écran d’un contrôle de zone de liste déroulante dans le ruban Microsoft Paint.](images/controls/combobox.png)

## <a name="combo-box-properties"></a><span data-ttu-id="df165-116">Propriétés de la zone de liste déroulante</span><span class="sxs-lookup"><span data-stu-id="df165-116">Combo Box Properties</span></span>

<span data-ttu-id="df165-117">L’infrastructure du ruban définit une collection de [clés de propriété](windowsribbon-reference-properties.md) pour le contrôle de zone de liste déroulante.</span><span class="sxs-lookup"><span data-stu-id="df165-117">The Ribbon framework defines a collection of [property keys](windowsribbon-reference-properties.md) for the Combo Box control.</span></span>

<span data-ttu-id="df165-118">En règle générale, une propriété de zone de liste déroulante est mise à jour dans l’interface ruban en invalidant la commande associée au contrôle via un appel à la méthode [**IUIFramework :: InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) .</span><span class="sxs-lookup"><span data-stu-id="df165-118">Typically, a Combo Box property is updated in the ribbon UI by invalidating the Command associated with the control through a call to the [**IUIFramework::InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) method.</span></span> <span data-ttu-id="df165-119">L’événement d’invalidation est géré, et les mises à jour de la propriété sont définies par la méthode de rappel [**IUICommandHandler :: UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) .</span><span class="sxs-lookup"><span data-stu-id="df165-119">The invalidation event is handled, and the property updates defined, by the [**IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) callback method.</span></span>

<span data-ttu-id="df165-120">La méthode de rappel [**IUICommandHandler :: UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) n’est pas exécutée et l’application a interrogé une valeur de propriété mise à jour, jusqu’à ce que la propriété soit requise par le Framework.</span><span class="sxs-lookup"><span data-stu-id="df165-120">The [**IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) callback method is not executed, and the application queried for an updated property value, until the property is required by the framework.</span></span> <span data-ttu-id="df165-121">Par exemple, lorsqu’un onglet est activé et qu’un contrôle est affiché dans l’interface ruban, ou lorsqu’une info-bulle est affichée.</span><span class="sxs-lookup"><span data-stu-id="df165-121">For example, when a tab is activated and a control revealed in the ribbon UI, or when a tooltip is displayed.</span></span>

> [!Note]  
> <span data-ttu-id="df165-122">Dans certains cas, une propriété peut être récupérée par le biais de la méthode [**IUIFramework :: GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) et définie avec la méthode [**IUIFramework :: SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) .</span><span class="sxs-lookup"><span data-stu-id="df165-122">In some cases, a property can be retrieved through the [**IUIFramework::GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) method and set with the [**IUIFramework::SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) method.</span></span>

 

<span data-ttu-id="df165-123">Le tableau suivant répertorie les clés de propriété associées au contrôle de zone de liste déroulante.</span><span class="sxs-lookup"><span data-stu-id="df165-123">The following table lists the property keys that are associated with the Combo Box control.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="df165-124">Clé de propriété</span><span class="sxs-lookup"><span data-stu-id="df165-124">Property Key</span></span></th>
<th><span data-ttu-id="df165-125">Notes</span><span class="sxs-lookup"><span data-stu-id="df165-125">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="df165-126"><a href="windowsribbon-reference-properties-uipkey-categories.md">UI_PKEY_Categories</a></span><span class="sxs-lookup"><span data-stu-id="df165-126"><a href="windowsribbon-reference-properties-uipkey-categories.md">UI_PKEY_Categories</a></span></span></td>
<td><span data-ttu-id="df165-127">Prend en charge <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework :: GetUICommandProperty</strong></a> et <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework :: SetUICommandProperty</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="df165-127">Supports <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> and <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="df165-128"><a href="windowsribbon-reference-properties-uipkey-enabled.md">UI_PKEY_Enabled</a></span><span class="sxs-lookup"><span data-stu-id="df165-128"><a href="windowsribbon-reference-properties-uipkey-enabled.md">UI_PKEY_Enabled</a></span></span></td>
<td><span data-ttu-id="df165-129">Prend en charge <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework :: GetUICommandProperty</strong></a> et <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework :: SetUICommandProperty</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="df165-129">Supports <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> and <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="df165-130"><a href="windowsribbon-reference-properties-uipkey-itemssource.md">UI_PKEY_ItemsSource</a></span><span class="sxs-lookup"><span data-stu-id="df165-130"><a href="windowsribbon-reference-properties-uipkey-itemssource.md">UI_PKEY_ItemsSource</a></span></span></td>
<td><span data-ttu-id="df165-131">Prend en charge <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework :: GetUICommandProperty</strong></a> et <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework :: SetUICommandProperty</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="df165-131">Supports <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> and <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="df165-132"><a href="windowsribbon-reference-properties-uipkey-keytip.md">UI_PKEY_Keytip</a></span><span class="sxs-lookup"><span data-stu-id="df165-132"><a href="windowsribbon-reference-properties-uipkey-keytip.md">UI_PKEY_Keytip</a></span></span></td>
<td><span data-ttu-id="df165-133">Peut uniquement être mis à jour par le biais d’une invalidation.</span><span class="sxs-lookup"><span data-stu-id="df165-133">Can only be updated through invalidation.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="df165-134"><a href="windowsribbon-reference-properties-uipkey-label.md">UI_PKEY_Label</a></span><span class="sxs-lookup"><span data-stu-id="df165-134"><a href="windowsribbon-reference-properties-uipkey-label.md">UI_PKEY_Label</a></span></span></td>
<td><span data-ttu-id="df165-135">Peut uniquement être mis à jour par le biais d’une invalidation.</span><span class="sxs-lookup"><span data-stu-id="df165-135">Can only be updated through invalidation.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="df165-136"><a href="windowsribbon-reference-properties-uipkey-largehighcontrastimage.md">UI_PKEY_LargeHighContrastImage</a></span><span class="sxs-lookup"><span data-stu-id="df165-136"><a href="windowsribbon-reference-properties-uipkey-largehighcontrastimage.md">UI_PKEY_LargeHighContrastImage</a></span></span></td>
<td><span data-ttu-id="df165-137">Peut uniquement être mis à jour par le biais d’une invalidation.</span><span class="sxs-lookup"><span data-stu-id="df165-137">Can only be updated through invalidation.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="df165-138"><a href="windowsribbon-reference-properties-uipkey-largeimage.md">UI_PKEY_LargeImage</a></span><span class="sxs-lookup"><span data-stu-id="df165-138"><a href="windowsribbon-reference-properties-uipkey-largeimage.md">UI_PKEY_LargeImage</a></span></span></td>
<td><span data-ttu-id="df165-139">Peut uniquement être mis à jour par le biais d’une invalidation.</span><span class="sxs-lookup"><span data-stu-id="df165-139">Can only be updated through invalidation.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="df165-140"><a href="windowsribbon-reference-properties-uipkey-selecteditem.md">UI_PKEY_SelectedItem</a></span><span class="sxs-lookup"><span data-stu-id="df165-140"><a href="windowsribbon-reference-properties-uipkey-selecteditem.md">UI_PKEY_SelectedItem</a></span></span></td>
<td><span data-ttu-id="df165-141">Prend en charge <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework :: GetUICommandProperty</strong></a> et <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework :: SetUICommandProperty</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="df165-141">Supports <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> and <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="df165-142"><a href="windowsribbon-reference-properties-uipkey-smallhighcontrastimage.md">UI_PKEY_SmallHighContrastImage</a></span><span class="sxs-lookup"><span data-stu-id="df165-142"><a href="windowsribbon-reference-properties-uipkey-smallhighcontrastimage.md">UI_PKEY_SmallHighContrastImage</a></span></span></td>
<td><span data-ttu-id="df165-143">Peut uniquement être mis à jour par le biais d’une invalidation.</span><span class="sxs-lookup"><span data-stu-id="df165-143">Can only be updated through invalidation.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="df165-144"><a href="windowsribbon-reference-properties-uipkey-smallimage.md">UI_PKEY_SmallImage</a></span><span class="sxs-lookup"><span data-stu-id="df165-144"><a href="windowsribbon-reference-properties-uipkey-smallimage.md">UI_PKEY_SmallImage</a></span></span></td>
<td><span data-ttu-id="df165-145">Peut uniquement être mis à jour par le biais d’une invalidation.</span><span class="sxs-lookup"><span data-stu-id="df165-145">Can only be updated through invalidation.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="df165-146"><a href="windowsribbon-reference-properties-uipkey-stringvalue.md">UI_PKEY_StringValue</a></span><span class="sxs-lookup"><span data-stu-id="df165-146"><a href="windowsribbon-reference-properties-uipkey-stringvalue.md">UI_PKEY_StringValue</a></span></span></td>
<td><span data-ttu-id="df165-147">Prend en charge <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework :: GetUICommandProperty</strong></a> et <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework :: SetUICommandProperty</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="df165-147">Supports <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> and <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="df165-148">Si la commande associée au contrôle est invalidée via un appel à <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand"><strong>IUIFramework :: InvalidateUICommand</strong></a>, le Framework interroge cette propriété lorsque <code>UI_INVALIDATIONS_VALUE</code> est passé comme valeur d' <em>indicateurs</em>.</span><span class="sxs-lookup"><span data-stu-id="df165-148">If the Command associated with the control is invalidated through a call to <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand"><strong>IUIFramework::InvalidateUICommand</strong></a>, the framework queries this property when <code>UI_INVALIDATIONS_VALUE</code> is passed as the value of <em>flags</em>.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="df165-149"><a href="windowsribbon-reference-properties-uipkey-tooltipdescription.md">UI_PKEY_TooltipDescription</a></span><span class="sxs-lookup"><span data-stu-id="df165-149"><a href="windowsribbon-reference-properties-uipkey-tooltipdescription.md">UI_PKEY_TooltipDescription</a></span></span></td>
<td><span data-ttu-id="df165-150">Peut uniquement être mis à jour par le biais d’une invalidation.</span><span class="sxs-lookup"><span data-stu-id="df165-150">Can only be updated through invalidation.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="df165-151"><a href="windowsribbon-reference-properties-uipkey-tooltiptitle.md">UI_PKEY_TooltipTitle</a></span><span class="sxs-lookup"><span data-stu-id="df165-151"><a href="windowsribbon-reference-properties-uipkey-tooltiptitle.md">UI_PKEY_TooltipTitle</a></span></span></td>
<td><span data-ttu-id="df165-152">Peut uniquement être mis à jour par le biais d’une invalidation.</span><span class="sxs-lookup"><span data-stu-id="df165-152">Can only be updated through invalidation.</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="df165-153">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="df165-153">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="df165-154">Bibliothèque de contrôles de l’infrastructure du ruban Windows</span><span class="sxs-lookup"><span data-stu-id="df165-154">Windows Ribbon Framework Control Library</span></span>](windowsribbon-controls-entry.md)
</dt> <dt>

[<span data-ttu-id="df165-155">**ComboBox, élément de balisage**</span><span class="sxs-lookup"><span data-stu-id="df165-155">**ComboBox markup element**</span></span>](windowsribbon-element-combobox.md)
</dt> <dt>

[<span data-ttu-id="df165-156">Utilisation des galeries</span><span class="sxs-lookup"><span data-stu-id="df165-156">Working with Galleries</span></span>](ribbon-controls-galleries.md)
</dt> <dt>

[<span data-ttu-id="df165-157">Exemple de Galerie</span><span class="sxs-lookup"><span data-stu-id="df165-157">Gallery Sample</span></span>](windowsribbon-gallerysample.md)
</dt> </dl>

