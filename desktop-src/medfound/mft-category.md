---
description: Les GUID suivants définissent des catégories pour les transformations de Media Foundation (MFTs). Ces catégories sont utilisées pour inscrire et énumérer les MFTs.
ms.assetid: eca3ae3b-e40a-407d-986c-d0a85b891f52
title: MFT_CATEGORY (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cb7bc74054ad9f201b1f2ca53b526826d34c510d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863965"
---
# <a name="mft_category"></a><span data-ttu-id="ca893-104">\_catégorie MFT</span><span class="sxs-lookup"><span data-stu-id="ca893-104">MFT\_CATEGORY</span></span>

<span data-ttu-id="ca893-105">Les GUID suivants définissent des catégories pour les transformations de Media Foundation (MFTs).</span><span class="sxs-lookup"><span data-stu-id="ca893-105">The following GUIDs define categories for Media Foundation transforms (MFTs).</span></span> <span data-ttu-id="ca893-106">Ces catégories sont utilisées pour inscrire et énumérer les MFTs.</span><span class="sxs-lookup"><span data-stu-id="ca893-106">These categories are used to register and enumerate MFTs.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="ca893-107">Constante</span><span class="sxs-lookup"><span data-stu-id="ca893-107">Constant</span></span></th>
<th style="text-align: left;"><span data-ttu-id="ca893-108">Description</span><span class="sxs-lookup"><span data-stu-id="ca893-108">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="MFT_CATEGORY_AUDIO_DECODER"></span><span id="mft_category_audio_decoder"></span><dl> <span data-ttu-id="ca893-109"><dt><strong>MFT_CATEGORY_AUDIO_DECODER</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="ca893-109"><dt><strong>MFT_CATEGORY_AUDIO_DECODER</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="ca893-110">Décodeurs audio.</span><span class="sxs-lookup"><span data-stu-id="ca893-110">Audio decoders.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="MFT_CATEGORY_AUDIO_EFFECT"></span><span id="mft_category_audio_effect"></span><dl> <span data-ttu-id="ca893-111"><dt><strong>MFT_CATEGORY_AUDIO_EFFECT</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="ca893-111"><dt><strong>MFT_CATEGORY_AUDIO_EFFECT</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="ca893-112">Effets audio.</span><span class="sxs-lookup"><span data-stu-id="ca893-112">Audio effects.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="MFT_CATEGORY_AUDIO_ENCODER"></span><span id="mft_category_audio_encoder"></span><dl> <span data-ttu-id="ca893-113"><dt><strong>MFT_CATEGORY_AUDIO_ENCODER</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="ca893-113"><dt><strong>MFT_CATEGORY_AUDIO_ENCODER</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="ca893-114">Encodeurs audio.</span><span class="sxs-lookup"><span data-stu-id="ca893-114">Audio encoders.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="MFT_CATEGORY_DEMULTIPLEXER"></span><span id="mft_category_demultiplexer"></span><dl> <span data-ttu-id="ca893-115"><dt><strong>MFT_CATEGORY_DEMULTIPLEXER</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="ca893-115"><dt><strong>MFT_CATEGORY_DEMULTIPLEXER</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="ca893-116">Démultiplexeurs.</span><span class="sxs-lookup"><span data-stu-id="ca893-116">Demultiplexers.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="MFT_CATEGORY_MULTIPLEXER"></span><span id="mft_category_multiplexer"></span><dl> <span data-ttu-id="ca893-117"><dt><strong>MFT_CATEGORY_MULTIPLEXER</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="ca893-117"><dt><strong>MFT_CATEGORY_MULTIPLEXER</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="ca893-118">Multiplexeurs.</span><span class="sxs-lookup"><span data-stu-id="ca893-118">Multiplexers.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="ca893-119">Dans Windows Vista, le pipeline Media Foundation ne prend pas en charge MFTs avec plus d’une entrée.</span><span class="sxs-lookup"><span data-stu-id="ca893-119">In Windows Vista, the Media Foundation pipeline does not support MFTs with more than one input.</span></span> <span data-ttu-id="ca893-120">Les MFTs à entrées multiples sont pris en charge dans Windows 7.</span><span class="sxs-lookup"><span data-stu-id="ca893-120">Multiple-input MFTs are supported in Windows 7.</span></span>
</blockquote>
<br/> <br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="MFT_CATEGORY_OTHER"></span><span id="mft_category_other"></span><dl> <span data-ttu-id="ca893-121"><dt><strong>MFT_CATEGORY_OTHER</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="ca893-121"><dt><strong>MFT_CATEGORY_OTHER</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="ca893-122">MFTs divers.</span><span class="sxs-lookup"><span data-stu-id="ca893-122">Miscellaneous MFTs.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="MFT_CATEGORY_VIDEO_DECODER"></span><span id="mft_category_video_decoder"></span><dl> <span data-ttu-id="ca893-123"><dt><strong>MFT_CATEGORY_VIDEO_DECODER</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="ca893-123"><dt><strong>MFT_CATEGORY_VIDEO_DECODER</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="ca893-124">Décodeurs vidéo.</span><span class="sxs-lookup"><span data-stu-id="ca893-124">Video decoders.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="MFT_CATEGORY_VIDEO_EFFECT"></span><span id="mft_category_video_effect"></span><dl> <span data-ttu-id="ca893-125"><dt><strong>MFT_CATEGORY_VIDEO_EFFECT</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="ca893-125"><dt><strong>MFT_CATEGORY_VIDEO_EFFECT</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="ca893-126">Effets vidéo.</span><span class="sxs-lookup"><span data-stu-id="ca893-126">Video effects.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="MFT_CATEGORY_VIDEO_RENDERER_EFFECT"></span><span id="mft_category_video_renderer_effect"></span><dl> <span data-ttu-id="ca893-127"><dt><strong>MFT_CATEGORY_VIDEO_RENDERER_EFFECT</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="ca893-127"><dt><strong>MFT_CATEGORY_VIDEO_RENDERER_EFFECT</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="ca893-128">Effets du convertisseur vidéo.</span><span class="sxs-lookup"><span data-stu-id="ca893-128">Video renderer effects.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="MFT_CATEGORY_VIDEO_ENCODER"></span><span id="mft_category_video_encoder"></span><dl> <span data-ttu-id="ca893-129"><dt><strong>MFT_CATEGORY_VIDEO_ENCODER</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="ca893-129"><dt><strong>MFT_CATEGORY_VIDEO_ENCODER</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="ca893-130">Encodeurs vidéo.</span><span class="sxs-lookup"><span data-stu-id="ca893-130">Video encoders.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="MFT_CATEGORY_VIDEO_PROCESSOR"></span><span id="mft_category_video_processor"></span><dl> <span data-ttu-id="ca893-131"><dt><strong>MFT_CATEGORY_VIDEO_PROCESSOR</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="ca893-131"><dt><strong>MFT_CATEGORY_VIDEO_PROCESSOR</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><blockquote>
[!Note]<br />
<span data-ttu-id="ca893-132">Introduit dans Windows 7.</span><span class="sxs-lookup"><span data-stu-id="ca893-132">Introduced in Windows 7.</span></span>
</blockquote>
<br/> <span data-ttu-id="ca893-133">Processeurs vidéo.</span><span class="sxs-lookup"><span data-stu-id="ca893-133">Video processors.</span></span> <br/> <span data-ttu-id="ca893-134">Cette catégorie est limitée à MFTs qui effectuent des conversions de format sur la vidéo non compressée, y compris les conversions d’espace colorimétrique.</span><span class="sxs-lookup"><span data-stu-id="ca893-134">This category is limited to MFTs that perform format conversions on uncompressed video, including color-space conversions.</span></span> <span data-ttu-id="ca893-135">Pour les effets vidéo qui modifient l’apparence de l’image (par exemple, un effet de flou ou une transformation de couleur en nuances de gris), utilisez la catégorie <strong>MFT_CATEGORY_VIDEO_EFFECT</strong> .</span><span class="sxs-lookup"><span data-stu-id="ca893-135">For video effects that modify the appearance of the image (such as a blur effect or a color-to-grayscale transform), use the <strong>MFT_CATEGORY_VIDEO_EFFECT</strong> category.</span></span><br/></td>
</tr>
</tbody>
</table>



## <a name="requirements"></a><span data-ttu-id="ca893-136">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ca893-136">Requirements</span></span>



| <span data-ttu-id="ca893-137">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ca893-137">Requirement</span></span> | <span data-ttu-id="ca893-138">Valeur</span><span class="sxs-lookup"><span data-stu-id="ca893-138">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="ca893-139">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ca893-139">Minimum supported client</span></span><br/> | <span data-ttu-id="ca893-140">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ca893-140">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="ca893-141">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ca893-141">Minimum supported server</span></span><br/> | <span data-ttu-id="ca893-142">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ca893-142">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="ca893-143">En-tête</span><span class="sxs-lookup"><span data-stu-id="ca893-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="ca893-144"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="ca893-144"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ca893-145">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ca893-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ca893-146">Constantes Media Foundation</span><span class="sxs-lookup"><span data-stu-id="ca893-146">Media Foundation Constants</span></span>](media-foundation-constants.md)
</dt> <dt>

[<span data-ttu-id="ca893-147">Transformations de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="ca893-147">Media Foundation Transforms</span></span>](media-foundation-transforms.md)
</dt> <dt>

[<span data-ttu-id="ca893-148">**MFTEnum**</span><span class="sxs-lookup"><span data-stu-id="ca893-148">**MFTEnum**</span></span>](/windows/desktop/api/mfapi/nf-mfapi-mftenum)
</dt> <dt>

[<span data-ttu-id="ca893-149">**MFTEnumEx**</span><span class="sxs-lookup"><span data-stu-id="ca893-149">**MFTEnumEx**</span></span>](/windows/desktop/api/mfapi/nf-mfapi-mftenumex)
</dt> <dt>

[<span data-ttu-id="ca893-150">**MFTRegister**</span><span class="sxs-lookup"><span data-stu-id="ca893-150">**MFTRegister**</span></span>](/windows/desktop/api/mfapi/nf-mfapi-mftregister)
</dt> </dl>

 

 




