---
description: Cette section répertorie les codes d’opération Raster binaires utilisés par les fonctions GetROP2 et SetROP2. Les codes d’opération Raster définissent la façon dont GDI combine les bits du stylet sélectionné avec les bits dans le bitmap de destination.
ms.assetid: 9a3a5b5d-b41f-4859-8830-98272983a635
title: Opérations raster binaires
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd8a70030b1940c31d036505a80a6b1868aececd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114739"
---
# <a name="binary-raster-operations"></a><span data-ttu-id="f310d-104">Opérations raster binaires</span><span class="sxs-lookup"><span data-stu-id="f310d-104">Binary Raster Operations</span></span>

<span data-ttu-id="f310d-105">Cette section répertorie les codes d’opération Raster binaires utilisés par les fonctions [**GetROP2**](/windows/desktop/api/Wingdi/nf-wingdi-getrop2) et [**SetROP2**](/windows/desktop/api/Wingdi/nf-wingdi-setrop2) .</span><span class="sxs-lookup"><span data-stu-id="f310d-105">This section lists the binary raster-operation codes used by the [**GetROP2**](/windows/desktop/api/Wingdi/nf-wingdi-getrop2) and [**SetROP2**](/windows/desktop/api/Wingdi/nf-wingdi-setrop2) functions.</span></span> <span data-ttu-id="f310d-106">Les codes d’opération Raster définissent la façon dont GDI combine les bits du stylet sélectionné avec les bits dans le bitmap de destination.</span><span class="sxs-lookup"><span data-stu-id="f310d-106">Raster-operation codes define how GDI combines the bits from the selected pen with the bits in the destination bitmap.</span></span>

<span data-ttu-id="f310d-107">Chaque code d’opération Raster représente une opération booléenne dans laquelle les valeurs des pixels dans le stylet sélectionné et le bitmap de destination sont combinées.</span><span class="sxs-lookup"><span data-stu-id="f310d-107">Each raster-operation code represents a Boolean operation in which the values of the pixels in the selected pen and the destination bitmap are combined.</span></span> <span data-ttu-id="f310d-108">Voici les deux opérandes utilisés dans ces opérations.</span><span class="sxs-lookup"><span data-stu-id="f310d-108">The following are the two operands used in these operations.</span></span>



| <span data-ttu-id="f310d-109">Opérande</span><span class="sxs-lookup"><span data-stu-id="f310d-109">Operand</span></span> | <span data-ttu-id="f310d-110">Signification</span><span class="sxs-lookup"><span data-stu-id="f310d-110">Meaning</span></span>            |
|---------|--------------------|
| <span data-ttu-id="f310d-111">P</span><span class="sxs-lookup"><span data-stu-id="f310d-111">P</span></span>       | <span data-ttu-id="f310d-112">Stylo sélectionné</span><span class="sxs-lookup"><span data-stu-id="f310d-112">Selected pen</span></span>       |
| <span data-ttu-id="f310d-113">D</span><span class="sxs-lookup"><span data-stu-id="f310d-113">D</span></span>       | <span data-ttu-id="f310d-114">Bitmap de destination</span><span class="sxs-lookup"><span data-stu-id="f310d-114">Destination bitmap</span></span> |



 

<span data-ttu-id="f310d-115">Les opérateurs booléens utilisés dans ces opérations suivent.</span><span class="sxs-lookup"><span data-stu-id="f310d-115">The Boolean operators used in these operations follow.</span></span>



| <span data-ttu-id="f310d-116">Opérateur</span><span class="sxs-lookup"><span data-stu-id="f310d-116">Operator</span></span> | <span data-ttu-id="f310d-117">Signification</span><span class="sxs-lookup"><span data-stu-id="f310d-117">Meaning</span></span>                    |
|----------|----------------------------|
| <span data-ttu-id="f310d-118">a</span><span class="sxs-lookup"><span data-stu-id="f310d-118">a</span></span>        | <span data-ttu-id="f310d-119">ET au niveau du bit</span><span class="sxs-lookup"><span data-stu-id="f310d-119">Bitwise AND</span></span>                |
| <span data-ttu-id="f310d-120">n</span><span class="sxs-lookup"><span data-stu-id="f310d-120">n</span></span>        | <span data-ttu-id="f310d-121">NOT au niveau du bit (inverse)</span><span class="sxs-lookup"><span data-stu-id="f310d-121">Bitwise NOT (inverse)</span></span>      |
| <span data-ttu-id="f310d-122">o</span><span class="sxs-lookup"><span data-stu-id="f310d-122">o</span></span>        | <span data-ttu-id="f310d-123">Opération de bits OR</span><span class="sxs-lookup"><span data-stu-id="f310d-123">Bitwise OR</span></span>                 |
| <span data-ttu-id="f310d-124">x</span><span class="sxs-lookup"><span data-stu-id="f310d-124">x</span></span>        | <span data-ttu-id="f310d-125">Or exclusif au niveau du bit (XOR)</span><span class="sxs-lookup"><span data-stu-id="f310d-125">Bitwise exclusive OR (XOR)</span></span> |



 

