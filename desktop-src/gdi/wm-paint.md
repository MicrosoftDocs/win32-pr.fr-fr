---
Description: Le \_ message WM Paint est envoyé lorsque le système ou une autre application effectue une requête pour peindre une partie de la fenêtre d’une application.
ms.assetid: afebaa07-cf00-47db-a919-46436f164881
title: Message WM_PAINT (winuser. h)
ms.topic: reference
ms.custom: snippet-project
ms.date: 05/31/2018
ms.openlocfilehash: b13e1779fb54a3db7905cb8fc738ef45558400f5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "104982954"
---
# <a name="wm_paint-message"></a><span data-ttu-id="27596-103">\_Message de peinture WM</span><span class="sxs-lookup"><span data-stu-id="27596-103">WM\_PAINT message</span></span>

<span data-ttu-id="27596-104">Le message **WM \_ Paint** est envoyé lorsque le système ou une autre application effectue une requête pour peindre une partie de la fenêtre d’une application.</span><span class="sxs-lookup"><span data-stu-id="27596-104">The **WM\_PAINT** message is sent when the system or another application makes a request to paint a portion of an application's window.</span></span> <span data-ttu-id="27596-105">Le message est envoyé lorsque la fonction [**UpdateWindow**](/windows/desktop/api/Winuser/nf-winuser-updatewindow) ou [**RedrawWindow**](/windows/desktop/api/Winuser/nf-winuser-redrawwindow) est appelée, ou par la [**fonction DispatchMessage**](/windows/win32/api/winuser/nf-winuser-dispatchmessage) lorsque l’application obtient un message **de \_ peinture WM** à l’aide de la fonction [**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage) ou [**PeekMessage**](/windows/win32/api/winuser/nf-winuser-peekmessagea) .</span><span class="sxs-lookup"><span data-stu-id="27596-105">The message is sent when the [**UpdateWindow**](/windows/desktop/api/Winuser/nf-winuser-updatewindow) or [**RedrawWindow**](/windows/desktop/api/Winuser/nf-winuser-redrawwindow) function is called, or by the [**DispatchMessage**](/windows/win32/api/winuser/nf-winuser-dispatchmessage) function when the application obtains a **WM\_PAINT** message by using the [**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage) or [**PeekMessage**](/windows/win32/api/winuser/nf-winuser-peekmessagea) function.</span></span>

