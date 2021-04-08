---
title: Message RBN_AUTOBREAK (commctrl. h)
description: Avertit le parent d’un Rebar qu’un saut apparaîtra dans la barre. Le parent détermine s’il faut effectuer l’arrêt. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: b7a63027-6cfa-4d5a-9ea6-fdd8b4fb6864
keywords:
- RBN_AUTOBREAK les contrôles de message Windows
topic_type:
- apiref
api_name:
- RBN_AUTOBREAK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d614277d89578cb66e528ba16656ed55681ebbcf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103844338"
---
# <a name="rbn_autobreak-message"></a><span data-ttu-id="a6641-106">Message de coupure de RBN \_</span><span class="sxs-lookup"><span data-stu-id="a6641-106">RBN\_AUTOBREAK message</span></span>

<span data-ttu-id="a6641-107">Avertit le parent [d’un Rebar](rebar-controls.md) qu’un saut apparaîtra dans la barre.</span><span class="sxs-lookup"><span data-stu-id="a6641-107">Notifies a [rebar's](rebar-controls.md) parent that a break will appear in the bar.</span></span> <span data-ttu-id="a6641-108">Le parent détermine s’il faut effectuer l’arrêt.</span><span class="sxs-lookup"><span data-stu-id="a6641-108">The parent determines whether to make the break.</span></span> <span data-ttu-id="a6641-109">Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="a6641-109">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
RBN_AUTOBREAK

    pnmRebarAutoBreak = (LPNMREBARAUTOBREAK) lParam;
```



## <a name="parameters"></a><span data-ttu-id="a6641-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a6641-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a6641-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a6641-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a6641-112">Pointeur vers une structure [**NMREBARAUTOBREAK**](/windows/win32/api/commctrl/ns-commctrl-nmrebarautobreak) qui contient des informations sur le code de notification.</span><span class="sxs-lookup"><span data-stu-id="a6641-112">Pointer to a [**NMREBARAUTOBREAK**](/windows/win32/api/commctrl/ns-commctrl-nmrebarautobreak) structure that contains information about the notification code.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a6641-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="a6641-113">Return value</span></span>

<span data-ttu-id="a6641-114">La valeur de retour de cette notification n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="a6641-114">The return value for this notification is not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="a6641-115">Notes</span><span class="sxs-lookup"><span data-stu-id="a6641-115">Remarks</span></span>

<span data-ttu-id="a6641-116">La valeur du membre **fAutoBreak** de la structure [**NMREBARAUTOBREAK**](/windows/win32/api/commctrl/ns-commctrl-nmrebarautobreak) indique si un arrêt doit se produire dans le rebar.</span><span class="sxs-lookup"><span data-stu-id="a6641-116">The value in the **fAutoBreak** member of the [**NMREBARAUTOBREAK**](/windows/win32/api/commctrl/ns-commctrl-nmrebarautobreak) structure indicates whether a break should occur in the rebar.</span></span>

<span data-ttu-id="a6641-117">Pour utiliser ce code de notification, spécifiez Comctl32.dll version 6 dans le manifeste.</span><span class="sxs-lookup"><span data-stu-id="a6641-117">To use this notification code, specify Comctl32.dll version 6 in the manifest.</span></span> <span data-ttu-id="a6641-118">Pour plus d’informations sur les manifestes, consultez [activation des styles visuels](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="a6641-118">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="a6641-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a6641-119">Requirements</span></span>



| <span data-ttu-id="a6641-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a6641-120">Requirement</span></span> | <span data-ttu-id="a6641-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="a6641-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a6641-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a6641-122">Minimum supported client</span></span><br/> | <span data-ttu-id="a6641-123">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a6641-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="a6641-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a6641-124">Minimum supported server</span></span><br/> | <span data-ttu-id="a6641-125">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a6641-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="a6641-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="a6641-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="a6641-127"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="a6641-127"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





