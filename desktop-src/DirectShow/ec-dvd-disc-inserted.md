---
description: Signale qu’un disque DVD a été inséré dans le lecteur.
ms.assetid: ce233c94-2eae-457c-919b-7c4d8334979a
title: EC_DVD_DISC_INSERTED (Dvdevcode. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_DISC_INSERTED
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: c98d32960e2ab6a21633899164b3ff84525f2aaf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537478"
---
# <a name="ec_dvd_disc_inserted"></a><span data-ttu-id="89b0c-103">\_disque DVD-EC \_ \_ inséré</span><span class="sxs-lookup"><span data-stu-id="89b0c-103">EC\_DVD\_DISC\_INSERTED</span></span>

<span data-ttu-id="89b0c-104">Signale qu’un disque DVD a été inséré dans le lecteur.</span><span class="sxs-lookup"><span data-stu-id="89b0c-104">Signals that a DVD disc was inserted into the drive.</span></span>

## <a name="parameters"></a><span data-ttu-id="89b0c-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="89b0c-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="89b0c-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="89b0c-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="89b0c-107">Zéro.</span><span class="sxs-lookup"><span data-stu-id="89b0c-107">Zero.</span></span>

</dd> <dt>

<span data-ttu-id="89b0c-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="89b0c-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="89b0c-109">Zéro.</span><span class="sxs-lookup"><span data-stu-id="89b0c-109">Zero.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="89b0c-110">Notes</span><span class="sxs-lookup"><span data-stu-id="89b0c-110">Remarks</span></span>

<span data-ttu-id="89b0c-111">La lecture commence automatiquement lorsqu’un disque est inséré.</span><span class="sxs-lookup"><span data-stu-id="89b0c-111">Playback automatically begins when a disc is inserted.</span></span> <span data-ttu-id="89b0c-112">L’application n’a pas besoin d’effectuer d’action particulière en réponse à cet événement.</span><span class="sxs-lookup"><span data-stu-id="89b0c-112">The application does not have to take any special action in response to this event.</span></span>

<span data-ttu-id="89b0c-113">Cet événement est déclenché dans tous les domaines.</span><span class="sxs-lookup"><span data-stu-id="89b0c-113">This event is raised in all domains.</span></span>

## <a name="requirements"></a><span data-ttu-id="89b0c-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="89b0c-114">Requirements</span></span>



| <span data-ttu-id="89b0c-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="89b0c-115">Requirement</span></span> | <span data-ttu-id="89b0c-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="89b0c-116">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="89b0c-117">En-tête</span><span class="sxs-lookup"><span data-stu-id="89b0c-117">Header</span></span><br/> | <dl> <span data-ttu-id="89b0c-118"><dt>Dvdevcode. h (inclure DShow. h)</dt></span><span class="sxs-lookup"><span data-stu-id="89b0c-118"><dt>Dvdevcode.h (include Dshow.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="89b0c-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="89b0c-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="89b0c-120">Applications DVD</span><span class="sxs-lookup"><span data-stu-id="89b0c-120">DVD Applications</span></span>](dvd-applications.md)
</dt> <dt>

[<span data-ttu-id="89b0c-121">Codes de notification des événements DVD</span><span class="sxs-lookup"><span data-stu-id="89b0c-121">DVD Event Notification Codes</span></span>](dvd-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="89b0c-122">Notification d’événement dans DirectShow</span><span class="sxs-lookup"><span data-stu-id="89b0c-122">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