<span data-ttu-id="27596-106">Une fenêtre reçoit ce message par le biais de sa fonction [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="27596-106">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
LRESULT CALLBACK WindowProc(
  HWND hwnd, 
  UINT  uMsg, 
  WPARAM wParam, 
  LPARAM lParam     
);
```



## <a name="parameters"></a><span data-ttu-id="27596-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="27596-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="27596-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="27596-108">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="27596-109">Ce paramètre n'est pas utilisé.</span><span class="sxs-lookup"><span data-stu-id="27596-109">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="27596-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="27596-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="27596-111">Ce paramètre n'est pas utilisé.</span><span class="sxs-lookup"><span data-stu-id="27596-111">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="27596-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="27596-112">Return value</span></span>

<span data-ttu-id="27596-113">Une application retourne la valeur zéro si elle traite ce message.</span><span class="sxs-lookup"><span data-stu-id="27596-113">An application returns zero if it processes this message.</span></span>

## <a name="example"></a><span data-ttu-id="27596-114">Exemple</span><span class="sxs-lookup"><span data-stu-id="27596-114">Example</span></span>

```c
LRESULT CALLBACK WindowProc(HWND hwnd, UINT uMsg, WPARAM wParam, LPARAM lParam)
{
    switch (uMsg)
    {
    case WM_DESTROY:
        PostQuitMessage(0);
        return 0;

    case WM_PAINT:
        {
            PAINTSTRUCT ps;
            HDC hdc = BeginPaint(hwnd, &ps);

            // All painting occurs here, between BeginPaint and EndPaint.
            FillRect(hdc, &ps.rcPaint, (HBRUSH) (COLOR_WINDOW+1));
            EndPaint(hwnd, &ps);
        }
        return 0;
    }

    return DefWindowProc(hwnd, uMsg, wParam, lParam);
}

```

<span data-ttu-id="27596-115">Exemple tiré d' [exemples classiques Windows](https://github.com/microsoft/Windows-classic-samples/blob/18cbd05ee44455cd7552804dcf2c9d6db619b412/Samples/Win7Samples/begin/LearnWin32/HelloWorld/cpp/main.cpp) sur GitHub.</span><span class="sxs-lookup"><span data-stu-id="27596-115">Example from [Windows Classic Samples](https://github.com/microsoft/Windows-classic-samples/blob/18cbd05ee44455cd7552804dcf2c9d6db619b412/Samples/Win7Samples/begin/LearnWin32/HelloWorld/cpp/main.cpp) on GitHub.</span></span>

## <a name="remarks"></a><span data-ttu-id="27596-116">Notes</span><span class="sxs-lookup"><span data-stu-id="27596-116">Remarks</span></span>

<span data-ttu-id="27596-117">Le message **WM \_ Paint** est généré par le système et ne doit pas être envoyé par une application.</span><span class="sxs-lookup"><span data-stu-id="27596-117">The **WM\_PAINT** message is generated by the system and should not be sent by an application.</span></span> <span data-ttu-id="27596-118">Pour forcer une fenêtre à dessiner dans un contexte de périphérique spécifique, utilisez le message WM [**\_ Print**](wm-print.md) ou [**WM \_ PRINTCLIENT**](wm-printclient.md) .</span><span class="sxs-lookup"><span data-stu-id="27596-118">To force a window to draw into a specific device context, use the [**WM\_PRINT**](wm-print.md) or [**WM\_PRINTCLIENT**](wm-printclient.md) message.</span></span> <span data-ttu-id="27596-119">Notez que cela nécessite que la fenêtre cible prenne en charge le message **WM \_ PRINTCLIENT** .</span><span class="sxs-lookup"><span data-stu-id="27596-119">Note that this requires the target window to support the **WM\_PRINTCLIENT** message.</span></span> <span data-ttu-id="27596-120">La plupart des contrôles courants prennent en charge le message **WM \_ PRINTCLIENT** .</span><span class="sxs-lookup"><span data-stu-id="27596-120">Most common controls support the **WM\_PRINTCLIENT** message.</span></span>

<span data-ttu-id="27596-121">La fonction [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)  valide la région de mise à jour.</span><span class="sxs-lookup"><span data-stu-id="27596-121">The [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)  function validates the update region.</span></span> <span data-ttu-id="27596-122">La fonction peut également envoyer le message [**WM \_ NCPAINT**](wm-ncpaint.md) à la procédure de fenêtre si le frame de fenêtre doit être peint et envoyer le message [**WM \_ ERASEBKGND**](../winmsg/wm-erasebkgnd.md) si l’arrière-plan de la fenêtre doit être effacé.</span><span class="sxs-lookup"><span data-stu-id="27596-122">The function may also send the [**WM\_NCPAINT**](wm-ncpaint.md) message to the window procedure if the window frame must be painted and send the [**WM\_ERASEBKGND**](../winmsg/wm-erasebkgnd.md) message if the window background must be erased.</span></span>

<span data-ttu-id="27596-123">Le système envoie ce message lorsqu’il n’y a pas d’autres messages dans la file d’attente des messages de l’application.</span><span class="sxs-lookup"><span data-stu-id="27596-123">The system sends this message when there are no other messages in the application's message queue.</span></span> <span data-ttu-id="27596-124">[**DispatchMessage**](/windows/win32/api/winuser/nf-winuser-dispatchmessage) détermine où envoyer le message. [**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage) détermine le message à distribuer.</span><span class="sxs-lookup"><span data-stu-id="27596-124">[**DispatchMessage**](/windows/win32/api/winuser/nf-winuser-dispatchmessage) determines where to send the message; [**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage) determines which message to dispatch.</span></span> <span data-ttu-id="27596-125">**GetMessage** retourne le message de **\_ peinture WM** lorsqu’il n’y a pas d’autres messages dans la file d’attente de messages de l’application, et **DispatchMessage** envoie le message à la procédure de fenêtre appropriée.</span><span class="sxs-lookup"><span data-stu-id="27596-125">**GetMessage** returns the **WM\_PAINT** message when there are no other messages in the application's message queue, and **DispatchMessage** sends the message to the appropriate window procedure.</span></span>

<span data-ttu-id="27596-126">Une fenêtre peut recevoir des messages de peinture internes suite à l’appel de [**RedrawWindow**](/windows/desktop/api/Winuser/nf-winuser-redrawwindow) avec l' \_ indicateur RDW INTERNALPAINT défini.</span><span class="sxs-lookup"><span data-stu-id="27596-126">A window may receive internal paint messages as a result of calling [**RedrawWindow**](/windows/desktop/api/Winuser/nf-winuser-redrawwindow) with the RDW\_INTERNALPAINT flag set.</span></span> <span data-ttu-id="27596-127">Dans ce cas, la fenêtre peut ne pas avoir de zone de mise à jour.</span><span class="sxs-lookup"><span data-stu-id="27596-127">In this case, the window may not have an update region.</span></span> <span data-ttu-id="27596-128">Une application peut appeler la fonction [**GetUpdateRect**](/windows/desktop/api/Winuser/nf-winuser-getupdaterect) pour déterminer si la fenêtre a une région de mise à jour.</span><span class="sxs-lookup"><span data-stu-id="27596-128">An application may call the [**GetUpdateRect**](/windows/desktop/api/Winuser/nf-winuser-getupdaterect) function to determine whether the window has an update region.</span></span> <span data-ttu-id="27596-129">Si **GetUpdateRect** retourne la valeur zéro, l’application n’a pas besoin d’appeler les fonctions [**BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint) et [**EndPaint**](/windows/desktop/api/Winuser/nf-winuser-endpaint) .</span><span class="sxs-lookup"><span data-stu-id="27596-129">If **GetUpdateRect** returns zero, the application need not call the [**BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint) and [**EndPaint**](/windows/desktop/api/Winuser/nf-winuser-endpaint) functions.</span></span>

<span data-ttu-id="27596-130">Une application doit vérifier s’il existe des peintures internes nécessaires en examinant ses structures de données internes pour chaque message **WM \_ Paint** , car un message **\_ WM** peut avoir été provoqué par une région de mise à jour non null et un appel à [**RedrawWindow**](/windows/desktop/api/Winuser/nf-winuser-redrawwindow) avec l' \_ indicateur RDW INTERNALPAINT défini.</span><span class="sxs-lookup"><span data-stu-id="27596-130">An application must check for any necessary internal painting by looking at its internal data structures for each **WM\_PAINT** message, because a **WM\_PAINT** message may have been caused by both a non-NULL update region and a call to [**RedrawWindow**](/windows/desktop/api/Winuser/nf-winuser-redrawwindow) with the RDW\_INTERNALPAINT flag set.</span></span>

<span data-ttu-id="27596-131">Le système envoie un message **de \_ peinture WM** interne une seule fois.</span><span class="sxs-lookup"><span data-stu-id="27596-131">The system sends an internal **WM\_PAINT** message only once.</span></span> <span data-ttu-id="27596-132">Après qu’un message de **\_ peinture WM** interne a été retourné à partir de [**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage) ou [**PeekMessage**](/windows/win32/api/winuser/nf-winuser-peekmessagea) ou qu’il est envoyé à une fenêtre par [**UpdateWindow**](/windows/desktop/api/Winuser/nf-winuser-updatewindow), le système ne publie pas ou n’envoie pas d’autres messages de **\_ peinture WM** tant que la fenêtre n’est pas invalidée ou jusqu’à ce que [**RedrawWindow**](/windows/desktop/api/Winuser/nf-winuser-redrawwindow) soit rappelé avec l' \_ indicateur RDW INTERNALPAINT défini.</span><span class="sxs-lookup"><span data-stu-id="27596-132">After an internal **WM\_PAINT** message is returned from [**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage) or [**PeekMessage**](/windows/win32/api/winuser/nf-winuser-peekmessagea) or is sent to a window by [**UpdateWindow**](/windows/desktop/api/Winuser/nf-winuser-updatewindow), the system does not post or send further **WM\_PAINT** messages until the window is invalidated or until [**RedrawWindow**](/windows/desktop/api/Winuser/nf-winuser-redrawwindow) is called again with the RDW\_INTERNALPAINT flag set.</span></span>

<span data-ttu-id="27596-133">Pour certains contrôles courants, le traitement du message de **\_ peinture WM** par défaut vérifie le paramètre *wParam* .</span><span class="sxs-lookup"><span data-stu-id="27596-133">For some common controls, the default **WM\_PAINT** message processing checks the *wParam* parameter.</span></span> <span data-ttu-id="27596-134">Si *wParam* est non null, le contrôle suppose que la valeur est un HDC et peint à l’aide de ce contexte de périphérique.</span><span class="sxs-lookup"><span data-stu-id="27596-134">If *wParam* is non-NULL, the control assumes that the value is an HDC and paints using that device context.</span></span>

## <a name="requirements"></a><span data-ttu-id="27596-135">Spécifications</span><span class="sxs-lookup"><span data-stu-id="27596-135">Requirements</span></span>



| <span data-ttu-id="27596-136">Condition requise</span><span class="sxs-lookup"><span data-stu-id="27596-136">Requirement</span></span> | <span data-ttu-id="27596-137">Valeur</span><span class="sxs-lookup"><span data-stu-id="27596-137">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="27596-138">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="27596-138">Minimum supported client</span></span><br/> | <span data-ttu-id="27596-139">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="27596-139">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="27596-140">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="27596-140">Minimum supported server</span></span><br/> | <span data-ttu-id="27596-141">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="27596-141">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="27596-142">En-tête</span><span class="sxs-lookup"><span data-stu-id="27596-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="27596-143"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="27596-143"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="27596-144">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="27596-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="27596-145">Vue d’ensemble de la peinture et du dessin</span><span class="sxs-lookup"><span data-stu-id="27596-145">Painting and Drawing Overview</span></span>](painting-and-drawing.md)
</dt> <dt>

[<span data-ttu-id="27596-146">Peinture et dessin de messages</span><span class="sxs-lookup"><span data-stu-id="27596-146">Painting and Drawing Messages</span></span>](painting-and-drawing-messages.md)
</dt> <dt>

[<span data-ttu-id="27596-147">**BeginPaint**</span><span class="sxs-lookup"><span data-stu-id="27596-147">**BeginPaint**</span></span>](/windows/desktop/api/Winuser/nf-winuser-beginpaint)
</dt> <dt>

[<span data-ttu-id="27596-148">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="27596-148">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[<span data-ttu-id="27596-149">**DispatchMessage**</span><span class="sxs-lookup"><span data-stu-id="27596-149">**DispatchMessage**</span></span>](/windows/win32/api/winuser/nf-winuser-dispatchmessage)
</dt> <dt>

[<span data-ttu-id="27596-150">**EndPaint**</span><span class="sxs-lookup"><span data-stu-id="27596-150">**EndPaint**</span></span>](/windows/desktop/api/Winuser/nf-winuser-endpaint)
</dt> <dt>

[<span data-ttu-id="27596-151">**GetMessage**</span><span class="sxs-lookup"><span data-stu-id="27596-151">**GetMessage**</span></span>](/windows/win32/api/winuser/nf-winuser-getmessage)
</dt> <dt>

[<span data-ttu-id="27596-152">**GetUpdateRect**</span><span class="sxs-lookup"><span data-stu-id="27596-152">**GetUpdateRect**</span></span>](/windows/desktop/api/Winuser/nf-winuser-getupdaterect)
</dt> <dt>

[<span data-ttu-id="27596-153">**PeekMessage**</span><span class="sxs-lookup"><span data-stu-id="27596-153">**PeekMessage**</span></span>](/windows/win32/api/winuser/nf-winuser-peekmessagea)
</dt> <dt>

[<span data-ttu-id="27596-154">**RedrawWindow**</span><span class="sxs-lookup"><span data-stu-id="27596-154">**RedrawWindow**</span></span>](/windows/desktop/api/Winuser/nf-winuser-redrawwindow)
</dt> <dt>

[<span data-ttu-id="27596-155">**UpdateWindow**</span><span class="sxs-lookup"><span data-stu-id="27596-155">**UpdateWindow**</span></span>](/windows/desktop/api/Winuser/nf-winuser-updatewindow)
</dt> <dt>

[<span data-ttu-id="27596-156">**\_ERASEBKGND WM**</span><span class="sxs-lookup"><span data-stu-id="27596-156">**WM\_ERASEBKGND**</span></span>](../winmsg/wm-erasebkgnd.md)
</dt> <dt>

[<span data-ttu-id="27596-157">**\_NCPAINT WM**</span><span class="sxs-lookup"><span data-stu-id="27596-157">**WM\_NCPAINT**</span></span>](wm-ncpaint.md)
</dt> <dt>

[<span data-ttu-id="27596-158">**\_impression WM**</span><span class="sxs-lookup"><span data-stu-id="27596-158">**WM\_PRINT**</span></span>](wm-print.md)
</dt> <dt>

[<span data-ttu-id="27596-159">**\_PRINTCLIENT WM**</span><span class="sxs-lookup"><span data-stu-id="27596-159">**WM\_PRINTCLIENT**</span></span>](wm-printclient.md)
</dt> </dl>

 

 
