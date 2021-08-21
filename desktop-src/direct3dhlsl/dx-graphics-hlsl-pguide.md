---
title: Guide de programmation pour le HLSL
description: Les données entrent dans le pipeline graphique en tant que flux de primitives et sont traitées par les étapes du nuanceur.
ms.assetid: 4894e085-30e7-4cc5-8ae6-a84b601e4ce3
ms.topic: article
ms.date: 02/21/2019
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: ca0b1f93b3c5f56cd7a074571ec6657cedc924688606e3612a66ef0f9e40d51e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117726068"
---
# <a name="programming-guide-for-hlsl"></a>Guide de programmation pour le HLSL

Les données entrent dans le pipeline graphique en tant que flux de primitives et sont traitées par les étapes du nuanceur. Les étapes de nuanceur réelles dépendent de la version de Direct3D, mais incluent certainement les étapes vertex, pixel et Geometry. D’autres étapes incluent les nuanceurs de la coque et du domaine pour le pavage et le nuanceur de calcul. Ces étapes sont entièrement programmables à l’aide du langage[HLSL](dx-graphics-hlsl-reference.md)(High Level Shading Language).

Les nuanceurs HLSL peuvent être compilés au moment de la création ou au moment de l’exécution et définis au moment de l’exécution dans l’étape de pipeline appropriée. Les nuanceurs Direct3D 9 peuvent être conçus à l’aide du [nuanceur modèle 1](dx-graphics-hlsl-sm1.md), du [nuanceur modèle 2](dx-graphics-hlsl-sm2.md) et du [nuancier modèle 3](dx-graphics-hlsl-sm3.md); Les nuanceurs Direct3D 10 peuvent uniquement être conçus sur le [modèle de nuanceur 4](dx-graphics-hlsl-sm4.md). Les nuanceurs Direct3D 11 peuvent être conçus sur le [nuancier Model 5](d3d11-graphics-reference-sm5.md). Direct3D 11,3 et Direct3D 12 peuvent être conçus sur le [modèle de nuanceur 5,1](shader-model-5-1.md), et Direct3D 12 peut également être conçu sur le [modèle de nuanceur 6](shader-model-6-0.md).

## <a name="in-this-section"></a>Contenu de cette section

| Rubrique | Description |
|-|-|
| [Utilisation de la liaison de nuanceur](using-shader-linking.md) | Nous montrons comment créer des fonctions HLSL précompilées, les empaqueter dans des bibliothèques et les lier à des nuanceurs complets au moment de l’exécution. |
| [Écriture de nuanceurs HLSL dans Direct3D 9](dx-graphics-hlsl-writing-shaders-9.md) | |
| [Utilisation de nuanceurs dans Direct3D 9](dx-graphics-hlsl-using-shaders-9.md) | |
| [Utilisation des nuanceurs dans Direct3D 10](dx-graphics-hlsl-using-shaders-10.md) | |
| [Optimisation des nuanceurs HLSL](dx-graphics-hlsl-optimize.md) | |
| [Débogage des nuanceurs dans Visual Studio](dx-graphics-hlsl-debug-visual-studio.md) | le dernier outil de débogage des nuanceurs est désormais fourni sous la forme d’une fonctionnalité de Microsoft Visual Studio, appelée Visual Studio débogueur graphics.  |
| [Compilation des nuanceurs](dx-graphics-hlsl-part1.md) | Examinons à présent les différentes façons de compiler le code et les conventions de votre nuanceur pour les extensions de fichier pour le code du nuanceur. |
| [Spécification de cibles de compilateur](specifying-compiler-targets.md) | Ici, nous répertorions les cibles pour les différents profils que les fonctions **D3DCompile \*** et le compilateur HLSL prennent en charge. |
| [Décompresser et compresser le \_ format DXGI pour la modification des images In-Place](dx-graphics-hlsl-unpacking-packing-dxgi-format.md) | |
| [Utilisation de la précision minimale HLSL](using-hlsl-minimum-precision.md) | à partir de Windows 8, les pilotes graphiques peuvent implémenter des [types de données scalaires HLSL](dx-graphics-hlsl-scalar.md) de précision minimale à l’aide d’une précision supérieure ou égale à la précision de bit spécifiée.  |
| [Nuanceur HLSL modèle 5](overviews-direct3d-11-hlsl.md) | |
| [Modèle de nuanceur HLSL 5,1](hlsl-shader-model-5-1-features-for-direct3d-12.md) | Cette section décrit les fonctionnalités du modèle de nuanceur 5,1 telles qu’elles s’appliquent dans la pratique à D3D12 et à D3D 11.3. Tout le matériel DirectX 12 prend en charge le modèle de nuanceur 5,1. |
| [Modèle de nuanceur HLSL 6.0](hlsl-shader-model-6-0-features-for-direct3d-12.md) | Décrit les fonctions intrinsèques de l’opération Wave ajoutées au modèle de nuanceur HLSL 6,0. |
| [Modèle de nuanceur HLSL 6,4](hlsl-shader-model-6-4-features-for-direct3d-12.md) | Décrit les Machine Learning intrinsèques ajoutés au modèle de nuanceur HLSL 6,4. |

## <a name="related-topics"></a>Rubriques connexes

* [HLSL](dx-graphics-hlsl.md)
* [Référence pour le langage HLSL](dx-graphics-hlsl-reference.md)
