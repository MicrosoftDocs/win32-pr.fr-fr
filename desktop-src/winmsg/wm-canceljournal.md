---
description: Publié dans une application lorsqu’un utilisateur annule les activités de journalisation de l’application. Le message est publié avec un handle de fenêtre NULL.
ms.assetid: 7515acb5-4526-40f7-abb7-822a073ac7dc
title: Message WM_CANCELJOURNAL (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3a5676472d12c8cef2a03e508eca6bb742596a36
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106530624"
---
# <a name="wm_canceljournal-message"></a><span data-ttu-id="5b5aa-104">\_Message WM CANCELJOURNAL</span><span class="sxs-lookup"><span data-stu-id="5b5aa-104">WM\_CANCELJOURNAL message</span></span>

<span data-ttu-id="5b5aa-105">Publié dans une application lorsqu’un utilisateur annule les activités de journalisation de l’application.</span><span class="sxs-lookup"><span data-stu-id="5b5aa-105">Posted to an application when a user cancels the application's journaling activities.</span></span> <span data-ttu-id="5b5aa-106">Le message est publié avec un handle de fenêtre **null** .</span><span class="sxs-lookup"><span data-stu-id="5b5aa-106">The message is posted with a **NULL** window handle.</span></span>


```C++
#define WM_CANCELJOURNAL                0x004B
```



## <a name="parameters"></a><span data-ttu-id="5b5aa-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5b5aa-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5b5aa-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="5b5aa-108">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5b5aa-109">Ce paramètre n'est pas utilisé.</span><span class="sxs-lookup"><span data-stu-id="5b5aa-109">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="5b5aa-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="5b5aa-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5b5aa-111">Ce paramètre n'est pas utilisé.</span><span class="sxs-lookup"><span data-stu-id="5b5aa-111">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5b5aa-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="5b5aa-112">Return value</span></span>

<span data-ttu-id="5b5aa-113">Type : **void**</span><span class="sxs-lookup"><span data-stu-id="5b5aa-113">Type: **void**</span></span>

<span data-ttu-id="5b5aa-114">Ce message ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="5b5aa-114">This message does not return a value.</span></span> <span data-ttu-id="5b5aa-115">Il est destiné à être traité à partir de la boucle principale d’une application ou d’une procédure de hook [**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage) , et non à partir d’une procédure de fenêtre.</span><span class="sxs-lookup"><span data-stu-id="5b5aa-115">It is meant to be processed from within an application's main loop or a [**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage) hook procedure, not from a window procedure.</span></span>

## <a name="remarks"></a><span data-ttu-id="5b5aa-116">Notes</span><span class="sxs-lookup"><span data-stu-id="5b5aa-116">Remarks</span></span>

<span data-ttu-id="5b5aa-117">L’enregistrement de journal et les modes de lecture sont des modes imposés sur le système qui permettent à une application d’enregistrer ou de lire des entrées d’utilisateur de manière séquentielle.</span><span class="sxs-lookup"><span data-stu-id="5b5aa-117">Journal record and playback modes are modes imposed on the system that let an application sequentially record or play back user input.</span></span> <span data-ttu-id="5b5aa-118">Le système passe à ces modes lorsqu’une application installe une procédure de hook [*JournalRecordProc*](/previous-versions/windows/desktop/legacy/ms644983(v=vs.85)) ou [*JournalPlaybackProc*](/previous-versions/windows/desktop/legacy/ms644982(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="5b5aa-118">The system enters these modes when an application installs a [*JournalRecordProc*](/previous-versions/windows/desktop/legacy/ms644983(v=vs.85)) or [*JournalPlaybackProc*](/previous-versions/windows/desktop/legacy/ms644982(v=vs.85)) hook procedure.</span></span> <span data-ttu-id="5b5aa-119">Lorsque le système se trouve dans l’un de ces modes de journalisation, les applications doivent mettre en lecture les entrées de la file d’attente d’entrée.</span><span class="sxs-lookup"><span data-stu-id="5b5aa-119">When the system is in either of these journaling modes, applications must take turns reading input from the input queue.</span></span> <span data-ttu-id="5b5aa-120">Si une application cesse de lire l’entrée alors que le système est en mode de journalisation, les autres applications sont forcées à attendre.</span><span class="sxs-lookup"><span data-stu-id="5b5aa-120">If any one application stops reading input while the system is in a journaling mode, other applications are forced to wait.</span></span>

<span data-ttu-id="5b5aa-121">Pour garantir un système robuste, qui ne peut pas être rendu non réactif par une application, le système annule automatiquement les activités de journalisation lorsqu’un utilisateur appuie sur CTRL + ECHAP ou CTRL + ALT + SUPPR.</span><span class="sxs-lookup"><span data-stu-id="5b5aa-121">To ensure a robust system, one that cannot be made unresponsive by any one application, the system automatically cancels any journaling activities when a user presses CTRL+ESC or CTRL+ALT+DEL.</span></span> <span data-ttu-id="5b5aa-122">Le système décroche ensuite les procédures de hook de journalisation et publie un message **WM \_ CANCELJOURNAL** , avec un handle de fenêtre **null** , à l’application qui définit le hook de journalisation.</span><span class="sxs-lookup"><span data-stu-id="5b5aa-122">The system then unhooks any journaling hook procedures, and posts a **WM\_CANCELJOURNAL** message, with a **NULL** window handle, to the application that set the journaling hook.</span></span>

<span data-ttu-id="5b5aa-123">Le message **WM \_ CANCELJOURNAL** a un handle de fenêtre **null** , il ne peut donc pas être distribué à une procédure de fenêtre.</span><span class="sxs-lookup"><span data-stu-id="5b5aa-123">The **WM\_CANCELJOURNAL** message has a **NULL** window handle, therefore it cannot be dispatched to a window procedure.</span></span> <span data-ttu-id="5b5aa-124">Il existe deux façons pour une application de voir un **message WM \_ CANCELJOURNAL** : si l’application s’exécute dans sa propre boucle principale, elle doit intercepter le message entre son appel à [**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage) ou [**PeekMessage**](/windows/win32/api/winuser/nf-winuser-peekmessagea) et son appel à [**DispatchMessage**](/windows/win32/api/winuser/nf-winuser-dispatchmessage).</span><span class="sxs-lookup"><span data-stu-id="5b5aa-124">There are two ways for an application to see a **WM\_CANCELJOURNAL** message: If the application is running in its own main loop, it must catch the message between its call to [**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage) or [**PeekMessage**](/windows/win32/api/winuser/nf-winuser-peekmessagea) and its call to [**DispatchMessage**](/windows/win32/api/winuser/nf-winuser-dispatchmessage).</span></span> <span data-ttu-id="5b5aa-125">Si l’application ne s’exécute pas dans sa propre boucle principale, elle doit définir une procédure de hook [*GetMsgProc*](/previous-versions/windows/desktop/legacy/ms644981(v=vs.85)) (à l’aide d’un appel à [**SetWindowsHookEx**](/windows/win32/api/winuser/nf-winuser-setwindowshookexa) en spécifiant le type de hook **BL \_ GETMESSAGE** ) qui surveille le message.</span><span class="sxs-lookup"><span data-stu-id="5b5aa-125">If the application is not running in its own main loop, it must set a [*GetMsgProc*](/previous-versions/windows/desktop/legacy/ms644981(v=vs.85)) hook procedure (through a call to [**SetWindowsHookEx**](/windows/win32/api/winuser/nf-winuser-setwindowshookexa) specifying the **WH\_GETMESSAGE** hook type) that watches for the message.</span></span>

<span data-ttu-id="5b5aa-126">Lorsqu’une application voit un message **WM \_ CANCELJOURNAL** , elle peut supposer deux choses : l’utilisateur a annulé intentionnellement l’enregistrement du journal ou le mode de lecture, et le système a déjà décroché un enregistrement de journal ou des procédures de hook de lecture.</span><span class="sxs-lookup"><span data-stu-id="5b5aa-126">When an application sees a **WM\_CANCELJOURNAL** message, it can assume two things: the user has intentionally canceled the journal record or playback mode, and the system has already unhooked any journal record or playback hook procedures.</span></span>

<span data-ttu-id="5b5aa-127">Notez que les combinaisons de touches mentionnées ci-dessus (CTRL + ESC ou CTRL + ALT + SUPPR) provoquent l’annulation de la journalisation par le système.</span><span class="sxs-lookup"><span data-stu-id="5b5aa-127">Note that the key combinations mentioned above (CTRL+ESC or CTRL+ALT+DEL) cause the system to cancel journaling.</span></span> <span data-ttu-id="5b5aa-128">Si une application ne répond pas, elle donne à l’utilisateur un moyen de récupération.</span><span class="sxs-lookup"><span data-stu-id="5b5aa-128">If any one application is made unresponsive, they give the user a means of recovery.</span></span> <span data-ttu-id="5b5aa-129">Le code de la touche virtuelle [**VK \_ Cancel**](../inputdev/virtual-key-codes.md) (généralement implémentée en tant que combinaison de touches CTRL + ATTN) est ce qu’une application qui est en mode d’enregistrement journal doit surveiller comme signal indiquant que l’utilisateur souhaite annuler l’activité de journalisation.</span><span class="sxs-lookup"><span data-stu-id="5b5aa-129">The [**VK\_CANCEL**](../inputdev/virtual-key-codes.md) virtual key code (usually implemented as the CTRL+BREAK key combination) is what an application that is in journal record mode should watch for as a signal that the user wishes to cancel the journaling activity.</span></span> <span data-ttu-id="5b5aa-130">La différence réside dans le fait que la surveillance de **VK \_ Cancel** est un comportement suggéré pour la journalisation des applications, tandis que CTRL + ESC ou Ctrl + Alt + Suppr oblige le système à annuler la journalisation quel que soit le comportement de l’application de journalisation.</span><span class="sxs-lookup"><span data-stu-id="5b5aa-130">The difference is that watching for **VK\_CANCEL** is a suggested behavior for journaling applications, whereas CTRL+ESC or CTRL+ALT+DEL cause the system to cancel journaling regardless of a journaling application's behavior.</span></span>

## <a name="requirements"></a><span data-ttu-id="5b5aa-131">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5b5aa-131">Requirements</span></span>



| <span data-ttu-id="5b5aa-132">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5b5aa-132">Requirement</span></span> | <span data-ttu-id="5b5aa-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="5b5aa-133">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5b5aa-134">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5b5aa-134">Minimum supported client</span></span><br/> | <span data-ttu-id="5b5aa-135">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5b5aa-135">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="5b5aa-136">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5b5aa-136">Minimum supported server</span></span><br/> | <span data-ttu-id="5b5aa-137">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5b5aa-137">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="5b5aa-138">En-tête</span><span class="sxs-lookup"><span data-stu-id="5b5aa-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="5b5aa-139"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5b5aa-139"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5b5aa-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5b5aa-140">See also</span></span>

<dl> <dt>

<span data-ttu-id="5b5aa-141">**Référence**</span><span class="sxs-lookup"><span data-stu-id="5b5aa-141">**Reference**</span></span>
</dt> <dt>

<span data-ttu-id="5b5aa-142">[*JournalPlaybackProc*](/previous-versions/windows/desktop/legacy/ms644982(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="5b5aa-142">[*JournalPlaybackProc*](/previous-versions/windows/desktop/legacy/ms644982(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="5b5aa-143">[*JournalRecordProc*](/previous-versions/windows/desktop/legacy/ms644983(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="5b5aa-143">[*JournalRecordProc*](/previous-versions/windows/desktop/legacy/ms644983(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="5b5aa-144">[*GetMsgProc*](/previous-versions/windows/desktop/legacy/ms644981(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="5b5aa-144">[*GetMsgProc*](/previous-versions/windows/desktop/legacy/ms644981(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="5b5aa-145">**SetWindowsHookEx**</span><span class="sxs-lookup"><span data-stu-id="5b5aa-145">**SetWindowsHookEx**</span></span>](/windows/win32/api/winuser/nf-winuser-setwindowshookexa)
</dt> <dt>

<span data-ttu-id="5b5aa-146">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="5b5aa-146">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="5b5aa-147">Hooks</span><span class="sxs-lookup"><span data-stu-id="5b5aa-147">Hooks</span></span>](hooks.md)
</dt> </dl>

 

 
