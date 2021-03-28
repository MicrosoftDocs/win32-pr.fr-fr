---
description: Le \_ message WM DISPLAYCHANGE est envoyé à toutes les fenêtres lorsque la résolution d’affichage a changé.
ms.assetid: 5a6111fd-648e-41a9-aaf8-e5d93f5d54cd
title: Message WM_DISPLAYCHANGE (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 682612529fd40b22481612bb26a954bec45e3901
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104202480"
---
# <a name="wm_displaychange-message"></a><span data-ttu-id="2c6ff-103">\_Message WM DISPLAYCHANGE</span><span class="sxs-lookup"><span data-stu-id="2c6ff-103">WM\_DISPLAYCHANGE message</span></span>

<span data-ttu-id="2c6ff-104">Le message **WM \_ DISPLAYCHANGE** est envoyé à toutes les fenêtres lorsque la résolution d’affichage a changé.</span><span class="sxs-lookup"><span data-stu-id="2c6ff-104">The **WM\_DISPLAYCHANGE** message is sent to all windows when the display resolution has changed.</span></span>

<span data-ttu-id="2c6ff-105">Une fenêtre reçoit ce message par le biais de sa fonction [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="2c6ff-105">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
LRESULT CALLBACK WindowProc(
  HWND hwnd, 
  UINT  uMsg, 
  WPARAM wParam, 
  LPARAM lParam   
);
```



## <a name="parameters"></a><span data-ttu-id="2c6ff-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2c6ff-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2c6ff-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="2c6ff-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2c6ff-108">Nouvelle profondeur d’image de l’affichage, en bits par pixel.</span><span class="sxs-lookup"><span data-stu-id="2c6ff-108">The new image depth of the display, in bits per pixel.</span></span>

</dd> <dt>

<span data-ttu-id="2c6ff-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="2c6ff-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2c6ff-110">Le mot de poids faible spécifie la résolution horizontale de l’écran.</span><span class="sxs-lookup"><span data-stu-id="2c6ff-110">The low-order word specifies the horizontal resolution of the screen.</span></span>

<span data-ttu-id="2c6ff-111">Le mot de poids fort spécifie la résolution verticale de l’écran.</span><span class="sxs-lookup"><span data-stu-id="2c6ff-111">The high-order word specifies the vertical resolution of the screen.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2c6ff-112">Notes</span><span class="sxs-lookup"><span data-stu-id="2c6ff-112">Remarks</span></span>

<span data-ttu-id="2c6ff-113">Ce message est envoyé uniquement aux fenêtres de niveau supérieur.</span><span class="sxs-lookup"><span data-stu-id="2c6ff-113">This message is only sent to top-level windows.</span></span> <span data-ttu-id="2c6ff-114">Pour toutes les autres fenêtres, il est publié.</span><span class="sxs-lookup"><span data-stu-id="2c6ff-114">For all other windows it is posted.</span></span>

## <a name="requirements"></a><span data-ttu-id="2c6ff-115">Spécifications</span><span class="sxs-lookup"><span data-stu-id="2c6ff-115">Requirements</span></span>



| <span data-ttu-id="2c6ff-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2c6ff-116">Requirement</span></span> | <span data-ttu-id="2c6ff-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="2c6ff-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2c6ff-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2c6ff-118">Minimum supported client</span></span><br/> | <span data-ttu-id="2c6ff-119">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2c6ff-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="2c6ff-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2c6ff-120">Minimum supported server</span></span><br/> | <span data-ttu-id="2c6ff-121">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2c6ff-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="2c6ff-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="2c6ff-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="2c6ff-123"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2c6ff-123"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2c6ff-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2c6ff-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2c6ff-125">Vue d’ensemble de la peinture et du dessin</span><span class="sxs-lookup"><span data-stu-id="2c6ff-125">Painting and Drawing Overview</span></span>](painting-and-drawing.md)
</dt> <dt>

[<span data-ttu-id="2c6ff-126">Peinture et dessin de messages</span><span class="sxs-lookup"><span data-stu-id="2c6ff-126">Painting and Drawing Messages</span></span>](painting-and-drawing-messages.md)
</dt> <dt>

<span data-ttu-id="2c6ff-127">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="2c6ff-127">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="2c6ff-128">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="2c6ff-128">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span></span>
</dt> </dl>

 

 
