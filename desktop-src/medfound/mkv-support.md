---
description: Cette section décrit la prise en charge Media Foundation pour les fichiers Matroska Media Container (MKV).
title: Prise en charge de Matroska Media Container (MKV)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aceb7a836b4a0409af3c359c8d81a0f232e6eb61082960cfb2b0705531de199c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119102139"
---
# <a name="matroska-media-container-mkv-support"></a>Prise en charge de Matroska Media Container (MKV)

Cette section décrit la prise en charge Media Foundation pour les fichiers Matroska Media Container (MKV).

Le format MKV peut prendre en charge plusieurs codecs vidéo et audio, comme H. 264 et AAC audio. En général, les conteneurs décrivent la disposition des données audio et vidéo et les informations supplémentaires qui sont utilisées pour décrire ces flux A/V. Les conteneurs peuvent également inclure des données qui complètent les flux A/V, telles que le titre, les langues des flux audio, les pistes de sous-titre ou de légende, les polices pour ces sous-titres, images, informations de chapitre et menus. MKV est un format très flexible qui prend en charge un grand nombre de ces fonctionnalités de conteneur. Pour plus d’informations sur le format MKV, consultez [https://matroska.org](https://matroska.org/)


## <a name="mkv-container-feature-support"></a>Prise en charge des fonctionnalités de conteneur MKV
Les fonctionnalités de conteneur MKV sont prises en charge sur le par Media Foundation des manières suivantes :
- Si une ou plusieurs pistes vidéo sont présentes, la première piste est lue.
- Si une ou plusieurs pistes audio sont présentes, la première piste est lue.
- Les suivis de légende sont pris en charge, mais ne sont pas sélectionnés (lus) par défaut.
- Si une ou plusieurs polices ou images sont présentes, les légendes et les images ne sont pas rendues, même si le fichier est chargé et lu.
- Les informations de menu ne sont pas prises en charge et ne sont pas affichées, mais le fichier est chargé et lu.
- Si les fichiers contenant des chapitres font référence à des fichiers supplémentaires, les fichiers supplémentaires ne sont pas lus.
- Les images miniatures sont disponibles lorsque vous recherchez des fichiers sur des lecteurs USB à l’aide de l’Explorateur de fichiers.

Cet ensemble de fonctionnalités doit permettre la lecture de la plupart des fichiers MKV s’ils contiennent des codecs pris en charge.
Les fichiers MKV qui contiennent des pistes vidéo et audio encodées avec les codecs répertoriés dans la section suivante sont pris en charge.

## <a name="supported-mkv-codecs"></a>Codecs MKV pris en charge

### <a name="video-codec-support-for-mkv"></a>Prise en charge des codecs vidéo pour MKV

ID Matroska : V_MPEG4/ISO/AVC

- MF_MT_SUBTYPE Media Foundation MSFT : MFVideoFormat_H264
- Description : vidéo H. 264
- Identificateurs FourCC ou WAV : H264 –

ID Matroska : V_MPEG2

- MF_MT_SUBTYPE Media Foundation MSFT : MFVideoFormat_MPEG2
- Description : vidéo MPEG-2

ID Matroska : V_MPEG1

- MF_MT_SUBTYPE Media Foundation MSFT : MFVideoFormat_MPG1
- Description : MPEG-1 Video
- Identificateurs FourCC ou WAV : MPG1

ID Matroska : V_MPEG4/MS/V3

- MF_MT_SUBTYPE Media Foundation MSFT : MFVideoFormat_MP43
- Description : codec Microsoft MPEG 4 version 3
- Identificateurs FourCC ou WAV : MP43

ID Matroska : V_MPEG4/ISO/ASP

- MF_MT_SUBTYPE Media Foundation MSFT : MFVideoFormat_MP4V
- Description : vidéo MPEG-4 part 2
- Identificateurs FourCC ou WAV : MP4V

ID Matroska : V_MS/VFW/FOURCC

- Description : Cartes à plusieurs codecs généralement pris en charge dans le format AVI et disponibles sur la console.

ID Matroska : V_THEORA

- MF_MT_SUBTYPE Media Foundation MSFT : MFVideoFormat_Theora
- Description : Theora
- Identificateurs FourCC ou WAV : Theo

ID Matroska : V_MPEG4/ISO/SP

- MF_MT_SUBTYPE Media Foundation MSFT : MFVideoFormat_MP4V
- Description : profil simple ISO MPEG4 (DivX4)
- Identificateurs FourCC ou WAV : MP4V

ID Matroska : V_MPEG4/ISO/AP

- MF_MT_SUBTYPE Media Foundation MSFT : MFVideoFormat_MP4V
- Description : profil simple Advanced standard MPEG4 ISO (DivX5, XviD, FFMPEG)
- Identificateurs FourCC ou WAV : MP4V


ID Matroska : V_MPEGH/ISO/HEVC 

- MF_MT_SUBTYPE Media Foundation MSFT : MFVideoFormat_HEVC
- Description : HEVC/H. 265
- Identificateurs FourCC ou WAV : 

ID Matroska : V_VP8

- MF_MT_SUBTYPE Media Foundation MSFT : MFVideoFormat_VP80
- Description : format du codec VP8
- Identificateurs FourCC ou WAV : VP80

ID Matroska : V_VP9

- MF_MT_SUBTYPE Media Foundation MSFT : MFVideoFormat_VP90
- Description : format du codec VP9
- Identificateurs FourCC ou WAV : VP90

ID Matroska : V_MJPEG

- MF_MT_SUBTYPE Media Foundation MSFT : MFVideoFormat_MJPG
- Description : Motion JPEG
- Identificateurs FourCC ou WAV : MJPG

ID Matroska : V_AV1

- MF_MT_SUBTYPE Media Foundation MSFT : MFVideoFormat_AV1
- Description : AOMedia Video 1
- Identificateurs FourCC ou WAV : AV01

### <a name="audio-codec-support-for-mkv"></a>Prise en charge des codecs audio pour MKV

ID Matroska : A_AAC

- MF_MT_SUBTYPE Media Foundation MSFT : MFAudioFormat_AAC
- Description : codage audio avancé (AAC)
- Identificateurs FourCC ou WAV : WAVE_FORMAT_MPEG_HEAAC

ID Matroska : A_AC3

- MF_MT_SUBTYPE Media Foundation MSFT : MFAudioFormat_Dolby_AC3
- Description : Dolby AC3
- Identificateurs FourCC ou WAV : WAVE_FORMAT_DOLBY_AC3_SPDIF

ID Matroska : A_MPEG/L3

- MF_MT_SUBTYPE Media Foundation MSFT : MFAudioFormat_MP3
- Description : MPEG Audio Layer-3 (MP3)
- Identificateurs FourCC ou WAV : WAVE_FORMAT_MPEGLAYER3

ID Matroska : A_MPEG/L1

- MF_MT_SUBTYPE Media Foundation MSFT : MFAudioFormat_MPEG
- Description : charge utile MPEG-1
- Identificateurs FourCC ou WAV : WAVE_FORMAT_MPEG

ID Matroska : A_PCM/INT/BIG

- MF_MT_SUBTYPE Media Foundation MSFT : MFAudioFormat_PCM
- Description : audio PCM non compressé
- Identificateurs FourCC ou WAV : WAVE_FORMAT_PCM

ID Matroska : A_PCM/INT/LIT

- MF_MT_SUBTYPE Media Foundation MSFT : MFAudioFormat_PCM
- Description : audio PCM non compressé
- Identificateurs FourCC ou WAV : WAVE_FORMAT_PCM

ID Matroska : A_PCM/FLOAT/IEEE

- MF_MT_SUBTYPE Media Foundation MSFT : MFAudioFormat_Float
- Description : audio à virgule flottante IEEE non compressé
- Identificateurs FourCC ou WAV : WAVE_FORMAT_IEEE_FLOAT

ID Matroska : A_ALAC

- MF_MT_SUBTYPE Media Foundation MSFT : MFAudioFormat_ALAC
- Description : codec audio Apple sans perte
- Identificateurs FourCC ou WAV : 

ID Matroska : A_MPEG/L2

- MF_MT_SUBTYPE Media Foundation MSFT : MFAudioFormat_MPEG
- Description : MPEG Audio 1, 2 couche II
- Identificateurs FourCC ou WAV : WAVE_FORMAT_MPEG

ID Matroska : A_DTS

- MF_MT_SUBTYPE Media Foundation MSFT : MEDIASUBTYPE_DTS_HD
- Description : système de théâtre numérique
- Identificateurs FourCC ou WAV : WAVE_FORMAT_DTS

ID Matroska : A_OPUS

- MF_MT_SUBTYPE Media Foundation MSFT : MFAudioFormat_Opus
- Description : opus
- Identificateurs FourCC ou WAV : WAVE_FORMAT_OPUS

ID Matroska : A_VORBIS

- MF_MT_SUBTYPE Media Foundation MSFT : MFAudioFormat_Vorbis
- Description : Vorbis
- Identificateurs FourCC ou WAV : 

ID Matroska : A_FLAC

- MF_MT_SUBTYPE Media Foundation MSFT : MFAudioFormat_FLAC
- Description : codec audio gratuit sans perte
- Identificateurs FourCC ou WAV : WAVE_FORMAT_FLAC

ID Matroska : A_AAC/MAIN

- MF_MT_SUBTYPE Media Foundation MSFT : MFAudioFormat_AAC
- Description : codage audio avancé (AAC)
- Identificateurs FourCC ou WAV : WAVE_FORMAT_MPEG_HEAAC

ID Matroska : A_EAC3

- MF_MT_SUBTYPE Media Foundation MSFT : MFAudioFormat_Dolby_DDPlus
- Description : Enhanced AC-3
- Identificateurs FourCC ou WAV : 

ID Matroska : A_TRUEHD

- MF_MT_SUBTYPE Media Foundation MSFT : MEDIASUBTYPE_DOLBY_TRUEHD
- Description : Dolby TrueHD
- Identificateurs FourCC ou WAV : 

ID Matroska : A_MS/ACM

- MSFT Media Foundation MF_MT_SUBTYPE : Cartes à plusieurs types audio WAVE_FORMAT définis dans mmreg. h


### <a name="subtitles-codec-support-for-mkv"></a>Prise en charge du codec sous-titres pour MKV

ID Matroska : S_TEXT/ASCII

- MF_MT_SUBTYPE Media Foundation MSFT : MFSubtitleFormat_SRT
- Description : texte ASCII

ID Matroska : S_TEXT/UTF8

- MF_MT_SUBTYPE Media Foundation MSFT : MFSubtitleFormat_SRT
- Description : texte brut UTF-8

ID Matroska : S_TEXT/SSA

- MF_MT_SUBTYPE Media Foundation MSFT : MFSubtitleFormat_SSA
- Description : format des sous-titres

ID Matroska : S_TEXT/ASS

- MF_MT_SUBTYPE Media Foundation MSFT : MFSubtitleFormat_SSA
- Description : format des sous-titres avancés

ID Matroska : S_VOBSUB

- MF_MT_SUBTYPE Media Foundation MSFT : MFSubtitleFormat_VobSub
- Description : VobSub sous-titres

ID Matroska : S_HDMV/PGS

- MF_MT_SUBTYPE Media Foundation MSFT : MFSubtitleFormat_PGS
- Description : HDMV Presentation Graphics sous-titres (PG)


## <a name="technical-details-regarding-codecs"></a>Détails techniques concernant les codecs

Pour obtenir des détails techniques sur les codecs, consultez les rubriques suivantes.

- [Spécifications du codec Matroska](http://www.matroska.org/technical/specs/codecid/index.html)
- [GUID de sous-type audio](audio-subtype-guids.md)
- [GUID de sous-type de vidéo](video-subtype-guids.md)


## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Formats multimédias pris en charge dans Media Foundation](supported-media-formats-in-media-foundation.md)
</dt> <dt>

[Guide de programmation Media Foundation](media-foundation-programming-guide.md)
</dt> </dl>

 

 



