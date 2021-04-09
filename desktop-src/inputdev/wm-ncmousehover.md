---
title: Message WM_NCMOUSEHOVER (winuser. h)
description: Publié dans une fenêtre lorsque le curseur pointe sur la zone non cliente de la fenêtre pendant la période spécifiée dans un appel antérieur à TrackMouseEvent.
ms.assetid: ca1afdc2-7884-445e-b9b7-4d7dd5dcea38
keywords:
- WM_NCMOUSEHOVER l’entrée du clavier et de la souris du message
topic_type:
- apiref
api_name:
- WM_NCMOUSEHOVER
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cde2e70b04602de5936e945789007a6c5fea8542
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104033174"
---
# <a name="wm_ncmousehover-message"></a><span data-ttu-id="6299d-104">\_Message WM NCMOUSEHOVER</span><span class="sxs-lookup"><span data-stu-id="6299d-104">WM\_NCMOUSEHOVER message</span></span>

<span data-ttu-id="6299d-105">Publié dans une fenêtre lorsque le curseur pointe sur la zone non cliente de la fenêtre pendant la période spécifiée dans un appel antérieur à [**TrackMouseEvent**](/windows/win32/api/winuser/nf-winuser-trackmouseevent).</span><span class="sxs-lookup"><span data-stu-id="6299d-105">Posted to a window when the cursor hovers over the nonclient area of the window for the period of time specified in a prior call to [**TrackMouseEvent**](/windows/win32/api/winuser/nf-winuser-trackmouseevent).</span></span>

