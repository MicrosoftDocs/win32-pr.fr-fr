---
description: L’encodeur audio Microsoft Media Foundation MPEG-2 est une transformation de Media Foundation qui encode le contenu audio mono ou stéréo en MPEG-1 audio (ISO/IEC 11172-3) ou MPEG-2 audio (ISO/IEC 13818-3).
ms.assetid: EBEFED1F-D0B8-4C7E-B1FB-CDE3BDFD99AA
title: Encodeur audio MPEG-2
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2454e542ba59f4955668bd1fcefbf5dbc0f11551
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863422"
---
# <a name="mpeg-2-audio-encoder"></a>Encodeur audio MPEG-2

L’encodeur audio Microsoft Media Foundation MPEG-2 est une [transformation de Media Foundation](media-foundation-transforms.md) qui encode le contenu audio mono ou stéréo en MPEG-1 audio (ISO/IEC 11172-3) ou MPEG-2 audio (ISO/IEC 13818-3).

L’encodeur prend en charge les données audio de couche 1 et 2. Il ne prend pas en charge le format audio MPEG-Layer 3 (MP3). Pour MPEG-2, l’encodeur prend en charge la partie basse fréquence d’échantillonnage (LSF) de l’audio MPEG-2. Elle ne prend pas en charge les extensions multicanaux. La table MFT génère un flux élémentaire MPEG. Il ne peut pas générer des flux élémentaires, des flux de programmes ou des flux de transport de paquets.

## <a name="class-identifier"></a>Identificateur de classe

L’identificateur de classe (CLSID) de l’encodeur audio MEPG-2 est **CLSID \_ CMPEG2AudioEncoderMFT**, défini dans le fichier d’en-tête wmcodecdsp. h.

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
<td>Obligatoire. Doit être <strong>MFAudioFormat_MPEG</strong>. Ce sous-type est utilisé pour MPEG-1 et MPEG-2 audio.</td>
</tr>
<tr class="odd">
<td><a href="mf-mt-audio-samples-per-second-attribute.md">MF_MT_AUDIO_SAMPLES_PER_SECOND</a></td>
<td>Échantillons par seconde.</td>
<td>Obligatoire. Les valeurs suivantes sont prises en charge pour MPEG-1 et MPEG-2 :
<ul>
<li>32000</li>
<li>44100</li>
<li>48 000</li>
</ul>
En outre, les valeurs suivantes sont prises en charge pour MPEG-2 LSF : <br/>
<ul>
<li>16000</li>
<li>22050</li>
<li>24 000</li>
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
<td>Optionnel. S’il est défini, la valeur doit être 0x3 pour les canaux stéréo (avant gauche et droit) ou 0x4 pour mono (canal avant centre).</td>
</tr>
<tr class="even">
<td><a href="mf-mt-audio-avg-bytes-per-second-attribute.md">MF_MT_AUDIO_AVG_BYTES_PER_SECOND</a></td>
<td>Vitesse de transmission du flux MPEG encodé, en octets par seconde.</td>
<td>Optionnel.<br/> Les spécifications ISO/IEC 11172-3 et ISO/IEC 13818-3 (LSF) définissent plusieurs vitesses de transmission, en fonction de la fréquence d’échantillonnage, du nombre de canaux et de la couche audio (1 ou 2). <br/> L’encodeur est défini par défaut sur audio de couche 2. Si l’attribut <a href="mf-mt-audio-avg-bytes-per-second-attribute.md">MF_MT_AUDIO_AVG_BYTES_PER_SECOND</a> n’est pas défini, l’encodeur utilise les vitesses de transmission par défaut suivantes :<br/>
<ul>
<li>Stéréo MPEG-1:224 000 bits par seconde (BPS) = 28 000 octets par seconde.</li>
<li>MPEG-1 mono : 192 000 BPS = 24 000 octets par seconde.</li>
<li>MPEG-2 LSF, mono ou stéréo : 160 000 BPS = 20 000 octets par seconde.</li>
</ul>
Cet attribut peut être défini sur d’autres valeurs. Si la valeur n’est pas valide conformément aux spécifications MPEG, la table MFT rejette le type de média.<br/> Vous pouvez également définir la vitesse de transmission à l’aide de l’interface <a href="/windows/desktop/api/strmif/nn-strmif-icodecapi"><strong>ICodecAPI</strong></a> . Pour plus d'informations, consultez la section Notes.<br/></td>
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
<td>Optionnel. Si cette valeur est définie, la valeur doit correspondre au type de sortie.</td>
</tr>
<tr class="odd">
<td><a href="mf-mt-audio-valid-bits-per-sample-attribute.md">MF_MT_AUDIO_VALID_BITS_PER_SAMPLE</a></td>
<td>Nombre de bits de données audio valides dans chaque exemple audio.</td>
<td>Optionnel. Si cette valeur est définie, la valeur doit être identique à <a href="mf-mt-audio-bits-per-sample-attribute.md">MF_MT_AUDIO_BITS_PER_SAMPLE</a>.</td>
</tr>
</tbody>
</table>



 

