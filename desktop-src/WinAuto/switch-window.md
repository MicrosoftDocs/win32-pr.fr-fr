---
title: Fenêtre de basculement (référence des éléments d’interface utilisateur MSAA)
description: La fenêtre commutateur s’affiche chaque fois qu’un utilisateur appuie sur ALT + TAB pour basculer vers une autre application. La fenêtre commutateur contient une icône pour chaque application en cours d’exécution.
ms.assetid: 77b32eb1-7722-410b-b141-ac09fc7fdffb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eead618e23f8a56c90b37eae2386f16a90f6dd67
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103675618"
---
# <a name="switch-window-msaa-ui-element-reference"></a><span data-ttu-id="d638f-104">Fenêtre de basculement (référence des éléments d’interface utilisateur MSAA)</span><span class="sxs-lookup"><span data-stu-id="d638f-104">Switch Window (MSAA UI Element Reference)</span></span>

<span data-ttu-id="d638f-105">La fenêtre commutateur s’affiche chaque fois qu’un utilisateur appuie sur ALT + TAB pour basculer vers une autre application.</span><span class="sxs-lookup"><span data-stu-id="d638f-105">The switch window displays whenever a user presses ALT+TAB to switch to a different application.</span></span> <span data-ttu-id="d638f-106">La fenêtre commutateur contient une icône pour chaque application en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="d638f-106">The switch window contains an icon for each application currently running.</span></span>

<span data-ttu-id="d638f-107">Le nom de classe de fenêtre pour la fenêtre de commutateur est « \# 32771 ».</span><span class="sxs-lookup"><span data-stu-id="d638f-107">The window class name for the switch window is "\#32771".</span></span>

## <a name="iaccessible-methods"></a><span data-ttu-id="d638f-108">Méthodes IAccessible</span><span class="sxs-lookup"><span data-stu-id="d638f-108">IAccessible Methods</span></span>

<span data-ttu-id="d638f-109">La fenêtre commutateur prend en charge les méthodes [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) suivantes :</span><span class="sxs-lookup"><span data-stu-id="d638f-109">The switch window supports the following [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) methods:</span></span>



| <span data-ttu-id="d638f-110">Méthode</span><span class="sxs-lookup"><span data-stu-id="d638f-110">Method</span></span>                                                                    | <span data-ttu-id="d638f-111">Commentaires</span><span class="sxs-lookup"><span data-stu-id="d638f-111">Comments</span></span>                                                                                                                                                                                                                          |
|---------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d638f-112">**accDoDefaultAction**</span><span class="sxs-lookup"><span data-stu-id="d638f-112">**accDoDefaultAction**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction) | <span data-ttu-id="d638f-113">L’objet de fenêtre de commutateur lui-même n’a pas de propriété **DefaultAction** .</span><span class="sxs-lookup"><span data-stu-id="d638f-113">The switch window object itself does not have a **DefaultAction** property.</span></span> <span data-ttu-id="d638f-114">La méthode [**accDoDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction) pour chaque élément de la fenêtre Switch active l’élément spécifié.</span><span class="sxs-lookup"><span data-stu-id="d638f-114">The [**accDoDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction) method for each item in the switch window activates the specified item.</span></span> |
| [<span data-ttu-id="d638f-115">**accHitTest**</span><span class="sxs-lookup"><span data-stu-id="d638f-115">**accHitTest**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)                 |                                                                                                                                                                                                                                   |
| [<span data-ttu-id="d638f-116">**accLocation**</span><span class="sxs-lookup"><span data-stu-id="d638f-116">**accLocation**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)               |                                                                                                                                                                                                                                   |
| [<span data-ttu-id="d638f-117">**accNavigate**</span><span class="sxs-lookup"><span data-stu-id="d638f-117">**accNavigate**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)               |                                                                                                                                                                                                                                   |
| [<span data-ttu-id="d638f-118">**accSelect**</span><span class="sxs-lookup"><span data-stu-id="d638f-118">**accSelect**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)                   |                                                                                                                                                                                                                                   |



 

## <a name="iaccessible-properties"></a><span data-ttu-id="d638f-119">Propriétés IAccessible</span><span class="sxs-lookup"><span data-stu-id="d638f-119">IAccessible Properties</span></span>

<span data-ttu-id="d638f-120">La fenêtre commutateur prend en charge les propriétés [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) suivantes :</span><span class="sxs-lookup"><span data-stu-id="d638f-120">The switch window supports the following [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) properties:</span></span>



