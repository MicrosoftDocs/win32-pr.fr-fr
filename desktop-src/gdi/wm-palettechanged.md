---
description: Le \_ message WM PALETTECHANGED est envoyé à toutes les fenêtres de niveau supérieur et Overlapped une fois que la fenêtre avec le focus clavier a réalisé sa palette logique, ce qui modifie la palette du système.
ms.assetid: 2eed568b-1a16-47d2-ae26-3f1dec35e893
title: Message WM_PALETTECHANGED (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c5a02bffe5206c7550cce2ec62203f3dbea2d246
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103755821"
---
# <a name="wm_palettechanged-message"></a><span data-ttu-id="9b4bd-103">\_Message WM PALETTECHANGED</span><span class="sxs-lookup"><span data-stu-id="9b4bd-103">WM\_PALETTECHANGED message</span></span>

<span data-ttu-id="9b4bd-104">Le message **WM \_ PALETTECHANGED** est envoyé à toutes les fenêtres de niveau supérieur et Overlapped une fois que la fenêtre avec le focus clavier a réalisé sa palette logique, ce qui modifie la palette du système.</span><span class="sxs-lookup"><span data-stu-id="9b4bd-104">The **WM\_PALETTECHANGED** message is sent to all top-level and overlapped windows after the window with the keyboard focus has realized its logical palette, thereby changing the system palette.</span></span> <span data-ttu-id="9b4bd-105">Ce message active une fenêtre qui utilise une palette de couleurs, mais n’a pas le focus clavier pour réaliser sa palette logique et mettre à jour sa zone cliente.</span><span class="sxs-lookup"><span data-stu-id="9b4bd-105">This message enables a window that uses a color palette but does not have the keyboard focus to realize its logical palette and update its client area.</span></span>

<span data-ttu-id="9b4bd-106">Une fenêtre reçoit ce message par le biais de sa fonction [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="9b4bd-106">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
LRESULT CALLBACK WindowProc(
  HWND hwnd, 
  UINT  uMsg, 
  WPARAM wParam, 
  LPARAM lParam    
);
```



## <a name="parameters"></a><span data-ttu-id="9b4bd-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9b4bd-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9b4bd-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="9b4bd-108">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9b4bd-109">Handle de la fenêtre qui a provoqué la modification de la palette système.</span><span class="sxs-lookup"><span data-stu-id="9b4bd-109">A handle to the window that caused the system palette to change.</span></span>

</dd> <dt>

<span data-ttu-id="9b4bd-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="9b4bd-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9b4bd-111">Ce paramètre n'est pas utilisé.</span><span class="sxs-lookup"><span data-stu-id="9b4bd-111">This parameter is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9b4bd-112">Notes</span><span class="sxs-lookup"><span data-stu-id="9b4bd-112">Remarks</span></span>

<span data-ttu-id="9b4bd-113">Ce message doit être envoyé à toutes les fenêtres de niveau supérieur et avec chevauchement, y compris celui qui a modifié la palette du système.</span><span class="sxs-lookup"><span data-stu-id="9b4bd-113">This message must be sent to all top-level and overlapped windows, including the one that changed the system palette.</span></span> <span data-ttu-id="9b4bd-114">Si des fenêtres enfants utilisent une palette de couleurs, ce message doit également leur être transmis.</span><span class="sxs-lookup"><span data-stu-id="9b4bd-114">If any child windows use a color palette, this message must be passed on to them as well.</span></span>

<span data-ttu-id="9b4bd-115">Pour éviter de créer une boucle infinie, une fenêtre qui reçoit ce message ne doit pas réaliser sa palette, sauf si elle détermine que *wParam* ne contient pas son propre handle de fenêtre.</span><span class="sxs-lookup"><span data-stu-id="9b4bd-115">To avoid creating an infinite loop, a window that receives this message must not realize its palette, unless it determines that *wParam* does not contain its own window handle.</span></span>

## <a name="requirements"></a><span data-ttu-id="9b4bd-116">Spécifications</span><span class="sxs-lookup"><span data-stu-id="9b4bd-116">Requirements</span></span>



| <span data-ttu-id="9b4bd-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9b4bd-117">Requirement</span></span> | <span data-ttu-id="9b4bd-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="9b4bd-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9b4bd-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9b4bd-119">Minimum supported client</span></span><br/> | <span data-ttu-id="9b4bd-120">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9b4bd-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="9b4bd-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9b4bd-121">Minimum supported server</span></span><br/> | <span data-ttu-id="9b4bd-122">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9b4bd-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="9b4bd-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="9b4bd-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="9b4bd-124"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="9b4bd-124"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9b4bd-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9b4bd-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9b4bd-126">Vue d’ensemble des couleurs</span><span class="sxs-lookup"><span data-stu-id="9b4bd-126">Colors Overview</span></span>](colors.md)
</dt> <dt>

[<span data-ttu-id="9b4bd-127">Messages de couleur</span><span class="sxs-lookup"><span data-stu-id="9b4bd-127">Color Messages</span></span>](color-messages.md)
</dt> <dt>

[<span data-ttu-id="9b4bd-128">**\_PALETTEISCHANGING WM**</span><span class="sxs-lookup"><span data-stu-id="9b4bd-128">**WM\_PALETTEISCHANGING**</span></span>](wm-paletteischanging.md)
</dt> <dt>

[<span data-ttu-id="9b4bd-129">**\_QUERYNEWPALETTE WM**</span><span class="sxs-lookup"><span data-stu-id="9b4bd-129">**WM\_QUERYNEWPALETTE**</span></span>](wm-querynewpalette.md)
</dt> </dl>

 

 
