---
title: Shader, modèle 6
description: Le modèle de nuanceur 6,0 ajoute une plage d’intrinsèques de l’opération Wave pour les nuanceurs de pixels et de calcul.
ms.assetid: 2F28F86D-F599-47EA-90D7-6833ABA976FC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33eb4eab2a92e929bdefdc1df0f9cb1e0d84909a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127524504"
---
# <a name="shader-model-6"></a>Shader, modèle 6

Toutes les fonctions d’intrinsèques Wave non quadruples sont disponibles dans toutes les étapes du nuanceur. Les intrinsèques Quad Wave sont uniquement disponibles dans les nuanceurs de pixels et de calcul.

## <a name="in-this-section"></a>Contenu de cette section



| Rubrique                                                                 | Description                                                                                                                                                               |
|-----------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**QuadReadAcrossDiagonal**](quadreadacrossdiagonal.md)<br/> | Retourne la valeur locale spécifiée qui est lue à partir de la voie diagonalement opposée dans ce Quad.<br/>                                                                |
| [**QuadReadLaneAt**](quadreadlaneat.md)<br/>                   | Retourne la valeur source spécifiée à partir du Lane identifié par l’ID Lane dans le quad actuel.<br/>                                                            |
| [**QuadReadAcrossX**](quadswapx.md)<br/>                      | Retourne la valeur locale spécifiée lue à partir de l’autre Lane dans ce Quad sur l’axe X.<br/>                                                                    |
| [**QuadReadAcrossY**](quadswapy.md)<br/>                      | Retourne la valeur source spécifiée lue à partir de l’autre Lane dans ce Quad sur l’axe Y.<br/>                                                                   |
| [**WaveActiveAllEqual**](waveactiveallequal.md)<br/>           | Retourne la valeur true si l’expression est la même pour chaque voie active de l’onde actuelle (et donc uniforme sur celle-ci).<br/>                                             |
| [**WaveActiveBitAnd**](waveallbitand.md)<br/>                  | Retourne l’opération de bits AND de toutes les valeurs de l’expression sur tous les couloirs actifs de l’onde actuelle et la réplique vers tous les couloirs actifs. <br/>           |
| [**WaveActiveBitOr**](waveallbitor.md)<br/>                    | Retourne l’opération or au niveau du bit de toutes les valeurs de l’expression sur tous les couloirs actifs de l’onde actuelle et la réplique vers tous les couloirs actifs. <br/>            |
| [**WaveActiveBitXor**](waveallbitxor.md)<br/>                  | Retourne l’opérateur de bits XOR de toutes les valeurs de l’expression sur tous les couloirs actifs de l’onde actuelle et les réplique sur tous les couloirs actifs. <br/>           |
| [**WaveActiveCountBits**](waveactivecountbits.md)<br/>         | Compte le nombre de variables booléennes qui ont la valeur true sur tous les couloirs actifs de l’onde actuelle, et réplique le résultat sur tous les couloirs de l’onde.<br/> |
| [**WaveActiveMax**](waveallmax.md)<br/>                        | Retourne la valeur maximale de l’expression sur tous les couloirs actifs de l’onde actuelle et la réplique sur tous les couloirs actifs. <br/>                           |
| [**WaveActiveMin**](waveallmin.md)<br/>                        | Retourne la valeur minimale de l’expression sur tous les couloirs actifs de l’onde actuelle pour la répliquer à tous les couloirs actifs. <br/>                               |
| [**WaveActiveProduct**](waveallproduct.md)<br/>                | Multiplie les valeurs de l’expression sur tous les couloirs actifs de l’onde actuelle et les réplique sur tous les couloirs actifs.<br/>                       |
| [**WaveActiveSum**](waveallsum.md)<br/>                        | Additionne la valeur de l’expression sur tous les couloirs actifs de l’onde actuelle et la réplique sur tous les couloirs de l’onde actuelle.<br/>                            |
| [**WaveActiveAllTrue**](wavealltrue.md)<br/>                   | Retourne la valeur true si l’expression est vraie dans tous les couloirs actifs de l’onde actuelle.<br/>                                                                                |
| [**WaveActiveAnyTrue**](waveanytrue.md)<br/>                   | Retourne la valeur true si l’expression est vraie dans l’un des couloirs actifs de l’onde actuelle.<br/>                                                                         |
| [**WaveActiveBallot**](waveballot.md)<br/>                     | Retourne un masque de bits d’entier non signé 4 bits de l’évaluation de l’expression booléenne pour tous les couloirs actifs dans l’onde spécifiée. <br/>                              |
| [**WaveGetLaneCount**](wavegetlanecount.md)<br/>               | Retourne le nombre de couloirs dans une vague sur cette architecture. <br/>                                                                                                   |
| [**WaveGetLaneIndex**](wavegetlaneindex.md)<br/>               | Retourne l’index de la voie active dans l’onde actuelle. <br/>                                                                                                |
| [**WaveIsFirstLane**](waveisfirstlane.md)<br/>                 | Retourne true uniquement pour la voie active dans l’onde actuelle avec l’index le plus petit. <br/>                                                                            |
| [**WavePrefixCountBits**](waveprefixcountbytes.md)<br/>        | Retourne la somme de toutes les variables booléennes spécifiées ayant la valeur true sur tous les couloirs actifs dont les index sont plus petits que le couloir actuel. <br/>                        |
| [**WavePrefixProduct**](waveprefixproduct.md)<br/>             | Retourne le produit de toutes les valeurs des couloirs actifs dans cette vague avec des index inférieurs à ce couloir.<br/>                                                    |
| [**WavePrefixSum**](waveprefixsum.md)<br/>                     | Retourne la somme de toutes les valeurs des couloirs actifs avec des index plus petits que celui-ci.<br/>                                                                   |
| [**WaveReadLaneFirst**](wavereadfirstlane.md)<br/>             | Retourne la valeur de l’expression pour la voie active de l’onde actuelle avec l’index le plus petit. <br/>                                                          |
| [**WaveReadLaneAt**](wavereadlaneat.md)<br/>                   | Retourne la valeur de l’expression pour l’index Lane donné dans l’onde spécifiée.<br/>                                                                        |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Vue d’ensemble du modèle de nuanceur 6](hlsl-shader-model-6-0-features-for-direct3d-12.md)
</dt> <dt>

[Modèles de nuanceur et profils Shader](dx-graphics-hlsl-models.md)
</dt> </dl>

 

 





