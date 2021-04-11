---
title: MCN_SELCHANGE le code de notification (commctrl. h)
description: Envoyé par un contrôle Month Calendar lorsque la date ou la plage de dates actuellement sélectionnée change. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: 8923524f-d257-409d-bd3e-021684b88856
keywords:
- Contrôles Windows de code de notification MCN_SELCHANGE
topic_type:
- apiref
api_name:
- MCN_SELCHANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ffa328ca0173afd3a577f6cf14e0204cd5c0f7d5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032492"
---
# <a name="mcn_selchange-notification-code"></a><span data-ttu-id="f2681-105">\_Code de notification MCN selChange</span><span class="sxs-lookup"><span data-stu-id="f2681-105">MCN\_SELCHANGE notification code</span></span>

<span data-ttu-id="f2681-106">Envoyé par un contrôle Month Calendar lorsque la date ou la plage de dates actuellement sélectionnée change.</span><span class="sxs-lookup"><span data-stu-id="f2681-106">Sent by a month calendar control when the currently selected date or range of dates changes.</span></span> <span data-ttu-id="f2681-107">Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="f2681-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
MCN_SELCHANGE

    lpNMSelChange = (LPNMSELCHANGE) lParam;
```



## <a name="parameters"></a><span data-ttu-id="f2681-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f2681-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f2681-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f2681-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f2681-110">Pointeur vers une structure [**NMSELCHANGE**](/windows/win32/api/commctrl/ns-commctrl-nmselchange) qui contient des informations sur la plage de dates actuellement sélectionnée.</span><span class="sxs-lookup"><span data-stu-id="f2681-110">Pointer to an [**NMSELCHANGE**](/windows/win32/api/commctrl/ns-commctrl-nmselchange) structure that contains information about the currently selected date range.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f2681-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="f2681-111">Return value</span></span>

<span data-ttu-id="f2681-112">Pas de valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="f2681-112">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f2681-113">Notes</span><span class="sxs-lookup"><span data-stu-id="f2681-113">Remarks</span></span>

<span data-ttu-id="f2681-114">Par exemple, le contrôle envoie MCN \_ selChange lorsque l’utilisateur modifie explicitement la sélection dans le mois en cours ou lorsque la sélection est implicitement modifiée en réponse à la navigation vers le mois suivant/précédent.</span><span class="sxs-lookup"><span data-stu-id="f2681-114">For example, the control sends MCN\_SELCHANGE when the user explicitly changes the selection within the current month or when the selection is implicitly changed in response to next/previous month navigation.</span></span> <span data-ttu-id="f2681-115">Ce code de notification est également envoyé par le système à intervalles réguliers afin que le contrôle puisse répondre aux modifications de date.</span><span class="sxs-lookup"><span data-stu-id="f2681-115">This notification code is also sent by the system at regular intervals so that the control can respond to date changes.</span></span>

<span data-ttu-id="f2681-116">Ce code de notification est similaire à [MCN \_ Select](mcn-select.md), mais il est envoyé en réponse à toute modification de sélection.</span><span class="sxs-lookup"><span data-stu-id="f2681-116">This notification code is similar to [MCN\_SELECT](mcn-select.md), but it is sent in response to any selection change.</span></span> <span data-ttu-id="f2681-117">MCN \_ Select est envoyé uniquement pour une sélection de date explicite.</span><span class="sxs-lookup"><span data-stu-id="f2681-117">MCN\_SELECT is sent only for an explicit date selection.</span></span>

## <a name="requirements"></a><span data-ttu-id="f2681-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f2681-118">Requirements</span></span>



| <span data-ttu-id="f2681-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f2681-119">Requirement</span></span> | <span data-ttu-id="f2681-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="f2681-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f2681-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f2681-121">Minimum supported client</span></span><br/> | <span data-ttu-id="f2681-122">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f2681-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="f2681-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f2681-123">Minimum supported server</span></span><br/> | <span data-ttu-id="f2681-124">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f2681-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f2681-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="f2681-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="f2681-126"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="f2681-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