<span data-ttu-id="f310d-126">Toutes les opérations booléennes sont présentées en notation polonais inverse.</span><span class="sxs-lookup"><span data-stu-id="f310d-126">All Boolean operations are presented in reverse Polish notation.</span></span> <span data-ttu-id="f310d-127">Par exemple, l’opération suivante remplace les valeurs des pixels de l’image bitmap de destination par une combinaison des valeurs de pixel du stylet et du pinceau sélectionné :</span><span class="sxs-lookup"><span data-stu-id="f310d-127">For example, the following operation replaces the values of the pixels in the destination bitmap with a combination of the pixel values of the pen and the selected brush:</span></span>


```C++
DPo 
```



<span data-ttu-id="f310d-128">Chaque code d’opération Raster est un entier 32 bits dont le mot de poids fort est un index d’opération booléen et dont le mot de poids faible est le code d’opération.</span><span class="sxs-lookup"><span data-stu-id="f310d-128">Each raster-operation code is a 32-bit integer whose high-order word is a Boolean operation index and whose low-order word is the operation code.</span></span> <span data-ttu-id="f310d-129">L’index d’opération 16 bits est une valeur 8 bits étendue de zéro qui représente tous les résultats possibles résultant de l’opération booléenne sur deux paramètres (dans ce cas, les valeurs de stylet et de destination).</span><span class="sxs-lookup"><span data-stu-id="f310d-129">The 16-bit operation index is a zero-extended 8-bit value that represents all possible outcomes resulting from the Boolean operation on two parameters (in this case, the pen and destination values).</span></span> <span data-ttu-id="f310d-130">Par exemple, les index d’opération pour les opérations DPo et DPan sont affichés dans la liste suivante.</span><span class="sxs-lookup"><span data-stu-id="f310d-130">For example, the operation indexes for the DPo and DPan operations are shown in the following list.</span></span>



| <span data-ttu-id="f310d-131">P</span><span class="sxs-lookup"><span data-stu-id="f310d-131">P</span></span>   | <span data-ttu-id="f310d-132">D</span><span class="sxs-lookup"><span data-stu-id="f310d-132">D</span></span>   | <span data-ttu-id="f310d-133">DPo</span><span class="sxs-lookup"><span data-stu-id="f310d-133">DPo</span></span> | <span data-ttu-id="f310d-134">Dpan</span><span class="sxs-lookup"><span data-stu-id="f310d-134">Dpan</span></span> |
|-----|-----|-----|------|
| <span data-ttu-id="f310d-135">0</span><span class="sxs-lookup"><span data-stu-id="f310d-135">0</span></span>   | <span data-ttu-id="f310d-136">0</span><span class="sxs-lookup"><span data-stu-id="f310d-136">0</span></span>   | <span data-ttu-id="f310d-137">0</span><span class="sxs-lookup"><span data-stu-id="f310d-137">0</span></span>   | <span data-ttu-id="f310d-138">1</span><span class="sxs-lookup"><span data-stu-id="f310d-138">1</span></span>    |
| <span data-ttu-id="f310d-139">0</span><span class="sxs-lookup"><span data-stu-id="f310d-139">0</span></span>   | <span data-ttu-id="f310d-140">1</span><span class="sxs-lookup"><span data-stu-id="f310d-140">1</span></span>   | <span data-ttu-id="f310d-141">1</span><span class="sxs-lookup"><span data-stu-id="f310d-141">1</span></span>   | <span data-ttu-id="f310d-142">1</span><span class="sxs-lookup"><span data-stu-id="f310d-142">1</span></span>    |
| <span data-ttu-id="f310d-143">1</span><span class="sxs-lookup"><span data-stu-id="f310d-143">1</span></span>   | <span data-ttu-id="f310d-144">0</span><span class="sxs-lookup"><span data-stu-id="f310d-144">0</span></span>   | <span data-ttu-id="f310d-145">1</span><span class="sxs-lookup"><span data-stu-id="f310d-145">1</span></span>   | <span data-ttu-id="f310d-146">1</span><span class="sxs-lookup"><span data-stu-id="f310d-146">1</span></span>    |
| <span data-ttu-id="f310d-147">1</span><span class="sxs-lookup"><span data-stu-id="f310d-147">1</span></span>   | <span data-ttu-id="f310d-148">1</span><span class="sxs-lookup"><span data-stu-id="f310d-148">1</span></span>   | <span data-ttu-id="f310d-149">1</span><span class="sxs-lookup"><span data-stu-id="f310d-149">1</span></span>   | <span data-ttu-id="f310d-150">0</span><span class="sxs-lookup"><span data-stu-id="f310d-150">0</span></span>    |



 

