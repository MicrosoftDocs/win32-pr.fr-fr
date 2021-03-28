---
description: Le \_ message WM QUERYNEWPALETTE informe une fenêtre qu’il est sur le point de recevoir le focus clavier, ce qui donne à la fenêtre la possibilité de réaliser sa palette logique lorsqu’il reçoit le focus.
ms.assetid: bc9f76ca-62af-4f0b-8791-49269a1b23d1
title: Message WM_QUERYNEWPALETTE (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3ca664bbb6fb30a0508f9429dd62af489c092db7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104973050"
---
# <a name="wm_querynewpalette-message"></a><span data-ttu-id="cd7fb-103">\_Message WM QUERYNEWPALETTE</span><span class="sxs-lookup"><span data-stu-id="cd7fb-103">WM\_QUERYNEWPALETTE message</span></span>

<span data-ttu-id="cd7fb-104">Le message **WM \_ QUERYNEWPALETTE** informe une fenêtre qu’il est sur le point de recevoir le focus clavier, ce qui donne à la fenêtre la possibilité de réaliser sa palette logique lorsqu’il reçoit le focus.</span><span class="sxs-lookup"><span data-stu-id="cd7fb-104">The **WM\_QUERYNEWPALETTE** message informs a window that it is about to receive the keyboard focus, giving the window the opportunity to realize its logical palette when it receives the focus.</span></span>

<span data-ttu-id="cd7fb-105">Une fenêtre reçoit ce message par le biais de sa fonction [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="cd7fb-105">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
LRESULT CALLBACK WindowProc(
  HWND hwnd, 
  UINT  uMsg, 
  WPARAM wParam, 
  LPARAM lParam     
);
```



## <a name="parameters"></a><span data-ttu-id="cd7fb-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="cd7fb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cd7fb-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="cd7fb-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="cd7fb-108">Ce paramètre n'est pas utilisé.</span><span class="sxs-lookup"><span data-stu-id="cd7fb-108">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="cd7fb-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="cd7fb-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="cd7fb-110">Ce paramètre n'est pas utilisé.</span><span class="sxs-lookup"><span data-stu-id="cd7fb-110">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cd7fb-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="cd7fb-111">Return value</span></span>

<span data-ttu-id="cd7fb-112">Si la fenêtre réalise sa palette logique, elle doit retourner la **valeur true**; Sinon, elle doit retourner **false**.</span><span class="sxs-lookup"><span data-stu-id="cd7fb-112">If the window realizes its logical palette, it must return **TRUE**; otherwise, it must return **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="cd7fb-113">Spécifications</span><span class="sxs-lookup"><span data-stu-id="cd7fb-113">Requirements</span></span>



| <span data-ttu-id="cd7fb-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="cd7fb-114">Requirement</span></span> | <span data-ttu-id="cd7fb-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="cd7fb-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cd7fb-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cd7fb-116">Minimum supported client</span></span><br/> | <span data-ttu-id="cd7fb-117">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="cd7fb-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="cd7fb-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cd7fb-118">Minimum supported server</span></span><br/> | <span data-ttu-id="cd7fb-119">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="cd7fb-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="cd7fb-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="cd7fb-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="cd7fb-121"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="cd7fb-121"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cd7fb-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cd7fb-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cd7fb-123">Vue d’ensemble des couleurs</span><span class="sxs-lookup"><span data-stu-id="cd7fb-123">Colors Overview</span></span>](colors.md)
</dt> <dt>

[<span data-ttu-id="cd7fb-124">Messages de couleur</span><span class="sxs-lookup"><span data-stu-id="cd7fb-124">Color Messages</span></span>](color-messages.md)
</dt> <dt>

[<span data-ttu-id="cd7fb-125">**\_PALETTECHANGED WM**</span><span class="sxs-lookup"><span data-stu-id="cd7fb-125">**WM\_PALETTECHANGED**</span></span>](wm-palettechanged.md)
</dt> <dt>

[<span data-ttu-id="cd7fb-126">**\_PALETTEISCHANGING WM**</span><span class="sxs-lookup"><span data-stu-id="cd7fb-126">**WM\_PALETTEISCHANGING**</span></span>](wm-paletteischanging.md)
</dt> </dl>

 

 
