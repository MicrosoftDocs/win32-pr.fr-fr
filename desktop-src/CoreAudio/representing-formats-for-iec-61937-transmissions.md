---
description: Avec l’augmentation des appareils de stockage multimédia qui requièrent des formats audio compressés, les applications doivent identifier, décrire et utiliser un grand nombre de nouveaux contenus audio encodés pour transmettre du contenu à partir de PC à des appareils tels que HDMI ou DisplayPort récepteur.
ms.assetid: 86f3396c-b32a-4d70-9f21-e38a745f78bf
title: Représentation des formats des transmissions IEC 61937
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0700329aafe7e7bc0e09b532c1ac29b9957ca905
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106515367"
---
# <a name="representing-formats-for-iec-61937-transmissions"></a>Représentation des formats des transmissions IEC 61937

Avec l’augmentation des appareils de stockage multimédia qui requièrent des formats audio compressés, les applications doivent identifier, décrire et utiliser un grand nombre de nouveaux contenus audio encodés pour transmettre du contenu à partir de PC à des appareils tels que HDMI ou DisplayPort récepteur.

Pour représenter un flux audio encodé à transmettre sur une interface compatible IEC 61937, une application doit fournir les éléments suivants :

-   Caractéristiques d’un flux audio encodé à transmettre.

-   Caractéristiques d’un flux audio décodé sur l’appareil cible.

Dans Windows Vista et les systèmes d’exploitation Windows antérieurs, une application peut déduire le niveau de qualité d’un format audio à partir du nombre de canaux, de la taille de l’échantillon et du débit de données d’un flux audio qui utilise le format. Pour un format PCM, ces informations sont disponibles à partir des membres **nChannels**, **nSamplesPerSec** et **nAvgBytesPerSec** de la structure **WAVEFORMATEX** qui spécifie le format. Pour un format non-PCM, ces trois membres ont été commandeered pour stocker des informations sur les données compressées dans le flux audio. Par conséquent, la structure **WAVEFORMATEX** ne dispose pas d’informations sur le nombre effectif de canaux, la taille de l’échantillon et le débit de données du flux audio non-PCM après la décompression et la lecture du flux. En fonction des informations contenues dans cette structure, un utilisateur ou une application peut avoir des difficultés à déduire le niveau de qualité du flux non-PCM.

**WAVEFORMATEX** a été étendu à la structure **WAVEFORMATEXTENSIBLE** pour fournir les caractéristiques de flux supplémentaires. Toutefois, cette structure ne convient pas non plus à la description du flux des transmissions IEC 61937, car elle a été conçue pour représenter un ensemble unique de caractéristiques et utilisée pour les données PCM multicanaux non compressées.

Dans Windows 7, le système d’exploitation résout ce problème en fournissant la prise en charge d’une nouvelle structure, **WAVEFORMATEXTENSIBLE \_ IEC61937** qui étend **WAVEFORMATEXTENSIBLE** structure pour stocker deux jeux de caractéristiques de flux audio : le format audio encodé avant la transmission et les caractéristiques du flux audio après qu’il a été décodé. La nouvelle structure spécifie explicitement le nombre effectif de canaux, la taille de l’échantillon et le débit de données d’un format non-PCM. Avec ces informations, une application peut déduire le niveau de qualité du flux non-PCM après sa décompression et sa lecture.

La structure **WAVEFORMATEXTENSIBLE \_ IEC61937** est déclarée dans l’en-tête KsMedia. h inclus dans le kit de développement logiciel (SDK) Windows 7. Le membre **FormatExt** est la structure **WAVEFORMATEXTENSIBLE** qui stocke les caractéristiques du flux à transmettre. Le membre de **format** de la structure **WAVEFORMATEXTENSIBLE** est la structure **WAVEFORMATEX** . Le contenu de ce **WAVEFORMATEX** et **WAVEFORMATEXTENSIBLE** indique à une application si la structure peut être interprétée comme une structure **\_ IEC61937 WAVEFORMATEXTENSIBLE** . Pour une structure **WAVEFORMATEXTENSIBLE \_ IEC61937** :

