---
description: Envoyé par une application de formation basée sur ordinateur (FAO) pour séparer les messages d’entrée utilisateur des autres messages envoyés via la \_ procédure JOURNALPLAYBACK.
ms.assetid: 9ac265be-1fcc-476f-9dee-3e961340b5a1
title: Message WM_QUEUESYNC (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 06d859f858ab7cf8182282cc20dbf514cfc2d9b4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106524664"
---
# <a name="wm_queuesync-message"></a><span data-ttu-id="4268b-103">\_Message WM QUEUESYNC</span><span class="sxs-lookup"><span data-stu-id="4268b-103">WM\_QUEUESYNC message</span></span>

<span data-ttu-id="4268b-104">Envoyé par une application de formation basée sur ordinateur (FAO) pour séparer les messages d’entrée utilisateur des autres messages envoyés via la procédure [**\_ JOURNALPLAYBACK**](about-hooks.md) .</span><span class="sxs-lookup"><span data-stu-id="4268b-104">Sent by a computer-based training (CBT) application to separate user-input messages from other messages sent through the [**WH\_JOURNALPLAYBACK**](about-hooks.md) procedure.</span></span>


```C++
#define WM_QUEUESYNC                    0x0023
```



## <a name="parameters"></a><span data-ttu-id="4268b-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4268b-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4268b-106">*wParam*</span><span class="sxs-lookup"><span data-stu-id="4268b-106">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4268b-107">Ce paramètre n'est pas utilisé.</span><span class="sxs-lookup"><span data-stu-id="4268b-107">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="4268b-108">*lParam*</span><span class="sxs-lookup"><span data-stu-id="4268b-108">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4268b-109">Ce paramètre n'est pas utilisé.</span><span class="sxs-lookup"><span data-stu-id="4268b-109">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4268b-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="4268b-110">Return value</span></span>

<span data-ttu-id="4268b-111">Type : **void**</span><span class="sxs-lookup"><span data-stu-id="4268b-111">Type: **void**</span></span>

<span data-ttu-id="4268b-112">Une application CBT doit retourner zéro si elle traite ce message.</span><span class="sxs-lookup"><span data-stu-id="4268b-112">A CBT application should return zero if it processes this message.</span></span>

## <a name="remarks"></a><span data-ttu-id="4268b-113">Notes</span><span class="sxs-lookup"><span data-stu-id="4268b-113">Remarks</span></span>

<span data-ttu-id="4268b-114">Chaque fois qu’une application CBT utilise la procédure [**\_ JOURNALPLAYBACK**](about-hooks.md) , les premier et dernier messages sont **WM \_ QUEUESYNC**.</span><span class="sxs-lookup"><span data-stu-id="4268b-114">Whenever a CBT application uses the [**WH\_JOURNALPLAYBACK**](about-hooks.md) procedure, the first and last messages are **WM\_QUEUESYNC**.</span></span> <span data-ttu-id="4268b-115">Cela permet à l’application CBT d’intercepter et d’examiner les messages initiés par l’utilisateur sans le faire pour les événements qu’elle envoie.</span><span class="sxs-lookup"><span data-stu-id="4268b-115">This allows the CBT application to intercept and examine user-initiated messages without doing so for events that it sends.</span></span>

<span data-ttu-id="4268b-116">Si une application spécifie un handle de fenêtre **null** , le message est publié dans la file d’attente de messages de la fenêtre active.</span><span class="sxs-lookup"><span data-stu-id="4268b-116">If an application specifies a **NULL** window handle, the message is posted to the message queue of the active window.</span></span>

## <a name="requirements"></a><span data-ttu-id="4268b-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4268b-117">Requirements</span></span>



| <span data-ttu-id="4268b-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4268b-118">Requirement</span></span> | <span data-ttu-id="4268b-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="4268b-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4268b-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4268b-120">Minimum supported client</span></span><br/> | <span data-ttu-id="4268b-121">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4268b-121">Windows XP \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="4268b-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4268b-122">Minimum supported server</span></span><br/> | <span data-ttu-id="4268b-123">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4268b-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="4268b-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="4268b-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="4268b-125"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4268b-125"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4268b-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4268b-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="4268b-127">**Référence**</span><span class="sxs-lookup"><span data-stu-id="4268b-127">**Reference**</span></span>
</dt> <dt>

<span data-ttu-id="4268b-128">[*JournalPlaybackProc*](/previous-versions/windows/desktop/legacy/ms644982(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="4268b-128">[*JournalPlaybackProc*](/previous-versions/windows/desktop/legacy/ms644982(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="4268b-129">**SetWindowsHookEx**</span><span class="sxs-lookup"><span data-stu-id="4268b-129">**SetWindowsHookEx**</span></span>](/windows/win32/api/winuser/nf-winuser-setwindowshookexa)
</dt> <dt>

<span data-ttu-id="4268b-130">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="4268b-130">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="4268b-131">Hooks</span><span class="sxs-lookup"><span data-stu-id="4268b-131">Hooks</span></span>](hooks.md)
</dt> </dl>

 

 
