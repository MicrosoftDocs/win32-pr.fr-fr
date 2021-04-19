---
description: 'Le décodeur Microsoft Media Foundation AAC est une Media Foundation transformation qui décode les profils de codage audio avancé (AAC) et d’efficacité élevée (HE-AAC) suivants :'
ms.assetid: 036fb0ee-8165-41a3-b41a-2e9bf035a6a6
title: Décodeur AAC
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 82dde090dee98cddce9658366bde593b5fc779d7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106516653"
---
# <a name="aac-decoder"></a>Décodeur AAC

Le décodeur Microsoft Media Foundation AAC est une [Media Foundation transformation](media-foundation-transforms.md) qui décode les profils de codage audio avancé (AAC) et d’efficacité élevée (HE-AAC) suivants :

-   Profil LC (Multichannel) MPEG-2 AAC
-   MPEG-4 HE-AAC v1 (Multichannel) avec le cœur AAC-LC.
-   MPEG-4 HE-AAC V2 (stéréo) avec le cœur AAC-LC.

Le décodeur AAC prend en charge les flux AAC bruts sans en-tête ni AAC dans un flux de transport de données audio (ADTS).

À compter de Windows 8, le décodeur AAC prend également en charge le décodage des flux de transport audio MPEG-4 avec une couche multiplex (LATM) et une couche de synchronisation (garantie). Il peut également convertir un flux LATM/garantie en ADTS.

## <a name="media-types"></a>Types de médias

Le décodeur AAC prend en charge les types de média suivants.

### <a name="input-types"></a>Types d’entrée

Le décodeur AAC prend en charge les sous-types audio suivants :



| Subtype                     | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   | En-tête       |
|-----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------|
| **MFAudioFormat_AAC**      | AAC brut ou ADTS AAC.<br/> Pour ce sous-type, le type de média donne le taux d’échantillonnage et le nombre de canaux avant l’application des outils de réplication en bande spectrale (SBR) et de la stéréo paramétrique (PS), le cas échéant. L’effet de l’outil SBR est de doubler le taux d’échantillonnage décodé par rapport au taux d’échantillonnage AAC-LC de base. L’effet de l’outil PS est de décoder le stéréo à partir d’un flux en AAC-LC Core à canaux mono.<br/> Ce sous-type est équivalent à **MEDIASUBTYPE_MPEG_HEAAC**, défini dans wmcodecdsp. h. Consultez [GUID de sous-type audio](audio-subtype-guids.md). <br/> La [source du fichier MPEG-4](mpeg-4-file-source.md) et l’analyseur ADTS génèrent ce sous-type. <br/> | mfapi. h      |
| **MEDIASUBTYPE_RAW_AAC1** | AAC brut. <br/> Ce sous-type est utilisé pour l’AAC contenu dans un fichier AVI avec la balise de format audio égale à WAVE_FORMAT_RAW_AAC1 (0x00FF). <br/> Pour ce sous-type, le type de média donne le taux d’échantillonnage et le nombre de canaux après l’application des outils SBR et PS, le cas échéant.<br/>                                                                                                                                                                                                                                                                                                                                                                                      | wmcodecdsp. h |



 

