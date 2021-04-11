---
description: Une application envoie le \_ message WM MDITILE à une fenêtre cliente d’interface multidocument (MDI) pour réorganiser toutes ses fenêtres enfants MDI dans un format de vignette.
ms.assetid: a480ba61-807e-4d0e-bda2-f1876e0bb13c
title: Message WM_MDITILE (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0cf7ee38fbb3622e2d17bf4cea5a28b6b492a244
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104201382"
---
# <a name="wm_mditile-message"></a><span data-ttu-id="38521-103">\_Message WM MDITILE</span><span class="sxs-lookup"><span data-stu-id="38521-103">WM\_MDITILE message</span></span>

<span data-ttu-id="38521-104">Une application envoie le message **WM \_ MDITILE** à une fenêtre cliente d’interface multidocument (MDI) pour réorganiser toutes ses fenêtres enfants MDI dans un format de vignette.</span><span class="sxs-lookup"><span data-stu-id="38521-104">An application sends the **WM\_MDITILE** message to a multiple-document interface (MDI) client window to arrange all of its MDI child windows in a tile format.</span></span>


```C++
#define WM_MDITILE                      0x0226
```



## <a name="parameters"></a><span data-ttu-id="38521-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="38521-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="38521-106">*wParam*</span><span class="sxs-lookup"><span data-stu-id="38521-106">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="38521-107">Option de mosaïque.</span><span class="sxs-lookup"><span data-stu-id="38521-107">The tiling option.</span></span> <span data-ttu-id="38521-108">Ce paramètre peut avoir l’une des valeurs suivantes, éventuellement combinées avec **MDITILE \_ SKIPDISABLED** pour empêcher les fenêtres enfants MDI désactivées d’être présentées en mosaïque.</span><span class="sxs-lookup"><span data-stu-id="38521-108">This parameter can be one of the following values, optionally combined with **MDITILE\_SKIPDISABLED** to prevent disabled MDI child windows from being tiled.</span></span>



| <span data-ttu-id="38521-109">Valeur</span><span class="sxs-lookup"><span data-stu-id="38521-109">Value</span></span>                                                                                                                                                                                                                                    | <span data-ttu-id="38521-110">Signification</span><span class="sxs-lookup"><span data-stu-id="38521-110">Meaning</span></span>                                |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------|
| <span id="MDITILE_HORIZONTAL"></span><span id="mditile_horizontal"></span><dl> <span data-ttu-id="38521-111"><dt>**MDITILE \_**</dt> <dt>0x0001</dt> horizontal</span><span class="sxs-lookup"><span data-stu-id="38521-111"><dt>**MDITILE\_HORIZONTAL**</dt> <dt>0x0001</dt></span></span> </dl> | <span data-ttu-id="38521-112">Mosaïques horizontalement les fenêtres.</span><span class="sxs-lookup"><span data-stu-id="38521-112">Tiles windows horizontally.</span></span><br/> |
| <span id="MDITILE_VERTICAL"></span><span id="mditile_vertical"></span><dl> <span data-ttu-id="38521-113"><dt>**MDITILE \_ VERTICAL**</dt> <dt>0x0000</dt></span><span class="sxs-lookup"><span data-stu-id="38521-113"><dt>**MDITILE\_VERTICAL**</dt> <dt>0x0000</dt></span></span> </dl>       | <span data-ttu-id="38521-114">Mosaïque verticalement les fenêtres.</span><span class="sxs-lookup"><span data-stu-id="38521-114">Tiles windows vertically.</span></span><br/>   |



 

</dd> <dt>

<span data-ttu-id="38521-115">*lParam*</span><span class="sxs-lookup"><span data-stu-id="38521-115">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="38521-116">Ce paramètre n'est pas utilisé.</span><span class="sxs-lookup"><span data-stu-id="38521-116">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="38521-117">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="38521-117">Return value</span></span>

<span data-ttu-id="38521-118">Type : **bool**</span><span class="sxs-lookup"><span data-stu-id="38521-118">Type: **BOOL**</span></span>

<span data-ttu-id="38521-119">Si le message est correctement exécuté, la valeur de retour est **true**.</span><span class="sxs-lookup"><span data-stu-id="38521-119">If the message succeeds, the return value is **TRUE**.</span></span>

<span data-ttu-id="38521-120">Si le message échoue, la valeur de retour est **false**.</span><span class="sxs-lookup"><span data-stu-id="38521-120">If the message fails, the return value is **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="38521-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="38521-121">Requirements</span></span>



| <span data-ttu-id="38521-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="38521-122">Requirement</span></span> | <span data-ttu-id="38521-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="38521-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="38521-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="38521-124">Minimum supported client</span></span><br/> | <span data-ttu-id="38521-125">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="38521-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="38521-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="38521-126">Minimum supported server</span></span><br/> | <span data-ttu-id="38521-127">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="38521-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="38521-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="38521-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="38521-129"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="38521-129"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="38521-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="38521-130">See also</span></span>

<dl> <dt>

<span data-ttu-id="38521-131">**Référence**</span><span class="sxs-lookup"><span data-stu-id="38521-131">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="38521-132">**\_MDICASCADE WM**</span><span class="sxs-lookup"><span data-stu-id="38521-132">**WM\_MDICASCADE**</span></span>](wm-mdicascade.md)
</dt> <dt>

[<span data-ttu-id="38521-133">**\_MDIICONARRANGE WM**</span><span class="sxs-lookup"><span data-stu-id="38521-133">**WM\_MDIICONARRANGE**</span></span>](wm-mdiiconarrange.md)
</dt> <dt>

<span data-ttu-id="38521-134">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="38521-134">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="38521-135">Interface multidocument</span><span class="sxs-lookup"><span data-stu-id="38521-135">Multiple Document Interface</span></span>](multiple-document-interface.md)
</dt> </dl>

 

 




