---
title: Message WM_MOUSELEAVE (winuser. h)
description: Publié dans une fenêtre lorsque le curseur quitte la zone cliente de la fenêtre spécifiée dans un appel antérieur à TrackMouseEvent.
ms.assetid: b23d24ff-531a-4b6d-8848-f82ac5568995
keywords:
- WM_MOUSELEAVE l’entrée du clavier et de la souris du message
topic_type:
- apiref
api_name:
- WM_MOUSELEAVE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7dc96022e94df7f518b21b1c9a46895fc9204b08
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464926"
---
# <a name="wm_mouseleave-message"></a><span data-ttu-id="07616-104">\_Message WM MOUSELEAVE</span><span class="sxs-lookup"><span data-stu-id="07616-104">WM\_MOUSELEAVE message</span></span>

<span data-ttu-id="07616-105">Publié dans une fenêtre lorsque le curseur quitte la zone cliente de la fenêtre spécifiée dans un appel antérieur à [**TrackMouseEvent**](/windows/win32/api/winuser/nf-winuser-trackmouseevent).</span><span class="sxs-lookup"><span data-stu-id="07616-105">Posted to a window when the cursor leaves the client area of the window specified in a prior call to [**TrackMouseEvent**](/windows/win32/api/winuser/nf-winuser-trackmouseevent).</span></span>

<span data-ttu-id="07616-106">Une fenêtre reçoit ce message par le biais de sa fonction [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="07616-106">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_MOUSELEAVE                   0x02A3
```



## <a name="parameters"></a><span data-ttu-id="07616-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="07616-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="07616-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="07616-108">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="07616-109">Ce paramètre n’est pas utilisé et doit être égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="07616-109">This parameter is not used and must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="07616-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="07616-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="07616-111">Ce paramètre n’est pas utilisé et doit être égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="07616-111">This parameter is not used and must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="07616-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="07616-112">Return value</span></span>

<span data-ttu-id="07616-113">Si une application traite ce message, elle doit retourner la valeur zéro.</span><span class="sxs-lookup"><span data-stu-id="07616-113">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="07616-114">Notes</span><span class="sxs-lookup"><span data-stu-id="07616-114">Remarks</span></span>

<span data-ttu-id="07616-115">Tout le suivi demandé par [**TrackMouseEvent**](/windows/win32/api/winuser/nf-winuser-trackmouseevent) est annulé lorsque ce message est généré.</span><span class="sxs-lookup"><span data-stu-id="07616-115">All tracking requested by [**TrackMouseEvent**](/windows/win32/api/winuser/nf-winuser-trackmouseevent) is canceled when this message is generated.</span></span> <span data-ttu-id="07616-116">L’application doit appeler **TrackMouseEvent** quand la souris entre à nouveau dans sa fenêtre si elle nécessite un suivi supplémentaire du comportement de pointage de la souris.</span><span class="sxs-lookup"><span data-stu-id="07616-116">The application must call **TrackMouseEvent** when the mouse reenters its window if it requires further tracking of mouse hover behavior.</span></span>

## <a name="requirements"></a><span data-ttu-id="07616-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="07616-117">Requirements</span></span>



| <span data-ttu-id="07616-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="07616-118">Requirement</span></span> | <span data-ttu-id="07616-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="07616-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="07616-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="07616-120">Minimum supported client</span></span><br/> | <span data-ttu-id="07616-121">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="07616-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="07616-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="07616-122">Minimum supported server</span></span><br/> | <span data-ttu-id="07616-123">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="07616-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="07616-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="07616-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="07616-125"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="07616-125"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="07616-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="07616-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="07616-127">**Référence**</span><span class="sxs-lookup"><span data-stu-id="07616-127">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="07616-128">**GetCapture**</span><span class="sxs-lookup"><span data-stu-id="07616-128">**GetCapture**</span></span>](/windows/win32/api/winuser/nf-winuser-getcapture)
</dt> <dt>

[<span data-ttu-id="07616-129">**SetCapture**</span><span class="sxs-lookup"><span data-stu-id="07616-129">**SetCapture**</span></span>](/windows/win32/api/winuser/nf-winuser-setcapture)
</dt> <dt>

[<span data-ttu-id="07616-130">**TrackMouseEvent**</span><span class="sxs-lookup"><span data-stu-id="07616-130">**TrackMouseEvent**</span></span>](/windows/win32/api/winuser/nf-winuser-trackmouseevent)
</dt> <dt>

[<span data-ttu-id="07616-131">**TRACKMOUSEEVENT**</span><span class="sxs-lookup"><span data-stu-id="07616-131">**TRACKMOUSEEVENT**</span></span>](/windows/win32/api/winuser/ns-winuser-trackmouseevent)
</dt> <dt>

[<span data-ttu-id="07616-132">**\_NCMOUSELEAVE WM**</span><span class="sxs-lookup"><span data-stu-id="07616-132">**WM\_NCMOUSELEAVE**</span></span>](wm-ncmouseleave.md)
</dt> <dt>

<span data-ttu-id="07616-133">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="07616-133">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="07616-134">Entrée de la souris</span><span class="sxs-lookup"><span data-stu-id="07616-134">Mouse Input</span></span>](mouse-input.md)
</dt> </dl>

 

