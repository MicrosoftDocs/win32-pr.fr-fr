---
title: Groupe d’onglets
description: Un groupe d’onglets est un contrôle contextuel qui est masqué ou affiché au moment de l’exécution, en fonction de l’état d’un document ou d’un espace de travail. Le groupe d’onglets contient un ensemble de contrôles d’onglet liés au contexte.
ms.assetid: 5b74ff46-2543-43f3-ab42-dab1bc67a75e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 253c803a07c0d27692442ddb7a291930a261a2ae
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104316008"
---
# <a name="tab-group"></a><span data-ttu-id="e83d9-104">Groupe d’onglets</span><span class="sxs-lookup"><span data-stu-id="e83d9-104">Tab Group</span></span>

<span data-ttu-id="e83d9-105">Un groupe d’onglets est un contrôle contextuel qui est masqué ou affiché au moment de l’exécution, en fonction de l’état d’un document ou d’un espace de travail.</span><span class="sxs-lookup"><span data-stu-id="e83d9-105">A Tab Group is a contextual control that is hidden or displayed at run time, based on a document or workspace state.</span></span> <span data-ttu-id="e83d9-106">Le groupe d’onglets contient un ensemble de contrôles d' [onglet](windowsribbon-controls-tab.md) liés au contexte.</span><span class="sxs-lookup"><span data-stu-id="e83d9-106">The Tab Group contains a set of context-related [Tab](windowsribbon-controls-tab.md) controls.</span></span>

