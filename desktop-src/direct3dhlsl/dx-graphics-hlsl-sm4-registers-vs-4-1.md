---
title: Registres-vs_4_1
description: Cette section contient des informations de référence pour les registres d’entrée et de sortie implémentés par le nuanceur de sommets version 4 \_ 1.
ms.assetid: ea449195-d012-4a14-9760-b738a8623343
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 0164b1d82a9d371e735177f381e2a1a97aa062aaca8c65a00d4959a32279ed11
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119119923"
---
# <a name="registers---vs_4_1"></a>Registres-vs \_ 4 \_ 1

Cette section contient des informations de référence pour les registres d’entrée et de sortie implémentés par le nuanceur de sommets version 4 \_ 1.

## <a name="input-registers"></a>Registres d’entrée



| S’inscrire      | Nom | Count              | R/W (Lecture/écriture) | Dimension | Indexable par r\# | Valeurs par défaut | DCL obligatoire |
|---------------|------|--------------------|-----|-----------|------------------|----------|--------------|
| r\#           |      | 4096 (r \# + x \# \[ n \] ) | R/W (Lecture/écriture) | 4         | Non               | None     | Oui          |
| x \# \[ n\]      |      | 4096 (r \# + x \# \[ n \] ) | R/W (Lecture/écriture) | 4         | Oui              | None     | Oui          |
| v\#           |      | 32                 | R   | 4         | Oui              | None     | Oui          |
| t\#           |      | 128                | R   | 1         | Non               | None     | Oui          |
| s\#           |      | 16                 | R   | 1         | Non               | None     | Oui          |
| \# \[ index CB\] |      | 15                 | R   | 4         | Oui (contenu)    | Aucun     | Oui          |
| \[index ICB\]  |      | 1                  | R   | 4         | Oui (contenu)    | Aucun     | Oui          |



 

## <a name="output-registers"></a>Registres de sortie



| S’inscrire | Nom            | Count | R/W (Lecture/écriture) | Dimension | Indexable par r\# | Valeurs par défaut | DCL obligatoire |
|----------|-----------------|-------|-----|-----------|------------------|----------|--------------|
| NULL     | Ignorer le résultat  | N/A   | W   | N/A       | N/A              | N/A      | Non           |
| sorties\#      | Registre de sortie | 32    | W   | N/A       | N/A              | 4        | Oui          |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Nuanceur modèle 4](dx-graphics-hlsl-sm4.md)
</dt> </dl>

 

 




