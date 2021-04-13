---
title: Message WM_NCRBUTTONUP (winuser. h)
description: Publié lorsque l’utilisateur relâche le bouton droit de la souris alors que le curseur se trouve dans la zone non cliente d’une fenêtre. Ce message est publié dans la fenêtre qui contient le curseur. Si une fenêtre a capturé la souris, ce message n’est pas publié.
ms.assetid: dc77c235-9e57-4051-b197-bd7ee7535a6f
keywords:
- WM_NCRBUTTONUP l’entrée du clavier et de la souris du message
topic_type:
- apiref
api_name:
- WM_NCRBUTTONUP
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b5fb977e442b2af312f9267576c622ddd35022fd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466134"
---
# <a name="wm_ncrbuttonup-message"></a><span data-ttu-id="c4200-106">\_Message WM NCRBUTTONUP</span><span class="sxs-lookup"><span data-stu-id="c4200-106">WM\_NCRBUTTONUP message</span></span>

<span data-ttu-id="c4200-107">Publié lorsque l’utilisateur relâche le bouton droit de la souris alors que le curseur se trouve dans la zone non cliente d’une fenêtre.</span><span class="sxs-lookup"><span data-stu-id="c4200-107">Posted when the user releases the right mouse button while the cursor is within the nonclient area of a window.</span></span> <span data-ttu-id="c4200-108">Ce message est publié dans la fenêtre qui contient le curseur.</span><span class="sxs-lookup"><span data-stu-id="c4200-108">This message is posted to the window that contains the cursor.</span></span> <span data-ttu-id="c4200-109">Si une fenêtre a capturé la souris, ce message n’est pas publié.</span><span class="sxs-lookup"><span data-stu-id="c4200-109">If a window has captured the mouse, this message is not posted.</span></span>

