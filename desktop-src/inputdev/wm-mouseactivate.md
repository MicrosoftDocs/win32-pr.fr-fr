---
title: Message WM_MOUSEACTIVATE (winuser. h)
description: Envoyé lorsque le curseur se trouve dans une fenêtre inactive et que l’utilisateur appuie sur un bouton de la souris. La fenêtre parente reçoit ce message uniquement si la fenêtre enfant la passe à la fonction DefWindowProc.
ms.assetid: 335c0819-a655-4dd1-9511-1f148b87271c
keywords:
- WM_MOUSEACTIVATE l’entrée du clavier et de la souris du message
topic_type:
- apiref
api_name:
- WM_MOUSEACTIVATE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5ba74141f8d519541d1e63327179fff2f27ad403
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103401"
---
# <a name="wm_mouseactivate-message"></a><span data-ttu-id="61fa1-105">\_Message WM MOUSEACTIVATE</span><span class="sxs-lookup"><span data-stu-id="61fa1-105">WM\_MOUSEACTIVATE message</span></span>

<span data-ttu-id="61fa1-106">Envoyé lorsque le curseur se trouve dans une fenêtre inactive et que l’utilisateur appuie sur un bouton de la souris.</span><span class="sxs-lookup"><span data-stu-id="61fa1-106">Sent when the cursor is in an inactive window and the user presses a mouse button.</span></span> <span data-ttu-id="61fa1-107">La fenêtre parente reçoit ce message uniquement si la fenêtre enfant la passe à la fonction [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) .</span><span class="sxs-lookup"><span data-stu-id="61fa1-107">The parent window receives this message only if the child window passes it to the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function.</span></span>