Pour configurer le décodeur AAC, définissez les attributs suivants sur le type de média d’entrée.



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
<td>Pour plus d’informations, reportez-vous à la description précédente.</td>
</tr>
<tr class="odd">
<td><a href="mf-mt-aac-audio-profile-level-indication.md">MF_MT_AAC_AUDIO_PROFILE_LEVEL_INDICATION</a></td>
<td>Profil et niveau audio. <br/></td>
<td>Optionnel. S’applique uniquement aux <strong>MFAudioFormat_AAC</strong>. <br/> La valeur de cet attribut est le champ <strong>audioProfileLevelIndication</strong> , tel que défini par la norme ISO/IEC 14496-3. <br/> S’il est inconnu, défini à zéro ou à 0xFE ( &quot; aucun profil audio n’est spécifié &quot; ).<br/></td>
</tr>
<tr class="even">
<td><a href="mf-mt-aac-payload-type.md">MF_MT_AAC_PAYLOAD_TYPE</a></td>
<td>Type de charge utile.<br/></td>
<td>S’applique uniquement aux <strong>MFAudioFormat_AAC</strong>. Le décodeur prend en charge les types de charge utile suivants : <br/>
<ul>
<li>0 : AAC brut. Le flux contient uniquement des éléments raw_data_block (), comme défini par MPEG-2.</li>
<li>1 : ADTS. Le flux contient un adts_sequence (), tel que défini par MPEG-2. Une seule raw_data_block () par adts_frame () est autorisée.</li>
<li>3 : flux de transport audio avec une couche de synchronisation (garantie) et une couche multiplex (LATM). Parmi les trois types de garantie, seul <strong>AudioSyncStream</strong> est pris en charge. La couche multiplex est <strong>AudioMuxElement</strong>, restreinte à un programme audio et une couche.</li>
</ul>
<a href="mf-mt-aac-payload-type.md">MF_MT_AAC_PAYLOAD_TYPE</a> est facultatif. Si cet attribut n’est pas spécifié, la valeur par défaut 0 est utilisée, qui spécifie que le flux contient uniquement des éléments raw_data_block.<br/></td>
</tr>
<tr class="odd">
<td><a href="mf-mt-audio-bits-per-sample-attribute.md"><strong>MF_MT_AUDIO_BITS_PER_SAMPLE</strong></a></td>
<td>Profondeur de bits souhaitée du fichier audio PCM décodé.</td>

</tr>
<tr class="even">
<td><a href="mf-mt-audio-channel-mask-attribute.md"><strong>MF_MT_AUDIO_CHANNEL_MASK</strong></a></td>
<td>Spécifie l’affectation des canaux audio aux positions des haut-parleurs.</td>
<td>Optionnel. Pour plus d’informations, consultez <a href="#format-constraints">mettre en forme les contraintes</a>.</td>
</tr>
<tr class="odd">
<td><a href="mf-mt-audio-num-channels-attribute.md"><strong>MF_MT_AUDIO_NUM_CHANNELS</strong></a></td>
<td>Nombre de canaux, y compris le canal à fréquence faible (LFE), le cas échéant.<br/></td>
<td>L’interprétation de cette valeur dépend du sous-type de média, comme décrit précédemment.<br/></td>
</tr>
<tr class="even">
<td><a href="mf-mt-audio-samples-per-second-attribute.md"><strong>MF_MT_AUDIO_SAMPLES_PER_SECOND</strong></a></td>
<td>Taux d’échantillonnage, en échantillons par seconde.<br/></td>
<td>L’interprétation de cette valeur dépend du sous-type de média, comme décrit précédemment.<br/></td>
</tr>
<tr class="odd">
<td><a href="mf-mt-user-data-attribute.md"><strong>MF_MT_USER_DATA</strong></a></td>
<td>Informations de mise en forme supplémentaires.</td>
<td>La valeur de cet attribut dépend du sous-type.<br/>
<ul>
<li><strong>MFAudioFormat_AAC</strong>: contient la partie de la structure <a href="/windows/desktop/api/mmreg/ns-mmreg-heaacwaveinfo"><strong>HEAACWAVEINFO</strong></a> qui apparaît après la structure <strong>WAVEFORMATEX</strong> (autrement dit, après le membre <strong>wfx</strong> ). Cela est suivi des données AudioSpecificConfig (), telles que définies par la norme ISO/IEC 14496-3.</li>
<li><strong>MEDIASUBTYPE_RAW_AAC1</strong>: contient les données AudioSpecificConfig (). Ces données doivent apparaître. dans le cas contraire, le décodeur rejettera le type de média.</li>
</ul>
La longueur des données AudioSpecificConfig () est de 2 octets pour AAC-LC ou HE-AAC avec signal implicite de SBR/PS. Elle est supérieure à 2 octets pour le HE-AAC avec signalement explicite de SBR/PS.<br/> La valeur de <strong>audioObjectType</strong> telle que définie dans AudioSpecificConfig () doit être 2, ce qui indique AAC-LC. La valeur de <strong>extensionAudioObjectType</strong> doit être 5 pour SBR ou 29 pour PS. <br/></td>
</tr>
</tbody>
</table>



 

### <a name="output-types"></a>Types de sortie

