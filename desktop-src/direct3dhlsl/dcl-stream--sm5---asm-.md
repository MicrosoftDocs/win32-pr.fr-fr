---
title: dcl_stream (SM5-ASM)
description: Déclare un flux de sortie de nuanceur Geometry.
ms.assetid: 0A8B8AB5-B7B0-46BB-91E8-B2E8E3D64B74
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5f46903c3257c280788e91c25700743a23c146fe
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104381228"
---
# <a name="dcl_stream-sm5---asm"></a><span data-ttu-id="a4d7a-103">\_flux DCL (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="a4d7a-103">dcl\_stream (sm5 - asm)</span></span>

<span data-ttu-id="a4d7a-104">Déclare un flux de sortie de nuanceur Geometry.</span><span class="sxs-lookup"><span data-stu-id="a4d7a-104">Declare a geometry shader output stream.</span></span>



| <span data-ttu-id="a4d7a-105">\_flux DCL m\#</span><span class="sxs-lookup"><span data-stu-id="a4d7a-105">dcl\_stream m\#</span></span> |
|-----------------|



 



| <span data-ttu-id="a4d7a-106">Élément</span><span class="sxs-lookup"><span data-stu-id="a4d7a-106">Item</span></span>                                                       | <span data-ttu-id="a4d7a-107">Description</span><span class="sxs-lookup"><span data-stu-id="a4d7a-107">Description</span></span>                             |
|------------------------------------------------------------|-----------------------------------------|
| <span data-ttu-id="a4d7a-108"><span id="m_"></span><span id="M_"></span>*lecteur\#*</span><span class="sxs-lookup"><span data-stu-id="a4d7a-108"><span id="m_"></span><span id="M_"></span>*m\#*</span></span><br/> | <span data-ttu-id="a4d7a-109">\[dans le \] flux 0.. 3 (M0.. m3).</span><span class="sxs-lookup"><span data-stu-id="a4d7a-109">\[in\] Stream 0..3 (m0..m3).</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="a4d7a-110">Notes</span><span class="sxs-lookup"><span data-stu-id="a4d7a-110">Remarks</span></span>

<span data-ttu-id="a4d7a-111">Un flux donné ne peut être déclaré qu’une seule fois.</span><span class="sxs-lookup"><span data-stu-id="a4d7a-111">A given stream can only be declared once.</span></span>

<span data-ttu-id="a4d7a-112">Si aucun flux n’est déclaré, les déclarations de topologie de sortie et de sortie sont supposées être pour le flux 0.</span><span class="sxs-lookup"><span data-stu-id="a4d7a-112">If no streams are declared, output and output topology declarations are assumed to be for stream 0.</span></span>

<span data-ttu-id="a4d7a-113">Le premier **\_ flux DCL** ne peut pas apparaître après des instructions de **\_ sortie DCL** ou **DCL \_ outputTopology** .</span><span class="sxs-lookup"><span data-stu-id="a4d7a-113">The first **dcl\_stream** cannot appear after any **dcl\_output** or **dcl\_outputTopology** statements.</span></span>

<span data-ttu-id="a4d7a-114">Les instructions de **\_ sortie DCL** ou **DCL \_ outputToplogy** après toute instruction du **\_ flux DCL** m \# définissent les sorties du flux m \# .</span><span class="sxs-lookup"><span data-stu-id="a4d7a-114">Any **dcl\_output** or **dcl\_outputToplogy** statements after any **dcl\_stream** m\# statement define the outputs for stream m\#.</span></span>

<span data-ttu-id="a4d7a-115">Cette instruction s’applique aux étapes suivantes du nuanceur :</span><span class="sxs-lookup"><span data-stu-id="a4d7a-115">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="a4d7a-116">Sommet</span><span class="sxs-lookup"><span data-stu-id="a4d7a-116">Vertex</span></span> | <span data-ttu-id="a4d7a-117">Forme</span><span class="sxs-lookup"><span data-stu-id="a4d7a-117">Hull</span></span> | <span data-ttu-id="a4d7a-118">Domain</span><span class="sxs-lookup"><span data-stu-id="a4d7a-118">Domain</span></span> | <span data-ttu-id="a4d7a-119">Géométrie</span><span class="sxs-lookup"><span data-stu-id="a4d7a-119">Geometry</span></span> | <span data-ttu-id="a4d7a-120">Pixel</span><span class="sxs-lookup"><span data-stu-id="a4d7a-120">Pixel</span></span> | <span data-ttu-id="a4d7a-121">Compute</span><span class="sxs-lookup"><span data-stu-id="a4d7a-121">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        | <span data-ttu-id="a4d7a-122">X</span><span class="sxs-lookup"><span data-stu-id="a4d7a-122">X</span></span>        |       |         |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="a4d7a-123">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="a4d7a-123">Minimum Shader Model</span></span>

<span data-ttu-id="a4d7a-124">Cette instruction est prise en charge dans les modèles de nuanceur suivants :</span><span class="sxs-lookup"><span data-stu-id="a4d7a-124">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="a4d7a-125">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="a4d7a-125">Shader Model</span></span>                                              | <span data-ttu-id="a4d7a-126">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="a4d7a-126">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="a4d7a-127">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="a4d7a-127">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="a4d7a-128">Oui</span><span class="sxs-lookup"><span data-stu-id="a4d7a-128">yes</span></span>       |
| [<span data-ttu-id="a4d7a-129">Modèle de nuanceur 4,1</span><span class="sxs-lookup"><span data-stu-id="a4d7a-129">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="a4d7a-130">non</span><span class="sxs-lookup"><span data-stu-id="a4d7a-130">no</span></span>        |
| [<span data-ttu-id="a4d7a-131">Nuanceur modèle 4</span><span class="sxs-lookup"><span data-stu-id="a4d7a-131">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="a4d7a-132">non</span><span class="sxs-lookup"><span data-stu-id="a4d7a-132">no</span></span>        |
| [<span data-ttu-id="a4d7a-133">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="a4d7a-133">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="a4d7a-134">non</span><span class="sxs-lookup"><span data-stu-id="a4d7a-134">no</span></span>        |
| [<span data-ttu-id="a4d7a-135">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="a4d7a-135">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="a4d7a-136">non</span><span class="sxs-lookup"><span data-stu-id="a4d7a-136">no</span></span>        |
| [<span data-ttu-id="a4d7a-137">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="a4d7a-137">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="a4d7a-138">non</span><span class="sxs-lookup"><span data-stu-id="a4d7a-138">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="a4d7a-139">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="a4d7a-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a4d7a-140">Assembly modèle 5 du nuanceur (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="a4d7a-140">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