<span data-ttu-id="6299d-106">Une fenêtre reçoit ce message par le biais de sa fonction [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="6299d-106">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_NCMOUSEHOVER                 0x02A0
```



## <a name="parameters"></a><span data-ttu-id="6299d-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6299d-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6299d-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="6299d-108">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6299d-109">Valeur du test de positionnement retournée par la fonction [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) suite au traitement du message [**WM \_ NCHITTEST**](wm-nchittest.md) .</span><span class="sxs-lookup"><span data-stu-id="6299d-109">The hit-test value returned by the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function as a result of processing the [**WM\_NCHITTEST**](wm-nchittest.md) message.</span></span> <span data-ttu-id="6299d-110">Pour obtenir la liste des valeurs de test de positionnement, consultez **WM \_ NCHITTEST**.</span><span class="sxs-lookup"><span data-stu-id="6299d-110">For a list of hit-test values, see **WM\_NCHITTEST**.</span></span>

</dd> <dt>

<span data-ttu-id="6299d-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="6299d-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6299d-112">Structure de [**points**](/previous-versions//dd162808(v=vs.85)) qui contient les coordonnées x et y du curseur.</span><span class="sxs-lookup"><span data-stu-id="6299d-112">A [**POINTS**](/previous-versions//dd162808(v=vs.85)) structure that contains the x- and y-coordinates of the cursor.</span></span> <span data-ttu-id="6299d-113">Les coordonnées sont relatives à l’angle supérieur gauche de l’écran.</span><span class="sxs-lookup"><span data-stu-id="6299d-113">The coordinates are relative to the upper-left corner of the screen.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6299d-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="6299d-114">Return value</span></span>

<span data-ttu-id="6299d-115">Si une application traite ce message, elle doit retourner la valeur zéro.</span><span class="sxs-lookup"><span data-stu-id="6299d-115">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="6299d-116">Notes</span><span class="sxs-lookup"><span data-stu-id="6299d-116">Remarks</span></span>

<span data-ttu-id="6299d-117">Le suivi de survol s’arrête lorsque ce message est généré.</span><span class="sxs-lookup"><span data-stu-id="6299d-117">Hover tracking stops when this message is generated.</span></span> <span data-ttu-id="6299d-118">L’application doit appeler à nouveau [**TrackMouseEvent**](/windows/win32/api/winuser/nf-winuser-trackmouseevent) si elle nécessite un suivi supplémentaire du comportement de pointage de la souris.</span><span class="sxs-lookup"><span data-stu-id="6299d-118">The application must call [**TrackMouseEvent**](/windows/win32/api/winuser/nf-winuser-trackmouseevent) again if it requires further tracking of mouse hover behavior.</span></span>

<span data-ttu-id="6299d-119">Vous pouvez également utiliser les macros [**obten \_ x \_ lParam**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) et [**obten \_ Y \_ lParam**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) pour extraire les valeurs des coordonnées x et y de *lParam*.</span><span class="sxs-lookup"><span data-stu-id="6299d-119">You can also use the [**GET\_X\_LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) and [**GET\_Y\_LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) macros to extract the values of the x- and y- coordinates from *lParam*.</span></span>


```
xPos = GET_X_LPARAM(lParam); 
yPos = GET_Y_LPARAM(lParam); 
```



> [!IMPORTANT]
> <span data-ttu-id="6299d-120">N’utilisez pas les macros [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) ou [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) pour extraire les coordonnées x et y de la position du curseur, car ces macros renvoient des résultats incorrects sur les systèmes avec plusieurs moniteurs.</span><span class="sxs-lookup"><span data-stu-id="6299d-120">Do not use the [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) or [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) macros to extract the x- and y- coordinates of the cursor position because these macros return incorrect results on systems with multiple monitors.</span></span> <span data-ttu-id="6299d-121">Les systèmes avec plusieurs moniteurs peuvent avoir des coordonnées x et y négatives, et **LOWORD** et **HIWORD** traitent les coordonnées comme des quantités non signées.</span><span class="sxs-lookup"><span data-stu-id="6299d-121">Systems with multiple monitors can have negative x- and y- coordinates, and **LOWORD** and **HIWORD** treat the coordinates as unsigned quantities.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="6299d-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6299d-122">Requirements</span></span>



| <span data-ttu-id="6299d-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6299d-123">Requirement</span></span> | <span data-ttu-id="6299d-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="6299d-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6299d-125">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6299d-125">Minimum supported client</span></span><br/> | <span data-ttu-id="6299d-126">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6299d-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="6299d-127">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6299d-127">Minimum supported server</span></span><br/> | <span data-ttu-id="6299d-128">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6299d-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="6299d-129">En-tête</span><span class="sxs-lookup"><span data-stu-id="6299d-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="6299d-130"><dt>Winuser. h (inclure Windowsx. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6299d-130"><dt>Winuser.h (include Windowsx.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6299d-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6299d-131">See also</span></span>

<dl> <dt>

<span data-ttu-id="6299d-132">**Référence**</span><span class="sxs-lookup"><span data-stu-id="6299d-132">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="6299d-133">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="6299d-133">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[<span data-ttu-id="6299d-134">**Obtient \_ X \_ lParam**</span><span class="sxs-lookup"><span data-stu-id="6299d-134">**GET\_X\_LPARAM**</span></span>](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam)
</dt> <dt>

[<span data-ttu-id="6299d-135">**Obtient \_ le \_ lParam Y**</span><span class="sxs-lookup"><span data-stu-id="6299d-135">**GET\_Y\_LPARAM**</span></span>](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam)
</dt> <dt>

[<span data-ttu-id="6299d-136">**TrackMouseEvent**</span><span class="sxs-lookup"><span data-stu-id="6299d-136">**TrackMouseEvent**</span></span>](/windows/win32/api/winuser/nf-winuser-trackmouseevent)
</dt> <dt>

[<span data-ttu-id="6299d-137">**TRACKMOUSEEVENT**</span><span class="sxs-lookup"><span data-stu-id="6299d-137">**TRACKMOUSEEVENT**</span></span>](/windows/win32/api/winuser/ns-winuser-trackmouseevent)
</dt> <dt>

[<span data-ttu-id="6299d-138">**\_NCHITTEST WM**</span><span class="sxs-lookup"><span data-stu-id="6299d-138">**WM\_NCHITTEST**</span></span>](wm-nchittest.md)
</dt> <dt>

[<span data-ttu-id="6299d-139">**\_MOUSEHOVER WM**</span><span class="sxs-lookup"><span data-stu-id="6299d-139">**WM\_MOUSEHOVER**</span></span>](wm-mousehover.md)
</dt> <dt>

<span data-ttu-id="6299d-140">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="6299d-140">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="6299d-141">Entrée de la souris</span><span class="sxs-lookup"><span data-stu-id="6299d-141">Mouse Input</span></span>](mouse-input.md)
</dt> <dt>

<span data-ttu-id="6299d-142">**Autres ressources**</span><span class="sxs-lookup"><span data-stu-id="6299d-142">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="6299d-143">**MAKEPOINTS**</span><span class="sxs-lookup"><span data-stu-id="6299d-143">**MAKEPOINTS**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-makepoints)
</dt> <dt>

<span data-ttu-id="6299d-144">[**MOMENTS**](/previous-versions//dd162808(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="6299d-144">[**POINTS**](/previous-versions//dd162808(v=vs.85))</span></span>
</dt> </dl>

 

