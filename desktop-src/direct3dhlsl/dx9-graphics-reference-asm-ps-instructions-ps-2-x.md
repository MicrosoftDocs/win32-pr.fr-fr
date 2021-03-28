---
title: Instructions ps_2_x
description: Cette section contient des informations de référence pour les instructions de nuanceur de pixels version 2 \_ x.
ms.assetid: a9b5f9dd-1139-4f80-ada6-e2fc0fb7effe
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 047067d26f9b85ef981a007059d9f2e87ae28ce3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104971751"
---
# <a name="ps_2_x-instructions"></a>\_instructions PS 2 \_ x

Cette section contient des informations de référence pour les instructions de nuanceur de pixels version 2 \_ x.

Il existe plusieurs types d’instructions de nuanceur de pixels, comme indiqué dans le tableau. Les colonnes à droite indiquent les éléments suivants :

-   Emplacements d’instruction : nombre d’emplacements d’instruction utilisés par chaque instruction.
-   Programme d’installation : un nuanceur de pixels doit avoir une instruction de version et doit être la première instruction.
-   Arithmétique : ces instructions fournissent les opérations mathématiques dans un nuanceur.
-   Texture : ces instructions permettent de charger et d’échantillonner des données de texture, et de modifier des coordonnées de texture.
-   Contrôle de flow : ces instructions fournissent un contrôle de workflow statique et dynamique à l’exécution des instructions.
-   Nouveauté : ces instructions sont nouvelles dans cette version.

## <a name="instruction-set"></a>Jeu d'instructions



