---
description: La \_ \_ \_ structure d’embouts de la configuration du flux vidéo TAPI \_ est contenue dans la structure de la \_ configuration du flux TAPI \_ \_ lorsque le membre CapsType est défini sur le membre VideoCap de l’Union StreamConfigCapsType.
ms.assetid: 8812755a-50e8-4d8e-ab67-7a3a4b2a4a67
title: Structure TAPI_VIDEO_STREAM_CONFIG_CAPS (Ipmsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 525a35cb7c7332aa4e80fe8d5e2436e75e2d5c08
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106538148"
---
# <a name="tapi_video_stream_config_caps-structure"></a><span data-ttu-id="94178-103">\_Structure d' \_ \_ \_ embouts de la configuration du flux vidéo TAPI</span><span class="sxs-lookup"><span data-stu-id="94178-103">TAPI\_VIDEO\_STREAM\_CONFIG\_CAPS structure</span></span>

<span data-ttu-id="94178-104">\[ Cette structure n’est pas disponible pour une utilisation dans Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="94178-104">\[ This structure is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="94178-105">L’API cliente RTC offre des fonctionnalités similaires.\]</span><span class="sxs-lookup"><span data-stu-id="94178-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="94178-106">La structure d' **\_ \_ \_ \_ embouts de la configuration du flux vidéo TAPI** est contenue dans la  structure de la [**\_ \_ configuration \_ du flux TAPI**](tapi-stream-config-caps.md) lorsque le membre CapsType est défini sur le membre **VideoCap** de l’Union [**StreamConfigCapsType**](streamconfigcapstype.md) .</span><span class="sxs-lookup"><span data-stu-id="94178-106">The **TAPI\_VIDEO\_STREAM\_CONFIG\_CAPS** structure is contained by the [**TAPI\_STREAM\_CONFIG\_CAPS**](tapi-stream-config-caps.md) structure when the **CapsType** member is set to the **VideoCap** member of the [**StreamConfigCapsType**](streamconfigcapstype.md) union.</span></span>

## <a name="syntax"></a><span data-ttu-id="94178-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="94178-107">Syntax</span></span>


```C++
} TAPI_VIDEO_STREAM_CONFIG_CAPS;
```



## <a name="members"></a><span data-ttu-id="94178-108">Membres</span><span class="sxs-lookup"><span data-stu-id="94178-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="94178-109">**Description**</span><span class="sxs-lookup"><span data-stu-id="94178-109">**Description**</span></span>
</dt> <dd>

<span data-ttu-id="94178-110">Description conviviale du type de configuration de flux audio à afficher aux utilisateurs de l’application.</span><span class="sxs-lookup"><span data-stu-id="94178-110">A friendly description of the audio stream configuration type for display to application users.</span></span>

</dd> <dt>

<span data-ttu-id="94178-111">**VideoStandard**</span><span class="sxs-lookup"><span data-stu-id="94178-111">**VideoStandard**</span></span>
</dt> <dd>

<span data-ttu-id="94178-112">Standard vidéo en cours d’utilisation.</span><span class="sxs-lookup"><span data-stu-id="94178-112">Video standard being used.</span></span>

</dd> <dt>

<span data-ttu-id="94178-113">**Inverser**</span><span class="sxs-lookup"><span data-stu-id="94178-113">**InputSize**</span></span>
</dt> <dd>

<span data-ttu-id="94178-114">Taille d’entrée du frame.</span><span class="sxs-lookup"><span data-stu-id="94178-114">Input size of frame.</span></span>

</dd> <dt>

<span data-ttu-id="94178-115">**MinCroppingSize**</span><span class="sxs-lookup"><span data-stu-id="94178-115">**MinCroppingSize**</span></span>
</dt> <dd>

<span data-ttu-id="94178-116">Taille minimale du rognage.</span><span class="sxs-lookup"><span data-stu-id="94178-116">Minimum cropping size.</span></span>

</dd> <dt>

<span data-ttu-id="94178-117">**MaxCroppingSize**</span><span class="sxs-lookup"><span data-stu-id="94178-117">**MaxCroppingSize**</span></span>
</dt> <dd>

<span data-ttu-id="94178-118">Taille maximale du rognage.</span><span class="sxs-lookup"><span data-stu-id="94178-118">Maximum cropping size.</span></span>

</dd> <dt>

<span data-ttu-id="94178-119">**CropGranularityX**</span><span class="sxs-lookup"><span data-stu-id="94178-119">**CropGranularityX**</span></span>
</dt> <dd>

<span data-ttu-id="94178-120">Granularité du rognage autorisé le long de l’axe x.</span><span class="sxs-lookup"><span data-stu-id="94178-120">Granularity of cropping allowed along the x-axis.</span></span>

</dd> <dt>

<span data-ttu-id="94178-121">**CropGranularityY**</span><span class="sxs-lookup"><span data-stu-id="94178-121">**CropGranularityY**</span></span>
</dt> <dd>

<span data-ttu-id="94178-122">Granularité du rognage autorisé le long de l’axe y.</span><span class="sxs-lookup"><span data-stu-id="94178-122">Granularity of cropping allowed along the y-axis.</span></span>

</dd> <dt>

<span data-ttu-id="94178-123">**CropAlignX**</span><span class="sxs-lookup"><span data-stu-id="94178-123">**CropAlignX**</span></span>
</dt> <dd>

<span data-ttu-id="94178-124">Alignement du rognage de l’axe x.</span><span class="sxs-lookup"><span data-stu-id="94178-124">Alignment of x-axis cropping.</span></span>

</dd> <dt>

<span data-ttu-id="94178-125">**CropAlignY**</span><span class="sxs-lookup"><span data-stu-id="94178-125">**CropAlignY**</span></span>
</dt> <dd>

<span data-ttu-id="94178-126">Alignement du rognage de l’axe y.</span><span class="sxs-lookup"><span data-stu-id="94178-126">Alignment of y-axis cropping.</span></span>

</dd> <dt>

<span data-ttu-id="94178-127">**MinOutputSize**</span><span class="sxs-lookup"><span data-stu-id="94178-127">**MinOutputSize**</span></span>
</dt> <dd>

<span data-ttu-id="94178-128">Taille minimale résultante de la fenêtre vidéo.</span><span class="sxs-lookup"><span data-stu-id="94178-128">Minimum resultant size of video window.</span></span>

</dd> <dt>

<span data-ttu-id="94178-129">**MaxOutputSize**</span><span class="sxs-lookup"><span data-stu-id="94178-129">**MaxOutputSize**</span></span>
</dt> <dd>

<span data-ttu-id="94178-130">Taille maximale résultante de la fenêtre vidéo.</span><span class="sxs-lookup"><span data-stu-id="94178-130">Maximum resultant size of video window.</span></span>

</dd> <dt>

<span data-ttu-id="94178-131">**OutputGranularityX**</span><span class="sxs-lookup"><span data-stu-id="94178-131">**OutputGranularityX**</span></span>
</dt> <dd>

<span data-ttu-id="94178-132">Granularité de la taille de sortie le long de l’axe x.</span><span class="sxs-lookup"><span data-stu-id="94178-132">Granularity of output size along the x-axis.</span></span>

</dd> <dt>

<span data-ttu-id="94178-133">**OutputGranularityY**</span><span class="sxs-lookup"><span data-stu-id="94178-133">**OutputGranularityY**</span></span>
</dt> <dd>

<span data-ttu-id="94178-134">Granularité de la taille de sortie le long de l’axe y.</span><span class="sxs-lookup"><span data-stu-id="94178-134">Granularity of output size along the y-axis.</span></span>

</dd> <dt>

<span data-ttu-id="94178-135">**StretchTapsX**</span><span class="sxs-lookup"><span data-stu-id="94178-135">**StretchTapsX**</span></span>
</dt> <dd>

<span data-ttu-id="94178-136">Étirer le long de l’axe x.</span><span class="sxs-lookup"><span data-stu-id="94178-136">Stretch along the x-axis.</span></span>

</dd> <dt>

<span data-ttu-id="94178-137">**StretchTapsY**</span><span class="sxs-lookup"><span data-stu-id="94178-137">**StretchTapsY**</span></span>
</dt> <dd>

<span data-ttu-id="94178-138">Étirement le long de l’axe y.</span><span class="sxs-lookup"><span data-stu-id="94178-138">Stretch along the y-axis.</span></span>

</dd> <dt>

<span data-ttu-id="94178-139">**ShrinkTapsX**</span><span class="sxs-lookup"><span data-stu-id="94178-139">**ShrinkTapsX**</span></span>
</dt> <dd>

<span data-ttu-id="94178-140">Rétrécir le long de l’axe x.</span><span class="sxs-lookup"><span data-stu-id="94178-140">Shrink along the x-axis.</span></span>

</dd> <dt>

<span data-ttu-id="94178-141">**ShrinkTapsY**</span><span class="sxs-lookup"><span data-stu-id="94178-141">**ShrinkTapsY**</span></span>
</dt> <dd>

<span data-ttu-id="94178-142">Rétrécir le long de l’axe y.</span><span class="sxs-lookup"><span data-stu-id="94178-142">Shrink along the y-axis.</span></span>

</dd> <dt>

<span data-ttu-id="94178-143">**MinFrameInterval**</span><span class="sxs-lookup"><span data-stu-id="94178-143">**MinFrameInterval**</span></span>
</dt> <dd>

<span data-ttu-id="94178-144">Intervalle de trame vidéo minimal.</span><span class="sxs-lookup"><span data-stu-id="94178-144">Minimum video frame interval.</span></span>

</dd> <dt>

<span data-ttu-id="94178-145">**MaxFrameInterval**</span><span class="sxs-lookup"><span data-stu-id="94178-145">**MaxFrameInterval**</span></span>
</dt> <dd>

<span data-ttu-id="94178-146">Intervalle de trame vidéo maximal.</span><span class="sxs-lookup"><span data-stu-id="94178-146">Maximum video frame interval.</span></span>

</dd> <dt>

<span data-ttu-id="94178-147">**MinBitsPerSecond**</span><span class="sxs-lookup"><span data-stu-id="94178-147">**MinBitsPerSecond**</span></span>
</dt> <dd>

<span data-ttu-id="94178-148">Nombre minimal de bits par seconde.</span><span class="sxs-lookup"><span data-stu-id="94178-148">Minimum bits per second.</span></span>

</dd> <dt>

<span data-ttu-id="94178-149">**MaxBitsPerSecond**</span><span class="sxs-lookup"><span data-stu-id="94178-149">**MaxBitsPerSecond**</span></span>
</dt> <dd>

<span data-ttu-id="94178-150">Nombre maximal de bits par seconde.</span><span class="sxs-lookup"><span data-stu-id="94178-150">Maximum bits per second.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="94178-151">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="94178-151">Requirements</span></span>



| <span data-ttu-id="94178-152">Condition requise</span><span class="sxs-lookup"><span data-stu-id="94178-152">Requirement</span></span> | <span data-ttu-id="94178-153">Valeur</span><span class="sxs-lookup"><span data-stu-id="94178-153">Value</span></span> |
|-------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="94178-154">Version TAPI</span><span class="sxs-lookup"><span data-stu-id="94178-154">TAPI version</span></span><br/> | <span data-ttu-id="94178-155">Nécessite TAPI 3,1</span><span class="sxs-lookup"><span data-stu-id="94178-155">Requires TAPI 3.1</span></span><br/>                                                       |
| <span data-ttu-id="94178-156">En-tête</span><span class="sxs-lookup"><span data-stu-id="94178-156">Header</span></span><br/>       | <dl> <span data-ttu-id="94178-157"><dt>Ipmsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="94178-157"><dt>Ipmsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="94178-158">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="94178-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="94178-159">**\_majuscules de la configuration de flux TAPI \_ \_**</span><span class="sxs-lookup"><span data-stu-id="94178-159">**TAPI\_STREAM\_CONFIG\_CAPS**</span></span>](tapi-stream-config-caps.md)
</dt> </dl>

 

 




