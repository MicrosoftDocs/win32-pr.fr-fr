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
# <a name="shader-model-5"></a><span data-ttu-id="7c517-103">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="7c517-103">Shader Model 5</span></span>

<span data-ttu-id="7c517-104">Cette section contient les pages de référence pour HLSL Shader Model 5.</span><span class="sxs-lookup"><span data-stu-id="7c517-104">This section contains the reference pages for HLSL Shader Model 5.</span></span>

<span data-ttu-id="7c517-105">Le Shader Model 5 est un sur-ensemble des capacités du [nuanceur modèle 4](dx-graphics-hlsl-sm4.md).</span><span class="sxs-lookup"><span data-stu-id="7c517-105">Shader Model 5 is a superset of the capabilites in [Shader Model 4](dx-graphics-hlsl-sm4.md).</span></span> <span data-ttu-id="7c517-106">Il a été conçu à l’aide d’un noyau-nuanceur commun qui fournit un ensemble commun de fonctionnalités à tous les nuanceurs programmables, qui sont uniquement programmables à l’aide du langage HLSL.</span><span class="sxs-lookup"><span data-stu-id="7c517-106">It has been designed using a common-shader core which provides a common set of features to all programmable shaders, which are only programmable using HLSL.</span></span>



| <span data-ttu-id="7c517-107">Fonctionnalité</span><span class="sxs-lookup"><span data-stu-id="7c517-107">Feature</span></span>                   | <span data-ttu-id="7c517-108">Utilité</span><span class="sxs-lookup"><span data-stu-id="7c517-108">Capability</span></span>                                                                                                                                             |
|---------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7c517-109">Jeu d'instructions</span><span class="sxs-lookup"><span data-stu-id="7c517-109">Instruction Set</span></span>           | [<span data-ttu-id="7c517-110">**Fonctions intrinsèques HLSL**</span><span class="sxs-lookup"><span data-stu-id="7c517-110">**HLSL intrinsic functions**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                                               |
| <span data-ttu-id="7c517-111">Vertex shader Max</span><span class="sxs-lookup"><span data-stu-id="7c517-111">Vertex Shader Max</span></span>         | <span data-ttu-id="7c517-112">Pas de restriction</span><span class="sxs-lookup"><span data-stu-id="7c517-112">No restriction</span></span>                                                                                                                                         |
| <span data-ttu-id="7c517-113">Nuanceur de pixels max.</span><span class="sxs-lookup"><span data-stu-id="7c517-113">Pixel Shader Max</span></span>          | <span data-ttu-id="7c517-114">Pas de restriction</span><span class="sxs-lookup"><span data-stu-id="7c517-114">No restriction</span></span>                                                                                                                                         |
| <span data-ttu-id="7c517-115">Nouveaux profils de nuanceur ajoutés</span><span class="sxs-lookup"><span data-stu-id="7c517-115">New Shader Profiles Added</span></span> | <span data-ttu-id="7c517-116">CS \_ 4 \_ 0, GS \_ 4 \_ 0 \* , PS \_ 4 \_ 0 \* , vs \_ 4 \_ 0 \* , CS \_ 4 \_ 1, GS \_ 4 \_ 1 \* , PS \_ 4 \_ 1 \* , vs \_ 4 \_ 1 \* , CS \_ 5 0 \_ , DS \_ 5 \_ 0, GS \_ 5 \_ 0, HS \_ 5 \_ 0, PS \_ 5 0 \_ , vs \_ 5 \_ 0</span><span class="sxs-lookup"><span data-stu-id="7c517-116">cs\_4\_0, gs\_4\_0\*, ps\_4\_0\*, vs\_4\_0\*, cs\_4\_1, gs\_4\_1\*, ps\_4\_1\*, vs\_4\_1\*, cs\_5\_0, ds\_5\_0, gs\_5\_0, hs\_5\_0, ps\_5\_0, vs\_5\_0</span></span> |



 

<span data-ttu-id="7c517-117">\* -GS \_ 4 \_ 0, GS \_ 4 \_ 1, PS \_ 4 \_ 0, PS \_ 4 \_ 1, vs \_ 4 \_ 0 et vs \_ 4 \_ 1 ont été introduits dans le modèle de nuanceur 4,0. Toutefois, DirectX 11 ajoute la prise en charge des [mémoires tampons structurées](/windows/desktop/direct3d11/direct3d-11-advanced-stages-cs-resources) et des mémoires tampons d’adresses d’octets au nuanceur de modèle 4 s’exécutant sur le matériel DirectX 10.</span><span class="sxs-lookup"><span data-stu-id="7c517-117">\* - gs\_4\_0, gs\_4\_1, ps\_4\_0, ps\_4\_1, vs\_4\_0 and vs\_4\_1 were introduced in Shader Model 4.0, however, DirectX 11 adds support for [structured buffers](/windows/desktop/direct3d11/direct3d-11-advanced-stages-cs-resources) and byte address buffers to Shader Model 4 running on DirectX 10 hardware.</span></span>

<span data-ttu-id="7c517-118">Le Shader Model 5 présente le [nuanceur de calcul](/windows/desktop/direct3d11/direct3d-11-advanced-stages-compute-shader) qui fournit un calcul universel à grande vitesse.</span><span class="sxs-lookup"><span data-stu-id="7c517-118">Shader Model 5 introduces the [compute shader](/windows/desktop/direct3d11/direct3d-11-advanced-stages-compute-shader) which provides high-speed general purpose computing.</span></span>