Le décodeur prend en charge les types de sortie suivants :



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Subtype</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>MFAudioFormat_Float</strong></td>
<td>Audio à virgule flottante IEEE.</td>
</tr>
<tr class="even">
<td><strong>MFAudioFormat_PCM</strong></td>
<td>audio PCM 16 bits.</td>
</tr>
<tr class="odd">
<td><strong>MFAudioFormat_AAC</strong></td>
<td>Requiert Windows 8. <br/> Ce type de sortie peut être utilisé pour convertir un flux AAC au format garantie/LATM au format ADTS. <br/> Pour convertir un flux garantie/LATM en un flux ADTS, définissez le type d’entrée sur <strong>MFAudioFormat_AAC</strong> avec le type de charge utile 3 (garantie). Définissez ensuite le type de sortie sur <strong>MFAudioFormat_AAC</strong> avec le type de charge utile 1 (ADTS). Le décodeur reformatera le conainter sans décoder le flux binaire. <br/>
<blockquote>
[!Note]<br />
Le décodeur n’inscrit pas <strong>MFAudioFormat_AAC</strong> comme type de sortie. Toutefois, si l’application définit le type d’entrée comme décrit, la méthode <a href="/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype"><strong>IMFTransform :: GetOutputAvailableType</strong></a> retourne <strong>MFAudioFormat_AAC</strong> dans la liste des types de sortie disponibles.
</blockquote>
<br/> <br/></td>
</tr>
</tbody>
</table>



 

Si le flux d’entrée contient plus de deux canaux, le décodeur AAC fournit deux options pour le format de sortie :

-   La même configuration de canal que le type d’entrée.
-   Pliure en stéréo.

## <a name="format-constraints"></a>Contraintes de format

Le taux d’échantillonnage audio décodé doit être l’un des suivants, après l’application de SBR (le cas échéant) :

-   8 kHz
-   11,025 kHz
-   12 kHz
-   16 kHz
-   22,05 kHz
-   24 kHz
-   32 kHz
-   44,1 kHz
-   48 kHz

Les taux d’échantillonnage supérieurs à 48 kHz ne sont pas pris en charge.

Le décodeur prend en charge jusqu’à 6 canaux audio. Pour chaque configuration de haut-parleur, le décodeur s’attend à ce que les éléments syntaxiques AAC apparaissent dans un certain ordre. Le tableau suivant répertorie les configurations de conférencier prises en charge. La troisième colonne de la table répertorie les éléments syntaxiques attendus et leur ordre, en utilisant la notation suivante :

-   <SCE1>: Le single_channel_element (SCE) associé au haut-parleur central.
-   <SCE2>: SCE associée à l’orateur Back central.
-   <CPE1>: Le channel_pair_element (CPE) associé aux haut-parleurs frontaux.
-   <CPE2>: L’ECP associé aux enceintes Back (ou Side)
-   <LFE>: Le lfe_channel_element (LFE).

Pour plus d’informations sur ces éléments syntaxiques, reportez-vous à la norme ISO/IEC 13818-7.



| Configuration       | Masque de canal                                                                                                                                                              | Éléments syntaxiques AAC                          |
|---------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------|
| Mono                | **SPEAKER_FRONT_CENTER**                                                                                                                                                | <SCE1>                                    |
| Stéréo ou double mono | **SPEAKER_FRONT_LEFT** \| **SPEAKER_FRONT_RIGHT**                                                                                                                     | <CPE1>                                    |
| 2/1                 | **SPEAKER_FRONT_LEFT** \| **SPEAKER_FRONT_RIGHT** \| **SPEAKER_BACK_CENTER**                                                                                        | <CPE1><SCE1>                        |
| 2/2                 | **SPEAKER_FRONT_LEFT** \| **SPEAKER_FRONT_RIGHT** \| **SPEAKER_BACK_LEFT** \| **SPEAKER_BACK_RIGHT**                                                              | <CPE1><CPE2>                        |
| 3/0                 | **SPEAKER_FRONT_LEFT** \| **SPEAKER_FRONT_RIGHT** \| **SPEAKER_FRONT_CENTER**                                                                                       | <SCE1><CPE1>                        |
| 3/1                 | **SPEAKER_FRONT_LEFT** \| **SPEAKER_FRONT_RIGHT** \| **SPEAKER_FRONT_CENTER** \| **SPEAKER_BACK_CENTER**                                                          | <SCE1><CPE1><SCE2>            |
| 3/2                 | **SPEAKER_FRONT_LEFT** \| **SPEAKER_FRONT_RIGHT** \| **SPEAKER_FRONT_CENTER** \| **SPEAKER_BACK_LEFT** \| **SPEAKER_BACK_RIGHT**                                | <SCE1><CPE1><CPE2>            |
| 3/2 + LFE           | **SPEAKER_FRONT_LEFT** \| **SPEAKER_FRONT_RIGHT** \| **SPEAKER_FRONT_CENTER** \| **SPEAKER_LOW_FREQUENCY** \| **SPEAKER_BACK_LEFT** \| **SPEAKER_BACK_RIGHT** | <SCE1><CPE1><CPE2><LFE> |



 