<span data-ttu-id="61fa1-108">Une fenêtre reçoit ce message par le biais de sa fonction [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="61fa1-108">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_MOUSEACTIVATE                0x0021
```



## <a name="parameters"></a><span data-ttu-id="61fa1-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="61fa1-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="61fa1-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="61fa1-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="61fa1-111">Handle de la fenêtre parente de niveau supérieur de la fenêtre en cours d’activation.</span><span class="sxs-lookup"><span data-stu-id="61fa1-111">A handle to the top-level parent window of the window being activated.</span></span>

</dd> <dt>

<span data-ttu-id="61fa1-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="61fa1-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="61fa1-113">Le mot de poids faible spécifie la valeur du test de positionnement retournée par la fonction [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) suite au traitement du message [**WM \_ NCHITTEST**](wm-nchittest.md) .</span><span class="sxs-lookup"><span data-stu-id="61fa1-113">The low-order word specifies the hit-test value returned by the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function as a result of processing the [**WM\_NCHITTEST**](wm-nchittest.md) message.</span></span> <span data-ttu-id="61fa1-114">Pour obtenir la liste des valeurs de test de positionnement, consultez **WM \_ NCHITTEST**.</span><span class="sxs-lookup"><span data-stu-id="61fa1-114">For a list of hit-test values, see **WM\_NCHITTEST**.</span></span>

<span data-ttu-id="61fa1-115">Le mot de poids fort spécifie l’identificateur du message de souris généré quand l’utilisateur appuie sur un bouton de la souris.</span><span class="sxs-lookup"><span data-stu-id="61fa1-115">The high-order word specifies the identifier of the mouse message generated when the user pressed a mouse button.</span></span> <span data-ttu-id="61fa1-116">Le message de la souris est soit ignoré, soit publié dans la fenêtre, en fonction de la valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="61fa1-116">The mouse message is either discarded or posted to the window, depending on the return value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="61fa1-117">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="61fa1-117">Return value</span></span>

<span data-ttu-id="61fa1-118">La valeur de retour spécifie si la fenêtre doit être activée et si l’identificateur du message de la souris doit être ignoré.</span><span class="sxs-lookup"><span data-stu-id="61fa1-118">The return value specifies whether the window should be activated and whether the identifier of the mouse message should be discarded.</span></span> <span data-ttu-id="61fa1-119">Il doit s’agir de l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="61fa1-119">It must be one of the following values.</span></span>



| <span data-ttu-id="61fa1-120">Code/valeur de retour</span><span class="sxs-lookup"><span data-stu-id="61fa1-120">Return code/value</span></span>                                                                                                                                          | <span data-ttu-id="61fa1-121">Description</span><span class="sxs-lookup"><span data-stu-id="61fa1-121">Description</span></span>                                                                      |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="61fa1-122"><dt>**Ma \_ ACTIVER**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="61fa1-122"><dt>**MA\_ACTIVATE**</dt> <dt>1</dt></span></span> </dl>         | <span data-ttu-id="61fa1-123">Active la fenêtre et n’ignore pas le message de la souris.</span><span class="sxs-lookup"><span data-stu-id="61fa1-123">Activates the window, and does not discard the mouse message.</span></span><br/>         |
| <dl> <span data-ttu-id="61fa1-124"><dt>**Ma \_ ACTIVATEANDEAT**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="61fa1-124"><dt>**MA\_ACTIVATEANDEAT**</dt> <dt>2</dt></span></span> </dl>   | <span data-ttu-id="61fa1-125">Active la fenêtre et ignore le message de la souris.</span><span class="sxs-lookup"><span data-stu-id="61fa1-125">Activates the window, and discards the mouse message.</span></span><br/>                 |
| <dl> <span data-ttu-id="61fa1-126"><dt>**Ma \_ Noactivate**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="61fa1-126"><dt>**MA\_NOACTIVATE**</dt> <dt>3</dt></span></span> </dl>       | <span data-ttu-id="61fa1-127">N’active pas la fenêtre et n’ignore pas le message de la souris.</span><span class="sxs-lookup"><span data-stu-id="61fa1-127">Does not activate the window, and does not discard the mouse message.</span></span><br/> |
| <dl> <span data-ttu-id="61fa1-128"><dt>**Ma \_ NOACTIVATEANDEAT**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="61fa1-128"><dt>**MA\_NOACTIVATEANDEAT**</dt> <dt>4</dt></span></span> </dl> | <span data-ttu-id="61fa1-129">N’active pas la fenêtre, mais ignore le message de la souris.</span><span class="sxs-lookup"><span data-stu-id="61fa1-129">Does not activate the window, but discards the mouse message.</span></span><br/>         |



 

## <a name="remarks"></a><span data-ttu-id="61fa1-130">Notes</span><span class="sxs-lookup"><span data-stu-id="61fa1-130">Remarks</span></span>

<span data-ttu-id="61fa1-131">La fonction [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) transmet le message à la fenêtre parente d’une fenêtre enfant avant tout traitement.</span><span class="sxs-lookup"><span data-stu-id="61fa1-131">The [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function passes the message to a child window's parent window before any processing occurs.</span></span> <span data-ttu-id="61fa1-132">La fenêtre parente détermine s’il faut activer la fenêtre enfant.</span><span class="sxs-lookup"><span data-stu-id="61fa1-132">The parent window determines whether to activate the child window.</span></span> <span data-ttu-id="61fa1-133">Si elle active la fenêtre enfant, la fenêtre parente doit retourner **ma \_ noactivate** ou **ma \_ NOACTIVATEANDEAT** pour empêcher le système de traiter le message plus en détail.</span><span class="sxs-lookup"><span data-stu-id="61fa1-133">If it activates the child window, the parent window should return **MA\_NOACTIVATE** or **MA\_NOACTIVATEANDEAT** to prevent the system from processing the message further.</span></span>

## <a name="requirements"></a><span data-ttu-id="61fa1-134">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="61fa1-134">Requirements</span></span>



| <span data-ttu-id="61fa1-135">Condition requise</span><span class="sxs-lookup"><span data-stu-id="61fa1-135">Requirement</span></span> | <span data-ttu-id="61fa1-136">Valeur</span><span class="sxs-lookup"><span data-stu-id="61fa1-136">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="61fa1-137">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="61fa1-137">Minimum supported client</span></span><br/> | <span data-ttu-id="61fa1-138">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="61fa1-138">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="61fa1-139">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="61fa1-139">Minimum supported server</span></span><br/> | <span data-ttu-id="61fa1-140">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="61fa1-140">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="61fa1-141">En-tête</span><span class="sxs-lookup"><span data-stu-id="61fa1-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="61fa1-142"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="61fa1-142"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="61fa1-143">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="61fa1-143">See also</span></span>

<dl> <dt>

<span data-ttu-id="61fa1-144">**Référence**</span><span class="sxs-lookup"><span data-stu-id="61fa1-144">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="61fa1-145">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="61fa1-145">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

<span data-ttu-id="61fa1-146">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="61fa1-146">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="61fa1-147">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="61fa1-147">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="61fa1-148">**\_NCHITTEST WM**</span><span class="sxs-lookup"><span data-stu-id="61fa1-148">**WM\_NCHITTEST**</span></span>](wm-nchittest.md)
</dt> <dt>

<span data-ttu-id="61fa1-149">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="61fa1-149">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="61fa1-150">Entrée de la souris</span><span class="sxs-lookup"><span data-stu-id="61fa1-150">Mouse Input</span></span>](mouse-input.md)
</dt> </dl>

 

