---
title: Message LB_GETCURSEL (winuser. h)
description: Obtient l’index de l’élément actuellement sélectionné, le cas échéant, dans une zone de liste à sélection unique.
ms.assetid: 39ab7f77-6c8e-45a4-aad4-47eba0a11a11
keywords:
- LB_GETCURSEL les contrôles de message Windows
topic_type:
- apiref
api_name:
- LB_GETCURSEL
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4a6209f1f5b67e059f9a2b8a224e6f96ec671e38
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104033205"
---
# <a name="lb_getcursel-message"></a><span data-ttu-id="536c1-104">\_Message GETCURSEL lb</span><span class="sxs-lookup"><span data-stu-id="536c1-104">LB\_GETCURSEL message</span></span>

<span data-ttu-id="536c1-105">Obtient l’index de l’élément actuellement sélectionné, le cas échéant, dans une zone de liste à sélection unique.</span><span class="sxs-lookup"><span data-stu-id="536c1-105">Gets the index of the currently selected item, if any, in a single-selection list box.</span></span>

## <a name="parameters"></a><span data-ttu-id="536c1-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="536c1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="536c1-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="536c1-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="536c1-108">Non utilisé ; doit être égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="536c1-108">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="536c1-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="536c1-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="536c1-110">Non utilisé ; doit être égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="536c1-110">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="536c1-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="536c1-111">Return value</span></span>

<span data-ttu-id="536c1-112">Dans une zone de liste à sélection unique, la valeur de retour est l’index de base zéro de l’élément actuellement sélectionné.</span><span class="sxs-lookup"><span data-stu-id="536c1-112">In a single-selection list box, the return value is the zero-based index of the currently selected item.</span></span> <span data-ttu-id="536c1-113">S’il n’y a aucune sélection, la valeur de retour est LB \_ Err.</span><span class="sxs-lookup"><span data-stu-id="536c1-113">If there is no selection, the return value is LB\_ERR.</span></span>

## <a name="remarks"></a><span data-ttu-id="536c1-114">Notes</span><span class="sxs-lookup"><span data-stu-id="536c1-114">Remarks</span></span>

<span data-ttu-id="536c1-115">Pour récupérer les index des éléments sélectionnés dans une zone de liste à sélection multiple, utilisez le message [**lb \_ GETSELITEMS**](lb-getselitems.md) .</span><span class="sxs-lookup"><span data-stu-id="536c1-115">To retrieve the indexes of the selected items in a multiple-selection list box, use the [**LB\_GETSELITEMS**](lb-getselitems.md) message.</span></span> <span data-ttu-id="536c1-116">Pour déterminer si l’élément qui a le rectangle de focus dans une zone de liste à sélection multiple est sélectionné, utilisez le message [**lb \_ GETSEL**](lb-getsel.md) .</span><span class="sxs-lookup"><span data-stu-id="536c1-116">To determine whether the item that has the focus rectangle in a multiple selection list box is selected, use the [**LB\_GETSEL**](lb-getsel.md) message.</span></span>

<span data-ttu-id="536c1-117">En cas d’envoi à une zone de liste à sélection multiple, **lb \_ GETCURSEL** retourne l’index de l’élément qui a le rectangle de focus.</span><span class="sxs-lookup"><span data-stu-id="536c1-117">If sent to a multiple-selection list box, **LB\_GETCURSEL** returns the index of the item that has the focus rectangle.</span></span> <span data-ttu-id="536c1-118">Si aucun élément n’est sélectionné, la valeur retournée est zéro.</span><span class="sxs-lookup"><span data-stu-id="536c1-118">If no items are selected, it returns zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="536c1-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="536c1-119">Requirements</span></span>



| <span data-ttu-id="536c1-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="536c1-120">Requirement</span></span> | <span data-ttu-id="536c1-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="536c1-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="536c1-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="536c1-122">Minimum supported client</span></span><br/> | <span data-ttu-id="536c1-123">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="536c1-123">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="536c1-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="536c1-124">Minimum supported server</span></span><br/> | <span data-ttu-id="536c1-125">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="536c1-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="536c1-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="536c1-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="536c1-127"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="536c1-127"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="536c1-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="536c1-128">See also</span></span>

<dl> <dt>

<span data-ttu-id="536c1-129">**Référence**</span><span class="sxs-lookup"><span data-stu-id="536c1-129">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="536c1-130">**\_GETCARETINDEX lb**</span><span class="sxs-lookup"><span data-stu-id="536c1-130">**LB\_GETCARETINDEX**</span></span>](lb-getcaretindex.md)
</dt> <dt>

[<span data-ttu-id="536c1-131">**\_GETSEL lb**</span><span class="sxs-lookup"><span data-stu-id="536c1-131">**LB\_GETSEL**</span></span>](lb-getsel.md)
</dt> <dt>

[<span data-ttu-id="536c1-132">**\_GETSELITEMS lb**</span><span class="sxs-lookup"><span data-stu-id="536c1-132">**LB\_GETSELITEMS**</span></span>](lb-getselitems.md)
</dt> <dt>

[<span data-ttu-id="536c1-133">**\_SETCURSEL lb**</span><span class="sxs-lookup"><span data-stu-id="536c1-133">**LB\_SETCURSEL**</span></span>](lb-setcursel.md)
</dt> </dl>

 

 





