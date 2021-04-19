---
Description: Envoyé à une fenêtre après la modification de sa taille.
ms.assetid: e3e14dcd-9236-48bd-a692-6985d8146f81
title: Message WM_SIZE (winuser. h)
ms.topic: reference
ms.custom: snippet-project
ms.date: 07/27/2020
ms.openlocfilehash: 04afafd3faafc4ea8c400472254dcf4ec4afa050
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106533258"
---
# <a name="wm_size-message"></a><span data-ttu-id="e7349-103">\_Message de taille WM</span><span class="sxs-lookup"><span data-stu-id="e7349-103">WM\_SIZE message</span></span>

<span data-ttu-id="e7349-104">Envoyé à une fenêtre après la modification de sa taille.</span><span class="sxs-lookup"><span data-stu-id="e7349-104">Sent to a window after its size has changed.</span></span>

<span data-ttu-id="e7349-105">Une fenêtre reçoit ce message par le biais de sa fonction [**WindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca) .</span><span class="sxs-lookup"><span data-stu-id="e7349-105">A window receives this message through its [**WindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca) function.</span></span>


```C++
#define WM_SIZE                         0x0005
```



## <a name="parameters"></a><span data-ttu-id="e7349-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e7349-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e7349-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="e7349-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e7349-108">Type de redimensionnement demandé.</span><span class="sxs-lookup"><span data-stu-id="e7349-108">The type of resizing requested.</span></span> <span data-ttu-id="e7349-109">Ce paramètre peut prendre les valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="e7349-109">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="e7349-110">Valeur</span><span class="sxs-lookup"><span data-stu-id="e7349-110">Value</span></span>                                                                                                                                                                                                                   | <span data-ttu-id="e7349-111">Signification</span><span class="sxs-lookup"><span data-stu-id="e7349-111">Meaning</span></span>                                                                                                            |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| <span id="SIZE_MAXHIDE"></span><span id="size_maxhide"></span><dl> <span data-ttu-id="e7349-112"><dt>**Taille \_ MAXHIDE**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="e7349-112"><dt>**SIZE\_MAXHIDE**</dt> <dt>4</dt></span></span> </dl>       | <span data-ttu-id="e7349-113">Le message est envoyé à toutes les fenêtres indépendantes lorsqu’une autre fenêtre est agrandie.</span><span class="sxs-lookup"><span data-stu-id="e7349-113">Message is sent to all pop-up windows when some other window is maximized.</span></span><br/>                              |
| <span id="SIZE_MAXIMIZED"></span><span id="size_maximized"></span><dl> <span data-ttu-id="e7349-114"><dt>**Taille \_ AGRANDIe**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="e7349-114"><dt>**SIZE\_MAXIMIZED**</dt> <dt>2</dt></span></span> </dl> | <span data-ttu-id="e7349-115">La fenêtre a été agrandie.</span><span class="sxs-lookup"><span data-stu-id="e7349-115">The window has been maximized.</span></span><br/>                                                                          |
| <span id="SIZE_MAXSHOW"></span><span id="size_maxshow"></span><dl> <span data-ttu-id="e7349-116"><dt>**Taille \_ MAXSHOW**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="e7349-116"><dt>**SIZE\_MAXSHOW**</dt> <dt>3</dt></span></span> </dl>       | <span data-ttu-id="e7349-117">Le message est envoyé à toutes les fenêtres indépendantes quand une autre fenêtre a été restaurée à sa taille précédente.</span><span class="sxs-lookup"><span data-stu-id="e7349-117">Message is sent to all pop-up windows when some other window has been restored to its former size.</span></span><br/>      |
| <span id="SIZE_MINIMIZED"></span><span id="size_minimized"></span><dl> <span data-ttu-id="e7349-118"><dt>**Taille \_ RÉDUIT**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="e7349-118"><dt>**SIZE\_MINIMIZED**</dt> <dt>1</dt></span></span> </dl> | <span data-ttu-id="e7349-119">La fenêtre a été réduite.</span><span class="sxs-lookup"><span data-stu-id="e7349-119">The window has been minimized.</span></span><br/>                                                                          |
| <span id="SIZE_RESTORED"></span><span id="size_restored"></span><dl> <span data-ttu-id="e7349-120"><dt>**Taille \_ RESTAURÉ**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="e7349-120"><dt>**SIZE\_RESTORED**</dt> <dt>0</dt></span></span> </dl>    | <span data-ttu-id="e7349-121">La fenêtre a été redimensionnée, mais ni la **taille \_ réduite** ni la **valeur \_ agrandie** à la taille ne s’appliquent.</span><span class="sxs-lookup"><span data-stu-id="e7349-121">The window has been resized, but neither the **SIZE\_MINIMIZED** nor **SIZE\_MAXIMIZED** value applies.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="e7349-122">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e7349-122">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e7349-123">Le mot de poids faible de *lParam* spécifie la nouvelle largeur de la zone cliente.</span><span class="sxs-lookup"><span data-stu-id="e7349-123">The low-order word of *lParam* specifies the new width of the client area.</span></span>