-   Le membre **wFormatTag** de **WAVEFORMATEX** doit contenir le \_ format Wave \_ extensible ( `FormatExt.Format.wFormatTag = WAVE_FORMAT_EXTENSIBLE` ).

-   Le membre de sous- **format** de la structure **WAVEFORMATEXTENSIBLE** spécifie le GUID du format encodé à transmettre. Par exemple, `FormatExt.SubFormat = KSDATAFORMAT_SUBTYPE_IEC61937_DOLBY_DIGITAL` indique le format Dolby Digital plus. Pour obtenir les GUID pris en charge, consultez GUID de sous-format.

-   La taille indiquée par le membre **cbSize** du WAVEFORMATEX est de 34 octets. (`FormatExt.Format.cbSize = 34`). La taille totale de **WAVEFORMATEXTENSIBLE \_ IEC61937** est de 52 octets.

Les membres **dwEncodedSamplesPerSec**, **dwEncodedChannelCount** et **dwAverageBytesPerSec** de **WAVEFORMATEXTENSIBLE \_ IEC61937** décrivent la fréquence d’échantillonnage, le nombre de canaux et le débit binaire en octets du flux du flux audio après qu’il a été décodé.

## <a name="subformat-guids"></a>GUID de sous-format

Dans Windows 7, l’en-tête KsMedia. h contient les définitions des GUID de sous-format pour les formats audio compressés définis par CEA-861-D. Les GUID sont spécifiés dans le membre de sous-format du **WAVEFORMATEXTENSIBLE**, spécifié dans le membre **FormatExt** de la structure **\_ IEC61937 WAVEFORMATEXTENSIBLE** ( `WAVEFORMATEXTENSIBLE_IEC61937.FormatExt.Subformat` ).

Les GUID pour les formats audio compressés disponibles en tant que formats audio conformes aux normes IEC 61937 standard sont répertoriés dans le tableau suivant. Ces formats sont similaires aux représentations existantes du codage actif 3 (AC-3) et des formats de sons Digital Theater (DTS) dans Windows.



| Type CEA 861 | GUID de sous-format                                                                                                          | Description                                  |
|--------------|-------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| 0x00         |                                                                                                                         | Reportez-vous au flux.                         |
| 0x01         | 00000000-0000-0010-8000-00aa00389b71<br/> KSDATAFORMAT \_ sous-type \_ WAVEFORMATEX<br/>                          | PCM 60958 IEC                                |
| 0x02         | 00000092-0000-0010-8000-00aa00389b71<br/> KSDATAFORMAT \_ sous-type \_ IEC61937 \_ Dolby \_ Digital<br/>              | AC-3                                         |
| 0x03         | 00000003-0cea-0010-8000-00aa00389b71<br/> KSDATAFORMAT \_ sous-type \_ IEC61937 \_ MPEG1<br/>                       | MPEG-1 (couche 1 & 2)                         |
| 0x04         | 00000004-0cea-0010-8000-00aa00389b71<br/> KSDATAFORMAT \_ sous-type \_ IEC61937 \_ mpeg3<br/>                       | MPEG-3 (couche 3)                             |
| 0x05         | 00000005-0cea-0010-8000-00aa00389b71<br/> KSDATAFORMAT \_ sous-type \_ IEC61937 \_ MPEG2 <br/>                      | MPEG-2 (Multichannel)                         |
| 0x06         | 00000006-0cea-0010-8000-00aa00389b71<br/> KSDATAFORMAT \_ sous-type \_ IEC61937 \_ AAC<br/>                         | Codage audio avancé (MPEG-2/4 AAC dans ADTS) |
| 0x07         | 00000008-0000-0010-8000-00aa00389b71<br/> KSDATAFORMAT \_ sous-type \_ IEC61937 \_ Dts<br/>                         | DTS                                          |
| 0x0A         | 0000000a-0cea-0010-8000-00aa00389b71<br/> KSDATAFORMAT \_ sous-type \_ IEC61937 \_ Dolby \_ Digital \_ plus<br/>        | Dolby Digital plus                           |
| 0x0A         | 0000010a-0cea-0010-8000-00aa00389b71<br/> KSDATAFORMAT \_ sous-type \_ IEC61937 \_ Dolby \_ Digital \_ plus \_ Atmos<br/> | Dolby Atmos encodé avec Dolby Digital plus  |
| 0x0F         |                                                                                                                         | Réservé non utilisé                              |



 

