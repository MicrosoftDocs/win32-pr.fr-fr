---
title: Registres-vs_3_0
description: Cette section contient des informations de référence pour les registres d’entrée et de sortie implémentés par le nuanceur de vertex version 3 \_ 0.
ms.assetid: af81f1c4-9c11-455e-a565-1b80f1ee8683
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 47353a3f312a2abbd6f4fe5ea1dcd1ed9495a9d0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103674717"
---
# <a name="registers---vs_3_0"></a>Registres-vs \_ 3 \_ 0

Cette section contient des informations de référence pour les registres d’entrée et de sortie implémentés par le nuanceur de vertex version 3 \_ 0.

## <a name="input-registers"></a>Registres d’entrée



| S’inscrire | Nom                                                                                      | Count      | R/W (Lecture/écriture) | \# Ports de lecture | \# Lectures/inst | Dimension | RelAddr | Valeurs par défaut     | DCL obligatoire |
|----------|-------------------------------------------------------------------------------------------|------------|-----|---------------|-----------------|-----------|---------|--------------|--------------|
| v\#      | [Registre d’entrée](dx9-graphics-reference-asm-vs-registers-input.md)                       | 16         | R   | 1             | Illimité       | 4         | a0/aL   | Voir la remarque 1   | Oui          |
| r\#      | [Registre temporaire](dx9-graphics-reference-asm-vs-registers-temporary.md)               | 32         | R/W (Lecture/écriture) | 3             | Illimité       | 4         | Non      | None         | Non           |
| c\#      | [Registre à virgule flottante constante](dx9-graphics-reference-asm-vs-registers-constant-float.md)     | Voir la remarque 2 | R   | 1             | Illimité       | 4         | a0/aL   | (0, 0, 0, 0) | Non           |
| a0       | [Registre d’adresses](dx9-graphics-reference-asm-vs-registers-address.md)                   | 1          | R/W (Lecture/écriture) | 1             | Illimité       | 4         | Non      | None         | Non           |
| p\#      | [Registre booléen constant](dx9-graphics-reference-asm-vs-registers-constant-boolean.md) | 16         | R   | 1             | 1               | 1         | Non      | FALSE        | Non           |
| cliqu\#      | [Registre d’entiers constant](dx9-graphics-reference-asm-vs-registers-constant-integer.md) | 16         | R   | 1             | 1               | 4         | Non      | (0, 0, 0, 0) | Non           |
| &       | [Registre de compteur de boucle](dx9-graphics-reference-asm-vs-registers-loop-counter.md)         | 1          | R   | 1             | Illimité       | 1         | Non      | None         | Non           |
| P0       | [Registre de prédicat](dx9-graphics-reference-asm-vs-registers-predicate.md)               | 1          | R/W (Lecture/écriture) | 1             | 1               | 4         | non      | Aucun         | non           |
| s\#      | [Échantillonneur (Direct3D 9 ASM-vs)](dx9-graphics-reference-asm-vs-registers-sampler.md)        | 4          | R   | 1             | 1               | 4         | Non      | Voir la remarque 3   | Oui          |



 

Remarques :

1.  Partial (0, 0, 0, 1) : si seul un sous-ensemble de canaux est mis à jour, les autres canaux ont par défaut la valeur (0, 0, 0, 1).
2.  Égal à D3DCAPS9. MaxVertexShaderConst (au moins 256 pour vs \_ 3 \_ 0).
3.  Les valeurs par défaut de recherche d’échantillonneur existent, mais les valeurs dépendent du format de texture.

## <a name="output-registers"></a>Registres de sortie

Les registres de sortie ont été réduits en \# registres de 12 o (sortie). Elles peuvent être utilisées pour tout ce que l’utilisateur souhaite interpoler pour le nuanceur de pixels : coordonnées de la texture, couleurs, brouillard, etc.



| S’inscrire | Nom            | Count | R/W (Lecture/écriture) | Dimension | RelAddr | Valeurs par défaut | DCL obligatoire |
|----------|-----------------|-------|-----|-----------|---------|----------|--------------|
| sorties\#      | Registre de sortie | 12    | W   | 4         | &      | Aucun     | Oui          |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Registres de nuanceur vertex](dx9-graphics-reference-asm-vs-registers.md)
</dt> </dl>

 

 




