---
title: Message LB_SELITEMRANGE (winuser. h)
description: Sélectionne ou désélectionne un ou plusieurs éléments consécutifs dans une zone de liste à sélection multiple.
ms.assetid: 817d62df-98a3-40b3-8d62-86bf07ad797f
keywords:
- LB_SELITEMRANGE les contrôles de message Windows
topic_type:
- apiref
api_name:
- LB_SELITEMRANGE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a137b90a817519cf23c894dc19417dd2d9b6b7f3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104033148"
---
# <a name="lb_selitemrange-message"></a><span data-ttu-id="8e8b2-104">\_Message SELITEMRANGE lb</span><span class="sxs-lookup"><span data-stu-id="8e8b2-104">LB\_SELITEMRANGE message</span></span>

<span data-ttu-id="8e8b2-105">Sélectionne ou désélectionne un ou plusieurs éléments consécutifs dans une zone de liste à sélection multiple.</span><span class="sxs-lookup"><span data-stu-id="8e8b2-105">Selects or deselects one or more consecutive items in a multiple-selection list box.</span></span>

## <a name="parameters"></a><span data-ttu-id="8e8b2-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8e8b2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8e8b2-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="8e8b2-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8e8b2-108">**True** pour sélectionner la plage d’éléments, ou **false** pour la désélectionner.</span><span class="sxs-lookup"><span data-stu-id="8e8b2-108">**TRUE** to select the range of items, or **FALSE** to deselect it.</span></span>

</dd> <dt>

<span data-ttu-id="8e8b2-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="8e8b2-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8e8b2-110">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) spécifie l’index de base zéro du premier élément à sélectionner.</span><span class="sxs-lookup"><span data-stu-id="8e8b2-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) specifies the zero-based index of the first item to select.</span></span> <span data-ttu-id="8e8b2-111">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) spécifie l’index de base zéro du dernier élément à sélectionner.</span><span class="sxs-lookup"><span data-stu-id="8e8b2-111">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the zero-based index of the last item to select.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8e8b2-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="8e8b2-112">Return value</span></span>

<span data-ttu-id="8e8b2-113">Si une erreur se produit, la valeur de retour est LB \_ Err.</span><span class="sxs-lookup"><span data-stu-id="8e8b2-113">If an error occurs, the return value is LB\_ERR.</span></span>

## <a name="remarks"></a><span data-ttu-id="8e8b2-114">Notes</span><span class="sxs-lookup"><span data-stu-id="8e8b2-114">Remarks</span></span>

<span data-ttu-id="8e8b2-115">Utilisez ce message uniquement avec les zones de liste à sélection multiple.</span><span class="sxs-lookup"><span data-stu-id="8e8b2-115">Use this message only with multiple-selection list boxes.</span></span>

<span data-ttu-id="8e8b2-116">Ce message peut sélectionner une plage uniquement dans les 65 536 premiers éléments.</span><span class="sxs-lookup"><span data-stu-id="8e8b2-116">This message can select a range only within the first 65,536 items.</span></span>

## <a name="requirements"></a><span data-ttu-id="8e8b2-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8e8b2-117">Requirements</span></span>



| <span data-ttu-id="8e8b2-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8e8b2-118">Requirement</span></span> | <span data-ttu-id="8e8b2-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="8e8b2-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8e8b2-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8e8b2-120">Minimum supported client</span></span><br/> | <span data-ttu-id="8e8b2-121">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8e8b2-121">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="8e8b2-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8e8b2-122">Minimum supported server</span></span><br/> | <span data-ttu-id="8e8b2-123">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8e8b2-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="8e8b2-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="8e8b2-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="8e8b2-125"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="8e8b2-125"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8e8b2-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8e8b2-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="8e8b2-127">**Référence**</span><span class="sxs-lookup"><span data-stu-id="8e8b2-127">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="8e8b2-128">**\_SELITEMRANGEEX lb**</span><span class="sxs-lookup"><span data-stu-id="8e8b2-128">**LB\_SELITEMRANGEEX**</span></span>](lb-selitemrangeex.md)
</dt> <dt>

[<span data-ttu-id="8e8b2-129">**\_SETSEL lb**</span><span class="sxs-lookup"><span data-stu-id="8e8b2-129">**LB\_SETSEL**</span></span>](lb-setsel.md)
</dt> <dt>

<span data-ttu-id="8e8b2-130">**Autres ressources**</span><span class="sxs-lookup"><span data-stu-id="8e8b2-130">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="8e8b2-131">**MAKELPARAM**</span><span class="sxs-lookup"><span data-stu-id="8e8b2-131">**MAKELPARAM**</span></span>](/windows/desktop/api/winuser/nf-winuser-makelparam)
</dt> </dl>

 