Pour les AAC bruts, chaque exemple d’entrée doit contenir exactement une trame compressée AAC complète.

Pour ADTS, chaque exemple d’entrée peut contenir plusieurs images audio, ainsi que des frames partiels, qui peuvent s’étendre sur des limites d’échantillon. Chaque en-tête ADTS doit être suivi d’une trame AAC.

Le décodeur AAC ne prend pas en charge les éléments suivants :

-   Profil principal, Sample-Rate profil Scalable (SRS) ou profil de prédiction à long terme (LTP).
-   Format d’échange de données audio (ADIF).
-   Flux de transport LATM/LAOS.
-   Couplage des éléments de canal. Le décodeur ignore les images audio avec l’opération.
-   AAC-LC avec une taille d’image 960-Sample. Seuls 1024-les exemples de frames sont pris en charge.

## <a name="transform-attributes"></a>Attributs de transformation

Le décodeur AAC implémente la méthode [**IMFTransform :: GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) . Les applications peuvent utiliser cette méthode pour récupérer ou définir les attributs suivants.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Attribut</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="/windows/desktop/DirectShow/avdecaudiodualmono-property"><strong>CODECAPI_AVDecAudioDualMono</strong></a></td>
<td>Spécifie si le contenu audio à 2 canaux est encodé en stéréo ou en double mono. Traiter en lecture seule.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/DirectShow/avdecaudiodualmonorepromode-property"><strong>CODECAPI_AVDecAudioDualMonoReproMode</strong></a></td>
<td>Spécifie comment le décodeur reproduit un double audio mono. La valeur par défaut est <strong>eAVDecAudioDualMonoReproMode_LEFT_MONO</strong>: sortie CH1 vers les haut-parleurs gauche et droit. <br/> Les applications peuvent définir cette propriété pour modifier le comportement par défaut.<br/></td>
</tr>
<tr class="odd">
<td><a href="mft-support-dynamic-format-change-attribute.md"><strong>MFT_SUPPORT_DYNAMIC_FORMAT_CHANGE</strong></a></td>
<td>Le décodeur AAC ne gère pas les modifications de format dynamiques et doit être vidé ou vidé avant qu’un nouveau type de média d’entrée soit défini. Traiter cet attribut comme étant en lecture seule. <br/>
<blockquote>
[!Note]<br />
Le décodeur AAC signale incorrectement la valeur <strong>true</strong> pour cet attribut.
</blockquote>
<br/> <br/> Dans Windows 7, le décodeur signale incorrectement la valeur <strong>true</strong> pour cet attribut. Dans Windows 8, le décodeur signale <strong>false</strong>, qui est la valeur correcte<br/></td>
</tr>
</tbody>
</table>



 

## <a name="example-media-types"></a>Exemples de types de média

Voici un exemple de type de média d’entrée nécessaire pour un flux de 6 canaux, 48-kHz AAC-LC, à l’aide d’une charge AAC brute :



| Attribut                                                                                      | Valeur                                                                                |
|------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|
| [**MF_MT_MAJOR_TYPE**](mf-mt-major-type-attribute.md)                                      | **MFMediaType_Audio**                                                               |
| [**MF_MT_SUBTYPE**](mf-mt-subtype-attribute.md)                                             | **MFAudioFormat_AAC**                                                               |
| [**MF_MT_AUDIO_SAMPLES_PER_SECOND**](mf-mt-audio-samples-per-second-attribute.md)        | 48 000                                                                                |
| [**MF_MT_AUDIO_NUM_CHANNELS**](mf-mt-audio-num-channels-attribute.md)                     | 6                                                                                    |
| [MF_MT_AAC_PAYLOAD_TYPE](mf-mt-aac-payload-type.md)                                       | 0                                                                                    |
| [**MF_MT_USER_DATA**](mf-mt-user-data-attribute.md)                                        | {0x00, 0x00, 0x2A, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x11, 0xb0} |
| [MF_MT_AAC_AUDIO_PROFILE_LEVEL_INDICATION](mf-mt-aac-audio-profile-level-indication.md) | 0x2a (facultatif)                                                                      |



 

