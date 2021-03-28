---
title: dcl_input vGSInstanceID (SM5-ASM)
description: Activer l’instanciation de nuanceur Geometry.
ms.assetid: 47B9BAD5-0FFF-4DB7-B34A-7811B8A4F792
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3134a9d372f1fde5457f26235fe9a6a5439c58c1
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104313762"
---
# <a name="dcl_input-vgsinstanceid-sm5---asm"></a><span data-ttu-id="31493-103">\_vGSInstanceID d’entrée DCL (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="31493-103">dcl\_input vGSInstanceID (sm5 - asm)</span></span>

<span data-ttu-id="31493-104">Activer l’instanciation de nuanceur Geometry.</span><span class="sxs-lookup"><span data-stu-id="31493-104">Enable geometry shader instancing.</span></span>



| <span data-ttu-id="31493-105">\_vGSInstanceID d’entrée DCL, instanceCount</span><span class="sxs-lookup"><span data-stu-id="31493-105">dcl\_input vGSInstanceID, instanceCount</span></span> |
|-----------------------------------------|



 



| <span data-ttu-id="31493-106">Élément</span><span class="sxs-lookup"><span data-stu-id="31493-106">Item</span></span>                                                                                                                       | <span data-ttu-id="31493-107">Description</span><span class="sxs-lookup"><span data-stu-id="31493-107">Description</span></span>                           |
|----------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <span data-ttu-id="31493-108"><span id="vGSInstanceID"></span><span id="vgsinstanceid"></span><span id="VGSINSTANCEID"></span>*vGSInstanceID*</span><span class="sxs-lookup"><span data-stu-id="31493-108"><span id="vGSInstanceID"></span><span id="vgsinstanceid"></span><span id="VGSINSTANCEID"></span>*vGSInstanceID*</span></span><br/> | <span data-ttu-id="31493-109">\[dans \] l’ID d’instance.</span><span class="sxs-lookup"><span data-stu-id="31493-109">\[in\] The instance ID.</span></span><br/>    |
| <span data-ttu-id="31493-110"><span id="instanceCount"></span><span id="instancecount"></span><span id="INSTANCECOUNT"></span>*instanceCount*</span><span class="sxs-lookup"><span data-stu-id="31493-110"><span id="instanceCount"></span><span id="instancecount"></span><span id="INSTANCECOUNT"></span>*instanceCount*</span></span><br/> | <span data-ttu-id="31493-111">\[dans \] le nombre d’instances.</span><span class="sxs-lookup"><span data-stu-id="31493-111">\[in\] The instance count.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="31493-112">Notes</span><span class="sxs-lookup"><span data-stu-id="31493-112">Remarks</span></span>

<span data-ttu-id="31493-113">Le paramètre *instanceCount* de la déclaration spécifie le nombre d’instances que le nuanceur Geometry doit exécuter pour chaque primitive d’entrée.</span><span class="sxs-lookup"><span data-stu-id="31493-113">The *instanceCount* parameter of the declaration specifies how many instances the geometry shader should execute for each input primitive.</span></span> <span data-ttu-id="31493-114">La valeur maximale pour *instanceCount* est 32.</span><span class="sxs-lookup"><span data-stu-id="31493-114">The maximum value for *instanceCount* is 32.</span></span>

<span data-ttu-id="31493-115">Le nombre maximal de vertex déclarés pour la sortie, via [**DCL \_ maxOutputVertexCount**](dcl-maxoutputvertexcount.md), s’applique individuellement à chaque instance.</span><span class="sxs-lookup"><span data-stu-id="31493-115">The maximum number of vertices declared for output, via [**dcl\_maxOutputVertexCount**](dcl-maxoutputvertexcount.md), applies individually to each instance.</span></span>

