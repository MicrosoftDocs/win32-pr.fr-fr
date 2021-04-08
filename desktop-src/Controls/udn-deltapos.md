---
title: UDN_DELTAPOS le code de notification (commctrl. h)
description: Envoyé par le système d’exploitation à la fenêtre parente d’un contrôle up-up lorsque la position du contrôle est sur le point d’être modifiée.
ms.assetid: 66262566-d35a-4b2a-8157-d1e789a21016
keywords:
- Contrôles Windows de code de notification UDN_DELTAPOS
topic_type:
- apiref
api_name:
- UDN_DELTAPOS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dec8f0ec2200d1f18e48c068b581b42868db197b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741684"
---
# <a name="udn_deltapos-notification-code"></a><span data-ttu-id="4e3bc-104">\_Code de notification UDN DELTAPOS</span><span class="sxs-lookup"><span data-stu-id="4e3bc-104">UDN\_DELTAPOS notification code</span></span>

<span data-ttu-id="4e3bc-105">Envoyé par le système d’exploitation à la fenêtre parente d’un contrôle up-up lorsque la position du contrôle est sur le point d’être modifiée.</span><span class="sxs-lookup"><span data-stu-id="4e3bc-105">Sent by the operating system to the parent window of an up-down control when the position of the control is about to change.</span></span> <span data-ttu-id="4e3bc-106">Cela se produit lorsque l’utilisateur demande une modification de la valeur en appuyant sur la flèche haut ou bas du contrôle.</span><span class="sxs-lookup"><span data-stu-id="4e3bc-106">This happens when the user requests a change in the value by pressing the control's up or down arrow.</span></span> <span data-ttu-id="4e3bc-107">Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="4e3bc-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
UDN_DELTAPOS 

    lpnmud = (LPNMUPDOWN) lParam;
```



## <a name="parameters"></a><span data-ttu-id="4e3bc-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4e3bc-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4e3bc-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="4e3bc-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4e3bc-110">Pointeur vers une structure [**NMUPDOWN**](/windows/win32/api/commctrl/ns-commctrl-nmupdown) qui contient des informations sur la modification de la position.</span><span class="sxs-lookup"><span data-stu-id="4e3bc-110">Pointer to an [**NMUPDOWN**](/windows/win32/api/commctrl/ns-commctrl-nmupdown) structure that contains information about the position change.</span></span> <span data-ttu-id="4e3bc-111">Le membre **IPOS** de cette structure contient la position actuelle du contrôle.</span><span class="sxs-lookup"><span data-stu-id="4e3bc-111">The **iPos** member of this structure contains the current position of the control.</span></span> <span data-ttu-id="4e3bc-112">Le membre **iDelta** de la structure est un entier signé qui contient la modification de position proposée.</span><span class="sxs-lookup"><span data-stu-id="4e3bc-112">The **iDelta** member of the structure is a signed integer that contains the proposed change in position.</span></span> <span data-ttu-id="4e3bc-113">Si l’utilisateur a cliqué sur le bouton haut, il s’agit d’une valeur positive.</span><span class="sxs-lookup"><span data-stu-id="4e3bc-113">If the user has clicked the up button, this is a positive value.</span></span> <span data-ttu-id="4e3bc-114">Si l’utilisateur a cliqué sur le bouton enfoncé, il s’agit d’une valeur négative.</span><span class="sxs-lookup"><span data-stu-id="4e3bc-114">If the user has clicked the down button, this is a negative value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4e3bc-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="4e3bc-115">Return value</span></span>

<span data-ttu-id="4e3bc-116">Retourne une valeur différente de zéro pour empêcher la modification de la position du contrôle, ou zéro pour autoriser la modification.</span><span class="sxs-lookup"><span data-stu-id="4e3bc-116">Return nonzero to prevent the change in the control's position, or zero to allow the change.</span></span>

## <a name="remarks"></a><span data-ttu-id="4e3bc-117">Notes</span><span class="sxs-lookup"><span data-stu-id="4e3bc-117">Remarks</span></span>

<span data-ttu-id="4e3bc-118">Le \_ Code de notification UDN DELTAPOS est envoyé avant le message [**WM \_ VSCROLL**](wm-vscroll.md) ou [**WM \_ HSCROLL**](wm-hscroll.md) , qui modifie en fait la position du contrôle.</span><span class="sxs-lookup"><span data-stu-id="4e3bc-118">The UDN\_DELTAPOS notification code is sent before the [**WM\_VSCROLL**](wm-vscroll.md) or [**WM\_HSCROLL**](wm-hscroll.md) message, which actually changes the control's position.</span></span> <span data-ttu-id="4e3bc-119">Cela vous permet d’examiner, d’autoriser, de modifier ou d’interdire la modification.</span><span class="sxs-lookup"><span data-stu-id="4e3bc-119">This lets you examine, allow, modify, or disallow the change.</span></span>

## <a name="requirements"></a><span data-ttu-id="4e3bc-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4e3bc-120">Requirements</span></span>



| <span data-ttu-id="4e3bc-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4e3bc-121">Requirement</span></span> | <span data-ttu-id="4e3bc-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="4e3bc-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="4e3bc-123">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4e3bc-123">Minimum supported client</span></span><br/> | <span data-ttu-id="4e3bc-124">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4e3bc-124">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="4e3bc-125">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4e3bc-125">Minimum supported server</span></span><br/> | <span data-ttu-id="4e3bc-126">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4e3bc-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="4e3bc-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="4e3bc-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="4e3bc-128"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="4e3bc-128"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4e3bc-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4e3bc-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4e3bc-130">**WM, \_ commande**</span><span class="sxs-lookup"><span data-stu-id="4e3bc-130">**WM\_COMMAND**</span></span>](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

