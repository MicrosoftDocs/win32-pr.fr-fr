---
title: msad4
description: Compare une valeur de référence de 4 octets et une valeur source de 8 octets et accumule un vecteur de 4 sommes. Chaque somme correspond à la somme masquée de différences absolues d’un alignement d’octets différent entre la valeur de référence et la valeur source.
ms.assetid: 6497F9AE-4524-44C2-A1C6-2A4ACB30FA9C
keywords:
- HLSL msad4
topic_type:
- apiref
api_name:
- msad4
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 552db3afd07677777b47e939d659c0f6e333e496
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104971855"
---
# <a name="msad4"></a><span data-ttu-id="fee7d-105">msad4</span><span class="sxs-lookup"><span data-stu-id="fee7d-105">msad4</span></span>

<span data-ttu-id="fee7d-106">Compare une valeur de référence de 4 octets et une valeur source de 8 octets et accumule un vecteur de 4 sommes.</span><span class="sxs-lookup"><span data-stu-id="fee7d-106">Compares a 4-byte reference value and an 8-byte source value and accumulates a vector of 4 sums.</span></span> <span data-ttu-id="fee7d-107">Chaque somme correspond à la somme masquée de différences absolues d’un alignement d’octets différent entre la valeur de référence et la valeur source.</span><span class="sxs-lookup"><span data-stu-id="fee7d-107">Each sum corresponds to the masked sum of absolute differences of a different byte alignment between the reference value and the source value.</span></span>



| <span data-ttu-id="fee7d-108">uint4 result = msad4 (référence uint, source uint2, uint4 cumuler);</span><span class="sxs-lookup"><span data-stu-id="fee7d-108">uint4 result = msad4(uint reference, uint2 source, uint4 accum);</span></span> |
|------------------------------------------------------------------|



 

## <a name="parameters"></a><span data-ttu-id="fee7d-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="fee7d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fee7d-110"><span id="reference"></span><span id="REFERENCE"></span>*faire*</span><span class="sxs-lookup"><span data-stu-id="fee7d-110"><span id="reference"></span><span id="REFERENCE"></span>*reference*</span></span>
</dt> <dd>

<span data-ttu-id="fee7d-111">\[dans \] le tableau de référence de 4 octets dans une valeur **uint** .</span><span class="sxs-lookup"><span data-stu-id="fee7d-111">\[in\] The reference array of 4 bytes in one **uint** value.</span></span>

</dd> <dt>

<span data-ttu-id="fee7d-112"><span id="source"></span><span id="SOURCE"></span>*code*</span><span class="sxs-lookup"><span data-stu-id="fee7d-112"><span id="source"></span><span id="SOURCE"></span>*source*</span></span>
</dt> <dd>

<span data-ttu-id="fee7d-113">\[dans \] le tableau source de 8 octets dans deux valeurs **uint2** .</span><span class="sxs-lookup"><span data-stu-id="fee7d-113">\[in\] The source array of 8 bytes in two **uint2** values.</span></span>

</dd> <dt>

<span data-ttu-id="fee7d-114"><span id="accum"></span><span id="ACCUM"></span>*cumuleur*</span><span class="sxs-lookup"><span data-stu-id="fee7d-114"><span id="accum"></span><span id="ACCUM"></span>*accum*</span></span>
</dt> <dd>

<span data-ttu-id="fee7d-115">\[dans \] un vecteur de 4 valeurs.</span><span class="sxs-lookup"><span data-stu-id="fee7d-115">\[in\] A vector of 4 values.</span></span> <span data-ttu-id="fee7d-116">**msad4** ajoute ce vecteur à la somme masquée de différences absolues des différents alignements d’octets entre la valeur de référence et la valeur source.</span><span class="sxs-lookup"><span data-stu-id="fee7d-116">**msad4** adds this vector to the masked sum of absolute differences of the different byte alignments between the reference value and the source value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fee7d-117">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="fee7d-117">Return Value</span></span>

