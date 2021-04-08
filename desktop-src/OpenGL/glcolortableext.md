---
title: fonction glColorTableEXT (GL. h)
description: La fonction glColorTableEXT spécifie le format et la taille d’une palette pour les textures de palette ciblées.
ms.assetid: f3d7b1a1-97a5-47ef-a0ca-5e58acb86bb4
keywords:
- glColorTableEXT fonction OpenGL
topic_type:
- apiref
api_name:
- glColorTableEXT
api_location:
- Gl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cd0d5fd5c848e787f480e3e1893b9b25e4bbd3de
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742212"
---
# <a name="glcolortableext-function"></a><span data-ttu-id="77cb2-104">glColorTableEXT fonction)</span><span class="sxs-lookup"><span data-stu-id="77cb2-104">glColorTableEXT function</span></span>

<span data-ttu-id="77cb2-105">La fonction **glColorTableEXT** spécifie le format et la taille d’une palette pour les textures de palette ciblées.</span><span class="sxs-lookup"><span data-stu-id="77cb2-105">The **glColorTableEXT** function specifies the format and size of a palette for targeted paletted textures.</span></span>

## <a name="syntax"></a><span data-ttu-id="77cb2-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="77cb2-106">Syntax</span></span>


```C++
void WINAPI glColorTableEXT(
         GLenum  target,
         GLenum  internalFormat,
         GLsizei width,
         GLenum  format,
         GLenum  type,
   const GLvoid  *data
);
```



## <a name="parameters"></a><span data-ttu-id="77cb2-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="77cb2-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="77cb2-108">*cible*</span><span class="sxs-lookup"><span data-stu-id="77cb2-108">*target*</span></span> 
</dt> <dd>

<span data-ttu-id="77cb2-109">Texture cible dont la palette doit être modifiée.</span><span class="sxs-lookup"><span data-stu-id="77cb2-109">The target texture that is to have its palette changed.</span></span> <span data-ttu-id="77cb2-110">Doit être une TEXTURE \_ 1D, une texture \_ 2D, une texture de proxy \_ \_ 1D ou une texture de proxy \_ \_ 2D.</span><span class="sxs-lookup"><span data-stu-id="77cb2-110">Must be TEXTURE\_1D, TEXTURE\_2D, PROXY\_TEXTURE\_1D, or PROXY\_TEXTURE\_2D.</span></span>

</dd> <dt>

<span data-ttu-id="77cb2-111">*internalFormat*</span><span class="sxs-lookup"><span data-stu-id="77cb2-111">*internalFormat*</span></span> 
</dt> <dd>

<span data-ttu-id="77cb2-112">Format interne et résolution de la palette.</span><span class="sxs-lookup"><span data-stu-id="77cb2-112">The internal format and resolution of the palette.</span></span> <span data-ttu-id="77cb2-113">Ce paramètre peut prendre l’une des valeurs symboliques suivantes.</span><span class="sxs-lookup"><span data-stu-id="77cb2-113">This parameter can assume one of the following symbolic values.</span></span>