<span data-ttu-id="7c517-119">Une liste plus complète des fonctionnalités du nuanceur 5 est incluse dans la liste des [fonctionnalités de Direct3D 11](/windows/desktop/direct3d11/direct3d-11-features).</span><span class="sxs-lookup"><span data-stu-id="7c517-119">A more complete listing of Shader Model 5 features is included in a listing of the [Direct3D 11 features](/windows/desktop/direct3d11/direct3d-11-features).</span></span>

<span data-ttu-id="7c517-120">La section de l' [assembly Shader Model 5](shader-model-5-assembly--directx-hlsl-.md) décrit les instructions d’assembly prises en charge par le modèle de nuanceur 5.</span><span class="sxs-lookup"><span data-stu-id="7c517-120">The [Shader Model 5 Assembly](shader-model-5-assembly--directx-hlsl-.md) section describes the assembly instructions that the Shader Model 5 supports.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="7c517-121">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="7c517-121">In This Section</span></span>



| <span data-ttu-id="7c517-122">Élément</span><span class="sxs-lookup"><span data-stu-id="7c517-122">Item</span></span>                                                                                                                                                                                                                                                        | <span data-ttu-id="7c517-123">Description</span><span class="sxs-lookup"><span data-stu-id="7c517-123">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="7c517-124"><span id="Shader_Model_5_Attributes"></span><span id="shader_model_5_attributes"></span><span id="SHADER_MODEL_5_ATTRIBUTES"></span>[Attributs du modèle de nuanceur 5](d3d11-graphics-reference-sm5-attributes.md)</span><span class="sxs-lookup"><span data-stu-id="7c517-124"><span id="Shader_Model_5_Attributes"></span><span id="shader_model_5_attributes"></span><span id="SHADER_MODEL_5_ATTRIBUTES"></span>[Shader Model 5 Attributes](d3d11-graphics-reference-sm5-attributes.md)</span></span><br/>                                     | <span data-ttu-id="7c517-125">Pages de référence pour les attributs du Shader Model 5.</span><span class="sxs-lookup"><span data-stu-id="7c517-125">Reference pages for Shader Model 5 attributes.</span></span><br/>          |
| <span data-ttu-id="7c517-126"><span id="Shader_Model_5_Intrinsic_Functions"></span><span id="shader_model_5_intrinsic_functions"></span><span id="SHADER_MODEL_5_INTRINSIC_FUNCTIONS"></span>[Fonctions intrinsèques du modèle de nuanceur 5](d3d11-graphics-reference-sm5-intrinsics.md)</span><span class="sxs-lookup"><span data-stu-id="7c517-126"><span id="Shader_Model_5_Intrinsic_Functions"></span><span id="shader_model_5_intrinsic_functions"></span><span id="SHADER_MODEL_5_INTRINSIC_FUNCTIONS"></span>[Shader Model 5 Intrinsic Functions](d3d11-graphics-reference-sm5-intrinsics.md)</span></span><br/> | <span data-ttu-id="7c517-127">Pages de référence pour les fonctions intrinsèques du nuancier Model 5.</span><span class="sxs-lookup"><span data-stu-id="7c517-127">Reference pages for Shader Model 5 intrinsic functions.</span></span><br/> |
| <span data-ttu-id="7c517-128"><span id="Shader_Model_5_Objects"></span><span id="shader_model_5_objects"></span><span id="SHADER_MODEL_5_OBJECTS"></span>[Objets Shader Model 5](d3d11-graphics-reference-sm5-objects.md)</span><span class="sxs-lookup"><span data-stu-id="7c517-128"><span id="Shader_Model_5_Objects"></span><span id="shader_model_5_objects"></span><span id="SHADER_MODEL_5_OBJECTS"></span>[Shader Model 5 Objects](d3d11-graphics-reference-sm5-objects.md)</span></span><br/>                                                    | <span data-ttu-id="7c517-129">Pages de référence pour les objets et méthodes de nuanceur de modèle 5.</span><span class="sxs-lookup"><span data-stu-id="7c517-129">Reference pages for Shader Model 5 objects and methods.</span></span><br/> |
| <span data-ttu-id="7c517-130"><span id="Shader_Model_5_System_Values"></span><span id="shader_model_5_system_values"></span><span id="SHADER_MODEL_5_SYSTEM_VALUES"></span>[Valeurs système du Shader Model 5](d3d11-graphics-reference-sm5-system-values.md)</span><span class="sxs-lookup"><span data-stu-id="7c517-130"><span id="Shader_Model_5_System_Values"></span><span id="shader_model_5_system_values"></span><span id="SHADER_MODEL_5_SYSTEM_VALUES"></span>[Shader Model 5 System Values](d3d11-graphics-reference-sm5-system-values.md)</span></span><br/>                      | <span data-ttu-id="7c517-131">Pages de référence pour les valeurs système du Shader Model 5.</span><span class="sxs-lookup"><span data-stu-id="7c517-131">Reference pages for Shader Model 5 system values.</span></span><br/>       |



 

## <a name="related-topics"></a><span data-ttu-id="7c517-132">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="7c517-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7c517-133">Modèles de nuanceur et profils Shader</span><span class="sxs-lookup"><span data-stu-id="7c517-133">Shader Models vs Shader Profiles</span></span>](dx-graphics-hlsl-models.md)
</dt> </dl>

 

