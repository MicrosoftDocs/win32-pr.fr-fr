---
title: dcl_resource (SM4-ASM)
description: '\_ressource DCL (SM4-ASM)'
ms.assetid: 045610f0-f7db-4bf2-bfea-501bbee94601
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: bb65a8ea83feaf2fec80403fc9ac6c2ab38c1936
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/20/2019
ms.locfileid: "103679181"
---
# <a name="dcl_resource-sm4---asm"></a><span data-ttu-id="aa434-103">\_ressource DCL (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="aa434-103">dcl\_resource (sm4 - asm)</span></span>

<span data-ttu-id="aa434-104">Déclare une ressource d’entrée de nuanceur non multiéchantillonnée.</span><span class="sxs-lookup"><span data-stu-id="aa434-104">Declares a non-multisampled shader-input resource.</span></span>



| <span data-ttu-id="aa434-105">DCL \_ Resource *TN*, *resourceType*, *ReturnType (s)*</span><span class="sxs-lookup"><span data-stu-id="aa434-105">dcl\_resource *tN*, *resourceType*, *returnType(s)*</span></span> |
|-----------------------------------------------------|



 

<span data-ttu-id="aa434-106">Déclare une ressource d’entrée de nuanceur à échantillonnages.</span><span class="sxs-lookup"><span data-stu-id="aa434-106">Declares a multisampled shader-input resource.</span></span>



| <span data-ttu-id="aa434-107">DCL \_ Resource *TN*, *resourceType \[ size \] nn*, *ReturnType (s)*</span><span class="sxs-lookup"><span data-stu-id="aa434-107">dcl\_resource *tN*, *resourceType\[size\]NN*, *returnType(s)*</span></span> |
|---------------------------------------------------------------|



 



| <span data-ttu-id="aa434-108">Élément</span><span class="sxs-lookup"><span data-stu-id="aa434-108">Item</span></span>                                                                                                                                                     | <span data-ttu-id="aa434-109">Description</span><span class="sxs-lookup"><span data-stu-id="aa434-109">Description</span></span>                                                                                                                                                                                                                                                              |
|----------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="aa434-110"><span id="tN"></span><span id="tn"></span><span id="TN"></span>t *N*</span><span class="sxs-lookup"><span data-stu-id="aa434-110"><span id="tN"></span><span id="tn"></span><span id="TN"></span>t *N*</span></span><br/>                                                                           | <span data-ttu-id="aa434-111">\[dans \] le registre de texture, où *N* est un entier qui désigne le numéro du Registre.</span><span class="sxs-lookup"><span data-stu-id="aa434-111">\[in\] The texture register, where *N* is an integer that denotes the register number.</span></span><br/>                                                                                                                                                                        |
| <span data-ttu-id="aa434-112"><span id="resourceType"></span><span id="resourcetype"></span><span id="RESOURCETYPE"></span>*resourceType*</span><span class="sxs-lookup"><span data-stu-id="aa434-112"><span id="resourceType"></span><span id="resourcetype"></span><span id="RESOURCETYPE"></span>*resourceType*</span></span><br/>                                   | <span data-ttu-id="aa434-113">\[dans \] tout type d’objet figurant dans la page [texture-objet](dx-graphics-hlsl-to-type.md) .</span><span class="sxs-lookup"><span data-stu-id="aa434-113">\[in\] Any object type listed in the [texture-object](dx-graphics-hlsl-to-type.md) page.</span></span><br/>                                                                                                                                                                     |
| <span data-ttu-id="aa434-114"><span id="resourceType_size_NN"></span><span id="resourcetype_size_nn"></span><span id="RESOURCETYPE_SIZE_NN"></span>*taille du resourceType \[ \] nn*</span><span class="sxs-lookup"><span data-stu-id="aa434-114"><span id="resourceType_size_NN"></span><span id="resourcetype_size_nn"></span><span id="RESOURCETYPE_SIZE_NN"></span>*resourceType\[size\]NN*</span></span><br/> | <span data-ttu-id="aa434-115">\[dans \] un Texture2D ou un type d’objet Texture2DArray (consultez la page [texture-objet](dx-graphics-hlsl-to-type.md) ); la *taille* est un entier facultatif qui indique le nombre d’éléments dans le tableau ; *Nn* est un entier qui indique le nombre d’échantillonnages.</span><span class="sxs-lookup"><span data-stu-id="aa434-115">\[in\] A Texture2D or a Texture2DArray object type (see the [texture-object](dx-graphics-hlsl-to-type.md) page); *size* is an optional integer that denotes the number of elements in the array; *NN* is an integer that denotes the number of multisamples.</span></span><br/> |
| <span data-ttu-id="aa434-116"><span id="returnType_s_"></span><span id="returntype_s_"></span><span id="RETURNTYPE_S_"></span>*returnType (s)*</span><span class="sxs-lookup"><span data-stu-id="aa434-116"><span id="returnType_s_"></span><span id="returntype_s_"></span><span id="RETURNTYPE_S_"></span>*returnType(s)*</span></span><br/>                               | <span data-ttu-id="aa434-117">\[dans \] le type de retour par composant qui est l’un des suivants : UNORM, ronfler, Saint, uint ou float.</span><span class="sxs-lookup"><span data-stu-id="aa434-117">\[in\] Per-component return type which is one of the following: UNORM, SNORM, SINT, UINT, or FLOAT.</span></span> <span data-ttu-id="aa434-118">Le nombre de types de retour peut être égal à 1 (si tous les composants sont du même type), mais peut avoir jusqu’à quatre.</span><span class="sxs-lookup"><span data-stu-id="aa434-118">The number of return types can be as few as 1 (if all components are the same type), but can be as many as four.</span></span><br/>                                          |



 

