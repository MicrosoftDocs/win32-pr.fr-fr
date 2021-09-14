---
description: Il existe deux façons d’encoder des cartes de texture qui présentent une transparence plus complexe.
ms.assetid: cae788f6-60f1-4987-8f06-bf4256bccd9b
title: Textures avec canaux alpha (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2c361b0335ef4f36b4efc9c90c71270e855f5db
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126924476"
---
# <a name="textures-with-alpha-channels-direct3d-9"></a>Textures avec canaux alpha (Direct3D 9)

Il existe deux façons d’encoder des cartes de texture qui présentent une transparence plus complexe. Dans chaque cas, un bloc qui décrit la transparence précède le bloc 64 bits déjà décrit. La transparence est représentée sous la forme d’une image bitmap 4x4 avec 4 bits par pixel (codage explicite), ou avec moins de bits et une interpolation linéaire analogue à ce qui est utilisé pour l’encodage des couleurs.

Le bloc de transparence et le bloc de couleur sont disposés comme indiqué dans le tableau suivant.



| Adresse du mot | bloc de bits 64                      |
|--------------|-----------------------------------|
| 3:0          | Bloc de transparence                |
| 7:4          | Précédemment décrit le bloc 64 bits |



 

## <a name="explicit-texture-encoding"></a>Encodage de texture explicite

Pour l’encodage de texture explicite (formats DXT2 et DXT3), les composants alpha des texels qui décrivent la transparence sont encodés dans une bitmap 4x4 avec 4 bits par Texel. Ces quatre bits peuvent être obtenus par le biais de différents moyens, tels que le tramage ou en utilisant les quatre bits les plus significatifs des données alpha. Toutefois, ils sont créés, mais ils sont utilisés de la même manière, sans aucune forme d’interpolation.

Le diagramme suivant montre un bloc de transparence 64 bits.

![diagramme d’un bloc de transparence 64 bits](images/colors4.png)

> [!Note]  
> La méthode de compression de Direct3D utilise les quatre bits les plus significatifs.

 

Les tableaux suivants montrent comment les informations alpha sont disposées en mémoire, pour chaque mot de 16 bits.

Ce tableau contient la disposition pour Word 0.



| Bits          | Alpha      |
|---------------|------------|
| 3:0 (LSB \* )   | \[0 \] \[ 0\] |
| 7:4           | \[0 \] \[ 1\] |
| 11:8          | \[0 \] \[ 2\] |
| 15:12 (MSB \* ) | \[0 \] \[ 3\] |



 

\*bit le moins significatif, bit le plus significatif (MSB)

Ce tableau contient la mise en page de Word 1.



| Bits        | Alpha      |
|-------------|------------|
| 3:0 (LSB)   | \[1 \] \[ 0\] |
| 7:4         | \[1 \] \[ 1\] |
| 11:8        | \[1 \] \[ 2\] |
| 15:12 (MSB) | \[1 \] \[ 3\] |



 

Ce tableau contient la disposition pour Word 2.



| Bits        | Alpha      |
|-------------|------------|
| 3:0 (LSB)   | \[2 \] \[ 0\] |
| 7:4         | \[2 \] \[ 1\] |
| 11:8        | \[2 \] \[ 2\] |
| 15:12 (MSB) | \[2 \] \[ 3\] |



 

Ce tableau contient la disposition pour Word 3.



| Bits        | Alpha      |
|-------------|------------|
| 3:0 (LSB)   | \[3 \] \[ 0\] |
| 7:4         | \[3 \] \[ 1\] |
| 11:8        | \[3 \] \[ 2\] |
| 15:12 (MSB) | \[3 \] \[ 3\] |



 

La différence entre DXT2 et DXT3 est que, dans le format DXT2, il est supposé que les données de couleur ont été prémultipliées par Alpha. Dans le format DXT3, il est supposé que la couleur n’est pas prémultipliée par Alpha. Ces deux formats sont nécessaires, car, dans la plupart des cas, au moment où une texture est utilisée, l’examen des données n’est pas suffisant pour déterminer si les valeurs de couleur ont été multipliées par Alpha. Étant donné que ces informations sont nécessaires au moment de l’exécution, les deux codes FOURCC sont utilisés pour différencier ces cas. Toutefois, les données et la méthode d’interpolation utilisées pour ces deux formats sont identiques.

La comparaison de couleurs utilisée dans DXT1 pour déterminer si le Texel est transparent n’est pas utilisé dans ce format. Il est supposé que, sans la couleur, les données de couleur sont toujours traitées comme si elles étaient en mode 4 couleurs. En d’autres termes, l’instruction if en haut du code DXT1 doit être la suivante :


```
if ((color_0 > color_1) OR !DXT1) {
```



## <a name="three-bit-linear-alpha-interpolation"></a>Three-Bit l’interpolation alpha linéaire

L’encodage de la transparence pour les formats DXT4 et DXT5 est basé sur un concept similaire à l’encodage linéaire utilisé pour la couleur. Les valeurs alpha 2 8 bits et une image bitmap 4x4 avec trois bits par pixel sont stockées dans les huit premiers octets du bloc. Les valeurs alpha représentatives sont utilisées pour interpoler les valeurs alpha intermédiaires. Des informations supplémentaires sont disponibles dans la manière dont les deux valeurs alpha sont stockées. Si alpha \_ 0 est supérieur à alpha \_ 1, les six valeurs alpha intermédiaires sont créées par l’interpolation. Dans le cas contraire, quatre valeurs alpha intermédiaires sont interpolées entre les caractères alpha extrêmes spécifiés. Les deux valeurs alpha implicites supplémentaires sont 0 (entièrement transparentes) et 255 (entièrement opaques).

L’exemple de code suivant illustre cet algorithme.


```
// 8-alpha or 6-alpha block?    
if (alpha_0 > alpha_1) {    
    // 8-alpha block:  derive the other six alphas.    
    // Bit code 000 = alpha_0, 001 = alpha_1, others are interpolated.
    alpha_2 = (6 * alpha_0 + 1 * alpha_1 + 3) / 7;    // bit code 010
    alpha_3 = (5 * alpha_0 + 2 * alpha_1 + 3) / 7;    // bit code 011
    alpha_4 = (4 * alpha_0 + 3 * alpha_1 + 3) / 7;    // bit code 100
    alpha_5 = (3 * alpha_0 + 4 * alpha_1 + 3) / 7;    // bit code 101
    alpha_6 = (2 * alpha_0 + 5 * alpha_1 + 3) / 7;    // bit code 110
    alpha_7 = (1 * alpha_0 + 6 * alpha_1 + 3) / 7;    // bit code 111  
}    
else {  
    // 6-alpha block.    
    // Bit code 000 = alpha_0, 001 = alpha_1, others are interpolated.
    alpha_2 = (4 * alpha_0 + 1 * alpha_1 + 2) / 5;    // Bit code 010
    alpha_3 = (3 * alpha_0 + 2 * alpha_1 + 2) / 5;    // Bit code 011
    alpha_4 = (2 * alpha_0 + 3 * alpha_1 + 2) / 5;    // Bit code 100
    alpha_5 = (1 * alpha_0 + 4 * alpha_1 + 2) / 5;    // Bit code 101
    alpha_6 = 0;                                      // Bit code 110
    alpha_7 = 255;                                    // Bit code 111
}
```



La disposition de la mémoire du bloc alpha est la suivante :



| Byte | Alpha                                                          |
|------|----------------------------------------------------------------|
| 0    | Alpha \_ 0                                                       |
| 1    | Alpha \_ 1                                                       |
| 2    | \[0 \] \[ 2 \] (2 MSBS), \[ 0 \] \[ \] \[ \] \[ 1,0\]                    |
| 3    | \[1 \] \[ 1 \] (1 MSB), \[ 1 \] \[ 0 \] , \[ 0 \] \[ 3 \] , \[ 0 \] \[ 2 \] (1 LSB) |
| 4    | \[1 \] \[ 3 \] , \[ 1 \] \[ 2 \] , \[ 1 \] \[ 1 \] (2 LSBs)                    |
| 5    | \[2 \] \[ 2 \] (2 MSBS), \[ 2 \] \[ 1 \] , \[ 2 \] \[ 0\]                    |
| 6    | \[3 \] \[ 1 \] (1 MSB), \[ 3 \] \[ 0 \] , \[ 2 \] \[ 3 \] , \[ 2 \] \[ 2 \] (1 LSB) |
| 7    | \[3 \] \[ 3 \] , \[ 3 \] \[ 2 \] , \[ 3 \] \[ 1 \] (2 LSBs)                    |



 

La différence entre DXT4 et DXT5 est que dans le format DXT4 il est supposé que les données de couleur ont été prémultipliées par Alpha. Dans le format DXT5, il est supposé que la couleur n’est pas prémultipliée par Alpha. Ces deux formats sont nécessaires, car, dans la plupart des cas, au moment où une texture est utilisée, l’examen des données n’est pas suffisant pour déterminer si les valeurs de couleur ont été multipliées par Alpha. Étant donné que ces informations sont nécessaires au moment de l’exécution, les deux codes FOURCC sont utilisés pour différencier ces cas. Toutefois, les données et la méthode d’interpolation utilisées pour ces deux formats sont identiques.

La comparaison de couleurs utilisée dans DXT1 pour déterminer si le Texel est transparent n’est pas utilisé avec ces formats. Il est supposé que, sans la couleur, les données de couleur sont toujours traitées comme si elles étaient en mode 4 couleurs. En d’autres termes, l’instruction if en haut du code DXT1 doit être :


```
if ((color_0 > color_1) OR !DXT1) {
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Ressources de texture compressées](compressed-texture-resources.md)
</dt> </dl>

 

 



