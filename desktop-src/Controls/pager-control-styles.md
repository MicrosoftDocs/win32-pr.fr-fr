---
title: Styles de contrôle de pagineur (CommCtrl. h)
description: Cette section répertorie les styles de fenêtre utilisés lors de la création de contrôles de pagineur.
ms.assetid: 619fd8cc-e231-41af-8744-a29d14f2c6f8
topic_type:
- apiref
api_name:
- PGS_AUTOSCROLL
- PGS_DRAGNDROP
- PGS_HORZ
- PGS_VERT
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 496737f714ecb58c0d5a349207114cbf338e2c54
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106524003"
---
# <a name="pager-control-styles"></a><span data-ttu-id="d510b-103">Styles de contrôle de pagineur</span><span class="sxs-lookup"><span data-stu-id="d510b-103">Pager Control Styles</span></span>

<span data-ttu-id="d510b-104">Cette section répertorie les styles de fenêtre utilisés lors de la création de contrôles de pagineur.</span><span class="sxs-lookup"><span data-stu-id="d510b-104">This section lists the window styles used when creating pager controls.</span></span>



| <span data-ttu-id="d510b-105">Constante</span><span class="sxs-lookup"><span data-stu-id="d510b-105">Constant</span></span>                                                                                                                                                         | <span data-ttu-id="d510b-106">Description</span><span class="sxs-lookup"><span data-stu-id="d510b-106">Description</span></span>                                                                                                                                                                                                                 |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PGS_AUTOSCROLL"></span><span id="pgs_autoscroll"></span><dl> <span data-ttu-id="d510b-107"><dt>**DÉFILEMENT automatique PG \_**</dt></span><span class="sxs-lookup"><span data-stu-id="d510b-107"><dt>**PGS\_AUTOSCROLL**</dt></span></span> </dl> | <span data-ttu-id="d510b-108">Le contrôle de pagineur défile lorsque l’utilisateur place la souris sur l’un des boutons de défilement.</span><span class="sxs-lookup"><span data-stu-id="d510b-108">The pager control will scroll when the user hovers the mouse over one of the scroll buttons.</span></span><br/>                                                                                                                     |
| <span id="PGS_DRAGNDROP"></span><span id="pgs_dragndrop"></span><dl> <span data-ttu-id="d510b-109"><dt>**PG \_ DRAGNDROP**</dt></span><span class="sxs-lookup"><span data-stu-id="d510b-109"><dt>**PGS\_DRAGNDROP**</dt></span></span> </dl>    | <span data-ttu-id="d510b-110">La fenêtre contenue peut être une cible de glisser-déplacer.</span><span class="sxs-lookup"><span data-stu-id="d510b-110">The contained window can be a drag-and-drop target.</span></span> <span data-ttu-id="d510b-111">Le contrôle de pagineur effectue automatiquement un défilement si un élément est déplacé de l’extérieur du pagineur sur l’un des boutons de défilement.</span><span class="sxs-lookup"><span data-stu-id="d510b-111">The pager control will automatically scroll if an item is dragged from outside the pager over one of the scroll buttons.</span></span><br/>                                     |
| <span id="PGS_HORZ"></span><span id="pgs_horz"></span><dl> <span data-ttu-id="d510b-112"><dt>**PG \_ Horiz**</dt></span><span class="sxs-lookup"><span data-stu-id="d510b-112"><dt>**PGS\_HORZ**</dt></span></span> </dl>                   | <span data-ttu-id="d510b-113">Crée un contrôle de pagineur qui peut faire défiler horizontalement.</span><span class="sxs-lookup"><span data-stu-id="d510b-113">Creates a pager control that can be scrolled horizontally.</span></span> <span data-ttu-id="d510b-114">Ce style et le style **PG \_ vert** s’excluent mutuellement et ne peuvent pas être combinés.</span><span class="sxs-lookup"><span data-stu-id="d510b-114">This style and the **PGS\_VERT** style are mutually exclusive and cannot be combined.</span></span><br/>                                                                 |
| <span id="PGS_VERT"></span><span id="pgs_vert"></span><dl> <span data-ttu-id="d510b-115"><dt>**PG \_ vert**</dt></span><span class="sxs-lookup"><span data-stu-id="d510b-115"><dt>**PGS\_VERT**</dt></span></span> </dl>                   | <span data-ttu-id="d510b-116">Crée un contrôle de pagineur qui peut être défilé verticalement.</span><span class="sxs-lookup"><span data-stu-id="d510b-116">Creates a pager control that can be scrolled vertically.</span></span> <span data-ttu-id="d510b-117">Il s’agit de la direction par défaut si aucun style de direction n’est spécifié.</span><span class="sxs-lookup"><span data-stu-id="d510b-117">This is the default direction if no direction style is specified.</span></span> <span data-ttu-id="d510b-118">Ce style et le **style \_ Hori PG** s’excluent mutuellement et ne peuvent pas être combinés.</span><span class="sxs-lookup"><span data-stu-id="d510b-118">This style and the **PGS\_HORZ** style are mutually exclusive and cannot be combined.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="d510b-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d510b-119">Requirements</span></span>



| <span data-ttu-id="d510b-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d510b-120">Requirement</span></span> | <span data-ttu-id="d510b-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="d510b-121">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d510b-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="d510b-122">Header</span></span><br/> | <dl> <span data-ttu-id="d510b-123"><dt>CommCtrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="d510b-123"><dt>CommCtrl.h</dt></span></span> </dl> |



 

 





