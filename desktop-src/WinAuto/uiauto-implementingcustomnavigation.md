---
title: Modèle de contrôle CustomNavigation
description: Fournit des instructions et des conventions pour implémenter l’interface ICustomNavigationProvider, y compris des informations sur les propriétés et les méthodes.
ms.assetid: 428540BB-5CC0-4F49-8384-0FFC130FBB38
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 97cc6524585f3ddd7ec764a791141fce9daa3c4f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104196721"
---
# <a name="customnavigation-control-pattern"></a><span data-ttu-id="12c8b-103">Modèle de contrôle CustomNavigation</span><span class="sxs-lookup"><span data-stu-id="12c8b-103">CustomNavigation Control Pattern</span></span>

<span data-ttu-id="12c8b-104">Fournit des instructions et des conventions pour implémenter l’interface **ICustomNavigationProvider** , y compris des informations sur les propriétés et les méthodes.</span><span class="sxs-lookup"><span data-stu-id="12c8b-104">Describes guidelines and conventions for implementing the **ICustomNavigationProvider** interface, including information about properties and methods.</span></span> <span data-ttu-id="12c8b-105">Le modèle de contrôle **CustomNavigation** est utilisé pour activer la navigation personnalisée entre des contrôles dans des structures de type hiérarchie, telles que des éléments de liste, des listes à puces, des listes numérotées et des en-têtes.</span><span class="sxs-lookup"><span data-stu-id="12c8b-105">The **CustomNavigation** control pattern is used to enable custom navigation between controls in hierarchy-like structures such as list items, bulleted lists, numbered lists and headings.</span></span> <span data-ttu-id="12c8b-106">Cela permet aux fournisseurs de décrire des structures ou de définir les relations navigables à l’aide de l’élément seul et pas seulement du contrôle conteneur.</span><span class="sxs-lookup"><span data-stu-id="12c8b-106">This enables providers to describe structures or define the navigable relationships using the element alone and not just the containing control.</span></span>

<span data-ttu-id="12c8b-107">Pour obtenir des exemples de contrôles qui implémentent ce modèle de contrôle, consultez [types de contrôle et leurs modèles de contrôle pris en charge](uiauto-controlpatternmapping.md).</span><span class="sxs-lookup"><span data-stu-id="12c8b-107">For examples of controls that implement this control pattern, see [Control Types and Their Supported Control Patterns](uiauto-controlpatternmapping.md).</span></span>

