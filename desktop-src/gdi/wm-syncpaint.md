---
description: Le \_ message WM SYNCPAINT est utilisé pour synchroniser la peinture tout en évitant la liaison de threads GUI indépendants.
ms.assetid: 4446be4e-e0b9-46ce-95b2-bea876348c25
title: Message WM_SYNCPAINT (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5602e867af9b7ce467e8979c9f341758414ad287
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104991497"
---
# <a name="wm_syncpaint-message"></a><span data-ttu-id="17c1d-103">\_Message WM SYNCPAINT</span><span class="sxs-lookup"><span data-stu-id="17c1d-103">WM\_SYNCPAINT message</span></span>

<span data-ttu-id="17c1d-104">Le message **WM \_ SYNCPAINT** est utilisé pour synchroniser la peinture tout en évitant la liaison de threads GUI indépendants.</span><span class="sxs-lookup"><span data-stu-id="17c1d-104">The **WM\_SYNCPAINT** message is used to synchronize painting while avoiding linking independent GUI threads.</span></span>

<span data-ttu-id="17c1d-105">Une fenêtre reçoit ce message par le biais de sa fonction [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="17c1d-105">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
LRESULT CALLBACK WindowProc(
  HWND hwnd, 
  UINT  uMsg, 
  WPARAM wParam, 
  LPARAM lParam     
);
```



## <a name="parameters"></a><span data-ttu-id="17c1d-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="17c1d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="17c1d-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="17c1d-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="17c1d-108">Ce paramètre n'est pas utilisé.</span><span class="sxs-lookup"><span data-stu-id="17c1d-108">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="17c1d-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="17c1d-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="17c1d-110">Ce paramètre n'est pas utilisé.</span><span class="sxs-lookup"><span data-stu-id="17c1d-110">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="17c1d-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="17c1d-111">Return value</span></span>

<span data-ttu-id="17c1d-112">Une application retourne la valeur zéro si elle traite ce message.</span><span class="sxs-lookup"><span data-stu-id="17c1d-112">An application returns zero if it processes this message.</span></span>

## <a name="remarks"></a><span data-ttu-id="17c1d-113">Notes</span><span class="sxs-lookup"><span data-stu-id="17c1d-113">Remarks</span></span>

<span data-ttu-id="17c1d-114">Quand une fenêtre a été masquée, affichée, déplacée ou dimensionnée, le système peut déterminer qu’il est nécessaire d’envoyer un message **WM \_ SYNCPAINT** aux fenêtres de niveau supérieur d’autres threads.</span><span class="sxs-lookup"><span data-stu-id="17c1d-114">When a window has been hidden, shown, moved, or sized, the system may determine that it is necessary to send a **WM\_SYNCPAINT** message to the top-level windows of other threads.</span></span> <span data-ttu-id="17c1d-115">Les applications doivent transmettre **WM \_ SYNCPAINT** à [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)  pour traitement.</span><span class="sxs-lookup"><span data-stu-id="17c1d-115">Applications must pass **WM\_SYNCPAINT** to [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)  for processing.</span></span> <span data-ttu-id="17c1d-116">La fonction **DefWindowProc** envoie un message [**WM \_ NCPAINT**](wm-ncpaint.md) à la procédure de fenêtre si le frame de fenêtre doit être peint et envoie un message [**WM \_ ERASEBKGND**](../winmsg/wm-erasebkgnd.md) si l’arrière-plan de la fenêtre doit être effacé.</span><span class="sxs-lookup"><span data-stu-id="17c1d-116">The **DefWindowProc** function will send a [**WM\_NCPAINT**](wm-ncpaint.md) message to the window procedure if the window frame must be painted and send a [**WM\_ERASEBKGND**](../winmsg/wm-erasebkgnd.md) message if the window background must be erased.</span></span>

## <a name="requirements"></a><span data-ttu-id="17c1d-117">Spécifications</span><span class="sxs-lookup"><span data-stu-id="17c1d-117">Requirements</span></span>



| <span data-ttu-id="17c1d-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="17c1d-118">Requirement</span></span> | <span data-ttu-id="17c1d-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="17c1d-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="17c1d-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="17c1d-120">Minimum supported client</span></span><br/> | <span data-ttu-id="17c1d-121">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="17c1d-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="17c1d-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="17c1d-122">Minimum supported server</span></span><br/> | <span data-ttu-id="17c1d-123">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="17c1d-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="17c1d-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="17c1d-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="17c1d-125"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="17c1d-125"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="17c1d-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="17c1d-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="17c1d-127">Vue d’ensemble de la peinture et du dessin</span><span class="sxs-lookup"><span data-stu-id="17c1d-127">Painting and Drawing Overview</span></span>](painting-and-drawing.md)
</dt> <dt>

[<span data-ttu-id="17c1d-128">Peinture et dessin de messages</span><span class="sxs-lookup"><span data-stu-id="17c1d-128">Painting and Drawing Messages</span></span>](painting-and-drawing-messages.md)
</dt> <dt>

[<span data-ttu-id="17c1d-129">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="17c1d-129">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[<span data-ttu-id="17c1d-130">**GetDCEx**</span><span class="sxs-lookup"><span data-stu-id="17c1d-130">**GetDCEx**</span></span>](/windows/desktop/api/Winuser/nf-winuser-getdcex)
</dt> <dt>

[<span data-ttu-id="17c1d-131">**GetWindowDC**</span><span class="sxs-lookup"><span data-stu-id="17c1d-131">**GetWindowDC**</span></span>](/windows/desktop/api/Winuser/nf-winuser-getwindowdc)
</dt> <dt>

[<span data-ttu-id="17c1d-132">**\_peinture WM**</span><span class="sxs-lookup"><span data-stu-id="17c1d-132">**WM\_PAINT**</span></span>](wm-paint.md)
</dt> </dl>

 

 