<span data-ttu-id="f310d-151">La liste suivante présente les modes de dessin et les opérations booléennes qu’ils représentent.</span><span class="sxs-lookup"><span data-stu-id="f310d-151">The following list outlines the drawing modes and the Boolean operations that they represent.</span></span>



| <span data-ttu-id="f310d-152">Opération Raster</span><span class="sxs-lookup"><span data-stu-id="f310d-152">Raster operation</span></span> | <span data-ttu-id="f310d-153">Opération booléenne</span><span class="sxs-lookup"><span data-stu-id="f310d-153">Boolean operation</span></span> |
|------------------|-------------------|
| <span data-ttu-id="f310d-154">R2 \_ noir</span><span class="sxs-lookup"><span data-stu-id="f310d-154">R2\_BLACK</span></span>        | <span data-ttu-id="f310d-155">0</span><span class="sxs-lookup"><span data-stu-id="f310d-155">0</span></span>                 |
| <span data-ttu-id="f310d-156">\_COPYPEN R2</span><span class="sxs-lookup"><span data-stu-id="f310d-156">R2\_COPYPEN</span></span>      | <span data-ttu-id="f310d-157">P</span><span class="sxs-lookup"><span data-stu-id="f310d-157">P</span></span>                 |
| <span data-ttu-id="f310d-158">\_MASKNOTPEN R2</span><span class="sxs-lookup"><span data-stu-id="f310d-158">R2\_MASKNOTPEN</span></span>   | <span data-ttu-id="f310d-159">DPna</span><span class="sxs-lookup"><span data-stu-id="f310d-159">DPna</span></span>              |
| <span data-ttu-id="f310d-160">\_MASKPEN R2</span><span class="sxs-lookup"><span data-stu-id="f310d-160">R2\_MASKPEN</span></span>      | <span data-ttu-id="f310d-161">DPa</span><span class="sxs-lookup"><span data-stu-id="f310d-161">DPa</span></span>               |
| <span data-ttu-id="f310d-162">\_MASKPENNOT R2</span><span class="sxs-lookup"><span data-stu-id="f310d-162">R2\_MASKPENNOT</span></span>   | <span data-ttu-id="f310d-163">PDna</span><span class="sxs-lookup"><span data-stu-id="f310d-163">PDna</span></span>              |
| <span data-ttu-id="f310d-164">\_MERGENOTPEN R2</span><span class="sxs-lookup"><span data-stu-id="f310d-164">R2\_MERGENOTPEN</span></span>  | <span data-ttu-id="f310d-165">DPno</span><span class="sxs-lookup"><span data-stu-id="f310d-165">DPno</span></span>              |
| <span data-ttu-id="f310d-166">\_MERGEPEN R2</span><span class="sxs-lookup"><span data-stu-id="f310d-166">R2\_MERGEPEN</span></span>     | <span data-ttu-id="f310d-167">DPo</span><span class="sxs-lookup"><span data-stu-id="f310d-167">DPo</span></span>               |
| <span data-ttu-id="f310d-168">\_MERGEPENNOT R2</span><span class="sxs-lookup"><span data-stu-id="f310d-168">R2\_MERGEPENNOT</span></span>  | <span data-ttu-id="f310d-169">PDno</span><span class="sxs-lookup"><span data-stu-id="f310d-169">PDno</span></span>              |
| <span data-ttu-id="f310d-170">R2 \_ NOP</span><span class="sxs-lookup"><span data-stu-id="f310d-170">R2\_NOP</span></span>          | <span data-ttu-id="f310d-171">D</span><span class="sxs-lookup"><span data-stu-id="f310d-171">D</span></span>                 |
| <span data-ttu-id="f310d-172">R2 \_ non</span><span class="sxs-lookup"><span data-stu-id="f310d-172">R2\_NOT</span></span>          | <span data-ttu-id="f310d-173">Nom unique</span><span class="sxs-lookup"><span data-stu-id="f310d-173">Dn</span></span>                |
| <span data-ttu-id="f310d-174">\_NOTCOPYPEN R2</span><span class="sxs-lookup"><span data-stu-id="f310d-174">R2\_NOTCOPYPEN</span></span>   | <span data-ttu-id="f310d-175">PN</span><span class="sxs-lookup"><span data-stu-id="f310d-175">Pn</span></span>                |
| <span data-ttu-id="f310d-176">\_NOTMASKPEN R2</span><span class="sxs-lookup"><span data-stu-id="f310d-176">R2\_NOTMASKPEN</span></span>   | <span data-ttu-id="f310d-177">DPan</span><span class="sxs-lookup"><span data-stu-id="f310d-177">DPan</span></span>              |
| <span data-ttu-id="f310d-178">\_NOTMERGEPEN R2</span><span class="sxs-lookup"><span data-stu-id="f310d-178">R2\_NOTMERGEPEN</span></span>  | <span data-ttu-id="f310d-179">DPon</span><span class="sxs-lookup"><span data-stu-id="f310d-179">DPon</span></span>              |
| <span data-ttu-id="f310d-180">\_NOTXORPEN R2</span><span class="sxs-lookup"><span data-stu-id="f310d-180">R2\_NOTXORPEN</span></span>    | <span data-ttu-id="f310d-181">DPxn</span><span class="sxs-lookup"><span data-stu-id="f310d-181">DPxn</span></span>              |
| <span data-ttu-id="f310d-182">\_Blanc R2</span><span class="sxs-lookup"><span data-stu-id="f310d-182">R2\_WHITE</span></span>        | <span data-ttu-id="f310d-183">1</span><span class="sxs-lookup"><span data-stu-id="f310d-183">1</span></span>                 |
| <span data-ttu-id="f310d-184">\_XORPEN R2</span><span class="sxs-lookup"><span data-stu-id="f310d-184">R2\_XORPEN</span></span>       | <span data-ttu-id="f310d-185">DPx</span><span class="sxs-lookup"><span data-stu-id="f310d-185">DPx</span></span>               |



 

