---
description: Signale que le lecteur de DVD a commencé la lecture d’un nouveau programme dans le \_ domaine du nom du domaine DVD \_ .
ms.assetid: c0745615-d527-4d93-9118-30419c6c811e
title: EC_DVD_CHAPTER_START (Dvdevcode. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_CHAPTER_START
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: 87a4408f1631d8a23cf42e790688856d6c246393
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106543586"
---
# <a name="ec_dvd_chapter_start"></a><span data-ttu-id="35b7b-103">\_début du \_ chapitre du DVD EC \_</span><span class="sxs-lookup"><span data-stu-id="35b7b-103">EC\_DVD\_CHAPTER\_START</span></span>

<span data-ttu-id="35b7b-104">Signale que le lecteur de DVD a commencé la lecture d’un nouveau programme dans le \_ domaine du nom du domaine DVD \_ .</span><span class="sxs-lookup"><span data-stu-id="35b7b-104">Signals that the DVD player started playback of a new program in the DVD\_DOMAIN\_Title domain.</span></span>

## <a name="parameters"></a><span data-ttu-id="35b7b-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="35b7b-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="35b7b-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="35b7b-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="35b7b-107">Valeur **DWORD** indiquant le nouveau numéro de chapitre (programme).</span><span class="sxs-lookup"><span data-stu-id="35b7b-107">**DWORD** value indicating the new chapter (program) number.</span></span>

</dd> <dt>

<span data-ttu-id="35b7b-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="35b7b-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="35b7b-109">Zéro.</span><span class="sxs-lookup"><span data-stu-id="35b7b-109">Zero.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="35b7b-110">Notes</span><span class="sxs-lookup"><span data-stu-id="35b7b-110">Remarks</span></span>

<span data-ttu-id="35b7b-111">Seuls les films linéaires simples signalent cet événement.</span><span class="sxs-lookup"><span data-stu-id="35b7b-111">Only simple linear movies signal this event.</span></span>

<span data-ttu-id="35b7b-112">Cet événement est déclenché dans le domaine de titre.</span><span class="sxs-lookup"><span data-stu-id="35b7b-112">This event is raised in the title domain.</span></span>

## <a name="requirements"></a><span data-ttu-id="35b7b-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="35b7b-113">Requirements</span></span>



| <span data-ttu-id="35b7b-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="35b7b-114">Requirement</span></span> | <span data-ttu-id="35b7b-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="35b7b-115">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="35b7b-116">En-tête</span><span class="sxs-lookup"><span data-stu-id="35b7b-116">Header</span></span><br/> | <dl> <span data-ttu-id="35b7b-117"><dt>Dvdevcode. h (inclure DShow. h)</dt></span><span class="sxs-lookup"><span data-stu-id="35b7b-117"><dt>Dvdevcode.h (include Dshow.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="35b7b-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="35b7b-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="35b7b-119">Applications DVD</span><span class="sxs-lookup"><span data-stu-id="35b7b-119">DVD Applications</span></span>](dvd-applications.md)
</dt> <dt>

[<span data-ttu-id="35b7b-120">Codes de notification des événements DVD</span><span class="sxs-lookup"><span data-stu-id="35b7b-120">DVD Event Notification Codes</span></span>](dvd-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="35b7b-121">Notification d’événement dans DirectShow</span><span class="sxs-lookup"><span data-stu-id="35b7b-121">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> <dt>

[<span data-ttu-id="35b7b-122">**\_Énumération de domaine DVD**</span><span class="sxs-lookup"><span data-stu-id="35b7b-122">**DVD\_DOMAIN Enumeration**</span></span>](/windows/win32/api/strmif/ne-strmif-dvd_domain)
</dt> </dl>

 

 




