---
title: Message SBM_SETRANGE (winuser. h)
description: Le \_ message SBM SEtrange est envoyé pour définir les valeurs de position minimale et maximale pour le contrôle de barre de défilement.
ms.assetid: 9cf84354-3944-4c10-9b59-39427b840868
keywords:
- SBM_SETRANGE les contrôles de message Windows
topic_type:
- apiref
api_name:
- SBM_SETRANGE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f7a720531ae58fdb0712b8f23fd1aef88b3e4caa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103844193"
---
# <a name="sbm_setrange-message"></a><span data-ttu-id="76d1f-104">\_Message de DÉtrange SBM</span><span class="sxs-lookup"><span data-stu-id="76d1f-104">SBM\_SETRANGE message</span></span>

<span data-ttu-id="76d1f-105">Le message **SBM \_ SetRange** est envoyé pour définir les valeurs de position minimale et maximale pour le contrôle de barre de défilement.</span><span class="sxs-lookup"><span data-stu-id="76d1f-105">The **SBM\_SETRANGE** message is sent to set the minimum and maximum position values for the scroll bar control.</span></span>

<span data-ttu-id="76d1f-106">Les applications ne doivent pas envoyer ce message directement.</span><span class="sxs-lookup"><span data-stu-id="76d1f-106">Applications should not send this message directly.</span></span> <span data-ttu-id="76d1f-107">Au lieu de cela, ils doivent utiliser la fonction [**SetScrollRange**](/windows/desktop/api/Winuser/nf-winuser-setscrollrange) .</span><span class="sxs-lookup"><span data-stu-id="76d1f-107">Instead, they should use the [**SetScrollRange**](/windows/desktop/api/Winuser/nf-winuser-setscrollrange) function.</span></span> <span data-ttu-id="76d1f-108">Une fenêtre reçoit ce message par le biais de sa fonction [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="76d1f-108">A window receives this message through its [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span> <span data-ttu-id="76d1f-109">Les applications qui implémentent un contrôle de barre de défilement personnalisé doivent répondre à ces messages pour que la fonction **SetScrollRange** fonctionne correctement.</span><span class="sxs-lookup"><span data-stu-id="76d1f-109">Applications which implement a custom scroll bar control must respond to these messages for the **SetScrollRange** function to work properly.</span></span>

## <a name="parameters"></a><span data-ttu-id="76d1f-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="76d1f-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="76d1f-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="76d1f-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="76d1f-112">Spécifie la position de défilement minimale.</span><span class="sxs-lookup"><span data-stu-id="76d1f-112">Specifies the minimum scrolling position.</span></span>

</dd> <dt>

<span data-ttu-id="76d1f-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="76d1f-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="76d1f-114">Spécifie la position de défilement maximale.</span><span class="sxs-lookup"><span data-stu-id="76d1f-114">Specifies the maximum scrolling position.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="76d1f-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="76d1f-115">Return value</span></span>

<span data-ttu-id="76d1f-116">**ComCtl32.dll version 5,0**: si la position de la case de défilement a changé, la valeur de retour est la position précédente de la case de défilement ; dans le cas contraire, il est égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="76d1f-116">**ComCtl32.dll version 5.0**: If the position of the scroll box changed, the return value is the previous position of the scroll box; otherwise, it is zero.</span></span>

<span data-ttu-id="76d1f-117">**ComCtl32.dll version 6,0**: position actuelle de la case de défilement, qu’elle ait été modifiée ou non.</span><span class="sxs-lookup"><span data-stu-id="76d1f-117">**ComCtl32.dll version 6.0**: The current position of the scroll box, regardless of whether it has changed.</span></span>

## <a name="remarks"></a><span data-ttu-id="76d1f-118">Notes</span><span class="sxs-lookup"><span data-stu-id="76d1f-118">Remarks</span></span>

<span data-ttu-id="76d1f-119">Les valeurs par défaut de la position minimale et maximale sont égales à zéro.</span><span class="sxs-lookup"><span data-stu-id="76d1f-119">The default minimum and maximum position values are zero.</span></span> <span data-ttu-id="76d1f-120">La différence entre les valeurs spécifiées par les paramètres *wParam* et *lParam* ne doit pas être supérieure à MAXLONG.</span><span class="sxs-lookup"><span data-stu-id="76d1f-120">The difference between the values specified by the *wParam* and *lParam* parameters must not be greater than MAXLONG.</span></span>

<span data-ttu-id="76d1f-121">Si les valeurs de position minimale et maximale sont égales, le contrôle de barre de défilement est masqué et, en fait, désactivé.</span><span class="sxs-lookup"><span data-stu-id="76d1f-121">If the minimum and maximum position values are equal, the scroll bar control is hidden and, in effect, disabled.</span></span>

## <a name="requirements"></a><span data-ttu-id="76d1f-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="76d1f-122">Requirements</span></span>



| <span data-ttu-id="76d1f-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="76d1f-123">Requirement</span></span> | <span data-ttu-id="76d1f-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="76d1f-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="76d1f-125">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="76d1f-125">Minimum supported client</span></span><br/> | <span data-ttu-id="76d1f-126">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="76d1f-126">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="76d1f-127">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="76d1f-127">Minimum supported server</span></span><br/> | <span data-ttu-id="76d1f-128">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="76d1f-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="76d1f-129">En-tête</span><span class="sxs-lookup"><span data-stu-id="76d1f-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="76d1f-130"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="76d1f-130"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="76d1f-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="76d1f-131">See also</span></span>

<dl> <dt>

<span data-ttu-id="76d1f-132">**Référence**</span><span class="sxs-lookup"><span data-stu-id="76d1f-132">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="76d1f-133">**\_GETPOS SBM**</span><span class="sxs-lookup"><span data-stu-id="76d1f-133">**SBM\_GETPOS**</span></span>](sbm-getpos.md)
</dt> <dt>

[<span data-ttu-id="76d1f-134">**\_GETRANGE SBM**</span><span class="sxs-lookup"><span data-stu-id="76d1f-134">**SBM\_GETRANGE**</span></span>](sbm-getrange.md)
</dt> <dt>

[<span data-ttu-id="76d1f-135">**\_SetPos SBM**</span><span class="sxs-lookup"><span data-stu-id="76d1f-135">**SBM\_SETPOS**</span></span>](sbm-setpos.md)
</dt> <dt>

[<span data-ttu-id="76d1f-136">**\_SETRANGEREDRAW SBM**</span><span class="sxs-lookup"><span data-stu-id="76d1f-136">**SBM\_SETRANGEREDRAW**</span></span>](sbm-setrangeredraw.md)
</dt> </dl>

 

