---
title: Message WM_KILLFOCUS (winuser. h)
description: Envoyé à une fenêtre juste avant de perdre le focus clavier.
ms.assetid: 6d32a09b-a856-4f94-9544-3345b3a700f4
keywords:
- WM_KILLFOCUS l’entrée du clavier et de la souris du message
topic_type:
- apiref
api_name:
- WM_KILLFOCUS
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c0e3bba54f2cdb500ba2ba691ffd30419d5beff1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032723"
---
# <a name="wm_killfocus-message"></a><span data-ttu-id="cdd1e-104">\_Message WM KILLFOCUS</span><span class="sxs-lookup"><span data-stu-id="cdd1e-104">WM\_KILLFOCUS message</span></span>

<span data-ttu-id="cdd1e-105">Envoyé à une fenêtre juste avant de perdre le focus clavier.</span><span class="sxs-lookup"><span data-stu-id="cdd1e-105">Sent to a window immediately before it loses the keyboard focus.</span></span>


```C++
#define WM_KILLFOCUS                    0x0008
```



## <a name="parameters"></a><span data-ttu-id="cdd1e-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="cdd1e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cdd1e-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="cdd1e-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="cdd1e-108">Handle vers la fenêtre qui reçoit le focus clavier.</span><span class="sxs-lookup"><span data-stu-id="cdd1e-108">A handle to the window that receives the keyboard focus.</span></span> <span data-ttu-id="cdd1e-109">Ce paramètre peut être **NULL**.</span><span class="sxs-lookup"><span data-stu-id="cdd1e-109">This parameter can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="cdd1e-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="cdd1e-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="cdd1e-111">Ce paramètre n'est pas utilisé.</span><span class="sxs-lookup"><span data-stu-id="cdd1e-111">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cdd1e-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="cdd1e-112">Return value</span></span>

<span data-ttu-id="cdd1e-113">Une application doit retourner zéro si elle traite ce message.</span><span class="sxs-lookup"><span data-stu-id="cdd1e-113">An application should return zero if it processes this message.</span></span>

## <a name="remarks"></a><span data-ttu-id="cdd1e-114">Notes</span><span class="sxs-lookup"><span data-stu-id="cdd1e-114">Remarks</span></span>

<span data-ttu-id="cdd1e-115">Si une application affiche un signe insertion, le point d’insertion doit être détruit à ce stade.</span><span class="sxs-lookup"><span data-stu-id="cdd1e-115">If an application is displaying a caret, the caret should be destroyed at this point.</span></span>

<span data-ttu-id="cdd1e-116">Lors du traitement de ce message, n’effectuez pas d’appels de fonction qui affichent ou activent une fenêtre.</span><span class="sxs-lookup"><span data-stu-id="cdd1e-116">While processing this message, do not make any function calls that display or activate a window.</span></span> <span data-ttu-id="cdd1e-117">Cela amène le thread à donner le contrôle et peut entraîner l’arrêt de la réponse de l’application aux messages.</span><span class="sxs-lookup"><span data-stu-id="cdd1e-117">This causes the thread to yield control and can cause the application to stop responding to messages.</span></span> <span data-ttu-id="cdd1e-118">Pour plus d’informations, consultez [blocage des messages](/windows/desktop/winmsg/about-messages-and-message-queues).</span><span class="sxs-lookup"><span data-stu-id="cdd1e-118">For more information, see [Message Deadlocks](/windows/desktop/winmsg/about-messages-and-message-queues).</span></span>

## <a name="requirements"></a><span data-ttu-id="cdd1e-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="cdd1e-119">Requirements</span></span>



| <span data-ttu-id="cdd1e-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="cdd1e-120">Requirement</span></span> | <span data-ttu-id="cdd1e-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="cdd1e-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cdd1e-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cdd1e-122">Minimum supported client</span></span><br/> | <span data-ttu-id="cdd1e-123">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="cdd1e-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="cdd1e-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cdd1e-124">Minimum supported server</span></span><br/> | <span data-ttu-id="cdd1e-125">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="cdd1e-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="cdd1e-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="cdd1e-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="cdd1e-127"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="cdd1e-127"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cdd1e-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cdd1e-128">See also</span></span>

<dl> <dt>

<span data-ttu-id="cdd1e-129">**Référence**</span><span class="sxs-lookup"><span data-stu-id="cdd1e-129">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="cdd1e-130">**SetFocus**</span><span class="sxs-lookup"><span data-stu-id="cdd1e-130">**SetFocus**</span></span>](/windows/win32/api/winuser/nf-winuser-setfocus)
</dt> <dt>

[<span data-ttu-id="cdd1e-131">**WM \_ SetFocus**</span><span class="sxs-lookup"><span data-stu-id="cdd1e-131">**WM\_SETFOCUS**</span></span>](wm-setfocus.md)
</dt> <dt>

<span data-ttu-id="cdd1e-132">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="cdd1e-132">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="cdd1e-133">Entrée au clavier</span><span class="sxs-lookup"><span data-stu-id="cdd1e-133">Keyboard Input</span></span>](keyboard-input.md)
</dt> </dl>

 

