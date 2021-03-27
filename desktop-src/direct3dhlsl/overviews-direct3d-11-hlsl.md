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
# <a name="hlsl-shader-model-5"></a><span data-ttu-id="aaef7-103">Nuanceur HLSL modèle 5</span><span class="sxs-lookup"><span data-stu-id="aaef7-103">HLSL Shader Model 5</span></span>

<span data-ttu-id="aaef7-104">Cette section contient des informations générales sur le langage du nuanceur High-Level, notamment sur les nouvelles fonctionnalités du nuanceur modèle 5 introduites dans Microsoft Direct3D 11.</span><span class="sxs-lookup"><span data-stu-id="aaef7-104">This section contains overview material for the High-Level Shader Language, specifically the new features in shader model 5 introduced in Microsoft Direct3D 11.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="aaef7-105">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="aaef7-105">In This Section</span></span>



| <span data-ttu-id="aaef7-106">Élément</span><span class="sxs-lookup"><span data-stu-id="aaef7-106">Item</span></span>                                                                                                                                                                                                               | <span data-ttu-id="aaef7-107">Description</span><span class="sxs-lookup"><span data-stu-id="aaef7-107">Description</span></span>                                                                                                                                                                                                                                                                                                                                                            |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="aaef7-108"><span id="Dynamic_Linking"></span><span id="dynamic_linking"></span><span id="DYNAMIC_LINKING"></span>[Liaison dynamique](overviews-direct3d-11-hlsl-dynamic-linking.md)</span><span class="sxs-lookup"><span data-stu-id="aaef7-108"><span id="Dynamic_Linking"></span><span id="dynamic_linking"></span><span id="DYNAMIC_LINKING"></span>[Dynamic Linking](overviews-direct3d-11-hlsl-dynamic-linking.md)</span></span><br/>                                 | <span data-ttu-id="aaef7-109">La liaison dynamique permet à l’exécution de prendre une décision au moment du traçage (plutôt que au moment de la compilation) sur le chemin d’accès du code à exécuter.</span><span class="sxs-lookup"><span data-stu-id="aaef7-109">Dynamic linking allows the runtime to make a decision at draw-time (rather than compile-time) about which code path to run.</span></span> <span data-ttu-id="aaef7-110">Cela réduit le problème de prolifération de nuanceur causé par les nuanceurs avec des signatures d’entrée quasiment identiques.</span><span class="sxs-lookup"><span data-stu-id="aaef7-110">This reduces the shader proliferation problem caused by shaders with nearly identical input signatures.</span></span><br/>                                                                                                                         |
| <span data-ttu-id="aaef7-111"><span id="Geometry_Shader_Features"></span><span id="geometry_shader_features"></span><span id="GEOMETRY_SHADER_FEATURES"></span>[Fonctionnalités du nuanceur Geometry](overviews-direct3d-11-hlsl-gs-features.md)</span><span class="sxs-lookup"><span data-stu-id="aaef7-111"><span id="Geometry_Shader_Features"></span><span id="geometry_shader_features"></span><span id="GEOMETRY_SHADER_FEATURES"></span>[Geometry Shader Features](overviews-direct3d-11-hlsl-gs-features.md)</span></span><br/> | <span data-ttu-id="aaef7-112">Nouvelles fonctionnalités de nuanceur Geometry, notamment : instanciation, qui offre une amélioration des performances lorsque l’ordre des primitives dans le flux n’a pas d’importance, et des flux de sortie à plusieurs points pour qu’un nuanceur puisse produire des vertex sur plusieurs flux.</span><span class="sxs-lookup"><span data-stu-id="aaef7-112">New geometry shader features including: instancing, which provides a performance boost when the order of primitives in the stream doesn't matter, and multiple point output streams so a shader can output vertices on more than one stream.</span></span><br/>                                                                                                                |
| <span data-ttu-id="aaef7-113"><span id="Tessellation"></span><span id="tessellation"></span><span id="TESSELLATION"></span>[Mosaïque](/windows/desktop/direct3d11/direct3d-11-advanced-stages-tessellation)</span><span class="sxs-lookup"><span data-stu-id="aaef7-113"><span id="Tessellation"></span><span id="tessellation"></span><span id="TESSELLATION"></span>[Tessellation](/windows/desktop/direct3d11/direct3d-11-advanced-stages-tessellation)</span></span><br/>                                        | <span data-ttu-id="aaef7-114">Le runtime Direct3D 11 prend en charge trois nouvelles étapes qui implémentent la polygonalisation, qui convertit les surfaces de sous-division de faible détail en primitives de détail supérieures sur le GPU.</span><span class="sxs-lookup"><span data-stu-id="aaef7-114">The Direct3D 11 runtime supports three new stages that implement tessellation, which converts low-detail subdivision surfaces into higher-detail primitives on the GPU.</span></span> <span data-ttu-id="aaef7-115">Polygonalisation des vignettes (ou fractionnement) des surfaces de poids fort dans des structures appropriées pour le rendu.</span><span class="sxs-lookup"><span data-stu-id="aaef7-115">Tessellation tiles (or breaks up) high-order surfaces into suitable structures for rendering.</span></span> <span data-ttu-id="aaef7-116">Les trois étapes de pavage sont les étapes de nuanceur-nuanceur, du paveur et nuanceur de domaine.</span><span class="sxs-lookup"><span data-stu-id="aaef7-116">The three tessellation stages are hull-shader, tessellator, and domain-shader stages.</span></span><br/> |



 

<span data-ttu-id="aaef7-117">En outre, la section de référence traite de nombreux nouveaux éléments d’API pour le nuanceur 5, y compris : [attributs](d3d11-graphics-reference-sm5-attributes.md), [fonctions intrinsèques](d3d11-graphics-reference-sm5-intrinsics.md), [objets et méthodes de nuanceur 5](d3d11-graphics-reference-sm5-objects.md)et [valeurs système](d3d11-graphics-reference-sm5-system-values.md).</span><span class="sxs-lookup"><span data-stu-id="aaef7-117">In addition, the reference section covers many new API elements for shader model 5 including: [attributes](d3d11-graphics-reference-sm5-attributes.md), [intrinsic functions](d3d11-graphics-reference-sm5-intrinsics.md), [shader model 5 objects and methods](d3d11-graphics-reference-sm5-objects.md), and [system values](d3d11-graphics-reference-sm5-system-values.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="aaef7-118">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="aaef7-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="aaef7-119">Guide de programmation pour HLSL</span><span class="sxs-lookup"><span data-stu-id="aaef7-119">Programming Guide for HLSL</span></span>](dx-graphics-hlsl-pguide.md)
</dt> </dl>

 

