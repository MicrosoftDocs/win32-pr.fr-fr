---
title: Message CB_GETHORIZONTALEXTENT (winuser. h)
description: Obtient la largeur, en pixels, que peut faire défiler la zone de liste horizontalement (largeur avec défilement). Cela s’applique uniquement si la zone de liste comporte une barre de défilement horizontale.
ms.assetid: 7c9fff88-2750-4c94-b7f6-6bdd81c224e9
keywords:
- CB_GETHORIZONTALEXTENT les contrôles de message Windows
topic_type:
- apiref
api_name:
- CB_GETHORIZONTALEXTENT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a2b1fb7c8fe7549360801516364528c9a2ef1f1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032855"
---
# <a name="cb_gethorizontalextent-message"></a><span data-ttu-id="1de6e-105">\_Message GETHORIZONTALEXTENT CB</span><span class="sxs-lookup"><span data-stu-id="1de6e-105">CB\_GETHORIZONTALEXTENT message</span></span>

<span data-ttu-id="1de6e-106">Obtient la largeur, en pixels, que peut faire défiler la zone de liste horizontalement (largeur avec défilement).</span><span class="sxs-lookup"><span data-stu-id="1de6e-106">Gets the width, in pixels, that the list box can be scrolled horizontally (the scrollable width).</span></span> <span data-ttu-id="1de6e-107">Cela s’applique uniquement si la zone de liste comporte une barre de défilement horizontale.</span><span class="sxs-lookup"><span data-stu-id="1de6e-107">This is applicable only if the list box has a horizontal scroll bar.</span></span>

## <a name="parameters"></a><span data-ttu-id="1de6e-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1de6e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1de6e-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="1de6e-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1de6e-110">Non utilisé ; doit être égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="1de6e-110">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="1de6e-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="1de6e-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1de6e-112">Non utilisé ; doit être égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="1de6e-112">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1de6e-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="1de6e-113">Return value</span></span>

<span data-ttu-id="1de6e-114">La valeur de retour est la largeur de défilement, en pixels.</span><span class="sxs-lookup"><span data-stu-id="1de6e-114">The return value is the scrollable width, in pixels.</span></span>

## <a name="requirements"></a><span data-ttu-id="1de6e-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1de6e-115">Requirements</span></span>



| <span data-ttu-id="1de6e-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1de6e-116">Requirement</span></span> | <span data-ttu-id="1de6e-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="1de6e-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1de6e-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1de6e-118">Minimum supported client</span></span><br/> | <span data-ttu-id="1de6e-119">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1de6e-119">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="1de6e-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1de6e-120">Minimum supported server</span></span><br/> | <span data-ttu-id="1de6e-121">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1de6e-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="1de6e-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="1de6e-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="1de6e-123"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1de6e-123"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1de6e-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1de6e-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1de6e-125">**\_SETHORIZONTALEXTENT CB**</span><span class="sxs-lookup"><span data-stu-id="1de6e-125">**CB\_SETHORIZONTALEXTENT**</span></span>](cb-sethorizontalextent.md)
</dt> </dl>

 

 





