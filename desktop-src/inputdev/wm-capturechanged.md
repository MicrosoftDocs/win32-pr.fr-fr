---
title: Message WM_CAPTURECHANGED (winuser. h)
description: Envoyé à la fenêtre qui perd la capture de la souris.
ms.assetid: 79c8f65e-31fa-4bdb-9e88-0160a52b5b7d
keywords:
- WM_CAPTURECHANGED l’entrée du clavier et de la souris du message
topic_type:
- apiref
api_name:
- WM_CAPTURECHANGED
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 050bc00a7ab19e22e0fe4ea1f35271707180d4d4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103405"
---
# <a name="wm_capturechanged-message"></a><span data-ttu-id="208fc-104">\_Message WM CAPTURECHANGED</span><span class="sxs-lookup"><span data-stu-id="208fc-104">WM\_CAPTURECHANGED message</span></span>

<span data-ttu-id="208fc-105">Envoyé à la fenêtre qui perd la capture de la souris.</span><span class="sxs-lookup"><span data-stu-id="208fc-105">Sent to the window that is losing the mouse capture.</span></span>

<span data-ttu-id="208fc-106">Une fenêtre reçoit ce message par le biais de sa fonction [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="208fc-106">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_CAPTURECHANGED               0x0215
```



## <a name="parameters"></a><span data-ttu-id="208fc-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="208fc-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="208fc-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="208fc-108">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="208fc-109">Ce paramètre n'est pas utilisé.</span><span class="sxs-lookup"><span data-stu-id="208fc-109">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="208fc-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="208fc-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="208fc-111">Handle de la fenêtre qui obtient la capture de la souris.</span><span class="sxs-lookup"><span data-stu-id="208fc-111">A handle to the window gaining the mouse capture.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="208fc-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="208fc-112">Return value</span></span>

<span data-ttu-id="208fc-113">Une application doit retourner zéro si elle traite ce message.</span><span class="sxs-lookup"><span data-stu-id="208fc-113">An application should return zero if it processes this message.</span></span>

## <a name="remarks"></a><span data-ttu-id="208fc-114">Notes</span><span class="sxs-lookup"><span data-stu-id="208fc-114">Remarks</span></span>

<span data-ttu-id="208fc-115">Une fenêtre reçoit ce message même s’il appelle [**ReleaseCapture**](/windows/win32/api/winuser/nf-winuser-releasecapture) lui-même.</span><span class="sxs-lookup"><span data-stu-id="208fc-115">A window receives this message even if it calls [**ReleaseCapture**](/windows/win32/api/winuser/nf-winuser-releasecapture) itself.</span></span> <span data-ttu-id="208fc-116">Une application ne doit pas tenter de définir la capture de la souris en réponse à ce message.</span><span class="sxs-lookup"><span data-stu-id="208fc-116">An application should not attempt to set the mouse capture in response to this message.</span></span>

<span data-ttu-id="208fc-117">Lorsqu’il reçoit ce message, une fenêtre doit se redessiner, si nécessaire, pour refléter le nouvel état de la capture de la souris.</span><span class="sxs-lookup"><span data-stu-id="208fc-117">When it receives this message, a window should redraw itself, if necessary, to reflect the new mouse-capture state.</span></span>

## <a name="requirements"></a><span data-ttu-id="208fc-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="208fc-118">Requirements</span></span>



| <span data-ttu-id="208fc-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="208fc-119">Requirement</span></span> | <span data-ttu-id="208fc-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="208fc-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="208fc-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="208fc-121">Minimum supported client</span></span><br/> | <span data-ttu-id="208fc-122">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="208fc-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="208fc-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="208fc-123">Minimum supported server</span></span><br/> | <span data-ttu-id="208fc-124">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="208fc-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="208fc-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="208fc-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="208fc-126"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="208fc-126"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="208fc-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="208fc-127">See also</span></span>

<dl> <dt>

<span data-ttu-id="208fc-128">**Référence**</span><span class="sxs-lookup"><span data-stu-id="208fc-128">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="208fc-129">**ReleaseCapture**</span><span class="sxs-lookup"><span data-stu-id="208fc-129">**ReleaseCapture**</span></span>](/windows/win32/api/winuser/nf-winuser-releasecapture)
</dt> <dt>

[<span data-ttu-id="208fc-130">**SetCapture**</span><span class="sxs-lookup"><span data-stu-id="208fc-130">**SetCapture**</span></span>](/windows/win32/api/winuser/nf-winuser-setcapture)
</dt> <dt>

<span data-ttu-id="208fc-131">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="208fc-131">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="208fc-132">Entrée de la souris</span><span class="sxs-lookup"><span data-stu-id="208fc-132">Mouse Input</span></span>](mouse-input.md)
</dt> </dl>

 

