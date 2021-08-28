---
description: Décrit les API vidéo Direct3D 12 équivalentes aux versions précédentes.
ms.assetid: ''
title: Vidéo sur la migration vers Direct3D 12.
ms.topic: article
ms.date: 06/03/2019
ms.openlocfilehash: 4004c35c21d9d6c67c0af3f9413521cf845437cddbc2ce245c3da495ed3daca5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119777419"
---
# <a name="migrating-to-direct3d-12-video"></a>Vidéo sur la migration vers Direct3D 12.

Cet article décrit les API vidéo Direct3D 12 utilisées pour implémenter les fonctionnalités disponibles dans les versions précédentes. Dans l’intérêt d’améliorer les performances et la convivialité des fonctionnalités vidéo de priorité la plus élevée, certaines fonctionnalités de Direct3D 11 sont entièrement ou partiellement non prises en charge dans Direct3D 12. 

Notez que, bien que la plupart des fonctionnalités de Direct3D 11 soient disponibles dans Direct3D 12, la conception de l’API a changé. dans de nombreux cas, il n’y a pas de mappage un-à-un entre les deux ensembles d’API. Les tableaux ci-dessous visent à vous faire remonter aux API les plus pertinentes dans Direct3D 12 pour chaque API Direct3D 11, mais la façon dont vous utilisez les nouvelles API peut être très différente. Par exemple :

- Pour décoder une image vidéo, les API vidéo Direct3D 11 utilisent des appels à [DecoderBeginFrame](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-decoderbeginframe), [GetDecoderBuffer](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-getdecoderbuffer), [SubmitDecoderBuffers](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-submitdecoderbuffers)et [DecoderEndFrame](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-decoderendframe). Avec Direct3D 12, une seule méthode est utilisée,  [ID3D12VideoDecodeCommandList ::D ecodeframe](/windows/win32/api/d3d12video/nf-d3d12video-id3d12videodecodecommandlist-decodeframe).
- Pour le traitement vidéo, Direct3D 11 a fourni des méthodes individuelles pour définir les différentes valeurs de configuration, telles que [VideoProcessorSetOutputColorSpace](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorsetoutputcolorspace) et [VideoProcessorSetOutputAlphaFillMode](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorsetoutputalphafillmode). Dans Direct3D 12, ces valeurs sont définies lorsque le processeur vidéo est créé, dans l’appel à [ID3D12VideoDevice :: CreateVideoProcessor](/windows/win32/api/d3d12video/nf-d3d12video-id3d12videodevice-createvideoprocessor), ou lorsque le frame est traité avec un appel à [ID3D12VideoProcessCommandList1 ::P rocessframes1](/windows/win32/api/d3d12video/nf-d3d12video-id3d12videoprocesscommandlist1-processframes1).





## <a name="id3d11videocontext"></a>ID3D11VideoContext
Fournit les fonctionnalités vidéo d’un appareil Direct3D 11, y compris le décodage vidéo, le traitement vidéo, la protection du contenu basé sur GPU et le chiffrement/déchiffrement vidéo. Cette fonctionnalité est partiellement implémentée pour Direct3D 12.


