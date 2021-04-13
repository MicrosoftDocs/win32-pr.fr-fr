---
title: Message WM_NCRBUTTONDBLCLK (winuser. h)
description: Publié lorsque l’utilisateur double-clique avec le bouton droit de la souris alors que le curseur se trouve dans la zone non cliente d’une fenêtre. Ce message est publié dans la fenêtre qui contient le curseur. Si une fenêtre a capturé la souris, ce message n’est pas publié.
ms.assetid: 20d62b05-07de-49da-b160-29fa1f5067fa
keywords:
- WM_NCRBUTTONDBLCLK l’entrée du clavier et de la souris du message
topic_type:
- apiref
api_name:
- WM_NCRBUTTONDBLCLK
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fee33d9b31f99a00181427c9a715df792d95fe55
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508942"
---
# <a name="wm_ncrbuttondblclk-message"></a><span data-ttu-id="dbf45-106">\_Message WM NCRBUTTONDBLCLK</span><span class="sxs-lookup"><span data-stu-id="dbf45-106">WM\_NCRBUTTONDBLCLK message</span></span>

<span data-ttu-id="dbf45-107">Publié lorsque l’utilisateur double-clique avec le bouton droit de la souris alors que le curseur se trouve dans la zone non cliente d’une fenêtre.</span><span class="sxs-lookup"><span data-stu-id="dbf45-107">Posted when the user double-clicks the right mouse button while the cursor is within the nonclient area of a window.</span></span> <span data-ttu-id="dbf45-108">Ce message est publié dans la fenêtre qui contient le curseur.</span><span class="sxs-lookup"><span data-stu-id="dbf45-108">This message is posted to the window that contains the cursor.</span></span> <span data-ttu-id="dbf45-109">Si une fenêtre a capturé la souris, ce message n’est pas publié.</span><span class="sxs-lookup"><span data-stu-id="dbf45-109">If a window has captured the mouse, this message is not posted.</span></span>

