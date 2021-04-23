---
description: Types vidéo H. 264
ms.assetid: aa3166b2-6b04-44fa-bc9d-c8ff46f99201
title: Types vidéo H. 264
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 692a751e197e2e7bbb088b30dd2a3f5f199d56de
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909017"
---
# <a name="h264-video-types"></a><span data-ttu-id="76116-103">Types vidéo H. 264</span><span class="sxs-lookup"><span data-stu-id="76116-103">H.264 Video Types</span></span>

<span data-ttu-id="76116-104">Les sous-types de médias suivants sont définis pour la vidéo H. 264.</span><span class="sxs-lookup"><span data-stu-id="76116-104">The following media subtypes are defined for H.264 video.</span></span>



| <span data-ttu-id="76116-105">Subtype</span><span class="sxs-lookup"><span data-stu-id="76116-105">Subtype</span></span>                | <span data-ttu-id="76116-106">FOURCC</span><span class="sxs-lookup"><span data-stu-id="76116-106">FOURCC</span></span> | <span data-ttu-id="76116-107">Description</span><span class="sxs-lookup"><span data-stu-id="76116-107">Description</span></span>                                                    |
|------------------------|--------|----------------------------------------------------------------|
| <span data-ttu-id="76116-108">**MEDIASUBTYPE \_ AVC1**</span><span class="sxs-lookup"><span data-stu-id="76116-108">**MEDIASUBTYPE\_AVC1**</span></span> | <span data-ttu-id="76116-109">'AVC1'</span><span class="sxs-lookup"><span data-stu-id="76116-109">'AVC1'</span></span> | <span data-ttu-id="76116-110">Binaire H. 264 sans codes de démarrage.</span><span class="sxs-lookup"><span data-stu-id="76116-110">H.264 bitstream without start codes.</span></span>                           |
| <span data-ttu-id="76116-111">**MEDIASUBTYPE \_ H264 –**</span><span class="sxs-lookup"><span data-stu-id="76116-111">**MEDIASUBTYPE\_H264**</span></span> | <span data-ttu-id="76116-112">H264 –</span><span class="sxs-lookup"><span data-stu-id="76116-112">'H264'</span></span> | <span data-ttu-id="76116-113">Binaire H. 264 avec codes de démarrage.</span><span class="sxs-lookup"><span data-stu-id="76116-113">H.264 bitstream with start codes.</span></span>                              |
| <span data-ttu-id="76116-114">**MEDIASUBTYPE \_ H264 –**</span><span class="sxs-lookup"><span data-stu-id="76116-114">**MEDIASUBTYPE\_h264**</span></span> | <span data-ttu-id="76116-115">H264 –</span><span class="sxs-lookup"><span data-stu-id="76116-115">'h264'</span></span> | <span data-ttu-id="76116-116">Équivalent à **MEDIASUBTYPE \_ H264 –**, avec un FourCC différent.</span><span class="sxs-lookup"><span data-stu-id="76116-116">Equivalent to **MEDIASUBTYPE\_H264**, with a different FOURCC.</span></span> |
| <span data-ttu-id="76116-117">**MEDIASUBTYPE \_ x264**</span><span class="sxs-lookup"><span data-stu-id="76116-117">**MEDIASUBTYPE\_X264**</span></span> | <span data-ttu-id="76116-118">'X264'</span><span class="sxs-lookup"><span data-stu-id="76116-118">'X264'</span></span> | <span data-ttu-id="76116-119">Équivalent à **MEDIASUBTYPE \_ H264 –**, avec un FourCC différent.</span><span class="sxs-lookup"><span data-stu-id="76116-119">Equivalent to **MEDIASUBTYPE\_H264**, with a different FOURCC.</span></span> |
| <span data-ttu-id="76116-120">**MEDIASUBTYPE \_ x264**</span><span class="sxs-lookup"><span data-stu-id="76116-120">**MEDIASUBTYPE\_x264**</span></span> | <span data-ttu-id="76116-121">'x264'</span><span class="sxs-lookup"><span data-stu-id="76116-121">'x264'</span></span> | <span data-ttu-id="76116-122">Équivalent à **MEDIASUBTYPE \_ H264 –**, avec un FourCC différent.</span><span class="sxs-lookup"><span data-stu-id="76116-122">Equivalent to **MEDIASUBTYPE\_H264**, with a different FOURCC.</span></span> |



 

<span data-ttu-id="76116-123">Ces GUID de sous-type sont déclarés dans wmcodecdsp. h.</span><span class="sxs-lookup"><span data-stu-id="76116-123">These subtype GUIDs are declared in wmcodecdsp.h.</span></span>

