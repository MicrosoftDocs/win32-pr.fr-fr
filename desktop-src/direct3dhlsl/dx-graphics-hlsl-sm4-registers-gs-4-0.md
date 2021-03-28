---
title: Registres-gs_4_0
description: Cette section contient des informations de référence pour les registres d’entrée et de sortie implémentés par le nuanceur Geometry version 4 \_ 0.
ms.assetid: 1f3ebd71-19de-4e26-87f0-4fb5c8e2a343
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 9c5db86ffb797434af4badd6496b71a4ad684583
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104507263"
---
# <a name="registers---gs_4_0"></a>Registres-GS \_ 4 \_ 0

Cette section contient des informations de référence pour les registres d’entrée et de sortie implémentés par le nuanceur Geometry version 4 \_ 0.

## <a name="input-registers"></a>Registres d’entrée



| S’inscrire                 | Nom | Count              | R/W (Lecture/écriture) | Dimension        | Indexable par r\# | Valeurs par défaut | DCL obligatoire |
|--------------------------|------|--------------------|-----|------------------|------------------|----------|--------------|
| r\#                      |      | 4096 (r \# + x \# \[ n \] ) | R/W (Lecture/écriture) | 4                | Non               | None     | Oui          |
| x \# \[ n\]                 |      | 4096 (r \# + x \# \[ n \] ) | R/W (Lecture/écriture) | 4                | Oui              | None     | Oui          |
| \# \[ élément sommet \] \[ v\] |      | 32                 | R   | 4 (COMP) \* 6 (vert) | Oui              | None     | Oui          |
| vprim                    |      | 1                  | R   | 1                | Non               | None     | Oui          |
| t\#                      |      | 128                | R   | 1                | Non               | None     | Oui          |
| s\#                      |      | 16                 | R   | 1                | Non               | None     | Oui          |
| \# \[ index CB\]            |      | 15                 | R   | 4                | Oui (contenu)    | Aucun     | Oui          |
| \[index ICB\]             |      | 1                  | R   | 4                | Oui (contenu)    | Aucun     | Oui          |



 

## <a name="output-registers"></a>Registres de sortie



| S’inscrire | Nom            | Count | R/W (Lecture/écriture) | Dimension | Indexable par r\# | Valeurs par défaut | DCL obligatoire |
|----------|-----------------|-------|-----|-----------|------------------|----------|--------------|
| NULL     | Ignorer le résultat  | N/A   | W   | N/A       | N/A              | N/A      | Non           |
| sorties\#      | Registre de sortie | 32    | W   | N/A       | N/A              | 4        | Oui          |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Nuanceur modèle 4](dx-graphics-hlsl-sm4.md)
</dt> </dl>

 

 




