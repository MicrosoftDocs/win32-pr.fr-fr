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
ms.openlocfilehash: d658d2d14d149d5d83d673269f2a414d7feaa22f13f1b32f57c4b80500fb1398
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119673099"
---
# <a name="registers---vs_3_0"></a>Registres-vs \_ 3 \_ 0

Cette section contient des informations de référence pour les registres d’entrée et de sortie implémentés par le nuanceur de vertex version 3 \_ 0.

## <a name="input-registers"></a>Registres d’entrée



| S’inscrire | Name                                                                                      | Count      | R/W (Lecture/écriture) | \# Ports de lecture | \# Lectures/inst | Dimension | RelAddr | Valeurs par défaut     | DCL obligatoire |
|----------|-------------------------------------------------------------------------------------------|------------|-----|---------------|-----------------|-----------|---------|--------------|--------------|
| v\#      | [Registre d’entrée](dx9-graphics-reference-asm-vs-registers-input.md)                       | 16         | R   | 1             | illimitées       | 4         | a0/aL   | Voir la remarque 1   | Oui          |
| r\#      | [Registre temporaire](dx9-graphics-reference-asm-vs-registers-temporary.md)               | 32         | R/W (Lecture/écriture) | 3             | illimitées       | 4         | Non      | Aucun         | Non           |
| c\#      | [Registre à virgule flottante constante](dx9-graphics-reference-asm-vs-registers-constant-float.md)     | Voir la remarque 2 | R   | 1             | illimitées       | 4         | a0/aL   | (0, 0, 0, 0) | Non           |
| a0       | [Registre d’adresses](dx9-graphics-reference-asm-vs-registers-address.md)                   | 1          | R/W (Lecture/écriture) | 1             | illimitées       | 4         | Non      | Aucun         | Non           |
| b\#      | [Registre booléen constant](dx9-graphics-reference-asm-vs-registers-constant-boolean.md) | 16         | R   | 1             | 1               | 1         | Non      | FALSE        | Non           |
| cliqu\#      | [Registre d’entiers constant](dx9-graphics-reference-asm-vs-registers-constant-integer.md) | 16         | R   | 1             | 1               | 4         | Non      | (0, 0, 0, 0) | Non           |
| &       | [Registre de compteur de boucle](dx9-graphics-reference-asm-vs-registers-loop-counter.md)         | 1          | R   | 1             | illimitées       | 1         | Non      | Aucun         | Non           |
| P0       | [Registre de prédicat](dx9-graphics-reference-asm-vs-registers-predicate.md)               | 1          | R/W (Lecture/écriture) | 1             | 1               | 4         | non      | aucun         | non           |
| s\#      | [Échantillonneur (Direct3D 9 ASM-vs)](dx9-graphics-reference-asm-vs-registers-sampler.md)        | 4          | R   | 1             | 1               | 4         | Non      | Voir la remarque 3   | Oui          |



 

Remarques :

1.  Partial (0, 0, 0, 1) : si seul un sous-ensemble de canaux est mis à jour, les autres canaux ont par défaut la valeur (0, 0, 0, 1).
2.  Égal à D3DCAPS9. MaxVertexShaderConst (au moins 256 pour vs \_ 3 \_ 0).
3.  Les valeurs par défaut de recherche d’échantillonneur existent, mais les valeurs dépendent du format de texture.

## <a name="output-registers"></a>Registres de sortie

Les registres de sortie ont été réduits en \# registres de 12 o (sortie). Elles peuvent être utilisées pour tout ce que l’utilisateur souhaite interpoler pour le nuanceur de pixels : coordonnées de la texture, couleurs, brouillard, etc.



| S’inscrire | Name            | Count | R/W (Lecture/écriture) | Dimension | RelAddr | Valeurs par défaut | DCL obligatoire |
|----------|-----------------|-------|-----|-----------|---------|----------|--------------|
| sorties\#      | Registre de sortie | 12    | W   | 4         | &      | Aucun     | Oui          |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Registres de nuanceur vertex](dx9-graphics-reference-asm-vs-registers.md)
</dt> </dl>

 

 




