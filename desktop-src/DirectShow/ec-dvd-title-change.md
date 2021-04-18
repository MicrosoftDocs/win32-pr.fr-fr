---
description: Indique quand le numéro de titre du DVD actuel change.
ms.assetid: 9888f2ec-fc2d-4d6d-a03d-b381373337eb
title: EC_DVD_TITLE_CHANGE (Dvdevcode. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_TITLE_CHANGE
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: 9539d29704797b1c7b001d426250762d2ed27b3e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106525993"
---
# <a name="ec_dvd_title_change"></a><span data-ttu-id="29610-103">\_modification du \_ titre du DVD EC \_</span><span class="sxs-lookup"><span data-stu-id="29610-103">EC\_DVD\_TITLE\_CHANGE</span></span>

<span data-ttu-id="29610-104">Indique quand le numéro de titre du DVD actuel change.</span><span class="sxs-lookup"><span data-stu-id="29610-104">Indicates when the current DVD title number changes.</span></span>

## <a name="parameters"></a><span data-ttu-id="29610-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="29610-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="29610-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="29610-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="29610-107">Valeur **DWORD** indiquant le nouveau numéro de titre.</span><span class="sxs-lookup"><span data-stu-id="29610-107">**DWORD** value indicating the new title number.</span></span>

</dd> <dt>

<span data-ttu-id="29610-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="29610-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="29610-109">Zéro.</span><span class="sxs-lookup"><span data-stu-id="29610-109">Zero.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="29610-110">Notes</span><span class="sxs-lookup"><span data-stu-id="29610-110">Remarks</span></span>

<span data-ttu-id="29610-111">Les numéros de titres vont de 1 à 99.</span><span class="sxs-lookup"><span data-stu-id="29610-111">Title numbers range from 1 to 99.</span></span> <span data-ttu-id="29610-112">Ce nombre indique le TTN, qui est le numéro de titre par rapport à l’ensemble du disque, et non le \_ ttn STM qui est le numéro de titre par rapport à un STM en cours.</span><span class="sxs-lookup"><span data-stu-id="29610-112">This number indicates the TTN, which is the title number with respect to the whole disc, not the VTS\_TTN which is the title number with respect to just a current VTS.</span></span>

<span data-ttu-id="29610-113">Cet événement est déclenché dans le domaine de titre.</span><span class="sxs-lookup"><span data-stu-id="29610-113">This event is raised in the title domain.</span></span>

## <a name="requirements"></a><span data-ttu-id="29610-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="29610-114">Requirements</span></span>



| <span data-ttu-id="29610-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="29610-115">Requirement</span></span> | <span data-ttu-id="29610-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="29610-116">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="29610-117">En-tête</span><span class="sxs-lookup"><span data-stu-id="29610-117">Header</span></span><br/> | <dl> <span data-ttu-id="29610-118"><dt>Dvdevcode. h (inclure DShow. h)</dt></span><span class="sxs-lookup"><span data-stu-id="29610-118"><dt>Dvdevcode.h (include Dshow.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="29610-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="29610-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="29610-120">Applications DVD</span><span class="sxs-lookup"><span data-stu-id="29610-120">DVD Applications</span></span>](dvd-applications.md)
</dt> <dt>

[<span data-ttu-id="29610-121">Codes de notification des événements DVD</span><span class="sxs-lookup"><span data-stu-id="29610-121">DVD Event Notification Codes</span></span>](dvd-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="29610-122">Notification d’événement dans DirectShow</span><span class="sxs-lookup"><span data-stu-id="29610-122">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