<span data-ttu-id="12c8b-108">Cette rubrique contient les sections suivantes.</span><span class="sxs-lookup"><span data-stu-id="12c8b-108">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="12c8b-109">Conventions et directives d'implémentation</span><span class="sxs-lookup"><span data-stu-id="12c8b-109">Implementation Guidelines and Conventions</span></span>](#implementation-guidelines-and-conventions)
-   [<span data-ttu-id="12c8b-110">Membres requis pour **ICustomNavigationProvider**</span><span class="sxs-lookup"><span data-stu-id="12c8b-110">Required Members for **ICustomNavigationProvider**</span></span>](#required-members-for-icustomnavigationprovider)
-   [<span data-ttu-id="12c8b-111">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="12c8b-111">Related topics</span></span>](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a><span data-ttu-id="12c8b-112">Conventions et directives d'implémentation</span><span class="sxs-lookup"><span data-stu-id="12c8b-112">Implementation Guidelines and Conventions</span></span>

<span data-ttu-id="12c8b-113">Lorsque vous implémentez le fournisseur **CustomNavigation** , notez les conventions et recommandations suivantes :</span><span class="sxs-lookup"><span data-stu-id="12c8b-113">When implementing the **CustomNavigation** provider, note the following guidelines and conventions:</span></span>

-   <span data-ttu-id="12c8b-114">Les valeurs de propriété pour **PositionInSet**, **SizeOfSet** et **Level** sont des valeurs entières basées sur un.</span><span class="sxs-lookup"><span data-stu-id="12c8b-114">Property values for **PositionInSet**, **SizeOfSet**, and **Level** are one-based integer values.</span></span>
-   <span data-ttu-id="12c8b-115">**ICustomNavigationProvider** ne fournit pas de manipulation active du contrôle, comme déplacer des positions, ajouter et supprimer des éléments, ou promouvoir et rétrograder des niveaux.</span><span class="sxs-lookup"><span data-stu-id="12c8b-115">**ICustomNavigationProvider** does not provide for active manipulation of the control such as moving positions, adding and removing items, or promoting and demoting levels.</span></span>
-   <span data-ttu-id="12c8b-116">Les contrôles qui implémentent **ICustomNavigationProvider** ont généralement une structure hiérarchique, mais peuvent ignorer des niveaux à l’aide de la méthode **Navigate** .</span><span class="sxs-lookup"><span data-stu-id="12c8b-116">Controls that implement **ICustomNavigationProvider** typically have a hierarchical structure, but can skip levels by using the **Navigate** method.</span></span> <span data-ttu-id="12c8b-117">Les propriétés **PositionInSet**, **SizeOfSet** et **Level** sont requises sur le modèle.</span><span class="sxs-lookup"><span data-stu-id="12c8b-117">The properties **PositionInSet**, **SizeOfSet**, and **Level** are required on the pattern.</span></span>

## <a name="required-members-for-icustomnavigationprovider"></a><span data-ttu-id="12c8b-118">Membres requis pour **ICustomNavigationProvider**</span><span class="sxs-lookup"><span data-stu-id="12c8b-118">Required Members for **ICustomNavigationProvider**</span></span>

<span data-ttu-id="12c8b-119">Les propriétés suivantes sont requises pour implémenter l’interface **ICustomNavigationProvider** .</span><span class="sxs-lookup"><span data-stu-id="12c8b-119">The following properties are required for implementing the **ICustomNavigationProvider** interface.</span></span>



| <span data-ttu-id="12c8b-120">Membres nécessaires</span><span class="sxs-lookup"><span data-stu-id="12c8b-120">Required members</span></span>                                                                  | <span data-ttu-id="12c8b-121">Type de membre</span><span class="sxs-lookup"><span data-stu-id="12c8b-121">Member type</span></span> | <span data-ttu-id="12c8b-122">Notes</span><span class="sxs-lookup"><span data-stu-id="12c8b-122">Notes</span></span>                                                                               |
|-----------------------------------------------------------------------------------|-------------|-------------------------------------------------------------------------------------|
| [<span data-ttu-id="12c8b-123">**CachedLevel**</span><span class="sxs-lookup"><span data-stu-id="12c8b-123">**CachedLevel**</span></span>](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement4-get_cachedlevel)                   | <span data-ttu-id="12c8b-124">Propriété</span><span class="sxs-lookup"><span data-stu-id="12c8b-124">Property</span></span>    | <span data-ttu-id="12c8b-125">Situé sur l’interface [**IUIAutomationElement4**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement4) .</span><span class="sxs-lookup"><span data-stu-id="12c8b-125">Located on [**IUIAutomationElement4**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement4) interface.</span></span> |
| [<span data-ttu-id="12c8b-126">**CachedPositionInSet**</span><span class="sxs-lookup"><span data-stu-id="12c8b-126">**CachedPositionInSet**</span></span>](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement4-get_cachedpositioninset)   | <span data-ttu-id="12c8b-127">Propriété</span><span class="sxs-lookup"><span data-stu-id="12c8b-127">Property</span></span>    | <span data-ttu-id="12c8b-128">Situé sur l’interface [**IUIAutomationElement4**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement4) .</span><span class="sxs-lookup"><span data-stu-id="12c8b-128">Located on [**IUIAutomationElement4**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement4) interface.</span></span> |
| [<span data-ttu-id="12c8b-129">**CachedSizeOfSet**</span><span class="sxs-lookup"><span data-stu-id="12c8b-129">**CachedSizeOfSet**</span></span>](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement4-get_cachedsizeofset)           | <span data-ttu-id="12c8b-130">Propriété</span><span class="sxs-lookup"><span data-stu-id="12c8b-130">Property</span></span>    | <span data-ttu-id="12c8b-131">Situé sur l’interface [**IUIAutomationElement4**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement4) .</span><span class="sxs-lookup"><span data-stu-id="12c8b-131">Located on [**IUIAutomationElement4**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement4) interface.</span></span> |
| [<span data-ttu-id="12c8b-132">**CurrentLevel**</span><span class="sxs-lookup"><span data-stu-id="12c8b-132">**CurrentLevel**</span></span>](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement4-get_currentlevel)                 | <span data-ttu-id="12c8b-133">Propriété</span><span class="sxs-lookup"><span data-stu-id="12c8b-133">Property</span></span>    | <span data-ttu-id="12c8b-134">Situé sur l’interface [**IUIAutomationElement4**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement4) .</span><span class="sxs-lookup"><span data-stu-id="12c8b-134">Located on [**IUIAutomationElement4**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement4) interface.</span></span> |
| [<span data-ttu-id="12c8b-135">**CurrentPositionInSet**</span><span class="sxs-lookup"><span data-stu-id="12c8b-135">**CurrentPositionInSet**</span></span>](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement4-get_currentpositioninset) | <span data-ttu-id="12c8b-136">Propriété</span><span class="sxs-lookup"><span data-stu-id="12c8b-136">Property</span></span>    | <span data-ttu-id="12c8b-137">Situé sur l’interface [**IUIAutomationElement4**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement4) .</span><span class="sxs-lookup"><span data-stu-id="12c8b-137">Located on [**IUIAutomationElement4**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement4) interface.</span></span> |
| [<span data-ttu-id="12c8b-138">**CurrentSizeOfSet**</span><span class="sxs-lookup"><span data-stu-id="12c8b-138">**CurrentSizeOfSet**</span></span>](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement4-get_currentsizeofset)         | <span data-ttu-id="12c8b-139">Propriété</span><span class="sxs-lookup"><span data-stu-id="12c8b-139">Property</span></span>    | <span data-ttu-id="12c8b-140">Situé sur l’interface [**IUIAutomationElement4**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement4) .</span><span class="sxs-lookup"><span data-stu-id="12c8b-140">Located on [**IUIAutomationElement4**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement4) interface.</span></span> |
| [<span data-ttu-id="12c8b-141">**Sélectionnez**</span><span class="sxs-lookup"><span data-stu-id="12c8b-141">**Navigate**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementproviderfragment-navigate)                   | <span data-ttu-id="12c8b-142">Méthode</span><span class="sxs-lookup"><span data-stu-id="12c8b-142">Method</span></span>      | <span data-ttu-id="12c8b-143">Aucun</span><span class="sxs-lookup"><span data-stu-id="12c8b-143">None</span></span>                                                                                |



 

<span data-ttu-id="12c8b-144">Ce modèle de contrôle n’est associé à aucune méthode ou aucun événement.</span><span class="sxs-lookup"><span data-stu-id="12c8b-144">This control pattern has no associated methods or events.</span></span>

## <a name="related-topics"></a><span data-ttu-id="12c8b-145">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="12c8b-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="12c8b-146">Types de contrôle et leurs modèles de contrôle pris en charge</span><span class="sxs-lookup"><span data-stu-id="12c8b-146">Control Types and Their Supported Control Patterns</span></span>](uiauto-controlpatternmapping.md)
</dt> <dt>

[<span data-ttu-id="12c8b-147">ListItem, contrôle</span><span class="sxs-lookup"><span data-stu-id="12c8b-147">ListItem Control</span></span>](uiauto-supportlistitemcontroltype.md)
</dt> <dt>

[<span data-ttu-id="12c8b-148">Contrôle HeaderItem</span><span class="sxs-lookup"><span data-stu-id="12c8b-148">HeaderItem Control</span></span>](uiauto-supportheaderitemcontroltype.md)
</dt> <dt>

[<span data-ttu-id="12c8b-149">DataItem, contrôle</span><span class="sxs-lookup"><span data-stu-id="12c8b-149">DataItem Control</span></span>](uiauto-supportdataitemcontroltype.md)
</dt> <dt>

[<span data-ttu-id="12c8b-150">Vue d'ensemble des modèles de contrôle UI Automation</span><span class="sxs-lookup"><span data-stu-id="12c8b-150">UI Automation Control Patterns Overview</span></span>](uiauto-controlpatternsoverview.md)
</dt> </dl>

 

 




