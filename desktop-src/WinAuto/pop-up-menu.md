---
title: Menu contextuel (référence des éléments d’interface utilisateur MSAA)
description: Un menu contextuel affiche une liste de commandes de menu.
ms.assetid: 9dbfa2d7-a086-4348-8b84-7e36d33e2d27
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 785fe8ac7a70352116b3a77cf30034092de04a23
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840381"
---
# <a name="pop-up-menu-msaa-ui-element-reference"></a><span data-ttu-id="5033e-103">Menu contextuel (référence des éléments d’interface utilisateur MSAA)</span><span class="sxs-lookup"><span data-stu-id="5033e-103">Pop-up Menu (MSAA UI Element Reference)</span></span>

> [!Note]  
> <span data-ttu-id="5033e-104">Cette rubrique décrit les objets **menu contextuel** à des fins de référence des éléments d’interface utilisateur MSAA.</span><span class="sxs-lookup"><span data-stu-id="5033e-104">This topic describes **Pop-up Menu** objects for purposes of MSAA UI Element Reference.</span></span> <span data-ttu-id="5033e-105">La procédure de création d’objets de **menu contextuel** dans différentes infrastructures d’interface utilisateur n’est pas décrite ici.</span><span class="sxs-lookup"><span data-stu-id="5033e-105">How to create **Pop-up Menu** objects in various UI frameworks is not described here.</span></span> <span data-ttu-id="5033e-106">Consultez la documentation de référence sur les API pour l’infrastructure d’interface utilisateur que vous utilisez.</span><span class="sxs-lookup"><span data-stu-id="5033e-106">See the API reference documentation for the UI framework you're using.</span></span>

 

<span data-ttu-id="5033e-107">Un menu contextuel affiche une liste de commandes de menu.</span><span class="sxs-lookup"><span data-stu-id="5033e-107">A pop-up menu displays a list of menu commands.</span></span> <span data-ttu-id="5033e-108">Microsoft Active Accessibility crée un objet menu contextuel lorsqu’un élément de menu est ouvert dans une barre de menus.</span><span class="sxs-lookup"><span data-stu-id="5033e-108">Microsoft Active Accessibility creates a menu pop-up object when a menu item in a menu bar is opened.</span></span> <span data-ttu-id="5033e-109">Microsoft Active Accessibility crée également des objets menus contextuels pour les menus contextuels, qui s’affichent quand l’utilisateur clique avec le bouton droit sur un élément d’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="5033e-109">Microsoft Active Accessibility also creates menu pop-up objects for context menus, which are displayed when the user right-clicks a user interface element.</span></span>

<span data-ttu-id="5033e-110">Le nom de la classe de fenêtre d’un menu contextuel est « \# 32768 ».</span><span class="sxs-lookup"><span data-stu-id="5033e-110">The window class name for a pop-up menu is "\#32768".</span></span>

## <a name="iaccessible-methods"></a><span data-ttu-id="5033e-111">Méthodes IAccessible</span><span class="sxs-lookup"><span data-stu-id="5033e-111">IAccessible Methods</span></span>

<span data-ttu-id="5033e-112">Un menu contextuel prend en charge les méthodes [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) suivantes :</span><span class="sxs-lookup"><span data-stu-id="5033e-112">A pop-up menu supports the following [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) methods:</span></span>

