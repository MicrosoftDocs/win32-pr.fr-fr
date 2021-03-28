---
title: EvaluateAttributeSnapped fonction)
description: Évalue le centre de gravité des pixels avec un décalage.
ms.assetid: f5085016-0e94-49bb-96b6-42fa15c30b9f
keywords:
- EvaluateAttributeSnapped fonction HLSL
topic_type:
- apiref
api_name:
- EvaluateAttributeSnapped
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 70a9389ed9e9f4fff16f82610cb611bc4da2c7a3
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104990672"
---
# <a name="evaluateattributesnapped-function"></a><span data-ttu-id="0c615-104">EvaluateAttributeSnapped fonction)</span><span class="sxs-lookup"><span data-stu-id="0c615-104">EvaluateAttributeSnapped function</span></span>

<span data-ttu-id="0c615-105">Évalue le centre de gravité des pixels avec un décalage.</span><span class="sxs-lookup"><span data-stu-id="0c615-105">Evaluates at the pixel centroid with an offset.</span></span>

## <a name="syntax"></a><span data-ttu-id="0c615-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0c615-106">Syntax</span></span>

``` syntax
numeric EvaluateAttributeSnapped(
  in attrib numeric value,
  in 
            int2 offset
);
```

## <a name="parameters"></a><span data-ttu-id="0c615-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0c615-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0c615-108">*valeur* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="0c615-108">*value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0c615-109">Type : **Attrib Numeric**</span><span class="sxs-lookup"><span data-stu-id="0c615-109">Type: **attrib numeric**</span></span>

<span data-ttu-id="0c615-110">Valeur d'entrée.</span><span class="sxs-lookup"><span data-stu-id="0c615-110">The input value.</span></span>

</dd> <dt>

<span data-ttu-id="0c615-111">*décalage* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="0c615-111">*offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0c615-112">Type : **Int2**</span><span class="sxs-lookup"><span data-stu-id="0c615-112">Type: **int2**</span></span>

<span data-ttu-id="0c615-113">Décalage 2D à partir du centre de pixels à l’aide d’une grille 16x16.</span><span class="sxs-lookup"><span data-stu-id="0c615-113">A 2D offset from the pixel center using a 16x16 grid.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0c615-114">Notes</span><span class="sxs-lookup"><span data-stu-id="0c615-114">Remarks</span></span>

<span data-ttu-id="0c615-115">La plage du paramètre *offset* doit être définie par le code d’octet suivant.</span><span class="sxs-lookup"><span data-stu-id="0c615-115">The range for the *offset* parameter must be defined by the following byte code.</span></span>

<span data-ttu-id="0c615-116">Seuls les 4 bits les moins significatifs des deux premiers composants (U, V) de l’offset de pixel sont utilisés.</span><span class="sxs-lookup"><span data-stu-id="0c615-116">Only the least significant 4 bits of the first two components (U, V) of the pixel offset are used.</span></span> <span data-ttu-id="0c615-117">La conversion du point fixe 4 bits en float est la suivante (MSB... LSB), où le MSB est à la fois une partie de la fraction et détermine le signe :</span><span class="sxs-lookup"><span data-stu-id="0c615-117">The conversion from the 4-bit fixed point to float is as follows (MSB...LSB), where the MSB is both a part of the fraction and determines the sign:</span></span>

-   <span data-ttu-id="0c615-118">1000 =-0,5 f (-8/16)</span><span class="sxs-lookup"><span data-stu-id="0c615-118">1000 = -0.5f (-8 / 16)</span></span>
-   <span data-ttu-id="0c615-119">1001 =-0.4375 f (-7/16)</span><span class="sxs-lookup"><span data-stu-id="0c615-119">1001 = -0.4375f (-7 / 16)</span></span>
-   <span data-ttu-id="0c615-120">1010 =-0.375 f (-6/16)</span><span class="sxs-lookup"><span data-stu-id="0c615-120">1010 = -0.375f (-6 / 16)</span></span>
-   <span data-ttu-id="0c615-121">1011 =-0.3125 f (-5/16)</span><span class="sxs-lookup"><span data-stu-id="0c615-121">1011 = -0.3125f (-5 / 16)</span></span>
-   <span data-ttu-id="0c615-122">1100 =-0,25 f (-4/16)</span><span class="sxs-lookup"><span data-stu-id="0c615-122">1100 = -0.25f (-4 / 16)</span></span>
-   <span data-ttu-id="0c615-123">1101 =-0.1875 f (-3/16)</span><span class="sxs-lookup"><span data-stu-id="0c615-123">1101 = -0.1875f (-3 / 16)</span></span>
-   <span data-ttu-id="0c615-124">1110 =-0,125 f (-2/16)</span><span class="sxs-lookup"><span data-stu-id="0c615-124">1110 = -0.125f (-2 / 16)</span></span>
-   <span data-ttu-id="0c615-125">1111 =-0.0625 f (-1/16)</span><span class="sxs-lookup"><span data-stu-id="0c615-125">1111 = -0.0625f (-1 / 16)</span></span>
-   <span data-ttu-id="0c615-126">0000 = 0.0 f (0/16)</span><span class="sxs-lookup"><span data-stu-id="0c615-126">0000 = 0.0f ( 0 / 16)</span></span>
-   <span data-ttu-id="0c615-127">0001 = 0.0625 f (1/16)</span><span class="sxs-lookup"><span data-stu-id="0c615-127">0001 = 0.0625f ( 1 / 16)</span></span>
-   <span data-ttu-id="0c615-128">0010 = 0,125 f (2/16)</span><span class="sxs-lookup"><span data-stu-id="0c615-128">0010 = 0.125f ( 2 / 16)</span></span>
-   <span data-ttu-id="0c615-129">0011 = 0.1875 f (3/16)</span><span class="sxs-lookup"><span data-stu-id="0c615-129">0011 = 0.1875f ( 3 / 16)</span></span>
-   <span data-ttu-id="0c615-130">0100 = 0,25 f (4/16)</span><span class="sxs-lookup"><span data-stu-id="0c615-130">0100 = 0.25f ( 4 / 16)</span></span>
-   <span data-ttu-id="0c615-131">0101 = 0.3125 f (5/16)</span><span class="sxs-lookup"><span data-stu-id="0c615-131">0101 = 0.3125f ( 5 / 16)</span></span>
-   <span data-ttu-id="0c615-132">0110 = 0.375 f (6/16)</span><span class="sxs-lookup"><span data-stu-id="0c615-132">0110 = 0.375f ( 6 / 16)</span></span>
-   <span data-ttu-id="0c615-133">0111 = 0.4375 f (7/16)</span><span class="sxs-lookup"><span data-stu-id="0c615-133">0111 = 0.4375f ( 7 / 16)</span></span>

