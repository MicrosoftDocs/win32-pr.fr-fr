---
title: Registres-vs_1_1
description: Cette section contient des informations de référence pour les registres d’entrée et de sortie implémentés par le nuanceur de vertex version 1 \_ 1.
ms.assetid: 8b19a0da-1561-450f-a36a-35ac7ea6e17a
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 4bcfadae2b1dca70298ffed188de2e6075892563b27bf6f624f2139e441600cd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117908003"
---
# <a name="registers---vs_1_1"></a>Registres-vs \_ 1 \_ 1

Cette section contient des informations de référence pour les registres d’entrée et de sortie implémentés par le nuanceur de vertex version 1 \_ 1.

## <a name="input-registers"></a>Registres d’entrée



| S’inscrire | Nom                                                                                  | Count      | R/W (Lecture/écriture) | \# Ports de lecture | \# Lectures/inst | Dimension  | RelAddr | Valeurs par défaut     | DCL obligatoire |
|----------|---------------------------------------------------------------------------------------|------------|-----|---------------|-----------------|------------|---------|--------------|--------------|
| a0       | [Registre d’adresses](dx9-graphics-reference-asm-vs-registers-address.md)               | 1          | R/W (Lecture/écriture) | 1             | illimitées       | Voir la remarque 3 | Non      | Aucun         | Non           |
| c\#      | [Registre à virgule flottante constante](dx9-graphics-reference-asm-vs-registers-constant-float.md) | Voir la remarque 2 | R   | 1             | illimitées       | 4          | a0. x    | (0, 0, 0, 0) | Non           |
| v\#      | [Registre d’entrée](dx9-graphics-reference-asm-vs-registers-input.md)                   | 16         | R   | 1             | illimitées       | 4          | Non      | Voir la remarque 1   | Oui          |
| r\#      | [Registre temporaire](dx9-graphics-reference-asm-vs-registers-temporary.md)           | 12         | R/W (Lecture/écriture) | 3             | illimitées       | 4          | Non      | Aucun         | Non           |



 

Remarques :

1.  Partial (0, 0, 0, 1) : si seul un sous-ensemble de canaux est mis à jour, les autres canaux ont par défaut la valeur (0, 0, 0, 1).
2.  Égal à D3DCAPS9. MaxVertexShaderConst (au moins 96 pour vs \_ 1 \_ 1).
3.  Seul le canal. x est disponible.

## <a name="output-registers"></a>Registres de sortie



| S’inscrire | Nom                        | Count | R/W (Lecture/écriture) | Dimension | RelAddr | Valeurs par défaut | DCL obligatoire |
|----------|-----------------------------|-------|-----|-----------|---------|----------|--------------|
| oPos     | Registre de position           | 1     | W   | 4         | Non      | Aucun     | Non           |
| oFog     | Registre de brouillard                | 1     | W   | 1         | Non      | Aucun     | Non           |
| Décide     | Registre de la taille du point         | 1     | W   | 1         | Non      | Aucun     | Non           |
| Diamètre\#     | Registre des couleurs ; Voir la remarque 1  | 2     | W   | 4         | Non      | Aucun     | Non           |
| oT\#     | Registre de coordonnées de texture | 8     | W   | 4         | Non      | Aucun     | Non           |



 

Remarques :

-   oD0 est la sortie de couleur diffuse ; oD1 est la sortie de couleur spéculaire.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Registres de nuanceur vertex](dx9-graphics-reference-asm-vs-registers.md)
</dt> </dl>

 

 