-   [<span data-ttu-id="e83d9-107">Détails</span><span class="sxs-lookup"><span data-stu-id="e83d9-107">Details</span></span>](#details)
-   [<span data-ttu-id="e83d9-108">Propriétés du groupe d’onglets</span><span class="sxs-lookup"><span data-stu-id="e83d9-108">Tab Group Properties</span></span>](#tab-group-properties)
-   [<span data-ttu-id="e83d9-109">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="e83d9-109">Related topics</span></span>](#related-topics)

## <a name="details"></a><span data-ttu-id="e83d9-110">Détails</span><span class="sxs-lookup"><span data-stu-id="e83d9-110">Details</span></span>

<span data-ttu-id="e83d9-111">En règle générale, un groupe d’onglets s’affiche au cours d’États d’un document ou d’un espace de travail spécifique, par exemple lorsqu’un utilisateur sélectionne un type d’objet particulier.</span><span class="sxs-lookup"><span data-stu-id="e83d9-111">Typically, a Tab Group is displayed during specific document or workspace states, such as when a user selects a particular object type.</span></span> <span data-ttu-id="e83d9-112">Par exemple, la sélection d’une image contenue dans l’en-tête d’une table peut nécessiter l’affichage de différents onglets contextuels qui exposent les fonctionnalités de la table et de l’image.</span><span class="sxs-lookup"><span data-stu-id="e83d9-112">For example, the selection of an image contained in the header of a table might require various contextual tabs to be displayed that expose both table and image functionality.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="e83d9-113">Un groupe d’onglets ne prend pas en charge les [modes d’application](ribbon-applicationmodes.md).</span><span class="sxs-lookup"><span data-stu-id="e83d9-113">A Tab Group does not support [application modes](ribbon-applicationmodes.md).</span></span> <span data-ttu-id="e83d9-114">Toutefois, les contrôles d' [onglet](windowsribbon-controls-tab.md) individuels au sein d’un groupe d’onglets peuvent.</span><span class="sxs-lookup"><span data-stu-id="e83d9-114">However, the individual [Tab](windowsribbon-controls-tab.md) controls within a Tab Group may.</span></span>

 

<span data-ttu-id="e83d9-115">La capture d’écran suivante montre un [onglet](windowsribbon-controls-tab.md) contextuel de Windows 7 Paint.</span><span class="sxs-lookup"><span data-stu-id="e83d9-115">The following screen shot shows a contextual [Tab](windowsribbon-controls-tab.md) from Windows 7 Paint.</span></span>

![capture d’écran qui montre un contrôle d’onglet contextuel.](images/controls/contextualtab.png)

## <a name="tab-group-properties"></a><span data-ttu-id="e83d9-117">Propriétés du groupe d’onglets</span><span class="sxs-lookup"><span data-stu-id="e83d9-117">Tab Group Properties</span></span>

<span data-ttu-id="e83d9-118">L’infrastructure du ruban définit une collection de [clés de propriété](windowsribbon-reference-properties.md) pour le contrôle de groupe d’onglets.</span><span class="sxs-lookup"><span data-stu-id="e83d9-118">The Ribbon framework defines a collection of [property keys](windowsribbon-reference-properties.md) for the Tab Group control.</span></span>

<span data-ttu-id="e83d9-119">En règle générale, une propriété de groupe d’onglets est mise à jour dans l’interface ruban en invalidant la commande associée au contrôle via un appel à la méthode [**IUIFramework :: InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) .</span><span class="sxs-lookup"><span data-stu-id="e83d9-119">Typically, a Tab Group property is updated in the ribbon UI by invalidating the Command associated with the control through a call to the [**IUIFramework::InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) method.</span></span> <span data-ttu-id="e83d9-120">L’événement d’invalidation est géré, et les mises à jour de la propriété sont définies par la méthode de rappel [**IUICommandHandler :: UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) .</span><span class="sxs-lookup"><span data-stu-id="e83d9-120">The invalidation event is handled, and the property updates defined, by the [**IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) callback method.</span></span>

<span data-ttu-id="e83d9-121">La méthode de rappel [**IUICommandHandler :: UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) n’est pas exécutée et l’application a interrogé une valeur de propriété mise à jour, jusqu’à ce que la propriété soit requise par le Framework.</span><span class="sxs-lookup"><span data-stu-id="e83d9-121">The [**IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) callback method is not executed, and the application queried for an updated property value, until the property is required by the framework.</span></span> <span data-ttu-id="e83d9-122">Par exemple, lorsqu’un onglet est activé et qu’un contrôle est affiché dans l’interface ruban, ou lorsqu’une info-bulle est affichée.</span><span class="sxs-lookup"><span data-stu-id="e83d9-122">For example, when a tab is activated and a control revealed in the ribbon UI, or when a tooltip is displayed.</span></span>

> [!Note]  
> <span data-ttu-id="e83d9-123">Dans certains cas, une propriété peut être récupérée par le biais de la méthode [**IUIFramework :: GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) et définie avec la méthode [**IUIFramework :: SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) .</span><span class="sxs-lookup"><span data-stu-id="e83d9-123">In some cases, a property can be retrieved through the [**IUIFramework::GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) method and set with the [**IUIFramework::SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) method.</span></span>

 

<span data-ttu-id="e83d9-124">Le tableau suivant répertorie les clés de propriété associées au contrôle de groupe d’onglets.</span><span class="sxs-lookup"><span data-stu-id="e83d9-124">The following table lists the property keys that are associated with the Tab Group control.</span></span>



| <span data-ttu-id="e83d9-125">Clé de propriété</span><span class="sxs-lookup"><span data-stu-id="e83d9-125">Property Key</span></span>                                                                                     | <span data-ttu-id="e83d9-126">Notes</span><span class="sxs-lookup"><span data-stu-id="e83d9-126">Notes</span></span>                                                                                                                                                                                                                         |
|--------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e83d9-127">IU \_ \_ ContextAvailable</span><span class="sxs-lookup"><span data-stu-id="e83d9-127">UI\_PKEY\_ContextAvailable</span></span>](windowsribbon-reference-properties-uipkey-contextavailable.md)     | <span data-ttu-id="e83d9-128">Prend en charge [**IUIFramework :: GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) et [**IUIFramework :: SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty).</span><span class="sxs-lookup"><span data-stu-id="e83d9-128">Supports [**IUIFramework::GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) and [**IUIFramework::SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty).</span></span> |
| [<span data-ttu-id="e83d9-129">KeyTip de l’interface utilisateur \_ \_</span><span class="sxs-lookup"><span data-stu-id="e83d9-129">UI\_PKEY\_Keytip</span></span>](windowsribbon-reference-properties-uipkey-keytip.md)                         | <span data-ttu-id="e83d9-130">Peut uniquement être mis à jour par le biais d’une invalidation.</span><span class="sxs-lookup"><span data-stu-id="e83d9-130">Can only be updated through invalidation.</span></span>                                                                                                                                                                                     |
| [<span data-ttu-id="e83d9-131">\_Étiquette de nom de l’interface utilisateur \_</span><span class="sxs-lookup"><span data-stu-id="e83d9-131">UI\_PKEY\_Label</span></span>](windowsribbon-reference-properties-uipkey-label.md)                           | <span data-ttu-id="e83d9-132">Peut uniquement être mis à jour par le biais d’une invalidation.</span><span class="sxs-lookup"><span data-stu-id="e83d9-132">Can only be updated through invalidation.</span></span>                                                                                                                                                                                     |
| [<span data-ttu-id="e83d9-133">IU \_ \_ TooltipDescription</span><span class="sxs-lookup"><span data-stu-id="e83d9-133">UI\_PKEY\_TooltipDescription</span></span>](windowsribbon-reference-properties-uipkey-tooltipdescription.md) | <span data-ttu-id="e83d9-134">Peut uniquement être mis à jour par le biais d’une invalidation.</span><span class="sxs-lookup"><span data-stu-id="e83d9-134">Can only be updated through invalidation.</span></span>                                                                                                                                                                                     |
| [<span data-ttu-id="e83d9-135">IU \_ \_ TooltipTitle</span><span class="sxs-lookup"><span data-stu-id="e83d9-135">UI\_PKEY\_TooltipTitle</span></span>](windowsribbon-reference-properties-uipkey-tooltiptitle.md)             | <span data-ttu-id="e83d9-136">Peut uniquement être mis à jour par le biais d’une invalidation.</span><span class="sxs-lookup"><span data-stu-id="e83d9-136">Can only be updated through invalidation.</span></span>                                                                                                                                                                                     |



 

## <a name="related-topics"></a><span data-ttu-id="e83d9-137">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="e83d9-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e83d9-138">Bibliothèque de contrôles de l’infrastructure du ruban Windows</span><span class="sxs-lookup"><span data-stu-id="e83d9-138">Windows Ribbon Framework Control Library</span></span>](windowsribbon-controls-entry.md)
</dt> <dt>

[<span data-ttu-id="e83d9-139">**Élément de balisage TabGroup**</span><span class="sxs-lookup"><span data-stu-id="e83d9-139">**TabGroup markup element**</span></span>](windowsribbon-element-tabgroup.md)
</dt> </dl>

 

 