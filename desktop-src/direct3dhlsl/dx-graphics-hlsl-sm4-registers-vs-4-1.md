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
ms.openlocfilehash: df2254c111303129327d255f94727a5e42ac1c0c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126941108"
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
| \# \[ index CB\] |      | 15                 | R   | 4         | Oui (contenu)    | None     | Oui          |
| \[index ICB\]  |      | 1                  | R   | 4         | Oui (contenu)    | None     | Oui          |



 

## <a name="output-registers"></a>Registres de sortie



| S’inscrire | Nom            | Count | R/W (Lecture/écriture) | Dimension | Indexable par r\# | Valeurs par défaut | DCL obligatoire |
|----------|-----------------|-------|-----|-----------|------------------|----------|--------------|
| NULL     | Ignorer le résultat  | N/A   | W   | N/A       | N/A              | N/A      | Non           |
| sorties\#      | Registre de sortie | 32    | W   | N/A       | N/A              | 4        | Oui          |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Nuanceur modèle 4](dx-graphics-hlsl-sm4.md)
</dt> </dl>

 

 




