---
description: Signale qu’une modification de la vitesse de lecture du DVD a été lancée.
ms.assetid: 2a1e3c21-1623-4e43-8c7b-1a34514442c9
title: EC_DVD_PLAYBACK_RATE_CHANGE (Dvdevcode. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_PLAYBACK_RATE_CHANGE
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: 20ddc41fd70906fabc522daa4dcb7714b71e4251
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537442"
---
# <a name="ec_dvd_playback_rate_change"></a><span data-ttu-id="de7b4-103">\_changement du \_ taux de lecture des DVD EC \_ \_</span><span class="sxs-lookup"><span data-stu-id="de7b4-103">EC\_DVD\_PLAYBACK\_RATE\_CHANGE</span></span>

<span data-ttu-id="de7b4-104">Signale qu’une modification de la vitesse de lecture du DVD a été lancée.</span><span class="sxs-lookup"><span data-stu-id="de7b4-104">Signals that a rate change in DVD playback has been initiated.</span></span>

## <a name="parameters"></a><span data-ttu-id="de7b4-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="de7b4-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="de7b4-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="de7b4-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="de7b4-107">Valeur de type LONG indiquant le nouveau taux de lecture.</span><span class="sxs-lookup"><span data-stu-id="de7b4-107">LONG indicating the new playback rate.</span></span> <span data-ttu-id="de7b4-108">La valeur est la vitesse de lecture réelle multipliée par 10 000, donc la vitesse de lecture est égale à 10000,0/ *lParam1*.</span><span class="sxs-lookup"><span data-stu-id="de7b4-108">The value is the actual playback rate multiplied by 10,000, so the playback rate equals 10000.0 / *lParam1*.</span></span> <span data-ttu-id="de7b4-109">Les valeurs inférieures à zéro indiquent le mode de lecture inversée, tandis que les valeurs supérieures à zéro indiquent le mode de lecture en avant.</span><span class="sxs-lookup"><span data-stu-id="de7b4-109">Values less than zero indicate reverse playback mode, and values greater than zero indicate forward playback mode.</span></span>

</dd> <dt>

<span data-ttu-id="de7b4-110"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="de7b4-110"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="de7b4-111">Zéro.</span><span class="sxs-lookup"><span data-stu-id="de7b4-111">Zero.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="de7b4-112">Notes</span><span class="sxs-lookup"><span data-stu-id="de7b4-112">Remarks</span></span>

<span data-ttu-id="de7b4-113">Cet événement est déclenché dans le domaine de titre.</span><span class="sxs-lookup"><span data-stu-id="de7b4-113">This event is raised in the title domain.</span></span>

<span data-ttu-id="de7b4-114">La *Vitesse* de lecture est l’inverse de la vitesse *de lecture.*</span><span class="sxs-lookup"><span data-stu-id="de7b4-114">Playback *rate* is the inverse of playback *speed*.</span></span> <span data-ttu-id="de7b4-115">Par exemple, si la vitesse de lecture est 2x, le taux est de 0,5.</span><span class="sxs-lookup"><span data-stu-id="de7b4-115">For example, if playback speed is 2x, the rate is 0.5.</span></span>

## <a name="requirements"></a><span data-ttu-id="de7b4-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="de7b4-116">Requirements</span></span>



| <span data-ttu-id="de7b4-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="de7b4-117">Requirement</span></span> | <span data-ttu-id="de7b4-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="de7b4-118">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="de7b4-119">En-tête</span><span class="sxs-lookup"><span data-stu-id="de7b4-119">Header</span></span><br/> | <dl> <span data-ttu-id="de7b4-120"><dt>Dvdevcode. h (inclure DShow. h)</dt></span><span class="sxs-lookup"><span data-stu-id="de7b4-120"><dt>Dvdevcode.h (include Dshow.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="de7b4-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="de7b4-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="de7b4-122">Applications DVD</span><span class="sxs-lookup"><span data-stu-id="de7b4-122">DVD Applications</span></span>](dvd-applications.md)
</dt> <dt>

[<span data-ttu-id="de7b4-123">Codes de notification des événements DVD</span><span class="sxs-lookup"><span data-stu-id="de7b4-123">DVD Event Notification Codes</span></span>](dvd-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="de7b4-124">Notification d’événement dans DirectShow</span><span class="sxs-lookup"><span data-stu-id="de7b4-124">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




