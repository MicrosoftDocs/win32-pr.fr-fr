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
# <a name="mft_category"></a>\_catégorie MFT

Les GUID suivants définissent des catégories pour les transformations de Media Foundation (MFTs). Ces catégories sont utilisées pour inscrire et énumérer les MFTs.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;">Constante</th>
<th style="text-align: left;">Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="MFT_CATEGORY_AUDIO_DECODER"></span><span id="mft_category_audio_decoder"></span><dl> <dt><strong>MFT_CATEGORY_AUDIO_DECODER</strong></dt> </dl></td>
<td style="text-align: left;">Décodeurs audio.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="MFT_CATEGORY_AUDIO_EFFECT"></span><span id="mft_category_audio_effect"></span><dl> <dt><strong>MFT_CATEGORY_AUDIO_EFFECT</strong></dt> </dl></td>
<td style="text-align: left;">Effets audio.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="MFT_CATEGORY_AUDIO_ENCODER"></span><span id="mft_category_audio_encoder"></span><dl> <dt><strong>MFT_CATEGORY_AUDIO_ENCODER</strong></dt> </dl></td>
<td style="text-align: left;">Encodeurs audio.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="MFT_CATEGORY_DEMULTIPLEXER"></span><span id="mft_category_demultiplexer"></span><dl> <dt><strong>MFT_CATEGORY_DEMULTIPLEXER</strong></dt> </dl></td>
<td style="text-align: left;">Démultiplexeurs.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="MFT_CATEGORY_MULTIPLEXER"></span><span id="mft_category_multiplexer"></span><dl> <dt><strong>MFT_CATEGORY_MULTIPLEXER</strong></dt> </dl></td>
<td style="text-align: left;">Multiplexeurs.<br/>
<blockquote>
[!Note]<br />
Dans Windows Vista, le pipeline Media Foundation ne prend pas en charge MFTs avec plus d’une entrée. Les MFTs à entrées multiples sont pris en charge dans Windows 7.
</blockquote>
<br/> <br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="MFT_CATEGORY_OTHER"></span><span id="mft_category_other"></span><dl> <dt><strong>MFT_CATEGORY_OTHER</strong></dt> </dl></td>
<td style="text-align: left;">MFTs divers.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="MFT_CATEGORY_VIDEO_DECODER"></span><span id="mft_category_video_decoder"></span><dl> <dt><strong>MFT_CATEGORY_VIDEO_DECODER</strong></dt> </dl></td>
<td style="text-align: left;">Décodeurs vidéo.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="MFT_CATEGORY_VIDEO_EFFECT"></span><span id="mft_category_video_effect"></span><dl> <dt><strong>MFT_CATEGORY_VIDEO_EFFECT</strong></dt> </dl></td>
<td style="text-align: left;">Effets vidéo.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="MFT_CATEGORY_VIDEO_RENDERER_EFFECT"></span><span id="mft_category_video_renderer_effect"></span><dl> <dt><strong>MFT_CATEGORY_VIDEO_RENDERER_EFFECT</strong></dt> </dl></td>
<td style="text-align: left;">Effets du convertisseur vidéo.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="MFT_CATEGORY_VIDEO_ENCODER"></span><span id="mft_category_video_encoder"></span><dl> <dt><strong>MFT_CATEGORY_VIDEO_ENCODER</strong></dt> </dl></td>
<td style="text-align: left;">Encodeurs vidéo.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="MFT_CATEGORY_VIDEO_PROCESSOR"></span><span id="mft_category_video_processor"></span><dl> <dt><strong>MFT_CATEGORY_VIDEO_PROCESSOR</strong></dt> </dl></td>
<td style="text-align: left;"><blockquote>
[!Note]<br />
Introduit dans Windows 7.
</blockquote>
<br/> Processeurs vidéo. <br/> Cette catégorie est limitée à MFTs qui effectuent des conversions de format sur la vidéo non compressée, y compris les conversions d’espace colorimétrique. Pour les effets vidéo qui modifient l’apparence de l’image (par exemple, un effet de flou ou une transformation de couleur en nuances de gris), utilisez la catégorie <strong>MFT_CATEGORY_VIDEO_EFFECT</strong> .<br/></td>
</tr>
</tbody>
</table>



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                     |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                               |
| En-tête<br/>                   | <dl> <dt>Mfapi. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Constantes Media Foundation](media-foundation-constants.md)
</dt> <dt>

[Transformations de Media Foundation](media-foundation-transforms.md)
</dt> <dt>

[**MFTEnum**](/windows/desktop/api/mfapi/nf-mfapi-mftenum)
</dt> <dt>

[**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex)
</dt> <dt>

[**MFTRegister**](/windows/desktop/api/mfapi/nf-mfapi-mftregister)
</dt> </dl>

 

 




