---
description: Cette rubrique décrit les formats YUV 10 et 16 bits recommandés pour la capture, le traitement et l’affichage de vidéos dans le système d’exploitation Microsoft Windows.
ms.assetid: fcaaaa6f-f886-4f6e-9c3c-e513ccc90d37
title: Formats vidéo YUV 10 bits et 16 bits
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6bbc357653848cd51ce6f56ebd8a1da3e5f60403
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113443"
---
# <a name="10-bit-and-16-bit-yuv-video-formats"></a><span data-ttu-id="d96de-103">Formats vidéo YUV 10 bits et 16 bits</span><span class="sxs-lookup"><span data-stu-id="d96de-103">10-bit and 16-bit YUV Video Formats</span></span>

<span data-ttu-id="d96de-104">Cette rubrique décrit les formats YUV 10 et 16 bits recommandés pour la capture, le traitement et l’affichage de vidéos dans le système d’exploitation Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="d96de-104">This topic describes the 10- and 16-bit YUV formats that are recommended for capturing, processing, and displaying video in the Microsoft Windows operating system.</span></span>

<span data-ttu-id="d96de-105">Cette rubrique contient les sections suivantes :</span><span class="sxs-lookup"><span data-stu-id="d96de-105">This topic contains the following sections:</span></span>

-   [<span data-ttu-id="d96de-106">Vue d’ensemble</span><span class="sxs-lookup"><span data-stu-id="d96de-106">Overview</span></span>](#overview)
-   [<span data-ttu-id="d96de-107">Codes FOURCC pour YUV 10 bits et 16 bits</span><span class="sxs-lookup"><span data-stu-id="d96de-107">FOURCC Codes For 10-Bit and 16-Bit YUV</span></span>](#fourcc-codes-for-10-bit-and-16-bit-yuv)
-   [<span data-ttu-id="d96de-108">Définitions de surface</span><span class="sxs-lookup"><span data-stu-id="d96de-108">Surface Definitions</span></span>](#surface-definitions)
    -   [<span data-ttu-id="d96de-109">4:2:0 formats</span><span class="sxs-lookup"><span data-stu-id="d96de-109">4:2:0 Formats</span></span>](#420-formats)
    -   [<span data-ttu-id="d96de-110">4:2:2 formats</span><span class="sxs-lookup"><span data-stu-id="d96de-110">4:2:2 Formats</span></span>](#422-formats)
    -   [<span data-ttu-id="d96de-111">4:4:4 formats</span><span class="sxs-lookup"><span data-stu-id="d96de-111">4:4:4 Formats</span></span>](#444-formats)
-   [<span data-ttu-id="d96de-112">Formats YUV préférés</span><span class="sxs-lookup"><span data-stu-id="d96de-112">Preferred YUV Formats</span></span>](#preferred-yuv-formats)
-   [<span data-ttu-id="d96de-113">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="d96de-113">Related topics</span></span>](#related-topics)

## <a name="overview"></a><span data-ttu-id="d96de-114">Vue d’ensemble</span><span class="sxs-lookup"><span data-stu-id="d96de-114">Overview</span></span>

<span data-ttu-id="d96de-115">Ces formats utilisent une représentation à virgule fixe pour le canal de luminance et les canaux Chroma (C’b et C’r).</span><span class="sxs-lookup"><span data-stu-id="d96de-115">These formats use a fixed-point representation for both the luma channel and the chroma (C'b and C'r) channels.</span></span> <span data-ttu-id="d96de-116">Les valeurs d’échantillonnage sont des valeurs 8 bits mises à l’échelle, à l’aide d’un facteur d’échelle de 2 ^ (n − 8), où n est égal à 10 ou 16, comme pour les sections 7.7-7.8 et 7.11-7.12 de SMPTE 274M.</span><span class="sxs-lookup"><span data-stu-id="d96de-116">Sample values are scaled 8-bit values, using a scaling factor of 2^(n − 8), where n is either 10 or 16, as per sections 7.7-7.8 and 7.11-7.12 of SMPTE 274M.</span></span> <span data-ttu-id="d96de-117">Les conversions de précision peuvent être effectuées à l’aide de décalages binaires simples.</span><span class="sxs-lookup"><span data-stu-id="d96de-117">Precision conversions can be performed using simple bit shifts.</span></span> <span data-ttu-id="d96de-118">Par exemple, si le point blanc d’un format 8 bits est 235, le format 10 bits correspondant a un point blanc à 940 (235 × 4).</span><span class="sxs-lookup"><span data-stu-id="d96de-118">For example, if the white point of an 8-bit format is 235, the corresponding 10-bit format has a white point at 940 (235 × 4).</span></span>

<span data-ttu-id="d96de-119">Les représentations 16 bits décrites ici utilisent des valeurs de **mot** Little-endian pour chaque canal.</span><span class="sxs-lookup"><span data-stu-id="d96de-119">The 16-bit representations described here use little-endian **WORD** values for each channel.</span></span> <span data-ttu-id="d96de-120">Les formats 10 bits utilisent également 16 bits pour chaque canal, avec les 6 bits les plus bas définis sur zéro, comme indiqué dans le diagramme suivant.</span><span class="sxs-lookup"><span data-stu-id="d96de-120">The 10-bit formats also use 16 bits for each channel, with the lowest 6 bits set to zero, as shown in the following diagram.</span></span>

![Diagramme montrant la représentation de 10 bits](images/ee3aae23-4f0a-47d0-a46c-f3d7d94205e6.gif)

<span data-ttu-id="d96de-122">Étant donné que les représentations 10 bits et 16 bits du même format YUV ont la même disposition en mémoire, il est possible d’effectuer un cast d’une représentation de 10 bits en une représentation 16, sans perte de précision.</span><span class="sxs-lookup"><span data-stu-id="d96de-122">Because the 10-bit and 16-bit representations of the same YUV format have the same memory layout, it is possible to cast a 10-bit representation to a 16-representation with no loss of precision.</span></span> <span data-ttu-id="d96de-123">Il est également possible d’effectuer un cast d’une représentation 16 bits vers une représentation de 10 bits.</span><span class="sxs-lookup"><span data-stu-id="d96de-123">It is also possible to cast a 16-bit representation down to a 10-bit representation.</span></span> <span data-ttu-id="d96de-124">(Les formats Y416 et Y410 sont toutefois une exception à cette règle générale, car ils ne partagent pas la même disposition en mémoire.)</span><span class="sxs-lookup"><span data-stu-id="d96de-124">(The Y416 and Y410 formats are an exception to this general rule, however, because they do not share the same memory layout.)</span></span>

<span data-ttu-id="d96de-125">Lorsque le matériel graphique lit une surface qui contient une représentation de 10 bits, il doit ignorer les 6 bits de poids faible de chaque canal.</span><span class="sxs-lookup"><span data-stu-id="d96de-125">When the graphics hardware reads a surface that contains a 10-bit representation, it should ignore the low-order 6 bits of each channel.</span></span> <span data-ttu-id="d96de-126">Toutefois, si une surface contient des données 16 bits valides, elle doit être identifiée comme une surface de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="d96de-126">If a surface contains valid 16-bit data, however, it should be identified as a 16-bit surface.</span></span>

<span data-ttu-id="d96de-127">Dans les formats qui contiennent alpha, un pixel complètement transparent a une valeur alpha égale à zéro et un pixel complètement opaque a une valeur alpha (2 ^ n) – 1, où n est le nombre de bits alpha.</span><span class="sxs-lookup"><span data-stu-id="d96de-127">In the formats that contain alpha, a completely transparent pixel has an alpha value of zero, and a completely opaque pixel has an alpha value of (2^n) – 1, where n is the number of alpha bits.</span></span> <span data-ttu-id="d96de-128">Alpha est supposée être une valeur linéaire appliquée à chaque composant une fois que le composant a été converti en sa forme linéaire normalisée.</span><span class="sxs-lookup"><span data-stu-id="d96de-128">Alpha is assumed to be a linear value that is applied to each component after the component has been converted into its normalized linear form.</span></span>

<span data-ttu-id="d96de-129">Pour les images dans la mémoire vidéo, le pilote Graphics sélectionne l’alignement de la mémoire de l’aire.</span><span class="sxs-lookup"><span data-stu-id="d96de-129">For images in video memory, the graphics driver selects the memory alignment of the surface.</span></span> <span data-ttu-id="d96de-130">La surface doit être alignée sur la **valeur DWORD** .</span><span class="sxs-lookup"><span data-stu-id="d96de-130">The surface must be **DWORD** aligned.</span></span> <span data-ttu-id="d96de-131">Autrement dit, les lignes individuelles au sein d’une surface sont assurées de démarrer à une limite de 32 bits, bien que l’alignement puisse être supérieur à 32 bits.</span><span class="sxs-lookup"><span data-stu-id="d96de-131">That is, individual lines within a surface are guaranteed to start at a 32-bit boundary, although the alignment can be larger than 32 bits.</span></span> <span data-ttu-id="d96de-132">L’origine (0,0) est toujours l’angle supérieur gauche de la surface.</span><span class="sxs-lookup"><span data-stu-id="d96de-132">The origin (0,0) is always the upper-left corner of the surface.</span></span>

<span data-ttu-id="d96de-133">Dans le cadre de cette documentation, le terme *U* est équivalent à *CB* et le terme *V* équivaut à *CR*.</span><span class="sxs-lookup"><span data-stu-id="d96de-133">For the purposes of this documentation, the term *U* is equivalent to *Cb*, and the term *V* is equivalent to *Cr*.</span></span>

## <a name="fourcc-codes-for-10-bit-and-16-bit-yuv"></a><span data-ttu-id="d96de-134">Codes FOURCC pour YUV 10 bits et 16 bits</span><span class="sxs-lookup"><span data-stu-id="d96de-134">FOURCC Codes For 10-Bit and 16-Bit YUV</span></span>

<span data-ttu-id="d96de-135">Les Codes FOURCC pour les formats décrits ici utilisent la Convention suivante :</span><span class="sxs-lookup"><span data-stu-id="d96de-135">The FOURCC codes for the formats described here use the following convention:</span></span>

-   <span data-ttu-id="d96de-136">Si le format est planaire, le premier caractère du code FOURCC est « P ».</span><span class="sxs-lookup"><span data-stu-id="d96de-136">If the format is planar, the first character in the FOURCC code is 'P'.</span></span> <span data-ttu-id="d96de-137">Si le format est compressé, le premier caractère est « Y ».</span><span class="sxs-lookup"><span data-stu-id="d96de-137">If the format is packed, the first character is 'Y'.</span></span>
-   <span data-ttu-id="d96de-138">Le deuxième caractère du code FOURCC est déterminé par l’échantillonnage de chrominance, comme indiqué dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="d96de-138">The second character in the FOURCC code is determined by the chroma sampling, as shown in the following table.</span></span>

    

    | <span data-ttu-id="d96de-139">Échantillonnage Chroma</span><span class="sxs-lookup"><span data-stu-id="d96de-139">Chroma sampling</span></span> | <span data-ttu-id="d96de-140">Lettre de code FOURCC</span><span class="sxs-lookup"><span data-stu-id="d96de-140">FOURCC code letter</span></span> |
    |-----------------|--------------------|
    | <span data-ttu-id="d96de-141">4:4:4</span><span class="sxs-lookup"><span data-stu-id="d96de-141">4:4:4</span></span>           | <span data-ttu-id="d96de-142">4</span><span class="sxs-lookup"><span data-stu-id="d96de-142">'4'</span></span>                |
    | <span data-ttu-id="d96de-143">4:2:2</span><span class="sxs-lookup"><span data-stu-id="d96de-143">4:2:2</span></span>           | <span data-ttu-id="d96de-144">2</span><span class="sxs-lookup"><span data-stu-id="d96de-144">'2'</span></span>                |
    | <span data-ttu-id="d96de-145">4:2:1</span><span class="sxs-lookup"><span data-stu-id="d96de-145">4:2:1</span></span>           | <span data-ttu-id="d96de-146">« 1 »</span><span class="sxs-lookup"><span data-stu-id="d96de-146">'1'</span></span>                |
    | <span data-ttu-id="d96de-147">4:2:0</span><span class="sxs-lookup"><span data-stu-id="d96de-147">4:2:0</span></span>           | <span data-ttu-id="d96de-148">« 0 »</span><span class="sxs-lookup"><span data-stu-id="d96de-148">'0'</span></span>                |

    

     

-   <span data-ttu-id="d96de-149">Les deux derniers caractères du FOURCC indiquent le nombre de bits par canal, soit' 16 'pour 16 bits ou' 10 'pour 10 bits.</span><span class="sxs-lookup"><span data-stu-id="d96de-149">The final two characters in the FOURCC indicate the number of bits per channel, either '16' for 16 bits or '10' for 10 bits.</span></span>

<span data-ttu-id="d96de-150">À l’aide de ce schéma, les Codes FOURCC suivants ont été définis.</span><span class="sxs-lookup"><span data-stu-id="d96de-150">Using this scheme, the following FOURCC codes have been defined.</span></span> <span data-ttu-id="d96de-151">Aucun format 4:2:1 pour YUV de 10 ou 16 bits n’a été défini pour l’instant.</span><span class="sxs-lookup"><span data-stu-id="d96de-151">No 4:2:1 formats for 10-bit or 16-bit YUV have been defined at this time.</span></span>



| <span data-ttu-id="d96de-152">FOURCC</span><span class="sxs-lookup"><span data-stu-id="d96de-152">FOURCC</span></span> | <span data-ttu-id="d96de-153">Description</span><span class="sxs-lookup"><span data-stu-id="d96de-153">Description</span></span>            |
|--------|------------------------|
| <span data-ttu-id="d96de-154">P016</span><span class="sxs-lookup"><span data-stu-id="d96de-154">P016</span></span>   | <span data-ttu-id="d96de-155">Planar, 4:2:0, 16 bits.</span><span class="sxs-lookup"><span data-stu-id="d96de-155">Planar, 4:2:0, 16-bit.</span></span> |
| <span data-ttu-id="d96de-156">P010</span><span class="sxs-lookup"><span data-stu-id="d96de-156">P010</span></span>   | <span data-ttu-id="d96de-157">Planar, 4:2:0, 10 bits.</span><span class="sxs-lookup"><span data-stu-id="d96de-157">Planar, 4:2:0, 10-bit.</span></span> |
| <span data-ttu-id="d96de-158">P216</span><span class="sxs-lookup"><span data-stu-id="d96de-158">P216</span></span>   | <span data-ttu-id="d96de-159">Planar, 4:2:2, 16 bits.</span><span class="sxs-lookup"><span data-stu-id="d96de-159">Planar, 4:2:2, 16-bit.</span></span> |
| <span data-ttu-id="d96de-160">P210</span><span class="sxs-lookup"><span data-stu-id="d96de-160">P210</span></span>   | <span data-ttu-id="d96de-161">Planar, 4:2:2, 10 bits.</span><span class="sxs-lookup"><span data-stu-id="d96de-161">Planar, 4:2:2, 10-bit.</span></span> |
| <span data-ttu-id="d96de-162">Y216</span><span class="sxs-lookup"><span data-stu-id="d96de-162">Y216</span></span>   | <span data-ttu-id="d96de-163">Compressé, 4:2:2, 16 bits.</span><span class="sxs-lookup"><span data-stu-id="d96de-163">Packed, 4:2:2, 16-bit.</span></span> |
| <span data-ttu-id="d96de-164">Y210</span><span class="sxs-lookup"><span data-stu-id="d96de-164">Y210</span></span>   | <span data-ttu-id="d96de-165">Compressé, 4:2:2, 10 bits.</span><span class="sxs-lookup"><span data-stu-id="d96de-165">Packed, 4:2:2, 10-bit.</span></span> |
| <span data-ttu-id="d96de-166">Y416</span><span class="sxs-lookup"><span data-stu-id="d96de-166">Y416</span></span>   | <span data-ttu-id="d96de-167">Compressé, 4:4:4, 16 bits</span><span class="sxs-lookup"><span data-stu-id="d96de-167">Packed, 4:4:4, 16-bit</span></span>  |
| <span data-ttu-id="d96de-168">Y410</span><span class="sxs-lookup"><span data-stu-id="d96de-168">Y410</span></span>   | <span data-ttu-id="d96de-169">Compressé, 4:4:4, 10 bits.</span><span class="sxs-lookup"><span data-stu-id="d96de-169">Packed, 4:4:4, 10-bit.</span></span> |



 

<span data-ttu-id="d96de-170">Les GUID de sous-type ont également été définis à partir de ces FOURCCs ; consultez [GUID de sous-type de vidéo](video-subtype-guids.md).</span><span class="sxs-lookup"><span data-stu-id="d96de-170">Subtype GUIDs have also been defined from these FOURCCs; see [Video Subtype GUIDs](video-subtype-guids.md).</span></span>

## <a name="surface-definitions"></a><span data-ttu-id="d96de-171">Définitions de surface</span><span class="sxs-lookup"><span data-stu-id="d96de-171">Surface Definitions</span></span>

<span data-ttu-id="d96de-172">Cette section décrit la disposition de la mémoire de chaque format.</span><span class="sxs-lookup"><span data-stu-id="d96de-172">This section describes the memory layout of each format.</span></span> <span data-ttu-id="d96de-173">Dans les descriptions qui suivent, le terme **mot** fait référence à une valeur de 16 bits Little-endian et le terme **DWORD** fait référence à une valeur de 32 bits Little-endian.</span><span class="sxs-lookup"><span data-stu-id="d96de-173">In the descriptions that follow, the term **WORD** refers to a little-endian 16-bit value, and the term **DWORD** refers to a little-endian 32-bit value.</span></span>

### <a name="420-formats"></a><span data-ttu-id="d96de-174">4:2:0 formats</span><span class="sxs-lookup"><span data-stu-id="d96de-174">4:2:0 Formats</span></span>

<span data-ttu-id="d96de-175">Deux formats 4:2:0 sont définis, avec les Codes FOURCC P016 et P010.</span><span class="sxs-lookup"><span data-stu-id="d96de-175">Two 4:2:0 formats are defined, with the FOURCC codes P016 and P010.</span></span> <span data-ttu-id="d96de-176">Ils partagent la même disposition en mémoire, mais P016 utilise 16 bits par canal et P010 utilise 10 bits par canal.</span><span class="sxs-lookup"><span data-stu-id="d96de-176">They share the same memory layout, but P016 uses 16 bits per channel and P010 uses 10 bits per channel.</span></span>

### <a name="p016-and-p010"></a><span data-ttu-id="d96de-177">P016 et P010</span><span class="sxs-lookup"><span data-stu-id="d96de-177">P016 and P010</span></span>

<span data-ttu-id="d96de-178">Dans ces deux formats, tous les échantillons Y apparaissent en premier dans la mémoire sous la forme d’un tableau de **mots** avec un nombre pair de lignes.</span><span class="sxs-lookup"><span data-stu-id="d96de-178">In these two formats, all Y samples appear first in memory as an array of **WORD** s with an even number of lines.</span></span> <span data-ttu-id="d96de-179">La largeur de la surface peut être supérieure à la largeur du plan Y.</span><span class="sxs-lookup"><span data-stu-id="d96de-179">The surface stride can be larger than the width of the Y plane.</span></span> <span data-ttu-id="d96de-180">Ce tableau est immédiatement suivi d’un tableau de **mots** qui contient des exemples entrelacés vous et V, comme indiqué dans le diagramme suivant.</span><span class="sxs-lookup"><span data-stu-id="d96de-180">This array is followed immediately by an array of **WORD** s that contains interleaved U and V samples, as shown in the following diagram.</span></span>

![Diagramme montrant la disposition des pixels P016 et P010](images/1e1c4d66-6172-4d3a-bd25-4b5caa67edcd.gif)

<span data-ttu-id="d96de-182">Si le tableau U-V combiné est adressé comme un tableau de **DWORD** s, le mot le moins significatif (LSW) contient la valeur U et le mot le plus significatif (MSW) contient la valeur V.</span><span class="sxs-lookup"><span data-stu-id="d96de-182">If the combined U-V array is addressed as an array of **DWORD** s, the least significant word (LSW) contains the U value and the most significant word (MSW) contains the V value.</span></span> <span data-ttu-id="d96de-183">La valeur Stride du plan U-V combiné est égale au Stride du plan Y.</span><span class="sxs-lookup"><span data-stu-id="d96de-183">The stride of the combined U-V plane is equal to the stride of the Y plane.</span></span> <span data-ttu-id="d96de-184">Le plan U-V comporte un demi-nombre de lignes comme plan Y.</span><span class="sxs-lookup"><span data-stu-id="d96de-184">The U-V plane has half as many lines as the Y plane.</span></span>

<span data-ttu-id="d96de-185">Ces deux formats sont les formats de pixel planaires 4:2:0 préférés pour les représentations YUV de plus grande précision.</span><span class="sxs-lookup"><span data-stu-id="d96de-185">These two formats are the preferred 4:2:0 planar pixel formats for higher precision YUV representations.</span></span> <span data-ttu-id="d96de-186">Ils sont censés être une exigence de terme intermédiaire pour les accélérateurs d’accélération vidéo DirectX (DXVA) qui prennent en charge la vidéo 4:2:0 10 bits ou 16 bits.</span><span class="sxs-lookup"><span data-stu-id="d96de-186">They are expected to be an intermediate-term requirement for DirectX Video Acceleration (DXVA) accelerators that support 10-bit or 16-bit 4:2:0 video.</span></span>

### <a name="422-formats"></a><span data-ttu-id="d96de-187">4:2:2 formats</span><span class="sxs-lookup"><span data-stu-id="d96de-187">4:2:2 Formats</span></span>

<span data-ttu-id="d96de-188">Quatre formats 4:2:2 sont définis, deux plans planaires et deux compressés.</span><span class="sxs-lookup"><span data-stu-id="d96de-188">Four 4:2:2 formats are defined, two planar and two packed.</span></span> <span data-ttu-id="d96de-189">Ils ont les Codes FOURCC suivants :</span><span class="sxs-lookup"><span data-stu-id="d96de-189">They have the following FOURCC codes:</span></span>

-   <span data-ttu-id="d96de-190">P216</span><span class="sxs-lookup"><span data-stu-id="d96de-190">P216</span></span>
-   <span data-ttu-id="d96de-191">P210</span><span class="sxs-lookup"><span data-stu-id="d96de-191">P210</span></span>
-   <span data-ttu-id="d96de-192">Y216</span><span class="sxs-lookup"><span data-stu-id="d96de-192">Y216</span></span>
-   <span data-ttu-id="d96de-193">Y210</span><span class="sxs-lookup"><span data-stu-id="d96de-193">Y210</span></span>

### <a name="p216-and-p210"></a><span data-ttu-id="d96de-194">P216 et P210</span><span class="sxs-lookup"><span data-stu-id="d96de-194">P216 and P210</span></span>

<span data-ttu-id="d96de-195">Dans ces deux formats planaires, tous les échantillons Y apparaissent en premier dans la mémoire sous la forme d’un tableau de **mots** avec un nombre pair de lignes.</span><span class="sxs-lookup"><span data-stu-id="d96de-195">In these two planar formats, all Y samples appear first in memory as an array of **WORD** s with an even number of lines.</span></span> <span data-ttu-id="d96de-196">La largeur de la surface peut être supérieure à la largeur du plan Y.</span><span class="sxs-lookup"><span data-stu-id="d96de-196">The surface stride can be larger than the width of the Y plane.</span></span> <span data-ttu-id="d96de-197">Ce tableau est immédiatement suivi d’un tableau de **mots** qui contient des exemples entrelacés vous et V, comme indiqué dans le diagramme suivant.</span><span class="sxs-lookup"><span data-stu-id="d96de-197">This array is followed immediately by an array of **WORD** s that contains interleaved U and V samples, as shown in the following diagram.</span></span>

![Diagramme montrant la disposition des pixels p216 et P210](images/ff672fef-218f-4722-b806-d06c77fe8cfa.gif)

<span data-ttu-id="d96de-199">Si le tableau U-V combiné est adressé comme un tableau de **DWORD** s, LSW contient la valeur U et le MSW contient la valeur V.</span><span class="sxs-lookup"><span data-stu-id="d96de-199">If the combined U-V array is addressed as an array of **DWORD** s, the LSW contains the U value and the MSW contains the V value.</span></span> <span data-ttu-id="d96de-200">La valeur Stride du plan U-V combiné est égale au Stride du plan Y.</span><span class="sxs-lookup"><span data-stu-id="d96de-200">The stride of the combined U-V plane is equal to the stride of the Y plane.</span></span> <span data-ttu-id="d96de-201">Le plan U-V a le même nombre de lignes que le plan Y.</span><span class="sxs-lookup"><span data-stu-id="d96de-201">The U-V plane has the same number of lines as the Y plane.</span></span>

<span data-ttu-id="d96de-202">Ces deux formats sont les formats de pixel planaires 4:2:2 préférés pour les représentations YUV de plus grande précision.</span><span class="sxs-lookup"><span data-stu-id="d96de-202">These two formats are the preferred 4:2:2 planar pixel formats for higher precision YUV representations.</span></span> <span data-ttu-id="d96de-203">Ils sont censés être une exigence de terme intermédiaire pour les accélérateurs d’accélération vidéo DirectX (DXVA) qui prennent en charge la vidéo 4:2:2 10 bits ou 16 bits.</span><span class="sxs-lookup"><span data-stu-id="d96de-203">They are expected to be an intermediate-term requirement for DirectX Video Acceleration (DXVA) accelerators that support 10-bit or 16-bit 4:2:2 video.</span></span>

### <a name="y216-and-y210"></a><span data-ttu-id="d96de-204">Y216 et Y210</span><span class="sxs-lookup"><span data-stu-id="d96de-204">Y216 and Y210</span></span>

<span data-ttu-id="d96de-205">Dans ces deux formats compactés, chaque paire de pixels est stockée sous la forme d’un tableau de quatre **mots**, comme indiqué dans l’illustration suivante.</span><span class="sxs-lookup"><span data-stu-id="d96de-205">In these two packed formats, each pair of pixels is stored as an array of four **WORD** s, as shown in the following illustration.</span></span>

![Diagramme montrant la disposition des pixels y216 et Y210.](images/6f68aeeb-18ca-48ee-82c4-5b79d5510e9f.gif)

<span data-ttu-id="d96de-207">Le premier **mot** du tableau contient le premier échantillon y dans la paire, le deuxième **mot** contient l’exemple U, le troisième **mot** contient le deuxième échantillon y et le quatrième **mot** contient l’exemple V.</span><span class="sxs-lookup"><span data-stu-id="d96de-207">The first **WORD** in the array contains the first Y sample in the pair, the second **WORD** contains the U sample, the third **WORD** contains the second Y sample, and the fourth **WORD** contains the V sample.</span></span>

<span data-ttu-id="d96de-208">Y210 est identique à Y216, sauf que chaque échantillon contient uniquement 10 bits de données significatives.</span><span class="sxs-lookup"><span data-stu-id="d96de-208">Y210 is identical to Y216 except that each sample contains only 10 bits of significant data.</span></span> <span data-ttu-id="d96de-209">Les 6 bits de poids faible sont définis sur zéro, comme décrit précédemment.</span><span class="sxs-lookup"><span data-stu-id="d96de-209">The least significant 6 bits are set to zero, as described previously.</span></span>

### <a name="444-formats"></a><span data-ttu-id="d96de-210">4:4:4 formats</span><span class="sxs-lookup"><span data-stu-id="d96de-210">4:4:4 Formats</span></span>

<span data-ttu-id="d96de-211">Deux formats 4:4:4 sont définis, avec les Codes FOURCC Y410 et Y416.</span><span class="sxs-lookup"><span data-stu-id="d96de-211">Two 4:4:4 formats are defined, with the FOURCC codes Y410 and Y416.</span></span> <span data-ttu-id="d96de-212">Les deux sont des formats compactés.</span><span class="sxs-lookup"><span data-stu-id="d96de-212">Both are packed formats.</span></span>

### <a name="y410"></a><span data-ttu-id="d96de-213">Y410</span><span class="sxs-lookup"><span data-stu-id="d96de-213">Y410</span></span>

<span data-ttu-id="d96de-214">Ce format est une représentation de 10 bits compressée qui comprend 2 bits d’alpha.</span><span class="sxs-lookup"><span data-stu-id="d96de-214">This format is a packed 10-bit representation that includes 2 bits of alpha.</span></span> <span data-ttu-id="d96de-215">Chaque pixel est encodé sous la forme d’une **valeur DWORD** unique avec la disposition de mémoire indiquée dans le diagramme suivant.</span><span class="sxs-lookup"><span data-stu-id="d96de-215">Each pixel is encoded as a single **DWORD** with the memory layout shown in the following diagram.</span></span>

![Diagramme montrant la disposition des pixels Y410.](images/f8a71437-e3f1-4331-be30-f766c028d648.gif)

<span data-ttu-id="d96de-217">Bits 0-9 contiennent l’exemple U, bits 10-19 contiennent l’échantillon Y, bits 20-29 contiennent l’exemple V et bits 30-31 contient la valeur alpha.</span><span class="sxs-lookup"><span data-stu-id="d96de-217">Bits 0-9 contain the U sample, bits 10-19 contain the Y sample, bits 20-29 contain the V sample, and bits 30-31 contain the alpha value.</span></span> <span data-ttu-id="d96de-218">Pour indiquer qu’un pixel est entièrement opaque, une application doit définir les deux bits alpha égaux à 0x03.</span><span class="sxs-lookup"><span data-stu-id="d96de-218">To indicate that a pixel is fully opaque, an application must set the two alpha bits equal to 0x03.</span></span>

### <a name="y416"></a><span data-ttu-id="d96de-219">Y416</span><span class="sxs-lookup"><span data-stu-id="d96de-219">Y416</span></span>

<span data-ttu-id="d96de-220">Ce format est une représentation 16 bits compressée qui comprend 16 bits d’alpha.</span><span class="sxs-lookup"><span data-stu-id="d96de-220">This format is a packed 16-bit representation that includes 16 bits of alpha.</span></span> <span data-ttu-id="d96de-221">Chaque pixel est encodé sous la forme d’une paire de **DWORD** s, comme indiqué dans l’illustration suivante.</span><span class="sxs-lookup"><span data-stu-id="d96de-221">Each pixel is encoded as a pair of **DWORD** s, as shown in the following illustration.</span></span>

![Diagramme montrant la disposition des pixels y416.](images/c928523a-25d3-4712-9aec-5b492b51435f.gif)

<span data-ttu-id="d96de-223">Bits 0-15 contiennent l’exemple U, bits 16-31 contiennent l’échantillon Y, bits 32-47 contiennent l’exemple V et bits 48-63 contient la valeur alpha.</span><span class="sxs-lookup"><span data-stu-id="d96de-223">Bits 0-15 contain the U sample, bits 16-31 contain the Y sample, bits 32-47 contain the V sample, and bits 48-63 contain the alpha value.</span></span>

<span data-ttu-id="d96de-224">Pour indiquer qu’un pixel est entièrement opaque, une application doit définir les deux bits alpha égaux à 0xFFFF.</span><span class="sxs-lookup"><span data-stu-id="d96de-224">To indicate that a pixel is fully opaque, an application must set the two alpha bits equal to 0xFFFF.</span></span> <span data-ttu-id="d96de-225">Ce format est principalement conçu comme un format intermédiaire lors du traitement de l’image afin d’éviter l’accumulation des erreurs.</span><span class="sxs-lookup"><span data-stu-id="d96de-225">This format is intended primarily as an intermediate format during image processing to avoid the accumulation of errors.</span></span>

## <a name="preferred-yuv-formats"></a><span data-ttu-id="d96de-226">Formats YUV préférés</span><span class="sxs-lookup"><span data-stu-id="d96de-226">Preferred YUV Formats</span></span>

<span data-ttu-id="d96de-227">Le tableau suivant répertorie les formats YUV préférés, y compris les formats 8 bits.</span><span class="sxs-lookup"><span data-stu-id="d96de-227">The following table lists the preferred YUV formats, including 8-bit formats.</span></span>



| <span data-ttu-id="d96de-228">Format</span><span class="sxs-lookup"><span data-stu-id="d96de-228">Format</span></span> | <span data-ttu-id="d96de-229">Échantillonnage Chroma</span><span class="sxs-lookup"><span data-stu-id="d96de-229">Chroma sampling</span></span> | <span data-ttu-id="d96de-230">Condensé ou planaire</span><span class="sxs-lookup"><span data-stu-id="d96de-230">Packed or planar</span></span> | <span data-ttu-id="d96de-231">Bits par canal</span><span class="sxs-lookup"><span data-stu-id="d96de-231">Bits per channel</span></span> |
|--------|-----------------|------------------|------------------|
| <span data-ttu-id="d96de-232">AYUV</span><span class="sxs-lookup"><span data-stu-id="d96de-232">AYUV</span></span>   | <span data-ttu-id="d96de-233">4:4:4</span><span class="sxs-lookup"><span data-stu-id="d96de-233">4:4:4</span></span>           | <span data-ttu-id="d96de-234">Riche</span><span class="sxs-lookup"><span data-stu-id="d96de-234">Packed</span></span>           | <span data-ttu-id="d96de-235">8</span><span class="sxs-lookup"><span data-stu-id="d96de-235">8</span></span>                |
| <span data-ttu-id="d96de-236">Y410</span><span class="sxs-lookup"><span data-stu-id="d96de-236">Y410</span></span>   | <span data-ttu-id="d96de-237">4:4:4</span><span class="sxs-lookup"><span data-stu-id="d96de-237">4:4:4</span></span>           | <span data-ttu-id="d96de-238">Riche</span><span class="sxs-lookup"><span data-stu-id="d96de-238">Packed</span></span>           | <span data-ttu-id="d96de-239">10</span><span class="sxs-lookup"><span data-stu-id="d96de-239">10</span></span>               |
| <span data-ttu-id="d96de-240">Y416</span><span class="sxs-lookup"><span data-stu-id="d96de-240">Y416</span></span>   | <span data-ttu-id="d96de-241">4:4:4</span><span class="sxs-lookup"><span data-stu-id="d96de-241">4:4:4</span></span>           | <span data-ttu-id="d96de-242">Riche</span><span class="sxs-lookup"><span data-stu-id="d96de-242">Packed</span></span>           | <span data-ttu-id="d96de-243">16</span><span class="sxs-lookup"><span data-stu-id="d96de-243">16</span></span>               |
| <span data-ttu-id="d96de-244">AI44</span><span class="sxs-lookup"><span data-stu-id="d96de-244">AI44</span></span>   | <span data-ttu-id="d96de-245">4:4:4</span><span class="sxs-lookup"><span data-stu-id="d96de-245">4:4:4</span></span>           | <span data-ttu-id="d96de-246">Riche</span><span class="sxs-lookup"><span data-stu-id="d96de-246">Packed</span></span>           | <span data-ttu-id="d96de-247">En palette</span><span class="sxs-lookup"><span data-stu-id="d96de-247">Palettized</span></span>       |
| <span data-ttu-id="d96de-248">YUY2</span><span class="sxs-lookup"><span data-stu-id="d96de-248">YUY2</span></span>   | <span data-ttu-id="d96de-249">4:2:2</span><span class="sxs-lookup"><span data-stu-id="d96de-249">4:2:2</span></span>           | <span data-ttu-id="d96de-250">Riche</span><span class="sxs-lookup"><span data-stu-id="d96de-250">Packed</span></span>           | <span data-ttu-id="d96de-251">8</span><span class="sxs-lookup"><span data-stu-id="d96de-251">8</span></span>                |
| <span data-ttu-id="d96de-252">Y210</span><span class="sxs-lookup"><span data-stu-id="d96de-252">Y210</span></span>   | <span data-ttu-id="d96de-253">4:2:2</span><span class="sxs-lookup"><span data-stu-id="d96de-253">4:2:2</span></span>           | <span data-ttu-id="d96de-254">Riche</span><span class="sxs-lookup"><span data-stu-id="d96de-254">Packed</span></span>           | <span data-ttu-id="d96de-255">10</span><span class="sxs-lookup"><span data-stu-id="d96de-255">10</span></span>               |
| <span data-ttu-id="d96de-256">Y216</span><span class="sxs-lookup"><span data-stu-id="d96de-256">Y216</span></span>   | <span data-ttu-id="d96de-257">4:2:2</span><span class="sxs-lookup"><span data-stu-id="d96de-257">4:2:2</span></span>           | <span data-ttu-id="d96de-258">Riche</span><span class="sxs-lookup"><span data-stu-id="d96de-258">Packed</span></span>           | <span data-ttu-id="d96de-259">16</span><span class="sxs-lookup"><span data-stu-id="d96de-259">16</span></span>               |
| <span data-ttu-id="d96de-260">P210</span><span class="sxs-lookup"><span data-stu-id="d96de-260">P210</span></span>   | <span data-ttu-id="d96de-261">4:2:2</span><span class="sxs-lookup"><span data-stu-id="d96de-261">4:2:2</span></span>           | <span data-ttu-id="d96de-262">Planaire</span><span class="sxs-lookup"><span data-stu-id="d96de-262">Planar</span></span>           | <span data-ttu-id="d96de-263">10</span><span class="sxs-lookup"><span data-stu-id="d96de-263">10</span></span>               |
| <span data-ttu-id="d96de-264">P216</span><span class="sxs-lookup"><span data-stu-id="d96de-264">P216</span></span>   | <span data-ttu-id="d96de-265">4:2:2</span><span class="sxs-lookup"><span data-stu-id="d96de-265">4:2:2</span></span>           | <span data-ttu-id="d96de-266">Planaire</span><span class="sxs-lookup"><span data-stu-id="d96de-266">Planar</span></span>           | <span data-ttu-id="d96de-267">16</span><span class="sxs-lookup"><span data-stu-id="d96de-267">16</span></span>               |
| <span data-ttu-id="d96de-268">NV12</span><span class="sxs-lookup"><span data-stu-id="d96de-268">NV12</span></span>   | <span data-ttu-id="d96de-269">4:2:0</span><span class="sxs-lookup"><span data-stu-id="d96de-269">4:2:0</span></span>           | <span data-ttu-id="d96de-270">Planaire</span><span class="sxs-lookup"><span data-stu-id="d96de-270">Planar</span></span>           | <span data-ttu-id="d96de-271">8</span><span class="sxs-lookup"><span data-stu-id="d96de-271">8</span></span>                |
| <span data-ttu-id="d96de-272">P010</span><span class="sxs-lookup"><span data-stu-id="d96de-272">P010</span></span>   | <span data-ttu-id="d96de-273">4:2:0</span><span class="sxs-lookup"><span data-stu-id="d96de-273">4:2:0</span></span>           | <span data-ttu-id="d96de-274">Planaire</span><span class="sxs-lookup"><span data-stu-id="d96de-274">Planar</span></span>           | <span data-ttu-id="d96de-275">10</span><span class="sxs-lookup"><span data-stu-id="d96de-275">10</span></span>               |
| <span data-ttu-id="d96de-276">P016</span><span class="sxs-lookup"><span data-stu-id="d96de-276">P016</span></span>   | <span data-ttu-id="d96de-277">4:2:0</span><span class="sxs-lookup"><span data-stu-id="d96de-277">4:2:0</span></span>           | <span data-ttu-id="d96de-278">Planaire</span><span class="sxs-lookup"><span data-stu-id="d96de-278">Planar</span></span>           | <span data-ttu-id="d96de-279">16</span><span class="sxs-lookup"><span data-stu-id="d96de-279">16</span></span>               |
| <span data-ttu-id="d96de-280">NV11</span><span class="sxs-lookup"><span data-stu-id="d96de-280">NV11</span></span>   | <span data-ttu-id="d96de-281">4:1:1</span><span class="sxs-lookup"><span data-stu-id="d96de-281">4:1:1</span></span>           | <span data-ttu-id="d96de-282">Planaire</span><span class="sxs-lookup"><span data-stu-id="d96de-282">Planar</span></span>           | <span data-ttu-id="d96de-283">8</span><span class="sxs-lookup"><span data-stu-id="d96de-283">8</span></span>                |



 

<span data-ttu-id="d96de-284">Si un objet prend en charge un schéma d’échantillonnage couleur et de profondeur de bits donné, il est recommandé de prendre en charge les formats YUV correspondants listés dans ce tableau.</span><span class="sxs-lookup"><span data-stu-id="d96de-284">It is recommended that if an object supports a given bit depth and chroma sampling scheme, it should support the corresponding YUV formats listed in this table.</span></span> <span data-ttu-id="d96de-285">(Les objets peuvent prendre en charge des formats supplémentaires non répertoriés ici.)</span><span class="sxs-lookup"><span data-stu-id="d96de-285">(Objects might support additional formats not listed here.)</span></span>

## <a name="related-topics"></a><span data-ttu-id="d96de-286">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="d96de-286">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d96de-287">Formats YUV 8 bits recommandés pour le rendu vidéo</span><span class="sxs-lookup"><span data-stu-id="d96de-287">Recommended 8-Bit YUV Formats for Video Rendering</span></span>](recommended-8-bit-yuv-formats-for-video-rendering.md)
</dt> <dt>

[<span data-ttu-id="d96de-288">GUID de sous-type de vidéo</span><span class="sxs-lookup"><span data-stu-id="d96de-288">Video Subtype GUIDs</span></span>](video-subtype-guids.md)
</dt> <dt>

[<span data-ttu-id="d96de-289">Types de média vidéo</span><span class="sxs-lookup"><span data-stu-id="d96de-289">Video Media Types</span></span>](video-media-types.md)
</dt> </dl>

 

 



