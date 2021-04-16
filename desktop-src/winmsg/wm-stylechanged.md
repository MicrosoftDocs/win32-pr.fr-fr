---
description: Envoyé à une fenêtre après que la fonction SetWindowLong a modifié un ou plusieurs styles de la fenêtre.
ms.assetid: 37bc4e1a-f75d-4851-8dee-97fa2da90254
title: Message WM_STYLECHANGED (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d5429db06dea95dbbc003e432a2b619c5cf8d056
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104529835"
---
# <a name="wm_stylechanged-message"></a><span data-ttu-id="3a254-103">\_Message WM STYLECHANGED</span><span class="sxs-lookup"><span data-stu-id="3a254-103">WM\_STYLECHANGED message</span></span>

<span data-ttu-id="3a254-104">Envoyé à une fenêtre après que la fonction [**SetWindowLong**](/windows/win32/api/winuser/nf-winuser-setwindowlonga) a modifié un ou plusieurs styles de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="3a254-104">Sent to a window after the [**SetWindowLong**](/windows/win32/api/winuser/nf-winuser-setwindowlonga) function has changed one or more of the window's styles.</span></span>

<span data-ttu-id="3a254-105">Une fenêtre reçoit ce message par le biais de sa fonction [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="3a254-105">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_STYLECHANGED                 0x007D
```



## <a name="parameters"></a><span data-ttu-id="3a254-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3a254-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3a254-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="3a254-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3a254-108">Indique si les styles de la fenêtre ou les styles de fenêtre étendus ont changé.</span><span class="sxs-lookup"><span data-stu-id="3a254-108">Indicates whether the window's styles or extended window styles have changed.</span></span> <span data-ttu-id="3a254-109">Ce paramètre peut être une ou plusieurs des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="3a254-109">This parameter can be one or more of the following values.</span></span>



| <span data-ttu-id="3a254-110">Valeur</span><span class="sxs-lookup"><span data-stu-id="3a254-110">Value</span></span>                                                                                                                                                                                                            | <span data-ttu-id="3a254-111">Signification</span><span class="sxs-lookup"><span data-stu-id="3a254-111">Meaning</span></span>                                             |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <span id="GWL_EXSTYLE"></span><span id="gwl_exstyle"></span><dl> <span data-ttu-id="3a254-112"><dt>**GWL \_ ExStyle**</dt> <dt>-20</dt></span><span class="sxs-lookup"><span data-stu-id="3a254-112"><dt>**GWL\_EXSTYLE**</dt> <dt>-20</dt></span></span> </dl> | <span data-ttu-id="3a254-113">Les styles de fenêtre étendus ont changé.</span><span class="sxs-lookup"><span data-stu-id="3a254-113">The extended window styles have changed.</span></span><br/> |
| <span id="GWL_STYLE"></span><span id="gwl_style"></span><dl> <span data-ttu-id="3a254-114"><dt>**GWL \_ STYLE**</dt> <dt>-16</dt></span><span class="sxs-lookup"><span data-stu-id="3a254-114"><dt>**GWL\_STYLE**</dt> <dt>-16</dt></span></span> </dl>       | <span data-ttu-id="3a254-115">Les styles de fenêtre ont été modifiés.</span><span class="sxs-lookup"><span data-stu-id="3a254-115">The window styles have changed.</span></span><br/>          |



 

</dd> <dt>

<span data-ttu-id="3a254-116">*lParam*</span><span class="sxs-lookup"><span data-stu-id="3a254-116">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3a254-117">Pointeur vers une structure [**STYLESTRUCT**](/windows/win32/api/winuser/ns-winuser-stylestruct) qui contient les nouveaux styles pour la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="3a254-117">A pointer to a [**STYLESTRUCT**](/windows/win32/api/winuser/ns-winuser-stylestruct) structure that contains the new styles for the window.</span></span> <span data-ttu-id="3a254-118">Une application peut examiner les styles, mais ne peut pas les modifier.</span><span class="sxs-lookup"><span data-stu-id="3a254-118">An application can examine the styles, but cannot change them.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3a254-119">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="3a254-119">Return value</span></span>

<span data-ttu-id="3a254-120">Type : **LRESULT**</span><span class="sxs-lookup"><span data-stu-id="3a254-120">Type: **LRESULT**</span></span>

<span data-ttu-id="3a254-121">Une application doit retourner zéro si elle traite ce message.</span><span class="sxs-lookup"><span data-stu-id="3a254-121">An application should return zero if it processes this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="3a254-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3a254-122">Requirements</span></span>



| <span data-ttu-id="3a254-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3a254-123">Requirement</span></span> | <span data-ttu-id="3a254-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="3a254-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3a254-125">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3a254-125">Minimum supported client</span></span><br/> | <span data-ttu-id="3a254-126">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3a254-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="3a254-127">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3a254-127">Minimum supported server</span></span><br/> | <span data-ttu-id="3a254-128">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3a254-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="3a254-129">En-tête</span><span class="sxs-lookup"><span data-stu-id="3a254-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="3a254-130"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3a254-130"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3a254-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3a254-131">See also</span></span>

<dl> <dt>

<span data-ttu-id="3a254-132">**Référence**</span><span class="sxs-lookup"><span data-stu-id="3a254-132">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="3a254-133">**SetWindowLong**</span><span class="sxs-lookup"><span data-stu-id="3a254-133">**SetWindowLong**</span></span>](/windows/win32/api/winuser/nf-winuser-setwindowlonga)
</dt> <dt>

[<span data-ttu-id="3a254-134">**STYLESTRUCT**</span><span class="sxs-lookup"><span data-stu-id="3a254-134">**STYLESTRUCT**</span></span>](/windows/win32/api/winuser/ns-winuser-stylestruct)
</dt> <dt>

[<span data-ttu-id="3a254-135">**\_STYLECHANGING WM**</span><span class="sxs-lookup"><span data-stu-id="3a254-135">**WM\_STYLECHANGING**</span></span>](wm-stylechanging.md)
</dt> <dt>

<span data-ttu-id="3a254-136">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="3a254-136">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="3a254-137">Windows</span><span class="sxs-lookup"><span data-stu-id="3a254-137">Windows</span></span>](windows.md)
</dt> </dl>

 

 
