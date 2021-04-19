---
description: L’encodeur Windows Media Video 9 encode les flux vidéo.
ms.assetid: 1d0a41bc-7f7c-4e25-860c-1108ab292951
title: Encodeur Windows Media Video 9 (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c36ee5823c585d60ee74e75f99e8ec9b4d91f5cc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537833"
---
# <a name="windows-media-video-9-encoder"></a>Encodeur Windows Media Video 9

L’encodeur Windows Media Video 9 encode les flux vidéo. L’encodeur prend en charge les quatre catégories de sortie encodées suivantes.

-   Profil simple Windows Media Video 9
-   Profil principal du Windows Media Video 9
-   Profil avancé Windows Media Video 9
-   Image Windows Media Video 9,1

## <a name="class-identifier"></a>Identificateur de classe

L’identificateur de classe (CLSID) de l’encodeur de Windows Media Video est représenté par la constante **CLSID \_ CWMV9EncMediaObject**. Vous pouvez créer une instance de l’encodeur vidéo en appelant **CoCreateInstance**.

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

Le tableau suivant présente les codes à quatre caractères (FOURCCs) qui correspondent aux catégories de sortie encodée.



| Category                               | FOURCC                                   |
|----------------------------------------|------------------------------------------|
| Profil simple Windows Media Video 9   | "WMV3"                                   |
| Profil principal du Windows Media Video 9     | "WMV3"                                   |
| Profil avancé Windows Media Video 9 | "WVC1"                                   |
| Image Windows Media Video 9,1          | « WMVP » pour 9,1, « WVP2 » pour 9,1 version 2 |



 

Pour faire la distinction entre profil simple et profil principal, définissez la propriété [**MFPKEY \_ DECODERCOMPLEXITYREQUESTED**](mfpkey-decodercomplexityrequestedproperty.md) .

## <a name="properties"></a>Propriétés

L’encodeur Windows Media Video 9 prend en charge les propriétés suivantes.



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
Profil simple, profil principal, profil avancé, image.<br />
En écriture seule.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-avgframerateproperty.md"><strong>MFPKEY_AVGFRAMERATE</strong></a></td>
<td>Spécifie la fréquence d’images moyenne du contenu vidéo, en images par seconde.<br/> <dl> Windows XP et versions ultérieures.<br />
Profil simple, profil principal, profil avancé, image.<br />
Lecture seule.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-bavgproperty.md"><strong>MFPKEY_BAVG</strong></a></td>
<td>Spécifie la fenêtre de mémoire tampon, en millisecondes, d’un flux de vitesse de transmission variable (VBR) contraints à sa vitesse de transmission moyenne (spécifiée par <a href="mfpkey-ravgproperty.md"><strong>MFPKEY_RAVG</strong></a>).<br/> <dl> Windows XP et versions ultérieures.<br />
Profil simple, profil principal, profil avancé.<br />
En lecture/écriture.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-bdeltaqpproperty.md"><strong>MFPKEY_BDELTAQP</strong></a></td>
<td>Spécifie l’augmentation Delta entre le quantificateur d’image du frame d’ancrage et le quantificateur d’image du cadre B.<br/> <dl> Windows XP et versions ultérieures.<br />
Profil principal, profil avancé.<br />
En écriture seule.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-bmaxproperty.md"><strong>MFPKEY_BMAX</strong></a></td>
<td>Spécifie la fenêtre de mémoire tampon, en millisecondes, d’un flux de vitesse de transmission variable (VBR) avec restriction à sa vitesse de transmission maximale (spécifiée par <a href="mfpkey-rmaxproperty.md"><strong>MFPKEY_RMAX</strong></a>).<br/> <dl> Windows XP et versions ultérieures.<br />
Profil simple, profil principal, profil avancé, image.<br />
En lecture/écriture.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-bufferfullnessinfirstbyteproperty.md"><strong>MFPKEY_BUFFERFULLNESSINFIRSTBYTE</strong></a></td>
<td>Spécifie si le flux de bits vidéo encodé contient une valeur de saturation de la mémoire tampon avec chaque image clé.<br/> <dl> Windows XP et versions ultérieures.<br />
Profil simple, profil principal, profil avancé.<br />
Lecture seule.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-closedentrypointproperty.md"><strong>MFPKEY_CLOSEDENTRYPOINT</strong></a></td>
<td>Spécifie le modèle d’encodage à utiliser au début d’un groupe d’images.<br/> <dl> Windows Vista et versions ultérieures.<br />
Profil simple, profil principal, profil avancé, image.<br />
En écriture seule.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-codedframesproperty.md"><strong>MFPKEY_CODEDFRAMES</strong></a></td>
<td>Spécifie le nombre de trames vidéo encodées par le codec.<br/> <dl> Windows XP et versions ultérieures.<br />
Profil simple, profil principal, profil avancé.<br />
Lecture seule.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-codednonzeroframesproperty.md"><strong>MFPKEY_CODEDNONZEROFRAMES</strong></a></td>
<td>Spécifie le nombre de trames vidéo encodées par le codec qui contiennent réellement des données.<br/> <dl> Windows XP et versions ultérieures.<br />
Profil simple, profil principal, profil avancé.<br />
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
Profil simple, profil principal. Profil avancé.<br />
En écriture seule.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-compressionoptimizationtypeproperty.md"><strong>MFPKEY_COMPRESSIONOPTIMIZATIONTYPE</strong></a></td>
<td>Spécifie le type d’optimisation à utiliser pour le codec de profil avancé Windows Media Video 9.<br/> <dl> Windows XP et versions ultérieures.<br />
Profil simple, profil principal, profil avancé.<br />
Écriture.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-crispproperty.md"><strong>MFPKEY_CRISP</strong></a></td>
<td>Spécifie une représentation numérique du compromis entre le lissage du mouvement et la qualité de l’image dans la sortie du codec.<br/> <dl> Windows XP et versions ultérieures.<br />
Profil simple, profil principal, profil avancé.<br />
En écriture seule.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-datarateproperty.md"><strong>MFPKEY_DATARATE</strong></a></td>
<td>Non utilisé.<br/></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-decodercomplexityprofileproperty.md"><strong>MFPKEY_DECODERCOMPLEXITYPROFILE</strong></a></td>
<td>Spécifie le modèle de conformité de périphérique auquel le contenu encodé est conforme.<br/> <dl> Windows XP et versions ultérieures.<br />
Profil simple, profil principal, profil avancé, image.<br />
Lecture seule.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-decodercomplexityrequestedproperty.md"><strong>MFPKEY_DECODERCOMPLEXITYREQUESTED</strong></a></td>
<td>Spécifie le modèle de conformité de périphérique que vous souhaitez utiliser pour l’encodage vidéo.<br/> <dl> Windows XP et versions ultérieures.<br />
Profil simple, profil principal, profil avancé.<br />
En écriture seule.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-deltamvrangeindexproperty.md"><strong>MFPKEY_DELTAMVRANGEINDEX</strong></a></td>
<td>Spécifie la méthode utilisée pour encoder les informations de vecteur de mouvement.<br/> <dl> Windows XP et versions ultérieures.<br />
Profil simple, profil principal, profil avancé.<br />
En écriture seule.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-denoiseoptionproperty.md"><strong>MFPKEY_DENOISEOPTION</strong></a></td>
<td>Spécifie si le codec doit utiliser le filtre de bruit lors de l’encodage.<br/> <dl> Windows XP et versions ultérieures.<br />
Profil simple, profil principal, profil avancé.<br />
En écriture seule.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-desired-vbrqualityproperty.md"><strong>MFPKEY_DESIRED_VBRQUALITY</strong></a></td>
<td>Spécifie le niveau de qualité souhaité pour l’encodage VBR (variable-bit-rate) basé sur la qualité (1 passe).<br/> <dl> Windows Vista et versions ultérieures.<br />
Profil simple, profil principal, profil avancé, image.<br />
En écriture seule.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-droppedframesproperty.md"><strong>MFPKEY_DROPPEDFRAMES</strong></a></td>
<td>Spécifie le nombre de trames vidéo supprimées pendant l’encodage.<br/> <dl> Windows XP et versions ultérieures.<br />
Profil simple, profil principal, profil avancé.<br />
Lecture seule.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-endofpassproperty.md"><strong>MFPKEY_ENDOFPASS</strong></a></td>
<td>Spécifie la fin d’une passe d’encodage.<br/> <dl> Windows XP et versions ultérieures.<br />
Profil simple, profil principal, profil avancé.<br />
En écriture seule.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-forceframeheightproperty.md"><strong>MFPKEY_FORCEFRAMEHEIGHT</strong></a></td>
<td>Spécifie une hauteur de frame intermédiaire pour la vidéo encodée.<br/> <dl> Windows XP et versions ultérieures.<br />
Profil avancé.<br />
En écriture seule.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-forceframewidthproperty.md"><strong>MFPKEY_FORCEFRAMEWIDTH</strong></a></td>
<td>Spécifie une largeur de frame intermédiaire pour la vidéo encodée.<br/> <dl> Windows XP et versions ultérieures.<br />
Profil avancé.<br />
En écriture seule.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-forcemediansettingproperty.md"><strong>MFPKEY_FORCEMEDIANSETTING</strong></a></td>
<td>Spécifie si le codec doit utiliser le filtrage médian pendant l’encodage.<br/> <dl> Windows XP et versions ultérieures.<br />
Profil simple, profil principal, profil avancé.<br />
En écriture seule.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-fourccproperty.md"><strong>MFPKEY_FOURCC</strong></a></td>
<td>Spécifie le FOURCC qui identifie l’encodeur que vous souhaitez utiliser.<br/> <dl> Windows XP et versions ultérieures.<br />
Profil simple, profil principal, profil avancé, image.<br />
En écriture seule.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-framecountproperty.md"><strong>MFPKEY_FRAMECOUNT</strong></a></td>
<td>Obsolète.<br/></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-fullframerateproperty.md"><strong>MFPKEY_FULLFRAMERATE</strong></a></td>
<td>Spécifie si l’encodeur est autorisé à déposer des frames.<br/> <dl> Windows XP et versions ultérieures.<br />
Profil simple, profil principal, profil avancé, image.<br />
En écriture seule.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-interlacedcodingenabledproperty.md"><strong>MFPKEY_INTERLACEDCODINGENABLED</strong></a></td>
<td>Spécifie si la sortie du codec sera entrelacée.<br/> <dl> Windows XP et versions ultérieures.<br />
Profil avancé.<br />
En écriture seule.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-keydistproperty.md"><strong>MFPKEY_KEYDIST</strong></a></td>
<td>Spécifie la durée maximale, en millisecondes, entre les images clés de la sortie du codec.<br/> <dl> Windows XP et versions ultérieures.<br />
Profil simple, profil principal, profil avancé, image.<br />
En écriture seule.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-liveencodeproperty.md"><strong>MFPKEY_LIVEENCODE</strong></a></td>
<td>Non utilisé.<br/></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-lookaheadproperty.md"><strong>MFPKEY_LOOKAHEAD</strong></a></td>
<td>Spécifie le nombre de frames après le frame actuel que le codec évaluera avant d’encoder le frame actuel.<br/> <dl> Windows XP et versions ultérieures.<br />
Profil simple, profil principal, profil avancé.<br />
En écriture seule.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-loopfilterproperty.md"><strong>MFPKEY_LOOPFILTER</strong></a></td>
<td>Spécifie si le codec doit utiliser le filtre de déblocage en boucle lors de l’encodage.<br/> <dl> Windows XP et versions ultérieures.<br />
Profil principal, profil avancé.<br />
En écriture seule.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-macroblockmodecostmethodproperty.md"><strong>MFPKEY_MACROBLOCKMODECOSTMETHOD</strong></a></td>
<td>Spécifie la méthode de coût utilisée par le codec pour déterminer le mode bloc macro à utiliser.<br/> <dl> Windows XP et versions ultérieures.<br />
Profil simple, profil principal, profil avancé.<br />
En écriture seule.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-motionmatchmethodproperty.md"><strong>MFPKEY_MOTIONMATCHMETHOD</strong></a></td>
<td>Spécifie la méthode à utiliser pour la correspondance de mouvement.<br/> <dl> Windows XP et versions ultérieures.<br />
Profil simple, profil principal, profil avancé.<br />
En écriture seule.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-motionsearchlevelproperty.md"><strong>MFPKEY_MOTIONSEARCHLEVEL</strong></a></td>
<td>Spécifie les types d’informations vidéo utilisées dans les opérations de recherche de mouvement.<br/> <dl> Windows XP et versions ultérieures.<br />
Profil simple, profil principal, profil avancé.<br />
En écriture seule.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-motionsearchrangeproperty.md"><strong>MFPKEY_MOTIONSEARCHRANGE</strong></a></td>
<td>Spécifie la plage utilisée dans les recherches de mouvement.<br/> <dl> Windows XP et versions ultérieures.<br />
Profil principal, profil avancé.<br />
En écriture seule.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-noiseedgeremovalproperty.md"><strong>MFPKEY_NOISEEDGEREMOVAL</strong></a></td>
<td>Spécifie si le codec doit tenter de détecter les bords bruyants du cadre et les supprimer.<br/> <dl> Windows XP et versions ultérieures.<br />
Profil simple, profil principal, profil avancé.<br />
En écriture seule.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-numbframesproperty.md"><strong>MFPKEY_NUMBFRAMES</strong></a></td>
<td>Spécifie le nombre de frames prédictifs bidirectionnels (frames B).<br/> <dl> Windows XP et versions ultérieures.<br />
Profil principal, profil avancé.<br />
En écriture seule.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-numthreadsproperty.md"><strong>MFPKEY_NUMTHREADS</strong></a></td>
<td>Spécifie le nombre de threads que le codec doit utiliser pour l’encodage.<br/> <dl> Windows XP et versions ultérieures.<br />
Profil simple, profil principal, profil avancé.<br />
En écriture seule.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-passesrecommendedproperty.md"><strong>MFPKEY_PASSESRECOMMENDED</strong></a></td>
<td>Spécifie le nombre maximal de passes prises en charge par le codec.<br/> <dl> Windows XP et versions ultérieures.<br />
Profil simple, profil principal, profil avancé, image.<br />
Lecture seule.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-passesusedproperty.md"><strong>MFPKEY_PASSESUSED</strong></a></td>
<td>Spécifie le nombre de passes qui seront utilisées par le codec pour encoder le contenu.<br/> <dl> Windows XP et versions ultérieures.<br />
Profil simple, profil principal, profil avancé, image.<br />
En lecture/écriture.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-perceptualoptlevelproperty.md"><strong>MFPKEY_PERCEPTUALOPTLEVEL</strong></a></td>
<td>Spécifie si le codec doit utiliser l’optimisation de perception conservatrice lors de l’encodage.<br/> <dl> Windows XP et versions ultérieures.<br />
Profil principal, profil avancé.<br />
En écriture seule.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-producedummyframesproperty.md"><strong>MFPKEY_PRODUCEDUMMYFRAMES</strong></a></td>
<td>Spécifie si l’encodeur génère des entrées de frame factice dans le flux binaire pour les frames en double.<br/> <dl> Windows XP et versions ultérieures.<br />
Profil simple, profil principal, profil avancé.<br />
En écriture seule.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-qpperframeproperty.md"><strong>MFPKEY_QPPERFRAME</strong></a></td>
<td>Spécifie QP.<br/> <dl> Windows Vista et versions ultérieures.<br />
Profil simple, profil principal, profil avancé, image.<br />
En écriture seule.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-rangereduxproperty.md"><strong>MFPKEY_RANGEREDUX</strong></a></td>
<td>Spécifie le degré auquel le codec doit réduire la plage de couleurs effectives de la vidéo.<br/> <dl> Windows XP et versions ultérieures.<br />
Profil avancé.<br />
En écriture seule.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-ravgproperty.md"><strong>MFPKEY_RAVG</strong></a></td>
<td>Spécifie la vitesse de transmission moyenne, en bits par seconde, utilisée pour l’encodage VBR (variable-bit-rate) à 2 passes.<br/> <dl> Windows XP et versions ultérieures.<br />
Profil simple, profil principal, profil avancé.<br />
En lecture/écriture.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-rdsubpixelsearchproperty.md"><strong>MFPKEY_RDSUBPIXELSEARCH</strong></a></td>
<td>Spécifie si l’encodeur utilise la recherche de MV sous-pixel basée sur les services Bureau à distance. <br/> <dl> Windows XP et versions ultérieures.<br />
Profil simple, profil principal, profil avancé, image.<br />
En écriture seule.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-reencendbuffersizeproperty.md"><strong>MFPKEY_REENCENDBUFFERSIZE</strong></a></td>
<td>Pour le ré-encodage de segment, spécifie la taille de la mémoire tampon.<br/> <dl> Windows Vista et versions ultérieures.<br />
Profil simple, profil principal, profil avancé, image.<br />
En écriture seule.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-reencdurationproperty.md"><strong>MFPKEY_REENCDURATION</strong></a></td>
<td>Pour le ré-encodage de segment, spécifie la durée du segment à recoder.<br/> <dl> Windows Vista et versions ultérieures.<br />
Profil simple, profil principal, profil avancé, image.<br />
En écriture seule.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-reencqprefproperty.md"><strong>MFPKEY_REENCQPREF</strong></a></td>
<td>Pour le ré-encodage de segment, spécifie le quantificateur du frame avant le segment de départ.<br/> <dl> Windows Vista et versions ultérieures.<br />
Profil simple, profil principal, profil avancé, image.<br />
En écriture seule.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-reencstartbuffersizeproperty.md"><strong>MFPKEY_REENCSTARTBUFFERSIZE</strong></a></td>
<td>Pour le ré-encodage de segment, spécifie la saturation de la mémoire tampon de départ.<br/> <dl> Windows Vista et versions ultérieures.<br />
Profil simple, profil principal, profil avancé, image.<br />
En écriture seule.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-rmaxproperty.md"><strong>MFPKEY_RMAX</strong></a></td>
<td>Spécifie le taux de bits de pointe, en bits par seconde, utilisé pour le VBR (variable-bit-bit-rate) avec une limite de 2 passes.<br/> <dl> Windows XP et versions ultérieures.<br />
Profil simple, profil principal, profil avancé.<br />
En lecture/écriture.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-totalframesproperty.md"><strong>MFPKEY_TOTALFRAMES</strong></a></td>
<td>Spécifie le nombre de trames vidéo transmises à l’encodeur pendant le processus d’encodage.<br/> <dl> Windows XP et versions ultérieures.<br />
Profil simple, profil principal, profil avancé, image.<br />
Lecture seule.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-vbrenabledproperty.md"><strong>MFPKEY_VBRENABLED</strong></a></td>
<td>Spécifie si le codec utilise l’encodage VBR (variable-bit-rate).<br/> <dl> Windows XP et versions ultérieures.<br />
Profil simple, profil principal, profil avancé, image.<br />
En lecture/écriture.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-vbrqualityproperty.md"><strong>MFPKEY_VBRQUALITY</strong></a></td>
<td>Spécifie le niveau de qualité réel pour l’encodage VBR (variable-bit-rate) basé sur la qualité (1 passe).<br/> <dl> Windows XP et versions ultérieures.<br />
Profil simple, profil principal, profil avancé.<br />
En écriture seule.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-videoscalingproperty.md"><strong>MFPKEY_VIDEOSCALING</strong></a></td>
<td>Spécifie si le codec utilise l’optimisation de la mise à l’échelle vidéo.<br/> <dl> Windows XP et versions ultérieures.<br />
Profil simple, profil principal, profil avancé.<br />
En écriture seule.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-videowindowproperty.md"><strong>MFPKEY_VIDEOWINDOW</strong></a></td>
<td>Spécifie la quantité de contenu, en millisecondes, qui peut tenir dans la mémoire tampon du modèle.<br/> <dl> Windows XP et versions ultérieures.<br />
Profil avancé.<br />
En écriture seule.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-volheaderforreencodeproperty.md"><strong>MFPKEY_VOLHEADERFORREENCODE</strong></a></td>
<td>Pour le ré-encodage de segment, spécifie les données privées du codec du fichier qui est à nouveau codé.<br/> <dl> Windows Vista et versions ultérieures.<br />
Profil simple, profil principal, profil avancé, image.<br />
En écriture seule.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-vtypeproperty.md"><strong>MFPKEY_VTYPE</strong></a></td>
<td>Spécifie le type de logique qui sera utilisé par le codec pour détecter la vidéo source entrelacée.<br/> <dl> Windows XP et versions ultérieures.<br />
Profil avancé.<br />
En écriture seule.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-zerobyteframesproperty.md"><strong>MFPKEY_ZEROBYTEFRAMES</strong></a></td>
<td>Spécifie le nombre de trames vidéo qui ont été ignorées, car il s’agissait de doublons de trames précédentes.<br/> <dl> Windows XP et versions ultérieures.<br />
Profil simple, profil principal, profil avancé.<br />
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
| DLL<br/>    | <dl> <dt>Wmvencod.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Objets codec](codecobjects.md)
</dt> <dt>

[Implémentation du codec](codecimplementation.md)
</dt> </dl>

 

 
