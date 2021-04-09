---
description: Microsoft Media Foundation.
ms.assetid: 4C397139-6553-4707-B737-7C31C5D423BA
title: Encodeur audio MP3
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7ea2b22d2fe8cd51f9a2990970493e0415f34d3c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104034159"
---
# <a name="mp3-audio-encoder"></a>Encodeur audio MP3

L’encodeur audio MP3 Microsoft Media Foundation est une [transformation de Media Foundation](media-foundation-transforms.md) (MFT) qui encode le contenu audio MPEG-1 (MP3).

## <a name="class-identifier"></a>Identificateur de classe

L’identificateur de classe (CLSID) de l’encodeur MP3 est **CLSID \_ MP3ACMCodecWrapper**, défini dans le fichier d’en-tête wmcodecdsp. h.

## <a name="media-types"></a>Types de médias

L’encodeur MP3 prend en charge les types de média suivants. Le type de sortie doit être défini avant le type d’entrée.

### <a name="output-types"></a>Types de sortie

Définissez les attributs suivants sur le type de média de sortie.



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Attribut</th>
<th>Description</th>
<th>Notes</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="mf-mt-major-type-attribute.md"><strong>MF_MT_MAJOR_TYPE</strong></a></td>
<td>Type principal.</td>
<td>Doit être <strong>MFMediaType_Audio</strong>.</td>
</tr>
<tr class="even">
<td><a href="mf-mt-subtype-attribute.md"><strong>MF_MT_SUBTYPE</strong></a></td>
<td>Sous-type audio.</td>
<td>Doit être <strong>MFAudioFormat_MP3</strong>.</td>
</tr>
<tr class="odd">
<td><a href="mf-mt-audio-avg-bytes-per-second-attribute.md"><strong>MF_MT_AUDIO_AVG_BYTES_PER_SECOND</strong></a></td>
<td>Vitesse de transmission du flux MP3 encodé, en octets par seconde.</td>
<td>L’encodeur prend en charge toutes les vitesses de transmission définies par la norme (32, 40, 48, 56, 64, 80, 96, 112, 128, 160, 192, 224, 256 ou 320 Kbits/s).<br/> Les vitesses de transmission par défaut sont de 128 Kbits/s pour mono et 320 kbps pour le stéréo.<br/> Utilisez cet attribut pour spécifier la vitesse de transmission encodée.<br/></td>
</tr>
<tr class="even">
<td><a href="mf-mt-audio-num-channels-attribute.md"><strong>MF_MT_AUDIO_NUM_CHANNELS</strong></a></td>
<td>Nombre de canaux.</td>
<td>Les valeurs suivantes sont admises :
<ul>
<li>1 (mono)</li>
<li>2 (stéréo)</li>
</ul></td>
</tr>
<tr class="odd">
<td><a href="mf-mt-audio-samples-per-second-attribute.md"><strong>MF_MT_AUDIO_SAMPLES_PER_SECOND</strong></a></td>
<td>Échantillons par seconde.</td>
<td>Les valeurs suivantes sont admises :
<ul>
<li>48000 (48 KHz)</li>
<li>44100 (44,1 KHz)</li>
<li>32000 (32 KHz)</li>
</ul></td>
</tr>
<tr class="even">
<td><a href="mf-mt-user-data-attribute.md">MF_MT_USER_DATA</a></td>
<td>Données de codec supplémentaires.</td>
<td>Cet attribut contient les 12 octets de la structure <a href="/windows/desktop/api/mmreg/ns-mmreg-mpeglayer3waveformat"><strong>MPEGLAYER3WAVEFORMAT</strong></a> qui suivent le membre <strong>wfx</strong> de cette structure.</td>
</tr>
</tbody>
</table>



 

Vous pouvez également remplir une structure [**MPEGLAYER3WAVEFORMAT**](/windows/win32/api/mmreg/ns-mmreg-mpeglayer3waveformat) et appeler [**MFInitMediaTypeFromWaveFormatEx**](/windows/desktop/api/mfapi/nf-mfapi-mfinitmediatypefromwaveformatex) pour convertir la structure en un type de média Media Foundation.

