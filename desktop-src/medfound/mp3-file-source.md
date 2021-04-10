---
description: La source de fichier MP3 analyse les fichiers MP3.
ms.assetid: 37362642-1b8a-4fb3-950d-ed1afe3696e5
title: Source du fichier MP3
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2241e3b99d5a1918be8ff0182a9eca8939c12ce2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114382"
---
# <a name="mp3-file-source"></a><span data-ttu-id="7c08a-103">Source du fichier MP3</span><span class="sxs-lookup"><span data-stu-id="7c08a-103">MP3 File Source</span></span>

<span data-ttu-id="7c08a-104">La source de fichier MP3 analyse les fichiers MP3.</span><span class="sxs-lookup"><span data-stu-id="7c08a-104">The MP3 file source parses MP3 files.</span></span>

<span data-ttu-id="7c08a-105">La source du fichier MP3 génère des mémoires tampons qui contiennent des images audio MPEG-1.</span><span class="sxs-lookup"><span data-stu-id="7c08a-105">The MP3 file source outputs buffers that contain MPEG-1 audio frames.</span></span> <span data-ttu-id="7c08a-106">Elle ne décode pas l’audio.</span><span class="sxs-lookup"><span data-stu-id="7c08a-106">It does not decode the audio.</span></span>

## <a name="file-extensions-and-mime-types"></a><span data-ttu-id="7c08a-107">Extensions de fichier et types MIME</span><span class="sxs-lookup"><span data-stu-id="7c08a-107">File Extensions and MIME Types</span></span>

<span data-ttu-id="7c08a-108">La source du fichier MP3 est la source du média par défaut pour l’extension de nom de fichier suivante :</span><span class="sxs-lookup"><span data-stu-id="7c08a-108">The MP3 file source is the default media source for the following file name extension:</span></span>

-   <span data-ttu-id="7c08a-109">.mp3</span><span class="sxs-lookup"><span data-stu-id="7c08a-109">.mp3</span></span>

<span data-ttu-id="7c08a-110">Il s’agit également de la source du média par défaut pour les types MIME suivants.</span><span class="sxs-lookup"><span data-stu-id="7c08a-110">It is also the default media source for the following MIME types.</span></span>

-   <span data-ttu-id="7c08a-111">audio/MPEG</span><span class="sxs-lookup"><span data-stu-id="7c08a-111">audio/mpeg</span></span>
-   <span data-ttu-id="7c08a-112">audio/x-mp3</span><span class="sxs-lookup"><span data-stu-id="7c08a-112">audio/x-mp3</span></span>
-   <span data-ttu-id="7c08a-113">audio/x-MPEG</span><span class="sxs-lookup"><span data-stu-id="7c08a-113">audio/x-mpeg</span></span>

## <a name="media-types"></a><span data-ttu-id="7c08a-114">Types de médias</span><span class="sxs-lookup"><span data-stu-id="7c08a-114">Media Types</span></span>

<span data-ttu-id="7c08a-115">Le type de média proposé par la source du fichier MP3 contient les attributs suivants.</span><span class="sxs-lookup"><span data-stu-id="7c08a-115">The media type offered by the MP3 file source contains the following attributes.</span></span>



