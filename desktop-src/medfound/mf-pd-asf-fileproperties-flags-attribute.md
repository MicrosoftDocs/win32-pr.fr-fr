---
description: Spécifie si un fichier ASF (Advanced Systems Format) est diffusé ou recherché. Cette valeur correspond au champ Flags de l’objet de propriétés de fichier, défini dans la spécification ASF.
ms.assetid: 427f0dca-f945-4c89-a87a-a7c86291b1c5
title: Attribut MF_PD_ASF_FILEPROPERTIES_FLAGS (Wmcontainer. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ee294642188a0f2e22143feeca6791fea591cbb9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106530634"
---
# <a name="mf_pd_asf_fileproperties_flags-attribute"></a><span data-ttu-id="2068a-104">MF \_ PD \_ ASF \_ - \_ attribut flags</span><span class="sxs-lookup"><span data-stu-id="2068a-104">MF\_PD\_ASF\_FILEPROPERTIES\_FLAGS attribute</span></span>

<span data-ttu-id="2068a-105">Spécifie si un fichier ASF (Advanced Systems Format) est diffusé ou recherché.</span><span class="sxs-lookup"><span data-stu-id="2068a-105">Specifies whether an Advanced Systems Format (ASF) file is broadcast or seekable.</span></span> <span data-ttu-id="2068a-106">Cette valeur correspond au champ Flags de l’objet de propriétés de fichier, défini dans la spécification ASF.</span><span class="sxs-lookup"><span data-stu-id="2068a-106">This value corresponds to the Flags field of the File Properties Object, defined in the ASF specification.</span></span>

## <a name="data-type"></a><span data-ttu-id="2068a-107">Type de données</span><span class="sxs-lookup"><span data-stu-id="2068a-107">Data type</span></span>

<span data-ttu-id="2068a-108">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="2068a-108">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="2068a-109">Notes</span><span class="sxs-lookup"><span data-stu-id="2068a-109">Remarks</span></span>

<span data-ttu-id="2068a-110">Cet attribut s’applique aux descripteurs de présentation pour le contenu ASF.</span><span class="sxs-lookup"><span data-stu-id="2068a-110">This attribute applies to presentation descriptors for ASF content.</span></span> <span data-ttu-id="2068a-111">La valeur de l’attribut est une opération or au niveau du bit des indicateurs suivants :</span><span class="sxs-lookup"><span data-stu-id="2068a-111">The value of the attribute is a bitwise OR of the following flags:</span></span>



| <span data-ttu-id="2068a-112">Indicateur</span><span class="sxs-lookup"><span data-stu-id="2068a-112">Flag</span></span> | <span data-ttu-id="2068a-113">Description</span><span class="sxs-lookup"><span data-stu-id="2068a-113">Description</span></span>                                                                                                                                                                                                                                                                                       |
|------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2068a-114">0x01</span><span class="sxs-lookup"><span data-stu-id="2068a-114">0x01</span></span> | <span data-ttu-id="2068a-115">Indicateur de diffusion.</span><span class="sxs-lookup"><span data-stu-id="2068a-115">Broadcast flag.</span></span> <span data-ttu-id="2068a-116">Le fichier est en cours de création.</span><span class="sxs-lookup"><span data-stu-id="2068a-116">The file is in the process of being created.</span></span>                                                                                                                                                                                                                                      |
| <span data-ttu-id="2068a-117">0x02</span><span class="sxs-lookup"><span data-stu-id="2068a-117">0x02</span></span> | <span data-ttu-id="2068a-118">Indicateur de recherche.</span><span class="sxs-lookup"><span data-stu-id="2068a-118">Seekable flag.</span></span> <span data-ttu-id="2068a-119">Le fichier peut être recherché.</span><span class="sxs-lookup"><span data-stu-id="2068a-119">The file is seekable.</span></span><br/> <span data-ttu-id="2068a-120">Un fichier peut être recherché si un flux audio est présent et que la taille maximale des paquets de données est égale à la taille minimale des paquets de données.</span><span class="sxs-lookup"><span data-stu-id="2068a-120">A file is seekable if an audio stream is present and the maximum data packet size equals the minimum data packet size.</span></span> <span data-ttu-id="2068a-121">Il peut également être recherché si le fichier a un flux audio et un flux vidéo avec un objet index simple correspondant.</span><span class="sxs-lookup"><span data-stu-id="2068a-121">It can also be seekable if the file has an audio stream and a video stream with a matching Simple Index Object.</span></span><br/> |



 

<span data-ttu-id="2068a-122">La méthode [**IMFASFContentInfo :: GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) génère cet attribut à partir des métadonnées ASF.</span><span class="sxs-lookup"><span data-stu-id="2068a-122">The [**IMFASFContentInfo::GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) method generates this attribute from the ASF metadata.</span></span>

<span data-ttu-id="2068a-123">Si l’indicateur de diffusion est défini, les attributs suivants dans le descripteur de présentation ne sont pas valides :</span><span class="sxs-lookup"><span data-stu-id="2068a-123">If the broadcast flag is set, the following attributes in the presentation descriptor are not valid:</span></span>

-   [<span data-ttu-id="2068a-124">**ID du fichier. MF \_ PD \_ ASF \_ FichierPropriétés \_ \_**</span><span class="sxs-lookup"><span data-stu-id="2068a-124">**MF\_PD\_ASF\_FILEPROPERTIES\_FILE\_ID**</span></span>](mf-pd-asf-fileproperties-file-id-attribute.md)
-   [<span data-ttu-id="2068a-125">**heure de création de MF \_ PD \_ ASF \_ FichierPropriétés \_ \_**</span><span class="sxs-lookup"><span data-stu-id="2068a-125">**MF\_PD\_ASF\_FILEPROPERTIES\_CREATION\_TIME**</span></span>](mf-pd-asf-fileproperties-creation-time-attribute.md)
-   [<span data-ttu-id="2068a-126">**\_paquets MF PD \_ ASF FM \_ \_**</span><span class="sxs-lookup"><span data-stu-id="2068a-126">**MF\_PD\_ASF\_FILEPROPERTIES\_PACKETS**</span></span>](mf-pd-asf-fileproperties-packets-attribute.md)
-   [<span data-ttu-id="2068a-127">**\_durée de \_ \_ \_ lecture \_ MF PD ASF**</span><span class="sxs-lookup"><span data-stu-id="2068a-127">**MF\_PD\_ASF\_FILEPROPERTIES\_PLAY\_DURATION**</span></span>](mf-pd-asf-fileproperties-play-duration-attribute.md)
-   [<span data-ttu-id="2068a-128">**durée d’envoi de la norme MF \_ PD \_ ASF \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="2068a-128">**MF\_PD\_ASF\_FILEPROPERTIES\_SEND\_DURATION**</span></span>](mf-pd-asf-fileproperties-send-duration-attribute.md)

<span data-ttu-id="2068a-129">En outre, les valeurs d’attribut taille de paquet [**\_ maximale MF PD \_ ASF \_ FichierPropriétés \_ Max \_ \_**](mf-pd-asf-fileproperties-max-packet-size-attribute.md) et [**MF \_ PD \_ ASF \_ FichierPropriétés \_ Min \_ Packet \_ Size**](mf-pd-asf-fileproperties-min-packet-size-attribute.md) sont définies sur la taille de paquet réelle.</span><span class="sxs-lookup"><span data-stu-id="2068a-129">In addition, the [**MF\_PD\_ASF\_FILEPROPERTIES\_MAX\_PACKET\_SIZE**](mf-pd-asf-fileproperties-max-packet-size-attribute.md) attribute and [**MF\_PD\_ASF\_FILEPROPERTIES\_MIN\_PACKET\_SIZE**](mf-pd-asf-fileproperties-min-packet-size-attribute.md) attribute values are set to the actual packet size.</span></span>

## <a name="requirements"></a><span data-ttu-id="2068a-130">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2068a-130">Requirements</span></span>



| <span data-ttu-id="2068a-131">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2068a-131">Requirement</span></span> | <span data-ttu-id="2068a-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="2068a-132">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="2068a-133">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2068a-133">Minimum supported client</span></span><br/> | <span data-ttu-id="2068a-134">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2068a-134">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="2068a-135">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2068a-135">Minimum supported server</span></span><br/> | <span data-ttu-id="2068a-136">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2068a-136">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="2068a-137">En-tête</span><span class="sxs-lookup"><span data-stu-id="2068a-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="2068a-138"><dt>Wmcontainer. h</dt></span><span class="sxs-lookup"><span data-stu-id="2068a-138"><dt>Wmcontainer.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2068a-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2068a-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2068a-140">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="2068a-140">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="2068a-141">**IMFAttributes::GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="2068a-141">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="2068a-142">**IMFAttributes::SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="2068a-142">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="2068a-143">**IMFPresentationDescriptor**</span><span class="sxs-lookup"><span data-stu-id="2068a-143">**IMFPresentationDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[<span data-ttu-id="2068a-144">Attributs du descripteur de présentation</span><span class="sxs-lookup"><span data-stu-id="2068a-144">Presentation Descriptor Attributes</span></span>](presentation-descriptor-attributes.md)
</dt> <dt>

[<span data-ttu-id="2068a-145">Objet d’en-tête ASF</span><span class="sxs-lookup"><span data-stu-id="2068a-145">ASF Header Object</span></span>](asf-file-structure.md)
</dt> <dt>

[<span data-ttu-id="2068a-146">Descripteurs de présentation</span><span class="sxs-lookup"><span data-stu-id="2068a-146">Presentation Descriptors</span></span>](presentation-descriptors.md)
</dt> </dl>

 

 