Les GUID pour les formats audio compressés transmis dans des exemples de paquets audio à vitesse de transmission élevée sont répertoriés dans le tableau suivant.



| Type CEA 861 | GUID de sous-format                                                                                           | Description                                                                                                                     |
|--------------|----------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| 0x0B         | 0000000b-0cea-0010-8000-00aa00389b71<br/> KSDATAFORMAT \_ sous-type \_ IEC61937 \_ DTS \_ HD<br/>      | DTS-HD (24 bits, 96Khz)                                                                                                          |
| 0x0c         | 0000000c-0cea-0010-8000-00aa00389b71<br/> KSDATAFORMAT \_ sous-type \_ IEC61937 \_ Dolby \_ MLP<br/>   | Dolby MAT 1,0 :<br/> Dolby TrueHD (MLP – méridien Lossless compression) – 24 bits 192KHz/jusqu’à 18 Mbits/s, 8 canaux) <br/> |
| 0x0c         | 0000010c-0cea-0010-8000-00aa00389b71<br/> KSDATAFORMAT \_ sous-type \_ IEC61937 \_ Dolby \_ MAT20<br/> | Dolby MAT 2,0 : <br/> Dolby TrueHD – 24 bits 192KHz/jusqu’à 18 Mbits/s, 8 canaux ou LPCM jusqu’à 24 Mbits/s. <br/>           |
| 0x0c         | 0000030c-0cea-0010-8000-00aa00389b71<br/> KSDATAFORMAT \_ sous-type \_ IEC61937 \_ Dolby \_ MAT21<br/> | Dolby MAT 2,1 : <br/> Dolby TrueHD – 24 bits 192KHz/jusqu’à 18 Mbits/s, 8 canaux ou LPCM jusqu’à 24 Mbits/s. <br/>           |
| 0x0E         | 00000164-0000-0010-8000-00aa00389b71<br/> KSDATAFORMAT \_ sous-type \_ IEC61937 \_ WMA \_ Pro<br/>     | Windows Media Audio (WMA) Pro                                                                                                   |



 

Le pilote de classe audio HD fourni par Microsoft prend en charge les formats PCM, AC3, DTS, AAC, Dolby Digital plus, WMA Pro, MAT (MLP). Les GUID pour les formats audio compressés qui ne sont pas pris en charge par le pilote de classe HD Audio et peuvent être implémentés par des solutions tierces sont répertoriés dans le tableau suivant.



| Type CEA 861 | GUID de sous-format                                                                                              | Description                                                                    |
|--------------|-------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| 0x08         | 00000008-0cea-0010-8000-00aa00389b71<br/> KSDATAFORMAT \_ sous-type \_ IEC61937 \_ ATRAC<br/>           | Transformation adaptative du codage acoustique (ATRAC)                                     |
| 0x09         | 00000009-0cea-0010-8000-00aa00389b71<br/> KSDATAFORMAT \_ sous-type \_ IEC61937 \_ un \_ bit \_ audio<br/> | Audio One-Bit                                                                  |
| 0x0D         | 0000000d-0cea-0010-8000-00aa00389b71<br/> KSDATAFORMAT \_ sous-type \_ IEC61937 \_ DST<br/>             | Transport direct stream (DST) : DSD compressé sans perte (direct stream Digital). |



 

## <a name="dolby-digital-plus-format"></a>Format Dolby Digital plus

Lorsque le contenu Dolby Digital plus est transmis via IEC 60958, le taux d’échantillonnage des liens doit être de quatre fois la fréquence d’échantillonnage du contenu. Dolby Digital plus prend en charge des taux d’échantillonnage de contenu de 32 KHz, 44,1 KHz et 48 KHz. Les interfaces comme HDMI ne prennent pas en charge 128 KHz (32 KHz x 4). par conséquent, seuls les taux d’échantillonnage de contenu 44,1 et 48 KHz peuvent être pris en charge.

