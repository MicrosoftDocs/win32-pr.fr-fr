---
description: Signale une condition d’avertissement de DVD.
ms.assetid: d7221e8a-089f-4eaf-a193-548709c14336
title: EC_DVD_WARNING (Dvdevcode. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_WARNING
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: 7f25d4565c2afeb4619f7832f6d5742e07dcca0c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540202"
---
# <a name="ec_dvd_warning"></a><span data-ttu-id="14aa7-103">\_avertissement de DVD EC \_</span><span class="sxs-lookup"><span data-stu-id="14aa7-103">EC\_DVD\_WARNING</span></span>

<span data-ttu-id="14aa7-104">Signale une condition d’avertissement de DVD.</span><span class="sxs-lookup"><span data-stu-id="14aa7-104">Signals a DVD warning condition.</span></span>

## <a name="parameters"></a><span data-ttu-id="14aa7-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="14aa7-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="14aa7-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="14aa7-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="14aa7-107">Valeur **DWORD** indiquant la condition d’avertissement.</span><span class="sxs-lookup"><span data-stu-id="14aa7-107">**DWORD** value indicating the warning condition.</span></span> <span data-ttu-id="14aa7-108">Membre du type de données énuméré de l' [**\_ Avertissement DVD**](/previous-versions/windows/desktop/api/dvdevcod/ne-dvdevcod-dvd_warning) .</span><span class="sxs-lookup"><span data-stu-id="14aa7-108">Member of the [**DVD\_WARNING**](/previous-versions/windows/desktop/api/dvdevcod/ne-dvdevcod-dvd_warning) enumerated data type.</span></span>

</dd> <dt>

<span data-ttu-id="14aa7-109"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="14aa7-109"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="14aa7-110">Si *pParam1* est égal à l' \_ Avertissement DVD \_ ouvert, à la recherche d’avertissement sur le DVD \_ \_ ou \_ à l’avertissement de DVD \_ lu, *LParam2* contient le dernier code d’erreur retourné par **GetLastError**.</span><span class="sxs-lookup"><span data-stu-id="14aa7-110">If *pParam1* equals DVD\_WARNING\_Open, DVD\_WARNING\_Seek, or DVD\_WARNING\_Read, then *lParam2* contains the last error code returned from **GetLastError**.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="14aa7-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="14aa7-111">Requirements</span></span>



| <span data-ttu-id="14aa7-112">Condition requise</span><span class="sxs-lookup"><span data-stu-id="14aa7-112">Requirement</span></span> | <span data-ttu-id="14aa7-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="14aa7-113">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="14aa7-114">En-tête</span><span class="sxs-lookup"><span data-stu-id="14aa7-114">Header</span></span><br/> | <dl> <span data-ttu-id="14aa7-115"><dt>Dvdevcode. h (inclure DShow. h)</dt></span><span class="sxs-lookup"><span data-stu-id="14aa7-115"><dt>Dvdevcode.h (include Dshow.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="14aa7-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="14aa7-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="14aa7-117">Applications DVD</span><span class="sxs-lookup"><span data-stu-id="14aa7-117">DVD Applications</span></span>](dvd-applications.md)
</dt> <dt>

[<span data-ttu-id="14aa7-118">Codes de notification des événements DVD</span><span class="sxs-lookup"><span data-stu-id="14aa7-118">DVD Event Notification Codes</span></span>](dvd-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="14aa7-119">Notification d’événement dans DirectShow</span><span class="sxs-lookup"><span data-stu-id="14aa7-119">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




