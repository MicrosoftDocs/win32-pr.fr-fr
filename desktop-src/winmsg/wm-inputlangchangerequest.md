---
description: Publié dans la fenêtre qui a le focus lorsque l’utilisateur choisit une nouvelle langue d’entrée, soit avec la touche de raccourci (spécifiée dans l’application du panneau de configuration du clavier), soit à partir de l’indicateur de la barre des tâches système.
ms.assetid: db38c31c-6ae4-4401-82b8-7fd220c1678c
title: Message WM_INPUTLANGCHANGEREQUEST (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b1df361c479978083c29281764e65c48b131c22b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106529170"
---
# <a name="wm_inputlangchangerequest-message"></a><span data-ttu-id="f436b-103">\_Message WM INPUTLANGCHANGEREQUEST</span><span class="sxs-lookup"><span data-stu-id="f436b-103">WM\_INPUTLANGCHANGEREQUEST message</span></span>

<span data-ttu-id="f436b-104">Publié dans la fenêtre qui a le focus lorsque l’utilisateur choisit une nouvelle langue d’entrée, soit avec la touche de raccourci (spécifiée dans l’application du panneau de configuration du clavier), soit à partir de l’indicateur de la barre des tâches système.</span><span class="sxs-lookup"><span data-stu-id="f436b-104">Posted to the window with the focus when the user chooses a new input language, either with the hotkey (specified in the Keyboard control panel application) or from the indicator on the system taskbar.</span></span> <span data-ttu-id="f436b-105">Une application peut accepter la modification en transmettant le message à la fonction [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) ou refuser la modification (et l’empêcher d’avoir lieu) en retournant immédiatement.</span><span class="sxs-lookup"><span data-stu-id="f436b-105">An application can accept the change by passing the message to the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function or reject the change (and prevent it from taking place) by returning immediately.</span></span>

<span data-ttu-id="f436b-106">Une fenêtre reçoit ce message par le biais de sa fonction [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="f436b-106">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_INPUTLANGCHANGEREQUEST       0x0050
```



## <a name="parameters"></a><span data-ttu-id="f436b-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f436b-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f436b-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f436b-108">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f436b-109">Nouveaux paramètres régionaux d’entrée.</span><span class="sxs-lookup"><span data-stu-id="f436b-109">The new input locale.</span></span> <span data-ttu-id="f436b-110">Ce paramètre peut être une combinaison des indicateurs suivants.</span><span class="sxs-lookup"><span data-stu-id="f436b-110">This parameter can be a combination of the following flags.</span></span>



| <span data-ttu-id="f436b-111">Valeur</span><span class="sxs-lookup"><span data-stu-id="f436b-111">Value</span></span>                                                                                                                                                                                                                                                            | <span data-ttu-id="f436b-112">Signification</span><span class="sxs-lookup"><span data-stu-id="f436b-112">Meaning</span></span>                                                                                                                                                                    |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="INPUTLANGCHANGE_BACKWARD"></span><span id="inputlangchange_backward"></span><dl> <span data-ttu-id="f436b-113"><dt>**INPUTLANGCHANGE \_**</dt> <dt>0x0004</dt> inversé</span><span class="sxs-lookup"><span data-stu-id="f436b-113"><dt>**INPUTLANGCHANGE\_BACKWARD**</dt> <dt>0x0004</dt></span></span> </dl>       | <span data-ttu-id="f436b-114">Une touche d’accès rapide a été utilisée pour choisir les paramètres régionaux d’entrée précédents dans la liste des paramètres régionaux d’entrée installés.</span><span class="sxs-lookup"><span data-stu-id="f436b-114">A hot key was used to choose the previous input locale in the installed list of input locales.</span></span> <span data-ttu-id="f436b-115">Cet indicateur ne peut pas être utilisé avec l' \_ indicateur INPUTLANGCHANGE Forward.</span><span class="sxs-lookup"><span data-stu-id="f436b-115">This flag cannot be used with the INPUTLANGCHANGE\_FORWARD flag.</span></span><br/> |
| <span id="INPUTLANGCHANGE_FORWARD"></span><span id="inputlangchange_forward"></span><dl> <span data-ttu-id="f436b-116"><dt>**INPUTLANGCHANGE \_ TRANSFÉRER**</dt> <dt>0x0002</dt></span><span class="sxs-lookup"><span data-stu-id="f436b-116"><dt>**INPUTLANGCHANGE\_FORWARD**</dt> <dt>0x0002</dt></span></span> </dl>          | <span data-ttu-id="f436b-117">Une touche d’accès rapide a été utilisée pour choisir les paramètres régionaux d’entrée suivants dans la liste des paramètres régionaux d’entrée installés.</span><span class="sxs-lookup"><span data-stu-id="f436b-117">A hot key was used to choose the next input locale in the installed list of input locales.</span></span> <span data-ttu-id="f436b-118">Cet indicateur ne peut pas être utilisé avec l' \_ indicateur INPUTLANGCHANGE Backward.</span><span class="sxs-lookup"><span data-stu-id="f436b-118">This flag cannot be used with the INPUTLANGCHANGE\_BACKWARD flag.</span></span><br/>    |
| <span id="INPUTLANGCHANGE_SYSCHARSET"></span><span id="inputlangchange_syscharset"></span><dl> <span data-ttu-id="f436b-119"><dt>**INPUTLANGCHANGE \_ SYSCHARSET**</dt> <dt>0x0001</dt></span><span class="sxs-lookup"><span data-stu-id="f436b-119"><dt>**INPUTLANGCHANGE\_SYSCHARSET**</dt> <dt>0x0001</dt></span></span> </dl> | <span data-ttu-id="f436b-120">La nouvelle disposition de clavier de paramètres régionaux d’entrée peut être utilisée avec le jeu de caractères système.</span><span class="sxs-lookup"><span data-stu-id="f436b-120">The new input locale's keyboard layout can be used with the system character set.</span></span><br/>                                                                               |



 

</dd> <dt>

<span data-ttu-id="f436b-121">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f436b-121">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f436b-122">Identificateur de paramètres régionaux d’entrée.</span><span class="sxs-lookup"><span data-stu-id="f436b-122">The input locale identifier.</span></span> <span data-ttu-id="f436b-123">Pour plus d’informations, consultez [langues, paramètres régionaux et dispositions de clavier](../inputdev/about-keyboard-input.md).</span><span class="sxs-lookup"><span data-stu-id="f436b-123">For more information, see [Languages, Locales, and Keyboard Layouts](../inputdev/about-keyboard-input.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f436b-124">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="f436b-124">Return value</span></span>

<span data-ttu-id="f436b-125">Type : **LRESULT**</span><span class="sxs-lookup"><span data-stu-id="f436b-125">Type: **LRESULT**</span></span>

<span data-ttu-id="f436b-126">Ce message est publié, non envoyé, à l’application. la valeur de retour est donc ignorée.</span><span class="sxs-lookup"><span data-stu-id="f436b-126">This message is posted, not sent, to the application, so the return value is ignored.</span></span> <span data-ttu-id="f436b-127">Pour accepter la modification, l’application doit transmettre le message à [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca).</span><span class="sxs-lookup"><span data-stu-id="f436b-127">To accept the change, the application should pass the message to [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca).</span></span> <span data-ttu-id="f436b-128">Pour refuser la modification, l’application doit retourner zéro sans appeler **DefWindowProc**.</span><span class="sxs-lookup"><span data-stu-id="f436b-128">To reject the change, the application should return zero without calling **DefWindowProc**.</span></span>

## <a name="remarks"></a><span data-ttu-id="f436b-129">Notes</span><span class="sxs-lookup"><span data-stu-id="f436b-129">Remarks</span></span>

<span data-ttu-id="f436b-130">Lorsque la fonction [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) reçoit le message **WM \_ INPUTLANGCHANGEREQUEST** , elle active les nouveaux paramètres régionaux d’entrée et avertit l’application de la modification en envoyant le message [**WM \_ INPUTLANGCHANGE**](wm-inputlangchange.md) .</span><span class="sxs-lookup"><span data-stu-id="f436b-130">When the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function receives the **WM\_INPUTLANGCHANGEREQUEST** message, it activates the new input locale and notifies the application of the change by sending the [**WM\_INPUTLANGCHANGE**](wm-inputlangchange.md) message.</span></span>

<span data-ttu-id="f436b-131">L’indicateur de langue n’est présent dans la barre des tâches que si vous avez installé plusieurs dispositions de clavier et si vous avez activé l’indicateur à l’aide de l’application du panneau de configuration du clavier.</span><span class="sxs-lookup"><span data-stu-id="f436b-131">The language indicator is present on the taskbar only if you have installed more than one keyboard layout and if you have enabled the indicator using the Keyboard control panel application.</span></span>

## <a name="requirements"></a><span data-ttu-id="f436b-132">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f436b-132">Requirements</span></span>



| <span data-ttu-id="f436b-133">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f436b-133">Requirement</span></span> | <span data-ttu-id="f436b-134">Valeur</span><span class="sxs-lookup"><span data-stu-id="f436b-134">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f436b-135">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f436b-135">Minimum supported client</span></span><br/> | <span data-ttu-id="f436b-136">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f436b-136">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="f436b-137">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f436b-137">Minimum supported server</span></span><br/> | <span data-ttu-id="f436b-138">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f436b-138">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="f436b-139">En-tête</span><span class="sxs-lookup"><span data-stu-id="f436b-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="f436b-140"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f436b-140"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f436b-141">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f436b-141">See also</span></span>

<dl> <dt>

<span data-ttu-id="f436b-142">**Référence**</span><span class="sxs-lookup"><span data-stu-id="f436b-142">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="f436b-143">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="f436b-143">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[<span data-ttu-id="f436b-144">**\_INPUTLANGCHANGE WM**</span><span class="sxs-lookup"><span data-stu-id="f436b-144">**WM\_INPUTLANGCHANGE**</span></span>](wm-inputlangchange.md)
</dt> <dt>

<span data-ttu-id="f436b-145">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="f436b-145">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="f436b-146">Windows</span><span class="sxs-lookup"><span data-stu-id="f436b-146">Windows</span></span>](windows.md)
</dt> </dl>

 

 
