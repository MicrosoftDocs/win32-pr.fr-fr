---
description: Une application envoie le \_ message WM MDIICONARRANGE à une fenêtre cliente d’interface multidocument (MDI) pour réorganiser toutes les fenêtres enfants MDI réduites. Elle n’affecte pas les fenêtres enfants qui ne sont pas réduites.
ms.assetid: 935b9e29-224d-449e-b89f-b6062bed7702
title: Message WM_MDIICONARRANGE (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc2d50d4bccebe3e9758752cc7d0d259e973875c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484753"
---
# <a name="wm_mdiiconarrange-message"></a><span data-ttu-id="ebe47-104">\_Message WM MDIICONARRANGE</span><span class="sxs-lookup"><span data-stu-id="ebe47-104">WM\_MDIICONARRANGE message</span></span>

<span data-ttu-id="ebe47-105">Une application envoie le message **WM \_ MDIICONARRANGE** à une fenêtre cliente d’interface multidocument (MDI) pour réorganiser toutes les fenêtres enfants MDI réduites.</span><span class="sxs-lookup"><span data-stu-id="ebe47-105">An application sends the **WM\_MDIICONARRANGE** message to a multiple-document interface (MDI) client window to arrange all minimized MDI child windows.</span></span> <span data-ttu-id="ebe47-106">Elle n’affecte pas les fenêtres enfants qui ne sont pas réduites.</span><span class="sxs-lookup"><span data-stu-id="ebe47-106">It does not affect child windows that are not minimized.</span></span>


```C++
#define WM_MDIICONARRANGE               0x0228
```



## <a name="parameters"></a><span data-ttu-id="ebe47-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ebe47-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ebe47-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="ebe47-108">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ebe47-109">Ce paramètre n’est pas utilisé ; elle doit être égale à zéro.</span><span class="sxs-lookup"><span data-stu-id="ebe47-109">This parameter is not used; it must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="ebe47-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ebe47-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ebe47-111">Ce paramètre n’est pas utilisé ; elle doit être égale à zéro.</span><span class="sxs-lookup"><span data-stu-id="ebe47-111">This parameter is not used; it must be zero.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ebe47-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ebe47-112">Requirements</span></span>



| <span data-ttu-id="ebe47-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ebe47-113">Requirement</span></span> | <span data-ttu-id="ebe47-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="ebe47-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ebe47-115">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ebe47-115">Minimum supported client</span></span><br/> | <span data-ttu-id="ebe47-116">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ebe47-116">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="ebe47-117">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ebe47-117">Minimum supported server</span></span><br/> | <span data-ttu-id="ebe47-118">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ebe47-118">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="ebe47-119">En-tête</span><span class="sxs-lookup"><span data-stu-id="ebe47-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="ebe47-120"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ebe47-120"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ebe47-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ebe47-121">See also</span></span>

<dl> <dt>

<span data-ttu-id="ebe47-122">**Référence**</span><span class="sxs-lookup"><span data-stu-id="ebe47-122">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="ebe47-123">**\_MDICASCADE WM**</span><span class="sxs-lookup"><span data-stu-id="ebe47-123">**WM\_MDICASCADE**</span></span>](wm-mdicascade.md)
</dt> <dt>

[<span data-ttu-id="ebe47-124">**\_MDITILE WM**</span><span class="sxs-lookup"><span data-stu-id="ebe47-124">**WM\_MDITILE**</span></span>](wm-mditile.md)
</dt> <dt>

<span data-ttu-id="ebe47-125">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="ebe47-125">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="ebe47-126">Interface multidocument</span><span class="sxs-lookup"><span data-stu-id="ebe47-126">Multiple Document Interface</span></span>](multiple-document-interface.md)
</dt> </dl>

 

 




