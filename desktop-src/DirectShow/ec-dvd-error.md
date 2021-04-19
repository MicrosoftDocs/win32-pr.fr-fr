---
description: Signale une condition d’erreur de DVD.
ms.assetid: 2cd3e0c4-e2b7-4aa1-9f3c-9003eabfb08a
title: EC_DVD_ERROR (Dvdevcode. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_ERROR
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: 3b338889836bf78a334784ea66c0e346e9f6b672
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106523961"
---
# <a name="ec_dvd_error"></a><span data-ttu-id="24c3a-103">\_erreur de DVD EC \_</span><span class="sxs-lookup"><span data-stu-id="24c3a-103">EC\_DVD\_ERROR</span></span>

<span data-ttu-id="24c3a-104">Signale une condition d’erreur de DVD.</span><span class="sxs-lookup"><span data-stu-id="24c3a-104">Signals a DVD error condition.</span></span>

## <a name="parameters"></a><span data-ttu-id="24c3a-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="24c3a-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="24c3a-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="24c3a-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="24c3a-107">Valeur **DWORD** indiquant la condition d’erreur.</span><span class="sxs-lookup"><span data-stu-id="24c3a-107">**DWORD** value indicating the error condition.</span></span> <span data-ttu-id="24c3a-108">Membre du type de données énumérées de l' [**\_ erreur DVD**](/previous-versions/windows/desktop/api/dvdevcod/ne-dvdevcod-dvd_error) .</span><span class="sxs-lookup"><span data-stu-id="24c3a-108">Member of the [**DVD\_ERROR**](/previous-versions/windows/desktop/api/dvdevcod/ne-dvdevcod-dvd_error) enumerated data type.</span></span>

</dd> <dt>

<span data-ttu-id="24c3a-109"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="24c3a-109"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="24c3a-110">La signification dépend de la valeur de *lParam1*.</span><span class="sxs-lookup"><span data-stu-id="24c3a-110">Meaning depends on the value of *lParam1*.</span></span> <span data-ttu-id="24c3a-111">Pour plus d’informations, consultez [**\_ erreur de DVD**](/previous-versions/windows/desktop/api/dvdevcod/ne-dvdevcod-dvd_error) .</span><span class="sxs-lookup"><span data-stu-id="24c3a-111">See [**DVD\_ERROR**](/previous-versions/windows/desktop/api/dvdevcod/ne-dvdevcod-dvd_error) for more information.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="24c3a-112">Notes</span><span class="sxs-lookup"><span data-stu-id="24c3a-112">Remarks</span></span>

<span data-ttu-id="24c3a-113">Cet événement est déclenché dans tous les domaines.</span><span class="sxs-lookup"><span data-stu-id="24c3a-113">This event is raised in all domains.</span></span>

## <a name="requirements"></a><span data-ttu-id="24c3a-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="24c3a-114">Requirements</span></span>



| <span data-ttu-id="24c3a-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="24c3a-115">Requirement</span></span> | <span data-ttu-id="24c3a-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="24c3a-116">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="24c3a-117">En-tête</span><span class="sxs-lookup"><span data-stu-id="24c3a-117">Header</span></span><br/> | <dl> <span data-ttu-id="24c3a-118"><dt>Dvdevcode. h (inclure DShow. h)</dt></span><span class="sxs-lookup"><span data-stu-id="24c3a-118"><dt>Dvdevcode.h (include Dshow.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="24c3a-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="24c3a-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="24c3a-120">Applications DVD</span><span class="sxs-lookup"><span data-stu-id="24c3a-120">DVD Applications</span></span>](dvd-applications.md)
</dt> <dt>

[<span data-ttu-id="24c3a-121">Codes de notification des événements DVD</span><span class="sxs-lookup"><span data-stu-id="24c3a-121">DVD Event Notification Codes</span></span>](dvd-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="24c3a-122">Notification d’événement dans DirectShow</span><span class="sxs-lookup"><span data-stu-id="24c3a-122">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




