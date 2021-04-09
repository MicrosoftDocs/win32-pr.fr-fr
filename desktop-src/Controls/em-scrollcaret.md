---
title: Message EM_SCROLLCARET (winuser. h)
description: Fait défiler le signe insertion dans un contrôle d’édition. Vous pouvez envoyer ce message à un contrôle d’édition ou à un contrôle d’édition enrichi.
ms.assetid: 7a33034d-9369-49f8-a881-0c1d2cedff6a
keywords:
- EM_SCROLLCARET les contrôles de message Windows
topic_type:
- apiref
api_name:
- EM_SCROLLCARET
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: faa9f4bd69605f5e8fad36a683c9be2894546cb0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106264"
---
# <a name="em_scrollcaret-message"></a><span data-ttu-id="4e641-105">\_Message SCROLLCARET em</span><span class="sxs-lookup"><span data-stu-id="4e641-105">EM\_SCROLLCARET message</span></span>

<span data-ttu-id="4e641-106">Fait défiler le signe insertion dans un contrôle d’édition.</span><span class="sxs-lookup"><span data-stu-id="4e641-106">Scrolls the caret into view in an edit control.</span></span> <span data-ttu-id="4e641-107">Vous pouvez envoyer ce message à un contrôle d’édition ou à un contrôle d’édition enrichi.</span><span class="sxs-lookup"><span data-stu-id="4e641-107">You can send this message to either an edit control or a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="4e641-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4e641-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4e641-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="4e641-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4e641-110">Ce paramètre est réservé.</span><span class="sxs-lookup"><span data-stu-id="4e641-110">This parameter is reserved.</span></span> <span data-ttu-id="4e641-111">Elle doit être définie sur zéro.</span><span class="sxs-lookup"><span data-stu-id="4e641-111">It should be set to zero.</span></span>

</dd> <dt>

<span data-ttu-id="4e641-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="4e641-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4e641-113">Ce paramètre est réservé.</span><span class="sxs-lookup"><span data-stu-id="4e641-113">This parameter is reserved.</span></span> <span data-ttu-id="4e641-114">Elle doit être définie sur zéro.</span><span class="sxs-lookup"><span data-stu-id="4e641-114">It should be set to zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4e641-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="4e641-115">Return value</span></span>

<span data-ttu-id="4e641-116">La valeur de retour n’est pas significative.</span><span class="sxs-lookup"><span data-stu-id="4e641-116">The return value is not meaningful.</span></span>

## <a name="remarks"></a><span data-ttu-id="4e641-117">Notes</span><span class="sxs-lookup"><span data-stu-id="4e641-117">Remarks</span></span>

<span data-ttu-id="4e641-118">**Modification riche :** Pris en charge dans Microsoft Rich Edit 1,0 et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="4e641-118">**Rich Edit:** Supported in Microsoft Rich Edit 1.0 and later.</span></span> <span data-ttu-id="4e641-119">Pour plus d’informations sur la compatibilité des versions RichEdit avec les différentes versions du système, consultez [à propos des contrôles](about-rich-edit-controls.md)RichEdit.</span><span class="sxs-lookup"><span data-stu-id="4e641-119">For information about the compatibility of rich edit versions with the various system versions, see [About Rich Edit Controls](about-rich-edit-controls.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="4e641-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4e641-120">Requirements</span></span>



| <span data-ttu-id="4e641-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4e641-121">Requirement</span></span> | <span data-ttu-id="4e641-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="4e641-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4e641-123">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4e641-123">Minimum supported client</span></span><br/> | <span data-ttu-id="4e641-124">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4e641-124">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="4e641-125">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4e641-125">Minimum supported server</span></span><br/> | <span data-ttu-id="4e641-126">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4e641-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="4e641-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="4e641-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="4e641-128"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4e641-128"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4e641-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4e641-129">See also</span></span>

<dl> <dt>

<span data-ttu-id="4e641-130">**Référence**</span><span class="sxs-lookup"><span data-stu-id="4e641-130">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="4e641-131">**\_LINESCROLL em**</span><span class="sxs-lookup"><span data-stu-id="4e641-131">**EM\_LINESCROLL**</span></span>](em-linescroll.md)
</dt> <dt>

[<span data-ttu-id="4e641-132">**\_défilement em**</span><span class="sxs-lookup"><span data-stu-id="4e641-132">**EM\_SCROLL**</span></span>](em-scroll.md)
</dt> <dt>

[<span data-ttu-id="4e641-133">**\_VSCROLL WM**</span><span class="sxs-lookup"><span data-stu-id="4e641-133">**WM\_VSCROLL**</span></span>](wm-vscroll.md)
</dt> </dl>

 

 





