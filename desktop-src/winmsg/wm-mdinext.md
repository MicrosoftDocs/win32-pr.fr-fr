---
description: Une application envoie le \_ message WM MDINEXT à une fenêtre cliente d’interface multidocument (MDI) pour activer la fenêtre enfant suivante ou précédente.
ms.assetid: a4822b99-330a-4094-bad9-b9a5923e02a8
title: Message WM_MDINEXT (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 20e0af031c11ea37129e1405e31b07b18f023b7d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103751205"
---
# <a name="wm_mdinext-message"></a><span data-ttu-id="f8b6e-103">\_Message WM MDINEXT</span><span class="sxs-lookup"><span data-stu-id="f8b6e-103">WM\_MDINEXT message</span></span>

<span data-ttu-id="f8b6e-104">Une application envoie le message **WM \_ MDINEXT** à une fenêtre cliente d’interface multidocument (MDI) pour activer la fenêtre enfant suivante ou précédente.</span><span class="sxs-lookup"><span data-stu-id="f8b6e-104">An application sends the **WM\_MDINEXT** message to a multiple-document interface (MDI) client window to activate the next or previous child window.</span></span>


```C++
#define WM_MDINEXT                      0x0224
```



## <a name="parameters"></a><span data-ttu-id="f8b6e-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f8b6e-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f8b6e-106">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f8b6e-106">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f8b6e-107">Handle de la fenêtre enfant MDI.</span><span class="sxs-lookup"><span data-stu-id="f8b6e-107">A handle to the MDI child window.</span></span> <span data-ttu-id="f8b6e-108">Le système active la fenêtre enfant qui est immédiatement avant ou après la fenêtre enfant spécifiée, selon la valeur du paramètre *lParam* .</span><span class="sxs-lookup"><span data-stu-id="f8b6e-108">The system activates the child window that is immediately before or after the specified child window, depending on the value of the *lParam* parameter.</span></span> <span data-ttu-id="f8b6e-109">Si le paramètre *wParam* est **null**, le système active la fenêtre enfant qui est immédiatement avant ou après la fenêtre enfant actuellement active.</span><span class="sxs-lookup"><span data-stu-id="f8b6e-109">If the *wParam* parameter is **NULL**, the system activates the child window that is immediately before or after the currently active child window.</span></span>

</dd> <dt>

<span data-ttu-id="f8b6e-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f8b6e-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f8b6e-111">Si ce paramètre est égal à zéro, le système active la fenêtre enfant MDI suivante et place la fenêtre enfant identifiée par le paramètre *wParam* derrière toutes les autres fenêtres enfants.</span><span class="sxs-lookup"><span data-stu-id="f8b6e-111">If this parameter is zero, the system activates the next MDI child window and places the child window identified by the *wParam* parameter behind all other child windows.</span></span> <span data-ttu-id="f8b6e-112">Si ce paramètre est différent de zéro, le système active la fenêtre enfant précédente, en la plaçant devant la fenêtre enfant identifiée par *wParam*.</span><span class="sxs-lookup"><span data-stu-id="f8b6e-112">If this parameter is nonzero, the system activates the previous child window, placing it in front of the child window identified by *wParam*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f8b6e-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="f8b6e-113">Return value</span></span>

<span data-ttu-id="f8b6e-114">Type : **zéro**</span><span class="sxs-lookup"><span data-stu-id="f8b6e-114">Type: **zero**</span></span>

<span data-ttu-id="f8b6e-115">La valeur de retour est toujours zéro.</span><span class="sxs-lookup"><span data-stu-id="f8b6e-115">The return value is always zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="f8b6e-116">Notes</span><span class="sxs-lookup"><span data-stu-id="f8b6e-116">Remarks</span></span>

<span data-ttu-id="f8b6e-117">Si une fenêtre cliente MDI reçoit un message qui modifie l’activation de ses fenêtres enfants alors que la fenêtre enfant MDI active est agrandie, le système restaure la fenêtre enfant active et agrandit la fenêtre enfant qui vient d’être activée.</span><span class="sxs-lookup"><span data-stu-id="f8b6e-117">If an MDI client window receives any message that changes the activation of its child windows while the active MDI child window is maximized, the system restores the active child window and maximizes the newly activated child window.</span></span>

## <a name="requirements"></a><span data-ttu-id="f8b6e-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f8b6e-118">Requirements</span></span>



| <span data-ttu-id="f8b6e-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f8b6e-119">Requirement</span></span> | <span data-ttu-id="f8b6e-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="f8b6e-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f8b6e-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f8b6e-121">Minimum supported client</span></span><br/> | <span data-ttu-id="f8b6e-122">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f8b6e-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="f8b6e-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f8b6e-123">Minimum supported server</span></span><br/> | <span data-ttu-id="f8b6e-124">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f8b6e-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="f8b6e-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="f8b6e-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="f8b6e-126"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f8b6e-126"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f8b6e-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f8b6e-127">See also</span></span>

<dl> <dt>

<span data-ttu-id="f8b6e-128">**Référence**</span><span class="sxs-lookup"><span data-stu-id="f8b6e-128">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="f8b6e-129">**\_MDIACTIVATE WM**</span><span class="sxs-lookup"><span data-stu-id="f8b6e-129">**WM\_MDIACTIVATE**</span></span>](wm-mdiactivate.md)
</dt> <dt>

[<span data-ttu-id="f8b6e-130">**\_MDIGETACTIVE WM**</span><span class="sxs-lookup"><span data-stu-id="f8b6e-130">**WM\_MDIGETACTIVE**</span></span>](wm-mdigetactive.md)
</dt> <dt>

<span data-ttu-id="f8b6e-131">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="f8b6e-131">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="f8b6e-132">Interface multidocument</span><span class="sxs-lookup"><span data-stu-id="f8b6e-132">Multiple Document Interface</span></span>](multiple-document-interface.md)
</dt> </dl>

 

 




