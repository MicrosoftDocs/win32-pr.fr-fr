---
description: Il existe deux façons d’encoder des cartes de texture qui présentent une transparence plus complexe.
ms.assetid: cae788f6-60f1-4987-8f06-bf4256bccd9b
title: Textures avec canaux alpha (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2c361b0335ef4f36b4efc9c90c71270e855f5db
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104566774"
---
# <a name="textures-with-alpha-channels-direct3d-9"></a><span data-ttu-id="d0b6b-103">Textures avec canaux alpha (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="d0b6b-103">Textures with Alpha Channels (Direct3D 9)</span></span>

<span data-ttu-id="d0b6b-104">Il existe deux façons d’encoder des cartes de texture qui présentent une transparence plus complexe.</span><span class="sxs-lookup"><span data-stu-id="d0b6b-104">There are two ways to encode texture maps that exhibit more complex transparency.</span></span> <span data-ttu-id="d0b6b-105">Dans chaque cas, un bloc qui décrit la transparence précède le bloc 64 bits déjà décrit.</span><span class="sxs-lookup"><span data-stu-id="d0b6b-105">In each case, a block that describes the transparency precedes the 64-bit block already described.</span></span> <span data-ttu-id="d0b6b-106">La transparence est représentée sous la forme d’une image bitmap 4x4 avec 4 bits par pixel (codage explicite), ou avec moins de bits et une interpolation linéaire analogue à ce qui est utilisé pour l’encodage des couleurs.</span><span class="sxs-lookup"><span data-stu-id="d0b6b-106">The transparency is either represented as a 4x4 bitmap with 4 bits per pixel (explicit encoding), or with fewer bits and linear interpolation that is analogous to what is used for color encoding.</span></span>

<span data-ttu-id="d0b6b-107">Le bloc de transparence et le bloc de couleur sont disposés comme indiqué dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="d0b6b-107">The transparency block and the color block are arranged as shown in the following table.</span></span>



| <span data-ttu-id="d0b6b-108">Adresse du mot</span><span class="sxs-lookup"><span data-stu-id="d0b6b-108">Word address</span></span> | <span data-ttu-id="d0b6b-109">bloc de bits 64</span><span class="sxs-lookup"><span data-stu-id="d0b6b-109">64-bit block</span></span>                      |
|--------------|-----------------------------------|
| <span data-ttu-id="d0b6b-110">3:0</span><span class="sxs-lookup"><span data-stu-id="d0b6b-110">3:0</span></span>          | <span data-ttu-id="d0b6b-111">Bloc de transparence</span><span class="sxs-lookup"><span data-stu-id="d0b6b-111">Transparency block</span></span>                |
| <span data-ttu-id="d0b6b-112">7:4</span><span class="sxs-lookup"><span data-stu-id="d0b6b-112">7:4</span></span>          | <span data-ttu-id="d0b6b-113">Précédemment décrit le bloc 64 bits</span><span class="sxs-lookup"><span data-stu-id="d0b6b-113">Previously described 64-bit block</span></span> |



 

## <a name="explicit-texture-encoding"></a><span data-ttu-id="d0b6b-114">Encodage de texture explicite</span><span class="sxs-lookup"><span data-stu-id="d0b6b-114">Explicit Texture Encoding</span></span>

<span data-ttu-id="d0b6b-115">Pour l’encodage de texture explicite (formats DXT2 et DXT3), les composants alpha des texels qui décrivent la transparence sont encodés dans une bitmap 4x4 avec 4 bits par Texel.</span><span class="sxs-lookup"><span data-stu-id="d0b6b-115">For explicit texture encoding (DXT2 and DXT3 formats), the alpha components of the texels that describe transparency are encoded in a 4x4 bitmap with 4 bits per texel.</span></span> <span data-ttu-id="d0b6b-116">Ces quatre bits peuvent être obtenus par le biais de différents moyens, tels que le tramage ou en utilisant les quatre bits les plus significatifs des données alpha.</span><span class="sxs-lookup"><span data-stu-id="d0b6b-116">These four bits can be achieved through a variety of means such as dithering or by using the four most significant bits of the alpha data.</span></span> <span data-ttu-id="d0b6b-117">Toutefois, ils sont créés, mais ils sont utilisés de la même manière, sans aucune forme d’interpolation.</span><span class="sxs-lookup"><span data-stu-id="d0b6b-117">However they are produced, they are used just as they are, without any form of interpolation.</span></span>

<span data-ttu-id="d0b6b-118">Le diagramme suivant montre un bloc de transparence 64 bits.</span><span class="sxs-lookup"><span data-stu-id="d0b6b-118">The following diagram shows a 64-bit transparency block.</span></span>

![diagramme d’un bloc de transparence 64 bits](images/colors4.png)

> [!Note]  
> <span data-ttu-id="d0b6b-120">La méthode de compression de Direct3D utilise les quatre bits les plus significatifs.</span><span class="sxs-lookup"><span data-stu-id="d0b6b-120">The compression method of Direct3D uses the four most significant bits.</span></span>

 

<span data-ttu-id="d0b6b-121">Les tableaux suivants montrent comment les informations alpha sont disposées en mémoire, pour chaque mot de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="d0b6b-121">The following tables illustrate how the alpha information is laid out in memory, for each 16-bit word.</span></span>

<span data-ttu-id="d0b6b-122">Ce tableau contient la disposition pour Word 0.</span><span class="sxs-lookup"><span data-stu-id="d0b6b-122">This table contains the layout for word 0.</span></span>



| <span data-ttu-id="d0b6b-123">Bits</span><span class="sxs-lookup"><span data-stu-id="d0b6b-123">Bits</span></span>          | <span data-ttu-id="d0b6b-124">Alpha</span><span class="sxs-lookup"><span data-stu-id="d0b6b-124">Alpha</span></span>      |
|---------------|------------|
| <span data-ttu-id="d0b6b-125">3:0 (LSB \* )</span><span class="sxs-lookup"><span data-stu-id="d0b6b-125">3:0 (LSB\*)</span></span>   | <span data-ttu-id="d0b6b-126">\[0 \] \[ 0\]</span><span class="sxs-lookup"><span data-stu-id="d0b6b-126">\[0\]\[0\]</span></span> |
| <span data-ttu-id="d0b6b-127">7:4</span><span class="sxs-lookup"><span data-stu-id="d0b6b-127">7:4</span></span>           | <span data-ttu-id="d0b6b-128">\[0 \] \[ 1\]</span><span class="sxs-lookup"><span data-stu-id="d0b6b-128">\[0\]\[1\]</span></span> |
| <span data-ttu-id="d0b6b-129">11:8</span><span class="sxs-lookup"><span data-stu-id="d0b6b-129">11:8</span></span>          | <span data-ttu-id="d0b6b-130">\[0 \] \[ 2\]</span><span class="sxs-lookup"><span data-stu-id="d0b6b-130">\[0\]\[2\]</span></span> |
| <span data-ttu-id="d0b6b-131">15:12 (MSB \* )</span><span class="sxs-lookup"><span data-stu-id="d0b6b-131">15:12 (MSB\*)</span></span> | <span data-ttu-id="d0b6b-132">\[0 \] \[ 3\]</span><span class="sxs-lookup"><span data-stu-id="d0b6b-132">\[0\]\[3\]</span></span> |



 

<span data-ttu-id="d0b6b-133">\*bit le moins significatif, bit le plus significatif (MSB)</span><span class="sxs-lookup"><span data-stu-id="d0b6b-133">\*least-significant bit, most significant bit (MSB)</span></span>

<span data-ttu-id="d0b6b-134">Ce tableau contient la mise en page de Word 1.</span><span class="sxs-lookup"><span data-stu-id="d0b6b-134">This table contains the layout for word 1.</span></span>



| <span data-ttu-id="d0b6b-135">Bits</span><span class="sxs-lookup"><span data-stu-id="d0b6b-135">Bits</span></span>        | <span data-ttu-id="d0b6b-136">Alpha</span><span class="sxs-lookup"><span data-stu-id="d0b6b-136">Alpha</span></span>      |
|-------------|------------|
| <span data-ttu-id="d0b6b-137">3:0 (LSB)</span><span class="sxs-lookup"><span data-stu-id="d0b6b-137">3:0 (LSB)</span></span>   | <span data-ttu-id="d0b6b-138">\[1 \] \[ 0\]</span><span class="sxs-lookup"><span data-stu-id="d0b6b-138">\[1\]\[0\]</span></span> |
| <span data-ttu-id="d0b6b-139">7:4</span><span class="sxs-lookup"><span data-stu-id="d0b6b-139">7:4</span></span>         | <span data-ttu-id="d0b6b-140">\[1 \] \[ 1\]</span><span class="sxs-lookup"><span data-stu-id="d0b6b-140">\[1\]\[1\]</span></span> |
| <span data-ttu-id="d0b6b-141">11:8</span><span class="sxs-lookup"><span data-stu-id="d0b6b-141">11:8</span></span>        | <span data-ttu-id="d0b6b-142">\[1 \] \[ 2\]</span><span class="sxs-lookup"><span data-stu-id="d0b6b-142">\[1\]\[2\]</span></span> |
| <span data-ttu-id="d0b6b-143">15:12 (MSB)</span><span class="sxs-lookup"><span data-stu-id="d0b6b-143">15:12 (MSB)</span></span> | <span data-ttu-id="d0b6b-144">\[1 \] \[ 3\]</span><span class="sxs-lookup"><span data-stu-id="d0b6b-144">\[1\]\[3\]</span></span> |



 

<span data-ttu-id="d0b6b-145">Ce tableau contient la disposition pour Word 2.</span><span class="sxs-lookup"><span data-stu-id="d0b6b-145">This table contains the layout for word 2.</span></span>



| <span data-ttu-id="d0b6b-146">Bits</span><span class="sxs-lookup"><span data-stu-id="d0b6b-146">Bits</span></span>        | <span data-ttu-id="d0b6b-147">Alpha</span><span class="sxs-lookup"><span data-stu-id="d0b6b-147">Alpha</span></span>      |
|-------------|------------|
| <span data-ttu-id="d0b6b-148">3:0 (LSB)</span><span class="sxs-lookup"><span data-stu-id="d0b6b-148">3:0 (LSB)</span></span>   | <span data-ttu-id="d0b6b-149">\[2 \] \[ 0\]</span><span class="sxs-lookup"><span data-stu-id="d0b6b-149">\[2\]\[0\]</span></span> |
| <span data-ttu-id="d0b6b-150">7:4</span><span class="sxs-lookup"><span data-stu-id="d0b6b-150">7:4</span></span>         | <span data-ttu-id="d0b6b-151">\[2 \] \[ 1\]</span><span class="sxs-lookup"><span data-stu-id="d0b6b-151">\[2\]\[1\]</span></span> |
| <span data-ttu-id="d0b6b-152">11:8</span><span class="sxs-lookup"><span data-stu-id="d0b6b-152">11:8</span></span>        | <span data-ttu-id="d0b6b-153">\[2 \] \[ 2\]</span><span class="sxs-lookup"><span data-stu-id="d0b6b-153">\[2\]\[2\]</span></span> |
| <span data-ttu-id="d0b6b-154">15:12 (MSB)</span><span class="sxs-lookup"><span data-stu-id="d0b6b-154">15:12 (MSB)</span></span> | <span data-ttu-id="d0b6b-155">\[2 \] \[ 3\]</span><span class="sxs-lookup"><span data-stu-id="d0b6b-155">\[2\]\[3\]</span></span> |



 

<span data-ttu-id="d0b6b-156">Ce tableau contient la disposition pour Word 3.</span><span class="sxs-lookup"><span data-stu-id="d0b6b-156">This table contains the layout for word 3.</span></span>



| <span data-ttu-id="d0b6b-157">Bits</span><span class="sxs-lookup"><span data-stu-id="d0b6b-157">Bits</span></span>        | <span data-ttu-id="d0b6b-158">Alpha</span><span class="sxs-lookup"><span data-stu-id="d0b6b-158">Alpha</span></span>      |
|-------------|------------|
| <span data-ttu-id="d0b6b-159">3:0 (LSB)</span><span class="sxs-lookup"><span data-stu-id="d0b6b-159">3:0 (LSB)</span></span>   | <span data-ttu-id="d0b6b-160">\[3 \] \[ 0\]</span><span class="sxs-lookup"><span data-stu-id="d0b6b-160">\[3\]\[0\]</span></span> |
| <span data-ttu-id="d0b6b-161">7:4</span><span class="sxs-lookup"><span data-stu-id="d0b6b-161">7:4</span></span>         | <span data-ttu-id="d0b6b-162">\[3 \] \[ 1\]</span><span class="sxs-lookup"><span data-stu-id="d0b6b-162">\[3\]\[1\]</span></span> |
| <span data-ttu-id="d0b6b-163">11:8</span><span class="sxs-lookup"><span data-stu-id="d0b6b-163">11:8</span></span>        | <span data-ttu-id="d0b6b-164">\[3 \] \[ 2\]</span><span class="sxs-lookup"><span data-stu-id="d0b6b-164">\[3\]\[2\]</span></span> |
| <span data-ttu-id="d0b6b-165">15:12 (MSB)</span><span class="sxs-lookup"><span data-stu-id="d0b6b-165">15:12 (MSB)</span></span> | <span data-ttu-id="d0b6b-166">\[3 \] \[ 3\]</span><span class="sxs-lookup"><span data-stu-id="d0b6b-166">\[3\]\[3\]</span></span> |



 

<span data-ttu-id="d0b6b-167">La différence entre DXT2 et DXT3 est que, dans le format DXT2, il est supposé que les données de couleur ont été prémultipliées par Alpha.</span><span class="sxs-lookup"><span data-stu-id="d0b6b-167">The difference between DXT2 and DXT3 are that, in the DXT2 format, it is assumed that the color data has been premultiplied by alpha.</span></span> <span data-ttu-id="d0b6b-168">Dans le format DXT3, il est supposé que la couleur n’est pas prémultipliée par Alpha.</span><span class="sxs-lookup"><span data-stu-id="d0b6b-168">In the DXT3 format, it is assumed that the color is not premultiplied by alpha.</span></span> <span data-ttu-id="d0b6b-169">Ces deux formats sont nécessaires, car, dans la plupart des cas, au moment où une texture est utilisée, l’examen des données n’est pas suffisant pour déterminer si les valeurs de couleur ont été multipliées par Alpha.</span><span class="sxs-lookup"><span data-stu-id="d0b6b-169">These two formats are needed because, in most cases, by the time a texture is used, just examining the data is not sufficient to determine if the color values have been multiplied by alpha.</span></span> <span data-ttu-id="d0b6b-170">Étant donné que ces informations sont nécessaires au moment de l’exécution, les deux codes FOURCC sont utilisés pour différencier ces cas.</span><span class="sxs-lookup"><span data-stu-id="d0b6b-170">Because this information is needed at run time, the two FOURCC codes are used to differentiate these cases.</span></span> <span data-ttu-id="d0b6b-171">Toutefois, les données et la méthode d’interpolation utilisées pour ces deux formats sont identiques.</span><span class="sxs-lookup"><span data-stu-id="d0b6b-171">However, the data and interpolation method used for these two formats is identical.</span></span>

<span data-ttu-id="d0b6b-172">La comparaison de couleurs utilisée dans DXT1 pour déterminer si le Texel est transparent n’est pas utilisé dans ce format.</span><span class="sxs-lookup"><span data-stu-id="d0b6b-172">The color compare used in DXT1 to determine if the texel is transparent is not used in this format.</span></span> <span data-ttu-id="d0b6b-173">Il est supposé que, sans la couleur, les données de couleur sont toujours traitées comme si elles étaient en mode 4 couleurs.</span><span class="sxs-lookup"><span data-stu-id="d0b6b-173">It is assumed that without the color compare the color data is always treated as if in 4-color mode.</span></span> <span data-ttu-id="d0b6b-174">En d’autres termes, l’instruction if en haut du code DXT1 doit être la suivante :</span><span class="sxs-lookup"><span data-stu-id="d0b6b-174">In other words, the if statement at the top of the DXT1 code should be the following:</span></span>


```
if ((color_0 > color_1) OR !DXT1) {
```



## <a name="three-bit-linear-alpha-interpolation"></a><span data-ttu-id="d0b6b-175">Three-Bit l’interpolation alpha linéaire</span><span class="sxs-lookup"><span data-stu-id="d0b6b-175">Three-Bit Linear Alpha Interpolation</span></span>

<span data-ttu-id="d0b6b-176">L’encodage de la transparence pour les formats DXT4 et DXT5 est basé sur un concept similaire à l’encodage linéaire utilisé pour la couleur.</span><span class="sxs-lookup"><span data-stu-id="d0b6b-176">The encoding of transparency for the DXT4 and DXT5 formats is based on a concept similar to the linear encoding used for color.</span></span> <span data-ttu-id="d0b6b-177">Les valeurs alpha 2 8 bits et une image bitmap 4x4 avec trois bits par pixel sont stockées dans les huit premiers octets du bloc.</span><span class="sxs-lookup"><span data-stu-id="d0b6b-177">Two 8-bit alpha values and a 4x4 bitmap with three bits per pixel are stored in the first eight bytes of the block.</span></span> <span data-ttu-id="d0b6b-178">Les valeurs alpha représentatives sont utilisées pour interpoler les valeurs alpha intermédiaires.</span><span class="sxs-lookup"><span data-stu-id="d0b6b-178">The representative alpha values are used to interpolate intermediate alpha values.</span></span> <span data-ttu-id="d0b6b-179">Des informations supplémentaires sont disponibles dans la manière dont les deux valeurs alpha sont stockées.</span><span class="sxs-lookup"><span data-stu-id="d0b6b-179">Additional information is available in the way the two alpha values are stored.</span></span> <span data-ttu-id="d0b6b-180">Si alpha \_ 0 est supérieur à alpha \_ 1, les six valeurs alpha intermédiaires sont créées par l’interpolation.</span><span class="sxs-lookup"><span data-stu-id="d0b6b-180">If alpha\_0 is greater than alpha\_1, then six intermediate alpha values are created by the interpolation.</span></span> <span data-ttu-id="d0b6b-181">Dans le cas contraire, quatre valeurs alpha intermédiaires sont interpolées entre les caractères alpha extrêmes spécifiés.</span><span class="sxs-lookup"><span data-stu-id="d0b6b-181">Otherwise, four intermediate alpha values are interpolated between the specified alpha extremes.</span></span> <span data-ttu-id="d0b6b-182">Les deux valeurs alpha implicites supplémentaires sont 0 (entièrement transparentes) et 255 (entièrement opaques).</span><span class="sxs-lookup"><span data-stu-id="d0b6b-182">The two additional implicit alpha values are 0 (fully transparent) and 255 (fully opaque).</span></span>

<span data-ttu-id="d0b6b-183">L’exemple de code suivant illustre cet algorithme.</span><span class="sxs-lookup"><span data-stu-id="d0b6b-183">The following code example illustrates this algorithm.</span></span>


```
// 8-alpha or 6-alpha block?    
if (alpha_0 > alpha_1) {    
    // 8-alpha block:  derive the other six alphas.    
    // Bit code 000 = alpha_0, 001 = alpha_1, others are interpolated.
    alpha_2 = (6 * alpha_0 + 1 * alpha_1 + 3) / 7;    // bit code 010
    alpha_3 = (5 * alpha_0 + 2 * alpha_1 + 3) / 7;    // bit code 011
    alpha_4 = (4 * alpha_0 + 3 * alpha_1 + 3) / 7;    // bit code 100
    alpha_5 = (3 * alpha_0 + 4 * alpha_1 + 3) / 7;    // bit code 101
    alpha_6 = (2 * alpha_0 + 5 * alpha_1 + 3) / 7;    // bit code 110
    alpha_7 = (1 * alpha_0 + 6 * alpha_1 + 3) / 7;    // bit code 111  
}    
else {  
    // 6-alpha block.    
    // Bit code 000 = alpha_0, 001 = alpha_1, others are interpolated.
    alpha_2 = (4 * alpha_0 + 1 * alpha_1 + 2) / 5;    // Bit code 010
    alpha_3 = (3 * alpha_0 + 2 * alpha_1 + 2) / 5;    // Bit code 011
    alpha_4 = (2 * alpha_0 + 3 * alpha_1 + 2) / 5;    // Bit code 100
    alpha_5 = (1 * alpha_0 + 4 * alpha_1 + 2) / 5;    // Bit code 101
    alpha_6 = 0;                                      // Bit code 110
    alpha_7 = 255;                                    // Bit code 111
}
```



<span data-ttu-id="d0b6b-184">La disposition de la mémoire du bloc alpha est la suivante :</span><span class="sxs-lookup"><span data-stu-id="d0b6b-184">The memory layout of the alpha block is as follows:</span></span>



| <span data-ttu-id="d0b6b-185">Byte</span><span class="sxs-lookup"><span data-stu-id="d0b6b-185">Byte</span></span> | <span data-ttu-id="d0b6b-186">Alpha</span><span class="sxs-lookup"><span data-stu-id="d0b6b-186">Alpha</span></span>                                                          |
|------|----------------------------------------------------------------|
| <span data-ttu-id="d0b6b-187">0</span><span class="sxs-lookup"><span data-stu-id="d0b6b-187">0</span></span>    | <span data-ttu-id="d0b6b-188">Alpha \_ 0</span><span class="sxs-lookup"><span data-stu-id="d0b6b-188">Alpha\_0</span></span>                                                       |
| <span data-ttu-id="d0b6b-189">1</span><span class="sxs-lookup"><span data-stu-id="d0b6b-189">1</span></span>    | <span data-ttu-id="d0b6b-190">Alpha \_ 1</span><span class="sxs-lookup"><span data-stu-id="d0b6b-190">Alpha\_1</span></span>                                                       |
| <span data-ttu-id="d0b6b-191">2</span><span class="sxs-lookup"><span data-stu-id="d0b6b-191">2</span></span>    | <span data-ttu-id="d0b6b-192">\[0 \] \[ 2 \] (2 MSBS), \[ 0 \] \[ \] \[ \] \[ 1,0\]</span><span class="sxs-lookup"><span data-stu-id="d0b6b-192">\[0\]\[2\] (2 MSBs), \[0\]\[1\], \[0\]\[0\]</span></span>                    |
| <span data-ttu-id="d0b6b-193">3</span><span class="sxs-lookup"><span data-stu-id="d0b6b-193">3</span></span>    | <span data-ttu-id="d0b6b-194">\[1 \] \[ 1 \] (1 MSB), \[ 1 \] \[ 0 \] , \[ 0 \] \[ 3 \] , \[ 0 \] \[ 2 \] (1 LSB)</span><span class="sxs-lookup"><span data-stu-id="d0b6b-194">\[1\]\[1\] (1 MSB), \[1\]\[0\], \[0\]\[3\], \[0\]\[2\] (1 LSB)</span></span> |
| <span data-ttu-id="d0b6b-195">4</span><span class="sxs-lookup"><span data-stu-id="d0b6b-195">4</span></span>    | <span data-ttu-id="d0b6b-196">\[1 \] \[ 3 \] , \[ 1 \] \[ 2 \] , \[ 1 \] \[ 1 \] (2 LSBs)</span><span class="sxs-lookup"><span data-stu-id="d0b6b-196">\[1\]\[3\], \[1\]\[2\], \[1\]\[1\] (2 LSBs)</span></span>                    |
| <span data-ttu-id="d0b6b-197">5</span><span class="sxs-lookup"><span data-stu-id="d0b6b-197">5</span></span>    | <span data-ttu-id="d0b6b-198">\[2 \] \[ 2 \] (2 MSBS), \[ 2 \] \[ 1 \] , \[ 2 \] \[ 0\]</span><span class="sxs-lookup"><span data-stu-id="d0b6b-198">\[2\]\[2\] (2 MSBs), \[2\]\[1\], \[2\]\[0\]</span></span>                    |
| <span data-ttu-id="d0b6b-199">6</span><span class="sxs-lookup"><span data-stu-id="d0b6b-199">6</span></span>    | <span data-ttu-id="d0b6b-200">\[3 \] \[ 1 \] (1 MSB), \[ 3 \] \[ 0 \] , \[ 2 \] \[ 3 \] , \[ 2 \] \[ 2 \] (1 LSB)</span><span class="sxs-lookup"><span data-stu-id="d0b6b-200">\[3\]\[1\] (1 MSB), \[3\]\[0\], \[2\]\[3\], \[2\]\[2\] (1 LSB)</span></span> |
| <span data-ttu-id="d0b6b-201">7</span><span class="sxs-lookup"><span data-stu-id="d0b6b-201">7</span></span>    | <span data-ttu-id="d0b6b-202">\[3 \] \[ 3 \] , \[ 3 \] \[ 2 \] , \[ 3 \] \[ 1 \] (2 LSBs)</span><span class="sxs-lookup"><span data-stu-id="d0b6b-202">\[3\]\[3\], \[3\]\[2\], \[3\]\[1\] (2 LSBs)</span></span>                    |



 

<span data-ttu-id="d0b6b-203">La différence entre DXT4 et DXT5 est que dans le format DXT4 il est supposé que les données de couleur ont été prémultipliées par Alpha.</span><span class="sxs-lookup"><span data-stu-id="d0b6b-203">The difference between DXT4 and DXT5 is that in the DXT4 format it is assumed that the color data has been premultiplied by alpha.</span></span> <span data-ttu-id="d0b6b-204">Dans le format DXT5, il est supposé que la couleur n’est pas prémultipliée par Alpha.</span><span class="sxs-lookup"><span data-stu-id="d0b6b-204">In the DXT5 format, it is assumed the color is not premultiplied by alpha.</span></span> <span data-ttu-id="d0b6b-205">Ces deux formats sont nécessaires, car, dans la plupart des cas, au moment où une texture est utilisée, l’examen des données n’est pas suffisant pour déterminer si les valeurs de couleur ont été multipliées par Alpha.</span><span class="sxs-lookup"><span data-stu-id="d0b6b-205">These two formats are needed because, in most cases, by the time a texture is used, just examining the data is not sufficient to determine if the color values have been multiplied by alpha.</span></span> <span data-ttu-id="d0b6b-206">Étant donné que ces informations sont nécessaires au moment de l’exécution, les deux codes FOURCC sont utilisés pour différencier ces cas.</span><span class="sxs-lookup"><span data-stu-id="d0b6b-206">Because this information is needed at run time, the two FOURCC codes are used to differentiate these cases.</span></span> <span data-ttu-id="d0b6b-207">Toutefois, les données et la méthode d’interpolation utilisées pour ces deux formats sont identiques.</span><span class="sxs-lookup"><span data-stu-id="d0b6b-207">However, the data and interpolation method used for these two formats is identical.</span></span>

<span data-ttu-id="d0b6b-208">La comparaison de couleurs utilisée dans DXT1 pour déterminer si le Texel est transparent n’est pas utilisé avec ces formats.</span><span class="sxs-lookup"><span data-stu-id="d0b6b-208">The color compare used in DXT1 to determine if the texel is transparent is not used with these formats.</span></span> <span data-ttu-id="d0b6b-209">Il est supposé que, sans la couleur, les données de couleur sont toujours traitées comme si elles étaient en mode 4 couleurs.</span><span class="sxs-lookup"><span data-stu-id="d0b6b-209">It is assumed that without the color compare the color data is always treated as if in 4-color mode.</span></span> <span data-ttu-id="d0b6b-210">En d’autres termes, l’instruction if en haut du code DXT1 doit être :</span><span class="sxs-lookup"><span data-stu-id="d0b6b-210">In other words, the if statement at the top of the DXT1 code should be:</span></span>


```
if ((color_0 > color_1) OR !DXT1) {
```



## <a name="related-topics"></a><span data-ttu-id="d0b6b-211">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="d0b6b-211">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d0b6b-212">Ressources de texture compressées</span><span class="sxs-lookup"><span data-stu-id="d0b6b-212">Compressed Texture Resources</span></span>](compressed-texture-resources.md)
</dt> </dl>

 

 



