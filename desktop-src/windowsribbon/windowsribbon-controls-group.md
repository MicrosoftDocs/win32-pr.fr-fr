---
title: Groupe (infrastructure de ruban Windows)
description: Le groupe organise les commandes et les contrôles associés au sein d’un onglet.
ms.assetid: 5d098d3f-a4ee-4f76-8c81-832d0c49cb80
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 903bd422d11fea81ed03a48bf8e9437f9caab699
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104383756"
---
# <a name="group-windows-ribbon-framework"></a><span data-ttu-id="4b39d-103">Groupe (infrastructure de ruban Windows)</span><span class="sxs-lookup"><span data-stu-id="4b39d-103">Group (Windows Ribbon Framework)</span></span>

<span data-ttu-id="4b39d-104">Le groupe organise les commandes et les contrôles associés au sein d’un [onglet](windowsribbon-controls-tab.md).</span><span class="sxs-lookup"><span data-stu-id="4b39d-104">The Group organizes related Commands and controls within a [Tab](windowsribbon-controls-tab.md).</span></span>

-   [<span data-ttu-id="4b39d-105">Détails</span><span class="sxs-lookup"><span data-stu-id="4b39d-105">Details</span></span>](#details)
-   [<span data-ttu-id="4b39d-106">Propriétés de groupe</span><span class="sxs-lookup"><span data-stu-id="4b39d-106">Group Properties</span></span>](#group-properties)
-   [<span data-ttu-id="4b39d-107">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="4b39d-107">Related topics</span></span>](#related-topics)

## <a name="details"></a><span data-ttu-id="4b39d-108">Détails</span><span class="sxs-lookup"><span data-stu-id="4b39d-108">Details</span></span>

<span data-ttu-id="4b39d-109">La capture d’écran suivante illustre le contrôle du groupe de ruban.</span><span class="sxs-lookup"><span data-stu-id="4b39d-109">The following screen shot illustrates the Ribbon Group control.</span></span>

![capture d’écran avec légendes montrant un groupe.](images/controls/group.png)

## <a name="group-properties"></a><span data-ttu-id="4b39d-111">Propriétés de groupe</span><span class="sxs-lookup"><span data-stu-id="4b39d-111">Group Properties</span></span>

<span data-ttu-id="4b39d-112">L’infrastructure du ruban définit une collection de [clés de propriété](windowsribbon-reference-properties.md) pour le contrôle de groupe.</span><span class="sxs-lookup"><span data-stu-id="4b39d-112">The Ribbon framework defines a collection of [property keys](windowsribbon-reference-properties.md) for the Group control.</span></span>

<span data-ttu-id="4b39d-113">En règle générale, une propriété de groupe est mise à jour dans l’interface utilisateur du ruban en invalidant la commande associée au contrôle via un appel à la méthode [**IUIFramework :: InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) .</span><span class="sxs-lookup"><span data-stu-id="4b39d-113">Typically, a Group property is updated in the ribbon UI by invalidating the Command associated with the control through a call to the [**IUIFramework::InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) method.</span></span> <span data-ttu-id="4b39d-114">L’événement d’invalidation est géré, et les mises à jour de la propriété sont définies par la méthode de rappel [**IUICommandHandler :: UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) .</span><span class="sxs-lookup"><span data-stu-id="4b39d-114">The invalidation event is handled, and the property updates defined, by the [**IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) callback method.</span></span>

<span data-ttu-id="4b39d-115">La méthode de rappel [**IUICommandHandler :: UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) n’est pas exécutée et l’application a interrogé une valeur de propriété mise à jour, jusqu’à ce que la propriété soit requise par le Framework.</span><span class="sxs-lookup"><span data-stu-id="4b39d-115">The [**IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) callback method is not executed, and the application queried for an updated property value, until the property is required by the framework.</span></span> <span data-ttu-id="4b39d-116">Par exemple, lorsqu’un onglet est activé et qu’un contrôle est affiché dans l’interface ruban, ou lorsqu’une info-bulle est affichée.</span><span class="sxs-lookup"><span data-stu-id="4b39d-116">For example, when a tab is activated and a control revealed in the ribbon UI, or when a tooltip is displayed.</span></span>

> [!Note]  
> <span data-ttu-id="4b39d-117">Dans certains cas, une propriété peut être récupérée par le biais de la méthode [**IUIFramework :: GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) et définie avec la méthode [**IUIFramework :: SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) .</span><span class="sxs-lookup"><span data-stu-id="4b39d-117">In some cases, a property can be retrieved through the [**IUIFramework::GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) method and set with the [**IUIFramework::SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) method.</span></span>

 

<span data-ttu-id="4b39d-118">Le tableau suivant répertorie les clés de propriété associées au contrôle de groupe.</span><span class="sxs-lookup"><span data-stu-id="4b39d-118">The following table lists the property keys that are associated with the Group control.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="4b39d-119">Clé de propriété</span><span class="sxs-lookup"><span data-stu-id="4b39d-119">Property Key</span></span></th>
<th><span data-ttu-id="4b39d-120">Notes</span><span class="sxs-lookup"><span data-stu-id="4b39d-120">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="4b39d-121"><a href="windowsribbon-reference-properties-uipkey-keytip.md">UI_PKEY_Keytip</a></span><span class="sxs-lookup"><span data-stu-id="4b39d-121"><a href="windowsribbon-reference-properties-uipkey-keytip.md">UI_PKEY_Keytip</a></span></span></td>
<td><span data-ttu-id="4b39d-122">Peut uniquement être mis à jour par le biais d’une invalidation.</span><span class="sxs-lookup"><span data-stu-id="4b39d-122">Can only be updated through invalidation.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="4b39d-123">L’infrastructure requiert que la valeur de <a href="windowsribbon-reference-properties-uipkey-keytip.md">UI_PKEY_Keytip</a> pour un contrôle de groupe commence par la lettre Z majuscule. Si la valeur fournie par l’application dans la méthode de rappel <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty"><strong>IUICommandHandler :: UpdateProperty</strong></a> ne commence pas par la lettre Z, cette valeur est ignorée et une valeur est générée par l’infrastructure à la place.</span><span class="sxs-lookup"><span data-stu-id="4b39d-123">The framework requires that the value of <a href="windowsribbon-reference-properties-uipkey-keytip.md">UI_PKEY_Keytip</a> for a Group control begins with the upper-case letter Z. If the value supplied by the application in the <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty"><strong>IUICommandHandler::UpdateProperty</strong></a> callback method does not begin with the letter Z, this value is ignored and a value is generated by the framework instead.</span></span> <span data-ttu-id="4b39d-124">La valeur du Framework est la lettre Z suivie d’une valeur numérique commençant à 1 et qui s’incrémente séquentiellement, selon les besoins, pour les contrôles de groupe suivants (Z1, Z2,..., ZX).</span><span class="sxs-lookup"><span data-stu-id="4b39d-124">The framework value is the letter Z followed by a numeric value starting at 1 and increasing sequentially, as required, for subsequent Group controls (Z1, Z2, ..., Zx).</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4b39d-125"><a href="windowsribbon-reference-properties-uipkey-label.md">UI_PKEY_Label</a></span><span class="sxs-lookup"><span data-stu-id="4b39d-125"><a href="windowsribbon-reference-properties-uipkey-label.md">UI_PKEY_Label</a></span></span></td>
<td><span data-ttu-id="4b39d-126">Peut uniquement être mis à jour par le biais d’une invalidation.</span><span class="sxs-lookup"><span data-stu-id="4b39d-126">Can only be updated through invalidation.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4b39d-127"><a href="windowsribbon-reference-properties-uipkey-largehighcontrastimage.md">UI_PKEY_LargeHighContrastImage</a></span><span class="sxs-lookup"><span data-stu-id="4b39d-127"><a href="windowsribbon-reference-properties-uipkey-largehighcontrastimage.md">UI_PKEY_LargeHighContrastImage</a></span></span></td>
<td><span data-ttu-id="4b39d-128">Peut uniquement être mis à jour par le biais d’une invalidation.</span><span class="sxs-lookup"><span data-stu-id="4b39d-128">Can only be updated through invalidation.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4b39d-129"><a href="windowsribbon-reference-properties-uipkey-largeimage.md">UI_PKEY_LargeImage</a></span><span class="sxs-lookup"><span data-stu-id="4b39d-129"><a href="windowsribbon-reference-properties-uipkey-largeimage.md">UI_PKEY_LargeImage</a></span></span></td>
<td><span data-ttu-id="4b39d-130">Peut uniquement être mis à jour par le biais d’une invalidation.</span><span class="sxs-lookup"><span data-stu-id="4b39d-130">Can only be updated through invalidation.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4b39d-131"><a href="windowsribbon-reference-properties-uipkey-smallhighcontrastimage.md">UI_PKEY_SmallHighContrastImage</a></span><span class="sxs-lookup"><span data-stu-id="4b39d-131"><a href="windowsribbon-reference-properties-uipkey-smallhighcontrastimage.md">UI_PKEY_SmallHighContrastImage</a></span></span></td>
<td><span data-ttu-id="4b39d-132">Peut uniquement être mis à jour par le biais d’une invalidation.</span><span class="sxs-lookup"><span data-stu-id="4b39d-132">Can only be updated through invalidation.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4b39d-133"><a href="windowsribbon-reference-properties-uipkey-smallimage.md">UI_PKEY_SmallImage</a></span><span class="sxs-lookup"><span data-stu-id="4b39d-133"><a href="windowsribbon-reference-properties-uipkey-smallimage.md">UI_PKEY_SmallImage</a></span></span></td>
<td><span data-ttu-id="4b39d-134">Peut uniquement être mis à jour par le biais d’une invalidation.</span><span class="sxs-lookup"><span data-stu-id="4b39d-134">Can only be updated through invalidation.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4b39d-135"><a href="windowsribbon-reference-properties-uipkey-tooltipdescription.md">UI_PKEY_TooltipDescription</a></span><span class="sxs-lookup"><span data-stu-id="4b39d-135"><a href="windowsribbon-reference-properties-uipkey-tooltipdescription.md">UI_PKEY_TooltipDescription</a></span></span></td>
<td><span data-ttu-id="4b39d-136">Peut uniquement être mis à jour par le biais d’une invalidation.</span><span class="sxs-lookup"><span data-stu-id="4b39d-136">Can only be updated through invalidation.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4b39d-137"><a href="windowsribbon-reference-properties-uipkey-tooltiptitle.md">UI_PKEY_TooltipTitle</a></span><span class="sxs-lookup"><span data-stu-id="4b39d-137"><a href="windowsribbon-reference-properties-uipkey-tooltiptitle.md">UI_PKEY_TooltipTitle</a></span></span></td>
<td><span data-ttu-id="4b39d-138">Peut uniquement être mis à jour par le biais d’une invalidation.</span><span class="sxs-lookup"><span data-stu-id="4b39d-138">Can only be updated through invalidation.</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="4b39d-139">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="4b39d-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4b39d-140">Bibliothèque de contrôles de l’infrastructure du ruban Windows</span><span class="sxs-lookup"><span data-stu-id="4b39d-140">Windows Ribbon Framework Control Library</span></span>](windowsribbon-controls-entry.md)
</dt> <dt>

[<span data-ttu-id="4b39d-141">**élément Group**</span><span class="sxs-lookup"><span data-stu-id="4b39d-141">**Group element**</span></span>](windowsribbon-element-group.md)
</dt> </dl>

