---
title: Message WM_NCXBUTTONUP (winuser. h)
description: Publié lorsque l’utilisateur relâche le premier ou le second bouton X lorsque le curseur se trouve dans la zone non cliente d’une fenêtre. Ce message est publié dans la fenêtre qui contient le curseur. Si une fenêtre a capturé la souris, ce message n’est pas publié.
ms.assetid: 07ab5d4e-9912-4867-9146-8abc5addc15d
keywords:
- WM_NCXBUTTONUP l’entrée du clavier et de la souris du message
topic_type:
- apiref
api_name:
- WM_NCXBUTTONUP
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6330849a433787dd09fad536f005d91f60376013
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742348"
---
# <a name="wm_ncxbuttonup-message"></a><span data-ttu-id="f599e-106">\_Message WM NCXBUTTONUP</span><span class="sxs-lookup"><span data-stu-id="f599e-106">WM\_NCXBUTTONUP message</span></span>

<span data-ttu-id="f599e-107">Publié lorsque l’utilisateur relâche le premier ou le second bouton X lorsque le curseur se trouve dans la zone non cliente d’une fenêtre.</span><span class="sxs-lookup"><span data-stu-id="f599e-107">Posted when the user releases the first or second X button while the cursor is in the nonclient area of a window.</span></span> <span data-ttu-id="f599e-108">Ce message est publié dans la fenêtre qui contient le curseur.</span><span class="sxs-lookup"><span data-stu-id="f599e-108">This message is posted to the window that contains the cursor.</span></span> <span data-ttu-id="f599e-109">Si une fenêtre a capturé la souris, ce message n’est *pas* publié.</span><span class="sxs-lookup"><span data-stu-id="f599e-109">If a window has captured the mouse, this message is *not* posted.</span></span>