| Direct3D 11 | Direct3D 12 |
|-------------|----------------|
| [ConfigureAuthenticatedChannel](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-configureauthenticatedchannel) | Non implémenté |
| [DecoderBeginFrame](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-decoderbeginframe)| [ID3D12VideoDecodeCommandList ::D ecodeframe](/windows/win32/api/d3d12video/nf-d3d12video-id3d12videodecodecommandlist-decodeframe),  [D3D12_VIDEO_DECODE_FRAME_ARGUMENT](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_video_decode_frame_argument), [D3D12_VIDEO_DECODE_COMPRESSED_BITSTREAM](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_video_decode_compressed_bitstream), [D3D12_VIDEO_DECODE_REFERENCE_FRAMES](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_video_decode_reference_frames) |
| [DecoderEndFrame](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-decoderendframe) | [ID3D12VideoDecodeCommandList](/windows/win32/api/d3d12video/nn-d3d12video-id3d12videodecodecommandlist) |
| [DecoderExtension](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-decoderextension) | Non implémenté. |
| [DecryptionBlt](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-decryptionblt)  | Non implémenté. |
| [EncryptionBlt](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-encryptionblt) | Non implémenté. |
| [FinishSessionKeyRefresh](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-finishsessionkeyrefresh) | Non implémenté. |
| [GetDecoderBuffer](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-getdecoderbuffer) | Non implémenté. Les mémoires tampons compressées sont gérées par l’application dans Direct3D 12. |
| [GetEncryptionBltKey](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-getencryptionbltkey) | Non implémenté. | 
| [NegotiateAuthenticatedChannelKeyExchange](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-negotiateauthenticatedchannelkeyexchange) | Non implémenté. |
| [NegotiateCryptoSessionKeyExchange](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-negotiatecryptosessionkeyexchange) | Non implémenté. |
| [QueryAuthenticatedChannel](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-queryauthenticatedchannel) | Non implémenté. |
| [ReleaseDecoderBuffer](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-releasedecoderbuffer) | Non implémenté. Les mémoires tampons compressées sont gérées par l’application dans Direct3D 12. |
| [StartSessionKeyRefresh](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-startsessionkeyrefresh) | Non implémenté |
| [SubmitDecoderBuffers](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-submitdecoderbuffers) | [ID3D12VideoDecodeCommandList ::D ecodeFrame](/windows/win32/api/d3d12video/nf-d3d12video-id3d12videodecodecommandlist-decodeframe) |
| [VideoProcessorBlt](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorblt) | [ID3D12VideoProcessCommandList1 ::P rocessFrames1](/windows/win32/api/d3d12video/nf-d3d12video-id3d12videoprocesscommandlist1-processframes1) |
| [VideoProcessorGetOutputAlphaFillMode](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorgetoutputalphafillmode) [VideoProcessorSetOutputAlphaFillMode](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorsetoutputalphafillmode) | [D3D12_VIDEO_PROCESS_OUTPUT_STREAM_DESC. AlphaFillMode](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_video_process_output_stream_desc) |
| [VideoProcessorGetOutputBackgroundColor](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorgetoutputbackgroundcolor) [VideoProcessorSetOutputBackgroundColor](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorsetoutputbackgroundcolor) | [D3D12_VIDEO_PROCESS_OUTPUT_STREAM_DESC. BackgroundColor](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_video_process_output_stream_desc)  |
| [VideoProcessorGetOutputColorSpace](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorgetoutputcolorspace) [VideoProcessorSetOutputColorSpace](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorsetoutputcolorspace) | [D3D12_VIDEO_PROCESS_OUTPUT_STREAM_DESC. ColorSpace](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_video_process_output_stream_desc)  |
| [VideoProcessorGetOutputConstriction](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorgetoutputconstriction) [VideoProcessorSetOutputConstriction](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorsetoutputconstriction) | Non implémenté. Le logiciel DRM n’est pas pris en charge. |
| [VideoProcessorGetOutputExtension](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorgetoutputextension) [VideoProcessorSetOutputExtension](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorsetoutputextension) | Non implémenté. |
| [VideoProcessorGetOutputStereoMode](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorgetoutputstereomode) [VideoProcessorSetOutputStereoMode](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorsetoutputstereomode) | [D3D12_VIDEO_PROCESS_OUTPUT_STREAM_DESC. EnableStereo](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_video_process_output_stream_desc) |
| [VideoProcessorGetOutputTargetRect](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorgetoutputtargetrect) [VideoProcessorSetOutputTargetRect](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorsetoutputtargetrect) | [D3D12_VIDEO_PROCESS_OUTPUT_STREAM_ARGUMENTS. TargetRectangle](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_video_process_output_stream_arguments) |
| [VideoProcessorGetStreamAlpha](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorgetstreamalpha) [VideoProcessorSetStreamAlpha](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorsetstreamalpha)  | [D3D12_VIDEO_PROCESS_ALPHA_BLENDING. Lettres](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_video_process_alpha_blending) |
| [VideoProcessorGetStreamAutoProcessingMode](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorgetstreamautoprocessingmode) [VideoProcessorSetStreamAutoProcessingMode](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorsetstreamautoprocessingmode) | [D3D12_VIDEO_PROCESS_INPUT_STREAM_DESC. EnableAutoProcessing](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_video_process_input_stream_desc) |
| [VideoProcessorGetStreamColorSpace](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorgetstreamcolorspace) [VideoProcessorSetStreamColorSpace](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorsetstreamcolorspace) | [D3D12_VIDEO_PROCESS_INPUT_STREAM_ARGUMENTS. ColorSpace](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_video_process_input_stream_desc) |
| [VideoProcessorGetStreamDestRect](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorgetstreamdestrect) [VideoProcessorSetStreamDestRect](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorsetstreamdestrect) | [D3D12_VIDEO_PROCESS_INPUT_STREAM_ARGUMENTS. DestinationRectangle](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_video_process_input_stream_desc) |
| [VideoProcessorGetStreamExtension](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorgetstreamextension) [VideoProcessorSetStreamExtension](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorsetstreamextension) | Non implémenté. |
| [VideoProcessorGetStreamFilter](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorgetstreamfilter) [VideoProcessorSetStreamFilter](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorsetstreamfilter) | [D3D12_VIDEO_PROCESS_INPUT_STREAM_ARGUMENTS. FilterFlags](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_video_process_input_stream_desc) |
| [VideoProcessorGetStreamFrameFormat](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorgetstreamframeformat) [VideoProcessorSetStreamFrameFormat](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorsetstreamframeformat) | [D3D12_VIDEO_PROCESS_INPUT_STREAM_ARGUMENTS. Format](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_video_process_input_stream_desc) |
| [VideoProcessorGetStreamLumaKey](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorgetstreamlumakey) [VideoProcessorSetStreamLumaKey](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorsetstreamlumakey) | [D3D12_VIDEO_PROCESS_INPUT_STREAM_ARGUMENTS. LumaKey](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_video_process_input_stream_desc) |
| [VideoProcessorGetStreamOutputRate](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorgetstreamoutputrate) [VideoProcessorSetStreamOutputRate](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorsetstreamoutputrate) | [D3D12_VIDEO_PROCESS_OUTPUT_STREAM_DESC. Fréquence](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_video_process_output_stream_desc) |
| [VideoProcessorGetStreamPalette](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorgetstreampalette) [VideoProcessorSetStreamPalette](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorsetstreampalette) | Non implémenté |
| [VideoProcessorGetStreamPixelAspectRatio](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorgetstreampixelaspectratio) [VideoProcessorSetStreamPixelAspectRatio](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorsetstreampixelaspectratio) | [D3D12_VIDEO_PROCESS_INPUT_STREAM_ARGUMENTS. Modifiez](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_video_process_input_stream_arguments) |
| [VideoProcessorGetStreamRotation](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorgetstreamrotation) [VideoProcessorSetStreamRotation](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorsetstreamrotation) | [D3D12_VIDEO_PROCESS_INPUT_STREAM_ARGUMENTS. Modifiez](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_video_process_input_stream_arguments) |
| [VideoProcessorGetStreamSourceRect](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorgetstreamsourcerect) [VideoProcessorSetStreamSourceRect](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorsetstreamsourcerect) | [D3D12_VIDEO_PROCESS_INPUT_STREAM_ARGUMENTS. Modifiez](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_video_process_input_stream_arguments) |
| [VideoProcessorGetStreamStereoFormat](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorgetstreamstereoformat) [VideoProcessorSetStreamStereoFormat](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorsetstreamstereoformat) | [D3D12_VIDEO_PROCESS_INPUT_STREAM_ARGUMENTS. Modifiez](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_video_process_input_stream_arguments) |