> [!Note]  
> <span data-ttu-id="0c615-134">Les bords gauche et supérieur d’un pixel sont inclus dans le décalage ; Toutefois, les bords inférieur et droit ne sont pas inclus.</span><span class="sxs-lookup"><span data-stu-id="0c615-134">The left and top edges of a pixel are included in the offset; however, the bottom and right edges are not included.</span></span> <span data-ttu-id="0c615-135">Tous les autres bits dans l’entier 32 bits et les valeurs de décalage V sont ignorés.</span><span class="sxs-lookup"><span data-stu-id="0c615-135">All other bits in the 32-bit integer U and V offset values are ignored.</span></span>

 

<span data-ttu-id="0c615-136">Une implémentation peut prendre le décalage fourni par le nuanceur et obtenir une valeur à virgule fixe 32 bits complète (28,4), qui s’étend sur la plage valide, en effectuant le calcul suivant :</span><span class="sxs-lookup"><span data-stu-id="0c615-136">An implementation can take the offset provided by the shader and obtain a full 32-bit fixed point value (28.4), which spans the valid range, by performing the following calculation:</span></span>


```
iU = (iU<<28)>>28  // keep lowest 4 bits and sign extend, which yields [-8..7]
```



<span data-ttu-id="0c615-137">Si une implémentation doit mapper le décalage à un décalage à virgule flottante, elle effectue le calcul suivant :</span><span class="sxs-lookup"><span data-stu-id="0c615-137">If an implementation must map the offset to a floating-point offset, it performs the following calculation:</span></span>


```
fU = ((float)iU)/16
```



### <a name="minimum-shader-model"></a><span data-ttu-id="0c615-138">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="0c615-138">Minimum Shader Model</span></span>

<span data-ttu-id="0c615-139">Cette fonction est prise en charge dans les modèles de nuanceur suivants.</span><span class="sxs-lookup"><span data-stu-id="0c615-139">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="0c615-140">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="0c615-140">Shader Model</span></span>                                                                | <span data-ttu-id="0c615-141">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="0c615-141">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="0c615-142">[Nuancier modèle 5](d3d11-graphics-reference-sm5.md) et modèles de nuanceur supérieurs</span><span class="sxs-lookup"><span data-stu-id="0c615-142">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="0c615-143">Oui</span><span class="sxs-lookup"><span data-stu-id="0c615-143">yes</span></span>       |



 

<span data-ttu-id="0c615-144">Cette fonction est prise en charge dans les types de nuanceurs suivants :</span><span class="sxs-lookup"><span data-stu-id="0c615-144">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="0c615-145">Sommet</span><span class="sxs-lookup"><span data-stu-id="0c615-145">Vertex</span></span> | <span data-ttu-id="0c615-146">Forme</span><span class="sxs-lookup"><span data-stu-id="0c615-146">Hull</span></span> | <span data-ttu-id="0c615-147">Domain</span><span class="sxs-lookup"><span data-stu-id="0c615-147">Domain</span></span> | <span data-ttu-id="0c615-148">Géométrie</span><span class="sxs-lookup"><span data-stu-id="0c615-148">Geometry</span></span> | <span data-ttu-id="0c615-149">Pixel</span><span class="sxs-lookup"><span data-stu-id="0c615-149">Pixel</span></span> | <span data-ttu-id="0c615-150">Compute</span><span class="sxs-lookup"><span data-stu-id="0c615-150">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="0c615-151">x</span><span class="sxs-lookup"><span data-stu-id="0c615-151">x</span></span>     |         |



 

## <a name="see-also"></a><span data-ttu-id="0c615-152">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0c615-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0c615-153">Fonctions intrinsèques</span><span class="sxs-lookup"><span data-stu-id="0c615-153">Intrinsic Functions</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[<span data-ttu-id="0c615-154">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="0c615-154">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




