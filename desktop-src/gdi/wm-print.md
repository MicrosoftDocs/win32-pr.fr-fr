---
description: Le \_ message d’impression WM est envoyé à une fenêtre pour demander qu’il se dessine dans le contexte de périphérique spécifié, le plus souvent dans un contexte de périphérique d’impression.
ms.assetid: e6be2ecd-603a-405f-8a48-68d971e1f6de
title: Message WM_PRINT (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5a012d26e4357a639a7eb8d7930937a06a991124
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104034369"
---
# <a name="wm_print-message"></a><span data-ttu-id="94521-103">\_Message d’impression WM</span><span class="sxs-lookup"><span data-stu-id="94521-103">WM\_PRINT message</span></span>

<span data-ttu-id="94521-104">Le message d' **\_ impression WM** est envoyé à une fenêtre pour demander qu’il se dessine dans le contexte de périphérique spécifié, le plus souvent dans un contexte de périphérique d’impression.</span><span class="sxs-lookup"><span data-stu-id="94521-104">The **WM\_PRINT** message is sent to a window to request that it draw itself in the specified device context, most commonly in a printer device context.</span></span>

<span data-ttu-id="94521-105">Une fenêtre reçoit ce message par le biais de sa fonction [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="94521-105">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
LRESULT CALLBACK WindowProc(
  HWND hwnd, 
  UINT  uMsg, 
  WPARAM wParam, 
  LPARAM lParam     
);
```



## <a name="parameters"></a><span data-ttu-id="94521-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="94521-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="94521-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="94521-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="94521-108">Handle vers le contexte de périphérique dans lequel dessiner.</span><span class="sxs-lookup"><span data-stu-id="94521-108">A handle to the device context to draw in.</span></span>

</dd> <dt>

<span data-ttu-id="94521-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="94521-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="94521-110">Options de dessin.</span><span class="sxs-lookup"><span data-stu-id="94521-110">The drawing options.</span></span> <span data-ttu-id="94521-111">Ce paramètre peut être une ou plusieurs des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="94521-111">This parameter can be one or more of the following values.</span></span>



| <span data-ttu-id="94521-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="94521-112">Value</span></span>                                                                                                                                                                  | <span data-ttu-id="94521-113">Signification</span><span class="sxs-lookup"><span data-stu-id="94521-113">Meaning</span></span>                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| <span id="PRF_CHECKVISIBLE"></span><span id="prf_checkvisible"></span><dl> <span data-ttu-id="94521-114"><dt>**\_CHECKVISIBLE PRF**</dt></span><span class="sxs-lookup"><span data-stu-id="94521-114"><dt>**PRF\_CHECKVISIBLE**</dt></span></span> </dl> | <span data-ttu-id="94521-115">Dessine la fenêtre uniquement si elle est visible.</span><span class="sxs-lookup"><span data-stu-id="94521-115">Draws the window only if it is visible.</span></span><br/>          |
| <span id="PRF_CHILDREN"></span><span id="prf_children"></span><dl> <span data-ttu-id="94521-116"><dt>**\_enfants PRF**</dt></span><span class="sxs-lookup"><span data-stu-id="94521-116"><dt>**PRF\_CHILDREN**</dt></span></span> </dl>             | <span data-ttu-id="94521-117">Dessine toutes les fenêtres enfants visibles.</span><span class="sxs-lookup"><span data-stu-id="94521-117">Draws all visible children windows.</span></span><br/>              |
| <span id="PRF_CLIENT"></span><span id="prf_client"></span><dl> <span data-ttu-id="94521-118"><dt>**\_client PRF**</dt></span><span class="sxs-lookup"><span data-stu-id="94521-118"><dt>**PRF\_CLIENT**</dt></span></span> </dl>                   | <span data-ttu-id="94521-119">Dessine la zone cliente de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="94521-119">Draws the client area of the window.</span></span><br/>             |
| <span id="PRF_ERASEBKGND"></span><span id="prf_erasebkgnd"></span><dl> <span data-ttu-id="94521-120"><dt>**\_ERASEBKGND PRF**</dt></span><span class="sxs-lookup"><span data-stu-id="94521-120"><dt>**PRF\_ERASEBKGND**</dt></span></span> </dl>       | <span data-ttu-id="94521-121">Efface l’arrière-plan avant de dessiner la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="94521-121">Erases the background before drawing the window.</span></span><br/> |
| <span id="PRF_NONCLIENT"></span><span id="prf_nonclient"></span><dl> <span data-ttu-id="94521-122"><dt>**PRF non \_ client**</dt></span><span class="sxs-lookup"><span data-stu-id="94521-122"><dt>**PRF\_NONCLIENT**</dt></span></span> </dl>          | <span data-ttu-id="94521-123">Dessine la zone non cliente de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="94521-123">Draws the nonclient area of the window.</span></span><br/>          |
| <span id="PRF_OWNED"></span><span id="prf_owned"></span><dl> <span data-ttu-id="94521-124"><dt>**PRF \_ appartenant**</dt></span><span class="sxs-lookup"><span data-stu-id="94521-124"><dt>**PRF\_OWNED**</dt></span></span> </dl>                      | <span data-ttu-id="94521-125">Dessine toutes les fenêtres détenues.</span><span class="sxs-lookup"><span data-stu-id="94521-125">Draws all owned windows.</span></span><br/>                         |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="94521-126">Notes</span><span class="sxs-lookup"><span data-stu-id="94521-126">Remarks</span></span>

<span data-ttu-id="94521-127">La fonction [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) traite ce message en fonction de l’option de dessin spécifiée : si PRF \_ CHECKVISIBLE est spécifié et que la fenêtre n’est pas visible, ne rien faire, si PRF \_ non client est spécifié, dessinez la zone non cliente dans le contexte de périphérique spécifié, si PRF \_ ERASEBKGND est spécifié, envoyez la fenêtre un message [**WM \_ ERASEBKGND**](../winmsg/wm-erasebkgnd.md) , si \_ le client PRF est spécifié, envoyez à la fenêtre un message [**WM \_ PRINTCLIENT**](wm-printclient.md) , si les \_ enfants PRF sont définis, envoyer **\_** \_ **\_** un message d’impression WM à chaque fenêtre enfant visible.</span><span class="sxs-lookup"><span data-stu-id="94521-127">The [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function processes this message based on which drawing option is specified: if PRF\_CHECKVISIBLE is specified and the window is not visible, do nothing, if PRF\_NONCLIENT is specified, draw the nonclient area in the specified device context, if PRF\_ERASEBKGND is specified, send the window a [**WM\_ERASEBKGND**](../winmsg/wm-erasebkgnd.md) message, if PRF\_CLIENT is specified, send the window a [**WM\_PRINTCLIENT**](wm-printclient.md) message, if PRF\_CHILDREN is set, send each visible child window a **WM\_PRINT** message, if PRF\_OWNED is set, send each visible owned window a **WM\_PRINT** message.</span></span>

## <a name="requirements"></a><span data-ttu-id="94521-128">Spécifications</span><span class="sxs-lookup"><span data-stu-id="94521-128">Requirements</span></span>



| <span data-ttu-id="94521-129">Condition requise</span><span class="sxs-lookup"><span data-stu-id="94521-129">Requirement</span></span> | <span data-ttu-id="94521-130">Valeur</span><span class="sxs-lookup"><span data-stu-id="94521-130">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="94521-131">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="94521-131">Minimum supported client</span></span><br/> | <span data-ttu-id="94521-132">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="94521-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="94521-133">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="94521-133">Minimum supported server</span></span><br/> | <span data-ttu-id="94521-134">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="94521-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="94521-135">En-tête</span><span class="sxs-lookup"><span data-stu-id="94521-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="94521-136"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="94521-136"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="94521-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="94521-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="94521-138">Vue d’ensemble de la peinture et du dessin</span><span class="sxs-lookup"><span data-stu-id="94521-138">Painting and Drawing Overview</span></span>](painting-and-drawing.md)
</dt> <dt>

[<span data-ttu-id="94521-139">Peinture et dessin de messages</span><span class="sxs-lookup"><span data-stu-id="94521-139">Painting and Drawing Messages</span></span>](painting-and-drawing-messages.md)
</dt> <dt>

[<span data-ttu-id="94521-140">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="94521-140">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[<span data-ttu-id="94521-141">**\_ERASEBKGND WM**</span><span class="sxs-lookup"><span data-stu-id="94521-141">**WM\_ERASEBKGND**</span></span>](../winmsg/wm-erasebkgnd.md)
</dt> <dt>

[<span data-ttu-id="94521-142">**\_PRINTCLIENT WM**</span><span class="sxs-lookup"><span data-stu-id="94521-142">**WM\_PRINTCLIENT**</span></span>](wm-printclient.md)
</dt> </dl>

 

 
