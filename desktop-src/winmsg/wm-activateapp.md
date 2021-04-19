---
description: Envoyé lorsqu’une fenêtre appartenant à une application différente de celle de la fenêtre active va être activée. Le message est envoyé à l’application dont la fenêtre est activée et à l’application dont la fenêtre est désactivée.
ms.assetid: fc3626ac-8f19-4aa6-8fe9-5020d00c09db
title: Message WM_ACTIVATEAPP (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ee2d64b90426e004a3c18fdc60538fd21862c42f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106533991"
---
# <a name="wm_activateapp-message"></a><span data-ttu-id="0e2cc-104">\_Message WM ACTIVATEAPP</span><span class="sxs-lookup"><span data-stu-id="0e2cc-104">WM\_ACTIVATEAPP message</span></span>

<span data-ttu-id="0e2cc-105">Envoyé lorsqu’une fenêtre appartenant à une application différente de celle de la fenêtre active va être activée.</span><span class="sxs-lookup"><span data-stu-id="0e2cc-105">Sent when a window belonging to a different application than the active window is about to be activated.</span></span> <span data-ttu-id="0e2cc-106">Le message est envoyé à l’application dont la fenêtre est activée et à l’application dont la fenêtre est désactivée.</span><span class="sxs-lookup"><span data-stu-id="0e2cc-106">The message is sent to the application whose window is being activated and to the application whose window is being deactivated.</span></span>

<span data-ttu-id="0e2cc-107">Une fenêtre reçoit ce message par le biais de sa fonction [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="0e2cc-107">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_ACTIVATEAPP                  0x001C
```



## <a name="parameters"></a><span data-ttu-id="0e2cc-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0e2cc-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0e2cc-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="0e2cc-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0e2cc-110">Indique si la fenêtre est activée ou désactivée.</span><span class="sxs-lookup"><span data-stu-id="0e2cc-110">Indicates whether the window is being activated or deactivated.</span></span> <span data-ttu-id="0e2cc-111">Ce paramètre a la **valeur true** si la fenêtre est activée ; la **valeur est false** si la fenêtre est désactivée.</span><span class="sxs-lookup"><span data-stu-id="0e2cc-111">This parameter is **TRUE** if the window is being activated; it is **FALSE** if the window is being deactivated.</span></span>

</dd> <dt>

<span data-ttu-id="0e2cc-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="0e2cc-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0e2cc-113">Identificateur du thread.</span><span class="sxs-lookup"><span data-stu-id="0e2cc-113">The thread identifier.</span></span> <span data-ttu-id="0e2cc-114">Si le paramètre *wParam* a la **valeur true**, *lParam* est l’identificateur du thread qui détient la fenêtre désactivée.</span><span class="sxs-lookup"><span data-stu-id="0e2cc-114">If the *wParam* parameter is **TRUE**, *lParam* is the identifier of the thread that owns the window being deactivated.</span></span> <span data-ttu-id="0e2cc-115">Si *wParam* a la **valeur false**, *lParam* est l’identificateur du thread qui détient la fenêtre en cours d’activation.</span><span class="sxs-lookup"><span data-stu-id="0e2cc-115">If *wParam* is **FALSE**, *lParam* is the identifier of the thread that owns the window being activated.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0e2cc-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="0e2cc-116">Return value</span></span>

<span data-ttu-id="0e2cc-117">Type : **LRESULT**</span><span class="sxs-lookup"><span data-stu-id="0e2cc-117">Type: **LRESULT**</span></span>

<span data-ttu-id="0e2cc-118">Si une application traite ce message, elle doit retourner la valeur zéro.</span><span class="sxs-lookup"><span data-stu-id="0e2cc-118">If an application processes this message, it should return zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="0e2cc-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0e2cc-119">Requirements</span></span>



| <span data-ttu-id="0e2cc-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0e2cc-120">Requirement</span></span> | <span data-ttu-id="0e2cc-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="0e2cc-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0e2cc-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0e2cc-122">Minimum supported client</span></span><br/> | <span data-ttu-id="0e2cc-123">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0e2cc-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="0e2cc-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0e2cc-124">Minimum supported server</span></span><br/> | <span data-ttu-id="0e2cc-125">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0e2cc-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="0e2cc-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="0e2cc-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="0e2cc-127"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0e2cc-127"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0e2cc-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0e2cc-128">See also</span></span>

<dl> <dt>

<span data-ttu-id="0e2cc-129">**Référence**</span><span class="sxs-lookup"><span data-stu-id="0e2cc-129">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="0e2cc-130">**activation de WM \_**</span><span class="sxs-lookup"><span data-stu-id="0e2cc-130">**WM\_ACTIVATE**</span></span>](../inputdev/wm-activate.md)
</dt> <dt>

<span data-ttu-id="0e2cc-131">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="0e2cc-131">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="0e2cc-132">Windows</span><span class="sxs-lookup"><span data-stu-id="0e2cc-132">Windows</span></span>](windows.md)
</dt> </dl>

 

 
