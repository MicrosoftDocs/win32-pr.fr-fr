---
title: Modèle de nuanceur 5,1
description: Cette section contient les pages de référence pour le modèle de nuanceur HLSL 5,1, introduites avec D3D12.
ms.assetid: 814FAC95-7FD5-450F-964B-18E687DBCC56
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d5fd2f2a2f4ebe86a090ebade8ebf8a033a7c612
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104990748"
---
# <a name="shader-model-51"></a><span data-ttu-id="0ebfc-103">Modèle de nuanceur 5,1</span><span class="sxs-lookup"><span data-stu-id="0ebfc-103">Shader Model 5.1</span></span>

<span data-ttu-id="0ebfc-104">Cette section contient les pages de référence pour le modèle de nuanceur HLSL 5,1, introduites avec D3D12.</span><span class="sxs-lookup"><span data-stu-id="0ebfc-104">This section contains the reference pages for HLSL Shader Model 5.1, introduced with D3D12.</span></span>

<span data-ttu-id="0ebfc-105">Le modèle de nuanceur 5,1 est fonctionnellement très similaire au [nuanceur 5](d3d11-graphics-reference-sm5.md), la principale modification est plus flexible dans la sélection des ressources en autorisant l’indexation de tableaux de descripteurs à partir d’un nuanceur.</span><span class="sxs-lookup"><span data-stu-id="0ebfc-105">Shader Model 5.1 is functionally very similar to [Shader Model 5](d3d11-graphics-reference-sm5.md), the main change is more flexibility in resource selection by allowing indexing of arrays of descriptors from within a shader.</span></span>



| <span data-ttu-id="0ebfc-106">Fonctionnalité</span><span class="sxs-lookup"><span data-stu-id="0ebfc-106">Feature</span></span>                   | <span data-ttu-id="0ebfc-107">Utilité</span><span class="sxs-lookup"><span data-stu-id="0ebfc-107">Capability</span></span>                                                                |
|---------------------------|---------------------------------------------------------------------------|
| <span data-ttu-id="0ebfc-108">Jeu d'instructions</span><span class="sxs-lookup"><span data-stu-id="0ebfc-108">Instruction Set</span></span>           | [<span data-ttu-id="0ebfc-109">**Fonctions intrinsèques HLSL**</span><span class="sxs-lookup"><span data-stu-id="0ebfc-109">**HLSL intrinsic functions**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)  |
| <span data-ttu-id="0ebfc-110">Vertex shader Max</span><span class="sxs-lookup"><span data-stu-id="0ebfc-110">Vertex Shader Max</span></span>         | <span data-ttu-id="0ebfc-111">Pas de restriction</span><span class="sxs-lookup"><span data-stu-id="0ebfc-111">No restriction</span></span>                                                            |
| <span data-ttu-id="0ebfc-112">Nuanceur de pixels max.</span><span class="sxs-lookup"><span data-stu-id="0ebfc-112">Pixel Shader Max</span></span>          | <span data-ttu-id="0ebfc-113">Pas de restriction</span><span class="sxs-lookup"><span data-stu-id="0ebfc-113">No restriction</span></span>                                                            |
| <span data-ttu-id="0ebfc-114">Nouveaux profils de nuanceur ajoutés</span><span class="sxs-lookup"><span data-stu-id="0ebfc-114">New Shader Profiles Added</span></span> | <span data-ttu-id="0ebfc-115">CS \_ 5 \_ 1, DS \_ 5 \_ 1, GS \_ 5 \_ 1, HS \_ 5 \_ 1, PS \_ 5 \_ 1, vs \_ 5 \_ 1, rootsig \_ 1 \_ 0</span><span class="sxs-lookup"><span data-stu-id="0ebfc-115">cs\_5\_1, ds\_5\_1, gs\_5\_1, hs\_5\_1, ps\_5\_1, vs\_5\_1, rootsig\_1\_0</span></span> |



 

## <a name="in-this-section"></a><span data-ttu-id="0ebfc-116">Contenu de cette section</span><span class="sxs-lookup"><span data-stu-id="0ebfc-116">In this section</span></span>



| <span data-ttu-id="0ebfc-117">Rubrique</span><span class="sxs-lookup"><span data-stu-id="0ebfc-117">Topic</span></span>                                                                           | <span data-ttu-id="0ebfc-118">Description</span><span class="sxs-lookup"><span data-stu-id="0ebfc-118">Description</span></span>                                                           |
|---------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| [<span data-ttu-id="0ebfc-119">Objets modèle de nuanceur 5,1</span><span class="sxs-lookup"><span data-stu-id="0ebfc-119">Shader Model 5.1 Objects</span></span>](shader-model-5-1-objects.md)<br/>             | <span data-ttu-id="0ebfc-120">Les objets suivants ont été ajoutés au nuanceur modèle 5,1.</span><span class="sxs-lookup"><span data-stu-id="0ebfc-120">The following objects have been added to shader model 5.1.</span></span><br/> |
| [<span data-ttu-id="0ebfc-121">Valeurs système du modèle de nuanceur 5,1</span><span class="sxs-lookup"><span data-stu-id="0ebfc-121">Shader Model 5.1 System Values</span></span>](shader-model-5-1-system-values.md)<br/> | <span data-ttu-id="0ebfc-122">Le modèle de nuanceur 5,1 ajoute les nouvelles valeurs système suivantes.</span><span class="sxs-lookup"><span data-stu-id="0ebfc-122">Shader Model 5.1 adds the following new system values.</span></span><br/>     |



 

## <a name="related-topics"></a><span data-ttu-id="0ebfc-123">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="0ebfc-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0ebfc-124">Modèles de nuanceur et profils Shader</span><span class="sxs-lookup"><span data-stu-id="0ebfc-124">Shader Models vs Shader Profiles</span></span>](dx-graphics-hlsl-models.md)
</dt> <dt>

[<span data-ttu-id="0ebfc-125">Caractéristiques du modèle de nuanceur HLSL 5,1 pour Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="0ebfc-125">HLSL Shader Model 5.1 Features for Direct3D 12</span></span>](hlsl-shader-model-5-1-features-for-direct3d-12.md)
</dt> </dl>

 

 





