---
description: Le décodeur Windows Media Audio décode les flux audio qui ont été encodés par l’encodeur Windows Media Audio.
ms.assetid: 2d8e4a97-34a7-4eee-9567-7ae98fa282b9
title: Décodeur Windows Media Audio (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 70f11242f237b8d9709baea6d445a8426236913c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106532556"
---
# <a name="windows-media-audio-decoder"></a>Décodeur Windows Media Audio

Le décodeur Windows Media Audio décode les flux audio qui ont été encodés par l’encodeur [**Windows Media Audio**](windowsmediaaudioencoder.md). Le codeur et le décodeur prennent en charge trois catégories de données audio encodées : Windows Media Audio standard, Windows Media Audio Professional et Windows Media Audio Lossless.

## <a name="class-identifier"></a>Identificateur de classe

L’identificateur de classe (CLSID) du décodeur de Windows Media Audio est représenté par la constante **CLSID \_ CWMADecMediaObject**. Vous pouvez créer une instance du décodeur audio en appelant **CoCreateInstance**.

## <a name="input-formats"></a>Formats d’entrée

Le tableau suivant répertorie les balises de format audio qui représentent les catégories d’entrée prises en charge par le décodeur Windows Media Audio. Pour plus d’informations sur la définition des types d’entrée et de sortie pour le décodeur, consultez [configuration du décodage audio](configuringaudiodecoding.md).



| Balise de format, constante             | Mettre en forme la valeur de balise | Format audio                     |
|---------------------------------|------------------|----------------------------------|
| \_WMAUDIO2 format \_ Wave          | 0x0161           | Windows Media Audio standard     |
| \_WMAUDIO3 format \_ Wave          | 0x0162           | Windows Media Audio professionnel |
| WAVE \_ format \_ WMAUDIO \_ Lossless | 0x0163           | Windows Media Audio sans perte     |



 

## <a name="output-formats"></a>Formats de sortie

Le tableau suivant répertorie les balises de format audio qui représentent les types de sortie pris en charge par le **décodeur Windows Media Audio**. Pour plus d’informations sur la définition des types d’entrée et de sortie pour le décodeur, consultez Configuration de l' [encodage audio](configuringaudioencoding.md).



| Balise de format, constante       | Mettre en forme la valeur de balise | Format audio                                          |
|---------------------------|------------------|-------------------------------------------------------|
| \_PCM format \_ Wave         | 0x0001           | Format PCM                                            |
| \_format Wave \_ IEEE \_ float | 0x0003           | Virgule flottante IEEE                                   |
| \_format Wave \_ extensible  | 0xFFFE           | Format PCM/IEEE dans la structure **WAVEFORMATEXTENSIBLE** |



 

## <a name="interfaces"></a>Interfaces

Un objet décodeur audio expose l’interface **IMediaObject** afin que l’objet puisse être utilisé en tant qu’objet de média DirectX (DMO) et expose l’interface **IMFTransform** afin que l’objet puisse être utilisé en tant que transformation de Media Foundation (MFT).

Un décodeur Windows Media Audio se comporte comme un DMO ou une table MFT en fonction des interfaces que vous obtenez et de la version de Windows en cours d’exécution. Le tableau suivant indique les conditions sous lesquelles un décodeur audio se comporte comme un DMO ou une table MFT.



| Système d’exploitation | Comportement du décodeur                                                                                                                                                                      |
|------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Windows XP       | Un décodeur de Windows Media Audio se comporte toujours comme un DMO.                                                                                                                                |
| Windows Vista    | Par défaut, un décodeur de Windows Media Audio se comporte comme un DMO. Si vous obtenez une interface **IMFTransform** ou une interface **IPropertyStore** sur un décodeur audio, elle se comporte comme une table MFT. |
| Windows 7        | Par défaut, un décodeur de Windows Media Audio se comporte comme un DMO. Si vous obtenez une interface **IMFTransform** sur un décodeur audio, elle se comporte comme une table MFT.                                    |



 

## <a name="properties"></a>Propriétés

Le décodeur Windows Media Audio prend en charge les propriétés suivantes.



<table>
<thead>
<tr class="header">
<th>Propriété</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="mfpkey-decoder-maxnumpcmsampleswithpaddedsilenceproperty.md"><strong>MFPKEY_Decoder_MaxNumPCMSamplesWithPaddedSilence</strong></a></td>
<td>Spécifie le nombre maximal d’échantillons PCM supplémentaires qui peuvent être retournés à la fin du décodage d’un fichier.<br/> <dl> Windows Vista et versions ultérieures.<br />
Standard, professionnel, sans perte.<br />
Lecture seule.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-wmadec-drcmodeproperty.md"><strong>MFPKEY_WMADEC_DRCMODE</strong></a></td>
<td>Spécifie le mode de contrôle de plage dynamique qui sera utilisé par le décodeur audio.<br/> <dl> Windows XP et versions ultérieures.<br />
Standard, professionnel, sans perte.<br />
En écriture seule.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-wmadec-folddown-matrixproperty.md"><strong>MFPKEY_WMADEC_FOLDDOWN_MATRIX</strong></a></td>
<td>Spécifie les coefficients de repli pour le décodage de l’audio multicanaux pour un nombre de canaux inférieur à celui contenu dans le flux encodé. <br/> <dl> Windows XP et versions ultérieures.<br />
Professional<br />
En écriture seule.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-wmadec-hiresoutputproperty.md"><strong>MFPKEY_WMADEC_HIRESOUTPUT</strong></a></td>
<td>Spécifie si le décodeur audio doit fournir une sortie haute résolution.<br/> <dl> Windows XP et versions ultérieures.<br />
Professionnel, sans perte.<br />
En écriture seule.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-wmadec-ltrtoutputproperty.md"><strong>MFPKEY_WMADEC_LTRTOUTPUT</strong></a></td>
<td>Spécifie si le décodeur audio doit effectuer Lt-Rt pli vers le dessous.<br/> <dl> Windows Vista et versions ultérieures.<br />
Professionnel.<br />
En écriture seule.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-wmadec-spkrcfgproperty.md"><strong>MFPKEY_WMADEC_SPKRCFG</strong></a></td>
<td>Spécifie la configuration de l’orateur sur l’ordinateur client.<br/> <dl> Windows XP et versions ultérieures.<br />
Professionnel.<br />
En écriture seule.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-wmadrc-avgrefproperty.md"><strong>MFPKEY_WMADRC_AVGREF</strong></a></td>
<td>Spécifie le niveau de volume moyen de contenu audio.<br/> <dl> Windows XP et versions ultérieures.<br />
Professionnel, sans perte.<br />
En lecture/écriture.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-wmadrc-avgtargetproperty.md"><strong>MFPKEY_WMADRC_AVGTARGET</strong></a></td>
<td>Spécifie le niveau de volume moyen souhaité de contenu audio de sortie.<br/> <dl> Windows XP et versions ultérieures.<br />
Professionnel, sans perte.<br />
En écriture seule.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-wmadrc-peakrefproperty.md"><strong>MFPKEY_WMADRC_PEAKREF</strong></a></td>
<td>Spécifie le niveau de volume le plus élevé dans le contenu audio.<br/> <dl> Windows XP et versions ultérieures.<br />
Professionnel, sans perte.<br />
En lecture/écriture.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-wmadrc-peaktargetproperty.md"><strong>MFPKEY_WMADRC_PEAKTARGET</strong></a></td>
<td>Spécifie le niveau de volume maximal souhaité pour le contenu audio de sortie.<br/> <dl> Windows XP et versions ultérieures.<br />
Professionnel, sans perte.<br />
En écriture seule.<br />
</dl></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|-----------------------------------------------------------------------------------------|
| Client<br/> | Windows XP, Windows Vista ou Windows 7<br/>                                       |
| En-tête<br/> | <dl> <dt>Wmcodecdsp. h</dt> </dl> |
| DLL<br/>    | <dl> <dt>Wmadmod.dll</dt> </dl>  |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Objets codec](codecobjects.md)
</dt> <dt>

[Implémentation du codec](codecimplementation.md)
</dt> </dl>

 

 




