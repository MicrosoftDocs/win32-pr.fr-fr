---
description: L’encodeur audio Dolby est une Media Foundation transformation (MFT) qui encode le son mono ou stéréo sur Dolby Digital, également appelé Dolby AC-3.
ms.assetid: CBC31132-046C-4CD7-9DBA-20A9C666FB43
title: Encodeur audio Dolby Digital
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f901587b816bc17d62f4095e093b661ce55f0009
ms.sourcegitcommit: 88049609e29f91a42442235885abf56f598b06b3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/19/2021
ms.locfileid: "110153562"
---
# <a name="dolby-digital-audio-encoder"></a>Encodeur audio Dolby Digital

L’encodeur audio Dolby est une [Media Foundation transformation](media-foundation-transforms.md) (MFT) qui encode le son mono ou stéréo sur Dolby Digital, également appelé Dolby AC-3. L’encodeur ne prend pas en charge les entrées multicanal, telles que la configuration du canal 5,1.

> [!IMPORTANT]
> Pour les versions de Windows antérieures à Windows 8, l’implémentation Microsoft de la technologie Dolby Digital est limitée aux termes du programme de gestion de licences Dolby Digital à utiliser par les applications Microsoft.

 

Pour plus d’informations sur Dolby Digital Audio, reportez-vous à la version B du document ATSC *audio compression standard (AC-3, E-AC-3)*.

## <a name="class-identifier"></a>Identificateur de classe

L’identificateur de classe (CLSID) de l’encodeur audio Dolby est **CLSID \_ CMSDolbyDigitalEncMFT**, défini dans le fichier d’en-tête wmcodecdsp. h.

## <a name="output-types"></a>Types de sortie

Le type de sortie doit être défini en premier, avant le type d’entrée. Le tableau suivant répertorie les attributs obligatoires et facultatifs pour le type de média de sortie.



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
<td><a href="mf-mt-major-type-attribute.md">MF_MT_MAJOR_TYPE</a></td>
<td>Type principal.</td>
<td>Obligatoire. Doit être <strong>MFMediaType_Audio</strong>.</td>
</tr>
<tr class="even">
<td><a href="mf-mt-subtype-attribute.md">MF_MT_SUBTYPE</a></td>
<td>Sous-type audio.</td>
<td>Obligatoire. Doit être <strong>MFAudioFormat_Dolby_AC3</strong>.</td>
</tr>
<tr class="odd">
<td><a href="mf-mt-audio-samples-per-second-attribute.md">MF_MT_AUDIO_SAMPLES_PER_SECOND</a></td>
<td>Échantillons par seconde.</td>
<td>Obligatoire. Les valeurs suivantes sont admises :
<ul>
<li>32000</li>
<li>44100</li>
<li>48 000</li>
</ul></td>
</tr>
<tr class="even">
<td><a href="mf-mt-audio-num-channels-attribute.md">MF_MT_AUDIO_NUM_CHANNELS</a></td>
<td>Nombre de canaux.</td>
<td>Obligatoire. Doit avoir la valeur 1 (mono) ou 2 (stéréo).</td>
</tr>
<tr class="odd">
<td><a href="mf-mt-audio-channel-mask-attribute.md">MF_MT_AUDIO_CHANNEL_MASK</a></td>
<td>Spécifie l’affectation des canaux audio aux positions des haut-parleurs.</td>
<td>facultatif. S’il est défini, la valeur doit être 0x3 pour les canaux stéréo (avant gauche et droit) ou 0x4 pour mono (canal avant centre).</td>
</tr>
<tr class="even">
<td><a href="mf-mt-audio-avg-bytes-per-second-attribute.md">MF_MT_AUDIO_AVG_BYTES_PER_SECOND</a></td>
<td>Débit binaire du flux AC-3 encodé, en octets par seconde.</td>
<td>facultatif. Consultez la section Notes pour connaître les valeurs valides. Si cet attribut n’est pas défini, l’encodeur utilise une vitesse de transmission par défaut, comme décrit dans la section Notes.</td>
</tr>
</tbody>
</table>



 

Si les attributs facultatifs ne sont pas définis, l’encodeur les ajoute au type de média après que le type a été défini.

## <a name="input-types"></a>Types d’entrée