Les valeurs définies par une application dans la \_ structure IEC61937 WAVEFORMATEXTENSIBLE pour représenter le format Dolby Digital plus à un taux d’échantillonnage de contenu de 48 kHz sont indiquées dans l’exemple suivant.


```C++
WAVEFORMATEXTENSIBLE_IEC61937 wfext;
Wfext.FormatExt.Format.wFormatTag = WAVE_FORMAT_EXTENSIBLE;
wfext.FormatExt.Format.nChannels = 2;              // One IEC 60958 Line.
wfext.FormatExt.Format.nSamplesPerSec = 192000;    // Link runs at 192 KHz.
wfext.FormatExt.Format.nAvgBytesPerSec = 768000;   // 192 KHz * 4.
wfext.FormatExt.Format.nBlockAlign = 4;            // 16 bits * 2 channels.
wfext.FormatExt.Format.wBitsPerSample = 16;        // Always at 16 bits over IEC 60958.
wfext.FormatExt.Format.cbSize = 34;                // Indicates that Format is part of a 
                                                   // WAVEFORMATEXTENSIBLE_IEC61937 structure.
wfext.FormatExt.Samples.wValidBitsPerSample = 16;
wfext.FormatExt.dwChannelMask = KSAUDIO_SPEAKER_5POINT1;    // Dolby 5.1 Surround.
wfext.FormatExt.SubFormat = KSDATAFORMAT_SUBTYPE_IEC61937_DOLBY_DIGITAL_PLUS;
wfext.dwEncodedSamplesPerSec = 48000;                       // Sample rate of encoded content.
wfext.dwEncodedChannelCount = 6;                            // Encoded data contains 6 channels.
wfext.dwAverageBytesPerSec = 0;                             // Ignored for this format.
```



## <a name="dolby-truehd-mat"></a>Dolby TrueHD (MAT)

Le contenu Dolby TrueHD est transmis sur les canaux 60958 à 176,4 kHz/8 (ce qui nécessite une fréquence d’images IEC 60958 de 705,6 kHz) pour les taux d’échantillonnage du contenu des canaux 44,1, 88,2 et 176,4 kHz et 192 kHz/8 (nécessitant une fréquence d’images IEC 60958 de 768 kHz) pour les taux d’échantillonnage de contenu de 48, 96 et 192 kHz.

Les valeurs définies par une application dans la \_ structure IEC61937 WAVEFORMATEXTENSIBLE pour représenter Dolby TrueHD à un taux d’échantillonnage de contenu de 96 kHz sont indiquées dans les exemples suivants.

Dolby MAT 1,0


```C++
WAVEFORMATEXTENSIBLE_IEC61937 wfext;
Wfext.FormatExt.Format.wFormatTag = WAVE_FORMAT_EXTENSIBLE;
wfext.FormatExt.Format.nChannels = 8;                // Four IEC 60958 Lines.
wfext.FormatExt.Format.nSamplesPerSec = 192000;      // Link runs at 192 KHz.
wfext.FormatExt.Format.nAvgBytesPerSec = 3072000;    // 192 KHz * 16.
wfext.FormatExt.Format.nBlockAlign = 16;             // 16-bits * 8 channels.
wfext.FormatExt.Format.wBitsPerSample = 16;          // Always at 16 bits over IEC 60958.
wfext.FormatExt.Format.cbSize = 34;                  // Indicates that Format is part of a 
                                                     // WAVEFORMATEXTENSIBLE_IEC61937 structure.
wfext.FormatExt.Samples.wValidBitsPerSample = 16;
wfext.FormatExt.dwChannelMask = KSAUDIO_SPEAKER_7POINT1;    // Dolby 7.1 Surround.
wfext.FormatExt.SubFormat = KSDATAFORMAT_SUBTYPE_IEC61937_DOLBY_MLP; // This structure indicates MLP (MAT 1.0) support.
wfext.dwEncodedSamplesPerSec = 96000;                       // Sample rate of encoded content.
wfext.dwEncodedChannelCount = 8;                            // Encoded data contains 8 channels.
wfext.dwAverageBytesPerSec = 0;                             // Ignored for this format.
```



