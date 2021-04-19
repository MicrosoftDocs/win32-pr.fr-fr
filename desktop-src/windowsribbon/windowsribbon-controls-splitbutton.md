---
title: Bouton partagé
description: Le bouton partagé est un contrôle composite avec lequel l’utilisateur peut sélectionner une valeur par défaut liée à un bouton principal, ou sélectionner dans une liste de valeurs s’excluant mutuellement dans une liste déroulante liée à un bouton secondaire.
ms.assetid: 0939b3be-fa88-4864-8096-a664ab2e97b5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b78aa261eebb24404eeaf8b3fdad7f630331f58
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/08/2020
ms.locfileid: "106512760"
---
# <a name="split-button"></a><span data-ttu-id="10f47-103">Bouton partagé</span><span class="sxs-lookup"><span data-stu-id="10f47-103">Split Button</span></span>

<span data-ttu-id="10f47-104">Le bouton partagé est un contrôle composite avec lequel l’utilisateur peut sélectionner une valeur par défaut liée à un bouton principal, ou sélectionner dans une liste de valeurs s’excluant mutuellement dans une liste déroulante liée à un bouton secondaire.</span><span class="sxs-lookup"><span data-stu-id="10f47-104">The Split Button is a composite control with which the user can select a default value bound to a primary button, or select from a list of mutually exclusive values displayed in a drop-down list bound to a secondary button.</span></span>