|                                                                                |                                                                                                                                                                                                                                |
|--------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d638f-121">**Obtient \_ accChildCount**</span><span class="sxs-lookup"><span data-stu-id="d638f-121">**get\_accChildCount**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount)       | <span data-ttu-id="d638f-122">La propriété **ChildCount** est égale à zéro.</span><span class="sxs-lookup"><span data-stu-id="d638f-122">The **ChildCount** property is zero.</span></span>                                                                                                                                                                                           |
| [<span data-ttu-id="d638f-123">**Obtient \_ accDefaultAction**</span><span class="sxs-lookup"><span data-stu-id="d638f-123">**get\_accDefaultAction**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdefaultaction) | <span data-ttu-id="d638f-124">L’objet de fenêtre de commutateur lui-même n’a pas de propriété **DefaultAction** .</span><span class="sxs-lookup"><span data-stu-id="d638f-124">The switch window object itself does not have a **DefaultAction** property.</span></span> <span data-ttu-id="d638f-125">La propriété **DefaultAction** pour chaque élément de la fenêtre commutateur est « Switch ».</span><span class="sxs-lookup"><span data-stu-id="d638f-125">The **DefaultAction** property for each item in the switch window is "Switch".</span></span>                                                                     |
| [<span data-ttu-id="d638f-126">**Obtient \_ accFocus**</span><span class="sxs-lookup"><span data-stu-id="d638f-126">**get\_accFocus**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)                 | <span data-ttu-id="d638f-127">L’objet parent de la fenêtre de basculement ne peut pas recevoir le focus. Seuls les enfants individuels peuvent recevoir le focus.</span><span class="sxs-lookup"><span data-stu-id="d638f-127">The switch window parent object cannot receive focus; only the individual children can receive focus.</span></span>                                                                                                                          |
| [<span data-ttu-id="d638f-128">**Obtient \_ accName**</span><span class="sxs-lookup"><span data-stu-id="d638f-128">**get\_accName**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)                   | <span data-ttu-id="d638f-129">L’objet de fenêtre de commutateur lui-même n’a pas de propriété **Name** .</span><span class="sxs-lookup"><span data-stu-id="d638f-129">The switch window object itself does not have a **Name** property.</span></span> <span data-ttu-id="d638f-130">La propriété **nom** de chaque icône d’application dans la fenêtre commutateur est la même que le nom de l’application affichée.</span><span class="sxs-lookup"><span data-stu-id="d638f-130">The **Name** property for each application icon in the switch window is the same as the displayed application name.</span></span>                                         |
| [<span data-ttu-id="d638f-131">**Obtient \_ accRole**</span><span class="sxs-lookup"><span data-stu-id="d638f-131">**get\_accRole**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)                   | <span data-ttu-id="d638f-132">L’objet de fenêtre de commutateur lui-même a une propriété **role** « Window \[ 32771 \] ».</span><span class="sxs-lookup"><span data-stu-id="d638f-132">The switch window object itself has a **Role** property of "window \[32771\]".</span></span> <span data-ttu-id="d638f-133">En outre, chaque icône d’application dans la fenêtre commutateur a la propriété **role** [**ListItem du \_ système \_ de rôle**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="d638f-133">Also, each application icon in the switch window has the **Role** property [**ROLE\_SYSTEM\_LISTITEM**](object-roles.md).</span></span> |
| [<span data-ttu-id="d638f-134">**Obtient \_ accState**</span><span class="sxs-lookup"><span data-stu-id="d638f-134">**get\_accState**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)                 | <span data-ttu-id="d638f-135">L’objet de fenêtre de commutateur lui-même ne prend pas en charge la propriété **State** .</span><span class="sxs-lookup"><span data-stu-id="d638f-135">The switch window object itself does not support the **State** property.</span></span> <span data-ttu-id="d638f-136">La valeur d' **État** pour les éléments de la vue liste est le [**focus du \_ système \_ d’État**](object-state-constants.md).</span><span class="sxs-lookup"><span data-stu-id="d638f-136">The **State** value for the list view items is [**STATE\_SYSTEM\_FOCUSABLE**](object-state-constants.md).</span></span>                     |



 

## <a name="related-topics"></a><span data-ttu-id="d638f-137">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="d638f-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d638f-138">IAccessible, interface</span><span class="sxs-lookup"><span data-stu-id="d638f-138">IAccessible Interface</span></span>](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

 