| <span data-ttu-id="7c08a-116">Attribut</span><span class="sxs-lookup"><span data-stu-id="7c08a-116">Attribute</span></span>                                                                                    | <span data-ttu-id="7c08a-117">Description</span><span class="sxs-lookup"><span data-stu-id="7c08a-117">Description</span></span>                                                                                                                                        |
|----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7c08a-118">**\_type de \_ majeurese MF MT \_**</span><span class="sxs-lookup"><span data-stu-id="7c08a-118">**MF\_MT\_MAJOR\_TYPE**</span></span>](mf-mt-major-type-attribute.md)                                    | <span data-ttu-id="7c08a-119">Égal à **MFMediaType \_ audio**.</span><span class="sxs-lookup"><span data-stu-id="7c08a-119">Equal to **MFMediaType\_Audio**.</span></span>                                                                                                                   |
| [<span data-ttu-id="7c08a-120">**\_sous- \_ type MF MT**</span><span class="sxs-lookup"><span data-stu-id="7c08a-120">**MF\_MT\_SUBTYPE**</span></span>](mf-mt-subtype-attribute.md)                                           | <span data-ttu-id="7c08a-121">Égal à **MFAudioFormat \_ mp3** ou **MFAudioFormat \_ MPEG**.</span><span class="sxs-lookup"><span data-stu-id="7c08a-121">Equal to **MFAudioFormat\_MP3** or **MFAudioFormat\_MPEG**.</span></span>                                                                                        |
| [<span data-ttu-id="7c08a-122">**\_octets de \_ données audio MF MT- \_ \_ octets \_ par \_ seconde**</span><span class="sxs-lookup"><span data-stu-id="7c08a-122">**MF\_MT\_AUDIO\_AVG\_BYTES\_PER\_SECOND**</span></span>](mf-mt-audio-avg-bytes-per-second-attribute.md) | <span data-ttu-id="7c08a-123">Nombre moyen d’octets par seconde.</span><span class="sxs-lookup"><span data-stu-id="7c08a-123">Average number of bytes per second.</span></span>                                                                                                                |
| [<span data-ttu-id="7c08a-124">**\_alignement de \_ \_ bloc audio MF MT \_**</span><span class="sxs-lookup"><span data-stu-id="7c08a-124">**MF\_MT\_AUDIO\_BLOCK\_ALIGNMENT**</span></span>](mf-mt-audio-block-alignment-attribute.md)             | <span data-ttu-id="7c08a-125">Égal à 1.</span><span class="sxs-lookup"><span data-stu-id="7c08a-125">Equal to 1.</span></span>                                                                                                                                        |
| [<span data-ttu-id="7c08a-126">**\_canaux de \_ \_ numéros audio MF MT \_**</span><span class="sxs-lookup"><span data-stu-id="7c08a-126">**MF\_MT\_AUDIO\_NUM\_CHANNELS**</span></span>](mf-mt-audio-num-channels-attribute.md)                   | <span data-ttu-id="7c08a-127">Nombre de canaux audio.</span><span class="sxs-lookup"><span data-stu-id="7c08a-127">Number of audio channels.</span></span>                                                                                                                          |
| [<span data-ttu-id="7c08a-128">**\_ \_ échantillons audio MF \_ MT \_ par \_ seconde**</span><span class="sxs-lookup"><span data-stu-id="7c08a-128">**MF\_MT\_AUDIO\_SAMPLES\_PER\_SECOND**</span></span>](mf-mt-audio-samples-per-second-attribute.md)      | <span data-ttu-id="7c08a-129">Nombre d’échantillons audio par seconde.</span><span class="sxs-lookup"><span data-stu-id="7c08a-129">Number of audio samples per second.</span></span>                                                                                                                |
| [<span data-ttu-id="7c08a-130">**\_ \_ données utilisateur MF \_ MT**</span><span class="sxs-lookup"><span data-stu-id="7c08a-130">**MF\_MT\_USER\_DATA**</span></span>](mf-mt-user-data-attribute.md)                                      | <span data-ttu-id="7c08a-131">Contient la partie d’une structure [**MPEGLAYER3WAVEFORMAT**](/windows/win32/api/mmreg/ns-mmreg-mpeglayer3waveformat) qui apparaît après le membre **wfx** de la structure.</span><span class="sxs-lookup"><span data-stu-id="7c08a-131">Contains the portion of a [**MPEGLAYER3WAVEFORMAT**](/windows/win32/api/mmreg/ns-mmreg-mpeglayer3waveformat) structure that appears after the **wfx** member of the structure.</span></span> |



 

## <a name="interfaces"></a><span data-ttu-id="7c08a-132">Interfaces</span><span class="sxs-lookup"><span data-stu-id="7c08a-132">Interfaces</span></span>

<span data-ttu-id="7c08a-133">La source de fichier MP3 expose les interfaces suivantes via [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)):</span><span class="sxs-lookup"><span data-stu-id="7c08a-133">The MP3 file source exposes the following interfaces through [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)):</span></span>

-   [<span data-ttu-id="7c08a-134">**IMFGetService**</span><span class="sxs-lookup"><span data-stu-id="7c08a-134">**IMFGetService**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice)
-   [<span data-ttu-id="7c08a-135">**IMFMediaEventGenerator**</span><span class="sxs-lookup"><span data-stu-id="7c08a-135">**IMFMediaEventGenerator**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator)
-   [<span data-ttu-id="7c08a-136">**IMFMediaSource**</span><span class="sxs-lookup"><span data-stu-id="7c08a-136">**IMFMediaSource**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource)

