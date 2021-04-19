---
title: Message WM_NCXBUTTONDBLCLK (winuser. h)
description: Publié lorsque l’utilisateur double-clique sur le premier ou le second bouton X lorsque le curseur se trouve dans la zone non cliente d’une fenêtre. Ce message est publié dans la fenêtre qui contient le curseur. Si une fenêtre a capturé la souris, ce message n’est pas publié.
ms.assetid: 8c0b1e96-9cbb-4ef8-83ff-9253f1a934ef
keywords:
- WM_NCXBUTTONDBLCLK l’entrée du clavier et de la souris du message
topic_type:
- apiref
api_name:
- WM_NCXBUTTONDBLCLK
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1455f6d6c2fa40f34bbfbe00e0c7a30daa52f375
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106539017"
---
# <a name="wm_ncxbuttondblclk-message"></a><span data-ttu-id="963bc-106">\_Message WM NCXBUTTONDBLCLK</span><span class="sxs-lookup"><span data-stu-id="963bc-106">WM\_NCXBUTTONDBLCLK message</span></span>

<span data-ttu-id="963bc-107">Publié lorsque l’utilisateur double-clique sur le premier ou le second bouton X lorsque le curseur se trouve dans la zone non cliente d’une fenêtre.</span><span class="sxs-lookup"><span data-stu-id="963bc-107">Posted when the user double-clicks the first or second X button while the cursor is in the nonclient area of a window.</span></span> <span data-ttu-id="963bc-108">Ce message est publié dans la fenêtre qui contient le curseur.</span><span class="sxs-lookup"><span data-stu-id="963bc-108">This message is posted to the window that contains the cursor.</span></span> <span data-ttu-id="963bc-109">Si une fenêtre a capturé la souris, ce message n’est pas publié.</span><span class="sxs-lookup"><span data-stu-id="963bc-109">If a window has captured the mouse, this message is not posted.</span></span>

