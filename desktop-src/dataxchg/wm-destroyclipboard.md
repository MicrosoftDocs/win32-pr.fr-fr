---
title: Message WM_DESTROYCLIPBOARD (winuser. h)
description: Envoyé au propriétaire du presse-papiers lorsqu’un appel à la fonction EmptyClipboard vide le presse-papiers. Une fenêtre reçoit ce message par le biais de sa fonction WindowProc.
ms.assetid: 9f75b7fb-e9ae-4876-ba99-7db931b9c2ff
keywords:
- WM_DESTROYCLIPBOARD l’échange de données de message
topic_type:
- apiref
api_name:
- WM_DESTROYCLIPBOARD
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4c3e4b6c2e2d378d0f78cee1824b1e4ce17a433a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942857"
---
# <a name="wm_destroyclipboard-message"></a><span data-ttu-id="7e23c-105">\_Message WM DESTROYCLIPBOARD</span><span class="sxs-lookup"><span data-stu-id="7e23c-105">WM\_DESTROYCLIPBOARD message</span></span>

<span data-ttu-id="7e23c-106">Envoyé au propriétaire du presse-papiers lorsqu’un appel à la fonction [**EmptyClipboard**](/windows/desktop/api/Winuser/nf-winuser-emptyclipboard) vide le presse-papiers.</span><span class="sxs-lookup"><span data-stu-id="7e23c-106">Sent to the clipboard owner when a call to the [**EmptyClipboard**](/windows/desktop/api/Winuser/nf-winuser-emptyclipboard) function empties the clipboard.</span></span>

<span data-ttu-id="7e23c-107">Une fenêtre reçoit ce message par le biais de sa fonction [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="7e23c-107">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_DESTROYCLIPBOARD             0x0307
```



## <a name="parameters"></a><span data-ttu-id="7e23c-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7e23c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7e23c-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="7e23c-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7e23c-110">Ce paramètre n’est pas utilisé et doit être égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="7e23c-110">This parameter is not used and must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="7e23c-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="7e23c-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7e23c-112">Ce paramètre n’est pas utilisé et doit être égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="7e23c-112">This parameter is not used and must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7e23c-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="7e23c-113">Return value</span></span>

<span data-ttu-id="7e23c-114">Si une application traite ce message, elle doit retourner la valeur zéro.</span><span class="sxs-lookup"><span data-stu-id="7e23c-114">If an application processes this message, it should return zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="7e23c-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7e23c-115">Requirements</span></span>



| <span data-ttu-id="7e23c-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7e23c-116">Requirement</span></span> | <span data-ttu-id="7e23c-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="7e23c-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7e23c-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7e23c-118">Minimum supported client</span></span><br/> | <span data-ttu-id="7e23c-119">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7e23c-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="7e23c-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7e23c-120">Minimum supported server</span></span><br/> | <span data-ttu-id="7e23c-121">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7e23c-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="7e23c-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="7e23c-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="7e23c-123"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7e23c-123"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7e23c-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7e23c-124">See also</span></span>

<dl> <dt>

<span data-ttu-id="7e23c-125">**Référence**</span><span class="sxs-lookup"><span data-stu-id="7e23c-125">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="7e23c-126">**EmptyClipboard**</span><span class="sxs-lookup"><span data-stu-id="7e23c-126">**EmptyClipboard**</span></span>](/windows/desktop/api/Winuser/nf-winuser-emptyclipboard)
</dt> <dt>

<span data-ttu-id="7e23c-127">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="7e23c-127">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="7e23c-128">Presse-papiers</span><span class="sxs-lookup"><span data-stu-id="7e23c-128">Clipboard</span></span>](clipboard.md)
</dt> </dl>

 

