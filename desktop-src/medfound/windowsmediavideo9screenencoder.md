---
description: l’encodeur d’écran Windows Media Video 9 est optimisé pour l’encodage des captures d’écran séquentielles à partir des moniteurs d’ordinateur.
ms.assetid: 22faebf8-40c0-47f9-b66b-c0a8b5ba7202
title: Windows Encodeur d’écran Media Video 9 (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a6d9fbe59671d978fb7374acbbc8ed1d8e9ea5afded0154242c4d1ccb4df3d4d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119713139"
---
# <a name="windows-media-video-9-screen-encoder"></a>Windows Encodeur d’écran Media Video 9

l’encodeur d’écran Windows Media Video 9 est optimisé pour l’encodage des captures d’écran séquentielles à partir des moniteurs d’ordinateur.

## <a name="class-identifier"></a>Identificateur de classe

l’identificateur de classe (CLSID) de l’encodeur d’écran Windows Media Video 9 est représenté par la constante **clsid \_ CMSSCEncMediaObject2**. Vous pouvez créer une instance de l’encodeur en appelant **CoCreateInstance**.

## <a name="input-types"></a>Types d’entrée

Les types d’entrée suivants sont pris en charge par l’encodeur d’écran de la version 9 lorsqu’il est utilisé en tant qu’objet de média DirectX (DMO).

-   MEDIASUBTYPE \_ Rgb24
-   MEDIASUBTYPE \_ RGB32
-   MEDIASUBTYPE \_ ARGB32
-   MEDIASUBTYPE \_ RGB565
-   MEDIASUBTYPE \_ RGB555
-   MEDIASUBTYPE \_ RGB8

Les types d’entrée suivants sont pris en charge par l’encodeur d’écran de la version 9 lorsqu’il est utilisé en tant que Media Foundation Transform (MFT).

-   MFVideoFormat \_ Rgb24
-   MFVideoFormat \_ RGB32
-   MFVideoFormat \_ ARGB32
-   MFVideoFormat \_ RGB565
-   MFVideoFormat \_ RGB555
-   MFVideoFormat \_ RGB8

## <a name="output-types"></a>Types de sortie

le code à quatre caractères (FOURCC) pour Windows Media Video contenu encodé à l’écran Version 9 est « MSS2 ».

Les types de sortie suivants sont pris en charge par l’encodeur d’écran de la version 9.

-   MEDIASUBTYPE \_ MSS2

## <a name="encoder-properties"></a>Propriétés de l’encodeur

l’encodeur d’écran Windows Media Video 9 prend en charge les propriétés suivantes.



<table>
<thead>
<tr class="header">
<th>Propriété</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="mfpkey-asfoverheadperframeproperty.md">MFPKEY_ASFOVERHEADPERFRAME</a></td>
<td>Spécifie la surcharge, en octets par paquet, requise pour le conteneur utilisé pour stocker le contenu compressé.<br/> <dl> Windows XP et versions ultérieures.<br />
En écriture seule.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-bavgproperty.md">MFPKEY_BAVG</a></td>
<td>Spécifie la fenêtre de mémoire tampon, en millisecondes, d’un flux de vitesse de transmission variable (VBR) contraints à sa vitesse de transmission moyenne (spécifiée par <a href="mfpkey-ravgproperty.md">MFPKEY_RAVG</a>).<br/> <dl> Windows XP et versions ultérieures.<br />
En lecture/écriture.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-bmaxproperty.md">MFPKEY_BMAX</a></td>
<td>Spécifie la fenêtre de mémoire tampon, en millisecondes, d’un flux de vitesse de transmission variable (VBR) avec restriction à sa vitesse de transmission maximale (spécifiée par <a href="mfpkey-rmaxproperty.md">MFPKEY_RMAX</a>).<br/> <dl> Windows XP et versions ultérieures.<br />
En lecture/écriture.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-bufferfullnessinfirstbyteproperty.md">MFPKEY_BUFFERFULLNESSINFIRSTBYTE</a></td>
<td>Spécifie si le flux de bits vidéo encodé contient une valeur de saturation de la mémoire tampon avec chaque image clé.<br/> <dl> Windows XP et versions ultérieures.<br />
Lecture seule.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-codedframesproperty.md">MFPKEY_CODEDFRAMES</a></td>
<td>Spécifie le nombre de trames vidéo encodées par le codec.<br/> <dl> Windows XP et versions ultérieures.<br />
Lecture seule.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-codednonzeroframesproperty.md">MFPKEY_CODEDNONZEROFRAMES</a></td>
<td>Spécifie le nombre de trames vidéo encodées par le codec qui contiennent réellement des données.<br/> <dl> Windows XP et versions ultérieures.<br />
Lecture seule.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-complexityproperty.md">MFPKEY_COMPLEXITY</a></td>
<td>Cette propriété est remplacée par <a href="mfpkey-complexityexproperty.md">MFPKEY_COMPLEXITYEX</a>.<br/></td>
</tr>
<tr class="even">
<td><a href="mfpkey-complexityexproperty.md">MFPKEY_COMPLEXITYEX</a></td>
<td>Spécifie la complexité de l’algorithme d’encodeur.<br/> <dl> Windows Vista et versions ultérieures.<br />
En écriture seule.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-crispproperty.md">MFPKEY_CRISP</a></td>
<td>Spécifie une représentation numérique du compromis entre le lissage du mouvement et la qualité de l’image dans la sortie du codec.<br/> <dl> Windows XP et versions ultérieures.<br />
En écriture seule.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-droppedframesproperty.md">MFPKEY_DROPPEDFRAMES</a></td>
<td>Spécifie le nombre de trames vidéo supprimées pendant l’encodage.<br/> <dl> Windows XP et versions ultérieures.<br />
Lecture seule.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-endofpassproperty.md">MFPKEY_ENDOFPASS</a></td>
<td>Spécifie la fin d’une passe d’encodage.<br/> <dl> Windows XP et versions ultérieures.<br />
En écriture seule.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-fourccproperty.md">MFPKEY_FOURCC</a></td>
<td>Spécifie le FOURCC qui identifie l’encodeur que vous souhaitez utiliser.<br/> <dl> Windows XP et versions ultérieures.<br />
En écriture seule.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-keydistproperty.md">MFPKEY_KEYDIST</a></td>
<td>Spécifie la durée maximale, en millisecondes, entre les images clés de la sortie du codec.<br/> <dl> Windows XP et versions ultérieures.<br />
En écriture seule.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-liveencodeproperty.md">MFPKEY_LIVEENCODE</a></td>
<td>Obsolète.<br/></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-passesrecommendedproperty.md">MFPKEY_PASSESRECOMMENDED</a></td>
<td>Spécifie le nombre maximal de passes prises en charge par le codec.<br/> <dl> Windows XP et versions ultérieures.<br />
Lecture seule.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-passesusedproperty.md">MFPKEY_PASSESUSED</a></td>
<td>Windows XP et versions ultérieures. En lecture/écriture.<br/> Spécifie le nombre de passes qui seront utilisées par le codec pour encoder le contenu.<br/> <dl> Windows XP et versions ultérieures.<br />
En lecture/écriture.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-qpperframeproperty.md">MFPKEY_QPPERFRAME</a></td>
<td>Spécifie QP. Les valeurs possibles sont 1,0 à 31,0.<br/> <dl> Windows Vista et versions ultérieures.<br />
En écriture seule.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-ravgproperty.md">MFPKEY_RAVG</a></td>
<td>Spécifie la vitesse de transmission moyenne, en bits par seconde, utilisée pour l’encodage VBR (variable-bit-rate) à 2 passes.<br/> <dl> Windows XP et versions ultérieures.<br />
En lecture/écriture.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-rmaxproperty.md">MFPKEY_RMAX</a></td>
<td>Spécifie le taux de bits de pointe, en bits par seconde, utilisé pour l’encodage VBR (variable-bit-rate) avec restriction de 2 passes.<br/> <dl> Windows XP et versions ultérieures.<br />
En lecture/écriture.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-totalframesproperty.md">MFPKEY_TOTALFRAMES</a></td>
<td>Spécifie le nombre de trames vidéo transmises à l’encodeur pendant le processus d’encodage.<br/> <dl> Windows XP et versions ultérieures.<br />
Lecture seule.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-vbrenabledproperty.md">MFPKEY_VBRENABLED</a></td>
<td>Spécifie si le codec utilise l’encodage VBR (variable-bit-rate).<br/> <dl> Windows XP et versions ultérieures.<br />
En lecture/écriture.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-vbrqualityproperty.md">MFPKEY_VBRQUALITY</a></td>
<td>Spécifie le niveau de qualité réel pour l’encodage VBR (variable-bit-rate) basé sur la qualité (1 passe).<br/> <dl> Windows XP et versions ultérieures.<br />
En écriture seule.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-videowindowproperty.md">MFPKEY_VIDEOWINDOW</a></td>
<td>Quantité de contenu, en millisecondes, qui peut tenir dans la mémoire tampon du modèle.<br/> <dl> Windows XP et versions ultérieures,<br />
En écriture seule.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-zerobyteframesproperty.md">MFPKEY_ZEROBYTEFRAMES</a></td>
<td>Spécifie le nombre de trames vidéo qui ont été ignorées, car il s’agissait de doublons de trames précédentes.<br/> <dl> Windows XP et versions ultérieures.<br />
Lecture seule.<br />
</dl></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a>Remarques

un objet d’encodeur d’écran expose l’interface **IMediaObject** afin que l’objet puisse être utilisé en tant qu’objet de média DirectX (DMO) et expose l’interface **IMFTransform** afin que l’objet puisse être utilisé en tant que transformation de Media Foundation (MFT).

un encodeur d’écran se comporte comme un DMO ou une table MFT selon les interfaces que vous obtenez et la version de Windows en cours d’exécution. le tableau suivant indique les conditions sous lesquelles un encodeur d’écran se comporte comme un DMO ou une table MFT.



| Système d’exploitation            | Comportement de l’encodeur                                                                                                                                    |
|-----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| Windows XP                  | un encodeur d’écran de média Windows se comporte toujours comme un DMO.                                                                                             |
| Windows Vista et Windows 7 | par défaut, un encodeur d’écran de support Windows se comporte comme un DMO. Si vous obtenez une interface **IMFTransform** sur un encodeur d’écran, elle se comporte comme une table MFT. |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|-----------------------------------------------------------------------------------------|
| Client<br/> | Windows XP, Windows Vista ou Windows 7<br/>                                       |
| En-tête<br/> | <dl> <dt>Wmcodecdsp. h</dt> </dl> |
| DLL<br/>    | <dl> <dt>Wmvsencd.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Objets codec](codecobjects.md)
</dt> <dt>

[Implémentation du codec](codecimplementation.md)
</dt> <dt>

[utilisation du Codec d’écran Windows Media Video 9](usingthewindowsmediavideo9screencodec.md)
</dt> <dt>

[Windows Décodeur d’écran Media Video 9](windowsmediavideo9screendecoder.md)
</dt> </dl>

 

 