-   [<span data-ttu-id="10f47-105">Introduction</span><span class="sxs-lookup"><span data-stu-id="10f47-105">Introduction</span></span>](#introduction)
-   [<span data-ttu-id="10f47-106">Propriétés du bouton partagé</span><span class="sxs-lookup"><span data-stu-id="10f47-106">Split Button Properties</span></span>](#split-button-properties)
-   [<span data-ttu-id="10f47-107">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="10f47-107">Related topics</span></span>](#related-topics)

## <a name="introduction"></a><span data-ttu-id="10f47-108">Introduction</span><span class="sxs-lookup"><span data-stu-id="10f47-108">Introduction</span></span>

<span data-ttu-id="10f47-109">Ce contrôle est utile pour exposer des éléments étroitement liés dans les cas où une valeur par défaut évidente est disponible et où les éléments individuels peuvent être représentés par une image, du texte, ou les deux.</span><span class="sxs-lookup"><span data-stu-id="10f47-109">This control is useful for exposing closely related items in cases where an obvious default is available and where the individual items can be represented by an image, text, or both.</span></span>

<span data-ttu-id="10f47-110">La capture d’écran suivante illustre le bouton partagé du ruban.</span><span class="sxs-lookup"><span data-stu-id="10f47-110">The following screen shot illustrates the Ribbon Split Button.</span></span>

![capture d’écran d’un contrôle SplitButton dans un exemple de ruban.](images/controls/splitbutton.png)

## <a name="split-button-properties"></a><span data-ttu-id="10f47-112">Propriétés du bouton partagé</span><span class="sxs-lookup"><span data-stu-id="10f47-112">Split Button Properties</span></span>

<span data-ttu-id="10f47-113">L’infrastructure du ruban définit une collection de [clés de propriété](windowsribbon-reference-properties.md) pour le contrôle bouton partagé.</span><span class="sxs-lookup"><span data-stu-id="10f47-113">The Ribbon framework defines a collection of [property keys](windowsribbon-reference-properties.md) for the Split Button control.</span></span>

<span data-ttu-id="10f47-114">En règle générale, une propriété de bouton partagé est mise à jour dans l’interface utilisateur du ruban en invalidant la commande associée au contrôle via un appel à la méthode [**IUIFramework :: InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) .</span><span class="sxs-lookup"><span data-stu-id="10f47-114">Typically, a Split Button property is updated in the ribbon UI by invalidating the Command associated with the control through a call to the [**IUIFramework::InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) method.</span></span> <span data-ttu-id="10f47-115">L’événement d’invalidation est géré, et les mises à jour de la propriété sont définies par la méthode de rappel [**IUICommandHandler :: UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) .</span><span class="sxs-lookup"><span data-stu-id="10f47-115">The invalidation event is handled, and the property updates defined, by the [**IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) callback method.</span></span>

<span data-ttu-id="10f47-116">La méthode de rappel [**IUICommandHandler :: UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) n’est pas exécutée et l’application a interrogé une valeur de propriété mise à jour, jusqu’à ce que la propriété soit requise par le Framework.</span><span class="sxs-lookup"><span data-stu-id="10f47-116">The [**IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) callback method is not executed, and the application queried for an updated property value, until the property is required by the framework.</span></span> <span data-ttu-id="10f47-117">Par exemple, lorsqu’un onglet est activé et qu’un contrôle est affiché dans l’interface ruban, ou lorsqu’une info-bulle est affichée.</span><span class="sxs-lookup"><span data-stu-id="10f47-117">For example, when a tab is activated and a control revealed in the ribbon UI, or when a tooltip is displayed.</span></span>

> [!Note]  
> <span data-ttu-id="10f47-118">Dans certains cas, une propriété peut être récupérée par le biais de la méthode [**IUIFramework :: GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) et définie avec la méthode [**IUIFramework :: SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) .</span><span class="sxs-lookup"><span data-stu-id="10f47-118">In some cases, a property can be retrieved through the [**IUIFramework::GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) method and set with the [**IUIFramework::SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) method.</span></span>

 

<span data-ttu-id="10f47-119">Le tableau suivant répertorie les clés de propriété associées au contrôle bouton partagé.</span><span class="sxs-lookup"><span data-stu-id="10f47-119">The following table lists the property keys that are associated with the Split Button control.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="10f47-120">Clé de propriété</span><span class="sxs-lookup"><span data-stu-id="10f47-120">Property Key</span></span></th>
<th><span data-ttu-id="10f47-121">Notes</span><span class="sxs-lookup"><span data-stu-id="10f47-121">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="10f47-122"><a href="windowsribbon-reference-properties-uipkey-enabled.md">UI_PKEY_Enabled</a></span><span class="sxs-lookup"><span data-stu-id="10f47-122"><a href="windowsribbon-reference-properties-uipkey-enabled.md">UI_PKEY_Enabled</a></span></span></td>
<td><span data-ttu-id="10f47-123">Prend en charge <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework :: GetUICommandProperty</strong></a> et <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework :: SetUICommandProperty</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="10f47-123">Supports <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> and <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>.</span></span><br/> <span data-ttu-id="10f47-124">Si tous les éléments enfants sont désactivés, l’infrastructure définit <a href="windowsribbon-reference-properties-uipkey-enabled.md">UI_PKEY_Enabled</a> sur false (0).</span><span class="sxs-lookup"><span data-stu-id="10f47-124">If all child items are disabled, the framework sets <a href="windowsribbon-reference-properties-uipkey-enabled.md">UI_PKEY_Enabled</a> to false (0).</span></span> <span data-ttu-id="10f47-125">Dans le cas contraire, si un ou plusieurs éléments enfants sont activés, UI_PKEY_Enabled a la valeur true (-1).</span><span class="sxs-lookup"><span data-stu-id="10f47-125">Otherwise, if one or more child items are enabled, UI_PKEY_Enabled is set to true (-1).</span></span>
<blockquote>
[!Important]<br />
<span data-ttu-id="10f47-126">La propriété <a href="windowsribbon-reference-properties-uipkey-enabled.md">UI_PKEY_Enabled</a> du contrôle de bouton partagé doit être invalidée après l’activation ou la désactivation d’un ou plusieurs éléments enfants.</span><span class="sxs-lookup"><span data-stu-id="10f47-126">The <a href="windowsribbon-reference-properties-uipkey-enabled.md">UI_PKEY_Enabled</a> property for the Split Button control should be invalidated after one or more child items are enabled or disabled.</span></span> <span data-ttu-id="10f47-127">Cela garantit que l’infrastructure interroge la valeur de propriété mise à jour et actualise l’état du contrôle bouton partagé dans l’interface utilisateur du ruban.</span><span class="sxs-lookup"><span data-stu-id="10f47-127">This ensures that the framework queries the updated property value and refreshes the state of the Split Button control in the ribbon UI.</span></span>
</blockquote>
<br/> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="10f47-128"><a href="windowsribbon-reference-properties-uipkey-keytip.md">UI_PKEY_Keytip</a></span><span class="sxs-lookup"><span data-stu-id="10f47-128"><a href="windowsribbon-reference-properties-uipkey-keytip.md">UI_PKEY_Keytip</a></span></span></td>
<td><span data-ttu-id="10f47-129">Peut uniquement être mis à jour par le biais d’une invalidation.</span><span class="sxs-lookup"><span data-stu-id="10f47-129">Can only be updated through invalidation.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="10f47-130"><a href="windowsribbon-reference-properties-uipkey-tooltipdescription.md">UI_PKEY_TooltipDescription</a></span><span class="sxs-lookup"><span data-stu-id="10f47-130"><a href="windowsribbon-reference-properties-uipkey-tooltipdescription.md">UI_PKEY_TooltipDescription</a></span></span></td>
<td><span data-ttu-id="10f47-131">Peut uniquement être mis à jour par le biais d’une invalidation.</span><span class="sxs-lookup"><span data-stu-id="10f47-131">Can only be updated through invalidation.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="10f47-132"><a href="windowsribbon-reference-properties-uipkey-tooltiptitle.md">UI_PKEY_TooltipTitle</a></span><span class="sxs-lookup"><span data-stu-id="10f47-132"><a href="windowsribbon-reference-properties-uipkey-tooltiptitle.md">UI_PKEY_TooltipTitle</a></span></span></td>
<td><span data-ttu-id="10f47-133">Peut uniquement être mis à jour par le biais d’une invalidation.</span><span class="sxs-lookup"><span data-stu-id="10f47-133">Can only be updated through invalidation.</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="10f47-134">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="10f47-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="10f47-135">Bibliothèque de contrôles de l’infrastructure du ruban Windows</span><span class="sxs-lookup"><span data-stu-id="10f47-135">Windows Ribbon Framework Control Library</span></span>](windowsribbon-controls-entry.md)
</dt> <dt>

[<span data-ttu-id="10f47-136">**Élément de balisage SplitButton**</span><span class="sxs-lookup"><span data-stu-id="10f47-136">**SplitButton markup element**</span></span>](windowsribbon-element-splitbutton.md)
</dt> </dl>