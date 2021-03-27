---
title: Modèle de nuanceur HLSL 6,4
description: Décrit les Machine Learning intrinsèques ajoutés au modèle de nuanceur HLSL 6,4.
ms.topic: article
ms.date: 02/21/2019
ms.openlocfilehash: 10e74b268243ab059c2d0945887a6d429d40bb53
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2021
ms.locfileid: "103869645"
---
# <a name="hlsl-shader-model-64"></a><span data-ttu-id="e4c12-103">Modèle de nuanceur HLSL 6,4</span><span class="sxs-lookup"><span data-stu-id="e4c12-103">HLSL Shader Model 6.4</span></span>

<span data-ttu-id="e4c12-104">Décrit les Machine Learning intrinsèques ajoutés au modèle de nuanceur HLSL 6,4.</span><span class="sxs-lookup"><span data-stu-id="e4c12-104">Describes the machine learning intrinsics added to HLSL Shader Model 6.4.</span></span>

## <a name="shader-model-64"></a><span data-ttu-id="e4c12-105">Modèle de nuanceur 6,4</span><span class="sxs-lookup"><span data-stu-id="e4c12-105">Shader Model 6.4</span></span>
<span data-ttu-id="e4c12-106">Ces fonctions intrinsèques sont une fonctionnalité requise/prise en charge du modèle de nuanceur 6,4.</span><span class="sxs-lookup"><span data-stu-id="e4c12-106">These intrinsics are a required/supported feature of Shader model 6.4.</span></span> <span data-ttu-id="e4c12-107">Par conséquent, aucune vérification de bit de capacité distincte n’est requise, au-delà de la garantie de l’utilisation du modèle de nuanceur 6,4.</span><span class="sxs-lookup"><span data-stu-id="e4c12-107">Consequently, no separate capability bit check is required, beyond assuring the use of Shader Model 6.4.</span></span> <span data-ttu-id="e4c12-108">Le client minimal pris en charge pour ces routines est Windows 10, version 1903.</span><span class="sxs-lookup"><span data-stu-id="e4c12-108">The minimum supported client for these routines is Windows 10, version 1903.</span></span>

## <a name="shading-language-intrinsics"></a><span data-ttu-id="e4c12-109">Intrinsèques du langage d’ombrage</span><span class="sxs-lookup"><span data-stu-id="e4c12-109">Shading language intrinsics</span></span>

### <a name="unsigned-integer-dot-product-of-4-elements-and-accumulate"></a><span data-ttu-id="e4c12-110">Entier non signé Dot-Product de 4 éléments et cumuler</span><span class="sxs-lookup"><span data-stu-id="e4c12-110">Unsigned Integer Dot-Product of 4 Elements and Accumulate</span></span>
```syntax
uint32 dot4add_u8packed(uint32 a, uint32 b, uint32 acc); // ubyte4 a, b;
```
 
<span data-ttu-id="e4c12-111">Un point-produit d’entier non signé à 4 dimensions avec Add.</span><span class="sxs-lookup"><span data-stu-id="e4c12-111">A 4-dimensional unsigned integer dot-product with add.</span></span> <span data-ttu-id="e4c12-112">Multiplie chaque paire correspondante d’octets de type entier 8 bits non signés dans les deux valeurs DWORD d’entrée et additionne les résultats dans l’accumulation d’entiers non signés 32 bits.</span><span class="sxs-lookup"><span data-stu-id="e4c12-112">Multiplies together each corresponding pair of unsigned 8-bit int bytes in the two input DWORDs, and sums the results into the 32-bit unsigned integer accumulator.</span></span> <span data-ttu-id="e4c12-113">Cette instruction fonctionne dans une seule voie SIMD de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="e4c12-113">This instruction operates within a single 32-bit wide SIMD lane.</span></span> <span data-ttu-id="e4c12-114">Les entrées sont également supposées être des quantités de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="e4c12-114">The inputs are also assumed to be 32-bit quantities.</span></span>
 
### <a name="signed-integer-dot-product-of-4-elements-and-accumulate"></a><span data-ttu-id="e4c12-115">Dot-Product entier signé de 4 éléments et cumul</span><span class="sxs-lookup"><span data-stu-id="e4c12-115">Signed Integer Dot-Product of 4 Elements and Accumulate</span></span>
```syntax
int32 dot4add_i8packed(uint32 a, uint32 b, int32 acc); // signed byte4 a, b;
```

