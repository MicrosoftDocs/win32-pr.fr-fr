---
description: Une application envoie le \_ message WM MDIACTIVATE à une fenêtre cliente d’interface multidocument (MDI, multiple-document interface) pour indiquer à la fenêtre cliente d’activer une autre fenêtre enfant MDI.
ms.assetid: c5de18b5-fac3-4e55-9eca-3b6672df0e7b
title: Message WM_MDIACTIVATE (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b240c41d3b7127a5d69b855f3a5587e194b02d96
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106518488"
---
# <a name="wm_mdiactivate-message"></a><span data-ttu-id="f2d33-103">\_Message WM MDIACTIVATE</span><span class="sxs-lookup"><span data-stu-id="f2d33-103">WM\_MDIACTIVATE message</span></span>

<span data-ttu-id="f2d33-104">Une application envoie le message **WM \_ MDIACTIVATE** à une fenêtre cliente d’interface multidocument (MDI, multiple-document interface) pour indiquer à la fenêtre cliente d’activer une autre fenêtre enfant MDI.</span><span class="sxs-lookup"><span data-stu-id="f2d33-104">An application sends the **WM\_MDIACTIVATE** message to a multiple-document interface (MDI) client window to instruct the client window to activate a different MDI child window.</span></span>


```C++
#define WM_MDIACTIVATE                  0x0222
```



## <a name="parameters"></a><span data-ttu-id="f2d33-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f2d33-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f2d33-106">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f2d33-106">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f2d33-107">Handle de la fenêtre enfant MDI à activer.</span><span class="sxs-lookup"><span data-stu-id="f2d33-107">A handle to the MDI child window to be activated.</span></span>

</dd> <dt>

<span data-ttu-id="f2d33-108">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f2d33-108">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f2d33-109">Ce paramètre n'est pas utilisé.</span><span class="sxs-lookup"><span data-stu-id="f2d33-109">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f2d33-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="f2d33-110">Return value</span></span>

<span data-ttu-id="f2d33-111">Type : **LRESULT**</span><span class="sxs-lookup"><span data-stu-id="f2d33-111">Type: **LRESULT**</span></span>

<span data-ttu-id="f2d33-112">Si une application envoie ce message à une fenêtre cliente MDI, la valeur de retour est zéro.</span><span class="sxs-lookup"><span data-stu-id="f2d33-112">If an application sends this message to an MDI client window, the return value is zero.</span></span>

<span data-ttu-id="f2d33-113">Une fenêtre enfant MDI doit retourner zéro si elle traite ce message.</span><span class="sxs-lookup"><span data-stu-id="f2d33-113">An MDI child window should return zero if it processes this message.</span></span>

## <a name="remarks"></a><span data-ttu-id="f2d33-114">Notes</span><span class="sxs-lookup"><span data-stu-id="f2d33-114">Remarks</span></span>

<span data-ttu-id="f2d33-115">Lorsque la fenêtre cliente traite ce message, il envoie **WM \_ MDIACTIVATE** à la fenêtre enfant qui est désactivée et à la fenêtre enfant en cours d’activation.</span><span class="sxs-lookup"><span data-stu-id="f2d33-115">As the client window processes this message, it sends **WM\_MDIACTIVATE** to the child window being deactivated and to the child window being activated.</span></span> <span data-ttu-id="f2d33-116">Les paramètres de message reçus par une fenêtre enfant MDI sont les suivants :</span><span class="sxs-lookup"><span data-stu-id="f2d33-116">The message parameters received by an MDI child window are as follows:</span></span>

<dl> <dt>

<span data-ttu-id="f2d33-117"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span><span class="sxs-lookup"><span data-stu-id="f2d33-117"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span></span>
</dt> <dd>

<span data-ttu-id="f2d33-118">Handle de la fenêtre enfant MDI en cours de désactivation.</span><span class="sxs-lookup"><span data-stu-id="f2d33-118">A handle to the MDI child window being deactivated.</span></span>

</dd> <dt>

<span data-ttu-id="f2d33-119"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span><span class="sxs-lookup"><span data-stu-id="f2d33-119"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="f2d33-120">Handle de la fenêtre enfant MDI en cours d’activation.</span><span class="sxs-lookup"><span data-stu-id="f2d33-120">A handle to the MDI child window being activated.</span></span>

</dd> </dl>

<span data-ttu-id="f2d33-121">Une fenêtre enfant MDI est activée indépendamment de la fenêtre frame MDI.</span><span class="sxs-lookup"><span data-stu-id="f2d33-121">An MDI child window is activated independently of the MDI frame window.</span></span> <span data-ttu-id="f2d33-122">Lorsque la fenêtre frame devient active, la fenêtre enfant qui a été activée pour la dernière fois à l’aide du message **WM \_ MDIACTIVATE** reçoit le message [**WM \_ NCACTIVATE**](wm-ncactivate.md) pour dessiner un cadre de fenêtre et une barre de titre active ; la fenêtre enfant ne reçoit pas un autre message **WM \_ MDIACTIVATE** .</span><span class="sxs-lookup"><span data-stu-id="f2d33-122">When the frame window becomes active, the child window last activated by using the **WM\_MDIACTIVATE** message receives the [**WM\_NCACTIVATE**](wm-ncactivate.md) message to draw an active window frame and title bar; the child window does not receive another **WM\_MDIACTIVATE** message.</span></span>

## <a name="requirements"></a><span data-ttu-id="f2d33-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f2d33-123">Requirements</span></span>



| <span data-ttu-id="f2d33-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f2d33-124">Requirement</span></span> | <span data-ttu-id="f2d33-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="f2d33-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f2d33-126">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f2d33-126">Minimum supported client</span></span><br/> | <span data-ttu-id="f2d33-127">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f2d33-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="f2d33-128">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f2d33-128">Minimum supported server</span></span><br/> | <span data-ttu-id="f2d33-129">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f2d33-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="f2d33-130">En-tête</span><span class="sxs-lookup"><span data-stu-id="f2d33-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="f2d33-131"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f2d33-131"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f2d33-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f2d33-132">See also</span></span>

<dl> <dt>

<span data-ttu-id="f2d33-133">**Référence**</span><span class="sxs-lookup"><span data-stu-id="f2d33-133">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="f2d33-134">**\_MDIGETACTIVE WM**</span><span class="sxs-lookup"><span data-stu-id="f2d33-134">**WM\_MDIGETACTIVE**</span></span>](wm-mdigetactive.md)
</dt> <dt>

[<span data-ttu-id="f2d33-135">**\_MDINEXT WM**</span><span class="sxs-lookup"><span data-stu-id="f2d33-135">**WM\_MDINEXT**</span></span>](wm-mdinext.md)
</dt> <dt>

[<span data-ttu-id="f2d33-136">**\_NCACTIVATE WM**</span><span class="sxs-lookup"><span data-stu-id="f2d33-136">**WM\_NCACTIVATE**</span></span>](wm-ncactivate.md)
</dt> <dt>

<span data-ttu-id="f2d33-137">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="f2d33-137">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="f2d33-138">Interface multidocument</span><span class="sxs-lookup"><span data-stu-id="f2d33-138">Multiple Document Interface</span></span>](multiple-document-interface.md)
</dt> </dl>

 

 




