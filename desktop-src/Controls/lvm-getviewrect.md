---
title: Message LVM_GETVIEWRECT (commctrl. h)
description: Récupère le rectangle englobant de tous les éléments dans le contrôle List-View. La vue liste doit être en mode icône ou petite icône. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro ListView GetViewRect.
ms.assetid: 69b96f86-8b7e-42c1-ad73-f9b2732ab9f9
keywords:
- LVM_GETVIEWRECT les contrôles de message Windows
topic_type:
- apiref
api_name:
- LVM_GETVIEWRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d4c4fdf0e8466d3fb0b2ad164241c3f6a541570
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104033138"
---
# <a name="lvm_getviewrect-message"></a><span data-ttu-id="5b2a7-106">\_Message GETVIEWRECT LVM</span><span class="sxs-lookup"><span data-stu-id="5b2a7-106">LVM\_GETVIEWRECT message</span></span>

<span data-ttu-id="5b2a7-107">Récupère le rectangle englobant de tous les éléments dans le contrôle List-View.</span><span class="sxs-lookup"><span data-stu-id="5b2a7-107">Retrieves the bounding rectangle of all items in the list-view control.</span></span> <span data-ttu-id="5b2a7-108">La vue liste doit être en mode icône ou petite icône.</span><span class="sxs-lookup"><span data-stu-id="5b2a7-108">The list view must be in icon or small icon view.</span></span> <span data-ttu-id="5b2a7-109">Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**ListView \_ GetViewRect**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getviewrect) .</span><span class="sxs-lookup"><span data-stu-id="5b2a7-109">You can send this message explicitly or by using the [**ListView\_GetViewRect**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getviewrect) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="5b2a7-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5b2a7-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5b2a7-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="5b2a7-111">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="5b2a7-112">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="5b2a7-112">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="5b2a7-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="5b2a7-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5b2a7-114">Pointeur vers une structure [**Rect**](/previous-versions//dd162897(v=vs.85)) qui reçoit le rectangle englobant.</span><span class="sxs-lookup"><span data-stu-id="5b2a7-114">Pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure that receives the bounding rectangle.</span></span> <span data-ttu-id="5b2a7-115">Toutes les coordonnées sont relatives à la zone visible du contrôle List-View.</span><span class="sxs-lookup"><span data-stu-id="5b2a7-115">All coordinates are relative to the visible area of the list-view control.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5b2a7-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="5b2a7-116">Return value</span></span>

<span data-ttu-id="5b2a7-117">Retourne la **valeur true** en cas de réussite, ou **false** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="5b2a7-117">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="5b2a7-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5b2a7-118">Requirements</span></span>



| <span data-ttu-id="5b2a7-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5b2a7-119">Requirement</span></span> | <span data-ttu-id="5b2a7-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="5b2a7-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5b2a7-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5b2a7-121">Minimum supported client</span></span><br/> | <span data-ttu-id="5b2a7-122">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5b2a7-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="5b2a7-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5b2a7-123">Minimum supported server</span></span><br/> | <span data-ttu-id="5b2a7-124">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5b2a7-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="5b2a7-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="5b2a7-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="5b2a7-126"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="5b2a7-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