<span data-ttu-id="fee7d-118">Vecteur de 4 sommes.</span><span class="sxs-lookup"><span data-stu-id="fee7d-118">A vector of 4 sums.</span></span> <span data-ttu-id="fee7d-119">Chaque somme correspond à la somme masquée de différences absolues d’alignements d’octets différents entre la valeur de référence et la valeur source.</span><span class="sxs-lookup"><span data-stu-id="fee7d-119">Each sum corresponds to the masked sum of absolute differences of different byte alignments between the reference value and the source value.</span></span> <span data-ttu-id="fee7d-120">**msad4** n’inclut pas de différence dans la somme si cette différence est masquée (autrement dit, l’octet de référence est 0).</span><span class="sxs-lookup"><span data-stu-id="fee7d-120">**msad4** doesn't include a difference in the sum if that difference is masked (that is, the reference byte is 0).</span></span>

## <a name="remarks"></a><span data-ttu-id="fee7d-121">Notes</span><span class="sxs-lookup"><span data-stu-id="fee7d-121">Remarks</span></span>

<span data-ttu-id="fee7d-122">Pour utiliser l’intrinsèque **msad4** dans le code de votre nuanceur, appelez la méthode [**ID3D11Device :: CheckFeatureSupport**](/windows/desktop/api/d3d11/nf-d3d11-id3d11device-checkfeaturesupport) avec la [**\_ fonctionnalité d3d11 \_ d3d11 \_ options**](/windows/desktop/api/d3d11/ne-d3d11-d3d11_feature) pour vérifier que l’appareil Direct3D prend en charge l’option de fonctionnalité [**SAD4ShaderInstructions**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_feature_data_d3d11_options) .</span><span class="sxs-lookup"><span data-stu-id="fee7d-122">To use the **msad4** intrinsic in your shader code, call the [**ID3D11Device::CheckFeatureSupport**](/windows/desktop/api/d3d11/nf-d3d11-id3d11device-checkfeaturesupport) method with [**D3D11\_FEATURE\_D3D11\_OPTIONS**](/windows/desktop/api/d3d11/ne-d3d11-d3d11_feature) to verify that the Direct3D device supports the [**SAD4ShaderInstructions**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_feature_data_d3d11_options) feature option.</span></span> <span data-ttu-id="fee7d-123">L’intrinsèque **msad4** requiert un pilote d’affichage WDDM 1,2, et tous les pilotes d’affichage WDDM 1,2 doivent prendre en charge **msad4**.</span><span class="sxs-lookup"><span data-stu-id="fee7d-123">The **msad4** intrinsic requires a WDDM 1.2 display driver, and all WDDM 1.2 display drivers must support **msad4**.</span></span> <span data-ttu-id="fee7d-124">Si votre application crée un appareil de rendu avec le [niveau de fonctionnalité](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) 11,0 ou 11,1 et que la cible de compilation est Shader Model 5 ou version ultérieure, le code source HLSL peut utiliser l’intrinsèque **msad4** .</span><span class="sxs-lookup"><span data-stu-id="fee7d-124">If your app creates a rendering device with [feature level](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) 11.0 or 11.1 and the compilation target is shader model 5 or later, the HLSL source code can use the **msad4** intrinsic.</span></span>

<span data-ttu-id="fee7d-125">Les valeurs de retour sont uniquement précises jusqu’à 65535.</span><span class="sxs-lookup"><span data-stu-id="fee7d-125">Return values are only accurate up to 65535.</span></span> <span data-ttu-id="fee7d-126">Si vous appelez l’intrinsèque **msad4** avec des entrées qui peuvent entraîner des valeurs de retour supérieures à 65535, **msad4** produit des résultats non définis.</span><span class="sxs-lookup"><span data-stu-id="fee7d-126">If you call the **msad4** intrinsic with inputs that might result in return values greater than 65535, **msad4** produces undefined results.</span></span>

### <a name="minimum-shader-model"></a><span data-ttu-id="fee7d-127">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="fee7d-127">Minimum Shader Model</span></span>

