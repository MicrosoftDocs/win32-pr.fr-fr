---
description: Envoyé à une fenêtre dont la taille, la position ou l’emplacement dans l’ordre de plan a été modifié à la suite d’un appel à la fonction SetWindowPos ou à une autre fonction de gestion de fenêtre.
ms.assetid: 1eabd0b1-1f92-4576-b7fb-8af50fb04526
title: Message WM_WINDOWPOSCHANGED (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5d9bda353a1c7546727818a8a3975696000da0e8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112842"
---
# <a name="wm_windowposchanged-message"></a><span data-ttu-id="faed2-103">\_Message WM WINDOWPOSCHANGED</span><span class="sxs-lookup"><span data-stu-id="faed2-103">WM\_WINDOWPOSCHANGED message</span></span>

<span data-ttu-id="faed2-104">Envoyé à une fenêtre dont la taille, la position ou l’emplacement dans l’ordre de plan a été modifié à la suite d’un appel à la fonction [**SetWindowPos**](/windows/win32/api/winuser/nf-winuser-setwindowpos) ou à une autre fonction de gestion de fenêtre.</span><span class="sxs-lookup"><span data-stu-id="faed2-104">Sent to a window whose size, position, or place in the Z order has changed as a result of a call to the [**SetWindowPos**](/windows/win32/api/winuser/nf-winuser-setwindowpos) function or another window-management function.</span></span>

<span data-ttu-id="faed2-105">Une fenêtre reçoit ce message par le biais de sa fonction [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="faed2-105">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_WINDOWPOSCHANGED             0x0047
```



## <a name="parameters"></a><span data-ttu-id="faed2-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="faed2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="faed2-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="faed2-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="faed2-108">Ce paramètre n'est pas utilisé.</span><span class="sxs-lookup"><span data-stu-id="faed2-108">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="faed2-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="faed2-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="faed2-110">Pointeur vers une structure [**WINDOWPOS**](/windows/win32/api/winuser/ns-winuser-windowpos) qui contient des informations sur les nouvelles taille et position de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="faed2-110">A pointer to a [**WINDOWPOS**](/windows/win32/api/winuser/ns-winuser-windowpos) structure that contains information about the window's new size and position.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="faed2-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="faed2-111">Return value</span></span>

<span data-ttu-id="faed2-112">Type : **LRESULT**</span><span class="sxs-lookup"><span data-stu-id="faed2-112">Type: **LRESULT**</span></span>

<span data-ttu-id="faed2-113">Si une application traite ce message, elle doit retourner la valeur zéro.</span><span class="sxs-lookup"><span data-stu-id="faed2-113">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="faed2-114">Notes</span><span class="sxs-lookup"><span data-stu-id="faed2-114">Remarks</span></span>

<span data-ttu-id="faed2-115">Par défaut, la fonction [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) envoie les messages de [**\_ taille WM**](wm-size.md) et de [**\_ déplacement WM**](wm-move.md) à la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="faed2-115">By default, the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function sends the [**WM\_SIZE**](wm-size.md) and [**WM\_MOVE**](wm-move.md) messages to the window.</span></span> <span data-ttu-id="faed2-116">Les messages de **\_ taille WM** et de **\_ déplacement WM** ne sont pas envoyés si une application gère le message **WM \_ WINDOWPOSCHANGED** sans appeler **DefWindowProc**.</span><span class="sxs-lookup"><span data-stu-id="faed2-116">The **WM\_SIZE** and **WM\_MOVE** messages are not sent if an application handles the **WM\_WINDOWPOSCHANGED** message without calling **DefWindowProc**.</span></span> <span data-ttu-id="faed2-117">Il est plus efficace d’effectuer un traitement des modifications de déplacement ou de taille pendant le message **WM \_ WINDOWPOSCHANGED** sans appeler **DefWindowProc**.</span><span class="sxs-lookup"><span data-stu-id="faed2-117">It is more efficient to perform any move or size change processing during the **WM\_WINDOWPOSCHANGED** message without calling **DefWindowProc**.</span></span>

## <a name="requirements"></a><span data-ttu-id="faed2-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="faed2-118">Requirements</span></span>



| <span data-ttu-id="faed2-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="faed2-119">Requirement</span></span> | <span data-ttu-id="faed2-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="faed2-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="faed2-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="faed2-121">Minimum supported client</span></span><br/> | <span data-ttu-id="faed2-122">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="faed2-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="faed2-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="faed2-123">Minimum supported server</span></span><br/> | <span data-ttu-id="faed2-124">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="faed2-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="faed2-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="faed2-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="faed2-126"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="faed2-126"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="faed2-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="faed2-127">See also</span></span>

<dl> <dt>

<span data-ttu-id="faed2-128">**Référence**</span><span class="sxs-lookup"><span data-stu-id="faed2-128">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="faed2-129">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="faed2-129">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[<span data-ttu-id="faed2-130">**EndDeferWindowPos**</span><span class="sxs-lookup"><span data-stu-id="faed2-130">**EndDeferWindowPos**</span></span>](/windows/win32/api/winuser/nf-winuser-enddeferwindowpos)
</dt> <dt>

[<span data-ttu-id="faed2-131">**SetWindowPos**</span><span class="sxs-lookup"><span data-stu-id="faed2-131">**SetWindowPos**</span></span>](/windows/win32/api/winuser/nf-winuser-setwindowpos)
</dt> <dt>

[<span data-ttu-id="faed2-132">**WINDOWPOS**</span><span class="sxs-lookup"><span data-stu-id="faed2-132">**WINDOWPOS**</span></span>](/windows/win32/api/winuser/ns-winuser-windowpos)
</dt> <dt>

[<span data-ttu-id="faed2-133">**déplacement de WM \_**</span><span class="sxs-lookup"><span data-stu-id="faed2-133">**WM\_MOVE**</span></span>](wm-move.md)
</dt> <dt>

[<span data-ttu-id="faed2-134">**taille du WM \_**</span><span class="sxs-lookup"><span data-stu-id="faed2-134">**WM\_SIZE**</span></span>](wm-size.md)
</dt> <dt>

[<span data-ttu-id="faed2-135">**\_WINDOWPOSCHANGING WM**</span><span class="sxs-lookup"><span data-stu-id="faed2-135">**WM\_WINDOWPOSCHANGING**</span></span>](wm-windowposchanging.md)
</dt> <dt>

<span data-ttu-id="faed2-136">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="faed2-136">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="faed2-137">Windows</span><span class="sxs-lookup"><span data-stu-id="faed2-137">Windows</span></span>](windows.md)
</dt> </dl>

 

 