<span data-ttu-id="f599e-110">Une fenêtre reçoit ce message par le biais de sa fonction [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="f599e-110">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_NCXBUTTONUP                  0x00AC
```



## <a name="parameters"></a><span data-ttu-id="f599e-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f599e-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f599e-112">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f599e-112">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f599e-113">Le mot de poids faible spécifie la valeur du test de positionnement retournée par la fonction [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) du traitement du message [**WM \_ NCHITTEST**](wm-nchittest.md) .</span><span class="sxs-lookup"><span data-stu-id="f599e-113">The low-order word specifies the hit-test value returned by the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function from processing the [**WM\_NCHITTEST**](wm-nchittest.md) message.</span></span> <span data-ttu-id="f599e-114">Pour obtenir la liste des valeurs de test de positionnement, consultez **WM \_ NCHITTEST**.</span><span class="sxs-lookup"><span data-stu-id="f599e-114">For a list of hit-test values, see **WM\_NCHITTEST**.</span></span>

<span data-ttu-id="f599e-115">Le mot de poids fort indique le bouton qui a été relâché.</span><span class="sxs-lookup"><span data-stu-id="f599e-115">The high-order word indicates which button was released.</span></span> <span data-ttu-id="f599e-116">Il peut avoir l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="f599e-116">It can be one of the following values.</span></span>



| <span data-ttu-id="f599e-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="f599e-117">Value</span></span>                                                                                                                                                                                                     | <span data-ttu-id="f599e-118">Signification</span><span class="sxs-lookup"><span data-stu-id="f599e-118">Meaning</span></span>                                      |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <span id="XBUTTON1"></span><span id="xbutton1"></span><dl> <span data-ttu-id="f599e-119"><dt>**Le bouton XButton1**</dt> <dt>0x0001</dt></span><span class="sxs-lookup"><span data-stu-id="f599e-119"><dt>**XBUTTON1**</dt> <dt>0x0001</dt></span></span> </dl> | <span data-ttu-id="f599e-120">Le premier bouton X a été relâché.</span><span class="sxs-lookup"><span data-stu-id="f599e-120">The first X button was released.</span></span><br/>  |
| <span id="XBUTTON2"></span><span id="xbutton2"></span><dl> <span data-ttu-id="f599e-121"><dt>**XButton2**</dt> <dt>0x0002</dt></span><span class="sxs-lookup"><span data-stu-id="f599e-121"><dt>**XBUTTON2**</dt> <dt>0x0002</dt></span></span> </dl> | <span data-ttu-id="f599e-122">Le deuxième bouton X a été relâché.</span><span class="sxs-lookup"><span data-stu-id="f599e-122">The second X button was released.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="f599e-123">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f599e-123">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f599e-124">Pointeur vers une structure de [**points**](/previous-versions//dd162808(v=vs.85)) qui contient les coordonnées x et y du curseur.</span><span class="sxs-lookup"><span data-stu-id="f599e-124">A pointer to a [**POINTS**](/previous-versions//dd162808(v=vs.85)) structure that contains the x- and y-coordinates of the cursor.</span></span> <span data-ttu-id="f599e-125">Les coordonnées sont relatives à l’angle supérieur gauche de l’écran.</span><span class="sxs-lookup"><span data-stu-id="f599e-125">The coordinates are relative to the upper-left corner of the screen.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f599e-126">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="f599e-126">Return value</span></span>

<span data-ttu-id="f599e-127">Si une application traite ce message, elle doit retourner la **valeur true**.</span><span class="sxs-lookup"><span data-stu-id="f599e-127">If an application processes this message, it should return **TRUE**.</span></span> <span data-ttu-id="f599e-128">Pour plus d’informations sur le traitement de la valeur de retour, consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="f599e-128">For more information about processing the return value, see the Remarks section.</span></span>

## <a name="remarks"></a><span data-ttu-id="f599e-129">Notes</span><span class="sxs-lookup"><span data-stu-id="f599e-129">Remarks</span></span>

<span data-ttu-id="f599e-130">Utilisez le code suivant pour récupérer les informations dans le paramètre *wParam* .</span><span class="sxs-lookup"><span data-stu-id="f599e-130">Use the following code to get the information in the *wParam* parameter.</span></span>


```
nHittest = GET_NCHITTEST_WPARAM(wParam); 
fwButton = GET_XBUTTON_WPARAM(wParam); 
```



<span data-ttu-id="f599e-131">Vous pouvez également utiliser le code suivant pour récupérer les coordonnées x et y à partir de *lParam*:</span><span class="sxs-lookup"><span data-stu-id="f599e-131">You can also use the following code to get the x- and y-coordinates from *lParam*:</span></span>


```
xPos = GET_X_LPARAM(lParam); 
yPos = GET_Y_LPARAM(lParam); 
```



> [!IMPORTANT]
> <span data-ttu-id="f599e-132">N’utilisez pas les macros [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) ou [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) pour extraire les coordonnées x et y de la position du curseur, car ces macros renvoient des résultats incorrects sur les systèmes avec plusieurs moniteurs.</span><span class="sxs-lookup"><span data-stu-id="f599e-132">Do not use the [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) or [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) macros to extract the x- and y- coordinates of the cursor position because these macros return incorrect results on systems with multiple monitors.</span></span> <span data-ttu-id="f599e-133">Les systèmes avec plusieurs moniteurs peuvent avoir des coordonnées x et y négatives, et **LOWORD** et **HIWORD** traitent les coordonnées comme des quantités non signées.</span><span class="sxs-lookup"><span data-stu-id="f599e-133">Systems with multiple monitors can have negative x- and y- coordinates, and **LOWORD** and **HIWORD** treat the coordinates as unsigned quantities.</span></span>

 

<span data-ttu-id="f599e-134">Par défaut, la fonction [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) teste le point spécifié pour atteindre la position du curseur et effectue l’action appropriée.</span><span class="sxs-lookup"><span data-stu-id="f599e-134">By default, the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function tests the specified point to get the position of the cursor and performs the appropriate action.</span></span> <span data-ttu-id="f599e-135">Le cas échéant, il envoie le message [**WM \_ SYSCOMMAND**](/windows/desktop/menurc/wm-syscommand) à la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="f599e-135">If appropriate, it sends the [**WM\_SYSCOMMAND**](/windows/desktop/menurc/wm-syscommand) message to the window.</span></span>

<span data-ttu-id="f599e-136">Contrairement aux [**messages \_ WM NCLBUTTONUP**](wm-nclbuttonup.md), [**WM \_ NCMBUTTONUP**](wm-ncmbuttonup.md)et [**WM \_ NCRBUTTONUP**](wm-ncrbuttonup.md) , une application doit retourner la **valeur true** à partir de ce message si elle le traite.</span><span class="sxs-lookup"><span data-stu-id="f599e-136">Unlike the [**WM\_NCLBUTTONUP**](wm-nclbuttonup.md), [**WM\_NCMBUTTONUP**](wm-ncmbuttonup.md), and [**WM\_NCRBUTTONUP**](wm-ncrbuttonup.md) messages, an application should return **TRUE** from this message if it processes it.</span></span> <span data-ttu-id="f599e-137">Cela permettra aux logiciels qui simulent ce message sur les systèmes Windows antérieurs à Windows 2000 de déterminer si la procédure de fenêtre a traité le message ou appelé [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) pour le traiter.</span><span class="sxs-lookup"><span data-stu-id="f599e-137">Doing so will allow software that simulates this message on Windows systems earlier than Windows 2000 to determine whether the window procedure processed the message or called [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) to process it.</span></span>

## <a name="requirements"></a><span data-ttu-id="f599e-138">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f599e-138">Requirements</span></span>



| <span data-ttu-id="f599e-139">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f599e-139">Requirement</span></span> | <span data-ttu-id="f599e-140">Valeur</span><span class="sxs-lookup"><span data-stu-id="f599e-140">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f599e-141">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f599e-141">Minimum supported client</span></span><br/> | <span data-ttu-id="f599e-142">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f599e-142">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="f599e-143">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f599e-143">Minimum supported server</span></span><br/> | <span data-ttu-id="f599e-144">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f599e-144">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="f599e-145">En-tête</span><span class="sxs-lookup"><span data-stu-id="f599e-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="f599e-146"><dt>Winuser. h (inclure Windowsx. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f599e-146"><dt>Winuser.h (include Windowsx.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f599e-147">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f599e-147">See also</span></span>

<dl> <dt>

<span data-ttu-id="f599e-148">**Référence**</span><span class="sxs-lookup"><span data-stu-id="f599e-148">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="f599e-149">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="f599e-149">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[<span data-ttu-id="f599e-150">**Obtient \_ X \_ lParam**</span><span class="sxs-lookup"><span data-stu-id="f599e-150">**GET\_X\_LPARAM**</span></span>](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam)
</dt> <dt>

[<span data-ttu-id="f599e-151">**Obtient \_ le \_ lParam Y**</span><span class="sxs-lookup"><span data-stu-id="f599e-151">**GET\_Y\_LPARAM**</span></span>](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam)
</dt> <dt>

[<span data-ttu-id="f599e-152">**\_NCHITTEST WM**</span><span class="sxs-lookup"><span data-stu-id="f599e-152">**WM\_NCHITTEST**</span></span>](wm-nchittest.md)
</dt> <dt>

[<span data-ttu-id="f599e-153">**\_NCXBUTTONDBLCLK WM**</span><span class="sxs-lookup"><span data-stu-id="f599e-153">**WM\_NCXBUTTONDBLCLK**</span></span>](wm-ncxbuttondblclk.md)
</dt> <dt>

[<span data-ttu-id="f599e-154">**\_NCXBUTTONDOWN WM**</span><span class="sxs-lookup"><span data-stu-id="f599e-154">**WM\_NCXBUTTONDOWN**</span></span>](wm-ncxbuttondown.md)
</dt> <dt>

[<span data-ttu-id="f599e-155">**\_SYSCOMMAND WM**</span><span class="sxs-lookup"><span data-stu-id="f599e-155">**WM\_SYSCOMMAND**</span></span>](/windows/desktop/menurc/wm-syscommand)
</dt> <dt>

<span data-ttu-id="f599e-156">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="f599e-156">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="f599e-157">Entrée de la souris</span><span class="sxs-lookup"><span data-stu-id="f599e-157">Mouse Input</span></span>](mouse-input.md)
</dt> <dt>

<span data-ttu-id="f599e-158">**Autres ressources**</span><span class="sxs-lookup"><span data-stu-id="f599e-158">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="f599e-159">**MAKEPOINTS**</span><span class="sxs-lookup"><span data-stu-id="f599e-159">**MAKEPOINTS**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-makepoints)
</dt> <dt>

<span data-ttu-id="f599e-160">[**MOMENTS**](/previous-versions//dd162808(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="f599e-160">[**POINTS**](/previous-versions//dd162808(v=vs.85))</span></span>
</dt> </dl>

 