<span data-ttu-id="dbf45-110">Une fenêtre reçoit ce message par le biais de sa fonction [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="dbf45-110">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_NCRBUTTONDBLCLK              0x00A6
```



## <a name="parameters"></a><span data-ttu-id="dbf45-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="dbf45-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dbf45-112">*wParam*</span><span class="sxs-lookup"><span data-stu-id="dbf45-112">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="dbf45-113">Valeur du test de positionnement retournée par la fonction [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) suite au traitement du message [**WM \_ NCHITTEST**](wm-nchittest.md) .</span><span class="sxs-lookup"><span data-stu-id="dbf45-113">The hit-test value returned by the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function as a result of processing the [**WM\_NCHITTEST**](wm-nchittest.md) message.</span></span> <span data-ttu-id="dbf45-114">Pour obtenir la liste des valeurs de test de positionnement, consultez **WM \_ NCHITTEST**.</span><span class="sxs-lookup"><span data-stu-id="dbf45-114">For a list of hit-test values, see **WM\_NCHITTEST**.</span></span>

</dd> <dt>

<span data-ttu-id="dbf45-115">*lParam*</span><span class="sxs-lookup"><span data-stu-id="dbf45-115">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="dbf45-116">Structure de [**points**](/previous-versions//dd162808(v=vs.85)) qui contient les coordonnées x et y du curseur.</span><span class="sxs-lookup"><span data-stu-id="dbf45-116">A [**POINTS**](/previous-versions//dd162808(v=vs.85)) structure that contains the x- and y-coordinates of the cursor.</span></span> <span data-ttu-id="dbf45-117">Les coordonnées sont relatives à l’angle supérieur gauche de l’écran.</span><span class="sxs-lookup"><span data-stu-id="dbf45-117">The coordinates are relative to the upper-left corner of the screen.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dbf45-118">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="dbf45-118">Return value</span></span>

<span data-ttu-id="dbf45-119">Si une application traite ce message, elle doit retourner la valeur zéro.</span><span class="sxs-lookup"><span data-stu-id="dbf45-119">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="dbf45-120">Notes</span><span class="sxs-lookup"><span data-stu-id="dbf45-120">Remarks</span></span>

<span data-ttu-id="dbf45-121">Une fenêtre n’a pas besoin du style **cs \_ DBLCLKS** pour recevoir les messages **WM \_ NCRBUTTONDBLCLK** .</span><span class="sxs-lookup"><span data-stu-id="dbf45-121">A window need not have the **CS\_DBLCLKS** style to receive **WM\_NCRBUTTONDBLCLK** messages.</span></span>

<span data-ttu-id="dbf45-122">Le système génère un message **WM \_ NCRBUTTONDBLCLK** quand l’utilisateur appuie sur, relâche, puis appuie à nouveau sur le bouton droit de la souris dans la limite de temps du double-clic du système.</span><span class="sxs-lookup"><span data-stu-id="dbf45-122">The system generates a **WM\_NCRBUTTONDBLCLK** message when the user presses, releases, and again presses the right mouse button within the system's double-click time limit.</span></span> <span data-ttu-id="dbf45-123">Le fait de double-cliquer sur le bouton droit de la souris génère en fait quatre messages : [**WM \_ NCRBUTTONDOWN**](wm-ncrbuttondown.md), [**WM \_ NCRBUTTONUP**](wm-ncrbuttonup.md), **WM \_ NCRBUTTONDBLCLK** et **WM \_ NCRBUTTONUP** .</span><span class="sxs-lookup"><span data-stu-id="dbf45-123">Double-clicking the right mouse button actually generates four messages: [**WM\_NCRBUTTONDOWN**](wm-ncrbuttondown.md), [**WM\_NCRBUTTONUP**](wm-ncrbuttonup.md), **WM\_NCRBUTTONDBLCLK**, and **WM\_NCRBUTTONUP** again.</span></span>

<span data-ttu-id="dbf45-124">Vous pouvez également utiliser les macros [**obten \_ x \_ lParam**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) et [**obten \_ Y \_ lParam**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) pour extraire les valeurs des coordonnées x et y de *lParam*.</span><span class="sxs-lookup"><span data-stu-id="dbf45-124">You can also use the [**GET\_X\_LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) and [**GET\_Y\_LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) macros to extract the values of the x- and y- coordinates from *lParam*.</span></span>


```
xPos = GET_X_LPARAM(lParam); 
yPos = GET_Y_LPARAM(lParam); 
```



> [!IMPORTANT]
> <span data-ttu-id="dbf45-125">N’utilisez pas les macros [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) ou [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) pour extraire les coordonnées x et y de la position du curseur, car ces macros renvoient des résultats incorrects sur les systèmes avec plusieurs moniteurs.</span><span class="sxs-lookup"><span data-stu-id="dbf45-125">Do not use the [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) or [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) macros to extract the x- and y- coordinates of the cursor position because these macros return incorrect results on systems with multiple monitors.</span></span> <span data-ttu-id="dbf45-126">Les systèmes avec plusieurs moniteurs peuvent avoir des coordonnées x et y négatives, et **LOWORD** et **HIWORD** traitent les coordonnées comme des quantités non signées.</span><span class="sxs-lookup"><span data-stu-id="dbf45-126">Systems with multiple monitors can have negative x- and y- coordinates, and **LOWORD** and **HIWORD** treat the coordinates as unsigned quantities.</span></span>

 

<span data-ttu-id="dbf45-127">Si c’est le cas, le système envoie le message [**WM \_ SYSCOMMAND**](/windows/desktop/menurc/wm-syscommand) à la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="dbf45-127">If it is appropriate to do so, the system sends the [**WM\_SYSCOMMAND**](/windows/desktop/menurc/wm-syscommand) message to the window.</span></span>

## <a name="requirements"></a><span data-ttu-id="dbf45-128">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="dbf45-128">Requirements</span></span>



| <span data-ttu-id="dbf45-129">Condition requise</span><span class="sxs-lookup"><span data-stu-id="dbf45-129">Requirement</span></span> | <span data-ttu-id="dbf45-130">Valeur</span><span class="sxs-lookup"><span data-stu-id="dbf45-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dbf45-131">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="dbf45-131">Minimum supported client</span></span><br/> | <span data-ttu-id="dbf45-132">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="dbf45-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="dbf45-133">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="dbf45-133">Minimum supported server</span></span><br/> | <span data-ttu-id="dbf45-134">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="dbf45-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="dbf45-135">En-tête</span><span class="sxs-lookup"><span data-stu-id="dbf45-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="dbf45-136"><dt>Winuser. h (inclure Windowsx. h)</dt></span><span class="sxs-lookup"><span data-stu-id="dbf45-136"><dt>Winuser.h (include Windowsx.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dbf45-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="dbf45-137">See also</span></span>

<dl> <dt>

<span data-ttu-id="dbf45-138">**Référence**</span><span class="sxs-lookup"><span data-stu-id="dbf45-138">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="dbf45-139">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="dbf45-139">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[<span data-ttu-id="dbf45-140">**Obtient \_ X \_ lParam**</span><span class="sxs-lookup"><span data-stu-id="dbf45-140">**GET\_X\_LPARAM**</span></span>](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam)
</dt> <dt>

[<span data-ttu-id="dbf45-141">**Obtient \_ le \_ lParam Y**</span><span class="sxs-lookup"><span data-stu-id="dbf45-141">**GET\_Y\_LPARAM**</span></span>](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam)
</dt> <dt>

[<span data-ttu-id="dbf45-142">**\_NCHITTEST WM**</span><span class="sxs-lookup"><span data-stu-id="dbf45-142">**WM\_NCHITTEST**</span></span>](wm-nchittest.md)
</dt> <dt>

[<span data-ttu-id="dbf45-143">**\_NCRBUTTONDOWN WM**</span><span class="sxs-lookup"><span data-stu-id="dbf45-143">**WM\_NCRBUTTONDOWN**</span></span>](wm-ncrbuttondown.md)
</dt> <dt>

[<span data-ttu-id="dbf45-144">**\_NCRBUTTONUP WM**</span><span class="sxs-lookup"><span data-stu-id="dbf45-144">**WM\_NCRBUTTONUP**</span></span>](wm-ncrbuttonup.md)
</dt> <dt>

[<span data-ttu-id="dbf45-145">**\_SYSCOMMAND WM**</span><span class="sxs-lookup"><span data-stu-id="dbf45-145">**WM\_SYSCOMMAND**</span></span>](/windows/desktop/menurc/wm-syscommand)
</dt> <dt>

<span data-ttu-id="dbf45-146">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="dbf45-146">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="dbf45-147">Entrée de la souris</span><span class="sxs-lookup"><span data-stu-id="dbf45-147">Mouse Input</span></span>](mouse-input.md)
</dt> <dt>

<span data-ttu-id="dbf45-148">**Autres ressources**</span><span class="sxs-lookup"><span data-stu-id="dbf45-148">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="dbf45-149">**MAKEPOINTS**</span><span class="sxs-lookup"><span data-stu-id="dbf45-149">**MAKEPOINTS**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-makepoints)
</dt> <dt>

<span data-ttu-id="dbf45-150">[**MOMENTS**](/previous-versions//dd162808(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="dbf45-150">[**POINTS**](/previous-versions//dd162808(v=vs.85))</span></span>
</dt> </dl>

 