<span data-ttu-id="76116-124">La principale différence entre ces types de média réside dans la présence de codes de démarrage dans le flux binaire.</span><span class="sxs-lookup"><span data-stu-id="76116-124">The main difference between these media types is the presence of start codes in the bitstream.</span></span> <span data-ttu-id="76116-125">Si le sous-type est **MEDIASUBTYPE \_ AVC1**, le flux binaire ne contient pas de codes de début.</span><span class="sxs-lookup"><span data-stu-id="76116-125">If the subtype is **MEDIASUBTYPE\_AVC1**, the bitstream does not contain start codes.</span></span>

### <a name="h264-bitstream-with-start-codes"></a><span data-ttu-id="76116-126">Binaire H. 264 avec codes de démarrage</span><span class="sxs-lookup"><span data-stu-id="76116-126">H.264 Bitstream with Start Codes</span></span>

<span data-ttu-id="76116-127">H. 264 les séquences binaires transmises à l’air, ou contenues dans des flux de programme ou de transport MPEG-2, ou enregistrées sur HD-DVD, sont mises en forme comme décrit dans l’annexe B de l’ITU-T Rec. H. 264.</span><span class="sxs-lookup"><span data-stu-id="76116-127">H.264 bitstreams that are transmitted over the air, or contained in MPEG-2 program or transport streams, or recorded on HD-DVD, are formatted as described in Annex B of ITU-T Rec. H.264.</span></span> <span data-ttu-id="76116-128">Conformément à cette spécification, le flux binaire se compose d’une séquence d’unités de couche d’abstraction de réseau (NALUs), dont chacune est précédée d’un code de démarrage égal à 0x000001 ou 0x00000001.</span><span class="sxs-lookup"><span data-stu-id="76116-128">According to this specification, the bitstream consists of a sequence of network abstraction layer units (NALUs), each of which is prefixed with a start code equal to 0x000001 or 0x00000001.</span></span>

<span data-ttu-id="76116-129">Lorsque les codes de démarrage sont présents dans le flux binaire, le type de média suivant est utilisé :</span><span class="sxs-lookup"><span data-stu-id="76116-129">When start codes are present in the bitstream, the following media type is used:</span></span>



| <span data-ttu-id="76116-130">Étiquette</span><span class="sxs-lookup"><span data-stu-id="76116-130">Label</span></span> | <span data-ttu-id="76116-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="76116-131">Value</span></span> |
|-------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="76116-132">Type principal</span><span class="sxs-lookup"><span data-stu-id="76116-132">Major type</span></span>  | <span data-ttu-id="76116-133">**Vidéo de MEDIATYPE \_**</span><span class="sxs-lookup"><span data-stu-id="76116-133">**MEDIATYPE\_Video**</span></span>                                                                              |
| <span data-ttu-id="76116-134">Sous-types</span><span class="sxs-lookup"><span data-stu-id="76116-134">Subtypes</span></span>    | <span data-ttu-id="76116-135">**MEDIASUBTYPE \_ H264 –**, **MEDIASUBTYPE \_ H264 –**, **MEDIASUBTYPE \_ x264** ou **MEDIASUBTYPE \_** x264</span><span class="sxs-lookup"><span data-stu-id="76116-135">**MEDIASUBTYPE\_H264**, **MEDIASUBTYPE\_h264**, **MEDIASUBTYPE\_X264**, or **MEDIASUBTYPE\_x264**</span></span> |
| <span data-ttu-id="76116-136">Type de format</span><span class="sxs-lookup"><span data-stu-id="76116-136">Format type</span></span> | <span data-ttu-id="76116-137">**Format \_ VideoInfo**, **format \_ VideoInfo2**, **format \_ mpeg2video** ou **GUID \_ null**</span><span class="sxs-lookup"><span data-stu-id="76116-137">**FORMAT\_VideoInfo**, **FORMAT\_VideoInfo2**, **FORMAT\_MPEG2Video**, or **GUID\_NULL**</span></span>          |



 

<span data-ttu-id="76116-138">Si le type de format **est \_ null GUID**, aucune structure de format n’est présente.</span><span class="sxs-lookup"><span data-stu-id="76116-138">If the format type is **GUID\_NULL**, no format structure is present.</span></span>

<span data-ttu-id="76116-139">Lorsque le flux binaire contient des codes de début, l’un des types de format répertoriés ici est suffisant, car le décodeur ne nécessite aucune information supplémentaire pour analyser le flux.</span><span class="sxs-lookup"><span data-stu-id="76116-139">When the bitstream contains start codes, any of the format types listed here is sufficient, because the decoder does not require any additional information to parse the stream.</span></span> <span data-ttu-id="76116-140">Le flux de données contient déjà toutes les informations requises par le décodeur, et les codes de démarrage permettent au décodeur de localiser le début de chaque NALU.</span><span class="sxs-lookup"><span data-stu-id="76116-140">The bitstream already contains all of the information needed by the decoder, and the start codes enable the decoder to locate the start of each NALU.</span></span>

