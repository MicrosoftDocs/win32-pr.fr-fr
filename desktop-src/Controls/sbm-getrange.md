---
title: Message SBM_GETRANGE (winuser. h)
description: Le \_ message SBM GETRANGE est envoyé pour récupérer les valeurs de position minimale et maximale pour le contrôle de barre de défilement.
ms.assetid: 661a9491-3bf6-4685-aea0-c5e4126313af
keywords:
- SBM_GETRANGE les contrôles de message Windows
topic_type:
- apiref
api_name:
- SBM_GETRANGE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a8ca47e0474152a9771d2787c4a039fb2c868b8c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942540"
---
# <a name="sbm_getrange-message"></a><span data-ttu-id="cbc4b-104">\_Message SBM GETRANGE</span><span class="sxs-lookup"><span data-stu-id="cbc4b-104">SBM\_GETRANGE message</span></span>

<span data-ttu-id="cbc4b-105">Le message **SBM \_ GETRANGE** est envoyé pour récupérer les valeurs de position minimale et maximale pour le contrôle de barre de défilement.</span><span class="sxs-lookup"><span data-stu-id="cbc4b-105">The **SBM\_GETRANGE** message is sent to retrieve the minimum and maximum position values for the scroll bar control.</span></span>

<span data-ttu-id="cbc4b-106">Les applications ne doivent pas envoyer ce message directement.</span><span class="sxs-lookup"><span data-stu-id="cbc4b-106">Applications should not send this message directly.</span></span> <span data-ttu-id="cbc4b-107">Au lieu de cela, ils doivent utiliser la fonction [**GetScrollRange**](/windows/desktop/api/Winuser/nf-winuser-getscrollrange) .</span><span class="sxs-lookup"><span data-stu-id="cbc4b-107">Instead, they should use the [**GetScrollRange**](/windows/desktop/api/Winuser/nf-winuser-getscrollrange) function.</span></span> <span data-ttu-id="cbc4b-108">Une fenêtre reçoit ce message par le biais de sa fonction [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="cbc4b-108">A window receives this message through its [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span> <span data-ttu-id="cbc4b-109">Les applications qui implémentent un contrôle de barre de défilement personnalisé doivent répondre à ces messages pour que la fonction **GetScrollRange** fonctionne correctement.</span><span class="sxs-lookup"><span data-stu-id="cbc4b-109">Applications which implement a custom scroll bar control must respond to these messages for the **GetScrollRange** function to work properly.</span></span>

## <a name="parameters"></a><span data-ttu-id="cbc4b-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="cbc4b-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cbc4b-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="cbc4b-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="cbc4b-112">Pointeur vers une variable qui reçoit la position de défilement minimale.</span><span class="sxs-lookup"><span data-stu-id="cbc4b-112">Pointer to a variable that receives the minimum scrolling position.</span></span>

</dd> <dt>

<span data-ttu-id="cbc4b-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="cbc4b-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="cbc4b-114">Pointeur vers une variable qui reçoit la position de défilement maximale.</span><span class="sxs-lookup"><span data-stu-id="cbc4b-114">Pointer to a variable that receives the maximum scrolling position.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cbc4b-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="cbc4b-115">Return value</span></span>

<span data-ttu-id="cbc4b-116">Ce message ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="cbc4b-116">This message does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="cbc4b-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="cbc4b-117">Requirements</span></span>



| <span data-ttu-id="cbc4b-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="cbc4b-118">Requirement</span></span> | <span data-ttu-id="cbc4b-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="cbc4b-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cbc4b-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cbc4b-120">Minimum supported client</span></span><br/> | <span data-ttu-id="cbc4b-121">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="cbc4b-121">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="cbc4b-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cbc4b-122">Minimum supported server</span></span><br/> | <span data-ttu-id="cbc4b-123">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="cbc4b-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="cbc4b-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="cbc4b-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="cbc4b-125"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="cbc4b-125"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cbc4b-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cbc4b-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="cbc4b-127">**Référence**</span><span class="sxs-lookup"><span data-stu-id="cbc4b-127">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="cbc4b-128">**\_GETPOS SBM**</span><span class="sxs-lookup"><span data-stu-id="cbc4b-128">**SBM\_GETPOS**</span></span>](sbm-getpos.md)
</dt> <dt>

[<span data-ttu-id="cbc4b-129">**\_SetPos SBM**</span><span class="sxs-lookup"><span data-stu-id="cbc4b-129">**SBM\_SETPOS**</span></span>](sbm-setpos.md)
</dt> <dt>

[<span data-ttu-id="cbc4b-130">**\_DÉtrange SBM**</span><span class="sxs-lookup"><span data-stu-id="cbc4b-130">**SBM\_SETRANGE**</span></span>](sbm-setrange.md)
</dt> <dt>

[<span data-ttu-id="cbc4b-131">**\_SETRANGEREDRAW SBM**</span><span class="sxs-lookup"><span data-stu-id="cbc4b-131">**SBM\_SETRANGEREDRAW**</span></span>](sbm-setrangeredraw.md)
</dt> </dl>

 

