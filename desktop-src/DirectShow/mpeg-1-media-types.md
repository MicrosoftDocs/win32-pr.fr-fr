---
description: Cette section répertorie les types de médias utilisés pour les données MPEG-1.
ms.assetid: 4ea1cb84-0558-4c4a-9483-1b0f2a8f76f8
title: Types de média MPEG-1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35d1ff7c121c52db39d574f9bbae3650b04312e9
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/03/2021
ms.locfileid: "106535739"
---
# <a name="mpeg-1-media-types"></a>Types de média MPEG-1

Cette section répertorie les types de médias utilisés pour les données MPEG-1.

## <a name="mpeg-1-system-stream"></a>Flux système MPEG-1



|                       |                                                 |
|-----------------------|-------------------------------------------------|
| Type principal            | Flux de MEDIATYPE \_                               |
| Subtype               | MEDIASUBTYPE \_ MPEG1System                       |
| Type de format           | FORMAT \_ MPEGStreams                             |
| Structure de format      | [**AM \_ MPEGSYSTEMTYPE**](/previous-versions/windows/desktop/api/mpegtype/ns-mpegtype-am_mpegsystemtype) |
| Exemple de contenu multimédia | Flux d’octets ; aucun alignement                       |



 

## <a name="mpeg-1-system-stream-from-video-cd"></a>Flux système MPEG-1 à partir d’un CD vidéo



|                       |                            |
|-----------------------|----------------------------|
| Type principal            | Flux de MEDIATYPE \_          |
| Subtype               | MEDIASUBTYPE \_ MPEG1VideoCD |
| Type de format           | GUID \_ null                 |
| Structure de format      | Aucun                       |
| Exemple de contenu multimédia | Flux d’octets ; aucun alignement. |



 

## <a name="mpeg-1-audio-packet"></a>Paquet audio MPEG-1



|                       |                                                |
|-----------------------|------------------------------------------------|
| Type principal            | Audio de MEDIATYPE \_                               |
| Subtype               | MEDIASUBTYPE \_ MPEG1Packet                      |
| Type de format           | FORMAT \_ WaveFormatEx                           |
| Structure de format      | [**MPEG1WAVEFORMAT**](/windows/desktop/api/mmreg/ns-mmreg-mpeg1waveformat)     |
| Exemple de contenu multimédia | Paquet MPEG-1 unique, y compris l’en-tête de paquet. |



 

## <a name="mpeg-1-audio-payload"></a>Charge utile MPEG-1



|                       |                                            |
|-----------------------|--------------------------------------------|
| Type principal            | Audio de MEDIATYPE \_                           |
| Subtype               | MEDIASUBTYPE \_ MPEG1Payload                 |
| Type de format           | FORMAT \_ WaveFormatEx                       |
| Structure de format      | [**MPEG1WAVEFORMAT**](/windows/desktop/api/mmreg/ns-mmreg-mpeg1waveformat) |
| Exemple de contenu multimédia | Données audio MPEG-1 alignées sur les octets.            |



 

## <a name="mpeg-1-video-packet"></a>Paquet vidéo MPEG-1



|                       |                                                |
|-----------------------|------------------------------------------------|
| Type principal            | Vidéo de MEDIATYPE \_                               |
| Subtype               | MEDIASUBTYPE \_ MPEG1Packet                      |
| Type de format           | FORMAT \_ mpegvideo                              |
| Structure de format      | [**MPEG1VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-mpeg1videoinfo)       |
| Exemple de contenu multimédia | Paquet MPEG-1 unique, y compris l’en-tête de paquet. |



 

## <a name="mpeg-1-video-payload"></a>Charge utile vidéo MPEG-1



|                       |                                          |
|-----------------------|------------------------------------------|
| Type principal            | Vidéo de MEDIATYPE \_                         |
| Subtype               | MEDIASUBTYPE \_ MPEG1Payload               |
| Type de format           | FORMAT \_ mpegvideo                        |
| Structure de format      | [**MPEG1VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-mpeg1videoinfo) |
| Exemple de contenu multimédia | Données vidéo MPEG-1 alignées sur les octets.          |



 

## <a name="mpeg-1-native-video-stream"></a>Flux vidéo natif MPEG-1



|                       |                                                |
|-----------------------|------------------------------------------------|
| Type principal            | Flux de MEDIATYPE \_                              |
| Subtype               | MEDIASUBTYPE \_ MPEG1Video                      |
| Type de format           | GUID \_ null                                     |
| Structure de format      | Aucun                                           |
| Exemple de contenu multimédia | Tableau d’octets de flux vidéo (aucune couche système). |



 

## <a name="mpeg-1-native-audio-stream"></a>Flux audio natif MPEG-1



|                       |                                                |
|-----------------------|------------------------------------------------|
| Type principal            | Flux de MEDIATYPE \_                              |
| Subtype               | MEDIASUBTYPE \_ MPEG1Audio                      |
| Type de format           | GUID \_ null                                     |
| Structure de format      | Aucun                                           |
| Exemple de contenu multimédia | Tableau d’octets de flux audio (aucune couche système). |



 

## <a name="remarks"></a>Notes

Les filtres MPEG-1 DirectShow prennent en charge ces types comme suit.



| Filtrer               | Sens | Types de média pris en charge                                                                                             |
|----------------------|-----------|-------------------------------------------------------------------------------------------------------------------|
| Séparateur MPEG-1      | Entrée     | MPEG-1 système streamMPEG-1 flux système à partir du CD vidéo<br/>                                                 |
| Séparateur MPEG-1      | Output    | Charge utile MPEG-1 audio packetMPEG-1 audio<br/> Paquet vidéo MPEG-1<br/> Charge utile vidéo MPEG-1<br/> |
| Codec audio logiciel | Entrée     | Charge utile MPEG-1 audio packetMPEG-1 audio<br/>                                                                |
| Codec vidéo logiciel | Entrée     | Charge utile vidéo MPEG-1 Video packetMPEG-1<br/>                                                                |
| Codec audio logiciel | Output    | Audio PCM                                                                                                         |
| Codec vidéo logiciel | Output    | Vidéo non compressée (Y41P, YUY2, UYVY, RGB-24, RGB-32, RGB-565, RGB-555, RVB-8)                                    |



 

Les types de média de paquets vidéo MPEG-1 et de charge utile contiennent un en-tête de séquence complet afin que les données puissent être lues à partir du milieu d’un fichier sans avoir besoin d’un en-tête de séquence pour initialiser la lecture vidéo.

L’en-tête de séquence vidéo est ajouté au type de données vidéo pour la vidéo MPEG, de sorte que la lecture peut commencer à partir du milieu d’un flux. La longueur de ce champ est de 140 octets. Il comprend le code de début d’en-tête de séquence (0x000001B3) au début, ainsi que toutes les matrices de quantification trouvées dans le premier en-tête de séquence rencontré.

 

 




