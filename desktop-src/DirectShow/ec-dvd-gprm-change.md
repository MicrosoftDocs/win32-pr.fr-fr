---
description: Envoyé lorsque la valeur d’un registre de paramètres général (GPRM) change.
ms.assetid: 3e0c400e-9ea5-458c-9eca-97d66a440590
title: EC_DVD_GPRM_Change (Dvdevcode. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_GPRM_Change
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: f67a8646a72689c2570462f7dc4aeee6b2474136
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106538085"
---
# <a name="ec_dvd_gprm_change"></a><span data-ttu-id="930f7-103">\_Modification de \_ GPRM de DVD EC \_</span><span class="sxs-lookup"><span data-stu-id="930f7-103">EC\_DVD\_GPRM\_Change</span></span>

<span data-ttu-id="930f7-104">Envoyé lorsque la valeur d’un registre de paramètres général (GPRM) change.</span><span class="sxs-lookup"><span data-stu-id="930f7-104">Sent when the value of a general parameter register (GPRM) changes.</span></span>

## <a name="parameters"></a><span data-ttu-id="930f7-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="930f7-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="930f7-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="930f7-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="930f7-107">Index de base zéro de la valeur GPRM qui a changé.</span><span class="sxs-lookup"><span data-stu-id="930f7-107">The zero-based index of the GPRM value that changed.</span></span>

</dd> <dt>

<span data-ttu-id="930f7-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="930f7-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="930f7-109">Les 16 bits inférieurs contiennent la nouvelle valeur GPRM.</span><span class="sxs-lookup"><span data-stu-id="930f7-109">The lower 16 bits contains the new GPRM value.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="930f7-110">Notes</span><span class="sxs-lookup"><span data-stu-id="930f7-110">Remarks</span></span>

<span data-ttu-id="930f7-111">Cet événement est désactivé par défaut.</span><span class="sxs-lookup"><span data-stu-id="930f7-111">This event is disabled by default.</span></span> <span data-ttu-id="930f7-112">Pour activer cet événement, appelez [**IDvdControl2 :: SetOption**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-setoption) et affectez à l’option **DVD \_ EnableLoggingEvents** la **valeur true**.</span><span class="sxs-lookup"><span data-stu-id="930f7-112">To enable this event, call [**IDvdControl2::SetOption**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-setoption) and set the **DVD\_EnableLoggingEvents** option to **TRUE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="930f7-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="930f7-113">Requirements</span></span>



| <span data-ttu-id="930f7-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="930f7-114">Requirement</span></span> | <span data-ttu-id="930f7-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="930f7-115">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="930f7-116">En-tête</span><span class="sxs-lookup"><span data-stu-id="930f7-116">Header</span></span><br/> | <dl> <span data-ttu-id="930f7-117"><dt>Dvdevcode. h (inclure DShow. h)</dt></span><span class="sxs-lookup"><span data-stu-id="930f7-117"><dt>Dvdevcode.h (include Dshow.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="930f7-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="930f7-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="930f7-119">Applications DVD</span><span class="sxs-lookup"><span data-stu-id="930f7-119">DVD Applications</span></span>](dvd-applications.md)
</dt> <dt>

[<span data-ttu-id="930f7-120">Codes de notification des événements DVD</span><span class="sxs-lookup"><span data-stu-id="930f7-120">DVD Event Notification Codes</span></span>](dvd-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="930f7-121">Notification d’événement dans DirectShow</span><span class="sxs-lookup"><span data-stu-id="930f7-121">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> <dt>

[<span data-ttu-id="930f7-122">**IDvdInfo2::GetAllGPRMs**</span><span class="sxs-lookup"><span data-stu-id="930f7-122">**IDvdInfo2::GetAllGPRMs**</span></span>](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getallgprms)
</dt> </dl>

 

 