### <a name="input-types"></a>Types d’entrée

Définissez les attributs suivants sur le type de média d’entrée.



| Attribut                                                                               | Description         | Notes                         |
|-----------------------------------------------------------------------------------------|---------------------|---------------------------------|
| [**\_type de \_ majeurese MF MT \_**](mf-mt-major-type-attribute.md)                               | Type principal.         | Doit être **MFMediaType \_ audio**. |
| [**\_sous- \_ type MF MT**](mf-mt-subtype-attribute.md)                                      | Sous-type.            | Doit être **MFAudioFormat \_ PCM**. |
| [**\_bits de \_ sortie audio MF \_ \_ par \_ échantillon**](mf-mt-audio-bits-per-sample-attribute.md)       | Bits par échantillon.    | Doit être 16.                     |
| [**\_ \_ échantillons audio MF \_ MT \_ par \_ seconde**](mf-mt-audio-samples-per-second-attribute.md) | Échantillons par seconde. | Doit correspondre au type de sortie.     |
| [**\_canaux de \_ \_ numéros audio MF MT \_**](mf-mt-audio-num-channels-attribute.md)              | Nombre de canaux. | Doit correspondre au type de sortie.     |



 

L’encodeur prend en charge uniquement l’entrée PCM de type entier 16 bits. Elle ne prend pas en charge l’entrée à virgule flottante 32 bits.

### <a name="media-formats"></a>Formats multimédias

La norme MPEG-1 et MPEG-2 définit des formats audio de couche 3 252. L’encodeur MP3 prend en charge la norme avec quelques exceptions, ainsi que certains formats supplémentaires, comme décrit ci-dessous. La couche 3 est définie comme suit :



| Condition requise | Valeur |
|----------------------------------|---------------------------------------------------------------|
| Canaux                         | mono ou stéréo                                                |
| Taux d’échantillonnage MPEG-1 en kHz       | 44,1, 48, 32                                                  |
| Débits binaires encodés MPEG-1 en Kbits/s | 32, 40, 48, 56, 64, 80, 96, 112, 128, 160, 192, 224, 256, 320 |
| Taux d’échantillonnage MPEG-2 en kHz       | 8, 11,025, 12, 16, 22,05, 24                                  |
| Débits binaires encodés MPEG-2 en Kbits/s | 8, 16, 24, 32, 40, 48, 56, 64, 80, 96, 112, 144, 160          |



 

L’encodeur MP3 prend également en charge les formats suivants.



| Échantillonnage | Vitesse de transmission     | Numéro de canal |
|-------------|--------------|----------------|
| 8000        | 18000, 20000 | 2              |
| 11025       | 18000, 20000 | 1 ou 2         |
| 12 000       | 18000, 20000 | 1 ou 2         |
| 16000       | 18000, 20000 | 1              |
| 32000       | 144000       | 1 ou 2         |
| 44100       | 144000       | 1 ou 2         |
| 48 000       | 144000       | 1 ou 2         |



 

L’encodeur MP3 ne prend pas en charge les formats suivants définis par la norme.



| Échantillonnage | Vitesses de transmission                                    | Numéro de canal |
|-------------|----------------------------------------------|----------------|
| 12 000       | 80000, 96000, 112000, 128000, 144000, 160000 | 1 ou 2         |
| 11025       | 80000, 96000, 112000, 128000, 144000, 160000 | 1 ou 2         |
| 8000        | 80000, 96000, 112000, 128000, 144000, 160000 | 1 ou 2         |
| 8000        | 8000, 11025, 12000, 16000, 22050, 24000      | 2              |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 8 uniquement\]<br/>           |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2012 \[ uniquement\]<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Objets codec](codecobjects.md)
</dt> </dl>

 

 
