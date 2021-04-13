---
title: Message LB_GETANCHORINDEX (winuser. h)
description: Obtient l’index de l’élément d’ancrage \ 8212 ; autrement dit, l’élément à partir duquel commence une sélection multiple. Une sélection multiple s’étend sur tous les éléments de l’élément d’ancrage à l’élément du signe insertion.
ms.assetid: vs|controls|~\controls\listboxes\listboxreference\listboxmessages\lb_getanchorindex.htm
keywords:
- LB_GETANCHORINDEX les contrôles de message Windows
topic_type:
- apiref
api_name:
- LB_GETANCHORINDEX
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5502a234424b818bb46e9c4326839b5aff2f83d0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104509302"
---
# <a name="lb_getanchorindex-message"></a><span data-ttu-id="58a9b-105">\_Message GETANCHORINDEX lb</span><span class="sxs-lookup"><span data-stu-id="58a9b-105">LB\_GETANCHORINDEX message</span></span>

<span data-ttu-id="58a9b-106">Obtient l’index de l’élément d’ancrage qui est, l’élément à partir duquel une sélection multiple démarre.</span><span class="sxs-lookup"><span data-stu-id="58a9b-106">Gets the index of the anchor item that is, the item from which a multiple selection starts.</span></span> <span data-ttu-id="58a9b-107">Une sélection multiple s’étend sur tous les éléments de l’élément d’ancrage à l’élément du signe insertion.</span><span class="sxs-lookup"><span data-stu-id="58a9b-107">A multiple selection spans all items from the anchor item to the caret item.</span></span>

## <a name="parameters"></a><span data-ttu-id="58a9b-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="58a9b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="58a9b-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="58a9b-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="58a9b-110">Non utilisé ; doit être égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="58a9b-110">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="58a9b-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="58a9b-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="58a9b-112">Non utilisé ; doit être égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="58a9b-112">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="58a9b-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="58a9b-113">Return value</span></span>

<span data-ttu-id="58a9b-114">La valeur de retour est l’index de l’élément d’ancrage.</span><span class="sxs-lookup"><span data-stu-id="58a9b-114">The return value is the index of the anchor item.</span></span>

## <a name="requirements"></a><span data-ttu-id="58a9b-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="58a9b-115">Requirements</span></span>



| <span data-ttu-id="58a9b-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="58a9b-116">Requirement</span></span> | <span data-ttu-id="58a9b-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="58a9b-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="58a9b-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="58a9b-118">Minimum supported client</span></span><br/> | <span data-ttu-id="58a9b-119">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="58a9b-119">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="58a9b-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="58a9b-120">Minimum supported server</span></span><br/> | <span data-ttu-id="58a9b-121">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="58a9b-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="58a9b-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="58a9b-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="58a9b-123"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="58a9b-123"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="58a9b-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="58a9b-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="58a9b-125">**\_SETANCHORINDEX lb**</span><span class="sxs-lookup"><span data-stu-id="58a9b-125">**LB\_SETANCHORINDEX**</span></span>](lb-setanchorindex.md)
</dt> </dl>

 

 