<span data-ttu-id="c4200-110">Une fenêtre reçoit ce message par le biais de sa fonction [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="c4200-110">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_NCRBUTTONUP                  0x00A5
```



## <a name="parameters"></a><span data-ttu-id="c4200-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c4200-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c4200-112">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c4200-112">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c4200-113">Valeur du test de positionnement retournée par la fonction [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) suite au traitement du message [**WM \_ NCHITTEST**](wm-nchittest.md) .</span><span class="sxs-lookup"><span data-stu-id="c4200-113">The hit-test value returned by the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function as a result of processing the [**WM\_NCHITTEST**](wm-nchittest.md) message.</span></span> <span data-ttu-id="c4200-114">Pour obtenir la liste des valeurs de test de positionnement, consultez **WM \_ NCHITTEST**.</span><span class="sxs-lookup"><span data-stu-id="c4200-114">For a list of hit-test values, see **WM\_NCHITTEST**.</span></span>

</dd> <dt>

<span data-ttu-id="c4200-115">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c4200-115">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c4200-116">Structure de [**points**](/previous-versions//dd162808(v=vs.85)) qui contient les coordonnées x et y du curseur.</span><span class="sxs-lookup"><span data-stu-id="c4200-116">A [**POINTS**](/previous-versions//dd162808(v=vs.85)) structure that contains the x- and y-coordinates of the cursor.</span></span> <span data-ttu-id="c4200-117">Les coordonnées sont relatives à l’angle supérieur gauche de l’écran.</span><span class="sxs-lookup"><span data-stu-id="c4200-117">The coordinates are relative to the upper-left corner of the screen.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c4200-118">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="c4200-118">Return value</span></span>

<span data-ttu-id="c4200-119">Si une application traite ce message, elle doit retourner la valeur zéro.</span><span class="sxs-lookup"><span data-stu-id="c4200-119">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="c4200-120">Notes</span><span class="sxs-lookup"><span data-stu-id="c4200-120">Remarks</span></span>

<span data-ttu-id="c4200-121">Vous pouvez également utiliser les macros [**obten \_ x \_ lParam**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) et [**obten \_ Y \_ lParam**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) pour extraire les valeurs des coordonnées x et y de *lParam*.</span><span class="sxs-lookup"><span data-stu-id="c4200-121">You can also use the [**GET\_X\_LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) and [**GET\_Y\_LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) macros to extract the values of the x- and y- coordinates from *lParam*.</span></span>


```
xPos = GET_X_LPARAM(lParam); 
yPos = GET_Y_LPARAM(lParam); 
```



> [!IMPORTANT]
> <span data-ttu-id="c4200-122">N’utilisez pas les macros [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) ou [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) pour extraire les coordonnées x et y de la position du curseur, car ces macros renvoient des résultats incorrects sur les systèmes avec plusieurs moniteurs.</span><span class="sxs-lookup"><span data-stu-id="c4200-122">Do not use the [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) or [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) macros to extract the x- and y- coordinates of the cursor position because these macros return incorrect results on systems with multiple monitors.</span></span> <span data-ttu-id="c4200-123">Les systèmes avec plusieurs moniteurs peuvent avoir des coordonnées x et y négatives, et **LOWORD** et **HIWORD** traitent les coordonnées comme des quantités non signées.</span><span class="sxs-lookup"><span data-stu-id="c4200-123">Systems with multiple monitors can have negative x- and y- coordinates, and **LOWORD** and **HIWORD** treat the coordinates as unsigned quantities.</span></span>

 

<span data-ttu-id="c4200-124">Si c’est le cas, le système envoie le message [**WM \_ SYSCOMMAND**](/windows/desktop/menurc/wm-syscommand) à la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="c4200-124">If it is appropriate to do so, the system sends the [**WM\_SYSCOMMAND**](/windows/desktop/menurc/wm-syscommand) message to the window.</span></span>

## <a name="requirements"></a><span data-ttu-id="c4200-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c4200-125">Requirements</span></span>



| <span data-ttu-id="c4200-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c4200-126">Requirement</span></span> | <span data-ttu-id="c4200-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="c4200-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c4200-128">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c4200-128">Minimum supported client</span></span><br/> | <span data-ttu-id="c4200-129">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c4200-129">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="c4200-130">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c4200-130">Minimum supported server</span></span><br/> | <span data-ttu-id="c4200-131">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c4200-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="c4200-132">En-tête</span><span class="sxs-lookup"><span data-stu-id="c4200-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="c4200-133"><dt>Winuser. h (inclure Windowsx. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c4200-133"><dt>Winuser.h (include Windowsx.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c4200-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c4200-134">See also</span></span>

<dl> <dt>

<span data-ttu-id="c4200-135">**Référence**</span><span class="sxs-lookup"><span data-stu-id="c4200-135">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="c4200-136">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="c4200-136">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[<span data-ttu-id="c4200-137">**Obtient \_ X \_ lParam**</span><span class="sxs-lookup"><span data-stu-id="c4200-137">**GET\_X\_LPARAM**</span></span>](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam)
</dt> <dt>

[<span data-ttu-id="c4200-138">**Obtient \_ le \_ lParam Y**</span><span class="sxs-lookup"><span data-stu-id="c4200-138">**GET\_Y\_LPARAM**</span></span>](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam)
</dt> <dt>

[<span data-ttu-id="c4200-139">**\_NCHITTEST WM**</span><span class="sxs-lookup"><span data-stu-id="c4200-139">**WM\_NCHITTEST**</span></span>](wm-nchittest.md)
</dt> <dt>

[<span data-ttu-id="c4200-140">**\_NCRBUTTONDBLCLK WM**</span><span class="sxs-lookup"><span data-stu-id="c4200-140">**WM\_NCRBUTTONDBLCLK**</span></span>](wm-ncrbuttondblclk.md)
</dt> <dt>

[<span data-ttu-id="c4200-141">**\_NCRBUTTONDOWN WM**</span><span class="sxs-lookup"><span data-stu-id="c4200-141">**WM\_NCRBUTTONDOWN**</span></span>](wm-ncrbuttondown.md)
</dt> <dt>

[<span data-ttu-id="c4200-142">**\_SYSCOMMAND WM**</span><span class="sxs-lookup"><span data-stu-id="c4200-142">**WM\_SYSCOMMAND**</span></span>](/windows/desktop/menurc/wm-syscommand)
</dt> <dt>

<span data-ttu-id="c4200-143">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="c4200-143">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="c4200-144">Entrée de la souris</span><span class="sxs-lookup"><span data-stu-id="c4200-144">Mouse Input</span></span>](mouse-input.md)
</dt> <dt>

<span data-ttu-id="c4200-145">**Autres ressources**</span><span class="sxs-lookup"><span data-stu-id="c4200-145">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="c4200-146">**MAKEPOINTS**</span><span class="sxs-lookup"><span data-stu-id="c4200-146">**MAKEPOINTS**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-makepoints)
</dt> <dt>

<span data-ttu-id="c4200-147">[**MOMENTS**](/previous-versions//dd162808(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="c4200-147">[**POINTS**](/previous-versions//dd162808(v=vs.85))</span></span>
</dt> </dl>

 

