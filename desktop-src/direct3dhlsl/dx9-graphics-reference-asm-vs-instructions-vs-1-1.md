---
title: Instructions-vs_1_1
description: Cette section contient des informations de référence pour les instructions du nuanceur vertex version 1 \_ 1.
ms.assetid: db3c14ce-6e50-4931-b07f-966acc7ffb0a
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: f980640009158c6c4dc684158836d1514ca47755fea700ac7cc619f6e7574409
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119789089"
---
# <a name="instructions---vs_1_1"></a>Instructions-vs \_ 1 \_ 1

Cette section contient des informations de référence pour les instructions du nuanceur vertex version 1 \_ 1.

Il existe plusieurs types d’instructions de nuanceur de sommets, comme indiqué dans le tableau. Les colonnes à droite indiquent les éléments suivants :

-   Emplacements d’instruction : nombre d’emplacements d’instruction utilisés par chaque instruction.
-   Configuration-instructions non arithmétiques. Chaque nuanceur doit avoir une instruction de version et doit être la première instruction.
-   Arithmétique : ces instructions fournissent les opérations mathématiques dans un nuanceur.
-   Nouveauté : ces instructions sont nouvelles dans cette version.

## <a name="instruction-set"></a>Jeu d'instructions



| Name                                                                           | Description                                                                                                     | Emplacements des instructions | Installation | Arithmétique | Nouveau |
|--------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|-------------------|-------|------------|-----|
| [Ajouter-vs](add---vs.md)                                                       | Ajouter deux vecteurs                                                                                                 | 1                 |       | x          | x   |
| [\_entrée d’utilisation DCL (SM1, SM2, SM3-vs ASM)](dcl-usage-input-register---vs.md) | Déclarer des registres de vertex d’entrée (voir [registres-vs \_ 1 \_ 1](dx9-graphics-reference-asm-vs-registers-vs-1-1.md)) | 0                 | x     |            | x   |
| [def-vs](def---vs.md)                                                       | Définir des constantes                                                                                                | 0                 | x     |            | x   |
| [DP3-vs](dp3---vs.md)                                                       | Produit scalaire à trois composants                                                                                     | 1                 |       | x          | x   |
| [DP4-vs](dp4---vs.md)                                                       | Produit scalaire à quatre composants                                                                                      | 1                 |       | x          | x   |
| [DST-vs](dst---vs.md)                                                       | Calculer le vecteur de distance                                                                                   | 1                 |       | x          | x   |
| [exp-vs](exp---vs.md)                                                       | Précision totale 2<sup>x</sup>                                                                                    | 10                |       | x          | x   |
| [exp-vs](exp---vs.md)                                                       | Précision partielle 2<sup>x</sup>                                                                                 | 1                 |       | x          | x   |
| [FRC-vs](frc---vs.md)                                                       | Composant fractionnaire                                                                                            | 3                 |       | x          | x   |
| [lit-vs](lit---vs.md)                                                       | Calcul de l’éclairage partiel                                                                                    | 1                 |       | x          | x   |
| [journalisation-vs](log---vs.md)                                                       | ₂ du journal de précision complète (x)                                                                                          | 10                |       | x          | x   |
| [logP-vs](logp---vs.md)                                                     | ₂ de journal de précision partielle (x)                                                                                       | 1                 |       | x          | x   |
| [M3X2-vs](m3x2---vs.md)                                                     | matrice multiplier                                                                                                    | 2                 |       | x          | x   |
| [M3x3-vs](m3x3---vs.md)                                                     | 3 x 3                                                                                                    | 3                 |       | x          | x   |
| [M3x4-vs](m3x4---vs.md)                                                     | 3x4 multiplier                                                                                                    | 4                 |       | x          | x   |
| [m4x3-vs](m4x3---vs.md)                                                     | 4x3 multiplier                                                                                                    | 3                 |       | x          | x   |
| [M4X4-vs](m4x4---vs.md)                                                     | 4 x 4                                                                                                    | 4                 |       | x          | x   |
| [Mad-vs](mad---vs.md)                                                       | Multiplier et ajouter                                                                                                | 1                 |       | x          | x   |
| [Max-vs](max---vs.md)                                                       | Maximum                                                                                                         | 1                 |       | x          | x   |
| [min-vs](min---vs.md)                                                       | Minimum                                                                                                         | 1                 |       | x          | x   |
| [MOV-vs](mov---vs.md)                                                       | Déplacer                                                                                                            | 1                 |       | x          | x   |
| [Mul-vs](mul---vs.md)                                                       | Multiplier                                                                                                        | 1                 |       | x          | x   |
| [NOP-vs](nop---vs.md)                                                       | Pas d'opération                                                                                                    | 1                 |       | x          | x   |
| [RCP-vs](rcp---vs.md)                                                       | Mutuel                                                                                                      | 1                 |       | x          | x   |
| [rsq-vs](rsq---vs.md)                                                       | Racine carrée réciproque                                                                                          | 1                 |       | x          | x   |
| [SGE-vs](sge---vs.md)                                                       | Comparaison supérieur ou égal à                                                                                   | 1                 |       | x          | x   |
| [des SLT-vs](slt---vs.md)                                                       | Inférieur à compare                                                                                               | 1                 |       | x          | x   |
| [sous-vs](sub---vs.md)                                                       | Soustraire                                                                                                        | 1                 |       | x          | x   |
| [comparatif](vs---vs.md)                                                              | Version                                                                                                         | 0                 | x     |            | x   |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Instructions du nuanceur de sommets](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




