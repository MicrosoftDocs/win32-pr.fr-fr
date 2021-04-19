---
description: Indique le nouveau domaine du lecteur DVD.
ms.assetid: 4faa46d6-2ba2-44a3-b237-acac3b32f8b1
title: EC_DVD_DOMAIN_CHANGE (Dvdevcode. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_DOMAIN_CHANGE
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: 815b6b2dd318d0b7716f4cf640ef3f83dacd0d60
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106520859"
---
# <a name="ec_dvd_domain_change"></a><span data-ttu-id="ee658-103">\_modification du \_ domaine du DVD EC \_</span><span class="sxs-lookup"><span data-stu-id="ee658-103">EC\_DVD\_DOMAIN\_CHANGE</span></span>

<span data-ttu-id="ee658-104">Indique le nouveau domaine du lecteur DVD.</span><span class="sxs-lookup"><span data-stu-id="ee658-104">Indicates the DVD player's new domain.</span></span>

## <a name="parameters"></a><span data-ttu-id="ee658-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ee658-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ee658-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="ee658-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="ee658-107">Valeur **DWORD** indiquant le nouveau domaine.</span><span class="sxs-lookup"><span data-stu-id="ee658-107">**DWORD** value indicating the new domain.</span></span> <span data-ttu-id="ee658-108">Membre du type de données énuméré du [**\_ domaine DVD**](/windows/win32/api/strmif/ne-strmif-dvd_domain) .</span><span class="sxs-lookup"><span data-stu-id="ee658-108">Member of the [**DVD\_DOMAIN**](/windows/win32/api/strmif/ne-strmif-dvd_domain) enumerated data type.</span></span>

</dd> <dt>

<span data-ttu-id="ee658-109"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="ee658-109"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="ee658-110">Zéro.</span><span class="sxs-lookup"><span data-stu-id="ee658-110">Zero.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ee658-111">Notes</span><span class="sxs-lookup"><span data-stu-id="ee658-111">Remarks</span></span>

<span data-ttu-id="ee658-112">Le lecteur DVD signale cet événement chaque fois qu’il modifie des domaines.</span><span class="sxs-lookup"><span data-stu-id="ee658-112">The DVD player signals this event whenever it changes domains.</span></span>

<span data-ttu-id="ee658-113">Cet événement est déclenché dans tous les domaines DVD.</span><span class="sxs-lookup"><span data-stu-id="ee658-113">This event is raised in all DVD domains.</span></span>

## <a name="requirements"></a><span data-ttu-id="ee658-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ee658-114">Requirements</span></span>



| <span data-ttu-id="ee658-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ee658-115">Requirement</span></span> | <span data-ttu-id="ee658-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="ee658-116">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ee658-117">En-tête</span><span class="sxs-lookup"><span data-stu-id="ee658-117">Header</span></span><br/> | <dl> <span data-ttu-id="ee658-118"><dt>Dvdevcode. h (inclure DShow. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ee658-118"><dt>Dvdevcode.h (include Dshow.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ee658-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ee658-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ee658-120">Applications DVD</span><span class="sxs-lookup"><span data-stu-id="ee658-120">DVD Applications</span></span>](dvd-applications.md)
</dt> <dt>

[<span data-ttu-id="ee658-121">Codes de notification des événements DVD</span><span class="sxs-lookup"><span data-stu-id="ee658-121">DVD Event Notification Codes</span></span>](dvd-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="ee658-122">Notification d’événement dans DirectShow</span><span class="sxs-lookup"><span data-stu-id="ee658-122">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




