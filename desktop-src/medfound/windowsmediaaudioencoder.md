---
description: 'L’encodeur Windows Media Audio encode des flux audio. L’encodeur prend en charge trois catégories de sorties encodées : Windows Media Audio standard, Windows Media Audio Professional et Windows Media Audio Lossless.'
ms.assetid: 1f6a3a9f-b534-4a6b-b773-0315c759624e
title: Encodeur Windows Media Audio (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f9f1d5b9e5f890a43958bcc304dd2d305844fdb4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537626"
---
# <a name="windows-media-audio-encoder"></a>Encodeur Windows Media Audio

L’encodeur Windows Media Audio encode des flux audio. L’encodeur prend en charge trois catégories de sorties encodées : Windows Media Audio standard, Windows Media Audio Professional et Windows Media Audio Lossless.

## <a name="class-identifier"></a>Identificateur de classe

L’identificateur de classe (CLSID) de l’encodeur de Windows Media Audio est représenté par la constante **CLSID \_ CWMAEncMediaObject**. Vous pouvez créer une instance de l’encodeur audio en appelant **CoCreateInstance**.

## <a name="input-formats"></a>Formats d’entrée

Le tableau suivant répertorie les balises de format audio qui représentent les catégories d’entrée prises en charge par l’encodeur Windows Media Audio. Pour plus d’informations sur la définition des types d’entrée et de sortie pour l’encodeur, consultez Configuration de l' [encodage audio](configuringaudioencoding.md).



| Balise de format, constante       | Mettre en forme la valeur de balise | Format audio                                          |
|---------------------------|------------------|-------------------------------------------------------|
| \_PCM format \_ Wave         | 0x0001           | Format PCM                                            |
| \_format Wave \_ IEEE \_ float | 0x0003           | Virgule flottante IEEE                                   |
| \_format Wave \_ extensible  | 0xFFFE           | Format PCM/IEEE dans la structure **WAVEFORMATEXTENSIBLE** |



 

## <a name="output-formats"></a>Formats de sortie

Le tableau suivant répertorie les balises de format audio qui représentent les catégories de sortie prises en charge par l’encodeur Windows Media Audio.



| Balise de format, constante             | Mettre en forme la valeur de balise | Format audio                     |
|---------------------------------|------------------|----------------------------------|
| \_WMAUDIO2 format \_ Wave          | 0x0161           | Windows Media Audio standard     |
| \_WMAUDIO3 format \_ Wave          | 0x0162           | Windows Media Audio professionnel |
| WAVE \_ format \_ WMAUDIO \_ Lossless | 0x0163           | Windows Media Audio sans perte     |



 

## <a name="interfaces"></a>Interfaces

Un objet endoder audio expose l’interface **IMediaObject** afin que l’objet puisse être utilisé en tant qu’objet de média DirectX (DMO) et expose l’interface **IMFTransform** afin que l’objet puisse être utilisé en tant que transformation de Media Foundation (MFT).

Un encodeur Windows Media Audio se comporte comme un DMO ou une table MFT en fonction des interfaces que vous obtenez et de la version de Windows en cours d’exécution. Le tableau suivant indique les conditions dans lesquelles un encodeur audio se comporte comme un DMO ou une table MFT.



| Système d’exploitation | Comportement de l’encodeur                                                                                                                                                                      |
|------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Windows XP       | Un encodeur Windows Media Audio se comporte toujours comme un DMO.                                                                                                                                |
| Windows Vista    | Par défaut, un encodeur Windows Media Audio se comporte comme un DMO. Si vous obtenez une interface **IMFTransform** ou une interface **IPropertyStore** sur un encodeur audio, elle se comporte comme une table MFT. |
| Windows 7        | Par défaut, un encodeur Windows Media Audio se comporte comme un DMO. Si vous obtenez une interface **IMFTransform** sur un encodeur audio, elle se comporte comme une table MFT.                                    |



 

## <a name="encoder-properties"></a>Propriétés de l’encodeur

L’encodeur Windows Media Audio prend en charge les propriétés suivantes.



<table>
<thead>
<tr class="header">
<th>Propriété</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="mfpkey-avgconstrainedproperty.md"><strong>MFPKEY_AVGCONSTRAINED</strong></a></td>
<td>Spécifie si l’encodeur utilise l’encodage VBR moyen-contrôlable.<br/> <dl> Windows Vista et versions ultérieures.<br />
Standard, professionnel, sans perte.<br />
En lecture/écriture.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-bmaxproperty.md"><strong>MFPKEY_BMAX</strong></a></td>
<td>Spécifie la fenêtre de mémoire tampon, en millisecondes, d’un flux de vitesse de transmission variable (VBR) avec restriction à sa vitesse de transmission maximale.<br/> <dl> Windows XP et versions ultérieures.<br />
Standard, professionnel.<br />
En lecture/écriture.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-checkdataconsistency2pproperty.md"><strong>MFPKEY_CHECKDATACONSISTENCY2P</strong></a></td>
<td>Spécifie si l’encodeur doit vérifier la cohérence des données entre les passes lors de l’exécution du codage VBR en deux passes. <br/> <dl> Windows Vista et versions ultérieures.<br />
Standard, professionnel, sans perte.<br />
Lecture seule.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-constraindeclatencyproperty.md"><strong>MFPKEY_CONSTRAINDECLATENCY</strong></a></td>
<td>Spécifie si l’encodeur est limité par une latence maximale de décodeur.<br/> <dl> Windows Vista et versions ultérieures.<br />
Standard, professionnel, sans perte.<br />
En lecture/écriture.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-constrainenccomplexityproperty.md"><strong>MFPKEY_CONSTRAINENCCOMPLEXITY</strong></a></td>
<td>Spécifie si la complexité de l’algorithme d’encodage est restreinte.<br/> <dl> Windows Vista et versions ultérieures.<br />
Standard, professionnel, sans perte.<br />
En lecture/écriture.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-constrainenclatencyproperty.md"><strong>MFPKEY_CONSTRAINENCLATENCY</strong></a></td>
<td>Spécifie si l’encodeur est limité par une latence maximale.<br/> <dl> Windows Vista et versions ultérieures.<br />
Standard, professionnel, sans perte.<br />
En lecture/écriture.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-constrain-enumerated-vbrqualityproperty.md"><strong>MFPKEY_CONSTRAIN_ENUMERATED_VBRQUALITY</strong></a></td>
<td>Spécifie si les modes énumérés par l’encodeur sont limités à ceux qui répondent à une exigence de qualité.<br/> <dl> Windows Vista et versions ultérieures.<br />
Standard, professionnel, sans perte.<br />
En lecture/écriture.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-decodercomplexityprofileproperty.md"><strong>MFPKEY_DECODERCOMPLEXITYPROFILE</strong></a></td>
<td>Spécifie le profil de complexité du contenu encodé.<br/> <dl> Windows XP et versions ultérieures.<br />
Standard, professionnel, sans perte.<br />
Lecture seule.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-desired-vbrqualityproperty.md"><strong>MFPKEY_DESIRED_VBRQUALITY</strong></a></td>
<td>Spécifie le niveau de qualité souhaité pour l’encodage VBR.<br/> <dl> Windows Vista et versions ultérieures.<br />
Standard, professionnel, sans perte.<br />
En écriture seule.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-dyn-allow-noisesubproperty.md"><strong>MFPKEY_DYN_ALLOW_NOISESUB</strong></a></td>
<td>Spécifie si l’encodeur utilise la substitution de bruit.<br/> <dl> Windows Vista et versions ultérieures.<br />
Standard, professionnel, sans perte.<br />
En lecture/écriture.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-dyn-allow-pcmrangelimitingproperty.md"><strong>MFPKEY_DYN_ALLOW_PCMRANGELIMITING</strong></a></td>
<td>Spécifie si l’encodeur utilise la limitation de plage PCM.<br/> <dl> Windows Vista et versions ultérieures.<br />
Standard, professionnel, sans perte.<br />
En lecture/écriture.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-dyn-bandtrunc-bwceilproperty.md"><strong>MFPKEY_DYN_BANDTRUNC_BWCEIL</strong></a></td>
<td>Spécifie la bande passante codée maximale autorisée par la troncation de la bande dans l’encodeur.<br/> <dl> Windows Vista et versions ultérieures.<br />
Standard, professionnel, sans perte.<br />
En lecture/écriture.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-dyn-bandtrunc-bwfloorproperty.md"><strong>MFPKEY_DYN_BANDTRUNC_BWFLOOR</strong></a></td>
<td>Spécifie la bande passante codée minimale autorisée par la troncation de la bande dans l’encodeur.<br/> <dl> Windows Vista et versions ultérieures.<br />
Standard, professionnel, sans perte.<br />
En lecture/écriture.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-dyn-bandtrunc-qceilproperty.md"><strong>MFPKEY_DYN_BANDTRUNC_QCEIL</strong></a></td>
<td>Spécifie la qualité à laquelle la bande passante minimale codée est autorisée. <br/> <dl> Windows Vista et versions ultérieures.<br />
Standard, professionnel, sans perte.<br />
En lecture/écriture.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-dyn-bandtrunc-qfloorproperty.md"><strong>MFPKEY_DYN_BANDTRUNC_QFLOOR</strong></a></td>
<td>Spécifie la qualité à laquelle la bande passante codée maximale est autorisée.<br/> <dl> Windows Vista et versions ultérieures.<br />
Standard, professionnel, sans perte.<br />
En lecture/écriture.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-dyn-bandtruncationproperty.md"><strong>MFPKEY_DYN_BANDTRUNCATION</strong></a></td>
<td>Spécifie si l’encodeur effectue une troncation de bande.<br/> <dl> Windows Vista et versions ultérieures.<br />
Standard, professionnel, sans perte.<br />
En lecture/écriture.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-dyn-simplemaskproperty.md"><strong>MFPKEY_DYN_SIMPLEMASK</strong></a></td>
<td>Spécifie si l’encodeur utilise le style de calcul de masque effectué par la version 7 de l’encodeur Windows Media Audio.<br/> <dl> Windows Vista et versions ultérieures.<br />
Standard, professionnel, sans perte.<br />
En lecture/écriture.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-dyn-stereo-preprocproperty.md"><strong>MFPKEY_DYN_STEREO_PREPROC</strong></a></td>
<td>Spécifie si l’encodeur effectue un traitement d’image stéréo. <br/> <dl> Windows Vista et versions ultérieures.<br />
Standard, professionnel, sans perte.<br />
En lecture/écriture.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-dyn-vbr-bavgproperty.md"><strong>MFPKEY_DYN_VBR_BAVG</strong></a></td>
<td>Spécifie la fenêtre de mémoire tampon, en millisecondes, pour un encodeur qui est configuré pour utiliser l’encodage VBR moyen-contrôlable.<br/> <dl> Windows Vista et versions ultérieures.<br />
Standard, professionnel, sans perte.<br />
En lecture/écriture.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-dyn-vbr-ravgproperty.md"><strong>MFPKEY_DYN_VBR_RAVG</strong></a></td>
<td>Spécifie la vitesse de transmission moyenne, en bits par seconde, pour un encodeur qui est configuré pour utiliser l’encodage VBR moyen-contrôlable.<br/> <dl> Windows Vista et versions ultérieures.<br />
Standard, professionnel, sans perte.<br />
En lecture/écriture.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-enccomplexityproperty.md"><strong>MFPKEY_ENCCOMPLEXITY</strong></a></td>
<td>Spécifie la complexité de l’algorithme d’encodage.<br/> <dl> Windows Vista et versions ultérieures.<br />
Standard, professionnel, sans perte.<br />
En lecture/écriture.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-endofpassproperty.md"><strong>MFPKEY_ENDOFPASS</strong></a></td>
<td>Spécifie la fin d’une passe d’encodage.<br/> <dl> Windows XP et versions ultérieures.<br />
Standard, professionnel.<br />
En écriture seule.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-enhanced-wmaproperty.md"><strong>MFPKEY_ENHANCED_WMA</strong></a></td>
<td>Spécifie si l’encodeur principal utilise la &quot; &quot; fonctionnalité plus.<br/> <dl> Windows Vista et versions ultérieures.<br />
Professionnel.<br />
En lecture/écriture.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-maxdeclatencymsproperty.md"><strong>MFPKEY_MAXDECLATENCYMS</strong></a></td>
<td>Spécifie la latence maximale pour le décodeur, en millisecondes.<br/> <dl> Windows Vista et versions ultérieures.<br />
Standard, professionnel, sans perte.<br />
En écriture seule.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-maxenclatencymsproperty.md"><strong>MFPKEY_MAXENCLATENCYMS</strong></a></td>
<td>Spécifie la latence maximale pour l’encodeur, en millisecondes.<br/> <dl> Windows Vista et versions ultérieures.<br />
Standard, professionnel, sans perte.<br />
En écriture seule.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-most-recently-enumerated-vbrqualityproperty.md"><strong>MFPKEY_MOST_RECENTLY_ENUMERATED_VBRQUALITY</strong></a></td>
<td>Spécifie le niveau de qualité VBR du type de sortie énuméré le plus récemment.<br/> <dl> Windows Vista et versions ultérieures.<br />
Standard, professionnel, sans perte.<br />
Lecture seule.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-passesrecommendedproperty.md"><strong>MFPKEY_PASSESRECOMMENDED</strong></a></td>
<td>Spécifie le nombre maximal de passes prises en charge par l’encodeur.<br/> <dl> Windows XP et versions ultérieures.<br />
Standard, professionnel, sans perte.<br />
Lecture seule.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-passesusedproperty.md"><strong>MFPKEY_PASSESUSED</strong></a></td>
<td>Spécifie le nombre de passes qui seront utilisées par l’encodeur pour encoder le contenu.<br/> <dl> Windows XP et versions ultérieures.<br />
Standard, professionnel, sans perte.<br />
En lecture/écriture.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-peakconstrainedproperty.md"><strong>MFPKEY_PEAKCONSTRAINED</strong></a></td>
<td>Spécifie si l’encodeur est imposé par une vitesse de transmission de pic.<br/> <dl> Windows Vista et versions ultérieures.<br />
Standard, professionnel.<br />
En lecture/écriture.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-preferred-framesizeproperty.md"><strong>MFPKEY_PREFERRED_FRAMESIZE</strong></a></td>
<td>Spécifie le nombre d’échantillons par défaut par image.<br/> <dl> Windows Vista et versions ultérieures.<br />
Professionnel.<br />
En lecture/écriture.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-requesting-a-framesizeproperty.md"><strong>MFPKEY_REQUESTING_A_FRAMESIZE</strong></a></td>
<td>Spécifie si l’encodeur doit utiliser une taille de frame préférée.<br/> <dl> Windows Vista et versions ultérieures.<br />
Professionnel.<br />
En lecture/écriture.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-rmaxproperty.md"><strong>MFPKEY_RMAX</strong></a></td>
<td>Spécifie le taux de bits de pointe, en bits par seconde, utilisé pour l’encodage VBR (variable-bit-rate) avec restriction de 2 passes. <br/> <dl> Windows XP et versions ultérieures.<br />
Standard, professionnel.<br />
En lecture/écriture.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-stat-bavgproperty.md"><strong>MFPKEY_STAT_BAVG</strong></a></td>
<td>Spécifie la fenêtre de mémoire tampon moyenne, en millisecondes, d’un flux encodé.<br/> <dl> Windows XP et versions ultérieures.<br />
Standard, professionnel, sans perte.<br />
Lecture seule.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-stat-bmaxproperty.md"><strong>MFPKEY_STAT_BMAX</strong></a></td>
<td>Spécifie la fenêtre de mémoire tampon maximale, en millisecondes, d’un flux encodé.<br/> <dl> Windows XP et versions ultérieures.<br />
Standard, professionnel, sans perte.<br />
Lecture seule.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-stat-ravgproperty.md"><strong>MFPKEY_STAT_RAVG</strong></a></td>
<td>Spécifie la vitesse de transmission moyenne, en bits par seconde, d’un flux encodé.<br/> <dl> Windows XP et versions ultérieures.<br />
Standard, professionnel, sans perte.<br />
Lecture seule.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-stat-rmaxproperty.md"><strong>MFPKEY_STAT_RMAX</strong></a></td>
<td>Spécifie la vitesse de transmission maximale, en bits par seconde, d’un flux encodé.<br/> <dl> Windows XP et versions ultérieures.<br />
Standard, professionnel, sans perte.<br />
Lecture seule.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-vbrenabledproperty.md"><strong>MFPKEY_VBRENABLED</strong></a></td>
<td>Spécifie si l’encodeur utilise l’encodage VBR.<br/> <dl> Windows XP et versions ultérieures.<br />
Standard, professionnel, sans perte.<br />
En lecture/écriture.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-wma-elementary-streamproperty.md"><strong>MFPKEY_WMA_ELEMENTARY_STREAM</strong></a></td>
<td>Cette propriété n’est pas utilisée actuellement par le codec Windows Media Audio.<br/></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-wmadrc-avgrefproperty.md"><strong>MFPKEY_WMADRC_AVGREF</strong></a></td>
<td>Spécifie le niveau de volume moyen de contenu audio.<br/> <dl> Windows XP et versions ultérieures.<br />
Standard, professionnel, sans perte.<br />
Lecture seule.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-wmadrc-peakrefproperty.md"><strong>MFPKEY_WMADRC_PEAKREF</strong></a></td>
<td>Spécifie le niveau de volume le plus élevé dans le contenu audio.<br/> <dl> Windows XP et versions ultérieures.<br />
Standard, professionnel, sans perte.<br />
Lecture seule.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-wmaenc-avgbytespersecproperty.md"><strong>MFPKEY_WMAENC_AVGBYTESPERSEC</strong></a></td>
<td>Spécifie le nombre moyen d’octets par seconde pour le son encodé en VBR.<br/> <dl> Windows XP et versions ultérieures.<br />
Standard, professionnel, sans perte.<br />
Lecture seule.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-wmaenc-bufferlesscbrproperty.md"><strong>MFPKEY_WMAENC_BUFFERLESSCBR</strong></a></td>
<td>Spécifie si l’encodeur doit produire 1 paquet WMA par trame.<br/> <dl> Windows Vista et versions ultérieures.<br />
Standard, professionnel, sans perte.<br />
En lecture/écriture.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-wmaenc-generate-drc-paramsproperty.md"><strong>MFPKEY_WMAENC_GENERATE_DRC_PARAMS</strong></a></td>
<td>Spécifie si l’encodeur doit générer des paramètres de contrôle de plage dynamique.<br/> <dl> Windows Vista et versions ultérieures.<br />
Standard, professionnel, sans perte.<br />
En lecture/écriture.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-wmaenc-origwaveformatproperty.md"><strong>MFPKEY_WMAENC_ORIGWAVEFORMAT</strong></a></td>
<td>Spécifie la structure <strong>WAVEFORMATEX</strong> décrivant le contenu audio d’entrée.<br/> <dl> Windows XP et versions ultérieures.<br />
Standard, professionnel.<br />
En lecture/écriture.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-wmaenc-rtspdifproperty.md"><strong>MFPKEY_WMAENC_RTSPDIF</strong></a></td>
<td>Spécifie si l’encodeur doit activer l’encodage S/PDIF en temps réel.<br/> <dl> Windows Vista et versions ultérieures.<br />
Professionnel.<br />
En lecture/écriture.<br />
</dl></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|-----------------------------------------------------------------------------------------|
| Client<br/> | Windows XP, Windows Vista ou Windows 7<br/>                                       |
| En-tête<br/> | <dl> <dt>Wmcodecdsp. h</dt> </dl> |
| DLL<br/>    | <dl> <dt>Wmadmoe.dll</dt> </dl>  |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Objets codec](codecobjects.md)
</dt> <dt>

[Implémentation du codec](codecimplementation.md)
</dt> </dl>

 

 