Dolby MAT 2,0


```C++
WAVEFORMATEXTENSIBLE_IEC61937 wfext;
Wfext.FormatExt.Format.wFormatTag = WAVE_FORMAT_EXTENSIBLE;
wfext.FormatExt.Format.nChannels = 8;                // Four IEC 60958 Lines.
wfext.FormatExt.Format.nSamplesPerSec = 192000;      // Link runs at 192 KHz.
wfext.FormatExt.Format.nAvgBytesPerSec = 3072000;    // 192 KHz * 16.
wfext.FormatExt.Format.nBlockAlign = 16;             // 16-bits * 8 channels.
wfext.FormatExt.Format.wBitsPerSample = 16;          // Always at 16 bits over IEC 60958.
wfext.FormatExt.Format.cbSize = 34;                  // Indicates that Format is part of a 
                                                     // WAVEFORMATEXTENSIBLE_IEC61937 structure.
wfext.FormatExt.Samples.wValidBitsPerSample = 16;
wfext.FormatExt.dwChannelMask = KSAUDIO_SPEAKER_7POINT1;    // Dolby 7.1 Surround.
wfext.FormatExt.SubFormat = KSDATAFORMAT_SUBTYPE_IEC61937_DOLBY_MAT20; // This structure indicates MAT 2.0 support.
wfext.dwEncodedSamplesPerSec = 96000;                       // Sample rate of encoded content.
wfext.dwEncodedChannelCount = 8;                            // Encoded data contains 8 channels.
wfext.dwAverageBytesPerSec = 0;                             // Ignored for this format.
```



Dolby MAT 2,1


```C++
WAVEFORMATEXTENSIBLE_IEC61937 wfext;
Wfext.FormatExt.Format.wFormatTag = WAVE_FORMAT_EXTENSIBLE;
wfext.FormatExt.Format.nChannels = 8;                // Four IEC 60958 Lines.
wfext.FormatExt.Format.nSamplesPerSec = 192000;      // Link runs at 192 KHz.
wfext.FormatExt.Format.nAvgBytesPerSec = 3072000;    // 192 KHz * 16.
wfext.FormatExt.Format.nBlockAlign = 16;             // 16-bits * 8 channels.
wfext.FormatExt.Format.wBitsPerSample = 16;          // Always at 16 bits over IEC 60958.
wfext.FormatExt.Format.cbSize = 34;                  // Indicates that Format is part of a 
                                                     // WAVEFORMATEXTENSIBLE_IEC61937 structure.
wfext.FormatExt.Samples.wValidBitsPerSample = 16;
wfext.FormatExt.dwChannelMask = KSAUDIO_SPEAKER_7POINT1;    // Dolby 7.1 Surround.
wfext.FormatExt.SubFormat = KSDATAFORMAT_SUBTYPE_IEC61937_DOLBY_MAT21; // This structure indicates MAT 2.1 support.
wfext.dwEncodedSamplesPerSec = 96000;                       // Sample rate of encoded content.
wfext.dwEncodedChannelCount = 8;                            // Encoded data contains 8 channels.
wfext.dwAverageBytesPerSec = 0;                             // Ignored for this format.
```



> [!Note]  
> La prise en charge d’une version de Dolby MAT n’implique pas la prise en charge de Dolby MAT avec un numéro de version inférieur. Étant donné que Dolby MAT 2,1 offre une compatibilité descendante avec les versions précédentes de Dolby MAT, un pilote de classe qui indique la prise en charge de Dolby MAT 2,1 indique en général également la prise en charge de Dolby MAT 2,0 et Dolby MAT 1,0, à l’aide d’une \_ structure IEC61937 WAVEFORMATEXTENSIBLE distincte pour chaque version.

 

## <a name="wma-pro"></a>WMA Pro

Le contenu audio WMA Pro peut être encodé dans l’un des quatre profils listés dans le tableau suivant.



