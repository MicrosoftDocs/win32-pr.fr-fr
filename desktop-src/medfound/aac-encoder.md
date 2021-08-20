---
description: L’encodeur AAC Microsoft Media Foundation est une Media Foundation transformation qui encode le profil LC (Advanced Audio Coding) faible complexité (LC), tel que défini par la norme ISO/IEC 13818-7 (MPEG-2 audio part 7).
ms.assetid: d88a8c32-c71f-4ddb-af8c-e2fb54c2322c
title: Encodeur AAC
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9fb6867ad42645ffc2bbf2b853e215d3794053157a776e02eddf015b320e3215
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119943369"
---
# <a name="aac-encoder"></a>Encodeur AAC

L’encodeur AAC Microsoft Media Foundation est une [Media Foundation transformation](media-foundation-transforms.md) qui encode le profil LC (Advanced Audio Coding) faible complexité (LC), tel que défini par la norme ISO/IEC 13818-7 (MPEG-2 audio part 7).

L’encodeur AAC ne prend pas en charge l’encodage sur d’autres profils AAC, tels que main, SSR ou LTP.

## <a name="class-identifier"></a>Identificateur de classe

L’identificateur de classe (CLSID) de l’encodeur AAC est **CLSID \_ AACMFTEncoder**, défini dans le fichier d’en-tête wmcodecdsp. h.

## <a name="media-types"></a>Types de médias

L’encodeur AAC prend en charge les types de média suivants. Vous pouvez définir les types dans l’un ou l’autre type d’entrée de commande, ou le type de sortie en premier.

### <a name="input-types"></a>Types d’entrée

Définissez les attributs suivants sur le type de média d’entrée.



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
<td>Sous-type.</td>
<td>Doit être <strong>MFAudioFormat_PCM</strong>.</td>
</tr>
<tr class="odd">
<td><a href="mf-mt-audio-bits-per-sample-attribute.md"><strong>MF_MT_AUDIO_BITS_PER_SAMPLE</strong></a></td>
<td>Bits par échantillon.</td>
<td>Doit être 16.</td>
</tr>
<tr class="even">
<td><a href="mf-mt-audio-samples-per-second-attribute.md"><strong>MF_MT_AUDIO_SAMPLES_PER_SECOND</strong></a></td>
<td>Échantillons par seconde.</td>
<td>Les valeurs suivantes sont admises :
<ul>
<li>44100 (44,1 KHz)</li>
<li>48000 (48 KHz)</li>
</ul></td>
</tr>
<tr class="odd">
<td><a href="mf-mt-audio-num-channels-attribute.md"><strong>MF_MT_AUDIO_NUM_CHANNELS</strong></a></td>
<td>Nombre de canaux.</td>
<td>Doit être 1 (mono) ou 2 (stéréo), ou 6 (5,1).
<blockquote>
[!Note]<br />
la prise en charge de 6 canaux audio a été introduite avec Windows 10 et n’est pas disponible pour les versions antérieures de Windows.
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

Une fois que le type d’entrée est défini, l’encodeur dérive les valeurs suivantes et les ajoute au type de média :

-   [**\_octets de \_ données audio MF MT- \_ \_ octets \_ par \_ seconde**](mf-mt-audio-avg-bytes-per-second-attribute.md)
-   [**\_alignement de \_ \_ bloc audio MF MT \_**](mf-mt-audio-block-alignment-attribute.md)
-   [**\_vitesse de \_ \_ transmission moy. MF**](mf-mt-avg-bitrate-attribute.md)

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
<td>Doit être <strong>MFAudioFormat_AAC</strong>.</td>
</tr>
<tr class="odd">
<td><a href="mf-mt-audio-bits-per-sample-attribute.md"><strong>MF_MT_AUDIO_BITS_PER_SAMPLE</strong></a></td>
<td>Bits par échantillon.</td>
<td>Doit être 16.</td>
</tr>
<tr class="even">
<td><a href="mf-mt-audio-samples-per-second-attribute.md"><strong>MF_MT_AUDIO_SAMPLES_PER_SECOND</strong></a></td>
<td>Échantillons par seconde.</td>
<td>Doit correspondre au type d’entrée.</td>
</tr>
<tr class="odd">
<td><a href="mf-mt-audio-num-channels-attribute.md"><strong>MF_MT_AUDIO_NUM_CHANNELS</strong></a></td>
<td>Nombre de canaux.</td>
<td>Doit correspondre au type d’entrée.</td>
</tr>
<tr class="even">
<td><a href="mf-mt-audio-avg-bytes-per-second-attribute.md"><strong>MF_MT_AUDIO_AVG_BYTES_PER_SECOND</strong></a></td>
<td>Vitesse de transmission du flux AAC encodé, en octets par seconde.</td>
<td>Les valeurs suivantes sont admises :
<ul>
<li>12 000</li>
<li>16000</li>
<li>20000</li>
<li>24 000</li>
</ul>
La valeur par défaut pour mono et stéréo est 12000 (96 Kbits/s).<br/></td>
</tr>
<tr class="odd">
<td><a href="mf-mt-aac-payload-type.md">MF_MT_AAC_PAYLOAD_TYPE</a></td>
<td>Type de charge utile AAC.</td>
<td>Facultatif. Si cette valeur est définie, la valeur doit être égale à zéro, ce qui indique que le flux contient uniquement des éléments raw_data_block.<br/> Facultatif. Si l’attribut n’est pas défini, la valeur par défaut est zéro, ce qui indique que le flux contient uniquement des éléments de raw_data_block (AAC brut). <br/> dans Windows 7, si cet attribut est défini, la valeur doit être égale à zéro.<br/> à partir de Windows 8, la valeur peut être 0 (aac brut) ou 1 (ADTS aac). <br/></td>
</tr>
<tr class="even">
<td><a href="mf-mt-aac-audio-profile-level-indication.md">MF_MT_AAC_AUDIO_PROFILE_LEVEL_INDICATION</a></td>
<td>Le niveau et le profil audio AAC.</td>
<td>Facultatif. Les valeurs suivantes sont admises :
<ul>
<li>0x29 (par défaut)</li>
<li>0x2A</li>
<li>0x2B</li>
<li>0x2C</li>
<li>0x2E</li>
<li>0x2F</li>
<li>0x30</li>
<li>0x31</li>
<li>0x32</li>
<li>0x33</li>
</ul></td>
</tr>
</tbody>
</table>