| <span data-ttu-id="77cb2-114">Constante</span><span class="sxs-lookup"><span data-stu-id="77cb2-114">Constant</span></span>       | <span data-ttu-id="77cb2-115">Format de base</span><span class="sxs-lookup"><span data-stu-id="77cb2-115">Base Format</span></span> | <span data-ttu-id="77cb2-116">Bits R</span><span class="sxs-lookup"><span data-stu-id="77cb2-116">R Bits</span></span> | <span data-ttu-id="77cb2-117">Bits G</span><span class="sxs-lookup"><span data-stu-id="77cb2-117">G Bits</span></span> | <span data-ttu-id="77cb2-118">Bits B</span><span class="sxs-lookup"><span data-stu-id="77cb2-118">B Bits</span></span> | <span data-ttu-id="77cb2-119">Un bits</span><span class="sxs-lookup"><span data-stu-id="77cb2-119">A Bits</span></span> |
|----------------|-------------|--------|--------|--------|--------|
| <span data-ttu-id="77cb2-120">GL \_ R3 \_ G3 \_ a2</span><span class="sxs-lookup"><span data-stu-id="77cb2-120">GL\_R3\_G3\_B2</span></span> | <span data-ttu-id="77cb2-121">\_RGB GL</span><span class="sxs-lookup"><span data-stu-id="77cb2-121">GL\_RGB</span></span>     | <span data-ttu-id="77cb2-122">3</span><span class="sxs-lookup"><span data-stu-id="77cb2-122">3</span></span>      | <span data-ttu-id="77cb2-123">3</span><span class="sxs-lookup"><span data-stu-id="77cb2-123">3</span></span>      | <span data-ttu-id="77cb2-124">2</span><span class="sxs-lookup"><span data-stu-id="77cb2-124">2</span></span>      |        |
| <span data-ttu-id="77cb2-125">\_RGB4 GL</span><span class="sxs-lookup"><span data-stu-id="77cb2-125">GL\_RGB4</span></span>       | <span data-ttu-id="77cb2-126">\_RGB GL</span><span class="sxs-lookup"><span data-stu-id="77cb2-126">GL\_RGB</span></span>     | <span data-ttu-id="77cb2-127">4</span><span class="sxs-lookup"><span data-stu-id="77cb2-127">4</span></span>      | <span data-ttu-id="77cb2-128">4</span><span class="sxs-lookup"><span data-stu-id="77cb2-128">4</span></span>      | <span data-ttu-id="77cb2-129">4</span><span class="sxs-lookup"><span data-stu-id="77cb2-129">4</span></span>      |        |
| <span data-ttu-id="77cb2-130">\_RGB5 GL</span><span class="sxs-lookup"><span data-stu-id="77cb2-130">GL\_RGB5</span></span>       | <span data-ttu-id="77cb2-131">\_RGB GL</span><span class="sxs-lookup"><span data-stu-id="77cb2-131">GL\_RGB</span></span>     | <span data-ttu-id="77cb2-132">5</span><span class="sxs-lookup"><span data-stu-id="77cb2-132">5</span></span>      | <span data-ttu-id="77cb2-133">5</span><span class="sxs-lookup"><span data-stu-id="77cb2-133">5</span></span>      | <span data-ttu-id="77cb2-134">5</span><span class="sxs-lookup"><span data-stu-id="77cb2-134">5</span></span>      |        |
| <span data-ttu-id="77cb2-135">\_RGB8 GL</span><span class="sxs-lookup"><span data-stu-id="77cb2-135">GL\_RGB8</span></span>       | <span data-ttu-id="77cb2-136">\_RGB GL</span><span class="sxs-lookup"><span data-stu-id="77cb2-136">GL\_RGB</span></span>     | <span data-ttu-id="77cb2-137">8</span><span class="sxs-lookup"><span data-stu-id="77cb2-137">8</span></span>      | <span data-ttu-id="77cb2-138">8</span><span class="sxs-lookup"><span data-stu-id="77cb2-138">8</span></span>      | <span data-ttu-id="77cb2-139">8</span><span class="sxs-lookup"><span data-stu-id="77cb2-139">8</span></span>      |        |
| <span data-ttu-id="77cb2-140">\_RGB10 GL</span><span class="sxs-lookup"><span data-stu-id="77cb2-140">GL\_RGB10</span></span>      | <span data-ttu-id="77cb2-141">\_RGB GL</span><span class="sxs-lookup"><span data-stu-id="77cb2-141">GL\_RGB</span></span>     | <span data-ttu-id="77cb2-142">10</span><span class="sxs-lookup"><span data-stu-id="77cb2-142">10</span></span>     | <span data-ttu-id="77cb2-143">10</span><span class="sxs-lookup"><span data-stu-id="77cb2-143">10</span></span>     | <span data-ttu-id="77cb2-144">10</span><span class="sxs-lookup"><span data-stu-id="77cb2-144">10</span></span>     |        |
| <span data-ttu-id="77cb2-145">\_RGB12 GL</span><span class="sxs-lookup"><span data-stu-id="77cb2-145">GL\_RGB12</span></span>      | <span data-ttu-id="77cb2-146">\_RGB GL</span><span class="sxs-lookup"><span data-stu-id="77cb2-146">GL\_RGB</span></span>     | <span data-ttu-id="77cb2-147">12</span><span class="sxs-lookup"><span data-stu-id="77cb2-147">12</span></span>     | <span data-ttu-id="77cb2-148">12</span><span class="sxs-lookup"><span data-stu-id="77cb2-148">12</span></span>     | <span data-ttu-id="77cb2-149">12</span><span class="sxs-lookup"><span data-stu-id="77cb2-149">12</span></span>     |        |
| <span data-ttu-id="77cb2-150">\_RGB16 GL</span><span class="sxs-lookup"><span data-stu-id="77cb2-150">GL\_RGB16</span></span>      | <span data-ttu-id="77cb2-151">\_RGB GL</span><span class="sxs-lookup"><span data-stu-id="77cb2-151">GL\_RGB</span></span>     | <span data-ttu-id="77cb2-152">16</span><span class="sxs-lookup"><span data-stu-id="77cb2-152">16</span></span>     | <span data-ttu-id="77cb2-153">16</span><span class="sxs-lookup"><span data-stu-id="77cb2-153">16</span></span>     | <span data-ttu-id="77cb2-154">16</span><span class="sxs-lookup"><span data-stu-id="77cb2-154">16</span></span>     |        |
| <span data-ttu-id="77cb2-155">\_RGBA2 GL</span><span class="sxs-lookup"><span data-stu-id="77cb2-155">GL\_RGBA2</span></span>      | <span data-ttu-id="77cb2-156">GL \_ RVBA</span><span class="sxs-lookup"><span data-stu-id="77cb2-156">GL\_RGBA</span></span>    | <span data-ttu-id="77cb2-157">2</span><span class="sxs-lookup"><span data-stu-id="77cb2-157">2</span></span>      | <span data-ttu-id="77cb2-158">2</span><span class="sxs-lookup"><span data-stu-id="77cb2-158">2</span></span>      | <span data-ttu-id="77cb2-159">2</span><span class="sxs-lookup"><span data-stu-id="77cb2-159">2</span></span>      | <span data-ttu-id="77cb2-160">2</span><span class="sxs-lookup"><span data-stu-id="77cb2-160">2</span></span>      |
| <span data-ttu-id="77cb2-161">\_RGBA4 GL</span><span class="sxs-lookup"><span data-stu-id="77cb2-161">GL\_RGBA4</span></span>      | <span data-ttu-id="77cb2-162">GL \_ RVBA</span><span class="sxs-lookup"><span data-stu-id="77cb2-162">GL\_RGBA</span></span>    | <span data-ttu-id="77cb2-163">4</span><span class="sxs-lookup"><span data-stu-id="77cb2-163">4</span></span>      | <span data-ttu-id="77cb2-164">4</span><span class="sxs-lookup"><span data-stu-id="77cb2-164">4</span></span>      | <span data-ttu-id="77cb2-165">4</span><span class="sxs-lookup"><span data-stu-id="77cb2-165">4</span></span>      | <span data-ttu-id="77cb2-166">4</span><span class="sxs-lookup"><span data-stu-id="77cb2-166">4</span></span>      |
| <span data-ttu-id="77cb2-167">GL \_ RGB5 \_ a1</span><span class="sxs-lookup"><span data-stu-id="77cb2-167">GL\_RGB5\_A1</span></span>   | <span data-ttu-id="77cb2-168">GL \_ RVBA</span><span class="sxs-lookup"><span data-stu-id="77cb2-168">GL\_RGBA</span></span>    | <span data-ttu-id="77cb2-169">5</span><span class="sxs-lookup"><span data-stu-id="77cb2-169">5</span></span>      | <span data-ttu-id="77cb2-170">5</span><span class="sxs-lookup"><span data-stu-id="77cb2-170">5</span></span>      | <span data-ttu-id="77cb2-171">5</span><span class="sxs-lookup"><span data-stu-id="77cb2-171">5</span></span>      | <span data-ttu-id="77cb2-172">1</span><span class="sxs-lookup"><span data-stu-id="77cb2-172">1</span></span>      |
| <span data-ttu-id="77cb2-173">\_RGBA8 GL</span><span class="sxs-lookup"><span data-stu-id="77cb2-173">GL\_RGBA8</span></span>      | <span data-ttu-id="77cb2-174">GL \_ RVBA</span><span class="sxs-lookup"><span data-stu-id="77cb2-174">GL\_RGBA</span></span>    | <span data-ttu-id="77cb2-175">8</span><span class="sxs-lookup"><span data-stu-id="77cb2-175">8</span></span>      | <span data-ttu-id="77cb2-176">8</span><span class="sxs-lookup"><span data-stu-id="77cb2-176">8</span></span>      | <span data-ttu-id="77cb2-177">8</span><span class="sxs-lookup"><span data-stu-id="77cb2-177">8</span></span>      | <span data-ttu-id="77cb2-178">8</span><span class="sxs-lookup"><span data-stu-id="77cb2-178">8</span></span>      |
| <span data-ttu-id="77cb2-179">GL \_ RG10 \_ a2</span><span class="sxs-lookup"><span data-stu-id="77cb2-179">GL\_RG10\_A2</span></span>   | <span data-ttu-id="77cb2-180">GL \_ RVBA</span><span class="sxs-lookup"><span data-stu-id="77cb2-180">GL\_RGBA</span></span>    | <span data-ttu-id="77cb2-181">10</span><span class="sxs-lookup"><span data-stu-id="77cb2-181">10</span></span>     | <span data-ttu-id="77cb2-182">10</span><span class="sxs-lookup"><span data-stu-id="77cb2-182">10</span></span>     | <span data-ttu-id="77cb2-183">10</span><span class="sxs-lookup"><span data-stu-id="77cb2-183">10</span></span>     | <span data-ttu-id="77cb2-184">2</span><span class="sxs-lookup"><span data-stu-id="77cb2-184">2</span></span>      |
| <span data-ttu-id="77cb2-185">\_RGB12 GL</span><span class="sxs-lookup"><span data-stu-id="77cb2-185">GL\_RGB12</span></span>      | <span data-ttu-id="77cb2-186">GL \_ RVBA</span><span class="sxs-lookup"><span data-stu-id="77cb2-186">GL\_RGBA</span></span>    | <span data-ttu-id="77cb2-187">12</span><span class="sxs-lookup"><span data-stu-id="77cb2-187">12</span></span>     | <span data-ttu-id="77cb2-188">12</span><span class="sxs-lookup"><span data-stu-id="77cb2-188">12</span></span>     | <span data-ttu-id="77cb2-189">12</span><span class="sxs-lookup"><span data-stu-id="77cb2-189">12</span></span>     | <span data-ttu-id="77cb2-190">12</span><span class="sxs-lookup"><span data-stu-id="77cb2-190">12</span></span>     |
| <span data-ttu-id="77cb2-191">\_RGBA16 GL</span><span class="sxs-lookup"><span data-stu-id="77cb2-191">GL\_RGBA16</span></span>     | <span data-ttu-id="77cb2-192">GL \_ RVBA</span><span class="sxs-lookup"><span data-stu-id="77cb2-192">GL\_RGBA</span></span>    | <span data-ttu-id="77cb2-193">16</span><span class="sxs-lookup"><span data-stu-id="77cb2-193">16</span></span>     | <span data-ttu-id="77cb2-194">16</span><span class="sxs-lookup"><span data-stu-id="77cb2-194">16</span></span>     | <span data-ttu-id="77cb2-195">16</span><span class="sxs-lookup"><span data-stu-id="77cb2-195">16</span></span>     | <span data-ttu-id="77cb2-196">16</span><span class="sxs-lookup"><span data-stu-id="77cb2-196">16</span></span>     |



 

