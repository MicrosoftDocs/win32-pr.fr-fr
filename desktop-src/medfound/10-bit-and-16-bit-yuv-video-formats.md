---
description: cette rubrique décrit les formats YUV 10 et 16 bits recommandés pour la capture, le traitement et l’affichage de vidéos dans le système d’exploitation Microsoft Windows.
ms.assetid: fcaaaa6f-f886-4f6e-9c3c-e513ccc90d37
title: Formats vidéo YUV 10 bits et 16 bits
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 09652929257c071bd735e1d6c7ec36e1767d904da7d2364ac3e30c61c81f342f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118065729"
---
# <a name="10-bit-and-16-bit-yuv-video-formats"></a>Formats vidéo YUV 10 bits et 16 bits

cette rubrique décrit les formats YUV 10 et 16 bits recommandés pour la capture, le traitement et l’affichage de vidéos dans le système d’exploitation Microsoft Windows.

Cette rubrique contient les sections suivantes :

-   [Vue d'ensemble](#overview)
-   [Codes FOURCC pour YUV 10 bits et 16 bits](#fourcc-codes-for-10-bit-and-16-bit-yuv)
-   [Définitions de surface](#surface-definitions)
    -   [4:2:0 formats](#420-formats)
    -   [4:2:2 formats](#422-formats)
    -   [4:4:4 formats](#444-formats)
-   [Formats YUV préférés](#preferred-yuv-formats)
-   [Rubriques connexes](#related-topics)

## <a name="overview"></a>Vue d’ensemble

Ces formats utilisent une représentation à virgule fixe pour le canal de luminance et les canaux Chroma (C’b et C’r). Les valeurs d’échantillonnage sont des valeurs 8 bits mises à l’échelle, à l’aide d’un facteur d’échelle de 2 ^ (n − 8), où n est égal à 10 ou 16, comme pour les sections 7.7-7.8 et 7.11-7.12 de SMPTE 274M. Les conversions de précision peuvent être effectuées à l’aide de décalages binaires simples. Par exemple, si le point blanc d’un format 8 bits est 235, le format 10 bits correspondant a un point blanc à 940 (235 × 4).

Les représentations 16 bits décrites ici utilisent des valeurs de **mot** Little-endian pour chaque canal. Les formats 10 bits utilisent également 16 bits pour chaque canal, avec les 6 bits les plus bas définis sur zéro, comme indiqué dans le diagramme suivant.

![Diagramme montrant la représentation de 10 bits](images/ee3aae23-4f0a-47d0-a46c-f3d7d94205e6.gif)

Étant donné que les représentations 10 bits et 16 bits du même format YUV ont la même disposition en mémoire, il est possible d’effectuer un cast d’une représentation de 10 bits en une représentation 16, sans perte de précision. Il est également possible d’effectuer un cast d’une représentation 16 bits vers une représentation de 10 bits. (Les formats Y416 et Y410 sont toutefois une exception à cette règle générale, car ils ne partagent pas la même disposition en mémoire.)

Lorsque le matériel graphique lit une surface qui contient une représentation de 10 bits, il doit ignorer les 6 bits de poids faible de chaque canal. Toutefois, si une surface contient des données 16 bits valides, elle doit être identifiée comme une surface de 16 bits.

Dans les formats qui contiennent alpha, un pixel complètement transparent a une valeur alpha égale à zéro et un pixel complètement opaque a une valeur alpha (2 ^ n) – 1, où n est le nombre de bits alpha. Alpha est supposée être une valeur linéaire appliquée à chaque composant une fois que le composant a été converti en sa forme linéaire normalisée.

Pour les images dans la mémoire vidéo, le pilote Graphics sélectionne l’alignement de la mémoire de l’aire. La surface doit être alignée sur la **valeur DWORD** . Autrement dit, les lignes individuelles au sein d’une surface sont assurées de démarrer à une limite de 32 bits, bien que l’alignement puisse être supérieur à 32 bits. L’origine (0,0) est toujours l’angle supérieur gauche de la surface.

Dans le cadre de cette documentation, le terme *U* est équivalent à *CB* et le terme *V* équivaut à *CR*.

## <a name="fourcc-codes-for-10-bit-and-16-bit-yuv"></a>Codes FOURCC pour YUV 10 bits et 16 bits

Les Codes FOURCC pour les formats décrits ici utilisent la Convention suivante :

-   Si le format est planaire, le premier caractère du code FOURCC est « P ». Si le format est compressé, le premier caractère est « Y ».
-   Le deuxième caractère du code FOURCC est déterminé par l’échantillonnage de chrominance, comme indiqué dans le tableau suivant.

    

    | Échantillonnage Chroma | Lettre de code FOURCC |
    |-----------------|--------------------|
    | 4:4:4           | 4                |
    | 4:2:2           | 2                |
    | 4:2:1           | « 1 »                |
    | 4:2:0           | « 0 »                |

    

     

-   Les deux derniers caractères du FOURCC indiquent le nombre de bits par canal, soit' 16 'pour 16 bits ou' 10 'pour 10 bits.

À l’aide de ce schéma, les Codes FOURCC suivants ont été définis. Aucun format 4:2:1 pour YUV de 10 ou 16 bits n’a été défini pour l’instant.



| FOURCC | Description            |
|--------|------------------------|
| P016   | Planar, 4:2:0, 16 bits. |
| P010   | Planar, 4:2:0, 10 bits. |
| P216   | Planar, 4:2:2, 16 bits. |
| P210   | Planar, 4:2:2, 10 bits. |
| Y216   | Compressé, 4:2:2, 16 bits. |
| Y210   | Compressé, 4:2:2, 10 bits. |
| Y416   | Compressé, 4:4:4, 16 bits  |
| Y410   | Compressé, 4:4:4, 10 bits. |



 

Les GUID de sous-type ont également été définis à partir de ces FOURCCs ; consultez [GUID de sous-type de vidéo](video-subtype-guids.md).

## <a name="surface-definitions"></a>Définitions de surface

Cette section décrit la disposition de la mémoire de chaque format. Dans les descriptions qui suivent, le terme **mot** fait référence à une valeur de 16 bits Little-endian et le terme **DWORD** fait référence à une valeur de 32 bits Little-endian.

### <a name="420-formats"></a>4:2:0 formats

Deux formats 4:2:0 sont définis, avec les Codes FOURCC P016 et P010. Ils partagent la même disposition en mémoire, mais P016 utilise 16 bits par canal et P010 utilise 10 bits par canal.

### <a name="p016-and-p010"></a>P016 et P010

Dans ces deux formats, tous les échantillons Y apparaissent en premier dans la mémoire sous la forme d’un tableau de **mots** avec un nombre pair de lignes. La largeur de la surface peut être supérieure à la largeur du plan Y. Ce tableau est immédiatement suivi d’un tableau de **mots** qui contient des exemples entrelacés vous et V, comme indiqué dans le diagramme suivant.

![Diagramme montrant la disposition des pixels P016 et P010](images/1e1c4d66-6172-4d3a-bd25-4b5caa67edcd.gif)

Si le tableau U-V combiné est adressé comme un tableau de **DWORD** s, le mot le moins significatif (LSW) contient la valeur U et le mot le plus significatif (MSW) contient la valeur V. La valeur Stride du plan U-V combiné est égale au Stride du plan Y. Le plan U-V comporte un demi-nombre de lignes comme plan Y.

Ces deux formats sont les formats de pixel planaires 4:2:0 préférés pour les représentations YUV de plus grande précision. Ils sont censés être une exigence de terme intermédiaire pour les accélérateurs d’accélération vidéo DirectX (DXVA) qui prennent en charge la vidéo 4:2:0 10 bits ou 16 bits.

### <a name="422-formats"></a>4:2:2 formats

Quatre formats 4:2:2 sont définis, deux plans planaires et deux compressés. Ils ont les Codes FOURCC suivants :

-   P216
-   P210
-   Y216
-   Y210

### <a name="p216-and-p210"></a>P216 et P210

Dans ces deux formats planaires, tous les échantillons Y apparaissent en premier dans la mémoire sous la forme d’un tableau de **mots** avec un nombre pair de lignes. La largeur de la surface peut être supérieure à la largeur du plan Y. Ce tableau est immédiatement suivi d’un tableau de **mots** qui contient des exemples entrelacés vous et V, comme indiqué dans le diagramme suivant.

![Diagramme montrant la disposition des pixels p216 et P210](images/ff672fef-218f-4722-b806-d06c77fe8cfa.gif)

Si le tableau U-V combiné est adressé comme un tableau de **DWORD** s, LSW contient la valeur U et le MSW contient la valeur V. La valeur Stride du plan U-V combiné est égale au Stride du plan Y. Le plan U-V a le même nombre de lignes que le plan Y.

Ces deux formats sont les formats de pixel planaires 4:2:2 préférés pour les représentations YUV de plus grande précision. Ils sont censés être une exigence de terme intermédiaire pour les accélérateurs d’accélération vidéo DirectX (DXVA) qui prennent en charge la vidéo 4:2:2 10 bits ou 16 bits.

### <a name="y216-and-y210"></a>Y216 et Y210

Dans ces deux formats compactés, chaque paire de pixels est stockée sous la forme d’un tableau de quatre **mots**, comme indiqué dans l’illustration suivante.

![Diagramme montrant la disposition des pixels y216 et Y210.](images/6f68aeeb-18ca-48ee-82c4-5b79d5510e9f.gif)

Le premier **mot** du tableau contient le premier échantillon y dans la paire, le deuxième **mot** contient l’exemple U, le troisième **mot** contient le deuxième échantillon y et le quatrième **mot** contient l’exemple V.

Y210 est identique à Y216, sauf que chaque échantillon contient uniquement 10 bits de données significatives. Les 6 bits de poids faible sont définis sur zéro, comme décrit précédemment.

### <a name="444-formats"></a>4:4:4 formats

Deux formats 4:4:4 sont définis, avec les Codes FOURCC Y410 et Y416. Les deux sont des formats compactés.

### <a name="y410"></a>Y410

Ce format est une représentation de 10 bits compressée qui comprend 2 bits d’alpha. Chaque pixel est encodé sous la forme d’une **valeur DWORD** unique avec la disposition de mémoire indiquée dans le diagramme suivant.

![Diagramme montrant la disposition des pixels Y410.](images/f8a71437-e3f1-4331-be30-f766c028d648.gif)

Bits 0-9 contiennent l’exemple U, bits 10-19 contiennent l’échantillon Y, bits 20-29 contiennent l’exemple V et bits 30-31 contient la valeur alpha. Pour indiquer qu’un pixel est entièrement opaque, une application doit définir les deux bits alpha égaux à 0x03.

### <a name="y416"></a>Y416

Ce format est une représentation 16 bits compressée qui comprend 16 bits d’alpha. Chaque pixel est encodé sous la forme d’une paire de **DWORD** s, comme indiqué dans l’illustration suivante.

![Diagramme montrant la disposition des pixels y416.](images/c928523a-25d3-4712-9aec-5b492b51435f.gif)

Bits 0-15 contiennent l’exemple U, bits 16-31 contiennent l’échantillon Y, bits 32-47 contiennent l’exemple V et bits 48-63 contient la valeur alpha.

Pour indiquer qu’un pixel est entièrement opaque, une application doit définir les deux bits alpha égaux à 0xFFFF. Ce format est principalement conçu comme un format intermédiaire lors du traitement de l’image afin d’éviter l’accumulation des erreurs.

## <a name="preferred-yuv-formats"></a>Formats YUV préférés

Le tableau suivant répertorie les formats YUV préférés, y compris les formats 8 bits.



| Format | Échantillonnage Chroma | Condensé ou planaire | Bits par canal |
|--------|-----------------|------------------|------------------|
| AYUV   | 4:4:4           | Riche           | 8                |
| Y410   | 4:4:4           | Riche           | 10               |
| Y416   | 4:4:4           | Riche           | 16               |
| AI44   | 4:4:4           | Riche           | En palette       |
| YUY2   | 4:2:2           | Riche           | 8                |
| Y210   | 4:2:2           | Riche           | 10               |
| Y216   | 4:2:2           | Riche           | 16               |
| P210   | 4:2:2           | Planaire           | 10               |
| P216   | 4:2:2           | Planaire           | 16               |
| NV12   | 4:2:0           | Planaire           | 8                |
| P010   | 4:2:0           | Planaire           | 10               |
| P016   | 4:2:0           | Planaire           | 16               |
| NV11   | 4:1:1           | Planaire           | 8                |



 

Si un objet prend en charge un schéma d’échantillonnage couleur et de profondeur de bits donné, il est recommandé de prendre en charge les formats YUV correspondants listés dans ce tableau. (Les objets peuvent prendre en charge des formats supplémentaires non répertoriés ici.)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Formats YUV 8 bits recommandés pour le rendu vidéo](recommended-8-bit-yuv-formats-for-video-rendering.md)
</dt> <dt>

[GUID de sous-type de vidéo](video-subtype-guids.md)
</dt> <dt>

[Types de média vidéo](video-media-types.md)
</dt> </dl>

 

 