Les 12 premiers octets de [**MF_MT_USER_DATA**](mf-mt-user-data-attribute.md) correspondent aux membres de la structure [**HEAACWAVEINFO**](/windows/desktop/api/mmreg/ns-mmreg-heaacwaveinfo) suivants :

-   **wPayloadType** = 0 (AAC brut)
-   **wAudioProfileLevelIndication** = 0X2a (profil AAC, niveau 4)
-   **wStructType** = 0

Les deux derniers octets de [**MF_MT_USER_DATA**](mf-mt-user-data-attribute.md) contenir la valeur de AudioSpecificConfig (), comme défini par MPEG-4.

-   AudioSpecificConfig. audioObjectType = 2 (AAC LC) (5 bits)
-   AudioSpecificConfig. samplingFrequencyIndex = 3 (4 bits)
-   AudioSpecificConfig. channelConfiguration = 6 (4 bits)
-   GASpecificConfig. frameLengthFlag = 0 (1 bit)
-   GASpecificConfig. dependsOnCoreCoder = 0 (1 bit)
-   GASpecificConfig. extensionFlag = 0 (1 bit)

À partir de ce type d’entrée, utilisez le type de média de sortie suivant pour recevoir le fichier audio PCM à virgule flottante 32 bits à 6 canaux du décodeur :



| Attribut                                                                                    | Valeur                    |
|----------------------------------------------------------------------------------------------|--------------------------|
| [**MF_MT_MAJOR_TYPE**](mf-mt-major-type-attribute.md)                                    | **MFMediaType_Audio**   |
| [**MF_MT_SUBTYPE**](mf-mt-subtype-attribute.md)                                           | **MFAudioFormat_Float** |
| [**MF_MT_AUDIO_BITS_PER_SAMPLE**](mf-mt-audio-bits-per-sample-attribute.md)            | 32                       |
| [**MF_MT_AUDIO_SAMPLES_PER_SECOND**](mf-mt-audio-samples-per-second-attribute.md)      | 48 000                    |
| [**MF_MT_AUDIO_NUM_CHANNELS**](mf-mt-audio-num-channels-attribute.md)                   | 6                        |
| [**MF_MT_AUDIO_AVG_BYTES_PER_SECOND**](mf-mt-audio-avg-bytes-per-second-attribute.md) | 1152000 (facultatif)       |
| [**MF_MT_AUDIO_BLOCK_ALIGNMENT**](mf-mt-audio-block-alignment-attribute.md)             | 24 (facultatif)            |
| [**MF_MT_AUDIO_CHANNEL_MASK**](mf-mt-audio-channel-mask-attribute.md)                   | 0x3F (facultatif)          |



 

Si la mise à jour du supplément Platform pour Windows Vista est installée, le décodeur audio AAC est disponible sur Windows Vista, mais il est accessible sur Windows Vista uniquement à l’aide du [lecteur source](source-reader.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 7 uniquement\]<br/>                                                                                                                                                  |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 R2 \[ uniquement\]<br/>                                                                                                                                     |
| DLL<br/>                      | <dl> <dt>Msmpeg2adec.dll sur Windows 7 ; </dt> <dt>MSAudDecMFT.dll sur Windows 8</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Objets codec](codecobjects.md)
</dt> <dt>

[Types de média AAC](aac-media-types.md)
</dt> <dt>

[Types de média audio](audio-media-types.md)
</dt> <dt>

[**Décodeur audio Microsoft MPEG-1/DD/AAC**](/windows/desktop/DirectShow/microsoft-mpeg-1-dd-audio-decoder)
</dt> <dt>

[Prise en charge MPEG-4 dans Media Foundation](mpeg-4-support-in-media-foundation.md)
</dt> <dt>

[Formats multimédias pris en charge dans Media Foundation](supported-media-formats-in-media-foundation.md)
</dt> </dl>