| Nom                                                             | Description                                                                                      | Emplacements des instructions | Programme d’installation | Arithmétique | Texture | Contrôle de flux | Nouveau |
|------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|-------------------|-------|------------|---------|--------------|-----|
| [ABS-PS](abs---ps.md)                                         | Valeur absolue                                                                                   | 1                 |       | x          |         |              |     |
| [Add-PS](add---ps.md)                                         | Ajouter deux vecteurs                                                                                  | 1                 |       | x          |         |              |     |
| [Break-PS](break---ps.md)                                     | Sortir d’un REP... bloc endrep                                                                | 1                 |       |            |         | x            | x   |
| [arrêter \_ COMP-PS](break-comp---ps.md)                          | Sortir d’un REP de manière conditionnelle... bloc endrep, avec comparaison                               | 3                 |       |            |         | x            | x   |
| [breakp-PS](break-p---ps.md)                                  | Sortir d’un REP... bloc endrep, basé sur un prédicat                                          | 3                 |       |            |         | x            | x   |
| [appeler-PS](call---ps.md)                                       | Appeler une sous-routine                                                                                | 2                 |       |            |         | x            | x   |
| [callnz bool-PS](callnz-bool---ps.md)                         | Appeler une sous-routine si un registre booléen n’est pas égal à zéro                                              | 3                 |       |            |         | x            | x   |
| [callnz prédit-PS](callnz-pred---ps.md)                         | Appeler une sous-routine si un registre de prédicat n’est pas égal à zéro                                            | 3                 |       |            |         | x            | x   |
| [CMP-PS](cmp---ps.md)                                         | Comparer la source à 0                                                                              | 1                 |       | x          |         |              |     |
| [CRS-PS](crs---ps.md)                                         | Produit croisé                                                                                    | 2                 |       | x          |         |              |     |
| [DCL \_ samplerType (SM2, SM3-PS ASM)](dcl-samplertype---ps.md) | Déclarer la dimension de texture pour un échantillonneur                                                      | 0                 | x     |            |         |              |     |
| [DCL-(SM2, SM3-PS ASM)](dcl---ps.md)                        | Déclarez l’association entre les registres de sortie du nuanceur de sommets et les registres d’entrée de nuanceur de pixels. | 0                 | x     |            |         |              |     |
| [def-PS](def---ps.md)                                         | Définir des constantes                                                                                 | 0                 | x     |            |         |              |     |
| [defb-PS](defb---ps.md)                                       | Définir une constante booléenne                                                                        | 0                 | x     |            |         |              | x   |
| [DEFAUT-PS](defi---ps.md)                                       | Définir une constante entière                                                                       | 0                 | x     |            |         |              | x   |
| [dp2add-PS](dp2add---ps.md)                                   | produit 2D point et ajouter                                                                           | 2                 |       | x          |         |              |     |
| [DP3-PS](dp3---ps.md)                                         | produit point 3D                                                                                   | 1                 |       | x          |         |              |     |
| [DP4-PS](dp4---ps.md)                                         | produit point 4D                                                                                   | 1                 |       | x          |         |              |     |
| [DSX-PS](dsx---ps.md)                                         | Taux de modification de l’axe x                                                                | 2                 |       | x          |         |              | x   |
| [DSY-PS](dsy---ps.md)                                         | Taux de variation sur la direction y                                                                | 2                 |       | x          |         |              | x   |
| [else-PS](else---ps.md)                                       | Commencer un bloc Else                                                                              | 1                 |       |            |         | x            | x   |
| [endif-PS](endif---ps.md)                                     | Terminer un if... bloc Else                                                                           | 1                 |       |            |         | x            | x   |
| [endrep-PS](endrep---ps.md)                                   | Fin d’un bloc REPEAT                                                                            | 2                 |       |            |         | x            | x   |
| [exp-PS](exp---ps.md)                                         | Précision totale 2<sup>x</sup>                                                                     | 1                 |       | x          |         |              |     |
| [FRC-PS](frc---ps.md)                                         | Composant fractionnaire                                                                             | 1                 |       | x          |         |              |     |
| [Si bool-PS](if-bool---ps.md)                                 | Commencer un bloc If                                                                                | 3                 |       |            |         | x            | x   |
| [Si \_ COMP-PS](if-comp---ps.md)                                | Commencer un bloc If par une comparaison                                                              | 3                 |       |            |         | x            | x   |
| [Si prédit-PS](if-pred---ps.md)                                 | Commencer un bloc If avec un prédicat                                                               | 3                 |       |            |         | x            | x   |
| [étiquette-PS](label---ps.md)                                     | Étiquette                                                                                            | 0                 |       |            |         | x            | x   |
| [Journal-PS](log---ps.md)                                         | ₂ du journal de précision complète (x)                                                                           | 1                 |       | x          |         |              |     |
| [LRP-PS](lrp---ps.md)                                         | Interpolation linéaire                                                                               | 2                 |       | x          |         |              |     |
| [M3X2-PS](m3x2---ps.md)                                       | matrice multiplier                                                                                     | 2                 |       | x          |         |              |     |
| [M3x3-PS](m3x3---ps.md)                                       | 3 x 3                                                                                     | 3                 |       | x          |         |              |     |
| [M3x4-PS](m3x4---ps.md)                                       | 3x4 multiplier                                                                                     | 4                 |       | x          |         |              |     |
| [m4x3-PS](m4x3---ps.md)                                       | 4x3 multiplier                                                                                     | 3                 |       | x          |         |              |     |
| [M4X4-PS](m4x4---ps.md)                                       | 4 x 4                                                                                     | 4                 |       | x          |         |              |     |
| [Mad-PS](mad---ps.md)                                         | Multiplier et ajouter                                                                                 | 1                 |       | x          |         |              |     |
| [Max-PS](max---ps.md)                                         | Maximale                                                                                          | 1                 |       | x          |         |              |     |
| [min-PS](min---ps.md)                                         | Minimum                                                                                          | 1                 |       | x          |         |              |     |
| [MOV-PS](mov---ps.md)                                         | Déplacer                                                                                             | 1                 |       | x          |         |              |     |
| [Mul-PS](mul---ps.md)                                         | Multiplier                                                                                         | 1                 |       | x          |         |              |     |
| [NOP-PS](nop---ps.md)                                         | Pas d'opération                                                                                     | 1                 |       | x          |         |              |     |
| [NRM-PS](nrm---ps.md)                                         | Normaliser                                                                                        | 3                 |       | x          |         |              |     |
| [Pow-PS](pow---ps.md)                                         | x<sup>y</sup>                                                                                    | 3                 |       | x          |         |              |     |
| [alimentation](ps---ps.md)                                                | Version                                                                                          | 0                 | x     |            |         |              |     |
| [RCP-PS](rcp---ps.md)                                         | Mutuel                                                                                       | 1                 |       | x          |         |              |     |
| [REP-PS](rep---ps.md)                                         | Répéter                                                                                           | 3                 |       |            |         | x            | x   |
| [RET-PS](ret---ps.md)                                         | Fin d’une sous-routine                                                                              | 1                 |       |            |         | x            | x   |
| [rsq-PS](rsq---ps.md)                                         | Racine carrée réciproque                                                                           | 1                 |       | x          |         |              |     |
| [\_COMP setp](setp-comp---ps.md)                                 | Définir le registre de prédicat                                                                       | 1                 |       |            |         | x            | x   |
| [SinCos,-PS](sincos---ps.md)                                   | Sinus et cosinus                                                                                  | 8                 |       | x          |         |              |     |
| [sous-PS](sub---ps.md)                                         | Soustraire                                                                                         | 1                 |       | x          |         |              |     |
| [texkill-PS](texkill---ps.md)                                 | Arrêter le rendu de pixel                                                                                | Voir la remarque 1        |       |            | x       |              |     |
| [texld-PS \_ 2 \_ 0 et haut](texld---ps-2-0.md)                    | Échantillonner une texture                                                                                 | Voir la remarque 2        |       |            | x       |              |     |
| [texldb-PS](texldb---ps.md)                                   | Échantillonnage de texture avec décalage de niveau de détail par rapport à w-Component                                      | Voir la remarque 3        |       |            | x       |              |     |
| [texldd-PS](texldd---ps.md)                                   | Échantillonnage de texture avec des dégradés fournis par l’utilisateur                                                    | 3                 |       |            | x       |              | x   |
| [texldp-PS](texldp---ps.md)                                   | Échantillonnage de texture avec division projectaire par w-Component                                           | Voir la remarque 4        |       |            | x       |              |     |



 

Remarques :

1.  Si [**D3DD3DPSHADERCAPS2 \_ 0 \_ NOTEXINSTRUCTIONLIMIT**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0) est défini, emplacements = 2 ; sinon, emplacements = 1.
2.  Si [**D3DD3DPSHADERCAPS2 \_ 0 \_ NOTEXINSTRUCTIONLIMIT**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0) est défini et que la texture est un mappage de cube, emplacements = 4 ; sinon slot = 1.
3.  Si [**D3DD3DPSHADERCAPS2 \_ 0 \_ NOTEXINSTRUCTIONLIMIT**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0) est défini, slots = 6 ; sinon, emplacements = 1.
4.  Si [**D3DD3DPSHADERCAPS2 \_ 0 \_ NOTEXINSTRUCTIONLIMIT**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0) n’est pas défini, slots = 1 ; sinon :
    -   Si [**D3DD3DPSHADERCAPS2 \_ 0 \_ NOTEXINSTRUCTIONLIMIT**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0) est défini et que la texture est un mappage de cube, emplacements = 4.
    -   Si [**D3DD3DPSHADERCAPS2 \_ 0 \_ NOTEXINSTRUCTIONLIMIT**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0) est défini et que la texture n’est pas un mappage de cube, emplacements = 3.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Instructions sur le nuanceur de pixels](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 