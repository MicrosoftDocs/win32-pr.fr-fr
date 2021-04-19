---
description: Un certain nombre de sous-types sont définis pour la vidéo DV. Chaque possède un code FOURCC et une valeur GUID correspondante. Tous ces formats ne sont pas pris en charge ; Pour plus d’informations, consultez la section Notes.
ms.assetid: d8390bd4-0339-4955-992c-92b8c9f6bf88
title: Sous-types vidéo DV (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cbacb15f5801d959fbc5150546cff04dea687753
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541418"
---
# <a name="dv-video-subtypes"></a><span data-ttu-id="cd9bf-105">Sous-types vidéo DV</span><span class="sxs-lookup"><span data-stu-id="cd9bf-105">DV Video Subtypes</span></span>

<span data-ttu-id="cd9bf-106">Un certain nombre de sous-types sont définis pour la vidéo DV.</span><span class="sxs-lookup"><span data-stu-id="cd9bf-106">A number of subtypes are defined for DV video.</span></span> <span data-ttu-id="cd9bf-107">Chaque possède un code FOURCC et une valeur GUID correspondante.</span><span class="sxs-lookup"><span data-stu-id="cd9bf-107">Each has a FOURCC code and a corresponding GUID value.</span></span> <span data-ttu-id="cd9bf-108">Tous ces formats ne sont pas pris en charge ; Pour plus d’informations, consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="cd9bf-108">Not all of these formats are supported; see the Remarks section for more information.</span></span>

## <a name="consumer-formats"></a><span data-ttu-id="cd9bf-109">Formats grand public</span><span class="sxs-lookup"><span data-stu-id="cd9bf-109">Consumer Formats</span></span>



| <span data-ttu-id="cd9bf-110">FOURCC</span><span class="sxs-lookup"><span data-stu-id="cd9bf-110">FOURCC</span></span> | <span data-ttu-id="cd9bf-111">GUID</span><span class="sxs-lookup"><span data-stu-id="cd9bf-111">GUID</span></span>               | <span data-ttu-id="cd9bf-112">Débit des données</span><span class="sxs-lookup"><span data-stu-id="cd9bf-112">Data Rate</span></span> | <span data-ttu-id="cd9bf-113">Description</span><span class="sxs-lookup"><span data-stu-id="cd9bf-113">Description</span></span>                  |
|--------|--------------------|-----------|------------------------------|
| <span data-ttu-id="cd9bf-114">'dvsl'</span><span class="sxs-lookup"><span data-stu-id="cd9bf-114">'dvsl'</span></span> | <span data-ttu-id="cd9bf-115">MEDIASUBTYPE \_ dvsl</span><span class="sxs-lookup"><span data-stu-id="cd9bf-115">MEDIASUBTYPE\_dvsl</span></span> | <span data-ttu-id="cd9bf-116">12,5 Mbits/s</span><span class="sxs-lookup"><span data-stu-id="cd9bf-116">12.5 Mbps</span></span> | <span data-ttu-id="cd9bf-117">SD-magnétoscope numérique (525-60 ou 625-50)</span><span class="sxs-lookup"><span data-stu-id="cd9bf-117">SD-DVCR (525-60 or 625-50)</span></span>   |
| <span data-ttu-id="cd9bf-118">'dvsd'</span><span class="sxs-lookup"><span data-stu-id="cd9bf-118">'dvsd'</span></span> | <span data-ttu-id="cd9bf-119">MEDIASUBTYPE \_ DVSD</span><span class="sxs-lookup"><span data-stu-id="cd9bf-119">MEDIASUBTYPE\_dvsd</span></span> | <span data-ttu-id="cd9bf-120">25 Mbits/s</span><span class="sxs-lookup"><span data-stu-id="cd9bf-120">25 Mbps</span></span>   | <span data-ttu-id="cd9bf-121">SDL-magnétoscope numérique (525-60 ou 625-50)</span><span class="sxs-lookup"><span data-stu-id="cd9bf-121">SDL-DVCR (525-60 or 625-50)</span></span>  |
| <span data-ttu-id="cd9bf-122">'dvhd'</span><span class="sxs-lookup"><span data-stu-id="cd9bf-122">'dvhd'</span></span> | <span data-ttu-id="cd9bf-123">MEDIASUBTYPE \_ dvhd</span><span class="sxs-lookup"><span data-stu-id="cd9bf-123">MEDIASUBTYPE\_dvhd</span></span> | <span data-ttu-id="cd9bf-124">50 Mbits/s</span><span class="sxs-lookup"><span data-stu-id="cd9bf-124">50 Mbps</span></span>   | <span data-ttu-id="cd9bf-125">HD-magnétoscope numérique (1125-60 ou 1250-50)</span><span class="sxs-lookup"><span data-stu-id="cd9bf-125">HD-DVCR (1125-60 or 1250-50)</span></span> |



 

<span data-ttu-id="cd9bf-126">Reportez-vous à IEC-61834 pour plus d’informations sur ces formats.</span><span class="sxs-lookup"><span data-stu-id="cd9bf-126">Refer to IEC-61834 for more information about these formats.</span></span>

## <a name="professional-formats"></a><span data-ttu-id="cd9bf-127">Formats professionnels</span><span class="sxs-lookup"><span data-stu-id="cd9bf-127">Professional Formats</span></span>



| <span data-ttu-id="cd9bf-128">FOURCC</span><span class="sxs-lookup"><span data-stu-id="cd9bf-128">FOURCC</span></span> | <span data-ttu-id="cd9bf-129">GUID</span><span class="sxs-lookup"><span data-stu-id="cd9bf-129">GUID</span></span>               | <span data-ttu-id="cd9bf-130">Débit des données</span><span class="sxs-lookup"><span data-stu-id="cd9bf-130">Data Rate</span></span> | <span data-ttu-id="cd9bf-131">Description</span><span class="sxs-lookup"><span data-stu-id="cd9bf-131">Description</span></span>                                 |
|--------|--------------------|-----------|---------------------------------------------|
| <span data-ttu-id="cd9bf-132">'dv25'</span><span class="sxs-lookup"><span data-stu-id="cd9bf-132">'dv25'</span></span> | <span data-ttu-id="cd9bf-133">MEDIASUBTYPE \_ DV25</span><span class="sxs-lookup"><span data-stu-id="cd9bf-133">MEDIASUBTYPE\_dv25</span></span> | <span data-ttu-id="cd9bf-134">25 Mbits/s</span><span class="sxs-lookup"><span data-stu-id="cd9bf-134">25 Mbps</span></span>   | <span data-ttu-id="cd9bf-135">DVCPRO 25 (525-60 ou 625-50).</span><span class="sxs-lookup"><span data-stu-id="cd9bf-135">DVCPRO 25 (525-60 or 625-50).</span></span>               |
| <span data-ttu-id="cd9bf-136">'dv50'</span><span class="sxs-lookup"><span data-stu-id="cd9bf-136">'dv50'</span></span> | <span data-ttu-id="cd9bf-137">MEDIASUBTYPE \_ DV50</span><span class="sxs-lookup"><span data-stu-id="cd9bf-137">MEDIASUBTYPE\_dv50</span></span> | <span data-ttu-id="cd9bf-138">50 Mbits/s</span><span class="sxs-lookup"><span data-stu-id="cd9bf-138">50 Mbps</span></span>   | <span data-ttu-id="cd9bf-139">DVCPRO 50 (525-60 ou 625-50)</span><span class="sxs-lookup"><span data-stu-id="cd9bf-139">DVCPRO 50 (525-60 or 625-50)</span></span>                |
| <span data-ttu-id="cd9bf-140">'dvh1'</span><span class="sxs-lookup"><span data-stu-id="cd9bf-140">'dvh1'</span></span> | <span data-ttu-id="cd9bf-141">MEDIASUBTYPE \_ dvh1</span><span class="sxs-lookup"><span data-stu-id="cd9bf-141">MEDIASUBTYPE\_dvh1</span></span> | <span data-ttu-id="cd9bf-142">100 Mbits/s</span><span class="sxs-lookup"><span data-stu-id="cd9bf-142">100 Mbps</span></span>  | <span data-ttu-id="cd9bf-143">DVCPRO 100 (1080/60i, 1080/50i, ou 720/60P)</span><span class="sxs-lookup"><span data-stu-id="cd9bf-143">DVCPRO 100 (1080/60i, 1080/50i, or 720/60P)</span></span> |



 

<span data-ttu-id="cd9bf-144">Pour plus d’informations sur dvh1, reportez-vous à SMPTE 314M pour plus d’informations sur DV25 et DV50, et sur SMPTE 370M.</span><span class="sxs-lookup"><span data-stu-id="cd9bf-144">Refer to SMPTE 314M for more information about dv25 and dv50, and SMPTE 370M for more information about dvh1.</span></span>

## <a name="miscellaneous"></a><span data-ttu-id="cd9bf-145">Divers</span><span class="sxs-lookup"><span data-stu-id="cd9bf-145">Miscellaneous</span></span>

<span data-ttu-id="cd9bf-146">Deux sous-types DV supplémentaires sont définis dans le fichier d’en-tête UUID. h.</span><span class="sxs-lookup"><span data-stu-id="cd9bf-146">Two additional DV subtypes are defined in the header file Uuids.h.</span></span> <span data-ttu-id="cd9bf-147">Celles-ci correspondent aux Codes FOURCC produits par certains codecs DV. elles ne correspondent à aucune norme DV définie.</span><span class="sxs-lookup"><span data-stu-id="cd9bf-147">These correspond to FOURCC codes that are produced by certain DV codecs; they do not correspond to any defined DV standards.</span></span> <span data-ttu-id="cd9bf-148">Ces sous-types sont obsolètes et ne doivent pas être utilisés.</span><span class="sxs-lookup"><span data-stu-id="cd9bf-148">These subtypes are obsolete and should not be used.</span></span>



| <span data-ttu-id="cd9bf-149">FOURCC</span><span class="sxs-lookup"><span data-stu-id="cd9bf-149">FOURCC</span></span> | <span data-ttu-id="cd9bf-150">GUID</span><span class="sxs-lookup"><span data-stu-id="cd9bf-150">GUID</span></span>               |
|--------|--------------------|
| <span data-ttu-id="cd9bf-151">MENÉS par</span><span class="sxs-lookup"><span data-stu-id="cd9bf-151">'DVCS'</span></span> | <span data-ttu-id="cd9bf-152">MEDIASUBTYPE \_ menés par</span><span class="sxs-lookup"><span data-stu-id="cd9bf-152">MEDIASUBTYPE\_DVCS</span></span> |
| <span data-ttu-id="cd9bf-153">'DVSD'</span><span class="sxs-lookup"><span data-stu-id="cd9bf-153">'DVSD'</span></span> | <span data-ttu-id="cd9bf-154">MEDIASUBTYPE \_ DVSD</span><span class="sxs-lookup"><span data-stu-id="cd9bf-154">MEDIASUBTYPE\_DVSD</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="cd9bf-155">Notes</span><span class="sxs-lookup"><span data-stu-id="cd9bf-155">Remarks</span></span>

<span data-ttu-id="cd9bf-156">Le tableau suivant indique les débits de données pris en charge, en mégabits par seconde (Mbits/s), pour les pilotes MSDV et UVC.</span><span class="sxs-lookup"><span data-stu-id="cd9bf-156">The following table shows the supported data rates, in megabits per second (Mbps), for the MSDV and UVC drivers.</span></span>



| <span data-ttu-id="cd9bf-157">Système d’exploitation</span><span class="sxs-lookup"><span data-stu-id="cd9bf-157">Operating System</span></span>                                                                 | <span data-ttu-id="cd9bf-158">Pilote MSDV (IEEE 1394)</span><span class="sxs-lookup"><span data-stu-id="cd9bf-158">MSDV (IEEE 1394) Driver</span></span> | <span data-ttu-id="cd9bf-159">Pilote UVC</span><span class="sxs-lookup"><span data-stu-id="cd9bf-159">UVC Driver</span></span>    |
|----------------------------------------------------------------------------------|-------------------------|---------------|
| <span data-ttu-id="cd9bf-160">Windows XP Service Pack 1 ou version antérieure</span><span class="sxs-lookup"><span data-stu-id="cd9bf-160">Windows XP Service Pack 1 or earlier</span></span>                                             | <span data-ttu-id="cd9bf-161">12,5, 25</span><span class="sxs-lookup"><span data-stu-id="cd9bf-161">12.5, 25</span></span>                | <span data-ttu-id="cd9bf-162">Non disponible</span><span class="sxs-lookup"><span data-stu-id="cd9bf-162">Not available</span></span> |
| <span data-ttu-id="cd9bf-163">Windows XP Service Pack 2 ou version ultérieure, Windows Server 2003 Service Pack 1 ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="cd9bf-163">Windows XP Service Pack 2 or later, Windows Server 2003 Service Pack 1 or later.</span></span> | <span data-ttu-id="cd9bf-164">12,5, 25, 50, 100</span><span class="sxs-lookup"><span data-stu-id="cd9bf-164">12.5, 25, 50, 100</span></span>       | <span data-ttu-id="cd9bf-165">12,5, 25</span><span class="sxs-lookup"><span data-stu-id="cd9bf-165">12.5, 25</span></span>      |



 

<span data-ttu-id="cd9bf-166">Pour les flux de 25 Mbits/s, le comportement du pilote MSDV a changé dans Windows Vista avant Windows Vista, le pilote MSDV a toujours défini le type de média sur MEDIASUBTYPE \_ DVSD pour les flux de 25 Mbits/s, que la source soit SDL-magnétoscope ou DVCPRO 25.</span><span class="sxs-lookup"><span data-stu-id="cd9bf-166">For 25-Mbps streams, the behavior of the MSDV driver has changed in Windows Vista Prior to Windows Vista, the MSDV driver always set the media type to MEDIASUBTYPE\_dvsd for 25-Mbps streams, regardless of whether the source was SDL-DVCR or DVCPRO 25.</span></span> <span data-ttu-id="cd9bf-167">Le type de média « DV25 » n’a pas été utilisé.</span><span class="sxs-lookup"><span data-stu-id="cd9bf-167">The 'dv25' media type was not used.</span></span> <span data-ttu-id="cd9bf-168">À compter de Windows Vista, le pilote MSDV distingue maintenant ces deux formats.</span><span class="sxs-lookup"><span data-stu-id="cd9bf-168">Starting with Windows Vista, the MSDV driver now distinguishes between these two formats.</span></span> <span data-ttu-id="cd9bf-169">Pour SDL-magnétoscope, il continue d’utiliser le sous-type « DVSD ».</span><span class="sxs-lookup"><span data-stu-id="cd9bf-169">For SDL-DVCR, it continues to use the 'dvsd' subtype.</span></span> <span data-ttu-id="cd9bf-170">Pour DVCPRO 25, elle utilise désormais le sous-type « DV25 ».</span><span class="sxs-lookup"><span data-stu-id="cd9bf-170">For DVCPRO 25, it now uses the 'dv25' subtype.</span></span>

<span data-ttu-id="cd9bf-171">Les filtres de décodage [DV](dv-splitter-filter.md) DirectShow et [DV Video](dv-video-decoder-filter.md) ne prennent en charge que les formats de magnétoscope numérique SDL.</span><span class="sxs-lookup"><span data-stu-id="cd9bf-171">The DirectShow [DV Splitter](dv-splitter-filter.md) and [DV Video Decoder](dv-video-decoder-filter.md) filters support SDL-DVCR formats only.</span></span> <span data-ttu-id="cd9bf-172">Les données peuvent être PAL ou NTSC.</span><span class="sxs-lookup"><span data-stu-id="cd9bf-172">The data can be PAL or NTSC.</span></span> <span data-ttu-id="cd9bf-173">Des filtres ou codecs tiers peuvent être disponibles pour analyser d’autres formats DV, à condition que le débit de données soit pris en charge par le pilote MSDV ou UVC.</span><span class="sxs-lookup"><span data-stu-id="cd9bf-173">Third-party filters or codecs may be available that can parse other DV formats, as long as the data rate is supported by the MSDV or UVC driver.</span></span>

## <a name="requirements"></a><span data-ttu-id="cd9bf-174">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="cd9bf-174">Requirements</span></span>



| <span data-ttu-id="cd9bf-175">Condition requise</span><span class="sxs-lookup"><span data-stu-id="cd9bf-175">Requirement</span></span> | <span data-ttu-id="cd9bf-176">Valeur</span><span class="sxs-lookup"><span data-stu-id="cd9bf-176">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="cd9bf-177">En-tête</span><span class="sxs-lookup"><span data-stu-id="cd9bf-177">Header</span></span><br/> | <dl> <span data-ttu-id="cd9bf-178"><dt>DShow. h</dt></span><span class="sxs-lookup"><span data-stu-id="cd9bf-178"><dt>Dshow.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cd9bf-179">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cd9bf-179">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cd9bf-180">Vidéo numérique dans DirectShow</span><span class="sxs-lookup"><span data-stu-id="cd9bf-180">Digital Video in DirectShow</span></span>](digital-video-in-directshow.md)
</dt> <dt>

[<span data-ttu-id="cd9bf-181">Pilote MSDV</span><span class="sxs-lookup"><span data-stu-id="cd9bf-181">MSDV Driver</span></span>](msdv-driver.md)
</dt> <dt>

[<span data-ttu-id="cd9bf-182">Sous-types de vidéos</span><span class="sxs-lookup"><span data-stu-id="cd9bf-182">Video Subtypes</span></span>](video-subtypes.md)
</dt> </dl>

 

 




