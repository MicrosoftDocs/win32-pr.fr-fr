---
description: Publié dans la file d’attente de messages du thread d’installation lors de l’expiration d’un minuteur. Le message est publié par la fonction GetMessage ou PeekMessage.
ms.assetid: 419e3f05-35ec-4e48-b24d-ab98df687b20
title: Message WM_TIMER (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c7c99db67c9c9b3419e477ccd0a78133df453a7c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104209760"
---
# <a name="wm_timer-message"></a><span data-ttu-id="63530-104">\_Message du minuteur WM</span><span class="sxs-lookup"><span data-stu-id="63530-104">WM\_TIMER message</span></span>

<span data-ttu-id="63530-105">Publié dans la file d’attente de messages du thread d’installation lors de l’expiration d’un minuteur.</span><span class="sxs-lookup"><span data-stu-id="63530-105">Posted to the installing thread's message queue when a timer expires.</span></span> <span data-ttu-id="63530-106">Le message est publié par la fonction [**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage) ou [**PeekMessage**](/windows/win32/api/winuser/nf-winuser-peekmessagea) .</span><span class="sxs-lookup"><span data-stu-id="63530-106">The message is posted by the [**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage) or [**PeekMessage**](/windows/win32/api/winuser/nf-winuser-peekmessagea) function.</span></span>


```C++
#define WM_TIMER                        0x0113
```



## <a name="parameters"></a><span data-ttu-id="63530-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="63530-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="63530-108">*wParam* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="63530-108">*wParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="63530-109">Identificateur de la minuterie.</span><span class="sxs-lookup"><span data-stu-id="63530-109">The timer identifier.</span></span>

</dd> <dt>

<span data-ttu-id="63530-110">*lParam* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="63530-110">*lParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="63530-111">Pointeur vers une fonction de rappel définie par l’application qui a été passée à la fonction [**SetTimer**](/windows/win32/api/winuser/nf-winuser-settimer) lors de l’installation du minuteur.</span><span class="sxs-lookup"><span data-stu-id="63530-111">A pointer to an application-defined callback function that was passed to the [**SetTimer**](/windows/win32/api/winuser/nf-winuser-settimer) function when the timer was installed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="63530-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="63530-112">Return value</span></span>

<span data-ttu-id="63530-113">Type : **LRESULT**</span><span class="sxs-lookup"><span data-stu-id="63530-113">Type: **LRESULT**</span></span>

<span data-ttu-id="63530-114">Une application doit retourner zéro si elle traite ce message.</span><span class="sxs-lookup"><span data-stu-id="63530-114">An application should return zero if it processes this message.</span></span>

## <a name="remarks"></a><span data-ttu-id="63530-115">Notes</span><span class="sxs-lookup"><span data-stu-id="63530-115">Remarks</span></span>

<span data-ttu-id="63530-116">Vous pouvez traiter le message en fournissant un cas de **\_ minuterie WM** dans la procédure de fenêtre.</span><span class="sxs-lookup"><span data-stu-id="63530-116">You can process the message by providing a **WM\_TIMER** case in the window procedure.</span></span> <span data-ttu-id="63530-117">Sinon, [**DispatchMessage**](/windows/win32/api/winuser/nf-winuser-dispatchmessage) appellera la fonction de rappel [*TimerProc*](/windows/win32/api/winuser/nc-winuser-timerproc) spécifiée dans l’appel à la fonction [**SetTimer**](/windows/win32/api/winuser/nf-winuser-settimer) utilisée pour installer la minuterie.</span><span class="sxs-lookup"><span data-stu-id="63530-117">Otherwise, [**DispatchMessage**](/windows/win32/api/winuser/nf-winuser-dispatchmessage) will call the [*TimerProc*](/windows/win32/api/winuser/nc-winuser-timerproc) callback function specified in the call to the [**SetTimer**](/windows/win32/api/winuser/nf-winuser-settimer) function used to install the timer.</span></span>

<span data-ttu-id="63530-118">Le message du **\_ minuteur WM** est un message de priorité basse.</span><span class="sxs-lookup"><span data-stu-id="63530-118">The **WM\_TIMER** message is a low-priority message.</span></span> <span data-ttu-id="63530-119">Les fonctions [**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage) et [**PeekMessage**](/windows/win32/api/winuser/nf-winuser-peekmessagea) publient ce message uniquement lorsqu’aucun autre message de priorité plus élevée ne se trouve dans la file d’attente de messages du thread.</span><span class="sxs-lookup"><span data-stu-id="63530-119">The [**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage) and [**PeekMessage**](/windows/win32/api/winuser/nf-winuser-peekmessagea) functions post this message only when no other higher-priority messages are in the thread's message queue.</span></span>

## <a name="requirements"></a><span data-ttu-id="63530-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="63530-120">Requirements</span></span>



| <span data-ttu-id="63530-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="63530-121">Requirement</span></span> | <span data-ttu-id="63530-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="63530-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="63530-123">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="63530-123">Minimum supported client</span></span><br/> | <span data-ttu-id="63530-124">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="63530-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="63530-125">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="63530-125">Minimum supported server</span></span><br/> | <span data-ttu-id="63530-126">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="63530-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="63530-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="63530-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="63530-128"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="63530-128"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="63530-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="63530-129">See also</span></span>

<dl> <dt>

<span data-ttu-id="63530-130">**Référence**</span><span class="sxs-lookup"><span data-stu-id="63530-130">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="63530-131">**GetMessage**</span><span class="sxs-lookup"><span data-stu-id="63530-131">**GetMessage**</span></span>](/windows/win32/api/winuser/nf-winuser-getmessage)
</dt> <dt>

[<span data-ttu-id="63530-132">**PeekMessage**</span><span class="sxs-lookup"><span data-stu-id="63530-132">**PeekMessage**</span></span>](/windows/win32/api/winuser/nf-winuser-peekmessagea)
</dt> <dt>

[<span data-ttu-id="63530-133">**SetTimer**</span><span class="sxs-lookup"><span data-stu-id="63530-133">**SetTimer**</span></span>](/windows/win32/api/winuser/nf-winuser-settimer)
</dt> <dt>

[<span data-ttu-id="63530-134">**TimerProc**</span><span class="sxs-lookup"><span data-stu-id="63530-134">**TimerProc**</span></span>](/windows/win32/api/winuser/nc-winuser-timerproc)
</dt> <dt>

<span data-ttu-id="63530-135">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="63530-135">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="63530-136">Minuteurs</span><span class="sxs-lookup"><span data-stu-id="63530-136">Timers</span></span>](timers.md)
</dt> </dl>

 

 