</dd> <dt>

<span data-ttu-id="77cb2-197">*width*</span><span class="sxs-lookup"><span data-stu-id="77cb2-197">*width*</span></span> 
</dt> <dd>

<span data-ttu-id="77cb2-198">Taille de la palette.</span><span class="sxs-lookup"><span data-stu-id="77cb2-198">The size of the palette.</span></span> <span data-ttu-id="77cb2-199">Doit être 2n = 1 pour un entier *n*.</span><span class="sxs-lookup"><span data-stu-id="77cb2-199">Must be 2n = 1 for some integer *n*.</span></span>

</dd> <dt>

<span data-ttu-id="77cb2-200">*format*</span><span class="sxs-lookup"><span data-stu-id="77cb2-200">*format*</span></span> 
</dt> <dd>

<span data-ttu-id="77cb2-201">Format des données de pixels.</span><span class="sxs-lookup"><span data-stu-id="77cb2-201">The format of the pixel data.</span></span> <span data-ttu-id="77cb2-202">Les constantes symboliques suivantes sont acceptées.</span><span class="sxs-lookup"><span data-stu-id="77cb2-202">The following symbolic constants are accepted.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="77cb2-203">Valeur</span><span class="sxs-lookup"><span data-stu-id="77cb2-203">Value</span></span></th>
<th><span data-ttu-id="77cb2-204">Signification</span><span class="sxs-lookup"><span data-stu-id="77cb2-204">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="GL_RGBA"></span><span id="gl_rgba"></span><dl> <span data-ttu-id="77cb2-205"><dt><strong>GL_RGBA</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="77cb2-205"><dt><strong>GL_RGBA</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="77cb2-206">Chaque pixel est un groupe de quatre composants dans cet ordre : rouge, vert, bleu, alpha.</span><span class="sxs-lookup"><span data-stu-id="77cb2-206">Each pixel is a group of four components in this order: red, green, blue, alpha.</span></span> <span data-ttu-id="77cb2-207">Le format RVBA est déterminé de la façon suivante :</span><span class="sxs-lookup"><span data-stu-id="77cb2-207">The RGBA format is determined in this way:</span></span> <br/>
<ol>
<li><span data-ttu-id="77cb2-208">La fonction <strong>glColorTableEXT</strong> convertit les valeurs à virgule flottante directement en un format interne avec une précision non spécifiée.</span><span class="sxs-lookup"><span data-stu-id="77cb2-208">The <strong>glColorTableEXT</strong> function converts floating-point values directly to an internal format with unspecified precision.</span></span> <span data-ttu-id="77cb2-209">Les valeurs entières signées sont mappées de façon linéaire au format interne de telle sorte que la valeur entière représentable la plus positive corresponde à 1,0, et la valeur entière représentable la plus négative correspond à-1,0.</span><span class="sxs-lookup"><span data-stu-id="77cb2-209">Signed integer values are mapped linearly to the internal format such that the most positive representable integer value maps to 1.0, and the most negative representable integer value maps to -1.0.</span></span> <span data-ttu-id="77cb2-210">Les données entières non signées sont mappées de la même façon : la plus grande valeur entière correspond à 1,0, et zéro est mappé à 0,0.</span><span class="sxs-lookup"><span data-stu-id="77cb2-210">Unsigned integer data is mapped similarly: the largest integer value maps to 1.0, and zero maps to 0.0.</span></span></li>
<li><span data-ttu-id="77cb2-211">La fonction <strong>glColorTableEXT</strong> multiplie les valeurs de couleur résultantes par GL_c_SCALE et les ajoute à GL_c_BIAS, où <em>c</em> est rouge, vert, bleu et alpha pour les composants de couleur respectifs.</span><span class="sxs-lookup"><span data-stu-id="77cb2-211">The <strong>glColorTableEXT</strong> function multiplies the resulting color values by GL_c_SCALE and adds them to GL_c_BIAS, where <em>c</em> is RED, GREEN, BLUE, and ALPHA for the respective color components.</span></span> <span data-ttu-id="77cb2-212">Les résultats sont ancrés à la plage [0, 1].</span><span class="sxs-lookup"><span data-stu-id="77cb2-212">The results are clamped to the range [0,1].</span></span></li>
<li><span data-ttu-id="77cb2-213">Si GL_MAP_COLOR a la <strong>valeur true</strong>, <strong>glColorTableEXT</strong> met à l’échelle chaque composant de couleur en fonction de la taille de la table de recherche GL_PIXEL_MAP_c_TO_c, puis remplace le composant par la valeur qu’il référence dans cette table. <em>c</em> est R, G, B ou a, respectivement.</span><span class="sxs-lookup"><span data-stu-id="77cb2-213">If GL_MAP_COLOR is <strong>TRUE</strong>, <strong>glColorTableEXT</strong> scales each color component by the size of lookup table GL_PIXEL_MAP_c_TO_c, then replaces the component by the value that it references in that table; <em>c</em> is R, G, B, or A, respectively.</span></span></li>
<li><span data-ttu-id="77cb2-214">La fonction <strong>glColorTableEXT</strong> convertit les couleurs RVBA obtenues en fragments en attachant la coordonnée <em>z</em>et la coordonnée de texture de la position raster actuelle à chaque pixel, puis en affectant les coordonnées de la fenêtre <em>x</em> et <em>y</em> au <em>n</em>ième fragment, de telle sorte que<em>x</em>?</span><span class="sxs-lookup"><span data-stu-id="77cb2-214">The <strong>glColorTableEXT</strong> function converts the resulting RGBA colors to fragments by attaching the current raster position <em>z</em>-coordinate and texture coordinates to each pixel, then assigning <em>x</em> and <em>y</em> window coordinates to the <em>n</em>th fragment such that<em>x</em>?</span></span><span data-ttu-id="77cb2-215"> = <em>x</em><sub>r</sub> + <em>n</em> mod <em>largeur</em></span><span class="sxs-lookup"><span data-stu-id="77cb2-215"> = <em>x</em><sub>r</sub> + <em>n</em> mod <em>width</em></span></span><br/> <span data-ttu-id="77cb2-216"><em></em>y?</span><span class="sxs-lookup"><span data-stu-id="77cb2-216"><em></em>y?</span></span><span data-ttu-id="77cb2-217"> = <em></em><sub>r</sub> +<em>n/largeur</em> o</span><span class="sxs-lookup"><span data-stu-id="77cb2-217"> = <em>y</em><sub>r</sub> +<em>n / width</em></span></span><br/> <span data-ttu-id="77cb2-218">où (<em>x</em><sub>r</sub> , <em>y</em><sub>r</sub> ) est la position de la trame actuelle.</span><span class="sxs-lookup"><span data-stu-id="77cb2-218">where (<em>x</em><sub>r</sub> , <em>y</em><sub>r</sub> ) is the current raster position.</span></span><br/></li>
<li><span data-ttu-id="77cb2-219">Ces fragments de pixels sont ensuite traités comme les fragments générés par la pixellisation des points, des lignes ou des polygones.</span><span class="sxs-lookup"><span data-stu-id="77cb2-219">These pixel fragments are then treated just like the fragments generated by rasterizing points, lines, or polygons.</span></span> <span data-ttu-id="77cb2-220">La fonction <strong>glColorTableEXT</strong> applique le mappage de texture, le brouillard et toutes les opérations de fragment avant d’écrire les fragments dans le trame.</span><span class="sxs-lookup"><span data-stu-id="77cb2-220">The <strong>glColorTableEXT</strong> function applies texture mapping, fog, and all the fragment operations before writing the fragments to the framebuffer.</span></span></li>
</ol></td>
</tr>
<tr class="even">
<td><span id="GL_RED"></span><span id="gl_red"></span><dl> <span data-ttu-id="77cb2-221"><dt><strong>GL_RED</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="77cb2-221"><dt><strong>GL_RED</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="77cb2-222">Chaque pixel est un composant rouge unique.</span><span class="sxs-lookup"><span data-stu-id="77cb2-222">Each pixel is a single red component.</span></span><br/> <span data-ttu-id="77cb2-223">La fonction <strong>glColorTableEXT</strong> convertit ce composant au format interne de la même façon que le composant rouge d’un pixel RVBA est, puis le convertit en pixel RVBA avec le vert et le bleu réglés sur 0,0 et alpha défini sur 1,0.</span><span class="sxs-lookup"><span data-stu-id="77cb2-223">The <strong>glColorTableEXT</strong> function converts this component to the internal format in the same way that the red component of an RGBA pixel is, then converts it to an RGBA pixel with green and blue set to 0.0, and alpha set to 1.0.</span></span> <span data-ttu-id="77cb2-224">Après cette conversion, le pixel est traité comme s’il avait été lu en tant que pixel RVBA.</span><span class="sxs-lookup"><span data-stu-id="77cb2-224">After this conversion, the pixel is treated just as if it had been read as an RGBA pixel.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="GL_GREEN"></span><span id="gl_green"></span><dl> <span data-ttu-id="77cb2-225"><dt><strong>GL_GREEN</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="77cb2-225"><dt><strong>GL_GREEN</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="77cb2-226">Chaque pixel est un composant vert unique.</span><span class="sxs-lookup"><span data-stu-id="77cb2-226">Each pixel is a single green component.</span></span><br/> <span data-ttu-id="77cb2-227">La fonction <strong>glColorTableEXT</strong> convertit ce composant au format interne de la même façon que le composant vert d’un pixel RVBA est, puis le convertit en pixel RVBA avec rouge et bleu défini sur 0,0, et alpha défini sur 1,0.</span><span class="sxs-lookup"><span data-stu-id="77cb2-227">The <strong>glColorTableEXT</strong> function converts this component to the internal format in the same way that the green component of an RGBA pixel is, and then converts it to an RGBA pixel with red and blue set to 0.0, and alpha set to 1.0.</span></span> <span data-ttu-id="77cb2-228">Après cette conversion, le pixel est traité comme s’il avait été lu en tant que pixel RVBA.</span><span class="sxs-lookup"><span data-stu-id="77cb2-228">After this conversion, the pixel is treated just as if it had been read as an RGBA pixel.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="GL_BLUE"></span><span id="gl_blue"></span><dl> <span data-ttu-id="77cb2-229"><dt><strong>GL_BLUE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="77cb2-229"><dt><strong>GL_BLUE</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="77cb2-230">Chaque pixel est un composant bleu unique.</span><span class="sxs-lookup"><span data-stu-id="77cb2-230">Each pixel is a single blue component.</span></span><br/> <span data-ttu-id="77cb2-231">La fonction <strong>glColorTableEXT</strong> convertit ce composant au format interne de la même façon que le composant bleu d’un pixel RVBA est, puis le convertit en pixel RVBA avec Red et Green défini sur 0,0, et alpha défini sur 1,0.</span><span class="sxs-lookup"><span data-stu-id="77cb2-231">The <strong>glColorTableEXT</strong> function converts this component to the internal format in the same way that the blue component of an RGBA pixel is, and then converts it to an RGBA pixel with red and green set to 0.0, and alpha set to 1.0.</span></span> <span data-ttu-id="77cb2-232">Après cette conversion, le pixel est traité comme s’il avait été lu en tant que pixel RVBA.</span><span class="sxs-lookup"><span data-stu-id="77cb2-232">After this conversion, the pixel is treated just as if it had been read as an RGBA pixel.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="GL_ALPHA"></span><span id="gl_alpha"></span><dl> <span data-ttu-id="77cb2-233"><dt><strong>GL_ALPHA</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="77cb2-233"><dt><strong>GL_ALPHA</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="77cb2-234">Chaque pixel est un composant alpha unique.</span><span class="sxs-lookup"><span data-stu-id="77cb2-234">Each pixel is a single alpha component.</span></span><br/> <span data-ttu-id="77cb2-235">La fonction <strong>glColorTableEXT</strong> convertit ce composant au format interne de la même façon que le composant alpha d’un pixel RVBA est, puis le convertit en un pixel RVBA avec rouge, vert et bleu défini sur 0,0.</span><span class="sxs-lookup"><span data-stu-id="77cb2-235">The <strong>glColorTableEXT</strong> function converts this component to the internal format in the same way that the alpha component of an RGBA pixel is, and then converts it to an RGBA pixel with red, green, and blue set to 0.0.</span></span> <span data-ttu-id="77cb2-236">Après cette conversion, le pixel est traité comme s’il avait été lu en tant que pixel RVBA.</span><span class="sxs-lookup"><span data-stu-id="77cb2-236">After this conversion, the pixel is treated just as if it had been read as an RGBA pixel.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="GL_RGB"></span><span id="gl_rgb"></span><dl> <span data-ttu-id="77cb2-237"><dt><strong>GL_RGB</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="77cb2-237"><dt><strong>GL_RGB</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="77cb2-238">Chaque pixel est un groupe de trois composants dans cet ordre : rouge, vert, bleu.</span><span class="sxs-lookup"><span data-stu-id="77cb2-238">Each pixel is a group of three components in this order: red, green, blue.</span></span><br/> <span data-ttu-id="77cb2-239">La fonction <strong>glColorTableEXT</strong> convertit chaque composant au format interne de la même façon que les composants rouge, vert et bleu d’un pixel RVBA.</span><span class="sxs-lookup"><span data-stu-id="77cb2-239">The <strong>glColorTableEXT</strong> function converts each component to the internal format in the same way that the red, green, and blue components of an RGBA pixel are.</span></span> <span data-ttu-id="77cb2-240">La triple couleur est convertie en un pixel RVBA avec alpha défini sur 1,0.</span><span class="sxs-lookup"><span data-stu-id="77cb2-240">The color triple is converted to an RGBA pixel with alpha set to 1.0.</span></span> <span data-ttu-id="77cb2-241">Après cette conversion, le pixel est traité comme s’il avait été lu en tant que pixel RVBA.</span><span class="sxs-lookup"><span data-stu-id="77cb2-241">After this conversion, the pixel is treated just as if it had been read as an RGBA pixel.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="GL_BGR_EXT"></span><span id="gl_bgr_ext"></span><dl> <span data-ttu-id="77cb2-242"><dt><strong>GL_BGR_EXT</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="77cb2-242"><dt><strong>GL_BGR_EXT</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="77cb2-243">Chaque pixel est un groupe de trois composants dans cet ordre : bleu, vert, rouge.</span><span class="sxs-lookup"><span data-stu-id="77cb2-243">Each pixel is a group of three components in this order: blue, green, red.</span></span><br/> <span data-ttu-id="77cb2-244">GL_BGR_EXT fournit un format qui correspond à la disposition mémoire des bitmaps indépendants du périphérique Windows (DIB).</span><span class="sxs-lookup"><span data-stu-id="77cb2-244">GL_BGR_EXT provides a format that matches the memory layout of Windows device-independent bitmaps (DIBs).</span></span> <span data-ttu-id="77cb2-245">Par conséquent, vos applications peuvent utiliser les mêmes données avec les appels de fonction Windows et les appels de fonction de pixel OpenGL.</span><span class="sxs-lookup"><span data-stu-id="77cb2-245">Thus your applications can use the same data with Windows function calls and OpenGL pixel function calls.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="GL_BGRA_EXT"></span><span id="gl_bgra_ext"></span><dl> <span data-ttu-id="77cb2-246"><dt><strong>GL_BGRA_EXT</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="77cb2-246"><dt><strong>GL_BGRA_EXT</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="77cb2-247">Chaque pixel est un groupe de quatre composants dans l’ordre suivant : bleu, vert, rouge, alpha.</span><span class="sxs-lookup"><span data-stu-id="77cb2-247">Each pixel is a group of four components in this order: blue, green, red, alpha.</span></span><br/> <span data-ttu-id="77cb2-248">GL_BGRA_EXT fournit un format qui correspond à la disposition mémoire des bitmaps indépendants du périphérique Windows (DIB).</span><span class="sxs-lookup"><span data-stu-id="77cb2-248">GL_BGRA_EXT provides a format that matches the memory layout of Windows device-independent bitmaps (DIBs).</span></span> <span data-ttu-id="77cb2-249">Par conséquent, vos applications peuvent utiliser les mêmes données avec les appels de fonction Windows et les appels de fonction de pixel OpenGL.</span><span class="sxs-lookup"><span data-stu-id="77cb2-249">Thus your applications can use the same data with Windows function calls and OpenGL pixel function calls.</span></span><br/></td>
</tr>
</tbody>
</table>



 

