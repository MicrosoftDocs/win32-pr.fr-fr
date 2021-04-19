---
description: Spécifie le type de conteneur d’un fichier encodé.
ms.assetid: 97fd968a-6843-4695-aece-02f9acd618fd
title: Attribut MF_TRANSCODE_CONTAINERTYPE (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7f86b8d5890a771200feda265c3878b6eb7030b2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106518562"
---
# <a name="mf_transcode_containertype-attribute"></a><span data-ttu-id="36501-103">\_Attribut CONTAINERTYPE de transcodage MF \_</span><span class="sxs-lookup"><span data-stu-id="36501-103">MF\_TRANSCODE\_CONTAINERTYPE attribute</span></span>

<span data-ttu-id="36501-104">Spécifie le type de conteneur d’un fichier encodé.</span><span class="sxs-lookup"><span data-stu-id="36501-104">Specifies the container type of an encoded file.</span></span> <span data-ttu-id="36501-105">Les types de conteneur sont pris en charge par Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="36501-105">The container types are supported by Media Foundation.</span></span>

## <a name="data-type"></a><span data-ttu-id="36501-106">Type de données</span><span class="sxs-lookup"><span data-stu-id="36501-106">Data type</span></span>

<span data-ttu-id="36501-107">**GUID**</span><span class="sxs-lookup"><span data-stu-id="36501-107">**GUID**</span></span>

<span data-ttu-id="36501-108">Les valeurs possibles pour les types de conteneurs fournis par Media Foundation sont décrites dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="36501-108">Possible values for the container types provided by Media Foundation are described in the following table.</span></span>



| <span data-ttu-id="36501-109">Valeur</span><span class="sxs-lookup"><span data-stu-id="36501-109">Value</span></span>                                                                                                                                                                                                                                                                 | <span data-ttu-id="36501-110">Signification</span><span class="sxs-lookup"><span data-stu-id="36501-110">Meaning</span></span>                                                                            |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <span id="MFTranscodeContainerType_ASF"></span><span id="mftranscodecontainertype_asf"></span><span id="MFTRANSCODECONTAINERTYPE_ASF"></span><dl> <span data-ttu-id="36501-111"><dt>**MFTranscodeContainerType \_ ASF**</dt></span><span class="sxs-lookup"><span data-stu-id="36501-111"><dt>**MFTranscodeContainerType\_ASF**</dt></span></span> </dl>             | <span data-ttu-id="36501-112">Conteneur de fichiers ASF.</span><span class="sxs-lookup"><span data-stu-id="36501-112">ASF file container.</span></span><br/>                                                     |
| <span id="MFTranscodeContainerType_MPEG4"></span><span id="mftranscodecontainertype_mpeg4"></span><span id="MFTRANSCODECONTAINERTYPE_MPEG4"></span><dl> <span data-ttu-id="36501-113"><dt>**MFTranscodeContainerType \_ MPEG4**</dt></span><span class="sxs-lookup"><span data-stu-id="36501-113"><dt>**MFTranscodeContainerType\_MPEG4**</dt></span></span> </dl>     | <span data-ttu-id="36501-114">Conteneur de fichiers MP4.</span><span class="sxs-lookup"><span data-stu-id="36501-114">MP4 file container.</span></span><br/>                                                     |
| <span id="MFTranscodeContainerType_MP3"></span><span id="mftranscodecontainertype_mp3"></span><span id="MFTRANSCODECONTAINERTYPE_MP3"></span><dl> <span data-ttu-id="36501-115"><dt>**\_Mp3 MFTranscodeContainerType**</dt></span><span class="sxs-lookup"><span data-stu-id="36501-115"><dt>**MFTranscodeContainerType\_MP3**</dt></span></span> </dl>             | <span data-ttu-id="36501-116">Conteneur de fichiers MP3.</span><span class="sxs-lookup"><span data-stu-id="36501-116">MP3 file container.</span></span><br/>                                                     |
| <span id="MFTranscodeContainerType_3GP"></span><span id="mftranscodecontainertype_3gp"></span><span id="MFTRANSCODECONTAINERTYPE_3GP"></span><dl> <span data-ttu-id="36501-117"><dt>**MFTranscodeContainerType \_ 3GP**</dt></span><span class="sxs-lookup"><span data-stu-id="36501-117"><dt>**MFTranscodeContainerType\_3GP**</dt></span></span> </dl>             | <span data-ttu-id="36501-118">conteneur de fichiers 3GP.</span><span class="sxs-lookup"><span data-stu-id="36501-118">3GP file container.</span></span> <br/>                                                    |
| <span id="MFTranscodeContainerType_AC3"></span><span id="mftranscodecontainertype_ac3"></span><span id="MFTRANSCODECONTAINERTYPE_AC3"></span><dl> <span data-ttu-id="36501-119"><dt>**MFTranscodeContainerType \_ AC3**</dt></span><span class="sxs-lookup"><span data-stu-id="36501-119"><dt>**MFTranscodeContainerType\_AC3**</dt></span></span> </dl>             | <span data-ttu-id="36501-120">Conteneur de fichiers AC3.</span><span class="sxs-lookup"><span data-stu-id="36501-120">AC3 file container.</span></span> <br/>                                                    |
| <span id="MFTranscodeContainerType_ADTS"></span><span id="mftranscodecontainertype_adts"></span><span id="MFTRANSCODECONTAINERTYPE_ADTS"></span><dl> <span data-ttu-id="36501-121"><dt>**MFTranscodeContainerType \_ ADTS**</dt></span><span class="sxs-lookup"><span data-stu-id="36501-121"><dt>**MFTranscodeContainerType\_ADTS**</dt></span></span> </dl>         | <span data-ttu-id="36501-122">Conteneur de fichiers ADTS.</span><span class="sxs-lookup"><span data-stu-id="36501-122">ADTS file container.</span></span> <br/>                                                   |
| <span id="MFTranscodeContainerType_MPEG2"></span><span id="mftranscodecontainertype_mpeg2"></span><span id="MFTRANSCODECONTAINERTYPE_MPEG2"></span><dl> <span data-ttu-id="36501-123"><dt>**MFTranscodeContainerType \_ MPEG2**</dt></span><span class="sxs-lookup"><span data-stu-id="36501-123"><dt>**MFTranscodeContainerType\_MPEG2**</dt></span></span> </dl>     | <span data-ttu-id="36501-124">Conteneur de fichiers MPEG2.</span><span class="sxs-lookup"><span data-stu-id="36501-124">MPEG2 file container.</span></span> <br/>                                                  |
| <span id="MFTranscodeContainerType_FMPEG4"></span><span id="mftranscodecontainertype_fmpeg4"></span><span id="MFTRANSCODECONTAINERTYPE_FMPEG4"></span><dl> <span data-ttu-id="36501-125"><dt>**MFTranscodeContainerType \_ FMPEG4**</dt></span><span class="sxs-lookup"><span data-stu-id="36501-125"><dt>**MFTranscodeContainerType\_FMPEG4**</dt></span></span> </dl> | <span data-ttu-id="36501-126">Conteneur de fichiers FMPEG4.</span><span class="sxs-lookup"><span data-stu-id="36501-126">FMPEG4 file container.</span></span> <br/>                                                 |
| <span id="MFTranscodeContainerType_WAVE"></span><span id="mftranscodecontainertype_wave"></span><span id="MFTRANSCODECONTAINERTYPE_WAVE"></span><dl> <span data-ttu-id="36501-127"><dt>**MFTranscodeContainerType \_ Wave**</dt></span><span class="sxs-lookup"><span data-stu-id="36501-127"><dt>**MFTranscodeContainerType\_WAVE**</dt></span></span> </dl>         | <span data-ttu-id="36501-128">Conteneur de fichiers WAVE.</span><span class="sxs-lookup"><span data-stu-id="36501-128">WAVE file container.</span></span><br/> <span data-ttu-id="36501-129">Pris en charge dans Windows 8.1 et et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="36501-129">Supported in Windows 8.1 and and later.</span></span><br/> |
| <span id="MFTranscodeContainerType_AVI"></span><span id="mftranscodecontainertype_avi"></span><span id="MFTRANSCODECONTAINERTYPE_AVI"></span><dl> <span data-ttu-id="36501-130"><dt>**\_AVI MFTranscodeContainerType**</dt></span><span class="sxs-lookup"><span data-stu-id="36501-130"><dt>**MFTranscodeContainerType\_AVI**</dt></span></span> </dl>             | <span data-ttu-id="36501-131">Conteneur de fichiers AVI.</span><span class="sxs-lookup"><span data-stu-id="36501-131">AVI file container.</span></span><br/> <span data-ttu-id="36501-132">Pris en charge dans Windows 8.1 et et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="36501-132">Supported in Windows 8.1 and and later.</span></span><br/>  |
| <span id="MFTranscodeContainerType_AMR"></span><span id="mftranscodecontainertype_amr"></span><span id="MFTRANSCODECONTAINERTYPE_AMR"></span><dl> <span data-ttu-id="36501-133"><dt>**MFTranscodeContainerType \_ Amr**</dt></span><span class="sxs-lookup"><span data-stu-id="36501-133"><dt>**MFTranscodeContainerType\_AMR**</dt></span></span> </dl>             | <span data-ttu-id="36501-134">Conteneur de fichiers AMR.</span><span class="sxs-lookup"><span data-stu-id="36501-134">AMR file container.</span></span> <br/>                                                    |



 

## <a name="getset"></a><span data-ttu-id="36501-135">Obtenir/définir</span><span class="sxs-lookup"><span data-stu-id="36501-135">Get/set</span></span>

<span data-ttu-id="36501-136">Pour récupérer cet attribut, appelez [**IMFAttributes :: GetGuid**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getguid).</span><span class="sxs-lookup"><span data-stu-id="36501-136">To get this attribute, call [**IMFAttributes::GetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getguid).</span></span>

<span data-ttu-id="36501-137">Pour définir cet attribut, appelez [**IMFAttributes :: SetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid).</span><span class="sxs-lookup"><span data-stu-id="36501-137">To set this attribute, call [**IMFAttributes::SetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid).</span></span>

## <a name="remarks"></a><span data-ttu-id="36501-138">Notes</span><span class="sxs-lookup"><span data-stu-id="36501-138">Remarks</span></span>

<span data-ttu-id="36501-139">Cet attribut est utilisé avec la fonctionnalité de transcodage rapide et l’objet enregistreur récepteur.</span><span class="sxs-lookup"><span data-stu-id="36501-139">This attribute is used with both the Fast Transcode feature and the sink writer object.</span></span>

<span data-ttu-id="36501-140">La constante GUID de cet attribut est exportée à partir de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="36501-140">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

### <a name="fast-transcode"></a><span data-ttu-id="36501-141">Transcodage rapide</span><span class="sxs-lookup"><span data-stu-id="36501-141">Fast Transcode</span></span>

<span data-ttu-id="36501-142">L’application doit définir l’attribut de conteneur sur le profil de transcodage avant de générer la topologie de transcodage.</span><span class="sxs-lookup"><span data-stu-id="36501-142">The application must set the container attribute on the transcode profile before building the transcode topology.</span></span> <span data-ttu-id="36501-143">Le générateur de topologies analyse cet attribut et charge le récepteur multimédia approprié dans le pipeline.</span><span class="sxs-lookup"><span data-stu-id="36501-143">The topology builder analyses this attribute and loads the appropriate media sink in the pipeline.</span></span> <span data-ttu-id="36501-144">Pour plus d'informations, voir les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="36501-144">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="36501-145">**IMFTranscodeProfile::GetContainerAttributes**</span><span class="sxs-lookup"><span data-stu-id="36501-145">**IMFTranscodeProfile::GetContainerAttributes**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-getcontainerattributes)
-   [<span data-ttu-id="36501-146">**IMFTranscodeProfile::SetContainerAttributes**</span><span class="sxs-lookup"><span data-stu-id="36501-146">**IMFTranscodeProfile::SetContainerAttributes**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setcontainerattributes)

### <a name="sink-writer"></a><span data-ttu-id="36501-147">Enregistreur du récepteur</span><span class="sxs-lookup"><span data-stu-id="36501-147">Sink Writer</span></span>

<span data-ttu-id="36501-148">Cet attribut peut être utilisé pour configurer le type de conteneur de fichiers pour le writer du récepteur.</span><span class="sxs-lookup"><span data-stu-id="36501-148">This attribute can be used to configure the file-container type for the sink writer.</span></span> <span data-ttu-id="36501-149">Pour plus d’informations, consultez [attributs du writer du récepteur](sink-writer-attributes.md).</span><span class="sxs-lookup"><span data-stu-id="36501-149">For more information, see [Sink Writer Attributes](sink-writer-attributes.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="36501-150">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="36501-150">Requirements</span></span>



| <span data-ttu-id="36501-151">Condition requise</span><span class="sxs-lookup"><span data-stu-id="36501-151">Requirement</span></span> | <span data-ttu-id="36501-152">Valeur</span><span class="sxs-lookup"><span data-stu-id="36501-152">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="36501-153">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="36501-153">Minimum supported client</span></span><br/> | <span data-ttu-id="36501-154">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="36501-154">Windows 7 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="36501-155">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="36501-155">Minimum supported server</span></span><br/> | <span data-ttu-id="36501-156">Applications de bureau Windows Server 2008 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="36501-156">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="36501-157">En-tête</span><span class="sxs-lookup"><span data-stu-id="36501-157">Header</span></span><br/>                   | <dl> <span data-ttu-id="36501-158"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="36501-158"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="36501-159">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="36501-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="36501-160">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="36501-160">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="36501-161">API de transcodage</span><span class="sxs-lookup"><span data-stu-id="36501-161">Transcode API</span></span>](transcode-api.md)
</dt> </dl>

 

 




