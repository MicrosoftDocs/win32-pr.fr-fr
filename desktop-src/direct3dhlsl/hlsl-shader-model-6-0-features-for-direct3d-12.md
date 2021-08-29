---
title: Modèle de nuanceur HLSL 6.0
description: Décrit les fonctions intrinsèques de l’opération Wave ajoutées au modèle de nuanceur HLSL 6,0.
ms.assetid: BF968CD3-AC67-48DB-B93F-EF54B680106F
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 494dbb4fd3008bbb3b5441fbc4867f5009c8d3df
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122886105"
---
# <a name="hlsl-shader-model-60"></a>Modèle de nuanceur HLSL 6.0

Décrit les fonctions intrinsèques de l’opération Wave ajoutées au modèle de nuanceur HLSL 6,0.

- [Modèle de nuanceur 6,0](#shader-model-60)
- [Terminologie](#terminology)
- [Intrinsèques du langage d’ombrage](#shading-language-intrinsics)
    - [Requête Wave](#wave-query)
    - [Voix des sons](#wave-vote)
    - [Broadcast Wave](#wave-broadcast)
    - [Réduction des vagues](#wave-reduction)
    - [Balayage et préfixe Wave](#wave-scan-and-prefix)
    - [Opérations de lecture aléatoire à quatre cœurs](#quad-wide-shuffle-operations)
- [Fonctionnalité matérielle](#hardware-capability)
- [Rubriques connexes](#related-topics)

## <a name="shader-model-60"></a>Modèle de nuanceur 6,0

Pour les modèles de nuanceur antérieurs, la programmation HLSL n’expose qu’un seul thread d’exécution. De nouvelles opérations de niveau Wave sont fournies, à partir du modèle 6,0, afin de tirer explicitement parti du parallélisme des GPU actuels. de nombreux threads peuvent s’exécuter dans échelons sur le même cœur simultanément. Par exemple, les intrinsèques Model 6,0 permettent l’élimination des constructions de cloisonnement lorsque la portée de la synchronisation est comprise dans la largeur du processeur SIMD, ou dans tout autre ensemble de threads qui sont considérés comme atomiques les uns par rapport aux autres.

Les cas d’utilisation potentiels incluent : compactage de flux, réductions, transposer des blocs, tri bitonique ou transformations de Fourier rapide (FFT), compartimentage, déduplication de flux et scénarios similaires.

La plupart des intrinsèques apparaissent dans les nuanceurs de pixels et les nuanceurs de calcul, bien qu’il existe certaines exceptions (notées pour chaque fonction). Les fonctions ont été ajoutées à la configuration requise pour le niveau de fonctionnalité DirectX 12,0, sous l’API de niveau 12.

Le paramètre de *&lt; &gt; type* et la valeur de retour de ces fonctions impliquent le type de l’expression, les types pris en charge sont ceux de la liste suivante qui sont *également* présents dans le modèle de nuanceur cible pour votre application :

- Half, Half2, half3, half4
- float, float2, float3, float4
- double, double2, double3, double4
- int, Int2, Int3, INT4
- uint, uint2, uint3, uint4
- short, Short2, short3, Short4
- UShort, ushort2, ushort3, ushort4
- UInt64 \_ t, UInt64 \_ T2, UInt64 \_ T3, UInt64 \_ T4

Certaines opérations (comme les opérateurs de bits) prennent uniquement en charge les types d’entiers.

## <a name="terminology"></a>Terminologie

| **Terme** | **Définition** |
|-|-|
| Couloir | Un seul thread d’exécution. Les modèles de nuanceur antérieurs à la version 6,0 exposent uniquement l’un d’entre eux au niveau de la langue, ce qui laisse l’expansion au traitement SIMD parallèle entièrement jusqu’à l’implémentation. |
| Vague | Un ensemble de couloirs (threads) exécutés simultanément dans le processeur. Aucune barrière explicite n’est requise pour garantir qu’elles s’exécutent en parallèle. Les concepts similaires sont les suivants : « Warp » et « Wavefront ». |
| Voie inactive | Un couloir qui n’est pas exécuté, par exemple en raison du déroulement du contrôle, ou un travail insuffisant pour remplir la taille minimale de l’onde. |
| Voie active | Voie pour laquelle l’exécution est exécutée. Dans les nuanceurs de pixels, il peut inclure tous les couloirs de pixels d’assistance. |
| Quadruple | Ensemble de 4 couloirs adjacents correspondant aux pixels disposés en carré 2x2. Ils sont utilisés pour estimer les dégradés par différenciation dans x ou y. Une vague peut être composée de plusieurs Quad. Tous les pixels d’un quadruple actif sont exécutés (et peuvent être des « couloirs actifs »), mais ceux qui ne produisent pas de résultats visibles sont « couloirs d’assistance ». |
| Voie d’assistance | Une voie qui est exécutée uniquement à des fins de dégradés dans le nuanceur de pixels Quad. La sortie d’un tel couloir est ignorée et n’est donc pas rendue sur la surface de destination. |

## <a name="shading-language-intrinsics"></a>Intrinsèques du langage d’ombrage

Toutes les opérations de ce modèle de nuanceur ont été ajoutées dans une plage de fonctions intrinsèques.

### <a name="wave-query"></a>Requête Wave

Intrinsèques pour l’interrogation d’une seule vague.

| **Intrinsic** | **Description** | **Nuanceur de pixels** | **Nuanceur de calcul** |
|-|-|-|-|
| [**WaveGetLaneCount**](wavegetlanecount.md) | Retourne le nombre de couloirs dans l’onde actuelle. | \* | \* |
| [**WaveGetLaneIndex**](wavegetlaneindex.md) | Retourne l’index de la voie active dans l’onde actuelle. | \* | \* |
| [**WaveIsFirstLane**](waveisfirstlane.md) | Retourne true uniquement pour la voie active dans l’onde actuelle avec le plus petit index | \* | \* |

### <a name="wave-vote"></a>Voix des sons

Cet ensemble d’intrinsèques compare les valeurs entre les threads actifs actuellement à partir de l’onde actuelle.

| **Intrinsic** | **Description** | **Nuanceur de pixels** | **Nuanceur de calcul** |
|-|-|-|-|
| [**WaveActiveAnyTrue**](waveanytrue.md) | Retourne la valeur true si l’expression est vraie dans une voie active de l’onde actuelle. | \* | \* |
| [**WaveActiveAllTrue**](wavealltrue.md) | Retourne la valeur true si l’expression est vraie dans tous les couloirs actifs de l’onde actuelle. | \* | \* |
| [**WaveActiveBallot**](waveballot.md) | Retourne un masque de bits d’entier non signé 64 bits de l’évaluation de l’expression booléenne pour tous les couloirs actifs dans l’onde spécifiée. | \* | \* |

### <a name="wave-broadcast"></a>Broadcast Wave

Ces fonctions intrinsèques activent tous les couloirs actifs dans l’onde actuelle pour recevoir la valeur de la voie spécifiée, en la diffusant efficacement. La valeur de retour d’une voie non valide n’est pas définie.

| **Intrinsic** | **Description** | **Nuanceur de pixels** | **Nuanceur de calcul** |
|-|-|-|-|
| [**WaveReadLaneAt**](wavereadlaneat.md) | Retourne la valeur de l’expression pour l’index Lane donné dans l’onde spécifiée. | \* | \* |
| [**WaveReadLaneFirst**](wavereadfirstlane.md) | Retourne la valeur de l’expression pour la voie active de l’onde actuelle avec l’index le plus petit. | \* | \* |

### <a name="wave-reduction"></a>Réduction des vagues

Ces fonctions intrinsèques calculent l’opération spécifiée sur tous les couloirs actifs de l’onde et diffusent le résultat final à tous les couloirs actifs. Par conséquent, la sortie finale est garantie uniforme sur toute la vague.

| **Intrinsic** | **Description** | **Nuanceur de pixels** | **Nuanceur de calcul** |
|-|-|-|-|
| [**WaveActiveAllEqual**](waveactiveallequal.md) | Retourne la valeur true si l’expression est la même pour chaque voie active de l’onde actuelle (et donc uniforme sur celle-ci). | \* | \* |
| [**WaveActiveBitAnd**](waveallbitand.md) | Retourne l’opération de bits AND de toutes les valeurs de l’expression sur tous les couloirs actifs de l’onde actuelle, puis réplique le résultat sur tous les couloirs de l’onde. | \* | \* |
| [**WaveActiveBitOr**](waveallbitor.md) | Retourne l’opération or au niveau du bit de toutes les valeurs de l’expression sur tous les couloirs actifs de l’onde actuelle, puis réplique le résultat sur tous les couloirs de l’onde. | \* | \* |
| [**WaveActiveBitXor**](waveallbitxor.md) | Retourne l’opérateur de bits or exclusif de toutes les valeurs de l’expression sur tous les couloirs actifs de l’onde actuelle, puis réplique le résultat sur tous les couloirs de l’onde. | \* | \* |
| [**WaveActiveCountBits**](waveactivecountbits.md) | Compte le nombre de variables booléennes qui ont la valeur true sur tous les couloirs actifs de l’onde actuelle, et réplique le résultat sur tous les couloirs de l’onde. | \* | \* |
| [**WaveActiveMax**](waveallmax.md) | Calcule la valeur maximale de l’expression sur tous les couloirs actifs de l’onde actuelle et réplique le résultat sur tous les couloirs de l’onde. | \* | \* |
| [**WaveActiveMin**](waveallmin.md) | Calcule la valeur minimale de l’expression sur tous les couloirs actifs de l’onde actuelle et réplique le résultat sur tous les couloirs de l’onde. | \* | \* |
| [**WaveActiveProduct**](waveallproduct.md) | Multiplie les valeurs de l’expression ensemble sur tous les couloirs actifs de l’onde actuelle et réplique le résultat sur tous les couloirs de l’onde. | \* | \* |
| [**WaveActiveSum**](waveallsum.md) | Additionne la valeur de l’expression sur tous les couloirs actifs de l’onde actuelle et la réplique sur tous les couloirs de l’onde actuelle, puis réplique le résultat sur tous les couloirs de l’onde. | \* | \* |

### <a name="wave-scan-and-prefix"></a>Balayage et préfixe Wave

Ces fonctions intrinsèques appliquent l’opération à chaque voie et laissent chaque résultat partiel du calcul dans la voie correspondante.

| **Intrinsic** | **Description** | **Nuanceur de pixels** | **Nuanceur de calcul** |
|-|-|-|-|
| [**WavePrefixCountBits**](waveprefixcountbytes.md) | Retourne la somme de toutes les variables booléennes spécifiées ayant la valeur true sur tous les couloirs actifs dont les index sont plus petits que le couloir actuel. | \* | \* |
| [**WavePrefixSum**](waveprefixsum.md) | Retourne la somme de toutes les valeurs des couloirs actifs avec des index plus petits que celui-ci. | \* | \* |
| [**WavePrefixProduct**](waveprefixproduct.md) | Retourne le produit de toutes les valeurs des couloirs avant l’un des sons spécifiés. | \* | \* |

### <a name="quad-wide-shuffle-operations"></a>Opérations de lecture aléatoire à quatre cœurs

Ces fonctions intrinsèques effectuent des opérations de permutation sur les valeurs sur une vague connue pour contenir des Quad nuanceurs de pixels, comme défini ici. Les index des pixels du quadruple sont définis dans la ligne d’analyse ou l’ordre de lecture, où les coordonnées au sein d’un quadruple sont :

+---------> X 

| [0] [1] 

| [2] [3] 

v 

O 


Ces routines fonctionnent dans des nuanceurs de calcul ou des nuanceurs de pixels. Dans les nuanceurs de calcul, ils fonctionnent en quatre cœurs définis comme des groupes uniformément divisés de 4 au sein d’une vague SIMD. Dans les nuanceurs de pixels, ils doivent être utilisés sur les vagues capturées par WaveQuadLanes, sinon les résultats ne sont pas définis.

| **Intrinsic** | **Description** | **Nuanceur de pixels** | **Nuanceur de calcul** |
|-|-|-|-|
| [**QuadReadLaneAt**](quadreadlaneat.md) | Retourne la valeur source spécifiée lue à partir de la voie du quadruple actuel identifié par quadLaneID \[ 0.. 3, \] qui doit être uniforme sur le quadruple. | \* | |
| [**QuadReadAcrossDiagonal**](quadreadacrossdiagonal.md) | Retourne la valeur locale spécifiée qui est lue à partir de la voie diagonalement opposée dans ce Quad. | \* | |
| [**QuadReadAcrossX**](quadswapx.md) | Retourne la valeur source spécifiée lue à partir de l’autre Lane dans ce Quad sur l’axe X. | \* | |
| [**QuadReadAcrossY**](quadswapy.md) | Retourne la valeur source spécifiée lue à partir de l’autre Lane dans ce Quad sur l’axe Y. | \* | |

## <a name="hardware-capability"></a>Fonctionnalité matérielle

Pour vérifier que les fonctionnalités de l’opération Wave sont disponibles sur un matériel spécifique, appelez [**ID3D12Device :: CheckFeatureSupport**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-checkfeaturesupport), en notant la description et l’utilisation de la structure de données de la [**\_ fonctionnalité D3D12 \_ \_ D3D12 \_ options1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options1) .

## <a name="related-topics"></a>Rubriques connexes

* [Guide de programmation pour HLSL](dx-graphics-hlsl-pguide.md)
* [Intrinsèques du modèle de nuanceur 6](shader-model-6-0.md)
