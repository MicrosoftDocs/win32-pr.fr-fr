---
description: Les tableaux suivants répertorient les GUID de sous-type de média pour l’audio. Le cas échéant, chaque table répertorie la balise de format équivalente, déclarée dans mmreg. h.
ms.assetid: 55012be5-2d61-4d38-aab7-0c42f161f555
title: Sous-types audio
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 82b9ccbe83a20f23976e506124c674119eee3a96
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127112153"
---
# <a name="audio-subtypes"></a>Sous-types audio

Les tableaux suivants répertorient les GUID de sous-type de média pour l’audio. Le cas échéant, chaque table répertorie la balise de format équivalente, déclarée dans mmreg. h.

## <a name="uncompressed-audio-types"></a>Types audio non compressés



| GUID                          | Description                | En-tête  | Balise de format équivalente                  |
|-------------------------------|----------------------------|---------|----------------------------------------|
| **MEDIASUBTYPE \_ IEEE \_ float** | Audio à virgule flottante IEEE. | UUID. h | **Vague \_ FORMAT \_ IEEE \_ float** (0x0003) |
| **\_PCM MEDIASUBTYPE**         | Audio PCM.                 | UUID. h | **Vague \_ FORMAT \_ PCM** (0x0001)         |



 

## <a name="mpeg-4-and-aac-audio-types"></a>Types audio MPEG-4 et AAC



| GUID                              | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               | En-tête       | Balise de format équivalente                      |
|-----------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------|--------------------------------------------|
| **MEDIASUBTYPE \_ MPEG \_ ADTS \_ AAC** | Audio de codage audio avancé (AAC) au format ADTS (audio Data Transport Stream).<br/> Le bloc de format est une structure [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) avec **wFormatTag** égal **au \_ format Wave \_ MPEG \_ ADTS \_ AAC**.<br/> La structure [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) spécifie le taux d’échantillonnage et le nombre de canaux du cœur AAC-LC, avant l’application de la réplication de bande spectrale ou des outils PS (Stereo), le cas échéant.<br/> Aucune donnée supplémentaire n’est requise après la structure [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) .<br/>                                                                                                                                                                 | wmcodecdsp. h | **Vague \_ FORMAT \_ MPEG \_ ADTS \_ AAC** (0x1600) |
| **MEDIASUBTYPE \_ MPEG \_ HEAAC**     | High-Efficiency flux de codage audio avancé (HE-AAC).<br/> Le bloc de format est une structure [**HEAACWAVEFORMAT**](/windows/win32/api/mmreg/ns-mmreg-heaacwaveformat) .<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 | wmcodecdsp. h | **Vague \_ FORMAT \_ MPEG \_ HEAAC** (0x1610)     |
| **MEDIASUBTYPE \_ MPEG \_ garantie**      | Flux de transport audio MPEG-4 avec une couche de synchronisation (garantie) et une couche multiplex (LATM).<br/> Le bloc de format est une structure [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) avec **wFormatTag** égal **au \_ format Wave \_ MPEG \_ garantie**.<br/> La structure [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) spécifie le taux d’échantillonnage et le nombre de canaux du cœur AAC-LC, avant d’appliquer les outils Spectra spectral ou PS, le cas échéant.<br/> Aucune donnée supplémentaire n’est requise après la structure [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) .<br/>                                                                                                                                                                                             | wmcodecdsp. h | **Vague \_ FORMAT \_ MPEG \_ garantie** (0x1602)      |
| **MEDIASUBTYPE \_ brut \_ AAC1**       | AAC brut.<br/> Le bloc de format est une structure [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) avec **wFormatTag** égal **au \_ format Wave \_ RAW \_ AAC1**.<br/> La structure [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) spécifie le taux d’échantillonnage et le nombre de canaux dans le son décodé après l’application des outils SBR et PS, le cas échéant.<br/> La structure [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) est suivie d’octets supplémentaires qui contiennent les données AudioSpecificConfig (), comme défini par la norme ISO/IEC 14496-3 (MPEG-4 audio). <br/> La longueur des données AudioSpecificConfig () est de 2 octets pour AAC-LC ou HE-AAC avec signal implicite de SBR/PS. Elle est supérieure à 2 octets pour le HE-AAC avec signalement explicite de SBR/PS.<br/> | wmcodecdps. h | **Vague \_ FORMAT \_ \_ AAC1 brut** (0x00FF)       |



 

## <a name="dolby-audio-types"></a>Types audio Dolby



| GUID                                | Description                                                                                                                                                                                                             | En-tête       | Balise de format équivalente                        |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------|----------------------------------------------|
| **MEDIASUBTYPE \_ Dolby \_ DDplus**     | Audio Dolby Digital plus.                                                                                                                                                                                               | wmcodecdsp. h | n/a                                          |
| **MEDIASUBTYPE \_ Dolby \_ AC3**        | Audio Dolby Digital (AC-3).                                                                                                                                                                                             | ksuuids. h    | n/a                                          |
| **MEDIASUBTYPE \_ Dolby \_ AC3 \_ SPDIF** | Dolby AC-3 sur S/PDIF.                                                                                                                                                                                                 | UUID. h      | **Vague \_ FORMAT \_ Dolby \_ AC3 \_ SPDIF** (0x0092) |
| **MEDIASUBTYPE \_ DVM**               | Codec DVM AC-3. Utilisé lors de la lecture d’un fichier AVI avec Dolby Digital Audio.<br/> Le bloc de format est une structure [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) dont la balise de format est égale au **\_ format Wave \_ DVM**.<br/> | wmcodecdsp. h | **Vague \_ FORMAT \_ DVM** (0x2000)               |
| **MEDIASUBTYPE \_ , \_ sport brut**        | AC-3 sur S/PDIF ; consultez la section Notes.                                                                                                                                                                                          | UUID. h      | **Vague \_ FORMAT \_ \_ sport brut** (0x0240)        |
| **MEDIASUBTYPE \_ SPDIF \_ \_ 241h**  | AC-3 sur S/PDIF ; consultez la section Notes.                                                                                                                                                                                          | UUID. h      | **Vague \_ FORMAT \_ esst \_ AC3** (0x0241)         |



 

