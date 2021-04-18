---
description: Envoyé lorsque l’exlocateur VMR-7's a appelé la méthode de retournement DirectDraw sur la surface qui est présentée. Cela permet à VMR de conserver sa table de surfaces DirectXVA synchronisée avec la chaîne de retournement de DirectDraw.
ms.assetid: e298857b-0579-48b4-add0-72320bc52d63
title: EC_VMR_SURFACE_FLIPPED (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1feafaa58f0cacdafde04591d494dbb9a9eb258e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526740"
---
# <a name="ec_vmr_surface_flipped"></a><span data-ttu-id="f7530-104">\_surface EC \_ VMR \_ retournée</span><span class="sxs-lookup"><span data-stu-id="f7530-104">EC\_VMR\_SURFACE\_FLIPPED</span></span>

<span data-ttu-id="f7530-105">Envoyé lorsque l’exlocateur VMR-7's a appelé la méthode de retournement DirectDraw sur la surface qui est présentée.</span><span class="sxs-lookup"><span data-stu-id="f7530-105">Sent when the VMR-7's allocator presenter has called the DirectDraw Flip method on the surface being presented.</span></span> <span data-ttu-id="f7530-106">Cela permet à VMR de conserver sa table de surfaces DirectXVA synchronisée avec la chaîne de retournement de DirectDraw.</span><span class="sxs-lookup"><span data-stu-id="f7530-106">This allows the VMR to keep its DirectXVA table of surfaces synchronized with DirectDraw's flipping chain.</span></span>

## <a name="parameters"></a><span data-ttu-id="f7530-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f7530-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f7530-108"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="f7530-108"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="f7530-109">(**HRESULT**) Code d’état retourné par la méthode de retournement DirectDraw.</span><span class="sxs-lookup"><span data-stu-id="f7530-109">(**HRESULT**) Status code returned from the DirectDraw Flip method.</span></span>

</dd> <dt>

<span data-ttu-id="f7530-110"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="f7530-110"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="f7530-111">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="f7530-111">Not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f7530-112">Notes</span><span class="sxs-lookup"><span data-stu-id="f7530-112">Remarks</span></span>

<span data-ttu-id="f7530-113">Les exlocateurs personnalisés-présentateurs pour VMR-7 doivent envoyer cet événement.</span><span class="sxs-lookup"><span data-stu-id="f7530-113">Custom allocator-presenters for the VMR-7 should send this event.</span></span> <span data-ttu-id="f7530-114">Cet événement n’est pas transféré aux applications et n’est pas utilisé avec Allocator-Presenters pour VMR-9.</span><span class="sxs-lookup"><span data-stu-id="f7530-114">This event is not forwarded to applications and it is not used with allocator-presenters for the VMR-9.</span></span>

## <a name="requirements"></a><span data-ttu-id="f7530-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f7530-115">Requirements</span></span>



| <span data-ttu-id="f7530-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f7530-116">Requirement</span></span> | <span data-ttu-id="f7530-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="f7530-117">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="f7530-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="f7530-118">Header</span></span><br/> | <dl> <span data-ttu-id="f7530-119"><dt>DShow. h</dt></span><span class="sxs-lookup"><span data-stu-id="f7530-119"><dt>Dshow.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f7530-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f7530-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f7530-121">Codes de notification d’événement</span><span class="sxs-lookup"><span data-stu-id="f7530-121">Event Notification Codes</span></span>](event-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="f7530-122">Notification d’événement dans DirectShow</span><span class="sxs-lookup"><span data-stu-id="f7530-122">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




