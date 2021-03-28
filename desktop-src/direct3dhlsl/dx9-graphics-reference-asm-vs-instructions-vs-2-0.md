---
title: Instructions-vs_2_0
description: Cette section contient des informations de référence pour les instructions du nuanceur vertex version 2 \_ 0.
ms.assetid: f5ca3e44-3c71-4221-9381-cea521d984e0
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: bf8ea2dbe5d70cc4be8d3867cafc6127138f833a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104380165"
---
# <a name="instructions---vs_2_0"></a>Instructions-vs \_ 2 \_ 0

Cette section contient des informations de référence pour les instructions du nuanceur vertex version 2 \_ 0.

Il existe plusieurs types d’instructions de nuanceur de sommets, comme indiqué dans le tableau. Les colonnes à droite indiquent les éléments suivants :

-   Emplacements d’instruction : nombre d’emplacements d’instruction utilisés par chaque instruction.
-   Configuration-instructions non arithmétiques. Chaque nuanceur doit avoir une instruction de version et doit être la première instruction.
-   Arithmétique : ces instructions fournissent les opérations mathématiques dans un nuanceur.
-   Contrôle de flow : ces instructions ajoutent des fonctionnalités de contrôle de Flow, telles que [Loop](loop---vs.md)... [ENDLOOP](endloop---vs.md), [If](if-bool---vs.md)... [sinon](else---vs.md)... [endif-vs](endif---vs.md)et les appels de sous-routine.
-   Nouveauté : ces instructions sont nouvelles dans cette version.

## <a name="instruction-set"></a>Jeu d'instructions



