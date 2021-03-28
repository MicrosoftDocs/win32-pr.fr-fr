---
title: Shader, modèle 5
description: Cette section contient les pages de référence pour HLSL Shader Model 5.
ms.assetid: ec646940-8901-45c5-a44c-434c8acae2aa
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: f379301008190367a40959a319d01cfad127f6b4
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104382152"
---
# <a name="shader-model-5"></a>Shader, modèle 5

Cette section contient les pages de référence pour HLSL Shader Model 5.

Le Shader Model 5 est un sur-ensemble des capacités du [nuanceur modèle 4](dx-graphics-hlsl-sm4.md). Il a été conçu à l’aide d’un noyau-nuanceur commun qui fournit un ensemble commun de fonctionnalités à tous les nuanceurs programmables, qui sont uniquement programmables à l’aide du langage HLSL.



| Fonctionnalité                   | Utilité                                                                                                                                             |
|---------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| Jeu d'instructions           | [**Fonctions intrinsèques HLSL**](dx-graphics-hlsl-intrinsic-functions.md)                                                                               |
| Vertex shader Max         | Pas de restriction                                                                                                                                         |
| Nuanceur de pixels max.          | Pas de restriction                                                                                                                                         |
| Nouveaux profils de nuanceur ajoutés | CS \_ 4 \_ 0, GS \_ 4 \_ 0 \* , PS \_ 4 \_ 0 \* , vs \_ 4 \_ 0 \* , CS \_ 4 \_ 1, GS \_ 4 \_ 1 \* , PS \_ 4 \_ 1 \* , vs \_ 4 \_ 1 \* , CS \_ 5 0 \_ , DS \_ 5 \_ 0, GS \_ 5 \_ 0, HS \_ 5 \_ 0, PS \_ 5 0 \_ , vs \_ 5 \_ 0 |



 

\* -GS \_ 4 \_ 0, GS \_ 4 \_ 1, PS \_ 4 \_ 0, PS \_ 4 \_ 1, vs \_ 4 \_ 0 et vs \_ 4 \_ 1 ont été introduits dans le modèle de nuanceur 4,0. Toutefois, DirectX 11 ajoute la prise en charge des [mémoires tampons structurées](/windows/desktop/direct3d11/direct3d-11-advanced-stages-cs-resources) et des mémoires tampons d’adresses d’octets au nuanceur de modèle 4 s’exécutant sur le matériel DirectX 10.

Le Shader Model 5 présente le [nuanceur de calcul](/windows/desktop/direct3d11/direct3d-11-advanced-stages-compute-shader) qui fournit un calcul universel à grande vitesse.

Une liste plus complète des fonctionnalités du nuanceur 5 est incluse dans la liste des [fonctionnalités de Direct3D 11](/windows/desktop/direct3d11/direct3d-11-features).

La section de l' [assembly Shader Model 5](shader-model-5-assembly--directx-hlsl-.md) décrit les instructions d’assembly prises en charge par le modèle de nuanceur 5.

## <a name="in-this-section"></a>Dans cette section



| Élément                                                                                                                                                                                                                                                        | Description                                                        |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <span id="Shader_Model_5_Attributes"></span><span id="shader_model_5_attributes"></span><span id="SHADER_MODEL_5_ATTRIBUTES"></span>[Attributs du modèle de nuanceur 5](d3d11-graphics-reference-sm5-attributes.md)<br/>                                     | Pages de référence pour les attributs du Shader Model 5.<br/>          |
| <span id="Shader_Model_5_Intrinsic_Functions"></span><span id="shader_model_5_intrinsic_functions"></span><span id="SHADER_MODEL_5_INTRINSIC_FUNCTIONS"></span>[Fonctions intrinsèques du modèle de nuanceur 5](d3d11-graphics-reference-sm5-intrinsics.md)<br/> | Pages de référence pour les fonctions intrinsèques du nuancier Model 5.<br/> |
| <span id="Shader_Model_5_Objects"></span><span id="shader_model_5_objects"></span><span id="SHADER_MODEL_5_OBJECTS"></span>[Objets Shader Model 5](d3d11-graphics-reference-sm5-objects.md)<br/>                                                    | Pages de référence pour les objets et méthodes de nuanceur de modèle 5.<br/> |
| <span id="Shader_Model_5_System_Values"></span><span id="shader_model_5_system_values"></span><span id="SHADER_MODEL_5_SYSTEM_VALUES"></span>[Valeurs système du Shader Model 5](d3d11-graphics-reference-sm5-system-values.md)<br/>                      | Pages de référence pour les valeurs système du Shader Model 5.<br/>       |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Modèles de nuanceur et profils Shader](dx-graphics-hlsl-models.md)
</dt> </dl>

 