<span data-ttu-id="aa434-119">Une ressource est accessible en HLSL à l’aide de la [charge](dx-graphics-hlsl-to-load.md); une texture non multiéchantillonnée est également accessible à l’aide de l’un des exemples de méthodes d' [objet de texture](dx-graphics-hlsl-to-type.md) HLSL.</span><span class="sxs-lookup"><span data-stu-id="aa434-119">A resource is accessed in HLSL using [load](dx-graphics-hlsl-to-load.md); a non-multisampled texture can also be accessed using any of the HLSL [texture object](dx-graphics-hlsl-to-type.md) sample methods.</span></span>

<span data-ttu-id="aa434-120">Si une ressource est liée à une étape de nuanceur, le format de ressource est validé par rapport au type de retour.</span><span class="sxs-lookup"><span data-stu-id="aa434-120">If a resource is bound to a shader stage, the resource format will be validated against the return type.</span></span>

<span data-ttu-id="aa434-121">Cette instruction s’applique aux étapes suivantes du nuanceur :</span><span class="sxs-lookup"><span data-stu-id="aa434-121">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="aa434-122">Nuanceur de sommets</span><span class="sxs-lookup"><span data-stu-id="aa434-122">Vertex Shader</span></span> | <span data-ttu-id="aa434-123">Nuanceur de géométrie</span><span class="sxs-lookup"><span data-stu-id="aa434-123">Geometry Shader</span></span> | <span data-ttu-id="aa434-124">Nuanceur de pixels</span><span class="sxs-lookup"><span data-stu-id="aa434-124">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="aa434-125">x</span><span class="sxs-lookup"><span data-stu-id="aa434-125">x</span></span>             | <span data-ttu-id="aa434-126">x</span><span class="sxs-lookup"><span data-stu-id="aa434-126">x</span></span>               | <span data-ttu-id="aa434-127">x</span><span class="sxs-lookup"><span data-stu-id="aa434-127">x</span></span>            |



 

<span data-ttu-id="aa434-128">Cette instruction est incluse pour faciliter le débogage d’un nuanceur dans l’assembly. vous ne pouvez pas créer de nuanceur dans un langage assembleur à l’aide du nuanceur modèle 4.</span><span class="sxs-lookup"><span data-stu-id="aa434-128">This instruction is included to aid in debugging a shader in assembly; you cannot author a shader in assembly language using Shader Model 4.</span></span>

## <a name="example"></a><span data-ttu-id="aa434-129">Exemple</span><span class="sxs-lookup"><span data-stu-id="aa434-129">Example</span></span>

<span data-ttu-id="aa434-130">Voici un exemple.</span><span class="sxs-lookup"><span data-stu-id="aa434-130">Here is an example.</span></span>


```
dcl_resource t3, buffer, UNORM
```



## <a name="minimum-shader-model"></a><span data-ttu-id="aa434-131">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="aa434-131">Minimum Shader Model</span></span>

<span data-ttu-id="aa434-132">Cette fonction est prise en charge dans les modèles de nuanceur suivants.</span><span class="sxs-lookup"><span data-stu-id="aa434-132">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="aa434-133">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="aa434-133">Shader Model</span></span>                                              | <span data-ttu-id="aa434-134">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="aa434-134">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="aa434-135">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="aa434-135">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="aa434-136">Oui</span><span class="sxs-lookup"><span data-stu-id="aa434-136">yes</span></span>       |
| [<span data-ttu-id="aa434-137">Modèle de nuanceur 4,1</span><span class="sxs-lookup"><span data-stu-id="aa434-137">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="aa434-138">Oui</span><span class="sxs-lookup"><span data-stu-id="aa434-138">yes</span></span>       |
| [<span data-ttu-id="aa434-139">Nuanceur modèle 4</span><span class="sxs-lookup"><span data-stu-id="aa434-139">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="aa434-140">Oui</span><span class="sxs-lookup"><span data-stu-id="aa434-140">yes</span></span>       |
| [<span data-ttu-id="aa434-141">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="aa434-141">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="aa434-142">non</span><span class="sxs-lookup"><span data-stu-id="aa434-142">no</span></span>        |
| [<span data-ttu-id="aa434-143">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="aa434-143">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="aa434-144">non</span><span class="sxs-lookup"><span data-stu-id="aa434-144">no</span></span>        |
| [<span data-ttu-id="aa434-145">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="aa434-145">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="aa434-146">non</span><span class="sxs-lookup"><span data-stu-id="aa434-146">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="aa434-147">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="aa434-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="aa434-148">Assembly modèle 4 du nuanceur (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="aa434-148">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





