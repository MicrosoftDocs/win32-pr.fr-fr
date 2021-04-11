---
title: Étape nuanceur de sommets
description: L’étape vertex-shader (VS) traite les vertex de l’assembleur d’entrée, en effectuant des opérations par vertex telles que les transformations, l’apparence, la transformation et l’éclairage par vertex.
ms.assetid: C6A39F48-A243-4049-8AED-0B521BEDFA76
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b19a291b4abed572da54f9a2616ce19e926e1c6f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104031268"
---
# <a name="vertex-shader-stage"></a>Étape nuanceur de sommets

L’étape vertex-shader (VS) traite les vertex de l’assembleur d’entrée, en effectuant des opérations par vertex telles que les transformations, l’apparence, la transformation et l’éclairage par vertex. Les nuanceurs vertex fonctionnent toujours sur un vertex d’entrée unique et produisent un seul vertex de sortie. L’étape du nuanceur de sommets doit toujours être active pour que le pipeline s’exécute. Si aucune modification ou transformation de vertex n’est requise, un nuanceur de sommets directs doit être créé et défini sur le pipeline.

## <a name="the-vertex-shader"></a>Nuanceur de sommets

Chaque vertex d’entrée de nuanceur de sommets peut être constitué de vecteurs jusqu’à 16 32 bits (jusqu’à 4 composants chacun) et chaque vertex de sortie peut être constitué de plusieurs vecteurs à 4 composants de 16 32 bits. Tous les nuanceurs de vertex doivent avoir au minimum une entrée et une sortie, ce qui peut être aussi limité qu’une seule valeur scalaire.

L’étape vertex-shader peut consommer deux valeurs générées par le système à partir de l’assembleur d’entrée : VertexID et InstanceID (consultez valeurs système et sémantiques). Étant donné que VertexID et InstanceID sont tous deux significatifs au niveau d’un vertex, et que les ID générés par le matériel peuvent uniquement être introduits dans la première étape qui les comprend, ces valeurs d’ID peuvent uniquement être chargées dans l’étape de nuanceur de sommets.

Les nuanceurs vertex sont toujours exécutés sur tous les vertex, y compris les vertex adjacents dans les topologies de la primitive d’entrée avec contiguïté. Le nombre de fois que le nuanceur vertex a été exécuté peut être interrogé à partir du processeur à l’aide des statistiques de pipeline VSInvocations.

Un nuanceur de sommets peut effectuer des opérations d’échantillonnage de charge et de texture lorsque les dérivés de l’espace écran ne sont pas requis (à l’aide des fonctions intrinsèques HLSL : [Sample (DirectX HLSL texture Object)](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-to-sample), [SAMPLECMPLEVELZERO (DirectX HLSL texture Object)](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-to-samplecmplevelzero)et [SampleGrad (DirectX HLSL texture Object)](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-to-samplegrad)).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Pipeline graphique](overviews-direct3d-11-graphics-pipeline.md)
</dt> <dt>

[Étapes de pipeline (Direct3D 10)](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-pipeline-stages)
</dt> </dl>

 

 