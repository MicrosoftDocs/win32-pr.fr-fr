---
description: Types vidéo H. 264
ms.assetid: aa3166b2-6b04-44fa-bc9d-c8ff46f99201
title: Types vidéo H. 264
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2dcd33703798e305947cdcd663c7a86c7c494683
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103949952"
---
# <a name="h264-video-types"></a><span data-ttu-id="e6d8a-103">Types vidéo H. 264</span><span class="sxs-lookup"><span data-stu-id="e6d8a-103">H.264 Video Types</span></span>

<span data-ttu-id="e6d8a-104">Les sous-types de médias suivants sont définis pour la vidéo H. 264.</span><span class="sxs-lookup"><span data-stu-id="e6d8a-104">The following media subtypes are defined for H.264 video.</span></span>



| <span data-ttu-id="e6d8a-105">Subtype</span><span class="sxs-lookup"><span data-stu-id="e6d8a-105">Subtype</span></span>                | <span data-ttu-id="e6d8a-106">FOURCC</span><span class="sxs-lookup"><span data-stu-id="e6d8a-106">FOURCC</span></span> | <span data-ttu-id="e6d8a-107">Description</span><span class="sxs-lookup"><span data-stu-id="e6d8a-107">Description</span></span>                                                    |
|------------------------|--------|----------------------------------------------------------------|
| <span data-ttu-id="e6d8a-108">**MEDIASUBTYPE \_ AVC1**</span><span class="sxs-lookup"><span data-stu-id="e6d8a-108">**MEDIASUBTYPE\_AVC1**</span></span> | <span data-ttu-id="e6d8a-109">'AVC1'</span><span class="sxs-lookup"><span data-stu-id="e6d8a-109">'AVC1'</span></span> | <span data-ttu-id="e6d8a-110">Binaire H. 264 sans codes de démarrage.</span><span class="sxs-lookup"><span data-stu-id="e6d8a-110">H.264 bitstream without start codes.</span></span>                           |
| <span data-ttu-id="e6d8a-111">**MEDIASUBTYPE \_ H264 –**</span><span class="sxs-lookup"><span data-stu-id="e6d8a-111">**MEDIASUBTYPE\_H264**</span></span> | <span data-ttu-id="e6d8a-112">H264 –</span><span class="sxs-lookup"><span data-stu-id="e6d8a-112">'H264'</span></span> | <span data-ttu-id="e6d8a-113">Binaire H. 264 avec codes de démarrage.</span><span class="sxs-lookup"><span data-stu-id="e6d8a-113">H.264 bitstream with start codes.</span></span>                              |
| <span data-ttu-id="e6d8a-114">**MEDIASUBTYPE \_ H264 –**</span><span class="sxs-lookup"><span data-stu-id="e6d8a-114">**MEDIASUBTYPE\_h264**</span></span> | <span data-ttu-id="e6d8a-115">H264 –</span><span class="sxs-lookup"><span data-stu-id="e6d8a-115">'h264'</span></span> | <span data-ttu-id="e6d8a-116">Équivalent à **MEDIASUBTYPE \_ H264 –**, avec un FourCC différent.</span><span class="sxs-lookup"><span data-stu-id="e6d8a-116">Equivalent to **MEDIASUBTYPE\_H264**, with a different FOURCC.</span></span> |
| <span data-ttu-id="e6d8a-117">**MEDIASUBTYPE \_ x264**</span><span class="sxs-lookup"><span data-stu-id="e6d8a-117">**MEDIASUBTYPE\_X264**</span></span> | <span data-ttu-id="e6d8a-118">'X264'</span><span class="sxs-lookup"><span data-stu-id="e6d8a-118">'X264'</span></span> | <span data-ttu-id="e6d8a-119">Équivalent à **MEDIASUBTYPE \_ H264 –**, avec un FourCC différent.</span><span class="sxs-lookup"><span data-stu-id="e6d8a-119">Equivalent to **MEDIASUBTYPE\_H264**, with a different FOURCC.</span></span> |
| <span data-ttu-id="e6d8a-120">**MEDIASUBTYPE \_ x264**</span><span class="sxs-lookup"><span data-stu-id="e6d8a-120">**MEDIASUBTYPE\_x264**</span></span> | <span data-ttu-id="e6d8a-121">'x264'</span><span class="sxs-lookup"><span data-stu-id="e6d8a-121">'x264'</span></span> | <span data-ttu-id="e6d8a-122">Équivalent à **MEDIASUBTYPE \_ H264 –**, avec un FourCC différent.</span><span class="sxs-lookup"><span data-stu-id="e6d8a-122">Equivalent to **MEDIASUBTYPE\_H264**, with a different FOURCC.</span></span> |



 

