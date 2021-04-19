---
description: Envoyé à une fenêtre déplacée par l’utilisateur. En traitant ce message, une application peut surveiller la position du rectangle de glissement et, si nécessaire, modifier sa position.
ms.assetid: f56a36c1-dbaa-438a-9e52-d12697a9dac9
title: Message WM_MOVING (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b5847189d64601ec999321920ead716fbdf22e2c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106513397"
---
# <a name="wm_moving-message"></a><span data-ttu-id="a9ae4-104">\_Message de déplacement WM</span><span class="sxs-lookup"><span data-stu-id="a9ae4-104">WM\_MOVING message</span></span>

<span data-ttu-id="a9ae4-105">Envoyé à une fenêtre déplacée par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="a9ae4-105">Sent to a window that the user is moving.</span></span> <span data-ttu-id="a9ae4-106">En traitant ce message, une application peut surveiller la position du rectangle de glissement et, si nécessaire, modifier sa position.</span><span class="sxs-lookup"><span data-stu-id="a9ae4-106">By processing this message, an application can monitor the position of the drag rectangle and, if needed, change its position.</span></span>

<span data-ttu-id="a9ae4-107">Une fenêtre reçoit ce message par le biais de sa fonction [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="a9ae4-107">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_MOVING                       0x0216
```



## <a name="parameters"></a><span data-ttu-id="a9ae4-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a9ae4-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a9ae4-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="a9ae4-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a9ae4-110">Ce paramètre n'est pas utilisé.</span><span class="sxs-lookup"><span data-stu-id="a9ae4-110">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="a9ae4-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a9ae4-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a9ae4-112">Pointeur vers une structure [**Rect**](/previous-versions//dd162897(v=vs.85)) avec la position actuelle de la fenêtre, en coordonnées d’écran.</span><span class="sxs-lookup"><span data-stu-id="a9ae4-112">A pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure with the current position of the window, in screen coordinates.</span></span> <span data-ttu-id="a9ae4-113">Pour modifier la position du rectangle de glissement, une application doit modifier les membres de cette structure.</span><span class="sxs-lookup"><span data-stu-id="a9ae4-113">To change the position of the drag rectangle, an application must change the members of this structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a9ae4-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="a9ae4-114">Return value</span></span>

<span data-ttu-id="a9ae4-115">Type : **LRESULT**</span><span class="sxs-lookup"><span data-stu-id="a9ae4-115">Type: **LRESULT**</span></span>

<span data-ttu-id="a9ae4-116">Une application doit retourner la **valeur true** si elle traite ce message.</span><span class="sxs-lookup"><span data-stu-id="a9ae4-116">An application should return **TRUE** if it processes this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="a9ae4-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a9ae4-117">Requirements</span></span>



| <span data-ttu-id="a9ae4-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a9ae4-118">Requirement</span></span> | <span data-ttu-id="a9ae4-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="a9ae4-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a9ae4-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a9ae4-120">Minimum supported client</span></span><br/> | <span data-ttu-id="a9ae4-121">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a9ae4-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="a9ae4-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a9ae4-122">Minimum supported server</span></span><br/> | <span data-ttu-id="a9ae4-123">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a9ae4-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="a9ae4-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="a9ae4-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="a9ae4-125"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a9ae4-125"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a9ae4-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a9ae4-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="a9ae4-127">**Référence**</span><span class="sxs-lookup"><span data-stu-id="a9ae4-127">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="a9ae4-128">**déplacement de WM \_**</span><span class="sxs-lookup"><span data-stu-id="a9ae4-128">**WM\_MOVE**</span></span>](wm-move.md)
</dt> <dt>

[<span data-ttu-id="a9ae4-129">**\_dimensionnement WM**</span><span class="sxs-lookup"><span data-stu-id="a9ae4-129">**WM\_SIZING**</span></span>](wm-sizing.md)
</dt> <dt>

<span data-ttu-id="a9ae4-130">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="a9ae4-130">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="a9ae4-131">Windows</span><span class="sxs-lookup"><span data-stu-id="a9ae4-131">Windows</span></span>](windows.md)
</dt> <dt>

<span data-ttu-id="a9ae4-132">**Autres ressources**</span><span class="sxs-lookup"><span data-stu-id="a9ae4-132">**Other Resources**</span></span>
</dt> <dt>

<span data-ttu-id="a9ae4-133">[**RECTANGULAIRE**](/previous-versions//dd162897(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="a9ae4-133">[**RECT**](/previous-versions//dd162897(v=vs.85))</span></span>
</dt> </dl>

 

 