## <a name="id3d11videocontext1"></a>ID3D11VideoContext1

Fournit les fonctionnalités vidéo étendues d’un appareil Direct3D 11, y compris les fonctionnalités DRM matérielles, les améliorations de l’utilisation de la surface, ainsi que des fonctionnalités de traitement vidéo. Cette fonctionnalité est implémentée pour Direct3D 12 via de nouvelles interfaces.


| Direct3D 11 | Direct3D 12 |
|-------------|----------------|
| CheckCryptoSessionStatus | TBD | 
| [DecoderEnableDownsampling](/windows/win32/api/d3d11_1/nf-d3d11_1-id3d11videocontext1-checkcryptosessionstatus) | [D3D12_VIDEO_DECODE_CONVERSION_ARGUMENTS](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_video_decode_conversion_arguments) |
| [DecoderUpdateDownsampling](/windows/win32/api/d3d11_1/nf-d3d11_1-id3d11videocontext1-decoderenabledownsampling) | [D3D12_VIDEO_DECODE_CONVERSION_ARGUMENTS](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_video_decode_conversion_arguments) |
| [GetDataForNewHardwareKey](/windows/win32/api/d3d11_1/nf-d3d11_1-id3d11videocontext1-getdatafornewhardwarekey) | TBD |
| [SubmitDecoderBuffers1](/windows/win32/api/d3d11_1/nf-d3d11_1-id3d11videocontext1-submitdecoderbuffers1) | [ID3D12VideoDecodeCommandList ::D ecodeFrame](/windows/win32/api/d3d12video/nf-d3d12video-id3d12videodecodecommandlist-decodeframe) |
| [VideoProcessorGetBehaviorHints](/windows/win32/api/d3d11_1/nf-d3d11_1-id3d11videocontext1-videoprocessorgetbehaviorhints) | TBD |
| [VideoProcessorGetOutputColorSpace1](/windows/win32/api/d3d11_1/nf-d3d11_1-id3d11videocontext1-videoprocessorgetoutputcolorspace1) [VideoProcessorSetOutputColorSpace1](/windows/win32/api/d3d11_1/nf-d3d11_1-id3d11videocontext1-videoprocessorsetoutputcolorspace1) | [D3D12_VIDEO_PROCESS_OUTPUT_STREAM_DESC. ColorSpace](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_video_process_output_stream_desc) |
| [VideoProcessorGetOutputShaderUsage](/windows/win32/api/d3d11_1/nf-d3d11_1-id3d11videocontext1-videoprocessorgetoutputshaderusage) [VideoProcessorSetOutputShaderUsage](/windows/win32/api/d3d11_1/nf-d3d11_1-id3d11videocontext1-videoprocessorsetoutputshaderusage) | TBD |
| [VideoProcessorGetStreamColorSpace1](/windows/win32/api/d3d11_1/nf-d3d11_1-id3d11videocontext1-videoprocessorgetstreamcolorspace1) [VideoProcessorSetStreamColorSpace1](/windows/win32/api/d3d11_1/nf-d3d11_1-id3d11videocontext1-videoprocessorsetstreamcolorspace1) | [D3D12_VIDEO_PROCESS_INPUT_STREAM_DESC. ColorSpace](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_video_process_input_stream_desc) |
| [VideoProcessorGetStreamMirror](/windows/win32/api/d3d11_1/nf-d3d11_1-id3d11videocontext1-videoprocessorgetstreammirror) [VideoProcessorSetStreamMirror](/windows/win32/api/d3d11_1/nf-d3d11_1-id3d11videocontext1-videoprocessorsetstreammirror) | [D3D12_VIDEO_PROCESS_INPUT_STREAM_ARGUMENTS. Modifiez](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_video_process_input_stream_arguments) |