Le tableau suivant répertorie les valeurs qui peuvent être utilisées pour l’attribut MF_MT_AAC_PROFILE_LEVEL_INDICATION.

| Valeur MF_MT_AAC_PROFILE_LEVEL_INDICATION | Profil                           |
|------------------------------------------|-----------------------------------|
| 0x29                                     | Profil AAC L2                    | 
| 0x2A                                     | Profil AAC n4                    | 
| 0x2B                                     | Profil AAC n5                    | 
| 0x2C                                     | Niveau d’efficacité élevé du profil L2 v1 | 
| 0x2E                                     | Niveau élevé d’efficacité v1 avec le profil AAC | 
| 0x2F                                     | Profil à haute performance v1 AAC-n5 | 
| 0x30                                     | Haut niveau d’efficacité 2 Profil AAC L2 | 
| 0x31                                     | Profil L3 v2 haute efficacité | 
| 0x32                                     | High EFFICACITE v2 AAC Profile n4 | 
| 0x33                                     | Profil à haute efficacité v2 AAC-n5 | 

 

Une fois le type de sortie défini, l’encodeur AAC met à jour le type en ajoutant l’attribut de [**\_ \_ \_ données utilisateur MF MT**](mf-mt-user-data-attribute.md) . Cet attribut contient la partie de la structure [**HEAACWAVEINFO**](/windows/desktop/api/mmreg/ns-mmreg-heaacwaveinfo) qui apparaît après la structure [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) (autrement dit, après le membre **wfx** ). Cela est suivi des données AudioSpecificConfig (), telles que définies par la norme ISO/IEC 14496-3.

Chaque exemple de sortie contient une trame AAC compressée sans en-tête. Ce format est équivalent à l' \_ élément Raw Data \_ Block () défini par MPEG-2. S’il est présent dans le type de sortie, l’attribut de [ \_ \_ \_ \_ type de charge utile PP MT AAC](mf-mt-aac-payload-type.md) doit avoir la valeur zéro pour indiquer ce type de charge utile.

Chaque exemple de sortie contient une trame AAC compressée correspondant aux exemples PCM 1024. Par exemple, à 48 kHz de taux d’échantillonnage, la durée d’un cadre compressé est de 21,33 ms.

Si [le \_ \_ type de \_ charge \_ utile MT MT AAC](mf-mt-aac-payload-type.md) est égal à zéro (valeur par défaut), chaque exemple de sortie contient un \_ élément Raw Data \_ Block () tel que défini par la norme ISO/IEC 13818-7.

## <a name="example-media-types"></a>Exemples de types de média

Voici un exemple des types de médias nécessaires pour encoder du son stéréo 44,1-kHz, 160-kbps en AAC brut

Type de média d’entrée :



| Attribut                                                                                    | Valeur                  |
|----------------------------------------------------------------------------------------------|------------------------|
| [**\_type de \_ majeurese MF MT \_**](mf-mt-major-type-attribute.md)                                    | **MFMediaType \_ audio** |
| [**\_sous- \_ type MF MT**](mf-mt-subtype-attribute.md)                                           | **\_PCM MFAudioFormat** |
| [**\_bits de \_ sortie audio MF \_ \_ par \_ échantillon**](mf-mt-audio-bits-per-sample-attribute.md)            | 16                     |
| [**\_ \_ échantillons audio MF \_ MT \_ par \_ seconde**](mf-mt-audio-samples-per-second-attribute.md)      | 44100                  |
| [**\_canaux de \_ \_ numéros audio MF MT \_**](mf-mt-audio-num-channels-attribute.md)                   | 2                      |
| [**\_octets de \_ données audio MF MT- \_ \_ octets \_ par \_ seconde**](mf-mt-audio-avg-bytes-per-second-attribute.md) | 176400 (facultatif)      |
| [**\_alignement de \_ \_ bloc audio MF MT \_**](mf-mt-audio-block-alignment-attribute.md)             | 4 (facultatif)           |
| [**MF \_ MT \_ tous les \_ exemples \_ indépendants**](mf-mt-all-samples-independent-attribute.md)         | 1 (facultatif)           |
| [**\_vitesse de \_ \_ transmission moy. MF**](mf-mt-avg-bitrate-attribute.md)                                  | 1411200 (facultatif)     |
| [**\_exemples de \_ \_ taille fixe \_ MF MF**](mf-mt-fixed-size-samples-attribute.md)                   | 1 (facultatif)           |



 