L’encodeur ne prend pas en charge la conversion de taux d’échantillonnage ou la conversion stéréo/mono. Si les attributs facultatifs ne sont pas définis, l’encodeur les ajoute au type de média après que le type a été défini.

## <a name="codec-properties"></a>Propriétés du codec

L’encodeur prend en charge les propriétés suivantes par le biais de l’interface [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) .



| Propriété                                                                                | Description                                                                                      | Valeur par défaut                                                                                                                                                          |
|-----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [CODECAPI \_ AVEncCommonMeanBitRate](../directshow/avenccommonmeanbitrate-property.md)               | Spécifie la vitesse de transmission encodée moyenne, en bits par seconde.                                      | Comme décrit pour l’attribut de [ \_ \_ \_ nombre moyen d' \_ octets \_ par \_ seconde de sortie audio MF MT](mf-mt-audio-avg-bytes-per-second-attribute.md) dans le type de média de sortie.                      |
| [CODECAPI \_ AVEncMPACodingMode](../directshow/avencmpacodingmode-property.md)                       | Spécifie le mode d’encodage audio MPEG.                                                          | Stéréo pour l’audio à 2 canaux, ou canal unique pour l’audio à 1 canal.<br/> Pour l’audio à 2 canaux, l’encodeur prend également en charge le double canal et la stéréo jointe.<br/> |
| [CODECAPI \_ AVEncMPACopyright](../directshow/avencmpacopyright-property.md)                         | Spécifie s’il faut définir le bit de copyright dans le flux audio MPEG.                             | Aucun copyright.                                                                                                                                                          |
| [CODECAPI \_ AVEncMPAEmphasisType](../directshow/avencmpaemphasistype-property.md)                   | Spécifie le type de filtre de désaccentuation à utiliser lorsque le flux encodé est décodé. | Aucune accentuation spécifiée.                                                                                                                                                 |
| [AVEncMPAEnableRedundancyProtection](../directshow/avencmpaenableredundancyprotection-property.md) | Spécifie s’il faut ajouter une vérification de redondance cyclique (CRC) à l’en-tête de trame.                    | Une somme de contrôle CRC est écrite dans le flux de bits.                                                                                                                           |
| [CODECAPI \_ AVEncMPALayer](../directshow/avencmpalayer-property.md)                                 | Spécifie la couche audio MPEG.                                                                  | Audio de couche 2.                                                                                                                                                         |
| [CODECAPI \_ AVEncMPAOriginalBitstream](../directshow/avencmpaoriginalbitstream-property.md)         | Spécifie s’il faut définir le bit d’origine dans le flux audio MPEG.                          | Le bit « original » est désactivé.                                                                                                                                                 |
| [CODECAPI \_ AVEncMPAPrivateUserBit](../directshow/avencmpaprivateuserbit-property.md)               | Spécifie s’il faut définir pour le bit d’utilisateur privé dans le flux audio MPEG.                      | Le bit d’utilisateur privé est désactivé.                                                                                                                                               |



 

Pour obtenir un pointeur vers l’interface [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) , appelez [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) sur la table MFT.

La table MFT implémente les méthodes [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) suivantes :

-   [**GetParameterRange**](/windows/win32/api/strmif/nf-strmif-icodecapi-getparameterrange)
-   [**GetParameterValues**](/windows/win32/api/strmif/nf-strmif-icodecapi-getparametervalues)
-   [**GetValue**](/windows/win32/api/strmif/nf-strmif-icodecapi-getvalue)
-   [**IsModifiable**](/windows/win32/api/strmif/nf-strmif-icodecapi-ismodifiable)
-   [**IsSupported**](/windows/win32/api/strmif/nf-strmif-icodecapi-issupported)
-   [**SetValue**](/windows/win32/api/strmif/nf-strmif-icodecapi-setvalue)

Toutes les autres méthodes [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) retournent **E \_ NOTIMPL**.

## <a name="remarks"></a>Notes

Chaque trame audio MPEG contient des échantillons audio 384 (couche 1) ou 1152 (couche 2) par canal. Toutefois, chaque mémoire tampon d’entrée de l’encodeur peut contenir un nombre quelconque d’échantillons PCM. La taille de chaque mémoire tampon d’entrée doit être un multiple de l’alignement de bloc. L’encodeur met en cache les exemples d’entrée jusqu’à ce qu’il soit suffisant pour une trame audio MPEG.

Chaque mémoire tampon de sortie contient une trame MPEG brute. La taille de chaque mémoire tampon de sortie dépend de la vitesse de transmission et du taux d’échantillonnage.

### <a name="configuring-the-encoder"></a>Configuration de l’encodeur

Pour modifier l’un des paramètres par défaut de l’encodeur, procédez comme suit :

1.  Créez une instance de la MFT de l’encodeur.
2.  Appelez [**IMFTransform :: GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) pour afficher la liste des types de sortie préférés. L’encodeur énumère tous les taux d’échantillonnage pour mono et stéréo. Sélectionnez l’un de ces types de média, en fonction du taux d’échantillonnage et du nombre de canaux. L' [attribut \_ \_ \_ nombre moyen d' \_ octets \_ par \_ seconde de sortie audio MF MT](mf-mt-audio-avg-bytes-per-second-attribute.md) indique la vitesse de transmission par défaut en octets par seconde.
3.  Facultatif : vous pouvez remplacer la vitesse de transmission par défaut en définissant une nouvelle valeur pour [MF \_ MT \_ audio \_ AVG \_ octets \_ par \_ seconde](mf-mt-audio-avg-bytes-per-second-attribute.md) sur le type de média de sortie. Les vitesses de transmission valides dépendent du taux d’échantillonnage, du nombre de canaux et de la couche audio.
    > [!Note]  
    > À ce stade du processus de configuration, l’encodeur utilise par défaut l’audio de couche 2 et n’accepte que les débits de couche 2. Vous serez en mesure de basculer l’encodeur vers la couche 1 à une étape ultérieure (Voir l’étape 7). Dans ce cas, laissez la vitesse de transmission par défaut pour l’instant ; vous pouvez le modifier à nouveau à l’étape 8.

     

