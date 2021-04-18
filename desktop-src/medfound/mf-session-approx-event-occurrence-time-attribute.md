---
description: Heure approximative à laquelle la session multimédia a déclenché un événement.
ms.assetid: 58083bc8-59cc-4503-8fae-36fcd864921a
title: Attribut MF_SESSION_APPROX_EVENT_OCCURRENCE_TIME (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a31b1970c2c9d86384c12c50777a8cee55e3ffd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106536509"
---
# <a name="mf_session_approx_event_occurrence_time-attribute"></a><span data-ttu-id="f74b2-103">\_ \_ \_ \_ \_ Attribut heure d’occurrence de l’événement de session MF</span><span class="sxs-lookup"><span data-stu-id="f74b2-103">MF\_SESSION\_APPROX\_EVENT\_OCCURRENCE\_TIME attribute</span></span>

<span data-ttu-id="f74b2-104">Heure approximative à laquelle la session multimédia a déclenché un événement.</span><span class="sxs-lookup"><span data-stu-id="f74b2-104">The approximate time when the Media Session raised an event.</span></span>

## <a name="data-type"></a><span data-ttu-id="f74b2-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="f74b2-105">Data type</span></span>

<span data-ttu-id="f74b2-106">**UINT64**</span><span class="sxs-lookup"><span data-stu-id="f74b2-106">**UINT64**</span></span>

<span data-ttu-id="f74b2-107">Traiter en tant que valeur **LongLong** .</span><span class="sxs-lookup"><span data-stu-id="f74b2-107">Treat as a **LONGLONG** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f74b2-108">Notes</span><span class="sxs-lookup"><span data-stu-id="f74b2-108">Remarks</span></span>

<span data-ttu-id="f74b2-109">Certains événements de la session multimédia ont cet attribut.</span><span class="sxs-lookup"><span data-stu-id="f74b2-109">Some events from the Media Session have this attribute.</span></span> <span data-ttu-id="f74b2-110">La valeur donne l’heure de la présentation approximative lorsque l’événement a été déclenché.</span><span class="sxs-lookup"><span data-stu-id="f74b2-110">The value gives the approximate presentation time when the event was raised.</span></span>

<span data-ttu-id="f74b2-111">Cet attribut est une valeur signée, bien qu’il soit stocké en tant que **UINT64**.</span><span class="sxs-lookup"><span data-stu-id="f74b2-111">This attribute is a signed value, although it is stored as a **UINT64**.</span></span>

<span data-ttu-id="f74b2-112">La constante GUID de cet attribut est exportée à partir de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="f74b2-112">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="f74b2-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f74b2-113">Requirements</span></span>



| <span data-ttu-id="f74b2-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f74b2-114">Requirement</span></span> | <span data-ttu-id="f74b2-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="f74b2-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="f74b2-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f74b2-116">Minimum supported client</span></span><br/> | <span data-ttu-id="f74b2-117">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f74b2-117">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="f74b2-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f74b2-118">Minimum supported server</span></span><br/> | <span data-ttu-id="f74b2-119">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f74b2-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="f74b2-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="f74b2-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="f74b2-121"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="f74b2-121"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f74b2-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f74b2-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f74b2-123">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="f74b2-123">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="f74b2-124">Attributs d'événement</span><span class="sxs-lookup"><span data-stu-id="f74b2-124">Event Attributes</span></span>](event-attributes.md)
</dt> <dt>

[<span data-ttu-id="f74b2-125">**IMFAttributes::GetUINT64**</span><span class="sxs-lookup"><span data-stu-id="f74b2-125">**IMFAttributes::GetUINT64**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64)
</dt> <dt>

[<span data-ttu-id="f74b2-126">**IMFAttributes::SetUINT64**</span><span class="sxs-lookup"><span data-stu-id="f74b2-126">**IMFAttributes::SetUINT64**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64)
</dt> </dl>

 

 