</dd> <dt>

<span data-ttu-id="77cb2-250">*type*</span><span class="sxs-lookup"><span data-stu-id="77cb2-250">*type*</span></span> 
</dt> <dd>

<span data-ttu-id="77cb2-251">Type de données pour les *données*.</span><span class="sxs-lookup"><span data-stu-id="77cb2-251">The data type for *data*.</span></span> <span data-ttu-id="77cb2-252">Les constantes symboliques suivantes sont acceptées : \_ octet non signé GL \_ , \_ octet GL, GL \_ non signé \_ short, GL \_ short, GL \_ unsigned \_ int, GL \_ int et GL \_ float.</span><span class="sxs-lookup"><span data-stu-id="77cb2-252">The following symbolic constants are accepted: GL\_UNSIGNED\_BYTE, GL\_BYTE, GL\_UNSIGNED\_SHORT, GL\_SHORT, GL\_UNSIGNED\_INT, GL\_INT, and GL\_FLOAT.</span></span>

<span data-ttu-id="77cb2-253">Le tableau suivant résume la signification des constantes valides pour le paramètre de *type* .</span><span class="sxs-lookup"><span data-stu-id="77cb2-253">The following table summarizes the meaning of the valid constants for the *type* parameter.</span></span>



| <span data-ttu-id="77cb2-254">Valeur</span><span class="sxs-lookup"><span data-stu-id="77cb2-254">Value</span></span>                                                                                                                                                                      | <span data-ttu-id="77cb2-255">Signification</span><span class="sxs-lookup"><span data-stu-id="77cb2-255">Meaning</span></span>                                          |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------|
| <span id="GL_UNSIGNED_BYTE"></span><span id="gl_unsigned_byte"></span><dl> <span data-ttu-id="77cb2-256"><dt>**\_octet non signé GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="77cb2-256"><dt>**GL\_UNSIGNED\_BYTE**</dt></span></span> </dl>    | <span data-ttu-id="77cb2-257">Entier 8 bits non signé</span><span class="sxs-lookup"><span data-stu-id="77cb2-257">Unsigned 8-bit integer</span></span><br/>                |
| <span id="GL_BYTE"></span><span id="gl_byte"></span><dl> <span data-ttu-id="77cb2-258"><dt>**\_octet GL**</dt></span><span class="sxs-lookup"><span data-stu-id="77cb2-258"><dt>**GL\_BYTE**</dt></span></span> </dl>                                | <span data-ttu-id="77cb2-259">Entier 8 bits signé</span><span class="sxs-lookup"><span data-stu-id="77cb2-259">Signed 8-bit integer</span></span><br/>                  |
| <span id="GL_UNSIGNED_SHORT"></span><span id="gl_unsigned_short"></span><dl> <span data-ttu-id="77cb2-260"><dt>**NON signé dans le GL \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="77cb2-260"><dt>**GL\_UNSIGNED\_SHORT**</dt></span></span> </dl> | <span data-ttu-id="77cb2-261">Entier 16 bits non signé</span><span class="sxs-lookup"><span data-stu-id="77cb2-261">Unsigned 16-bit integer</span></span><br/>               |
| <span id="GL_SHORT"></span><span id="gl_short"></span><dl> <span data-ttu-id="77cb2-262"><dt>**\_abrégé GL**</dt></span><span class="sxs-lookup"><span data-stu-id="77cb2-262"><dt>**GL\_SHORT**</dt></span></span> </dl>                             | <span data-ttu-id="77cb2-263">Entier 16 bits signé</span><span class="sxs-lookup"><span data-stu-id="77cb2-263">Signed 16-bit integer</span></span><br/>                 |
| <span id="GL_UNSIGNED_INT"></span><span id="gl_unsigned_int"></span><dl> <span data-ttu-id="77cb2-264"><dt>**\_entier non signé GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="77cb2-264"><dt>**GL\_UNSIGNED\_INT**</dt></span></span> </dl>       | <span data-ttu-id="77cb2-265">Entier 32 bits non signé</span><span class="sxs-lookup"><span data-stu-id="77cb2-265">Unsigned 32-bit integer</span></span><br/>               |
| <span id="GL_INT"></span><span id="gl_int"></span><dl> <span data-ttu-id="77cb2-266"><dt>**GL \_ int**</dt></span><span class="sxs-lookup"><span data-stu-id="77cb2-266"><dt>**GL\_INT**</dt></span></span> </dl>                                   | <span data-ttu-id="77cb2-267">Entier de 32 bits</span><span class="sxs-lookup"><span data-stu-id="77cb2-267">32-bit integer</span></span><br/>                        |
| <span id="GL_FLOAT"></span><span id="gl_float"></span><dl> <span data-ttu-id="77cb2-268"><dt>**valeur \_ float du GL**</dt></span><span class="sxs-lookup"><span data-stu-id="77cb2-268"><dt>**GL\_FLOAT**</dt></span></span> </dl>                             | <span data-ttu-id="77cb2-269">Valeur à virgule flottante simple précision</span><span class="sxs-lookup"><span data-stu-id="77cb2-269">Single-precision floating-point value</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="77cb2-270">*data*</span><span class="sxs-lookup"><span data-stu-id="77cb2-270">*data*</span></span> 
</dt> <dd>