-   [<span data-ttu-id="5033e-113">**accHitTest**</span><span class="sxs-lookup"><span data-stu-id="5033e-113">**accHitTest**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [<span data-ttu-id="5033e-114">**accLocation**</span><span class="sxs-lookup"><span data-stu-id="5033e-114">**accLocation**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)
-   [<span data-ttu-id="5033e-115">**accNavigate**</span><span class="sxs-lookup"><span data-stu-id="5033e-115">**accNavigate**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
-   [<span data-ttu-id="5033e-116">**accSelect**</span><span class="sxs-lookup"><span data-stu-id="5033e-116">**accSelect**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)

## <a name="iaccessible-properties"></a><span data-ttu-id="5033e-117">Propriétés IAccessible</span><span class="sxs-lookup"><span data-stu-id="5033e-117">IAccessible Properties</span></span>

<span data-ttu-id="5033e-118">Un menu contextuel prend en charge les propriétés [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) suivantes :</span><span class="sxs-lookup"><span data-stu-id="5033e-118">A pop-up menu supports the following [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) properties:</span></span>



| <span data-ttu-id="5033e-119">Propriété</span><span class="sxs-lookup"><span data-stu-id="5033e-119">Property</span></span>                                                                 | <span data-ttu-id="5033e-120">Commentaires</span><span class="sxs-lookup"><span data-stu-id="5033e-120">Comments</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|--------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5033e-121">**Obtient \_ accChild**</span><span class="sxs-lookup"><span data-stu-id="5033e-121">**get\_accChild**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchild)           | <span data-ttu-id="5033e-122">Récupère le [**IDispatch**](idispatch-interface.md) pour l’élément de menu spécifié.</span><span class="sxs-lookup"><span data-stu-id="5033e-122">Retrieves the [**IDispatch**](idispatch-interface.md) for the specified menu item.</span></span> <span data-ttu-id="5033e-123">Les ID enfants pour les éléments de menu sont numérotés séquentiellement de haut en bas à partir de 1.</span><span class="sxs-lookup"><span data-stu-id="5033e-123">The child IDs for the menu items are numbered sequentially from top to bottom starting with one.</span></span>                                                                                                                                                                                                                                                                                      |
| [<span data-ttu-id="5033e-124">**Obtient \_ accChildCount**</span><span class="sxs-lookup"><span data-stu-id="5033e-124">**get\_accChildCount**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount) | <span data-ttu-id="5033e-125">La propriété **ChildCount** est le nombre d’éléments de menu dans le menu, y compris les séparateurs de menu.</span><span class="sxs-lookup"><span data-stu-id="5033e-125">The **ChildCount** property is the number of menu items in the menu, including menu separators.</span></span>                                                                                                                                                                                                                                                                                                                                                                           |
| [<span data-ttu-id="5033e-126">**Obtient \_ accFocus**</span><span class="sxs-lookup"><span data-stu-id="5033e-126">**get\_accFocus**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)           |                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [<span data-ttu-id="5033e-127">**Obtient \_ accName**</span><span class="sxs-lookup"><span data-stu-id="5033e-127">**get\_accName**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)             | <span data-ttu-id="5033e-128">La propriété **Name** d’un menu contextuel est le même nom que le menu.</span><span class="sxs-lookup"><span data-stu-id="5033e-128">The **Name** property for a pop-up menu is the same name as the menu.</span></span> <span data-ttu-id="5033e-129">La propriété **Name** d’un menu contextuel est « context ».</span><span class="sxs-lookup"><span data-stu-id="5033e-129">The **Name** property for a context menu is "Context".</span></span>                                                                                                                                                                                                                                                                                                                                              |
| [<span data-ttu-id="5033e-130">**Obtient \_ accParent**</span><span class="sxs-lookup"><span data-stu-id="5033e-130">**get\_accParent**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)         | <span data-ttu-id="5033e-131">La propriété **parent** est une fenêtre ( [**\_ \_ fenêtre système de rôle**](object-roles.md) ) qui entoure le menu contextuel et qui possède les mêmes propriétés de **nom** et nom de classe de fenêtre que le menu contextuel.</span><span class="sxs-lookup"><span data-stu-id="5033e-131">The **Parent** property is a window ( [**ROLE\_SYSTEM\_WINDOW**](object-roles.md) ) that surrounds the pop-up menu and has the same **Name** property and window class name as the pop-up menu .</span></span>                                                                                                                                                                                                                                                      |
| [<span data-ttu-id="5033e-132">**Obtient \_ accRole**</span><span class="sxs-lookup"><span data-stu-id="5033e-132">**get\_accRole**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)             | <span data-ttu-id="5033e-133">La propriété **role** est le [**système de rôle \_ \_ MENUPOPUP**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="5033e-133">The **Role** property is [**ROLE\_SYSTEM\_MENUPOPUP**](object-roles.md).</span></span>                                                                                                                                                                                                                                                                                                                                                                           |
| [<span data-ttu-id="5033e-134">**Obtient \_ accState**</span><span class="sxs-lookup"><span data-stu-id="5033e-134">**get\_accState**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)           | <span data-ttu-id="5033e-135">La propriété d' **État** est une combinaison d’une ou plusieurs des [valeurs](object-state-constants.md)suivantes : état du système d’état [**\_ \_ invisible**](object-state-constants.md) système d’état \| [**\_ \_ non disponible**](object-state-constants.md) système \| [**\_ \_**](object-state-constants.md) \| [**\_ \_**](object-state-constants.md)</span><span class="sxs-lookup"><span data-stu-id="5033e-135">The **State** property is a combination of one or more of the following [values](object-state-constants.md): [**STATE\_SYSTEM\_INVISIBLE**](object-state-constants.md) \| [**STATE\_SYSTEM\_UNAVAILABLE**](object-state-constants.md) \| [**STATE\_SYSTEM\_FOCUSED**](object-state-constants.md) \| [**STATE\_SYSTEM\_FOCUSABLE**](object-state-constants.md)</span></span><br/> |



 

## <a name="notes"></a><span data-ttu-id="5033e-136">Notes</span><span class="sxs-lookup"><span data-stu-id="5033e-136">Notes</span></span>

-   <span data-ttu-id="5033e-137">Les objets de menu contextuel ne déclenchent pas les événements de [**\_ \_ création**](event-constants.md) d’objet d’événement et de [**\_ \_ destruction d’objet d’événement**](event-constants.md) .</span><span class="sxs-lookup"><span data-stu-id="5033e-137">Pop-up menu objects do not trigger [**EVENT\_OBJECT\_CREATE**](event-constants.md) and [**EVENT\_OBJECT\_DESTROY**](event-constants.md) events.</span></span>
-   <span data-ttu-id="5033e-138">Les menus à plusieurs colonnes ne prennent pas en charge les indicateurs [**NAVDIR \_ Left**](navigation-constants.md) ou [**NAVDIR \_ Right**](navigation-constants.md) de la méthode [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate) .</span><span class="sxs-lookup"><span data-stu-id="5033e-138">Multi-column menus do not support the [**NAVDIR\_LEFT**](navigation-constants.md) or [**NAVDIR\_RIGHT**](navigation-constants.md) flags of the [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate) method.</span></span>
-   <span data-ttu-id="5033e-139">Les événements [**du \_ système \_**](event-constants.md) d’événements MENUPOPUPSTART et du système d’événements [**\_ \_ MENUPOPUPEND**](event-constants.md) ne sont pas envoyés de manière cohérente.</span><span class="sxs-lookup"><span data-stu-id="5033e-139">The events [**EVENT\_SYSTEM\_MENUPOPUPSTART**](event-constants.md) and [**EVENT\_SYSTEM\_MENUPOPUPEND**](event-constants.md) are not sent consistently.</span></span> <span data-ttu-id="5033e-140">Il s’agit d’un problème connu qui est traité.</span><span class="sxs-lookup"><span data-stu-id="5033e-140">This is a known issue and is being addressed.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5033e-141">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="5033e-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5033e-142">IAccessible, interface</span><span class="sxs-lookup"><span data-stu-id="5033e-142">IAccessible Interface</span></span>](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> <dt>

[<span data-ttu-id="5033e-143">**Barre de menus**</span><span class="sxs-lookup"><span data-stu-id="5033e-143">**Menu Bar**</span></span>](menu-bar.md)
</dt> <dt>

[<span data-ttu-id="5033e-144">**Élément de menu**</span><span class="sxs-lookup"><span data-stu-id="5033e-144">**Menu Item**</span></span>](menu-item.md)
</dt> </dl>

 

 