4.  Appelez [**IMFTransform :: SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) pour définir le type de média de sortie. Si vous définissez votre propre valeur pour [MF \_ MT \_ audio \_ Moy \_ octets \_ par \_ seconde](mf-mt-audio-avg-bytes-per-second-attribute.md) et que la MFT rejette le type de média de sortie, cela est probablement dû au fait que vous avez spécifié une vitesse de transmission non valide.
5.  Appelez [**IMFTransform :: GetInputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputavailabletype) pour énumérer le type de média d’entrée. Étant donné que le taux d’échantillonnage et le nombre de canaux doivent être identiques à ceux du type de sortie, seules deux options sont énumérées : entrée PCM à virgule flottante 32 bits et entrée PCM de type entier 16 bits. Sélectionnez l’une de ces.
6.  Appelez [**IMFTransform :: SetInputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype) pour définir le type de média d’entrée.
7.  Facultatif : pour encoder l’audio de couche 1, définissez la propriété [CODECAPI \_ AVEncMPALayer](../directshow/avencmpalayer-property.md) sur **eAVEncMPALayer \_ 1**.
8.  Facultatif : pour modifier la vitesse de transmission, définissez la propriété [CODECAPI \_ AVEncCommonMeanBitRate](../directshow/avenccommonmeanbitrate-property.md) . La vitesse de transmission doit être l’un des taux de bits valides indiqués dans les spécifications MPEG-1 ou MPEG-2 LSF. Vous pouvez également appeler [**ICodecAPI :: getParameterValues**](/windows/win32/api/strmif/nf-strmif-icodecapi-getparametervalues) pour obtenir une liste de vitesses de transmission valides, en fonction des paramètres actuels.
9.  Facultatif : avec l’audio à 2 canaux, vous pouvez définir la propriété [CODECAPI \_ AVEncMPACodingMode](../directshow/avencmpacodingmode-property.md) pour changer le mode de codage en double canal ou stéréo jointe. Vous pouvez appeler [**ICodecAPI :: GetParameterRange**](/windows/win32/api/strmif/nf-strmif-icodecapi-getparameterrange) pour accéder aux options valides. (Pour l’audio de canal 1, la seule option est mono.)
10. Facultatif : définissez les autres propriétés [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) indiquées précédemment.

