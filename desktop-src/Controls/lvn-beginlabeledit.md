---
title: LVN_BEGINLABELEDIT le code de notification (commctrl. h)
description: Avertit une fenêtre parente d’un contrôle List-View à propos du début de la modification de l’étiquette d’un élément. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: c13a9e95-22a9-476e-aeee-4928b8b096b0
keywords:
- Contrôles Windows de code de notification LVN_BEGINLABELEDIT
topic_type:
- apiref
api_name:
- LVN_BEGINLABELEDIT
- LVN_BEGINLABELEDITA
- LVN_BEGINLABELEDITW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f77550b474534cee096b610a0805bce547d9b429
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103941710"
---
# <a name="lvn_beginlabeledit-notification-code"></a><span data-ttu-id="91ae7-105">\_Code de notification LVN BEGINLABELEDIT</span><span class="sxs-lookup"><span data-stu-id="91ae7-105">LVN\_BEGINLABELEDIT notification code</span></span>

<span data-ttu-id="91ae7-106">Avertit une fenêtre parente d’un contrôle List-View à propos du début de la modification de l’étiquette d’un élément.</span><span class="sxs-lookup"><span data-stu-id="91ae7-106">Notifies a list-view control's parent window about the start of label editing for an item.</span></span> <span data-ttu-id="91ae7-107">Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="91ae7-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
LVN_BEGINLABELEDIT

    pdi = (LPNMLVDISPINFO) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="91ae7-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="91ae7-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="91ae7-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="91ae7-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="91ae7-110">Pointeur vers une structure [**NMLVDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmlvdispinfoa) .</span><span class="sxs-lookup"><span data-stu-id="91ae7-110">Pointer to an [**NMLVDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmlvdispinfoa) structure.</span></span> <span data-ttu-id="91ae7-111">Le membre d' **élément** de cette structure est une structure [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) dont le membre **iItem** identifie l’élément en cours de modification.</span><span class="sxs-lookup"><span data-stu-id="91ae7-111">The **item** member of this structure is an [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) structure whose **iItem** member identifies the item being edited.</span></span> <span data-ttu-id="91ae7-112">Notez que les sous-éléments ne peuvent pas être modifiés ; le membre **iSubItem** est toujours défini sur zéro.</span><span class="sxs-lookup"><span data-stu-id="91ae7-112">Note that subitems cannot be edited; the **iSubItem** member is always set to zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="91ae7-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="91ae7-113">Return value</span></span>

<span data-ttu-id="91ae7-114">Pour permettre à l’utilisateur de modifier l’étiquette, retournez **false**.</span><span class="sxs-lookup"><span data-stu-id="91ae7-114">To allow the user to edit the label, return **FALSE**.</span></span>

<span data-ttu-id="91ae7-115">Pour empêcher l’utilisateur de modifier l’étiquette, retournez la **valeur true**.</span><span class="sxs-lookup"><span data-stu-id="91ae7-115">To prevent the user from editing the label, return **TRUE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="91ae7-116">Notes</span><span class="sxs-lookup"><span data-stu-id="91ae7-116">Remarks</span></span>

<span data-ttu-id="91ae7-117">Lorsque la modification d’étiquette commence, un contrôle d’édition est créé, positionné et initialisé.</span><span class="sxs-lookup"><span data-stu-id="91ae7-117">When label editing begins, an edit control is created, positioned, and initialized.</span></span> <span data-ttu-id="91ae7-118">Avant qu’il ne soit affiché, le contrôle List-View envoie sa fenêtre parente à un \_ Code de notification LVN BEGINLABELEDIT.</span><span class="sxs-lookup"><span data-stu-id="91ae7-118">Before it is displayed, the list-view control sends its parent window an LVN\_BEGINLABELEDIT notification code.</span></span>

<span data-ttu-id="91ae7-119">Pour personnaliser la modification des étiquettes, implémentez un gestionnaire pour LVN \_ BEGINLABELEDIT et envoyez-lui un message [**\_ GETEDITCONTROL LVM**](lvm-geteditcontrol.md) vers le contrôle List-View.</span><span class="sxs-lookup"><span data-stu-id="91ae7-119">To customize label editing, implement a handler for LVN\_BEGINLABELEDIT and have it send an [**LVM\_GETEDITCONTROL**](lvm-geteditcontrol.md) message to the list-view control.</span></span> <span data-ttu-id="91ae7-120">Si une étiquette est en cours de modification, la valeur de retour est un handle pour le contrôle d’édition.</span><span class="sxs-lookup"><span data-stu-id="91ae7-120">If a label is being edited, the return value will be a handle to the edit control.</span></span> <span data-ttu-id="91ae7-121">Utilisez ce handle pour personnaliser le contrôle d’édition en envoyant les messages **em \_ xxx** habituels.</span><span class="sxs-lookup"><span data-stu-id="91ae7-121">Use this handle to customize the edit control by sending the usual **EM\_XXX** messages.</span></span>

<span data-ttu-id="91ae7-122">Lorsque l’utilisateur annule ou termine la modification, la fenêtre parente reçoit un code de notification [LVN \_ ENDLABELEDIT](lvn-endlabeledit.md) .</span><span class="sxs-lookup"><span data-stu-id="91ae7-122">When the user cancels or completes the editing, the parent window receives an [LVN\_ENDLABELEDIT](lvn-endlabeledit.md) notification code.</span></span>

## <a name="requirements"></a><span data-ttu-id="91ae7-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="91ae7-123">Requirements</span></span>



| <span data-ttu-id="91ae7-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="91ae7-124">Requirement</span></span> | <span data-ttu-id="91ae7-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="91ae7-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="91ae7-126">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="91ae7-126">Minimum supported client</span></span><br/> | <span data-ttu-id="91ae7-127">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="91ae7-127">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="91ae7-128">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="91ae7-128">Minimum supported server</span></span><br/> | <span data-ttu-id="91ae7-129">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="91ae7-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="91ae7-130">En-tête</span><span class="sxs-lookup"><span data-stu-id="91ae7-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="91ae7-131"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="91ae7-131"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="91ae7-132">Noms Unicode et ANSI</span><span class="sxs-lookup"><span data-stu-id="91ae7-132">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="91ae7-133">**LVN \_ BEGINLABELEDITW** (Unicode) et **LVN \_ BEGINLABELEDITA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="91ae7-133">**LVN\_BEGINLABELEDITW** (Unicode) and **LVN\_BEGINLABELEDITA** (ANSI)</span></span><br/>     |



 

 





