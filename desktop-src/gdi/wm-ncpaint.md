---
description: Le \_ message WM NCPAINT est envoyé à une fenêtre quand son frame doit être peint.
ms.assetid: d8a2a8b9-2c5d-484c-be09-67eb33de67c0
title: Message WM_NCPAINT (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6f6c2e211f3dc1602821b0197d295f940606c262
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864317"
---
# <a name="wm_ncpaint-message"></a><span data-ttu-id="0cb22-103">\_Message WM NCPAINT</span><span class="sxs-lookup"><span data-stu-id="0cb22-103">WM\_NCPAINT message</span></span>

<span data-ttu-id="0cb22-104">Le message **WM \_ NCPAINT** est envoyé à une fenêtre quand son frame doit être peint.</span><span class="sxs-lookup"><span data-stu-id="0cb22-104">The **WM\_NCPAINT** message is sent to a window when its frame must be painted.</span></span>

<span data-ttu-id="0cb22-105">Une fenêtre reçoit ce message par le biais de sa fonction [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="0cb22-105">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
LRESULT CALLBACK WindowProc(
  HWND hwnd, 
  UINT  uMsg, 
  WPARAM wParam, 
  LPARAM lParam     
);
```



## <a name="parameters"></a><span data-ttu-id="0cb22-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0cb22-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0cb22-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="0cb22-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0cb22-108">Handle de la région de mise à jour de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="0cb22-108">A handle to the update region of the window.</span></span> <span data-ttu-id="0cb22-109">La région de mise à jour est découpée dans le frame de fenêtre.</span><span class="sxs-lookup"><span data-stu-id="0cb22-109">The update region is clipped to the window frame.</span></span>

</dd> <dt>

<span data-ttu-id="0cb22-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="0cb22-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0cb22-111">Ce paramètre n'est pas utilisé.</span><span class="sxs-lookup"><span data-stu-id="0cb22-111">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0cb22-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="0cb22-112">Return value</span></span>

<span data-ttu-id="0cb22-113">Une application retourne la valeur zéro si elle traite ce message.</span><span class="sxs-lookup"><span data-stu-id="0cb22-113">An application returns zero if it processes this message.</span></span>

## <a name="remarks"></a><span data-ttu-id="0cb22-114">Notes</span><span class="sxs-lookup"><span data-stu-id="0cb22-114">Remarks</span></span>

<span data-ttu-id="0cb22-115">La fonction [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) peint le cadre de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="0cb22-115">The [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function paints the window frame.</span></span>

<span data-ttu-id="0cb22-116">Une application peut intercepter le message **WM \_ NCPAINT** et peindre son propre cadre de fenêtre personnalisé.</span><span class="sxs-lookup"><span data-stu-id="0cb22-116">An application can intercept the **WM\_NCPAINT** message and paint its own custom window frame.</span></span> <span data-ttu-id="0cb22-117">La zone de découpage d’une fenêtre est toujours rectangulaire, même si la forme du cadre est modifiée.</span><span class="sxs-lookup"><span data-stu-id="0cb22-117">The clipping region for a window is always rectangular, even if the shape of the frame is altered.</span></span>

<span data-ttu-id="0cb22-118">La valeur *wParam* peut être passée à [**GetDCEx**](/windows/desktop/api/Winuser/nf-winuser-getdcex) comme dans l’exemple suivant.</span><span class="sxs-lookup"><span data-stu-id="0cb22-118">The *wParam* value can be passed to [**GetDCEx**](/windows/desktop/api/Winuser/nf-winuser-getdcex) as in the following example.</span></span>


```C++
case WM_NCPAINT:
{
    HDC hdc;
    hdc = GetDCEx(hwnd, (HRGN)wParam, DCX_WINDOW|DCX_INTERSECTRGN);
    // Paint into this DC 
    ReleaseDC(hwnd, hdc);
}
```



## <a name="requirements"></a><span data-ttu-id="0cb22-119">Spécifications</span><span class="sxs-lookup"><span data-stu-id="0cb22-119">Requirements</span></span>



| <span data-ttu-id="0cb22-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0cb22-120">Requirement</span></span> | <span data-ttu-id="0cb22-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="0cb22-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0cb22-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0cb22-122">Minimum supported client</span></span><br/> | <span data-ttu-id="0cb22-123">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0cb22-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="0cb22-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0cb22-124">Minimum supported server</span></span><br/> | <span data-ttu-id="0cb22-125">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0cb22-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="0cb22-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="0cb22-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="0cb22-127"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0cb22-127"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0cb22-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0cb22-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0cb22-129">Vue d’ensemble de la peinture et du dessin</span><span class="sxs-lookup"><span data-stu-id="0cb22-129">Painting and Drawing Overview</span></span>](painting-and-drawing.md)
</dt> <dt>

[<span data-ttu-id="0cb22-130">Peinture et dessin de messages</span><span class="sxs-lookup"><span data-stu-id="0cb22-130">Painting and Drawing Messages</span></span>](painting-and-drawing-messages.md)
</dt> <dt>

[<span data-ttu-id="0cb22-131">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="0cb22-131">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[<span data-ttu-id="0cb22-132">**GetWindowDC**</span><span class="sxs-lookup"><span data-stu-id="0cb22-132">**GetWindowDC**</span></span>](/windows/desktop/api/Winuser/nf-winuser-getwindowdc)
</dt> <dt>

[<span data-ttu-id="0cb22-133">**\_peinture WM**</span><span class="sxs-lookup"><span data-stu-id="0cb22-133">**WM\_PAINT**</span></span>](wm-paint.md)
</dt> <dt>

[<span data-ttu-id="0cb22-134">**GetDCEx**</span><span class="sxs-lookup"><span data-stu-id="0cb22-134">**GetDCEx**</span></span>](/windows/desktop/api/Winuser/nf-winuser-getdcex)
</dt> </dl>

 

 
