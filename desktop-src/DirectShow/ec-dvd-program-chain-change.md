---
description: Envoyé lorsque la chaîne de programme active (PGC) est modifiée.
ms.assetid: 80fcd059-6ab4-4116-ac3a-012c451237b3
title: EC_DVD_PROGRAM_CHAIN_CHANGE (Dvdevcode. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_PROGRAM_CHAIN_CHANGE
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: eefd45ac1d147a0409417f215e56a4db490dfdbe
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106530469"
---
# <a name="ec_dvd_program_chain_change"></a><span data-ttu-id="891d2-103">\_changement de \_ chaîne du programme de DVD EC \_ \_</span><span class="sxs-lookup"><span data-stu-id="891d2-103">EC\_DVD\_PROGRAM\_CHAIN\_CHANGE</span></span>

<span data-ttu-id="891d2-104">Envoyé lorsque la chaîne de programme active (PGC) est modifiée.</span><span class="sxs-lookup"><span data-stu-id="891d2-104">Sent when current program chain (PGC) changes.</span></span>

## <a name="parameters"></a><span data-ttu-id="891d2-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="891d2-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="891d2-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="891d2-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="891d2-107">Nouveau numéro de chaîne de programme (PGCN).</span><span class="sxs-lookup"><span data-stu-id="891d2-107">The new program chain number (PGCN).</span></span>

</dd> <dt>

<span data-ttu-id="891d2-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="891d2-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="891d2-109">Identificateur de paramètres régionaux (LCID) de la langue audio.</span><span class="sxs-lookup"><span data-stu-id="891d2-109">The locale identifier (LCID) of the audio language.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="891d2-110">Notes</span><span class="sxs-lookup"><span data-stu-id="891d2-110">Remarks</span></span>

<span data-ttu-id="891d2-111">Cet événement est désactivé par défaut.</span><span class="sxs-lookup"><span data-stu-id="891d2-111">This event is disabled by default.</span></span> <span data-ttu-id="891d2-112">Pour activer cet événement, appelez [**IDvdControl2 :: SetOption**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-setoption) et affectez à l’option **DVD \_ NotifyPositionChange** la **valeur true**.</span><span class="sxs-lookup"><span data-stu-id="891d2-112">To enable this event, call [**IDvdControl2::SetOption**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-setoption) and set the **DVD\_NotifyPositionChange** option to **TRUE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="891d2-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="891d2-113">Requirements</span></span>



| <span data-ttu-id="891d2-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="891d2-114">Requirement</span></span> | <span data-ttu-id="891d2-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="891d2-115">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="891d2-116">En-tête</span><span class="sxs-lookup"><span data-stu-id="891d2-116">Header</span></span><br/> | <dl> <span data-ttu-id="891d2-117"><dt>Dvdevcode. h (inclure DShow. h)</dt></span><span class="sxs-lookup"><span data-stu-id="891d2-117"><dt>Dvdevcode.h (include Dshow.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="891d2-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="891d2-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="891d2-119">Applications DVD</span><span class="sxs-lookup"><span data-stu-id="891d2-119">DVD Applications</span></span>](dvd-applications.md)
</dt> <dt>

[<span data-ttu-id="891d2-120">Codes de notification des événements DVD</span><span class="sxs-lookup"><span data-stu-id="891d2-120">DVD Event Notification Codes</span></span>](dvd-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="891d2-121">Notification d’événement dans DirectShow</span><span class="sxs-lookup"><span data-stu-id="891d2-121">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