## <a name="id3d11videodecoder"></a>ID3D11VideoDecoder

Représente un décodeur vidéo accéléré par le matériel pour Direct3D 11. Il s’agit d’une interface de wrapper autour de [ID3D11VideoContext](/windows/win32/api/d3d11/nn-d3d11-id3d11videocontext) qui expose les fonctionnalités de décodage réelles. Il n’existe aucune API équivalente pour la vidéo Direct3D 12.


## <a name="id3d11videodecoderoutputview"></a>ID3D11VideoDecoderOutputView

Identifie les surfaces de sortie accessibles pendant le décodage vidéo. Dans Direct3D 12, l’interface [ID3D12VideoProcessor](/windows/win32/api/d3d12video/nn-d3d12video-id3d12videoprocessor) utilise les objets [ID3D12Resource](/windows/win32/api/d3d12/nn-d3d12-id3d12resource) directement.

## <a name="id3d11videodevice"></a>ID3D11VideoDevice

Fournit le décodage vidéo et les fonctionnalités de traitement vidéo d’un appareil Direct3D 11. Il s’agit du point d’entrée principal pour créer l’appareil de décodage vidéo et la session de chiffrement, ainsi que pour le traitement vidéo, les fonctionnalités, les profils, etc. Cette fonctionnalité est partiellement implémentée pour Direct3D 12.


