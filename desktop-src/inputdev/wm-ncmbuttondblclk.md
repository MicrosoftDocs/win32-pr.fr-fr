---
title: Message WM_NCMBUTTONDBLCLK (winuser. h)
description: Publié lorsque l’utilisateur double-clique sur le bouton central de la souris lorsque le curseur se trouve dans la zone non cliente d’une fenêtre. Ce message est publié dans la fenêtre qui contient le curseur. Si une fenêtre a capturé la souris, ce message n’est pas publié.
ms.assetid: 7c0f8d6e-eb37-4873-a3f8-777e8b0b22bc
keywords:
- WM_NCMBUTTONDBLCLK l’entrée du clavier et de la souris du message
topic_type:
- apiref
api_name:
- WM_NCMBUTTONDBLCLK
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 612a0a7ca0a5731691ec244df505e3d058216e2f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741068"
---
# <a name="wm_ncmbuttondblclk-message"></a><span data-ttu-id="3af33-106">\_Message WM NCMBUTTONDBLCLK</span><span class="sxs-lookup"><span data-stu-id="3af33-106">WM\_NCMBUTTONDBLCLK message</span></span>

<span data-ttu-id="3af33-107">Publié lorsque l’utilisateur double-clique sur le bouton central de la souris lorsque le curseur se trouve dans la zone non cliente d’une fenêtre.</span><span class="sxs-lookup"><span data-stu-id="3af33-107">Posted when the user double-clicks the middle mouse button while the cursor is within the nonclient area of a window.</span></span> <span data-ttu-id="3af33-108">Ce message est publié dans la fenêtre qui contient le curseur.</span><span class="sxs-lookup"><span data-stu-id="3af33-108">This message is posted to the window that contains the cursor.</span></span> <span data-ttu-id="3af33-109">Si une fenêtre a capturé la souris, ce message n’est pas publié.</span><span class="sxs-lookup"><span data-stu-id="3af33-109">If a window has captured the mouse, this message is not posted.</span></span>