<span data-ttu-id="76116-141">Les sous-types suivants sont équivalents :</span><span class="sxs-lookup"><span data-stu-id="76116-141">The following subtypes are equivalent:</span></span>

### <a name="h264-bitstream-without-start-codes"></a><span data-ttu-id="76116-142">Binaire H. 264 sans codes de démarrage</span><span class="sxs-lookup"><span data-stu-id="76116-142">H.264 Bitstream Without Start Codes</span></span>

<span data-ttu-id="76116-143">Le format de conteneur MP4 stocke les données H. 264 sans code de début.</span><span class="sxs-lookup"><span data-stu-id="76116-143">The MP4 container format stores H.264 data without start codes.</span></span> <span data-ttu-id="76116-144">Au lieu de cela, chaque NALU est précédée d’un champ de longueur, ce qui donne la longueur du NALU en octets.</span><span class="sxs-lookup"><span data-stu-id="76116-144">Instead, each NALU is prefixed by a length field, which gives the length of the NALU in bytes.</span></span> <span data-ttu-id="76116-145">La taille du champ de longueur peut varier, mais est généralement de 1, 2 ou 4 octets.</span><span class="sxs-lookup"><span data-stu-id="76116-145">The size of the length field can vary, but is typically 1, 2, or 4 bytes.</span></span>

<span data-ttu-id="76116-146">Lorsque les codes de début ne sont pas présents dans le flux binaire, le type de média suivant est utilisé.</span><span class="sxs-lookup"><span data-stu-id="76116-146">When start codes are not present in the bitstream, the following media type is used.</span></span>



| <span data-ttu-id="76116-147">Étiquette</span><span class="sxs-lookup"><span data-stu-id="76116-147">Label</span></span> | <span data-ttu-id="76116-148">Valeur</span><span class="sxs-lookup"><span data-stu-id="76116-148">Value</span></span> |
|-------------|------------------------|
| <span data-ttu-id="76116-149">Type principal</span><span class="sxs-lookup"><span data-stu-id="76116-149">Major type</span></span>  | <span data-ttu-id="76116-150">**Vidéo de MEDIATYPE \_**</span><span class="sxs-lookup"><span data-stu-id="76116-150">**MEDIATYPE\_Video**</span></span>   |
| <span data-ttu-id="76116-151">Subtype</span><span class="sxs-lookup"><span data-stu-id="76116-151">Subtype</span></span>     | <span data-ttu-id="76116-152">**MEDIASUBTYPE \_ AVC1**</span><span class="sxs-lookup"><span data-stu-id="76116-152">**MEDIASUBTYPE\_AVC1**</span></span> |
| <span data-ttu-id="76116-153">Type de format</span><span class="sxs-lookup"><span data-stu-id="76116-153">Format type</span></span> | <span data-ttu-id="76116-154">**FORMAT \_ mpeg2video**</span><span class="sxs-lookup"><span data-stu-id="76116-154">**FORMAT\_MPEG2Video**</span></span> |



 

<span data-ttu-id="76116-155">Le bloc de format est une structure [**MPEG2VIDEOINFO**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-mpeg2videoinfo) .</span><span class="sxs-lookup"><span data-stu-id="76116-155">The format block is an [**MPEG2VIDEOINFO**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-mpeg2videoinfo) structure.</span></span> <span data-ttu-id="76116-156">Cette structure doit être remplie comme suit :</span><span class="sxs-lookup"><span data-stu-id="76116-156">This structure should be filled in as follows:</span></span>

