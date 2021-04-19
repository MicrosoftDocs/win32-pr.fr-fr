---
description: Envoyé lorsque le navigateur DVD traite une commande de navigation sur DVD.
ms.assetid: 95e502b6-330f-4bc7-8adc-851913987370
title: EC_DVD_NavigationCommand (Dvdevcode. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_NavigationCommand
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: e81dbf108868cbaec4c44a436f2c8271bb5f282a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537444"
---
# <a name="ec_dvd_navigationcommand"></a><span data-ttu-id="640cf-103">\_NavigationCommand de DVD EC \_</span><span class="sxs-lookup"><span data-stu-id="640cf-103">EC\_DVD\_NavigationCommand</span></span>

<span data-ttu-id="640cf-104">Envoyé lorsque le [navigateur DVD](dvd-navigator-filter.md) traite une commande de navigation sur DVD.</span><span class="sxs-lookup"><span data-stu-id="640cf-104">Sent when the [DVD Navigator](dvd-navigator-filter.md) processes a DVD navigation command.</span></span>

## <a name="parameters"></a><span data-ttu-id="640cf-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="640cf-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="640cf-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="640cf-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="640cf-107">32 bits inférieurs de la commande de navigation brute.</span><span class="sxs-lookup"><span data-stu-id="640cf-107">The lower 32 bits of the raw navigation command.</span></span>

</dd> <dt>

<span data-ttu-id="640cf-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="640cf-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="640cf-109">32 bits supérieurs de la commande de navigation brute.</span><span class="sxs-lookup"><span data-stu-id="640cf-109">The upper 32 bits of the raw navigation command.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="640cf-110">Notes</span><span class="sxs-lookup"><span data-stu-id="640cf-110">Remarks</span></span>

<span data-ttu-id="640cf-111">Cet événement est désactivé par défaut.</span><span class="sxs-lookup"><span data-stu-id="640cf-111">This event is disabled by default.</span></span> <span data-ttu-id="640cf-112">Pour activer cet événement, appelez [**IDvdControl2 :: SetOption**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-setoption) et affectez à l’option **DVD \_ EnableLoggingEvents** la **valeur true**.</span><span class="sxs-lookup"><span data-stu-id="640cf-112">To enable this event, call [**IDvdControl2::SetOption**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-setoption) and set the **DVD\_EnableLoggingEvents** option to **TRUE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="640cf-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="640cf-113">Requirements</span></span>



| <span data-ttu-id="640cf-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="640cf-114">Requirement</span></span> | <span data-ttu-id="640cf-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="640cf-115">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="640cf-116">En-tête</span><span class="sxs-lookup"><span data-stu-id="640cf-116">Header</span></span><br/> | <dl> <span data-ttu-id="640cf-117"><dt>Dvdevcode. h (inclure DShow. h)</dt></span><span class="sxs-lookup"><span data-stu-id="640cf-117"><dt>Dvdevcode.h (include Dshow.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="640cf-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="640cf-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="640cf-119">Applications DVD</span><span class="sxs-lookup"><span data-stu-id="640cf-119">DVD Applications</span></span>](dvd-applications.md)
</dt> <dt>

[<span data-ttu-id="640cf-120">Codes de notification des événements DVD</span><span class="sxs-lookup"><span data-stu-id="640cf-120">DVD Event Notification Codes</span></span>](dvd-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="640cf-121">Notification d’événement dans DirectShow</span><span class="sxs-lookup"><span data-stu-id="640cf-121">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