<span data-ttu-id="31493-116">Le nombre d’instances dans cette déclaration, multiplié par le nombre maximal de vertex par instance via la [**\_ maxOutputVertexCount DCL**](dcl-maxoutputvertexcount.md), doit être <= 1024.</span><span class="sxs-lookup"><span data-stu-id="31493-116">The instance count in this declaration, multiplied by the maximum vertex count per instance via [**dcl\_maxOutputVertexCount**](dcl-maxoutputvertexcount.md), must be <= 1024.</span></span>

<span data-ttu-id="31493-117">La quantité de données qu’une instance de nuanceur Geometry donnée peut émettre est 1024 scalaires maximum, validée en comptant toutes les valeurs scalaires déclarées pour l’entrée et en la multipliant par le nombre de vertex de sortie déclaré.</span><span class="sxs-lookup"><span data-stu-id="31493-117">The amount of data that a given geometry shader instance can emit is 1024 scalars maximum, validated by counting up all scalars declared for input and multiplying by the declared output vertex count.</span></span>

<span data-ttu-id="31493-118">L’utilisation de l’instanciation de nuanceur Geometry augmente efficacement la quantité totale de données qui peuvent être émises par primitive d’entrée.</span><span class="sxs-lookup"><span data-stu-id="31493-118">Use of geometry shader instancing effectively increases the total amount of data that can be emitted per input primitive.</span></span> <span data-ttu-id="31493-119">1024 Scalar pour une instance unique produit jusqu’à 1024 \* 32 scalaires de données de sortie sur toutes les instances de nuanceur Geometry pour une seule primitive d’entrée.</span><span class="sxs-lookup"><span data-stu-id="31493-119">1024 scalars for a single instance yields up to 1024\*32 scalars of output data across all geometry shader instances for a single input primitive.</span></span> <span data-ttu-id="31493-120">Toutefois, plus le nombre d’instances est élevé, plus le nombre de vertex de chaque instance peut être émis.</span><span class="sxs-lookup"><span data-stu-id="31493-120">However the more instances, the fewer vertices each instance can emit.</span></span> <span data-ttu-id="31493-121">Une seule instance (sans instanciation) peut émettre 1024 sommets.</span><span class="sxs-lookup"><span data-stu-id="31493-121">A single instance (no instancing) can emit 1024 vertices.</span></span> <span data-ttu-id="31493-122">Si vous déclarez \* 32 instances, cela signifie que chaque instance peut uniquement produire des sommets 1024/32 = 32.</span><span class="sxs-lookup"><span data-stu-id="31493-122">If you declare \*32 instances it means each instance can only output 1024/32 = 32 vertices.</span></span>

<span data-ttu-id="31493-123">La déclaration d’instanciation du nuanceur Geometry met à la disposition du programme un registre d’entrée d’entier 32 bits autonome, *vGSInstanceID*.</span><span class="sxs-lookup"><span data-stu-id="31493-123">The geometry shader instancing declaration makes available to the program a standalone 32-bit integer input register, *vGSInstanceID*.</span></span> <span data-ttu-id="31493-124">Chaque instance de nuanceur Geometry est identifiée par la valeur contenue dans *vGSInstanceID* \[ 0, 1, 2... \] .</span><span class="sxs-lookup"><span data-stu-id="31493-124">Each geometry shader instance is identified by the value contained in *vGSInstanceID* \[0,1,2...\].</span></span>

<span data-ttu-id="31493-125">*vGSInstanceID* ne fait pas partie du tableau de vertex d’entrée du nuanceur de géométrie (par exemple, 3 sommets lors de l’entrée d’un triangle).</span><span class="sxs-lookup"><span data-stu-id="31493-125">*vGSInstanceID* is not part of the geometry shader input vertex array (e.g. 3 vertices when inputting a triangle).</span></span> <span data-ttu-id="31493-126">Le Registre *vGSInstanceID* est autonome, comme vPrimitiveID.</span><span class="sxs-lookup"><span data-stu-id="31493-126">The *vGSInstanceID* register stands on its own, like vPrimitiveID.</span></span>

