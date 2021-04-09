---
title: Message LB_GETTOPINDEX (winuser. h)
description: Obtient l’index du premier élément visible dans une zone de liste.
ms.assetid: vs|controls|~\controls\listboxes\listboxreference\listboxmessages\lb_gettopindex.htm
keywords:
- LB_GETTOPINDEX les contrôles de message Windows
topic_type:
- apiref
api_name:
- LB_GETTOPINDEX
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bdeca8e3f40ab3105bb9703db9355d09a214f5fc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942165"
---
# <a name="lb_gettopindex-message"></a><span data-ttu-id="04797-104">\_Message GETTOPINDEX lb</span><span class="sxs-lookup"><span data-stu-id="04797-104">LB\_GETTOPINDEX message</span></span>

<span data-ttu-id="04797-105">Obtient l’index du premier élément visible dans une zone de liste.</span><span class="sxs-lookup"><span data-stu-id="04797-105">Gets the index of the first visible item in a list box.</span></span> <span data-ttu-id="04797-106">Initialement, l’élément avec l’index 0 est en haut de la zone de liste, mais si le contenu de la zone de liste a fait l’objet d’un défilement, un autre élément peut se trouver en haut.</span><span class="sxs-lookup"><span data-stu-id="04797-106">Initially the item with index 0 is at the top of the list box, but if the list box contents have been scrolled another item may be at the top.</span></span> <span data-ttu-id="04797-107">Le premier élément visible dans une zone de liste à plusieurs colonnes est l’élément en haut à gauche.</span><span class="sxs-lookup"><span data-stu-id="04797-107">The first visible item in a multiple-column list box is the top-left item.</span></span>

## <a name="parameters"></a><span data-ttu-id="04797-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="04797-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="04797-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="04797-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="04797-110">Non utilisé ; doit être égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="04797-110">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="04797-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="04797-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="04797-112">Non utilisé ; doit être égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="04797-112">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="04797-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="04797-113">Return value</span></span>

<span data-ttu-id="04797-114">La valeur de retour est l’index du premier élément visible dans la zone de liste.</span><span class="sxs-lookup"><span data-stu-id="04797-114">The return value is the index of the first visible item in the list box.</span></span>

## <a name="requirements"></a><span data-ttu-id="04797-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="04797-115">Requirements</span></span>



| <span data-ttu-id="04797-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="04797-116">Requirement</span></span> | <span data-ttu-id="04797-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="04797-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="04797-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="04797-118">Minimum supported client</span></span><br/> | <span data-ttu-id="04797-119">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="04797-119">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="04797-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="04797-120">Minimum supported server</span></span><br/> | <span data-ttu-id="04797-121">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="04797-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="04797-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="04797-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="04797-123"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="04797-123"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="04797-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="04797-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="04797-125">**\_SETTOPINDEX lb**</span><span class="sxs-lookup"><span data-stu-id="04797-125">**LB\_SETTOPINDEX**</span></span>](lb-settopindex.md)
</dt> </dl>

 

 





