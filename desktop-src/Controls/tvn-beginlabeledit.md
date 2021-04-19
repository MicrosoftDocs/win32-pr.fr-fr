---
title: TVN_BEGINLABELEDIT le code de notification (commctrl. h)
description: Avertit une fenêtre parente d’un contrôle Tree-View du début de la modification de l’étiquette d’un élément. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: 67ed1f1f-7ccc-4e84-9540-4a46f6cd3a44
keywords:
- Contrôles Windows de code de notification TVN_BEGINLABELEDIT
topic_type:
- apiref
api_name:
- TVN_BEGINLABELEDIT
- TVN_BEGINLABELEDITA
- TVN_BEGINLABELEDITW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 34eccdeda553d0792a2862e3ca81a0889539d5ae
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106509528"
---
# <a name="tvn_beginlabeledit-notification-code"></a><span data-ttu-id="89730-105">\_Code de notification TVN BEGINLABELEDIT</span><span class="sxs-lookup"><span data-stu-id="89730-105">TVN\_BEGINLABELEDIT notification code</span></span>

<span data-ttu-id="89730-106">Avertit une fenêtre parente d’un contrôle Tree-View du début de la modification de l’étiquette d’un élément.</span><span class="sxs-lookup"><span data-stu-id="89730-106">Notifies a tree-view control's parent window about the start of label editing for an item.</span></span> <span data-ttu-id="89730-107">Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="89730-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TVN_BEGINLABELEDIT 

    ptvdi = (LPNMTVDISPINFO) lParam 
```



## <a name="parameters"></a><span data-ttu-id="89730-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="89730-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="89730-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="89730-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="89730-110">Pointeur vers une structure [**NMTVDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmtvdispinfoa) .</span><span class="sxs-lookup"><span data-stu-id="89730-110">Pointer to an [**NMTVDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmtvdispinfoa) structure.</span></span> <span data-ttu-id="89730-111">Le membre de l' **élément** est une structure [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) qui contient des informations valides sur l’élément en cours de modification dans les membres **hitem**, **State**, **lParam** et **pszText** .</span><span class="sxs-lookup"><span data-stu-id="89730-111">The **item** member is a [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) structure that contains valid information about the item being edited in the **hItem**, **state**, **lParam**, and **pszText** members.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="89730-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="89730-112">Return value</span></span>

<span data-ttu-id="89730-113">Retourne la **valeur true** pour annuler la modification de l’étiquette.</span><span class="sxs-lookup"><span data-stu-id="89730-113">Returns **TRUE** to cancel label editing.</span></span>

## <a name="remarks"></a><span data-ttu-id="89730-114">Notes</span><span class="sxs-lookup"><span data-stu-id="89730-114">Remarks</span></span>

<span data-ttu-id="89730-115">Lorsque la modification d’étiquette commence, un contrôle d’édition est créé mais pas positionné ou affiché.</span><span class="sxs-lookup"><span data-stu-id="89730-115">When label editing begins, an edit control is created but not positioned or displayed.</span></span> <span data-ttu-id="89730-116">Avant qu’il ne soit affiché, le contrôle Tree-View envoie sa fenêtre parente un \_ Code de notification TVN BEGINLABELEDIT.</span><span class="sxs-lookup"><span data-stu-id="89730-116">Before it is displayed, the tree-view control sends its parent window a TVN\_BEGINLABELEDIT notification code.</span></span>

<span data-ttu-id="89730-117">Pour personnaliser la modification des étiquettes, implémentez un gestionnaire pour TVN \_ BEGINLABELEDIT et envoyez un message [**TVM \_ GETEDITCONTROL**](tvm-geteditcontrol.md) au contrôle Tree-View.</span><span class="sxs-lookup"><span data-stu-id="89730-117">To customize label editing, implement a handler for TVN\_BEGINLABELEDIT and have it send a [**TVM\_GETEDITCONTROL**](tvm-geteditcontrol.md) message to the tree-view control.</span></span> <span data-ttu-id="89730-118">Si une étiquette est en cours de modification, la valeur de retour est un handle pour le contrôle d’édition.</span><span class="sxs-lookup"><span data-stu-id="89730-118">If a label is being edited, the return value will be a handle to the edit control.</span></span> <span data-ttu-id="89730-119">Utilisez ce handle pour personnaliser le contrôle d’édition en envoyant les messages EM xxx habituels \_ .</span><span class="sxs-lookup"><span data-stu-id="89730-119">Use this handle to customize the edit control by sending the usual EM\_XXX messages.</span></span>

<span data-ttu-id="89730-120">Lorsque l’utilisateur annule ou termine la modification, la fenêtre parente reçoit un code de notification [TVN \_ ENDLABELEDIT](tvn-endlabeledit.md) .</span><span class="sxs-lookup"><span data-stu-id="89730-120">When the user cancels or completes the editing, the parent window receives a [TVN\_ENDLABELEDIT](tvn-endlabeledit.md) notification code.</span></span>

## <a name="requirements"></a><span data-ttu-id="89730-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="89730-121">Requirements</span></span>



| <span data-ttu-id="89730-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="89730-122">Requirement</span></span> | <span data-ttu-id="89730-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="89730-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="89730-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="89730-124">Minimum supported client</span></span><br/> | <span data-ttu-id="89730-125">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="89730-125">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="89730-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="89730-126">Minimum supported server</span></span><br/> | <span data-ttu-id="89730-127">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="89730-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="89730-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="89730-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="89730-129"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="89730-129"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="89730-130">Noms Unicode et ANSI</span><span class="sxs-lookup"><span data-stu-id="89730-130">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="89730-131">**TVN \_ BEGINLABELEDITW** (Unicode) et **TVN \_ BEGINLABELEDITA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="89730-131">**TVN\_BEGINLABELEDITW** (Unicode) and **TVN\_BEGINLABELEDITA** (ANSI)</span></span><br/>     |



 

 





