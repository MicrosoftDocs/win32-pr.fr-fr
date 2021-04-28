---
description: EC_DVD_VOBU_Timestamp-envoyé lorsque le navigateur DVD analyse un paquet PCI.
ms.assetid: 25548c23-22f0-47cb-9062-273ad39d3007
title: EC_DVD_VOBU_Timestamp (Dvdevcode. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_VOBU_Timestamp
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: 6bd06eb99cae60960db64a6f32df5e4c932b362f
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108094617"
---
# <a name="ec_dvd_vobu_timestamp"></a><span data-ttu-id="1d916-103">\_ \_ Horodatage VOBU de DVD EC \_</span><span class="sxs-lookup"><span data-stu-id="1d916-103">EC\_DVD\_VOBU\_Timestamp</span></span>

<span data-ttu-id="1d916-104">Envoyé lorsque le [navigateur DVD](dvd-navigator-filter.md) analyse un paquet PCI.</span><span class="sxs-lookup"><span data-stu-id="1d916-104">Sent when the [DVD Navigator](dvd-navigator-filter.md) parses a PCI packet.</span></span>

<span data-ttu-id="1d916-105">Les données d’événement sont l’horodatage de la dernière unité d’objet vidéo (VOBU).</span><span class="sxs-lookup"><span data-stu-id="1d916-105">The event data is the time stamp of the most recent video object unit (VOBU).</span></span>

## <a name="parameters"></a><span data-ttu-id="1d916-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1d916-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1d916-107"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="1d916-107"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="1d916-108">Contient le **DWORD** de poids faible de l’horodatage.</span><span class="sxs-lookup"><span data-stu-id="1d916-108">Contains the low-order **DWORD** of the time stamp.</span></span>

</dd> <dt>

<span data-ttu-id="1d916-109"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="1d916-109"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="1d916-110">Contient le **DWORD** de poids fort de l’horodatage.</span><span class="sxs-lookup"><span data-stu-id="1d916-110">Contains the high-order **DWORD** of the time stamp.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1d916-111">Notes </span><span class="sxs-lookup"><span data-stu-id="1d916-111">Remarks</span></span>

<span data-ttu-id="1d916-112">Cet événement est désactivé par défaut.</span><span class="sxs-lookup"><span data-stu-id="1d916-112">This event is disabled by default.</span></span> <span data-ttu-id="1d916-113">Pour activer cet événement, appelez [**IDvdControl2 :: SetOption**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-setoption) et affectez à l’option **DVD \_ EnableLoggingEvents** la **valeur true**.</span><span class="sxs-lookup"><span data-stu-id="1d916-113">To enable this event, call [**IDvdControl2::SetOption**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-setoption) and set the **DVD\_EnableLoggingEvents** option to **TRUE**.</span></span>

<span data-ttu-id="1d916-114">Reconstruisez l’horodatage comme suit :</span><span class="sxs-lookup"><span data-stu-id="1d916-114">Reconstruct the time stamp as follows:</span></span>


```C++
LARGE_INTEGER li;
li.LowPart = DWORD( lParam1 );
li.HighPart = DWORD( lParam2 );
```



## <a name="requirements"></a><span data-ttu-id="1d916-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1d916-115">Requirements</span></span>



| <span data-ttu-id="1d916-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1d916-116">Requirement</span></span> | <span data-ttu-id="1d916-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="1d916-117">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1d916-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="1d916-118">Header</span></span><br/> | <dl> <span data-ttu-id="1d916-119"><dt>Dvdevcode. h (inclure DShow. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1d916-119"><dt>Dvdevcode.h (include Dshow.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1d916-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1d916-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1d916-121">Applications DVD</span><span class="sxs-lookup"><span data-stu-id="1d916-121">DVD Applications</span></span>](dvd-applications.md)
</dt> <dt>

[<span data-ttu-id="1d916-122">Codes de notification des événements DVD</span><span class="sxs-lookup"><span data-stu-id="1d916-122">DVD Event Notification Codes</span></span>](dvd-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="1d916-123">Notification d’événement dans DirectShow</span><span class="sxs-lookup"><span data-stu-id="1d916-123">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




