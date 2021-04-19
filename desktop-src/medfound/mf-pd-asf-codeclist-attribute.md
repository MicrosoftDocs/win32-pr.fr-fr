---
description: Contient des informations sur les codecs et les formats utilisés pour encoder le contenu dans un fichier ASF (Advanced Systems Format). Cet attribut correspond à l’objet de liste de codec dans l’en-tête ASF, défini dans la spécification ASF.
ms.assetid: 6dde30d3-dbdc-469c-ad7e-5e670b7e0a64
title: Attribut MF_PD_ASF_CODECLIST (Wmcontainer. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 402c53c082ae57fed444168c559f99718322f8a9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106528286"
---
# <a name="mf_pd_asf_codeclist-attribute"></a><span data-ttu-id="c57c5-104">\_ \_ Attribut CODECLIST MF PD ASF \_</span><span class="sxs-lookup"><span data-stu-id="c57c5-104">MF\_PD\_ASF\_CODECLIST attribute</span></span>

<span data-ttu-id="c57c5-105">Contient des informations sur les codecs et les formats utilisés pour encoder le contenu dans un fichier ASF (Advanced Systems Format).</span><span class="sxs-lookup"><span data-stu-id="c57c5-105">Contains information about the codecs and formats that were used to encode the content in an Advanced Systems Format (ASF) file.</span></span> <span data-ttu-id="c57c5-106">Cet attribut correspond à l’objet de liste de codec dans l’en-tête ASF, défini dans la spécification ASF.</span><span class="sxs-lookup"><span data-stu-id="c57c5-106">This attribute corresponds to the Codec List Object in the ASF header, defined in the ASF specification.</span></span>

## <a name="data-type"></a><span data-ttu-id="c57c5-107">Type de données</span><span class="sxs-lookup"><span data-stu-id="c57c5-107">Data type</span></span>

<span data-ttu-id="c57c5-108">Tableau d’octets</span><span class="sxs-lookup"><span data-stu-id="c57c5-108">Byte array</span></span>

## <a name="remarks"></a><span data-ttu-id="c57c5-109">Notes</span><span class="sxs-lookup"><span data-stu-id="c57c5-109">Remarks</span></span>

<span data-ttu-id="c57c5-110">Cet attribut s’applique aux descripteurs de présentation pour le contenu ASF.</span><span class="sxs-lookup"><span data-stu-id="c57c5-110">This attribute applies to presentation descriptors for ASF content.</span></span>

<span data-ttu-id="c57c5-111">La méthode [**IMFASFContentInfo :: GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) crée le descripteur de présentation et génère cet attribut à partir de l’objet de liste de codecs dans l’en-tête ASF.</span><span class="sxs-lookup"><span data-stu-id="c57c5-111">The [**IMFASFContentInfo::GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) method creates the presentation descriptor and generates this attribute from the Codec List Object in the ASF header.</span></span> <span data-ttu-id="c57c5-112">Une application qui utilise la [source de média ASF](asf-media-source.md) peut obtenir cet attribut en appelant [**IMFMediaSource :: CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor) , puis en obtenant l’attribut à partir du descripteur de présentation.</span><span class="sxs-lookup"><span data-stu-id="c57c5-112">An application that uses the [ASF Media Source](asf-media-source.md) can get this attribute by calling [**IMFMediaSource::CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor) and then getting the attribute from the presentation descriptor.</span></span>

<span data-ttu-id="c57c5-113">Le tableau suivant montre la disposition de l’objet blob d’attributs.</span><span class="sxs-lookup"><span data-stu-id="c57c5-113">The following table shows the layout of the attribute blob.</span></span>



| <span data-ttu-id="c57c5-114">Champ d’objet de liste de codecs</span><span class="sxs-lookup"><span data-stu-id="c57c5-114">Codec List Object field</span></span> | <span data-ttu-id="c57c5-115">Type de données</span><span class="sxs-lookup"><span data-stu-id="c57c5-115">Data type</span></span>    | <span data-ttu-id="c57c5-116">Taille</span><span class="sxs-lookup"><span data-stu-id="c57c5-116">Size</span></span>    | <span data-ttu-id="c57c5-117">Description</span><span class="sxs-lookup"><span data-stu-id="c57c5-117">Description</span></span>                           |
|-------------------------|--------------|---------|---------------------------------------|
| <span data-ttu-id="c57c5-118">Nombre d’entrées de codec</span><span class="sxs-lookup"><span data-stu-id="c57c5-118">Codec Entries Count</span></span>     | <span data-ttu-id="c57c5-119">**GRANDE**</span><span class="sxs-lookup"><span data-stu-id="c57c5-119">**DWORD**</span></span>    | <span data-ttu-id="c57c5-120">4 octets</span><span class="sxs-lookup"><span data-stu-id="c57c5-120">4 bytes</span></span> | <span data-ttu-id="c57c5-121">Nombre de codecs</span><span class="sxs-lookup"><span data-stu-id="c57c5-121">Number of codecs</span></span>                      |
| <span data-ttu-id="c57c5-122">Entrées de codec</span><span class="sxs-lookup"><span data-stu-id="c57c5-122">Codec Entries</span></span>           | <span data-ttu-id="c57c5-123">**POIDS**\[\]</span><span class="sxs-lookup"><span data-stu-id="c57c5-123">**BYTE**\[\]</span></span> | <span data-ttu-id="c57c5-124">Variable</span><span class="sxs-lookup"><span data-stu-id="c57c5-124">Varies</span></span>  | <span data-ttu-id="c57c5-125">Tableau de structures d’informations de codec</span><span class="sxs-lookup"><span data-stu-id="c57c5-125">Array of codec information structures</span></span> |



 

<span data-ttu-id="c57c5-126">Le champ entrées de code est un tableau de structures.</span><span class="sxs-lookup"><span data-stu-id="c57c5-126">The Code Entries field is an array of structures.</span></span> <span data-ttu-id="c57c5-127">Le tableau suivant présente le format de chaque entrée :</span><span class="sxs-lookup"><span data-stu-id="c57c5-127">The following table shows the format of each entry:</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="c57c5-128">Champ d’objet de liste de codecs</span><span class="sxs-lookup"><span data-stu-id="c57c5-128">Codec List Object field</span></span></th>
<th><span data-ttu-id="c57c5-129">Type de données</span><span class="sxs-lookup"><span data-stu-id="c57c5-129">Data type</span></span></th>
<th><span data-ttu-id="c57c5-130">Taille</span><span class="sxs-lookup"><span data-stu-id="c57c5-130">Size</span></span></th>
<th><span data-ttu-id="c57c5-131">Description</span><span class="sxs-lookup"><span data-stu-id="c57c5-131">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="c57c5-132">Type</span><span class="sxs-lookup"><span data-stu-id="c57c5-132">Type</span></span></td>
<td><span data-ttu-id="c57c5-133"><strong>GRANDE</strong></span><span class="sxs-lookup"><span data-stu-id="c57c5-133"><strong>DWORD</strong></span></span></td>
<td><span data-ttu-id="c57c5-134">4 octets</span><span class="sxs-lookup"><span data-stu-id="c57c5-134">4 bytes</span></span></td>
<td><span data-ttu-id="c57c5-135">Type de codec.</span><span class="sxs-lookup"><span data-stu-id="c57c5-135">Codec type.</span></span> <span data-ttu-id="c57c5-136">Il peut s’agir de l’une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="c57c5-136">This can be one of the following values:</span></span><br/>
<ul>
<li><span data-ttu-id="c57c5-137">0x0001 : codec audio</span><span class="sxs-lookup"><span data-stu-id="c57c5-137">0x0001: Audio codec</span></span></li>
<li><span data-ttu-id="c57c5-138">0x0002 : codec vidéo</span><span class="sxs-lookup"><span data-stu-id="c57c5-138">0x0002: Video codec</span></span></li>
<li><span data-ttu-id="c57c5-139">0xFFFF : inconnu</span><span class="sxs-lookup"><span data-stu-id="c57c5-139">0xFFFF: Unknown</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c57c5-140">Longueur du nom du codec</span><span class="sxs-lookup"><span data-stu-id="c57c5-140">Codec Name Length</span></span></td>
<td><span data-ttu-id="c57c5-141"><strong>GRANDE</strong></span><span class="sxs-lookup"><span data-stu-id="c57c5-141"><strong>DWORD</strong></span></span></td>
<td><span data-ttu-id="c57c5-142">4 octets</span><span class="sxs-lookup"><span data-stu-id="c57c5-142">4 bytes</span></span></td>
<td><span data-ttu-id="c57c5-143">Taille, en octets, de la chaîne de nom du codec, y compris le caractère <strong>null</strong> .</span><span class="sxs-lookup"><span data-stu-id="c57c5-143">Size of the Codec Name string, in bytes, including the <strong>NULL</strong> character.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c57c5-144">Nom du codec</span><span class="sxs-lookup"><span data-stu-id="c57c5-144">Codec Name</span></span></td>
<td><span data-ttu-id="c57c5-145"><strong>WCHAR</strong>[]</span><span class="sxs-lookup"><span data-stu-id="c57c5-145"><strong>WCHAR</strong>[]</span></span></td>
<td><span data-ttu-id="c57c5-146">Variable</span><span class="sxs-lookup"><span data-stu-id="c57c5-146">Varies</span></span></td>
<td><span data-ttu-id="c57c5-147">Chaîne Unicode terminée par le caractère null qui contient le nom du codec, par exemple &quot; Windows Media Video 9 &quot; .</span><span class="sxs-lookup"><span data-stu-id="c57c5-147">Null-terminated Unicode string that contains the name of the codec, such as &quot;Windows Media Video 9&quot;.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c57c5-148">Longueur de la description du codec</span><span class="sxs-lookup"><span data-stu-id="c57c5-148">Codec Description Length</span></span></td>
<td><span data-ttu-id="c57c5-149"><strong>GRANDE</strong></span><span class="sxs-lookup"><span data-stu-id="c57c5-149"><strong>DWORD</strong></span></span></td>
<td><span data-ttu-id="c57c5-150">4 octets</span><span class="sxs-lookup"><span data-stu-id="c57c5-150">4 bytes</span></span></td>
<td><span data-ttu-id="c57c5-151">Taille, en octets, de la chaîne de description du codec, y compris le caractère <strong>null</strong> .</span><span class="sxs-lookup"><span data-stu-id="c57c5-151">Size of the Codec Description string, in bytes, including the <strong>NULL</strong> character.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c57c5-152">Description du codec</span><span class="sxs-lookup"><span data-stu-id="c57c5-152">Codec Description</span></span></td>
<td><span data-ttu-id="c57c5-153"><strong>WCHAR</strong>[]</span><span class="sxs-lookup"><span data-stu-id="c57c5-153"><strong>WCHAR</strong>[]</span></span></td>
<td><span data-ttu-id="c57c5-154">Variable</span><span class="sxs-lookup"><span data-stu-id="c57c5-154">Varies</span></span></td>
<td><span data-ttu-id="c57c5-155">Chaîne Unicode terminée par le caractère null qui contient une description du codec.</span><span class="sxs-lookup"><span data-stu-id="c57c5-155">A null-terminated Unicode string that contains a description of the codec.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c57c5-156">Longueur des informations du codec</span><span class="sxs-lookup"><span data-stu-id="c57c5-156">Codec Information Length</span></span></td>
<td><span data-ttu-id="c57c5-157"><strong>GRANDE</strong></span><span class="sxs-lookup"><span data-stu-id="c57c5-157"><strong>DWORD</strong></span></span></td>
<td><span data-ttu-id="c57c5-158">4 octets</span><span class="sxs-lookup"><span data-stu-id="c57c5-158">4 bytes</span></span></td>
<td><span data-ttu-id="c57c5-159">Taille du champ d’informations du codec, en octets.</span><span class="sxs-lookup"><span data-stu-id="c57c5-159">Size of the Codec Information field, in bytes.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c57c5-160">Informations sur le codec</span><span class="sxs-lookup"><span data-stu-id="c57c5-160">Codec Information</span></span></td>
<td><span data-ttu-id="c57c5-161"><strong>Byte</strong>[]</span><span class="sxs-lookup"><span data-stu-id="c57c5-161"><strong>BYTE</strong>[]</span></span></td>
<td><span data-ttu-id="c57c5-162">Variable</span><span class="sxs-lookup"><span data-stu-id="c57c5-162">Varies</span></span></td>
<td><span data-ttu-id="c57c5-163">Données de codec.</span><span class="sxs-lookup"><span data-stu-id="c57c5-163">Codec data.</span></span> <span data-ttu-id="c57c5-164">La signification de ces données dépend du codec.</span><span class="sxs-lookup"><span data-stu-id="c57c5-164">The meaning of this data depends on the codec.</span></span> <span data-ttu-id="c57c5-165">En règle générale, ces données indiquent le format.</span><span class="sxs-lookup"><span data-stu-id="c57c5-165">Typically, this data indicates the format.</span></span></td>
</tr>
</tbody>
</table>



 

> [!Note]  
> <span data-ttu-id="c57c5-166">La disposition de l’objet blob d’attribut ne correspond pas exactement à la disposition de l’objet de liste de codec dans l’en-tête ASF.</span><span class="sxs-lookup"><span data-stu-id="c57c5-166">The layout of the attribute blob does not exactly match the layout of the Codec List Object in the ASF header.</span></span> <span data-ttu-id="c57c5-167">En particulier, les longueurs de chaîne sont fournies en octets et incluent la taille de la marque de fin **null** .</span><span class="sxs-lookup"><span data-stu-id="c57c5-167">In particular, string lengths are given in bytes and include the size of the **NULL** terminator.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="c57c5-168">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c57c5-168">Requirements</span></span>



| <span data-ttu-id="c57c5-169">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c57c5-169">Requirement</span></span> | <span data-ttu-id="c57c5-170">Valeur</span><span class="sxs-lookup"><span data-stu-id="c57c5-170">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="c57c5-171">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c57c5-171">Minimum supported client</span></span><br/> | <span data-ttu-id="c57c5-172">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c57c5-172">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="c57c5-173">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c57c5-173">Minimum supported server</span></span><br/> | <span data-ttu-id="c57c5-174">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c57c5-174">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="c57c5-175">En-tête</span><span class="sxs-lookup"><span data-stu-id="c57c5-175">Header</span></span><br/>                   | <dl> <span data-ttu-id="c57c5-176"><dt>Wmcontainer. h</dt></span><span class="sxs-lookup"><span data-stu-id="c57c5-176"><dt>Wmcontainer.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c57c5-177">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c57c5-177">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c57c5-178">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="c57c5-178">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="c57c5-179">**IMFAttributes :: GetBlob**</span><span class="sxs-lookup"><span data-stu-id="c57c5-179">**IMFAttributes::GetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)
</dt> <dt>

[<span data-ttu-id="c57c5-180">**IMFAttributes :: SetBlob**</span><span class="sxs-lookup"><span data-stu-id="c57c5-180">**IMFAttributes::SetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)
</dt> <dt>

[<span data-ttu-id="c57c5-181">**IMFPresentationDescriptor**</span><span class="sxs-lookup"><span data-stu-id="c57c5-181">**IMFPresentationDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[<span data-ttu-id="c57c5-182">Attributs du descripteur de présentation</span><span class="sxs-lookup"><span data-stu-id="c57c5-182">Presentation Descriptor Attributes</span></span>](presentation-descriptor-attributes.md)
</dt> <dt>

[<span data-ttu-id="c57c5-183">Objet d’en-tête ASF</span><span class="sxs-lookup"><span data-stu-id="c57c5-183">ASF Header Object</span></span>](asf-file-structure.md)
</dt> <dt>

[<span data-ttu-id="c57c5-184">Descripteurs de présentation</span><span class="sxs-lookup"><span data-stu-id="c57c5-184">Presentation Descriptors</span></span>](presentation-descriptors.md)
</dt> </dl>

 

 




