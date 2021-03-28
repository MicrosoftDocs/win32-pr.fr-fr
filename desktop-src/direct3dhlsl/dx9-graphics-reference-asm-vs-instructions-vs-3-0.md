---
title: Instructions-vs_3_0
description: Cette section contient des informations de référence pour les instructions du nuanceur vertex version 3 \_ 0.
ms.assetid: 2309a643-dec8-4f2a-a217-e7f1e90b5f43
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 9f134c47f5697381c211808ce5a46ab5ee23031b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103940110"
---
# <a name="instructions---vs_3_0"></a>Instructions-vs \_ 3 \_ 0

Cette section contient des informations de référence pour les instructions du nuanceur vertex version 3 \_ 0.

Il existe plusieurs types d’instructions de nuanceur de sommets, comme indiqué dans le tableau. Les colonnes à droite indiquent les éléments suivants :

-   Emplacements d’instruction : nombre d’emplacements d’instruction utilisés par chaque instruction.
-   Configuration-instructions non arithmétiques. Chaque nuanceur doit avoir une instruction de version et doit être la première instruction.
-   Arithmétique : ces instructions fournissent les opérations mathématiques dans un nuanceur.
-   Texture : ces instructions prennent en charge la recherche d’adresses de texture.
-   Contrôle de la fluidité : ces instructions ajoutent un contrôle de Flow comme des boucles, des répétitions et [si bool-vs](if-bool---vs.md)... [sinon](else---vs.md)... [endif](endif---vs.md) (comparaisons).
-   Nouveauté : ces instructions sont nouvelles dans cette version.

## <a name="instruction-set"></a>Jeu d'instructions



