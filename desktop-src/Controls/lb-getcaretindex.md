---
title: Message LB_GETCARETINDEX (winuser. h)
description: Récupère l’index de l’élément qui a le focus dans une zone de liste à sélection multiple. L’élément peut être ou non sélectionné.
ms.assetid: vs|controls|~\controls\listboxes\listboxreference\listboxmessages\lb_getcaretindex.htm
keywords:
- LB_GETCARETINDEX les contrôles de message Windows
topic_type:
- apiref
api_name:
- LB_GETCARETINDEX
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b9e4b8b2c75d72cdec606942991e957d8109ac7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104033206"
---
# <a name="lb_getcaretindex-message"></a><span data-ttu-id="cfbb7-105">\_Message GETCARETINDEX lb</span><span class="sxs-lookup"><span data-stu-id="cfbb7-105">LB\_GETCARETINDEX message</span></span>

<span data-ttu-id="cfbb7-106">Récupère l’index de l’élément qui a le focus dans une zone de liste à sélection multiple.</span><span class="sxs-lookup"><span data-stu-id="cfbb7-106">Retrieves the index of the item that has the focus in a multiple-selection list box.</span></span> <span data-ttu-id="cfbb7-107">L’élément peut être ou non sélectionné.</span><span class="sxs-lookup"><span data-stu-id="cfbb7-107">The item may or may not be selected.</span></span>

## <a name="parameters"></a><span data-ttu-id="cfbb7-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="cfbb7-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cfbb7-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="cfbb7-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="cfbb7-110">Non utilisé ; doit être égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="cfbb7-110">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="cfbb7-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="cfbb7-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="cfbb7-112">Non utilisé ; doit être égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="cfbb7-112">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cfbb7-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="cfbb7-113">Return value</span></span>

<span data-ttu-id="cfbb7-114">La valeur de retour est l’index de base zéro de l’élément de zone de liste ayant le focus, ou 0 si aucun élément n’a le focus.</span><span class="sxs-lookup"><span data-stu-id="cfbb7-114">The return value is the zero-based index of the focused list box item, or 0 if no item has the focus.</span></span>

## <a name="remarks"></a><span data-ttu-id="cfbb7-115">Notes</span><span class="sxs-lookup"><span data-stu-id="cfbb7-115">Remarks</span></span>

<span data-ttu-id="cfbb7-116">Ce message peut également être utilisé pour obtenir l’index de l’élément qui est actuellement sélectionné dans une zone de liste à sélection unique.</span><span class="sxs-lookup"><span data-stu-id="cfbb7-116">This message can also be used to get the index of the item that is currently selected in a single-selection list box.</span></span>

## <a name="requirements"></a><span data-ttu-id="cfbb7-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="cfbb7-117">Requirements</span></span>



| <span data-ttu-id="cfbb7-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="cfbb7-118">Requirement</span></span> | <span data-ttu-id="cfbb7-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="cfbb7-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cfbb7-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cfbb7-120">Minimum supported client</span></span><br/> | <span data-ttu-id="cfbb7-121">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="cfbb7-121">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="cfbb7-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cfbb7-122">Minimum supported server</span></span><br/> | <span data-ttu-id="cfbb7-123">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="cfbb7-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="cfbb7-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="cfbb7-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="cfbb7-125"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="cfbb7-125"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cfbb7-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cfbb7-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cfbb7-127">**\_SETCARETINDEX lb**</span><span class="sxs-lookup"><span data-stu-id="cfbb7-127">**LB\_SETCARETINDEX**</span></span>](lb-setcaretindex.md)
</dt> </dl>

 

 





