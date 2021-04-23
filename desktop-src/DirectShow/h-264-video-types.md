---
description: Types vidéo H. 264
ms.assetid: aa3166b2-6b04-44fa-bc9d-c8ff46f99201
title: Types vidéo H. 264
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 692a751e197e2e7bbb088b30dd2a3f5f199d56de
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909017"
---
# <a name="h264-video-types"></a>Types vidéo H. 264

Les sous-types de médias suivants sont définis pour la vidéo H. 264.



| Subtype                | FOURCC | Description                                                    |
|------------------------|--------|----------------------------------------------------------------|
| **MEDIASUBTYPE \_ AVC1** | 'AVC1' | Binaire H. 264 sans codes de démarrage.                           |
| **MEDIASUBTYPE \_ H264 –** | H264 – | Binaire H. 264 avec codes de démarrage.                              |
| **MEDIASUBTYPE \_ H264 –** | H264 – | Équivalent à **MEDIASUBTYPE \_ H264 –**, avec un FourCC différent. |
| **MEDIASUBTYPE \_ x264** | 'X264' | Équivalent à **MEDIASUBTYPE \_ H264 –**, avec un FourCC différent. |
| **MEDIASUBTYPE \_ x264** | 'x264' | Équivalent à **MEDIASUBTYPE \_ H264 –**, avec un FourCC différent. |



 

Ces GUID de sous-type sont déclarés dans wmcodecdsp. h.

La principale différence entre ces types de média réside dans la présence de codes de démarrage dans le flux binaire. Si le sous-type est **MEDIASUBTYPE \_ AVC1**, le flux binaire ne contient pas de codes de début.

### <a name="h264-bitstream-with-start-codes"></a>Binaire H. 264 avec codes de démarrage

H. 264 les séquences binaires transmises à l’air, ou contenues dans des flux de programme ou de transport MPEG-2, ou enregistrées sur HD-DVD, sont mises en forme comme décrit dans l’annexe B de l’ITU-T Rec. H. 264. Conformément à cette spécification, le flux binaire se compose d’une séquence d’unités de couche d’abstraction de réseau (NALUs), dont chacune est précédée d’un code de démarrage égal à 0x000001 ou 0x00000001.

Lorsque les codes de démarrage sont présents dans le flux binaire, le type de média suivant est utilisé :



| Étiquette | Valeur |
|-------------|---------------------------------------------------------------------------------------------------|
| Type principal  | **Vidéo de MEDIATYPE \_**                                                                              |
| Sous-types    | **MEDIASUBTYPE \_ H264 –**, **MEDIASUBTYPE \_ H264 –**, **MEDIASUBTYPE \_ x264** ou **MEDIASUBTYPE \_** x264 |
| Type de format | **Format \_ VideoInfo**, **format \_ VideoInfo2**, **format \_ mpeg2video** ou **GUID \_ null**          |



 

Si le type de format **est \_ null GUID**, aucune structure de format n’est présente.

Lorsque le flux binaire contient des codes de début, l’un des types de format répertoriés ici est suffisant, car le décodeur ne nécessite aucune information supplémentaire pour analyser le flux. Le flux de données contient déjà toutes les informations requises par le décodeur, et les codes de démarrage permettent au décodeur de localiser le début de chaque NALU.

Les sous-types suivants sont équivalents :

### <a name="h264-bitstream-without-start-codes"></a>Binaire H. 264 sans codes de démarrage

Le format de conteneur MP4 stocke les données H. 264 sans code de début. Au lieu de cela, chaque NALU est précédée d’un champ de longueur, ce qui donne la longueur du NALU en octets. La taille du champ de longueur peut varier, mais est généralement de 1, 2 ou 4 octets.

Lorsque les codes de début ne sont pas présents dans le flux binaire, le type de média suivant est utilisé.



| Étiquette | Valeur |
|-------------|------------------------|
| Type principal  | **Vidéo de MEDIATYPE \_**   |
| Subtype     | **MEDIASUBTYPE \_ AVC1** |
| Type de format | **FORMAT \_ mpeg2video** |



 

Le bloc de format est une structure [**MPEG2VIDEOINFO**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-mpeg2videoinfo) . Cette structure doit être remplie comme suit :

-   **HDR**: structure [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) qui décrit le flux binaire. Aucune table de couleurs n’est présente après la partie [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) de la structure, et **biClrUsed** doit être égal à zéro.
-   **dwStartTimeCode**: non utilisé. Définit la valeur zéro.
-   **cbSequenceHeader**: longueur du tableau **dwSequenceHeader** en octets.
-   **dwProfile**: spécifie le profil H. 264.
-   **dwLevel**: spécifie le niveau H. 264.
-   **dwFlags**: nombre d’octets utilisés pour le champ de longueur qui apparaît avant chaque **Nalu**. Le champ longueur indique la taille du NALU suivant en octets. Par exemple, si **dwFlags** est 4, chaque Nalu est précédé d’un champ de longueur de 4 octets. Les valeurs valides sont 1, 2 et 4.
-   **dwSequenceHeader**: tableau d’octets qui peut contenir un jeu de paramètres de séquence (SPS) et un jeu de paramètres d’image (PPS) NALUs.

Le conteneur MP4 peut contenir des jeux de paramètres de séquence (SPS) ou des jeux de paramètres d’image (PPS) en tant qu’unités NAL spéciales dans les en-têtes de fichier ou dans un flux distinct (distinct du flux vidéo). Lorsque le format est établi, le type de média peut spécifier des unités SPS et PPS NAL dans le tableau **dwSequenceHeader** . Si **cbSequenceHeader** est supérieur à zéro, **dwSequenceHeader** est le début d’un tableau d’octets contenant les NALUs SPS et PPS, délimités par les champs de longueur de 2 octets, tous dans l’ordre d’octet réseau (Big-endian). Il est possible d’avoir à la fois SPS et PPS, un seul de ces types, ou aucun. Le type réel de chaque NALU peut être déterminé en examinant le champ **\_ \_ type d’unité nal** du Nalu lui-même.

Lorsque ce type de média est utilisé, chaque exemple de support commence au début d’un NALU, et les unités NAL n’englobent pas les échantillons. Cela permet au décodeur de récupérer des données endommagées ou des échantillons supprimés.

 

 



