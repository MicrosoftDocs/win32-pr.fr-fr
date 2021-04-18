---
description: Cette rubrique répertorie les formats multimédias que Microsoft Media Foundation prend en charge en mode natif.
ms.assetid: 69c12a28-4b58-4979-b4d8-ae37efa847fe
title: Formats multimédias pris en charge dans Media Foundation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00e8f698179d37fc6bde8d5d1dab25214727cd38
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/03/2021
ms.locfileid: "106520238"
---
# <a name="supported-media-formats-in-media-foundation"></a>Formats multimédias pris en charge dans Media Foundation

Cette rubrique répertorie les formats multimédias que Microsoft Media Foundation prend en charge en mode natif. Des tiers peuvent prendre en charge des formats supplémentaires en écrivant des plug-ins personnalisés.

## <a name="file-containers"></a>Conteneurs de fichiers



| Format                                           | Extensions de fichier          | Source du média                                 | Récepteur multimédia                                   | Nécessite                                                              |
|--------------------------------------------------|--------------------------|----------------------------------------------|----------------------------------------------|-----------------------------------------------------------------------|
| 3GP                                              | .3g2,. 3gp,. 3GP2,. 3GPP | [Source de fichier MPEG-4](mpeg-4-file-source.md) | Récepteur de fichiers 3GP                                | Windows 7                                                             |
| Format de streaming avancé (ASF)                  | . ASF,. WMA,. wmv         | [Source de média ASF](asf-media-source.md)     | [Récepteur multimédia ASF](asf-media-sinks.md)        | Windows Vista                                                         |
| Flux de transport des données audio (ADTS).              | . AAC,. ADTS              | Source du fichier ADTS                             | Aucun                                         | Windows 7                                                             |
| AVI                                              | .avi                     | Source du fichier AVI                              | Aucun                                         | Windows 7                                                             |
| MP3                                              | .mp3                     | [**Source du fichier MP3**](mp3-file-source.md)   | Récepteur de fichiers MP3                                | Source de fichier : Windows Vista<br/> Récepteur de fichiers : Windows 7<br/> |
| MPEG-4                                           | . M4A,. m4v,. mov,. MP4   | [Source de fichier MPEG-4](mpeg-4-file-source.md) | [**Récepteur de fichiers MPEG-4**](mpeg-4-file-sink.md) | Windows 7                                                             |
| SAMI (Synchronized Accessible Media Interchange) | . sami,. SMI              | [Source du média SAMI](sami-media-source.md)   | Aucun                                         | Windows Vista                                                         |
| WAVE                                             | .wav                     | Source du fichier AVI                              | Aucun                                         | Windows 7                                                             |



 

## <a name="audio-codecs"></a>Codecs audio



| Format                                              | Décodeur                                                                                                                                                          | Encodeur                                                                                                                                                          | Nécessite      |
|-----------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------|
| μ-codage de la Loi                                        | Audio Compression Manager (ACM) μ-codec de la Loi                                                                                                                      | Aucun                                                                                                                                                             | Windows Vista |
| Modulation de code par impulsion différentielle adaptative (ADPCM) | Codec ACM ADPCM                                                                                                                                                  | Aucun                                                                                                                                                             | Windows Vista |
| Codage audio avancé (AAC)                         | [**Décodeur AAC**](aac-decoder.md)                                                                                                                               | [**Encodeur AAC**](aac-encoder.md)                                                                                                                               | Windows 7     |
| MP3                                                 | [**Décodeur MP3 Windows Media**](windows-media-mp3-decoder.md)                                                                                                   | Aucun                                                                                                                                                             | Windows Vista |
| GSM 6.10                                            | Codec ACM GSM 6,10                                                                                                                                               | Aucun                                                                                                                                                             | Windows Vista |
| Audio Windows Media (WMA)                           | [**Décodeur Windows Media Audio**](windowsmediaaudiodecoder.md)<br/> [**Décodeur vocal Windows Media Audio**](windowsmediaaudiovoicedecoder.md)<br/> | [**Encodeur Windows Media Audio**](windowsmediaaudioencoder.md)<br/> [**Encodeur vocal Windows Media Audio**](windowsmediaaudiovoiceencoder.md)<br/> | Windows Vista |



 

> [!Note]  
> Media Foundation fournit des wrappers pour plusieurs codecs ACM, listés dans le tableau précédent. Toutefois, Media Foundation ne prend pas en charge les codecs ACM arbitraires.

 

## <a name="video-codecs"></a>Codecs vidéo



| Format                                                                                                         | Décodeur                                                                                                                                                                  | Encodeur                                                                                                                             | Nécessite      |
|----------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|---------------|
| Vidéo DV                                                                                                       | [**Décodeur vidéo DV**](dv-video-decoder.md)                                                                                                                             | Aucun                                                                                                                                | Windows 7     |
| H.264                                                                                                          | [**Décodeur vidéo H. 264**](h-264-video-decoder.md)                                                                                                                       | [**Encodeur vidéo H. 264**](h-264-video-encoder.md)                                                                                  | Windows 7     |
| H.263<br/> (Profil de base de référence H. 264 qui est compatible avec le mode d’en-tête vidéo abrégé MPEG-4 Pt2)<br/> | [**Décodeur vidéo MPEG-4 part 2**](mpeg4part2videodecoder.md)                                                                                                            | Aucun                                                                                                                                | Windows 8     |
| MJPEG                                                                                                          | Décodeur MJPEG                                                                                                                                                            | Aucun                                                                                                                                | Windows 7     |
| MPEG-4 partie 2                                                                                                  | [**Décodeur vidéo MPEG-4 part 2**](mpeg4part2videodecoder.md)                                                                                                            | Aucun                                                                                                                                | Windows 7     |
| MPEG-4 v1/v2/v3                                                                                                | [**Décodeur Windows Media MPEG-4 v3**](./windowsmediampeg4v3decoder.md)<br/> [**Décodeur Windows Media MPEG4 v1/v2**](windowsmediampeg4decoder.md)<br/>         | Aucun                                                                                                                                | Windows Vista |
| Vidéo Windows Media (WMV)                                                                                      | [**Décodeur Windows Media Video 9**](windowsmediavideo9decoder.md)<br/> [**Décodeur d’écran Windows Media Video 9**](windowsmediavideo9screendecoder.md)<br/> | Encodeur Windows Media Video 9<br/> Encodeur d’écran Windows Media Video 9<br/> Windows Media Video encodeur 7/8<br/> | Windows Vista |



 

> [!Note]  
> La colonne « requires » indique le système d’exploitation minimal requis pour utiliser ces codecs au sein d’une application Media Foundation. Certains de ces codecs ont été introduits avant Windows Vista en tant que [DirectX Media Objects](../directshow/directx-media-objects.md) (DMOs). Si un codec prend en charge la fonctionnalité DMO, il peut être utilisé avec [DirectShow](../directshow/directshow.md) ou le [Kit de développement logiciel (SDK) du format Windows Media](../wmformat/windows-media-format-11-sdk.md).

 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Objets codec](codecobjects.md)
</dt> <dt>

[Guide de programmation Media Foundation](media-foundation-programming-guide.md)
</dt> <dt>

[Sources et récepteurs multimédias](media-sources-and-sinks.md)
</dt> </dl>

 

 
