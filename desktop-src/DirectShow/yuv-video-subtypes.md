---
description: 'Les formats YUV sont classés en fonction des informations suivantes :'
ms.assetid: 452f017c-81ce-4be4-9962-4b9c1a9ce849
title: Sous-types vidéo YUV (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 312a3d9d8e12953353ed0f61fff67a05bf87426b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106544494"
---
# <a name="yuv-video-subtypes"></a>Sous-types vidéo YUV

Les formats YUV sont classés en fonction des informations suivantes :

**Formats compressés et formats planaires.** Dans un format compressé, les composants Y, U et V sont stockés dans un tableau unique. Les pixels sont organisés en groupes de macropixels, dont la disposition dépend du format. Dans un format Planar, les composants Y, U et V sont stockés séparément, sous la forme de trois plans.

**Échantillonnage Chroma.** Une notation appelée A :B: C notation est utilisée pour décrire la fréquence à laquelle vous et V sont échantillonnées par rapport à Y :

-   4:4:4 signifie aucun sous-échantillonnage des canaux Chroma.
-   4:2:2 signifie un sous-échantillonnage horizontal de 2:1, sans sous-échantillonnage vertical. Chaque ligne de numérisation contient quatre échantillons Y pour chacun des deux échantillons U ou V.
-   4:2:0 signifie le sous-échantillonnage horizontal 2:1 de 2:1, avec un sous-échantillonnage vertical.
-   4:1:1 signifie un sous-échantillonnage horizontal de 4:1, sans sous-échantillonnage vertical. Chaque ligne de numérisation contient quatre échantillons Y pour chaque exemple U ou V. 4:1:1 l’échantillonnage est moins courant que les autres formats, et n’est pas abordé en détail dans cet article.

**Bits par canal.** Les exemples de tailles les plus courants sont 8, 10 ou 16 bits par échantillon. Certains formats YUV sont en palette.

**Disposition de la mémoire.** Deux types de format YUV peuvent être identiques, mais ils utilisent des commandes différentes pour les échantillons Y, V et U en mémoire.

**Formats YUV recommandés**



| GUID               | Format | échantillonnage | Condensé ou planaire | Bits par canal |
|--------------------|--------|----------|------------------|------------------|
| MEDIASUBTYPE \_ AYUV | AYUV   | 4:4:4    | Riche           | 8                |
| MEDIASUBTYPE \_ YUY2 | YUY2   | 4:2:2    | Riche           | 8                |
| MEDIASUBTYPE \_ UYVY | UYVY   | 4:2:2    | Riche           | 8                |
| MEDIASUBTYPE \_ IMC1 | IMC1   | 4:2:0    | Planaire           | 8                |
| MEDIASUBTYPE \_ IMC3 | IMC2   | 4:2:0    | Planaire           | 8                |
| MEDIASUBTYPE \_ imc2 | IMC3   | 4:2:0    | Planaire           | 8                |
| MEDIASUBTYPE \_ IMC4 | IMC4   | 4:2:0    | Planaire           | 8                |
| MEDIASUBTYPE \_ YV12 | YV12   | 4:2:0    | Planaire           | 8                |
| MEDIASUBTYPE \_ NV12 | NV12   | 4:2:0    | Planaire           | 8                |



 

Pour obtenir une description de ces formats YUV pour le rendu vidéo sur Windows, consultez [formats YUV 8 bits recommandés pour le rendu vidéo](../medfound/recommended-8-bit-yuv-formats-for-video-rendering.md) .

**Autres types de format YUV**



| GUID               | Format                                                | échantillonnage                                                | Condensé ou planaire                                  | Bits par canal                             |
|--------------------|-------------------------------------------------------|---------------------------------------------------------|---------------------------------------------------|----------------------------------------------|
| MEDIASUBTYPE \_ I420 | I420                                                  | 4:2:0                                                   | Planaire                                            | 8                                            |
| MEDIASUBTYPE \_ IF09 | N'est plus pris en charge.<br/> Indeo YVU9<br/> | N'est plus pris en charge.<br/> Consultez la section Remarques.<br/> | N'est plus pris en charge.<br/> Planaire<br/> | N'est plus pris en charge.<br/> 8<br/> |
| MEDIASUBTYPE \_ IYUV | IYUV                                                  | 4:2:0                                                   | Planaire                                            | 8                                            |
| MEDIASUBTYPE \_ Y211 | Y211                                                  | Consultez la section Remarques.                                            | Riche                                            | 8                                            |
| MEDIASUBTYPE \_ Y411 | Y411                                                  | 4:1:1                                                   | Riche                                            | 8                                            |
| MEDIASUBTYPE \_ Y41P | Y41P                                                  | 4:1:1                                                   | Riche                                            | 8                                            |
| MEDIASUBTYPE \_ YVU9 | YVU9                                                  | Consultez la section Remarques.                                            | Planaire                                            | 8                                            |
| MEDIASUBTYPE \_ YVYU | YVYU                                                  | 4:2:2                                                   | Riche                                            | 8                                            |



 

-   I420 se compose d’un plan Y, suivi d’un plan U, suivi d’un plan V.
-   IYUV est identique à I420.
-   Y211 est un format compressé, dans lequel Y est échantillonné tous les 2 pixels horizontalement, et vous et V sont échantillonnés tous les 4 pixels horizontalement. Chaque macropixel est de 4 octets et contient 4 pixels. Il utilise l’ordre d’octet suivant :

    `Y0 U0 Y2 V0    Y4 U4 Y6 V4    Y8 U8 Y10 V8`

-   Y41P est un format compressé de 4:1:1. Il utilise l’ordre d’octet suivant :

    `U0 Y0 V0 Y1    U4 Y2 V4 Y3    Y4 Y5 Y6 Y7`

-   YVU9 est un format Planar, dans lequel vous et V sont échantillonnés tous les 4 pixels horizontalement et verticalement (parfois appelés 16:1:1). Le plan V apparaît avant le plan U.
-   Le format Indeo YVU9 (MEDIASUBTYPE \_ IF09) est une variante de YVU9 avec des informations supplémentaires sur l’image Delta après le plan U. Le codec Indeo n’est plus pris en charge dans Windows.
-   YVYU est similaire à UYVY avec un ordre d’octet différent : `Y0 V0 Y1 U0`

-   Le codec Indeo n’est plus pris en charge dans Windows.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>DShow. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Formats YUV 8 bits recommandés pour le rendu vidéo](../medfound/recommended-8-bit-yuv-formats-for-video-rendering.md)
</dt> <dt>

[Sous-types de vidéos](video-subtypes.md)
</dt> <dt>

[Utilisation des images vidéo](working-with-video-frames.md)
</dt> </dl>

 

 
