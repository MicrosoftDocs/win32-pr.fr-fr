---
description: Envoyé lorsque la valeur d’un registre de paramètres système (SPRM) change.
ms.assetid: 266b6de1-740d-4b3d-8487-5a9570d6c852
title: EC_DVD_SPRM_Change (Dvdevcode. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_SPRM_Change
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: 1af5b8637a197973bca2129a8b8a0198d20248eb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106535890"
---
# <a name="ec_dvd_sprm_change"></a><span data-ttu-id="d62e7-103">\_Modification de \_ SPRM de DVD EC \_</span><span class="sxs-lookup"><span data-stu-id="d62e7-103">EC\_DVD\_SPRM\_Change</span></span>

<span data-ttu-id="d62e7-104">Envoyé lorsque la valeur d’un registre de paramètres système (SPRM) change.</span><span class="sxs-lookup"><span data-stu-id="d62e7-104">Sent when the value of a system parameter register (SPRM) changes.</span></span>

## <a name="parameters"></a><span data-ttu-id="d62e7-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d62e7-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d62e7-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="d62e7-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="d62e7-107">Index de base zéro de la valeur SPRM qui a changé.</span><span class="sxs-lookup"><span data-stu-id="d62e7-107">The zero-based index of the SPRM value that changed.</span></span>

</dd> <dt>

<span data-ttu-id="d62e7-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="d62e7-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="d62e7-109">Les 16 bits inférieurs contiennent la nouvelle valeur SPRM.</span><span class="sxs-lookup"><span data-stu-id="d62e7-109">The lower 16 bits contains the new SPRM value.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d62e7-110">Notes</span><span class="sxs-lookup"><span data-stu-id="d62e7-110">Remarks</span></span>

<span data-ttu-id="d62e7-111">Cet événement est désactivé par défaut.</span><span class="sxs-lookup"><span data-stu-id="d62e7-111">This event is disabled by default.</span></span> <span data-ttu-id="d62e7-112">Pour activer cet événement, appelez [**IDvdControl2 :: SetOption**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-setoption) et affectez à l’option **DVD \_ EnableLoggingEvents** la **valeur true**.</span><span class="sxs-lookup"><span data-stu-id="d62e7-112">To enable this event, call [**IDvdControl2::SetOption**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-setoption) and set the **DVD\_EnableLoggingEvents** option to **TRUE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="d62e7-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d62e7-113">Requirements</span></span>



| <span data-ttu-id="d62e7-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d62e7-114">Requirement</span></span> | <span data-ttu-id="d62e7-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="d62e7-115">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d62e7-116">En-tête</span><span class="sxs-lookup"><span data-stu-id="d62e7-116">Header</span></span><br/> | <dl> <span data-ttu-id="d62e7-117"><dt>Dvdevcode. h (inclure DShow. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d62e7-117"><dt>Dvdevcode.h (include Dshow.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d62e7-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d62e7-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d62e7-119">Applications DVD</span><span class="sxs-lookup"><span data-stu-id="d62e7-119">DVD Applications</span></span>](dvd-applications.md)
</dt> <dt>

[<span data-ttu-id="d62e7-120">Codes de notification des événements DVD</span><span class="sxs-lookup"><span data-stu-id="d62e7-120">DVD Event Notification Codes</span></span>](dvd-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="d62e7-121">Notification d’événement dans DirectShow</span><span class="sxs-lookup"><span data-stu-id="d62e7-121">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> <dt>

[<span data-ttu-id="d62e7-122">**IDvdInfo2::GetAllSPRMs**</span><span class="sxs-lookup"><span data-stu-id="d62e7-122">**IDvdInfo2::GetAllSPRMs**</span></span>](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getallsprms)
</dt> </dl>

 

 