<span data-ttu-id="e7349-124">Le mot de poids fort de *lParam* spécifie la nouvelle hauteur de la zone cliente.</span><span class="sxs-lookup"><span data-stu-id="e7349-124">The high-order word of *lParam* specifies the new height of the client area.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e7349-125">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="e7349-125">Return value</span></span>

<span data-ttu-id="e7349-126">Type : **LRESULT**</span><span class="sxs-lookup"><span data-stu-id="e7349-126">Type: **LRESULT**</span></span>

<span data-ttu-id="e7349-127">Si une application traite ce message, elle doit retourner la valeur zéro.</span><span class="sxs-lookup"><span data-stu-id="e7349-127">If an application processes this message, it should return zero.</span></span>

## <a name="example"></a><span data-ttu-id="e7349-128">Exemple</span><span class="sxs-lookup"><span data-stu-id="e7349-128">Example</span></span>

```cpp
/******************************************************************
*                                                                 *
*  SimpleText::OnResize                                           *
*                                                                 *
*  If the application receives a WM_SIZE message, this method     *
*  resize the render target appropriately.                        *
*                                                                 *
******************************************************************/

void SimpleText::OnResize(UINT width, UINT height)
{
    if (pRT_)
    {
        D2D1_SIZE_U size;
        size.width = width;
        size.height = height;
        pRT_->Resize(size);
    }
}

LRESULT CALLBACK SimpleText::WndProc(HWND hwnd, UINT message, WPARAM wParam, LPARAM lParam)
{
   
    SimpleText *pSimpleText = reinterpret_cast<SimpleText *>(
                ::GetWindowLongPtr(hwnd, GWLP_USERDATA));

    if (pSimpleText)
    {
        switch(message)
        {
        case WM_SIZE:
            {
                UINT width = LOWORD(lParam);
                UINT height = HIWORD(lParam);
                pSimpleText->OnResize(width, height);
            }
            return 0;

// ...

```

<span data-ttu-id="e7349-129">Exemple tiré d' [exemples classiques Windows](https://github.com/microsoft/Windows-classic-samples/blob/1d363ff4bd17d8e20415b92e2ee989d615cc0d91/Samples/Win7Samples/multimedia/DirectWrite/HelloWorld/SimpleText.cpp) sur GitHub.</span><span class="sxs-lookup"><span data-stu-id="e7349-129">Example from [Windows classic samples](https://github.com/microsoft/Windows-classic-samples/blob/1d363ff4bd17d8e20415b92e2ee989d615cc0d91/Samples/Win7Samples/multimedia/DirectWrite/HelloWorld/SimpleText.cpp) on GitHub.</span></span>

## <a name="remarks"></a><span data-ttu-id="e7349-130">Notes</span><span class="sxs-lookup"><span data-stu-id="e7349-130">Remarks</span></span>

