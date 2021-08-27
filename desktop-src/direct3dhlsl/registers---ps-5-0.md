---
title: Registres-ps_5_0
description: Les registres d’entrée et de sortie suivants sont implémentés dans le nuanceur de pixels version 5 \_ 0.
ms.assetid: F16E5CB8-E1DB-48CD-8C20-DBF1DF971110
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d432e53626d547bcaf421a4b4ffd9c2aa0f5d0a78ecc3aff9f0b87059c40c0ac
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120095339"
---
# <a name="registers---ps_5_0"></a>Registres-PS \_ 5 \_ 0

Les registres d’entrée et de sortie suivants sont implémentés dans le nuanceur de pixels version 5 \_ 0.

## <a name="input-registers"></a>Registres d’entrée



| Type de Registre                                     | Count              | R/W (Lecture/écriture) | Dimension | Indexable par r\# | Valeurs par défaut | DCL obligatoire |
|---------------------------------------------------|--------------------|-----|-----------|------------------|----------|--------------|
| Temp 32 bits (r \# )                                 | 4096 (r \# + x \# \[ n \] ) | R/W (Lecture/écriture) | 4         | Non               | None     | Oui          |
| Tableau Temp indexable 32 bits (x \# \[ n \] )            | 4096 (r \# + x \# \[ n \] ) | R/W (Lecture/écriture) | 4         | Oui              | None     | Oui          |
| Attribut d’entrée 32 bits (v \# )                      | 32                 | R   | 4         | Oui              | None     | Oui          |
| Élément dans une ressource d’entrée (t \# )                | 128                | R   | 1         | Non               | None     | Oui          |
| Échantillonneur (s \# )                                     | 16                 | R   | 1         | Non               | None     | Oui          |
| Référence ConstantBuffer ( \# \[ index CB \] )          | 15                 | R   | 4         | Oui (contenu)    | Aucun     | Oui          |
| Référence ConstantBuffer immédiate ( \[ index ICB \] ) | 1                  | R   | 4         | Oui (contenu)    | Aucun     | Oui          |



 

## <a name="output-registers"></a>Registres de sortie



| Type de Registre                                                      | Count                   | R/W (Lecture/écriture) | Dimension                                | Indexable par r\# | Valeurs par défaut | DCL obligatoire |
|--------------------------------------------------------------------|-------------------------|-----|------------------------------------------|------------------|----------|--------------|
| NULL (ignorer le résultat, utile pour les opérations avec plusieurs résultats) | N/A                     | W   | N/A                                      | N/A              | N/A      | Non           |
| Élément de sortie 32 bits (o \# )                                        | 8                       | W   | 4                                        | N/A              | N/A      | Non           |
| Vue d’accès non trié (u \# )                                        | 8 \# de rendertargets | R/W (Lecture/écriture) | \_Composants du Registre d3d11 PS \_ cs \_ UAV \_ \_ | Non               | Non       | Oui          |
| 32-bit \[ 0.0 f.. \] oDepth (profondeur de sortie float) 1.0                  | 1                       | W   | 1                                        | N/A              | N/A      | Oui          |
| exemple de masque de sortie 32 bits UINT (oMask)                             | 1                       | W   | 1                                        | N/A              | N/A      | Oui          |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Shader, modèle 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




