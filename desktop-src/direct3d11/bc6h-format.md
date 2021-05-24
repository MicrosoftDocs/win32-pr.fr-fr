---
title: Format BC6H
description: Le format BC6H est un format de compression de texture conçu pour prendre en charge les espaces de couleurs HDR (large-Dynamic Range) dans les données sources.
ms.assetid: D6A1A729-5023-4A94-A8DB-5954D453E136
keywords:
- BC6H
- DXGI_FORMAT_BC6H
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 92ea15e0275bc478c0708ce08f531d8888a3c84d
ms.sourcegitcommit: ca37395fd832e798375e81142b97cffcffabf184
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/24/2021
ms.locfileid: "110335223"
---
# <a name="bc6h-format"></a><span data-ttu-id="49b18-105">Format BC6H</span><span class="sxs-lookup"><span data-stu-id="49b18-105">BC6H Format</span></span>

<span data-ttu-id="49b18-106">Le format BC6H est un format de compression de texture conçu pour prendre en charge les espaces de couleurs HDR (large-Dynamic Range) dans les données sources.</span><span class="sxs-lookup"><span data-stu-id="49b18-106">The BC6H format is a texture compression format designed to support high-dynamic range (HDR) color spaces in source data.</span></span>

-   [<span data-ttu-id="49b18-107">À propos du format BC6H/DXGI \_ \_ BC6H</span><span class="sxs-lookup"><span data-stu-id="49b18-107">About BC6H/DXGI\_FORMAT\_BC6H</span></span>](/windows)
-   [<span data-ttu-id="49b18-108">Implémentation de BC6H</span><span class="sxs-lookup"><span data-stu-id="49b18-108">BC6H Implementation</span></span>](#bc6h-implementation)
-   [<span data-ttu-id="49b18-109">Décodage du format BC6H</span><span class="sxs-lookup"><span data-stu-id="49b18-109">Decoding the BC6H Format</span></span>](#decoding-the-bc6h-format)
-   [<span data-ttu-id="49b18-110">Format de point de terminaison compressé BC6H</span><span class="sxs-lookup"><span data-stu-id="49b18-110">BC6H Compressed Endpoint Format</span></span>](#bc6h-compressed-endpoint-format)
-   [<span data-ttu-id="49b18-111">Extension de signe pour les valeurs de point de terminaison</span><span class="sxs-lookup"><span data-stu-id="49b18-111">Sign Extension for Endpoint Values</span></span>](#sign-extension-for-endpoint-values)
-   [<span data-ttu-id="49b18-112">Transformer inversion pour les valeurs de point de terminaison</span><span class="sxs-lookup"><span data-stu-id="49b18-112">Transform Inversion for Endpoint Values</span></span>](#transform-inversion-for-endpoint-values)
-   [<span data-ttu-id="49b18-113">DÉQUANTIFICATION des points de terminaison de couleur</span><span class="sxs-lookup"><span data-stu-id="49b18-113">Unquantization of Color Endpoints</span></span>](#unquantization-of-color-endpoints)
-   [<span data-ttu-id="49b18-114">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="49b18-114">Related topics</span></span>](#related-topics)

## <a name="about-bc6hdxgi_format_bc6h"></a><span data-ttu-id="49b18-115">À propos du format BC6H/DXGI \_ \_ BC6H</span><span class="sxs-lookup"><span data-stu-id="49b18-115">About BC6H/DXGI\_FORMAT\_BC6H</span></span>

<span data-ttu-id="49b18-116">Le format BC6H fournit une compression de haute qualité pour les images qui utilisent trois canaux de couleur HDR, avec une valeur de 16 bits pour chaque canal de couleur de la valeur (16:16:16).</span><span class="sxs-lookup"><span data-stu-id="49b18-116">The BC6H format provides high-quality compression for images that use three HDR color channels, with a 16-bit value for each color channel of the value (16:16:16).</span></span> <span data-ttu-id="49b18-117">Il n’existe pas de prise en charge d’un canal alpha.</span><span class="sxs-lookup"><span data-stu-id="49b18-117">There is no support for an alpha channel.</span></span>

<span data-ttu-id="49b18-118">BC6H est spécifié par les valeurs d' \_ énumération de format dxgi suivantes :</span><span class="sxs-lookup"><span data-stu-id="49b18-118">BC6H is specified by the following DXGI\_FORMAT enumeration values:</span></span>

-   <span data-ttu-id="49b18-119">**Dxgi \_ FORMAT \_ BC6H non \_ typé**.</span><span class="sxs-lookup"><span data-stu-id="49b18-119">**DXGI\_FORMAT\_BC6H\_TYPELESS**.</span></span>
-   <span data-ttu-id="49b18-120">**Dxgi \_ FORMAT \_ BC6H \_ UF16**.</span><span class="sxs-lookup"><span data-stu-id="49b18-120">**DXGI\_FORMAT\_BC6H\_UF16**.</span></span> <span data-ttu-id="49b18-121">Ce format BC6H n’utilise pas de bit de signe dans les valeurs de canaux de couleurs à virgule flottante 16 bits.</span><span class="sxs-lookup"><span data-stu-id="49b18-121">This BC6H format does not use a sign bit in the 16-bit floating point color channel values.</span></span>
-   <span data-ttu-id="49b18-122">**Dxgi \_ FORMAT \_ BC6H \_ SF16**. Ce format BC6H utilise un bit de signe dans les valeurs de canaux de couleurs à virgule flottante 16 bits.</span><span class="sxs-lookup"><span data-stu-id="49b18-122">**DXGI\_FORMAT\_BC6H\_SF16**.This BC6H format uses a sign bit in the 16-bit floating point color channel values.</span></span>

> [!Note]  
> <span data-ttu-id="49b18-123">Le format à virgule flottante de 16 bits pour les canaux de couleur est souvent appelé format à virgule flottante « demi-point ».</span><span class="sxs-lookup"><span data-stu-id="49b18-123">The 16 bit floating point format for color channels is often referred to as a "half" floating point format.</span></span> <span data-ttu-id="49b18-124">Ce format utilise la disposition en bits suivante :</span><span class="sxs-lookup"><span data-stu-id="49b18-124">This format has the following bit layout:</span></span>
>
> |  <span data-ttu-id="49b18-125">Format</span><span class="sxs-lookup"><span data-stu-id="49b18-125">Format</span></span>                     | <span data-ttu-id="49b18-126">Disposition des bits</span><span class="sxs-lookup"><span data-stu-id="49b18-126">Bit layout</span></span>                                                |
> |-----------------------|-------------------------------------------------|
> | <span data-ttu-id="49b18-127">UF16 (unsigned float)</span><span class="sxs-lookup"><span data-stu-id="49b18-127">UF16 (unsigned float)</span></span> | <span data-ttu-id="49b18-128">5 bits d’exposant + 11 bits de mantisse</span><span class="sxs-lookup"><span data-stu-id="49b18-128">5 exponent bits + 11 mantissa bits</span></span>              |
> | <span data-ttu-id="49b18-129">SF16 (float signé)</span><span class="sxs-lookup"><span data-stu-id="49b18-129">SF16 (signed float)</span></span>   | <span data-ttu-id="49b18-130">1 bit de signe + 5 bits d’exposant + 10 bits de mantisse</span><span class="sxs-lookup"><span data-stu-id="49b18-130">1 sign bit + 5 exponent bits + 10 mantissa bits</span></span> |
>
> 
>
>  

 

<span data-ttu-id="49b18-131">Le format BC6H peut être utilisé pour les ressources de texture [Texture2D](/windows/desktop/direct3d10/d3d10-graphics-reference-resource-structures) (y compris les tableaux), Texture3D ou TextureCube (y compris les tableaux).</span><span class="sxs-lookup"><span data-stu-id="49b18-131">The BC6H format can be used for [Texture2D](/windows/desktop/direct3d10/d3d10-graphics-reference-resource-structures) (including arrays), Texture3D, or TextureCube (including arrays) texture resources.</span></span> <span data-ttu-id="49b18-132">De même, ce format s’applique à toutes les surfaces de la carte MIP associées à ces ressources.</span><span class="sxs-lookup"><span data-stu-id="49b18-132">Similarly, this format applies to any MIP-map surfaces associated with these resources.</span></span>

<span data-ttu-id="49b18-133">BC6H utilise une taille de bloc fixe de 16 octets (128 bits) et une taille de vignette fixe de texels 4x4.</span><span class="sxs-lookup"><span data-stu-id="49b18-133">BC6H uses a fixed block size of 16 bytes (128 bits) and a fixed tile size of 4x4 texels.</span></span> <span data-ttu-id="49b18-134">Comme avec les formats BC précédents, les images de texture plus volumineuses que la taille de vignette prise en charge (4x4) sont compressées à l’aide de plusieurs blocs.</span><span class="sxs-lookup"><span data-stu-id="49b18-134">As with previous BC formats, texture images larger than the supported tile size (4x4) are compressed by using multiple blocks.</span></span> <span data-ttu-id="49b18-135">Cette identité d’adressage s’applique également aux images à trois dimensions, MIP-Maps, cubemaps et les tableaux de texture.</span><span class="sxs-lookup"><span data-stu-id="49b18-135">This addressing identity applies also to three-dimensional images, MIP-maps, cubemaps, and texture arrays.</span></span> <span data-ttu-id="49b18-136">Toutes les vignettes d’image doivent avoir le même format.</span><span class="sxs-lookup"><span data-stu-id="49b18-136">All image tiles must be of the same format.</span></span>

<span data-ttu-id="49b18-137">Voici quelques remarques importantes concernant le format BC6H :</span><span class="sxs-lookup"><span data-stu-id="49b18-137">Some important notes about the BC6H format:</span></span>

-   <span data-ttu-id="49b18-138">BC6H prend en charge la dénormalisation à virgule flottante, mais ne prend pas en charge INF (Infinity) et NaN (not a Number).</span><span class="sxs-lookup"><span data-stu-id="49b18-138">BC6H supports floating point denormalization, but does not support INF (infinity) and NaN (not a number).</span></span> <span data-ttu-id="49b18-139">L’exception est le mode signé de BC6H (DXGI \_ format \_ BC6H \_ SF16), qui prend en charge-INF (infini négatif).</span><span class="sxs-lookup"><span data-stu-id="49b18-139">The exception is the signed mode of BC6H (DXGI\_FORMAT\_BC6H\_SF16), which supports -INF (negative infinity).</span></span> <span data-ttu-id="49b18-140">Notez que cette prise en charge pour-INF est simplement un artefact du format lui-même et n’est pas spécifiquement pris en charge par les encodeurs pour ce format.</span><span class="sxs-lookup"><span data-stu-id="49b18-140">Note that this support for -INF is merely an artifact of the format itself, and is not specifically supported by encoders for this format.</span></span> <span data-ttu-id="49b18-141">En général, lorsque des encodeurs rencontrent des données d’entrée INF (positives ou négatives) ou NaN, ils doivent \\ convertir ces données en valeur de représentation non-INF autorisée maximale et mapper Nan à 0 avant la compression.</span><span class="sxs-lookup"><span data-stu-id="49b18-141">In general, when encoders encounter INF (positive or negative) or NaN input data, they should \\ convert that data to the maximum allowable non-INF representation value, and map NaN to 0 prior to compression.</span></span>
-   <span data-ttu-id="49b18-142">BC6H ne prend pas en charge un canal alpha.</span><span class="sxs-lookup"><span data-stu-id="49b18-142">BC6H does not support an alpha channel.</span></span>
-   <span data-ttu-id="49b18-143">Le décodeur BC6H effectue la décompression avant d’effectuer un filtrage de texture.</span><span class="sxs-lookup"><span data-stu-id="49b18-143">The BC6H decoder performs decompression before it performs texture filtering.</span></span>
-   <span data-ttu-id="49b18-144">La décompression BC6H doit être de bits correcte ; autrement dit, le matériel doit retourner des résultats qui sont identiques au décodeur décrit dans cette documentation.</span><span class="sxs-lookup"><span data-stu-id="49b18-144">BC6H decompression must be bit accurate; that is, the hardware must return results that are identical to the decoder described in this documentation.</span></span>

## <a name="bc6h-implementation"></a><span data-ttu-id="49b18-145">Implémentation de BC6H</span><span class="sxs-lookup"><span data-stu-id="49b18-145">BC6H Implementation</span></span>

<span data-ttu-id="49b18-146">Un bloc BC6H comprend des bits de mode, des points de terminaison compressés, des index compressés et un index de partition facultatif.</span><span class="sxs-lookup"><span data-stu-id="49b18-146">A BC6H block consists of mode bits, compressed endpoints, compressed indices, and an optional partition index.</span></span> <span data-ttu-id="49b18-147">Ce format spécifie 14 modes différents.</span><span class="sxs-lookup"><span data-stu-id="49b18-147">This format specifies 14 different modes.</span></span>

<span data-ttu-id="49b18-148">Une couleur de point de terminaison est stockée sous la forme d’un triplet RVB.</span><span class="sxs-lookup"><span data-stu-id="49b18-148">An endpoint color is stored as an RGB triplet.</span></span> <span data-ttu-id="49b18-149">BC6H définit une palette de couleurs sur une ligne approximative sur un certain nombre de points de terminaison de couleur définis.</span><span class="sxs-lookup"><span data-stu-id="49b18-149">BC6H defines a palette of colors on an approximate line across a number of defined color endpoints.</span></span> <span data-ttu-id="49b18-150">En outre, selon le mode, une vignette peut être divisée en deux régions ou traitée comme une seule région, où une vignette à deux régions a un ensemble distinct de points de terminaison de couleur pour chaque région.</span><span class="sxs-lookup"><span data-stu-id="49b18-150">Also, depending on the mode, a tile can be divided into two regions or treated as a single region, where a two-region tile has a separate set of color endpoints for each region.</span></span> <span data-ttu-id="49b18-151">BC6H stocke un index de palette par Texel.</span><span class="sxs-lookup"><span data-stu-id="49b18-151">BC6H stores one palette index per texel.</span></span>

<span data-ttu-id="49b18-152">Dans le cas de deux régions, il existe 32 partitions possibles.</span><span class="sxs-lookup"><span data-stu-id="49b18-152">In the two-region case, there are 32 possible partitions.</span></span>

## <a name="decoding-the-bc6h-format"></a><span data-ttu-id="49b18-153">Décodage du format BC6H</span><span class="sxs-lookup"><span data-stu-id="49b18-153">Decoding the BC6H Format</span></span>

<span data-ttu-id="49b18-154">Le pseudo-code ci-dessous montre les étapes à suivre pour décompresser le pixel à (x, y) en fonction du bloc BC6H de 16 octets.</span><span class="sxs-lookup"><span data-stu-id="49b18-154">The pseudocode below shows the steps to decompress the pixel at (x,y) given the 16 byte BC6H block.</span></span>

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

<span data-ttu-id="49b18-155">Le tableau suivant contient le nombre de bits et les valeurs pour chacun des 14 formats possibles pour les blocs BC6H.</span><span class="sxs-lookup"><span data-stu-id="49b18-155">The following table contains the bit count and values for each of the 14 possible formats for BC6H blocks.</span></span> 

| <span data-ttu-id="49b18-156">Mode</span><span class="sxs-lookup"><span data-stu-id="49b18-156">Mode</span></span> | <span data-ttu-id="49b18-157">Index de partition</span><span class="sxs-lookup"><span data-stu-id="49b18-157">Partition Indices</span></span> | <span data-ttu-id="49b18-158">Partition</span><span class="sxs-lookup"><span data-stu-id="49b18-158">Partition</span></span> | <span data-ttu-id="49b18-159">Points de terminaison de couleur</span><span class="sxs-lookup"><span data-stu-id="49b18-159">Color Endpoints</span></span>                  | <span data-ttu-id="49b18-160">Bits de mode</span><span class="sxs-lookup"><span data-stu-id="49b18-160">Mode Bits</span></span>      |
|------|-------------------|-----------|----------------------------------|----------------|
| <span data-ttu-id="49b18-161">1</span><span class="sxs-lookup"><span data-stu-id="49b18-161">1</span></span>    | <span data-ttu-id="49b18-162">46 bits</span><span class="sxs-lookup"><span data-stu-id="49b18-162">46 bits</span></span>           | <span data-ttu-id="49b18-163">5 bits</span><span class="sxs-lookup"><span data-stu-id="49b18-163">5 bits</span></span>    | <span data-ttu-id="49b18-164">75 bits (10,555, 10,555, 10,555)</span><span class="sxs-lookup"><span data-stu-id="49b18-164">75 bits (10.555, 10.555, 10.555)</span></span> | <span data-ttu-id="49b18-165">2 bits (00)</span><span class="sxs-lookup"><span data-stu-id="49b18-165">2 bits (00)</span></span>    |
| <span data-ttu-id="49b18-166">2</span><span class="sxs-lookup"><span data-stu-id="49b18-166">2</span></span>    | <span data-ttu-id="49b18-167">46 bits</span><span class="sxs-lookup"><span data-stu-id="49b18-167">46 bits</span></span>           | <span data-ttu-id="49b18-168">5 bits</span><span class="sxs-lookup"><span data-stu-id="49b18-168">5 bits</span></span>    | <span data-ttu-id="49b18-169">75 bits (7666, 7666, 7666)</span><span class="sxs-lookup"><span data-stu-id="49b18-169">75 bits (7666, 7666, 7666)</span></span>       | <span data-ttu-id="49b18-170">2 bits (01)</span><span class="sxs-lookup"><span data-stu-id="49b18-170">2 bits (01)</span></span>    |
| <span data-ttu-id="49b18-171">3</span><span class="sxs-lookup"><span data-stu-id="49b18-171">3</span></span>    | <span data-ttu-id="49b18-172">46 bits</span><span class="sxs-lookup"><span data-stu-id="49b18-172">46 bits</span></span>           | <span data-ttu-id="49b18-173">5 bits</span><span class="sxs-lookup"><span data-stu-id="49b18-173">5 bits</span></span>    | <span data-ttu-id="49b18-174">72 bits (11,555, 11,444, 11,444)</span><span class="sxs-lookup"><span data-stu-id="49b18-174">72 bits (11.555, 11.444, 11.444)</span></span> | <span data-ttu-id="49b18-175">5 bits (00010)</span><span class="sxs-lookup"><span data-stu-id="49b18-175">5 bits (00010)</span></span> |
| <span data-ttu-id="49b18-176">4</span><span class="sxs-lookup"><span data-stu-id="49b18-176">4</span></span>    | <span data-ttu-id="49b18-177">46 bits</span><span class="sxs-lookup"><span data-stu-id="49b18-177">46 bits</span></span>           | <span data-ttu-id="49b18-178">5 bits</span><span class="sxs-lookup"><span data-stu-id="49b18-178">5 bits</span></span>    | <span data-ttu-id="49b18-179">72 bits (11,444, 11,555, 11,444)</span><span class="sxs-lookup"><span data-stu-id="49b18-179">72 bits (11.444, 11.555, 11.444)</span></span> | <span data-ttu-id="49b18-180">5 bits (00110)</span><span class="sxs-lookup"><span data-stu-id="49b18-180">5 bits (00110)</span></span> |
| <span data-ttu-id="49b18-181">5</span><span class="sxs-lookup"><span data-stu-id="49b18-181">5</span></span>    | <span data-ttu-id="49b18-182">46 bits</span><span class="sxs-lookup"><span data-stu-id="49b18-182">46 bits</span></span>           | <span data-ttu-id="49b18-183">5 bits</span><span class="sxs-lookup"><span data-stu-id="49b18-183">5 bits</span></span>    | <span data-ttu-id="49b18-184">72 bits (11,444, 11,444, 11,555)</span><span class="sxs-lookup"><span data-stu-id="49b18-184">72 bits (11.444, 11.444, 11.555)</span></span> | <span data-ttu-id="49b18-185">5 bits (01010)</span><span class="sxs-lookup"><span data-stu-id="49b18-185">5 bits (01010)</span></span> |
| <span data-ttu-id="49b18-186">6</span><span class="sxs-lookup"><span data-stu-id="49b18-186">6</span></span>    | <span data-ttu-id="49b18-187">46 bits</span><span class="sxs-lookup"><span data-stu-id="49b18-187">46 bits</span></span>           | <span data-ttu-id="49b18-188">5 bits</span><span class="sxs-lookup"><span data-stu-id="49b18-188">5 bits</span></span>    | <span data-ttu-id="49b18-189">72 bits (9555, 9555, 9555)</span><span class="sxs-lookup"><span data-stu-id="49b18-189">72 bits (9555, 9555, 9555)</span></span>       | <span data-ttu-id="49b18-190">5 bits (01110)</span><span class="sxs-lookup"><span data-stu-id="49b18-190">5 bits (01110)</span></span> |
| <span data-ttu-id="49b18-191">7</span><span class="sxs-lookup"><span data-stu-id="49b18-191">7</span></span>    | <span data-ttu-id="49b18-192">46 bits</span><span class="sxs-lookup"><span data-stu-id="49b18-192">46 bits</span></span>           | <span data-ttu-id="49b18-193">5 bits</span><span class="sxs-lookup"><span data-stu-id="49b18-193">5 bits</span></span>    | <span data-ttu-id="49b18-194">72 bits (8666, 8555, 8555)</span><span class="sxs-lookup"><span data-stu-id="49b18-194">72 bits (8666, 8555, 8555)</span></span>       | <span data-ttu-id="49b18-195">5 bits (10010)</span><span class="sxs-lookup"><span data-stu-id="49b18-195">5 bits (10010)</span></span> |
| <span data-ttu-id="49b18-196">8</span><span class="sxs-lookup"><span data-stu-id="49b18-196">8</span></span>    | <span data-ttu-id="49b18-197">46 bits</span><span class="sxs-lookup"><span data-stu-id="49b18-197">46 bits</span></span>           | <span data-ttu-id="49b18-198">5 bits</span><span class="sxs-lookup"><span data-stu-id="49b18-198">5 bits</span></span>    | <span data-ttu-id="49b18-199">72 bits (8555, 8666, 8555)</span><span class="sxs-lookup"><span data-stu-id="49b18-199">72 bits (8555, 8666, 8555)</span></span>       | <span data-ttu-id="49b18-200">5 bits (10110)</span><span class="sxs-lookup"><span data-stu-id="49b18-200">5 bits (10110)</span></span> |
| <span data-ttu-id="49b18-201">9</span><span class="sxs-lookup"><span data-stu-id="49b18-201">9</span></span>    | <span data-ttu-id="49b18-202">46 bits</span><span class="sxs-lookup"><span data-stu-id="49b18-202">46 bits</span></span>           | <span data-ttu-id="49b18-203">5 bits</span><span class="sxs-lookup"><span data-stu-id="49b18-203">5 bits</span></span>    | <span data-ttu-id="49b18-204">72 bits (8555, 8555, 8666)</span><span class="sxs-lookup"><span data-stu-id="49b18-204">72 bits (8555, 8555, 8666)</span></span>       | <span data-ttu-id="49b18-205">5 bits (11010)</span><span class="sxs-lookup"><span data-stu-id="49b18-205">5 bits (11010)</span></span> |
| <span data-ttu-id="49b18-206">10</span><span class="sxs-lookup"><span data-stu-id="49b18-206">10</span></span>   | <span data-ttu-id="49b18-207">46 bits</span><span class="sxs-lookup"><span data-stu-id="49b18-207">46 bits</span></span>           | <span data-ttu-id="49b18-208">5 bits</span><span class="sxs-lookup"><span data-stu-id="49b18-208">5 bits</span></span>    | <span data-ttu-id="49b18-209">72 bits (6666, 6666, 6666)</span><span class="sxs-lookup"><span data-stu-id="49b18-209">72 bits (6666, 6666, 6666)</span></span>       | <span data-ttu-id="49b18-210">5 bits (11110)</span><span class="sxs-lookup"><span data-stu-id="49b18-210">5 bits (11110)</span></span> |
| <span data-ttu-id="49b18-211">11</span><span class="sxs-lookup"><span data-stu-id="49b18-211">11</span></span>   | <span data-ttu-id="49b18-212">63 bits</span><span class="sxs-lookup"><span data-stu-id="49b18-212">63 bits</span></span>           | <span data-ttu-id="49b18-213">0 bits</span><span class="sxs-lookup"><span data-stu-id="49b18-213">0 bits</span></span>    | <span data-ttu-id="49b18-214">60 bits (10,10, 10,10, 10,10)</span><span class="sxs-lookup"><span data-stu-id="49b18-214">60 bits (10.10, 10.10, 10.10)</span></span>    | <span data-ttu-id="49b18-215">5 bits (00011)</span><span class="sxs-lookup"><span data-stu-id="49b18-215">5 bits (00011)</span></span> |
| <span data-ttu-id="49b18-216">12</span><span class="sxs-lookup"><span data-stu-id="49b18-216">12</span></span>   | <span data-ttu-id="49b18-217">63 bits</span><span class="sxs-lookup"><span data-stu-id="49b18-217">63 bits</span></span>           | <span data-ttu-id="49b18-218">0 bits</span><span class="sxs-lookup"><span data-stu-id="49b18-218">0 bits</span></span>    | <span data-ttu-id="49b18-219">60 bits (11,9, 11,9, 11,9)</span><span class="sxs-lookup"><span data-stu-id="49b18-219">60 bits (11.9, 11.9, 11.9)</span></span>       | <span data-ttu-id="49b18-220">5 bits (00111)</span><span class="sxs-lookup"><span data-stu-id="49b18-220">5 bits (00111)</span></span> |
| <span data-ttu-id="49b18-221">13</span><span class="sxs-lookup"><span data-stu-id="49b18-221">13</span></span>   | <span data-ttu-id="49b18-222">63 bits</span><span class="sxs-lookup"><span data-stu-id="49b18-222">63 bits</span></span>           | <span data-ttu-id="49b18-223">0 bits</span><span class="sxs-lookup"><span data-stu-id="49b18-223">0 bits</span></span>    | <span data-ttu-id="49b18-224">60 bits (12,8, 12,8, 12,8)</span><span class="sxs-lookup"><span data-stu-id="49b18-224">60 bits (12.8, 12.8, 12.8)</span></span>       | <span data-ttu-id="49b18-225">5 bits (01011)</span><span class="sxs-lookup"><span data-stu-id="49b18-225">5 bits (01011)</span></span> |
| <span data-ttu-id="49b18-226">14</span><span class="sxs-lookup"><span data-stu-id="49b18-226">14</span></span>   | <span data-ttu-id="49b18-227">63 bits</span><span class="sxs-lookup"><span data-stu-id="49b18-227">63 bits</span></span>           | <span data-ttu-id="49b18-228">0 bits</span><span class="sxs-lookup"><span data-stu-id="49b18-228">0 bits</span></span>    | <span data-ttu-id="49b18-229">60 bits (16,4, 16,4, 16,4)</span><span class="sxs-lookup"><span data-stu-id="49b18-229">60 bits (16.4, 16.4, 16.4)</span></span>       | <span data-ttu-id="49b18-230">5 bits (01111)</span><span class="sxs-lookup"><span data-stu-id="49b18-230">5 bits (01111)</span></span> |



 

<span data-ttu-id="49b18-231">Chaque format de cette table peut être identifié de manière unique par les bits de mode.</span><span class="sxs-lookup"><span data-stu-id="49b18-231">Each format in this table can be uniquely identified by the mode bits.</span></span> <span data-ttu-id="49b18-232">Les dix premiers modes sont utilisés pour les vignettes de deux régions, et le champ de bits de mode peut avoir deux ou cinq bits de long.</span><span class="sxs-lookup"><span data-stu-id="49b18-232">The first ten modes are used for two-region tiles, and the mode bit field can be either two or five bits long.</span></span> <span data-ttu-id="49b18-233">Ces blocs comportent également des champs pour les points de terminaison de couleur compressés (72 ou 75 bits), la partition (5 bits) et les index de partition (46 bits).</span><span class="sxs-lookup"><span data-stu-id="49b18-233">These blocks also have fields for the compressed color endpoints (72 or 75 bits), the partition (5 bits), and the partition indices (46 bits).</span></span>

<span data-ttu-id="49b18-234">Pour les points de terminaison de couleur compressés, les valeurs du tableau précédent indiquent la précision des points de terminaison RVB stockés et le nombre de bits utilisés pour chaque valeur de couleur.</span><span class="sxs-lookup"><span data-stu-id="49b18-234">For the compressed color endpoints, the values in the preceding table note the precision of the stored RGB endpoints, and the number of bits used for each color value.</span></span> <span data-ttu-id="49b18-235">Par exemple, le mode 3 spécifie un niveau de précision de point de terminaison de couleur 11 et le nombre de bits utilisés pour stocker les valeurs Delta des points de terminaison transformés pour les couleurs rouge, bleu et vert (respectivement, 5, 4 et 4).</span><span class="sxs-lookup"><span data-stu-id="49b18-235">For example, mode 3 specifies a color endpoint precision level of 11, and the number of bits used to store the delta values of the transformed endpoints for the red, blue and green colors (5, 4, and 4 respectively).</span></span> <span data-ttu-id="49b18-236">Le mode 10 n’utilise pas la compression Delta et stocke à la place les quatre points de terminaison de couleur de manière explicite.</span><span class="sxs-lookup"><span data-stu-id="49b18-236">Mode 10 does not use delta compression, and instead stores all four color endpoints explicitly.</span></span>

<span data-ttu-id="49b18-237">Les quatre derniers modes de blocage sont utilisés pour les vignettes d’une région, où le champ de mode est de 5 bits.</span><span class="sxs-lookup"><span data-stu-id="49b18-237">The last four block modes are used for one-region tiles, where the mode field is 5 bits.</span></span> <span data-ttu-id="49b18-238">Ces blocs ont des champs pour les points de terminaison (60 bits) et les index compressés (63 bits).</span><span class="sxs-lookup"><span data-stu-id="49b18-238">These blocks have fields for the endpoints (60 bits) and the compressed indices (63 bits).</span></span> <span data-ttu-id="49b18-239">Le mode 11 (comme le mode 10) n’utilise pas la compression Delta et stocke à la place les deux points de terminaison de couleur de manière explicite.</span><span class="sxs-lookup"><span data-stu-id="49b18-239">Mode 11 (like Mode 10) does not use delta compression, and instead stores both color endpoints explicitly.</span></span>

<span data-ttu-id="49b18-240">Les modes 10011, 10111, 11011 et 11111 (non affichés) sont réservés.</span><span class="sxs-lookup"><span data-stu-id="49b18-240">Modes 10011, 10111, 11011, and 11111 (not shown) are reserved.</span></span> <span data-ttu-id="49b18-241">N’utilisez pas celles-ci dans votre encodeur.</span><span class="sxs-lookup"><span data-stu-id="49b18-241">Do not use these in your encoder.</span></span> <span data-ttu-id="49b18-242">Si le matériel reçoit des blocs avec l’un de ces modes spécifiés, le bloc décompressé résultant doit contenir uniquement des zéros dans tous les canaux, sauf pour le canal alpha.</span><span class="sxs-lookup"><span data-stu-id="49b18-242">If the hardware is passed blocks with one of these modes specified, the resulting decompressed block must contain all zeroes in all channels except for the alpha channel.</span></span>

<span data-ttu-id="49b18-243">Pour BC6H, le canal alpha doit toujours retourner 1,0 quel que soit le mode.</span><span class="sxs-lookup"><span data-stu-id="49b18-243">For BC6H, the alpha channel must always return 1.0 regardless of the mode.</span></span>

### <a name="bc6h-partition-set"></a><span data-ttu-id="49b18-244">Ensemble de partitions BC6H</span><span class="sxs-lookup"><span data-stu-id="49b18-244">BC6H Partition Set</span></span>

<span data-ttu-id="49b18-245">Il existe 32 jeux de partitions possibles pour une vignette de deux régions, qui sont définis dans le tableau ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="49b18-245">There are 32 possible partition sets for a two-region tile, and which are defined in the table below.</span></span> <span data-ttu-id="49b18-246">Chaque bloc 4x4 représente une forme unique.</span><span class="sxs-lookup"><span data-stu-id="49b18-246">Each 4x4 block represents a single shape.</span></span>

![Table des jeux de partitions bc6h](images/bc6h-partition-sets.png)

<span data-ttu-id="49b18-248">Dans ce tableau de jeux de partitions, l’entrée en gras et soulignée est l’emplacement de l’index de correction pour le sous-ensemble 1 (qui est spécifié avec un bit moins).</span><span class="sxs-lookup"><span data-stu-id="49b18-248">In this table of partition sets, the bolded and underlined entry is the location of the fix-up index for subset 1 (which is specified with one less bit).</span></span> <span data-ttu-id="49b18-249">L’index de correction pour le sous-ensemble 0 est toujours l’index 0, car le partitionnement est toujours organisé de telle sorte que l’index 0 soit toujours dans le sous-ensemble 0.</span><span class="sxs-lookup"><span data-stu-id="49b18-249">The fix-up index for subset 0 is always index 0, as the partitioning is always arranged such that index 0 is always in subset 0.</span></span> <span data-ttu-id="49b18-250">L’ordre des partitions va de l’angle supérieur gauche à l’angle inférieur droit, en les déplaçant de gauche à droite, puis de haut en bas.</span><span class="sxs-lookup"><span data-stu-id="49b18-250">Partition order goes from top-left to bottom-right, moving left to right and then top to bottom.</span></span>

## <a name="bc6h-compressed-endpoint-format"></a><span data-ttu-id="49b18-251">Format de point de terminaison compressé BC6H</span><span class="sxs-lookup"><span data-stu-id="49b18-251">BC6H Compressed Endpoint Format</span></span>

![champs de bits pour les formats de point de terminaison compressés bc6h](images/bc6h-headers-med.png)

<span data-ttu-id="49b18-253">Ce tableau montre les champs de bits des points de terminaison compressés en tant que fonction du format de point de terminaison, chaque colonne spécifiant un encodage et chaque ligne spécifiant un champ de bits.</span><span class="sxs-lookup"><span data-stu-id="49b18-253">This table shows the bit fields for the compressed endpoints as a function of the endpoint format, with each column specifying an encoding and each row specifying a bit field.</span></span> <span data-ttu-id="49b18-254">Cette approche utilise 82 bits pour les vignettes à deux régions et 65 bits pour les vignettes d’une région.</span><span class="sxs-lookup"><span data-stu-id="49b18-254">This approach takes up 82 bits for two-region tiles and 65 bits for one-region tiles.</span></span> <span data-ttu-id="49b18-255">Par exemple, les 5 premiers bits pour l’encodage d’une région \[ 16 4 \] ci-dessus (plus précisément la colonne la plus à droite) sont bits m \[ 4:0 \] , les 10 bits suivants sont bits RW \[ 9:0 \] , et ainsi de suite avec les 6 derniers bits contenant BW \[ 10:15 \] .</span><span class="sxs-lookup"><span data-stu-id="49b18-255">As an example, the first 5 bits for the one-region \[16 4\] encoding above (specifically the right-most column) are bits m\[4:0\], the next 10 bits are bits rw\[9:0\], and so on with the last 6 bits containing bw\[10:15\].</span></span>

<span data-ttu-id="49b18-256">Les noms de champs dans le tableau ci-dessus sont définis comme suit :</span><span class="sxs-lookup"><span data-stu-id="49b18-256">The field names in the table above are defined as follows:</span></span>

| <span data-ttu-id="49b18-257">Champ</span><span class="sxs-lookup"><span data-stu-id="49b18-257">Field</span></span> | <span data-ttu-id="49b18-258">Variable</span><span class="sxs-lookup"><span data-stu-id="49b18-258">Variable</span></span>          |
|-------|-------------------|
| <span data-ttu-id="49b18-259">m</span><span class="sxs-lookup"><span data-stu-id="49b18-259">m</span></span>     | <span data-ttu-id="49b18-260">mode</span><span class="sxs-lookup"><span data-stu-id="49b18-260">mode</span></span>              |
| <span data-ttu-id="49b18-261">d</span><span class="sxs-lookup"><span data-stu-id="49b18-261">d</span></span>     | <span data-ttu-id="49b18-262">index de forme</span><span class="sxs-lookup"><span data-stu-id="49b18-262">shape index</span></span>       |
| <span data-ttu-id="49b18-263">grave</span><span class="sxs-lookup"><span data-stu-id="49b18-263">rw</span></span>    | <span data-ttu-id="49b18-264">Endpt \[ 0 \] . \[0\]</span><span class="sxs-lookup"><span data-stu-id="49b18-264">endpt\[0\].A\[0\]</span></span> |
| <span data-ttu-id="49b18-265">RX</span><span class="sxs-lookup"><span data-stu-id="49b18-265">rx</span></span>    | <span data-ttu-id="49b18-266">Endpt \[ 0 \] . B \[ 0\]</span><span class="sxs-lookup"><span data-stu-id="49b18-266">endpt\[0\].B\[0\]</span></span> |
| <span data-ttu-id="49b18-267">quêtes</span><span class="sxs-lookup"><span data-stu-id="49b18-267">ry</span></span>    | <span data-ttu-id="49b18-268">Endpt \[ 1 \] . \[0\]</span><span class="sxs-lookup"><span data-stu-id="49b18-268">endpt\[1\].A\[0\]</span></span> |
| <span data-ttu-id="49b18-269">cm</span><span class="sxs-lookup"><span data-stu-id="49b18-269">rz</span></span>    | <span data-ttu-id="49b18-270">Endpt \[ 1 \] . B \[ 0\]</span><span class="sxs-lookup"><span data-stu-id="49b18-270">endpt\[1\].B\[0\]</span></span> |
| <span data-ttu-id="49b18-271">entrepôt</span><span class="sxs-lookup"><span data-stu-id="49b18-271">gw</span></span>    | <span data-ttu-id="49b18-272">Endpt \[ 0 \] . \[1\]</span><span class="sxs-lookup"><span data-stu-id="49b18-272">endpt\[0\].A\[1\]</span></span> |
| <span data-ttu-id="49b18-273">GX</span><span class="sxs-lookup"><span data-stu-id="49b18-273">gx</span></span>    | <span data-ttu-id="49b18-274">Endpt \[ 0 \] . B \[ 1\]</span><span class="sxs-lookup"><span data-stu-id="49b18-274">endpt\[0\].B\[1\]</span></span> |
| <span data-ttu-id="49b18-275">GY</span><span class="sxs-lookup"><span data-stu-id="49b18-275">gy</span></span>    | <span data-ttu-id="49b18-276">Endpt \[ 1 \] . \[1\]</span><span class="sxs-lookup"><span data-stu-id="49b18-276">endpt\[1\].A\[1\]</span></span> |
| <span data-ttu-id="49b18-277">gz</span><span class="sxs-lookup"><span data-stu-id="49b18-277">gz</span></span>    | <span data-ttu-id="49b18-278">Endpt \[ 1 \] . B \[ 1\]</span><span class="sxs-lookup"><span data-stu-id="49b18-278">endpt\[1\].B\[1\]</span></span> |
| <span data-ttu-id="49b18-279">p.c.</span><span class="sxs-lookup"><span data-stu-id="49b18-279">bw</span></span>    | <span data-ttu-id="49b18-280">Endpt \[ 0 \] . A \[ 2\]</span><span class="sxs-lookup"><span data-stu-id="49b18-280">endpt\[0\].A\[2\]</span></span> |
| <span data-ttu-id="49b18-281">BX</span><span class="sxs-lookup"><span data-stu-id="49b18-281">bx</span></span>    | <span data-ttu-id="49b18-282">Endpt \[ 0 \] . B \[ 2\]</span><span class="sxs-lookup"><span data-stu-id="49b18-282">endpt\[0\].B\[2\]</span></span> |
| <span data-ttu-id="49b18-283">by</span><span class="sxs-lookup"><span data-stu-id="49b18-283">by</span></span>    | <span data-ttu-id="49b18-284">Endpt \[ 1 \] . A \[ 2\]</span><span class="sxs-lookup"><span data-stu-id="49b18-284">endpt\[1\].A\[2\]</span></span> |
| <span data-ttu-id="49b18-285">Via</span><span class="sxs-lookup"><span data-stu-id="49b18-285">bz</span></span>    | <span data-ttu-id="49b18-286">Endpt \[ 1 \] . B \[ 2\]</span><span class="sxs-lookup"><span data-stu-id="49b18-286">endpt\[1\].B\[2\]</span></span> |



 

<span data-ttu-id="49b18-287">Endpt \[ i \] , où i est égal à 0 ou 1, fait référence respectivement au 0 ou au 1er ensemble de points de terminaison.</span><span class="sxs-lookup"><span data-stu-id="49b18-287">Endpt\[i\], where i is either 0 or 1, refers to the 0th or 1st set of endpoints respectively.</span></span>

## <a name="sign-extension-for-endpoint-values"></a><span data-ttu-id="49b18-288">Extension de signe pour les valeurs de point de terminaison</span><span class="sxs-lookup"><span data-stu-id="49b18-288">Sign Extension for Endpoint Values</span></span>

<span data-ttu-id="49b18-289">Pour les vignettes de deux régions, quatre valeurs de point de terminaison peuvent être étendues.</span><span class="sxs-lookup"><span data-stu-id="49b18-289">For two-region tiles, there are four endpoint values that can be sign extended.</span></span> <span data-ttu-id="49b18-290">Endpt \[ 0 \] . Un est signé uniquement si le format est un format signé ; les autres points de terminaison sont signés uniquement si le point de terminaison a été transformé ou si le format est un format signé.</span><span class="sxs-lookup"><span data-stu-id="49b18-290">Endpt\[0\].A is signed only if the format is a signed format; the other endpoints are signed only if the endpoint was transformed, or if the format is a signed format.</span></span> <span data-ttu-id="49b18-291">Le code ci-dessous illustre l’algorithme permettant d’étendre le signe des valeurs de point de terminaison à deux régions.</span><span class="sxs-lookup"><span data-stu-id="49b18-291">The code below demonstrates the algorithm for extending the sign of two-region endpoint values.</span></span>

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

<span data-ttu-id="49b18-292">Pour les vignettes d’une région, le comportement est le même, uniquement avec Endpt \[ 1 \] supprimé.</span><span class="sxs-lookup"><span data-stu-id="49b18-292">For one-region tiles, the behavior is the same, only with endpt\[1\] removed.</span></span>

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

## <a name="transform-inversion-for-endpoint-values"></a><span data-ttu-id="49b18-293">Transformer inversion pour les valeurs de point de terminaison</span><span class="sxs-lookup"><span data-stu-id="49b18-293">Transform Inversion for Endpoint Values</span></span>

<span data-ttu-id="49b18-294">Pour les vignettes de deux régions, la transformation applique l’inverse de l’encodage de différence, en ajoutant la valeur de base à Endpt \[ 0 \] . À trois autres entrées pour un total de 9 opérations d’ajout.</span><span class="sxs-lookup"><span data-stu-id="49b18-294">For two-region tiles, the transform applies the inverse of the difference encoding, adding the base value at endpt\[0\].A to the three other entries for a total of 9 add operations.</span></span> <span data-ttu-id="49b18-295">Dans l’image ci-dessous, la valeur de base est représentée sous la forme « a0 » et a la précision à virgule flottante la plus élevée.</span><span class="sxs-lookup"><span data-stu-id="49b18-295">In the image below, the base value is represented as "A0" and has the highest floating point precision.</span></span> <span data-ttu-id="49b18-296">« A1 », « B0 » et « B1 » sont tous des deltas calculés à partir de la valeur d’ancrage, et ces valeurs Delta sont représentées par une précision inférieure.</span><span class="sxs-lookup"><span data-stu-id="49b18-296">"A1," "B0," and "B1" are all deltas calculated from the anchor value, and these delta values are represented with lower precision.</span></span> <span data-ttu-id="49b18-297">(A0 correspond à Endpt \[ 0 \] . A, B0 correspond à Endpt \[ 0 \] . B, a1 correspond à Endpt \[ 1 \] . A, et B1 correspond à Endpt \[ 1 \] . B.)</span><span class="sxs-lookup"><span data-stu-id="49b18-297">(A0 corresponds to endpt\[0\].A, B0 corresponds to endpt\[0\].B, A1 corresponds to endpt\[1\].A, and B1 corresponds to endpt\[1\].B.)</span></span>

![calcul des valeurs de point de terminaison d’inversion de transformation](images/bc6h-transform-inverse.png)

<span data-ttu-id="49b18-299">Pour les vignettes d’une région, il n’y a qu’un seul décalage Delta, et donc seulement 3 opérations d’ajout.</span><span class="sxs-lookup"><span data-stu-id="49b18-299">For one-region tiles there is only one delta offset, and therefore only 3 add operations.</span></span>

<span data-ttu-id="49b18-300">Le décompresseur doit s’assurer que les résultats de la transformation inverse ne dépassent pas la précision de Endpt \[ 0 \] . a.</span><span class="sxs-lookup"><span data-stu-id="49b18-300">The decompressor must ensure that that the results of the inverse transform will not overflow the precision of endpt\[0\].a.</span></span> <span data-ttu-id="49b18-301">Dans le cas d’un dépassement de capacité, les valeurs résultant de la transformation inverse doivent être encapsulées dans le même nombre de bits.</span><span class="sxs-lookup"><span data-stu-id="49b18-301">In the case of an overflow, the values resulting from the inverse transform must wrap within the same number of bits.</span></span> <span data-ttu-id="49b18-302">Si la précision de a0 est de « p » bits, l’algorithme de transformation est le suivant :</span><span class="sxs-lookup"><span data-stu-id="49b18-302">If the precision of A0 is "p" bits, then the transform algorithm is:</span></span>

`B0 = (B0 + A0) & ((1 << p) - 1)`

<span data-ttu-id="49b18-303">Pour les formats signés, les résultats du calcul Delta doivent également être étendus.</span><span class="sxs-lookup"><span data-stu-id="49b18-303">For signed formats, the results of the delta calculation must be sign extended as well.</span></span> <span data-ttu-id="49b18-304">Si l’opération d’extension de signe prend en compte l’extension des deux signes, où 0 est positif et 1 est négatif, l’extension de signe 0 s’occupe de la bride ci-dessus.</span><span class="sxs-lookup"><span data-stu-id="49b18-304">If the sign extension operation considers extending both signs, where 0 is positive and 1 is negative, then the sign extension of 0 takes care of the clamp above.</span></span> <span data-ttu-id="49b18-305">De même, après la bride ci-dessus, seule une valeur de 1 (négatif) doit être une extension de signe.</span><span class="sxs-lookup"><span data-stu-id="49b18-305">Equivalently, after the clamp above, only a value of 1 (negative) needs to be sign extended.</span></span>

## <a name="unquantization-of-color-endpoints"></a><span data-ttu-id="49b18-306">DÉQUANTIFICATION des points de terminaison de couleur</span><span class="sxs-lookup"><span data-stu-id="49b18-306">Unquantization of Color Endpoints</span></span>

<span data-ttu-id="49b18-307">Étant donné les points de terminaison non compressés, l’étape suivante consiste à effectuer une DÉQUANTIFICATION initiale des points de terminaison de couleur.</span><span class="sxs-lookup"><span data-stu-id="49b18-307">Given the uncompressed endpoints, the next step is to perform an initial unquantization of the color endpoints.</span></span> <span data-ttu-id="49b18-308">Cela implique trois étapes :</span><span class="sxs-lookup"><span data-stu-id="49b18-308">This involves three steps:</span></span>

-   <span data-ttu-id="49b18-309">Une non-quantification des palettes de couleurs</span><span class="sxs-lookup"><span data-stu-id="49b18-309">An unquantization of the color palettes</span></span>
-   <span data-ttu-id="49b18-310">Interpolation des palettes</span><span class="sxs-lookup"><span data-stu-id="49b18-310">Interpolation of the palettes</span></span>
-   <span data-ttu-id="49b18-311">Finalisation de la DÉQUANTIFICATION</span><span class="sxs-lookup"><span data-stu-id="49b18-311">Unquantization finalization</span></span>

<span data-ttu-id="49b18-312">En séparant le processus de DÉQUANTIFICATION en deux parties (la DÉQUANTIFICATION de la palette de couleurs avant l’interpolation et la DÉQUANTIFICATION finale après l’interpolation) réduit le nombre d’opérations de multiplication requises par rapport à un processus de DÉQUANTIFICATION complet avant l’interpolation de palette.</span><span class="sxs-lookup"><span data-stu-id="49b18-312">Separating the unquantization process into two parts (color palette unquantization before interpolation and final unquantization after interpolation) reduces the number of multiplication operations required when compared to a full unquantization process before palette interpolation.</span></span>

<span data-ttu-id="49b18-313">Le code ci-dessous illustre le processus de récupération des estimations des valeurs de couleur 16 bits d’origine, puis l’utilisation des valeurs de pondération fournies pour ajouter 6 valeurs de couleur supplémentaires à la palette.</span><span class="sxs-lookup"><span data-stu-id="49b18-313">The code below illustrates the process for retrieving estimates of the original 16-bit color values, and then using the supplied weight values to add 6 additional color values to the palette.</span></span> <span data-ttu-id="49b18-314">La même opération est effectuée sur chaque canal.</span><span class="sxs-lookup"><span data-stu-id="49b18-314">The same operation is performed on each channel.</span></span>

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

<span data-ttu-id="49b18-315">L’exemple de code suivant illustre le processus d’interpolation, avec les observations suivantes :</span><span class="sxs-lookup"><span data-stu-id="49b18-315">The next code sample demonstrates the interpolation process, with the following observations:</span></span>

-   <span data-ttu-id="49b18-316">Étant donné que la plage complète des valeurs de couleur pour la fonction **unquantification** (ci-dessous) est comprise entre-32768 et 65535, l’interpolateur est implémenté à l’aide de l’arithmétique signée 17 bits.</span><span class="sxs-lookup"><span data-stu-id="49b18-316">Since the full range of color values for the **unquantize** function (below) are from -32768 to 65535, the interpolator is implemented using 17-bit signed arithmetic.</span></span>
-   <span data-ttu-id="49b18-317">Après l’interpolation, les valeurs sont passées à la fonction de non **\_ quantification** (décrite dans le troisième exemple de cette section), qui applique la mise à l’échelle finale.</span><span class="sxs-lookup"><span data-stu-id="49b18-317">After interpolation, the values are passed to the **finish\_unquantize** function (described in the third sample in this section), which applies the final scaling.</span></span>
-   <span data-ttu-id="49b18-318">Tous les décompresseurs de matériel sont requis pour retourner des résultats de bits précis avec ces fonctions.</span><span class="sxs-lookup"><span data-stu-id="49b18-318">All hardware decompressors are required to return bit-accurate results with these functions.</span></span>

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

<span data-ttu-id="49b18-319">**terminer la \_ désquantification** est appelé après l’interpolation de palette.</span><span class="sxs-lookup"><span data-stu-id="49b18-319">**finish\_unquantize** is called after palette interpolation.</span></span> <span data-ttu-id="49b18-320">La fonction **unquantificateur** reporte la mise à l’échelle de 31/32 pour Signed, 31/64 pour unsigned.</span><span class="sxs-lookup"><span data-stu-id="49b18-320">The **unquantize** function postpones the scaling by 31/32 for signed, 31/64 for unsigned.</span></span> <span data-ttu-id="49b18-321">Ce comportement est nécessaire pour récupérer la valeur finale dans une demi-plage valide (-0x7BFF ~ 0x7BFF) une fois l’interpolation de palette terminée afin de réduire le nombre de multiplications nécessaires.</span><span class="sxs-lookup"><span data-stu-id="49b18-321">This behavior is required to get the final value into valid half range(-0x7BFF ~ 0x7BFF) after the palette interpolation is completed in order to reduce the number of necessary multiplications.</span></span> <span data-ttu-id="49b18-322">**Terminer \_ unquantificateur** applique la mise à l’échelle finale et retourne une valeur **short non signée** qui est réinterprétée en **deux**.</span><span class="sxs-lookup"><span data-stu-id="49b18-322">**finish\_unquantize** applies the final scaling and returns an **unsigned short** value that gets reinterpreted into **half**.</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="49b18-323">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="49b18-323">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="49b18-324">Compression de bloc de texture dans Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="49b18-324">Texture Block Compression in Direct3D 11</span></span>](texture-block-compression-in-direct3d-11.md)
</dt> </dl>

 

 