| Direct3D 11 | Direct3D 12 |
|-------------|----------------|
| [CheckCryptoKeyExchange](/windows/win32/api/d3d11/nf-d3d11-id3d11videodevice-checkcryptokeyexchange) | Non implémenté. |
| [CheckVideoDecoderFormat](/windows/win32/api/d3d11/nf-d3d11-id3d11videodevice-checkvideodecoderformat) | [D3D12_FEATURE_DATA_VIDEO_DECODE_FORMATS](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_feature_data_video_decode_formats) |
| [CreateAuthenticatedChannel](/windows/win32/api/d3d11/nf-d3d11-id3d11videodevice-createauthenticatedchannel) | Non implémenté. |
| [CreateCryptoSession](/windows/win32/api/d3d11/nf-d3d11-id3d11videodevice-createcryptosession) | Non implémenté. |
| [CreateVideoDecoder](/windows/win32/api/d3d11/nf-d3d11-id3d11videodevice-createvideodecoder) | [ID3D12VideoDevice :: CreateVideoDecoder](/windows/win32/api/d3d12video/nf-d3d12video-id3d12videodevice-createvideodecoder)  [ID3D12VideoDevice :: CreateVideoDecoderHeap](/windows/win32/api/d3d12video/nf-d3d12video-id3d12videodevice-createvideodecoderheap) |
| [CreateVideoDecoderOutputView](/windows/win32/api/d3d11/nf-d3d11-id3d11videodevice-createvideodecoderoutputview) | [ID3D12Texture2D](/windows/win32/api/d3d11/nn-d3d11-id3d11texture2d) |
| [CreateVideoProcessor](/windows/win32/api/d3d11/nf-d3d11-id3d11videodevice-createvideoprocessor) | [ID3D12VideoDevice::CreateVideoProcessor](/windows/win32/api/d3d12video/nf-d3d12video-id3d12videodevice-createvideoprocessor)  |
| [CreateVideoProcessorEnumerator](/windows/win32/api/d3d11/nf-d3d11-id3d11videodevice-createvideoprocessorenumerator) | N/A |
| [CreateVideoProcessorInputView](/windows/win32/api/d3d11/nf-d3d11-id3d11videodevice-createvideoprocessorinputview) | [ID3D12Texture2D](/windows/win32/api/d3d11/nn-d3d11-id3d11texture2d) |
| [CreateVideoProcessorOutputView](/windows/win32/api/d3d11/nf-d3d11-id3d11videodevice-createvideoprocessoroutputview) | [ID3D12Texture2D](/windows/win32/api/d3d11/nn-d3d11-id3d11texture2d) |
| [GetContentProtectionCaps](/windows/win32/api/d3d11/nf-d3d11-id3d11videodevice-getcontentprotectioncaps) | TBD
| [GetVideoDecoderConfig](/windows/win32/api/d3d11/nf-d3d11-id3d11videodevice-getvideodecoderconfig) | Seul le mode VLD est pris en charge dans Direct3D 12. [D3D12_FEATURE_DATA_VIDEO_DECODE_PROFILES](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_feature_data_video_decode_profiles) [D3D12_FEATURE_DATA_VIDEO_DECODE_FORMATS](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_feature_data_video_decode_formats) |
| [GetVideoDecoderConfigCount](/windows/win32/api/d3d11/nf-d3d11-id3d11videodevice-getvideodecoderconfigcount) | N/A |
| [GetVideoDecoderProfile](/windows/win32/api/d3d11/nf-d3d11-id3d11videodevice-getvideodecoderprofile) | [D3D12_FEATURE_DATA_VIDEO_DECODE_PROFILES](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_feature_data_video_decode_profiles) |
| [GetVideoDecoderProfileCount](/windows/win32/api/d3d11/nf-d3d11-id3d11videodevice-getvideodecoderprofilecount) | [D3D12_FEATURE_DATA_VIDEO_DECODE_PROFILES. ProfileCount](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_feature_data_video_decode_profiles) |
| [SetPrivateData](/windows/win32/api/d3d11/nf-d3d11-id3d11videodevice-setprivatedata) | [ID3D12Object::SetPrivateData](/windows/win32/api/d3d12/nf-d3d12-id3d12object-setprivatedata) |
| [SetPrivateDataInterface](/windows/win32/api/d3d11/nf-d3d11-id3d11videodevice-setprivatedatainterface) | [ID3D12Object::SetPrivateDataInterface](/windows/win32/api/d3d12/nf-d3d12-id3d12object-setprivatedatainterface) |

