---
title: Message WM_ACTIVATE (winuser. h)
description: Envoyé à la fenêtre en cours d’activation et à la fenêtre désactivée.
ms.assetid: a62bb9f7-f286-4d0d-a1ca-370950c188b2
keywords:
- WM_ACTIVATE l’entrée du clavier et de la souris du message
topic_type:
- apiref
api_name:
- WM_ACTIVATE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dec28662aa2219ee9b3ad2e8cc8efac861d292f6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103408"
---
# <a name="wm_activate-message"></a><span data-ttu-id="08a1a-104">\_Message WM Activate</span><span class="sxs-lookup"><span data-stu-id="08a1a-104">WM\_ACTIVATE message</span></span>

<span data-ttu-id="08a1a-105">Envoyé à la fenêtre en cours d’activation et à la fenêtre désactivée.</span><span class="sxs-lookup"><span data-stu-id="08a1a-105">Sent to both the window being activated and the window being deactivated.</span></span> <span data-ttu-id="08a1a-106">Si les fenêtres utilisent la même file d’attente d’entrée, le message est envoyé de manière synchrone, d’abord à la procédure de fenêtre de la fenêtre de niveau supérieur désactivée, puis à la procédure de fenêtre de la fenêtre de niveau supérieur en cours d’activation.</span><span class="sxs-lookup"><span data-stu-id="08a1a-106">If the windows use the same input queue, the message is sent synchronously, first to the window procedure of the top-level window being deactivated, then to the window procedure of the top-level window being activated.</span></span> <span data-ttu-id="08a1a-107">Si les fenêtres utilisent des files d’attente d’entrée différentes, le message est envoyé de manière asynchrone, de sorte que la fenêtre est activée immédiatement.</span><span class="sxs-lookup"><span data-stu-id="08a1a-107">If the windows use different input queues, the message is sent asynchronously, so the window is activated immediately.</span></span>


```C++
#define WM_ACTIVATE                     0x0006
```



## <a name="parameters"></a><span data-ttu-id="08a1a-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="08a1a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="08a1a-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="08a1a-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="08a1a-110">Le mot de poids faible spécifie si la fenêtre est activée ou désactivée.</span><span class="sxs-lookup"><span data-stu-id="08a1a-110">The low-order word specifies whether the window is being activated or deactivated.</span></span> <span data-ttu-id="08a1a-111">Ce paramètre peut prendre les valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="08a1a-111">This parameter can be one of the following values.</span></span> <span data-ttu-id="08a1a-112">Le mot de poids fort spécifie l’État réduit de la fenêtre en cours d’activation ou de désactivation.</span><span class="sxs-lookup"><span data-stu-id="08a1a-112">The high-order word specifies the minimized state of the window being activated or deactivated.</span></span> <span data-ttu-id="08a1a-113">Une valeur différente de zéro indique que la fenêtre est réduite.</span><span class="sxs-lookup"><span data-stu-id="08a1a-113">A nonzero value indicates the window is minimized.</span></span>



| <span data-ttu-id="08a1a-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="08a1a-114">Value</span></span>                                                                                                                                                                                                                   | <span data-ttu-id="08a1a-115">Signification</span><span class="sxs-lookup"><span data-stu-id="08a1a-115">Meaning</span></span>                                                                                                                                                                                                    |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WA_ACTIVE"></span><span id="wa_active"></span><dl> <span data-ttu-id="08a1a-116"><dt>**Wa \_ ACTIF**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="08a1a-116"><dt>**WA\_ACTIVE**</dt> <dt>1</dt></span></span> </dl>                | <span data-ttu-id="08a1a-117">Activé par une méthode autre qu’un clic de souris (par exemple, par un appel à la fonction [**SetActiveWindow**](/windows/win32/api/winuser/nf-winuser-setactivewindow) ou à l’aide de l’interface clavier pour sélectionner la fenêtre).</span><span class="sxs-lookup"><span data-stu-id="08a1a-117">Activated by some method other than a mouse click (for example, by a call to the [**SetActiveWindow**](/windows/win32/api/winuser/nf-winuser-setactivewindow) function or by use of the keyboard interface to select the window).</span></span><br/> |
| <span id="WA_CLICKACTIVE"></span><span id="wa_clickactive"></span><dl> <span data-ttu-id="08a1a-118"><dt>**Wa \_ CLICKACTIVE**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="08a1a-118"><dt>**WA\_CLICKACTIVE**</dt> <dt>2</dt></span></span> </dl> | <span data-ttu-id="08a1a-119">Activé par un clic de souris.</span><span class="sxs-lookup"><span data-stu-id="08a1a-119">Activated by a mouse click.</span></span><br/>                                                                                                                                                                     |
| <span id="WA_INACTIVE"></span><span id="wa_inactive"></span><dl> <span data-ttu-id="08a1a-120"><dt>**Wa \_ Inactif**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="08a1a-120"><dt>**WA\_INACTIVE**</dt> <dt>0</dt></span></span> </dl>          | <span data-ttu-id="08a1a-121">Désactivé.</span><span class="sxs-lookup"><span data-stu-id="08a1a-121">Deactivated.</span></span><br/>                                                                                                                                                                                    |



 