Le tableau suivant répertorie les attributs obligatoires et facultatifs pour le type de média d’entrée.



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
<td><a href="mf-mt-major-type-attribute.md">MF_MT_MAJOR_TYPE</a></td>
<td>Type principal.</td>
<td>Obligatoire. Doit être <strong>MFMediaType_Audio</strong>.</td>
</tr>
<tr class="even">
<td><a href="mf-mt-subtype-attribute.md">MF_MT_SUBTYPE</a></td>
<td>Sous-type audio.</td>
<td>Obligatoire. Doit être <strong>MFAudioFormat_PCM</strong> ou <strong>MFAudioFormat_Float</strong>.</td>
</tr>
<tr class="odd">
<td><a href="mf-mt-audio-bits-per-sample-attribute.md">MF_MT_AUDIO_BITS_PER_SAMPLE</a></td>
<td>Nombre de bits par échantillon audio.</td>
<td>Obligatoire. La valeur doit être 16 si le sous-type est <strong>MFAudioFormat_PCM</strong>, ou 32 si le sous-type est <strong>MFAudioFormat_Float</strong>.</td>
</tr>
<tr class="even">
<td><a href="mf-mt-audio-samples-per-second-attribute.md">MF_MT_AUDIO_SAMPLES_PER_SECOND</a></td>
<td>Échantillons par seconde.</td>
<td>Obligatoire. Doit correspondre au type de sortie.</td>
</tr>
<tr class="odd">
<td><a href="mf-mt-audio-num-channels-attribute.md">MF_MT_AUDIO_NUM_CHANNELS</a></td>
<td>Nombre de canaux.</td>
<td>Obligatoire. Doit correspondre au type de sortie.</td>
</tr>
<tr class="even">
<td><a href="mf-mt-audio-block-alignment-attribute.md">MF_MT_AUDIO_BLOCK_ALIGNMENT</a></td>
<td>Alignement de bloc, en octets.</td>
<td>Obligatoire. Calculez la valeur comme suit :
<ul>
<li><strong>MFAudioFormat_PCM</strong>: nombre de canaux × 2.</li>
<li><strong>MFAudioFormat_Float</strong>: nombre de canaux × 4.</li>
</ul></td>
</tr>
<tr class="odd">
<td><a href="mf-mt-audio-avg-bytes-per-second-attribute.md">MF_MT_AUDIO_AVG_BYTES_PER_SECOND</a></td>
<td>Vitesse de transmission du flux de données AC3 encodé, en octets par seconde.</td>
<td>Obligatoire. Doit être égal à alignement de bloc × échantillons par seconde.</td>
</tr>
<tr class="even">
<td><a href="mf-mt-audio-channel-mask-attribute.md">MF_MT_AUDIO_CHANNEL_MASK</a></td>
<td>Spécifie l’affectation des canaux audio aux positions des haut-parleurs.</td>
<td>facultatif. Si cette valeur est définie, la valeur doit correspondre au type de sortie.</td>
</tr>
<tr class="odd">
<td><a href="mf-mt-audio-valid-bits-per-sample-attribute.md">MF_MT_AUDIO_VALID_BITS_PER_SAMPLE</a></td>
<td>Nombre de bits de données audio valides dans chaque exemple audio.</td>
<td>facultatif. Si cette valeur est définie, la valeur doit être identique à <a href="mf-mt-audio-bits-per-sample-attribute.md">MF_MT_AUDIO_BITS_PER_SAMPLE</a>.</td>
</tr>
</tbody>
</table>



 

L’encodeur ne prend pas en charge la conversion de taux d’échantillonnage ou la conversion stéréo/mono.

## <a name="remarks"></a>Remarques

Chaque trame audio Dolby AC-3 contient 1536 échantillons audio par canal. Toutefois, chaque mémoire tampon d’entrée de l’encodeur peut contenir un nombre quelconque d’échantillons PCM. La taille de chaque mémoire tampon d’entrée doit être un multiple de l’alignement de bloc. L’encodeur met en cache les exemples d’entrée jusqu’à ce qu’il soit suffisant pour les échantillons audio 1536 par canal ; à partir de là, l’encodeur génère une trame AC-3.

Chaque mémoire tampon de sortie contient une trame AC-3 brute. La durée est équivalente à la durée des échantillons PCM 1536 au taux d’échantillonnage actuel (32 ms) à 48 kHz, 34,83 ms à 44,1 kHz et 48 MS à 32 kHz). La taille de chaque mémoire tampon de sortie dépend de la vitesse de transmission et du taux d’échantillonnage.