Type de média de sortie :



| Attribut                                                                                      | Valeur                                                                                           |
|------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| [**\_type de \_ majeurese MF MT \_**](mf-mt-major-type-attribute.md)                                      | **MFMediaType \_ audio**                                                                          |
| [**\_sous- \_ type MF MT**](mf-mt-subtype-attribute.md)                                             | **MFAudioFormat \_ AAC**                                                                          |
| [**\_bits de \_ sortie audio MF \_ \_ par \_ échantillon**](mf-mt-audio-bits-per-sample-attribute.md)              | 16                                                                                              |
| [**\_ \_ échantillons audio MF \_ MT \_ par \_ seconde**](mf-mt-audio-samples-per-second-attribute.md)        | 44100                                                                                           |
| [**\_canaux de \_ \_ numéros audio MF MT \_**](mf-mt-audio-num-channels-attribute.md)                     | 2                                                                                               |
| [**\_octets de \_ données audio MF MT- \_ \_ octets \_ par \_ seconde**](mf-mt-audio-avg-bytes-per-second-attribute.md)   | 20000                                                                                           |
| [\_type de \_ \_ charge utile de l’AAC MT \_](mf-mt-aac-payload-type.md)                                       | 0 (facultatif)                                                                                    |
| [\_indication du \_ \_ niveau de \_ profil \_ audio MF MT AAC \_](mf-mt-aac-audio-profile-level-indication.md) | 0x29 (facultatif)                                                                                 |
| [**\_alignement de \_ \_ bloc audio MF MT \_**](mf-mt-audio-block-alignment-attribute.md)               | 1 (facultatif)                                                                                    |
| [**MF \_ MT \_ tous les \_ exemples \_ indépendants**](mf-mt-all-samples-independent-attribute.md)           | 0 (facultatif)                                                                                    |
| [**\_vitesse de \_ \_ transmission moy. MF**](mf-mt-avg-bitrate-attribute.md)                                    | 160000 (facultatif)                                                                               |
| [**\_ \_ données utilisateur MF \_ MT**](mf-mt-user-data-attribute.md)                                        | {0x00, 0x00, 0x29, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x12, 0x10} facultatif |



 

## <a name="remarks"></a>Remarques

Dans l’implémentation actuelle, chaque exemple d’entrée doit avoir une durée et une durée valides. Pour définir l’heure de l’exemple, appelez [**IMFSample :: SetSampleTime**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-setsampletime). Pour définir la durée de l’exemple, appelez [**IMFSample :: SetSampleDuration**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-setsampleduration).

Si l’heure de l’exemple n’est pas définie, la méthode [**IMFTransform ::P rocessinput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) de l’encodeur retourne **MF \_ E \_ no \_ Sample \_ timestamp**. Si la durée de l’échantillon n’est pas définie, la méthode **ProcessInput** retourne **MF \_ E \_ no \_ Sample \_ Duration**.

La durée de l’échantillon peut être calculée comme suit :


```C++
LONGLONG hnsSampleDuration = 
    ( nAudioSamplesPerChannel * (LONGLONG)10000000 )/nSamplesPerSec;
```



où *nAudioSamplesPerChannel* est le nombre d’échantillons audio PCM par canal dans la mémoire tampon d’entrée, et *nSamplesPerSec* est le taux d’échantillonnage, en échantillons par seconde.

> [!Note]  
> En raison d’un bogue dans l’implémentation actuelle, si la durée de l’échantillon est définie sur zéro, l’appel [**ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) a lieu, mais un appel ultérieur à [**IMFTransform ::P rocessoutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) lèvera une exception de division par zéro. Pour éviter cette erreur, définissez une durée différente de zéro valide pour chaque exemple d’entrée.

 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | applications de \[ bureau Windows 7 uniquement\]<br/>                                              |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 R2, \[ applications de bureau uniquement\]<br/>                                 |
| DLL<br/>                      | <dl> <dt>Mfaacenc.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Objets codec](codecobjects.md)
</dt> <dt>

[**Décodeur AAC**](aac-decoder.md)
</dt> <dt>

[Types de média AAC](aac-media-types.md)
</dt> <dt>

[Types de média audio](audio-media-types.md)
</dt> <dt>

[Prise en charge MPEG-4 dans Media Foundation](mpeg-4-support-in-media-foundation.md)
</dt> <dt>

[Formats multimédias pris en charge dans Media Foundation](supported-media-formats-in-media-foundation.md)
</dt> </dl>

 

