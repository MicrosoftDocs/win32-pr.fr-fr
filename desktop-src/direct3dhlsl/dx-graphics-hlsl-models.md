---
title: Modèles de nuanceur et profils Shader
description: Modèles de nuanceur et profils Shader
ms.assetid: 6224f05e-20b1-42ea-96fb-63dd0edb720e
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 963e68d5875c3ee512e7e0d6ee7c243db72f4400
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/30/2021
ms.locfileid: "113119614"
---
# <a name="shader-models-vs-shader-profiles"></a>Modèles de nuanceur et profils Shader

Le langage d’ombrage de haut niveau pour DirectX implémente une série de modèles de nuanceur. En HLSL, vous pouvez créer des nuanceurs programmables de type C pour le pipeline Direct3D. Chaque modèle de nuanceur s’appuie sur les fonctionnalités du modèle avant celui-ci, en implémentant davantage de fonctionnalités avec moins de restrictions.

Le Shader Model 1 a démarré avec DirectX 8 et inclut des instructions de niveau assembly et de type C. Ce modèle présente de nombreuses limitations provoquées par un matériel de nuanceur programmable précoce. Les modèles de nuanceur 2 et 3 s’étendent beaucoup sur le nombre d’instructions, et les nuanceurs de constantes pourraient utiliser. Elles sont bien plus puissantes que le modèle de nuanceur 1, mais contiennent néanmoins certaines des limitations existantes du premier modèle de nuanceur.

À compter de Windows Vista, le nuanceur modèle 4 est un remaniement complet. Il autorise un nombre illimité d’instructions et de constantes (dans les contraintes matérielles de votre ordinateur), a des objets basés sur des modèles pour rendre le nettoyeur d’échantillonnage de texture et plus efficace, et présente le moins de restrictions de modèle de nuanceur. Toutefois, elle nécessite la Windows Driver Model qui est uniquement disponible sur le système d’exploitation Windows Vista (ou version ultérieure).

## <a name="shader-profiles"></a>Profils de nuanceur

Un profil de nuanceur est la cible de la compilation d’un nuanceur. ce tableau répertorie les profils de nuanceur qui sont pris en charge par chaque modèle de nuanceur.



| Modèle de nuanceur                                                   | Profils de nuanceur                                                                                                                                                                                                                                                                                                      |
|----------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Modèle de nuanceur 1](dx-graphics-hlsl-sm1.md)         | vs \_ 1 \_ 1                                                                                                                                                                                                                                                                                              |
| [Nuancier, modèle 2](dx-graphics-hlsl-sm2.md)         | PS \_ 2 \_ 0, PS \_ 2 \_ x, vs \_ 2 \_ 0, vs \_ 2 \_ x, PS \_ 4 \_ 0 \_ niveau \_ 9 \_ 0, PS \_ 4 \_ 0 \_ niveau \_ 9 \_ 1, PS \_ 4 0 niveau 9 3, vs 4 0 niveau 9 0, vs 4 0 niveau 9 1, vs 4 0 niveau 9 3 \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ , lib \_ 4 \_ 0 \_ niveau \_ 9 \_ 1, lib \_ 4 \_ 0 \_ niveau \_ 9 \_ 3                                                                      |
| [Modèle de nuanceur 3](dx-graphics-hlsl-sm3.md)         | PS \_ 3 \_ 0, vs \_ 3 \_ 0                                                                                                                                                                                                                                                                                    |
| [Nuanceur modèle 4](dx-graphics-hlsl-sm4.md)         | CS \_ 4 \_ 0, GS \_ 4 \_ 0, PS \_ 4 \_ 0, vs \_ 4 \_ 0, CS \_ 4 \_ 1, GS \_ 4 \_ 1, PS \_ 4 \_ 1, vs \_ 4 \_ 1, lib \_ 4 \_ 0, lib \_ 4 \_ 1                                                                                                                                                                                                  |
| [Shader, modèle 5](d3d11-graphics-reference-sm5.md) | CS \_ 5 \_ 0, DS \_ 5 \_ 0, GS \_ 5 \_ 0, HS \_ 5 \_ 0, PS \_ 5 \_ 0, vs \_ 5 \_ 0, lib \_ 5 \_ 0 (même si GS \_ 4 \_ 0, GS \_ 4 \_ 1, PS 4 \_ \_ 0, PS \_ 4 \_ 1, vs \_ 4 \_ 0 et vs \_ 4 \_ 1 ont été introduits dans le modèle de nuanceur 4,0, le modèle de nuanceur 5 ajoute la prise en charge de ces profils de nuanceur pour les<br/> |
| [Shader, modèle 6](shader-model-6-0.md)             | CS \_ 6 \_ 0, DS \_ 6 \_ 0, GS \_ 6 \_ 0, HS \_ 6 \_ 0, PS \_ 6 \_ 0, vs \_ 6 \_ 0, lib \_ 6 \_ 0                                                                                                                                                                                                                                 |

Différences entre Direct3D 9 et Direct3D 10 :

- Direct3D 9 a introduit les modèles de nuanceur 1, 2 et 3.
- Direct3D 10 a introduit le nuanceur modèle 4.
- Direct3D 10,1 a introduit le modèle de nuanceur 4,1.



 

## <a name="effect-profiles"></a>Profils d’effet

Un profil d’effet est la cible pour la compilation d’un effet/nuanceur ; ce tableau répertorie les profils d’effet pris en charge par chaque version de Direct3D.

Différences entre Direct3D 9 et Direct3D 10 :

- Direct3D 9 a introduit Effect-profile des profils FX \_ 1 \_ 0 et FX \_ 2 \_ 0.
- Direct3D 10 a introduit Effect-Framework Profile FX \_ 4 \_ 0.
- Direct3D 10,1 a introduit Effect-Framework Profile FX \_ 4 \_ 1.
- Direct3D 11 a introduit Effect-Framework Profile FX \_ 5 \_ 0.

> [!Note]  
> Ces profils d’effets hérités sont déconseillés.

 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Référence pour le langage HLSL](dx-graphics-hlsl-reference.md)
</dt> </dl>

 

 





