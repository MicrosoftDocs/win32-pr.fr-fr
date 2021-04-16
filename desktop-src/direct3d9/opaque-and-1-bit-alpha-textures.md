---
description: Le format de texture DXT1 est pour les textures opaques ou qui ont une seule couleur transparente.
ms.assetid: a890ed0a-1f68-45b8-93cb-b621d1908d9f
title: Textures opaques et alpha 1 bits (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f629eff594d28d9a807021c0b9df0bd05ea66c3
ms.sourcegitcommit: 37f276b5d887a3aad04b1ba86e390dea9d87e591
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/04/2021
ms.locfileid: "104562069"
---
# <a name="opaque-and-1-bit-alpha-textures-direct3d-9"></a><span data-ttu-id="7738b-103">Textures opaques et alpha 1 bits (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="7738b-103">Opaque and 1-Bit Alpha Textures (Direct3D 9)</span></span>

<span data-ttu-id="7738b-104">Le format de texture DXT1 est pour les textures opaques ou qui ont une seule couleur transparente.</span><span class="sxs-lookup"><span data-stu-id="7738b-104">Texture format DXT1 is for textures that are opaque or have a single transparent color.</span></span>

<span data-ttu-id="7738b-105">Pour chaque bloc alpha opaque ou 1 bit, les valeurs 2 16 bits (format RVB 5:6:5) et une image bitmap 4x4 avec 2 bits par pixel sont stockées.</span><span class="sxs-lookup"><span data-stu-id="7738b-105">For each opaque or 1-bit alpha block, two 16-bit values (RGB 5:6:5 format) and a 4x4 bitmap with 2 bits per pixel are stored.</span></span> <span data-ttu-id="7738b-106">Cela totalise 64 bits pour 16 texels, ou quatre bits par Texel.</span><span class="sxs-lookup"><span data-stu-id="7738b-106">This totals 64 bits for 16 texels, or four bits per texel.</span></span> <span data-ttu-id="7738b-107">Dans la bitmap de bloc, il y a 2 bits par Texel pour choisir entre les quatre couleurs, deux d’entre elles étant stockées dans les données encodées.</span><span class="sxs-lookup"><span data-stu-id="7738b-107">In the block bitmap, there are 2 bits per texel to select between the four colors, two of which are stored in the encoded data.</span></span> <span data-ttu-id="7738b-108">Les deux autres couleurs sont dérivées de ces couleurs stockées par interpolation linéaire.</span><span class="sxs-lookup"><span data-stu-id="7738b-108">The other two colors are derived from these stored colors by linear interpolation.</span></span> <span data-ttu-id="7738b-109">Cette disposition est présentée dans le diagramme suivant.</span><span class="sxs-lookup"><span data-stu-id="7738b-109">This layout is shown in the following diagram.</span></span>

![diagramme de la disposition bitmap](images/colors1.png)

<span data-ttu-id="7738b-111">Le format alpha de 1 bit est distingué du format opaque en comparant les valeurs de couleur 2 16 bits stockées dans le bloc.</span><span class="sxs-lookup"><span data-stu-id="7738b-111">The 1-bit alpha format is distinguished from the opaque format by comparing the two 16-bit color values stored in the block.</span></span> <span data-ttu-id="7738b-112">Ils sont traités comme des entiers non signés.</span><span class="sxs-lookup"><span data-stu-id="7738b-112">They are treated as unsigned integers.</span></span> <span data-ttu-id="7738b-113">Si la première couleur est supérieure à la seconde, cela implique que seules les éléments de texture opaques sont définis.</span><span class="sxs-lookup"><span data-stu-id="7738b-113">If the first color is greater than the second, it implies that only opaque texels are defined.</span></span> <span data-ttu-id="7738b-114">Cela signifie que quatre couleurs sont utilisées pour représenter les texels.</span><span class="sxs-lookup"><span data-stu-id="7738b-114">This means four colors are used to represent the texels.</span></span> <span data-ttu-id="7738b-115">Dans un encodage en quatre couleurs, il existe deux couleurs dérivées et les quatre couleurs sont également réparties dans l’espace de couleurs RVB.</span><span class="sxs-lookup"><span data-stu-id="7738b-115">In four-color encoding, there are two derived colors and all four colors are equally distributed in RGB color space.</span></span> <span data-ttu-id="7738b-116">Ce format est similaire au format RVB 5:6:5.</span><span class="sxs-lookup"><span data-stu-id="7738b-116">This format is analogous to RGB 5:6:5 format.</span></span> <span data-ttu-id="7738b-117">Sinon, pour la transparence alpha de 1 bit, trois couleurs sont utilisées et le quatrième est réservé pour représenter des texels transparents.</span><span class="sxs-lookup"><span data-stu-id="7738b-117">Otherwise, for 1-bit alpha transparency, three colors are used and the fourth is reserved to represent transparent texels.</span></span>

<span data-ttu-id="7738b-118">Dans un encodage en trois couleurs, il existe une couleur dérivée et le quatrième code 2 bits est réservé pour indiquer une Texel transparente (informations alpha).</span><span class="sxs-lookup"><span data-stu-id="7738b-118">In three-color encoding, there is one derived color and the fourth 2-bit code is reserved to indicate a transparent texel (alpha information).</span></span> <span data-ttu-id="7738b-119">Ce format est analogue à RVBA 5:5:5:1, où le bit final est utilisé pour l’encodage du masque Alpha.</span><span class="sxs-lookup"><span data-stu-id="7738b-119">This format is analogous to RGBA 5:5:5:1, where the final bit is used for encoding the alpha mask.</span></span>

<span data-ttu-id="7738b-120">L’exemple de code suivant illustre l’algorithme permettant de déterminer si l’encodage à trois ou quatre couleurs est sélectionné :</span><span class="sxs-lookup"><span data-stu-id="7738b-120">The following code example illustrates the algorithm for deciding whether three- or four-color encoding is selected:</span></span>


```
if (color_0 > color_1) 
{
    // Four-color block: derive the other two colors.    
    // 00 = color_0, 01 = color_1, 10 = color_2, 11 = color_3
    // These 2-bit codes correspond to the 2-bit fields 
    // stored in the 64-bit block.
    color_2 = (2 * color_0 + color_1 + 1) / 3;
    color_3 = (color_0 + 2 * color_1 + 1) / 3;
}    
else
{ 
    // Three-color block: derive the other color.
    // 00 = color_0,  01 = color_1,  10 = color_2,  
    // 11 = transparent.
    // These 2-bit codes correspond to the 2-bit fields 
    // stored in the 64-bit block. 
    color_2 = (color_0 + color_1) / 2;    
    color_3 = transparent;    

}
```



<span data-ttu-id="7738b-121">Il est recommandé de définir les composants RVBA du pixel de transparence sur zéro avant la fusion.</span><span class="sxs-lookup"><span data-stu-id="7738b-121">It is recommended that you set the RGBA components of the transparency pixel to zero before blending.</span></span>

<span data-ttu-id="7738b-122">Les tableaux suivants indiquent la disposition de la mémoire pour le bloc de 8 octets.</span><span class="sxs-lookup"><span data-stu-id="7738b-122">The following tables show the memory layout for the 8-byte block.</span></span> <span data-ttu-id="7738b-123">Il est supposé que le premier index correspond à la coordonnée y et le second correspond à la coordonnée x.</span><span class="sxs-lookup"><span data-stu-id="7738b-123">It is assumed that the first index corresponds to the y-coordinate and the second corresponds to the x-coordinate.</span></span> <span data-ttu-id="7738b-124">Par exemple, Texel \[ 1 \] \[ 2 \] fait référence au pixel de la carte de texture à (x, y) = (2, 1).</span><span class="sxs-lookup"><span data-stu-id="7738b-124">For example, Texel\[1\]\[2\] refers to the texture map pixel at (x,y) = (2,1).</span></span>

<span data-ttu-id="7738b-125">Ce tableau contient la disposition de la mémoire pour le bloc de 8 octets (64 bits).</span><span class="sxs-lookup"><span data-stu-id="7738b-125">This table contains the memory layout for the 8-byte (64-bit) block.</span></span>



| <span data-ttu-id="7738b-126">Adresse du mot</span><span class="sxs-lookup"><span data-stu-id="7738b-126">Word address</span></span> | <span data-ttu-id="7738b-127">mot 16 bits</span><span class="sxs-lookup"><span data-stu-id="7738b-127">16-bit word</span></span>    |
|--------------|----------------|
| <span data-ttu-id="7738b-128">0</span><span class="sxs-lookup"><span data-stu-id="7738b-128">0</span></span>            | <span data-ttu-id="7738b-129">Couleur \_ 0</span><span class="sxs-lookup"><span data-stu-id="7738b-129">Color\_0</span></span>       |
| <span data-ttu-id="7738b-130">1</span><span class="sxs-lookup"><span data-stu-id="7738b-130">1</span></span>            | <span data-ttu-id="7738b-131">Couleur \_ 1</span><span class="sxs-lookup"><span data-stu-id="7738b-131">Color\_1</span></span>       |
| <span data-ttu-id="7738b-132">2</span><span class="sxs-lookup"><span data-stu-id="7738b-132">2</span></span>            | <span data-ttu-id="7738b-133">Mot bitmap \_ 0</span><span class="sxs-lookup"><span data-stu-id="7738b-133">Bitmap Word\_0</span></span> |
| <span data-ttu-id="7738b-134">3</span><span class="sxs-lookup"><span data-stu-id="7738b-134">3</span></span>            | <span data-ttu-id="7738b-135">Mot bitmap \_ 1</span><span class="sxs-lookup"><span data-stu-id="7738b-135">Bitmap Word\_1</span></span> |



 

<span data-ttu-id="7738b-136">\_La couleur 0 et \_ la couleur 1, les couleurs aux deux extrêmes sont présentées comme suit :</span><span class="sxs-lookup"><span data-stu-id="7738b-136">Color\_0 and Color\_1, the colors at the two extremes, are laid out as follows:</span></span>



| <span data-ttu-id="7738b-137">Bits</span><span class="sxs-lookup"><span data-stu-id="7738b-137">Bits</span></span>        | <span data-ttu-id="7738b-138">Couleur</span><span class="sxs-lookup"><span data-stu-id="7738b-138">Color</span></span>                 |
|-------------|-----------------------|
| <span data-ttu-id="7738b-139">4:0 (LSB \* )</span><span class="sxs-lookup"><span data-stu-id="7738b-139">4:0 (LSB\*)</span></span> | <span data-ttu-id="7738b-140">Composant de couleur bleu</span><span class="sxs-lookup"><span data-stu-id="7738b-140">Blue color component</span></span>  |
| <span data-ttu-id="7738b-141">10:5</span><span class="sxs-lookup"><span data-stu-id="7738b-141">10:5</span></span>        | <span data-ttu-id="7738b-142">Composant de couleur verte</span><span class="sxs-lookup"><span data-stu-id="7738b-142">Green color component</span></span> |
| <span data-ttu-id="7738b-143">15:11</span><span class="sxs-lookup"><span data-stu-id="7738b-143">15:11</span></span>       | <span data-ttu-id="7738b-144">Composant de couleur rouge</span><span class="sxs-lookup"><span data-stu-id="7738b-144">Red color component</span></span>   |



 

<span data-ttu-id="7738b-145">\*bit le moins significatif</span><span class="sxs-lookup"><span data-stu-id="7738b-145">\*least-significant bit</span></span>

<span data-ttu-id="7738b-146">Le mot bitmap \_ 0 est disposé comme suit :</span><span class="sxs-lookup"><span data-stu-id="7738b-146">Bitmap Word\_0 is laid out as follows:</span></span>



| <span data-ttu-id="7738b-147">Bits</span><span class="sxs-lookup"><span data-stu-id="7738b-147">Bits</span></span>          | <span data-ttu-id="7738b-148">Texel</span><span class="sxs-lookup"><span data-stu-id="7738b-148">Texel</span></span>           |
|---------------|-----------------|
| <span data-ttu-id="7738b-149">1:0 (LSB)</span><span class="sxs-lookup"><span data-stu-id="7738b-149">1:0 (LSB)</span></span>     | <span data-ttu-id="7738b-150">Texel \[ 0 \] \[ 0\]</span><span class="sxs-lookup"><span data-stu-id="7738b-150">Texel\[0\]\[0\]</span></span> |
| <span data-ttu-id="7738b-151">3:2</span><span class="sxs-lookup"><span data-stu-id="7738b-151">3:2</span></span>           | <span data-ttu-id="7738b-152">Texel \[ 0 \] \[ 1\]</span><span class="sxs-lookup"><span data-stu-id="7738b-152">Texel\[0\]\[1\]</span></span> |
| <span data-ttu-id="7738b-153">5:4</span><span class="sxs-lookup"><span data-stu-id="7738b-153">5:4</span></span>           | <span data-ttu-id="7738b-154">Texel \[ 0 \] \[ 2\]</span><span class="sxs-lookup"><span data-stu-id="7738b-154">Texel\[0\]\[2\]</span></span> |
| <span data-ttu-id="7738b-155">7:6</span><span class="sxs-lookup"><span data-stu-id="7738b-155">7:6</span></span>           | <span data-ttu-id="7738b-156">Texel \[ 0 \] \[ 3\]</span><span class="sxs-lookup"><span data-stu-id="7738b-156">Texel\[0\]\[3\]</span></span> |
| <span data-ttu-id="7738b-157">9:8</span><span class="sxs-lookup"><span data-stu-id="7738b-157">9:8</span></span>           | <span data-ttu-id="7738b-158">Texel \[ 1 \] \[ 0\]</span><span class="sxs-lookup"><span data-stu-id="7738b-158">Texel\[1\]\[0\]</span></span> |
| <span data-ttu-id="7738b-159">11:10</span><span class="sxs-lookup"><span data-stu-id="7738b-159">11:10</span></span>         | <span data-ttu-id="7738b-160">Texel \[ 1 \] \[ 1\]</span><span class="sxs-lookup"><span data-stu-id="7738b-160">Texel\[1\]\[1\]</span></span> |
| <span data-ttu-id="7738b-161">13:12</span><span class="sxs-lookup"><span data-stu-id="7738b-161">13:12</span></span>         | <span data-ttu-id="7738b-162">Texel \[ 1 \] \[ 2\]</span><span class="sxs-lookup"><span data-stu-id="7738b-162">Texel\[1\]\[2\]</span></span> |
| <span data-ttu-id="7738b-163">15:14 (MSB \* )</span><span class="sxs-lookup"><span data-stu-id="7738b-163">15:14 (MSB\*)</span></span> | <span data-ttu-id="7738b-164">Texel \[ 1 \] \[ 3\]</span><span class="sxs-lookup"><span data-stu-id="7738b-164">Texel\[1\]\[3\]</span></span> |



 

<span data-ttu-id="7738b-165">\*bit le plus significatif (MSB)</span><span class="sxs-lookup"><span data-stu-id="7738b-165">\*most significant bit (MSB)</span></span>

<span data-ttu-id="7738b-166">Le mot bitmap \_ 1 est disposé comme suit :</span><span class="sxs-lookup"><span data-stu-id="7738b-166">Bitmap Word\_1 is laid out as follows:</span></span>



| <span data-ttu-id="7738b-167">Bits</span><span class="sxs-lookup"><span data-stu-id="7738b-167">Bits</span></span>        | <span data-ttu-id="7738b-168">Texel</span><span class="sxs-lookup"><span data-stu-id="7738b-168">Texel</span></span>           |
|-------------|-----------------|
| <span data-ttu-id="7738b-169">1:0 (LSB)</span><span class="sxs-lookup"><span data-stu-id="7738b-169">1:0 (LSB)</span></span>   | <span data-ttu-id="7738b-170">Texel \[ 2 \] \[ 0\]</span><span class="sxs-lookup"><span data-stu-id="7738b-170">Texel\[2\]\[0\]</span></span> |
| <span data-ttu-id="7738b-171">3:2</span><span class="sxs-lookup"><span data-stu-id="7738b-171">3:2</span></span>         | <span data-ttu-id="7738b-172">Texel \[ 2 \] \[ 1\]</span><span class="sxs-lookup"><span data-stu-id="7738b-172">Texel\[2\]\[1\]</span></span> |
| <span data-ttu-id="7738b-173">5:4</span><span class="sxs-lookup"><span data-stu-id="7738b-173">5:4</span></span>         | <span data-ttu-id="7738b-174">Texel \[ 2 \] \[ 2\]</span><span class="sxs-lookup"><span data-stu-id="7738b-174">Texel\[2\]\[2\]</span></span> |
| <span data-ttu-id="7738b-175">7:6</span><span class="sxs-lookup"><span data-stu-id="7738b-175">7:6</span></span>         | <span data-ttu-id="7738b-176">Texel \[ 2 \] \[ 3\]</span><span class="sxs-lookup"><span data-stu-id="7738b-176">Texel\[2\]\[3\]</span></span> |
| <span data-ttu-id="7738b-177">9:8</span><span class="sxs-lookup"><span data-stu-id="7738b-177">9:8</span></span>         | <span data-ttu-id="7738b-178">Texel \[ 3 \] \[ 0\]</span><span class="sxs-lookup"><span data-stu-id="7738b-178">Texel\[3\]\[0\]</span></span> |
| <span data-ttu-id="7738b-179">11:10</span><span class="sxs-lookup"><span data-stu-id="7738b-179">11:10</span></span>       | <span data-ttu-id="7738b-180">Texel \[ 3 \] \[ 1\]</span><span class="sxs-lookup"><span data-stu-id="7738b-180">Texel\[3\]\[1\]</span></span> |
| <span data-ttu-id="7738b-181">13:12</span><span class="sxs-lookup"><span data-stu-id="7738b-181">13:12</span></span>       | <span data-ttu-id="7738b-182">Texel \[ 3 \] \[ 2\]</span><span class="sxs-lookup"><span data-stu-id="7738b-182">Texel\[3\]\[2\]</span></span> |
| <span data-ttu-id="7738b-183">15:14 (MSB)</span><span class="sxs-lookup"><span data-stu-id="7738b-183">15:14 (MSB)</span></span> | <span data-ttu-id="7738b-184">Texel \[ 3 \] \[ 3\]</span><span class="sxs-lookup"><span data-stu-id="7738b-184">Texel\[3\]\[3\]</span></span> |



 

## <a name="example-of-opaque-color-encoding"></a><span data-ttu-id="7738b-185">Exemple d’encodage de couleur opaque</span><span class="sxs-lookup"><span data-stu-id="7738b-185">Example of Opaque Color Encoding</span></span>

<span data-ttu-id="7738b-186">En guise d’exemple d’encodage opaque, supposons que les couleurs rouge et noir sont à l’extrême.</span><span class="sxs-lookup"><span data-stu-id="7738b-186">As an example of opaque encoding, assume that the colors red and black are at the extremes.</span></span> <span data-ttu-id="7738b-187">Le rouge est la couleur \_ 0 et le noir est la couleur \_ 1.</span><span class="sxs-lookup"><span data-stu-id="7738b-187">Red is color\_0, and black is color\_1.</span></span> <span data-ttu-id="7738b-188">Quatre couleurs interpolées forment le dégradé uniformément réparti entre eux.</span><span class="sxs-lookup"><span data-stu-id="7738b-188">There are four interpolated colors that form the uniformly distributed gradient between them.</span></span> <span data-ttu-id="7738b-189">Pour déterminer les valeurs de la bitmap 4x4, les calculs suivants sont utilisés :</span><span class="sxs-lookup"><span data-stu-id="7738b-189">To determine the values for the 4x4 bitmap, the following calculations are used:</span></span>


```
00 ? color_0
01 ? color_1
10 ? 2/3 color_0 + 1/3 color_1
11 ? 1/3 color_0 + 2/3 color_1
```



<span data-ttu-id="7738b-190">Le bitmap ressemble alors au diagramme suivant.</span><span class="sxs-lookup"><span data-stu-id="7738b-190">The bitmap then looks like the following diagram.</span></span>

![Diagramme qui affiche la disposition bitmap développée.](images/colors2.png)

<span data-ttu-id="7738b-192">Cela ressemble à la série de couleurs illustrée ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="7738b-192">This looks like the following illustrated series of colors.</span></span>

> [!Note]  
> <span data-ttu-id="7738b-193">Dans une image, pixel (0,0) apparaît en haut à gauche.</span><span class="sxs-lookup"><span data-stu-id="7738b-193">In an image, pixel (0,0) appears on the top left.</span></span>

 

![illustration d’un dégradé encodé opaque](images/redsquares.png)

## <a name="example-of-1-bit-alpha-encoding"></a><span data-ttu-id="7738b-195">Exemple d’encodage alpha 1 bits</span><span class="sxs-lookup"><span data-stu-id="7738b-195">Example of 1-Bit Alpha Encoding</span></span>

<span data-ttu-id="7738b-196">Ce format est sélectionné lorsque l’entier non signé 16 bits, Color \_ 0, est inférieur à l’entier 16 bits non signé, Color \_ 1.</span><span class="sxs-lookup"><span data-stu-id="7738b-196">This format is selected when the unsigned 16-bit integer, color\_0, is less than the unsigned 16-bit integer, color\_1.</span></span> <span data-ttu-id="7738b-197">Un exemple de ce format peut être utilisé dans une arborescence, par rapport à un ciel bleu.</span><span class="sxs-lookup"><span data-stu-id="7738b-197">An example of where this format can be used is leaves on a tree, shown against a blue sky.</span></span> <span data-ttu-id="7738b-198">Certains texels peuvent être marqués comme étant transparents alors que trois nuances de vert sont toujours disponibles pour les feuilles.</span><span class="sxs-lookup"><span data-stu-id="7738b-198">Some texels can be marked as transparent while three shades of green are still available for the leaves.</span></span> <span data-ttu-id="7738b-199">Deux couleurs corrigent les extrêmes, tandis que la troisième est une couleur interpolée.</span><span class="sxs-lookup"><span data-stu-id="7738b-199">Two colors fix the extremes, and the third is an interpolated color.</span></span>

<span data-ttu-id="7738b-200">L’illustration suivante est un exemple d’une telle image.</span><span class="sxs-lookup"><span data-stu-id="7738b-200">The following illustration is an example of such a picture.</span></span>

![illustration de l’encodage alpha 1 bits](images/greenthing.png)

<span data-ttu-id="7738b-202">Notez que lorsque l’image est affichée en blanc, le Texel est encodé comme transparent.</span><span class="sxs-lookup"><span data-stu-id="7738b-202">Note that where the image is shown as white, the texel would be encoded as transparent.</span></span> <span data-ttu-id="7738b-203">Notez également que les composants RVBA des texels transparents doivent être définis sur zéro avant la fusion.</span><span class="sxs-lookup"><span data-stu-id="7738b-203">Also note that the RGBA components of the transparent texels should be set to zero before blending.</span></span>

<span data-ttu-id="7738b-204">L’encodage bitmap des couleurs et de la transparence est déterminé à l’aide des calculs suivants.</span><span class="sxs-lookup"><span data-stu-id="7738b-204">The bitmap encoding for the colors and the transparency is determined using the following calculations.</span></span>


```
00 ? color_0
01 ? color_1
10 ? 1/2 color_0 + 1/2 color_1
11   ?   Transparent
```



<span data-ttu-id="7738b-205">Le bitmap ressemble alors au diagramme suivant.</span><span class="sxs-lookup"><span data-stu-id="7738b-205">The bitmap then looks like the following diagram.</span></span>

![diagramme de la disposition bitmap développée](images/colors3.png)

## <a name="related-topics"></a><span data-ttu-id="7738b-207">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="7738b-207">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7738b-208">Ressources de texture compressées</span><span class="sxs-lookup"><span data-stu-id="7738b-208">Compressed Texture Resources</span></span>](compressed-texture-resources.md)
</dt> </dl>

 

 



