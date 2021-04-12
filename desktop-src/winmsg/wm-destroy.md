---
description: Envoyé lorsqu’une fenêtre est en cours de destruction. Il est envoyé à la procédure de fenêtre de la fenêtre qui est détruite après la suppression de la fenêtre de l’écran.
ms.assetid: 089c0645-199b-4a90-9cbc-740f0cf3267d
title: Message WM_DESTROY (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1db195c22c38759146fb76e98edf4ca7f605a1c1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104203798"
---
# <a name="wm_destroy-message"></a><span data-ttu-id="4e812-104">\_Message de destruction WM</span><span class="sxs-lookup"><span data-stu-id="4e812-104">WM\_DESTROY message</span></span>

<span data-ttu-id="4e812-105">Envoyé lorsqu’une fenêtre est en cours de destruction.</span><span class="sxs-lookup"><span data-stu-id="4e812-105">Sent when a window is being destroyed.</span></span> <span data-ttu-id="4e812-106">Il est envoyé à la procédure de fenêtre de la fenêtre qui est détruite après la suppression de la fenêtre de l’écran.</span><span class="sxs-lookup"><span data-stu-id="4e812-106">It is sent to the window procedure of the window being destroyed after the window is removed from the screen.</span></span>

<span data-ttu-id="4e812-107">Ce message est d’abord envoyé à la fenêtre en cours de destruction, puis aux fenêtres enfants (le cas échéant) à mesure qu’elles sont détruites.</span><span class="sxs-lookup"><span data-stu-id="4e812-107">This message is sent first to the window being destroyed and then to the child windows (if any) as they are destroyed.</span></span> <span data-ttu-id="4e812-108">Pendant le traitement du message, il peut être supposé que toutes les fenêtres enfants existent toujours.</span><span class="sxs-lookup"><span data-stu-id="4e812-108">During the processing of the message, it can be assumed that all child windows still exist.</span></span>

<span data-ttu-id="4e812-109">Une fenêtre reçoit ce message par le biais de sa fonction [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="4e812-109">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_DESTROY                      0x0002
```



## <a name="parameters"></a><span data-ttu-id="4e812-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4e812-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4e812-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="4e812-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4e812-112">Ce paramètre n'est pas utilisé.</span><span class="sxs-lookup"><span data-stu-id="4e812-112">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="4e812-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="4e812-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4e812-114">Ce paramètre n'est pas utilisé.</span><span class="sxs-lookup"><span data-stu-id="4e812-114">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4e812-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="4e812-115">Return value</span></span>

<span data-ttu-id="4e812-116">Type : **LRESULT**</span><span class="sxs-lookup"><span data-stu-id="4e812-116">Type: **LRESULT**</span></span>

<span data-ttu-id="4e812-117">Si une application traite ce message, elle doit retourner la valeur zéro.</span><span class="sxs-lookup"><span data-stu-id="4e812-117">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="4e812-118">Notes</span><span class="sxs-lookup"><span data-stu-id="4e812-118">Remarks</span></span>

<span data-ttu-id="4e812-119">Si la fenêtre en cours de destruction fait partie de la chaîne du presse-papiers (définie en appelant la fonction [**SetClipboardViewer**](/windows/win32/api/winuser/nf-winuser-setclipboardviewer) ), la fenêtre doit se supprimer de la chaîne en traitant la fonction [**ChangeClipboardChain**](/windows/win32/api/winuser/nf-winuser-changeclipboardchain) avant de retourner le message de **\_ destruction WM** .</span><span class="sxs-lookup"><span data-stu-id="4e812-119">If the window being destroyed is part of the clipboard viewer chain (set by calling the [**SetClipboardViewer**](/windows/win32/api/winuser/nf-winuser-setclipboardviewer) function), the window must remove itself from the chain by processing the [**ChangeClipboardChain**](/windows/win32/api/winuser/nf-winuser-changeclipboardchain) function before returning from the **WM\_DESTROY** message.</span></span>

## <a name="requirements"></a><span data-ttu-id="4e812-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4e812-120">Requirements</span></span>



| <span data-ttu-id="4e812-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4e812-121">Requirement</span></span> | <span data-ttu-id="4e812-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="4e812-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4e812-123">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4e812-123">Minimum supported client</span></span><br/> | <span data-ttu-id="4e812-124">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4e812-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="4e812-125">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4e812-125">Minimum supported server</span></span><br/> | <span data-ttu-id="4e812-126">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4e812-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="4e812-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="4e812-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="4e812-128"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4e812-128"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4e812-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4e812-129">See also</span></span>

<dl> <dt>

<span data-ttu-id="4e812-130">**Référence**</span><span class="sxs-lookup"><span data-stu-id="4e812-130">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="4e812-131">**ChangeClipboardChain**</span><span class="sxs-lookup"><span data-stu-id="4e812-131">**ChangeClipboardChain**</span></span>](/windows/win32/api/winuser/nf-winuser-changeclipboardchain)
</dt> <dt>

[<span data-ttu-id="4e812-132">**DestroyWindow**</span><span class="sxs-lookup"><span data-stu-id="4e812-132">**DestroyWindow**</span></span>](/windows/win32/api/winuser/nf-winuser-destroywindow)
</dt> <dt>

[<span data-ttu-id="4e812-133">**PostQuitMessage**</span><span class="sxs-lookup"><span data-stu-id="4e812-133">**PostQuitMessage**</span></span>](/windows/win32/api/winuser/nf-winuser-postquitmessage)
</dt> <dt>

[<span data-ttu-id="4e812-134">**SetClipboardViewer**</span><span class="sxs-lookup"><span data-stu-id="4e812-134">**SetClipboardViewer**</span></span>](/windows/win32/api/winuser/nf-winuser-setclipboardviewer)
</dt> <dt>

[<span data-ttu-id="4e812-135">**\_Fermer WM**</span><span class="sxs-lookup"><span data-stu-id="4e812-135">**WM\_CLOSE**</span></span>](wm-close.md)
</dt> <dt>

<span data-ttu-id="4e812-136">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="4e812-136">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="4e812-137">Windows</span><span class="sxs-lookup"><span data-stu-id="4e812-137">Windows</span></span>](windows.md)
</dt> </dl>

 

 
