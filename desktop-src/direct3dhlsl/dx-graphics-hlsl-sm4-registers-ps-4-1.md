---
title: Registres-ps_4_1
description: Cette section contient des informations de référence pour les registres d’entrée et de sortie implémentés par le nuanceur de pixels version 4 \_ 1.
ms.assetid: d3f3e264-569e-43a6-a06b-a512d36a7b53
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 1cf70a24ad2fa7e77f7a5a90f6ec247179464f5c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126941112"
---
# <a name="registers---ps_4_1"></a>Registres-PS \_ 4 \_ 1

Cette section contient des informations de référence pour les registres d’entrée et de sortie implémentés par le nuanceur de pixels version 4 \_ 1.

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



| S’inscrire | Nom             | Count | R/W (Lecture/écriture) | Dimension | Indexable par r\# | Valeurs par défaut | DCL obligatoire |
|----------|------------------|-------|-----|-----------|------------------|----------|--------------|
| NULL     | Ignorer le résultat   | N/A   | W   | N/A       | N/A              | N/A      | Non           |
| sorties\#      | Registre de sortie  | 8     | W   | N/A       | N/A              | 4        | Non           |
| oDepth   | Profondeur de sortie     | 1     | W   | N/A       | N/A              | 1        | N/A          |
| oMask    | Masque MSAA de sortie | 1     | W   | N/A       | N/A              | 1        | N/A          |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Nuanceur modèle 4](dx-graphics-hlsl-sm4.md)
</dt> </dl>

 

 




