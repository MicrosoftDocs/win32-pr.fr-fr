---
description: EC_DVD_VOBU_Offset-envoyé lorsque le navigateur DVD analyse un paquet PCI.
ms.assetid: e2e65007-7c34-4be4-86b9-9491061891e5
title: EC_DVD_VOBU_Offset (Dvdevcode. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_VOBU_Offset
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: 9223f2d5bb25d7b950dba8fb19c152cf3184af93
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108119767"
---
# <a name="ec_dvd_vobu_offset"></a><span data-ttu-id="65d99-103">\_ \_ Décalage VOBU du DVD EC \_</span><span class="sxs-lookup"><span data-stu-id="65d99-103">EC\_DVD\_VOBU\_Offset</span></span>

<span data-ttu-id="65d99-104">Envoyé lorsque le [navigateur DVD](dvd-navigator-filter.md) analyse un paquet PCI.</span><span class="sxs-lookup"><span data-stu-id="65d99-104">Sent when the [DVD Navigator](dvd-navigator-filter.md) parses a PCI packet.</span></span>

## <a name="parameters"></a><span data-ttu-id="65d99-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="65d99-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="65d99-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="65d99-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="65d99-107">Décalage de bloc de l’unité d’objet vidéo (VOBU) la plus récente.</span><span class="sxs-lookup"><span data-stu-id="65d99-107">The block offset of the most recent video object unit (VOBU).</span></span>

</dd> <dt>

<span data-ttu-id="65d99-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="65d99-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="65d99-109">Numéro du jeu de titres vidéo actuel (VTSN).</span><span class="sxs-lookup"><span data-stu-id="65d99-109">The current video title set number (VTSN).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="65d99-110">Notes </span><span class="sxs-lookup"><span data-stu-id="65d99-110">Remarks</span></span>

<span data-ttu-id="65d99-111">Cet événement est désactivé par défaut.</span><span class="sxs-lookup"><span data-stu-id="65d99-111">This event is disabled by default.</span></span> <span data-ttu-id="65d99-112">Pour activer cet événement, appelez [**IDvdControl2 :: SetOption**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-setoption) et affectez à l’option **DVD \_ EnableLoggingEvents** la **valeur true**.</span><span class="sxs-lookup"><span data-stu-id="65d99-112">To enable this event, call [**IDvdControl2::SetOption**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-setoption) and set the **DVD\_EnableLoggingEvents** option to **TRUE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="65d99-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="65d99-113">Requirements</span></span>



| <span data-ttu-id="65d99-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="65d99-114">Requirement</span></span> | <span data-ttu-id="65d99-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="65d99-115">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="65d99-116">En-tête</span><span class="sxs-lookup"><span data-stu-id="65d99-116">Header</span></span><br/> | <dl> <span data-ttu-id="65d99-117"><dt>Dvdevcode. h (inclure DShow. h)</dt></span><span class="sxs-lookup"><span data-stu-id="65d99-117"><dt>Dvdevcode.h (include Dshow.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="65d99-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="65d99-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="65d99-119">Applications DVD</span><span class="sxs-lookup"><span data-stu-id="65d99-119">DVD Applications</span></span>](dvd-applications.md)
</dt> <dt>

[<span data-ttu-id="65d99-120">Codes de notification des événements DVD</span><span class="sxs-lookup"><span data-stu-id="65d99-120">DVD Event Notification Codes</span></span>](dvd-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="65d99-121">Notification d’événement dans DirectShow</span><span class="sxs-lookup"><span data-stu-id="65d99-121">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