| Nom                                                                           | Description                                                                                                                                                            | Emplacements des instructions | Programme d’installation | Arithmétique | Texture | Contrôle de flux | Nouveau |
|--------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------|-------|------------|---------|--------------|-----|
| [ABS-vs](abs---vs.md)                                                       | Valeur absolue                                                                                                                                                         | 1                 |       | x          |         |              |     |
| [Ajouter-vs](add---vs.md)                                                       | Ajouter deux vecteurs                                                                                                                                                        | 1                 |       | x          |         |              |     |
| [Break-vs](break---vs.md)                                                   | Sortir d’une [boucle-vs](loop---vs.md)... [ENDLOOP-vs](endloop---vs.md) ou [REP](rep---vs.md)... bloc [endrep](endrep---vs.md)                                  | 1                 |       |            |         | x            |     |
| [arrêt \_ COMP-vs](break-comp---vs.md)                                        | Sortir de manière conditionnelle d’une [boucle-vs](loop---vs.md)... [ENDLOOP-vs](endloop---vs.md) ou [REP](rep---vs.md)... bloc [endrep](endrep---vs.md) , avec comparaison | 3                 |       |            |         | x            |     |
| [breakp-vs](breakp---vs.md)                                                 | Sortir d’une [boucle-vs](loop---vs.md)... [ENDLOOP-vs](endloop---vs.md) ou [REP](rep---vs.md)... bloc [endrep](endrep---vs.md) , basé sur un prédicat            | 3                 |       |            |         | x            |     |
| [appel-vs](call---vs.md)                                                     | Appeler une sous-routine                                                                                                                                                      | 2                 |       |            |         | x            |     |
| [callnz bool-vs](callnz-bool---vs.md)                                       | Appeler une sous-routine si un registre booléen n’est pas égal à zéro                                                                                                                    | 3                 |       |            |         | x            |     |
| [callnz prédit-vs](callnz-pred---vs.md)                                       | Appeler une sous-routine si un registre de prédicat n’est pas égal à zéro                                                                                                                  | 3                 |       |            |         | x            |     |
| [CRS-vs](crs---vs.md)                                                       | Produit croisé                                                                                                                                                          | 2                 |       | x          |         |              |     |
| [\_entrée d’utilisation DCL (SM1, SM2, SM3-vs ASM)](dcl-usage-input-register---vs.md) | Déclarer des registres de vertex d’entrée (voir [registres-vs \_ 3 \_ 0](dx9-graphics-reference-asm-vs-registers-vs-3-0.md))                                                        | 0                 | x     |            |         |              |     |
| [DCL \_ samplerType (SM3-vs ASM)](dcl-samplertype---vs.md)                    | Déclarer la dimension de texture pour un échantillonneur                                                                                                                            | 0                 | x     |            |         |              | x   |
| [def-vs](def---vs.md)                                                       | Définir des constantes                                                                                                                                                       | 0                 | x     |            |         |              |     |
| [defb-vs](defb---vs.md)                                                     | Déclarer une constante booléenne                                                                                                                                             | 0                 | x     |            |         |              |     |
| [signatures-vs](defi---vs.md)                                                     | Déclarer une constante entière                                                                                                                                            | 0                 | x     |            |         |              |     |
| [DP3-vs](dp3---vs.md)                                                       | Produit scalaire à trois composants                                                                                                                                            | 1                 |       | x          |         |              |     |
| [DP4-vs](dp4---vs.md)                                                       | Produit scalaire à quatre composants                                                                                                                                             | 1                 |       | x          |         |              |     |
| [DST-vs](dst---vs.md)                                                       | Distance                                                                                                                                                               | 1                 |       | x          |         |              |     |
| [else-vs](else---vs.md)                                                     | Commencer un bloc [else](else---vs.md)                                                                                                                                   | 1                 |       |            |         | x            |     |
| [endif-vs](endif---vs.md)                                                   | Terminer une [si bool-vs](if-bool---vs.md)... bloc [else](else---vs.md)                                                                                                  | 1                 |       |            |         | x            |     |
| [ENDLOOP-vs](endloop---vs.md)                                               | Fin d’un bloc de [boucle-vs](loop---vs.md)                                                                                                                              | 2                 |       |            |         | x            |     |
| [endrep-vs](endrep---vs.md)                                                 | Fin d’un bloc REPEAT                                                                                                                                                  | 2                 |       |            |         | x            |     |
| [exp-vs](exp---vs.md)                                                       | Précision totale 2<sup>x</sup>                                                                                                                                           | 1                 |       | x          |         |              |     |
| [exp-vs](exp---vs.md)                                                       | Précision partielle 2<sup>x</sup>                                                                                                                                        | 1                 |       | x          |         |              |     |
| [FRC-vs](frc---vs.md)                                                       | Composant fractionnaire                                                                                                                                                   | 1                 |       | x          |         |              |     |
| [Si bool-vs](if-bool---vs.md)                                               | Commencer un bloc [If bool-vs](if-bool---vs.md) (à l’aide d’une condition booléenne)                                                                                            | 3                 |       |            |         | x            |     |
| [Si \_ COMP-vs](if-comp---vs.md)                                              | Commencer un bloc [If bool-vs](if-bool---vs.md) , avec une comparaison                                                                                                     | 3                 |       |            |         | x            |     |
| [Si prédit-vs](if-pred---vs.md)                                               | Commencer un bloc [If bool-vs](if-bool---vs.md) avec une condition de prédicat                                                                                             | 3                 |       |            |         | x            |     |
| [étiquette-vs](label---vs.md)                                                   | Étiquette                                                                                                                                                                  | 0                 |       |            |         | x            |     |
| [lit-vs](lit---vs.md)                                                       | Calculer l’éclairage                                                                                                                                                     | 3                 |       | x          |         |              |     |
| [journalisation-vs](log---vs.md)                                                       | ₂ du journal de précision complète (x)                                                                                                                                                 | 1                 |       | x          |         |              |     |
| [logP-vs](logp---vs.md)                                                     | ₂ de journal de précision partielle (x)                                                                                                                                              | 1                 |       | x          |         |              |     |
| [boucle-vs](loop---vs.md)                                                     | Loop                                                                                                                                                                   | 3                 |       |            |         | x            |     |
| [LRP-vs](lrp---vs.md)                                                       | Interpolation linéaire                                                                                                                                                   | 2                 |       | x          |         |              |     |
| [M3X2-vs](m3x2---vs.md)                                                     | matrice multiplier                                                                                                                                                           | 2                 |       | x          |         |              |     |
| [M3x3-vs](m3x3---vs.md)                                                     | 3 x 3                                                                                                                                                           | 3                 |       | x          |         |              |     |
| [M3x4-vs](m3x4---vs.md)                                                     | 3x4 multiplier                                                                                                                                                           | 4                 |       | x          |         |              |     |
| [m4x3-vs](m4x3---vs.md)                                                     | 4x3 multiplier                                                                                                                                                           | 3                 |       | x          |         |              |     |
| [M4X4-vs](m4x4---vs.md)                                                     | 4 x 4                                                                                                                                                           | 4                 |       | x          |         |              |     |
| [Mad-vs](mad---vs.md)                                                       | Multiplier et ajouter                                                                                                                                                       | 1                 |       | x          |         |              |     |
| [Max-vs](max---vs.md)                                                       | Maximale                                                                                                                                                                | 1                 |       | x          |         |              |     |
| [min-vs](min---vs.md)                                                       | Minimum                                                                                                                                                                | 1                 |       | x          |         |              |     |
| [MOV-vs](mov---vs.md)                                                       | Déplacer                                                                                                                                                                   | 1                 |       | x          |         |              |     |
| [Mova-vs](mova---vs.md)                                                     | Déplacer des données à partir d’un registre à virgule flottante vers un registre d’entiers                                                                                                        | 1                 |       | x          |         |              |     |
| [Mul-vs](mul---vs.md)                                                       | Multiplier                                                                                                                                                               | 1                 |       | x          |         |              |     |
| [NOP-vs](nop---vs.md)                                                       | Pas d'opération                                                                                                                                                           | 1                 |       | x          |         |              |     |
| [NRM-vs](nrm---vs.md)                                                       | Normaliser                                                                                                                                                              | 3                 |       | x          |         |              |     |
| [Pow-vs](pow---vs.md)                                                       | x<sup>y</sup>                                                                                                                                                          | 3                 |       | x          |         |              |     |
| [RCP-vs](rcp---vs.md)                                                       | Mutuel                                                                                                                                                             | 1                 |       | x          |         |              |     |
| [REP-vs](rep---vs.md)                                                       | Répéter                                                                                                                                                                 | 3                 |       |            |         | x            |     |
| [RET-vs](ret---vs.md)                                                       | Fin d’une sous-routine                                                                                                                                                    | 1                 |       |            |         | x            |     |
| [rsq-vs](rsq---vs.md)                                                       | Racine carrée réciproque                                                                                                                                                 | 1                 |       | x          |         |              |     |
| [\_COMP setp-vs](setp-comp---vs.md)                                          | Définir le registre de prédicat                                                                                                                                             | 1                 |       |            |         | x            |     |
| [SGE-vs](sge---vs.md)                                                       | Comparaison supérieur ou égal à                                                                                                                                          | 1                 |       | x          |         |              |     |
| [SGN-vs](sgn---vs.md)                                                       | Sign (Signer)                                                                                                                                                                   | 3                 |       | x          |         |              |     |
| [SinCos,-vs](sincos---vs.md)                                                 | Sinus et cosinus                                                                                                                                                        | 8                 |       | x          |         |              |     |
| [des SLT-vs](slt---vs.md)                                                       | Inférieur à compare                                                                                                                                                      | 1                 |       | x          |         |              |     |
| [sous-vs](sub---vs.md)                                                       | Soustraire                                                                                                                                                               | 1                 |       | x          |         |              |     |
| [texldl-vs](texldl---vs.md)                                                 | Charge de texture avec un niveau de détail défini par l’utilisateur                                                                                                                      | Voir la remarque 1        |       |            | x       |              | x   |
| [comparatif](vs---vs.md)                                                              | Version                                                                                                                                                                | 0                 | x     |            |         |              |     |



 

Remarques :

-   Si la texture est un mappage de cube, emplacements = 5 ; Sinon, emplacements = 2

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Instructions du nuanceur de sommets](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




