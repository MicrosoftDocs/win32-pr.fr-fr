---
description: Le \_ message WM PRINTCLIENT est envoyé à une fenêtre pour demander qu’il dessine sa zone cliente dans le contexte de périphérique spécifié, le plus souvent dans un contexte de périphérique d’impression.
ms.assetid: 8703ee74-812a-4ca2-8ee3-a3b8779739e7
title: Message WM_PRINTCLIENT (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 52aca68695964a35ab9a2c4e309cd71c2e9f7eca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104973511"
---
# <a name="wm_printclient-message"></a><span data-ttu-id="38b89-103">\_Message WM PRINTCLIENT</span><span class="sxs-lookup"><span data-stu-id="38b89-103">WM\_PRINTCLIENT message</span></span>

<span data-ttu-id="38b89-104">Le message **WM \_ PRINTCLIENT** est envoyé à une fenêtre pour demander qu’il dessine sa zone cliente dans le contexte de périphérique spécifié, le plus souvent dans un contexte de périphérique d’impression.</span><span class="sxs-lookup"><span data-stu-id="38b89-104">The **WM\_PRINTCLIENT** message is sent to a window to request that it draw its client area in the specified device context, most commonly in a printer device context.</span></span>

<span data-ttu-id="38b89-105">Contrairement à l' [**\_ impression WM**](wm-print.md), le **WM \_ PRINTCLIENT** n’est pas traité par [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca).</span><span class="sxs-lookup"><span data-stu-id="38b89-105">Unlike [**WM\_PRINT**](wm-print.md), **WM\_PRINTCLIENT** is not processed by [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca).</span></span> <span data-ttu-id="38b89-106">Une fenêtre doit traiter le message **WM \_ PRINTCLIENT** par le biais d’une fonction [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) définie par l’application pour qu’elle soit utilisée correctement.</span><span class="sxs-lookup"><span data-stu-id="38b89-106">A window should process the **WM\_PRINTCLIENT** message through an application-defined [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function for it to be used properly.</span></span>


```C++
LRESULT CALLBACK WindowProc(
  HWND hwnd, 
  UINT  uMsg, 
  WPARAM wParam, 
  LPARAM lParam     
);
```



## <a name="parameters"></a><span data-ttu-id="38b89-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="38b89-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="38b89-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="38b89-108">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="38b89-109">Handle vers le contexte de périphérique dans lequel dessiner.</span><span class="sxs-lookup"><span data-stu-id="38b89-109">A handle to the device context to draw in.</span></span>

</dd> <dt>

<span data-ttu-id="38b89-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="38b89-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="38b89-111">Options de dessin.</span><span class="sxs-lookup"><span data-stu-id="38b89-111">The drawing options.</span></span> <span data-ttu-id="38b89-112">Ce paramètre peut être une ou plusieurs des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="38b89-112">This parameter can be one or more of the following values.</span></span>



| <span data-ttu-id="38b89-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="38b89-113">Value</span></span>                                                                                                                                                                  | <span data-ttu-id="38b89-114">Signification</span><span class="sxs-lookup"><span data-stu-id="38b89-114">Meaning</span></span>                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| <span id="PRF_CHECKVISIBLE"></span><span id="prf_checkvisible"></span><dl> <span data-ttu-id="38b89-115"><dt>**\_CHECKVISIBLE PRF**</dt></span><span class="sxs-lookup"><span data-stu-id="38b89-115"><dt>**PRF\_CHECKVISIBLE**</dt></span></span> </dl> | <span data-ttu-id="38b89-116">Dessine la fenêtre uniquement si elle est visible.</span><span class="sxs-lookup"><span data-stu-id="38b89-116">Draws the window only if it is visible.</span></span><br/>          |
| <span id="PRF_CHILDREN"></span><span id="prf_children"></span><dl> <span data-ttu-id="38b89-117"><dt>**\_enfants PRF**</dt></span><span class="sxs-lookup"><span data-stu-id="38b89-117"><dt>**PRF\_CHILDREN**</dt></span></span> </dl>             | <span data-ttu-id="38b89-118">Dessine toutes les fenêtres enfants visibles.</span><span class="sxs-lookup"><span data-stu-id="38b89-118">Draws all visible children windows.</span></span><br/>              |
| <span id="PRF_CLIENT"></span><span id="prf_client"></span><dl> <span data-ttu-id="38b89-119"><dt>**\_client PRF**</dt></span><span class="sxs-lookup"><span data-stu-id="38b89-119"><dt>**PRF\_CLIENT**</dt></span></span> </dl>                   | <span data-ttu-id="38b89-120">Dessine la zone cliente de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="38b89-120">Draws the client area of the window.</span></span><br/>             |
| <span id="PRF_ERASEBKGND"></span><span id="prf_erasebkgnd"></span><dl> <span data-ttu-id="38b89-121"><dt>**\_ERASEBKGND PRF**</dt></span><span class="sxs-lookup"><span data-stu-id="38b89-121"><dt>**PRF\_ERASEBKGND**</dt></span></span> </dl>       | <span data-ttu-id="38b89-122">Efface l’arrière-plan avant de dessiner la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="38b89-122">Erases the background before drawing the window.</span></span><br/> |
| <span id="PRF_NONCLIENT"></span><span id="prf_nonclient"></span><dl> <span data-ttu-id="38b89-123"><dt>**PRF non \_ client**</dt></span><span class="sxs-lookup"><span data-stu-id="38b89-123"><dt>**PRF\_NONCLIENT**</dt></span></span> </dl>          | <span data-ttu-id="38b89-124">Dessine la zone non cliente de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="38b89-124">Draws the nonclient area of the window.</span></span><br/>          |
| <span id="PRF_OWNED"></span><span id="prf_owned"></span><dl> <span data-ttu-id="38b89-125"><dt>**PRF \_ appartenant**</dt></span><span class="sxs-lookup"><span data-stu-id="38b89-125"><dt>**PRF\_OWNED**</dt></span></span> </dl>                      | <span data-ttu-id="38b89-126">Dessine toutes les fenêtres détenues.</span><span class="sxs-lookup"><span data-stu-id="38b89-126">Draws all owned windows.</span></span><br/>                         |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="38b89-127">Notes</span><span class="sxs-lookup"><span data-stu-id="38b89-127">Remarks</span></span>

<span data-ttu-id="38b89-128">Une fenêtre peut traiter ce message à peu près de la même façon que la [**\_ peinture WM**](./wm-paint.md), sauf que [**BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint) et [**EndPaint**](/windows/desktop/api/Winuser/nf-winuser-endpaint) ne doivent pas être appelés (un contexte de périphérique est fourni) et que la fenêtre doit dessiner la totalité de la zone client au lieu de simplement la région non valide.</span><span class="sxs-lookup"><span data-stu-id="38b89-128">A window can process this message in much the same manner as [**WM\_PAINT**](./wm-paint.md), except that [**BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint) and [**EndPaint**](/windows/desktop/api/Winuser/nf-winuser-endpaint) need not be called (a device context is provided), and the window should draw its entire client area rather than just the invalid region.</span></span>

<span data-ttu-id="38b89-129">Les fenêtres qui peuvent être utilisées n’importe où dans le système, telles que les contrôles, doivent traiter ce message.</span><span class="sxs-lookup"><span data-stu-id="38b89-129">Windows that can be used anywhere in the system, such as controls, should process this message.</span></span> <span data-ttu-id="38b89-130">Il est probablement utile pour d’autres fenêtres de traiter ce message, car il est relativement facile à implémenter.</span><span class="sxs-lookup"><span data-stu-id="38b89-130">It is probably worthwhile for other windows to process this message as well because it is relatively easy to implement.</span></span>

<span data-ttu-id="38b89-131">La fonction [AnimateWindow](/windows/desktop/api/winuser/nf-winuser-animatewindow) nécessite que la fenêtre animée implémente le message **WM \_ PRINTCLIENT** .</span><span class="sxs-lookup"><span data-stu-id="38b89-131">The [AnimateWindow](/windows/desktop/api/winuser/nf-winuser-animatewindow) function requires that the window being animated implements the **WM\_PRINTCLIENT** message.</span></span>

## <a name="requirements"></a><span data-ttu-id="38b89-132">Spécifications</span><span class="sxs-lookup"><span data-stu-id="38b89-132">Requirements</span></span>



| <span data-ttu-id="38b89-133">Condition requise</span><span class="sxs-lookup"><span data-stu-id="38b89-133">Requirement</span></span> | <span data-ttu-id="38b89-134">Valeur</span><span class="sxs-lookup"><span data-stu-id="38b89-134">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="38b89-135">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="38b89-135">Minimum supported client</span></span><br/> | <span data-ttu-id="38b89-136">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="38b89-136">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="38b89-137">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="38b89-137">Minimum supported server</span></span><br/> | <span data-ttu-id="38b89-138">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="38b89-138">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="38b89-139">En-tête</span><span class="sxs-lookup"><span data-stu-id="38b89-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="38b89-140"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="38b89-140"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="38b89-141">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="38b89-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="38b89-142">Vue d’ensemble de la peinture et du dessin</span><span class="sxs-lookup"><span data-stu-id="38b89-142">Painting and Drawing Overview</span></span>](painting-and-drawing.md)
</dt> <dt>

[<span data-ttu-id="38b89-143">Peinture et dessin de messages</span><span class="sxs-lookup"><span data-stu-id="38b89-143">Painting and Drawing Messages</span></span>](painting-and-drawing-messages.md)
</dt> <dt>

[<span data-ttu-id="38b89-144">**AnimateWindow**</span><span class="sxs-lookup"><span data-stu-id="38b89-144">**AnimateWindow**</span></span>](/windows/win32/api/winuser/nf-winuser-animatewindow)
</dt> <dt>

[<span data-ttu-id="38b89-145">**BeginPaint**</span><span class="sxs-lookup"><span data-stu-id="38b89-145">**BeginPaint**</span></span>](/windows/desktop/api/Winuser/nf-winuser-beginpaint)
</dt> <dt>

[<span data-ttu-id="38b89-146">**EndPaint**</span><span class="sxs-lookup"><span data-stu-id="38b89-146">**EndPaint**</span></span>](/windows/desktop/api/Winuser/nf-winuser-endpaint)
</dt> <dt>

[<span data-ttu-id="38b89-147">**\_peinture WM**</span><span class="sxs-lookup"><span data-stu-id="38b89-147">**WM\_PAINT**</span></span>](wm-paint.md)
</dt> </dl>

 

 