<span data-ttu-id="e4c12-116">Un produit-point entier signé à 4 dimensions avec Add.</span><span class="sxs-lookup"><span data-stu-id="e4c12-116">A 4-dimensional signed integer dot-product with add.</span></span> <span data-ttu-id="e4c12-117">Multiplie chaque paire correspondante d’octets de type entier 8 bits signés dans les deux valeurs DWORD d’entrée et additionne les résultats dans l’accumulation d’entiers signés 32 bits.</span><span class="sxs-lookup"><span data-stu-id="e4c12-117">Multiplies together each corresponding pair of signed 8-bit int bytes in the two input DWORDs, and sums the results into the 32-bit signed integer accumulator.</span></span> <span data-ttu-id="e4c12-118">Cette instruction fonctionne dans une seule voie SIMD de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="e4c12-118">This instruction operates within a single 32-bit wide SIMD lane.</span></span> <span data-ttu-id="e4c12-119">Les entrées sont également supposées être des quantités de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="e4c12-119">The inputs are also assumed to be 32-bit quantities.</span></span>
 
### <a name="single-precision-floating-point-2-element-dot-product-and-accumulate"></a><span data-ttu-id="e4c12-120">Dot-Product à virgule flottante simple précision 2 éléments et cumuler</span><span class="sxs-lookup"><span data-stu-id="e4c12-120">Single Precision Floating Point 2-Element Dot-Product and Accumulate</span></span>
```syntax
float dot2add( half2 a, half2 b, float acc );
```

<span data-ttu-id="e4c12-121">Un point à virgule flottante à deux dimensions-produit de vecteurs Half2 avec Add.</span><span class="sxs-lookup"><span data-stu-id="e4c12-121">A 2-dimensional floating point dot-product of half2 vectors with add.</span></span> <span data-ttu-id="e4c12-122">Multiplie les éléments des deux vecteurs d’entrée float demi-précision et additionne les résultats dans l’accumulateur float 32 bits.</span><span class="sxs-lookup"><span data-stu-id="e4c12-122">Multiplies the elements of the two half-precision float input vectors together and sums the results into the 32-bit float accumulator.</span></span> <span data-ttu-id="e4c12-123">Ces instructions fonctionnent au sein d’une seule voie SIMD 32 bits.</span><span class="sxs-lookup"><span data-stu-id="e4c12-123">This instructions operates within a single 32-bit wide SIMD lane.</span></span> <span data-ttu-id="e4c12-124">Les entrées sont des quantités de 16 bits compressées dans la même voie.</span><span class="sxs-lookup"><span data-stu-id="e4c12-124">The inputs are 16-bit quantities packed into the same lane.</span></span>

<span data-ttu-id="e4c12-125">Cette fonctionnalité est couverte par le bit de fonctionnalité de faible précision (indiquant que la prise en charge native est présente).</span><span class="sxs-lookup"><span data-stu-id="e4c12-125">This is covered under the low-precision feature bit (indicating that native half and short support are present).</span></span>

### <a name="sv_shadingrate"></a><span data-ttu-id="e4c12-126">SV_ShadingRate</span><span class="sxs-lookup"><span data-stu-id="e4c12-126">SV_ShadingRate</span></span>
```syntax
uint shadingRate : SV_ShadingRate
```

<span data-ttu-id="e4c12-127">Entier non signé représentant le nombre de pixels cibles écrits par chaque appel du nuanceur de pixels.</span><span class="sxs-lookup"><span data-stu-id="e4c12-127">An unsigned integer representing how many target pixels are written by each invocation of the pixel shader.</span></span> <span data-ttu-id="e4c12-128">Les valeurs valides appartiennent à un ensemble de valeurs d’énumération [D3D12_SHADING_RATE](/windows/win32/api/d3d12/ne-d3d12-d3d12_shading_rate).</span><span class="sxs-lookup"><span data-stu-id="e4c12-128">Valid values belong to set of enumeration values [D3D12_SHADING_RATE](/windows/win32/api/d3d12/ne-d3d12-d3d12_shading_rate).</span></span>

<span data-ttu-id="e4c12-129">Cette valeur système est disponible sur les plateformes qui sont [D3D12_VARIABLE_SHADING_RATE_TIER_2](/windows/win32/api/d3d12/ne-d3d12-d3d12_variable_shading_rate_tier) ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="e4c12-129">This system value is available on platforms that are [D3D12_VARIABLE_SHADING_RATE_TIER_2](/windows/win32/api/d3d12/ne-d3d12-d3d12_variable_shading_rate_tier) or higher.</span></span> <span data-ttu-id="e4c12-130">Il peut être écrit à partir de au plus une des étapes du nuanceur de vertex ou Geometry.</span><span class="sxs-lookup"><span data-stu-id="e4c12-130">It can be written from at most one of vertex or geometry shader stages.</span></span> <span data-ttu-id="e4c12-131">Il peut être lu à partir de l’étape nuanceur de pixels.</span><span class="sxs-lookup"><span data-stu-id="e4c12-131">It can be read from the pixel shader stage.</span></span> <span data-ttu-id="e4c12-132">Pour plus d’informations, consultez l' [ombrage à taux variable](../direct3d12/vrs.md).</span><span class="sxs-lookup"><span data-stu-id="e4c12-132">For more information, see the [Variable-rate Shading](../direct3d12/vrs.md).</span></span>