---
description: Envoyé par une application pour indiquer à la fenêtre IME d’exécuter la commande demandée.
ms.assetid: 5d3b7f8a-57c9-41e3-8022-9a3f515fc32e
title: Message WM_IME_CONTROL (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bd0adc534883bc0b31984c8d3e9b57a04b555987
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862650"
---
# <a name="wm_ime_control-message"></a><span data-ttu-id="5b024-103">Message WM_IME_CONTROL</span><span class="sxs-lookup"><span data-stu-id="5b024-103">WM_IME_CONTROL message</span></span>

<span data-ttu-id="5b024-104">Envoyé par une application pour indiquer à la fenêtre IME d’exécuter la commande demandée.</span><span class="sxs-lookup"><span data-stu-id="5b024-104">Sent by an application to direct the IME window to carry out the requested command.</span></span> <span data-ttu-id="5b024-105">L’application utilise ce message pour contrôler la fenêtre IME qu’elle a créée.</span><span class="sxs-lookup"><span data-stu-id="5b024-105">The application uses this message to control the IME window that it has created.</span></span> <span data-ttu-id="5b024-106">Pour envoyer ce message, l’application appelle la fonction [**SendMessage**](/windows/win32/api/winuser/nf-winuser-sendmessage) avec les paramètres suivants.</span><span class="sxs-lookup"><span data-stu-id="5b024-106">To send this message, the application calls the [**SendMessage**](/windows/win32/api/winuser/nf-winuser-sendmessage) function with the following parameters.</span></span>


```C++
SendMessage(
  HWND   hwnd,
  WM_IME_CONTROL, 
  WPARAM wParam,
  LPARAM lParam             
);
```



## <a name="parameters"></a><span data-ttu-id="5b024-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5b024-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5b024-108">*HWND*</span><span class="sxs-lookup"><span data-stu-id="5b024-108">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="5b024-109">Handle de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="5b024-109">Handle to the window.</span></span>

</dd> <dt>

<span data-ttu-id="5b024-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="5b024-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5b024-111">Commande.</span><span class="sxs-lookup"><span data-stu-id="5b024-111">The command.</span></span> <span data-ttu-id="5b024-112">Ce paramètre peut prendre l'une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="5b024-112">This parameter can have one of the following values:</span></span>

<dl>
<dd><span data-ttu-id="5b024-113"><a href="imc-closestatuswindow.md">IMC_CLOSESTATUSWINDOW</a></span><span class="sxs-lookup"><span data-stu-id="5b024-113"><a href="imc-closestatuswindow.md">IMC_CLOSESTATUSWINDOW</a></span></span></dd> 
<dd><span data-ttu-id="5b024-114"><a href="imc-getcandidatepos.md">IMC_GETCANDIDATEPOS</a></span><span class="sxs-lookup"><span data-stu-id="5b024-114"><a href="imc-getcandidatepos.md">IMC_GETCANDIDATEPOS</a></span></span></dd> 
<dd><span data-ttu-id="5b024-115"><a href="imc-getcompositionfont.md">IMC_GETCOMPOSITIONFONT</a></span><span class="sxs-lookup"><span data-stu-id="5b024-115"><a href="imc-getcompositionfont.md">IMC_GETCOMPOSITIONFONT</a></span></span></dd> 
<dd><span data-ttu-id="5b024-116"><a href="imc-getcompositionwindow.md">IMC_GETCOMPOSITIONWINDOW</a></span><span class="sxs-lookup"><span data-stu-id="5b024-116"><a href="imc-getcompositionwindow.md">IMC_GETCOMPOSITIONWINDOW</a></span></span></dd> 
<dd><span data-ttu-id="5b024-117"><a href="imc-getstatuswindowpos.md">IMC_GETSTATUSWINDOWPOS</a></span><span class="sxs-lookup"><span data-stu-id="5b024-117"><a href="imc-getstatuswindowpos.md">IMC_GETSTATUSWINDOWPOS</a></span></span></dd> 
<dd><span data-ttu-id="5b024-118"><a href="imc-openstatuswindow.md">IMC_OPENSTATUSWINDOW</a></span><span class="sxs-lookup"><span data-stu-id="5b024-118"><a href="imc-openstatuswindow.md">IMC_OPENSTATUSWINDOW</a></span></span></dd> 
<dd><span data-ttu-id="5b024-119"><a href="imc-setcandidatepos.md">IMC_SETCANDIDATEPOS</a></span><span class="sxs-lookup"><span data-stu-id="5b024-119"><a href="imc-setcandidatepos.md">IMC_SETCANDIDATEPOS</a></span></span></dd> 
<dd><span data-ttu-id="5b024-120"><a href="imc-setcompositionfont.md">IMC_SETCOMPOSITIONFONT</a>></span><span class="sxs-lookup"><span data-stu-id="5b024-120"><a href="imc-setcompositionfont.md">IMC_SETCOMPOSITIONFONT</a>></span></span></dd> 
<dd><span data-ttu-id="5b024-121"><a href="imc-setcompositionwindow.md">IMC_SETCOMPOSITIONWINDOW</a></span><span class="sxs-lookup"><span data-stu-id="5b024-121"><a href="imc-setcompositionwindow.md">IMC_SETCOMPOSITIONWINDOW</a></span></span></dd> 
<dd><span data-ttu-id="5b024-122"><a href="imc-setstatuswindowpos.md">IMC_SETSTATUSWINDOWPOS</a></span><span class="sxs-lookup"><span data-stu-id="5b024-122"><a href="imc-setstatuswindowpos.md">IMC_SETSTATUSWINDOWPOS</a></span></span></dd> 
</dl>
</dd>

<dt>

<span data-ttu-id="5b024-123">*lParam*</span><span class="sxs-lookup"><span data-stu-id="5b024-123">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5b024-124">Données spécifiques à la commande, avec un format dépendant de la valeur du paramètre *wParam* .</span><span class="sxs-lookup"><span data-stu-id="5b024-124">Command-specific data, with format dependent on the value of the *wParam* parameter.</span></span> <span data-ttu-id="5b024-125">Pour plus d’informations, reportez-vous à la documentation de chaque commande.</span><span class="sxs-lookup"><span data-stu-id="5b024-125">For more information, refer to the documentation for each command.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5b024-126">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="5b024-126">Return value</span></span>

<span data-ttu-id="5b024-127">Le message retourne une valeur spécifique à la commande.</span><span class="sxs-lookup"><span data-stu-id="5b024-127">The message returns a command-specific value.</span></span>

## <a name="requirements"></a><span data-ttu-id="5b024-128">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5b024-128">Requirements</span></span>



| <span data-ttu-id="5b024-129">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5b024-129">Requirement</span></span> | <span data-ttu-id="5b024-130">Valeur</span><span class="sxs-lookup"><span data-stu-id="5b024-130">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5b024-131">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5b024-131">Minimum supported client</span></span><br/> | <span data-ttu-id="5b024-132">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5b024-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                                                                |
| <span data-ttu-id="5b024-133">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5b024-133">Minimum supported server</span></span><br/> | <span data-ttu-id="5b024-134">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5b024-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                                                      |
| <span data-ttu-id="5b024-135">En-tête</span><span class="sxs-lookup"><span data-stu-id="5b024-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="5b024-136"><dt>Winuser. h (inclure Windows. h); </dt> <dt>IMM. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5b024-136"><dt>Winuser.h (include Windows.h); </dt> <dt>Imm.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5b024-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5b024-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5b024-138">Gestionnaire de méthode d’entrée</span><span class="sxs-lookup"><span data-stu-id="5b024-138">Input Method Manager</span></span>](input-method-manager.md)
</dt> <dt>

[<span data-ttu-id="5b024-139">Messages du gestionnaire de méthode d’entrée</span><span class="sxs-lookup"><span data-stu-id="5b024-139">Input Method Manager Messages</span></span>](input-method-manager-messages.md)
</dt> <dt>

[<span data-ttu-id="5b024-140">IMC_CLOSESTATUSWINDOW</span><span class="sxs-lookup"><span data-stu-id="5b024-140">IMC_CLOSESTATUSWINDOW</span></span>](imc-closestatuswindow.md)
</dt> <dt>

[<span data-ttu-id="5b024-141">IMC_GETCANDIDATEPOS</span><span class="sxs-lookup"><span data-stu-id="5b024-141">IMC_GETCANDIDATEPOS</span></span>](imc-getcandidatepos.md)
</dt> <dt>

[<span data-ttu-id="5b024-142">IMC_GETCOMPOSITIONFONT</span><span class="sxs-lookup"><span data-stu-id="5b024-142">IMC_GETCOMPOSITIONFONT</span></span>](imc-getcompositionfont.md)
</dt> <dt>

[<span data-ttu-id="5b024-143">IMC_GETCOMPOSITIONWINDOW</span><span class="sxs-lookup"><span data-stu-id="5b024-143">IMC_GETCOMPOSITIONWINDOW</span></span>](imc-getcompositionwindow.md)
</dt> <dt>

[<span data-ttu-id="5b024-144">IMC_GETSTATUSWINDOWPOS</span><span class="sxs-lookup"><span data-stu-id="5b024-144">IMC_GETSTATUSWINDOWPOS</span></span>](imc-getstatuswindowpos.md)
</dt> <dt>

[<span data-ttu-id="5b024-145">IMC_OPENSTATUSWINDOW</span><span class="sxs-lookup"><span data-stu-id="5b024-145">IMC_OPENSTATUSWINDOW</span></span>](imc-openstatuswindow.md)
</dt> <dt>

[<span data-ttu-id="5b024-146">IMC_SETCANDIDATEPOS</span><span class="sxs-lookup"><span data-stu-id="5b024-146">IMC_SETCANDIDATEPOS</span></span>](imc-setcandidatepos.md)
</dt> <dt>

[<span data-ttu-id="5b024-147">IMC_SETCOMPOSITIONFONT</span><span class="sxs-lookup"><span data-stu-id="5b024-147">IMC_SETCOMPOSITIONFONT</span></span>](imc-setcompositionfont.md)
</dt> <dt>

[<span data-ttu-id="5b024-148">IMC_SETCOMPOSITIONWINDOW</span><span class="sxs-lookup"><span data-stu-id="5b024-148">IMC_SETCOMPOSITIONWINDOW</span></span>](imc-setcompositionwindow.md)
</dt> <dt>

[<span data-ttu-id="5b024-149">IMC_SETSTATUSWINDOWPOS</span><span class="sxs-lookup"><span data-stu-id="5b024-149">IMC_SETSTATUSWINDOWPOS</span></span>](imc-setstatuswindowpos.md)
</dt> </dl>

 

 
