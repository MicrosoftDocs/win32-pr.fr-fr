---
description: Avertit une fenêtre que sa zone non cliente est en cours de destruction. La fonction DestroyWindow envoie le \_ message WM NCDESTROY à la fenêtre qui suit le \_ message WM Destroy.
ms.assetid: 64ab268d-0e90-4401-81d3-a4da64196001
title: Message WM_NCDESTROY (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a462f679a29f471638299e037749adaf32a85dea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103952060"
---
# <a name="wm_ncdestroy-message"></a><span data-ttu-id="0817d-104">\_Message WM NCDESTROY</span><span class="sxs-lookup"><span data-stu-id="0817d-104">WM\_NCDESTROY message</span></span>

<span data-ttu-id="0817d-105">Avertit une fenêtre que sa zone non cliente est en cours de destruction.</span><span class="sxs-lookup"><span data-stu-id="0817d-105">Notifies a window that its nonclient area is being destroyed.</span></span> <span data-ttu-id="0817d-106">La fonction [**DestroyWindow**](/windows/win32/api/winuser/nf-winuser-destroywindow) envoie le message **WM \_ NCDESTROY** à la fenêtre qui suit le message [**WM \_ Destroy**](wm-destroy.md) .[**WM \_ Destroy**](wm-destroy.md) est utilisé pour libérer l’objet mémoire alloué associé à la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="0817d-106">The [**DestroyWindow**](/windows/win32/api/winuser/nf-winuser-destroywindow) function sends the **WM\_NCDESTROY** message to the window following the [**WM\_DESTROY**](wm-destroy.md) message.[**WM\_DESTROY**](wm-destroy.md) is used to free the allocated memory object associated with the window.</span></span>

<span data-ttu-id="0817d-107">Le message **WM \_ NCDESTROY** est envoyé une fois que les fenêtres enfants ont été détruites.</span><span class="sxs-lookup"><span data-stu-id="0817d-107">The **WM\_NCDESTROY** message is sent after the child windows have been destroyed.</span></span> <span data-ttu-id="0817d-108">En revanche, [**WM \_ Destroy**](wm-destroy.md) est envoyé avant la destruction des fenêtres enfants.</span><span class="sxs-lookup"><span data-stu-id="0817d-108">In contrast, [**WM\_DESTROY**](wm-destroy.md) is sent before the child windows are destroyed.</span></span>

<span data-ttu-id="0817d-109">Une fenêtre reçoit ce message par le biais de sa fonction [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="0817d-109">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_NCDESTROY                    0x0082
```



## <a name="parameters"></a><span data-ttu-id="0817d-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0817d-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0817d-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="0817d-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0817d-112">Ce paramètre n'est pas utilisé.</span><span class="sxs-lookup"><span data-stu-id="0817d-112">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="0817d-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="0817d-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0817d-114">Ce paramètre n'est pas utilisé.</span><span class="sxs-lookup"><span data-stu-id="0817d-114">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0817d-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="0817d-115">Return value</span></span>

<span data-ttu-id="0817d-116">Type : **LRESULT**</span><span class="sxs-lookup"><span data-stu-id="0817d-116">Type: **LRESULT**</span></span>

<span data-ttu-id="0817d-117">Si une application traite ce message, elle doit retourner la valeur zéro.</span><span class="sxs-lookup"><span data-stu-id="0817d-117">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="0817d-118">Notes</span><span class="sxs-lookup"><span data-stu-id="0817d-118">Remarks</span></span>

<span data-ttu-id="0817d-119">Ce message libère toute mémoire allouée de façon interne à la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="0817d-119">This message frees any memory internally allocated for the window.</span></span>

## <a name="requirements"></a><span data-ttu-id="0817d-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0817d-120">Requirements</span></span>



| <span data-ttu-id="0817d-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0817d-121">Requirement</span></span> | <span data-ttu-id="0817d-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="0817d-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0817d-123">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0817d-123">Minimum supported client</span></span><br/> | <span data-ttu-id="0817d-124">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0817d-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="0817d-125">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0817d-125">Minimum supported server</span></span><br/> | <span data-ttu-id="0817d-126">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0817d-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="0817d-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="0817d-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="0817d-128"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0817d-128"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0817d-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0817d-129">See also</span></span>

<dl> <dt>

<span data-ttu-id="0817d-130">**Référence**</span><span class="sxs-lookup"><span data-stu-id="0817d-130">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="0817d-131">**DestroyWindow**</span><span class="sxs-lookup"><span data-stu-id="0817d-131">**DestroyWindow**</span></span>](/windows/win32/api/winuser/nf-winuser-destroywindow)
</dt> <dt>

[<span data-ttu-id="0817d-132">**\_destructeur WM**</span><span class="sxs-lookup"><span data-stu-id="0817d-132">**WM\_DESTROY**</span></span>](wm-destroy.md)
</dt> <dt>

[<span data-ttu-id="0817d-133">**\_NCCREATE WM**</span><span class="sxs-lookup"><span data-stu-id="0817d-133">**WM\_NCCREATE**</span></span>](wm-nccreate.md)
</dt> <dt>

<span data-ttu-id="0817d-134">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="0817d-134">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="0817d-135">Windows</span><span class="sxs-lookup"><span data-stu-id="0817d-135">Windows</span></span>](windows.md)
</dt> </dl>

 

 
