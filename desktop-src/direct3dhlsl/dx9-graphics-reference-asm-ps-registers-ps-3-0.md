---
title: Registres de ps_3_0
description: Cet article contient des informations de référence pour les registres d’entrée et de sortie implémentés par le nuanceur de pixels version 3_0.
ms.assetid: 01bee50a-c1b7-4b15-9df8-1dd52d9ff163
keywords:
- vPos
- Registre de position, nuanceur de pixels
- Registres-ps_3_0
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: e1cd0173beabc8fbe21ad15e88e23fc1b6e84892
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112405492"
---
# <a name="ps_3_0-registers"></a>\_registres PS 3 \_ 0

Les nuanceurs de pixels dépendent des registres pour obtenir des données de vertex, pour produire des données de pixels, pour conserver des résultats temporaires pendant les calculs et pour identifier les étapes d’échantillonnage de texture. Il existe plusieurs types de registres, chacun avec une fonctionnalité unique. Cette section contient des informations de référence pour les registres d’entrée et de sortie implémentés par le nuanceur de pixels version 3 \_ 0.

## <a name="new-registers"></a>Nouveaux registres

### <a name="input-register"></a>Registre d’entrée

Les registres d’entrée (v \# ) sont désormais à virgule flottante intégrale et le [Registre de coordonnées de texture](dx9-graphics-reference-asm-ps-registers-texture-coordinate.md)s (t) y \# a été consolidé. La [ \_ sémantique DCL (SM3-PS ASM)](dcl-usage---ps.md) en haut du nuanceur est utilisée pour décrire ce qui est confronté dans un registre d’entrée particulier \_ . Une sémantique pour les types de pixels est introduite (similaire au côté vertex) pour ce modèle. Aucune fixation n’est effectuée lorsque les registres d’entrée sont définis comme des couleurs (comme les coordonnées de texture). L’évaluation des registres définis comme couleur diffère des coordonnées de texture lors de l’échantillonnage multiple.

### <a name="face-register"></a>Registre de visage

Le vFace (visage Register) est une nouveauté pour ce modèle. Il s’agit d’un registre scalaire à virgule flottante qui contiendra finalement la zone primitive. Toutefois, dans PS \_ 3 \_ 0, seul le signe de ce registre est valide. Par conséquent, si la valeur est inférieure à zéro (le bit de signe est défini sur négatif), la primitive est la face arrière (la zone est négative, à gauche). Par conséquent, dans PS \_ 3 \_ 0, il est logique de comparer ce registre à 0 (> 0 ou < 0). Dans le nuanceur de pixels, l’application peut prendre une décision quant à la technique d’éclairage à utiliser. L’éclairage à deux côtés peut être obtenu de cette manière. Ce registre requiert une déclaration, donc l’utilisation non déclarée est signalée comme une erreur. Pour les lignes et les primitives de point, ce registre n’est pas défini. Le registre de faces peut uniquement être utilisé comme condition avec les instructions suivantes : [setp \_ COMP-PS](setp-comp---ps.md), [si \_ COMP-PS](if-comp---ps.md)ou [break \_ COMP-PS](break-comp---ps.md).

### <a name="loop-counter-register"></a>Registre de compteur de boucle

Le [Registre du compteur de boucles](dx9-graphics-reference-asm-ps-registers-loop-counter.md) (Al) est nouveau pour ce modèle. Elle est incrémentée automatiquement à chaque exécution du bloc [Loop-PS](loop---ps.md) / [ENDLOOP-PS](endloop---ps.md) . Il peut être utilisé dans le bloc pour l’adressage relatif, si nécessaire. L’utilisation d’un registre de compteur de boucle en dehors de la boucle n’est pas valide.

### <a name="position-register"></a>Registre de position

Le registre de position (vPos) est une nouveauté pour ce modèle. Il contient les pixels actuels (x, y) des canaux correspondants. Les canaux (z, w) ne sont pas définis. Ce registre requiert une déclaration, donc l’utilisation non déclarée est signalée comme une erreur. Lorsqu’il est déclaré, ce registre doit avoir exactement l’un des masques suivants :. x,. y,. XY.

## <a name="input-register-types"></a>Types de registres d’entrée



| S’inscrire | Nom                                                                                      | Count | R/W (Lecture/écriture) | \# Ports de lecture | \# Lectures/inst | Dimension | RelAddr | Valeurs par défaut   | DCL obligatoire |
|----------|-------------------------------------------------------------------------------------------|-------|-----|---------------|---------------|-----------|---------|------------|--------------|
| v\#      | [Registre d’entrée](dx9-graphics-reference-asm-ps-registers-input-color.md)                 | 10    | R   | 1             | Illimité     | 4         | &      | Aucun       | Oui          |
| r\#      | [Registre temporaire](dx9-graphics-reference-asm-ps-registers-temporary.md)               | 32    | R/W (Lecture/écriture) | 3             | Illimité     | 4         | Non      | None       | Non           |
| c\#      | [Registre à virgule flottante constante](dx9-graphics-reference-asm-ps-registers-constant-float.md)     | 224   | R   | 1             | Illimité     | 4         | Non      | 0000       | Non           |
| cliqu\#      | [Registre d’entiers constant](dx9-graphics-reference-asm-ps-registers-constant-integer.md) | 16    | R   | 1             | 1             | 4         | Non      | 0000       | Non           |
| b\#      | [Registre booléen constant](dx9-graphics-reference-asm-ps-registers-constant-boolean.md) | 16    | R   | 1             | 1             | 1         | Non      | FALSE      | Non           |
| P0       | [Registre de prédicat](dx9-graphics-reference-asm-ps-registers-predicate.md)               | 1     | R   | 1             | 1             | 1         | Non      | None       | Non           |
| s\#      | [Échantillonneur (Direct3D 9 ASM-PS)](dx9-graphics-reference-asm-ps-registers-sampler.md)        | 16    | R   | 1             | 1             | 4         | Non      | Voir la remarque 1 | Oui          |
| vFace    | Registre de visage \_                                                                            | 1     | R   | 1             | Illimité     | 1         | Non      | None       | Oui          |
| vPos     | Registre de position \_                                                                        | 1     | R   | 1             | Illimité     | 4         | Non      | None       | Oui          |
| &       | \_Registre de compteur de boucle \_                                                                   | 1     | R   | 1             | Illimité     | 1         | n/a     | Aucun       | Non           |



 

Remarques :

-   Les valeurs par défaut pour les recherches d’échantillonneur existent, mais les valeurs dépendent du format de texture.

Le nombre de readports est le nombre de registres différents (pour chaque type de registre) qui peuvent être lus dans une instruction unique.

## <a name="output-register-types"></a>Types de registres de sortie



| S’inscrire | Nom                                                                              | Count                                                                             | R/W (Lecture/écriture) | Dimension | RelAddr | Valeurs par défaut | DCL obligatoire |
|----------|-----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|-----|-----------|---------|----------|--------------|
| c #     | [Registre des couleurs de sortie](dx9-graphics-reference-asm-ps-registers-output-color.md) | Voir [les textures à plusieurs éléments (Direct3D 9)](/windows/desktop/direct3d9/multiple-element-textures) | W   | 4         | Non      | None     | Non           |
| oDepth   | [Registre de profondeur de sortie](dx9-graphics-reference-asm-ps-registers-output-depth.md) | 1                                                                                 | W   | 1         | Non      | None     | Non           |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Inscrit](dx9-graphics-reference-asm-ps-registers.md)
</dt> </dl>

 

 