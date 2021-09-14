---
title: Registres-gs_4_1
description: Cette section contient des informations de référence pour les registres d’entrée et de sortie implémentés par les versions de nuanceur Geometry 4 \_ 0 et 4 \_ 1.
ms.assetid: 0312707D-11D0-45D0-9E8C-8BD2BC65352C
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a01f200bd4183843b1cfd2892fde5da442ca8d36
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126941123"
---
# <a name="registers---gs_4_1"></a>Registres-GS \_ 4 \_ 1

Cette section contient des informations de référence pour les registres d’entrée et de sortie implémentés par les versions de nuanceur Geometry 4 \_ 0 et 4 \_ 1.

## <a name="input-registers"></a>Registres d’entrée



| S’inscrire                 | Nom | Count              | R/W (Lecture/écriture) | Dimension        | Indexable par r\# | Valeurs par défaut | DCL obligatoire |
|--------------------------|------|--------------------|-----|------------------|------------------|----------|--------------|
| r\#                      |      | 4096 (r \# + x \# \[ n \] ) | R/W (Lecture/écriture) | 4                | Non               | None     | Oui          |
| x \# \[ n\]                 |      | 4096 (r \# + x \# \[ n \] ) | R/W (Lecture/écriture) | 4                | Oui              | None     | Oui          |
| \# \[ élément sommet \] \[ v\] |      | 32                 | R   | 4 (COMP) \* 6 (vert) | Oui              | None     | Oui          |
| vprim                    |      | 1                  | R   | 1                | Non               | None     | Oui          |
| t\#                      |      | 128                | R   | 1                | Non               | None     | Oui          |
| s\#                      |      | 16                 | R   | 1                | Non               | None     | Oui          |
| \# \[ index CB\]            |      | 15                 | R   | 4                | Oui (contenu)    | None     | Oui          |
| \[index ICB\]             |      | 1                  | R   | 4                | Oui (contenu)    | None     | Oui          |



 

## <a name="output-registers"></a>Registres de sortie



| S’inscrire | Nom            | Count | R/W (Lecture/écriture) | Dimension | Indexable par r\# | Valeurs par défaut | DCL obligatoire |
|----------|-----------------|-------|-----|-----------|------------------|----------|--------------|
| NULL     | Ignorer le résultat  | N/A   | W   | N/A       | N/A              | N/A      | Non           |
| sorties\#      | Registre de sortie | 32    | W   | N/A       | N/A              | 4        | Oui          |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Nuanceur modèle 4](dx-graphics-hlsl-sm4.md)
</dt> </dl>

 

 




