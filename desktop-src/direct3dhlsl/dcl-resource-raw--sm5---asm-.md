---
title: dcl_resource brut (SM5-ASM)
description: Déclarez une entrée de ressource de nuanceur et affectez-la à un registre d’espace réservé t \ a pour la ressource. | dcl_resource brut (SM5-ASM)
ms.assetid: ECBA9DAB-F217-47FB-9588-F35866004E72
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8dd6ccc5990e34990772a072086d9e080cde67b4
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104211492"
---
# <a name="dcl_resource-raw-sm5---asm"></a><span data-ttu-id="32e18-104">DCL \_ ressource brute (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="32e18-104">dcl\_resource raw (sm5 - asm)</span></span>

<span data-ttu-id="32e18-105">Déclarez une entrée de ressource de nuanceur et affectez-la à un \# Registre d’espace réservé t-a pour la ressource.</span><span class="sxs-lookup"><span data-stu-id="32e18-105">Declare a shader resource input and assign it to a t\# - a placeholder register for the resource.</span></span>



| <span data-ttu-id="32e18-106">\_ \_ dstSRV brute de la ressource DCL</span><span class="sxs-lookup"><span data-stu-id="32e18-106">dcl\_resource\_raw dstSRV</span></span> |
|---------------------------|



 



| <span data-ttu-id="32e18-107">Élément</span><span class="sxs-lookup"><span data-stu-id="32e18-107">Item</span></span>                                                                                           | <span data-ttu-id="32e18-108">Description</span><span class="sxs-lookup"><span data-stu-id="32e18-108">Description</span></span>                                                                                       |
|------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="32e18-109"><span id="dstSRV"></span><span id="dstsrv"></span><span id="DSTSRV"></span>*dstSRV*</span><span class="sxs-lookup"><span data-stu-id="32e18-109"><span id="dstSRV"></span><span id="dstsrv"></span><span id="DSTSRV"></span>*dstSRV*</span></span><br/> | <span data-ttu-id="32e18-110">\[dans \] un \# Registre t déclaré comme référence à un ShaderResourceView d’une mémoire tampon brute.</span><span class="sxs-lookup"><span data-stu-id="32e18-110">\[in\] A t\# register declared as a reference to a ShaderResourceView of a raw buffer.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="32e18-111">Notes</span><span class="sxs-lookup"><span data-stu-id="32e18-111">Remarks</span></span>

<span data-ttu-id="32e18-112">Le contenu de la structure n’a pas de type ; les opérations effectuées sur la mémoire peuvent interpréter implicitement les données comme ayant un type.</span><span class="sxs-lookup"><span data-stu-id="32e18-112">The contents of the structure have no type; operations performed on the memory may implicitly interpret the data as having a type.</span></span>

<span data-ttu-id="32e18-113">Les instructions qui font référence à un t brut \# acceptent une adresse 1D, une valeur non signée 32 bits qui spécifie l’offset d’octet à un emplacement aligné sur 32 bits dans la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="32e18-113">Instructions that reference a raw t\# take a 1D address, an unsigned 32-bit value specifying the byte offset to a 32-bit aligned location in the Buffer.</span></span> <span data-ttu-id="32e18-114">L’adresse doit être un multiple de 4 (octets).</span><span class="sxs-lookup"><span data-stu-id="32e18-114">The address must be a multiple of 4 (bytes).</span></span>

<span data-ttu-id="32e18-115">Les vues liées à t \# déclarées comme RAW doivent avoir une valeur RAW spécifiée lors de leur création ; sinon, le comportement en cas d’accès à partir d’un nuanceur n’est pas défini.</span><span class="sxs-lookup"><span data-stu-id="32e18-115">Views bound to t\# declared as raw must have RAW specified on their creation; otherwise behavior when accessed from a shader is undefined.</span></span>

<span data-ttu-id="32e18-116">CS \_ 4 \_ 0 et CS \_ 4 \_ 1 prennent en charge cette instruction.</span><span class="sxs-lookup"><span data-stu-id="32e18-116">cs\_4\_0 and cs\_4\_1 support this instruction.</span></span>

<span data-ttu-id="32e18-117">Cette instruction s’applique aux étapes suivantes du nuanceur :</span><span class="sxs-lookup"><span data-stu-id="32e18-117">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="32e18-118">Sommet</span><span class="sxs-lookup"><span data-stu-id="32e18-118">Vertex</span></span> | <span data-ttu-id="32e18-119">Forme</span><span class="sxs-lookup"><span data-stu-id="32e18-119">Hull</span></span> | <span data-ttu-id="32e18-120">Domain</span><span class="sxs-lookup"><span data-stu-id="32e18-120">Domain</span></span> | <span data-ttu-id="32e18-121">Géométrie</span><span class="sxs-lookup"><span data-stu-id="32e18-121">Geometry</span></span> | <span data-ttu-id="32e18-122">Pixel</span><span class="sxs-lookup"><span data-stu-id="32e18-122">Pixel</span></span> | <span data-ttu-id="32e18-123">Compute</span><span class="sxs-lookup"><span data-stu-id="32e18-123">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="32e18-124">X</span><span class="sxs-lookup"><span data-stu-id="32e18-124">X</span></span>      | <span data-ttu-id="32e18-125">X</span><span class="sxs-lookup"><span data-stu-id="32e18-125">X</span></span>    | <span data-ttu-id="32e18-126">X</span><span class="sxs-lookup"><span data-stu-id="32e18-126">X</span></span>      | <span data-ttu-id="32e18-127">X</span><span class="sxs-lookup"><span data-stu-id="32e18-127">X</span></span>        | <span data-ttu-id="32e18-128">X</span><span class="sxs-lookup"><span data-stu-id="32e18-128">X</span></span>     | <span data-ttu-id="32e18-129">X</span><span class="sxs-lookup"><span data-stu-id="32e18-129">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="32e18-130">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="32e18-130">Minimum Shader Model</span></span>

<span data-ttu-id="32e18-131">Cette instruction est prise en charge dans les modèles de nuanceur suivants :</span><span class="sxs-lookup"><span data-stu-id="32e18-131">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="32e18-132">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="32e18-132">Shader Model</span></span>                                              | <span data-ttu-id="32e18-133">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="32e18-133">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="32e18-134">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="32e18-134">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="32e18-135">Oui</span><span class="sxs-lookup"><span data-stu-id="32e18-135">yes</span></span>       |
| [<span data-ttu-id="32e18-136">Modèle de nuanceur 4,1</span><span class="sxs-lookup"><span data-stu-id="32e18-136">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="32e18-137">non</span><span class="sxs-lookup"><span data-stu-id="32e18-137">no</span></span>        |
| [<span data-ttu-id="32e18-138">Nuanceur modèle 4</span><span class="sxs-lookup"><span data-stu-id="32e18-138">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="32e18-139">non</span><span class="sxs-lookup"><span data-stu-id="32e18-139">no</span></span>        |
| [<span data-ttu-id="32e18-140">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="32e18-140">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="32e18-141">non</span><span class="sxs-lookup"><span data-stu-id="32e18-141">no</span></span>        |
| [<span data-ttu-id="32e18-142">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="32e18-142">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="32e18-143">non</span><span class="sxs-lookup"><span data-stu-id="32e18-143">no</span></span>        |
| [<span data-ttu-id="32e18-144">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="32e18-144">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="32e18-145">non</span><span class="sxs-lookup"><span data-stu-id="32e18-145">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="32e18-146">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="32e18-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="32e18-147">Assembly modèle 5 du nuanceur (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="32e18-147">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