<span data-ttu-id="7c08a-137">En outre, il expose les interfaces suivantes par le biais de [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice):</span><span class="sxs-lookup"><span data-stu-id="7c08a-137">In addition, it exposes the following interfaces through [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice):</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="7c08a-138">GUID du service</span><span class="sxs-lookup"><span data-stu-id="7c08a-138">Service GUID</span></span></th>
<th><span data-ttu-id="7c08a-139">Interface</span><span class="sxs-lookup"><span data-stu-id="7c08a-139">Interface</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="7c08a-140"><strong>MF_METADATA_PROVIDER_SERVICE</strong></span><span class="sxs-lookup"><span data-stu-id="7c08a-140"><strong>MF_METADATA_PROVIDER_SERVICE</strong></span></span></td>
<td><span data-ttu-id="7c08a-141"><a href="/windows/desktop/api/mfidl/nn-mfidl-imfmetadataprovider"><strong>IMFMetadataProvider</strong></a></span><span class="sxs-lookup"><span data-stu-id="7c08a-141"><a href="/windows/desktop/api/mfidl/nn-mfidl-imfmetadataprovider"><strong>IMFMetadataProvider</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7c08a-142"><strong>MF_PROPERTY_HANDLER_SERVICE</strong></span><span class="sxs-lookup"><span data-stu-id="7c08a-142"><strong>MF_PROPERTY_HANDLER_SERVICE</strong></span></span></td>
<td><span data-ttu-id="7c08a-143"><a href="/windows/desktop/api/propsys/nn-propsys-ipropertystore"><strong>IPropertyStore</strong></a>
</span><span class="sxs-lookup"><span data-stu-id="7c08a-143"><a href="/windows/desktop/api/propsys/nn-propsys-ipropertystore"><strong>IPropertyStore</strong></a>
</span></span><blockquote>
[!Note]<br />
<span data-ttu-id="7c08a-144">Consultez <a href="shell-metadata-providers.md">fournisseurs de métadonnées de Shell</a>.</span><span class="sxs-lookup"><span data-stu-id="7c08a-144">See <a href="shell-metadata-providers.md">Shell Metadata Providers</a>.</span></span>
</blockquote>
<br/> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7c08a-145"><strong>MF_RATE_CONTROL_SERVICE</strong></span><span class="sxs-lookup"><span data-stu-id="7c08a-145"><strong>MF_RATE_CONTROL_SERVICE</strong></span></span></td>
<td><span data-ttu-id="7c08a-146"><a href="/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol"><strong>IMFRateControl</strong></a></span><span class="sxs-lookup"><span data-stu-id="7c08a-146"><a href="/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol"><strong>IMFRateControl</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7c08a-147"><strong>MF_RATE_CONTROL_SERVICE</strong></span><span class="sxs-lookup"><span data-stu-id="7c08a-147"><strong>MF_RATE_CONTROL_SERVICE</strong></span></span></td>
<td><span data-ttu-id="7c08a-148"><a href="/windows/desktop/api/mfidl/nn-mfidl-imfratesupport"><strong>IMFRateSupport</strong></a></span><span class="sxs-lookup"><span data-stu-id="7c08a-148"><a href="/windows/desktop/api/mfidl/nn-mfidl-imfratesupport"><strong>IMFRateSupport</strong></a></span></span></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a><span data-ttu-id="7c08a-149">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7c08a-149">Requirements</span></span>



| <span data-ttu-id="7c08a-150">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7c08a-150">Requirement</span></span> | <span data-ttu-id="7c08a-151">Valeur</span><span class="sxs-lookup"><span data-stu-id="7c08a-151">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="7c08a-152">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7c08a-152">Minimum supported client</span></span><br/> | <span data-ttu-id="7c08a-153">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7c08a-153">Windows 7 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="7c08a-154">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7c08a-154">Minimum supported server</span></span><br/> | <span data-ttu-id="7c08a-155">Applications de bureau Windows Server 2008 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7c08a-155">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="7c08a-156">DLL</span><span class="sxs-lookup"><span data-stu-id="7c08a-156">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7c08a-157"><dt>Mf.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7c08a-157"><dt>Mf.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7c08a-158">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7c08a-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7c08a-159">Sources et récepteurs multimédias</span><span class="sxs-lookup"><span data-stu-id="7c08a-159">Media Sources and Sinks</span></span>](media-sources-and-sinks.md)
</dt> <dt>

[<span data-ttu-id="7c08a-160">Sources multimédias</span><span class="sxs-lookup"><span data-stu-id="7c08a-160">Media Sources</span></span>](media-sources.md)
</dt> <dt>

[<span data-ttu-id="7c08a-161">Résolveur source</span><span class="sxs-lookup"><span data-stu-id="7c08a-161">Source Resolver</span></span>](source-resolver.md)
</dt> <dt>

[<span data-ttu-id="7c08a-162">Formats multimédias pris en charge dans Media Foundation</span><span class="sxs-lookup"><span data-stu-id="7c08a-162">Supported Media Formats in Media Foundation</span></span>](supported-media-formats-in-media-foundation.md)
</dt> </dl>

 

 
