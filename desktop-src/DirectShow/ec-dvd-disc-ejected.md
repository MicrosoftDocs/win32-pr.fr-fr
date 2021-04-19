---
description: Signale qu’un disque DVD a été éjecté.
ms.assetid: 031156c2-f0f0-4a9e-b792-4d656ec49aef
title: EC_DVD_DISC_EJECTED (Dvdevcode. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_DISC_EJECTED
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: ab6c1333245b589d4f13bafcba89eada3ef98ab0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537479"
---
# <a name="ec_dvd_disc_ejected"></a><span data-ttu-id="c60ac-103">\_disque DVD d’EC \_ \_ éjecté</span><span class="sxs-lookup"><span data-stu-id="c60ac-103">EC\_DVD\_DISC\_EJECTED</span></span>

<span data-ttu-id="c60ac-104">Signale qu’un disque DVD a été éjecté.</span><span class="sxs-lookup"><span data-stu-id="c60ac-104">Signals that a DVD disc was ejected.</span></span>

## <a name="parameters"></a><span data-ttu-id="c60ac-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c60ac-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c60ac-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="c60ac-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="c60ac-107">Zéro.</span><span class="sxs-lookup"><span data-stu-id="c60ac-107">Zero.</span></span>

</dd> <dt>

<span data-ttu-id="c60ac-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="c60ac-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="c60ac-109">Zéro.</span><span class="sxs-lookup"><span data-stu-id="c60ac-109">Zero.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c60ac-110">Notes</span><span class="sxs-lookup"><span data-stu-id="c60ac-110">Remarks</span></span>

<span data-ttu-id="c60ac-111">La lecture s’arrête automatiquement lorsqu’un disque est éjecté.</span><span class="sxs-lookup"><span data-stu-id="c60ac-111">Playback automatically stops when a disc is ejected.</span></span> <span data-ttu-id="c60ac-112">L’application n’a pas besoin d’effectuer d’action particulière en réponse à cet événement.</span><span class="sxs-lookup"><span data-stu-id="c60ac-112">The application does not have to take any special action in response to this event.</span></span>

<span data-ttu-id="c60ac-113">Cet événement est déclenché dans tous les domaines.</span><span class="sxs-lookup"><span data-stu-id="c60ac-113">This event is raised in all domains.</span></span>

## <a name="requirements"></a><span data-ttu-id="c60ac-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c60ac-114">Requirements</span></span>



| <span data-ttu-id="c60ac-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c60ac-115">Requirement</span></span> | <span data-ttu-id="c60ac-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="c60ac-116">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c60ac-117">En-tête</span><span class="sxs-lookup"><span data-stu-id="c60ac-117">Header</span></span><br/> | <dl> <span data-ttu-id="c60ac-118"><dt>Dvdevcode. h (inclure DShow. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c60ac-118"><dt>Dvdevcode.h (include Dshow.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c60ac-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c60ac-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c60ac-120">Applications DVD</span><span class="sxs-lookup"><span data-stu-id="c60ac-120">DVD Applications</span></span>](dvd-applications.md)
</dt> <dt>

[<span data-ttu-id="c60ac-121">Codes de notification des événements DVD</span><span class="sxs-lookup"><span data-stu-id="c60ac-121">DVD Event Notification Codes</span></span>](dvd-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="c60ac-122">Notification d’événement dans DirectShow</span><span class="sxs-lookup"><span data-stu-id="c60ac-122">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




