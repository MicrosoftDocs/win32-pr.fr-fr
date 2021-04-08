---
title: Poignée de dimensionnement (référence des éléments d’interface utilisateur MSAA)
description: La poignée de dimensionnement est un pointeur de souris spécial dans le coin inférieur droit d’une fenêtre qui permet à un utilisateur de cliquer et de faire glisser la poignée de dimensionnement pour redimensionner la fenêtre.
ms.assetid: 886b27b3-e88d-47a1-85f3-a55bd14c7a7c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9fb7180a8936aff46903257e6be8ca4ab7f0e5b8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103675622"
---
# <a name="size-grip-msaa-ui-element-reference"></a><span data-ttu-id="103d9-103">Poignée de dimensionnement (référence des éléments d’interface utilisateur MSAA)</span><span class="sxs-lookup"><span data-stu-id="103d9-103">Size Grip (MSAA UI Element Reference)</span></span>

<span data-ttu-id="103d9-104">La poignée de dimensionnement est un pointeur de souris spécial dans le coin inférieur droit d’une fenêtre qui permet à un utilisateur de cliquer et de faire glisser la poignée de dimensionnement pour redimensionner la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="103d9-104">The size grip is a special mouse pointer in the lower-right corner of a window that allows a user to click and drag the size grip to resize the window.</span></span>

## <a name="iaccessible-methods"></a><span data-ttu-id="103d9-105">Méthodes IAccessible</span><span class="sxs-lookup"><span data-stu-id="103d9-105">IAccessible Methods</span></span>

<span data-ttu-id="103d9-106">La poignée de dimensionnement prend en charge les méthodes [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) suivantes :</span><span class="sxs-lookup"><span data-stu-id="103d9-106">The size grip supports the following [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) methods:</span></span>

-   [<span data-ttu-id="103d9-107">**accHitTest**</span><span class="sxs-lookup"><span data-stu-id="103d9-107">**accHitTest**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [<span data-ttu-id="103d9-108">**accLocation**</span><span class="sxs-lookup"><span data-stu-id="103d9-108">**accLocation**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)
-   [<span data-ttu-id="103d9-109">**accNavigate**</span><span class="sxs-lookup"><span data-stu-id="103d9-109">**accNavigate**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)

## <a name="iaccessible-properties"></a><span data-ttu-id="103d9-110">Propriétés IAccessible</span><span class="sxs-lookup"><span data-stu-id="103d9-110">IAccessible Properties</span></span>

<span data-ttu-id="103d9-111">La poignée de dimensionnement prend en charge les propriétés [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) suivantes :</span><span class="sxs-lookup"><span data-stu-id="103d9-111">The size grip supports the following [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) properties:</span></span>



| <span data-ttu-id="103d9-112">Propriété</span><span class="sxs-lookup"><span data-stu-id="103d9-112">Property</span></span>                                                                   | <span data-ttu-id="103d9-113">Commentaires</span><span class="sxs-lookup"><span data-stu-id="103d9-113">Comments</span></span>                                                                                                                                                               |
|----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="103d9-114">**Obtient \_ accDescription**</span><span class="sxs-lookup"><span data-stu-id="103d9-114">**get\_accDescription**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdescription) | <span data-ttu-id="103d9-115">La propriété **Description** est « peut être utilisée pour redimensionner la largeur et la hauteur d’une fenêtre ».</span><span class="sxs-lookup"><span data-stu-id="103d9-115">The **Description** property is "Can be used to resize a window's width and height".</span></span>                                                                                   |
| [<span data-ttu-id="103d9-116">**Obtient \_ accName**</span><span class="sxs-lookup"><span data-stu-id="103d9-116">**get\_accName**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)               | <span data-ttu-id="103d9-117">La propriété **Name** est « Size Box ».</span><span class="sxs-lookup"><span data-stu-id="103d9-117">The **Name** property is "Size box".</span></span>                                                                                                                                   |
| [<span data-ttu-id="103d9-118">**Obtient \_ accParent**</span><span class="sxs-lookup"><span data-stu-id="103d9-118">**get\_accParent**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)           | <span data-ttu-id="103d9-119">Fenêtre qui contient la poignée de dimensionnement.</span><span class="sxs-lookup"><span data-stu-id="103d9-119">The window that contains the size grip.</span></span>                                                                                                                                |
| [<span data-ttu-id="103d9-120">**Obtient \_ accRole**</span><span class="sxs-lookup"><span data-stu-id="103d9-120">**get\_accRole**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)               | <span data-ttu-id="103d9-121">La propriété **role** est [**la \_ \_ poignée du système de rôle**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="103d9-121">The **Role** property is [**ROLE\_SYSTEM\_GRIP**](object-roles.md).</span></span>                                                                                  |
| [<span data-ttu-id="103d9-122">**Obtient \_ accState**</span><span class="sxs-lookup"><span data-stu-id="103d9-122">**get\_accState**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)             | <span data-ttu-id="103d9-123">La valeur de la propriété **State** est zéro, ce qui signifie que l’objet est visible, ou le [**système d’État est \_ \_ invisible**](object-state-constants.md).</span><span class="sxs-lookup"><span data-stu-id="103d9-123">The value for the **State** property is zero, which means the object is visible, or [**STATE\_SYSTEM\_INVISIBLE**](object-state-constants.md).</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="103d9-124">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="103d9-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="103d9-125">IAccessible</span><span class="sxs-lookup"><span data-stu-id="103d9-125">IAccessible</span></span>](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

 