<span data-ttu-id="f310d-186">Pour un appareil monochrome, GDI mappe la valeur de zéro au noir et la valeur 1 à blanc.</span><span class="sxs-lookup"><span data-stu-id="f310d-186">For a monochrome device, GDI maps the value zero to black and the value 1 to white.</span></span> <span data-ttu-id="f310d-187">Si une application tente de dessiner avec un stylet noir sur une destination blanche à l’aide des opérations raster binaires disponibles, les résultats suivants se produisent.</span><span class="sxs-lookup"><span data-stu-id="f310d-187">If an application attempts to draw with a black pen on a white destination by using the available binary raster operations, the following results occur.</span></span>



| <span data-ttu-id="f310d-188">Opération Raster</span><span class="sxs-lookup"><span data-stu-id="f310d-188">Raster operation</span></span> | <span data-ttu-id="f310d-189">Résultats</span><span class="sxs-lookup"><span data-stu-id="f310d-189">Result</span></span>             |
|------------------|--------------------|
| <span data-ttu-id="f310d-190">R2 \_ noir</span><span class="sxs-lookup"><span data-stu-id="f310d-190">R2\_BLACK</span></span>        | <span data-ttu-id="f310d-191">Ligne noire visible</span><span class="sxs-lookup"><span data-stu-id="f310d-191">Visible black line</span></span> |
| <span data-ttu-id="f310d-192">\_COPYPEN R2</span><span class="sxs-lookup"><span data-stu-id="f310d-192">R2\_COPYPEN</span></span>      | <span data-ttu-id="f310d-193">Ligne noire visible</span><span class="sxs-lookup"><span data-stu-id="f310d-193">Visible black line</span></span> |
| <span data-ttu-id="f310d-194">\_MASKNOTPEN R2</span><span class="sxs-lookup"><span data-stu-id="f310d-194">R2\_MASKNOTPEN</span></span>   | <span data-ttu-id="f310d-195">Aucune ligne visible</span><span class="sxs-lookup"><span data-stu-id="f310d-195">No visible line</span></span>    |
| <span data-ttu-id="f310d-196">\_MASKPEN R2</span><span class="sxs-lookup"><span data-stu-id="f310d-196">R2\_MASKPEN</span></span>      | <span data-ttu-id="f310d-197">Ligne noire visible</span><span class="sxs-lookup"><span data-stu-id="f310d-197">Visible black line</span></span> |
| <span data-ttu-id="f310d-198">\_MASKPENNOT R2</span><span class="sxs-lookup"><span data-stu-id="f310d-198">R2\_MASKPENNOT</span></span>   | <span data-ttu-id="f310d-199">Ligne noire visible</span><span class="sxs-lookup"><span data-stu-id="f310d-199">Visible black line</span></span> |
| <span data-ttu-id="f310d-200">\_MERGENOTPEN R2</span><span class="sxs-lookup"><span data-stu-id="f310d-200">R2\_MERGENOTPEN</span></span>  | <span data-ttu-id="f310d-201">Aucune ligne visible</span><span class="sxs-lookup"><span data-stu-id="f310d-201">No visible line</span></span>    |
| <span data-ttu-id="f310d-202">\_MERGEPEN R2</span><span class="sxs-lookup"><span data-stu-id="f310d-202">R2\_MERGEPEN</span></span>     | <span data-ttu-id="f310d-203">Ligne noire visible</span><span class="sxs-lookup"><span data-stu-id="f310d-203">Visible black line</span></span> |
| <span data-ttu-id="f310d-204">\_MERGEPENNOT R2</span><span class="sxs-lookup"><span data-stu-id="f310d-204">R2\_MERGEPENNOT</span></span>  | <span data-ttu-id="f310d-205">Ligne noire visible</span><span class="sxs-lookup"><span data-stu-id="f310d-205">Visible black line</span></span> |
| <span data-ttu-id="f310d-206">R2 \_ NOP</span><span class="sxs-lookup"><span data-stu-id="f310d-206">R2\_NOP</span></span>          | <span data-ttu-id="f310d-207">Aucune ligne visible</span><span class="sxs-lookup"><span data-stu-id="f310d-207">No visible line</span></span>    |
| <span data-ttu-id="f310d-208">R2 \_ non</span><span class="sxs-lookup"><span data-stu-id="f310d-208">R2\_NOT</span></span>          | <span data-ttu-id="f310d-209">Ligne noire visible</span><span class="sxs-lookup"><span data-stu-id="f310d-209">Visible black line</span></span> |
| <span data-ttu-id="f310d-210">\_NOTCOPYPEN R2</span><span class="sxs-lookup"><span data-stu-id="f310d-210">R2\_NOTCOPYPEN</span></span>   | <span data-ttu-id="f310d-211">Aucune ligne visible</span><span class="sxs-lookup"><span data-stu-id="f310d-211">No visible line</span></span>    |
| <span data-ttu-id="f310d-212">\_NOTMASKPEN R2</span><span class="sxs-lookup"><span data-stu-id="f310d-212">R2\_NOTMASKPEN</span></span>   | <span data-ttu-id="f310d-213">Aucune ligne visible</span><span class="sxs-lookup"><span data-stu-id="f310d-213">No visible line</span></span>    |
| <span data-ttu-id="f310d-214">\_NOTMERGEPEN R2</span><span class="sxs-lookup"><span data-stu-id="f310d-214">R2\_NOTMERGEPEN</span></span>  | <span data-ttu-id="f310d-215">Ligne noire visible</span><span class="sxs-lookup"><span data-stu-id="f310d-215">Visible black line</span></span> |
| <span data-ttu-id="f310d-216">\_NOTXORPEN R2</span><span class="sxs-lookup"><span data-stu-id="f310d-216">R2\_NOTXORPEN</span></span>    | <span data-ttu-id="f310d-217">Ligne noire visible</span><span class="sxs-lookup"><span data-stu-id="f310d-217">Visible black line</span></span> |
| <span data-ttu-id="f310d-218">\_Blanc R2</span><span class="sxs-lookup"><span data-stu-id="f310d-218">R2\_WHITE</span></span>        | <span data-ttu-id="f310d-219">Aucune ligne visible</span><span class="sxs-lookup"><span data-stu-id="f310d-219">No visible line</span></span>    |
| <span data-ttu-id="f310d-220">\_XORPEN R2</span><span class="sxs-lookup"><span data-stu-id="f310d-220">R2\_XORPEN</span></span>       | <span data-ttu-id="f310d-221">Aucune ligne visible</span><span class="sxs-lookup"><span data-stu-id="f310d-221">No visible line</span></span>    |



 

