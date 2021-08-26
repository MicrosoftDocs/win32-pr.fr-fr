---
title: Registres-gs_5_0
description: Les registres d’entrée et de sortie suivants sont implémentés dans le nuanceur Geometry version 5 \_ 0.
ms.assetid: 9E99F584-611F-4CFC-B69A-66F2B4545D36
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89e0bac8baf9be8428b53fa7949229361edf04132079a7a6ca6989dab92c44aa
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120023499"
---
# <a name="registers---gs_5_0"></a>Registres-GS \_ 5 \_ 0

Les registres d’entrée et de sortie suivants sont implémentés dans le nuanceur Geometry version 5 \_ 0.

## <a name="input-registers"></a>Registres d’entrée



| Type de Registre                                     | Count              | R/W (Lecture/écriture) | Dimension         | Indexable par r\# | Valeurs par défaut | DCL obligatoire |
|---------------------------------------------------|--------------------|-----|-------------------|------------------|----------|--------------|
| Temp 32 bits (r \# )                                 | 4096 (r \# + x \# \[ n \] ) | R/W (Lecture/écriture) | 4                 | Non               | None     | Oui          |
| Tableau Temp indexable 32 bits (x \# \[ n \] )            | 4096 (r \# + x \# \[ n \] ) | R/W (Lecture/écriture) | 4                 | Oui              | None     | Oui          |
| Entrée 32 bits ( \[ élément sommet v \] \[ \] )             | 32                 | R   | 4 (COMP) \* 32 (vert) | Oui              | None     | Oui          |
| ID de la primitive d’entrée 32 bits (vPrim)                 | 1                  | R   | 1                 | Non               | None     | Oui          |
| ID d’instance d’entrée 32 bits (vInstanceID)            | 1                  | R   | 1                 | Non               | None     | Oui          |
| Élément dans une ressource d’entrée (t \# )                | 128                | R   | 1                 | Non               | None     | Oui          |
| Échantillonneur (s \# )                                     | 16                 | R   | 1                 | Non               | None     | Oui          |
| Référence ConstantBuffer ( \# \[ index CB \] )          | 15                 | R   | 4                 | Oui (contenu)    | Aucun     | Oui          |
| Référence ConstantBuffer immédiate ( \[ index ICB \] ) | 1                  | R   | 4                 | Oui (contenu)    | Aucun     | Oui          |



 

## <a name="output-registers"></a>Registres de sortie



| Type de Registre                                               | Count | R/W (Lecture/écriture) | Dimension | Indexable par r\# | Valeurs par défaut | DCL obligatoire |
|-------------------------------------------------------------|-------|-----|-----------|------------------|----------|--------------|
| NULL (ignorer le résultat, utile pour les opérations avec plusieurs résultats) | N/A   | W   | N/A       | N/A              | N/A      | Non           |
| Élément de données de vertex de sortie 32 bits (o \# )                     | 32    | W   | N/A       | N/A              | 4        | Oui          |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Shader, modèle 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




