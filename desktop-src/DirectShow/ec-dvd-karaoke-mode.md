---
description: Indique que le navigateur DVD a commencé à exécuter ou à terminer de relire les données karaoké.
ms.assetid: 910bf809-a56a-4d02-9c7e-429769a4ec2b
title: EC_DVD_KARAOKE_MODE (Dvdevcode. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_KARAOKE_MODE
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: fb83bc1de9c2933b53935c056b192eca74c4245c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106520858"
---
# <a name="ec_dvd_karaoke_mode"></a><span data-ttu-id="67c3b-103">\_ \_ mode karaoké du DVD EC \_</span><span class="sxs-lookup"><span data-stu-id="67c3b-103">EC\_DVD\_KARAOKE\_MODE</span></span>

<span data-ttu-id="67c3b-104">Indique que le [navigateur DVD](data-flow-in-the-dvd-navigator.md) a commencé à exécuter ou à terminer de relire les données karaoké.</span><span class="sxs-lookup"><span data-stu-id="67c3b-104">Indicates that the [DVD Navigator](data-flow-in-the-dvd-navigator.md) has either begun playing or finished playing karaoke data.</span></span>

## <a name="parameters"></a><span data-ttu-id="67c3b-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="67c3b-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="67c3b-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="67c3b-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="67c3b-107">Valeur booléenne.</span><span class="sxs-lookup"><span data-stu-id="67c3b-107">Boolean value.</span></span> <span data-ttu-id="67c3b-108">Si la **valeur est true**, une piste de karaoké est lue.</span><span class="sxs-lookup"><span data-stu-id="67c3b-108">If **TRUE**, a karaoke track is being played.</span></span> <span data-ttu-id="67c3b-109">Dans le cas contraire, aucune piste karaoké n’est lue.</span><span class="sxs-lookup"><span data-stu-id="67c3b-109">Otherwise, no karaoke track is being played.</span></span>

</dd> <dt>

<span data-ttu-id="67c3b-110"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="67c3b-110"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="67c3b-111">Réservé.</span><span class="sxs-lookup"><span data-stu-id="67c3b-111">Reserved.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="67c3b-112">Notes</span><span class="sxs-lookup"><span data-stu-id="67c3b-112">Remarks</span></span>

<span data-ttu-id="67c3b-113">Le lecteur DVD signale cet événement chaque fois qu’il modifie des domaines.</span><span class="sxs-lookup"><span data-stu-id="67c3b-113">The DVD player signals this event whenever it changes domains.</span></span>

<span data-ttu-id="67c3b-114">Cet événement est déclenché dans tous les domaines DVD.</span><span class="sxs-lookup"><span data-stu-id="67c3b-114">This event is raised in all DVD domains.</span></span>

## <a name="requirements"></a><span data-ttu-id="67c3b-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="67c3b-115">Requirements</span></span>



| <span data-ttu-id="67c3b-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="67c3b-116">Requirement</span></span> | <span data-ttu-id="67c3b-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="67c3b-117">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="67c3b-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="67c3b-118">Header</span></span><br/> | <dl> <span data-ttu-id="67c3b-119"><dt>Dvdevcode. h (inclure DShow. h)</dt></span><span class="sxs-lookup"><span data-stu-id="67c3b-119"><dt>Dvdevcode.h (include Dshow.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="67c3b-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="67c3b-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="67c3b-121">Applications DVD</span><span class="sxs-lookup"><span data-stu-id="67c3b-121">DVD Applications</span></span>](dvd-applications.md)
</dt> <dt>

[<span data-ttu-id="67c3b-122">Codes de notification des événements DVD</span><span class="sxs-lookup"><span data-stu-id="67c3b-122">DVD Event Notification Codes</span></span>](dvd-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="67c3b-123">Notification d’événement dans DirectShow</span><span class="sxs-lookup"><span data-stu-id="67c3b-123">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




