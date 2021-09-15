---
description: Les GUID suivants définissent des catégories pour les transformations de Media Foundation (MFTs). Ces catégories sont utilisées pour inscrire et énumérer les MFTs.
ms.assetid: eca3ae3b-e40a-407d-986c-d0a85b891f52
title: MFT_CATEGORY (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 12a65386561f18c105fde47d885ca97858131ecb
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127412891"
---
# <a name="mft_category"></a>\_catégorie MFT

Les GUID suivants définissent des catégories pour les transformations de Media Foundation (MFTs). Ces catégories sont utilisées pour inscrire et énumérer les MFTs.




| Constante | Description | 
|----------|-------------|
| <span id="MFT_CATEGORY_AUDIO_DECODER"></span><span id="mft_category_audio_decoder"></span><dl><dt><strong>MFT_CATEGORY_AUDIO_DECODER</strong></dt></dl> | Décodeurs audio.<br /> | 
| <span id="MFT_CATEGORY_AUDIO_EFFECT"></span><span id="mft_category_audio_effect"></span><dl><dt><strong>MFT_CATEGORY_AUDIO_EFFECT</strong></dt></dl> | Effets audio.<br /> | 
| <span id="MFT_CATEGORY_AUDIO_ENCODER"></span><span id="mft_category_audio_encoder"></span><dl><dt><strong>MFT_CATEGORY_AUDIO_ENCODER</strong></dt></dl> | Encodeurs audio.<br /> | 
| <span id="MFT_CATEGORY_DEMULTIPLEXER"></span><span id="mft_category_demultiplexer"></span><dl><dt><strong>MFT_CATEGORY_DEMULTIPLEXER</strong></dt></dl> | Démultiplexeurs.<br /> | 
| <span id="MFT_CATEGORY_MULTIPLEXER"></span><span id="mft_category_multiplexer"></span><dl><dt><strong>MFT_CATEGORY_MULTIPLEXER</strong></dt></dl> | Multiplexeurs.<br /><blockquote>[!Note]<br />dans Windows Vista, le pipeline Media Foundation ne prend pas en charge MFTs avec plus d’une entrée. les MFTs à entrées multiples sont pris en charge dans Windows 7.</blockquote><br /><br /> | 
| <span id="MFT_CATEGORY_OTHER"></span><span id="mft_category_other"></span><dl><dt><strong>MFT_CATEGORY_OTHER</strong></dt></dl> | MFTs divers.<br /> | 
| <span id="MFT_CATEGORY_VIDEO_DECODER"></span><span id="mft_category_video_decoder"></span><dl><dt><strong>MFT_CATEGORY_VIDEO_DECODER</strong></dt></dl> | Décodeurs vidéo.<br /> | 
| <span id="MFT_CATEGORY_VIDEO_EFFECT"></span><span id="mft_category_video_effect"></span><dl><dt><strong>MFT_CATEGORY_VIDEO_EFFECT</strong></dt></dl> | Effets vidéo.<br /> | 
| <span id="MFT_CATEGORY_VIDEO_RENDERER_EFFECT"></span><span id="mft_category_video_renderer_effect"></span><dl><dt><strong>MFT_CATEGORY_VIDEO_RENDERER_EFFECT</strong></dt></dl> | Effets du convertisseur vidéo.<br /> | 
| <span id="MFT_CATEGORY_VIDEO_ENCODER"></span><span id="mft_category_video_encoder"></span><dl><dt><strong>MFT_CATEGORY_VIDEO_ENCODER</strong></dt></dl> | Encodeurs vidéo.<br /> | 
| <span id="MFT_CATEGORY_VIDEO_PROCESSOR"></span><span id="mft_category_video_processor"></span><dl><dt><strong>MFT_CATEGORY_VIDEO_PROCESSOR</strong></dt></dl> | <blockquote>[!Note]<br />introduite dans Windows 7.</blockquote><br /> Processeurs vidéo. <br /> Cette catégorie est limitée à MFTs qui effectuent des conversions de format sur la vidéo non compressée, y compris les conversions d’espace colorimétrique. Pour les effets vidéo qui modifient l’apparence de l’image (par exemple, un effet de flou ou une transformation de couleur en nuances de gris), utilisez la catégorie <strong>MFT_CATEGORY_VIDEO_EFFECT</strong> .<br /> | 




## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                     |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                               |
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

 

 