<span data-ttu-id="e6d8a-123">Ces GUID de sous-type sont déclarés dans wmcodecdsp. h.</span><span class="sxs-lookup"><span data-stu-id="e6d8a-123">These subtype GUIDs are declared in wmcodecdsp.h.</span></span>

<span data-ttu-id="e6d8a-124">La principale différence entre ces types de média réside dans la présence de codes de démarrage dans le flux binaire.</span><span class="sxs-lookup"><span data-stu-id="e6d8a-124">The main difference between these media types is the presence of start codes in the bitstream.</span></span> <span data-ttu-id="e6d8a-125">Si le sous-type est **MEDIASUBTYPE \_ AVC1**, le flux binaire ne contient pas de codes de début.</span><span class="sxs-lookup"><span data-stu-id="e6d8a-125">If the subtype is **MEDIASUBTYPE\_AVC1**, the bitstream does not contain start codes.</span></span>

### <a name="h264-bitstream-with-start-codes"></a><span data-ttu-id="e6d8a-126">Binaire H. 264 avec codes de démarrage</span><span class="sxs-lookup"><span data-stu-id="e6d8a-126">H.264 Bitstream with Start Codes</span></span>

<span data-ttu-id="e6d8a-127">H. 264 les séquences binaires transmises à l’air, ou contenues dans des flux de programme ou de transport MPEG-2, ou enregistrées sur HD-DVD, sont mises en forme comme décrit dans l’annexe B de l’ITU-T Rec. H. 264.</span><span class="sxs-lookup"><span data-stu-id="e6d8a-127">H.264 bitstreams that are transmitted over the air, or contained in MPEG-2 program or transport streams, or recorded on HD-DVD, are formatted as described in Annex B of ITU-T Rec. H.264.</span></span> <span data-ttu-id="e6d8a-128">Conformément à cette spécification, le flux binaire se compose d’une séquence d’unités de couche d’abstraction de réseau (NALUs), dont chacune est précédée d’un code de démarrage égal à 0x000001 ou 0x00000001.</span><span class="sxs-lookup"><span data-stu-id="e6d8a-128">According to this specification, the bitstream consists of a sequence of network abstraction layer units (NALUs), each of which is prefixed with a start code equal to 0x000001 or 0x00000001.</span></span>

<span data-ttu-id="e6d8a-129">Lorsque les codes de démarrage sont présents dans le flux binaire, le type de média suivant est utilisé :</span><span class="sxs-lookup"><span data-stu-id="e6d8a-129">When start codes are present in the bitstream, the following media type is used:</span></span>