Pour spécifier le remplissage AC-3, utilisez le sous-type **MEDIASUBTYPE \_ Dolby \_ AC3 \_ SPDIF**, qui correspond à une balise de format 0x0092 (Wave \_ format \_ Dolby \_ AC3 \_ SPDIF). Les valeurs 0x240 et 0x241 ont également été utilisées pour indiquer le remplissage de l’AC-3, mais Microsoft encourage l’utilisation de 0x0092.

## <a name="miscellaneous-audio-types"></a>Types audio divers



| GUID                                | Description                                                                                                                                                                                                                                                                          | En-tête       | Balise de format équivalente           |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------|---------------------------------|
| **\_Audio DRM \_ MEDIASUBTYPE**        | Audio avec protection de la gestion des droits numériques (DRM).                                                                                                                                                                                                                               | UUID. h      | **Vague \_ FORMAT \_ DRM** (0x0009)  |
| **\_DTS MEDIASUBTYPE**               | Audio Digital Theater Systems (DTS).<br/> Le bloc de format est une structure [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) dont la balise de format est égale au **\_ format Wave \_ inconnu**.<br/>                                                                                              | ksuuids. h    | n/a                             |
| **MEDIASUBTYPE \_ DTS2**              | Audio Digital Theater Systems (DTS).<br/> Le bloc de format est une structure [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) dont la balise de format est égale au **\_ format Wave \_ DTS2**.<br/> Ce sous-type est équivalent à **MEDIASUBTYPE \_ DTS** mais utilise une balise de format différente.<br/> | wmcodecdsp. h | **Vague \_ FORMAT \_ DTS2** (0x2001) |
| **MEDIASUBTYPE \_ DVD \_ LPCM \_ audio**  | Données audio DVD.                                                                                                                                                                                                                                                                      | ksuuids. h    | n/a                             |
| **MEDIASUBTYPE \_ MPEG1AudioPayload** | Charge utile MPEG-1.                                                                                                                                                                                                                                                                | UUID. h      | **Vague \_ FORMAT \_ MPEG** (0x0050) |
| **MEDIASUBTYPE \_ MPEG1Packet**       | Paquet audio MPEG1.                                                                                                                                                                                                                                                                  | UUID. h      | n/a                             |
| **MEDIASUBTYPE \_ MPEG1Payload**      | Charge utile audio MPEG1.                                                                                                                                                                                                                                                                 | UUID. h      | n/a                             |
| **MEDIASUBTYPE \_ MPEG2 \_ audio**      | Données audio MPEG-2.                                                                                                                                                                                                                                                                   | ksuuids. h    | n/a                             |



 

## <a name="audio-format-tags"></a>Balises de format audio

Le champ **wFormatTag** de la structure [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) spécifie le type de format audio. Les exemples de média sont généralement un nombre entier d’échantillons, tel que spécifié dans le champ **wBitsPerSample** de la structure **WAVEFORMATEX** . Cela n’est pas nécessairement vrai pour les exemples audio MPEG qui peuvent provenir de flux de données en paquets et qui ne sont donc pas nécessairement empaquetés sur des limites d’échantillon/Frame. Pour l’audio MPEG, l’horodatage dans un échantillon de média est l’horodatage de la première image dont le premier octet est contenu dans l’échantillon de support.

Les sous-types de média sont définis pour chaque **wFormatTag** comme suit :

-   Le sous-champ Data1 du GUID de sous-type est le même que la valeur **wFormatTag** .
-   Le champ Data 2 est égal à 0.
-   Le champ Data 3 est 0x0010.
-   Le champ Data 4 est 0x80, 0x00, 0x00, 0xAA, 0x00, 0x38, 0x9B, 0x71.

Ainsi, pour les données audio PCM, le GUID de sous-type (défini dans UUID. h en tant que **MEDIASUBTYPE \_ PCM**) est :

`{00000001-0000-0010-8000-00AA00389B71}`

La fonction [**CreateAudioMediaType**](createaudiomediatype.md) peut être utilisée pour créer une structure de [**\_ \_ type de média am**](/windows/win32/api/strmif/ns-strmif-am_media_type) à partir d’une structure **WAVEFORMATEX** .

## <a name="obsolete-audio-types"></a>Types audio obsolètes

Les sous-types audio suivants sont obsolètes et ne doivent pas être utilisés :

-   **MEDIASUBTYPE \_ MPEG \_ brut \_ AAC**
-   **MEDIASUBTYPE \_ PCMAudioObsolete**

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_type de média am \_**](/windows/win32/api/strmif/ns-strmif-am_media_type)
</dt> <dt>

[Types de médias](media-types.md)
</dt> </dl>

 