Il est important de suivre l’ordre de ces étapes. En particulier, définissez le type de média de sortie avant de modifier les propriétés de [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) . En outre, vous devez définir les propriétés de **ICodecAPI** avant que MFT ne reçoive le premier exemple d’entrée. Une fois que la MFT reçoit l’entrée, les propriétés du codec sont en lecture seule et [**ICodecAPI :: SetValue**](/windows/win32/api/strmif/nf-strmif-icodecapi-setvalue) retourne la valeur **S \_ false**.

### <a name="supported-bit-rates"></a>Vitesses de transmission prises en charge

L’encodeur prend en charge les vitesses de transmission suivantes.



MPEG-1

MPEG-2

Couche 1

Couche 2

Couche 1

Couche 2

32

32\*

32

8

64

48\*

38

16

96

56\*

56

24

128

64

64

32

160

80\*

80

40

192

96

96

48

224

112

112

56

256

128

128

64

288

160

144

80

320

192

160

96

352

224\*\*

176

112

384

256\*\*

192

128

416

230\*\*

224

144

448

384\*\*

256

160



 

<dl> \* Mono uniquement  
\*\* Stéréo uniquement  
</dl>

### <a name="example-media-types"></a>Exemples de types de média

Voici un exemple des types de médias nécessaires pour encoder le PCM d’entiers 16 bits, 48-kHz de l’audio stéréo à la vitesse de transmission par défaut.

Type de média de sortie :

| Attribut                                                                           | Valeur                   |
|-------------------------------------------------------------------------------------|-------------------------|
| [\_type de \_ majeurese MF MT \_](mf-mt-major-type-attribute.md)                               | **MFMediaType \_ audio**  |
| [\_sous- \_ type MF MT](mf-mt-subtype-attribute.md)                                      | **\_MPEG MFAudioFormat** |
| [\_ \_ échantillons audio MF \_ MT \_ par \_ seconde](mf-mt-audio-samples-per-second-attribute.md) | 48 000                   |
| [\_canaux de \_ \_ numéros audio MF MT \_](mf-mt-audio-num-channels-attribute.md)              | 2                       |



 

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



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 8 uniquement\]<br/>                                                |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                 |
| DLL<br/>                      | <dl> <dt>Msmpeg2enc.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Objets codec](codecobjects.md)
</dt> </dl>

 

 
