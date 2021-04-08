---
description: Envoyé à une fenêtre lorsque la taille ou la position de la fenêtre est sur le point de changer. Une application peut utiliser ce message pour remplacer la taille et la position agrandies par défaut de la fenêtre, ou sa taille de suivi minimale ou maximale par défaut.
ms.assetid: af2295e0-2d0b-4ac0-b689-16138022f4b7
title: Message WM_GETMINMAXINFO (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a29cbca97d38f7fca90c93ef7bf0606ea49306da
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866758"
---
# <a name="wm_getminmaxinfo-message"></a><span data-ttu-id="a3ad5-104">\_Message WM GETMINMAXINFO</span><span class="sxs-lookup"><span data-stu-id="a3ad5-104">WM\_GETMINMAXINFO message</span></span>

<span data-ttu-id="a3ad5-105">Envoyé à une fenêtre lorsque la taille ou la position de la fenêtre est sur le point de changer.</span><span class="sxs-lookup"><span data-stu-id="a3ad5-105">Sent to a window when the size or position of the window is about to change.</span></span> <span data-ttu-id="a3ad5-106">Une application peut utiliser ce message pour remplacer la taille et la position agrandies par défaut de la fenêtre, ou sa taille de suivi minimale ou maximale par défaut.</span><span class="sxs-lookup"><span data-stu-id="a3ad5-106">An application can use this message to override the window's default maximized size and position, or its default minimum or maximum tracking size.</span></span>

<span data-ttu-id="a3ad5-107">Une fenêtre reçoit ce message par le biais de sa fonction [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="a3ad5-107">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_GETMINMAXINFO                0x0024
```



## <a name="parameters"></a><span data-ttu-id="a3ad5-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a3ad5-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a3ad5-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="a3ad5-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a3ad5-110">Ce paramètre n'est pas utilisé.</span><span class="sxs-lookup"><span data-stu-id="a3ad5-110">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="a3ad5-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a3ad5-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a3ad5-112">Pointeur vers une structure [**minmaxinfo,**](/windows/win32/api/winuser/ns-winuser-minmaxinfo) qui contient la position et les dimensions agrandies par défaut, ainsi que les tailles de suivi minimales et maximales par défaut.</span><span class="sxs-lookup"><span data-stu-id="a3ad5-112">A pointer to a [**MINMAXINFO**](/windows/win32/api/winuser/ns-winuser-minmaxinfo) structure that contains the default maximized position and dimensions, and the default minimum and maximum tracking sizes.</span></span> <span data-ttu-id="a3ad5-113">Une application peut remplacer les valeurs par défaut en définissant les membres de cette structure.</span><span class="sxs-lookup"><span data-stu-id="a3ad5-113">An application can override the defaults by setting the members of this structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a3ad5-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="a3ad5-114">Return value</span></span>

<span data-ttu-id="a3ad5-115">Type : **LRESULT**</span><span class="sxs-lookup"><span data-stu-id="a3ad5-115">Type: **LRESULT**</span></span>

<span data-ttu-id="a3ad5-116">Si une application traite ce message, elle doit retourner la valeur zéro.</span><span class="sxs-lookup"><span data-stu-id="a3ad5-116">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="a3ad5-117">Notes</span><span class="sxs-lookup"><span data-stu-id="a3ad5-117">Remarks</span></span>

<span data-ttu-id="a3ad5-118">La taille maximale de suivi est la plus grande taille de fenêtre qui peut être produite à l’aide des bordures pour dimensionner la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="a3ad5-118">The maximum tracking size is the largest window size that can be produced by using the borders to size the window.</span></span> <span data-ttu-id="a3ad5-119">La taille de suivi minimale est la plus petite taille de fenêtre qui peut être produite à l’aide des bordures pour dimensionner la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="a3ad5-119">The minimum tracking size is the smallest window size that can be produced by using the borders to size the window.</span></span>

## <a name="requirements"></a><span data-ttu-id="a3ad5-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a3ad5-120">Requirements</span></span>



| <span data-ttu-id="a3ad5-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a3ad5-121">Requirement</span></span> | <span data-ttu-id="a3ad5-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="a3ad5-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a3ad5-123">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a3ad5-123">Minimum supported client</span></span><br/> | <span data-ttu-id="a3ad5-124">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a3ad5-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="a3ad5-125">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a3ad5-125">Minimum supported server</span></span><br/> | <span data-ttu-id="a3ad5-126">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a3ad5-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="a3ad5-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="a3ad5-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="a3ad5-128"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a3ad5-128"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a3ad5-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a3ad5-129">See also</span></span>

<dl> <dt>

<span data-ttu-id="a3ad5-130">**Référence**</span><span class="sxs-lookup"><span data-stu-id="a3ad5-130">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="a3ad5-131">**MoveWindow**</span><span class="sxs-lookup"><span data-stu-id="a3ad5-131">**MoveWindow**</span></span>](/windows/win32/api/winuser/nf-winuser-movewindow)
</dt> <dt>

[<span data-ttu-id="a3ad5-132">**SetWindowPos**</span><span class="sxs-lookup"><span data-stu-id="a3ad5-132">**SetWindowPos**</span></span>](/windows/win32/api/winuser/nf-winuser-setwindowpos)
</dt> <dt>

[<span data-ttu-id="a3ad5-133">**MINMAXINFO,**</span><span class="sxs-lookup"><span data-stu-id="a3ad5-133">**MINMAXINFO**</span></span>](/windows/win32/api/winuser/ns-winuser-minmaxinfo)
</dt> <dt>

<span data-ttu-id="a3ad5-134">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="a3ad5-134">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="a3ad5-135">Windows</span><span class="sxs-lookup"><span data-stu-id="a3ad5-135">Windows</span></span>](windows.md)
</dt> </dl>

 

 