<span data-ttu-id="f310d-222">Pour un périphérique de couleur, GDI utilise des valeurs RVB pour représenter les couleurs du stylet et de la destination.</span><span class="sxs-lookup"><span data-stu-id="f310d-222">For a color device, GDI uses RGB values to represent the colors of the pen and the destination.</span></span> <span data-ttu-id="f310d-223">Une valeur de couleur RVB est un entier long qui contient un champ de couleur rouge, vert et bleu, chacun spécifiant l’intensité de la couleur spécifiée.</span><span class="sxs-lookup"><span data-stu-id="f310d-223">An RGB color value is a long integer that contains a red, a green, and a blue color field, each specifying the intensity of the specified color.</span></span> <span data-ttu-id="f310d-224">Les intensités sont comprises entre 0 et 255.</span><span class="sxs-lookup"><span data-stu-id="f310d-224">Intensities range from 0 through 255.</span></span> <span data-ttu-id="f310d-225">Les valeurs sont compressées dans les trois octets de poids faible de l’entier long.</span><span class="sxs-lookup"><span data-stu-id="f310d-225">The values are packed in the three low-order bytes of the long integer.</span></span> <span data-ttu-id="f310d-226">La couleur d’un stylet est toujours une couleur unie, mais la couleur de la destination peut être un mélange de deux ou trois couleurs.</span><span class="sxs-lookup"><span data-stu-id="f310d-226">The color of a pen is always a solid color, but the color of the destination may be a mixture of any two or three colors.</span></span> <span data-ttu-id="f310d-227">Si une application tente de dessiner avec un stylet blanc sur une destination bleue à l’aide des opérations raster binaires disponibles, les résultats suivants se produisent.</span><span class="sxs-lookup"><span data-stu-id="f310d-227">If an application attempts to draw with a white pen on a blue destination by using the available binary raster operations, the following results occur.</span></span>



