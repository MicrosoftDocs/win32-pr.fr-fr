---
title: Message TVM_GETSCROLLTIME (commctrl. h)
description: Récupère la durée maximale de défilement pour le contrôle Tree-View. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro GetScrollTime TreeView.
ms.assetid: 992d1906-cda3-4ac7-ba90-c681c551ac2e
keywords:
- TVM_GETSCROLLTIME les contrôles de message Windows
topic_type:
- apiref
api_name:
- TVM_GETSCROLLTIME
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e6f0bacc6c12dd7f54f20d882faf738c11848d59
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103209"
---
# <a name="tvm_getscrolltime-message"></a><span data-ttu-id="ffcd9-105">TVM \_ GETSCROLLTIME message</span><span class="sxs-lookup"><span data-stu-id="ffcd9-105">TVM\_GETSCROLLTIME message</span></span>

<span data-ttu-id="ffcd9-106">Récupère la durée maximale de défilement pour le contrôle Tree-View.</span><span class="sxs-lookup"><span data-stu-id="ffcd9-106">Retrieves the maximum scroll time for the tree-view control.</span></span> <span data-ttu-id="ffcd9-107">Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**\_ GetScrollTime TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getscrolltime) .</span><span class="sxs-lookup"><span data-stu-id="ffcd9-107">You can send this message explicitly or by using the [**TreeView\_GetScrollTime**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getscrolltime) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="ffcd9-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ffcd9-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ffcd9-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="ffcd9-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="ffcd9-110">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="ffcd9-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="ffcd9-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ffcd9-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="ffcd9-112">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="ffcd9-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ffcd9-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="ffcd9-113">Return value</span></span>

<span data-ttu-id="ffcd9-114">Retourne la durée maximale de défilement, en millisecondes.</span><span class="sxs-lookup"><span data-stu-id="ffcd9-114">Returns the maximum scroll time, in milliseconds.</span></span>

## <a name="remarks"></a><span data-ttu-id="ffcd9-115">Notes</span><span class="sxs-lookup"><span data-stu-id="ffcd9-115">Remarks</span></span>

<span data-ttu-id="ffcd9-116">La durée maximale de défilement est la durée la plus longue qu’une opération de défilement peut prendre.</span><span class="sxs-lookup"><span data-stu-id="ffcd9-116">The maximum scroll time is the longest amount of time that a scroll operation can take.</span></span> <span data-ttu-id="ffcd9-117">Le défilement est ajusté afin que le défilement s’effectue dans le délai de défilement maximal.</span><span class="sxs-lookup"><span data-stu-id="ffcd9-117">The scrolling will be adjusted so that the scroll will take place within the maximum scroll time.</span></span> <span data-ttu-id="ffcd9-118">Une opération de défilement peut prendre moins de temps que la valeur maximale.</span><span class="sxs-lookup"><span data-stu-id="ffcd9-118">A scroll operation may take less time than the maximum.</span></span>

## <a name="requirements"></a><span data-ttu-id="ffcd9-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ffcd9-119">Requirements</span></span>



| <span data-ttu-id="ffcd9-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ffcd9-120">Requirement</span></span> | <span data-ttu-id="ffcd9-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="ffcd9-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ffcd9-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ffcd9-122">Minimum supported client</span></span><br/> | <span data-ttu-id="ffcd9-123">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ffcd9-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="ffcd9-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ffcd9-124">Minimum supported server</span></span><br/> | <span data-ttu-id="ffcd9-125">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ffcd9-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ffcd9-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="ffcd9-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="ffcd9-127"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="ffcd9-127"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ffcd9-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ffcd9-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ffcd9-129">**TVM \_ SETSCROLLTIME**</span><span class="sxs-lookup"><span data-stu-id="ffcd9-129">**TVM\_SETSCROLLTIME**</span></span>](tvm-setscrolltime.md)
</dt> </dl>

 

 