|             |                                                                                                   |
|-------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e6d8a-130">Type principal</span><span class="sxs-lookup"><span data-stu-id="e6d8a-130">Major type</span></span>  | <span data-ttu-id="e6d8a-131">**Vidéo de MEDIATYPE \_**</span><span class="sxs-lookup"><span data-stu-id="e6d8a-131">**MEDIATYPE\_Video**</span></span>                                                                              |
| <span data-ttu-id="e6d8a-132">Sous-types</span><span class="sxs-lookup"><span data-stu-id="e6d8a-132">Subtypes</span></span>    | <span data-ttu-id="e6d8a-133">**MEDIASUBTYPE \_ H264 –**, **MEDIASUBTYPE \_ H264 –**, **MEDIASUBTYPE \_ x264** ou **MEDIASUBTYPE \_** x264</span><span class="sxs-lookup"><span data-stu-id="e6d8a-133">**MEDIASUBTYPE\_H264**, **MEDIASUBTYPE\_h264**, **MEDIASUBTYPE\_X264**, or **MEDIASUBTYPE\_x264**</span></span> |
| <span data-ttu-id="e6d8a-134">Type de format</span><span class="sxs-lookup"><span data-stu-id="e6d8a-134">Format type</span></span> | <span data-ttu-id="e6d8a-135">**Format \_ VideoInfo**, **format \_ VideoInfo2**, **format \_ mpeg2video** ou **GUID \_ null**</span><span class="sxs-lookup"><span data-stu-id="e6d8a-135">**FORMAT\_VideoInfo**, **FORMAT\_VideoInfo2**, **FORMAT\_MPEG2Video**, or **GUID\_NULL**</span></span>          |



 

<span data-ttu-id="e6d8a-136">Si le type de format **est \_ null GUID**, aucune structure de format n’est présente.</span><span class="sxs-lookup"><span data-stu-id="e6d8a-136">If the format type is **GUID\_NULL**, no format structure is present.</span></span>

<span data-ttu-id="e6d8a-137">Lorsque le flux binaire contient des codes de début, l’un des types de format répertoriés ici est suffisant, car le décodeur ne nécessite aucune information supplémentaire pour analyser le flux.</span><span class="sxs-lookup"><span data-stu-id="e6d8a-137">When the bitstream contains start codes, any of the format types listed here is sufficient, because the decoder does not require any additional information to parse the stream.</span></span> <span data-ttu-id="e6d8a-138">Le flux de données contient déjà toutes les informations requises par le décodeur, et les codes de démarrage permettent au décodeur de localiser le début de chaque NALU.</span><span class="sxs-lookup"><span data-stu-id="e6d8a-138">The bitstream already contains all of the information needed by the decoder, and the start codes enable the decoder to locate the start of each NALU.</span></span>

<span data-ttu-id="e6d8a-139">Les sous-types suivants sont équivalents :</span><span class="sxs-lookup"><span data-stu-id="e6d8a-139">The following subtypes are equivalent:</span></span>

### <a name="h264-bitstream-without-start-codes"></a><span data-ttu-id="e6d8a-140">Binaire H. 264 sans codes de démarrage</span><span class="sxs-lookup"><span data-stu-id="e6d8a-140">H.264 Bitstream Without Start Codes</span></span>

<span data-ttu-id="e6d8a-141">Le format de conteneur MP4 stocke les données H. 264 sans code de début.</span><span class="sxs-lookup"><span data-stu-id="e6d8a-141">The MP4 container format stores H.264 data without start codes.</span></span> <span data-ttu-id="e6d8a-142">Au lieu de cela, chaque NALU est précédée d’un champ de longueur, ce qui donne la longueur du NALU en octets.</span><span class="sxs-lookup"><span data-stu-id="e6d8a-142">Instead, each NALU is prefixed by a length field, which gives the length of the NALU in bytes.</span></span> <span data-ttu-id="e6d8a-143">La taille du champ de longueur peut varier, mais est généralement de 1, 2 ou 4 octets.</span><span class="sxs-lookup"><span data-stu-id="e6d8a-143">The size of the length field can vary, but is typically 1, 2, or 4 bytes.</span></span>

<span data-ttu-id="e6d8a-144">Lorsque les codes de début ne sont pas présents dans le flux binaire, le type de média suivant est utilisé.</span><span class="sxs-lookup"><span data-stu-id="e6d8a-144">When start codes are not present in the bitstream, the following media type is used.</span></span>



