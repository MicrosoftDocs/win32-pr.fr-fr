---
title: Tab (infrastructure du ruban Windows)
description: Un onglet contient des groupes de contrôles connexes.
ms.assetid: 7315ca96-73c8-4ea1-bce0-172ebc4dd43a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b760bfc0c588c71ee9dbffa32b6cebc12a39fea7
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104317077"
---
# <a name="tab-windows-ribbon-framework"></a><span data-ttu-id="5dabe-103">Tab (infrastructure du ruban Windows)</span><span class="sxs-lookup"><span data-stu-id="5dabe-103">Tab (Windows Ribbon Framework)</span></span>

<span data-ttu-id="5dabe-104">Un onglet contient des [groupes](windowsribbon-controls-group.md) de contrôles connexes.</span><span class="sxs-lookup"><span data-stu-id="5dabe-104">A Tab contains [groups](windowsribbon-controls-group.md) of related controls.</span></span>

-   [<span data-ttu-id="5dabe-105">Détails</span><span class="sxs-lookup"><span data-stu-id="5dabe-105">Details</span></span>](#details)
-   [<span data-ttu-id="5dabe-106">Propriétés de l’onglet</span><span class="sxs-lookup"><span data-stu-id="5dabe-106">Tab Properties</span></span>](#tab-properties)
-   [<span data-ttu-id="5dabe-107">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="5dabe-107">Related topics</span></span>](#related-topics)

## <a name="details"></a><span data-ttu-id="5dabe-108">Détails</span><span class="sxs-lookup"><span data-stu-id="5dabe-108">Details</span></span>

<span data-ttu-id="5dabe-109">Il existe trois types d’onglets dans l’infrastructure du ruban.</span><span class="sxs-lookup"><span data-stu-id="5dabe-109">There are three types of Tab in the Ribbon framework.</span></span>



| <span data-ttu-id="5dabe-110">Type</span><span class="sxs-lookup"><span data-stu-id="5dabe-110">Type</span></span>               | <span data-ttu-id="5dabe-111">Description</span><span class="sxs-lookup"><span data-stu-id="5dabe-111">Description</span></span>                                                                                                                                                                                                                                                                         |
|--------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5dabe-112">**Onglet principal**</span><span class="sxs-lookup"><span data-stu-id="5dabe-112">**Core tab**</span></span>       | <span data-ttu-id="5dabe-113">Onglets principaux qui organisent les fonctions par défaut de l’application.</span><span class="sxs-lookup"><span data-stu-id="5dabe-113">Core tabs that organize the default functions of the application.</span></span>                                                                                                                                                                                                                   |
| <span data-ttu-id="5dabe-114">**Onglet contextuel**</span><span class="sxs-lookup"><span data-stu-id="5dabe-114">**Contextual tab**</span></span> | <span data-ttu-id="5dabe-115">Onglets qui s’affichent au cours de l’état d’un document ou d’un espace de travail spécifique.</span><span class="sxs-lookup"><span data-stu-id="5dabe-115">Tabs that are displayed during specific document or workspace states.</span></span> <span data-ttu-id="5dabe-116">Par exemple, si un utilisateur sélectionne un type d’objet particulier, tel qu’une image contenue dans l’en-tête d’une table, différents onglets contextuels peuvent s’afficher et exposer les fonctionnalités de la table et de l’image.</span><span class="sxs-lookup"><span data-stu-id="5dabe-116">For example, if a user selects a particular object type, such as an image contained in the header of a table, then various contextual tabs might be displayed that expose both table and image functionality.</span></span> |
| <span data-ttu-id="5dabe-117">**Onglet modal**</span><span class="sxs-lookup"><span data-stu-id="5dabe-117">**Modal tab**</span></span>      | <span data-ttu-id="5dabe-118">Les onglets principaux qui s’affichent pendant un [mode d’application](ribbon-applicationmodes.md)de document ou d’espace de travail spécifique, tels que l’aperçu avant impression.</span><span class="sxs-lookup"><span data-stu-id="5dabe-118">Core tabs that are displayed during a specific document or workspace [application mode](ribbon-applicationmodes.md), such as print preview.</span></span>                                                                                                                                        |



 

<span data-ttu-id="5dabe-119">La capture d’écran suivante montre un onglet principal de Windows 7 Paint.</span><span class="sxs-lookup"><span data-stu-id="5dabe-119">The following screen shot shows a core Tab from Windows 7 Paint.</span></span>

![capture d’écran qui montre un contrôle d’onglet principal.](images/controls/coretab.png)

## <a name="tab-properties"></a><span data-ttu-id="5dabe-121">Propriétés de l’onglet</span><span class="sxs-lookup"><span data-stu-id="5dabe-121">Tab Properties</span></span>

<span data-ttu-id="5dabe-122">L’infrastructure du ruban définit une collection de [clés de propriété](windowsribbon-reference-properties.md) pour le contrôle onglet.</span><span class="sxs-lookup"><span data-stu-id="5dabe-122">The Ribbon framework defines a collection of [property keys](windowsribbon-reference-properties.md) for the Tab control.</span></span>

<span data-ttu-id="5dabe-123">En général, une propriété de tabulation est mise à jour dans l’interface utilisateur du ruban en invalidant la commande associée au contrôle via un appel à la méthode [**IUIFramework :: InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) .</span><span class="sxs-lookup"><span data-stu-id="5dabe-123">Typically, a Tab property is updated in the ribbon UI by invalidating the Command associated with the control through a call to the [**IUIFramework::InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) method.</span></span> <span data-ttu-id="5dabe-124">L’événement d’invalidation est géré, et les mises à jour de la propriété sont définies par la méthode de rappel [**IUICommandHandler :: UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) .</span><span class="sxs-lookup"><span data-stu-id="5dabe-124">The invalidation event is handled, and the property updates defined, by the [**IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) callback method.</span></span>

<span data-ttu-id="5dabe-125">La méthode de rappel [**IUICommandHandler :: UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) n’est pas exécutée et l’application a interrogé une valeur de propriété mise à jour, jusqu’à ce que la propriété soit requise par le Framework.</span><span class="sxs-lookup"><span data-stu-id="5dabe-125">The [**IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) callback method is not executed, and the application queried for an updated property value, until the property is required by the framework.</span></span> <span data-ttu-id="5dabe-126">Par exemple, lorsqu’un onglet est activé et qu’un contrôle est affiché dans l’interface ruban, ou lorsqu’une info-bulle est affichée.</span><span class="sxs-lookup"><span data-stu-id="5dabe-126">For example, when a tab is activated and a control revealed in the ribbon UI, or when a tooltip is displayed.</span></span>

> [!Note]  
> <span data-ttu-id="5dabe-127">Dans certains cas, une propriété peut être récupérée par le biais de la méthode [**IUIFramework :: GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) et définie avec la méthode [**IUIFramework :: SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) .</span><span class="sxs-lookup"><span data-stu-id="5dabe-127">In some cases, a property can be retrieved through the [**IUIFramework::GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) method and set with the [**IUIFramework::SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) method.</span></span>

 

<span data-ttu-id="5dabe-128">Le tableau suivant répertorie les clés de propriété associées au contrôle Tab.</span><span class="sxs-lookup"><span data-stu-id="5dabe-128">The following table lists the property keys that are associated with the Tab control.</span></span>



| <span data-ttu-id="5dabe-129">Clé de propriété</span><span class="sxs-lookup"><span data-stu-id="5dabe-129">Property Key</span></span>                                                                                     | <span data-ttu-id="5dabe-130">Notes</span><span class="sxs-lookup"><span data-stu-id="5dabe-130">Notes</span></span>                                     |
|--------------------------------------------------------------------------------------------------|-------------------------------------------|
| [<span data-ttu-id="5dabe-131">\_Étiquette de nom de l’interface utilisateur \_</span><span class="sxs-lookup"><span data-stu-id="5dabe-131">UI\_PKEY\_Label</span></span>](windowsribbon-reference-properties-uipkey-label.md)                           | <span data-ttu-id="5dabe-132">Peut uniquement être mis à jour par le biais d’une invalidation.</span><span class="sxs-lookup"><span data-stu-id="5dabe-132">Can only be updated through invalidation.</span></span> |
| [<span data-ttu-id="5dabe-133">KeyTip de l’interface utilisateur \_ \_</span><span class="sxs-lookup"><span data-stu-id="5dabe-133">UI\_PKEY\_Keytip</span></span>](windowsribbon-reference-properties-uipkey-keytip.md)                         | <span data-ttu-id="5dabe-134">Peut uniquement être mis à jour par le biais d’une invalidation.</span><span class="sxs-lookup"><span data-stu-id="5dabe-134">Can only be updated through invalidation.</span></span> |
| [<span data-ttu-id="5dabe-135">IU \_ \_ TooltipDescription</span><span class="sxs-lookup"><span data-stu-id="5dabe-135">UI\_PKEY\_TooltipDescription</span></span>](windowsribbon-reference-properties-uipkey-tooltipdescription.md) | <span data-ttu-id="5dabe-136">Peut uniquement être mis à jour par le biais d’une invalidation.</span><span class="sxs-lookup"><span data-stu-id="5dabe-136">Can only be updated through invalidation.</span></span> |
| [<span data-ttu-id="5dabe-137">IU \_ \_ TooltipTitle</span><span class="sxs-lookup"><span data-stu-id="5dabe-137">UI\_PKEY\_TooltipTitle</span></span>](windowsribbon-reference-properties-uipkey-tooltiptitle.md)             | <span data-ttu-id="5dabe-138">Peut uniquement être mis à jour par le biais d’une invalidation.</span><span class="sxs-lookup"><span data-stu-id="5dabe-138">Can only be updated through invalidation.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="5dabe-139">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="5dabe-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5dabe-140">Bibliothèque de contrôles de l’infrastructure du ruban Windows</span><span class="sxs-lookup"><span data-stu-id="5dabe-140">Windows Ribbon Framework Control Library</span></span>](windowsribbon-controls-entry.md)
</dt> <dt>

[<span data-ttu-id="5dabe-141">**Élément de balisage Tab**</span><span class="sxs-lookup"><span data-stu-id="5dabe-141">**Tab markup element**</span></span>](windowsribbon-element-tab.md)
</dt> </dl>

 

 
