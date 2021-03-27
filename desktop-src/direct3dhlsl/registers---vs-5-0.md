---
title: Registres-vs_5_0
description: Les registres d’entrée et de sortie suivants sont implémentés dans le nuanceur de sommets version 5 \_ 0.
ms.assetid: 475753C7-C055-4DB7-9DC3-6C734413A92B
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6eb1dc211f5f3dd8819577c796849dcb86012cc0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104971439"
---
# <a name="registers---vs_5_0"></a>Registres-vs \_ 5 \_ 0

Les registres d’entrée et de sortie suivants sont implémentés dans le nuanceur de sommets version 5 \_ 0.

## <a name="input-registers"></a>Registres d’entrée



| Type de Registre                                      | Count              | R/W (Lecture/écriture) | Dimension | Indexable par r\# | Valeurs par défaut | DCL obligatoire |
|----------------------------------------------------|--------------------|-----|-----------|------------------|----------|--------------|
| Temp 32 bits (r \# )                                  | 4096 (r \# + x \# \[ n \] ) | R/W (Lecture/écriture) | 4         | Non               | None     | Oui          |
| Tableau Temp indexable 32 bits (x \# \[ n \] )             | 4096 (r \# + x \# \[ n \] ) | R/W (Lecture/écriture) | 4         | Oui              | None     | Oui          |
| entrée 32 bits (v \# )                                 | 32                 | R   | 4         | Oui              | None     | Oui          |
| Élément dans une ressource d’entrée (t \# )                 | 128                | R   | 1         | Non               | None     | Oui          |
| Échantillonneur (s \# )                                      | 16                 | R   | 1         | Non               | None     | Oui          |
| Référence ConstantBuffer ( \# \[ index CB \] )           | 15                 | R   | 4         | Oui (contenu)    | Aucun     | Oui          |
| iImmediate ConstantBuffer Reference ( \[ index ICB \] ) | 1                  | R   | 4         | Oui (contenu)    | Aucun     | Oui          |



 

## <a name="output-registers"></a>Registres de sortie



| Type de Registre                                                      | Count | R/W (Lecture/écriture) | Dimension | Indexable par r\# | Valeurs par défaut | DCL obligatoire |
|--------------------------------------------------------------------|-------|-----|-----------|------------------|----------|--------------|
| NULL (ignorer le résultat, utile pour les opérations avec plusieurs résultats) | N/A   | W   | N/A       | N/A              | N/A      | Non           |
| Élément de données de vertex de sortie 32 bits (o \# )                            | 32    | W   | 4         | N/A              | N/A      | Oui          |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Shader, modèle 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




