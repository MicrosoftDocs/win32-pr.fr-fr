---
title: Sous-types de médias non compressés
description: Sous-types de médias non compressés
ms.assetid: 5586e62a-d0f5-45cc-a690-4efa244b3f32
keywords:
- Windows Media Format SDK, types de médias
- ASF (Advanced Systems Format), types de média
- ASF (format des systèmes avancés), types de média
- Windows Media Format SDK, sous-types de médias non compressés
- ASF (Advanced Systems Format), sous-types de médias non compressés
- ASF (format des systèmes avancés), sous-types de médias non compressés
- types de média, sous-types de médias non compressés
- sous-types de médias non compressés
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9cdbd691a3b43a83656feffa1be114b5180d24cc5e29359b4168a4656d99fd03
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119807339"
---
# <a name="uncompressed-media-subtypes"></a>Sous-types de médias non compressés

Le tableau suivant répertorie les sous-types de médias non compressés. Il s’agit de types utilisés comme formats d’entrée et de sortie, ainsi que de formats pour les flux non compressés. Tous les types dans les tableaux suivants ne sont pas pris en charge de toutes façons. Les types de format d’entrée et de sortie pris en charge peuvent être énumérés par le codec dans le writer et le lecteur/lecteur synchrone, respectivement. Pour plus d’informations sur les types pris en charge pour les flux non compressés, consultez [utilisation de l’audio et de la flux vidéo non compressés](using-uncompressed-audio-and-video-streams.md).

Les différents types de vidéo RGB RVB et en palette répertoriés ici définissent les couleurs à l’aide du format RVB, dans lequel chaque couleur est représentée par les valeurs d’intensité des composants rouge, vert et bleu du pixel. Chaque valeur d’intensité peut être comprise entre 0 et 255, soit environ 16 780 000 couleurs uniques. Le RVB traduit facilement en valeurs de couleur utilisées pour les moniteurs d’ordinateur, qui utilisent des phosphores rouges, vertes et bleus pour afficher la couleur. Les types de vidéos en palette doivent inclure les informations de palette directement après la structure [**WMVIDEOINFOHEADER**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmvideoinfoheader) . De même, la vidéo 16 bits nécessite des informations de champ de bits, qui doivent être incluses après la structure WMVIDEOINFOHEADER.

Plusieurs des sous-types de médias dans le tableau suivant fournissent moins de couleurs que le système RVB, comme décrit dans la colonne Description. Dans les types RGB en palette, les couleurs de la palette représentent les valeurs RVB, mais elles sont spécifiées par une valeur qui indique la position de la couleur dans la palette.



| Sous-type de média non compressé | Description                                                                                                                                                                                                              |
|----------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| WMMEDIASUBTYPE \_ RGB1       | Vidéo en palette RGB avec 1 bit de couleur représentant 2 couleurs. Généralement utilisé pour les images monochromes.                                                                                                                         |
| WMMEDIASUBTYPE \_ RGB4       | Vidéo en palette RGB avec 4 bits de couleur représentant 16 couleurs.                                                                                                                                                           |
| WMMEDIASUBTYPE \_ RGB8       | Vidéo en palette RGB avec 8 bits de couleur représentant 256 couleurs.                                                                                                                                                          |
| WMMEDIASUBTYPE \_ RGB565     | Vidéo RVB avec 16 bits de couleur représentant 65 536 couleurs. Ce format utilise 5 bits pour le rouge, 6 bits pour le vert et 5 bits pour le bleu.                                                                                         |
| WMMEDIASUBTYPE \_ RGB555     | Vidéo RVB avec 16 bits de couleur représentant 32 768 couleurs. Ce format utilise 5 bits pour chaque couleur et ignore le seizième bit.                                                                                           |
| WMMEDIASUBTYPE \_ Rgb24      | Vidéo RVB avec 24 bits de couleur représentant toutes les 16 777 216 couleurs disponibles pour le schéma de représentation de couleur RVB. Ce format utilise 8 bits pour chaque valeur d’intensité de couleur.                                                |
| WMMEDIASUBTYPE \_ RGB32      | Vidéo RVB avec des bits de couleur 32 représentant toutes les 16 777 216 couleurs disponibles pour le schéma de représentation de couleur RVB. Ce format utilise 8 bits pour chaque couleur et réserve les 8 bits restants pour les informations de transparence. |
| WMMEDIASUBTYPE \_ I420       | Vidéo YUV stockée au format 4:2:0 planaire, le plan U apparaissant en premier, suivi du plan V.                                                                                                                      |
| WMMEDIASUBTYPE \_ IYUV       | Identique à I420.                                                                                                                                                                                                       |
| WMMEDIASUBTYPE \_ YV12       | Vidéo YUV stockée au format 4:2:0 planaire, le plan V apparaissant en premier, suivi du plan U. YV12 est identique à I420, sauf que les plans vous et V sont basculés.                                               |
| WMMEDIASUBTYPE \_ YUY2       | Vidéo YUV stockée au format 4:2:2 compressé.                                                                                                                                                                                 |
| WMMEDIASUBTYPE \_ UYVY       | Vidéo YUV stockée au format 4:2:2 compressé. Semblable à YUY2 mais avec un classement des données différent.                                                                                                                            |
| WMMEDIASUBTYPE \_ YVYU       | Vidéo YUV stockée au format 4:2:2 compressé. Semblable à YUY2 mais avec un classement des données différent.                                                                                                                            |
| WMMEDIASUBTYPE \_ P422       | Vidéo YUV stockée à l’aide d’un format 4:2:2 planaire.                                                                                                                                                                            |
| WMMEDIASUBTYPE \_ YVU9       | Vidéo YUV stockée au format 16:1:1 planaire.                                                                                                                                                                                |
| \_PCM WMMEDIASUBTYPE        | Données audio non compressées stockées à l’aide de la modulation par impulsions de code.                                                                                                                                                              |
| \_DRM WMMEDIASUBTYPE        | Données audio chiffrées non compressées utilisées avec un chemin d’accès audio sécurisé.                                                                                                                                                       |
| WMSCRIPTTYPE \_ TwoStrings   | Commandes de script consistant en une chaîne contenant le type de commande et une chaîne contenant les données de commande. il s’agit du seul type de script pris en charge dans le kit de développement logiciel (SDK) de Format multimédia Windows.                                     |
| Webstream WMMEDIASUBTYPE \_  | Données de transfert de fichiers contenant des fichiers et des composants HTML pour la diffusion en continu Web.                                                                                                                                               |
| WMMEDIASUBTYPE \_ VIDEOIMAGE | type d’entrée pour le codec d’Image Windows Media Video 9. Les exemples sont une combinaison d’images bitmap et de données de transformation.                                                                                                |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Assigner des formats de sortie**](assigning-output-formats.md)
</dt> <dt>

[**Sous-types de média compressés**](compressed-media-subtypes.md)
</dt> <dt>

[**Identificateurs de type de média**](media-type-identifiers.md)
</dt> <dt>

[**Types de médias**](media-types.md)
</dt> <dt>

[**Pour énumérer les formats d’entrée**](to-enumerate-input-formats.md)
</dt> </dl>

 

 