-   <span data-ttu-id="76116-157">**HDR**: structure [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) qui décrit le flux binaire.</span><span class="sxs-lookup"><span data-stu-id="76116-157">**hdr**: A [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) structure that describes the bitstream.</span></span> <span data-ttu-id="76116-158">Aucune table de couleurs n’est présente après la partie [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) de la structure, et **biClrUsed** doit être égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="76116-158">No color table is present after the [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) portion of the structure, and **biClrUsed** must be zero.</span></span>
-   <span data-ttu-id="76116-159">**dwStartTimeCode**: non utilisé.</span><span class="sxs-lookup"><span data-stu-id="76116-159">**dwStartTimeCode**: Not used.</span></span> <span data-ttu-id="76116-160">Définit la valeur zéro.</span><span class="sxs-lookup"><span data-stu-id="76116-160">Set to zero.</span></span>
-   <span data-ttu-id="76116-161">**cbSequenceHeader**: longueur du tableau **dwSequenceHeader** en octets.</span><span class="sxs-lookup"><span data-stu-id="76116-161">**cbSequenceHeader**: The length of the **dwSequenceHeader** array in bytes.</span></span>
-   <span data-ttu-id="76116-162">**dwProfile**: spécifie le profil H. 264.</span><span class="sxs-lookup"><span data-stu-id="76116-162">**dwProfile**: Specifies the H.264 profile.</span></span>
-   <span data-ttu-id="76116-163">**dwLevel**: spécifie le niveau H. 264.</span><span class="sxs-lookup"><span data-stu-id="76116-163">**dwLevel**: Specifies the H.264 level.</span></span>
-   <span data-ttu-id="76116-164">**dwFlags**: nombre d’octets utilisés pour le champ de longueur qui apparaît avant chaque **Nalu**.</span><span class="sxs-lookup"><span data-stu-id="76116-164">**dwFlags**: The number of bytes used for the length field that appears before each **NALU**.</span></span> <span data-ttu-id="76116-165">Le champ longueur indique la taille du NALU suivant en octets.</span><span class="sxs-lookup"><span data-stu-id="76116-165">The length field indicates the size of the following NALU in bytes.</span></span> <span data-ttu-id="76116-166">Par exemple, si **dwFlags** est 4, chaque Nalu est précédé d’un champ de longueur de 4 octets.</span><span class="sxs-lookup"><span data-stu-id="76116-166">For example, if **dwFlags** is 4, each NALU is preceded by a 4-byte length field.</span></span> <span data-ttu-id="76116-167">Les valeurs valides sont 1, 2 et 4.</span><span class="sxs-lookup"><span data-stu-id="76116-167">The valid values are 1, 2, and 4.</span></span>
-   <span data-ttu-id="76116-168">**dwSequenceHeader**: tableau d’octets qui peut contenir un jeu de paramètres de séquence (SPS) et un jeu de paramètres d’image (PPS) NALUs.</span><span class="sxs-lookup"><span data-stu-id="76116-168">**dwSequenceHeader**: A byte array that may contain sequence parameter set (SPS) and picture parameter set (PPS) NALUs.</span></span>

<span data-ttu-id="76116-169">Le conteneur MP4 peut contenir des jeux de paramètres de séquence (SPS) ou des jeux de paramètres d’image (PPS) en tant qu’unités NAL spéciales dans les en-têtes de fichier ou dans un flux distinct (distinct du flux vidéo).</span><span class="sxs-lookup"><span data-stu-id="76116-169">The MP4 container might contain sequence parameter sets (SPS) or picture parameter sets (PPS) as special NAL units in file headers or in a separate stream (distinct from the video stream).</span></span> <span data-ttu-id="76116-170">Lorsque le format est établi, le type de média peut spécifier des unités SPS et PPS NAL dans le tableau **dwSequenceHeader** .</span><span class="sxs-lookup"><span data-stu-id="76116-170">When the format is established, the media type can specify SPS and PPS NAL units in the **dwSequenceHeader** array.</span></span> <span data-ttu-id="76116-171">Si **cbSequenceHeader** est supérieur à zéro, **dwSequenceHeader** est le début d’un tableau d’octets contenant les NALUs SPS et PPS, délimités par les champs de longueur de 2 octets, tous dans l’ordre d’octet réseau (Big-endian).</span><span class="sxs-lookup"><span data-stu-id="76116-171">If **cbSequenceHeader** is greater than zero, **dwSequenceHeader** is the start of a byte array containing SPS and PPS NALUs, delimited by 2-byte length fields, all in network byte order (big-endian).</span></span> <span data-ttu-id="76116-172">Il est possible d’avoir à la fois SPS et PPS, un seul de ces types, ou aucun.</span><span class="sxs-lookup"><span data-stu-id="76116-172">It is possible to have both SPS and PPS, only one of these types, or none.</span></span> <span data-ttu-id="76116-173">Le type réel de chaque NALU peut être déterminé en examinant le champ **\_ \_ type d’unité nal** du Nalu lui-même.</span><span class="sxs-lookup"><span data-stu-id="76116-173">The actual type of each NALU can be determined by examining the **nal\_unit\_type** field of the NALU itself.</span></span>

<span data-ttu-id="76116-174">Lorsque ce type de média est utilisé, chaque exemple de support commence au début d’un NALU, et les unités NAL n’englobent pas les échantillons.</span><span class="sxs-lookup"><span data-stu-id="76116-174">When this media type is used, each media sample starts at the beginning of a NALU, and NAL units do not span samples.</span></span> <span data-ttu-id="76116-175">Cela permet au décodeur de récupérer des données endommagées ou des échantillons supprimés.</span><span class="sxs-lookup"><span data-stu-id="76116-175">This enables the decoder to recover from data corruption or dropped samples.</span></span>

 

 



