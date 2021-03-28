---
title: Instructions ps_2_0
description: Cette section contient des informations de référence pour les instructions de nuanceur de pixels version 2 \_ 0.
ms.assetid: 70492436-4d0d-48e6-b3d2-8934931fb5c2
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: bac2a70ed0147885174c2290d5e58c92ae3347e7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104990664"
---
# <a name="ps_2_0-instructions"></a>\_instructions PS 2 \_ 0

Cette section contient des informations de référence pour les instructions de nuanceur de pixels version 2 \_ 0.

Il existe plusieurs types d’instructions de nuanceur de pixels, comme indiqué dans le tableau. Les colonnes à droite indiquent les éléments suivants :

-   Emplacements d’instruction : nombre d’emplacements d’instruction utilisés par chaque instruction.
-   Programme d’installation : un nuanceur de pixels doit avoir une instruction de version et doit être la première instruction.
-   Arithmétique : ces instructions fournissent les opérations mathématiques dans un nuanceur.
-   Texture : ces instructions permettent de charger et d’échantillonner des données de texture, et de modifier des coordonnées de texture.
-   Nouveauté : ces instructions sont nouvelles dans cette version.

## <a name="instruction-set"></a>Jeu d'instructions



| Nom                                                             | Description                                                                                      | Emplacements des instructions | Programme d’installation | Arithmétique | Texture | Nouveau |
|------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|-------------------|-------|------------|---------|-----|
| [ABS-PS](abs---ps.md)                                         | Valeur absolue                                                                                   | 1                 |       | x          |         | x   |
| [Add-PS](add---ps.md)                                         | Ajouter deux vecteurs                                                                                  | 1                 |       | x          |         |     |
| [CMP-PS](cmp---ps.md)                                         | Comparer la source à 0                                                                              | 1                 |       | x          |         |     |
| [CRS-PS](crs---ps.md)                                         | Produit croisé                                                                                    | 2                 |       | x          |         | x   |
| [DCL \_ samplerType (SM2, SM3-PS ASM)](dcl-samplertype---ps.md) | Déclarer la dimension de texture pour un échantillonneur                                                      | 0                 | x     |            |         | x   |
| [DCL-(SM2, SM3-PS ASM)](dcl---ps.md)                        | Déclarez l’association entre les registres de sortie du nuanceur de sommets et les registres d’entrée de nuanceur de pixels. | 0                 | x     |            |         | x   |
| [def-PS](def---ps.md)                                         | Définir des constantes                                                                                 | 0                 | x     |            |         |     |
| [dp2add-PS](dp2add---ps.md)                                   | produit 2D point et ajouter                                                                           | 2                 |       | x          |         | x   |
| [DP3-PS](dp3---ps.md)                                         | produit point 3D                                                                                   | 1                 |       | x          |         |     |
| [DP4-PS](dp4---ps.md)                                         | produit point 4D                                                                                   | 1                 |       | x          |         |     |
| [exp-PS](exp---ps.md)                                         | Précision totale 2<sup>x</sup>                                                                     | 1                 |       | x          |         | x   |
| [FRC-PS](frc---ps.md)                                         | Composant fractionnaire                                                                             | 1                 |       | x          |         | x   |
| [Journal-PS](log---ps.md)                                         | ₂ du journal de précision complète (x)                                                                           | 1                 |       | x          |         | x   |
| [LRP-PS](lrp---ps.md)                                         | Interpolation linéaire                                                                               | 2                 |       | x          |         |     |
| [M3X2-PS](m3x2---ps.md)                                       | matrice multiplier                                                                                     | 2                 |       | x          |         | x   |
| [M3x3-PS](m3x3---ps.md)                                       | 3 x 3                                                                                     | 3                 |       | x          |         | x   |
| [M3x4-PS](m3x4---ps.md)                                       | 3x4 multiplier                                                                                     | 4                 |       | x          |         | x   |
| [m4x3-PS](m4x3---ps.md)                                       | 4x3 multiplier                                                                                     | 3                 |       | x          |         | x   |
| [M4X4-PS](m4x4---ps.md)                                       | 4 x 4                                                                                     | 4                 |       | x          |         | x   |
| [Mad-PS](mad---ps.md)                                         | Multiplier et ajouter                                                                                 | 1                 |       | x          |         |     |
| [Max-PS](max---ps.md)                                         | Maximale                                                                                          | 1                 |       | x          |         | x   |
| [min-PS](min---ps.md)                                         | Minimum                                                                                          | 1                 |       | x          |         | x   |
| [MOV-PS](mov---ps.md)                                         | Déplacer                                                                                             | 1                 |       | x          |         |     |
| [Mul-PS](mul---ps.md)                                         | Multiplier                                                                                         | 1                 |       | x          |         |     |
| [NOP-PS](nop---ps.md)                                         | Pas d'opération                                                                                     | 1                 |       | x          |         |     |
| [NRM-PS](nrm---ps.md)                                         | Normaliser                                                                                        | 3                 |       | x          |         | x   |
| [Pow-PS](pow---ps.md)                                         | x<sup>y</sup>                                                                                    | 3                 |       | x          |         | x   |
| [alimentation](ps---ps.md)                                                | Version                                                                                          | 0                 | x     |            |         |     |
| [RCP-PS](rcp---ps.md)                                         | Mutuel                                                                                       | 1                 |       | x          |         | x   |
| [rsq-PS](rsq---ps.md)                                         | Racine carrée réciproque                                                                           | 1                 |       | x          |         | x   |
| [SinCos,-PS](sincos---ps.md)                                   | Sinus et cosinus                                                                                  | 8                 |       | x          |         | x   |
| [sous-PS](sub---ps.md)                                         | Soustraire                                                                                         | 1                 |       | x          |         |     |
| [texkill-PS](texkill---ps.md)                                 | Arrêter le rendu de pixel                                                                                | 1                 |       |            | x       |     |
| [texld-PS \_ 2 \_ 0 et haut](texld---ps-2-0.md)                    | Échantillonner une texture                                                                                 | 1                 |       |            | x       | x   |
| [texldb-PS](texldb---ps.md)                                   | Échantillonnage de texture avec décalage de niveau de détail par rapport à w-Component                                      | 1                 |       |            | x       | x   |
| [texldp-PS](texldp---ps.md)                                   | Échantillonnage de texture avec division projectaire par w-Component                                           | 1                 |       |            | x       | x   |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Instructions sur le nuanceur de pixels](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