<span data-ttu-id="77cb2-271">Pointeur vers les données de texture de palette.</span><span class="sxs-lookup"><span data-stu-id="77cb2-271">A pointer to the paletted texture data.</span></span> <span data-ttu-id="77cb2-272">Les données sont traitées comme des pixels uniques d’une entrée de palette de texture 1D pour une entrée de palette.</span><span class="sxs-lookup"><span data-stu-id="77cb2-272">The data is treated as single pixels of a 1-D texture palette entry for a palette entry.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="77cb2-273">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="77cb2-273">Return value</span></span>

<span data-ttu-id="77cb2-274">Cette fonction ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="77cb2-274">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="77cb2-275">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="77cb2-275">Error codes</span></span>

<span data-ttu-id="77cb2-276">Les codes d’erreur suivants peuvent être récupérés par la fonction [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="77cb2-276">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="77cb2-277">Nom</span><span class="sxs-lookup"><span data-stu-id="77cb2-277">Name</span></span>                                                                                                  | <span data-ttu-id="77cb2-278">Signification</span><span class="sxs-lookup"><span data-stu-id="77cb2-278">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="77cb2-279"><dt>**\_valeur non valide du GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="77cb2-279"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="77cb2-280">la *largeur* était un entier non valide.</span><span class="sxs-lookup"><span data-stu-id="77cb2-280">*width* was an invalid integer.</span></span><br/>                                                                                            |
| <dl> <span data-ttu-id="77cb2-281"><dt>**\_enum GL non valide \_**</dt></span><span class="sxs-lookup"><span data-stu-id="77cb2-281"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="77cb2-282">*target*, *internalFormat*, *format* ou *type* n’est pas une valeur acceptée.</span><span class="sxs-lookup"><span data-stu-id="77cb2-282">*target*, *internalFormat*, *format*, or *type* was not an accepted value.</span></span><br/>                                                 |
| <dl> <span data-ttu-id="77cb2-283"><dt>**\_opération non valide du GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="77cb2-283"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="77cb2-284">La fonction a été appelée entre un appel à [**glBegin**](glbegin.md) et l’appel correspondant à [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="77cb2-284">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="77cb2-285">Notes</span><span class="sxs-lookup"><span data-stu-id="77cb2-285">Remarks</span></span>

<span data-ttu-id="77cb2-286">Les textures de palette sont définies à l’aide d’une palette de couleurs et d’un ensemble de données d’image composé d’index pour les entrées de couleur d’une palette (une table des couleurs).</span><span class="sxs-lookup"><span data-stu-id="77cb2-286">Paletted textures are defined with a palette of colors and a set of image data that is composed of indexes to color entries of a palette (a color table).</span></span>

<span data-ttu-id="77cb2-287">La fonction **glColorTableEXT** spécifie la palette de texture d’une texture ciblée.</span><span class="sxs-lookup"><span data-stu-id="77cb2-287">The **glColorTableEXT** function specifies the texture palette of a targeted texture.</span></span> <span data-ttu-id="77cb2-288">Il récupère les *données* de la mémoire et convertit les données comme si chaque entrée de palette était un pixel unique d’une texture 1D.</span><span class="sxs-lookup"><span data-stu-id="77cb2-288">It takes the *data* from memory and converts the data as if each palette entry is a single pixel of a 1-D texture.</span></span> <span data-ttu-id="77cb2-289">La fonction **glColorTableEXT** décompresse et convertit les données et les convertit dans un format interne qui correspond le mieux au *format* donné.</span><span class="sxs-lookup"><span data-stu-id="77cb2-289">The **glColorTableEXT** function unpacks and converts the data and translates it into an internal format that matches the given *format* as closely as possible.</span></span>

<span data-ttu-id="77cb2-290">Si la *largeur* d’une palette est supérieure à la plage d’index de couleurs dans les données de texture, certaines entrées de palette ne sont pas utilisées.</span><span class="sxs-lookup"><span data-stu-id="77cb2-290">If a palette's *width* is greater than the range of the color indexes in the texture data, some of the palette entries are unused.</span></span> <span data-ttu-id="77cb2-291">Si la *largeur* d’une palette est inférieure à la plage des index de couleurs dans les données de texture, les bits les plus significatifs des données de texture sont ignorés et seul le nombre approprié de bits dans l’index est utilisé lors de l’accès à la palette.</span><span class="sxs-lookup"><span data-stu-id="77cb2-291">If a palette's *width* is less than the range of the color indexes in the texture data, the most significant bits of the texture data are ignored and only the appropriate number of bits in the index are used when accessing the palette.</span></span> <span data-ttu-id="77cb2-292">Lorsque vous spécifiez une *cible* de proxy à l’aide de la \_ texture \_ de proxy 1D ou \_ de la texture de proxy \_ 2D, la palette de la texture du proxy est redimensionnée et ses paramètres sont définis, mais aucune donnée n’est transférée ou accessible.</span><span class="sxs-lookup"><span data-stu-id="77cb2-292">When you specify a proxy *target* using PROXY\_TEXTURE\_1D or PROXY\_TEXTURE\_2D, the palette of the proxy texture is resized and its parameters are set but no data is transferred or accessed.</span></span>

<span data-ttu-id="77cb2-293">Lorsque le paramètre *cible* est \_ une texture \_ de proxy de GL \_ 1D ou \_ une texture de proxy GL \_ \_ 2D, et que l’implémentation ne prend pas en charge les valeurs spécifiées pour le *format* ou la *largeur*, **glColorTableEXT** peut ne pas réussir à créer la table de couleurs demandée.</span><span class="sxs-lookup"><span data-stu-id="77cb2-293">When the *target* parameter is GL\_PROXY\_TEXTURE\_1D or GL\_PROXY\_TEXTURE\_2D, and the implementation does not support the values specified for either *format* or *width*, **glColorTableEXT** can fail to create the requested color table.</span></span> <span data-ttu-id="77cb2-294">Dans ce cas, la table des couleurs est vide et tous les paramètres récupérés sont nuls.</span><span class="sxs-lookup"><span data-stu-id="77cb2-294">In this case, the color table is empty and all parameters retrieved will be zero.</span></span> <span data-ttu-id="77cb2-295">Vous pouvez déterminer si OpenGL prend en charge un format et une taille de table de couleur particuliers en appelant **glColorTableEXT** avec une cible de proxy, puis en appelant [**glGetColorTableParameterivEXT**](glgetcolortableparameterivext.md) ou [**glGetColorTableParameterfvEXT**](glgetcolortableparameterfvext.md) pour déterminer si le paramètre Width correspond à celui défini par **glColorTableEXT**.</span><span class="sxs-lookup"><span data-stu-id="77cb2-295">You can determine whether OpenGL supports a particular color table format and size by calling **glColorTableEXT** with a proxy target, and then calling [**glGetColorTableParameterivEXT**](glgetcolortableparameterivext.md) or [**glGetColorTableParameterfvEXT**](glgetcolortableparameterfvext.md) to determine whether the width parameter matches that set by **glColorTableEXT**.</span></span> <span data-ttu-id="77cb2-296">Si la largeur Récupérée est égale à zéro, la requête de la table de couleurs par **glColorTable** a échoué.</span><span class="sxs-lookup"><span data-stu-id="77cb2-296">If the retrieved width is zero, the color table request by **glColorTable** failed.</span></span> <span data-ttu-id="77cb2-297">Si la largeur Récupérée n’est pas égale à zéro, vous pouvez appeler **glColorTable** avec la cible réelle avec la texture \_ 1D ou texture \_ 2D pour définir la table des couleurs.</span><span class="sxs-lookup"><span data-stu-id="77cb2-297">If the retrieved width is not zero, you can call **glColorTable** with the real target with TEXTURE\_1D or TEXTURE\_2D to set the color table.</span></span>

> [!Note]  
> <span data-ttu-id="77cb2-298">La fonction **glColorTableEXT** est une fonction d’extension qui ne fait pas partie de la bibliothèque OpenGL standard, mais qui fait partie de l' \_ extension de texture de palette ext GL \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="77cb2-298">The **glColorTableEXT** function is an extension function that is not part of the standard OpenGL library but is part of the GL\_EXT\_paletted\_texture extension.</span></span> <span data-ttu-id="77cb2-299">Pour vérifier si votre implémentation d’OpenGL prend en charge **glColorTableEXT**, appelez [**glGetString**](glgetstring.md)( \_ Extensions GL).</span><span class="sxs-lookup"><span data-stu-id="77cb2-299">To check whether your implementation of OpenGL supports **glColorTableEXT**, call [**glGetString**](glgetstring.md)(GL\_EXTENSIONS).</span></span> <span data-ttu-id="77cb2-300">Si elle retourne la \_ \_ texture de palette ext GL \_ , **glColorTableEXT** est pris en charge.</span><span class="sxs-lookup"><span data-stu-id="77cb2-300">If it returns GL\_EXT\_paletted\_texture, **glColorTableEXT** is supported.</span></span> <span data-ttu-id="77cb2-301">Pour obtenir l’adresse de fonction d’une fonction d’extension, appelez [**wglGetProcAddress**](/windows/desktop/api/wingdi/nf-wingdi-wglgetprocaddress).</span><span class="sxs-lookup"><span data-stu-id="77cb2-301">To obtain the function address of an extension function, call [**wglGetProcAddress**](/windows/desktop/api/wingdi/nf-wingdi-wglgetprocaddress).</span></span>

 

<span data-ttu-id="77cb2-302">Pour récupérer les données de la table des couleurs réelles spécifiées par la fonction **glColorTableEXT** , appelez [**glGetColorTableEXT**](glgetcolortableext.md).</span><span class="sxs-lookup"><span data-stu-id="77cb2-302">To retrieve the actual color table data specified by the **glColorTableEXT** function, call [**glGetColorTableEXT**](glgetcolortableext.md).</span></span> <span data-ttu-id="77cb2-303">Pour récupérer les paramètres, tels que la *largeur* et le *format*, de la table de couleurs spécifiée par la fonction **GlColorTableEXT** , appelez la fonction **glGetColorTableParameterivEXT** ou **glGetColorTableParameterfvEXT** .</span><span class="sxs-lookup"><span data-stu-id="77cb2-303">To retrieve the parameters, such as *width* and *format*, of the color table specified by the **glColorTableEXT** function, call the **glGetColorTableParameterivEXT** or **glGetColorTableParameterfvEXT** function.</span></span>

## <a name="requirements"></a><span data-ttu-id="77cb2-304">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="77cb2-304">Requirements</span></span>



| <span data-ttu-id="77cb2-305">Condition requise</span><span class="sxs-lookup"><span data-stu-id="77cb2-305">Requirement</span></span> | <span data-ttu-id="77cb2-306">Valeur</span><span class="sxs-lookup"><span data-stu-id="77cb2-306">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="77cb2-307">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="77cb2-307">Minimum supported client</span></span><br/> | <span data-ttu-id="77cb2-308">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="77cb2-308">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                      |
| <span data-ttu-id="77cb2-309">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="77cb2-309">Minimum supported server</span></span><br/> | <span data-ttu-id="77cb2-310">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="77cb2-310">Windows 2000 Server \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="77cb2-311">En-tête</span><span class="sxs-lookup"><span data-stu-id="77cb2-311">Header</span></span><br/>                   | <dl> <span data-ttu-id="77cb2-312"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="77cb2-312"><dt>Gl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="77cb2-313">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="77cb2-313">See also</span></span>

<dl> <dt>

[<span data-ttu-id="77cb2-314">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="77cb2-314">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="77cb2-315">**glColorSubTableEXT**</span><span class="sxs-lookup"><span data-stu-id="77cb2-315">**glColorSubTableEXT**</span></span>](glcolorsubtableext.md)
</dt> <dt>

[<span data-ttu-id="77cb2-316">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="77cb2-316">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="77cb2-317">**glGetColorTableEXT**</span><span class="sxs-lookup"><span data-stu-id="77cb2-317">**glGetColorTableEXT**</span></span>](glgetcolortableext.md)
</dt> <dt>

[<span data-ttu-id="77cb2-318">**glGetColorTableParameterfvEXT**</span><span class="sxs-lookup"><span data-stu-id="77cb2-318">**glGetColorTableParameterfvEXT**</span></span>](glgetcolortableparameterfvext.md)
</dt> <dt>

[<span data-ttu-id="77cb2-319">**glGetColorTableParameterivEXT**</span><span class="sxs-lookup"><span data-stu-id="77cb2-319">**glGetColorTableParameterivEXT**</span></span>](glgetcolortableparameterivext.md)
</dt> <dt>

[<span data-ttu-id="77cb2-320">**wglGetProcAddress**</span><span class="sxs-lookup"><span data-stu-id="77cb2-320">**wglGetProcAddress**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-wglgetprocaddress)
</dt> </dl>

 

 





