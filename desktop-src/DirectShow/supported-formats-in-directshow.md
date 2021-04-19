---
description: Formats pris en charge dans DirectShow
ms.assetid: cd8af779-2fb5-4724-a838-5d0c8244f0d3
title: Formats pris en charge dans DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5a6c9a0c85a3ccdfd3db092ba2efce00a191493
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106521088"
---
# <a name="supported-formats-in-directshow"></a>Formats pris en charge dans DirectShow

DirectShow est une architecture ouverte, ce qui signifie qu’elle peut prendre en charge n’importe quel format, à condition qu’il y ait des filtres pour l’analyser et la décoder. Les filtres fournis par Microsoft, tels que les fichiers redistribuables via DirectShow ou les composants du système d’exploitation Windows, fournissent une prise en charge par défaut pour les formats de fichier et de compression suivants.

Types de fichiers :



| Type de fichier                                                                                        | Informations complémentaires                                                                                                                  |
|--------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| ASF (Advanced Systems Format), y compris Windows Media Audio (WMA) et Windows Media Video (WMV) | [Filtre de lecteur ASF WM](about-the-wm-asf-reader-filter.md)<br/> [Filtre d’enregistreur ASF WM](wm-asf-writer-filter.md)<br/> |
| AIFF                                                                                             | [Filtre de l’analyseur WAVE](wave-parser-filter.md)                                                                                      |
| AU                                                                                               | [Filtre de l’analyseur WAVE](wave-parser-filter.md)                                                                                      |
| AVI (Audio-Video Interleaved)                                                                    | [Filtre multiplex MUX](avi-mux-filter.md)<br/> [Filtre de séparateur AVI](avi-splitter-filter.md)<br/>                         |
| MIDI                                                                                             | [Filtre de l’analyseur MIDI](midi-parser-filter.md)<br/> [**Filtre de convertisseur MIDI**](midi-renderer-filter.md)<br/>           |
| SND                                                                                              |                                                                                                                                   |
| WAV                                                                                              | [Filtre de l’analyseur WAVE](wave-parser-filter.md)                                                                                      |



 

Formats de compression :



| Format                                        | Informations complémentaires                                                                                                                                                                                                                                |
|-----------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| AAC                                           | [**Décodeur audio Microsoft MPEG-1/DD/AAC**](microsoft-mpeg-1-dd-audio-decoder.md)                                                                                                                                                              |
| Cinepak                                       |                                                                                                                                                                                                                                                 |
| Vidéo numérique (DV)                            | [Filtre de décodage vidéo DV](dv-video-decoder-filter.md)<br/> [Filtre d’encodeur vidéo DV](dv-video-encoder-filter.md)<br/>                                                                                                             |
| H.264                                         | [**Décodeur vidéo Microsoft MPEG-2**](microsoft-mpeg-2-video-decoder.md)                                                                                                                                                                        |
| ISO MPEG-4 Video version 1,0                  |                                                                                                                                                                                                                                                 |
| Microsoft MPEG-4 version 3                    |                                                                                                                                                                                                                                                 |
| MJPEG                                         | [Filtre de compresseur MJPEG](mjpeg-compressor-filter.md)<br/> [Filtre de décompresseur MJPEG](mjpeg-decompressor-filter.md)<br/>                                                                                                         |
| MPEG Audio Layer-3 (MP3) (décompression uniquement) |                                                                                                                                                                                                                                                 |
| MPEG-1 couche I et audio couche II             | [**Décodeur audio Microsoft MPEG-1/DD/AAC**](microsoft-mpeg-1-dd-audio-decoder.md)<br/> [Filtre de décodage audio MPEG-1](mpeg-1-audio-decoder-filter.md)<br/>                                                                         |
| Vidéo MPEG-1                                  | [Filtre de décodage vidéo MPEG-1](mpeg-1-video-decoder-filter.md)<br/> [**Décodeur vidéo Microsoft MPEG-2**](microsoft-mpeg-2-video-decoder.md)<br/>                                                                                   |
| Audio MPEG-2                                  | [**Encodeur audio Microsoft MPEG-2**](microsoft-mpeg-2-audio-encoder.md)<br/> [**Encodeur Microsoft MPEG-2**](microsoft-mpeg-2-encoder.md)<br/>                                                                                     |
| Vidéo MPEG-2                                  | [**Encodeur Microsoft MPEG-2**](microsoft-mpeg-2-encoder.md)<br/> [**Décodeur vidéo Microsoft MPEG-2**](microsoft-mpeg-2-video-decoder.md)<br/> [**Encodeur vidéo Microsoft MPEG-2**](microsoft-mpeg-2-video-encoder.md)<br/> |



 

Pour plus d’informations sur la disponibilité de codecs tiers spécifiques pour la redistribution avec des applications DirectShow, contactez le fabricant du codec.

 

 




