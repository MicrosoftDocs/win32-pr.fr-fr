---
description: Spécifie le profil de conformité de périphérique pour l’encodage des fichiers ASF.
ms.assetid: 9a6b6402-ff53-4399-8616-06b7768a8737
title: Attribut MF_TRANSCODE_ENCODINGPROFILE (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 020344cb2c2f6fc4a539c7cdbc8df0dc69d80d3f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527406"
---
# <a name="mf_transcode_encodingprofile-attribute"></a><span data-ttu-id="7e00b-103">\_Attribut ENCODINGPROFILE de transcodage MF \_</span><span class="sxs-lookup"><span data-stu-id="7e00b-103">MF\_TRANSCODE\_ENCODINGPROFILE attribute</span></span>

<span data-ttu-id="7e00b-104">Spécifie le profil de conformité de périphérique pour l’encodage des fichiers ASF.</span><span class="sxs-lookup"><span data-stu-id="7e00b-104">Specifies the device conformance profile for encoding Advanced Streaming Format (ASF) files.</span></span>

## <a name="data-type"></a><span data-ttu-id="7e00b-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="7e00b-105">Data type</span></span>

<span data-ttu-id="7e00b-106">**LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="7e00b-106">**LPWSTR**</span></span>

## <a name="getset"></a><span data-ttu-id="7e00b-107">Obtenir/définir</span><span class="sxs-lookup"><span data-stu-id="7e00b-107">Get/set</span></span>

<span data-ttu-id="7e00b-108">Pour récupérer cet attribut, appelez [**IMFAttributes :: GetAllocatedString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getallocatedstring).</span><span class="sxs-lookup"><span data-stu-id="7e00b-108">To get this attribute, call [**IMFAttributes::GetAllocatedString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getallocatedstring).</span></span>

<span data-ttu-id="7e00b-109">Pour définir cet attribut, appelez [**IMFAttributes :: SetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring).</span><span class="sxs-lookup"><span data-stu-id="7e00b-109">To set this attribute, call [**IMFAttributes::SetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring).</span></span>

## <a name="remarks"></a><span data-ttu-id="7e00b-110">Notes</span><span class="sxs-lookup"><span data-stu-id="7e00b-110">Remarks</span></span>

<span data-ttu-id="7e00b-111">Utilisez cet attribut lors du transcodage sur un appareil qui prend en charge Windows Media.</span><span class="sxs-lookup"><span data-stu-id="7e00b-111">Use this attribute when transcoding to a device that supports Windows Media.</span></span> <span data-ttu-id="7e00b-112">Si cet attribut est défini, l’encodeur utilise le profil de conformité de périphérique, ou modèle, pour les codecs Windows Media.</span><span class="sxs-lookup"><span data-stu-id="7e00b-112">If this attribute is set, the encoder will use the device conformance profile, or template, for Windows Media codecs.</span></span> <span data-ttu-id="7e00b-113">Définissez l’attribut sur le profil de transcodage avant de générer la topologie de transcodage.</span><span class="sxs-lookup"><span data-stu-id="7e00b-113">Set the attribute on the transcode profile before building the transcode topology.</span></span>

<span data-ttu-id="7e00b-114">La valeur de cet attribut peut être l’une des chaînes de modèle de conformité énumérées dans les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="7e00b-114">The value of this attribute can be any of the conformance template strings listed in the following topics:</span></span>

-   [<span data-ttu-id="7e00b-115">Modèles de conformité des périphériques audio</span><span class="sxs-lookup"><span data-stu-id="7e00b-115">Audio Device Conformance Templates</span></span>](../wmformat/audio-device-conformance-templates.md)
-   [<span data-ttu-id="7e00b-116">Modèles de conformité des périphériques vidéo</span><span class="sxs-lookup"><span data-stu-id="7e00b-116">Video Device Conformance Templates</span></span>](../wmformat/video-device-conformance-templates.md)

<span data-ttu-id="7e00b-117">Pour l’encodage Windows Media Video, le générateur de topologies utilise cet attribut pour définir la propriété [**MFPKEY \_ DECODERCOMPLEXITYREQUESTED**](mfpkey-decodercomplexityrequestedproperty.md) sur l’encodeur.</span><span class="sxs-lookup"><span data-stu-id="7e00b-117">For Windows Media Video encoding, the topology builder uses this attribute to set the [**MFPKEY\_DECODERCOMPLEXITYREQUESTED**](mfpkey-decodercomplexityrequestedproperty.md) property on the encoder.</span></span> <span data-ttu-id="7e00b-118">L’encodeur tente d’utiliser le modèle spécifié pour encoder le contenu.</span><span class="sxs-lookup"><span data-stu-id="7e00b-118">The encoder will attempt to use the specified template to encode the content.</span></span> <span data-ttu-id="7e00b-119">Pour obtenir le modèle réel, parcourez les nœuds de la topologie de transcodage pour obtenir un pointeur vers le nœud de l’encodeur.</span><span class="sxs-lookup"><span data-stu-id="7e00b-119">To get the actual template, traverse the nodes of the transcode topology to get a pointer to the encoder node.</span></span> <span data-ttu-id="7e00b-120">Ensuite, récupérez la valeur de la propriété [**MFPKEY \_ DECODERCOMPLEXITYPROFILE**](mfpkey-decodercomplexityprofileproperty.md) à partir de l’encodeur.</span><span class="sxs-lookup"><span data-stu-id="7e00b-120">Then get the value of the [**MFPKEY\_DECODERCOMPLEXITYPROFILE**](mfpkey-decodercomplexityprofileproperty.md) property from the encoder.</span></span>

<span data-ttu-id="7e00b-121">Le générateur de topologies utilise également la valeur de cet attribut pour définir la propriété « DeviceConformanceTemplate » sur le récepteur de média ASF.</span><span class="sxs-lookup"><span data-stu-id="7e00b-121">The topology builder also uses the value of this attribute to set the "DeviceConformanceTemplate" property on the ASF media sink.</span></span>

<span data-ttu-id="7e00b-122">Si cet attribut est défini, l’objet de métadonnées du fichier ASF est toujours généré, quelle que soit la valeur spécifiée par l’application de l’attribut de [ \_ \_ \_ \_ transfert de métadonnées d’omission de transcodage MF](mf-transcode-skip-metadata-transfer.md) .</span><span class="sxs-lookup"><span data-stu-id="7e00b-122">If this attribute is set, the metadata object of the ASF file is always generated irrespective of the application-specified value of the [MF\_TRANSCODE\_SKIP\_METADATA\_TRANSFER](mf-transcode-skip-metadata-transfer.md) attribute.</span></span>

<span data-ttu-id="7e00b-123">Les valeurs typiques de cet attribut sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="7e00b-123">Typical values for this attribute include the following:</span></span>



| <span data-ttu-id="7e00b-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="7e00b-124">Value</span></span>   | <span data-ttu-id="7e00b-125">Description</span><span class="sxs-lookup"><span data-stu-id="7e00b-125">Description</span></span>                      |
|---------|----------------------------------|
| <span data-ttu-id="7e00b-126">FOURNISSEURS</span><span class="sxs-lookup"><span data-stu-id="7e00b-126">"AP"</span></span>    | <span data-ttu-id="7e00b-127">Vidéo sur les profils avancés</span><span class="sxs-lookup"><span data-stu-id="7e00b-127">Advanced profile video</span></span>           |
| <span data-ttu-id="7e00b-128">CANAL</span><span class="sxs-lookup"><span data-stu-id="7e00b-128">"MP"</span></span>    | <span data-ttu-id="7e00b-129">Vidéo sur le profil principal</span><span class="sxs-lookup"><span data-stu-id="7e00b-129">Main profile video</span></span>               |
| <span data-ttu-id="7e00b-130">SR</span><span class="sxs-lookup"><span data-stu-id="7e00b-130">"SP"</span></span>    | <span data-ttu-id="7e00b-131">Vidéo sur les profils simples</span><span class="sxs-lookup"><span data-stu-id="7e00b-131">Simple profile video</span></span>             |
| <span data-ttu-id="7e00b-132">"MP@LL"</span><span class="sxs-lookup"><span data-stu-id="7e00b-132">"MP@LL"</span></span> | <span data-ttu-id="7e00b-133">Profil principal, vidéo de niveau moyen</span><span class="sxs-lookup"><span data-stu-id="7e00b-133">Main profile, medium level video</span></span> |
| <span data-ttu-id="7e00b-134">NIV</span><span class="sxs-lookup"><span data-stu-id="7e00b-134">"L2"</span></span>    | <span data-ttu-id="7e00b-135">Profil audio, <= 160 Kbits/s</span><span class="sxs-lookup"><span data-stu-id="7e00b-135">Audio profile, <= 160 Kbps</span></span>    |



 

<span data-ttu-id="7e00b-136">La constante GUID de cet attribut est exportée à partir de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="7e00b-136">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="7e00b-137">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7e00b-137">Requirements</span></span>



| <span data-ttu-id="7e00b-138">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7e00b-138">Requirement</span></span> | <span data-ttu-id="7e00b-139">Valeur</span><span class="sxs-lookup"><span data-stu-id="7e00b-139">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="7e00b-140">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7e00b-140">Minimum supported client</span></span><br/> | <span data-ttu-id="7e00b-141">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7e00b-141">Windows 7 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="7e00b-142">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7e00b-142">Minimum supported server</span></span><br/> | <span data-ttu-id="7e00b-143">Applications de bureau Windows Server 2008 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7e00b-143">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="7e00b-144">En-tête</span><span class="sxs-lookup"><span data-stu-id="7e00b-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="7e00b-145"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="7e00b-145"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7e00b-146">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7e00b-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7e00b-147">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="7e00b-147">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="7e00b-148">API de transcodage</span><span class="sxs-lookup"><span data-stu-id="7e00b-148">Transcode API</span></span>](transcode-api.md)
</dt> <dt>

[<span data-ttu-id="7e00b-149">**IMFTranscodeProfile::GetAudioAttributes**</span><span class="sxs-lookup"><span data-stu-id="7e00b-149">**IMFTranscodeProfile::GetAudioAttributes**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-getaudioattributes)
</dt> <dt>

[<span data-ttu-id="7e00b-150">**IMFTranscodeProfile::SetAudioAttributes**</span><span class="sxs-lookup"><span data-stu-id="7e00b-150">**IMFTranscodeProfile::SetAudioAttributes**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setaudioattributes)
</dt> <dt>

[<span data-ttu-id="7e00b-151">**IMFTranscodeProfile::SetVideoAttributes**</span><span class="sxs-lookup"><span data-stu-id="7e00b-151">**IMFTranscodeProfile::SetVideoAttributes**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-getvideoattributes)
</dt> <dt>

[<span data-ttu-id="7e00b-152">**IMFTranscodeProfile::GetVideoAttributes**</span><span class="sxs-lookup"><span data-stu-id="7e00b-152">**IMFTranscodeProfile::GetVideoAttributes**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setvideoattributes)
</dt> </dl>

 

 
