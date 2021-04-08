---
description: Une application envoie le \_ message WM MDIDESTROY à une fenêtre cliente d’interface multidocument (MDI) pour fermer une fenêtre enfant MDI.
ms.assetid: b415393d-a5c2-4b70-af18-0dc7b3939a47
title: Message WM_MDIDESTROY (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: edea8fe8dadc691ca912df4e9ee5d57421124bcd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103751212"
---
# <a name="wm_mdidestroy-message"></a><span data-ttu-id="bd5d8-103">\_Message WM MDIDESTROY</span><span class="sxs-lookup"><span data-stu-id="bd5d8-103">WM\_MDIDESTROY message</span></span>

<span data-ttu-id="bd5d8-104">Une application envoie le message **WM \_ MDIDESTROY** à une fenêtre cliente d’interface multidocument (MDI) pour fermer une fenêtre enfant MDI.</span><span class="sxs-lookup"><span data-stu-id="bd5d8-104">An application sends the **WM\_MDIDESTROY** message to a multiple-document interface (MDI) client window to close an MDI child window.</span></span>


```C++
#define WM_MDIDESTROY                   0x0221
```



## <a name="parameters"></a><span data-ttu-id="bd5d8-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="bd5d8-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bd5d8-106">*wParam*</span><span class="sxs-lookup"><span data-stu-id="bd5d8-106">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="bd5d8-107">Handle de la fenêtre enfant MDI à fermer.</span><span class="sxs-lookup"><span data-stu-id="bd5d8-107">A handle to the MDI child window to be closed.</span></span>

</dd> <dt>

<span data-ttu-id="bd5d8-108">*lParam*</span><span class="sxs-lookup"><span data-stu-id="bd5d8-108">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="bd5d8-109">Ce paramètre n'est pas utilisé.</span><span class="sxs-lookup"><span data-stu-id="bd5d8-109">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bd5d8-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="bd5d8-110">Return value</span></span>

<span data-ttu-id="bd5d8-111">Type : **zéro**</span><span class="sxs-lookup"><span data-stu-id="bd5d8-111">Type: **zero**</span></span>

<span data-ttu-id="bd5d8-112">Ce message retourne toujours la valeur zéro.</span><span class="sxs-lookup"><span data-stu-id="bd5d8-112">This message always returns zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="bd5d8-113">Notes</span><span class="sxs-lookup"><span data-stu-id="bd5d8-113">Remarks</span></span>

<span data-ttu-id="bd5d8-114">Ce message supprime le titre de la fenêtre enfant MDI de la fenêtre frame MDI et désactive la fenêtre enfant.</span><span class="sxs-lookup"><span data-stu-id="bd5d8-114">This message removes the title of the MDI child window from the MDI frame window and deactivates the child window.</span></span> <span data-ttu-id="bd5d8-115">Une application doit utiliser ce message pour fermer toutes les fenêtres enfants MDI.</span><span class="sxs-lookup"><span data-stu-id="bd5d8-115">An application should use this message to close all MDI child windows.</span></span>

<span data-ttu-id="bd5d8-116">Si une fenêtre cliente MDI reçoit un message qui modifie l’activation de ses fenêtres enfants et que la fenêtre enfant MDI active est agrandie, le système restaure la fenêtre enfant active et agrandit la fenêtre enfant qui vient d’être activée.</span><span class="sxs-lookup"><span data-stu-id="bd5d8-116">If an MDI client window receives a message that changes the activation of its child windows and the active MDI child window is maximized, the system restores the active child window and maximizes the newly activated child window.</span></span>

## <a name="requirements"></a><span data-ttu-id="bd5d8-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="bd5d8-117">Requirements</span></span>



| <span data-ttu-id="bd5d8-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="bd5d8-118">Requirement</span></span> | <span data-ttu-id="bd5d8-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="bd5d8-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bd5d8-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bd5d8-120">Minimum supported client</span></span><br/> | <span data-ttu-id="bd5d8-121">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="bd5d8-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="bd5d8-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bd5d8-122">Minimum supported server</span></span><br/> | <span data-ttu-id="bd5d8-123">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="bd5d8-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="bd5d8-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="bd5d8-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="bd5d8-125"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="bd5d8-125"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bd5d8-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bd5d8-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="bd5d8-127">**Référence**</span><span class="sxs-lookup"><span data-stu-id="bd5d8-127">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="bd5d8-128">**\_MDICREATE WM**</span><span class="sxs-lookup"><span data-stu-id="bd5d8-128">**WM\_MDICREATE**</span></span>](wm-mdicreate.md)
</dt> <dt>

<span data-ttu-id="bd5d8-129">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="bd5d8-129">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="bd5d8-130">Interface multidocument</span><span class="sxs-lookup"><span data-stu-id="bd5d8-130">Multiple Document Interface</span></span>](multiple-document-interface.md)
</dt> </dl>

 

 




