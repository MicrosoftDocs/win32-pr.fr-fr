---
description: Envoyé à une fenêtre lorsque la fonction SetWindowLong est sur le paragraphe de la modification d’un ou plusieurs styles de la fenêtre.
ms.assetid: 71034362-3f67-49ae-bbbf-d38853ababb3
title: Message WM_STYLECHANGING (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 62e587797404bb361a443a60750d4de5ea6a8924
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103865234"
---
# <a name="wm_stylechanging-message"></a><span data-ttu-id="b9db7-103">\_Message WM STYLECHANGING</span><span class="sxs-lookup"><span data-stu-id="b9db7-103">WM\_STYLECHANGING message</span></span>

<span data-ttu-id="b9db7-104">Envoyé à une fenêtre lorsque la fonction [**SetWindowLong**](/windows/win32/api/winuser/nf-winuser-setwindowlonga) est sur le paragraphe de la modification d’un ou plusieurs styles de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="b9db7-104">Sent to a window when the [**SetWindowLong**](/windows/win32/api/winuser/nf-winuser-setwindowlonga) function is about to change one or more of the window's styles.</span></span>

<span data-ttu-id="b9db7-105">Une fenêtre reçoit ce message par le biais de sa fonction [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="b9db7-105">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_STYLECHANGING                0x007C
```



## <a name="parameters"></a><span data-ttu-id="b9db7-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b9db7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b9db7-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b9db7-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b9db7-108">Indique si les styles de la fenêtre ou les styles de fenêtre étendus sont modifiés.</span><span class="sxs-lookup"><span data-stu-id="b9db7-108">Indicates whether the window's styles or extended window styles are changing.</span></span> <span data-ttu-id="b9db7-109">Ce paramètre peut être une ou plusieurs des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="b9db7-109">This parameter can be one or more of the following values.</span></span>



| <span data-ttu-id="b9db7-110">Valeur</span><span class="sxs-lookup"><span data-stu-id="b9db7-110">Value</span></span>                                                                                                                                                                                                            | <span data-ttu-id="b9db7-111">Signification</span><span class="sxs-lookup"><span data-stu-id="b9db7-111">Meaning</span></span>                                             |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <span id="GWL_EXSTYLE"></span><span id="gwl_exstyle"></span><dl> <span data-ttu-id="b9db7-112"><dt>**GWL \_ ExStyle**</dt> <dt>-20</dt></span><span class="sxs-lookup"><span data-stu-id="b9db7-112"><dt>**GWL\_EXSTYLE**</dt> <dt>-20</dt></span></span> </dl> | <span data-ttu-id="b9db7-113">Les styles de fenêtre étendus sont modifiés.</span><span class="sxs-lookup"><span data-stu-id="b9db7-113">The extended window styles are changing.</span></span><br/> |
| <span id="GWL_STYLE"></span><span id="gwl_style"></span><dl> <span data-ttu-id="b9db7-114"><dt>**GWL \_ STYLE**</dt> <dt>-16</dt></span><span class="sxs-lookup"><span data-stu-id="b9db7-114"><dt>**GWL\_STYLE**</dt> <dt>-16</dt></span></span> </dl>       | <span data-ttu-id="b9db7-115">Les styles de fenêtre changent.</span><span class="sxs-lookup"><span data-stu-id="b9db7-115">The window styles are changing.</span></span><br/>          |



 

</dd> <dt>

<span data-ttu-id="b9db7-116">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b9db7-116">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b9db7-117">Pointeur vers une structure [**STYLESTRUCT**](/windows/win32/api/winuser/ns-winuser-stylestruct) qui contient les nouveaux styles proposés pour la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="b9db7-117">A pointer to a [**STYLESTRUCT**](/windows/win32/api/winuser/ns-winuser-stylestruct) structure that contains the proposed new styles for the window.</span></span> <span data-ttu-id="b9db7-118">Une application peut examiner les styles et, si nécessaire, les modifier.</span><span class="sxs-lookup"><span data-stu-id="b9db7-118">An application can examine the styles and, if necessary, change them.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b9db7-119">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="b9db7-119">Return value</span></span>

<span data-ttu-id="b9db7-120">Type : **LRESULT**</span><span class="sxs-lookup"><span data-stu-id="b9db7-120">Type: **LRESULT**</span></span>

<span data-ttu-id="b9db7-121">Une application doit retourner zéro si elle traite ce message.</span><span class="sxs-lookup"><span data-stu-id="b9db7-121">An application should return zero if it processes this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="b9db7-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b9db7-122">Requirements</span></span>



| <span data-ttu-id="b9db7-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b9db7-123">Requirement</span></span> | <span data-ttu-id="b9db7-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="b9db7-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b9db7-125">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b9db7-125">Minimum supported client</span></span><br/> | <span data-ttu-id="b9db7-126">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b9db7-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="b9db7-127">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b9db7-127">Minimum supported server</span></span><br/> | <span data-ttu-id="b9db7-128">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b9db7-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="b9db7-129">En-tête</span><span class="sxs-lookup"><span data-stu-id="b9db7-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="b9db7-130"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b9db7-130"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b9db7-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b9db7-131">See also</span></span>

<dl> <dt>

<span data-ttu-id="b9db7-132">**Référence**</span><span class="sxs-lookup"><span data-stu-id="b9db7-132">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="b9db7-133">**STYLESTRUCT**</span><span class="sxs-lookup"><span data-stu-id="b9db7-133">**STYLESTRUCT**</span></span>](/windows/win32/api/winuser/ns-winuser-stylestruct)
</dt> <dt>

[<span data-ttu-id="b9db7-134">**\_STYLECHANGED WM**</span><span class="sxs-lookup"><span data-stu-id="b9db7-134">**WM\_STYLECHANGED**</span></span>](wm-stylechanged.md)
</dt> <dt>

<span data-ttu-id="b9db7-135">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="b9db7-135">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="b9db7-136">Windows</span><span class="sxs-lookup"><span data-stu-id="b9db7-136">Windows</span></span>](windows.md)
</dt> </dl>

 

 
