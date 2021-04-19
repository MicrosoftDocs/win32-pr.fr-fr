---
description: "Les membres de l' \\_ \\_ énumération info typées participant identifient le type d’informations sur les participants récupérés par la méthode ITParticipant :: obten \\_ ParticipantTypedInfo. Cette énumération est utilisée par les applications qui accèdent au MSP IPConf."
ms.assetid: ca933d8c-bfb4-4a92-b412-112e228ccca2
title: Énumération PARTICIPANT_TYPED_INFO (Confpriv. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 16ab94a487f0ea098ee9b92144874057dc463036
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528723"
---
# <a name="participant_typed_info-enumeration"></a><span data-ttu-id="d7bae-104">\_Énumération des informations typées du participant \_</span><span class="sxs-lookup"><span data-stu-id="d7bae-104">PARTICIPANT\_TYPED\_INFO enumeration</span></span>

<span data-ttu-id="d7bae-105">\[**Participant \_ Les \_ informations typées** ne peuvent pas être utilisées dans Windows Vista, windows Server 2008 et les versions ultérieures du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="d7bae-105">\[**PARTICIPANT\_TYPED\_INFO** is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="d7bae-106">L’API cliente RTC offre des fonctionnalités similaires.\]</span><span class="sxs-lookup"><span data-stu-id="d7bae-106">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="d7bae-107">Les membres de l’énumération **\_ \_ info typées participant** identifient le type d’informations sur les participants récupérés par la méthode [**ITParticipant :: obten \_ ParticipantTypedInfo**](itparticipant-get-participanttypedinfo.md) .</span><span class="sxs-lookup"><span data-stu-id="d7bae-107">The members of the **PARTICIPANT\_TYPED\_INFO** enum identify the type of participant information being retrieved by the [**ITParticipant::get\_ParticipantTypedInfo**](itparticipant-get-participanttypedinfo.md) method.</span></span> <span data-ttu-id="d7bae-108">Cette énumération est utilisée par les applications qui accèdent au [MSP ipconf](ipconf-msp.md).</span><span class="sxs-lookup"><span data-stu-id="d7bae-108">This enum is used by applications that access the [IPConf MSP](ipconf-msp.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="d7bae-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d7bae-109">Syntax</span></span>


```C++
} PARTICIPANT_TYPED_INFO;
```



## <a name="constants"></a><span data-ttu-id="d7bae-110">Constantes</span><span class="sxs-lookup"><span data-stu-id="d7bae-110">Constants</span></span>

<dl> <dt>

<span data-ttu-id="d7bae-111"><span id="PTI_CANONICALNAME"></span><span id="pti_canonicalname"></span>**PTI \_ CANONICALNAME**</span><span class="sxs-lookup"><span data-stu-id="d7bae-111"><span id="PTI_CANONICALNAME"></span><span id="pti_canonicalname"></span>**PTI\_CANONICALNAME**</span></span>
</dt> <dd>

<span data-ttu-id="d7bae-112">Nom canonique du participant, tel que someone@example.com .</span><span class="sxs-lookup"><span data-stu-id="d7bae-112">Canonical name of participant, such as someone@example.com.</span></span>

</dd> <dt>

<span data-ttu-id="d7bae-113"><span id="PTI_NAME"></span><span id="pti_name"></span>**nom de PTI \_**</span><span class="sxs-lookup"><span data-stu-id="d7bae-113"><span id="PTI_NAME"></span><span id="pti_name"></span>**PTI\_NAME**</span></span>
</dt> <dd>

<span data-ttu-id="d7bae-114">Nom affichable du participant.</span><span class="sxs-lookup"><span data-stu-id="d7bae-114">Displayable name of participant.</span></span>

</dd> <dt>

<span data-ttu-id="d7bae-115"><span id="PTI_EMAILADDRESS"></span><span id="pti_emailaddress"></span>**PTI \_ EMAILADDRESS**</span><span class="sxs-lookup"><span data-stu-id="d7bae-115"><span id="PTI_EMAILADDRESS"></span><span id="pti_emailaddress"></span>**PTI\_EMAILADDRESS**</span></span>
</dt> <dd>

<span data-ttu-id="d7bae-116">Adresse e-mail du participant.</span><span class="sxs-lookup"><span data-stu-id="d7bae-116">Participant's email address.</span></span>

</dd> <dt>

<span data-ttu-id="d7bae-117"><span id="PTI_PHONENUMBER"></span><span id="pti_phonenumber"></span>**PTI \_ PHONENUMBER**</span><span class="sxs-lookup"><span data-stu-id="d7bae-117"><span id="PTI_PHONENUMBER"></span><span id="pti_phonenumber"></span>**PTI\_PHONENUMBER**</span></span>
</dt> <dd>

<span data-ttu-id="d7bae-118">Adresse de téléphone du participant.</span><span class="sxs-lookup"><span data-stu-id="d7bae-118">Participant's phone address.</span></span>

</dd> <dt>

<span data-ttu-id="d7bae-119"><span id="PTI_LOCATION"></span><span id="pti_location"></span>**\_emplacement PTI**</span><span class="sxs-lookup"><span data-stu-id="d7bae-119"><span id="PTI_LOCATION"></span><span id="pti_location"></span>**PTI\_LOCATION**</span></span>
</dt> <dd>

<span data-ttu-id="d7bae-120">Adresse géographique du participant.</span><span class="sxs-lookup"><span data-stu-id="d7bae-120">Participant's geographical address.</span></span>

</dd> <dt>

<span data-ttu-id="d7bae-121"><span id="PTI_TOOL"></span><span id="pti_tool"></span>**\_outil PTI**</span><span class="sxs-lookup"><span data-stu-id="d7bae-121"><span id="PTI_TOOL"></span><span id="pti_tool"></span>**PTI\_TOOL**</span></span>
</dt> <dd>

<span data-ttu-id="d7bae-122">Application du participant.</span><span class="sxs-lookup"><span data-stu-id="d7bae-122">Participant's application.</span></span>

</dd> <dt>

<span data-ttu-id="d7bae-123"><span id="PTI_NOTES"></span><span id="pti_notes"></span>**PTI \_ Notes**</span><span class="sxs-lookup"><span data-stu-id="d7bae-123"><span id="PTI_NOTES"></span><span id="pti_notes"></span>**PTI\_NOTES**</span></span>
</dt> <dd>

<span data-ttu-id="d7bae-124">Notes relatives au participant.</span><span class="sxs-lookup"><span data-stu-id="d7bae-124">Notes concerning participant.</span></span>

</dd> <dt>

<span data-ttu-id="d7bae-125"><span id="PTI_PRIVATE"></span><span id="pti_private"></span>**PTI \_ privé**</span><span class="sxs-lookup"><span data-stu-id="d7bae-125"><span id="PTI_PRIVATE"></span><span id="pti_private"></span>**PTI\_PRIVATE**</span></span>
</dt> <dd>

<span data-ttu-id="d7bae-126">Définit une extension de description source expérimentale ou spécifique à l’application (SDES).</span><span class="sxs-lookup"><span data-stu-id="d7bae-126">Defines an experimental or application-specific Source Description (SDES) extension.</span></span> <span data-ttu-id="d7bae-127">Pour plus d’informations, consultez la RFC 1889.</span><span class="sxs-lookup"><span data-stu-id="d7bae-127">See RFC 1889 for details.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d7bae-128">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d7bae-128">Requirements</span></span>



| <span data-ttu-id="d7bae-129">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d7bae-129">Requirement</span></span> | <span data-ttu-id="d7bae-130">Valeur</span><span class="sxs-lookup"><span data-stu-id="d7bae-130">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d7bae-131">Version TAPI</span><span class="sxs-lookup"><span data-stu-id="d7bae-131">TAPI version</span></span><br/> | <span data-ttu-id="d7bae-132">Nécessite TAPI 3,0 ou une version ultérieure</span><span class="sxs-lookup"><span data-stu-id="d7bae-132">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="d7bae-133">En-tête</span><span class="sxs-lookup"><span data-stu-id="d7bae-133">Header</span></span><br/>       | <dl> <span data-ttu-id="d7bae-134"><dt>Confpriv. h</dt></span><span class="sxs-lookup"><span data-stu-id="d7bae-134"><dt>Confpriv.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d7bae-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d7bae-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d7bae-136">**ITParticipant :: obtient \_ ParticipantTypedInfo**</span><span class="sxs-lookup"><span data-stu-id="d7bae-136">**ITParticipant::get\_ParticipantTypedInfo**</span></span>](itparticipant-get-participanttypedinfo.md)
</dt> <dt>

[<span data-ttu-id="d7bae-137">MSP IPConf</span><span class="sxs-lookup"><span data-stu-id="d7bae-137">IPConf MSP</span></span>](ipconf-msp.md)
</dt> <dt>

[<span data-ttu-id="d7bae-138">Interfaces MSP IPConf</span><span class="sxs-lookup"><span data-stu-id="d7bae-138">IPConf MSP Interfaces</span></span>](ipconf-msp-interfaces.md)
</dt> </dl>

 

 