<span data-ttu-id="31493-127">Lorsque chaque instance de nuanceur Geometry se termine, il existe une coupe implicite de la topologie de sortie, de sorte que les instances consécutives ne dépendent pas les unes des autres.</span><span class="sxs-lookup"><span data-stu-id="31493-127">When each geometry shader instance ends, there is an implicit cut in the output topology, so consecutive instances do not depend on each other.</span></span>

<span data-ttu-id="31493-128">Bien que le matériel puisse exécuter chaque instance de nuanceur Geometry en parallèle, la sortie de toutes les instances à la fin est sérialisée comme si tous les appels de nuanceur Geometry d’instance aient été exécutés de manière séquentielle dans une boucle qui itère *vGSInstanceID* de 0 à *instanceCount*-1, avec des coupes de topologie de sortie implicites à la fin de chaque instance.</span><span class="sxs-lookup"><span data-stu-id="31493-128">Although hardware may execute each geometry shader instance in parallel, the output of all instances at the end is serialized as if all the instanced geometry shader invocations ran sequentially in a loop iterating *vGSInstanceID* from 0 to *instanceCount*-1, with implicit output topology cuts at the end of each instance.</span></span>

<span data-ttu-id="31493-129">Cette instruction s’applique aux étapes suivantes du nuanceur :</span><span class="sxs-lookup"><span data-stu-id="31493-129">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="31493-130">Sommet</span><span class="sxs-lookup"><span data-stu-id="31493-130">Vertex</span></span> | <span data-ttu-id="31493-131">Forme</span><span class="sxs-lookup"><span data-stu-id="31493-131">Hull</span></span> | <span data-ttu-id="31493-132">Domain</span><span class="sxs-lookup"><span data-stu-id="31493-132">Domain</span></span> | <span data-ttu-id="31493-133">Géométrie</span><span class="sxs-lookup"><span data-stu-id="31493-133">Geometry</span></span> | <span data-ttu-id="31493-134">Pixel</span><span class="sxs-lookup"><span data-stu-id="31493-134">Pixel</span></span> | <span data-ttu-id="31493-135">Compute</span><span class="sxs-lookup"><span data-stu-id="31493-135">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        | <span data-ttu-id="31493-136">X</span><span class="sxs-lookup"><span data-stu-id="31493-136">X</span></span>        |       |         |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="31493-137">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="31493-137">Minimum Shader Model</span></span>

<span data-ttu-id="31493-138">Cette instruction est prise en charge dans les modèles de nuanceur suivants :</span><span class="sxs-lookup"><span data-stu-id="31493-138">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="31493-139">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="31493-139">Shader Model</span></span>                                              | <span data-ttu-id="31493-140">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="31493-140">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="31493-141">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="31493-141">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="31493-142">Oui</span><span class="sxs-lookup"><span data-stu-id="31493-142">yes</span></span>       |
| [<span data-ttu-id="31493-143">Modèle de nuanceur 4,1</span><span class="sxs-lookup"><span data-stu-id="31493-143">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="31493-144">non</span><span class="sxs-lookup"><span data-stu-id="31493-144">no</span></span>        |
| [<span data-ttu-id="31493-145">Nuanceur modèle 4</span><span class="sxs-lookup"><span data-stu-id="31493-145">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="31493-146">non</span><span class="sxs-lookup"><span data-stu-id="31493-146">no</span></span>        |
| [<span data-ttu-id="31493-147">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="31493-147">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="31493-148">non</span><span class="sxs-lookup"><span data-stu-id="31493-148">no</span></span>        |
| [<span data-ttu-id="31493-149">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="31493-149">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="31493-150">non</span><span class="sxs-lookup"><span data-stu-id="31493-150">no</span></span>        |
| [<span data-ttu-id="31493-151">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="31493-151">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="31493-152">non</span><span class="sxs-lookup"><span data-stu-id="31493-152">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="31493-153">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="31493-153">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="31493-154">Assembly modèle 5 du nuanceur (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="31493-154">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





