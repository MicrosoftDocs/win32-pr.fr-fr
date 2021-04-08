---
title: Button (infrastructure de ruban Windows)
description: Le bouton est un contrôle sur lequel l’utilisateur peut cliquer pour fournir une entrée à une application.
ms.assetid: 6d4aa571-dbea-4139-a6b7-45a85595dd04
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1514a1ae66e383d18f81d1ca0ee1a5a8e453335d
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104102645"
---
# <a name="button-windows-ribbon-framework"></a><span data-ttu-id="0574e-103">Button (infrastructure de ruban Windows)</span><span class="sxs-lookup"><span data-stu-id="0574e-103">Button (Windows Ribbon Framework)</span></span>

<span data-ttu-id="0574e-104">Le bouton est un contrôle sur lequel l’utilisateur peut cliquer pour fournir une entrée à une application.</span><span class="sxs-lookup"><span data-stu-id="0574e-104">The Button is a control the user can click to provide input to an application.</span></span>

-   [<span data-ttu-id="0574e-105">Introduction</span><span class="sxs-lookup"><span data-stu-id="0574e-105">Introduction</span></span>](#introduction)
-   [<span data-ttu-id="0574e-106">Propriétés du bouton</span><span class="sxs-lookup"><span data-stu-id="0574e-106">Button Properties</span></span>](#button-properties)
-   [<span data-ttu-id="0574e-107">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="0574e-107">Related topics</span></span>](#related-topics)

## <a name="introduction"></a><span data-ttu-id="0574e-108">Introduction</span><span class="sxs-lookup"><span data-stu-id="0574e-108">Introduction</span></span>

<span data-ttu-id="0574e-109">La capture d’écran suivante contient trois exemples de l’élément Button du ruban.</span><span class="sxs-lookup"><span data-stu-id="0574e-109">The following screen shot contains three examples of the Ribbon Button element.</span></span>

![capture d’écran des contrôles Button dans le ruban de Microsoft WordPad.](images/controls/button.png)

## <a name="button-properties"></a><span data-ttu-id="0574e-111">Propriétés du bouton</span><span class="sxs-lookup"><span data-stu-id="0574e-111">Button Properties</span></span>

<span data-ttu-id="0574e-112">L’infrastructure du ruban définit une collection de [clés de propriété](windowsribbon-reference-properties.md) pour le contrôle bouton.</span><span class="sxs-lookup"><span data-stu-id="0574e-112">The Ribbon framework defines a collection of [property keys](windowsribbon-reference-properties.md) for the Button control.</span></span>

<span data-ttu-id="0574e-113">En général, une propriété de bouton est mise à jour dans l’interface utilisateur du ruban en invalidant la commande associée au contrôle via un appel à la méthode [**IUIFramework :: InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) .</span><span class="sxs-lookup"><span data-stu-id="0574e-113">Typically, a Button property is updated in the ribbon UI by invalidating the Command associated with the control through a call to the [**IUIFramework::InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) method.</span></span> <span data-ttu-id="0574e-114">L’événement d’invalidation est géré, et les mises à jour de la propriété sont définies par la méthode de rappel [**IUICommandHandler :: UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) .</span><span class="sxs-lookup"><span data-stu-id="0574e-114">The invalidation event is handled, and the property updates defined, by the [**IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) callback method.</span></span>

<span data-ttu-id="0574e-115">La méthode de rappel [**IUICommandHandler :: UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) n’est pas exécutée et l’application a interrogé une valeur de propriété mise à jour, jusqu’à ce que la propriété soit requise par le Framework.</span><span class="sxs-lookup"><span data-stu-id="0574e-115">The [**IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) callback method is not executed, and the application queried for an updated property value, until the property is required by the framework.</span></span> <span data-ttu-id="0574e-116">Par exemple, lorsqu’un onglet est activé et qu’un contrôle est affiché dans l’interface ruban, ou lorsqu’une info-bulle est affichée.</span><span class="sxs-lookup"><span data-stu-id="0574e-116">For example, when a tab is activated and a control revealed in the ribbon UI, or when a tooltip is displayed.</span></span>

> [!Note]  
> <span data-ttu-id="0574e-117">Dans certains cas, une propriété peut être récupérée par le biais de la méthode [**IUIFramework :: GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) et définie avec la méthode [**IUIFramework :: SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) .</span><span class="sxs-lookup"><span data-stu-id="0574e-117">In some cases, a property can be retrieved through the [**IUIFramework::GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) method and set with the [**IUIFramework::SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) method.</span></span>

 

<span data-ttu-id="0574e-118">Le tableau suivant répertorie les clés de propriété associées au contrôle Button.</span><span class="sxs-lookup"><span data-stu-id="0574e-118">The following table lists the property keys that are associated with the Button control.</span></span>



| <span data-ttu-id="0574e-119">Clé de propriété</span><span class="sxs-lookup"><span data-stu-id="0574e-119">Property Key</span></span>                                                                                             | <span data-ttu-id="0574e-120">Notes</span><span class="sxs-lookup"><span data-stu-id="0574e-120">Notes</span></span>                                                                                                                                                                                                                         |
|----------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0574e-121">IU-au-dessus \_ \_ activé</span><span class="sxs-lookup"><span data-stu-id="0574e-121">UI\_PKEY\_Enabled</span></span>](windowsribbon-reference-properties-uipkey-enabled.md)                               | <span data-ttu-id="0574e-122">Prend en charge [**IUIFramework :: GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) et [**IUIFramework :: SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty).</span><span class="sxs-lookup"><span data-stu-id="0574e-122">Supports [**IUIFramework::GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) and [**IUIFramework::SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty).</span></span> |
| [<span data-ttu-id="0574e-123">KeyTip de l’interface utilisateur \_ \_</span><span class="sxs-lookup"><span data-stu-id="0574e-123">UI\_PKEY\_Keytip</span></span>](windowsribbon-reference-properties-uipkey-keytip.md)                                 | <span data-ttu-id="0574e-124">Peut uniquement être mis à jour par le biais d’une invalidation.</span><span class="sxs-lookup"><span data-stu-id="0574e-124">Can only be updated through invalidation.</span></span>                                                                                                                                                                                     |
| [<span data-ttu-id="0574e-125">\_Étiquette de nom de l’interface utilisateur \_</span><span class="sxs-lookup"><span data-stu-id="0574e-125">UI\_PKEY\_Label</span></span>](windowsribbon-reference-properties-uipkey-label.md)                                   | <span data-ttu-id="0574e-126">Peut uniquement être mis à jour par le biais d’une invalidation.</span><span class="sxs-lookup"><span data-stu-id="0574e-126">Can only be updated through invalidation.</span></span>                                                                                                                                                                                     |
| [<span data-ttu-id="0574e-127">IU \_ \_ LabelDescription</span><span class="sxs-lookup"><span data-stu-id="0574e-127">UI\_PKEY\_LabelDescription</span></span>](windowsribbon-reference-properties-uipkey-labeldescription.md)             | <span data-ttu-id="0574e-128">Peut uniquement être mis à jour par le biais d’une invalidation.</span><span class="sxs-lookup"><span data-stu-id="0574e-128">Can only be updated through invalidation.</span></span>                                                                                                                                                                                     |
| [<span data-ttu-id="0574e-129">IU \_ \_ LargeHighContrastImage</span><span class="sxs-lookup"><span data-stu-id="0574e-129">UI\_PKEY\_LargeHighContrastImage</span></span>](windowsribbon-reference-properties-uipkey-largehighcontrastimage.md) | <span data-ttu-id="0574e-130">Peut uniquement être mis à jour par le biais d’une invalidation.</span><span class="sxs-lookup"><span data-stu-id="0574e-130">Can only be updated through invalidation.</span></span>                                                                                                                                                                                     |
| [<span data-ttu-id="0574e-131">IU \_ \_ LARGEIMAGE</span><span class="sxs-lookup"><span data-stu-id="0574e-131">UI\_PKEY\_LargeImage</span></span>](windowsribbon-reference-properties-uipkey-largeimage.md)                         | <span data-ttu-id="0574e-132">Peut uniquement être mis à jour par le biais d’une invalidation.</span><span class="sxs-lookup"><span data-stu-id="0574e-132">Can only be updated through invalidation.</span></span>                                                                                                                                                                                     |
| [<span data-ttu-id="0574e-133">IU \_ \_ SmallHighContrastImage</span><span class="sxs-lookup"><span data-stu-id="0574e-133">UI\_PKEY\_SmallHighContrastImage</span></span>](windowsribbon-reference-properties-uipkey-smallhighcontrastimage.md) | <span data-ttu-id="0574e-134">Peut uniquement être mis à jour par le biais d’une invalidation.</span><span class="sxs-lookup"><span data-stu-id="0574e-134">Can only be updated through invalidation.</span></span>                                                                                                                                                                                     |
| [<span data-ttu-id="0574e-135">IU \_ \_ SmallImage</span><span class="sxs-lookup"><span data-stu-id="0574e-135">UI\_PKEY\_SmallImage</span></span>](windowsribbon-reference-properties-uipkey-smallimage.md)                         | <span data-ttu-id="0574e-136">Peut uniquement être mis à jour par le biais d’une invalidation.</span><span class="sxs-lookup"><span data-stu-id="0574e-136">Can only be updated through invalidation.</span></span>                                                                                                                                                                                     |
| [<span data-ttu-id="0574e-137">IU \_ \_ TooltipDescription</span><span class="sxs-lookup"><span data-stu-id="0574e-137">UI\_PKEY\_TooltipDescription</span></span>](windowsribbon-reference-properties-uipkey-tooltipdescription.md)         | <span data-ttu-id="0574e-138">Peut uniquement être mis à jour par le biais d’une invalidation.</span><span class="sxs-lookup"><span data-stu-id="0574e-138">Can only be updated through invalidation.</span></span>                                                                                                                                                                                     |
| [<span data-ttu-id="0574e-139">IU \_ \_ TooltipTitle</span><span class="sxs-lookup"><span data-stu-id="0574e-139">UI\_PKEY\_TooltipTitle</span></span>](windowsribbon-reference-properties-uipkey-tooltiptitle.md)                     | <span data-ttu-id="0574e-140">Peut uniquement être mis à jour par le biais d’une invalidation.</span><span class="sxs-lookup"><span data-stu-id="0574e-140">Can only be updated through invalidation.</span></span>                                                                                                                                                                                     |



 

## <a name="related-topics"></a><span data-ttu-id="0574e-141">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="0574e-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0574e-142">Bibliothèque de contrôles de l’infrastructure du ruban Windows</span><span class="sxs-lookup"><span data-stu-id="0574e-142">Windows Ribbon Framework Control Library</span></span>](windowsribbon-controls-entry.md)
</dt> <dt>

[<span data-ttu-id="0574e-143">**Élément de balisage de bouton**</span><span class="sxs-lookup"><span data-stu-id="0574e-143">**Button markup element**</span></span>](windowsribbon-element-button.md)
</dt> </dl>

 

 
