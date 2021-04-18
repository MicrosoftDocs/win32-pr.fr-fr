---
description: Spécifie les marqueurs dans un fichier ASF (Advanced Systems Format). Cet attribut correspond à l’objet marqueur dans l’en-tête ASF, défini dans la spécification ASF.
ms.assetid: 6458eb5f-72a2-4723-b26b-b63516aa2df3
title: Attribut MF_PD_ASF_MARKER (Wmcontainer. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d2ae9c5a6cfd79924b95a3b15a7146539d630aad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106522735"
---
# <a name="mf_pd_asf_marker-attribute"></a><span data-ttu-id="1f206-104">\_Attribut de \_ \_ marqueur ASF pour MF</span><span class="sxs-lookup"><span data-stu-id="1f206-104">MF\_PD\_ASF\_MARKER attribute</span></span>

<span data-ttu-id="1f206-105">Spécifie les marqueurs dans un fichier ASF (Advanced Systems Format).</span><span class="sxs-lookup"><span data-stu-id="1f206-105">Specifies the markers in an Advanced Systems Format (ASF) file.</span></span> <span data-ttu-id="1f206-106">Cet attribut correspond à l’objet marqueur dans l’en-tête ASF, défini dans la spécification ASF.</span><span class="sxs-lookup"><span data-stu-id="1f206-106">This attribute corresponds to the Marker Object in the ASF header, defined in the ASF specification.</span></span>

## <a name="data-type"></a><span data-ttu-id="1f206-107">Type de données</span><span class="sxs-lookup"><span data-stu-id="1f206-107">Data type</span></span>

<span data-ttu-id="1f206-108">Tableau d’octets</span><span class="sxs-lookup"><span data-stu-id="1f206-108">Byte array</span></span>

## <a name="remarks"></a><span data-ttu-id="1f206-109">Notes</span><span class="sxs-lookup"><span data-stu-id="1f206-109">Remarks</span></span>

<span data-ttu-id="1f206-110">Cet attribut s’applique aux descripteurs de présentation pour le contenu ASF.</span><span class="sxs-lookup"><span data-stu-id="1f206-110">This attribute applies to presentation descriptors for ASF content.</span></span>

<span data-ttu-id="1f206-111">La méthode [**IMFASFContentInfo :: GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) crée le descripteur de présentation et génère cet attribut à partir de l’objet marqueur.</span><span class="sxs-lookup"><span data-stu-id="1f206-111">The [**IMFASFContentInfo::GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) method creates the presentation descriptor and generates this attribute from the Marker Object.</span></span> <span data-ttu-id="1f206-112">Le tableau suivant indique le format de l’objet BLOB :</span><span class="sxs-lookup"><span data-stu-id="1f206-112">The following table shows the format of the blob:</span></span>



| <span data-ttu-id="1f206-113">Champ d’objet de marqueur</span><span class="sxs-lookup"><span data-stu-id="1f206-113">Marker Object field</span></span> | <span data-ttu-id="1f206-114">Type de données</span><span class="sxs-lookup"><span data-stu-id="1f206-114">Data type</span></span>    | <span data-ttu-id="1f206-115">Taille</span><span class="sxs-lookup"><span data-stu-id="1f206-115">Size</span></span>    | <span data-ttu-id="1f206-116">Description</span><span class="sxs-lookup"><span data-stu-id="1f206-116">Description</span></span>       |
|---------------------|--------------|---------|-------------------|
| <span data-ttu-id="1f206-117">Nombre de marqueurs</span><span class="sxs-lookup"><span data-stu-id="1f206-117">Markers Count</span></span>       | <span data-ttu-id="1f206-118">**GRANDE**</span><span class="sxs-lookup"><span data-stu-id="1f206-118">**DWORD**</span></span>    | <span data-ttu-id="1f206-119">4 octets</span><span class="sxs-lookup"><span data-stu-id="1f206-119">4 bytes</span></span> | <span data-ttu-id="1f206-120">Nombre de marqueurs</span><span class="sxs-lookup"><span data-stu-id="1f206-120">Number of markers</span></span> |
| <span data-ttu-id="1f206-121">Marqueurs</span><span class="sxs-lookup"><span data-stu-id="1f206-121">Markers</span></span>             | <span data-ttu-id="1f206-122">**POIDS**\[\]</span><span class="sxs-lookup"><span data-stu-id="1f206-122">**BYTE**\[\]</span></span> | <span data-ttu-id="1f206-123">Variable</span><span class="sxs-lookup"><span data-stu-id="1f206-123">Varies</span></span>  | <span data-ttu-id="1f206-124">Tableau de marqueurs</span><span class="sxs-lookup"><span data-stu-id="1f206-124">Array of markers</span></span>  |



 

<span data-ttu-id="1f206-125">Le premier **DWORD** est le nombre de marqueurs, suivi d’un tableau de marqueurs.</span><span class="sxs-lookup"><span data-stu-id="1f206-125">The first **DWORD** is the number of markers, followed by an array of markers.</span></span> <span data-ttu-id="1f206-126">Chaque marqueur a le format suivant :</span><span class="sxs-lookup"><span data-stu-id="1f206-126">Each marker has the following format:</span></span>



| <span data-ttu-id="1f206-127">Champ d’objet de marqueur</span><span class="sxs-lookup"><span data-stu-id="1f206-127">Marker Object field</span></span>       | <span data-ttu-id="1f206-128">Type de données</span><span class="sxs-lookup"><span data-stu-id="1f206-128">Data type</span></span>     | <span data-ttu-id="1f206-129">Taille</span><span class="sxs-lookup"><span data-stu-id="1f206-129">Size</span></span>    | <span data-ttu-id="1f206-130">Description</span><span class="sxs-lookup"><span data-stu-id="1f206-130">Description</span></span>                                                                       |
|---------------------------|---------------|---------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="1f206-131">Longueur de la description du marqueur</span><span class="sxs-lookup"><span data-stu-id="1f206-131">Marker Description Length</span></span> | <span data-ttu-id="1f206-132">**GRANDE**</span><span class="sxs-lookup"><span data-stu-id="1f206-132">**DWORD**</span></span>     | <span data-ttu-id="1f206-133">4 octets</span><span class="sxs-lookup"><span data-stu-id="1f206-133">4 bytes</span></span> | <span data-ttu-id="1f206-134">Taille, en octets, de la chaîne de description, y compris le caractère NULL.</span><span class="sxs-lookup"><span data-stu-id="1f206-134">Size of the description string, in bytes, including the NULL character.</span></span>           |
| <span data-ttu-id="1f206-135">Description du marqueur</span><span class="sxs-lookup"><span data-stu-id="1f206-135">Marker Description</span></span>        | <span data-ttu-id="1f206-136">**WCHAR**\[\]</span><span class="sxs-lookup"><span data-stu-id="1f206-136">**WCHAR**\[\]</span></span> | <span data-ttu-id="1f206-137">Variable</span><span class="sxs-lookup"><span data-stu-id="1f206-137">Varies</span></span>  | <span data-ttu-id="1f206-138">Chaîne terminée par le caractère null qui décrit le marqueur.</span><span class="sxs-lookup"><span data-stu-id="1f206-138">Null-terminated string that describes the marker.</span></span>                                 |
| <span data-ttu-id="1f206-139">Heure de présentation</span><span class="sxs-lookup"><span data-stu-id="1f206-139">Presentation Time</span></span>         | <span data-ttu-id="1f206-140">**LONGLONG**</span><span class="sxs-lookup"><span data-stu-id="1f206-140">**LONGLONG**</span></span>  | <span data-ttu-id="1f206-141">8 octets</span><span class="sxs-lookup"><span data-stu-id="1f206-141">8 bytes</span></span> | <span data-ttu-id="1f206-142">Heure de présentation du marqueur, en unités de 100 nanosecondes.</span><span class="sxs-lookup"><span data-stu-id="1f206-142">Presentation time of the marker, in 100-nanosecond units.</span></span>                         |
| <span data-ttu-id="1f206-143">Heure d’envoi</span><span class="sxs-lookup"><span data-stu-id="1f206-143">Send Time</span></span>                 | <span data-ttu-id="1f206-144">**LONGLONG**</span><span class="sxs-lookup"><span data-stu-id="1f206-144">**LONGLONG**</span></span>  | <span data-ttu-id="1f206-145">8 octets</span><span class="sxs-lookup"><span data-stu-id="1f206-145">8 bytes</span></span> | <span data-ttu-id="1f206-146">Heure d’envoi de l’entrée du marqueur, en millisecondes.</span><span class="sxs-lookup"><span data-stu-id="1f206-146">Send time of the marker entry, in milliseconds.</span></span>                                   |
| <span data-ttu-id="1f206-147">Offset</span><span class="sxs-lookup"><span data-stu-id="1f206-147">Offset</span></span>                    | <span data-ttu-id="1f206-148">**UINT64**</span><span class="sxs-lookup"><span data-stu-id="1f206-148">**UINT64**</span></span>    | <span data-ttu-id="1f206-149">8 octets</span><span class="sxs-lookup"><span data-stu-id="1f206-149">8 bytes</span></span> | <span data-ttu-id="1f206-150">Décalage, en octets, de l’objet de données qui spécifie la position du marché.</span><span class="sxs-lookup"><span data-stu-id="1f206-150">Offset, in bytes, into the Data Object that specifies the position of the market.</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="1f206-151">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1f206-151">Requirements</span></span>



| <span data-ttu-id="1f206-152">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1f206-152">Requirement</span></span> | <span data-ttu-id="1f206-153">Valeur</span><span class="sxs-lookup"><span data-stu-id="1f206-153">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="1f206-154">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1f206-154">Minimum supported client</span></span><br/> | <span data-ttu-id="1f206-155">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1f206-155">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="1f206-156">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1f206-156">Minimum supported server</span></span><br/> | <span data-ttu-id="1f206-157">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1f206-157">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="1f206-158">En-tête</span><span class="sxs-lookup"><span data-stu-id="1f206-158">Header</span></span><br/>                   | <dl> <span data-ttu-id="1f206-159"><dt>Wmcontainer. h</dt></span><span class="sxs-lookup"><span data-stu-id="1f206-159"><dt>Wmcontainer.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1f206-160">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1f206-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1f206-161">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="1f206-161">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="1f206-162">**IMFAttributes :: GetBlob**</span><span class="sxs-lookup"><span data-stu-id="1f206-162">**IMFAttributes::GetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)
</dt> <dt>

[<span data-ttu-id="1f206-163">**IMFAttributes :: SetBlob**</span><span class="sxs-lookup"><span data-stu-id="1f206-163">**IMFAttributes::SetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)
</dt> <dt>

[<span data-ttu-id="1f206-164">**IMFPresentationDescriptor**</span><span class="sxs-lookup"><span data-stu-id="1f206-164">**IMFPresentationDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[<span data-ttu-id="1f206-165">Attributs du descripteur de présentation</span><span class="sxs-lookup"><span data-stu-id="1f206-165">Presentation Descriptor Attributes</span></span>](presentation-descriptor-attributes.md)
</dt> <dt>

[<span data-ttu-id="1f206-166">Objet d’en-tête ASF</span><span class="sxs-lookup"><span data-stu-id="1f206-166">ASF Header Object</span></span>](asf-file-structure.md)
</dt> <dt>

[<span data-ttu-id="1f206-167">Descripteurs de présentation</span><span class="sxs-lookup"><span data-stu-id="1f206-167">Presentation Descriptors</span></span>](presentation-descriptors.md)
</dt> </dl>

 

 




