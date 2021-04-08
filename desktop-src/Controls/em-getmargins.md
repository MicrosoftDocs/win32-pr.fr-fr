---
title: Message EM_GETMARGINS (winuser. h)
description: Obtient les largeurs des marges gauche et droite d’un contrôle d’édition.
ms.assetid: 2482354b-aae0-4abd-8287-65c423f30abb
keywords:
- EM_GETMARGINS les contrôles de message Windows
topic_type:
- apiref
api_name:
- EM_GETMARGINS
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 239ad7e7888f5bceef60bf2719c3b67798b56220
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740300"
---
# <a name="em_getmargins-message"></a><span data-ttu-id="e3dab-104">\_Message GETMARGINS em</span><span class="sxs-lookup"><span data-stu-id="e3dab-104">EM\_GETMARGINS message</span></span>

<span data-ttu-id="e3dab-105">Obtient les largeurs des marges gauche et droite d’un contrôle d’édition.</span><span class="sxs-lookup"><span data-stu-id="e3dab-105">Gets the widths of the left and right margins for an edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="e3dab-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e3dab-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e3dab-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="e3dab-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e3dab-108">Non utilisé ; doit être égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="e3dab-108">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="e3dab-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e3dab-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e3dab-110">Non utilisé ; doit être égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="e3dab-110">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e3dab-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="e3dab-111">Return value</span></span>

<span data-ttu-id="e3dab-112">Retourne la largeur de la marge de gauche dans le LOWORD et la largeur de la marge droite dans le HIWORD.</span><span class="sxs-lookup"><span data-stu-id="e3dab-112">Returns the width of the left margin in the LOWORD, and the width of the right margin in the HIWORD.</span></span>

## <a name="remarks"></a><span data-ttu-id="e3dab-113">Notes</span><span class="sxs-lookup"><span data-stu-id="e3dab-113">Remarks</span></span>

<span data-ttu-id="e3dab-114">**Modification riche :** Le **message \_ GETMARGINS em** n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="e3dab-114">**Rich Edit:** The **EM\_GETMARGINS** message is not supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="e3dab-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e3dab-115">Requirements</span></span>



| <span data-ttu-id="e3dab-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e3dab-116">Requirement</span></span> | <span data-ttu-id="e3dab-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="e3dab-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e3dab-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e3dab-118">Minimum supported client</span></span><br/> | <span data-ttu-id="e3dab-119">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e3dab-119">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="e3dab-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e3dab-120">Minimum supported server</span></span><br/> | <span data-ttu-id="e3dab-121">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e3dab-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="e3dab-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="e3dab-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="e3dab-123"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e3dab-123"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e3dab-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e3dab-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e3dab-125">**\_setMargins em**</span><span class="sxs-lookup"><span data-stu-id="e3dab-125">**EM\_SETMARGINS**</span></span>](em-setmargins.md)
</dt> </dl>

 

 





