---
title: Nuanceur HLSL modèle 5
description: Nuanceur HLSL modèle 5
ms.assetid: 072c1ff2-ca1b-427c-9969-aa24ebb4ee38
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: b33b0e2f009b796eb0b8828cc195fb9543ba2b9b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103842429"
---
# <a name="hlsl-shader-model-5"></a>Nuanceur HLSL modèle 5

Cette section contient des informations générales sur le langage du nuanceur High-Level, notamment sur les nouvelles fonctionnalités du nuanceur modèle 5 introduites dans Microsoft Direct3D 11.

## <a name="in-this-section"></a>Dans cette section



| Élément                                                                                                                                                                                                               | Description                                                                                                                                                                                                                                                                                                                                                            |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Dynamic_Linking"></span><span id="dynamic_linking"></span><span id="DYNAMIC_LINKING"></span>[Liaison dynamique](overviews-direct3d-11-hlsl-dynamic-linking.md)<br/>                                 | La liaison dynamique permet à l’exécution de prendre une décision au moment du traçage (plutôt que au moment de la compilation) sur le chemin d’accès du code à exécuter. Cela réduit le problème de prolifération de nuanceur causé par les nuanceurs avec des signatures d’entrée quasiment identiques.<br/>                                                                                                                         |
| <span id="Geometry_Shader_Features"></span><span id="geometry_shader_features"></span><span id="GEOMETRY_SHADER_FEATURES"></span>[Fonctionnalités du nuanceur Geometry](overviews-direct3d-11-hlsl-gs-features.md)<br/> | Nouvelles fonctionnalités de nuanceur Geometry, notamment : instanciation, qui offre une amélioration des performances lorsque l’ordre des primitives dans le flux n’a pas d’importance, et des flux de sortie à plusieurs points pour qu’un nuanceur puisse produire des vertex sur plusieurs flux.<br/>                                                                                                                |
| <span id="Tessellation"></span><span id="tessellation"></span><span id="TESSELLATION"></span>[Mosaïque](/windows/desktop/direct3d11/direct3d-11-advanced-stages-tessellation)<br/>                                        | Le runtime Direct3D 11 prend en charge trois nouvelles étapes qui implémentent la polygonalisation, qui convertit les surfaces de sous-division de faible détail en primitives de détail supérieures sur le GPU. Polygonalisation des vignettes (ou fractionnement) des surfaces de poids fort dans des structures appropriées pour le rendu. Les trois étapes de pavage sont les étapes de nuanceur-nuanceur, du paveur et nuanceur de domaine.<br/> |



 

En outre, la section de référence traite de nombreux nouveaux éléments d’API pour le nuanceur 5, y compris : [attributs](d3d11-graphics-reference-sm5-attributes.md), [fonctions intrinsèques](d3d11-graphics-reference-sm5-intrinsics.md), [objets et méthodes de nuanceur 5](d3d11-graphics-reference-sm5-objects.md)et [valeurs système](d3d11-graphics-reference-sm5-system-values.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Guide de programmation pour HLSL](dx-graphics-hlsl-pguide.md)
</dt> </dl>

 

