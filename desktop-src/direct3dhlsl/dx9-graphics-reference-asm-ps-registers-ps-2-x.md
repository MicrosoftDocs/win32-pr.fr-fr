---
title: Registres de ps_2_x
description: Cet article contient des informations de référence pour les registres d’entrée et de sortie implémentés par le nuanceur de pixels version 2_x.
ms.assetid: 52bb6290-46e2-4d7d-9b96-b4c3e2abfe43
keywords:
- Registres-ps_2_x
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: be0e7f282978ada28c2dd71dc7c16dd317ddce42
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112406702"
---
# <a name="ps_2_x-registers"></a>\_registres PS 2 \_ x

Les nuanceurs de pixels dépendent des registres pour obtenir des données de vertex, pour produire des données de pixels, pour conserver des résultats temporaires pendant les calculs et pour identifier les étapes d’échantillonnage de texture. Il existe plusieurs types de registres, chacun avec une fonctionnalité unique. Cette section contient des informations de référence pour les registres d’entrée et de sortie implémentés par le nuanceur de pixels version 2 \_ x.

## <a name="input-register-types"></a>Types de registres d’entrée



| S’inscrire | Nom                                                                                          | Count      | R/W (Lecture/écriture)        | \# Ports de lecture | \# Lectures/inst | Dimension | RelAddr | Valeurs par défaut                  | DCL obligatoire |
|----------|-----------------------------------------------------------------------------------------------|------------|------------|---------------|---------------|-----------|---------|---------------------------|--------------|
| v\#      | [Registre des couleurs d’entrée](dx9-graphics-reference-asm-ps-registers-input-color.md)               | 2          | R          | 1             | Illimité     | 4         | N       | Partiel (0001). Voir la remarque 4 | Y            |
| r\#      | [Registre temporaire](dx9-graphics-reference-asm-ps-registers-temporary.md)                   | Voir la remarque 1 | R/W (Lecture/écriture)        | 3             | Illimité     | 4         | N       | Aucun                      | N            |
| c\#      | [Registre à virgule flottante constante](dx9-graphics-reference-asm-ps-registers-constant-float.md)         | 32         | R          | 1             | 2             | 4         | N       | 0000                      | N            |
| cliqu\#      | [Registre d’entiers constant](dx9-graphics-reference-asm-ps-registers-constant-integer.md)     | 16         | Voir la remarque 2 | 1             | 1             | 4         | N       | 0000                      | N            |
| b\#      | [Registre booléen constant](dx9-graphics-reference-asm-ps-registers-constant-boolean.md)     | 16         | Voir la remarque 2 | 1             | 1             | 1         | N       | FALSE                     | N            |
| P0       | [Registre de prédicat](dx9-graphics-reference-asm-ps-registers-predicate.md)                   | 1          | Voir la remarque 2 | 1             | 1             | 1         | N       | Aucun                      | Y            |
| s\#      | [Échantillonneur (Direct3D 9 ASM-PS)](dx9-graphics-reference-asm-ps-registers-sampler.md)            | 16         | Voir la remarque 3 | 1             | 1             | 4         | N       | Voir la remarque 5                | Y            |
| t\#      | [Registre de coordonnées de texture](dx9-graphics-reference-asm-ps-registers-texture-coordinate.md) | 8          | R          | 1             | 1             | 4         | N       | Aucun                      | Y            |



 

Remarques :

1.  12 min/32 max : le nombre de \# registres r est déterminé par D3DPSHADERCAPS2 \_ 0. NumTemps (qui est compris entre 12 et 32).
2.  Utilisable uniquement par une instruction de contrôle de Flow.
3.  Utilisable uniquement par une instruction d’échantillonnage de texture.
4.  Partial (x, y, z, w) : si seul un sous-ensemble de canaux est mis à jour dans le registre, les autres canaux ont par défaut les valeurs spécifiées (x, y, z, w).
5.  Les valeurs par défaut pour les recherches d’échantillonneur existent, mais les valeurs dépendent du format de texture.

Le nombre de readports est le nombre de registres différents (pour chaque type de registre) qui peuvent être lus dans une instruction unique.

## <a name="output-register-types"></a>Types de registres de sortie



| S’inscrire | Nom                                                                              | Count                                                                             | R/W (Lecture/écriture) | Dimension | RelAddr | Valeurs par défaut | DCL obligatoire |
|----------|-----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|-----|-----------|---------|----------|--------------|
| c #     | [Registre des couleurs de sortie](dx9-graphics-reference-asm-ps-registers-output-color.md) | Voir [les textures à plusieurs éléments (Direct3D 9)](/windows/desktop/direct3d9/multiple-element-textures) | W   | 4         | N       | Aucun     | N            |
| oDepth   | [Registre de profondeur de sortie](dx9-graphics-reference-asm-ps-registers-output-depth.md) | 1                                                                                 | W   | 1         | N       | Aucun     | N            |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Inscrit](dx9-graphics-reference-asm-ps-registers.md)
</dt> </dl>

 

 