|             |                        |
|-------------|------------------------|
| <span data-ttu-id="e6d8a-145">Type principal</span><span class="sxs-lookup"><span data-stu-id="e6d8a-145">Major type</span></span>  | <span data-ttu-id="e6d8a-146">**Vidéo de MEDIATYPE \_**</span><span class="sxs-lookup"><span data-stu-id="e6d8a-146">**MEDIATYPE\_Video**</span></span>   |
| <span data-ttu-id="e6d8a-147">Subtype</span><span class="sxs-lookup"><span data-stu-id="e6d8a-147">Subtype</span></span>     | <span data-ttu-id="e6d8a-148">**MEDIASUBTYPE \_ AVC1**</span><span class="sxs-lookup"><span data-stu-id="e6d8a-148">**MEDIASUBTYPE\_AVC1**</span></span> |
| <span data-ttu-id="e6d8a-149">Type de format</span><span class="sxs-lookup"><span data-stu-id="e6d8a-149">Format type</span></span> | <span data-ttu-id="e6d8a-150">**FORMAT \_ mpeg2video**</span><span class="sxs-lookup"><span data-stu-id="e6d8a-150">**FORMAT\_MPEG2Video**</span></span> |



 

<span data-ttu-id="e6d8a-151">Le bloc de format est une structure [**MPEG2VIDEOINFO**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-mpeg2videoinfo) .</span><span class="sxs-lookup"><span data-stu-id="e6d8a-151">The format block is an [**MPEG2VIDEOINFO**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-mpeg2videoinfo) structure.</span></span> <span data-ttu-id="e6d8a-152">Cette structure doit être remplie comme suit :</span><span class="sxs-lookup"><span data-stu-id="e6d8a-152">This structure should be filled in as follows:</span></span>

-   <span data-ttu-id="e6d8a-153">**HDR**: structure [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) qui décrit le flux binaire.</span><span class="sxs-lookup"><span data-stu-id="e6d8a-153">**hdr**: A [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) structure that describes the bitstream.</span></span> <span data-ttu-id="e6d8a-154">Aucune table de couleurs n’est présente après la partie [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) de la structure, et **biClrUsed** doit être égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="e6d8a-154">No color table is present after the [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) portion of the structure, and **biClrUsed** must be zero.</span></span>
-   <span data-ttu-id="e6d8a-155">**dwStartTimeCode**: non utilisé.</span><span class="sxs-lookup"><span data-stu-id="e6d8a-155">**dwStartTimeCode**: Not used.</span></span> <span data-ttu-id="e6d8a-156">Définit la valeur zéro.</span><span class="sxs-lookup"><span data-stu-id="e6d8a-156">Set to zero.</span></span>
-   <span data-ttu-id="e6d8a-157">**cbSequenceHeader**: longueur du tableau **dwSequenceHeader** en octets.</span><span class="sxs-lookup"><span data-stu-id="e6d8a-157">**cbSequenceHeader**: The length of the **dwSequenceHeader** array in bytes.</span></span>
-   <span data-ttu-id="e6d8a-158">**dwProfile**: spécifie le profil H. 264.</span><span class="sxs-lookup"><span data-stu-id="e6d8a-158">**dwProfile**: Specifies the H.264 profile.</span></span>
-   <span data-ttu-id="e6d8a-159">**dwLevel**: spécifie le niveau H. 264.</span><span class="sxs-lookup"><span data-stu-id="e6d8a-159">**dwLevel**: Specifies the H.264 level.</span></span>
-   <span data-ttu-id="e6d8a-160">**dwFlags**: nombre d’octets utilisés pour le champ de longueur qui apparaît avant chaque **Nalu**.</span><span class="sxs-lookup"><span data-stu-id="e6d8a-160">**dwFlags**: The number of bytes used for the length field that appears before each **NALU**.</span></span> <span data-ttu-id="e6d8a-161">Le champ longueur indique la taille du NALU suivant en octets.</span><span class="sxs-lookup"><span data-stu-id="e6d8a-161">The length field indicates the size of the following NALU in bytes.</span></span> <span data-ttu-id="e6d8a-162">Par exemple, si **dwFlags** est 4, chaque Nalu est précédé d’un champ de longueur de 4 octets.</span><span class="sxs-lookup"><span data-stu-id="e6d8a-162">For example, if **dwFlags** is 4, each NALU is preceded by a 4-byte length field.</span></span> <span data-ttu-id="e6d8a-163">Les valeurs valides sont 1, 2 et 4.</span><span class="sxs-lookup"><span data-stu-id="e6d8a-163">The valid values are 1, 2, and 4.</span></span>
-   <span data-ttu-id="e6d8a-164">**dwSequenceHeader**: tableau d’octets qui peut contenir un jeu de paramètres de séquence (SPS) et un jeu de paramètres d’image (PPS) NALUs.</span><span class="sxs-lookup"><span data-stu-id="e6d8a-164">**dwSequenceHeader**: A byte array that may contain sequence parameter set (SPS) and picture parameter set (PPS) NALUs.</span></span>