Pour spécifier la vitesse de transmission de l’encodage, définissez l’attribut de sortie [ \_ \_ \_ nombre moyen d' \_ octets \_ par \_ seconde du type MF MT audio par seconde](mf-mt-audio-avg-bytes-per-second-attribute.md) dans le type de sortie. Le tableau suivant indique la relation entre la vitesse de transmission de l’encodage et le \_ \_ nombre moyen d’octets de sortie audio MF MT \_ \_ \_ par \_ seconde.



| Débit binaire (Kbits/s) | [\_octets de \_ données audio MF MT- \_ \_ octets \_ par \_ seconde](mf-mt-audio-avg-bytes-per-second-attribute.md) | Remarques                                                 |
|-----------------|------------------------------------------------------------------------------------------|---------------------------------------------------------|
| 64              | 8000                                                                                     | Mono uniquement.                                              |
| 80              | 10000                                                                                    | Mono uniquement.                                              |
| 96              | 12 000                                                                                    | Mono uniquement.                                              |
| 112             | 14000                                                                                    | Mono uniquement.                                              |
| 128             | 16000                                                                                    | Mono ou stéréo.                                         |
| 160             | 20000                                                                                    | Mono ou stéréo.                                         |
| 192             | 24 000                                                                                    | Mono ou stéréo. Il s’agit du paramètre par défaut pour mono.   |
| 224             | 28000                                                                                    | Mono ou stéréo.                                         |
| 256             | 32000                                                                                    | Mono ou stéréo. Il s’agit du paramètre par défaut pour le stéréo. |
| 320             | 40000                                                                                    | Stéréo uniquement.                                            |
| 384             | 48 000                                                                                    | Stéréo uniquement.                                            |
| 448             | 56 000                                                                                    | Stéréo uniquement.                                            |



 

Le débit binaire d’encodage par défaut est défini à 256 kbits/s pour stéréo et 192 kbps pour mono. Les paramètres par défaut sont reflétés dans les types de média retournés par la méthode [**IMFTransform :: GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) de l’encodeur.

### <a name="example-media-types"></a>Exemples de types de média

Voici un exemple des types de médias nécessaires pour encoder le PCM d’entiers 16 bits, 48-kHz de l’audio stéréo à la vitesse de transmission par défaut de 256 kbits/s.

Type de média de sortie :

| Attribut                                                                           | Valeur                         |
|-------------------------------------------------------------------------------------|-------------------------------|
| [\_type de \_ majeurese MF MT \_](mf-mt-major-type-attribute.md)                               | **MFMediaType \_ audio**        |
| [\_sous- \_ type MF MT](mf-mt-subtype-attribute.md)                                      | **MFAudioFormat \_ Dolby \_ AC3** |
| [\_ \_ échantillons audio MF \_ MT \_ par \_ seconde](mf-mt-audio-samples-per-second-attribute.md) | 48 000                         |
| [\_canaux de \_ \_ numéros audio MF MT \_](mf-mt-audio-num-channels-attribute.md)              | 2                             |



 

Type de média d’entrée :

| Attribut                                                                                | Valeur                  |
|------------------------------------------------------------------------------------------|------------------------|
| [\_type de \_ majeurese MF MT \_](mf-mt-major-type-attribute.md)                                    | **MFMediaType \_ audio** |
| [\_sous- \_ type MF MT](mf-mt-subtype-attribute.md)                                           | **\_PCM MFAudioFormat** |
| [\_bits de \_ sortie audio MF \_ \_ par \_ échantillon](mf-mt-audio-bits-per-sample-attribute.md)            | 16                     |
| [\_ \_ échantillons audio MF \_ MT \_ par \_ seconde](mf-mt-audio-samples-per-second-attribute.md)      | 48 000                  |
| [\_canaux de \_ \_ numéros audio MF MT \_](mf-mt-audio-num-channels-attribute.md)                   | 2                      |
| [\_alignement de \_ \_ bloc audio MF MT \_](mf-mt-audio-block-alignment-attribute.md)             | 4                      |
| [\_octets de \_ données audio MF MT- \_ \_ octets \_ par \_ seconde](mf-mt-audio-avg-bytes-per-second-attribute.md) | 192000                 |



 

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications Windows 8 \[ Desktop Apps \| UWP\]<br/>                                       |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                               |
| DLL<br/>                      | <dl> <dt>Msac3enc.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Objets codec](codecobjects.md)
</dt> </dl>

 

 