<span data-ttu-id="fee7d-128">Cette fonction est prise en charge dans les modèles de nuanceur suivants.</span><span class="sxs-lookup"><span data-stu-id="fee7d-128">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="fee7d-129">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="fee7d-129">Shader Model</span></span>                                                | <span data-ttu-id="fee7d-130">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="fee7d-130">Supported</span></span> |
|-------------------------------------------------------------|-----------|
| [<span data-ttu-id="fee7d-131">Shader Model 5 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="fee7d-131">Shader model 5 or later</span></span>](d3d11-graphics-reference-sm5.md) | <span data-ttu-id="fee7d-132">Oui</span><span class="sxs-lookup"><span data-stu-id="fee7d-132">yes</span></span>       |



 

## <a name="examples"></a><span data-ttu-id="fee7d-133">Exemples</span><span class="sxs-lookup"><span data-stu-id="fee7d-133">Examples</span></span>

<span data-ttu-id="fee7d-134">Voici un exemple de calcul des résultats pour **msad4**:</span><span class="sxs-lookup"><span data-stu-id="fee7d-134">Here is an example result calculation for **msad4**:</span></span>


```
reference = 0xA100B2C3;
source.x = 0xD7B0C372
source.y = 0x4F57C2A3
accum = {1,2,3,4}
result.x alignment source: 0xD7B0C372
result.x = accum.x + |0xD7   0xA1| + 0 (masked) + |0xC3   0xB2| + |0x72   0xC3| = 1 + 54 + 0 + 17 + 81 = 153
result.y alignment source: 0xA3D7B0C3
result.y = accum.y + |0xA3   0xA1| + 0 (masked) + |0xB0   0xB2| + |0xC3   0xC3| = 2 + 2 + 0 + 2 + 0 = 6
result.z alignment source: 0xC2A3D7B0
result.z = accum.z + |0xC2   0xA1| + 0 (masked) + |0xD7   0xB2| + |0xB0   0xC3| = 3 + 33 + 0 + 37 + 19 = 92
result.w alignment source: 0x57C2A3D7
result.w = accum.w + |0x57   0xA1| + 0 (masked) + |0xA3   0xB2| + |0xD7   0xC3| = 4 + 74 + 0 + 15 + 20 = 113
result = {153,6,92,113}
```



<span data-ttu-id="fee7d-135">Voici un exemple de la façon dont vous pouvez utiliser **msad4** pour rechercher un modèle de référence dans une mémoire tampon :</span><span class="sxs-lookup"><span data-stu-id="fee7d-135">Here is an example of how you can use **msad4** to search for a reference pattern within a buffer:</span></span>


```
uint4 accum = {0,0,0,0};
for(uint i=0;i<REF_SIZE;i++)
    accum = msad4(
        buf_ref[i], 
        uint2(buf_src[DTid.x+i], buf_src[DTid.x+i+1]), 
        accum);
buf_accum[DTid.x] = accum;
```



## <a name="requirements"></a><span data-ttu-id="fee7d-136">Spécifications</span><span class="sxs-lookup"><span data-stu-id="fee7d-136">Requirements</span></span>



| <span data-ttu-id="fee7d-137">Condition requise</span><span class="sxs-lookup"><span data-stu-id="fee7d-137">Requirement</span></span> | <span data-ttu-id="fee7d-138">Valeur</span><span class="sxs-lookup"><span data-stu-id="fee7d-138">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------|
| <span data-ttu-id="fee7d-139">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fee7d-139">Minimum supported client</span></span><br/> | <span data-ttu-id="fee7d-140">Applications Windows 8 \[ Desktop Apps \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="fee7d-140">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>           |
| <span data-ttu-id="fee7d-141">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fee7d-141">Minimum supported server</span></span><br/> | <span data-ttu-id="fee7d-142">Applications de bureau Windows Server 2012 \[ \| apps UWP\]</span><span class="sxs-lookup"><span data-stu-id="fee7d-142">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="fee7d-143">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fee7d-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fee7d-144">Fonctions intrinsèques</span><span class="sxs-lookup"><span data-stu-id="fee7d-144">Intrinsic Functions</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

