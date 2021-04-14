---
title: Éléments récents
description: La liste éléments récents est un volet du menu de l’application qui affiche les éléments utilisés récemment (MRU) pour une application.
ms.assetid: fdead358-d303-46de-9f8e-6fc2832d8e94
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61f78c01fc4d6cc830eba644f7dcf22b6fb03e82
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104565249"
---
# <a name="recent-items"></a><span data-ttu-id="eb894-103">Éléments récents</span><span class="sxs-lookup"><span data-stu-id="eb894-103">Recent Items</span></span>

<span data-ttu-id="eb894-104">La liste éléments récents est un volet du menu de l' [application](windowsribbon-controls-applicationmenu.md) qui affiche les éléments utilisés récemment (MRU) pour une application.</span><span class="sxs-lookup"><span data-stu-id="eb894-104">The Recent Items list is a pane in the [Application Menu](windowsribbon-controls-applicationmenu.md) that displays the most recently used (MRU) items for an application.</span></span>

-   [<span data-ttu-id="eb894-105">Détails</span><span class="sxs-lookup"><span data-stu-id="eb894-105">Details</span></span>](#details)
-   [<span data-ttu-id="eb894-106">Propriétés des éléments récents</span><span class="sxs-lookup"><span data-stu-id="eb894-106">Recent Items Properties</span></span>](#recent-items-properties)
-   [<span data-ttu-id="eb894-107">Remarques</span><span class="sxs-lookup"><span data-stu-id="eb894-107">Remarks</span></span>](#remarks)
-   [<span data-ttu-id="eb894-108">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="eb894-108">Related topics</span></span>](#related-topics)

## <a name="details"></a><span data-ttu-id="eb894-109">Détails</span><span class="sxs-lookup"><span data-stu-id="eb894-109">Details</span></span>

<span data-ttu-id="eb894-110">La capture d’écran suivante illustre une liste d’éléments récents de WordPad pour Windows 7).</span><span class="sxs-lookup"><span data-stu-id="eb894-110">The following screen shot illustrates a Recent Items list from WordPad for Windows 7).</span></span>

![capture d’écran de la liste des éléments récents dans le ruban Microsoft Paint.](images/controls/recentitems.png)

<span data-ttu-id="eb894-112">Le [menu application](windowsribbon-controls-applicationmenu.md) ne peut avoir qu’une seule liste [**ApplicationMenu. RecentItems**](windowsribbon-element-applicationmenu-recentitems.md) , représentée par un élément **ApplicationMenu. RecentItems** , pour afficher les documents récents, les images, les films et les autres projets sur lesquels un utilisateur a travaillé.</span><span class="sxs-lookup"><span data-stu-id="eb894-112">The [Application Menu](windowsribbon-controls-applicationmenu.md) can have at most one [**ApplicationMenu.RecentItems**](windowsribbon-element-applicationmenu-recentitems.md) list, represented by an **ApplicationMenu.RecentItems** element, for displaying recent documents, pictures, movies, and other projects a user has been working on.</span></span> <span data-ttu-id="eb894-113">Le nombre d’éléments listés est compris entre zéro et le nombre maximal spécifié dans le balisage, avec une valeur par défaut de 10.</span><span class="sxs-lookup"><span data-stu-id="eb894-113">The number of listed items ranges from zero to the maximum number specified in markup, with a default value of ten.</span></span> <span data-ttu-id="eb894-114">Les éléments récents s’affichent sous la forme d’une liste numérotée de chaînes indiquant les noms de fichiers.</span><span class="sxs-lookup"><span data-stu-id="eb894-114">The recent items are displayed as a numbered list of strings indicating file names.</span></span> <span data-ttu-id="eb894-115">Il est recommandé d’utiliser la propriété [**Command. LabelDescription**](windowsribbon-element-command-labeldescription.md) pour fournir le chemin d’accès complet de l’emplacement du fichier, comme illustré dans la capture d’écran suivante.</span><span class="sxs-lookup"><span data-stu-id="eb894-115">It is recommended that the [**Command.LabelDescription**](windowsribbon-element-command-labeldescription.md) property be used to give the full path for the file location, as shown in the following screen shot .</span></span>

![capture d’écran d’une liste d’éléments récents dans un menu d’application.](images/overviews/applicationmenu-menurecentitems.png)

<span data-ttu-id="eb894-117">L’élément [**RecentItems**](windowsribbon-element-recentitems.md) a un attribut *EnablePinning* qui, s’il est défini sur `true` , affiche une icône d’épingle à droite de chaque élément de la liste, comme illustré dans la capture d’écran suivante.</span><span class="sxs-lookup"><span data-stu-id="eb894-117">The [**RecentItems**](windowsribbon-element-recentitems.md) element has an *EnablePinning* attribute that, if set to `true`, displays a pin icon to the right of each item in the list, as shown in the following screen shot.</span></span>

> [!Note]  
> <span data-ttu-id="eb894-118">L’épinglage est activé par défaut si l’attribut *EnablePinning* n’est pas spécifié.</span><span class="sxs-lookup"><span data-stu-id="eb894-118">Pinning is enabled by default if the *EnablePinning* attribute is not specified.</span></span>

 

![capture d’écran de l’épinglage d’éléments récents dans un menu d’application.](images/overviews/applicationmenu-menurecentitemspinned.png)

<span data-ttu-id="eb894-120">L’algorithme épinglé est conçu pour empêcher les éléments de tomber dans la liste des **éléments récents** .</span><span class="sxs-lookup"><span data-stu-id="eb894-120">The pinning algorithm is intended to keep items from falling off the **Recent items** list.</span></span> <span data-ttu-id="eb894-121">L’algorithme produit le comportement suivant :</span><span class="sxs-lookup"><span data-stu-id="eb894-121">The algorithm produces the following behavior:</span></span>

-   <span data-ttu-id="eb894-122">Un nouvel élément est toujours ajouté en haut de la liste des **éléments récents** .</span><span class="sxs-lookup"><span data-stu-id="eb894-122">A new item is always added at the top of the **Recent items** list.</span></span>
-   <span data-ttu-id="eb894-123">Les éléments se déplacent dans la liste au fil du temps.</span><span class="sxs-lookup"><span data-stu-id="eb894-123">Items will move down in the list over time.</span></span> <span data-ttu-id="eb894-124">Une fois la liste complète (atteint le nombre maximal d’éléments spécifiés dans le balisage), les éléments les plus anciens se trouvent en bas de la liste à mesure que de nouveaux éléments sont ajoutés en haut de la liste.</span><span class="sxs-lookup"><span data-stu-id="eb894-124">Once the list is full (reaches the maximum number of items specified in markup), older items fall off the bottom of the list as new items are added to the top of the list.</span></span>
-   <span data-ttu-id="eb894-125">Si un élément figure déjà dans la liste, mais fait l’objet d’un nouvel accès, il revient en haut de la liste.</span><span class="sxs-lookup"><span data-stu-id="eb894-125">If an item already appears somewhere in the list but is accessed again, it moves back to the top of the list.</span></span>
-   <span data-ttu-id="eb894-126">Si un élément est épinglé, il continue de parcourir la liste, mais il ne se situe pas en bas.</span><span class="sxs-lookup"><span data-stu-id="eb894-126">If an item is pinned, it will still travel down the list, but it will not fall off the bottom.</span></span> <span data-ttu-id="eb894-127">Au lieu de cela, une fois que la liste est pleine, le premier élément non épinglé au-dessus de l’élément épinglé s’arrête lorsqu’un nouvel élément est ajouté à la liste.</span><span class="sxs-lookup"><span data-stu-id="eb894-127">Instead, once the list is full, the first unpinned item above the pinned item will fall off when a new item is added to the list.</span></span>
-   <span data-ttu-id="eb894-128">Si le nombre d’éléments épinglés atteint toujours le nombre maximal d’éléments, aucun nouvel élément n’est ajouté à la liste tant qu’un élément n’est pas épinglé.</span><span class="sxs-lookup"><span data-stu-id="eb894-128">If the number of pinned items ever reaches the maximum number of items, then no new items will get added to the list until an item is unpinned.</span></span>

## <a name="recent-items-properties"></a><span data-ttu-id="eb894-129">Propriétés des éléments récents</span><span class="sxs-lookup"><span data-stu-id="eb894-129">Recent Items Properties</span></span>

<span data-ttu-id="eb894-130">L’infrastructure du ruban définit une collection de [clés de propriété](windowsribbon-reference-properties.md) pour le contrôle d’éléments récents.</span><span class="sxs-lookup"><span data-stu-id="eb894-130">The Ribbon framework defines a collection of [property keys](windowsribbon-reference-properties.md) for the Recent Items control.</span></span>

<span data-ttu-id="eb894-131">En général, une propriété Items récente est mise à jour dans l’interface ruban en invalidant la commande associée au contrôle via un appel à la méthode [**IUIFramework :: InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) .</span><span class="sxs-lookup"><span data-stu-id="eb894-131">Typically, a Recent Items property is updated in the ribbon UI by invalidating the Command associated with the control through a call to the [**IUIFramework::InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) method.</span></span> <span data-ttu-id="eb894-132">L’événement d’invalidation est géré, et les mises à jour de la propriété sont définies par la méthode de rappel [**IUICommandHandler :: UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) .</span><span class="sxs-lookup"><span data-stu-id="eb894-132">The invalidation event is handled, and the property updates defined, by the [**IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) callback method.</span></span>

<span data-ttu-id="eb894-133">La méthode de rappel [**IUICommandHandler :: UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) n’est pas exécutée et l’application a interrogé une valeur de propriété mise à jour, jusqu’à ce que la propriété soit requise par le Framework.</span><span class="sxs-lookup"><span data-stu-id="eb894-133">The [**IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) callback method is not executed, and the application queried for an updated property value, until the property is required by the framework.</span></span> <span data-ttu-id="eb894-134">Par exemple, lorsqu’un onglet est activé et qu’un contrôle est affiché dans l’interface ruban, ou lorsqu’une info-bulle est affichée.</span><span class="sxs-lookup"><span data-stu-id="eb894-134">For example, when a tab is activated and a control revealed in the ribbon UI, or when a tooltip is displayed.</span></span>

> [!Note]  
> <span data-ttu-id="eb894-135">Dans certains cas, une propriété peut être récupérée par le biais de la méthode [**IUIFramework :: GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) et définie avec la méthode [**IUIFramework :: SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) .</span><span class="sxs-lookup"><span data-stu-id="eb894-135">In some cases, a property can be retrieved through the [**IUIFramework::GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) method and set with the [**IUIFramework::SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) method.</span></span>

 

<span data-ttu-id="eb894-136">Le tableau suivant répertorie les clés de propriété associées au contrôle éléments récents.</span><span class="sxs-lookup"><span data-stu-id="eb894-136">The following table lists the property keys that are associated with the Recent Items control.</span></span>



| <span data-ttu-id="eb894-137">Clé de propriété</span><span class="sxs-lookup"><span data-stu-id="eb894-137">Property Key</span></span>                                                                       | <span data-ttu-id="eb894-138">Notes</span><span class="sxs-lookup"><span data-stu-id="eb894-138">Notes</span></span>                                     |
|------------------------------------------------------------------------------------|-------------------------------------------|
| [<span data-ttu-id="eb894-139">KeyTip de l’interface utilisateur \_ \_</span><span class="sxs-lookup"><span data-stu-id="eb894-139">UI\_PKEY\_Keytip</span></span>](windowsribbon-reference-properties-uipkey-keytip.md)           | <span data-ttu-id="eb894-140">Peut uniquement être mis à jour par le biais d’une invalidation.</span><span class="sxs-lookup"><span data-stu-id="eb894-140">Can only be updated through invalidation.</span></span> |
| [<span data-ttu-id="eb894-141">IU \_ \_ RecentItems</span><span class="sxs-lookup"><span data-stu-id="eb894-141">UI\_PKEY\_RecentItems</span></span>](windowsribbon-reference-properties-uipkey-recentitems.md) | <span data-ttu-id="eb894-142">Peut uniquement être mis à jour par le biais d’une invalidation.</span><span class="sxs-lookup"><span data-stu-id="eb894-142">Can only be updated through invalidation.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="eb894-143">Notes</span><span class="sxs-lookup"><span data-stu-id="eb894-143">Remarks</span></span>

<span data-ttu-id="eb894-144">La méthode [IApplicationDocumentLists :: GetList](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iapplicationdocumentlists-getlist) peut être utilisée pour récupérer la liste des derniers éléments de l’interpréteur de commandes Windows pour l’application ruban.</span><span class="sxs-lookup"><span data-stu-id="eb894-144">The [IApplicationDocumentLists::GetList](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iapplicationdocumentlists-getlist) method can be used to retrieve the Windows Shell MRU list for the Ribbon application.</span></span> <span data-ttu-id="eb894-145">L’objet récupéré par cette méthode peut ensuite être utilisé par l’application pour créer les données requises par l’infrastructure du ruban pour remplir la liste des **éléments récents** du menu de l' [application](windowsribbon-controls-applicationmenu.md).</span><span class="sxs-lookup"><span data-stu-id="eb894-145">The object retrieved by this method can then be used by the application to create the data required by the Ribbon framework to populate the **Recent items** list of the [Application Menu](windowsribbon-controls-applicationmenu.md).</span></span>

> [!Note]  
> <span data-ttu-id="eb894-146">Lors de l’utilisation de cette méthode, *ListType* doit avoir la valeur `ADLT_RECENT` .</span><span class="sxs-lookup"><span data-stu-id="eb894-146">When using this method, *listtype* should have the value `ADLT_RECENT`.</span></span>

 

<span data-ttu-id="eb894-147">Pour obtenir un exemple d’implémentation d’une liste d’éléments MRU dans une application de Framework de ruban, consultez l' [exemple HTMLEditRibbon](windowsribbon-htmleditribbonsample.md).</span><span class="sxs-lookup"><span data-stu-id="eb894-147">For an example of how to implement an MRU items list in a Ribbon framework application, see the [HTMLEditRibbon Sample](windowsribbon-htmleditribbonsample.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="eb894-148">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="eb894-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="eb894-149">Bibliothèque de contrôles de l’infrastructure du ruban Windows</span><span class="sxs-lookup"><span data-stu-id="eb894-149">Windows Ribbon Framework Control Library</span></span>](windowsribbon-controls-entry.md)
</dt> <dt>

[<span data-ttu-id="eb894-150">**Élément de balisage des éléments récents**</span><span class="sxs-lookup"><span data-stu-id="eb894-150">**Recent items markup element**</span></span>](windowsribbon-element-recentitems.md)
</dt> </dl>

 

 