<span data-ttu-id="e7349-131">Si la fonction [**SetScrollPos**](https://msdn.microsoft.com/library/Cc411085(v=MSDN.10).aspx) ou [**MoveWindow**](/windows/win32/api/winuser/nf-winuser-movewindow) est appelée pour une fenêtre enfant à la suite du message **de \_ taille WM** , le paramètre *bRedraw* ou *bRepaint* doit être différent de zéro pour provoquer la redessination de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="e7349-131">If the [**SetScrollPos**](https://msdn.microsoft.com/library/Cc411085(v=MSDN.10).aspx) or [**MoveWindow**](/windows/win32/api/winuser/nf-winuser-movewindow) function is called for a child window as a result of the **WM\_SIZE** message, the *bRedraw* or *bRepaint* parameter should be nonzero to cause the window to be repainted.</span></span>

<span data-ttu-id="e7349-132">Bien que la largeur et la hauteur d’une fenêtre soient des valeurs 32 bits, le paramètre *lParam* contient uniquement les 16 bits de poids faible de chacun.</span><span class="sxs-lookup"><span data-stu-id="e7349-132">Although the width and height of a window are 32-bit values, the *lParam* parameter contains only the low-order 16 bits of each.</span></span>

<span data-ttu-id="e7349-133">La fonction [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) envoie les messages de **\_ taille WM** et de **\_ déplacement WM** quand elle traite le message [**WM \_ WINDOWPOSCHANGED**](wm-windowposchanged.md) .</span><span class="sxs-lookup"><span data-stu-id="e7349-133">The [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function sends the **WM\_SIZE** and **WM\_MOVE** messages when it processes the [**WM\_WINDOWPOSCHANGED**](wm-windowposchanged.md) message.</span></span>
<span data-ttu-id="e7349-134">Les messages de **\_ taille WM** et de **\_ déplacement WM** ne sont pas envoyés si une application gère le message **WM \_ WINDOWPOSCHANGED** sans appeler **DefWindowProc**.</span><span class="sxs-lookup"><span data-stu-id="e7349-134">The **WM\_SIZE** and **WM\_MOVE** messages are not sent if an application handles the **WM\_WINDOWPOSCHANGED** message without calling **DefWindowProc**.</span></span>

## <a name="requirements"></a><span data-ttu-id="e7349-135">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e7349-135">Requirements</span></span>



| <span data-ttu-id="e7349-136">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e7349-136">Requirement</span></span> | <span data-ttu-id="e7349-137">Valeur</span><span class="sxs-lookup"><span data-stu-id="e7349-137">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e7349-138">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e7349-138">Minimum supported client</span></span><br/> | <span data-ttu-id="e7349-139">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e7349-139">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="e7349-140">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e7349-140">Minimum supported server</span></span><br/> | <span data-ttu-id="e7349-141">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e7349-141">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="e7349-142">En-tête</span><span class="sxs-lookup"><span data-stu-id="e7349-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="e7349-143"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e7349-143"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e7349-144">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e7349-144">See also</span></span>

<dl> <dt>

<span data-ttu-id="e7349-145">**Référence**</span><span class="sxs-lookup"><span data-stu-id="e7349-145">**Reference**</span></span>
</dt> <dt>

<span data-ttu-id="e7349-146">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="e7349-146">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="e7349-147">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="e7349-147">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="e7349-148">**MoveWindow**</span><span class="sxs-lookup"><span data-stu-id="e7349-148">**MoveWindow**</span></span>](/windows/win32/api/winuser/nf-winuser-movewindow)
</dt> <dt>

[<span data-ttu-id="e7349-149">**\_WINDOWPOSCHANGED WM**</span><span class="sxs-lookup"><span data-stu-id="e7349-149">**WM\_WINDOWPOSCHANGED**</span></span>](wm-windowposchanged.md)
</dt> <dt>

<span data-ttu-id="e7349-150">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="e7349-150">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="e7349-151">Windows</span><span class="sxs-lookup"><span data-stu-id="e7349-151">Windows</span></span>](windows.md)
</dt> <dt>

<span data-ttu-id="e7349-152">**Autres ressources**</span><span class="sxs-lookup"><span data-stu-id="e7349-152">**Other Resources**</span></span>
</dt> <dt>

<span data-ttu-id="e7349-153">[**SetScrollPos**](https://msdn.microsoft.com/library/Cc411085(v=MSDN.10).aspx)</span><span class="sxs-lookup"><span data-stu-id="e7349-153">[**SetScrollPos**](https://msdn.microsoft.com/library/Cc411085(v=MSDN.10).aspx)</span></span>
</dt> </dl>

 

 
