---
description: Cette rubrique répertorie les formats multimédias que Microsoft Media Foundation prend en charge en mode natif.
ms.assetid: 69c12a28-4b58-4979-b4d8-ae37efa847fe
title: Formats multimédias pris en charge dans Media Foundation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00e8f698179d37fc6bde8d5d1dab25214727cd38
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127414032"
---
# <a name="supported-media-formats-in-media-foundation"></a>Formats multimédias pris en charge dans Media Foundation

Cette rubrique répertorie les formats multimédias que Microsoft Media Foundation prend en charge en mode natif. Des tiers peuvent prendre en charge des formats supplémentaires en écrivant des plug-ins personnalisés.

## <a name="file-containers"></a>Conteneurs de fichiers



| Format                                           | Extensions de fichier          | Source du média                                 | Récepteur multimédia                                   | Nécessite                                                              |
|--------------------------------------------------|--------------------------|----------------------------------------------|----------------------------------------------|-----------------------------------------------------------------------|
| 3GP                                              | .3g2,. 3gp,. 3GP2,. 3GPP | [Source de fichier MPEG-4](mpeg-4-file-source.md) | Récepteur de fichiers 3GP                                | Windows 7                                                             |
| Format de streaming avancé (ASF)                  | . ASF,. WMA,. wmv         | [Source de média ASF](asf-media-source.md)     | [Récepteur multimédia ASF](asf-media-sinks.md)        | Windows Vista                                                         |
| Flux de transport des données audio (ADTS).              | . AAC,. ADTS              | Source du fichier ADTS                             | None                                         | Windows 7                                                             |
| AVI                                              | .avi                     | Source du fichier AVI                              | None                                         | Windows 7                                                             |
| MP3                                              | .mp3                     | [**Source du fichier MP3**](mp3-file-source.md)   | Récepteur de fichiers MP3                                | source du fichier : Windows Vista<br/> récepteur de fichiers : Windows 7<br/> |
| MPEG-4                                           | . M4A,. m4v,. mov, .mp4   | [Source de fichier MPEG-4](mpeg-4-file-source.md) | [**Récepteur de fichiers MPEG-4**](mpeg-4-file-sink.md) | Windows 7                                                             |
| SAMI (Synchronized Accessible Media Interchange) | . sami,. SMI              | [Source du média SAMI](sami-media-source.md)   | None                                         | Windows Vista                                                         |
| WAVE                                             | .wav                     | Source du fichier AVI                              | None                                         | Windows 7                                                             |



 

## <a name="audio-codecs"></a>Codecs audio



| Format                                              | Décodeur                                                                                                                                                          | Encodeur                                                                                                                                                          | Nécessite      |
|-----------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------|
| μ-codage de la Loi                                        | Audio Compression Manager (ACM) μ-codec de la Loi                                                                                                                      | None                                                                                                                                                             | Windows Vista |
| Modulation de code par impulsion différentielle adaptative (ADPCM) | Codec ACM ADPCM                                                                                                                                                  | None                                                                                                                                                             | Windows Vista |
| Codage audio avancé (AAC)                         | [**Décodeur AAC**](aac-decoder.md)                                                                                                                               | [**Encodeur AAC**](aac-encoder.md)                                                                                                                               | Windows 7     |
| MP3                                                 | [**Windows Décodeur MP3 multimédia**](windows-media-mp3-decoder.md)                                                                                                   | None                                                                                                                                                             | Windows Vista |
| GSM 6.10                                            | Codec ACM GSM 6,10                                                                                                                                               | None                                                                                                                                                             | Windows Vista |
| Audio Windows Media (WMA)                           | [**Windows Décodeur audio multimédia**](windowsmediaaudiodecoder.md)<br/> [**Windows Décodeur de voix Media audio**](windowsmediaaudiovoicedecoder.md)<br/> | [**Windows Encodeur audio multimédia**](windowsmediaaudioencoder.md)<br/> [**Windows Codeur Media Audio Voice**](windowsmediaaudiovoiceencoder.md)<br/> | Windows Vista |



 

> [!Note]  
> Media Foundation fournit des wrappers pour plusieurs codecs ACM, listés dans le tableau précédent. Toutefois, Media Foundation ne prend pas en charge les codecs ACM arbitraires.

 

## <a name="video-codecs"></a>Codecs vidéo



| Format                                                                                                         | Décodeur                                                                                                                                                                  | Encodeur                                                                                                                             | Nécessite      |
|----------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|---------------|
| Vidéo DV                                                                                                       | [**Décodeur vidéo DV**](dv-video-decoder.md)                                                                                                                             | None                                                                                                                                | Windows 7     |
| H.264                                                                                                          | [**Décodeur vidéo H. 264**](h-264-video-decoder.md)                                                                                                                       | [**Encodeur vidéo H. 264**](h-264-video-encoder.md)                                                                                  | Windows 7     |
| H.263<br/> (Profil de base de référence H. 264 qui est compatible avec le mode d’en-tête vidéo abrégé MPEG-4 Pt2)<br/> | [**Décodeur vidéo MPEG-4 part 2**](mpeg4part2videodecoder.md)                                                                                                            | None                                                                                                                                | Windows 8     |
| MJPEG                                                                                                          | Décodeur MJPEG                                                                                                                                                            | None                                                                                                                                | Windows 7     |
| MPEG-4 partie 2                                                                                                  | [**Décodeur vidéo MPEG-4 part 2**](mpeg4part2videodecoder.md)                                                                                                            | None                                                                                                                                | Windows 7     |
| MPEG-4 v1/v2/v3                                                                                                | [**Windows Décodeur Media MPEG-4 v3**](./windowsmediampeg4v3decoder.md)<br/> [**Windows Décodeur de média MPEG4 v1/v2**](windowsmediampeg4decoder.md)<br/>         | None                                                                                                                                | Windows Vista |
| Vidéo Windows Media (WMV)                                                                                      | [**Windows Décodeur Media Video 9**](windowsmediavideo9decoder.md)<br/> [**Windows Décodeur d’écran Media Video 9**](windowsmediavideo9screendecoder.md)<br/> | Windows Encodeur Media Video 9<br/> Windows Encodeur d’écran Media Video 9<br/> Windows Encodeur Video Media Video 7/8<br/> | Windows Vista |



 

> [!Note]  
> La colonne « requires » indique le système d’exploitation minimal requis pour utiliser ces codecs au sein d’une application Media Foundation. certains de ces codecs ont été introduits avant Windows Vista en tant que DMOs ( [DirectX Media objects](../directshow/directx-media-objects.md) ). si un codec prend en charge les fonctionnalités de DMO, il peut être utilisé avec [DirectShow](../directshow/directshow.md) ou le [kit de développement logiciel (SDK) Windows Media Format](../wmformat/windows-media-format-11-sdk.md).

 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Objets codec](codecobjects.md)
</dt> <dt>

[Guide de programmation Media Foundation](media-foundation-programming-guide.md)
</dt> <dt>

[Sources et récepteurs multimédias](media-sources-and-sinks.md)
</dt> </dl>

 

 
