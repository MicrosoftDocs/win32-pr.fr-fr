---
title: Registres-cs_5_0
description: Les registres d’entrée et de sortie suivants sont implémentés dans le nuanceur de calcul version 5 \_ 0.
ms.assetid: A602BA9F-0934-472F-BB07-5E7A97763CAB
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b01d761fba2b126559e18caf7cf917482d83fec952798b80c3ffc756a5bf3418
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120023579"
---
# <a name="registers---cs_5_0"></a>Registres-cs \_ 5 \_ 0

Les registres d’entrée et de sortie suivants sont implémentés dans le nuanceur de calcul version 5 \_ 0.

## <a name="input-registers"></a>Registres d’entrée



| Type de Registre                                        | Count                                                  | R/W (Lecture/écriture) | Dimension                        | Indexable par r\# | Valeurs par défaut | DCL obligatoire |
|------------------------------------------------------|--------------------------------------------------------|-----|----------------------------------|------------------|----------|--------------|
| Temp 32 bits (r \# )                                    | 4096 (r \# + x \# \[ n \] )                                     | R/W (Lecture/écriture) | 4                                | Non               | None     | Oui          |
| Tableau Temp indexable 32 bits (x \# \[ n \] )               | 4096 (r \# + x \# \[ n \] )                                     | R/W (Lecture/écriture) | 4                                | Oui              | None     | Oui          |
| Mémoire partagée de groupe de threads 32 bits (g \# \[ n \] )         | 8192 (somme de toutes les decls de mémoire partagée pour le groupe de threads) | R/W (Lecture/écriture) | 1 (peut être déclarée de différentes façons) | Oui              | None     | Oui          |
| Élément dans une ressource d’entrée (t \# )                   | 128                                                    | R   | 1                                | Non               | None     | Oui          |
| Échantillonneur (s \# )                                        | 16                                                     | R   | 1                                | Non               | None     | Oui          |
| Référence ConstantBuffer ( \# \[ index CB \] )             | 15                                                     | R   | 4                                | Oui (contenu)   | Aucun     | Oui          |
| Référence ConstantBuffer immédiate ( \[ index ICB \] )    | 1                                                      | R   | 4                                | Oui (contenu)    | Aucun     | Oui          |
| ThreadID (vThreadID.xyz)                             | 1                                                      | R   | 3                                | Non               | N/A      | Oui          |
| ThreadGroupID (vThreadGroupID.xyz)                   | 1                                                      | R   | 3                                | Non               | N/A      | Oui          |
| ThreadIDInGroup (vThreadIDInGroup.xyz)               | 1                                                      | R   | 3                                | Non               | N/A      | Oui          |
| ThreadIDInGroupFlattened (vThreadIDInGroupFlattened) | 1                                                      | R   | 1                                | Non               | N/A      | Oui          |



 

## <a name="output-registers"></a>Registres de sortie



| Type de Registre                                               | Count | R/W (Lecture/écriture) | Dimension | Indexable par r\# | Valeurs par défaut | DCL obligatoire |
|-------------------------------------------------------------|-------|-----|-----------|------------------|----------|--------------|
| NULL (ignorer le résultat, utile pour les opérations avec plusieurs résultats) | N/A   | W   | N/A       | N/A              | N/A      | Non           |
| Vue d’accès non trié (u \# )                                 | 8     | R/W (Lecture/écriture) | 1         | Non               | Non       | Oui          |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Shader, modèle 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




