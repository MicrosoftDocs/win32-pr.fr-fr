---
title: Message SBM_GETPOS (winuser. h)
description: Le \_ message SBM GETPOS est envoyé pour récupérer la position actuelle de la case de défilement d’un contrôle de barre de défilement.
ms.assetid: 00344d93-f205-4cda-aa25-6dd065f41b6e
keywords:
- SBM_GETPOS les contrôles de message Windows
topic_type:
- apiref
api_name:
- SBM_GETPOS
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d088fc790985e57928f1ab56cd42254b1a087dc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942541"
---
# <a name="sbm_getpos-message"></a><span data-ttu-id="ccea4-104">\_Message SBM GETPOS</span><span class="sxs-lookup"><span data-stu-id="ccea4-104">SBM\_GETPOS message</span></span>

<span data-ttu-id="ccea4-105">Le message **SBM \_ GETPOS** est envoyé pour récupérer la position actuelle de la case de défilement d’un contrôle de barre de défilement.</span><span class="sxs-lookup"><span data-stu-id="ccea4-105">The **SBM\_GETPOS** message is sent to retrieve the current position of the scroll box of a scroll bar control.</span></span> <span data-ttu-id="ccea4-106">La position actuelle est une valeur relative qui dépend de la plage de défilement actuelle.</span><span class="sxs-lookup"><span data-stu-id="ccea4-106">The current position is a relative value that depends on the current scrolling range.</span></span> <span data-ttu-id="ccea4-107">Par exemple, si la plage de défilement est comprise entre 0 et 100 et que la case de défilement se trouve au milieu de la barre, la position actuelle est 50.</span><span class="sxs-lookup"><span data-stu-id="ccea4-107">For example, if the scrolling range is 0 through 100 and the scroll box is in the middle of the bar, the current position is 50.</span></span>

<span data-ttu-id="ccea4-108">Les applications ne doivent pas envoyer ce message directement.</span><span class="sxs-lookup"><span data-stu-id="ccea4-108">Applications should not send this message directly.</span></span> <span data-ttu-id="ccea4-109">Au lieu de cela, ils doivent utiliser la fonction [**GetScrollPos**](/windows/desktop/api/Winuser/nf-winuser-getscrollpos) .</span><span class="sxs-lookup"><span data-stu-id="ccea4-109">Instead, they should use the [**GetScrollPos**](/windows/desktop/api/Winuser/nf-winuser-getscrollpos) function.</span></span> <span data-ttu-id="ccea4-110">Une fenêtre reçoit ce message par le biais de sa fonction [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="ccea4-110">A window receives this message through its [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span> <span data-ttu-id="ccea4-111">Les applications qui implémentent un contrôle de barre de défilement personnalisé doivent répondre à ces messages pour que la fonction **GetScrollPos** fonctionne correctement.</span><span class="sxs-lookup"><span data-stu-id="ccea4-111">Applications which implement a custom scroll bar control must respond to these messages for the **GetScrollPos** function to function properly.</span></span>

## <a name="parameters"></a><span data-ttu-id="ccea4-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ccea4-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ccea4-113">*wParam*</span><span class="sxs-lookup"><span data-stu-id="ccea4-113">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ccea4-114">Non utilisé ; doit être égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="ccea4-114">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="ccea4-115">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ccea4-115">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ccea4-116">Non utilisé ; doit être égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="ccea4-116">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ccea4-117">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="ccea4-117">Return value</span></span>

<span data-ttu-id="ccea4-118">La valeur de retour correspond à la position actuelle de la case de défilement dans la barre de défilement.</span><span class="sxs-lookup"><span data-stu-id="ccea4-118">The return value is the current position of the scroll box in the scroll bar.</span></span>

## <a name="requirements"></a><span data-ttu-id="ccea4-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ccea4-119">Requirements</span></span>



| <span data-ttu-id="ccea4-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ccea4-120">Requirement</span></span> | <span data-ttu-id="ccea4-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="ccea4-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ccea4-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ccea4-122">Minimum supported client</span></span><br/> | <span data-ttu-id="ccea4-123">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ccea4-123">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="ccea4-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ccea4-124">Minimum supported server</span></span><br/> | <span data-ttu-id="ccea4-125">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ccea4-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="ccea4-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="ccea4-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="ccea4-127"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ccea4-127"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ccea4-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ccea4-128">See also</span></span>

<dl> <dt>

<span data-ttu-id="ccea4-129">**Référence**</span><span class="sxs-lookup"><span data-stu-id="ccea4-129">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="ccea4-130">**\_GETRANGE SBM**</span><span class="sxs-lookup"><span data-stu-id="ccea4-130">**SBM\_GETRANGE**</span></span>](sbm-getrange.md)
</dt> <dt>

[<span data-ttu-id="ccea4-131">**\_SetPos SBM**</span><span class="sxs-lookup"><span data-stu-id="ccea4-131">**SBM\_SETPOS**</span></span>](sbm-setpos.md)
</dt> <dt>

[<span data-ttu-id="ccea4-132">**\_DÉtrange SBM**</span><span class="sxs-lookup"><span data-stu-id="ccea4-132">**SBM\_SETRANGE**</span></span>](sbm-setrange.md)
</dt> <dt>

[<span data-ttu-id="ccea4-133">**\_SETRANGEREDRAW SBM**</span><span class="sxs-lookup"><span data-stu-id="ccea4-133">**SBM\_SETRANGEREDRAW**</span></span>](sbm-setrangeredraw.md)
</dt> </dl>

 