<span data-ttu-id="963bc-110">Une fenêtre reçoit ce message par le biais de sa fonction [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="963bc-110">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_NCXBUTTONDBLCLK              0x00AD
```



## <a name="parameters"></a><span data-ttu-id="963bc-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="963bc-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="963bc-112">*wParam*</span><span class="sxs-lookup"><span data-stu-id="963bc-112">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="963bc-113">Le mot de poids faible spécifie la valeur du test de positionnement retournée par la fonction [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) du traitement du message [**WM \_ NCHITTEST**](wm-nchittest.md) .</span><span class="sxs-lookup"><span data-stu-id="963bc-113">The low-order word specifies the hit-test value returned by the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function from processing the [**WM\_NCHITTEST**](wm-nchittest.md) message.</span></span> <span data-ttu-id="963bc-114">Pour obtenir la liste des valeurs de test de positionnement, consultez **WM \_ NCHITTEST**.</span><span class="sxs-lookup"><span data-stu-id="963bc-114">For a list of hit-test values, see **WM\_NCHITTEST**.</span></span>

<span data-ttu-id="963bc-115">Le mot de poids fort indique sur quel bouton l’utilisateur a double-cliqué.</span><span class="sxs-lookup"><span data-stu-id="963bc-115">The high-order word indicates which button was double-clicked.</span></span> <span data-ttu-id="963bc-116">Il peut avoir l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="963bc-116">It can be one of the following values.</span></span>



| <span data-ttu-id="963bc-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="963bc-117">Value</span></span>                                                                                                                                                                                                     | <span data-ttu-id="963bc-118">Signification</span><span class="sxs-lookup"><span data-stu-id="963bc-118">Meaning</span></span>                                            |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------|
| <span id="XBUTTON1"></span><span id="xbutton1"></span><dl> <span data-ttu-id="963bc-119"><dt>**Le bouton XButton1**</dt> <dt>0x0001</dt></span><span class="sxs-lookup"><span data-stu-id="963bc-119"><dt>**XBUTTON1**</dt> <dt>0x0001</dt></span></span> </dl> | <span data-ttu-id="963bc-120">L’utilisateur a double-cliqué sur le premier bouton X.</span><span class="sxs-lookup"><span data-stu-id="963bc-120">The first X button was double-clicked..</span></span><br/> |
| <span id="XBUTTON2"></span><span id="xbutton2"></span><dl> <span data-ttu-id="963bc-121"><dt>**XButton2**</dt> <dt>0x0002</dt></span><span class="sxs-lookup"><span data-stu-id="963bc-121"><dt>**XBUTTON2**</dt> <dt>0x0002</dt></span></span> </dl> | <span data-ttu-id="963bc-122">L’utilisateur a double-cliqué sur le deuxième bouton X.</span><span class="sxs-lookup"><span data-stu-id="963bc-122">The second X button was double-clicked.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="963bc-123">*lParam*</span><span class="sxs-lookup"><span data-stu-id="963bc-123">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="963bc-124">Pointeur vers une structure de [**points**](/previous-versions//dd162808(v=vs.85)) qui contient les coordonnées x et y du curseur.</span><span class="sxs-lookup"><span data-stu-id="963bc-124">A pointer to a [**POINTS**](/previous-versions//dd162808(v=vs.85)) structure that contains the x- and y-coordinates of the cursor.</span></span> <span data-ttu-id="963bc-125">Les coordonnées sont relatives à l’angle supérieur gauche de l’écran.</span><span class="sxs-lookup"><span data-stu-id="963bc-125">The coordinates are relative to the upper-left corner of the screen.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="963bc-126">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="963bc-126">Return value</span></span>

<span data-ttu-id="963bc-127">Si une application traite ce message, elle doit retourner la **valeur true**.</span><span class="sxs-lookup"><span data-stu-id="963bc-127">If an application processes this message, it should return **TRUE**.</span></span> <span data-ttu-id="963bc-128">Pour plus d’informations sur le traitement de la valeur de retour, consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="963bc-128">For more information about processing the return value, see the Remarks section.</span></span>

## <a name="remarks"></a><span data-ttu-id="963bc-129">Notes</span><span class="sxs-lookup"><span data-stu-id="963bc-129">Remarks</span></span>

<span data-ttu-id="963bc-130">Utilisez le code suivant pour récupérer les informations dans le paramètre *wParam* .</span><span class="sxs-lookup"><span data-stu-id="963bc-130">Use the following code to get the information in the *wParam* parameter.</span></span>


```
nHittest = GET_NCHITTEST_WPARAM(wParam); 
fwButton = GET_XBUTTON_WPARAM(wParam); 
```



<span data-ttu-id="963bc-131">Vous pouvez également utiliser le code suivant pour récupérer les coordonnées x et y à partir de *lParam*:</span><span class="sxs-lookup"><span data-stu-id="963bc-131">You can also use the following code to get the x- and y-coordinates from *lParam*:</span></span>


```
xPos = GET_X_LPARAM(lParam); 
yPos = GET_Y_LPARAM(lParam); 
```



> [!IMPORTANT]
> <span data-ttu-id="963bc-132">N’utilisez pas les macros [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) ou [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) pour extraire les coordonnées x et y de la position du curseur, car ces macros renvoient des résultats incorrects sur les systèmes avec plusieurs moniteurs.</span><span class="sxs-lookup"><span data-stu-id="963bc-132">Do not use the [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) or [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) macros to extract the x- and y- coordinates of the cursor position because these macros return incorrect results on systems with multiple monitors.</span></span> <span data-ttu-id="963bc-133">Les systèmes avec plusieurs moniteurs peuvent avoir des coordonnées x et y négatives, et **LOWORD** et **HIWORD** traitent les coordonnées comme des quantités non signées.</span><span class="sxs-lookup"><span data-stu-id="963bc-133">Systems with multiple monitors can have negative x- and y- coordinates, and **LOWORD** and **HIWORD** treat the coordinates as unsigned quantities.</span></span>

 

<span data-ttu-id="963bc-134">Par défaut, la fonction [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) teste le point spécifié pour atteindre la position du curseur et effectue l’action appropriée.</span><span class="sxs-lookup"><span data-stu-id="963bc-134">By default, the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function tests the specified point to get the position of the cursor and performs the appropriate action.</span></span> <span data-ttu-id="963bc-135">Le cas échéant, il envoie le message [**WM \_ SYSCOMMAND**](/windows/desktop/menurc/wm-syscommand) à la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="963bc-135">If appropriate, it sends the [**WM\_SYSCOMMAND**](/windows/desktop/menurc/wm-syscommand) message to the window.</span></span>

<span data-ttu-id="963bc-136">Une fenêtre n’a pas besoin du style **cs \_ DBLCLKS** pour recevoir les messages **WM \_ NCXBUTTONDBLCLK** .</span><span class="sxs-lookup"><span data-stu-id="963bc-136">A window need not have the **CS\_DBLCLKS** style to receive **WM\_NCXBUTTONDBLCLK** messages.</span></span> <span data-ttu-id="963bc-137">Le système génère un message **WM \_ NCXBUTTONDBLCLK** quand l’utilisateur appuie sur, relâche, puis appuie à nouveau sur un bouton X dans la limite de temps du double-clic du système.</span><span class="sxs-lookup"><span data-stu-id="963bc-137">The system generates a **WM\_NCXBUTTONDBLCLK** message when the user presses, releases, and again presses an X button within the system's double-click time limit.</span></span> <span data-ttu-id="963bc-138">Le fait de double-cliquer sur l’un de ces boutons génère en fait quatre messages : [**WM \_ NCXBUTTONDOWN**](wm-ncxbuttondown.md), [**WM \_ NCXBUTTONUP**](wm-ncxbuttonup.md), **WM \_ NCXBUTTONDBLCLK** et **WM \_ NCXBUTTONUP** .</span><span class="sxs-lookup"><span data-stu-id="963bc-138">Double-clicking one of these buttons actually generates four messages: [**WM\_NCXBUTTONDOWN**](wm-ncxbuttondown.md), [**WM\_NCXBUTTONUP**](wm-ncxbuttonup.md), **WM\_NCXBUTTONDBLCLK**, and **WM\_NCXBUTTONUP** again.</span></span>

<span data-ttu-id="963bc-139">Contrairement aux [**messages \_ WM NCLBUTTONDBLCLK**](wm-nclbuttondblclk.md), [**WM \_ NCMBUTTONDBLCLK**](wm-ncmbuttondblclk.md)et [**WM \_ NCRBUTTONDBLCLK**](wm-ncrbuttondblclk.md) , une application doit retourner la **valeur true** à partir de ce message si elle le traite.</span><span class="sxs-lookup"><span data-stu-id="963bc-139">Unlike the [**WM\_NCLBUTTONDBLCLK**](wm-nclbuttondblclk.md), [**WM\_NCMBUTTONDBLCLK**](wm-ncmbuttondblclk.md), and [**WM\_NCRBUTTONDBLCLK**](wm-ncrbuttondblclk.md) messages, an application should return **TRUE** from this message if it processes it.</span></span> <span data-ttu-id="963bc-140">Cela permettra aux logiciels qui simulent ce message sur les systèmes Windows antérieurs à Windows 2000 de déterminer si la procédure de fenêtre a traité le message ou appelé [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) pour le traiter.</span><span class="sxs-lookup"><span data-stu-id="963bc-140">Doing so will allow software that simulates this message on Windows systems earlier than Windows 2000 to determine whether the window procedure processed the message or called [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) to process it.</span></span>

## <a name="requirements"></a><span data-ttu-id="963bc-141">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="963bc-141">Requirements</span></span>



| <span data-ttu-id="963bc-142">Condition requise</span><span class="sxs-lookup"><span data-stu-id="963bc-142">Requirement</span></span> | <span data-ttu-id="963bc-143">Valeur</span><span class="sxs-lookup"><span data-stu-id="963bc-143">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="963bc-144">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="963bc-144">Minimum supported client</span></span><br/> | <span data-ttu-id="963bc-145">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="963bc-145">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="963bc-146">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="963bc-146">Minimum supported server</span></span><br/> | <span data-ttu-id="963bc-147">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="963bc-147">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="963bc-148">En-tête</span><span class="sxs-lookup"><span data-stu-id="963bc-148">Header</span></span><br/>                   | <dl> <span data-ttu-id="963bc-149"><dt>Winuser. h (inclure Windowsx. h)</dt></span><span class="sxs-lookup"><span data-stu-id="963bc-149"><dt>Winuser.h (include Windowsx.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="963bc-150">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="963bc-150">See also</span></span>

<dl> <dt>

<span data-ttu-id="963bc-151">**Référence**</span><span class="sxs-lookup"><span data-stu-id="963bc-151">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="963bc-152">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="963bc-152">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[<span data-ttu-id="963bc-153">**Obtient \_ X \_ lParam**</span><span class="sxs-lookup"><span data-stu-id="963bc-153">**GET\_X\_LPARAM**</span></span>](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam)
</dt> <dt>

[<span data-ttu-id="963bc-154">**Obtient \_ le \_ lParam Y**</span><span class="sxs-lookup"><span data-stu-id="963bc-154">**GET\_Y\_LPARAM**</span></span>](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam)
</dt> <dt>

[<span data-ttu-id="963bc-155">**\_NCHITTEST WM**</span><span class="sxs-lookup"><span data-stu-id="963bc-155">**WM\_NCHITTEST**</span></span>](wm-nchittest.md)
</dt> <dt>

[<span data-ttu-id="963bc-156">**\_NCXBUTTONDOWN WM**</span><span class="sxs-lookup"><span data-stu-id="963bc-156">**WM\_NCXBUTTONDOWN**</span></span>](wm-ncxbuttondown.md)
</dt> <dt>

[<span data-ttu-id="963bc-157">**\_NCXBUTTONUP WM**</span><span class="sxs-lookup"><span data-stu-id="963bc-157">**WM\_NCXBUTTONUP**</span></span>](wm-ncxbuttonup.md)
</dt> <dt>

[<span data-ttu-id="963bc-158">**\_SYSCOMMAND WM**</span><span class="sxs-lookup"><span data-stu-id="963bc-158">**WM\_SYSCOMMAND**</span></span>](/windows/desktop/menurc/wm-syscommand)
</dt> <dt>

<span data-ttu-id="963bc-159">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="963bc-159">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="963bc-160">Entrée de la souris</span><span class="sxs-lookup"><span data-stu-id="963bc-160">Mouse Input</span></span>](mouse-input.md)
</dt> <dt>

<span data-ttu-id="963bc-161">**Autres ressources**</span><span class="sxs-lookup"><span data-stu-id="963bc-161">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="963bc-162">**MAKEPOINTS**</span><span class="sxs-lookup"><span data-stu-id="963bc-162">**MAKEPOINTS**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-makepoints)
</dt> <dt>

<span data-ttu-id="963bc-163">[**MOMENTS**](/previous-versions//dd162808(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="963bc-163">[**POINTS**](/previous-versions//dd162808(v=vs.85))</span></span>
</dt> </dl>

 

