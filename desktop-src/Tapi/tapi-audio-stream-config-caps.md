---
description: La \_ \_ \_ structure d’embouts de la configuration du flux audio TAPI \_ est contenue dans la structure de la \_ configuration du flux TAPI \_ \_ lorsque le membre CapsType est défini sur le membre AudioCap de l’Union StreamConfigCapsType.
ms.assetid: 61575839-4604-4c8b-ae4d-fe796c3c5314
title: Structure TAPI_AUDIO_STREAM_CONFIG_CAPS (Ipmsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: daec587a8e760bedd3ab9c6b3469ef8f70b72383
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541330"
---
# <a name="tapi_audio_stream_config_caps-structure"></a><span data-ttu-id="136ba-103">\_Structure d' \_ \_ \_ embouts de la configuration du flux audio TAPI</span><span class="sxs-lookup"><span data-stu-id="136ba-103">TAPI\_AUDIO\_STREAM\_CONFIG\_CAPS structure</span></span>

<span data-ttu-id="136ba-104">\[ Cette structure n’est pas disponible pour une utilisation dans Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="136ba-104">\[ This structure is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="136ba-105">L’API cliente RTC offre des fonctionnalités similaires.\]</span><span class="sxs-lookup"><span data-stu-id="136ba-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="136ba-106">La structure d' **\_ \_ \_ \_ embouts de la configuration du flux audio TAPI** est contenue dans la  structure de la [**\_ \_ configuration \_ du flux TAPI**](tapi-stream-config-caps.md) lorsque le membre CapsType est défini sur le membre **AudioCap** de l’Union [**StreamConfigCapsType**](streamconfigcapstype.md) .</span><span class="sxs-lookup"><span data-stu-id="136ba-106">The **TAPI\_AUDIO\_STREAM\_CONFIG\_CAPS** structure is contained by the [**TAPI\_STREAM\_CONFIG\_CAPS**](tapi-stream-config-caps.md) structure when the **CapsType** member is set to the **AudioCap** member of the [**StreamConfigCapsType**](streamconfigcapstype.md) union.</span></span>

## <a name="syntax"></a><span data-ttu-id="136ba-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="136ba-107">Syntax</span></span>


```C++
} TAPI_AUDIO_STREAM_CONFIG_CAPS;
```



## <a name="members"></a><span data-ttu-id="136ba-108">Membres</span><span class="sxs-lookup"><span data-stu-id="136ba-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="136ba-109">**Description**</span><span class="sxs-lookup"><span data-stu-id="136ba-109">**Description**</span></span>
</dt> <dd>

<span data-ttu-id="136ba-110">Description conviviale du type de configuration de flux audio à afficher aux utilisateurs de l’application.</span><span class="sxs-lookup"><span data-stu-id="136ba-110">A friendly description of the audio stream configuration type for display to application users.</span></span>

</dd> <dt>

<span data-ttu-id="136ba-111">**MinimumChannels**</span><span class="sxs-lookup"><span data-stu-id="136ba-111">**MinimumChannels**</span></span>
</dt> <dd>

<span data-ttu-id="136ba-112">Nombre minimal de canaux associés au flux.</span><span class="sxs-lookup"><span data-stu-id="136ba-112">The minimum number of channels associated with the stream.</span></span>

</dd> <dt>

<span data-ttu-id="136ba-113">**MaximumChannels**</span><span class="sxs-lookup"><span data-stu-id="136ba-113">**MaximumChannels**</span></span>
</dt> <dd>

<span data-ttu-id="136ba-114">Nombre maximal de canaux associés au flux.</span><span class="sxs-lookup"><span data-stu-id="136ba-114">The maximum number of channels associated with the stream.</span></span>

</dd> <dt>

<span data-ttu-id="136ba-115">**ChannelsGranularity**</span><span class="sxs-lookup"><span data-stu-id="136ba-115">**ChannelsGranularity**</span></span>
</dt> <dd>

<span data-ttu-id="136ba-116">Granularité du nombre de canaux.</span><span class="sxs-lookup"><span data-stu-id="136ba-116">The granularity of the channel count.</span></span>

</dd> <dt>

<span data-ttu-id="136ba-117">**MinimumBitsPerSample**</span><span class="sxs-lookup"><span data-stu-id="136ba-117">**MinimumBitsPerSample**</span></span>
</dt> <dd>

<span data-ttu-id="136ba-118">Nombre minimal de bits par échantillon.</span><span class="sxs-lookup"><span data-stu-id="136ba-118">The minimum number of bits per sample.</span></span>

</dd> <dt>

<span data-ttu-id="136ba-119">**MaximumBitsPerSample**</span><span class="sxs-lookup"><span data-stu-id="136ba-119">**MaximumBitsPerSample**</span></span>
</dt> <dd>

<span data-ttu-id="136ba-120">Nombre maximal de bits par échantillon.</span><span class="sxs-lookup"><span data-stu-id="136ba-120">The maximum number of bits per sample.</span></span>

</dd> <dt>

<span data-ttu-id="136ba-121">**BitsPerSampleGranularity**</span><span class="sxs-lookup"><span data-stu-id="136ba-121">**BitsPerSampleGranularity**</span></span>
</dt> <dd>

<span data-ttu-id="136ba-122">Granularité des bits par valeurs d’échantillon.</span><span class="sxs-lookup"><span data-stu-id="136ba-122">The granularity of the bits per sample values.</span></span>

</dd> <dt>

<span data-ttu-id="136ba-123">**MinimumSampleFrequency**</span><span class="sxs-lookup"><span data-stu-id="136ba-123">**MinimumSampleFrequency**</span></span>
</dt> <dd>

<span data-ttu-id="136ba-124">Fréquence d’échantillonnage minimale.</span><span class="sxs-lookup"><span data-stu-id="136ba-124">The minimum sampling frequency.</span></span>

</dd> <dt>

<span data-ttu-id="136ba-125">**MaximumSampleFrequency**</span><span class="sxs-lookup"><span data-stu-id="136ba-125">**MaximumSampleFrequency**</span></span>
</dt> <dd>

<span data-ttu-id="136ba-126">Fréquence d’échantillonnage maximale.</span><span class="sxs-lookup"><span data-stu-id="136ba-126">The maximum sampling frequency.</span></span>

</dd> <dt>

<span data-ttu-id="136ba-127">**SampleFrequencyGranularity**</span><span class="sxs-lookup"><span data-stu-id="136ba-127">**SampleFrequencyGranularity**</span></span>
</dt> <dd>

<span data-ttu-id="136ba-128">Granularité des valeurs de fréquence d’échantillonnage.</span><span class="sxs-lookup"><span data-stu-id="136ba-128">The granularity of the sampling frequency values.</span></span>

</dd> <dt>

<span data-ttu-id="136ba-129">**MinimumAvgBytesPerSec**</span><span class="sxs-lookup"><span data-stu-id="136ba-129">**MinimumAvgBytesPerSec**</span></span>
</dt> <dd>

<span data-ttu-id="136ba-130">Nombre moyen d’octets par seconde.</span><span class="sxs-lookup"><span data-stu-id="136ba-130">The minimum average bytes per second.</span></span>

</dd> <dt>

<span data-ttu-id="136ba-131">**MaximumAvgBytesPerSec**</span><span class="sxs-lookup"><span data-stu-id="136ba-131">**MaximumAvgBytesPerSec**</span></span>
</dt> <dd>

<span data-ttu-id="136ba-132">Nombre moyen d’octets par seconde.</span><span class="sxs-lookup"><span data-stu-id="136ba-132">The maximum average bytes per second.</span></span>

</dd> <dt>

<span data-ttu-id="136ba-133">**AvgBytesPerSecGranularity**</span><span class="sxs-lookup"><span data-stu-id="136ba-133">**AvgBytesPerSecGranularity**</span></span>
</dt> <dd>

<span data-ttu-id="136ba-134">Granularité des valeurs d’octets par seconde.</span><span class="sxs-lookup"><span data-stu-id="136ba-134">The granularity of the bytes per second values.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="136ba-135">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="136ba-135">Requirements</span></span>



| <span data-ttu-id="136ba-136">Condition requise</span><span class="sxs-lookup"><span data-stu-id="136ba-136">Requirement</span></span> | <span data-ttu-id="136ba-137">Valeur</span><span class="sxs-lookup"><span data-stu-id="136ba-137">Value</span></span> |
|-------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="136ba-138">Version TAPI</span><span class="sxs-lookup"><span data-stu-id="136ba-138">TAPI version</span></span><br/> | <span data-ttu-id="136ba-139">Nécessite TAPI 3,1</span><span class="sxs-lookup"><span data-stu-id="136ba-139">Requires TAPI 3.1</span></span><br/>                                                       |
| <span data-ttu-id="136ba-140">En-tête</span><span class="sxs-lookup"><span data-stu-id="136ba-140">Header</span></span><br/>       | <dl> <span data-ttu-id="136ba-141"><dt>Ipmsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="136ba-141"><dt>Ipmsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="136ba-142">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="136ba-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="136ba-143">**\_majuscules de la configuration de flux TAPI \_ \_**</span><span class="sxs-lookup"><span data-stu-id="136ba-143">**TAPI\_STREAM\_CONFIG\_CAPS**</span></span>](tapi-stream-config-caps.md)
</dt> </dl>

 

 




