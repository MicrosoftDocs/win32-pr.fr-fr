---
title: Format BC6H
description: Le format BC6H est un format de compression de texture conçu pour prendre en charge les espaces de couleurs HDR (large-Dynamic Range) dans les données sources.
ms.assetid: D6A1A729-5023-4A94-A8DB-5954D453E136
keywords:
- BC6H
- DXGI_FORMAT_BC6H
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ed4b934df742a4d2c99e20b52b7172b64e598dc
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104031597"
---
# <a name="bc6h-format"></a><span data-ttu-id="189c9-105">Format BC6H</span><span class="sxs-lookup"><span data-stu-id="189c9-105">BC6H Format</span></span>

<span data-ttu-id="189c9-106">Le format BC6H est un format de compression de texture conçu pour prendre en charge les espaces de couleurs HDR (large-Dynamic Range) dans les données sources.</span><span class="sxs-lookup"><span data-stu-id="189c9-106">The BC6H format is a texture compression format designed to support high-dynamic range (HDR) color spaces in source data.</span></span>

-   [<span data-ttu-id="189c9-107">À propos du format BC6H/DXGI \_ \_ BC6H</span><span class="sxs-lookup"><span data-stu-id="189c9-107">About BC6H/DXGI\_FORMAT\_BC6H</span></span>](/windows)
-   [<span data-ttu-id="189c9-108">Implémentation de BC6H</span><span class="sxs-lookup"><span data-stu-id="189c9-108">BC6H Implementation</span></span>](#bc6h-implementation)
-   [<span data-ttu-id="189c9-109">Décodage du format BC6H</span><span class="sxs-lookup"><span data-stu-id="189c9-109">Decoding the BC6H Format</span></span>](#decoding-the-bc6h-format)
-   [<span data-ttu-id="189c9-110">Format de point de terminaison compressé BC6H</span><span class="sxs-lookup"><span data-stu-id="189c9-110">BC6H Compressed Endpoint Format</span></span>](#bc6h-compressed-endpoint-format)
-   [<span data-ttu-id="189c9-111">Extension de signe pour les valeurs de point de terminaison</span><span class="sxs-lookup"><span data-stu-id="189c9-111">Sign Extension for Endpoint Values</span></span>](#sign-extension-for-endpoint-values)
-   [<span data-ttu-id="189c9-112">Transformer inversion pour les valeurs de point de terminaison</span><span class="sxs-lookup"><span data-stu-id="189c9-112">Transform Inversion for Endpoint Values</span></span>](#transform-inversion-for-endpoint-values)
-   [<span data-ttu-id="189c9-113">DÉQUANTIFICATION des points de terminaison de couleur</span><span class="sxs-lookup"><span data-stu-id="189c9-113">Unquantization of Color Endpoints</span></span>](#unquantization-of-color-endpoints)
-   [<span data-ttu-id="189c9-114">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="189c9-114">Related topics</span></span>](#related-topics)

## <a name="about-bc6hdxgi_format_bc6h"></a><span data-ttu-id="189c9-115">À propos du format BC6H/DXGI \_ \_ BC6H</span><span class="sxs-lookup"><span data-stu-id="189c9-115">About BC6H/DXGI\_FORMAT\_BC6H</span></span>

<span data-ttu-id="189c9-116">Le format BC6H fournit une compression de haute qualité pour les images qui utilisent trois canaux de couleur HDR, avec une valeur de 16 bits pour chaque canal de couleur de la valeur (16:16:16).</span><span class="sxs-lookup"><span data-stu-id="189c9-116">The BC6H format provides high-quality compression for images that use three HDR color channels, with a 16-bit value for each color channel of the value (16:16:16).</span></span> <span data-ttu-id="189c9-117">Il n’existe pas de prise en charge d’un canal alpha.</span><span class="sxs-lookup"><span data-stu-id="189c9-117">There is no support for an alpha channel.</span></span>

<span data-ttu-id="189c9-118">BC6H est spécifié par les valeurs d' \_ énumération de format dxgi suivantes :</span><span class="sxs-lookup"><span data-stu-id="189c9-118">BC6H is specified by the following DXGI\_FORMAT enumeration values:</span></span>

-   <span data-ttu-id="189c9-119">**Dxgi \_ FORMAT \_ BC6H non \_ typé**.</span><span class="sxs-lookup"><span data-stu-id="189c9-119">**DXGI\_FORMAT\_BC6H\_TYPELESS**.</span></span>
-   <span data-ttu-id="189c9-120">**Dxgi \_ FORMAT \_ BC6H \_ UF16**.</span><span class="sxs-lookup"><span data-stu-id="189c9-120">**DXGI\_FORMAT\_BC6H\_UF16**.</span></span> <span data-ttu-id="189c9-121">Ce format BC6H n’utilise pas de bit de signe dans les valeurs de canaux de couleurs à virgule flottante 16 bits.</span><span class="sxs-lookup"><span data-stu-id="189c9-121">This BC6H format does not use a sign bit in the 16-bit floating point color channel values.</span></span>
-   <span data-ttu-id="189c9-122">**Dxgi \_ FORMAT \_ BC6H \_ SF16**. Ce format BC6H utilise un bit de signe dans les valeurs de canaux de couleurs à virgule flottante 16 bits.</span><span class="sxs-lookup"><span data-stu-id="189c9-122">**DXGI\_FORMAT\_BC6H\_SF16**.This BC6H format uses a sign bit in the 16-bit floating point color channel values.</span></span>

> [!Note]  
> <span data-ttu-id="189c9-123">Le format à virgule flottante de 16 bits pour les canaux de couleur est souvent appelé format à virgule flottante « demi-point ».</span><span class="sxs-lookup"><span data-stu-id="189c9-123">The 16 bit floating point format for color channels is often referred to as a "half" floating point format.</span></span> <span data-ttu-id="189c9-124">Ce format utilise la disposition en bits suivante :</span><span class="sxs-lookup"><span data-stu-id="189c9-124">This format has the following bit layout:</span></span>
>
> |                       |                                                 |
> |-----------------------|-------------------------------------------------|
> | <span data-ttu-id="189c9-125">UF16 (unsigned float)</span><span class="sxs-lookup"><span data-stu-id="189c9-125">UF16 (unsigned float)</span></span> | <span data-ttu-id="189c9-126">5 bits d’exposant + 11 bits de mantisse</span><span class="sxs-lookup"><span data-stu-id="189c9-126">5 exponent bits + 11 mantissa bits</span></span>              |
> | <span data-ttu-id="189c9-127">SF16 (float signé)</span><span class="sxs-lookup"><span data-stu-id="189c9-127">SF16 (signed float)</span></span>   | <span data-ttu-id="189c9-128">1 bit de signe + 5 bits d’exposant + 10 bits de mantisse</span><span class="sxs-lookup"><span data-stu-id="189c9-128">1 sign bit + 5 exponent bits + 10 mantissa bits</span></span> |
>
> 
>
>  

 

<span data-ttu-id="189c9-129">Le format BC6H peut être utilisé pour les ressources de texture [Texture2D](/windows/desktop/direct3d10/d3d10-graphics-reference-resource-structures) (y compris les tableaux), Texture3D ou TextureCube (y compris les tableaux).</span><span class="sxs-lookup"><span data-stu-id="189c9-129">The BC6H format can be used for [Texture2D](/windows/desktop/direct3d10/d3d10-graphics-reference-resource-structures) (including arrays), Texture3D, or TextureCube (including arrays) texture resources.</span></span> <span data-ttu-id="189c9-130">De même, ce format s’applique à toutes les surfaces de la carte MIP associées à ces ressources.</span><span class="sxs-lookup"><span data-stu-id="189c9-130">Similarly, this format applies to any MIP-map surfaces associated with these resources.</span></span>

<span data-ttu-id="189c9-131">BC6H utilise une taille de bloc fixe de 16 octets (128 bits) et une taille de vignette fixe de texels 4x4.</span><span class="sxs-lookup"><span data-stu-id="189c9-131">BC6H uses a fixed block size of 16 bytes (128 bits) and a fixed tile size of 4x4 texels.</span></span> <span data-ttu-id="189c9-132">Comme avec les formats BC précédents, les images de texture plus volumineuses que la taille de vignette prise en charge (4x4) sont compressées à l’aide de plusieurs blocs.</span><span class="sxs-lookup"><span data-stu-id="189c9-132">As with previous BC formats, texture images larger than the supported tile size (4x4) are compressed by using multiple blocks.</span></span> <span data-ttu-id="189c9-133">Cette identité d’adressage s’applique également aux images à trois dimensions, MIP-Maps, cubemaps et les tableaux de texture.</span><span class="sxs-lookup"><span data-stu-id="189c9-133">This addressing identity applies also to three-dimensional images, MIP-maps, cubemaps, and texture arrays.</span></span> <span data-ttu-id="189c9-134">Toutes les vignettes d’image doivent avoir le même format.</span><span class="sxs-lookup"><span data-stu-id="189c9-134">All image tiles must be of the same format.</span></span>

<span data-ttu-id="189c9-135">Voici quelques remarques importantes concernant le format BC6H :</span><span class="sxs-lookup"><span data-stu-id="189c9-135">Some important notes about the BC6H format:</span></span>

-   <span data-ttu-id="189c9-136">BC6H prend en charge la dénormalisation à virgule flottante, mais ne prend pas en charge INF (Infinity) et NaN (not a Number).</span><span class="sxs-lookup"><span data-stu-id="189c9-136">BC6H supports floating point denormalization, but does not support INF (infinity) and NaN (not a number).</span></span> <span data-ttu-id="189c9-137">L’exception est le mode signé de BC6H (DXGI \_ format \_ BC6H \_ SF16), qui prend en charge-INF (infini négatif).</span><span class="sxs-lookup"><span data-stu-id="189c9-137">The exception is the signed mode of BC6H (DXGI\_FORMAT\_BC6H\_SF16), which supports -INF (negative infinity).</span></span> <span data-ttu-id="189c9-138">Notez que cette prise en charge pour-INF est simplement un artefact du format lui-même et n’est pas spécifiquement pris en charge par les encodeurs pour ce format.</span><span class="sxs-lookup"><span data-stu-id="189c9-138">Note that this support for -INF is merely an artifact of the format itself, and is not specifically supported by encoders for this format.</span></span> <span data-ttu-id="189c9-139">En général, lorsque des encodeurs rencontrent des données d’entrée INF (positives ou négatives) ou NaN, ils doivent \\ convertir ces données en valeur de représentation non-INF autorisée maximale et mapper Nan à 0 avant la compression.</span><span class="sxs-lookup"><span data-stu-id="189c9-139">In general, when encoders encounter INF (positive or negative) or NaN input data, they should \\ convert that data to the maximum allowable non-INF representation value, and map NaN to 0 prior to compression.</span></span>
-   <span data-ttu-id="189c9-140">BC6H ne prend pas en charge un canal alpha.</span><span class="sxs-lookup"><span data-stu-id="189c9-140">BC6H does not support an alpha channel.</span></span>
-   <span data-ttu-id="189c9-141">Le décodeur BC6H effectue la décompression avant d’effectuer un filtrage de texture.</span><span class="sxs-lookup"><span data-stu-id="189c9-141">The BC6H decoder performs decompression before it performs texture filtering.</span></span>
-   <span data-ttu-id="189c9-142">La décompression BC6H doit être de bits correcte ; autrement dit, le matériel doit retourner des résultats qui sont identiques au décodeur décrit dans cette documentation.</span><span class="sxs-lookup"><span data-stu-id="189c9-142">BC6H decompression must be bit accurate; that is, the hardware must return results that are identical to the decoder described in this documentation.</span></span>

## <a name="bc6h-implementation"></a><span data-ttu-id="189c9-143">Implémentation de BC6H</span><span class="sxs-lookup"><span data-stu-id="189c9-143">BC6H Implementation</span></span>

<span data-ttu-id="189c9-144">Un bloc BC6H comprend des bits de mode, des points de terminaison compressés, des index compressés et un index de partition facultatif.</span><span class="sxs-lookup"><span data-stu-id="189c9-144">A BC6H block consists of mode bits, compressed endpoints, compressed indices, and an optional partition index.</span></span> <span data-ttu-id="189c9-145">Ce format spécifie 14 modes différents.</span><span class="sxs-lookup"><span data-stu-id="189c9-145">This format specifies 14 different modes.</span></span>

<span data-ttu-id="189c9-146">Une couleur de point de terminaison est stockée sous la forme d’un triplet RVB.</span><span class="sxs-lookup"><span data-stu-id="189c9-146">An endpoint color is stored as an RGB triplet.</span></span> <span data-ttu-id="189c9-147">BC6H définit une palette de couleurs sur une ligne approximative sur un certain nombre de points de terminaison de couleur définis.</span><span class="sxs-lookup"><span data-stu-id="189c9-147">BC6H defines a palette of colors on an approximate line across a number of defined color endpoints.</span></span> <span data-ttu-id="189c9-148">En outre, selon le mode, une vignette peut être divisée en deux régions ou traitée comme une seule région, où une vignette à deux régions a un ensemble distinct de points de terminaison de couleur pour chaque région.</span><span class="sxs-lookup"><span data-stu-id="189c9-148">Also, depending on the mode, a tile can be divided into two regions or treated as a single region, where a two-region tile has a separate set of color endpoints for each region.</span></span> <span data-ttu-id="189c9-149">BC6H stocke un index de palette par Texel.</span><span class="sxs-lookup"><span data-stu-id="189c9-149">BC6H stores one palette index per texel.</span></span>

<span data-ttu-id="189c9-150">Dans le cas de deux régions, il existe 32 partitions possibles.</span><span class="sxs-lookup"><span data-stu-id="189c9-150">In the two-region case, there are 32 possible partitions.</span></span>

## <a name="decoding-the-bc6h-format"></a><span data-ttu-id="189c9-151">Décodage du format BC6H</span><span class="sxs-lookup"><span data-stu-id="189c9-151">Decoding the BC6H Format</span></span>

<span data-ttu-id="189c9-152">Le pseudo-code ci-dessous montre les étapes à suivre pour décompresser le pixel à (x, y) en fonction du bloc BC6H de 16 octets.</span><span class="sxs-lookup"><span data-stu-id="189c9-152">The pseudocode below shows the steps to decompress the pixel at (x,y) given the 16 byte BC6H block.</span></span>

``` syntax
decompress_bc6h(x, y, block)
{
    mode = extract_mode(block);
    endpoints;
    index;
    
    if(mode.type == ONE)
    {
        endpoints = extract_compressed_endpoints(mode, block);
        index = extract_index_ONE(x, y, block);
    }
    else //mode.type == TWO
    {
        partition = extract_partition(block);
        region = get_region(partition, x, y);
        endpoints = extract_compressed_endpoints(mode, region, block);
        index = extract_index_TWO(x, y, partition, block);
    }
    
    unquantize(endpoints);
    color = interpolate(index, endpoints);
    finish_unquantize(color);
}
```

<span data-ttu-id="189c9-153">Le tableau suivant contient le nombre de bits et les valeurs pour chacun des 14 formats possibles pour les blocs BC6H.</span><span class="sxs-lookup"><span data-stu-id="189c9-153">The following table contains the bit count and values for each of the 14 possible formats for BC6H blocks.</span></span> 

| <span data-ttu-id="189c9-154">Mode</span><span class="sxs-lookup"><span data-stu-id="189c9-154">Mode</span></span> | <span data-ttu-id="189c9-155">Index de partition</span><span class="sxs-lookup"><span data-stu-id="189c9-155">Partition Indices</span></span> | <span data-ttu-id="189c9-156">Partition</span><span class="sxs-lookup"><span data-stu-id="189c9-156">Partition</span></span> | <span data-ttu-id="189c9-157">Points de terminaison de couleur</span><span class="sxs-lookup"><span data-stu-id="189c9-157">Color Endpoints</span></span>                  | <span data-ttu-id="189c9-158">Bits de mode</span><span class="sxs-lookup"><span data-stu-id="189c9-158">Mode Bits</span></span>      |
|------|-------------------|-----------|----------------------------------|----------------|
| <span data-ttu-id="189c9-159">1</span><span class="sxs-lookup"><span data-stu-id="189c9-159">1</span></span>    | <span data-ttu-id="189c9-160">46 bits</span><span class="sxs-lookup"><span data-stu-id="189c9-160">46 bits</span></span>           | <span data-ttu-id="189c9-161">5 bits</span><span class="sxs-lookup"><span data-stu-id="189c9-161">5 bits</span></span>    | <span data-ttu-id="189c9-162">75 bits (10,555, 10,555, 10,555)</span><span class="sxs-lookup"><span data-stu-id="189c9-162">75 bits (10.555, 10.555, 10.555)</span></span> | <span data-ttu-id="189c9-163">2 bits (00)</span><span class="sxs-lookup"><span data-stu-id="189c9-163">2 bits (00)</span></span>    |
| <span data-ttu-id="189c9-164">2</span><span class="sxs-lookup"><span data-stu-id="189c9-164">2</span></span>    | <span data-ttu-id="189c9-165">46 bits</span><span class="sxs-lookup"><span data-stu-id="189c9-165">46 bits</span></span>           | <span data-ttu-id="189c9-166">5 bits</span><span class="sxs-lookup"><span data-stu-id="189c9-166">5 bits</span></span>    | <span data-ttu-id="189c9-167">75 bits (7666, 7666, 7666)</span><span class="sxs-lookup"><span data-stu-id="189c9-167">75 bits (7666, 7666, 7666)</span></span>       | <span data-ttu-id="189c9-168">2 bits (01)</span><span class="sxs-lookup"><span data-stu-id="189c9-168">2 bits (01)</span></span>    |
| <span data-ttu-id="189c9-169">3</span><span class="sxs-lookup"><span data-stu-id="189c9-169">3</span></span>    | <span data-ttu-id="189c9-170">46 bits</span><span class="sxs-lookup"><span data-stu-id="189c9-170">46 bits</span></span>           | <span data-ttu-id="189c9-171">5 bits</span><span class="sxs-lookup"><span data-stu-id="189c9-171">5 bits</span></span>    | <span data-ttu-id="189c9-172">72 bits (11,555, 11,444, 11,444)</span><span class="sxs-lookup"><span data-stu-id="189c9-172">72 bits (11.555, 11.444, 11.444)</span></span> | <span data-ttu-id="189c9-173">5 bits (00010)</span><span class="sxs-lookup"><span data-stu-id="189c9-173">5 bits (00010)</span></span> |
| <span data-ttu-id="189c9-174">4</span><span class="sxs-lookup"><span data-stu-id="189c9-174">4</span></span>    | <span data-ttu-id="189c9-175">46 bits</span><span class="sxs-lookup"><span data-stu-id="189c9-175">46 bits</span></span>           | <span data-ttu-id="189c9-176">5 bits</span><span class="sxs-lookup"><span data-stu-id="189c9-176">5 bits</span></span>    | <span data-ttu-id="189c9-177">72 bits (11,444, 11,555, 11,444)</span><span class="sxs-lookup"><span data-stu-id="189c9-177">72 bits (11.444, 11.555, 11.444)</span></span> | <span data-ttu-id="189c9-178">5 bits (00110)</span><span class="sxs-lookup"><span data-stu-id="189c9-178">5 bits (00110)</span></span> |
| <span data-ttu-id="189c9-179">5</span><span class="sxs-lookup"><span data-stu-id="189c9-179">5</span></span>    | <span data-ttu-id="189c9-180">46 bits</span><span class="sxs-lookup"><span data-stu-id="189c9-180">46 bits</span></span>           | <span data-ttu-id="189c9-181">5 bits</span><span class="sxs-lookup"><span data-stu-id="189c9-181">5 bits</span></span>    | <span data-ttu-id="189c9-182">72 bits (11,444, 11,444, 11,555)</span><span class="sxs-lookup"><span data-stu-id="189c9-182">72 bits (11.444, 11.444, 11.555)</span></span> | <span data-ttu-id="189c9-183">5 bits (01010)</span><span class="sxs-lookup"><span data-stu-id="189c9-183">5 bits (01010)</span></span> |
| <span data-ttu-id="189c9-184">6</span><span class="sxs-lookup"><span data-stu-id="189c9-184">6</span></span>    | <span data-ttu-id="189c9-185">46 bits</span><span class="sxs-lookup"><span data-stu-id="189c9-185">46 bits</span></span>           | <span data-ttu-id="189c9-186">5 bits</span><span class="sxs-lookup"><span data-stu-id="189c9-186">5 bits</span></span>    | <span data-ttu-id="189c9-187">72 bits (9555, 9555, 9555)</span><span class="sxs-lookup"><span data-stu-id="189c9-187">72 bits (9555, 9555, 9555)</span></span>       | <span data-ttu-id="189c9-188">5 bits (01110)</span><span class="sxs-lookup"><span data-stu-id="189c9-188">5 bits (01110)</span></span> |
| <span data-ttu-id="189c9-189">7</span><span class="sxs-lookup"><span data-stu-id="189c9-189">7</span></span>    | <span data-ttu-id="189c9-190">46 bits</span><span class="sxs-lookup"><span data-stu-id="189c9-190">46 bits</span></span>           | <span data-ttu-id="189c9-191">5 bits</span><span class="sxs-lookup"><span data-stu-id="189c9-191">5 bits</span></span>    | <span data-ttu-id="189c9-192">72 bits (8666, 8555, 8555)</span><span class="sxs-lookup"><span data-stu-id="189c9-192">72 bits (8666, 8555, 8555)</span></span>       | <span data-ttu-id="189c9-193">5 bits (10010)</span><span class="sxs-lookup"><span data-stu-id="189c9-193">5 bits (10010)</span></span> |
| <span data-ttu-id="189c9-194">8</span><span class="sxs-lookup"><span data-stu-id="189c9-194">8</span></span>    | <span data-ttu-id="189c9-195">46 bits</span><span class="sxs-lookup"><span data-stu-id="189c9-195">46 bits</span></span>           | <span data-ttu-id="189c9-196">5 bits</span><span class="sxs-lookup"><span data-stu-id="189c9-196">5 bits</span></span>    | <span data-ttu-id="189c9-197">72 bits (8555, 8666, 8555)</span><span class="sxs-lookup"><span data-stu-id="189c9-197">72 bits (8555, 8666, 8555)</span></span>       | <span data-ttu-id="189c9-198">5 bits (10110)</span><span class="sxs-lookup"><span data-stu-id="189c9-198">5 bits (10110)</span></span> |
| <span data-ttu-id="189c9-199">9</span><span class="sxs-lookup"><span data-stu-id="189c9-199">9</span></span>    | <span data-ttu-id="189c9-200">46 bits</span><span class="sxs-lookup"><span data-stu-id="189c9-200">46 bits</span></span>           | <span data-ttu-id="189c9-201">5 bits</span><span class="sxs-lookup"><span data-stu-id="189c9-201">5 bits</span></span>    | <span data-ttu-id="189c9-202">72 bits (8555, 8555, 8666)</span><span class="sxs-lookup"><span data-stu-id="189c9-202">72 bits (8555, 8555, 8666)</span></span>       | <span data-ttu-id="189c9-203">5 bits (11010)</span><span class="sxs-lookup"><span data-stu-id="189c9-203">5 bits (11010)</span></span> |
| <span data-ttu-id="189c9-204">10</span><span class="sxs-lookup"><span data-stu-id="189c9-204">10</span></span>   | <span data-ttu-id="189c9-205">46 bits</span><span class="sxs-lookup"><span data-stu-id="189c9-205">46 bits</span></span>           | <span data-ttu-id="189c9-206">5 bits</span><span class="sxs-lookup"><span data-stu-id="189c9-206">5 bits</span></span>    | <span data-ttu-id="189c9-207">72 bits (6666, 6666, 6666)</span><span class="sxs-lookup"><span data-stu-id="189c9-207">72 bits (6666, 6666, 6666)</span></span>       | <span data-ttu-id="189c9-208">5 bits (11110)</span><span class="sxs-lookup"><span data-stu-id="189c9-208">5 bits (11110)</span></span> |
| <span data-ttu-id="189c9-209">11</span><span class="sxs-lookup"><span data-stu-id="189c9-209">11</span></span>   | <span data-ttu-id="189c9-210">63 bits</span><span class="sxs-lookup"><span data-stu-id="189c9-210">63 bits</span></span>           | <span data-ttu-id="189c9-211">0 bits</span><span class="sxs-lookup"><span data-stu-id="189c9-211">0 bits</span></span>    | <span data-ttu-id="189c9-212">60 bits (10,10, 10,10, 10,10)</span><span class="sxs-lookup"><span data-stu-id="189c9-212">60 bits (10.10, 10.10, 10.10)</span></span>    | <span data-ttu-id="189c9-213">5 bits (00011)</span><span class="sxs-lookup"><span data-stu-id="189c9-213">5 bits (00011)</span></span> |
| <span data-ttu-id="189c9-214">12</span><span class="sxs-lookup"><span data-stu-id="189c9-214">12</span></span>   | <span data-ttu-id="189c9-215">63 bits</span><span class="sxs-lookup"><span data-stu-id="189c9-215">63 bits</span></span>           | <span data-ttu-id="189c9-216">0 bits</span><span class="sxs-lookup"><span data-stu-id="189c9-216">0 bits</span></span>    | <span data-ttu-id="189c9-217">60 bits (11,9, 11,9, 11,9)</span><span class="sxs-lookup"><span data-stu-id="189c9-217">60 bits (11.9, 11.9, 11.9)</span></span>       | <span data-ttu-id="189c9-218">5 bits (00111)</span><span class="sxs-lookup"><span data-stu-id="189c9-218">5 bits (00111)</span></span> |
| <span data-ttu-id="189c9-219">13</span><span class="sxs-lookup"><span data-stu-id="189c9-219">13</span></span>   | <span data-ttu-id="189c9-220">63 bits</span><span class="sxs-lookup"><span data-stu-id="189c9-220">63 bits</span></span>           | <span data-ttu-id="189c9-221">0 bits</span><span class="sxs-lookup"><span data-stu-id="189c9-221">0 bits</span></span>    | <span data-ttu-id="189c9-222">60 bits (12,8, 12,8, 12,8)</span><span class="sxs-lookup"><span data-stu-id="189c9-222">60 bits (12.8, 12.8, 12.8)</span></span>       | <span data-ttu-id="189c9-223">5 bits (01011)</span><span class="sxs-lookup"><span data-stu-id="189c9-223">5 bits (01011)</span></span> |
| <span data-ttu-id="189c9-224">14</span><span class="sxs-lookup"><span data-stu-id="189c9-224">14</span></span>   | <span data-ttu-id="189c9-225">63 bits</span><span class="sxs-lookup"><span data-stu-id="189c9-225">63 bits</span></span>           | <span data-ttu-id="189c9-226">0 bits</span><span class="sxs-lookup"><span data-stu-id="189c9-226">0 bits</span></span>    | <span data-ttu-id="189c9-227">60 bits (16,4, 16,4, 16,4)</span><span class="sxs-lookup"><span data-stu-id="189c9-227">60 bits (16.4, 16.4, 16.4)</span></span>       | <span data-ttu-id="189c9-228">5 bits (01111)</span><span class="sxs-lookup"><span data-stu-id="189c9-228">5 bits (01111)</span></span> |



 

<span data-ttu-id="189c9-229">Chaque format de cette table peut être identifié de manière unique par les bits de mode.</span><span class="sxs-lookup"><span data-stu-id="189c9-229">Each format in this table can be uniquely identified by the mode bits.</span></span> <span data-ttu-id="189c9-230">Les dix premiers modes sont utilisés pour les vignettes de deux régions, et le champ de bits de mode peut avoir deux ou cinq bits de long.</span><span class="sxs-lookup"><span data-stu-id="189c9-230">The first ten modes are used for two-region tiles, and the mode bit field can be either two or five bits long.</span></span> <span data-ttu-id="189c9-231">Ces blocs comportent également des champs pour les points de terminaison de couleur compressés (72 ou 75 bits), la partition (5 bits) et les index de partition (46 bits).</span><span class="sxs-lookup"><span data-stu-id="189c9-231">These blocks also have fields for the compressed color endpoints (72 or 75 bits), the partition (5 bits), and the partition indices (46 bits).</span></span>

<span data-ttu-id="189c9-232">Pour les points de terminaison de couleur compressés, les valeurs du tableau précédent indiquent la précision des points de terminaison RVB stockés et le nombre de bits utilisés pour chaque valeur de couleur.</span><span class="sxs-lookup"><span data-stu-id="189c9-232">For the compressed color endpoints, the values in the preceding table note the precision of the stored RGB endpoints, and the number of bits used for each color value.</span></span> <span data-ttu-id="189c9-233">Par exemple, le mode 3 spécifie un niveau de précision de point de terminaison de couleur 11 et le nombre de bits utilisés pour stocker les valeurs Delta des points de terminaison transformés pour les couleurs rouge, bleu et vert (respectivement, 5, 4 et 4).</span><span class="sxs-lookup"><span data-stu-id="189c9-233">For example, mode 3 specifies a color endpoint precision level of 11, and the number of bits used to store the delta values of the transformed endpoints for the red, blue and green colors (5, 4, and 4 respectively).</span></span> <span data-ttu-id="189c9-234">Le mode 10 n’utilise pas la compression Delta et stocke à la place les quatre points de terminaison de couleur de manière explicite.</span><span class="sxs-lookup"><span data-stu-id="189c9-234">Mode 10 does not use delta compression, and instead stores all four color endpoints explicitly.</span></span>

<span data-ttu-id="189c9-235">Les quatre derniers modes de blocage sont utilisés pour les vignettes d’une région, où le champ de mode est de 5 bits.</span><span class="sxs-lookup"><span data-stu-id="189c9-235">The last four block modes are used for one-region tiles, where the mode field is 5 bits.</span></span> <span data-ttu-id="189c9-236">Ces blocs ont des champs pour les points de terminaison (60 bits) et les index compressés (63 bits).</span><span class="sxs-lookup"><span data-stu-id="189c9-236">These blocks have fields for the endpoints (60 bits) and the compressed indices (63 bits).</span></span> <span data-ttu-id="189c9-237">Le mode 11 (comme le mode 10) n’utilise pas la compression Delta et stocke à la place les deux points de terminaison de couleur de manière explicite.</span><span class="sxs-lookup"><span data-stu-id="189c9-237">Mode 11 (like Mode 10) does not use delta compression, and instead stores both color endpoints explicitly.</span></span>

<span data-ttu-id="189c9-238">Les modes 10011, 10111, 11011 et 11111 (non affichés) sont réservés.</span><span class="sxs-lookup"><span data-stu-id="189c9-238">Modes 10011, 10111, 11011, and 11111 (not shown) are reserved.</span></span> <span data-ttu-id="189c9-239">N’utilisez pas celles-ci dans votre encodeur.</span><span class="sxs-lookup"><span data-stu-id="189c9-239">Do not use these in your encoder.</span></span> <span data-ttu-id="189c9-240">Si le matériel reçoit des blocs avec l’un de ces modes spécifiés, le bloc décompressé résultant doit contenir uniquement des zéros dans tous les canaux, sauf pour le canal alpha.</span><span class="sxs-lookup"><span data-stu-id="189c9-240">If the hardware is passed blocks with one of these modes specified, the resulting decompressed block must contain all zeroes in all channels except for the alpha channel.</span></span>

<span data-ttu-id="189c9-241">Pour BC6H, le canal alpha doit toujours retourner 1,0 quel que soit le mode.</span><span class="sxs-lookup"><span data-stu-id="189c9-241">For BC6H, the alpha channel must always return 1.0 regardless of the mode.</span></span>

### <a name="bc6h-partition-set"></a><span data-ttu-id="189c9-242">Ensemble de partitions BC6H</span><span class="sxs-lookup"><span data-stu-id="189c9-242">BC6H Partition Set</span></span>

<span data-ttu-id="189c9-243">Il existe 32 jeux de partitions possibles pour une vignette de deux régions, qui sont définis dans le tableau ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="189c9-243">There are 32 possible partition sets for a two-region tile, and which are defined in the table below.</span></span> <span data-ttu-id="189c9-244">Chaque bloc 4x4 représente une forme unique.</span><span class="sxs-lookup"><span data-stu-id="189c9-244">Each 4x4 block represents a single shape.</span></span>

![Table des jeux de partitions bc6h](images/bc6h-partition-sets.png)

<span data-ttu-id="189c9-246">Dans ce tableau de jeux de partitions, l’entrée en gras et soulignée est l’emplacement de l’index de correction pour le sous-ensemble 1 (qui est spécifié avec un bit moins).</span><span class="sxs-lookup"><span data-stu-id="189c9-246">In this table of partition sets, the bolded and underlined entry is the location of the fix-up index for subset 1 (which is specified with one less bit).</span></span> <span data-ttu-id="189c9-247">L’index de correction pour le sous-ensemble 0 est toujours l’index 0, car le partitionnement est toujours organisé de telle sorte que l’index 0 soit toujours dans le sous-ensemble 0.</span><span class="sxs-lookup"><span data-stu-id="189c9-247">The fix-up index for subset 0 is always index 0, as the partitioning is always arranged such that index 0 is always in subset 0.</span></span> <span data-ttu-id="189c9-248">L’ordre des partitions va de l’angle supérieur gauche à l’angle inférieur droit, en les déplaçant de gauche à droite, puis de haut en bas.</span><span class="sxs-lookup"><span data-stu-id="189c9-248">Partition order goes from top-left to bottom-right, moving left to right and then top to bottom.</span></span>

## <a name="bc6h-compressed-endpoint-format"></a><span data-ttu-id="189c9-249">Format de point de terminaison compressé BC6H</span><span class="sxs-lookup"><span data-stu-id="189c9-249">BC6H Compressed Endpoint Format</span></span>

![champs de bits pour les formats de point de terminaison compressés bc6h](images/bc6h-headers-med.png)

<span data-ttu-id="189c9-251">Ce tableau montre les champs de bits des points de terminaison compressés en tant que fonction du format de point de terminaison, chaque colonne spécifiant un encodage et chaque ligne spécifiant un champ de bits.</span><span class="sxs-lookup"><span data-stu-id="189c9-251">This table shows the bit fields for the compressed endpoints as a function of the endpoint format, with each column specifying an encoding and each row specifying a bit field.</span></span> <span data-ttu-id="189c9-252">Cette approche utilise 82 bits pour les vignettes à deux régions et 65 bits pour les vignettes d’une région.</span><span class="sxs-lookup"><span data-stu-id="189c9-252">This approach takes up 82 bits for two-region tiles and 65 bits for one-region tiles.</span></span> <span data-ttu-id="189c9-253">Par exemple, les 5 premiers bits pour l’encodage d’une région \[ 16 4 \] ci-dessus (plus précisément la colonne la plus à droite) sont bits m \[ 4:0 \] , les 10 bits suivants sont bits RW \[ 9:0 \] , et ainsi de suite avec les 6 derniers bits contenant BW \[ 10:15 \] .</span><span class="sxs-lookup"><span data-stu-id="189c9-253">As an example, the first 5 bits for the one-region \[16 4\] encoding above (specifically the right-most column) are bits m\[4:0\], the next 10 bits are bits rw\[9:0\], and so on with the last 6 bits containing bw\[10:15\].</span></span>

<span data-ttu-id="189c9-254">Les noms de champs dans le tableau ci-dessus sont définis comme suit :</span><span class="sxs-lookup"><span data-stu-id="189c9-254">The field names in the table above are defined as follows:</span></span>

| <span data-ttu-id="189c9-255">Champ</span><span class="sxs-lookup"><span data-stu-id="189c9-255">Field</span></span> | <span data-ttu-id="189c9-256">Variable</span><span class="sxs-lookup"><span data-stu-id="189c9-256">Variable</span></span>          |
|-------|-------------------|
| <span data-ttu-id="189c9-257">m</span><span class="sxs-lookup"><span data-stu-id="189c9-257">m</span></span>     | <span data-ttu-id="189c9-258">mode</span><span class="sxs-lookup"><span data-stu-id="189c9-258">mode</span></span>              |
| <span data-ttu-id="189c9-259">d</span><span class="sxs-lookup"><span data-stu-id="189c9-259">d</span></span>     | <span data-ttu-id="189c9-260">index de forme</span><span class="sxs-lookup"><span data-stu-id="189c9-260">shape index</span></span>       |
| <span data-ttu-id="189c9-261">grave</span><span class="sxs-lookup"><span data-stu-id="189c9-261">rw</span></span>    | <span data-ttu-id="189c9-262">Endpt \[ 0 \] . \[0\]</span><span class="sxs-lookup"><span data-stu-id="189c9-262">endpt\[0\].A\[0\]</span></span> |
| <span data-ttu-id="189c9-263">RX</span><span class="sxs-lookup"><span data-stu-id="189c9-263">rx</span></span>    | <span data-ttu-id="189c9-264">Endpt \[ 0 \] . B \[ 0\]</span><span class="sxs-lookup"><span data-stu-id="189c9-264">endpt\[0\].B\[0\]</span></span> |
| <span data-ttu-id="189c9-265">quêtes</span><span class="sxs-lookup"><span data-stu-id="189c9-265">ry</span></span>    | <span data-ttu-id="189c9-266">Endpt \[ 1 \] . \[0\]</span><span class="sxs-lookup"><span data-stu-id="189c9-266">endpt\[1\].A\[0\]</span></span> |
| <span data-ttu-id="189c9-267">cm</span><span class="sxs-lookup"><span data-stu-id="189c9-267">rz</span></span>    | <span data-ttu-id="189c9-268">Endpt \[ 1 \] . B \[ 0\]</span><span class="sxs-lookup"><span data-stu-id="189c9-268">endpt\[1\].B\[0\]</span></span> |
| <span data-ttu-id="189c9-269">entrepôt</span><span class="sxs-lookup"><span data-stu-id="189c9-269">gw</span></span>    | <span data-ttu-id="189c9-270">Endpt \[ 0 \] . \[1\]</span><span class="sxs-lookup"><span data-stu-id="189c9-270">endpt\[0\].A\[1\]</span></span> |
| <span data-ttu-id="189c9-271">GX</span><span class="sxs-lookup"><span data-stu-id="189c9-271">gx</span></span>    | <span data-ttu-id="189c9-272">Endpt \[ 0 \] . B \[ 1\]</span><span class="sxs-lookup"><span data-stu-id="189c9-272">endpt\[0\].B\[1\]</span></span> |
| <span data-ttu-id="189c9-273">GY</span><span class="sxs-lookup"><span data-stu-id="189c9-273">gy</span></span>    | <span data-ttu-id="189c9-274">Endpt \[ 1 \] . \[1\]</span><span class="sxs-lookup"><span data-stu-id="189c9-274">endpt\[1\].A\[1\]</span></span> |
| <span data-ttu-id="189c9-275">gz</span><span class="sxs-lookup"><span data-stu-id="189c9-275">gz</span></span>    | <span data-ttu-id="189c9-276">Endpt \[ 1 \] . B \[ 1\]</span><span class="sxs-lookup"><span data-stu-id="189c9-276">endpt\[1\].B\[1\]</span></span> |
| <span data-ttu-id="189c9-277">p.c.</span><span class="sxs-lookup"><span data-stu-id="189c9-277">bw</span></span>    | <span data-ttu-id="189c9-278">Endpt \[ 0 \] . A \[ 2\]</span><span class="sxs-lookup"><span data-stu-id="189c9-278">endpt\[0\].A\[2\]</span></span> |
| <span data-ttu-id="189c9-279">BX</span><span class="sxs-lookup"><span data-stu-id="189c9-279">bx</span></span>    | <span data-ttu-id="189c9-280">Endpt \[ 0 \] . B \[ 2\]</span><span class="sxs-lookup"><span data-stu-id="189c9-280">endpt\[0\].B\[2\]</span></span> |
| <span data-ttu-id="189c9-281">by</span><span class="sxs-lookup"><span data-stu-id="189c9-281">by</span></span>    | <span data-ttu-id="189c9-282">Endpt \[ 1 \] . A \[ 2\]</span><span class="sxs-lookup"><span data-stu-id="189c9-282">endpt\[1\].A\[2\]</span></span> |
| <span data-ttu-id="189c9-283">Via</span><span class="sxs-lookup"><span data-stu-id="189c9-283">bz</span></span>    | <span data-ttu-id="189c9-284">Endpt \[ 1 \] . B \[ 2\]</span><span class="sxs-lookup"><span data-stu-id="189c9-284">endpt\[1\].B\[2\]</span></span> |



 

<span data-ttu-id="189c9-285">Endpt \[ i \] , où i est égal à 0 ou 1, fait référence respectivement au 0 ou au 1er ensemble de points de terminaison.</span><span class="sxs-lookup"><span data-stu-id="189c9-285">Endpt\[i\], where i is either 0 or 1, refers to the 0th or 1st set of endpoints respectively.</span></span>

## <a name="sign-extension-for-endpoint-values"></a><span data-ttu-id="189c9-286">Extension de signe pour les valeurs de point de terminaison</span><span class="sxs-lookup"><span data-stu-id="189c9-286">Sign Extension for Endpoint Values</span></span>

<span data-ttu-id="189c9-287">Pour les vignettes de deux régions, quatre valeurs de point de terminaison peuvent être étendues.</span><span class="sxs-lookup"><span data-stu-id="189c9-287">For two-region tiles, there are four endpoint values that can be sign extended.</span></span> <span data-ttu-id="189c9-288">Endpt \[ 0 \] . Un est signé uniquement si le format est un format signé ; les autres points de terminaison sont signés uniquement si le point de terminaison a été transformé ou si le format est un format signé.</span><span class="sxs-lookup"><span data-stu-id="189c9-288">Endpt\[0\].A is signed only if the format is a signed format; the other endpoints are signed only if the endpoint was transformed, or if the format is a signed format.</span></span> <span data-ttu-id="189c9-289">Le code ci-dessous illustre l’algorithme permettant d’étendre le signe des valeurs de point de terminaison à deux régions.</span><span class="sxs-lookup"><span data-stu-id="189c9-289">The code below demonstrates the algorithm for extending the sign of two-region endpoint values.</span></span>

``` syntax
static void sign_extend_two_region(Pattern &p, IntEndpts endpts[NREGIONS_TWO])
{
    for (int i=0; i<NCHANNELS; ++i)
    {
      if (BC6H::FORMAT == SIGNED_F16)
        endpts[0].A[i] = SIGN_EXTEND(endpts[0].A[i], p.chan[i].prec);
      if (p.transformed || BC6H::FORMAT == SIGNED_F16)
      {
        endpts[0].B[i] = SIGN_EXTEND(endpts[0].B[i], p.chan[i].delta[0]);
        endpts[1].A[i] = SIGN_EXTEND(endpts[1].A[i], p.chan[i].delta[1]);
        endpts[1].B[i] = SIGN_EXTEND(endpts[1].B[i], p.chan[i].delta[2]);
      }
    }
}
```

<span data-ttu-id="189c9-290">Pour les vignettes d’une région, le comportement est le même, uniquement avec Endpt \[ 1 \] supprimé.</span><span class="sxs-lookup"><span data-stu-id="189c9-290">For one-region tiles, the behavior is the same, only with endpt\[1\] removed.</span></span>

``` syntax
static void sign_extend_one_region(Pattern &p, IntEndpts endpts[NREGIONS_ONE])
{
    for (int i=0; i<NCHANNELS; ++i)
    {
    if (BC6H::FORMAT == SIGNED_F16)
        endpts[0].A[i] = SIGN_EXTEND(endpts[0].A[i], p.chan[i].prec);
    if (p.transformed || BC6H::FORMAT == SIGNED_F16) 
        endpts[0].B[i] = SIGN_EXTEND(endpts[0].B[i], p.chan[i].delta[0]);
    }
}
```

## <a name="transform-inversion-for-endpoint-values"></a><span data-ttu-id="189c9-291">Transformer inversion pour les valeurs de point de terminaison</span><span class="sxs-lookup"><span data-stu-id="189c9-291">Transform Inversion for Endpoint Values</span></span>

<span data-ttu-id="189c9-292">Pour les vignettes de deux régions, la transformation applique l’inverse de l’encodage de différence, en ajoutant la valeur de base à Endpt \[ 0 \] . À trois autres entrées pour un total de 9 opérations d’ajout.</span><span class="sxs-lookup"><span data-stu-id="189c9-292">For two-region tiles, the transform applies the inverse of the difference encoding, adding the base value at endpt\[0\].A to the three other entries for a total of 9 add operations.</span></span> <span data-ttu-id="189c9-293">Dans l’image ci-dessous, la valeur de base est représentée sous la forme « a0 » et a la précision à virgule flottante la plus élevée.</span><span class="sxs-lookup"><span data-stu-id="189c9-293">In the image below, the base value is represented as "A0" and has the highest floating point precision.</span></span> <span data-ttu-id="189c9-294">« A1 », « B0 » et « B1 » sont tous des deltas calculés à partir de la valeur d’ancrage, et ces valeurs Delta sont représentées par une précision inférieure.</span><span class="sxs-lookup"><span data-stu-id="189c9-294">"A1," "B0," and "B1" are all deltas calculated from the anchor value, and these delta values are represented with lower precision.</span></span> <span data-ttu-id="189c9-295">(A0 correspond à Endpt \[ 0 \] . A, B0 correspond à Endpt \[ 0 \] . B, a1 correspond à Endpt \[ 1 \] . A, et B1 correspond à Endpt \[ 1 \] . B.)</span><span class="sxs-lookup"><span data-stu-id="189c9-295">(A0 corresponds to endpt\[0\].A, B0 corresponds to endpt\[0\].B, A1 corresponds to endpt\[1\].A, and B1 corresponds to endpt\[1\].B.)</span></span>

![calcul des valeurs de point de terminaison d’inversion de transformation](images/bc6h-transform-inverse.png)

<span data-ttu-id="189c9-297">Pour les vignettes d’une région, il n’y a qu’un seul décalage Delta, et donc seulement 3 opérations d’ajout.</span><span class="sxs-lookup"><span data-stu-id="189c9-297">For one-region tiles there is only one delta offset, and therefore only 3 add operations.</span></span>

<span data-ttu-id="189c9-298">Le décompresseur doit s’assurer que les résultats de la transformation inverse ne dépassent pas la précision de Endpt \[ 0 \] . a.</span><span class="sxs-lookup"><span data-stu-id="189c9-298">The decompressor must ensure that that the results of the inverse transform will not overflow the precision of endpt\[0\].a.</span></span> <span data-ttu-id="189c9-299">Dans le cas d’un dépassement de capacité, les valeurs résultant de la transformation inverse doivent être encapsulées dans le même nombre de bits.</span><span class="sxs-lookup"><span data-stu-id="189c9-299">In the case of an overflow, the values resulting from the inverse transform must wrap within the same number of bits.</span></span> <span data-ttu-id="189c9-300">Si la précision de a0 est de « p » bits, l’algorithme de transformation est le suivant :</span><span class="sxs-lookup"><span data-stu-id="189c9-300">If the precision of A0 is "p" bits, then the transform algorithm is:</span></span>

`B0 = (B0 + A0) & ((1 << p) - 1)`

<span data-ttu-id="189c9-301">Pour les formats signés, les résultats du calcul Delta doivent également être étendus.</span><span class="sxs-lookup"><span data-stu-id="189c9-301">For signed formats, the results of the delta calculation must be sign extended as well.</span></span> <span data-ttu-id="189c9-302">Si l’opération d’extension de signe prend en compte l’extension des deux signes, où 0 est positif et 1 est négatif, l’extension de signe 0 s’occupe de la bride ci-dessus.</span><span class="sxs-lookup"><span data-stu-id="189c9-302">If the sign extension operation considers extending both signs, where 0 is positive and 1 is negative, then the sign extension of 0 takes care of the clamp above.</span></span> <span data-ttu-id="189c9-303">De même, après la bride ci-dessus, seule une valeur de 1 (négatif) doit être une extension de signe.</span><span class="sxs-lookup"><span data-stu-id="189c9-303">Equivalently, after the clamp above, only a value of 1 (negative) needs to be sign extended.</span></span>

## <a name="unquantization-of-color-endpoints"></a><span data-ttu-id="189c9-304">DÉQUANTIFICATION des points de terminaison de couleur</span><span class="sxs-lookup"><span data-stu-id="189c9-304">Unquantization of Color Endpoints</span></span>

<span data-ttu-id="189c9-305">Étant donné les points de terminaison non compressés, l’étape suivante consiste à effectuer une DÉQUANTIFICATION initiale des points de terminaison de couleur.</span><span class="sxs-lookup"><span data-stu-id="189c9-305">Given the uncompressed endpoints, the next step is to perform an initial unquantization of the color endpoints.</span></span> <span data-ttu-id="189c9-306">Cela implique trois étapes :</span><span class="sxs-lookup"><span data-stu-id="189c9-306">This involves three steps:</span></span>

-   <span data-ttu-id="189c9-307">Une non-quantification des palettes de couleurs</span><span class="sxs-lookup"><span data-stu-id="189c9-307">An unquantization of the color palettes</span></span>
-   <span data-ttu-id="189c9-308">Interpolation des palettes</span><span class="sxs-lookup"><span data-stu-id="189c9-308">Interpolation of the palettes</span></span>
-   <span data-ttu-id="189c9-309">Finalisation de la DÉQUANTIFICATION</span><span class="sxs-lookup"><span data-stu-id="189c9-309">Unquantization finalization</span></span>

<span data-ttu-id="189c9-310">En séparant le processus de DÉQUANTIFICATION en deux parties (la DÉQUANTIFICATION de la palette de couleurs avant l’interpolation et la DÉQUANTIFICATION finale après l’interpolation) réduit le nombre d’opérations de multiplication requises par rapport à un processus de DÉQUANTIFICATION complet avant l’interpolation de palette.</span><span class="sxs-lookup"><span data-stu-id="189c9-310">Separating the unquantization process into two parts (color palette unquantization before interpolation and final unquantization after interpolation) reduces the number of multiplication operations required when compared to a full unquantization process before palette interpolation.</span></span>

<span data-ttu-id="189c9-311">Le code ci-dessous illustre le processus de récupération des estimations des valeurs de couleur 16 bits d’origine, puis l’utilisation des valeurs de pondération fournies pour ajouter 6 valeurs de couleur supplémentaires à la palette.</span><span class="sxs-lookup"><span data-stu-id="189c9-311">The code below illustrates the process for retrieving estimates of the original 16-bit color values, and then using the supplied weight values to add 6 additional color values to the palette.</span></span> <span data-ttu-id="189c9-312">La même opération est effectuée sur chaque canal.</span><span class="sxs-lookup"><span data-stu-id="189c9-312">The same operation is performed on each channel.</span></span>

``` syntax
int aWeight3[] = {0, 9, 18, 27, 37, 46, 55, 64};
int aWeight4[] = {0, 4, 9, 13, 17, 21, 26, 30, 34, 38, 43, 47, 51, 55, 60, 64};

// c1, c2: endpoints of a component
void generate_palette_unquantized(UINT8 uNumIndices, int c1, int c2, int prec, UINT16 palette[NINDICES])
{
    int* aWeights;
    if(uNumIndices == 8)
        aWeights = aWeight3;
    else  // uNumIndices == 16
        aWeights = aWeight4;

    int a = unquantize(c1, prec); 
    int b = unquantize(c2, prec);

    // interpolate
    for(int i = 0; i < uNumIndices; ++i)
        palette[i] = finish_unquantize((a * (64 - aWeights[i]) + b * aWeights[i] + 32) >> 6);
}
```

<span data-ttu-id="189c9-313">L’exemple de code suivant illustre le processus d’interpolation, avec les observations suivantes :</span><span class="sxs-lookup"><span data-stu-id="189c9-313">The next code sample demonstrates the interpolation process, with the following observations:</span></span>

-   <span data-ttu-id="189c9-314">Étant donné que la plage complète des valeurs de couleur pour la fonction **unquantification** (ci-dessous) est comprise entre-32768 et 65535, l’interpolateur est implémenté à l’aide de l’arithmétique signée 17 bits.</span><span class="sxs-lookup"><span data-stu-id="189c9-314">Since the full range of color values for the **unquantize** function (below) are from -32768 to 65535, the interpolator is implemented using 17-bit signed arithmetic.</span></span>
-   <span data-ttu-id="189c9-315">Après l’interpolation, les valeurs sont passées à la fonction de non **\_ quantification** (décrite dans le troisième exemple de cette section), qui applique la mise à l’échelle finale.</span><span class="sxs-lookup"><span data-stu-id="189c9-315">After interpolation, the values are passed to the **finish\_unquantize** function (described in the third sample in this section), which applies the final scaling.</span></span>
-   <span data-ttu-id="189c9-316">Tous les décompresseurs de matériel sont requis pour retourner des résultats de bits précis avec ces fonctions.</span><span class="sxs-lookup"><span data-stu-id="189c9-316">All hardware decompressors are required to return bit-accurate results with these functions.</span></span>

``` syntax
int unquantize(int comp, int uBitsPerComp)
{
    int unq, s = 0;
    switch(BC6H::FORMAT)
    {
    case UNSIGNED_F16:
        if(uBitsPerComp >= 15)
            unq = comp;
        else if(comp == 0)
            unq = 0;
        else if(comp == ((1 << uBitsPerComp) - 1))
            unq = 0xFFFF;
        else
            unq = ((comp << 16) + 0x8000) >> uBitsPerComp;
        break;

    case SIGNED_F16:
        if(uBitsPerComp >= 16)
            unq = comp;
        else
        {
            if(comp < 0)
            {
                s = 1;
                comp = -comp;
            }

            if(comp == 0)
                unq = 0;
            else if(comp >= ((1 << (uBitsPerComp - 1)) - 1))
                unq = 0x7FFF;
            else
                unq = ((comp << 15) + 0x4000) >> (uBitsPerComp-1);

            if(s)
                unq = -unq;
        }
        break;
    }
    return unq;
}
```

<span data-ttu-id="189c9-317">**terminer la \_ désquantification** est appelé après l’interpolation de palette.</span><span class="sxs-lookup"><span data-stu-id="189c9-317">**finish\_unquantize** is called after palette interpolation.</span></span> <span data-ttu-id="189c9-318">La fonction **unquantificateur** reporte la mise à l’échelle de 31/32 pour Signed, 31/64 pour unsigned.</span><span class="sxs-lookup"><span data-stu-id="189c9-318">The **unquantize** function postpones the scaling by 31/32 for signed, 31/64 for unsigned.</span></span> <span data-ttu-id="189c9-319">Ce comportement est nécessaire pour récupérer la valeur finale dans une demi-plage valide (-0x7BFF ~ 0x7BFF) une fois l’interpolation de palette terminée afin de réduire le nombre de multiplications nécessaires.</span><span class="sxs-lookup"><span data-stu-id="189c9-319">This behavior is required to get the final value into valid half range(-0x7BFF ~ 0x7BFF) after the palette interpolation is completed in order to reduce the number of necessary multiplications.</span></span> <span data-ttu-id="189c9-320">**Terminer \_ unquantificateur** applique la mise à l’échelle finale et retourne une valeur **short non signée** qui est réinterprétée en **deux**.</span><span class="sxs-lookup"><span data-stu-id="189c9-320">**finish\_unquantize** applies the final scaling and returns an **unsigned short** value that gets reinterpreted into **half**.</span></span>

``` syntax
unsigned short finish_unquantize(int comp)
{
    if(BC6H::FORMAT == UNSIGNED_F16)
    {
        comp = (comp * 31) >> 6;                                         // scale the magnitude by 31/64
        return (unsigned short) comp;
    }
    else // (BC6H::FORMAT == SIGNED_F16)
    {
        comp = (comp < 0) ? -(((-comp) * 31) >> 5) : (comp * 31) >> 5;   // scale the magnitude by 31/32
        int s = 0;
        if(comp < 0)
        {
            s = 0x8000;
            comp = -comp;
        }
        return (unsigned short) (s | comp);
    }
}
```

## <a name="related-topics"></a><span data-ttu-id="189c9-321">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="189c9-321">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="189c9-322">Compression de bloc de texture dans Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="189c9-322">Texture Block Compression in Direct3D 11</span></span>](texture-block-compression-in-direct3d-11.md)
</dt> </dl>

 

 