<span data-ttu-id="3af33-110">Une fenêtre reçoit ce message par le biais de sa fonction [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="3af33-110">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_NCMBUTTONDBLCLK              0x00A9
```



## <a name="parameters"></a><span data-ttu-id="3af33-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3af33-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3af33-112">*wParam*</span><span class="sxs-lookup"><span data-stu-id="3af33-112">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3af33-113">Valeur du test de positionnement retournée par la fonction [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) suite au traitement du message [**WM \_ NCHITTEST**](wm-nchittest.md) .</span><span class="sxs-lookup"><span data-stu-id="3af33-113">The hit-test value returned by the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function as a result of processing the [**WM\_NCHITTEST**](wm-nchittest.md) message.</span></span> <span data-ttu-id="3af33-114">Pour obtenir la liste des valeurs de test de positionnement, consultez **WM \_ NCHITTEST**.</span><span class="sxs-lookup"><span data-stu-id="3af33-114">For a list of hit-test values, see **WM\_NCHITTEST**.</span></span>

</dd> <dt>

<span data-ttu-id="3af33-115">*lParam*</span><span class="sxs-lookup"><span data-stu-id="3af33-115">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3af33-116">Structure de [**points**](/previous-versions//dd162808(v=vs.85)) qui contient les coordonnées x et y du curseur.</span><span class="sxs-lookup"><span data-stu-id="3af33-116">A [**POINTS**](/previous-versions//dd162808(v=vs.85)) structure that contains the x- and y-coordinates of the cursor.</span></span> <span data-ttu-id="3af33-117">Les coordonnées sont relatives à l’angle supérieur gauche de l’écran.</span><span class="sxs-lookup"><span data-stu-id="3af33-117">The coordinates are relative to the upper-left corner of the screen.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3af33-118">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="3af33-118">Return value</span></span>

<span data-ttu-id="3af33-119">Si une application traite ce message, elle doit retourner la valeur zéro.</span><span class="sxs-lookup"><span data-stu-id="3af33-119">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="3af33-120">Notes</span><span class="sxs-lookup"><span data-stu-id="3af33-120">Remarks</span></span>

<span data-ttu-id="3af33-121">Une fenêtre n’a pas besoin du style **cs \_ DBLCLKS** pour recevoir les messages **WM \_ NCMBUTTONDBLCLK** .</span><span class="sxs-lookup"><span data-stu-id="3af33-121">A window need not have the **CS\_DBLCLKS** style to receive **WM\_NCMBUTTONDBLCLK** messages.</span></span>

<span data-ttu-id="3af33-122">Le système génère un message **WM \_ NCMBUTTONDBLCLK** quand l’utilisateur appuie sur, relâche, puis appuie à nouveau sur le bouton central de la souris dans la limite de temps du double-clic du système.</span><span class="sxs-lookup"><span data-stu-id="3af33-122">The system generates a **WM\_NCMBUTTONDBLCLK** message when the user presses, releases, and again presses the middle mouse button within the system's double-click time limit.</span></span> <span data-ttu-id="3af33-123">Si vous double-cliquez sur le bouton central de la souris, vous générez en réalité quatre messages : [**WM \_ NCMBUTTONDOWN**](wm-ncmbuttondown.md), [**WM \_ NCMBUTTONUP**](wm-ncmbuttonup.md), **WM \_ NCMBUTTONDBLCLK** et **WM \_ NCMBUTTONUP** .</span><span class="sxs-lookup"><span data-stu-id="3af33-123">Double-clicking the middle mouse button actually generates four messages: [**WM\_NCMBUTTONDOWN**](wm-ncmbuttondown.md), [**WM\_NCMBUTTONUP**](wm-ncmbuttonup.md), **WM\_NCMBUTTONDBLCLK**, and **WM\_NCMBUTTONUP** again.</span></span>

<span data-ttu-id="3af33-124">Vous pouvez également utiliser les macros [**obten \_ x \_ lParam**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) et [**obten \_ Y \_ lParam**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) pour extraire les valeurs des coordonnées x et y de *lParam*.</span><span class="sxs-lookup"><span data-stu-id="3af33-124">You can also use the [**GET\_X\_LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) and [**GET\_Y\_LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) macros to extract the values of the x- and y- coordinates from *lParam*.</span></span>


```
xPos = GET_X_LPARAM(lParam); 
yPos = GET_Y_LPARAM(lParam); 
```



> [!IMPORTANT]
> <span data-ttu-id="3af33-125">N’utilisez pas les macros [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) ou [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) pour extraire les coordonnées x et y de la position du curseur, car ces macros renvoient des résultats incorrects sur les systèmes avec plusieurs moniteurs.</span><span class="sxs-lookup"><span data-stu-id="3af33-125">Do not use the [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) or [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) macros to extract the x- and y- coordinates of the cursor position because these macros return incorrect results on systems with multiple monitors.</span></span> <span data-ttu-id="3af33-126">Les systèmes avec plusieurs moniteurs peuvent avoir des coordonnées x et y négatives, et **LOWORD** et **HIWORD** traitent les coordonnées comme des quantités non signées.</span><span class="sxs-lookup"><span data-stu-id="3af33-126">Systems with multiple monitors can have negative x- and y- coordinates, and **LOWORD** and **HIWORD** treat the coordinates as unsigned quantities.</span></span>

 

<span data-ttu-id="3af33-127">Si c’est le cas, le système envoie le message [**WM \_ SYSCOMMAND**](/windows/desktop/menurc/wm-syscommand) à la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="3af33-127">If it is appropriate to do so, the system sends the [**WM\_SYSCOMMAND**](/windows/desktop/menurc/wm-syscommand) message to the window.</span></span>

## <a name="requirements"></a><span data-ttu-id="3af33-128">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3af33-128">Requirements</span></span>



| <span data-ttu-id="3af33-129">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3af33-129">Requirement</span></span> | <span data-ttu-id="3af33-130">Valeur</span><span class="sxs-lookup"><span data-stu-id="3af33-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3af33-131">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3af33-131">Minimum supported client</span></span><br/> | <span data-ttu-id="3af33-132">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3af33-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="3af33-133">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3af33-133">Minimum supported server</span></span><br/> | <span data-ttu-id="3af33-134">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3af33-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="3af33-135">En-tête</span><span class="sxs-lookup"><span data-stu-id="3af33-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="3af33-136"><dt>Winuser. h (inclure Windowsx. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3af33-136"><dt>Winuser.h (include Windowsx.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3af33-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3af33-137">See also</span></span>

<dl> <dt>

<span data-ttu-id="3af33-138">**Référence**</span><span class="sxs-lookup"><span data-stu-id="3af33-138">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="3af33-139">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="3af33-139">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[<span data-ttu-id="3af33-140">**Obtient \_ X \_ lParam**</span><span class="sxs-lookup"><span data-stu-id="3af33-140">**GET\_X\_LPARAM**</span></span>](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam)
</dt> <dt>

[<span data-ttu-id="3af33-141">**Obtient \_ le \_ lParam Y**</span><span class="sxs-lookup"><span data-stu-id="3af33-141">**GET\_Y\_LPARAM**</span></span>](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam)
</dt> <dt>

[<span data-ttu-id="3af33-142">**\_NCHITTEST WM**</span><span class="sxs-lookup"><span data-stu-id="3af33-142">**WM\_NCHITTEST**</span></span>](wm-nchittest.md)
</dt> <dt>

[<span data-ttu-id="3af33-143">**\_NCMBUTTONDOWN WM**</span><span class="sxs-lookup"><span data-stu-id="3af33-143">**WM\_NCMBUTTONDOWN**</span></span>](wm-ncmbuttondown.md)
</dt> <dt>

[<span data-ttu-id="3af33-144">**\_NCMBUTTONUP WM**</span><span class="sxs-lookup"><span data-stu-id="3af33-144">**WM\_NCMBUTTONUP**</span></span>](wm-ncmbuttonup.md)
</dt> <dt>

[<span data-ttu-id="3af33-145">**\_SYSCOMMAND WM**</span><span class="sxs-lookup"><span data-stu-id="3af33-145">**WM\_SYSCOMMAND**</span></span>](/windows/desktop/menurc/wm-syscommand)
</dt> <dt>

<span data-ttu-id="3af33-146">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="3af33-146">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="3af33-147">Entrée de la souris</span><span class="sxs-lookup"><span data-stu-id="3af33-147">Mouse Input</span></span>](mouse-input.md)
</dt> <dt>

<span data-ttu-id="3af33-148">**Autres ressources**</span><span class="sxs-lookup"><span data-stu-id="3af33-148">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="3af33-149">**MAKEPOINTS**</span><span class="sxs-lookup"><span data-stu-id="3af33-149">**MAKEPOINTS**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-makepoints)
</dt> <dt>

<span data-ttu-id="3af33-150">[**MOMENTS**](/previous-versions//dd162808(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="3af33-150">[**POINTS**](/previous-versions//dd162808(v=vs.85))</span></span>
</dt> </dl>

 

