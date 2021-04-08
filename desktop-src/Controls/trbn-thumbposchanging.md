---
title: TRBN_THUMBPOSCHANGING le code de notification (commctrl. h)
description: Indique que la position du curseur sur un TrackBar est modifiée. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: 0876e026-bc07-409d-b174-b97ed704fc11
keywords:
- Contrôles Windows de code de notification TRBN_THUMBPOSCHANGING
topic_type:
- apiref
api_name:
- TRBN_THUMBPOSCHANGING
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f23722b68f28a5157948ac6277858193366242fe
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "103953653"
---
# <a name="trbn_thumbposchanging-notification-code"></a><span data-ttu-id="642cb-105">\_Code de notification TRBN THUMBPOSCHANGING</span><span class="sxs-lookup"><span data-stu-id="642cb-105">TRBN\_THUMBPOSCHANGING notification code</span></span>

<span data-ttu-id="642cb-106">Indique que la position du curseur sur un TrackBar est modifiée.</span><span class="sxs-lookup"><span data-stu-id="642cb-106">Notifies that the thumb position on a trackbar is changing.</span></span> <span data-ttu-id="642cb-107">Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="642cb-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TRBN_THUMBPOSCHANGING

    lpNMTrbThumbPosChanging = (NMTRBTHUMBPOSCHANGING*) lParam;
```



## <a name="parameters"></a><span data-ttu-id="642cb-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="642cb-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="642cb-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="642cb-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="642cb-110">Pointeur vers une structure [**NMTRBTHUMBPOSCHANGING**](/windows/win32/api/commctrl/ns-commctrl-nmtrbthumbposchanging) .</span><span class="sxs-lookup"><span data-stu-id="642cb-110">Pointer to a [**NMTRBTHUMBPOSCHANGING**](/windows/win32/api/commctrl/ns-commctrl-nmtrbthumbposchanging) structure.</span></span> <span data-ttu-id="642cb-111">L’appelant est chargé d’allouer cette structure et de définir ses membres, y compris les membres de la structure [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) contenue.</span><span class="sxs-lookup"><span data-stu-id="642cb-111">The caller is responsible for allocating this structure and setting its members, including the members of the contained [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="642cb-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="642cb-112">Return value</span></span>

<span data-ttu-id="642cb-113">Retourne la **valeur true** pour empêcher le déplacement du curseur à la position spécifiée.</span><span class="sxs-lookup"><span data-stu-id="642cb-113">Return **TRUE** to prevent the thumb from moving to the specified position.</span></span>

## <a name="remarks"></a><span data-ttu-id="642cb-114">Notes</span><span class="sxs-lookup"><span data-stu-id="642cb-114">Remarks</span></span>

<span data-ttu-id="642cb-115">Envoyez cette notification aux clients qui n’écoutent pas les messages [**WM \_ HSCROLL**](wm-hscroll.md) ou [**WM \_ VSCROLL**](wm-vscroll.md) .</span><span class="sxs-lookup"><span data-stu-id="642cb-115">Send this notification to clients that do not listen for [**WM\_HSCROLL**](wm-hscroll.md) or [**WM\_VSCROLL**](wm-vscroll.md) messages.</span></span>

## <a name="requirements"></a><span data-ttu-id="642cb-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="642cb-116">Requirements</span></span>



| <span data-ttu-id="642cb-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="642cb-117">Requirement</span></span> | <span data-ttu-id="642cb-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="642cb-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="642cb-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="642cb-119">Minimum supported client</span></span><br/> | <span data-ttu-id="642cb-120">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="642cb-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="642cb-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="642cb-121">Minimum supported server</span></span><br/> | <span data-ttu-id="642cb-122">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="642cb-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="642cb-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="642cb-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="642cb-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="642cb-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