| Profil | Valeur de propriété                                                                                                                                                                                                                                                      | Description                                                                                                                         |
|---------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| M0      | Débit maximal-192000 BPS <br/> Taux d’échantillonnage maximal – 48 KHz <br/> Nombre maximal de canaux – 2 <br/> Taille maximale de la mémoire tampon – 600 \* 1024 bits <br/> Nombre maximal d’échantillons par image-2048 <br/> Nombre maximal de bits par trame-655536<br/>   | Recommandé pour la musique et la diffusion en continu à l’air.<br/> La vitesse de transmission maximale dans une trame audio est de 1536000 bps.<br/>          |
| M1      | Débit maximal-385000 BPS <br/> Taux d’échantillonnage maximal – 48 KHz <br/> Nombre maximal de canaux – 6 <br/> Taille maximale de la mémoire tampon – 600 \* 1024 bits <br/> Nombre maximal d’échantillons par image-4096 <br/> Nombre maximal de bits par trame-131072<br/>   | Recommandé pour les films de définition standard Surround Sound.<br/> La vitesse de transmission maximale dans une trame audio est de 1536000 bps.<br/> |
| M2      | Débit maximal-769000 BPS <br/> Taux d’échantillonnage maximal – 96 KHz <br/> Nombre maximal de canaux – 6 <br/> Taille maximale de la mémoire tampon – 1200 \* 1024 bits <br/> Nombre maximal d’échantillons par image-4096 <br/> Nombre maximal de bits par trame-131072<br/>  | Recommandé pour les films haute définition de son surround.<br/> Le débit maximal dans une trame audio est de 3072000 bps.<br/>         |
| M3      | Débit maximal-3 millions BPS <br/> Taux d’échantillonnage maximal – 96 KHz <br/> Nombre maximal de canaux – 8 <br/> Taille maximale de la mémoire tampon – 2400 \* 1024 bits <br/> Nombre maximal d’échantillons par image-4096 <br/> Nombre maximal de bits par trame-131072<br/> | Recommandé pour Digital Theater.<br/> Le débit maximal dans une trame audio est de 3072000 bps.<br/>                               |



 

Les profils M0 et M1 s’intègrent à un flux IEC 60958 48 KHz/16 bits/stéréo (1536000 BPS). Les profils m2 et M3 s’intègrent à un flux IEC 60958 96 KHz/16 bits/stéréo (3072000 BPS).

Les valeurs définies par une application dans la \_ structure IEC61937 WAVEFORMATEXTENSIBLE pour représenter WMA Pro en tant que profil m2 sont indiquées dans l’exemple suivant.


```C++
WAVEFORMATEXTENSIBLE_IEC61937 wfext;
Wfext.FormatExt.Format.wFormatTag = WAVE_FORMAT_EXTENSIBLE;
wfext.FormatExt.Format.nChannels = 2;             // One IEC 60958 Line.
wfext.FormatExt.Format.nSamplesPerSec = 96000;    // Link runs at 96 KHz.
wfext.FormatExt.Format.nAvgBytesPerSec = 384000;  // 96 KHz * 4.
wfext.FormatExt.Format.nBlockAlign = 4;           // 16 bits * 8 channels.
wfext.FormatExt.Format.wBitsPerSample = 16;       // Always at 16 bits over link.
wfext.FormatExt.Format.cbSize = 34;               // Indicates that Format is part of a 
                                                  // WAVEFORMATEXTENSIBLE_IEC61937 structure.
wfext.FormatExt.Samples.wValidBitsPerSample = 16;
wfext.FormatExt.dwChannelMask = KSAUDIO_SPEAKER_5POINT1;    // 5.1 Surround.
wfext.FormatExt.SubFormat = KSDATAFORMAT_SUBTYPE_IEC61937_WMA_PRO;
wfext.dwEncodedSamplesPerSec = 96000;                       // Sample rate of encoded content.
wfext.dwEncodedChannelCount = 6;                            // Encoded data contains 6 channels.
wfext.dwAverageBytesPerSec = 0;                             // Ignored for this format.
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Formats d’appareil](device-formats.md)
</dt> </dl>

 

 




