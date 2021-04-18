---
description: Cette rubrique présente les formats de pixel fournis par le WIC (Windows Imaging Component).
ms.assetid: 348b6d15-e339-4dce-99f3-4d639ee9bf7d
title: Vue d’ensemble des formats de pixel natifs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4df37481399ac8193effc5d8f93aa49050460ee6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106526146"
---
# <a name="native-pixel-formats-overview"></a>Vue d’ensemble des formats de pixel natifs

Cette rubrique présente les formats de pixel fournis par le WIC (Windows Imaging Component).

Un format de pixel décrit la disposition de la mémoire de chaque pixel dans une bitmap. Cette disposition de mémoire décrit la façon dont les données d’image d’une image bitmap sont encodées en spécifiant le format numérique et l’organisation du canal de couleurs. WIC prend en charge plusieurs formats numériques pour plusieurs schémas d’organisation de canaux de couleurs, fournissant une large gamme de formats de pixel.

-   [Profondeur de bit](#bit-depth)
-   [Encodage numérique](#numerical-encoding)
-   [Canaux de couleur](#color-channels)
    -   [Modèle de couleurs RVB/BGR](#rgbbgr-color-model)
    -   [Modèle de couleurs CMJN](#cmyk-color-model)
    -   [Modèle de couleur n-Channel](#n-channel-color-model)
    -   [Modèles de couleurs indexés et nuances de gris](#indexed-and-grayscale-color-models)
    -   [Modèle de couleurs Y’CbCr](#ycbcr-color-model)
-   [Format de pixel WIC](#wic-pixel-format)
    -   [Formats de pixel non définis](#undefined-pixel-formats)
    -   [Formats de pixel indexé](#indexed-pixel-formats)
    -   [Formats de pixel condensé](#packed-bit-pixel-formats)
    -   [Nuances de gris, formats de pixel](#grayscale-pixel-formats)
    -   [Formats de pixel RVB/BGR](#rgbbgr-pixel-formats)
    -   [Formats de pixel CMJN](#cmyk-pixel-formats)
    -   [Formats de pixel à n canaux](#n-channel-pixel-formats)
    -   [Formats de pixel alpha uniquement](#alpha-only-pixel-formats)
    -   [Formats de pixel Y’CbCr](#ycbcr-pixel-formats)
-   [Espace colorimétrique](#color-space)
-   [Formats d’images natives](#native-image-formats)
    -   [Codec natif BMP](#bmp-native-codec)
    -   [Codec natif GIF](#gif-native-codec)
    -   [Codec natif ICO](#ico-native-codec)
    -   [Codec natif JPEG](#jpeg-native-codec)
    -   [Codec natif PNG](#png-native-codec)
    -   [Codec natif TIFF](#tiff-native-codec)
    -   [JPEG-codec natif XR](#jpeg-xr-native-codec)
-   [Codec natif DDS](#dds-native-codec)
-   [Extensibilité du format de pixel](#pixel-format-extensibility)
-   [Rubriques connexes](#related-topics)

## <a name="bit-depth"></a>Profondeur de bit

La *profondeur en bits* est le nombre de bits utilisés pour encoder chaque canal de couleurs. Aujourd’hui, la plupart des images numériques utilisent une profondeur de 8 bits, ce qui signifie que chaque canal de couleur d’un pixel est représenté par 8 bits, fournissant 2 ⁸ (256) valeurs uniques par canal. Une image avec une profondeur de 8 et trois canaux de couleur (tels que le rouge, le vert et le bleu) utilise 24 bits par pixel (BPP), qui fournit 2 ² ⁴ (16 777 216) différentes couleurs par pixel.

Pour une meilleure résolution des couleurs, une profondeur de 16 ou 32 peut être utilisée. Cela fournit chaque canal de couleur avec 2 ¹ ⁶ (65 536) ou 2 ³ ² valeurs uniques, à un coût d’une capacité de mémoire par pixel supérieure.

Dans certains formats, la profondeur de bit n’est pas un multiple de 8. Ces formats sont appelés formats *compactés* , car les canaux de couleur d’un pixel ne sont pas alignés sur les limites d’octets. Par exemple, si les profondeur de bits de 5, trois canaux de couleur peuvent être stockés en 16 bits (y compris 1 bit de remplissage, pour que les pixels soient alignés sur les octets). Les formats compactés sont utiles lorsque la mémoire ou la puissance de traitement sont limitées.

## <a name="numerical-encoding"></a>Encodage numérique

Pour la majorité des images numériques actuelles, les octets non signés et les entiers courts non signés sont utilisés pour décrire la plage numérique de chaque canal de couleur. La valeur minimale (0) représente l’intensité nulle dans un canal de couleur unique, et le noir est atteint lorsque toutes les couches de couleur sont égales à zéro. De même, la valeur maximale représente une intensité complète et le blanc est obtenu lorsque toutes les couches de couleur sont en intensité complète. À une profondeur de 8 bits, un UINT fournit 256 valeurs uniques par canal de couleur (0-255). Un UINT de 16 bits fournit 65 536 valeurs uniques par canal de couleur (0-65 535).

En outre, WIC prend en charge les formats à virgule fixe et à virgule flottante. Ces formats prennent en charge des plages dynamiques plus grandes, car la totalité de la plage numérique de chaque canal de couleurs est supérieure à la plage visible. Par conséquent, les couleurs peuvent être ajustées au-dessus ou en dessous de la plage visible, pendant les étapes intermédiaires du traitement de l’image, sans perte d’informations sur l’image.

### <a name="fixed-point-numerical-encoding"></a>Encodage Fixed-Point numérique

les valeurs à virgule fixe 16 bits sont interprétées comme s 2.13 : bit de signe, deux bits entiers et treize bits fractionnaires. À l’aide de cette interprétation, une plage numérique comprise entre − 4,0 et + 3,999... peut être représenté, avec la valeur 1,0 représentée par la valeur entière signée 8192 (0x2000).

les valeurs à virgule fixe 32 bits sont interprétées comme s 7.24 : bit de signe, sept bits d’entier et vingt-quatre bits fractionnaires. À l’aide de cette interprétation, une plage numérique comprise entre − 128,0 et + 127,999... peut être représenté, avec la valeur 1,0 représentée par la valeur entière signée 16777216 (0x01000000).

## <a name="color-channels"></a>Canaux de couleur

Les canaux de couleur d’un format de pixel définissent la disposition de la mémoire de chaque couleur dans les données d’image d’une image bitmap. Il existe une variété de structures de canaux de couleurs communes aux images numériques actuelles et le WIC prend en charge un grand nombre d’entre eux.

### <a name="rgbbgr-color-model"></a>Modèle de couleurs RVB/BGR

Les formats RGB et BGR décrivent les couleurs dans un modèle de couleurs additif. La méthode la plus courante pour décrire une image est avec trois canaux de couleurs distincts représentant les couleurs rouge (R), vert (G) et bleu (B). WIC prend en charge ces trois canaux en ordre rouge-vert-bleu (RVB) ou bleu-vert-rouge (BGR). Il s’agit de l’ordre dans lequel chaque canal de couleur apparaît dans le flux de bits séquentiel. Par exemple, dans le \_ format GUID WICPixelFormat32bppRGB, chaque pixel est 32 bits de largeur. Le canal rouge est le premier octet (le moins significatif) en mémoire, suivi du vert, puis du bleu. À l’inverse, au format GUID \_ WICPixelFormat32bppBGR, les canaux de couleur sont dans l’ordre inverse. WIC prend en charge un certain nombre de formats RGB/BGR, y compris des formats de bits compactés spéciaux tels que GUID \_ WICPixelFormat16bppBGR555.

> [!Note]  
> Les canaux de couleur des formats de bit condensé BGR spéciaux ne sont pas des multiples de 8 comme les canaux de couleur dans des formats de pixel standard. Cela signifie que les valeurs de canal ne sont pas alignées en octets. Une attention particulière doit être prise lors de la lecture des canaux de couleur de bit condensé.

 

Outre les formats RVB et BGR, WIC fournit également des formats de pixel RVB et BGR qui prennent en charge un canal alpha (A). Le canal alpha fournit des données d’opacité pour le pixel. Pour les formats avec un canal alpha ajouté, le canal alpha est généralement le dernier dans l’ordre des canaux de couleurs. Par exemple, dans le format de pixel GUID \_ WICPixelFormat32bppBGRA, l’ordre des octets est bleu, vert et rouge, suivi du canal alpha.

WIC prend également en charge les formats de pixel RVB prémultipliés (P) alpha. Dans un format de pixel RVBA classique, les valeurs de couleur rouge, vert et bleu sont les valeurs de couleur réelles de l’image. Pour qu’une image composite soit au format RVBA standard, la valeur alpha de l’image de premier plan doit être multipliée par chacun des canaux rouge, vert et bleu avant d’être ajoutée à la couleur de l’image d’arrière-plan. Dans un format de pixel RVB alpha prémultiplié, chaque canal de couleur a déjà été multiplié par la valeur alpha. Cela fournit une méthode plus efficace de composition d’image avec les données de canal alpha. Pour récupérer les valeurs de couleur vraies de chaque canal dans un format de pixel PRGBA/PBGRA, la multiplication de canal alpha doit être inversée en divisant les valeurs de couleur par la valeur alpha.

### <a name="cmyk-color-model"></a>Modèle de couleurs CMJN

Le modèle CMJN est un modèle de couleur soustrait utilisé pour l’impression. Les couleurs produites par un modèle CMJN sont générées par la lumière qui n’est pas absorbée, mais qui sont reflétées. Le modèle CMJN est un modèle à quatre canaux de cyan (C), magenta (M), jaune (Y) et noir (K). Lorsque les quatre canaux de couleur sont à valeur maximale, le résultat est noir. À l’instar des modèles de couleur RVB/BGR, l’ordre des octets dans le flux de bits séquentiel est donné par le nom du format de pixel. Par exemple, dans le GUID de format de pixel \_ WICPixelFormat32bppCMYK, chaque pixel est composé de 32 bits. Le premier octet contient la valeur cyan, suivie par le magenta, le jaune et le noir. WIC fournit des formats de pixel pour le format CMJN à 32 et 64 bits par pixel (BPP).

En plus du modèle de couleurs CMJN standard, WIC fournit également CMJN avec alpha. Cela permet aux images CMJN d’avoir des données de fusion alpha semblables à celles du modèle de couleurs RVB/BGR. Le canal alpha est situé juste après le noir dans le flux de bits séquentiel d’une bitmap.

### <a name="n-channel-color-model"></a>Modèle de couleur n-Channel

Pour plus de flexibilité, WIC fournit également des formats de pixel qui n’ont pas d’ordre de canal prédéfini. WIC fournit des formats de pixel qui prennent en charge de trois à huit canaux de données d’image continue à des niveaux de profondeur de 8 et 16. Contrairement aux formats RVB/BGR et CMJN, les formats n-Channel ne spécifient pas l’ordre des canaux mais plutôt le nombre de canaux de couleur disponibles. Par exemple, dans le GUID de format de pixel \_ WICPixelFormat32bpp4Channels, chaque pixel est constitué de 32 bits avec chacun des 4 canaux occupant un seul octet.

WIC fournit également des formats de pixel pour n canaux avec alpha. Cela permet aux images à n canaux d’avoir des données de fusion alpha semblables aux modèles de couleurs RVB/BGR et CMJN. Le canal alpha est situé juste après le dernier canal de couleur dans le flux de bits séquentiel d’une bitmap.

### <a name="indexed-and-grayscale-color-models"></a>Modèles de couleurs indexés et nuances de gris

Les formats *indexés* utilisent une table de couleurs, appelée *palette*. La palette est stockée en externe dans les données de pixels ou n’est pas définie implicitement. La valeur de chaque pixel de l’image est un index de la palette. Avec un format indexé, le nombre de bits par pixel est directement lié au nombre d’entrées dans la palette. Cela réduit considérablement la quantité de données requises pour représenter l’image, mais limite également le nombre de couleurs disponibles pour l’image. WIC prend en charge les formats indexés avec 1, 2, 4 ou 8 BPP.

Pour les formats monochromes (nuances de gris), WIC prend en charge 1, 2, 4, 8, 16 et 32 bits par pixel. Pour les bits de profondeur 1, 8, 16 et 32, les données de couleur sont stockées dans un canal unique. Pour les profondeurs de bits 2 ou 4, les pixels sont des index dans une palette de nuances de gris.

### <a name="ycbcr-color-model"></a>Modèle de couleurs Y’CbCr

WIC ajoute la prise en charge du modèle de couleurs JPEG JFIF Y’CbCr. Y’CbCr des couleurs distinctes dans un composant de luminance (Y) et deux composants de chrominance (CB et CR). De nombreux fichiers JPEG stockent les données d’image en mode natif à l’aide du modèle de couleurs Y’CbCr.

Le système visuel humain est moins sensible aux modifications de chrominance que la luminance, et les formats Y’CbCr peuvent tirer parti de cette sensibilité réduite en réduisant la quantité de données de chrominance stockées par rapport à la luminance. Pour ce faire, il stocke la chrominance et la luminance dans des plans distincts et la mise à l’échelle de chaque plan de composant vers une résolution différente. Cette pratique est connue sous le nom de « échantillonnage Chroma ».

Étant donné que les données de chrominance et de luminance sont stockées séparément et peuvent être des résolutions différentes, WIC définit des formats de pixels de luminance et de chrominance distincts. WIC prend en charge les données de 8 bits par canal.

## <a name="wic-pixel-format"></a>Format de pixel WIC

Les formats de pixel dans WIC sont définis à l’aide de GUID pour éviter les conflits avec les IHV. WIC fournit un nom convivial pour référencer le GUID d’un format de pixel natif. La Convention d’affectation de noms pour les formats de pixel WIC est la suivante :

**\[GUID \_ WICPixelFormat \] \[ bits par pixel \] \[ type de \] \[ stockage de l’ordre des canaux\]**

| Mettre en forme le composant         | Description                                                                                                                                                                                                                                                                                                  |
|--------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **GUID \_ WICPixelFormat** | Identification descriptive de tous les formats de pixel WIC. Le nom convivial de tous les pixels de WIC commence par cette chaîne.                                                                                                                                                                                       |
| **Bits par pixel**       | Nombre de bits par pixel (BPP) utilisé pour le format de pixel.                                                                                                                                                                                                                                                |
| **Ordre des canaux**        | Modèle de canal de couleur et ordre de chaque canal pour le format.                                                                                                                                                                                                                                            |
| **Type de stockage**         | Encodage numérique utilisé pour le format de pixel. L’encodage par défaut est un entier non signé. Si rien ne suit les informations de modèle de couleur, un entier non signé (UINT) est implicite. FixedPoint et float sont utilisés pour identifier les formats de pixel qui utilisent l’encodage à virgule fixe et à virgule flottante respectivement. |



 

> [!Note]  
> Pour les formats n-Channel, \[ \] l’ordre des canaux ne spécifie pas l’ordre des couleurs, mais plutôt le nombre de canaux disponibles. Par exemple, \_ le GUID WICPixelFormat24bpp3Channels fournit 3 canaux de couleurs où « 3Channels » est l' \[ \] entrée d’ordre de canal, mais indique uniquement le nombre de canaux et non l’ordre.

 

Par exemple, le nom convivial GUID \_ WICPixelFormat24bppRGB signifie que le format de pixel utilise 24 bits par pixel et le modèle de couleurs RVB. Étant donné que le nom n’identifie pas explicitement un type de stockage, un entier non signé est implicite.

WIC prend en charge plusieurs formats de pixel. Les tableaux suivants regroupent des formats de pixel similaires par structure de couleur tout en fournissant des informations supplémentaires telles que la profondeur de bit, les bits par pixel et l’encodage numérique. Chaque table contient les informations suivantes :

-   **Nom convivial**. Nom convivial du format de pixel.
-   **Nombre de canaux**. Nombre de canaux de couleurs.
-   **Bits par canal**. Nombre de bits par canal (profondeur de bit).
-   **Bits par pixel**. Nombre de bits par pixel, y compris les bits de remplissage.
-   **Type de stockage**. Encodage numérique des données de l’image. Cette valeur peut être un entier non signé (UINT), un nombre à virgule fixe (FixedPoint) ou un nombre à virgule flottante (float).

> [!Note]  
> Par souci de clarté, ce document fait référence aux formats de pixel uniquement par leurs noms conviviaux. La valeur hexadécimale réelle pour les formats de pixel se trouve dans les fichiers wincodec. h/IDL.

 

### <a name="undefined-pixel-formats"></a>Formats de pixel non définis

La liste suivante affiche les formats de pixel génériques qui sont utilisés lorsque le format de pixel n’est pas défini ou n’est pas important pour une opération d’image.

-   GUID \_ WICPixelFormatUndefined
-   GUID \_ WICPixelFormatDontCare

### <a name="indexed-pixel-formats"></a>Formats de pixel indexé

Le tableau suivant répertorie les formats de pixel indexé fournis par WIC. Dans ces formats, la valeur de chaque pixel est un index dans une palette de couleurs.



| Nom convivial                   | Nombre de canaux | Bits par pixel | Type de stockage |
|---------------------------------|---------------|----------------|--------------|
| GUID \_ WICPixelFormat1bppIndexed | 1             | 1              | UINT         |
| GUID \_ WICPixelFormat2bppIndexed | 1             | 2              | UINT         |
| GUID \_ WICPixelFormat4bppIndexed | 1             | 4              | UINT         |
| GUID \_ WICPixelFormat8bppIndexed | 1             | 8              | UINT         |



 

### <a name="packed-bit-pixel-formats"></a>Formats de pixel condensé

Le tableau suivant répertorie les formats binaires compressés fournis par WIC. Dans ces formats, les données des canaux de couleurs ne sont pas alignées sur les octets.



| Nom convivial                          | Nombre de canaux | Bits par canal       | Bits par pixel | Type de stockage |
|-------------------------------------------|---------------|------------------------|----------------|--------------|
| GUID \_ WICPixelFormat16bppBGR555           | 3             | 5                      | 16             | UINT         |
| GUID \_ WICPixelFormat16bppBGR565           | 3             | 5 (B)/6 (G)/5 (R)         | 16             | UINT         |
| GUID \_ WICPixelFormat16bppBGRA555          | 4             | 5 (B)/5 (G)/5 (R)/1 (A)    | 16             | UINT         |
| GUID \_ WICPixelFormat32bppBGR101010        | 3             | 10                     | 32             | UINT         |
| GUID \_ WICPixelFormat32bppRGBA1010102      | 4             | 10 (R)/10 (G)/10 (B)/2 (A) | 32             | UINT         |
| GUID \_ WICPixelFormat32bppRGBA1010102XR    | 4             | 10 (R)/10 (G)/10 (B)/2 (A) | 32             | UINT         |
| GUID \_ WICPixelFormat32bppR10G10B10A2      | 4             | 10 (R)/10 (G)/10 (B)/2 (A) | 32             | UINT         |
| GUID \_ WICPixelFormat32bppR10G10B10A2HDR10 | 4             | 10 (R)/10 (G)/10 (B)/2 (A) | 32             | UINT         |

Pour les \_ formats GUID WICPixelFormat32bppBGR101010 et GUID \_ WICPixelFormat32bppRGBA1010102, le canal rouge est stocké dans les bits les moins significatifs. Pour les \_ formats GUID WICPixelFormat32bppR10G10B10A2 et GUID \_ WICPixelFormat32bppR10G10B10A2HDR10, le canal rouge est défini dans les bits les plus significatifs, la même disposition que [DXGI_FORMAT_R10G10B10A2_UNORM](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).

Le \_ format WICPIXELFORMAT32BPPR10G10B10A2HDR10 GUID est le format de pixel de 10 bits pour HDR10 (BT. 2020 Color Space et SMPTE St. 084 EOTF).

### <a name="grayscale-pixel-formats"></a>Nuances de gris, formats de pixel

Le tableau suivant répertorie les formats de nuances de gris fournis par WIC. Dans ces formats, les données de couleur représentent des nuances de gris.



| Nom convivial                           | Nombre de canaux | Bits par canal | Bits par pixel | Type de stockage |
|-----------------------------------------|---------------|------------------|----------------|--------------|
| GUID \_ WICPixelFormatBlackWhite          | 1             | 1                | 1              | UINT         |
| GUID \_ WICPixelFormat2bppGray            | 1             | 2                | 2              | UINT         |
| GUID \_ WICPixelFormat4bppGray            | 1             | 4                | 4              | UINT         |
| GUID \_ WICPixelFormat8bppGray            | 1             | 8                | 8              | UINT         |
| GUID \_ WICPixelFormat16bppGray           | 1             | 16               | 16             | UINT         |
| GUID \_ WICPixelFormat16bppGrayFixedPoint | 1             | 16               | 16             | FixedPoint   |
| GUID \_ WICPixelFormat16bppGrayHalf       | 1             | 16               | 16             | Float        |
| GUID \_ WICPixelFormat32bppGrayFloat      | 1             | 32               | 32             | Float        |
| GUID \_ WICPixelFormat32bppGrayFixedPoint | 1             | 32               | 32             | FixedPoint   |



 

### <a name="rgbbgr-pixel-formats"></a>Formats de pixel RVB/BGR

Le tableau suivant répertorie les formats RGB/BGR fournis par WIC. Ces formats séparent les données de couleur primaires en canaux rouge (R), vert (G) et bleu (B). Un canal alpha (A) supplémentaire est fourni pour les informations d’opacité dans certains formats.



| Nom convivial                            | Nombre de canaux | Bits par canal | Bits par pixel | Type de stockage |
|------------------------------------------|---------------|------------------|----------------|--------------|
| GUID \_ WICPixelFormat24bppRGB             | 3             | 8                | 24             | UINT         |
| GUID \_ WICPixelFormat24bppBGR             | 3             | 8                | 24             | UINT         |
| GUID \_ WICPixelFormat32bppBGR             | 3             | 8                | 32             | UINT         |
| GUID \_ WICPixelFormat32bppRGBA            | 4             | 8                | 32             | UINT         |
| GUID \_ WICPixelFormat32bppBGRA            | 4             | 8                | 32             | UINT         |
| GUID \_ WICPixelFormat32bppRGBE\*          | 4             | 8                | 32             | Float        |
| GUID \_ WICPixelFormat32bppPRGBA           | 4             | 8                | 32             | UINT         |
| GUID \_ WICPixelFormat32bppPBGRA           | 4             | 8                | 32             | UINT         |
| GUID \_ WICPixelFormat48bppRGB             | 3             | 16               | 48             | UINT         |
| GUID \_ WICPixelFormat48bppBGR             | 3             | 16               | 48             | UINT         |
| GUID \_ WICPixelFormat48bppRGBFixedPoint   | 3             | 16               | 48             | Fixe        |
| GUID \_ WICPixelFormat48bppBGRFixedPoint   | 3             | 16               | 48             | Fixe        |
| GUID \_ WICPixelFormat48bppRGBHalf         | 3             | 16               | 48             | Float        |
| GUID \_ WICPixelFormat64bppRGBA            | 4             | 16               | 64             | UINT         |
| GUID \_ WICPixelFormat64bppBGRA            | 4             | 16               | 64             | UINT         |
| GUID \_ WICPixelFormat64bppPRGBA           | 4             | 16               | 64             | UINT         |
| GUID \_ WICPixelFormat64bppPBGRA           | 4             | 16               | 64             | UINT         |
| GUID \_ WICPixelFormat64bppRGBFixedPoint   | 3             | 16               | 64             | Fixe        |
| GUID \_ WICPixelFormat64bppRGBAFixedPoint  | 4             | 16               | 64             | Fixe        |
| GUID \_ WICPixelFormat64bppBGRAFixedPoint  | 4             | 16               | 64             | Fixe        |
| GUID \_ WICPixelFormat64bppRGBHalf         | 3             | 16               | 64             | Float        |
| GUID \_ WICPixelFormat64bppRGBAHalf        | 4             | 16               | 64             | Float        |
| GUID \_ WICPixelFormat96bppRGBFixedPoint   | 3             | 32               | 96             | Fixe        |
| GUID \_ WICPixelFormat128bppRGBFloat       | 3             | 32               | 128            | Float        |
| GUID \_ WICPixelFormat128bppRGBAFloat      | 4             | 32               | 128            | Float        |
| GUID \_ WICPixelFormat128bppPRGBAFloat     | 4             | 32               | 128            | Float        |
| GUID \_ WICPixelFormat128bppRGBFixedPoint  | 3             | 32               | 128            | Fixe        |
| GUID \_ WICPixelFormat128bppRGBAFixedPoint | 4             | 32               | 128            | Fixe        |



 

> [!Note]  
> \*Le \_ format WICPIXELFORMAT32BPPRGBE GUID encode les valeurs à virgule flottante 3 16 bits en 4 octets, comme suit : trois mantisses non signés de 8 bits pour les canaux R, G et B, plus un exposant 8 bits partagé. Ce format fournit une précision à virgule flottante de 16 bits dans une représentation de pixels plus petite.

 

À compter de Windows 8 et de la [mise à jour de plateforme pour Windows 7](/windows/desktop/direct3darticles/platform-update-for-windows-7), WIC fournit des formats supplémentaires, présentés dans le tableau ci-dessous.



| Nom convivial                      | Nombre de canaux | Bits par canal | Bits par pixel | Type de stockage |
|------------------------------------|---------------|------------------|----------------|--------------|
| GUID \_ WICPixelFormat32bppRGB       | 3             | 8                | 32             | UINT         |
| GUID \_ WICPixelFormat64bppRGB       | 3             | 16               | 64             | UINT         |
| GUID \_ WICPixelFormat96bppRGBFloat  | 3             | 32               | 96             | FLOAT        |
| GUID \_ WICPixelFormat64bppPRGBAHalf | 4             | 16               | 64             | FLOAT        |



 

### <a name="cmyk-pixel-formats"></a>Formats de pixel CMJN

Le tableau suivant répertorie les formats CMJN fournis par WIC. Ces formats séparent les données de couleur primaire en canaux cyan (C), magenta (M), jaune (Y) et noir (K).



| Nom convivial                      | Nombre de canaux | Bits par canal | Bits par pixel | Type de stockage |
|------------------------------------|---------------|------------------|----------------|--------------|
| GUID \_ WICPixelFormat32bppCMYK      | 4             | 8                | 32             | UINT         |
| GUID \_ WICPixelFormat64bppCMYK      | 4             | 16               | 64             | UINT         |
| GUID \_ WICPixelFormat40bppCMYKAlpha | 5             | 8                | 40             | UINT         |
| GUID \_ WICPixelFormat80bppCMYKAlpha | 5             | 16               | 80             | UINT         |



 

### <a name="n-channel-pixel-formats"></a>Formats de pixel à n canaux

Le tableau suivant répertorie les formats de canaux n fournis par WIC. Ces formats fournissent un certain nombre de canaux de couleur non définis pour stocker des données d’image.



| Nom convivial                            | Nombre de canaux | Bits par canal | Bits par pixel | Type de stockage |
|------------------------------------------|---------------|------------------|----------------|--------------|
| GUID \_ WICPixelFormat24bpp3Channels       | 3             | 8                | 24             | UINT         |
| GUID \_ WICPixelFormat48bpp3Channels       | 3             | 16               | 48             | UINT         |
| GUID \_ WICPixelFormat32bpp3ChannelsAlpha  | 4             | 8                | 32             | UINT         |
| GUID \_ WICPixelFormat64bpp3ChannelsAlpha  | 4             | 16               | 64             | UINT         |
| GUID \_ WICPixelFormat32bpp4Channels       | 4             | 8                | 32             | UINT         |
| GUID \_ WICPixelFormat64bpp4Channels       | 4             | 16               | 64             | UINT         |
| GUID \_ WICPixelFormat40bpp4ChannelsAlpha  | 5             | 8                | 40             | UINT         |
| GUID \_ WICPixelFormat80bpp4ChannelsAlpha  | 5             | 16               | 80             | UINT         |
| GUID \_ WICPixelFormat40bpp5Channels       | 5             | 8                | 40             | UINT         |
| GUID \_ WICPixelFormat80bpp5Channels       | 5             | 16               | 80             | UINT         |
| GUID \_ WICPixelFormat48bpp5ChannelsAlpha  | 6             | 8                | 48             | UINT         |
| GUID \_ WICPixelFormat96bpp5ChannelsAlpha  | 6             | 16               | 96             | UINT         |
| GUID \_ WICPixelFormat48bpp6Channels       | 6             | 8                | 48             | UINT         |
| GUID \_ WICPixelFormat96bpp6Channels       | 6             | 16               | 96             | UINT         |
| GUID \_ WICPixelFormat56bpp6ChannelsAlpha  | 7             | 8                | 56             | UINT         |
| GUID \_ WICPixelFormat112bpp6ChannelsAlpha | 7             | 16               | 112            | UINT         |
| GUID \_ WICPixelFormat56bpp7Channels       | 7             | 8                | 56             | UINT         |
| GUID \_ WICPixelFormat112bpp7Channels      | 7             | 16               | 112            | UINT         |
| GUID \_ WICPixelFormat64bpp7ChannelsAlpha  | 8             | 8                | 64             | UINT         |
| GUID \_ WICPixelFormat128bpp7ChannelsAlpha | 8             | 16               | 128            | UINT         |
| GUID \_ WICPixelFormat64bpp8Channels       | 8             | 8                | 64             | UINT         |
| GUID \_ WICPixelFormat128bpp8Channels      | 8             | 16               | 128            | UINT         |
| GUID \_ WICPixelFormat72bpp8ChannelsAlpha  | 9             | 8                | 72             | UINT         |
| GUID \_ WICPixelFormat144bpp8ChannelsAlpha | 9             | 16               | 144            | UINT         |



 

### <a name="alpha-only-pixel-formats"></a>Formats de pixel alpha uniquement

Le tableau suivant répertorie les formats alpha uniquement fournis par WIC. Ce format contient uniquement des informations alpha.



| Nom convivial                 | Nombre de canaux | Bits par canal | Bits par pixel | Type de stockage |
|-------------------------------|---------------|------------------|----------------|--------------|
| GUID \_ WICPixelFormat8bppAlpha | 1             | 8                | 32             | UINT         |



 

### <a name="ycbcr-pixel-formats"></a>Formats de pixel Y’CbCr

Le tableau suivant répertorie les formats Y’CbCr fournis par WIC. Ces formats séparent les données de couleur primaire par la luminance (Y), la différence de chrominance bleue (CB) et la différence rouge Choma (CR). Notez que ces formats sont conçus pour stocker les données de pixels Y’CbCr JPEG JFIF.



| Nom convivial                 | Nombre de canaux | Bits par pixel | Type de stockage |
|-------------------------------|---------------|----------------|--------------|
| GUID \_ WICPixelFormat8bppY     | 1             | 8              | UINT         |
| GUID \_ WICPixelFormat8bppCb    | 1             | 8              | UINT         |
| GUID \_ WICPixelFormat8bppCr    | 1             | 8              | UINT         |
| GUID \_ WICPixelFormat16bppCbCr | 2             | 16             | UINT         |



 

## <a name="color-space"></a>Espace colorimétrique

Les formats de pixel en eux-mêmes n’ont pas d’espace de couleurs. En règle générale, l’espace colorimétrique est une interprétation sémantique des valeurs de pixel qui dépendent du contexte de l’image bitmap. Certaines images identifient un contexte de couleur qui définit l’espace colorimétrique de l’image. L’espace colorimétrique est déduit uniquement en l’absence d’un contexte de couleur.

Les informations de contexte de couleur sont définies par l’interface [**IWICColorContext**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext) pour WIC. Pour récupérer les informations de contexte de couleur pour une image, utilisez la méthode **GetColorContext** .

En l’absence d’informations d’espace de couleurs pour une image, la règle générale pour l’inférence de l’espace colorimétrique est que les formats UINT RVB et nuances de gris utilisent l’espace de couleurs RVB standard (sRVB), tandis que les formats RVB et en virgule flottante de virgule fixe et de nuances de gris utilisent l’espace de couleurs RVB étendu (ScRVB). Le modèle de couleurs CMJN utilise un espace de couleurs RWOP.

## <a name="native-image-formats"></a>Formats d’images natives

Chacun des codecs WIC fournis par Windows prend en charge un sous-ensemble des formats de pixel WIC. Pour chaque codec, les formats de décodage pris en charge peuvent être différents de ceux pris en charge.

Lors du décodage d’une image, si les données sont stockées en mode natif dans un format de pixel qui n’est pas pris en charge par le décodeur, il est converti dans un format pris en charge. Pour déterminer le format de pixel de sortie, appelez [**IWICBitmapFrameDecode :: GetPixelFormat**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-getpixelformat).

Lors de l’encodage d’une image, utilisez [**IWICBitmapFrameEncode :: SetPixelFormat**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setpixelformat) pour demander que l’encodeur utilise un format de pixel spécifique. L’encodeur retourne le format de pixel le plus proche pris en charge, qui peut être différent de ce qui a été demandé.

Les tableaux suivants affichent les formats de pixel pris en charge par les codecs WIC fournis par Windows.

### <a name="bmp-native-codec"></a>Codec natif BMP



| Formats de pixel du décodeur                   | Formats de pixel de l’encodeur                   |
|-----------------------------------------|-----------------------------------------|
| GUID \_ WICPixelFormat1bppIndexed         | GUID \_ WICPixelFormat1bppIndexed         |
| GUID \_ WICPixelFormat4bppIndexed         | GUID \_ WICPixelFormat4bppIndexed         |
| GUID \_ WICPixelFormat8bppIndexed         | GUID \_ WICPixelFormat8bppIndexed         |
| GUID \_ WICPixelFormat16bppBGR555         | GUID \_ WICPixelFormat16bppBGR555         |
| GUID \_ WICPixelFormat16bppBGR565         | GUID \_ WICPixelFormat16bppBGR565         |
| GUID \_ WICPixelFormat24bppBGR            | GUID \_ WICPixelFormat24bppBGR            |
| GUID \_ WICPixelFormat32bppBGR            | GUID \_ WICPixelFormat32bppBGR            |
| GUID \_ WICPixelFormat32bppBGRA\*         | GUID \_ WICPixelFormat32bppBGRA\*         |
| GUID \_ WICPixelFormat64bppRGBAFixedPoint | GUID \_ WICPixelFormat32bppPBGRA          |
|                                         | GUID \_ WICPixelFormat64bppRGBAFixedPoint |
|                                         | GUID \_ WICPixelFormat64bppBGRAFixedPoint |



 

> [!Note]  
> \_Le GUID WICPixelFormat32bppBGRA est uniquement pris en charge dans Windows 8, la [mise à jour de la plateforme pour Windows 7](/windows/desktop/direct3darticles/platform-update-for-windows-7)et les versions ultérieures.
>
> -   Pour encoder dans ce format, utilisez l’option d’encodeur **EnableV5Header32bppBGRA** . Le BMP sera écrit avec un en-tête BITMAPV5HEADER.
> -   Si un fichier a un BITMAPV5HEADER, il se décode en tant que GUID \_ WICPixelFormat32bppBGRA.

 

### <a name="gif-native-codec"></a>Codec natif GIF



| Formats de pixel du décodeur           | Formats de pixel de l’encodeur           |
|---------------------------------|---------------------------------|
| GUID \_ WICPixelFormat8bppIndexed | GUID \_ WICPixelFormat8bppIndexed |



 

### <a name="ico-native-codec"></a>Codec natif ICO



| Formats de pixel du décodeur         | Formats de pixel de l’encodeur |
|-------------------------------|-----------------------|
| GUID \_ WICPixelFormat32bppBGRA |                       |



 

### <a name="jpeg-native-codec"></a>Codec natif JPEG



| Formats de pixel du décodeur         | Formats de pixel de l’encodeur         |
|-------------------------------|-------------------------------|
| GUID \_ WICPixelFormat8bppGray  | GUID \_ WICPixelFormat8bppGray  |
| GUID \_ WICPixelFormat24bppBGR  | GUID \_ WICPixelFormat24bppBGR  |
| GUID \_ WICPixelFormat32bppCMYK | GUID \_ WICPixelFormat32bppCMYK |



 

### <a name="png-native-codec"></a>Codec natif PNG



| Formats de pixel du décodeur           | Formats de pixel de l’encodeur           |
|---------------------------------|---------------------------------|
| GUID \_ WICPixelFormat1bppIndexed | GUID \_ WICPixelFormat1bppIndexed |
| GUID \_ WICPixelFormat2bppIndexed | GUID \_ WICPixelFormat2bppIndexed |
| GUID \_ WICPixelFormat4bppIndexed | GUID \_ WICPixelFormat4bppIndexed |
| GUID \_ WICPixelFormat8bppIndexed | GUID \_ WICPixelFormat8bppIndexed |
| GUID \_ WICPixelFormatBlackWhite  | GUID \_ WICPixelFormatBlackWhite  |
| GUID \_ WICPixelFormat2bppGray    | GUID \_ WICPixelFormat2bppGray    |
| GUID \_ WICPixelFormat4bppGray    | GUID \_ WICPixelFormat4bppGray    |
| GUID \_ WICPixelFormat8bppGray    | GUID \_ WICPixelFormat8bppGray    |
| GUID \_ WICPixelFormat16bppGray   | GUID \_ WICPixelFormat16bppGray   |
| GUID \_ WICPixelFormat24bppBGR    | GUID \_ WICPixelFormat24bppBGR    |
| GUID \_ WICPixelFormat32bppBGRA   | GUID \_ WICPixelFormat32bppBGRA   |
| GUID \_ WICPixelFormat48bppRGB    | GUID \_ WICPixelFormat48bppRGB    |
| GUID \_ WICPixelFormat64bppRGBA   | GUID \_ WICPixelFormat48bppBGR    |
|                                 | GUID \_ WICPixelFormat64bppRGBA   |
|                                 | GUID \_ WICPixelFormat64bppBGRA   |



 

### <a name="tiff-native-codec"></a>Codec natif TIFF



| Formats de pixel du décodeur                | Formats de pixel de l’encodeur           |
|--------------------------------------|---------------------------------|
| GUID \_ WICPixelFormat1bppIndexed      | GUID \_ WICPixelFormat1bppIndexed |
| GUID \_ WICPixelFormat4bppIndexed      | GUID \_ WICPixelFormat4bppIndexed |
| GUID \_ WICPixelFormat8bppIndexed      | GUID \_ WICPixelFormat8bppIndexed |
| GUID \_ WICPixelFormatBlackWhite       | GUID \_ WICPixelFormatBlackWhite  |
| GUID \_ WICPixelFormat4bppGray         | GUID \_ WICPixelFormat4bppGray    |
| GUID \_ WICPixelFormat8bppGray         | GUID \_ WICPixelFormat8bppGray    |
| GUID \_ WICPixelFormat16bppGray        | GUID \_ WICPixelFormat16bppGray   |
| GUID \_ WICPixelFormat32bppGrayFloat   | GUID \_ WICPixelFormat24bppBGR    |
| GUID \_ WICPixelFormat24bppBGR         | GUID \_ WICPixelFormat32bppBGRA   |
| GUID \_ WICPixelFormat32bppBGRA        | GUID \_ WICPixelFormat32bppCMYK   |
| GUID \_ WICPixelFormat32bppPBGRA       | GUID \_ WICPixelFormat48bppRGB    |
| GUID \_ WICPixelFormat48bppRGB         | GUID \_ WICPixelFormat64bppRGBA   |
| GUID \_ WICPixelFormat32bppCMYK        |                                 |
| GUID \_ WICPixelFormat40bppCMYKAlpha   |                                 |
| GUID \_ WICPixelFormat64bppRGBA        |                                 |
| GUID \_ WICPixelFormat64bppPRGBA       |                                 |
| GUID \_ WICPixelFormat64bppCMYK        |                                 |
| GUID \_ WICPixelFormat80bppCMYKAlpha   |                                 |
| GUID \_ WICPixelFormat96bppRGBFloat\*  |                                 |
| GUID \_ WICPixelFormat128bppRGBAFloat  |                                 |
| GUID \_ WICPixelFormat128bppPRGBAFloat |                                 |



 

> [!Note]  
> \_Le GUID WICPixelFormat96bppRGBFloat est uniquement pris en charge dans Windows 8, la [mise à jour de la plateforme pour Windows 7](/windows/desktop/direct3darticles/platform-update-for-windows-7)et les versions ultérieures.

 

### <a name="jpeg-xr-native-codec"></a>JPEG-codec natif XR



| Formats de pixel du décodeur                    | Formats de pixel de l’encodeur                    |
|------------------------------------------|------------------------------------------|
| GUID \_ WICPixelFormatBlackWhite           | GUID \_ WICPixelFormatBlackWhite           |
| GUID \_ WICPixelFormat8bppGray             | GUID \_ WICPixelFormat8bppGray             |
| GUID \_ WICPixelFormat16bppBGR555          | GUID \_ WICPixelFormat16bppBGR555          |
| GUID \_ WICPixelFormat16bppGray            | GUID \_ WICPixelFormat16bppGray            |
| GUID \_ WICPixelFormat24bppBGR             | GUID \_ WICPixelFormat24bppBGR             |
| GUID \_ WICPixelFormat24bppRGB             | GUID \_ WICPixelFormat24bppRGB             |
| GUID \_ WICPixelFormat32bppBGR             | GUID \_ WICPixelFormat32bppBGR             |
| GUID \_ WICPixelFormat32bppBGRA            | GUID \_ WICPixelFormat32bppBGRA            |
| GUID \_ WICPixelFormat48bppRGBFixedPoint   | GUID \_ WICPixelFormat48bppRGBFixedPoint   |
| GUID \_ WICPixelFormat16bppGrayFixedPoint  | GUID \_ WICPixelFormat16bppGrayFixedPoint  |
| GUID \_ WICPixelFormat32bppBGR101010       | GUID \_ WICPixelFormat32bppBGR101010       |
| GUID \_ WICPixelFormat48bppRGB             | GUID \_ WICPixelFormat48bppRGB             |
| GUID \_ WICPixelFormat64bppRGBA            | GUID \_ WICPixelFormat64bppRGBA            |
| GUID \_ WICPixelFormat96bppRGBFixedPoint   | GUID \_ WICPixelFormat96bppRGBFixedPoint   |
| GUID \_ WICPixelFormat96bppRGBFixedPoint   | GUID \_ WICPixelFormat128bppRGBAFloat      |
| GUID \_ WICPixelFormat128bppRGBFloat       | GUID \_ WICPixelFormat128bppRGBFloat       |
| GUID \_ WICPixelFormat32bppCMYK            | GUID \_ WICPixelFormat32bppCMYK            |
| GUID \_ WICPixelFormat64bppRGBAFixedPoint  | GUID \_ WICPixelFormat64bppRGBAFixedPoint  |
| GUID \_ WICPixelFormat128bppRGBAFixedPoint | GUID \_ WICPixelFormat128bppRGBAFixedPoint |
| GUID \_ WICPixelFormat64bppCMYK            | GUID \_ WICPixelFormat64bppCMYK            |
| GUID \_ WICPixelFormat24bpp3Channels       | GUID \_ WICPixelFormat24bpp3Channels       |
| GUID \_ WICPixelFormat32bpp4Channels       | GUID \_ WICPixelFormat32bpp4Channels       |
| GUID \_ WICPixelFormat40bpp5Channels       | GUID \_ WICPixelFormat40bpp5Channels       |
| GUID \_ WICPixelFormat48bpp6Channels       | GUID \_ WICPixelFormat48bpp6Channels       |
| GUID \_ WICPixelFormat56bpp7Channels       | GUID \_ WICPixelFormat56bpp7Channels       |
| GUID \_ WICPixelFormat64bpp8Channels       | GUID \_ WICPixelFormat64bpp8Channels       |
| GUID \_ WICPixelFormat48bpp3Channels       | GUID \_ WICPixelFormat48bpp3Channels       |
| GUID \_ WICPixelFormat64bpp4Channels       | GUID \_ WICPixelFormat64bpp4Channels       |
| GUID \_ WICPixelFormat80bpp5Channels       | GUID \_ WICPixelFormat80bpp5Channels       |
| GUID \_ WICPixelFormat96bpp6Channels       | GUID \_ WICPixelFormat96bpp6Channels       |
| GUID \_ WICPixelFormat112bpp7Channels      | GUID \_ WICPixelFormat112bpp7Channels      |
| GUID \_ WICPixelFormat128bpp8Channels      | GUID \_ WICPixelFormat128bpp8Channels      |
| GUID \_ WICPixelFormat40bppCMYKAlpha       | GUID \_ WICPixelFormat40bppCMYKAlpha       |
| GUID \_ WICPixelFormat80bppCMYKAlpha       | GUID \_ WICPixelFormat80bppCMYKAlpha       |
| GUID \_ WICPixelFormat32bpp3ChannelsAlpha  | GUID \_ WICPixelFormat32bpp3ChannelsAlpha  |
| GUID \_ WICPixelFormat64bpp7ChannelsAlpha  | GUID \_ WICPixelFormat40bpp4ChannelsAlpha  |
| GUID \_ WICPixelFormat72bpp8ChannelsAlpha  | GUID \_ WICPixelFormat48bpp5ChannelsAlpha  |
| GUID \_ WICPixelFormat64bpp3ChannelsAlpha  | GUID \_ WICPixelFormat56bpp6ChannelsAlpha  |
| GUID \_ WICPixelFormat80bpp4ChannelsAlpha  | GUID \_ WICPixelFormat64bpp7ChannelsAlpha  |
| GUID \_ WICPixelFormat96bpp5ChannelsAlpha  | GUID \_ WICPixelFormat72bpp8ChannelsAlpha  |
| GUID \_ WICPixelFormat112bpp6ChannelsAlpha | GUID \_ WICPixelFormat64bpp3ChannelsAlpha  |
| GUID \_ WICPixelFormat128bpp7ChannelsAlpha | GUID \_ WICPixelFormat80bpp4ChannelsAlpha  |
| GUID \_ WICPixelFormat144bpp8ChannelsAlpha | GUID \_ WICPixelFormat96bpp5ChannelsAlpha  |
| GUID \_ WICPixelFormat64bppRGBAHalf        | GUID \_ WICPixelFormat112bpp6ChannelsAlpha |
| GUID \_ WICPixelFormat48bppRGBHalf         | GUID \_ WICPixelFormat128bpp7ChannelsAlpha |
| GUID \_ WICPixelFormat32bppRGBE            | GUID \_ WICPixelFormat144bpp8ChannelsAlpha |
| GUID \_ WICPixelFormat16bppGrayHalf        | GUID \_ WICPixelFormat64bppRGBAHalf        |
| GUID \_ WICPixelFormat32bppGrayFixedPoint  | GUID \_ WICPixelFormat48bppRGBHalf         |
| GUID \_ WICPixelFormat64bppRGBFixedPoint   | GUID \_ WICPixelFormat32bppRGBE            |
| GUID \_ WICPixelFormat128bppRGBFixedPoint  | GUID \_ WICPixelFormat16bppGrayHalf        |
| GUID \_ WICPixelFormat64bppRGBHalf         | GUID \_ WICPixelFormatBlackWhite           |



 

## <a name="dds-native-codec"></a>Codec natif DDS



| Formats de pixel du décodeur          | Formats de pixel de l’encodeur          |
|--------------------------------|--------------------------------|
| GUID \_ WICPixelFormat32bppBGRA  | GUID \_ WICPixelFormat32bppBGRA  |
| GUID \_ WICPixelFormat32bppPBGRA | GUID \_ WICPixelFormat32bppPBGRA |



 

> [!Note]  
> Le codec Windows DDS fourni prend en charge les fichiers DDS encodés à l’aide des valeurs de format DXGI suivantes \_ :

 

-   DXGI \_ format \_ BC1 \_ UNORM
-   DXGI \_ format \_ BC2 \_ UNORM
-   DXGI \_ format \_ BC3 \_ UNORM

Ils sont décodés et codés en tant que GUID \_ WICPixelFormat32bppBGRA ou GUID \_ WICPixelFormat32bppPBGRA. Pour plus d’informations, consultez [vue d’ensemble du format DDS](dds-format-overview.md).

## <a name="pixel-format-extensibility"></a>Extensibilité du format de pixel

Les formats d’image personnalisés peuvent utiliser des formats de pixel qui ne sont pas fournis en mode natif par WIC, par exemple YCbCr (YUV) et YCCK (Y/CB/CR/K). WIC fournit un modèle d’extensibilité qui permet aux formats de pixel intégrés et compléments de fonctionner dans le même pipeline d’acquisition d’images. Pour intégrer ces formats de pixels au pipeline d’imagerie WIC, vous devez créer des convertisseurs de format de pixel pour convertir les formats de pixel de complément en un ou plusieurs des formats de pixel natifs. L’interface principale pour la génération de convertisseurs de format est [**IWICFormatConverter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicformatconverter).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

**Méthodologique**
</dt> <dt>

[Vue d’ensemble du composant Windows Imaging](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[GUID et CLSID WIC](-wic-guids-clsids.md)
</dt> <dt>

**Autres ressources**
</dt> <dt>

[Comment écrire un CODEC WIC-Enabled](-wic-howtowriteacodec.md)
</dt> <dt>

[Spécification de photo HD 1,0](https://www.microsoft.com/whdc/xps/wmphoto.mspx)
</dt> </dl>

 

 