| <span data-ttu-id="f310d-228">Opération Raster</span><span class="sxs-lookup"><span data-stu-id="f310d-228">Raster operation</span></span> | <span data-ttu-id="f310d-229">Résultats</span><span class="sxs-lookup"><span data-stu-id="f310d-229">Result</span></span>                 |
|------------------|------------------------|
| <span data-ttu-id="f310d-230">R2 \_ noir</span><span class="sxs-lookup"><span data-stu-id="f310d-230">R2\_BLACK</span></span>        | <span data-ttu-id="f310d-231">Ligne noire visible</span><span class="sxs-lookup"><span data-stu-id="f310d-231">Visible black line</span></span>     |
| <span data-ttu-id="f310d-232">\_COPYPEN R2</span><span class="sxs-lookup"><span data-stu-id="f310d-232">R2\_COPYPEN</span></span>      | <span data-ttu-id="f310d-233">Ligne blanche visible</span><span class="sxs-lookup"><span data-stu-id="f310d-233">Visible white line</span></span>     |
| <span data-ttu-id="f310d-234">\_MASKNOTPEN R2</span><span class="sxs-lookup"><span data-stu-id="f310d-234">R2\_MASKNOTPEN</span></span>   | <span data-ttu-id="f310d-235">Ligne noire visible</span><span class="sxs-lookup"><span data-stu-id="f310d-235">Visible black line</span></span>     |
| <span data-ttu-id="f310d-236">\_MASKPEN R2</span><span class="sxs-lookup"><span data-stu-id="f310d-236">R2\_MASKPEN</span></span>      | <span data-ttu-id="f310d-237">Ligne bleue invisible</span><span class="sxs-lookup"><span data-stu-id="f310d-237">Invisible blue line</span></span>    |
| <span data-ttu-id="f310d-238">\_MASKPENNOT R2</span><span class="sxs-lookup"><span data-stu-id="f310d-238">R2\_MASKPENNOT</span></span>   | <span data-ttu-id="f310d-239">Trait rouge/vert visible</span><span class="sxs-lookup"><span data-stu-id="f310d-239">Visible red/green line</span></span> |
| <span data-ttu-id="f310d-240">\_MERGENOTPEN R2</span><span class="sxs-lookup"><span data-stu-id="f310d-240">R2\_MERGENOTPEN</span></span>  | <span data-ttu-id="f310d-241">Ligne bleue invisible</span><span class="sxs-lookup"><span data-stu-id="f310d-241">Invisible blue line</span></span>    |
| <span data-ttu-id="f310d-242">\_MERGEPEN R2</span><span class="sxs-lookup"><span data-stu-id="f310d-242">R2\_MERGEPEN</span></span>     | <span data-ttu-id="f310d-243">Ligne blanche visible</span><span class="sxs-lookup"><span data-stu-id="f310d-243">Visible white line</span></span>     |
| <span data-ttu-id="f310d-244">\_MERGEPENNOT R2</span><span class="sxs-lookup"><span data-stu-id="f310d-244">R2\_MERGEPENNOT</span></span>  | <span data-ttu-id="f310d-245">Ligne blanche visible</span><span class="sxs-lookup"><span data-stu-id="f310d-245">Visible white line</span></span>     |
| <span data-ttu-id="f310d-246">R2 \_ NOP</span><span class="sxs-lookup"><span data-stu-id="f310d-246">R2\_NOP</span></span>          | <span data-ttu-id="f310d-247">Ligne bleue invisible</span><span class="sxs-lookup"><span data-stu-id="f310d-247">Invisible blue line</span></span>    |
| <span data-ttu-id="f310d-248">R2 \_ non</span><span class="sxs-lookup"><span data-stu-id="f310d-248">R2\_NOT</span></span>          | <span data-ttu-id="f310d-249">Trait rouge/vert visible</span><span class="sxs-lookup"><span data-stu-id="f310d-249">Visible red/green line</span></span> |
| <span data-ttu-id="f310d-250">\_NOTCOPYPEN R2</span><span class="sxs-lookup"><span data-stu-id="f310d-250">R2\_NOTCOPYPEN</span></span>   | <span data-ttu-id="f310d-251">Ligne noire visible</span><span class="sxs-lookup"><span data-stu-id="f310d-251">Visible black line</span></span>     |
| <span data-ttu-id="f310d-252">\_NOTMASKPEN R2</span><span class="sxs-lookup"><span data-stu-id="f310d-252">R2\_NOTMASKPEN</span></span>   | <span data-ttu-id="f310d-253">Trait rouge/vert visible</span><span class="sxs-lookup"><span data-stu-id="f310d-253">Visible red/green line</span></span> |
| <span data-ttu-id="f310d-254">\_NOTMERGEPEN R2</span><span class="sxs-lookup"><span data-stu-id="f310d-254">R2\_NOTMERGEPEN</span></span>  | <span data-ttu-id="f310d-255">Ligne noire visible</span><span class="sxs-lookup"><span data-stu-id="f310d-255">Visible black line</span></span>     |
| <span data-ttu-id="f310d-256">\_NOTXORPEN R2</span><span class="sxs-lookup"><span data-stu-id="f310d-256">R2\_NOTXORPEN</span></span>    | <span data-ttu-id="f310d-257">Ligne bleue invisible</span><span class="sxs-lookup"><span data-stu-id="f310d-257">Invisible blue line</span></span>    |
| <span data-ttu-id="f310d-258">\_Blanc R2</span><span class="sxs-lookup"><span data-stu-id="f310d-258">R2\_WHITE</span></span>        | <span data-ttu-id="f310d-259">Ligne blanche visible</span><span class="sxs-lookup"><span data-stu-id="f310d-259">Visible white line</span></span>     |
| <span data-ttu-id="f310d-260">\_XORPEN R2</span><span class="sxs-lookup"><span data-stu-id="f310d-260">R2\_XORPEN</span></span>       | <span data-ttu-id="f310d-261">Trait rouge/vert visible</span><span class="sxs-lookup"><span data-stu-id="f310d-261">Visible red/green line</span></span> |



 

 

 



