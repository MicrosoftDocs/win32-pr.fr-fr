---
title: Message TVM_SETSCROLLTIME (commctrl. h)
description: Définit la durée maximale de défilement pour le contrôle Tree-View. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro SetScrollTime TreeView.
ms.assetid: b0ad81ba-0621-42b7-8fe1-f3bd5bc16d6a
keywords:
- TVM_SETSCROLLTIME les contrôles de message Windows
topic_type:
- apiref
api_name:
- TVM_SETSCROLLTIME
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b49fab2f662b5ec641d9ffc6cc276f2196d2613e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106510976"
---
# <a name="tvm_setscrolltime-message"></a><span data-ttu-id="2d1bd-105">TVM \_ SETSCROLLTIME message</span><span class="sxs-lookup"><span data-stu-id="2d1bd-105">TVM\_SETSCROLLTIME message</span></span>

<span data-ttu-id="2d1bd-106">Définit la durée maximale de défilement pour le contrôle Tree-View.</span><span class="sxs-lookup"><span data-stu-id="2d1bd-106">Sets the maximum scroll time for the tree-view control.</span></span> <span data-ttu-id="2d1bd-107">Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**\_ SetScrollTime TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setscrolltime) .</span><span class="sxs-lookup"><span data-stu-id="2d1bd-107">You can send this message explicitly or by using the [**TreeView\_SetScrollTime**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setscrolltime) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="2d1bd-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2d1bd-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2d1bd-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="2d1bd-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2d1bd-110">Nouvelle durée maximale de défilement, en millisecondes.</span><span class="sxs-lookup"><span data-stu-id="2d1bd-110">New maximum scroll time, in milliseconds.</span></span>

</dd> <dt>

<span data-ttu-id="2d1bd-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="2d1bd-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="2d1bd-112">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="2d1bd-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2d1bd-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="2d1bd-113">Return value</span></span>

<span data-ttu-id="2d1bd-114">Retourne le temps de défilement maximal précédent, en millisecondes.</span><span class="sxs-lookup"><span data-stu-id="2d1bd-114">Returns the previous maximum scroll time, in milliseconds.</span></span>

## <a name="remarks"></a><span data-ttu-id="2d1bd-115">Notes</span><span class="sxs-lookup"><span data-stu-id="2d1bd-115">Remarks</span></span>

<span data-ttu-id="2d1bd-116">La durée maximale de défilement est la durée la plus longue qu’une opération de défilement peut prendre.</span><span class="sxs-lookup"><span data-stu-id="2d1bd-116">The maximum scroll time is the longest amount of time that a scroll operation can take.</span></span> <span data-ttu-id="2d1bd-117">Le défilement est ajusté afin que le défilement s’effectue dans le délai de défilement maximal.</span><span class="sxs-lookup"><span data-stu-id="2d1bd-117">Scrolling will be adjusted so that the scroll will take place within the maximum scroll time.</span></span> <span data-ttu-id="2d1bd-118">Une opération de défilement peut prendre moins de temps que la valeur maximale.</span><span class="sxs-lookup"><span data-stu-id="2d1bd-118">A scroll operation may take less time than the maximum.</span></span>

## <a name="requirements"></a><span data-ttu-id="2d1bd-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2d1bd-119">Requirements</span></span>



| <span data-ttu-id="2d1bd-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2d1bd-120">Requirement</span></span> | <span data-ttu-id="2d1bd-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="2d1bd-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2d1bd-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2d1bd-122">Minimum supported client</span></span><br/> | <span data-ttu-id="2d1bd-123">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2d1bd-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="2d1bd-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2d1bd-124">Minimum supported server</span></span><br/> | <span data-ttu-id="2d1bd-125">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2d1bd-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="2d1bd-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="2d1bd-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="2d1bd-127"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="2d1bd-127"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2d1bd-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2d1bd-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2d1bd-129">**TVM \_ GETSCROLLTIME**</span><span class="sxs-lookup"><span data-stu-id="2d1bd-129">**TVM\_GETSCROLLTIME**</span></span>](tvm-getscrolltime.md)
</dt> </dl>

 

 





