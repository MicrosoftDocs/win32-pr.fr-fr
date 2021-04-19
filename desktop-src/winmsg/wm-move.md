---
description: Envoyé après qu’une fenêtre a été déplacée.
ms.assetid: 552ddc26-fe63-449b-8c82-bb927a2c1c41
title: Message WM_MOVE (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 56004ec47266a50bf2ac82a828b9046c84a8ebfb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106520577"
---
# <a name="wm_move-message"></a><span data-ttu-id="a0cfe-103">WM- \_ déplacer un message</span><span class="sxs-lookup"><span data-stu-id="a0cfe-103">WM\_MOVE message</span></span>

<span data-ttu-id="a0cfe-104">Envoyé après qu’une fenêtre a été déplacée.</span><span class="sxs-lookup"><span data-stu-id="a0cfe-104">Sent after a window has been moved.</span></span>

<span data-ttu-id="a0cfe-105">Une fenêtre reçoit ce message par le biais de sa fonction [**WindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca) .</span><span class="sxs-lookup"><span data-stu-id="a0cfe-105">A window receives this message through its [**WindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca) function.</span></span>


```C++
#define WM_MOVE                         0x0003
```



## <a name="parameters"></a><span data-ttu-id="a0cfe-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a0cfe-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a0cfe-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="a0cfe-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a0cfe-108">Ce paramètre n'est pas utilisé.</span><span class="sxs-lookup"><span data-stu-id="a0cfe-108">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="a0cfe-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a0cfe-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a0cfe-110">Coordonnées x et y de l’angle supérieur gauche de la zone cliente de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="a0cfe-110">The x and y coordinates of the upper-left corner of the client area of the window.</span></span> <span data-ttu-id="a0cfe-111">Le mot de poids faible contient la coordonnée x, tandis que le mot de poids fort contient la coordonnée y.</span><span class="sxs-lookup"><span data-stu-id="a0cfe-111">The low-order word contains the x-coordinate while the high-order word contains the y coordinate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a0cfe-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="a0cfe-112">Return value</span></span>

<span data-ttu-id="a0cfe-113">Type : **LRESULT**</span><span class="sxs-lookup"><span data-stu-id="a0cfe-113">Type: **LRESULT**</span></span>

<span data-ttu-id="a0cfe-114">Si une application traite ce message, elle doit retourner la valeur zéro.</span><span class="sxs-lookup"><span data-stu-id="a0cfe-114">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="a0cfe-115">Notes</span><span class="sxs-lookup"><span data-stu-id="a0cfe-115">Remarks</span></span>

<span data-ttu-id="a0cfe-116">Les paramètres sont fournis en coordonnées d’écran pour les fenêtres superposées et les fenêtres contextuelles et dans les coordonnées client-parent pour les fenêtres enfants.</span><span class="sxs-lookup"><span data-stu-id="a0cfe-116">The parameters are given in screen coordinates for overlapped and pop-up windows and in parent-client coordinates for child windows.</span></span>

<span data-ttu-id="a0cfe-117">L’exemple suivant montre comment obtenir la position à partir du paramètre *lParam* .</span><span class="sxs-lookup"><span data-stu-id="a0cfe-117">The following example demonstrates how to obtain the position from the *lParam* parameter.</span></span>


```
xPos = (int)(short) LOWORD(lParam);   // horizontal position 
yPos = (int)(short) HIWORD(lParam);   // vertical position 
```



<span data-ttu-id="a0cfe-118">Vous pouvez également utiliser la macro [**MAKEPOINTS**](/windows/win32/api/wingdi/nf-wingdi-makepoints) pour convertir le paramètre *lParam* en une structure [**points**](/previous-versions//dd162808(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="a0cfe-118">You can also use the [**MAKEPOINTS**](/windows/win32/api/wingdi/nf-wingdi-makepoints) macro to convert the *lParam* parameter to a [**POINTS**](/previous-versions//dd162808(v=vs.85)) structure.</span></span>

<span data-ttu-id="a0cfe-119">La fonction [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) envoie les messages de **\_ taille WM** et de **\_ déplacement WM** quand elle traite le message [**WM \_ WINDOWPOSCHANGED**](wm-windowposchanged.md) .</span><span class="sxs-lookup"><span data-stu-id="a0cfe-119">The [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function sends the **WM\_SIZE** and **WM\_MOVE** messages when it processes the [**WM\_WINDOWPOSCHANGED**](wm-windowposchanged.md) message.</span></span>
<span data-ttu-id="a0cfe-120">Les messages de **\_ taille WM** et de **\_ déplacement WM** ne sont pas envoyés si une application gère le message **WM \_ WINDOWPOSCHANGED** sans appeler **DefWindowProc**.</span><span class="sxs-lookup"><span data-stu-id="a0cfe-120">The **WM\_SIZE** and **WM\_MOVE** messages are not sent if an application handles the **WM\_WINDOWPOSCHANGED** message without calling **DefWindowProc**.</span></span>

## <a name="requirements"></a><span data-ttu-id="a0cfe-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a0cfe-121">Requirements</span></span>



| <span data-ttu-id="a0cfe-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a0cfe-122">Requirement</span></span> | <span data-ttu-id="a0cfe-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="a0cfe-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a0cfe-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a0cfe-124">Minimum supported client</span></span><br/> | <span data-ttu-id="a0cfe-125">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a0cfe-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="a0cfe-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a0cfe-126">Minimum supported server</span></span><br/> | <span data-ttu-id="a0cfe-127">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a0cfe-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="a0cfe-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="a0cfe-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="a0cfe-129"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a0cfe-129"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a0cfe-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a0cfe-130">See also</span></span>

<dl> <dt>

<span data-ttu-id="a0cfe-131">**Référence**</span><span class="sxs-lookup"><span data-stu-id="a0cfe-131">**Reference**</span></span>
</dt> <dt>

<span data-ttu-id="a0cfe-132">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="a0cfe-132">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="a0cfe-133">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="a0cfe-133">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="a0cfe-134">**\_WINDOWPOSCHANGED WM**</span><span class="sxs-lookup"><span data-stu-id="a0cfe-134">**WM\_WINDOWPOSCHANGED**</span></span>](wm-windowposchanged.md)
</dt> <dt>

<span data-ttu-id="a0cfe-135">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="a0cfe-135">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="a0cfe-136">Windows</span><span class="sxs-lookup"><span data-stu-id="a0cfe-136">Windows</span></span>](windows.md)
</dt> <dt>

<span data-ttu-id="a0cfe-137">**Autres ressources**</span><span class="sxs-lookup"><span data-stu-id="a0cfe-137">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="a0cfe-138">**MAKEPOINTS**</span><span class="sxs-lookup"><span data-stu-id="a0cfe-138">**MAKEPOINTS**</span></span>](/windows/win32/api/wingdi/nf-wingdi-makepoints)
</dt> <dt>

<span data-ttu-id="a0cfe-139">[**MOMENTS**](/previous-versions//dd162808(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="a0cfe-139">[**POINTS**](/previous-versions//dd162808(v=vs.85))</span></span>
</dt> </dl>

 

 
