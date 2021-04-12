---
description: Envoyé à une application lorsqu’une fenêtre est activée. Une fenêtre reçoit ce message par le biais de sa fonction WindowProc.
ms.assetid: ba1e7877-1612-4f2f-aced-0dd982352ad6
title: Message WM_IME_SETCONTEXT (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6b36cb1e80127d1a451dabcc457dc364a27878ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104201473"
---
# <a name="wm_ime_setcontext-message"></a><span data-ttu-id="ae5b5-104">Message de l' \_ IME SETCONTEXT du WM \_</span><span class="sxs-lookup"><span data-stu-id="ae5b5-104">WM\_IME\_SETCONTEXT message</span></span>

<span data-ttu-id="ae5b5-105">Envoyé à une application lorsqu’une fenêtre est activée.</span><span class="sxs-lookup"><span data-stu-id="ae5b5-105">Sent to an application when a window is activated.</span></span> <span data-ttu-id="ae5b5-106">Une fenêtre reçoit ce message par le biais de sa fonction [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="ae5b5-106">A window receives this message through its [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
LRESULT CALLBACK WindowProc(
  HWND  hwnd,  
  WM_IME_SETCONTEXT,  
  WPARAM wParam,      
  LPARAM lParam      
);
```



## <a name="parameters"></a><span data-ttu-id="ae5b5-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ae5b5-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ae5b5-108">*HWND*</span><span class="sxs-lookup"><span data-stu-id="ae5b5-108">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="ae5b5-109">Handle de fenêtre.</span><span class="sxs-lookup"><span data-stu-id="ae5b5-109">A handle to window.</span></span>

</dd> <dt>

<span data-ttu-id="ae5b5-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="ae5b5-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ae5b5-111">**True** si la fenêtre est active, et **false** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="ae5b5-111">**TRUE** if the window is active, and **FALSE** otherwise.</span></span>

</dd> <dt>

<span data-ttu-id="ae5b5-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ae5b5-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ae5b5-113">les options d’affichage ;</span><span class="sxs-lookup"><span data-stu-id="ae5b5-113">Display options.</span></span> <span data-ttu-id="ae5b5-114">Ce paramètre peut avoir une ou plusieurs des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="ae5b5-114">This parameter can have one or more of the following values.</span></span>



| <span data-ttu-id="ae5b5-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="ae5b5-115">Value</span></span>                                                                                                                                                                                                   | <span data-ttu-id="ae5b5-116">Signification</span><span class="sxs-lookup"><span data-stu-id="ae5b5-116">Meaning</span></span>                                                                   |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <span id="ISC_SHOWUICOMPOSITIONWINDOW"></span><span id="isc_showuicompositionwindow"></span><dl> <span data-ttu-id="ae5b5-117"><dt>**ISC \_ SHOWUICOMPOSITIONWINDOW**</dt></span><span class="sxs-lookup"><span data-stu-id="ae5b5-117"><dt>**ISC\_SHOWUICOMPOSITIONWINDOW**</dt></span></span> </dl> | <span data-ttu-id="ae5b5-118">Affiche la fenêtre de composition par le biais de la fenêtre de l’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="ae5b5-118">Show the composition window by user interface window.</span></span><br/>          |
| <span id="ISC_SHOWUIGUIDWINDOW"></span><span id="isc_showuiguidwindow"></span><dl> <span data-ttu-id="ae5b5-119"><dt>**ISC \_ SHOWUIGUIDWINDOW**</dt></span><span class="sxs-lookup"><span data-stu-id="ae5b5-119"><dt>**ISC\_SHOWUIGUIDWINDOW**</dt></span></span> </dl>                      | <span data-ttu-id="ae5b5-120">Affichez la fenêtre Guide par le biais de la fenêtre de l’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="ae5b5-120">Show the guide window by user interface window.</span></span><br/>                |
| <span id="ISC_SHOWUISOFTKBD"></span><span id="isc_showuisoftkbd"></span><dl> <span data-ttu-id="ae5b5-121"><dt>**ISC \_ SHOWUISOFTKBD**</dt></span><span class="sxs-lookup"><span data-stu-id="ae5b5-121"><dt>**ISC\_SHOWUISOFTKBD**</dt></span></span> </dl>                               | <span data-ttu-id="ae5b5-122">Affiche la fenêtre de l’interface utilisateur du clavier conditionnel.</span><span class="sxs-lookup"><span data-stu-id="ae5b5-122">Show the soft keyboard by user interface window.</span></span><br/>               |
| <span id="ISC_SHOWUICANDIDATEWINDOW"></span><span id="isc_showuicandidatewindow"></span><dl> <span data-ttu-id="ae5b5-123"><dt>**ISC \_ SHOWUICANDIDATEWINDOW**</dt></span><span class="sxs-lookup"><span data-stu-id="ae5b5-123"><dt>**ISC\_SHOWUICANDIDATEWINDOW**</dt></span></span> </dl>       | <span data-ttu-id="ae5b5-124">Affiche la fenêtre candidate de l’index 0 par la fenêtre de l’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="ae5b5-124">Show the candidate window of index 0 by user interface window.</span></span><br/> |
| <dl> <span data-ttu-id="ae5b5-125"><dt>ISC \_ SHOWUICANDIDATEWINDOW << 1</dt></span><span class="sxs-lookup"><span data-stu-id="ae5b5-125"><dt>ISC\_SHOWUICANDIDATEWINDOW << 1</dt></span></span> </dl>                                                                                        | <span data-ttu-id="ae5b5-126">Affiche la fenêtre candidate de l’index 1 par la fenêtre de l’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="ae5b5-126">Show the candidate window of index 1 by user interface window.</span></span><br/> |
| <dl> <span data-ttu-id="ae5b5-127"><dt>ISC \_ SHOWUICANDIDATEWINDOW << 2</dt></span><span class="sxs-lookup"><span data-stu-id="ae5b5-127"><dt>ISC\_SHOWUICANDIDATEWINDOW << 2</dt></span></span> </dl>                                                                                        | <span data-ttu-id="ae5b5-128">Affiche la fenêtre candidate de l’index 2 par la fenêtre de l’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="ae5b5-128">Show the candidate window of index 2 by user interface window.</span></span><br/> |
| <dl> <span data-ttu-id="ae5b5-129"><dt>ISC \_ SHOWUICANDIDATEWINDOW << 3</dt></span><span class="sxs-lookup"><span data-stu-id="ae5b5-129"><dt>ISC\_SHOWUICANDIDATEWINDOW << 3</dt></span></span> </dl>                                                                                        | <span data-ttu-id="ae5b5-130">Affiche la fenêtre candidate de l’index 3 par la fenêtre de l’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="ae5b5-130">Show the candidate window of index 3 by user interface window.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ae5b5-131">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="ae5b5-131">Return value</span></span>

<span data-ttu-id="ae5b5-132">Retourne la valeur retournée par [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) ou [**ImmIsUIMessage**](/windows/desktop/api/Imm/nf-imm-immisuimessagea).</span><span class="sxs-lookup"><span data-stu-id="ae5b5-132">Returns the value returned by [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) or [**ImmIsUIMessage**](/windows/desktop/api/Imm/nf-imm-immisuimessagea).</span></span>

## <a name="remarks"></a><span data-ttu-id="ae5b5-133">Notes</span><span class="sxs-lookup"><span data-stu-id="ae5b5-133">Remarks</span></span>

<span data-ttu-id="ae5b5-134">Si l’application a créé une fenêtre IME, elle doit appeler [**ImmIsUIMessage**](/windows/desktop/api/Imm/nf-imm-immisuimessagea).</span><span class="sxs-lookup"><span data-stu-id="ae5b5-134">If the application has created an IME window, it should call [**ImmIsUIMessage**](/windows/desktop/api/Imm/nf-imm-immisuimessagea).</span></span> <span data-ttu-id="ae5b5-135">Dans le cas contraire, il doit transmettre ce message à [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca).</span><span class="sxs-lookup"><span data-stu-id="ae5b5-135">Otherwise, it should pass this message to [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca).</span></span>

<span data-ttu-id="ae5b5-136">Si l’application dessine la fenêtre de composition, la fenêtre IME par défaut n’a pas besoin d’afficher sa fenêtre de composition.</span><span class="sxs-lookup"><span data-stu-id="ae5b5-136">If the application draws the composition window, the default IME window does not have to show its composition window.</span></span> <span data-ttu-id="ae5b5-137">Dans ce cas, l’application doit effacer la **valeur ISC \_ SHOWUICOMPOSITIONWINDOW** du paramètre *lParam* avant de transmettre le message à [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) ou [**ImmIsUIMessage**](/windows/desktop/api/Imm/nf-imm-immisuimessagea).</span><span class="sxs-lookup"><span data-stu-id="ae5b5-137">In this case, the application must clear the **ISC\_SHOWUICOMPOSITIONWINDOW** value from the *lParam* parameter before passing the message to [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) or [**ImmIsUIMessage**](/windows/desktop/api/Imm/nf-imm-immisuimessagea).</span></span> <span data-ttu-id="ae5b5-138">Pour afficher une certaine fenêtre de l’interface utilisateur, une application doit supprimer la valeur correspondante afin que l’IME ne l’affiche pas.</span><span class="sxs-lookup"><span data-stu-id="ae5b5-138">To display a certain user interface window, an application should remove the corresponding value so that the IME will not display it.</span></span>

## <a name="requirements"></a><span data-ttu-id="ae5b5-139">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ae5b5-139">Requirements</span></span>



| <span data-ttu-id="ae5b5-140">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ae5b5-140">Requirement</span></span> | <span data-ttu-id="ae5b5-141">Valeur</span><span class="sxs-lookup"><span data-stu-id="ae5b5-141">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ae5b5-142">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ae5b5-142">Minimum supported client</span></span><br/> | <span data-ttu-id="ae5b5-143">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ae5b5-143">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                                                                |
| <span data-ttu-id="ae5b5-144">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ae5b5-144">Minimum supported server</span></span><br/> | <span data-ttu-id="ae5b5-145">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ae5b5-145">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                                                      |
| <span data-ttu-id="ae5b5-146">En-tête</span><span class="sxs-lookup"><span data-stu-id="ae5b5-146">Header</span></span><br/>                   | <dl> <span data-ttu-id="ae5b5-147"><dt>Winuser. h (inclure Windows. h); </dt> <dt>IMM. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ae5b5-147"><dt>Winuser.h (include Windows.h); </dt> <dt>Imm.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ae5b5-148">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ae5b5-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ae5b5-149">Gestionnaire de méthode d’entrée</span><span class="sxs-lookup"><span data-stu-id="ae5b5-149">Input Method Manager</span></span>](input-method-manager.md)
</dt> <dt>

[<span data-ttu-id="ae5b5-150">Messages du gestionnaire de méthode d’entrée</span><span class="sxs-lookup"><span data-stu-id="ae5b5-150">Input Method Manager Messages</span></span>](input-method-manager-messages.md)
</dt> <dt>

[<span data-ttu-id="ae5b5-151">**ImmIsUIMessage**</span><span class="sxs-lookup"><span data-stu-id="ae5b5-151">**ImmIsUIMessage**</span></span>](/windows/desktop/api/Imm/nf-imm-immisuimessagea)
</dt> </dl>

 

 
