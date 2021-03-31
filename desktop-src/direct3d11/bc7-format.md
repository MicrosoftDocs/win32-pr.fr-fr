---
title: Format BC7
description: Le format BC7 est un format de compression de texture utilisé pour la compression de haute qualité des données RVB et RVBA.
ms.assetid: DF333106-293E-4B3E-A1EB-B0BF0ADBAC72
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b9b64c3d4a8b5e960077a9f33de82ff08cd4bbc
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104382459"
---
# <a name="bc7-format"></a><span data-ttu-id="1314a-103">Format BC7</span><span class="sxs-lookup"><span data-stu-id="1314a-103">BC7 Format</span></span>

<span data-ttu-id="1314a-104">Le format BC7 est un format de compression de texture utilisé pour la compression de haute qualité des données RVB et RVBA.</span><span class="sxs-lookup"><span data-stu-id="1314a-104">The BC7 format is a texture compression format used for high-quality compression of RGB and RGBA data.</span></span>

-   [<span data-ttu-id="1314a-105">À propos du format BC7/DXGI \_ \_ Bc7</span><span class="sxs-lookup"><span data-stu-id="1314a-105">About BC7/DXGI\_FORMAT\_BC7</span></span>](/windows)
-   [<span data-ttu-id="1314a-106">Implémentation de BC7</span><span class="sxs-lookup"><span data-stu-id="1314a-106">BC7 Implementation</span></span>](#bc7-implementation)
-   [<span data-ttu-id="1314a-107">Décodage du format BC7</span><span class="sxs-lookup"><span data-stu-id="1314a-107">Decoding the BC7 Format</span></span>](#decoding-the-bc7-format)
-   [<span data-ttu-id="1314a-108">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="1314a-108">Related topics</span></span>](#related-topics)

<span data-ttu-id="1314a-109">Pour plus d’informations sur les modes de blocage du format BC7, consultez [Référence du mode de formatage Bc7](bc7-format-mode-reference.md).</span><span class="sxs-lookup"><span data-stu-id="1314a-109">For info about the block modes of the BC7 format, see [BC7 Format Mode Reference](bc7-format-mode-reference.md).</span></span>

## <a name="about-bc7dxgi_format_bc7"></a><span data-ttu-id="1314a-110">À propos du format BC7/DXGI \_ \_ Bc7</span><span class="sxs-lookup"><span data-stu-id="1314a-110">About BC7/DXGI\_FORMAT\_BC7</span></span>

<span data-ttu-id="1314a-111">BC7 est spécifié par les valeurs d' \_ énumération de format dxgi suivantes :</span><span class="sxs-lookup"><span data-stu-id="1314a-111">BC7 is specified by the following DXGI\_FORMAT enumeration values:</span></span>

-   <span data-ttu-id="1314a-112">**Dxgi \_ FORMAT \_ Bc7 non \_ typé**.</span><span class="sxs-lookup"><span data-stu-id="1314a-112">**DXGI\_FORMAT\_BC7\_TYPELESS**.</span></span>
-   <span data-ttu-id="1314a-113">**Dxgi \_ FORMAT \_ Bc7 \_ UNORM**.</span><span class="sxs-lookup"><span data-stu-id="1314a-113">**DXGI\_FORMAT\_BC7\_UNORM**.</span></span>
-   <span data-ttu-id="1314a-114">**Dxgi \_ FORMAT \_ Bc7 \_ UNORM \_ sRVB**.</span><span class="sxs-lookup"><span data-stu-id="1314a-114">**DXGI\_FORMAT\_BC7\_UNORM\_SRGB**.</span></span>

<span data-ttu-id="1314a-115">Le format BC7 peut être utilisé pour les ressources de texture [Texture2D](/windows/desktop/direct3d10/d3d10-graphics-reference-resource-structures) (y compris les tableaux), Texture3D ou TextureCube (y compris les tableaux).</span><span class="sxs-lookup"><span data-stu-id="1314a-115">The BC7 format can be used for [Texture2D](/windows/desktop/direct3d10/d3d10-graphics-reference-resource-structures) (including arrays), Texture3D, or TextureCube (including arrays) texture resources.</span></span> <span data-ttu-id="1314a-116">De même, ce format s’applique à toutes les surfaces de la carte MIP associées à ces ressources.</span><span class="sxs-lookup"><span data-stu-id="1314a-116">Similarly, this format applies to any MIP-map surfaces associated with these resources.</span></span>

<span data-ttu-id="1314a-117">BC7 utilise une taille de bloc fixe de 16 octets (128 bits) et une taille de vignette fixe de texels 4x4.</span><span class="sxs-lookup"><span data-stu-id="1314a-117">BC7 uses a fixed block size of 16 bytes (128 bits) and a fixed tile size of 4x4 texels.</span></span> <span data-ttu-id="1314a-118">Comme avec les formats BC précédents, les images de texture plus volumineuses que la taille de vignette prise en charge (4x4) sont compressées à l’aide de plusieurs blocs.</span><span class="sxs-lookup"><span data-stu-id="1314a-118">As with previous BC formats, texture images larger than the supported tile size (4x4) are compressed by using multiple blocks.</span></span> <span data-ttu-id="1314a-119">Cette identité d’adressage s’applique également aux images en trois dimensions et aux tableaux MIP-Maps, cubemaps et texture.</span><span class="sxs-lookup"><span data-stu-id="1314a-119">This addressing identity also applies to three-dimensional images and MIP-maps, cubemaps, and texture arrays.</span></span> <span data-ttu-id="1314a-120">Toutes les vignettes d’image doivent avoir le même format.</span><span class="sxs-lookup"><span data-stu-id="1314a-120">All image tiles must be of the same format.</span></span>

<span data-ttu-id="1314a-121">BC7 compresse les images de données à virgule fixe à trois canaux (RVB) et à quatre canaux (RVBA).</span><span class="sxs-lookup"><span data-stu-id="1314a-121">BC7 compresses both three-channel (RGB) and four-channel (RGBA) fixed-point data images.</span></span> <span data-ttu-id="1314a-122">En règle générale, les données sources sont de 8 bits par composant de couleur (canal), bien que le format puisse encoder les données sources avec des bits plus élevés par composant de couleur.</span><span class="sxs-lookup"><span data-stu-id="1314a-122">Typically, source data is 8 bits per color component (channel), although the format is capable of encoding source data with higher bits per color component.</span></span> <span data-ttu-id="1314a-123">Toutes les vignettes d’image doivent avoir le même format.</span><span class="sxs-lookup"><span data-stu-id="1314a-123">All image tiles must be of the same format.</span></span>

<span data-ttu-id="1314a-124">Le décodeur BC7 effectue la décompression avant l’application du filtrage de texture.</span><span class="sxs-lookup"><span data-stu-id="1314a-124">The BC7 decoder performs decompression before texture filtering is applied.</span></span>

<span data-ttu-id="1314a-125">Le matériel de décompression BC7 doit être d’un bit précis ; autrement dit, le matériel doit retourner des résultats qui sont identiques aux résultats retournés par le décodeur décrit dans ce document.</span><span class="sxs-lookup"><span data-stu-id="1314a-125">BC7 decompression hardware must be bit accurate; that is, the hardware must return results that are identical to the results returned by the decoder described in this document.</span></span>

## <a name="bc7-implementation"></a><span data-ttu-id="1314a-126">Implémentation de BC7</span><span class="sxs-lookup"><span data-stu-id="1314a-126">BC7 Implementation</span></span>

<span data-ttu-id="1314a-127">Une implémentation de BC7 peut spécifier l’un des 8 modes, le mode spécifié dans le bit le moins significatif du bloc de 16 octets (128 bits).</span><span class="sxs-lookup"><span data-stu-id="1314a-127">A BC7 implementation can specify one of 8 modes, with the mode specified in the least significant bit of the 16 byte (128 bit) block.</span></span> <span data-ttu-id="1314a-128">Le mode est encodé par zéro, un ou plusieurs bits, avec la valeur 0 suivie d’un 1.</span><span class="sxs-lookup"><span data-stu-id="1314a-128">The mode is encoded by zero or more bits with a value of 0 followed by a 1.</span></span>

<span data-ttu-id="1314a-129">Un bloc BC7 peut contenir plusieurs paires de points de terminaison.</span><span class="sxs-lookup"><span data-stu-id="1314a-129">A BC7 block can contain multiple endpoint pairs.</span></span> <span data-ttu-id="1314a-130">Dans le cadre de cette documentation, l’ensemble d’index correspondant à une paire de points de terminaison peut être appelé « sous-ensemble ».</span><span class="sxs-lookup"><span data-stu-id="1314a-130">For the purposes of this documentation, the set of indices that correspond to an endpoint pair may be referred to as a "subset."</span></span> <span data-ttu-id="1314a-131">En outre, dans certains modes de blocage, la représentation du point de terminaison est encodée dans un formulaire qui, dans le cadre de cette documentation, est appelée « RBGP », où le bit « P » représente un bit moins significatif partagé pour les composants de couleur du point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="1314a-131">Also, in some block modes, the endpoint representation is encoded in a form that -- again, for the purposes of this documentation -- shall be referred to as "RBGP," where the "P" bit represents a shared least significant bit for the color components of the endpoint.</span></span> <span data-ttu-id="1314a-132">Par exemple, si la représentation du point de terminaison pour le format est « RGB 5.5.5.1 », le point de terminaison est interprété comme une valeur 6.6.6 RVB, où l’état du bit P définit le bit le moins significatif de chaque composant.</span><span class="sxs-lookup"><span data-stu-id="1314a-132">For example, if the endpoint representation for the format is "RGB 5.5.5.1," then the endpoint is interpreted as an RGB 6.6.6 value, where the state of the P-bit defines the least significant bit of each component.</span></span> <span data-ttu-id="1314a-133">De même, pour les données sources avec un canal alpha, si la représentation du format est « RGBAP 5.5.5.5.1 », le point de terminaison est interepreted comme RVBA 6.6.6.6.</span><span class="sxs-lookup"><span data-stu-id="1314a-133">Similarly, for source data with an alpha channel, if the representation for the format is "RGBAP 5.5.5.5.1," then the endpoint is interepreted as RGBA 6.6.6.6.</span></span> <span data-ttu-id="1314a-134">En fonction du mode de blocage, vous pouvez spécifier le bit le moins significatif partagé pour les deux points de terminaison d’un sous-ensemble, individuellement (2 P-bits par sous-ensemble), ou partagé entre les points de terminaison d’un sous-ensemble (1 P-bit par sous-ensemble).</span><span class="sxs-lookup"><span data-stu-id="1314a-134">Depending on the block mode, you can specify the shared least significant bit for either both endpoints of a subset individually (2 P-bits per subset), or shared between endpoints of a subset (1 P-bit per subset).</span></span>

<span data-ttu-id="1314a-135">Pour les blocs BC7 qui n’encodent pas explicitement le composant alpha, un bloc BC7 se compose de bits en mode, de bits de partition, de points de terminaison compressés, d’index compressés et d’un P-bit facultatif.</span><span class="sxs-lookup"><span data-stu-id="1314a-135">For BC7 blocks that don't explicitly encode the alpha component, a BC7 block consists of mode bits, partition bits, compressed endpoints, compressed indices, and an optional P-bit.</span></span> <span data-ttu-id="1314a-136">Dans ces blocs, les points de terminaison ont une représentation RVB uniquement et le composant alpha est décodé comme 1,0 pour tous les texels dans les données sources.</span><span class="sxs-lookup"><span data-stu-id="1314a-136">In these blocks the endpoints have an RGB-only representation and the alpha component is decoded as 1.0 for all texels in the source data.</span></span>

<span data-ttu-id="1314a-137">Pour les blocs BC7 qui ont des composants alpha et de couleur combinés, un bloc se compose de bits en mode, de points de terminaison compressés, d’index compressés et de bits de partition facultatifs et d’un bit P.</span><span class="sxs-lookup"><span data-stu-id="1314a-137">For BC7 blocks that have combined color and alpha components, a block consists of mode bits, compressed endpoints, compressed indices, and optional partition bits and a P-bit.</span></span> <span data-ttu-id="1314a-138">Dans ces blocs, les couleurs du point de terminaison sont exprimées au format RVBA et les valeurs des composants alpha sont interpolées avec les valeurs du composant de couleur.</span><span class="sxs-lookup"><span data-stu-id="1314a-138">In these blocks, the endpoint colors are expressed in RGBA format, and alpha component values are interpolated alongside the color component values.</span></span>

<span data-ttu-id="1314a-139">Pour les blocs BC7 qui possèdent des composants alpha et de couleur distincts, un bloc se compose de bits en mode, de bits de rotation, de points de terminaison compressés, d’index compressés et d’un bit sélecteur d’index facultatif.</span><span class="sxs-lookup"><span data-stu-id="1314a-139">For BC7 blocks that have separate color and alpha components, a block consists of mode bits, rotation bits, compressed endpoints, compressed indices, and an optional index selector bit.</span></span> <span data-ttu-id="1314a-140">Ces blocs ont un vecteur RVB effectif \[ R, G, B \] et un canal alpha scalaire \[ est \] encodé séparément.</span><span class="sxs-lookup"><span data-stu-id="1314a-140">These blocks have an effective RGB vector \[R, G, B\] and a scalar alpha channel \[A\] separately encoded.</span></span>

<span data-ttu-id="1314a-141">Le tableau suivant répertorie les composants de chaque type de bloc.</span><span class="sxs-lookup"><span data-stu-id="1314a-141">The following table lists the components of each block type.</span></span>



| <span data-ttu-id="1314a-142">Le bloc BC7 contient...</span><span class="sxs-lookup"><span data-stu-id="1314a-142">BC7 block contains...</span></span>     | <span data-ttu-id="1314a-143">bits de mode</span><span class="sxs-lookup"><span data-stu-id="1314a-143">mode bits</span></span> | <span data-ttu-id="1314a-144">bits de rotation</span><span class="sxs-lookup"><span data-stu-id="1314a-144">rotation bits</span></span> | <span data-ttu-id="1314a-145">bit de sélecteur d’index</span><span class="sxs-lookup"><span data-stu-id="1314a-145">index selector bit</span></span> | <span data-ttu-id="1314a-146">bits de partition</span><span class="sxs-lookup"><span data-stu-id="1314a-146">partition bits</span></span> | <span data-ttu-id="1314a-147">points de terminaison compressés</span><span class="sxs-lookup"><span data-stu-id="1314a-147">compressed endpoints</span></span> | <span data-ttu-id="1314a-148">Bit P</span><span class="sxs-lookup"><span data-stu-id="1314a-148">P-bit</span></span>    | <span data-ttu-id="1314a-149">index compressés</span><span class="sxs-lookup"><span data-stu-id="1314a-149">compressed indices</span></span> |
|---------------------------|-----------|---------------|--------------------|----------------|----------------------|----------|--------------------|
| <span data-ttu-id="1314a-150">composants de couleur uniquement</span><span class="sxs-lookup"><span data-stu-id="1314a-150">color components only</span></span>     | <span data-ttu-id="1314a-151">obligatoire</span><span class="sxs-lookup"><span data-stu-id="1314a-151">required</span></span>  | <span data-ttu-id="1314a-152">N/A</span><span class="sxs-lookup"><span data-stu-id="1314a-152">N/A</span></span>           | <span data-ttu-id="1314a-153">N/A</span><span class="sxs-lookup"><span data-stu-id="1314a-153">N/A</span></span>                | <span data-ttu-id="1314a-154">obligatoire</span><span class="sxs-lookup"><span data-stu-id="1314a-154">required</span></span>       | <span data-ttu-id="1314a-155">obligatoire</span><span class="sxs-lookup"><span data-stu-id="1314a-155">required</span></span>             | <span data-ttu-id="1314a-156">facultatif</span><span class="sxs-lookup"><span data-stu-id="1314a-156">optional</span></span> | <span data-ttu-id="1314a-157">obligatoire</span><span class="sxs-lookup"><span data-stu-id="1314a-157">required</span></span>           |
| <span data-ttu-id="1314a-158">couleur + alpha combiné</span><span class="sxs-lookup"><span data-stu-id="1314a-158">color + alpha combined</span></span>    | <span data-ttu-id="1314a-159">obligatoire</span><span class="sxs-lookup"><span data-stu-id="1314a-159">required</span></span>  | <span data-ttu-id="1314a-160">N/A</span><span class="sxs-lookup"><span data-stu-id="1314a-160">N/A</span></span>           | <span data-ttu-id="1314a-161">N/A</span><span class="sxs-lookup"><span data-stu-id="1314a-161">N/A</span></span>                | <span data-ttu-id="1314a-162">facultatif</span><span class="sxs-lookup"><span data-stu-id="1314a-162">optional</span></span>       | <span data-ttu-id="1314a-163">obligatoire</span><span class="sxs-lookup"><span data-stu-id="1314a-163">required</span></span>             | <span data-ttu-id="1314a-164">facultatif</span><span class="sxs-lookup"><span data-stu-id="1314a-164">optional</span></span> | <span data-ttu-id="1314a-165">obligatoire</span><span class="sxs-lookup"><span data-stu-id="1314a-165">required</span></span>           |
| <span data-ttu-id="1314a-166">Color et alpha séparés</span><span class="sxs-lookup"><span data-stu-id="1314a-166">color and alpha separated</span></span> | <span data-ttu-id="1314a-167">obligatoire</span><span class="sxs-lookup"><span data-stu-id="1314a-167">required</span></span>  | <span data-ttu-id="1314a-168">obligatoire</span><span class="sxs-lookup"><span data-stu-id="1314a-168">required</span></span>      | <span data-ttu-id="1314a-169">facultatif</span><span class="sxs-lookup"><span data-stu-id="1314a-169">optional</span></span>           | <span data-ttu-id="1314a-170">N/A</span><span class="sxs-lookup"><span data-stu-id="1314a-170">N/A</span></span>            | <span data-ttu-id="1314a-171">obligatoire</span><span class="sxs-lookup"><span data-stu-id="1314a-171">required</span></span>             | <span data-ttu-id="1314a-172">N/A</span><span class="sxs-lookup"><span data-stu-id="1314a-172">N/A</span></span>      | <span data-ttu-id="1314a-173">obligatoire</span><span class="sxs-lookup"><span data-stu-id="1314a-173">required</span></span>           |



 

<span data-ttu-id="1314a-174">BC7 définit une palette de couleurs sur une ligne approximative entre deux points de terminaison.</span><span class="sxs-lookup"><span data-stu-id="1314a-174">BC7 defines a palette of colors on an approximate line between two endpoints.</span></span> <span data-ttu-id="1314a-175">La valeur de mode détermine le nombre de paires de points de terminaison d’interpolation par bloc.</span><span class="sxs-lookup"><span data-stu-id="1314a-175">The mode value determines the number of interpolating endpoint pairs per block.</span></span> <span data-ttu-id="1314a-176">BC7 stocke un index de palette par Texel.</span><span class="sxs-lookup"><span data-stu-id="1314a-176">BC7 stores one palette index per texel.</span></span>

<span data-ttu-id="1314a-177">Pour chaque sous-ensemble d’index qui correspond à une paire de points de terminaison, l’encodeur résout l’état d’un bit des données d’index compressées pour ce sous-ensemble.</span><span class="sxs-lookup"><span data-stu-id="1314a-177">For each subset of indices that corresponds to a pair of endpoints, the encoder fixes the state of one bit of the compressed index data for that subset.</span></span> <span data-ttu-id="1314a-178">Pour ce faire, il choisit un ordre de point de terminaison qui permet à l’index de l’index « Fix-up » désigné de définir son bit le plus significatif à 0 et qui peut ensuite être ignoré, ce qui permet d’économiser un bit par sous-ensemble.</span><span class="sxs-lookup"><span data-stu-id="1314a-178">It does so by choosing an endpoint order that allows the index for the designated "fix-up" index to set its most significant bit to 0, and which can then be discarded, saving one bit per subset.</span></span> <span data-ttu-id="1314a-179">Pour les modes de blocage avec un seul sous-ensemble, l’index de correction est toujours l’index 0.</span><span class="sxs-lookup"><span data-stu-id="1314a-179">For block modes with only a single subset, the fix-up index is always index 0.</span></span>

## <a name="decoding-the-bc7-format"></a><span data-ttu-id="1314a-180">Décodage du format BC7</span><span class="sxs-lookup"><span data-stu-id="1314a-180">Decoding the BC7 Format</span></span>

<span data-ttu-id="1314a-181">Le pseudocode suivant décrit les étapes pour décompresser le pixel à (x, y) en fonction du bloc BC7 de 16 octets.</span><span class="sxs-lookup"><span data-stu-id="1314a-181">The following pseudocode outlines the steps to decompress the pixel at (x,y) given the 16 byte BC7 block.</span></span>

``` syntax
decompress_bc7(x, y, block)
{
    mode = extract_mode(block);
    
    //decode partition data from explicit partition bits
    subset_index = 0;
    num_subsets = 1;
    
    if (mode.type == 0 OR == 1 OR == 2 OR == 3 OR == 7)
    {
        num_subsets = get_num_subsets(mode.type);
        partition_set_id = extract_partition_set_id(mode, block);
        subset_index = get_partition_index(num_subsets, partition_set_id, x, y);
    }
    
    //extract raw, compressed endpoint bits
    UINT8 endpoint_array[num_subsets][4] = extract_endpoints(mode, block);
    
    //decode endpoint color and alpha for each subset
    fully_decode_endpoints(endpoint_array, mode, block);
    
    //endpoints are now complete.
    UINT8 endpoint_start[4] = endpoint_array[2 * subset_index];
    UINT8 endpoint_end[4]   = endpoint_array[2 * subset_index + 1];
        
    //Determine the palette index for this pixel
    alpha_index     = get_alpha_index(block, mode, x, y);
    alpha_bitcount  = get_alpha_bitcount(block, mode);
    color_index     = get_color_index(block, mode, x, y);
    color_bitcount  = get_color_bitcount(block, mode);

    //determine output
    UINT8 output[4];
    output.rgb = interpolate(endpoint_start.rgb, endpoint_end.rgb, color_index, color_bitcount);
    output.a   = interpolate(endpoint_start.a,   endpoint_end.a,   alpha_index, alpha_bitcount);
    
    if (mode.type == 4 OR == 5)
    {
        //Decode the 2 color rotation bits as follows:
        // 00 – Block format is Scalar(A) Vector(RGB) - no swapping
        // 01 – Block format is Scalar(R) Vector(AGB) - swap A and R
        // 10 – Block format is Scalar(G) Vector(RAB) - swap A and G
        // 11 - Block format is Scalar(B) Vector(RGA) - swap A and B
        rotation = extract_rot_bits(mode, block);
        output = swap_channels(output, rotation);
    }
    
}
```

<span data-ttu-id="1314a-182">Le pseudocode au décrit les étapes permettant de décoder entièrement la couleur du point de terminaison et les composants alpha pour chaque sous-ensemble en fonction d’un bloc BC7 de 16 octets.</span><span class="sxs-lookup"><span data-stu-id="1314a-182">The followoing pseudocode outlines the steps to fully decode endpoint color and alpha components for each subset given a 16-byte BC7 block.</span></span>

``` syntax
fully_decode_endpoints(endpoint_array, mode, block)
{
    //first handle modes that have P-bits
    if (mode.type == 0 OR == 1 OR == 3 OR == 6 OR == 7)
    {
        for each endpoint i
        {
            //component-wise left-shift
            endpoint_array[i].rgba = endpoint_array[i].rgba << 1;
        }
        
        //if P-bit is shared
        if (mode.type == 1) 
        {
            pbit_zero = extract_pbit_zero(mode, block);
            pbit_one = extract_pbit_one(mode, block);
            
            //rgb component-wise insert pbits
            endpoint_array[0].rgb |= pbit_zero;
            endpoint_array[1].rgb |= pbit_zero;
            endpoint_array[2].rgb |= pbit_one;
            endpoint_array[3].rgb |= pbit_one;  
        }
        else //unique P-bit per endpoint
        {  
            pbit_array = extract_pbit_array(mode, block);
            for each endpoint i
            {
                endpoint_array[i].rgba |= pbit_array[i];
            }
        }
    }

    for each endpoint i
    {
        // Color_component_precision & alpha_component_precision includes pbit
        // left shift endpoint components so that their MSB lies in bit 7
        endpoint_array[i].rgb = endpoint_array[i].rgb << (8 - color_component_precision(mode));
        endpoint_array[i].a = endpoint_array[i].a << (8 - alpha_component_precision(mode));

        // Replicate each component's MSB into the LSBs revealed by the left-shift operation above
        endpoint_array[i].rgb = endpoint_array[i].rgb | (endpoint_array[i].rgb >> color_component_precision(mode));
        endpoint_array[i].a = endpoint_array[i].a | (endpoint_array[i].a >> alpha_component_precision(mode));
    }
        
    //If this mode does not explicitly define the alpha component
    //set alpha equal to 1.0
    if (mode.type == 0 OR == 1 OR == 2 OR == 3)
    {
        for each endpoint i
        {
            endpoint_array[i].a = 255; //i.e. alpha = 1.0f
        }
    }
}
```

<span data-ttu-id="1314a-183">Pour générer chaque composant interpolé pour chaque sous-ensemble, utilisez l’algorithme suivant : « c » est le composant à générer ; Let « E0 » est ce composant du point de terminaison 0 du sous-ensemble ; et laissent « E1 » le composant du point de terminaison 1 du sous-ensemble.</span><span class="sxs-lookup"><span data-stu-id="1314a-183">To generate each interpolated component for each subset, use the following algorithm: let "c" be the component to generate; let "e0" be that component of endpoint 0 of the subset; and let "e1" be that component of endpoint 1 of the subset.</span></span>

``` syntax
UINT16 aWeight2[] = {0, 21, 43, 64};
UINT16 aWeight3[] = {0, 9, 18, 27, 37, 46, 55, 64};
UINT16 aWeight4[] = {0, 4, 9, 13, 17, 21, 26, 30, 34, 38, 43, 47, 51, 55, 60, 64};

UINT8 interpolate(UINT8 e0, UINT8 e1, UINT8 index, UINT8 indexprecision)
{
    if(indexprecision == 2)
        return (UINT8) (((64 - aWeights2[index])*UINT16(e0) + aWeights2[index]*UINT16(e1) + 32) >> 6);
    else if(indexprecision == 3)
        return (UINT8) (((64 - aWeights3[index])*UINT16(e0) + aWeights3[index]*UINT16(e1) + 32) >> 6);
    else // indexprecision == 4
        return (UINT8) (((64 - aWeights4[index])*UINT16(e0) + aWeights4[index]*UINT16(e1) + 32) >> 6);
}
```

<span data-ttu-id="1314a-184">Le pseudo-code suivant montre comment extraire les index et les nombres de bits pour les composants de couleur et alpha.</span><span class="sxs-lookup"><span data-stu-id="1314a-184">The following pseudocode illustrates how to extract indices and bit counts for color and alpha components.</span></span> <span data-ttu-id="1314a-185">Les blocs avec des couleurs distinctes et alpha ont également deux jeux de données d’index : un pour le canal vectoriel et un pour le canal scalaire.</span><span class="sxs-lookup"><span data-stu-id="1314a-185">Blocks with separate color and alpha also have two sets of index data: one for the vector channel, and one for the scalar channel.</span></span> <span data-ttu-id="1314a-186">Pour le mode 4, ces index se distinguent par des largeurs (2 ou 3 bits) et un sélecteur à un bit spécifie si les données vectorielles ou scalaires utilisent les index 3 bits.</span><span class="sxs-lookup"><span data-stu-id="1314a-186">For Mode 4, these indices are of differing widths (2 or 3 bits), and there is a one-bit selector which specifies whether the vector or scalar data uses the 3-bit indices.</span></span> <span data-ttu-id="1314a-187">(L’extraction du nombre de bits alpha est similaire à l’extraction du nombre de bits de couleur, mais avec un comportement inverse basé sur le bit **idxMode** .)</span><span class="sxs-lookup"><span data-stu-id="1314a-187">(Extracting the alpha bit count is similar to extracting color bit count but with inverse behavior based on the **idxMode** bit.)</span></span>

``` syntax
bitcount get_color_bitcount(block, mode)
{
    if (mode.type == 0 OR == 1)
        return 3;
    
    if (mode.type == 2 OR == 3 OR == 5 OR == 7)
        return 2;
    
    if (mode.type == 6)
        return 4;
        
    //The only remaining case is Mode 4 with 1-bit index selector
    idxMode = extract_idxMode(block);
    if (idxMode == 0)
        return 2;
    else
        return 3;
}
```

## <a name="related-topics"></a><span data-ttu-id="1314a-188">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="1314a-188">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1314a-189">Compression de bloc de texture dans Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="1314a-189">Texture Block Compression in Direct3D 11</span></span>](texture-block-compression-in-direct3d-11.md)
</dt> </dl>

 

 