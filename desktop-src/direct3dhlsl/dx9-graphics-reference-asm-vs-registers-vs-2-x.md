---
title: Registres-vs_2_x
description: Cette section contient des informations de référence pour les registres d’entrée et de sortie implémentés par le nuanceur de sommets version 2 \_ x.
ms.assetid: 35dfa3c8-be8e-4b2b-84c4-766850cf146c
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 6aebd9095e18abd5ac76988e46c2e061e30209c6
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126915316"
---
# <a name="registers---vs_2_x"></a>Registres-vs \_ 2 \_ x

Cette section contient des informations de référence pour les registres d’entrée et de sortie implémentés par le nuanceur de sommets version 2 \_ x.

## <a name="input-registers"></a>Registres d’entrée



| S’inscrire | Nom                                                                                      | Count      | R/W (Lecture/écriture) | \# Ports de lecture | \# Lectures/inst | Dimension | RelAddr | Valeurs par défaut     | DCL obligatoire |
|----------|-------------------------------------------------------------------------------------------|------------|-----|---------------|-----------------|-----------|---------|--------------|--------------|
| v\#      | [Registre d’entrée](dx9-graphics-reference-asm-vs-registers-input.md)                       | 16         | R   | 1             | Illimité       | 4         | Non      | Voir la remarque 1   | Oui          |
| r\#      | [Registre temporaire](dx9-graphics-reference-asm-vs-registers-temporary.md)               | Voir la remarque 2 | R/W (Lecture/écriture) | 3             | Illimité       | 4         | Non      | Aucun         | Non           |
| c\#      | [Registre à virgule flottante constante](dx9-graphics-reference-asm-vs-registers-constant-float.md)     | Voir la remarque 3 | R   | 1             | 2               | 4         | a0/aL | (0, 0, 0, 0) | Non           |
| a0       | [Registre d’adresses](dx9-graphics-reference-asm-vs-registers-address.md)                   | 1          | R/W (Lecture/écriture) | 1             | 2               | 4         | Non      | Aucun         | Non           |
| b\#      | [Registre booléen constant](dx9-graphics-reference-asm-vs-registers-constant-boolean.md) | 16         | R   | 1             | 1               | 1         | Non      | FALSE        | Non           |
| cliqu\#      | [Registre d’entiers constant](dx9-graphics-reference-asm-vs-registers-constant-integer.md) | 16         | R   | 1             | 1               | 4         | Non      | (0, 0, 0, 0) | Non           |
| &       | [Registre de compteur de boucle](dx9-graphics-reference-asm-vs-registers-loop-counter.md)         | 1          | R   | 1             | 2               | 1         | Non      | Aucun         | Non           |
| P0       | [Registre de prédicat](dx9-graphics-reference-asm-vs-registers-predicate.md)               | 1          | R/W (Lecture/écriture) | 1             | 1               | 4         | Non      | Aucun         | Non           |



 

Remarques :

1.  Partial (0, 0, 0, 1) : si seul un sous-ensemble de canaux est mis à jour, les autres canaux ont par défaut la valeur (0, 0, 0, 1).
2.  Égal à D3DCAPS9. VS20Caps. NumTemps (au moins 12 pour vs \_ 2 \_ x).
3.  Égal à D3DCAPS9. MaxVertexShaderConst (au moins 256 pour vs \_ 2 \_ x).

## <a name="output-registers"></a>Registres de sortie



| S’inscrire | Nom                                                                                          | Count | R/W (Lecture/écriture) | Dimension | RelAddr | Valeurs par défaut | DCL obligatoire |
|----------|-----------------------------------------------------------------------------------------------|-------|-----|-----------|---------|----------|--------------|
| oPos     | [Registre de position](dx9-graphics-reference-asm-vs-registers-position.md)                     | 1     | W   | 4         | Non      | Aucun     | Non           |
| oFog     | [Registre de brouillard](dx9-graphics-reference-asm-vs-registers-fog.md)                               | 1     | W   | 1         | Non      | Aucun     | Non           |
| Décide     | [Registre de la taille du point](dx9-graphics-reference-asm-vs-registers-point-size.md)                 | 1     | W   | 1         | Non      | Aucun     | Non           |
| Diamètre\#     | [Registre des couleurs](dx9-graphics-reference-asm-vs-registers-color.md); Voir la remarque 1               | 2     | W   | 4         | Non      | Aucun     | Non           |
| oT\#     | [Registre de coordonnées de texture](dx9-graphics-reference-asm-vs-registers-texture-coordinate.md) | 8     | W   | 4         | Non      | Aucun     | Non           |



 

Remarques :

-   oD0 est la sortie de couleur diffuse ; oD1 est la sortie de couleur spéculaire.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Registres de nuanceur vertex](dx9-graphics-reference-asm-vs-registers.md)
</dt> </dl>

 

 




