---
title: Registres-ps_4_0
description: Cette section contient des informations de référence pour les registres d’entrée et de sortie implémentés par le nuanceur de pixels version 4 \_ 0.
ms.assetid: 8b83667f-f599-4105-b68c-0d6aa7c528ab
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 3dea9606419f32a168c08cc1efbebb5e285d3815
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104379997"
---
# <a name="registers---ps_4_0"></a>Registres-PS \_ 4 \_ 0

Cette section contient des informations de référence pour les registres d’entrée et de sortie implémentés par le nuanceur de pixels version 4 \_ 0.

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
| sorties\#      | Registre de sortie | 8     | W   | N/A       | N/A              | 4        | Non           |
| oDepth   | Profondeur de sortie    | 1     | W   | N/A       | N/A              | 1        | N/A          |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Nuanceur modèle 4](dx-graphics-hlsl-sm4.md)
</dt> </dl>

 

 




