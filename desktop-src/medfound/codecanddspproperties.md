---
description: Les constantes codec et DSP IPropertyBag.
ms.assetid: 078b0eea-16dd-4427-b984-9e52a43de559
title: Constantes codec et DSP IPropertyBag
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88dcf85e22f55082bb9e2c49041490f4c7aceb2d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111879"
---
# <a name="codec-and-dsp-ipropertybag-constants"></a>Constantes codec et DSP IPropertyBag

Il existe deux méthodes de définition des propriétés sur le codec et les objets DSP par programme, à l’aide de l’interface **IPropertyBag** ou de l’interface **IPropertyStore** . La plupart des propriétés communes sont disponibles via les deux interfaces. L’utilisation de l’interface **IPropertyStore** est préférable à **IPropertyBag**.



| Constante de chaîne IPropertyBag          | Clé de propriété IPropertyStore                                                                         |
|---------------------------------------|-----------------------------------------------------------------------------------------------------|
| \_wszAvgFrameRate g                    | [MFPKEY \_ ASFOVERHEADPERFRAME](mfpkey-asfoverheadperframeproperty.md)                               |
| \_wszWMACAvgBytesPerSecond g           | [MFPKEY \_ WMAENC \_ AVGBYTESPERSEC](mfpkey-wmaenc-avgbytespersecproperty.md)                          |
| \_wszWMACDRCSetting g                  | [MFPKEY \_ WMADEC \_ DRCMODE](mfpkey-wmadec-drcmodeproperty.md)                                        |
| \_wszWMACHiResOutput g                 | [MFPKEY \_ WMADEC \_ HIRESOUTPUT](mfpkey-wmadec-hiresoutputproperty.md)                                |
| \_wszWMACMusicSpeechClassMode g        | [MFPKEY \_ WMAVOICE \_ enc \_ MusicSpeechClassMode](mfpkey-wmavoice-enc-musicspeechclassmodeproperty.md) |
| \_wszWMACOriginalWaveFormat g          | [MFPKEY \_ WMAENC \_ ORIGWAVEFORMAT](mfpkey-wmaenc-origwaveformatproperty.md)                          |
| \_wszWMACSpeakerConfig g               | [MFPKEY \_ WMADEC \_ SPKRCFG](mfpkey-wmadec-spkrcfgproperty.md)                                        |
| \_wszWMACVoiceBuffer g                 | [MFPKEY \_ WMAVOICE \_ enc \_ BufferWindow](mfpkey-wmavoice-enc-bufferwindowproperty.md)                 |
| \_wszWMACVoiceBuffer g                 | [\_EDL MFPKEY WMAVOICE \_ enc \_](mfpkey-wmavoice-enc-edlproperty.md)                                   |
| \_wszWMADRCAverageReference g          | [MFPKEY \_ WMADRC \_ AVGREF](mfpkey-wmadrc-avgrefproperty.md)                                          |
| \_wszWMADRCAverageTarget g             | [MFPKEY \_ WMADRC \_ AVGTARGET](mfpkey-wmadrc-avgtargetproperty.md)                                    |
| \_wszWMADRCPeakReference g             | [MFPKEY \_ WMADRC \_ PEAKREF](mfpkey-wmadrc-peakrefproperty.md)                                        |
| \_wszWMADRCPeakTarget g                | [MFPKEY \_ WMADRC \_ PEAKTARGET](mfpkey-wmadrc-peaktargetproperty.md)                                  |
| \_wszWMCPAudioVBRQuality g             | [MFPKEY \_ VBRQUALITY](mfpkey-vbrqualityproperty.md)                                                 |
| \_wszWMCPAudioVBRSupported g           | [MFPKEY \_ VBRENABLED](mfpkey-vbrenabledproperty.md)                                                 |
| \_wszWMCPMaxPasses g                   | [MFPKEY \_ PASSESRECOMMENDED](mfpkey-passesrecommendedproperty.md)                                   |
| \_wszWMVCAvgBitrate g                  | [MFPKEY \_ RAVG](mfpkey-ravgproperty.md)                                                             |
| \_wszWMVCBAvg g                        | [MFPKEY \_ BAVG](mfpkey-bavgproperty.md)                                                             |
| \_wszWMVCBDeltaQP g                    | [MFPKEY \_ BDELTAQP](mfpkey-bdeltaqpproperty.md)                                                     |
| \_wszWMVCBMax g                        | [MFPKEY \_ BMAX](mfpkey-bmaxproperty.md)                                                             |
| \_wszWMVCBufferFullnessInFirstByte g   | [MFPKEY \_ BUFFERFULLNESSINFIRSTBYTE](mfpkey-bufferfullnessinfirstbyteproperty.md)                   |
| \_wszWMVCCodedFrames g                 | [MFPKEY \_ CODEDFRAMES](mfpkey-codedframesproperty.md)                                               |
| \_wszWMVCComplexityEx g                | [MFPKEY \_ COMPLEXITYEX](mfpkey-complexityexproperty.md)                                             |
| \_wszWMVCComplexityMode g              | [\_complexité MFPKEY](mfpkey-complexityproperty.md)                                                 |
| \_wszWMVCCompressionOptimizationType g | [MFPKEY \_ COMPRESSIONOPTIMIZATIONTYPE](mfpkey-compressionoptimizationtypeproperty.md)               |
| \_wszWMVCCrisp g                       | [MFPKEY \_ clair](mfpkey-crispproperty.md)                                                           |
| \_wszWMVCDecoderComplexityProfile g    | [MFPKEY \_ DECODERCOMPLEXITYPROFILE](mfpkey-decodercomplexityprofileproperty.md)                     |
| \_wszWMVCDecoderComplexityRequested g  | [MFPKEY \_ DECODERCOMPLEXITYREQUESTED](mfpkey-decodercomplexityrequestedproperty.md)                 |
| \_wszWMVCDecoderDeinterlacing g        | [\_désentrelacer le DÉcodeur MFPKEY \_](mfpkey-decoder-deinterlacingproperty.md)                          |
| \_wszWMVCDenoiseOption g               | [MFPKEY \_ DENOISEOPTION](mfpkey-denoiseoptionproperty.md)                                           |
| \_wszWMVCEndOfPass g                   | [MFPKEY \_ ENDOFPASS](mfpkey-endofpassproperty.md)                                                   |
| \_wszWMVCForceFrameHeight g            | [MFPKEY \_ FORCEFRAMEHEIGHT](mfpkey-forceframeheightproperty.md)                                     |
| \_wszWMVCForceFrameWidth g             | [MFPKEY \_ FORCEFRAMEWIDTH](mfpkey-forceframewidthproperty.md)                                       |
| \_wszWMVCForceMedianSetting g          | [MFPKEY \_ FORCEMEDIANSETTING](mfpkey-forcemediansettingproperty.md)                                 |
| \_wszWMVCFOURCC g                      | [MFPKEY \_ FourCC](mfpkey-fourccproperty.md)                                                         |
| \_wszWMVCInterlacedCodingEnabled g     | [MFPKEY \_ INTERLACEDCODINGENABLED](mfpkey-interlacedcodingenabledproperty.md)                       |
| \_wszWMVCLookAhead g                   | [préanalyse MFPKEY \_](mfpkey-lookaheadproperty.md)                                                   |
| \_wszWMVCLoopFilter g                  | [MFPKEY \_ LOOPFILTER](mfpkey-loopfilterproperty.md)                                                 |
| \_wszWMVCMacroblockModeCostMethod g    | [MFPKEY \_ MACROBLOCKMODECOSTMETHOD](mfpkey-macroblockmodecostmethodproperty.md)                     |
| \_wszWMVCMaxBitrate g                  | [MFPKEY \_ Rmax](mfpkey-rmaxproperty.md)                                                             |
| \_wszWMVCMotionMatchMethod g           | [MFPKEY \_ MOTIONMATCHMETHOD](mfpkey-motionmatchmethodproperty.md)                                   |
| \_wszWMVCMotionSearchLevel g           | [MFPKEY \_ MOTIONSEARCHLEVEL](mfpkey-motionsearchlevelproperty.md)                                   |
| \_wszWMVCMotionSearchRange g           | [MFPKEY \_ MOTIONSEARCHRANGE](mfpkey-motionsearchrangeproperty.md)                                   |
| \_wszWMVCNoiseEdgeRemoval g            | [MFPKEY \_ NOISEEDGEREMOVAL](mfpkey-noiseedgeremovalproperty.md)                                     |
| \_wszWMVCNumThreads g                  | [MFPKEY \_ NUMTHREADS](mfpkey-numthreadsproperty.md)                                                 |
| \_wszWMVCPassesRecommended g           | [MFPKEY \_ PASSESRECOMMENDED](mfpkey-passesrecommendedproperty.md)                                   |
| \_wszWMVCPassesUsed g                  | [MFPKEY \_ PASSESUSED](mfpkey-passesusedproperty.md)                                                 |
| \_wszWMVCPerceptualOptLevel g          | [MFPKEY \_ PERCEPTUALOPTLEVEL](mfpkey-perceptualoptlevelproperty.md)                                 |
| \_wszWMVCProduceDummyFrames g          | [MFPKEY \_ PRODUCEDUMMYFRAMES](mfpkey-producedummyframesproperty.md)                                 |
| \_wszWMVCRangeRedux g                  | [MFPKEY \_ RANGEREDUX](mfpkey-rangereduxproperty.md)                                                 |
| \_wszWMVCTotalFrames g                 | [MFPKEY \_ TOTALFRAMES](mfpkey-totalframesproperty.md)                                               |
| \_wszWMVCVBREnabled g                  | [MFPKEY \_ VBRENABLED](mfpkey-vbrenabledproperty.md)                                                 |
| \_wszWMVCVBRQuality g                  | [MFPKEY \_ VBRQUALITY](mfpkey-vbrqualityproperty.md)                                                 |
| \_wszWMVCVideoScaling g                | [MFPKEY \_ VIDEOSCALING](mfpkey-videoscalingproperty.md)                                             |
| \_wszWMVCVType g                       | [MFPKEY \_ VTYPE](mfpkey-vtypeproperty.md)                                                           |
| \_wszWMVCZeroByteFrames g              | [MFPKEY \_ ZEROBYTEFRAMES](mfpkey-zerobyteframesproperty.md)                                         |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Codecs Windows Media](windows-media-codecs.md)
</dt> </dl>

 

 



