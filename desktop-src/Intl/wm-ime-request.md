---
description: Envoyé à une application pour fournir des commandes et demander des informations. Une fenêtre reçoit ce message par le biais de sa fonction WindowProc.
ms.assetid: c5e9f256-eed2-46cb-bb33-0e640a975f1f
title: Message WM_IME_REQUEST (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d0cea120d088fe1423b1d7dcb822307886675b5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106514190"
---
# <a name="wm_ime_request-message"></a><span data-ttu-id="02dcf-104">Message WM_IME_REQUEST</span><span class="sxs-lookup"><span data-stu-id="02dcf-104">WM_IME_REQUEST message</span></span>

<span data-ttu-id="02dcf-105">Envoyé à une application pour fournir des commandes et demander des informations.</span><span class="sxs-lookup"><span data-stu-id="02dcf-105">Sent to an application to provide commands and request information.</span></span> <span data-ttu-id="02dcf-106">Une fenêtre reçoit ce message par le biais de sa fonction [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="02dcf-106">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
LRESULT CALLBACK WindowProc(
  HWND  hwnd,       
  WM_IME_REQUEST,  
  WPARAM wParam,   
  LPARAM lParam    
);
```



## <a name="parameters"></a><span data-ttu-id="02dcf-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="02dcf-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="02dcf-108">*HWND*</span><span class="sxs-lookup"><span data-stu-id="02dcf-108">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="02dcf-109">Handle de fenêtre.</span><span class="sxs-lookup"><span data-stu-id="02dcf-109">A handle to window.</span></span>

</dd> <dt>

<span data-ttu-id="02dcf-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="02dcf-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="02dcf-111">Commande.</span><span class="sxs-lookup"><span data-stu-id="02dcf-111">Command.</span></span> <span data-ttu-id="02dcf-112">Ce paramètre peut prendre l'une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="02dcf-112">This parameter can have one of the following values:</span></span>

<dl> 
<dd><span data-ttu-id="02dcf-113"><a href="imr-candidatewindow.md">IMR_CANDIDATEWINDOW</a></span><span class="sxs-lookup"><span data-stu-id="02dcf-113"><a href="imr-candidatewindow.md">IMR_CANDIDATEWINDOW</a></span></span></dd> 
<dd><span data-ttu-id="02dcf-114"><a href="imr-compositionfont.md">IMR_COMPOSITIONFONT</a></span><span class="sxs-lookup"><span data-stu-id="02dcf-114"><a href="imr-compositionfont.md">IMR_COMPOSITIONFONT</a></span></span></dd> 
<dd><span data-ttu-id="02dcf-115"><a href="imr-compositionwindow.md">IMR_COMPOSITIONWINDOW</a></span><span class="sxs-lookup"><span data-stu-id="02dcf-115"><a href="imr-compositionwindow.md">IMR_COMPOSITIONWINDOW</a></span></span></dd> 
<dd><span data-ttu-id="02dcf-116"><a href="imr-confirmreconvertstring.md">IMR_CONFIRMRECONVERTSTRING</a></span><span class="sxs-lookup"><span data-stu-id="02dcf-116"><a href="imr-confirmreconvertstring.md">IMR_CONFIRMRECONVERTSTRING</a></span></span></dd> 
<dd><span data-ttu-id="02dcf-117"><a href="imr-documentfeed.md">IMR_DOCUMENTFEED</a></span><span class="sxs-lookup"><span data-stu-id="02dcf-117"><a href="imr-documentfeed.md">IMR_DOCUMENTFEED</a></span></span></dd> 
<dd><span data-ttu-id="02dcf-118"><a href="imr-querycharposition.md">IMR_QUERYCHARPOSITION</a></span><span class="sxs-lookup"><span data-stu-id="02dcf-118"><a href="imr-querycharposition.md">IMR_QUERYCHARPOSITION</a></span></span></dd> 
<dd><span data-ttu-id="02dcf-119"><a href="imr-reconvertstring.md">IMR_RECONVERTSTRING</a></span><span class="sxs-lookup"><span data-stu-id="02dcf-119"><a href="imr-reconvertstring.md">IMR_RECONVERTSTRING</a></span></span></dd> 
</dl> 
</dd> 
<dt>

<span data-ttu-id="02dcf-120">*lParam*</span><span class="sxs-lookup"><span data-stu-id="02dcf-120">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="02dcf-121">Données spécifiques à la commande.</span><span class="sxs-lookup"><span data-stu-id="02dcf-121">Command-specific data.</span></span> <span data-ttu-id="02dcf-122">Pour plus d’informations, consultez la description de chaque commande.</span><span class="sxs-lookup"><span data-stu-id="02dcf-122">For more information, see the description for each command.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="02dcf-123">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="02dcf-123">Return value</span></span>

<span data-ttu-id="02dcf-124">Retourne une valeur spécifique à une commande.</span><span class="sxs-lookup"><span data-stu-id="02dcf-124">Returns a command-specific value.</span></span>

## <a name="requirements"></a><span data-ttu-id="02dcf-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="02dcf-125">Requirements</span></span>



| <span data-ttu-id="02dcf-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="02dcf-126">Requirement</span></span> | <span data-ttu-id="02dcf-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="02dcf-127">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="02dcf-128">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="02dcf-128">Minimum supported client</span></span><br/> | <span data-ttu-id="02dcf-129">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="02dcf-129">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                                                                |
| <span data-ttu-id="02dcf-130">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="02dcf-130">Minimum supported server</span></span><br/> | <span data-ttu-id="02dcf-131">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="02dcf-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                                                      |
| <span data-ttu-id="02dcf-132">En-tête</span><span class="sxs-lookup"><span data-stu-id="02dcf-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="02dcf-133"><dt>Winuser. h (inclure Windows. h); </dt> <dt>IMM. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="02dcf-133"><dt>Winuser.h (include Windows.h); </dt> <dt>Imm.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="02dcf-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="02dcf-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="02dcf-135">Gestionnaire de méthode d’entrée</span><span class="sxs-lookup"><span data-stu-id="02dcf-135">Input Method Manager</span></span>](input-method-manager.md)
</dt> <dt>

[<span data-ttu-id="02dcf-136">Messages du gestionnaire de méthode d’entrée</span><span class="sxs-lookup"><span data-stu-id="02dcf-136">Input Method Manager Messages</span></span>](input-method-manager-messages.md)
</dt> <dt>

[<span data-ttu-id="02dcf-137">IMR_CANDIDATEWINDOW</span><span class="sxs-lookup"><span data-stu-id="02dcf-137">IMR_CANDIDATEWINDOW</span></span>](imr-candidatewindow.md)
</dt> <dt>

[<span data-ttu-id="02dcf-138">IMR_COMPOSITIONFONT</span><span class="sxs-lookup"><span data-stu-id="02dcf-138">IMR_COMPOSITIONFONT</span></span>](imr-compositionfont.md)
</dt> <dt>

[<span data-ttu-id="02dcf-139">IMR_COMPOSITIONWINDOW</span><span class="sxs-lookup"><span data-stu-id="02dcf-139">IMR_COMPOSITIONWINDOW</span></span>](imr-compositionwindow.md)
</dt> <dt>

[<span data-ttu-id="02dcf-140">IMR_CONFIRMRECONVERTSTRING</span><span class="sxs-lookup"><span data-stu-id="02dcf-140">IMR_CONFIRMRECONVERTSTRING</span></span>](imr-confirmreconvertstring.md)
</dt> <dt>

[<span data-ttu-id="02dcf-141">IMR_DOCUMENTFEED</span><span class="sxs-lookup"><span data-stu-id="02dcf-141">IMR_DOCUMENTFEED</span></span>](imr-documentfeed.md)
</dt> <dt>

[<span data-ttu-id="02dcf-142">IMR_QUERYCHARPOSITION</span><span class="sxs-lookup"><span data-stu-id="02dcf-142">IMR_QUERYCHARPOSITION</span></span>](imr-querycharposition.md)
</dt> <dt>

[<span data-ttu-id="02dcf-143">IMR_RECONVERTSTRING</span><span class="sxs-lookup"><span data-stu-id="02dcf-143">IMR_RECONVERTSTRING</span></span>](imr-reconvertstring.md)
</dt> </dl>

 

 