<span data-ttu-id="e6d8a-165">Le conteneur MP4 peut contenir des jeux de paramètres de séquence (SPS) ou des jeux de paramètres d’image (PPS) en tant qu’unités NAL spéciales dans les en-têtes de fichier ou dans un flux distinct (distinct du flux vidéo).</span><span class="sxs-lookup"><span data-stu-id="e6d8a-165">The MP4 container might contain sequence parameter sets (SPS) or picture parameter sets (PPS) as special NAL units in file headers or in a separate stream (distinct from the video stream).</span></span> <span data-ttu-id="e6d8a-166">Lorsque le format est établi, le type de média peut spécifier des unités SPS et PPS NAL dans le tableau **dwSequenceHeader** .</span><span class="sxs-lookup"><span data-stu-id="e6d8a-166">When the format is established, the media type can specify SPS and PPS NAL units in the **dwSequenceHeader** array.</span></span> <span data-ttu-id="e6d8a-167">Si **cbSequenceHeader** est supérieur à zéro, **dwSequenceHeader** est le début d’un tableau d’octets contenant les NALUs SPS et PPS, délimités par les champs de longueur de 2 octets, tous dans l’ordre d’octet réseau (Big-endian).</span><span class="sxs-lookup"><span data-stu-id="e6d8a-167">If **cbSequenceHeader** is greater than zero, **dwSequenceHeader** is the start of a byte array containing SPS and PPS NALUs, delimited by 2-byte length fields, all in network byte order (big-endian).</span></span> <span data-ttu-id="e6d8a-168">Il est possible d’avoir à la fois SPS et PPS, un seul de ces types, ou aucun.</span><span class="sxs-lookup"><span data-stu-id="e6d8a-168">It is possible to have both SPS and PPS, only one of these types, or none.</span></span> <span data-ttu-id="e6d8a-169">Le type réel de chaque NALU peut être déterminé en examinant le champ **\_ \_ type d’unité nal** du Nalu lui-même.</span><span class="sxs-lookup"><span data-stu-id="e6d8a-169">The actual type of each NALU can be determined by examining the **nal\_unit\_type** field of the NALU itself.</span></span>

<span data-ttu-id="e6d8a-170">Lorsque ce type de média est utilisé, chaque exemple de support commence au début d’un NALU, et les unités NAL n’englobent pas les échantillons.</span><span class="sxs-lookup"><span data-stu-id="e6d8a-170">When this media type is used, each media sample starts at the beginning of a NALU, and NAL units do not span samples.</span></span> <span data-ttu-id="e6d8a-171">Cela permet au décodeur de récupérer des données endommagées ou des échantillons supprimés.</span><span class="sxs-lookup"><span data-stu-id="e6d8a-171">This enables the decoder to recover from data corruption or dropped samples.</span></span>

 

 