</dd> <dt>

<span data-ttu-id="08a1a-122">*lParam*</span><span class="sxs-lookup"><span data-stu-id="08a1a-122">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="08a1a-123">Handle de la fenêtre en cours d’activation ou de désactivation, selon la valeur du paramètre *wParam* .</span><span class="sxs-lookup"><span data-stu-id="08a1a-123">A handle to the window being activated or deactivated, depending on the value of the *wParam* parameter.</span></span> <span data-ttu-id="08a1a-124">Si le mot de poids faible de *wParam* est **wa \_ inactif**, *lParam* est le handle de la fenêtre en cours d’activation.</span><span class="sxs-lookup"><span data-stu-id="08a1a-124">If the low-order word of *wParam* is **WA\_INACTIVE**, *lParam* is the handle to the window being activated.</span></span> <span data-ttu-id="08a1a-125">Si le mot de poids faible de *wParam* est **wa \_ active** ou **wa \_ CLICKACTIVE**, *lParam* est le handle de la fenêtre désactivée.</span><span class="sxs-lookup"><span data-stu-id="08a1a-125">If the low-order word of *wParam* is **WA\_ACTIVE** or **WA\_CLICKACTIVE**, *lParam* is the handle to the window being deactivated.</span></span> <span data-ttu-id="08a1a-126">Ce handle peut être **null**.</span><span class="sxs-lookup"><span data-stu-id="08a1a-126">This handle can be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="08a1a-127">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="08a1a-127">Return value</span></span>

<span data-ttu-id="08a1a-128">Si une application traite ce message, elle doit retourner la valeur zéro.</span><span class="sxs-lookup"><span data-stu-id="08a1a-128">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="08a1a-129">Notes</span><span class="sxs-lookup"><span data-stu-id="08a1a-129">Remarks</span></span>

<span data-ttu-id="08a1a-130">Si la fenêtre est activée et n’est pas réduite, la fonction [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) définit le focus clavier sur la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="08a1a-130">If the window is being activated and is not minimized, the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function sets the keyboard focus to the window.</span></span> <span data-ttu-id="08a1a-131">Si la fenêtre est activée par un clic de souris, elle reçoit également un message [**WM \_ MOUSEACTIVATE**](wm-mouseactivate.md) .</span><span class="sxs-lookup"><span data-stu-id="08a1a-131">If the window is activated by a mouse click, it also receives a [**WM\_MOUSEACTIVATE**](wm-mouseactivate.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="08a1a-132">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="08a1a-132">Requirements</span></span>



| <span data-ttu-id="08a1a-133">Condition requise</span><span class="sxs-lookup"><span data-stu-id="08a1a-133">Requirement</span></span> | <span data-ttu-id="08a1a-134">Valeur</span><span class="sxs-lookup"><span data-stu-id="08a1a-134">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="08a1a-135">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="08a1a-135">Minimum supported client</span></span><br/> | <span data-ttu-id="08a1a-136">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="08a1a-136">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="08a1a-137">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="08a1a-137">Minimum supported server</span></span><br/> | <span data-ttu-id="08a1a-138">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="08a1a-138">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="08a1a-139">En-tête</span><span class="sxs-lookup"><span data-stu-id="08a1a-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="08a1a-140"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="08a1a-140"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="08a1a-141">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="08a1a-141">See also</span></span>

<dl> <dt>

<span data-ttu-id="08a1a-142">**Référence**</span><span class="sxs-lookup"><span data-stu-id="08a1a-142">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="08a1a-143">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="08a1a-143">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[<span data-ttu-id="08a1a-144">**SetActiveWindow**</span><span class="sxs-lookup"><span data-stu-id="08a1a-144">**SetActiveWindow**</span></span>](/windows/win32/api/winuser/nf-winuser-setactivewindow)
</dt> <dt>

[<span data-ttu-id="08a1a-145">**\_MOUSEACTIVATE WM**</span><span class="sxs-lookup"><span data-stu-id="08a1a-145">**WM\_MOUSEACTIVATE**</span></span>](wm-mouseactivate.md)
</dt> <dt>

[<span data-ttu-id="08a1a-146">**\_NCACTIVATE WM**</span><span class="sxs-lookup"><span data-stu-id="08a1a-146">**WM\_NCACTIVATE**</span></span>](/windows/desktop/winmsg/wm-ncactivate)
</dt> <dt>

<span data-ttu-id="08a1a-147">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="08a1a-147">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="08a1a-148">Entrée au clavier</span><span class="sxs-lookup"><span data-stu-id="08a1a-148">Keyboard Input</span></span>](keyboard-input.md)
</dt> </dl>

 

