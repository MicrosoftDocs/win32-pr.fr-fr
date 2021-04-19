---
description: L' \_ énumération d’événement participant décrit les événements participants.
ms.assetid: 678165f2-ad0b-415f-86bf-8c4e3bd8d793
title: Énumération PARTICIPANT_EVENT (Ipmsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 225b1b9901efa5648dfaa326c53ed69cff2c4295
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106523589"
---
# <a name="participant_event-enumeration"></a><span data-ttu-id="98850-103">\_Énumération des événements participants</span><span class="sxs-lookup"><span data-stu-id="98850-103">PARTICIPANT\_EVENT enumeration</span></span>

<span data-ttu-id="98850-104">\[ Cette énumération n’est pas disponible pour une utilisation dans Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="98850-104">\[ This enumeration is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="98850-105">L’API cliente RTC offre des fonctionnalités similaires.\]</span><span class="sxs-lookup"><span data-stu-id="98850-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="98850-106">L’énumération d' **\_ événement participant** décrit les événements participants.</span><span class="sxs-lookup"><span data-stu-id="98850-106">The **PARTICIPANT\_EVENT** enum describes participant events.</span></span> <span data-ttu-id="98850-107">La méthode d' [**\_ événement ITParticipantEvent :: obtenir**](itparticipantevent-get-event.md) retourne un membre de cette énumération pour indiquer le type d’événement participant à la Conférence qui s’est produit.</span><span class="sxs-lookup"><span data-stu-id="98850-107">The [**ITParticipantEvent::get\_Event**](itparticipantevent-get-event.md) method returns a member of this enum to indicate the type of conference participant event that occurred.</span></span> <span data-ttu-id="98850-108">Cette énumération est utilisée par les applications qui accèdent au [MSP ipconf](ipconf-msp.md).</span><span class="sxs-lookup"><span data-stu-id="98850-108">This enum is used by applications that access the [IPConf MSP](ipconf-msp.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="98850-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="98850-109">Syntax</span></span>


```C++
} PARTICIPANT_EVENT;
```



## <a name="constants"></a><span data-ttu-id="98850-110">Constantes</span><span class="sxs-lookup"><span data-stu-id="98850-110">Constants</span></span>

<dl> <dt>

<span data-ttu-id="98850-111"><span id="PE_NEW_PARTICIPANT"></span><span id="pe_new_participant"></span>**\_nouveau \_ participant PE**</span><span class="sxs-lookup"><span data-stu-id="98850-111"><span id="PE_NEW_PARTICIPANT"></span><span id="pe_new_participant"></span>**PE\_NEW\_PARTICIPANT**</span></span>
</dt> <dd>

<span data-ttu-id="98850-112">Un nouveau participant a été ajouté à la Conférence.</span><span class="sxs-lookup"><span data-stu-id="98850-112">A new participant has been added to the conference.</span></span>

</dd> <dt>

<span data-ttu-id="98850-113"><span id="PE_INFO_CHANGE"></span><span id="pe_info_change"></span>**\_modification des informations PE \_**</span><span class="sxs-lookup"><span data-stu-id="98850-113"><span id="PE_INFO_CHANGE"></span><span id="pe_info_change"></span>**PE\_INFO\_CHANGE**</span></span>
</dt> <dd>

<span data-ttu-id="98850-114">Les informations sur un participant ont été modifiées.</span><span class="sxs-lookup"><span data-stu-id="98850-114">Information on a participant has changed.</span></span>

</dd> <dt>

<span data-ttu-id="98850-115"><span id="PE_PARTICIPANT_LEAVE"></span><span id="pe_participant_leave"></span>**\_absence de participant PE \_**</span><span class="sxs-lookup"><span data-stu-id="98850-115"><span id="PE_PARTICIPANT_LEAVE"></span><span id="pe_participant_leave"></span>**PE\_PARTICIPANT\_LEAVE**</span></span>
</dt> <dd>

<span data-ttu-id="98850-116">Un participant a quitté la Conférence.</span><span class="sxs-lookup"><span data-stu-id="98850-116">A participant has left the conference.</span></span>

</dd> <dt>

<span data-ttu-id="98850-117"><span id="PE_NEW_SUBSTREAM"></span><span id="pe_new_substream"></span>**nouveau sous- \_ \_ flux PE**</span><span class="sxs-lookup"><span data-stu-id="98850-117"><span id="PE_NEW_SUBSTREAM"></span><span id="pe_new_substream"></span>**PE\_NEW\_SUBSTREAM**</span></span>
</dt> <dd>

<span data-ttu-id="98850-118">Un nouveau sous-flux a été ajouté au participant.</span><span class="sxs-lookup"><span data-stu-id="98850-118">A new substream has been added to the participant.</span></span>

</dd> <dt>

<span data-ttu-id="98850-119"><span id="PE_SUBSTREAM_REMOVED"></span><span id="pe_substream_removed"></span>**sous- \_ flux PE \_ supprimé**</span><span class="sxs-lookup"><span data-stu-id="98850-119"><span id="PE_SUBSTREAM_REMOVED"></span><span id="pe_substream_removed"></span>**PE\_SUBSTREAM\_REMOVED**</span></span>
</dt> <dd>

<span data-ttu-id="98850-120">Un nouveau sous-flux a été supprimé du participant.</span><span class="sxs-lookup"><span data-stu-id="98850-120">A new substream has been removed from the participant.</span></span>

</dd> <dt>

<span data-ttu-id="98850-121"><span id="PE_SUBSTREAM_MAPPED"></span><span id="pe_substream_mapped"></span>**sous- \_ flux PE \_ mappé**</span><span class="sxs-lookup"><span data-stu-id="98850-121"><span id="PE_SUBSTREAM_MAPPED"></span><span id="pe_substream_mapped"></span>**PE\_SUBSTREAM\_MAPPED**</span></span>
</dt> <dd>

<span data-ttu-id="98850-122">Un participant a été mappé à un sous-flux.</span><span class="sxs-lookup"><span data-stu-id="98850-122">A participant has been mapped to a substream.</span></span>

</dd> <dt>

<span data-ttu-id="98850-123"><span id="PE_SUBSTREAM_UNMAPPED"></span><span id="pe_substream_unmapped"></span>**sous-flux PE non \_ \_ mappé**</span><span class="sxs-lookup"><span data-stu-id="98850-123"><span id="PE_SUBSTREAM_UNMAPPED"></span><span id="pe_substream_unmapped"></span>**PE\_SUBSTREAM\_UNMAPPED**</span></span>
</dt> <dd>

<span data-ttu-id="98850-124">Un participant a été démappé d’un sous-flux.</span><span class="sxs-lookup"><span data-stu-id="98850-124">A participant has been unmapped from a substream.</span></span>

</dd> <dt>

<span data-ttu-id="98850-125"><span id="PE_PARTICIPANT_TIMEOUT"></span><span id="pe_participant_timeout"></span>**\_ \_ délai d’attente des participants PE**</span><span class="sxs-lookup"><span data-stu-id="98850-125"><span id="PE_PARTICIPANT_TIMEOUT"></span><span id="pe_participant_timeout"></span>**PE\_PARTICIPANT\_TIMEOUT**</span></span>
</dt> <dd>

<span data-ttu-id="98850-126">Un participant a été supprimé de la Conférence en raison d’un délai d’attente.</span><span class="sxs-lookup"><span data-stu-id="98850-126">A participant has been removed from the conference due to a timeout.</span></span>

</dd> <dt>

<span data-ttu-id="98850-127"><span id="PE_PARTICIPANT_RECOVERED"></span><span id="pe_participant_recovered"></span>**\_participant PE \_ récupéré**</span><span class="sxs-lookup"><span data-stu-id="98850-127"><span id="PE_PARTICIPANT_RECOVERED"></span><span id="pe_participant_recovered"></span>**PE\_PARTICIPANT\_RECOVERED**</span></span>
</dt> <dd>

<span data-ttu-id="98850-128">Un participant supprimé est de nouveau visible.</span><span class="sxs-lookup"><span data-stu-id="98850-128">A removed participant is again visible.</span></span> <span data-ttu-id="98850-129">En règle générale, il s’agit d’un participant qui a dépassé le délai d’attente, mais les signaux sont maintenant reçus.</span><span class="sxs-lookup"><span data-stu-id="98850-129">Usually, this is a participant who timed out but signals are now being received.</span></span>

</dd> <dt>

<span data-ttu-id="98850-130"><span id="PE_PARTICIPANT_ACTIVE"></span><span id="pe_participant_active"></span>**\_participant PE \_ actif**</span><span class="sxs-lookup"><span data-stu-id="98850-130"><span id="PE_PARTICIPANT_ACTIVE"></span><span id="pe_participant_active"></span>**PE\_PARTICIPANT\_ACTIVE**</span></span>
</dt> <dd>

<span data-ttu-id="98850-131">Le participant est devenu actif dans la Conférence.</span><span class="sxs-lookup"><span data-stu-id="98850-131">The participant has become active in the conference.</span></span>

</dd> <dt>

<span data-ttu-id="98850-132"><span id="PE_PARTICIPANT_INACTIVE"></span><span id="pe_participant_inactive"></span>**\_participant PE \_ inactif**</span><span class="sxs-lookup"><span data-stu-id="98850-132"><span id="PE_PARTICIPANT_INACTIVE"></span><span id="pe_participant_inactive"></span>**PE\_PARTICIPANT\_INACTIVE**</span></span>
</dt> <dd>

<span data-ttu-id="98850-133">Le participant est devenu inactif dans la Conférence.</span><span class="sxs-lookup"><span data-stu-id="98850-133">The participant has become inactive in the conference.</span></span>

</dd> <dt>

<span data-ttu-id="98850-134"><span id="PE_LOCAL_TALKING"></span><span id="pe_local_talking"></span>**\_communication locale \_ PE**</span><span class="sxs-lookup"><span data-stu-id="98850-134"><span id="PE_LOCAL_TALKING"></span><span id="pe_local_talking"></span>**PE\_LOCAL\_TALKING**</span></span>
</dt> <dd>

<span data-ttu-id="98850-135">Le participant local a commencé à parler.</span><span class="sxs-lookup"><span data-stu-id="98850-135">The local participant has started to talk.</span></span>

</dd> <dt>

<span data-ttu-id="98850-136"><span id="PE_LOCAL_SILENT"></span><span id="pe_local_silent"></span>**PE \_ local en \_ mode silencieux**</span><span class="sxs-lookup"><span data-stu-id="98850-136"><span id="PE_LOCAL_SILENT"></span><span id="pe_local_silent"></span>**PE\_LOCAL\_SILENT**</span></span>
</dt> <dd>

<span data-ttu-id="98850-137">Le participant local est devenu silencieux dans la Conférence.</span><span class="sxs-lookup"><span data-stu-id="98850-137">The local participant has become silent in the conference.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="98850-138">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="98850-138">Requirements</span></span>



| <span data-ttu-id="98850-139">Condition requise</span><span class="sxs-lookup"><span data-stu-id="98850-139">Requirement</span></span> | <span data-ttu-id="98850-140">Valeur</span><span class="sxs-lookup"><span data-stu-id="98850-140">Value</span></span> |
|-------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="98850-141">Version TAPI</span><span class="sxs-lookup"><span data-stu-id="98850-141">TAPI version</span></span><br/> | <span data-ttu-id="98850-142">Nécessite TAPI 3,0 ou une version ultérieure</span><span class="sxs-lookup"><span data-stu-id="98850-142">Requires TAPI 3.0 or later</span></span><br/>                                              |
| <span data-ttu-id="98850-143">En-tête</span><span class="sxs-lookup"><span data-stu-id="98850-143">Header</span></span><br/>       | <dl> <span data-ttu-id="98850-144"><dt>Ipmsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="98850-144"><dt>Ipmsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="98850-145">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="98850-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="98850-146">**ITParticipantEvent :: obtient l' \_ événement**</span><span class="sxs-lookup"><span data-stu-id="98850-146">**ITParticipantEvent::get\_Event**</span></span>](itparticipantevent-get-event.md)
</dt> <dt>

[<span data-ttu-id="98850-147">MSP IPConf</span><span class="sxs-lookup"><span data-stu-id="98850-147">IPConf MSP</span></span>](ipconf-msp.md)
</dt> <dt>

[<span data-ttu-id="98850-148">Interfaces MSP IPConf</span><span class="sxs-lookup"><span data-stu-id="98850-148">IPConf MSP Interfaces</span></span>](ipconf-msp-interfaces.md)
</dt> </dl>

 

 




