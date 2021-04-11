---
description: Envoyé à la fenêtre la plus affectée au premier plan une fois que la langue d’entrée d’une application a été modifiée. Vous devez apporter des paramètres spécifiques à l’application et transmettre le message à la fonction DefWindowProc, qui le transmet à toutes les fenêtres enfants de premier niveau.
ms.assetid: 4d403b1d-f6f7-40d5-9bf5-6a9c4da0803c
title: Message WM_INPUTLANGCHANGE (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b0cdf04a775873e4cefe2c79269c14bd3d4da8d8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112846"
---
# <a name="wm_inputlangchange-message"></a><span data-ttu-id="dc6ed-104">\_Message WM INPUTLANGCHANGE</span><span class="sxs-lookup"><span data-stu-id="dc6ed-104">WM\_INPUTLANGCHANGE message</span></span>

<span data-ttu-id="dc6ed-105">Envoyé à la fenêtre la plus affectée au premier plan une fois que la langue d’entrée d’une application a été modifiée.</span><span class="sxs-lookup"><span data-stu-id="dc6ed-105">Sent to the topmost affected window after an application's input language has been changed.</span></span> <span data-ttu-id="dc6ed-106">Vous devez apporter des paramètres spécifiques à l’application et transmettre le message à la fonction [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) , qui le transmet à toutes les fenêtres enfants de premier niveau.</span><span class="sxs-lookup"><span data-stu-id="dc6ed-106">You should make any application-specific settings and pass the message to the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function, which passes the message to all first-level child windows.</span></span> <span data-ttu-id="dc6ed-107">Ces fenêtres enfants peuvent transmettre le message à [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) pour qu’il transmette le message à leurs fenêtres enfants, et ainsi de suite.</span><span class="sxs-lookup"><span data-stu-id="dc6ed-107">These child windows can pass the message to [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) to have it pass the message to their child windows, and so on.</span></span>

<span data-ttu-id="dc6ed-108">Une fenêtre reçoit ce message par le biais de sa fonction [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="dc6ed-108">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_INPUTLANGCHANGE              0x0051
```



## <a name="parameters"></a><span data-ttu-id="dc6ed-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="dc6ed-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dc6ed-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="dc6ed-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="dc6ed-111">Jeu de caractères des nouveaux paramètres régionaux.</span><span class="sxs-lookup"><span data-stu-id="dc6ed-111">The character set of the new locale.</span></span>

</dd> <dt>

<span data-ttu-id="dc6ed-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="dc6ed-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="dc6ed-113">Identificateur de paramètres régionaux d’entrée.</span><span class="sxs-lookup"><span data-stu-id="dc6ed-113">The input locale identifier.</span></span> <span data-ttu-id="dc6ed-114">Pour plus d’informations, consultez [langues, paramètres régionaux et dispositions de clavier](../inputdev/about-keyboard-input.md).</span><span class="sxs-lookup"><span data-stu-id="dc6ed-114">For more information, see [Languages, Locales, and Keyboard Layouts](../inputdev/about-keyboard-input.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dc6ed-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="dc6ed-115">Return value</span></span>

<span data-ttu-id="dc6ed-116">Type : **LRESULT**</span><span class="sxs-lookup"><span data-stu-id="dc6ed-116">Type: **LRESULT**</span></span>

<span data-ttu-id="dc6ed-117">Une application doit retourner une valeur différente de zéro si elle traite ce message.</span><span class="sxs-lookup"><span data-stu-id="dc6ed-117">An application should return nonzero if it processes this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="dc6ed-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="dc6ed-118">Requirements</span></span>



| <span data-ttu-id="dc6ed-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="dc6ed-119">Requirement</span></span> | <span data-ttu-id="dc6ed-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="dc6ed-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dc6ed-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="dc6ed-121">Minimum supported client</span></span><br/> | <span data-ttu-id="dc6ed-122">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="dc6ed-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="dc6ed-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="dc6ed-123">Minimum supported server</span></span><br/> | <span data-ttu-id="dc6ed-124">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="dc6ed-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="dc6ed-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="dc6ed-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="dc6ed-126"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="dc6ed-126"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dc6ed-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="dc6ed-127">See also</span></span>

<dl> <dt>

<span data-ttu-id="dc6ed-128">**Référence**</span><span class="sxs-lookup"><span data-stu-id="dc6ed-128">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="dc6ed-129">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="dc6ed-129">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[<span data-ttu-id="dc6ed-130">**\_INPUTLANGCHANGEREQUEST WM**</span><span class="sxs-lookup"><span data-stu-id="dc6ed-130">**WM\_INPUTLANGCHANGEREQUEST**</span></span>](wm-inputlangchangerequest.md)
</dt> <dt>

<span data-ttu-id="dc6ed-131">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="dc6ed-131">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="dc6ed-132">Windows</span><span class="sxs-lookup"><span data-stu-id="dc6ed-132">Windows</span></span>](windows.md)
</dt> </dl>

 

 
