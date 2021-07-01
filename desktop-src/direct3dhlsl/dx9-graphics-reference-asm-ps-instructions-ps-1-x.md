---
title: Instructions ps_1_1, ps_1_2, ps_1_3, ps_1_4
description: Cette section contient des informations de référence pour les instructions de nuanceur de pixels version 1 \_ X.
ms.assetid: cb496887-6755-4f29-b465-a36548b88722
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: cc624c3f3b64d41f428f68fcf2643f4600dcdec1
ms.sourcegitcommit: 7e4322a6ec1f964d5ad26e2e5e06cc8ce840030e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/01/2021
ms.locfileid: "113129897"
---
# <a name="ps_1_1-ps_1_2-ps_1_3-ps_1_4-instructions"></a>PS \_ 1 \_ 1, PS \_ 1 \_ 2, PS \_ 1 \_ 3, PS \_ 1 \_ 4-instructions

Cette section contient des informations de référence pour les instructions de nuanceur de pixels version 1 \_ X.

Il existe plusieurs types d’instructions de nuanceur de pixels, comme indiqué dans le tableau suivant.

## <a name="instruction-set"></a>Jeu d'instructions



| Version                                    | Description                                                                   | Emplacements des instructions | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 |
|--------------------------------------------|-------------------------------------------------------------------------------|-------------------|------|------|------|------|
| [alimentation](ps---ps.md)                          | Numéro de version                                                                | 0                 | x    | x    | x    | x    |
| Instructions de constante                      |                                                                               |                   | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 |
| [def-PS](def---ps.md)                   | Définir des constantes                                                              | 0                 | x    | x    | x    | x    |
| Instructions de phase                         |                                                                               |                   | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 |
| [phase-PS](phase---ps.md)               | Transition entre la phase 1 et la phase 2                                        | 0                 |      |      |      | x    |
| Instructions arithmétiques                    |                                                                               |                   | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 |
| [Add-PS](add---ps.md)                   | Ajouter deux vecteurs                                                               | 1                 | x    | x    | x    | x    |
| [Bem-PS](bem---ps.md)                   | Appliquer un environnement de bosselage factice-transformation de mappage                                   | 2                 |      |      |      | x    |
| [CMP-PS](cmp---ps.md)                   | Comparer la source à 0                                                           | 1 ¹                |      | x    | x    | x    |
| [CND-PS](cnd---ps.md)                   | Comparer la source à 0,5                                                         | 1                 | x    | x    | x    | x    |
| [DP3-PS](dp3---ps.md)                   | Produit scalaire à trois composants                                                   | 1                 | x    | x    | x    | x    |
| [DP4-PS](dp4---ps.md)                   | Produit scalaire à quatre composants                                                    | 1 ¹                |      | x    | x    | x    |
| [LRP-PS](lrp---ps.md)                   | Interpolation linéaire                                                            | 1                 | x    | x    | x    | x    |
| [Mad-PS](mad---ps.md)                   | Multiplier et ajouter                                                              | 1                 | x    | x    | x    | x    |
| [MOV-PS](mov---ps.md)                   | Déplacer                                                                          | 1                 | x    | x    | x    | x    |
| [Mul-PS](mul---ps.md)                   | Multiplier                                                                      | 1                 | x    | x    | x    | x    |
| [NOP-PS](nop---ps.md)                   | Pas d'opération                                                                  | 0                 | x    | x    | x    | x    |
| [sous-PS](sub---ps.md)                   | Soustraire                                                                      | 1                 | x    | x    | x    | x    |
| Instructions de texture                       |                                                                               |                   | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 |
| [Tex-PS](tex---ps.md)                   | Échantillonner une texture                                                              | 1                 | x    | x    | x    |      |
| [texbem-PS](texbem---ps.md)             | Appliquer un environnement de bosselage factice-transformation de mappage                                   | 1                 | x    | x    | x    |      |
| [texbeml-PS](texbeml---ps.md)           | Appliquer un environnement factice-transformation de la carte avec correction de luminance         | 1 +1 ²              | x    | x    | x    |      |
| [texcoord-PS](texcoord---ps.md)         | Interpréter les données de coordonnée de texture comme des données de couleur                               | 1                 | x    | x    | x    |      |
| [texcrd-PS](texcrd---ps.md)             | Copier les données de coordonnée de texture en tant que données de couleur                                    | 1                 |      |      |      | x    |
| [texdepth-PS](texdepth---ps.md)         | Calculer les valeurs de profondeur                                                        | 1                 |      |      |      | x    |
| [texdp3-PS](texdp3---ps.md)             | Produit scalaire à trois composants entre les données de texture et les coordonnées de texture  | 1                 |      | x    | x    |      |
| [texdp3tex-PS](texdp3tex---ps.md)       | Produit scalaire à trois composants et recherche de texture 1D                             | 1                 |      | x    | x    |      |
| [texkill-PS](texkill---ps.md)           | Annule le rendu des pixels en fonction d’une comparaison                             | 1                 | x    | x    | x    | x    |
| [texld-PS \_ 1 \_ 4](texld---ps-1-4.md)     | Échantillonner une texture                                                              | 1                 |      |      |      | x    |
| [texm3x2depth-PS](texm3x2depth---ps.md) | Calculer les valeurs de profondeur par pixel                                              | 1                 |      |      | x    |      |
| [texm3x2pad-PS](texm3x2pad---ps.md)     | Matrice de la première ligne, multiplication d’une matrice de deux lignes                        | 1                 | x    | x    | x    |      |
| [texm3x2tex-PS](texm3x2tex---ps.md)     | Matrice de lignes finale de multiplication d’une matrice de deux lignes                        | 1                 | x    | x    | x    |      |
| [texm3x3-PS](texm3x3---ps.md)           | multiplication de matrice 3x3                                                           | 1                 |      | x    | x    |      |
| [texm3x3pad-PS](texm3x3pad---ps.md)     | Multiplication de la première ligne ou de la deuxième ligne d’une matrice à trois lignes                   | 1                 | x    | x    | x    |      |
| [texm3x3spec-PS](texm3x3spec---ps.md)   | Multiplication de la dernière ligne d’une matrice de trois lignes                             | 1                 | x    | x    | x    |      |
| [texm3x3tex-PS](texm3x3tex---ps.md)     | Recherche de texture à l’aide d’une multiplication de matrice 3x3                                   | 1                 | x    | x    | x    |      |
| [texm3x3vspec-PS](texm3x3vspec---ps.md) | Recherche de texture à l’aide d’une matrice 3x3, avec un vecteur de rayon oculaire non constant | 1                 | x    | x    | x    |      |
| [texreg2ar-PS](texreg2ar---ps.md)       | Échantillonner une texture à l’aide des composants alpha et rouge                           | 1                 | x    | x    | x    |      |
| [texreg2gb-PS](texreg2gb---ps.md)       | Échantillonner une texture à l’aide des composants vert et bleu                          | 1                 | x    | x    | x    |      |
| [texreg2rgb-PS](texreg2rgb---ps.md)     | Échantillonner une texture à l’aide des composants rouge, vert et bleu                     | 1                 |      | x    | x    |      |



 

1.  1 emplacement dans le PS \_ 1 \_ 4 ; 2 emplacements dans PS \_ 1 \_ 2 et PS \_ 1 \_ 3
2.  1 + 1 = 1 instruction arithmétique + 1 instruction de texture

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Instructions sur le nuanceur de pixels](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




