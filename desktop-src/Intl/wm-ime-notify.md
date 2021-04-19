---
description: Envoyé à une application pour l’informer des modifications apportées à la fenêtre IME. Une fenêtre reçoit ce message par le biais de sa fonction WindowProc.
ms.assetid: 20e064b8-2baf-4b4c-8341-36c3e4643eff
title: Message WM_IME_NOTIFY (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ca5ab1b2a1fd62d159ab4f216bf9b1bb6892ed69
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106516471"
---
# <a name="wm_ime_notify-message"></a><span data-ttu-id="45ba0-104">Message WM_IME_NOTIFY</span><span class="sxs-lookup"><span data-stu-id="45ba0-104">WM_IME_NOTIFY message</span></span>

<span data-ttu-id="45ba0-105">Envoyé à une application pour l’informer des modifications apportées à la fenêtre IME.</span><span class="sxs-lookup"><span data-stu-id="45ba0-105">Sent to an application to notify it of changes to the IME window.</span></span> <span data-ttu-id="45ba0-106">Une fenêtre reçoit ce message par le biais de sa fonction [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="45ba0-106">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
LRESULT CALLBACK WindowProc(
  HWND  hwnd,       
  WM_IME_NOTIFY,   
  WPARAM wParam,   
  LPARAM lParam     
);
```



## <a name="parameters"></a><span data-ttu-id="45ba0-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="45ba0-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="45ba0-108">*HWND*</span><span class="sxs-lookup"><span data-stu-id="45ba0-108">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="45ba0-109">Handle de fenêtre.</span><span class="sxs-lookup"><span data-stu-id="45ba0-109">A handle to window.</span></span>

</dd> <dt>

<span data-ttu-id="45ba0-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="45ba0-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="45ba0-111">Commande.</span><span class="sxs-lookup"><span data-stu-id="45ba0-111">The command.</span></span> <span data-ttu-id="45ba0-112">Ce paramètre peut avoir l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="45ba0-112">This parameter can have one of the following values.</span></span>

<dl>
<dd><span data-ttu-id="45ba0-113"><a href="imn-changecandidate.md">IMN_CHANGECANDIDATE</a></span><span class="sxs-lookup"><span data-stu-id="45ba0-113"><a href="imn-changecandidate.md">IMN_CHANGECANDIDATE</a></span></span></dd> 
<dd><span data-ttu-id="45ba0-114"><a href="imn-closecandidate.md">IMN_CLOSECANDIDATE</a></span><span class="sxs-lookup"><span data-stu-id="45ba0-114"><a href="imn-closecandidate.md">IMN_CLOSECANDIDATE</a></span></span></dd> 
<dd><span data-ttu-id="45ba0-115"><a href="imn-closestatuswindow.md">IMN_CLOSESTATUSWINDOW</a></span><span class="sxs-lookup"><span data-stu-id="45ba0-115"><a href="imn-closestatuswindow.md">IMN_CLOSESTATUSWINDOW</a></span></span></dd> 
<dd><span data-ttu-id="45ba0-116"><a href="imn-guideline.md">IMN_GUIDELINE</a></span><span class="sxs-lookup"><span data-stu-id="45ba0-116"><a href="imn-guideline.md">IMN_GUIDELINE</a></span></span></dd> 
<dd><span data-ttu-id="45ba0-117"><a href="imn-opencandidate.md">IMN_OPENCANDIDATE</a></span><span class="sxs-lookup"><span data-stu-id="45ba0-117"><a href="imn-opencandidate.md">IMN_OPENCANDIDATE</a></span></span></dd> 
<dd><span data-ttu-id="45ba0-118"><a href="imn-openstatuswindow.md">IMN_OPENSTATUSWINDOW</a></span><span class="sxs-lookup"><span data-stu-id="45ba0-118"><a href="imn-openstatuswindow.md">IMN_OPENSTATUSWINDOW</a></span></span></dd> 
<dd><span data-ttu-id="45ba0-119"><a href="imn-setcandidatepos.md">IMN_SETCANDIDATEPOS</a></span><span class="sxs-lookup"><span data-stu-id="45ba0-119"><a href="imn-setcandidatepos.md">IMN_SETCANDIDATEPOS</a></span></span></dd> 
<dd><span data-ttu-id="45ba0-120"><a href="imn-setcompositionfont.md">IMN_SETCOMPOSITIONFONT</a></span><span class="sxs-lookup"><span data-stu-id="45ba0-120"><a href="imn-setcompositionfont.md">IMN_SETCOMPOSITIONFONT</a></span></span></dd> 
<dd><span data-ttu-id="45ba0-121"><a href="imn-setcompositionwindow.md">IMN_SETCOMPOSITIONWINDOW</a></span><span class="sxs-lookup"><span data-stu-id="45ba0-121"><a href="imn-setcompositionwindow.md">IMN_SETCOMPOSITIONWINDOW</a></span></span></dd> 
<dd><span data-ttu-id="45ba0-122"><a href="imn-setconversionmode.md">IMN_SETCONVERSIONMODE</a></span><span class="sxs-lookup"><span data-stu-id="45ba0-122"><a href="imn-setconversionmode.md">IMN_SETCONVERSIONMODE</a></span></span></dd> 
<dd><span data-ttu-id="45ba0-123"><a href="imn-setopenstatus.md">IMN_SETOPENSTATUS</a></span><span class="sxs-lookup"><span data-stu-id="45ba0-123"><a href="imn-setopenstatus.md">IMN_SETOPENSTATUS</a></span></span></dd> 
<dd><span data-ttu-id="45ba0-124"><a href="imn-setsentencemode.md">IMN_SETSENTENCEMODE</a></span><span class="sxs-lookup"><span data-stu-id="45ba0-124"><a href="imn-setsentencemode.md">IMN_SETSENTENCEMODE</a></span></span></dd> 
<dd><span data-ttu-id="45ba0-125"><a href="imn-setstatuswindowpos.md">IMN_SETSTATUSWINDOWPOS</a></span><span class="sxs-lookup"><span data-stu-id="45ba0-125"><a href="imn-setstatuswindowpos.md">IMN_SETSTATUSWINDOWPOS</a></span></span></dd> 
</dl> 
</dd> 
<dt>

<span data-ttu-id="45ba0-126">*lParam*</span><span class="sxs-lookup"><span data-stu-id="45ba0-126">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="45ba0-127">Données spécifiques à la commande, avec un format dépendant de la valeur du paramètre *wParam* .</span><span class="sxs-lookup"><span data-stu-id="45ba0-127">Command-specific data, with format dependent on the value of the *wParam* parameter.</span></span> <span data-ttu-id="45ba0-128">Pour plus d’informations, reportez-vous à la documentation de chaque commande.</span><span class="sxs-lookup"><span data-stu-id="45ba0-128">For more information, refer to the documentation for each command.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="45ba0-129">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="45ba0-129">Return value</span></span>

<span data-ttu-id="45ba0-130">La valeur de retour dépend de la commande envoyée.</span><span class="sxs-lookup"><span data-stu-id="45ba0-130">The return value depends on the command sent.</span></span>

## <a name="remarks"></a><span data-ttu-id="45ba0-131">Notes</span><span class="sxs-lookup"><span data-stu-id="45ba0-131">Remarks</span></span>

<span data-ttu-id="45ba0-132">Une application traite ce message s’il est responsable de la gestion de la fenêtre IME.</span><span class="sxs-lookup"><span data-stu-id="45ba0-132">An application processes this message if it is responsible for managing the IME window.</span></span>

## <a name="requirements"></a><span data-ttu-id="45ba0-133">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="45ba0-133">Requirements</span></span>



| <span data-ttu-id="45ba0-134">Condition requise</span><span class="sxs-lookup"><span data-stu-id="45ba0-134">Requirement</span></span> | <span data-ttu-id="45ba0-135">Valeur</span><span class="sxs-lookup"><span data-stu-id="45ba0-135">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="45ba0-136">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="45ba0-136">Minimum supported client</span></span><br/> | <span data-ttu-id="45ba0-137">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="45ba0-137">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                                                                |
| <span data-ttu-id="45ba0-138">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="45ba0-138">Minimum supported server</span></span><br/> | <span data-ttu-id="45ba0-139">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="45ba0-139">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                                                      |
| <span data-ttu-id="45ba0-140">En-tête</span><span class="sxs-lookup"><span data-stu-id="45ba0-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="45ba0-141"><dt>Winuser. h (inclure Windows. h); </dt> <dt>IMM. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="45ba0-141"><dt>Winuser.h (include Windows.h); </dt> <dt>Imm.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="45ba0-142">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="45ba0-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="45ba0-143">Gestionnaire de méthode d’entrée</span><span class="sxs-lookup"><span data-stu-id="45ba0-143">Input Method Manager</span></span>](input-method-manager.md)
</dt> <dt>

[<span data-ttu-id="45ba0-144">Messages du gestionnaire de méthode d’entrée</span><span class="sxs-lookup"><span data-stu-id="45ba0-144">Input Method Manager Messages</span></span>](input-method-manager-messages.md)
</dt> <dt>

[<span data-ttu-id="45ba0-145">IMN_CHANGECANDIDATE</span><span class="sxs-lookup"><span data-stu-id="45ba0-145">IMN_CHANGECANDIDATE</span></span>](imn-changecandidate.md)
</dt> <dt>

[<span data-ttu-id="45ba0-146">IMN_CLOSECANDIDATE</span><span class="sxs-lookup"><span data-stu-id="45ba0-146">IMN_CLOSECANDIDATE</span></span>](imn-closecandidate.md)
</dt> <dt>

[<span data-ttu-id="45ba0-147">IMN_CLOSESTATUSWINDOW</span><span class="sxs-lookup"><span data-stu-id="45ba0-147">IMN_CLOSESTATUSWINDOW</span></span>](imn-closestatuswindow.md)
</dt> <dt>

[<span data-ttu-id="45ba0-148">IMN_GUIDELINE</span><span class="sxs-lookup"><span data-stu-id="45ba0-148">IMN_GUIDELINE</span></span>](imn-guideline.md)
</dt> <dt>

[<span data-ttu-id="45ba0-149">IMN_OPENCANDIDATE</span><span class="sxs-lookup"><span data-stu-id="45ba0-149">IMN_OPENCANDIDATE</span></span>](imn-opencandidate.md)
</dt> <dt>

[<span data-ttu-id="45ba0-150">IMN_OPENSTATUSWINDOW</span><span class="sxs-lookup"><span data-stu-id="45ba0-150">IMN_OPENSTATUSWINDOW</span></span>](imn-openstatuswindow.md)
</dt> <dt>

[<span data-ttu-id="45ba0-151">IMN_SETCANDIDATEPOS</span><span class="sxs-lookup"><span data-stu-id="45ba0-151">IMN_SETCANDIDATEPOS</span></span>](imn-setcandidatepos.md)
</dt> <dt>

[<span data-ttu-id="45ba0-152">IMN_SETCOMPOSITIONFONT</span><span class="sxs-lookup"><span data-stu-id="45ba0-152">IMN_SETCOMPOSITIONFONT</span></span>](imn-setcompositionfont.md)
</dt> <dt>

[<span data-ttu-id="45ba0-153">IMN_SETCOMPOSITIONWINDOW</span><span class="sxs-lookup"><span data-stu-id="45ba0-153">IMN_SETCOMPOSITIONWINDOW</span></span>](imn-setcompositionwindow.md)
</dt> <dt>

[<span data-ttu-id="45ba0-154">IMN_SETCONVERSIONMODE</span><span class="sxs-lookup"><span data-stu-id="45ba0-154">IMN_SETCONVERSIONMODE</span></span>](imn-setconversionmode.md)
</dt> <dt>

[<span data-ttu-id="45ba0-155">IMN_SETOPENSTATUS</span><span class="sxs-lookup"><span data-stu-id="45ba0-155">IMN_SETOPENSTATUS</span></span>](imn-setopenstatus.md)
</dt> <dt>

[<span data-ttu-id="45ba0-156">IMN_SETSENTENCEMODE</span><span class="sxs-lookup"><span data-stu-id="45ba0-156">IMN_SETSENTENCEMODE</span></span>](imn-setsentencemode.md)
</dt> <dt>

[<span data-ttu-id="45ba0-157">IMN_SETSTATUSWINDOWPOS</span><span class="sxs-lookup"><span data-stu-id="45ba0-157">IMN_SETSTATUSWINDOWPOS</span></span>](imn-setstatuswindowpos.md)
</dt> </dl>

 

 
