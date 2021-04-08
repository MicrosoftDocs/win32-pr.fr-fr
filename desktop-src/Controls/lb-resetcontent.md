---
title: Message LB_RESETCONTENT (winuser. h)
description: Supprime tous les éléments d’une zone de liste.
ms.assetid: 3865e45e-62da-457a-801c-2f9a61687022
keywords:
- LB_RESETCONTENT les contrôles de message Windows
topic_type:
- apiref
api_name:
- LB_RESETCONTENT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c0091871df045812dcaa7a159cc456a1350d20f0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103844121"
---
# <a name="lb_resetcontent-message"></a><span data-ttu-id="796f5-104">\_Message RESETCONTENT lb</span><span class="sxs-lookup"><span data-stu-id="796f5-104">LB\_RESETCONTENT message</span></span>

<span data-ttu-id="796f5-105">Supprime tous les éléments d’une zone de liste.</span><span class="sxs-lookup"><span data-stu-id="796f5-105">Removes all items from a list box.</span></span>

## <a name="parameters"></a><span data-ttu-id="796f5-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="796f5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="796f5-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="796f5-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="796f5-108">Non utilisé ; doit être égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="796f5-108">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="796f5-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="796f5-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="796f5-110">Non utilisé ; doit être égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="796f5-110">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="796f5-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="796f5-111">Return value</span></span>

<span data-ttu-id="796f5-112">Ce message ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="796f5-112">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="796f5-113">Notes</span><span class="sxs-lookup"><span data-stu-id="796f5-113">Remarks</span></span>

<span data-ttu-id="796f5-114">Si la zone de liste a un style owner-drawn, mais pas le style [**\_ HASSTRINGS kg**](list-box-styles.md) , le propriétaire de la zone de liste reçoit un message [**WM \_ DELETEITEM**](wm-deleteitem.md) pour chaque élément de la zone de liste.</span><span class="sxs-lookup"><span data-stu-id="796f5-114">If the list box has an owner-drawn style but not the [**LBS\_HASSTRINGS**](list-box-styles.md) style, the owner of the list box receives a [**WM\_DELETEITEM**](wm-deleteitem.md) message for each item in the list box.</span></span>

## <a name="requirements"></a><span data-ttu-id="796f5-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="796f5-115">Requirements</span></span>



| <span data-ttu-id="796f5-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="796f5-116">Requirement</span></span> | <span data-ttu-id="796f5-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="796f5-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="796f5-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="796f5-118">Minimum supported client</span></span><br/> | <span data-ttu-id="796f5-119">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="796f5-119">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="796f5-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="796f5-120">Minimum supported server</span></span><br/> | <span data-ttu-id="796f5-121">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="796f5-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="796f5-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="796f5-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="796f5-123"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="796f5-123"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="796f5-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="796f5-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="796f5-125">**WM \_ DELETEITEM**</span><span class="sxs-lookup"><span data-stu-id="796f5-125">**WM\_DELETEITEM**</span></span>](wm-deleteitem.md)
</dt> </dl>

 

 





