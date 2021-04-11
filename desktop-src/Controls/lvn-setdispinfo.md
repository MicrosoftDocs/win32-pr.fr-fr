---
title: LVN_SETDISPINFO le code de notification (commctrl. h)
description: Avertit la fenêtre parente d’un contrôle List-View qu’il doit mettre à jour les informations qu’il gère pour un élément. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: 1ea51d50-4a57-4662-972e-89e916fa9b16
keywords:
- Contrôles Windows de code de notification LVN_SETDISPINFO
topic_type:
- apiref
api_name:
- LVN_SETDISPINFO
- LVN_SETDISPINFOA
- LVN_SETDISPINFOW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 659623d892f0f5a556f4890703d4e0dd725536b5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942480"
---
# <a name="lvn_setdispinfo-notification-code"></a><span data-ttu-id="efd42-105">\_Code de notification LVN SETDISPINFO</span><span class="sxs-lookup"><span data-stu-id="efd42-105">LVN\_SETDISPINFO notification code</span></span>

<span data-ttu-id="efd42-106">Avertit la fenêtre parente d’un contrôle List-View qu’il doit mettre à jour les informations qu’il gère pour un élément.</span><span class="sxs-lookup"><span data-stu-id="efd42-106">Notifies a list-view control's parent window that it must update the information it maintains for an item.</span></span> <span data-ttu-id="efd42-107">Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="efd42-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
LVN_SETDISPINFO
        
    pdi = (NMLVDISPINFO*) lParam
```



## <a name="parameters"></a><span data-ttu-id="efd42-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="efd42-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="efd42-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="efd42-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="efd42-110">Pointeur vers une structure [**NMLVDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmlvdispinfoa) qui spécifie les informations relatives à l’élément modifié.</span><span class="sxs-lookup"><span data-stu-id="efd42-110">Pointer to an [**NMLVDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmlvdispinfoa) structure that specifies information for the changed item.</span></span> <span data-ttu-id="efd42-111">Le membre d' **élément** de cette structure est une structure [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) qui contient des informations sur l’élément qui a été modifié.</span><span class="sxs-lookup"><span data-stu-id="efd42-111">The **item** member of this structure is an [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) structure that contains information about the item that was changed.</span></span> <span data-ttu-id="efd42-112">Le membre **pszText** de l' **élément** contient une valeur valide, que l’indicateur de \_ texte LVIF soit défini ou non dans le membre de **masque** de cette structure.</span><span class="sxs-lookup"><span data-stu-id="efd42-112">The **pszText** member of **item** contains a valid value, regardless of whether the LVIF\_TEXT flag is set in the **mask** member of this structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="efd42-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="efd42-113">Return value</span></span>

<span data-ttu-id="efd42-114">Pas de valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="efd42-114">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="efd42-115">Notes</span><span class="sxs-lookup"><span data-stu-id="efd42-115">Remarks</span></span>

<span data-ttu-id="efd42-116">Le récepteur de notification convertit *lParam* pour récupérer la structure [**NMLVDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmlvdispinfoa) .</span><span class="sxs-lookup"><span data-stu-id="efd42-116">The notification receiver casts *lParam* to retrieve the [**NMLVDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmlvdispinfoa) structure.</span></span> <span data-ttu-id="efd42-117">Le paramètre *wParam* contient le code du message.</span><span class="sxs-lookup"><span data-stu-id="efd42-117">The *wParam* parameter contains the message code.</span></span>

## <a name="requirements"></a><span data-ttu-id="efd42-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="efd42-118">Requirements</span></span>



| <span data-ttu-id="efd42-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="efd42-119">Requirement</span></span> | <span data-ttu-id="efd42-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="efd42-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="efd42-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="efd42-121">Minimum supported client</span></span><br/> | <span data-ttu-id="efd42-122">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="efd42-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="efd42-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="efd42-123">Minimum supported server</span></span><br/> | <span data-ttu-id="efd42-124">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="efd42-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="efd42-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="efd42-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="efd42-126"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="efd42-126"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="efd42-127">Noms Unicode et ANSI</span><span class="sxs-lookup"><span data-stu-id="efd42-127">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="efd42-128">**LVN \_ SETDISPINFOW** (Unicode) et **LVN \_ SETDISPINFOA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="efd42-128">**LVN\_SETDISPINFOW** (Unicode) and **LVN\_SETDISPINFOA** (ANSI)</span></span><br/>           |



## <a name="see-also"></a><span data-ttu-id="efd42-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="efd42-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="efd42-130">LVN \_ GETDISPINFO</span><span class="sxs-lookup"><span data-stu-id="efd42-130">LVN\_GETDISPINFO</span></span>](lvn-getdispinfo.md)
</dt> </dl>

 

 





