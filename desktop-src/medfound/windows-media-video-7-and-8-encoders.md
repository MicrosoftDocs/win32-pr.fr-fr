---
description: L’encodeur Windows Media Video 7/8 implémente les versions précédentes de l’encodeur Windows Media Video.
ms.assetid: c4165614-b9ec-4216-b36c-f57bc05e3a8e
title: Windows Media Video encodeur 7/8 (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: be5467d02681ef319a508f6f6581e1f3c0191950
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106543332"
---
# <a name="windows-media-video-78-encoder"></a>Windows Media Video encodeur 7/8

L’encodeur Windows Media Video 7/8 implémente les versions précédentes de l’encodeur Windows Media Video.

## <a name="class-identifier"></a>Identificateur de classe

L’identificateur de classe (CLSID) de l’encodeur Windows Media Video 7/8 est **CLSID \_ CWMVXEncMediaObject**. Vous pouvez créer une instance de l’encodeur en appelant **CoCreateInstance**.

## <a name="interfaces"></a>Interfaces

Un objet encodeur vidéo expose l’interface [**IMediaObject**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject) afin que l’objet puisse être utilisé en tant qu’objet de média DirectX (DMO) et expose l’interface [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) afin que l’objet puisse être utilisé en tant que transformation de Media Foundation (MFT).

Un encodeur vidéo se comporte comme un DMO ou une table MFT en fonction des interfaces que vous obtenez et de la version de Windows en cours d’exécution. Le tableau suivant présente les conditions dans lesquelles un encodeur vidéo se comporte comme un DMO ou une table MFT.



| Système d’exploitation            | Comportement de l’encodeur                                                                                                                                                      |
|-----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Windows XP                  | Un encodeur vidéo Windows Media se comporte toujours comme un DMO.                                                                                                                |
| Windows Vista et Windows 7 | Par défaut, un encodeur vidéo Windows Media se comporte comme un DMO. Si vous obtenez une interface [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) sur un encodeur vidéo, elle se comporte comme une table MFT. |



 

## <a name="input-formats"></a>Formats d’entrée

L’encodeur Windows Media Video prend en charge les sous-types de médias d’entrée suivants lorsqu’il agit en tant que DMO.

-   MEDIASUBTYPE \_ IYUV
-   MEDIASUBTYPE \_ I420
-   MEDIASUBTYPE \_ YV12
-   MEDIASUBTYPE \_ NV11
-   MEDIASUBTYPE \_ NV12
-   MEDIASUBTYPE \_ YUY2
-   MEDIASUBTYPE \_ UYVY
-   MEDIASUBTYPE \_ YVYU
-   MEDIASUBTYPE \_ RGB32
-   MEDIASUBTYPE \_ Rgb24
-   MEDIASUBTYPE \_ RGB565
-   MEDIASUBTYPE \_ RGB555
-   MEDIASUBTYPE \_ RGB8
-   photomotion MEDIASUBTYPE \_

L’encodeur Windows Media Video prend en charge les sous-types de médias d’entrée suivants lorsqu’il joue le rôle de MFT.

-   MFVideoFormat \_ IYUV
-   MFVideoFormat \_ I420
-   MFVideoFormat \_ YV12
-   MFVideoFormat \_ NV11
-   MFVideoFormat \_ NV12
-   MFVideoFormat \_ YUY2
-   MFVideoFormat \_ UYVY
-   MFVideoFormat \_ YVYU
-   MFVideoFormat \_ RGB32
-   MFVideoFormat \_ Rgb24
-   MFVideoFormat \_ RGB565
-   MFVideoFormat \_ RGB555
-   MFVideoFormat \_ RGB8
-   photomotion MEDIASUBTYPE \_

## <a name="output-formats"></a>Formats de sortie

Le tableau suivant présente les codes à quatre caractères (FOURCCs) pour les types de sortie pris en charge par l’encodeur Windows Media Video 7/8.



| Category              | FOURCC |
|-----------------------|--------|
| Windows Media Video 7 | "WMV1" |
| Windows Media Video 8 | "WMV2" |



 

## <a name="properties"></a>Propriétés

L’encodeur Windows Media Video 7/8 prend en charge les propriétés suivantes.



<table>
<thead>
<tr class="header">
<th>Propriété</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="mfpkey-asfoverheadperframeproperty.md"><strong>MFPKEY_ASFOVERHEADPERFRAME</strong></a></td>
<td>Spécifie la surcharge, en octets par paquet, requise pour le conteneur utilisé pour stocker le contenu compressé.<br/> <dl> Windows XP et versions ultérieures.<br />
En écriture seule.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-avgframerateproperty.md"><strong>MFPKEY_AVGFRAMERATE</strong></a></td>
<td>Spécifie la fréquence d’images moyenne du contenu vidéo, en images par seconde.<br/> <dl> Windows XP et versions ultérieures.<br />
Lecture seule.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-bavgproperty.md"><strong>MFPKEY_BAVG</strong></a></td>
<td>Spécifie la fenêtre de mémoire tampon, en millisecondes, d’un flux de vitesse de transmission variable (VBR) contraints à sa vitesse de transmission moyenne (spécifiée par <a href="mfpkey-ravgproperty.md"><strong>MFPKEY_RAVG</strong></a>).<br/> <dl> Windows XP et versions ultérieures.<br />
En lecture/écriture.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-bmaxproperty.md"><strong>MFPKEY_BMAX</strong></a></td>
<td>Spécifie la fenêtre de mémoire tampon, en millisecondes, d’un flux de vitesse de transmission variable (VBR) avec restriction à sa vitesse de transmission maximale (spécifiée par <a href="mfpkey-rmaxproperty.md"><strong>MFPKEY_RMAX</strong></a>).<br/> <dl> Windows XP et versions ultérieures.<br />
En lecture/écriture.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-bufferfullnessinfirstbyteproperty.md"><strong>MFPKEY_BUFFERFULLNESSINFIRSTBYTE</strong></a></td>
<td>Spécifie si le flux de bits vidéo encodé contient une valeur de saturation de la mémoire tampon avec chaque image clé.<br/> <dl> Windows XP et versions ultérieures.<br />
Lecture seule.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-codedframesproperty.md"><strong>MFPKEY_CODEDFRAMES</strong></a></td>
<td>Spécifie le nombre de trames vidéo encodées par le codec.<br/> <dl> Windows XP et versions ultérieures.<br />
Lecture seule.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-codednonzeroframesproperty.md"><strong>MFPKEY_CODEDNONZEROFRAMES</strong></a></td>
<td>Spécifie le nombre de trames vidéo encodées par le codec qui contiennent réellement des données.<br/> <dl> Windows XP et versions ultérieures.<br />
Lecture seule.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-complexityproperty.md"><strong>MFPKEY_COMPLEXITY</strong></a></td>
<td>Cette propriété est remplacée par <a href="mfpkey-complexityexproperty.md"><strong>MFPKEY_COMPLEXITYEX</strong></a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-complexityexproperty.md"><strong>MFPKEY_COMPLEXITYEX</strong></a></td>
<td>Spécifie la complexité de l’algorithme d’encodeur.<br/> <dl> Windows Vista et versions ultérieures.<br />
En écriture seule.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-crispproperty.md"><strong>MFPKEY_CRISP</strong></a></td>
<td>Spécifie une représentation numérique du compromis entre le lissage du mouvement et la qualité de l’image dans la sortie du codec.<br/> <dl> Windows XP et versions ultérieures.<br />
En écriture seule.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-decodercomplexityprofileproperty.md"><strong>MFPKEY_DECODERCOMPLEXITYPROFILE</strong></a></td>
<td>Spécifie le modèle de conformité de périphérique auquel le contenu encodé est conforme.<br/> <dl> Windows XP et versions ultérieures.<br />
Lecture seule.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-decodercomplexityrequestedproperty.md"><strong>MFPKEY_DECODERCOMPLEXITYREQUESTED</strong></a></td>
<td>Spécifie le modèle de conformité de périphérique que vous souhaitez utiliser pour l’encodage vidéo.<br/> <dl> Windows XP et versions ultérieures.<br />
En écriture seule.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-droppedframesproperty.md"><strong>MFPKEY_DROPPEDFRAMES</strong></a></td>
<td>Spécifie le nombre de trames vidéo supprimées pendant l’encodage.<br/> <dl> Windows XP et versions ultérieures.<br />
Lecture seule.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-endofpassproperty.md"><strong>MFPKEY_ENDOFPASS</strong></a></td>
<td>Spécifie la fin d’une passe d’encodage.<br/> <dl> Windows XP et versions ultérieures.<br />
En écriture seule.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-fourccproperty.md"><strong>MFPKEY_FOURCC</strong></a></td>
<td>Spécifie le FOURCC qui identifie l’encodeur que vous souhaitez utiliser.<br/> <dl> Windows XP et versions ultérieures.<br />
En écriture seule.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-interlacedcodingenabledproperty.md"><strong>MFPKEY_INTERLACEDCODINGENABLED</strong></a></td>
<td>Spécifie si la sortie du codec sera entrelacée.<br/> <dl> Windows XP et versions ultérieures.<br />
En écriture seule.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-keydistproperty.md"><strong>MFPKEY_KEYDIST</strong></a></td>
<td>Spécifie la durée maximale, en millisecondes, entre les images clés de la sortie du codec.<br/> <dl> Windows XP et versions ultérieures.<br />
En écriture seule.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-passesrecommendedproperty.md"><strong>MFPKEY_PASSESRECOMMENDED</strong></a></td>
<td>Spécifie le nombre maximal de passes prises en charge par le codec.<br/> <dl> Windows XP et versions ultérieures.<br />
Lecture seule.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-passesusedproperty.md"><strong>MFPKEY_PASSESUSED</strong></a></td>
<td>Spécifie le nombre de passes qui seront utilisées par le codec pour encoder le contenu.<br/> <dl> Windows XP et versions ultérieures.<br />
En lecture/écriture.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-producedummyframesproperty.md"><strong>MFPKEY_PRODUCEDUMMYFRAMES</strong></a></td>
<td>Spécifie si l’encodeur génère des entrées de frame factice dans le flux binaire pour les frames en double.<br/> <dl> Windows XP et versions ultérieures.<br />
En écriture seule.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-qpperframeproperty.md"><strong>MFPKEY_QPPERFRAME</strong></a></td>
<td>Spécifie QP.<br/> <dl> Windows Vista et versions ultérieures.<br />
En écriture seule.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-ravgproperty.md"><strong>MFPKEY_RAVG</strong></a></td>
<td>Spécifie la vitesse de transmission moyenne, en bits par seconde, utilisée pour l’encodage VBR (variable-bit-rate) à 2 passes.<br/> <dl> Windows XP et versions ultérieures.<br />
En lecture/écriture.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-rmaxproperty.md"><strong>MFPKEY_RMAX</strong></a></td>
<td>Spécifie le taux de bits de pointe, en bits par seconde, utilisé pour le VBR (variable-bit-bit-rate) avec une limite de 2 passes.<br/> <dl> Windows XP et versions ultérieures.<br />
En lecture/écriture.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-totalframesproperty.md"><strong>MFPKEY_TOTALFRAMES</strong></a></td>
<td>Spécifie le nombre de trames vidéo transmises à l’encodeur pendant le processus d’encodage.<br/> <dl> Windows XP et versions ultérieures.<br />
Lecture seule.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-vbrenabledproperty.md"><strong>MFPKEY_VBRENABLED</strong></a></td>
<td>Spécifie si le codec utilise l’encodage VBR (variable-bit-rate).<br/> <dl> Windows XP et versions ultérieures.<br />
En lecture/écriture.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-vbrqualityproperty.md"><strong>MFPKEY_VBRQUALITY</strong></a></td>
<td>Spécifie le niveau de qualité réel pour l’encodage VBR (variable-bit-rate) basé sur la qualité (1 passe).<br/> <dl> Windows XP et versions ultérieures.<br />
En écriture seule.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-videowindowproperty.md"><strong>MFPKEY_VIDEOWINDOW</strong></a></td>
<td>Spécifie la quantité de contenu, en millisecondes, qui peut tenir dans la mémoire tampon du modèle.<br/> <dl> Windows XP et versions ultérieures.<br />
En écriture seule.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-zerobyteframesproperty.md"><strong>MFPKEY_ZEROBYTEFRAMES</strong></a></td>
<td>Spécifie le nombre de trames vidéo qui ont été ignorées, car il s’agissait de doublons de trames précédentes.<br/> <dl> Windows XP et versions ultérieures.<br />
Lecture seule<br />
</dl></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|-----------------------------------------------------------------------------------------|
| Client<br/> | Windows XP, Windows Vista ou Windows 7<br/>                                       |
| En-tête<br/> | <dl> <dt>Wmcodecdsp. h</dt> </dl> |
| DLL<br/>    | <dl> <dt>Wmvxencd.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Objets codec](codecobjects.md)
</dt> <dt>

[Implémentation du codec](codecimplementation.md)
</dt> <dt>

[GUID de sous-type de vidéo](video-subtype-guids.md)
</dt> </dl>

 

 
