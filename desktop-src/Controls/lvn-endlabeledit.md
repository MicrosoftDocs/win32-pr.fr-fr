---
title: LVN_ENDLABELEDIT le code de notification (commctrl. h)
description: Avertit une fenêtre parente d’un contrôle List-View de la fin de la modification de l’étiquette d’un élément. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: 03129fef-abf1-4374-b4b8-503c46ef7115
keywords:
- Contrôles Windows de code de notification LVN_ENDLABELEDIT
topic_type:
- apiref
api_name:
- LVN_ENDLABELEDIT
- LVN_ENDLABELEDITA
- LVN_ENDLABELEDITW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1a33ab69a04202aeb3817d3eeadf01fb6f1fcaac
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106527580"
---
# <a name="lvn_endlabeledit-notification-code"></a><span data-ttu-id="a864b-105">\_Code de notification LVN ENDLABELEDIT</span><span class="sxs-lookup"><span data-stu-id="a864b-105">LVN\_ENDLABELEDIT notification code</span></span>

<span data-ttu-id="a864b-106">Avertit une fenêtre parente d’un contrôle List-View de la fin de la modification de l’étiquette d’un élément.</span><span class="sxs-lookup"><span data-stu-id="a864b-106">Notifies a list-view control's parent window about the end of label editing for an item.</span></span> <span data-ttu-id="a864b-107">Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="a864b-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
LVN_ENDLABELEDIT

    pdi = (LPNMLVDISPINFO) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="a864b-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a864b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a864b-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a864b-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a864b-110">Pointeur vers une structure [**NMLVDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmlvdispinfoa) .</span><span class="sxs-lookup"><span data-stu-id="a864b-110">Pointer to an [**NMLVDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmlvdispinfoa) structure.</span></span> <span data-ttu-id="a864b-111">Le membre d' **élément** de cette structure est une structure [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) dont le membre **iItem** identifie l’élément en cours de modification.</span><span class="sxs-lookup"><span data-stu-id="a864b-111">The **item** member of this structure is an [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) structure whose **iItem** member identifies the item being edited.</span></span> <span data-ttu-id="a864b-112">Le membre **pszText** de l' **élément** contient une valeur valide lorsque le \_ Code de notification ENDLABELEDIT LVN est envoyé, que l' \_ indicateur de texte LVIF soit défini ou non dans le membre **Mask** de la structure **LVITEM** .</span><span class="sxs-lookup"><span data-stu-id="a864b-112">The **pszText** member of **item** contains a valid value when the LVN\_ENDLABELEDIT notification code is sent, regardless of whether the LVIF\_TEXT flag is set in the **mask** member of the **LVITEM** structure.</span></span> <span data-ttu-id="a864b-113">Si l’utilisateur annule la modification, le membre **pszText** de la structure **LVITEM** est **null**; Sinon, **pszText** est l’adresse du texte modifié.</span><span class="sxs-lookup"><span data-stu-id="a864b-113">If the user cancels editing, the **pszText** member of the **LVITEM** structure is **NULL**; otherwise, **pszText** is the address of the edited text.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a864b-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="a864b-114">Return value</span></span>

<span data-ttu-id="a864b-115">Si le membre **pszText** de la structure [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) est non **null**, retourne **true** pour définir l’étiquette de l’élément sur le texte modifié.</span><span class="sxs-lookup"><span data-stu-id="a864b-115">If the **pszText** member of the [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) structure is non-**NULL**, return **TRUE** to set the item's label to the edited text.</span></span> <span data-ttu-id="a864b-116">Retourne **false** pour rejeter le texte modifié et revenir à l’étiquette d’origine.</span><span class="sxs-lookup"><span data-stu-id="a864b-116">Return **FALSE** to reject the edited text and revert to the original label.</span></span>

<span data-ttu-id="a864b-117">Si le membre **pszText** de la structure [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) est **null**, la valeur de retour est ignorée.</span><span class="sxs-lookup"><span data-stu-id="a864b-117">If the **pszText** member of the [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) structure is **NULL**, the return value is ignored.</span></span>

## <a name="remarks"></a><span data-ttu-id="a864b-118">Notes</span><span class="sxs-lookup"><span data-stu-id="a864b-118">Remarks</span></span>

<span data-ttu-id="a864b-119">La valeur de retour de la procédure de boîte de dialogue est si le message a été géré.</span><span class="sxs-lookup"><span data-stu-id="a864b-119">The return value of the dialog procedure is whether the message was handled.</span></span> <span data-ttu-id="a864b-120">La deuxième valeur de retour doit être définie en appelant [**SetwindowLongPtr**](/windows/win32/api/winuser/nf-winuser-setwindowlongptra) avec **DWLP_MSGRESULT**.</span><span class="sxs-lookup"><span data-stu-id="a864b-120">The second return value must be set by calling [**SetwindowLongPtr**](/windows/win32/api/winuser/nf-winuser-setwindowlongptra) with **DWLP_MSGRESULT**.</span></span>

<span data-ttu-id="a864b-121">Lorsque l’utilisateur commence à modifier une étiquette d’élément, la fenêtre parente du contrôle List-View reçoit un code de notification [LVN \_ BEGINLABELEDIT](lvn-beginlabeledit.md) .</span><span class="sxs-lookup"><span data-stu-id="a864b-121">When the user begins editing an item label, the parent window of the list-view control receives an [LVN\_BEGINLABELEDIT](lvn-beginlabeledit.md) notification code.</span></span> <span data-ttu-id="a864b-122">Lorsque l’utilisateur annule ou termine la modification, la fenêtre parente reçoit un \_ Code de notification LVN ENDLABELEDIT.</span><span class="sxs-lookup"><span data-stu-id="a864b-122">When the user cancels or completes the editing, the parent window receives an LVN\_ENDLABELEDIT notification code.</span></span>

## <a name="requirements"></a><span data-ttu-id="a864b-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a864b-123">Requirements</span></span>



| <span data-ttu-id="a864b-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a864b-124">Requirement</span></span> | <span data-ttu-id="a864b-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="a864b-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a864b-126">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a864b-126">Minimum supported client</span></span><br/> | <span data-ttu-id="a864b-127">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a864b-127">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="a864b-128">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a864b-128">Minimum supported server</span></span><br/> | <span data-ttu-id="a864b-129">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a864b-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="a864b-130">En-tête</span><span class="sxs-lookup"><span data-stu-id="a864b-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="a864b-131"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="a864b-131"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="a864b-132">Noms Unicode et ANSI</span><span class="sxs-lookup"><span data-stu-id="a864b-132">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="a864b-133">**LVN \_ ENDLABELEDITW** (Unicode) et **LVN \_ ENDLABELEDITA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="a864b-133">**LVN\_ENDLABELEDITW** (Unicode) and **LVN\_ENDLABELEDITA** (ANSI)</span></span><br/>         |



 

 





