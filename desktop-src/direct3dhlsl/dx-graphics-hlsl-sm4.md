---
title: Nuanceur modèle 4
description: Le nuancier modèle 4 est un sur-ensemble des fonctionnalités du nuanceur modèle 3, sauf que le nuanceur modèle 4 ne prend pas en charge les fonctionnalités du nuanceur modèle 1.
ms.assetid: 76155749-11e9-41ff-881d-8f77f2729364
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: c863d952990cd05394244fe662650df59568eeaf
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126941104"
---
# <a name="shader-model-4"></a>Nuanceur modèle 4

Le nuancier modèle 4 est un sur-ensemble des fonctionnalités du [nuanceur modèle 3](dx-graphics-hlsl-sm3.md), sauf que le nuanceur modèle 4 ne prend pas en charge les fonctionnalités du nuanceur modèle 1. Il a été conçu à l’aide d’un noyau-nuanceur commun qui fournit un ensemble commun de fonctionnalités à tous les nuanceurs programmables, qui sont uniquement programmables à l’aide du langage HLSL.




| Fonctionnalité | Utilité | 
|---------|------------|
| Jeu d'instructions | <a href="dx-graphics-hlsl-intrinsic-functions.md"><strong>Fonctions HLSL</strong></a> | 
| Ensemble de registres | Le jeu de registres est accessible via des membres dans des mémoires tampons de constante et de texture à l’aide de la sémantique HLSL pour des éléments tels que la compression de composants.<ul><li>Registres de nuanceur de pixels (voir <a href="dx-graphics-hlsl-sm4-registers-ps-4-0.md">Registers-ps_4_0</a> et <a href="dx-graphics-hlsl-sm4-registers-ps-4-1.md">registers-ps_4_1</a>)</li><li>Registres de nuanceur vertex (voir <a href="dx-graphics-hlsl-sm4-registers-vs-4-0.md">Registers-vs_4_0</a> et <a href="dx-graphics-hlsl-sm4-registers-vs-4-1.md">registers-vs_4_1</a>)</li><li>Registres de nuanceur Geometry (voir <a href="dx-graphics-hlsl-sm4-registers-gs-4-0.md">registres-gs_4_0</a> et <a href="dx-graphics-hlsl-sm4-registers-gs-4-1.md">registres-gs_4_1</a>)</li></ul> | 
| Vertex shader Max | Pas de restriction | 
| Nuanceur de pixels max. | Pas de restriction | 
| Nouveaux profils de nuanceur ajoutés | gs_4_0, ps_4_0, vs_4_0, gs_4_1 *, ps_4_1*, gs_4_1 * | 
| Nouveau profil de Effect-Framework ajouté | fx_4_0, fx_4_1 * | 




 

\* -GS \_ 4 \_ 1, PS \_ 4 \_ 1, vs \_ 4 \_ 1 et FX \_ 4 \_ 1 sont pris en charge sur Direct3D 10,1 ou une version ultérieure.

Le Shader Model 4 prend en charge une nouvelle étape de pipeline, l’étape Geometry-Shader, qui peut être utilisée pour créer ou modifier une géométrie existante. Il comprend également deux nouveaux types d’objets : un objet de sortie de flux conçu pour la diffusion en continu de données à partir de l’étape Geometry, et un objet texture basé sur un modèle qui implémente les fonctions d’échantillonnage de texture.

-   [Common-Shader Core](dx-graphics-hlsl-common-core.md)
-   [Constantes](dx-graphics-hlsl-constants.md)
-   [Geometry-objet Shader](dx-graphics-hlsl-geometry-shader.md)
-   [Stream-sortie (objet)](dx-graphics-hlsl-so-type.md)
-   [Texture, objet](dx-graphics-hlsl-to-type.md)

Le modèle de nuanceur 4 prend en charge les règles de compression qui déterminent la façon dont les données peuvent être réorganisées lors de leur stockage. Ces règles sont décrites dans [règles de compression pour les variables constantes](dx-graphics-hlsl-packing-rules.md) .

La section [Shader Model 4 assembly](dx-graphics-hlsl-sm4-asm.md) décrit les instructions d’assembly que les nuanciers Model 4 et shader model 4,1 prennent en charge.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Modèles de nuanceur et profils Shader](dx-graphics-hlsl-models.md)
</dt> </dl>

 

 




