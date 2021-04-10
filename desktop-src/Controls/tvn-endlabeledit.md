---
title: TVN_ENDLABELEDIT le code de notification (commctrl. h)
description: Avertit une fenêtre parente d’un contrôle Tree-View de la fin de la modification de l’étiquette d’un élément. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: 82eb9fcd-de10-4efb-8501-78c5af5e089e
keywords:
- Contrôles Windows de code de notification TVN_ENDLABELEDIT
topic_type:
- apiref
api_name:
- TVN_ENDLABELEDIT
- TVN_ENDLABELEDITA
- TVN_ENDLABELEDITW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c30d494ad90b3d55f85b1ad154aed0f814a1eec
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103900"
---
# <a name="tvn_endlabeledit-notification-code"></a><span data-ttu-id="1e401-105">\_Code de notification TVN ENDLABELEDIT</span><span class="sxs-lookup"><span data-stu-id="1e401-105">TVN\_ENDLABELEDIT notification code</span></span>

<span data-ttu-id="1e401-106">Avertit une fenêtre parente d’un contrôle Tree-View de la fin de la modification de l’étiquette d’un élément.</span><span class="sxs-lookup"><span data-stu-id="1e401-106">Notifies a tree-view control's parent window about the end of label editing for an item.</span></span> <span data-ttu-id="1e401-107">Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="1e401-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TVN_ENDLABELEDIT 

    ptvdi = (LPNMTVDISPINFO) lParam 
```



## <a name="parameters"></a><span data-ttu-id="1e401-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1e401-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1e401-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="1e401-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1e401-110">Pointeur vers une structure [**NMTVDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmtvdispinfoa) .</span><span class="sxs-lookup"><span data-stu-id="1e401-110">Pointer to an [**NMTVDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmtvdispinfoa) structure.</span></span> <span data-ttu-id="1e401-111">Le membre d' **élément** de cette structure est une structure [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) dont les membres **hitem**, **lParam** et **pszText** contiennent des informations valides sur l’élément qui a été modifié.</span><span class="sxs-lookup"><span data-stu-id="1e401-111">The **item** member of this structure is a [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) structure whose **hItem**, **lParam**, and **pszText** members contain valid information about the item that was edited.</span></span> <span data-ttu-id="1e401-112">Si la modification d’étiquette a été annulée, le membre **pszText** de la structure **TVITEM** est **null**; Sinon, **pszText** est l’adresse du texte modifié.</span><span class="sxs-lookup"><span data-stu-id="1e401-112">If label editing was canceled, the **pszText** member of the **TVITEM** structure is **NULL**; otherwise, **pszText** is the address of the edited text.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1e401-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="1e401-113">Return value</span></span>

<span data-ttu-id="1e401-114">Si le membre **pszText** n’est pas **null**, retourne **true** pour définir l’étiquette de l’élément sur le texte modifié.</span><span class="sxs-lookup"><span data-stu-id="1e401-114">If the **pszText** member is non-**NULL**, return **TRUE** to set the item's label to the edited text.</span></span> <span data-ttu-id="1e401-115">Retourne **false** pour rejeter le texte modifié et revenir à l’étiquette d’origine.</span><span class="sxs-lookup"><span data-stu-id="1e401-115">Return **FALSE** to reject the edited text and revert to the original label.</span></span>

## <a name="remarks"></a><span data-ttu-id="1e401-116">Notes</span><span class="sxs-lookup"><span data-stu-id="1e401-116">Remarks</span></span>

<span data-ttu-id="1e401-117">Si le membre **pszText** a la valeur **null**, la valeur de retour est ignorée.</span><span class="sxs-lookup"><span data-stu-id="1e401-117">If the **pszText** member is **NULL**, the return value is ignored.</span></span>

<span data-ttu-id="1e401-118">Si vous avez spécifié la \_ valeur LPSTR TEXTCALLBACK pour cet élément et que le membre **pszText** n’est pas **null**, votre \_ Gestionnaire TVN ENDLABELEDIT doit copier le texte de **pszText** dans votre stockage local.</span><span class="sxs-lookup"><span data-stu-id="1e401-118">If you specified the LPSTR\_TEXTCALLBACK value for this item and the **pszText** member is non-**NULL**, your TVN\_ENDLABELEDIT handler should copy the text from **pszText** to your local storage.</span></span>

## <a name="requirements"></a><span data-ttu-id="1e401-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1e401-119">Requirements</span></span>



| <span data-ttu-id="1e401-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1e401-120">Requirement</span></span> | <span data-ttu-id="1e401-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="1e401-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1e401-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1e401-122">Minimum supported client</span></span><br/> | <span data-ttu-id="1e401-123">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1e401-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="1e401-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1e401-124">Minimum supported server</span></span><br/> | <span data-ttu-id="1e401-125">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1e401-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="1e401-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="1e401-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="1e401-127"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="1e401-127"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="1e401-128">Noms Unicode et ANSI</span><span class="sxs-lookup"><span data-stu-id="1e401-128">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="1e401-129">**TVN \_ ENDLABELEDITW** (Unicode) et **TVN \_ ENDLABELEDITA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="1e401-129">**TVN\_ENDLABELEDITW** (Unicode) and **TVN\_ENDLABELEDITA** (ANSI)</span></span><br/>         |



 

 