| Nom                                                                           | Description                                                                                                     | Emplacements des instructions | Programme d’installation | Arithmétique | Contrôle de flux | Nouveau |
|--------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|-------------------|-------|------------|--------------|-----|
| [ABS-vs](abs---vs.md)                                                       | Valeur absolue                                                                                                  | 1                 |       | x          |              | x   |
| [Ajouter-vs](add---vs.md)                                                       | Ajouter deux vecteurs                                                                                                 | 1                 |       | x          |              |     |
| [appel-vs](call---vs.md)                                                     | Appeler une sous-routine                                                                                               | 2                 |       |            | x            | x   |
| [callnz bool-vs](callnz-bool---vs.md)                                       | Appeler une sous-routine si un registre booléen n’est pas égal à zéro                                                             | 3                 |       |            | x            | x   |
| [CRS-vs](crs---vs.md)                                                       | Produit croisé                                                                                                   | 2                 |       | x          |              | x   |
| [\_entrée d’utilisation DCL (SM1, SM2, SM3-vs ASM)](dcl-usage-input-register---vs.md) | Déclarer des registres de vertex d’entrée (voir [registres-vs \_ 2 \_ 0](dx9-graphics-reference-asm-vs-registers-vs-2-0.md)) | 0                 | x     |            |              |     |
| [def-vs](def---vs.md)                                                       | Définir des constantes                                                                                                | 0                 | x     |            |              |     |
| [defb-vs](defb---vs.md)                                                     | Définir une constante booléenne                                                                                       | 0                 | x     |            |              | x   |
| [signatures-vs](defi---vs.md)                                                     | Définir une constante entière                                                                                      | 0                 | x     |            |              | x   |
| [DP3-vs](dp3---vs.md)                                                       | Produit scalaire à trois composants                                                                                     | 1                 |       | x          |              |     |
| [DP4-vs](dp4---vs.md)                                                       | Produit scalaire à quatre composants                                                                                      | 1                 |       | x          |              |     |
| [DST-vs](dst---vs.md)                                                       | Calculer le vecteur de distance                                                                                   | 1                 |       | x          |              |     |
| [else-vs](else---vs.md)                                                     | Commencer un bloc [else-vs](else---vs.md)                                                                       | 1                 |       |            | x            | x   |
| [endif-vs](endif---vs.md)                                                   | Terminer une [si bool-vs](if-bool---vs.md)... [else-bloc vs](else---vs.md)                                      | 1                 |       |            | x            | x   |
| [ENDLOOP-vs](endloop---vs.md)                                               | Fin d’un bloc de [boucle-vs](loop---vs.md)                                                                       | 2                 |       |            | x            | x   |
| [endrep-vs](endrep---vs.md)                                                 | Fin d’un bloc REPEAT                                                                                           | 2                 |       |            | x            | x   |
| [exp-vs](exp---vs.md)                                                       | Précision totale 2<sup>x</sup>                                                                                    | 1                 |       | x          |              |     |
| [exp-vs](exp---vs.md)                                                       | Précision partielle 2<sup>x</sup>                                                                                 | 1                 |       | x          |              |     |
| [FRC-vs](frc---vs.md)                                                       | Composant fractionnaire                                                                                            | 1                 |       | x          |              |     |
| [Si bool-vs](if-bool---vs.md)                                               | Commencer un bloc [If bool-vs](if-bool---vs.md) (à l’aide d’une condition booléenne)                                     | 3                 |       |            | x            | x   |
| [étiquette-vs](label---vs.md)                                                   | Étiquette                                                                                                           | 0                 |       |            | x            | x   |
| [lit-vs](lit---vs.md)                                                       | Calcul de l’éclairage partiel                                                                                    | 3                 |       | x          |              |     |
| [journalisation-vs](log---vs.md)                                                       | ₂ du journal de précision complète (x)                                                                                          | 1                 |       | x          |              |     |
| [logP-vs](logp---vs.md)                                                     | ₂ de journal de précision partielle (x)                                                                                       | 1                 |       | x          |              |     |
| [boucle-vs](loop---vs.md)                                                     | Loop                                                                                                            | 3                 |       |            | x            | x   |
| [LRP-vs](lrp---vs.md)                                                       | Interpolation linéaire                                                                                            | 2                 |       | x          |              | x   |
| [M3X2-vs](m3x2---vs.md)                                                     | matrice multiplier                                                                                                    | 2                 |       | x          |              |     |
| [M3x3-vs](m3x3---vs.md)                                                     | 3 x 3                                                                                                    | 3                 |       | x          |              |     |
| [M3x4-vs](m3x4---vs.md)                                                     | 3x4 multiplier                                                                                                    | 4                 |       | x          |              |     |
| [m4x3-vs](m4x3---vs.md)                                                     | 4x3 multiplier                                                                                                    | 3                 |       | x          |              |     |
| [M4X4-vs](m4x4---vs.md)                                                     | 4 x 4                                                                                                    | 4                 |       | x          |              |     |
| [Mad-vs](mad---vs.md)                                                       | Multiplier et ajouter                                                                                                | 1                 |       | x          |              |     |
| [Max-vs](max---vs.md)                                                       | Maximale                                                                                                         | 1                 |       | x          |              |     |
| [min-vs](min---vs.md)                                                       | Minimum                                                                                                         | 1                 |       | x          |              |     |
| [MOV-vs](mov---vs.md)                                                       | Déplacer                                                                                                            | 1                 |       | x          |              |     |
| [Mova-vs](mova---vs.md)                                                     | Déplacer des données à partir d’un registre à virgule flottante vers le registre d’adresses (a0)                                           | 1                 |       | x          |              | x   |
| [Mul-vs](mul---vs.md)                                                       | Multiplier                                                                                                        | 1                 |       | x          |              |     |
| [NOP-vs](nop---vs.md)                                                       | Pas d'opération                                                                                                    | 1                 |       | x          |              |     |
| [NRM-vs](nrm---vs.md)                                                       | Normaliser un vecteur 4D                                                                                           | 3                 |       | x          |              | x   |
| [Pow-vs](pow---vs.md)                                                       | x<sup>y</sup>                                                                                                   | 3                 |       | x          |              | x   |
| [RCP-vs](rcp---vs.md)                                                       | Mutuel                                                                                                      | 1                 |       | x          |              |     |
| [REP-vs](rep---vs.md)                                                       | Répéter                                                                                                          | 3                 |       |            | x            | x   |
| [RET-vs](ret---vs.md)                                                       | Fin d’une sous-routine ou principale                                                                              | 1                 |       |            | x            | x   |
| [rsq-vs](rsq---vs.md)                                                       | Racine carrée réciproque                                                                                          | 1                 |       | x          |              |     |
| [SGE-vs](sge---vs.md)                                                       | Comparaison supérieur ou égal à                                                                                   | 1                 |       | x          |              |     |
| [SGN-vs](sgn---vs.md)                                                       | Sign (Signer)                                                                                                            | 3                 |       | x          |              | x   |
| [SinCos,-vs](sincos---vs.md)                                                 | Sinus et cosinus                                                                                                 | 8                 |       | x          |              | x   |
| [des SLT-vs](slt---vs.md)                                                       | Inférieur à compare                                                                                               | 1                 |       | x          |              |     |
| [sous-vs](sub---vs.md)                                                       | Soustraire                                                                                                        | 1                 |       | x          |              |     |
| [comparatif](vs---vs.md)                                                              | Version                                                                                                         | 0                 | x     |            |              |     |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Instructions du nuanceur de sommets](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




