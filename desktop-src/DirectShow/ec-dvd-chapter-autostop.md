---
description: Indique que la lecture du DVD s’est arrêtée à la suite d’un appel à la méthode IDvdControl2 ::P layChaptersAutoStop.
ms.assetid: ccafaf76-ec8c-4d67-9b29-565f3ed6593b
title: EC_DVD_CHAPTER_AUTOSTOP (Dvdevcode. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_CHAPTER_AUTOSTOP
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: 43e1414c0f9cee7e8daf37b87d5f0c3d0599a017
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106525579"
---
# <a name="ec_dvd_chapter_autostop"></a><span data-ttu-id="864cc-103">\_arrêt du \_ chapitre du DVD ce \_</span><span class="sxs-lookup"><span data-stu-id="864cc-103">EC\_DVD\_CHAPTER\_AUTOSTOP</span></span>

<span data-ttu-id="864cc-104">Indique que la lecture du DVD s’est arrêtée à la suite d’un appel à la méthode [**IDvdControl2 ::P laychaptersautostop**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-playchaptersautostop) .</span><span class="sxs-lookup"><span data-stu-id="864cc-104">Indicates that DVD playback stopped as the result of a call to the [**IDvdControl2::PlayChaptersAutoStop**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-playchaptersautostop) method.</span></span>

## <a name="parameters"></a><span data-ttu-id="864cc-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="864cc-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="864cc-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="864cc-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="864cc-107">Zéro.</span><span class="sxs-lookup"><span data-stu-id="864cc-107">Zero.</span></span>

</dd> <dt>

<span data-ttu-id="864cc-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="864cc-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="864cc-109">Zéro.</span><span class="sxs-lookup"><span data-stu-id="864cc-109">Zero.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="864cc-110">Notes</span><span class="sxs-lookup"><span data-stu-id="864cc-110">Remarks</span></span>

<span data-ttu-id="864cc-111">Cet événement est déclenché dans le domaine de titre.</span><span class="sxs-lookup"><span data-stu-id="864cc-111">This event is raised in the title domain.</span></span>

## <a name="requirements"></a><span data-ttu-id="864cc-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="864cc-112">Requirements</span></span>



| <span data-ttu-id="864cc-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="864cc-113">Requirement</span></span> | <span data-ttu-id="864cc-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="864cc-114">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="864cc-115">En-tête</span><span class="sxs-lookup"><span data-stu-id="864cc-115">Header</span></span><br/> | <dl> <span data-ttu-id="864cc-116"><dt>Dvdevcode. h (inclure DShow. h)</dt></span><span class="sxs-lookup"><span data-stu-id="864cc-116"><dt>Dvdevcode.h (include Dshow.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="864cc-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="864cc-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="864cc-118">Applications DVD</span><span class="sxs-lookup"><span data-stu-id="864cc-118">DVD Applications</span></span>](dvd-applications.md)
</dt> <dt>

[<span data-ttu-id="864cc-119">Codes de notification des événements DVD</span><span class="sxs-lookup"><span data-stu-id="864cc-119">DVD Event Notification Codes</span></span>](dvd-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="864cc-120">Notification d’événement dans DirectShow</span><span class="sxs-lookup"><span data-stu-id="864cc-120">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