## <a name="id3d11videodevice1"></a>ID3D11VideoDevice1

Fournit des fonctionnalités étendues de traitement vidéo et de décodage vidéo d’un appareil Direct3D 11, y compris d’autres extensions, des fonctionnalités DRM matérielles, des sous-échantillonnages de décodage, des fonctionnalités de décodage vidéo, etc. Cette fonctionnalité est implémentée pour Direct3D 12.

| Direct3D 11 | Direct3D 12 |
|-------------|----------------|
| [CheckVideoDecoderDownsampling](/windows/win32/api/d3d11_1/nf-d3d11_1-id3d11videodevice1-checkvideodecoderdownsampling) | [D3D12_FEATURE_DATA_VIDEO_DECODE_CONVERSION_SUPPORT](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_feature_data_video_decode_conversion_support) |
| [GetCryptoSessionPrivateDataSize](/windows/win32/api/d3d11_1/nf-d3d11_1-id3d11videodevice1-getcryptosessionprivatedatasize) | TBD |
| [GetVideoDecoderCaps](/windows/win32/api/d3d11_1/nf-d3d11_1-id3d11videodevice1-getvideodecodercaps) | [D3D12_FEATURE_DATA_VIDEO_DECODE_CONVERSION_SUPPORT](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_feature_data_video_decode_conversion_support) |
| [RecommendVideoDecoderDownsampleParameters](/windows/win32/api/d3d11_1/nf-d3d11_1-id3d11videodevice1-recommendvideodecoderdownsampleparameters) | [D3D12_FEATURE_DATA_VIDEO_DECODE_CONVERSION_SUPPORT](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_feature_data_video_decode_conversion_support) |


## <a name="id3d11videoprocessor"></a>ID3D11VideoProcessor

Représente un processeur vidéo pour Direct3D 11. Cette fonctionnalité est implémentée pour Direct3D 12 dans le [ID3D12VideoProcessor](/windows/win32/api/d3d12video/nn-d3d12video-id3d12videoprocessor)

| Direct3D 11 | Direct3D 12 |
|-------------|----------------|
| [GetContentDesc](/windows/win32/api/d3d11/nf-d3d11-id3d11videoprocessor-getcontentdesc)| Non implémenté |
| [GetRateConversionCaps](/windows/win32/api/d3d11/nf-d3d11-id3d11videoprocessor-getrateconversioncaps) | Non implémenté |


## <a name="id3d11videoprocessorenumerator-and-id3d11videoprocessorenumerator1"></a>ID3D11VideoProcessorEnumerator et ID3D11VideoProcessorEnumerator1

Énumère les fonctionnalités du processeur vidéo d’un appareil Direct3D 11.
Dans Direct3D 12, la fonctionnalité d’énumération est remplacée par [ID3D12VideoDevice :: CheckFeatureSupport](/windows/win32/api/d3d12video/nf-d3d12video-id3d12videodevice-checkfeaturesupport). 

##  <a name="id3d11videoprocessorinputview"></a>ID3D11VideoProcessorInputView

Identifie les surfaces d’entrée accessibles pendant le traitement vidéo.
Dans Direct3D 12, il est remplacé par ID3D12Texture2D.

##  <a name="id3d11videoprocessoroutputview"></a>ID3D11VideoProcessorOutputView

Identifie les surfaces de sortie accessibles pendant le traitement vidéo.
Dans Direct3D 12, il est remplacé par ID3D12Texture2D.

## <a name="id3d11authenticatedchannel"></a>ID3D11AuthenticatedChannel

Fournit un canal de communication sécurisé avec le pilote Graphics ou le runtime Microsoft Direct3D. Cette fonctionnalité n’est pas implémentée pour la vidéo Direct3D 12.

##  <a name="id3d11cryptosession"></a>ID3D11CryptoSession

Représente une session de chiffrement. Utilisé pour les scénarios DRM logiciels et matériels. Il n’existe aucune API publique équivalente pour Direct3D 12 Video.

## <a name="related-topics"></a>Rubriques connexes

[API vidéo Direct3D 12](direct3d-12-video-apis.md)


 

 




