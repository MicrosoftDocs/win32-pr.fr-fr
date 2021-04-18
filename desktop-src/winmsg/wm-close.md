---
Description: Envoyé en tant que signal qu’une fenêtre ou une application doit se terminer.
ms.assetid: 19500baf-e0ad-4dfa-804f-6a6e0652cffb
title: Message WM_CLOSE (winuser. h)
ms.topic: reference
ms.custom: snippet-project
ms.date: 05/31/2018
ms.openlocfilehash: 2f1403050cfd3c98ddf90df4399547158a583c50
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526532"
---
# <a name="wm_close-message"></a><span data-ttu-id="3aec8-103">\_Message de fermeture WM</span><span class="sxs-lookup"><span data-stu-id="3aec8-103">WM\_CLOSE message</span></span>

<span data-ttu-id="3aec8-104">Envoyé en tant que signal qu’une fenêtre ou une application doit se terminer.</span><span class="sxs-lookup"><span data-stu-id="3aec8-104">Sent as a signal that a window or an application should terminate.</span></span>

<span data-ttu-id="3aec8-105">Une fenêtre reçoit ce message par le biais de sa fonction [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="3aec8-105">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_CLOSE                        0x0010
```



## <a name="parameters"></a><span data-ttu-id="3aec8-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3aec8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3aec8-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="3aec8-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3aec8-108">Ce paramètre n'est pas utilisé.</span><span class="sxs-lookup"><span data-stu-id="3aec8-108">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="3aec8-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="3aec8-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3aec8-110">Ce paramètre n'est pas utilisé.</span><span class="sxs-lookup"><span data-stu-id="3aec8-110">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3aec8-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="3aec8-111">Return value</span></span>

<span data-ttu-id="3aec8-112">Type : **LRESULT**</span><span class="sxs-lookup"><span data-stu-id="3aec8-112">Type: **LRESULT**</span></span>

<span data-ttu-id="3aec8-113">Si une application traite ce message, elle doit retourner la valeur zéro.</span><span class="sxs-lookup"><span data-stu-id="3aec8-113">If an application processes this message, it should return zero.</span></span>

## <a name="example"></a><span data-ttu-id="3aec8-114">Exemple</span><span class="sxs-lookup"><span data-stu-id="3aec8-114">Example</span></span>

```cpp
LRESULT CALLBACK WindowProc(
    __in HWND hWindow,
    __in UINT uMsg,
    __in WPARAM wParam,
    __in LPARAM lParam)
{
    switch (uMsg)
    {
    case WM_CLOSE:
        DestroyWindow(hWindow);
        break;
    case WM_DESTROY:
        PostQuitMessage(0);
        break;
    default:
        return DefWindowProc(hWindow, uMsg, wParam, lParam);
    }

    return 0;
}
```
<span data-ttu-id="3aec8-115">Exemple tiré d' [exemples classiques Windows](https://github.com/microsoft/Windows-classic-samples/blob/1d363ff4bd17d8e20415b92e2ee989d615cc0d91/Samples/RadialController/cpp/RadialController.cpp) sur GitHub.</span><span class="sxs-lookup"><span data-stu-id="3aec8-115">Example from [Windows Classic Samples](https://github.com/microsoft/Windows-classic-samples/blob/1d363ff4bd17d8e20415b92e2ee989d615cc0d91/Samples/RadialController/cpp/RadialController.cpp) on GitHub.</span></span>


## <a name="remarks"></a><span data-ttu-id="3aec8-116">Notes</span><span class="sxs-lookup"><span data-stu-id="3aec8-116">Remarks</span></span>

<span data-ttu-id="3aec8-117">Une application peut inviter l’utilisateur à confirmer, avant de détruire une fenêtre, en traitant le message **WM \_ Close** et en appelant la fonction [**DestroyWindow**](/windows/win32/api/winuser/nf-winuser-destroywindow) uniquement si l’utilisateur confirme le choix.</span><span class="sxs-lookup"><span data-stu-id="3aec8-117">An application can prompt the user for confirmation, prior to destroying a window, by processing the **WM\_CLOSE** message and calling the [**DestroyWindow**](/windows/win32/api/winuser/nf-winuser-destroywindow) function only if the user confirms the choice.</span></span>

<span data-ttu-id="3aec8-118">Par défaut, la fonction [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) appelle la fonction [**DestroyWindow**](/windows/win32/api/winuser/nf-winuser-destroywindow) pour détruire la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="3aec8-118">By default, the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function calls the [**DestroyWindow**](/windows/win32/api/winuser/nf-winuser-destroywindow) function to destroy the window.</span></span>

## <a name="requirements"></a><span data-ttu-id="3aec8-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3aec8-119">Requirements</span></span>



| <span data-ttu-id="3aec8-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3aec8-120">Requirement</span></span> | <span data-ttu-id="3aec8-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="3aec8-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3aec8-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3aec8-122">Minimum supported client</span></span><br/> | <span data-ttu-id="3aec8-123">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3aec8-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="3aec8-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3aec8-124">Minimum supported server</span></span><br/> | <span data-ttu-id="3aec8-125">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3aec8-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="3aec8-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="3aec8-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="3aec8-127"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3aec8-127"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3aec8-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3aec8-128">See also</span></span>

<dl> <dt>

<span data-ttu-id="3aec8-129">**Référence**</span><span class="sxs-lookup"><span data-stu-id="3aec8-129">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="3aec8-130">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="3aec8-130">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[<span data-ttu-id="3aec8-131">**DestroyWindow**</span><span class="sxs-lookup"><span data-stu-id="3aec8-131">**DestroyWindow**</span></span>](/windows/win32/api/winuser/nf-winuser-destroywindow)
</dt> <dt>

<span data-ttu-id="3aec8-132">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="3aec8-132">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="3aec8-133">Windows</span><span class="sxs-lookup"><span data-stu-id="3aec8-133">Windows</span></span>](windows.md)
</dt> </dl>

 

 
