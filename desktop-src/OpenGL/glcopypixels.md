---
title: fonction glCopyPixels (GL. h)
description: La fonction glCopyPixels copie les pixels dans le trame.
ms.assetid: c4055928-7b8b-4d0f-94f3-e3b9c0503308
keywords:
- glCopyPixels fonction OpenGL
topic_type:
- apiref
api_name:
- glCopyPixels
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4a7ba0833534d21e48c251da6491fee2996c3ed9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942262"
---
# <a name="glcopypixels-function"></a><span data-ttu-id="b8b77-104">glCopyPixels fonction)</span><span class="sxs-lookup"><span data-stu-id="b8b77-104">glCopyPixels function</span></span>

<span data-ttu-id="b8b77-105">La fonction **glCopyPixels** copie les pixels dans le trame.</span><span class="sxs-lookup"><span data-stu-id="b8b77-105">The **glCopyPixels** function copies pixels in the framebuffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="b8b77-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b8b77-106">Syntax</span></span>


```C++
void WINAPI glCopyPixels(
   GLint   x,
   GLint   y,
   GLsizei width,
   GLsizei height,
   GLenum  type
);
```



## <a name="parameters"></a><span data-ttu-id="b8b77-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b8b77-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b8b77-108">*x*</span><span class="sxs-lookup"><span data-stu-id="b8b77-108">*x*</span></span> 
</dt> <dd>

<span data-ttu-id="b8b77-109">Coordonnée du plan x de la fenêtre du coin inférieur gauche de la zone rectangulaire de pixels à copier.</span><span class="sxs-lookup"><span data-stu-id="b8b77-109">The window x-plane coordinate of the lower-left corner of the rectangular region of pixels to be copied.</span></span>

</dd> <dt>

<span data-ttu-id="b8b77-110">*y*</span><span class="sxs-lookup"><span data-stu-id="b8b77-110">*y*</span></span> 
</dt> <dd>

<span data-ttu-id="b8b77-111">Coordonnée du plan y de la fenêtre du coin inférieur gauche de la zone rectangulaire de pixels à copier.</span><span class="sxs-lookup"><span data-stu-id="b8b77-111">The window y-plane coordinate of the lower-left corner of the rectangular region of pixels to be copied.</span></span>

</dd> <dt>

<span data-ttu-id="b8b77-112">*width*</span><span class="sxs-lookup"><span data-stu-id="b8b77-112">*width*</span></span> 
</dt> <dd>

<span data-ttu-id="b8b77-113">Dimension de largeur de la zone rectangulaire de pixels à copier.</span><span class="sxs-lookup"><span data-stu-id="b8b77-113">The width dimension of the rectangular region of pixels to be copied.</span></span> <span data-ttu-id="b8b77-114">Il ne doit pas être négatif.</span><span class="sxs-lookup"><span data-stu-id="b8b77-114">Must be nonnegative.</span></span>

</dd> <dt>

<span data-ttu-id="b8b77-115">*height*</span><span class="sxs-lookup"><span data-stu-id="b8b77-115">*height*</span></span> 
</dt> <dd>

<span data-ttu-id="b8b77-116">Dimension de la hauteur de la zone rectangulaire de pixels à copier.</span><span class="sxs-lookup"><span data-stu-id="b8b77-116">The height dimension of the rectangular region of pixels to be copied.</span></span> <span data-ttu-id="b8b77-117">Il ne doit pas être négatif.</span><span class="sxs-lookup"><span data-stu-id="b8b77-117">Must be nonnegative.</span></span>

</dd> <dt>

<span data-ttu-id="b8b77-118">*type*</span><span class="sxs-lookup"><span data-stu-id="b8b77-118">*type*</span></span> 
</dt> <dd>

<span data-ttu-id="b8b77-119">Spécifie si **glCopyPixels** doit copier les valeurs de couleur, les valeurs de profondeur ou les valeurs de gabarit.</span><span class="sxs-lookup"><span data-stu-id="b8b77-119">Specifies whether **glCopyPixels** is to copy color values, depth values, or stencil values.</span></span> <span data-ttu-id="b8b77-120">Les constantes symboliques acceptées sont.</span><span class="sxs-lookup"><span data-stu-id="b8b77-120">The acceptable symbolic constants are.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b8b77-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="b8b77-121">Value</span></span></th>
<th><span data-ttu-id="b8b77-122">Signification</span><span class="sxs-lookup"><span data-stu-id="b8b77-122">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="GL_COLOR"></span><span id="gl_color"></span><dl> <span data-ttu-id="b8b77-123"><dt><strong>GL_COLOR</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="b8b77-123"><dt><strong>GL_COLOR</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="b8b77-124">La fonction <strong>glCopyPixels</strong> lit les index ou les couleurs RVBA à partir de la mémoire tampon actuellement spécifiée comme mémoire tampon de la source de lecture (voir <a href="glreadbuffer.md"><strong>glReadBuffer</strong></a>).</span><span class="sxs-lookup"><span data-stu-id="b8b77-124">The <strong>glCopyPixels</strong> function reads indexes or RGBA colors from the buffer currently specified as the read source buffer (see <a href="glreadbuffer.md"><strong>glReadBuffer</strong></a>).</span></span> <br/> <span data-ttu-id="b8b77-125">Si OpenGL est en mode d’index des couleurs :</span><span class="sxs-lookup"><span data-stu-id="b8b77-125">If OpenGL is in color-index mode:</span></span><br/>
<ol>
<li><span data-ttu-id="b8b77-126">Chaque index lu à partir de cette mémoire tampon est converti en un format à virgule fixe avec un nombre non spécifié de bits à droite du point binaire.</span><span class="sxs-lookup"><span data-stu-id="b8b77-126">Each index that is read from this buffer is converted to a fixed-point format with an unspecified number of bits to the right of the binary point.</span></span></li>
<li><span data-ttu-id="b8b77-127">Chaque index est décalé vers la gauche de GL_INDEX_SHIFT bits et ajouté à GL_INDEX_OFFSET. Si GL_INDEX_SHIFT est négatif, le décalage est à droite.</span><span class="sxs-lookup"><span data-stu-id="b8b77-127">Each index is shifted left by GL_INDEX_SHIFT bits, and added to GL_INDEX_OFFSET.If GL_INDEX_SHIFT is negative, the shift is to the right.</span></span> <span data-ttu-id="b8b77-128">Dans les deux cas, zéro bits remplit les emplacements de bits non spécifiés dans le résultat.</span><span class="sxs-lookup"><span data-stu-id="b8b77-128">In either case, zero bits fill otherwise unspecified bit locations in the result.</span></span><br/></li>
<li><span data-ttu-id="b8b77-129">Si GL_MAP_COLOR a la valeur true, l’index est remplacé par la valeur qu’il référence dans la GL_PIXEL_MAP_I_TO_I de la table de recherche.</span><span class="sxs-lookup"><span data-stu-id="b8b77-129">If GL_MAP_COLOR is true, the index is replaced with the value that it references in lookup table GL_PIXEL_MAP_I_TO_I.</span></span></li>
<li><span data-ttu-id="b8b77-130">Que le remplacement de la recherche de l’index soit effectué ou non, la partie entière de l’index est ensuite <strong>et</strong>Ed avec 2<em><sup>b</sup></em> 1, où <em>b</em> est le nombre de bits dans une mémoire tampon d’index de couleurs.</span><span class="sxs-lookup"><span data-stu-id="b8b77-130">Whether the lookup replacement of the index is done or not, the integer part of the index is then <strong>AND</strong>ed with 2<em><sup>b</sup></em> 1, where <em>b</em> is the number of bits in a color-index buffer.</span></span></li>
</ol>
<span data-ttu-id="b8b77-131">Si OpenGL est en mode RVBA :</span><span class="sxs-lookup"><span data-stu-id="b8b77-131">If OpenGL is in RGBA mode:</span></span><br/>
<ol>
<li><span data-ttu-id="b8b77-132">Les composants rouge, vert, bleu et alpha de chaque pixel lu sont convertis en un format à virgule flottante interne avec une précision non spécifiée.</span><span class="sxs-lookup"><span data-stu-id="b8b77-132">The red, green, blue, and alpha components of each pixel that is read are converted to an internal floating-point format with unspecified precision.</span></span></li>
<li><span data-ttu-id="b8b77-133">La conversion mappe la plus grande valeur de composant représentable à 1,0, et la valeur de composant zéro à 0,0.</span><span class="sxs-lookup"><span data-stu-id="b8b77-133">The conversion maps the largest representable component value to 1.0, and component value zero to 0.0.</span></span></li>
<li><span data-ttu-id="b8b77-134">Les valeurs de couleur à virgule flottante résultantes sont ensuite multipliées par GL_c_SCALE et ajoutées à GL_c_BIAS, où <em>c</em> est rouge, vert, bleu et alpha pour les composants de couleur respectifs.</span><span class="sxs-lookup"><span data-stu-id="b8b77-134">The resulting floating-point color values are then multiplied by GL_c_SCALE and added to GL_c_BIAS, where <em>c</em> is RED, GREEN, BLUE, and ALPHA for the respective color components.</span></span></li>
<li><span data-ttu-id="b8b77-135">Les résultats sont ancrés à la plage [0, 1].</span><span class="sxs-lookup"><span data-stu-id="b8b77-135">The results are clamped to the range [0,1].</span></span></li>
<li><span data-ttu-id="b8b77-136">Si GL_MAP_COLOR a la valeur true, chaque composant de couleur est mis à l’échelle en fonction de la taille de la table de recherche GL_PIXEL_MAP_c_TO_c, puis remplacé par la valeur qu’il référence dans cette table. <em>c</em> est R, G, B ou a, respectivement.</span><span class="sxs-lookup"><span data-stu-id="b8b77-136">If GL_MAP_COLOR is true, each color component is scaled by the size of lookup table GL_PIXEL_MAP_c_TO_c, and then replaced by the value that it references in that table; <em>c</em> is R, G, B, or A, respectively.</span></span> <span data-ttu-id="b8b77-137">Les index résultants ou les couleurs RVBA sont ensuite convertis en fragments en attachant la coordonnée <em>z</em>et les coordonnées de texture de la position raster actuelle à chaque pixel, puis en affectant les coordonnées de la fenêtre (<em>x</em><sub>r</sub> + i, <em>y</em><sub>r</sub> + <em>j</em>), où (<em>x</em><sub>r</sub> , <em>y</em><sub>r</sub> ) est la position <em>de la</em> trame actuelle, et le pixel était le pixel dans <em>la</em> ligne</span><span class="sxs-lookup"><span data-stu-id="b8b77-137">The resulting indexes or RGBA colors are then converted to fragments by attaching the current raster position <em>z</em>-coordinate and texture coordinates to each pixel, and then assigning window coordinates (<em>x</em><sub>r</sub> + i, <em>y</em><sub>r</sub> + <em>j</em>), where (<em>x</em><sub>r</sub> , <em>y</em><sub>r</sub> ) is the current raster position, and the pixel was the pixel in the <em>i</em> position in the <em>j</em> row.</span></span> <span data-ttu-id="b8b77-138">Ces fragments de pixels sont ensuite traités comme les fragments générés par la pixellisation des points, des lignes ou des polygones.</span><span class="sxs-lookup"><span data-stu-id="b8b77-138">These pixel fragments are then treated just like the fragments generated by rasterizing points, lines, or polygons.</span></span> <span data-ttu-id="b8b77-139">Le mappage de texture, le brouillard et toutes les opérations de fragment sont appliqués avant que les fragments soient écrits dans le trame.</span><span class="sxs-lookup"><span data-stu-id="b8b77-139">Texture mapping, fog, and all the fragment operations are applied before the fragments are written to the framebuffer.</span></span><br/></li>
</ol></td>
</tr>
<tr class="even">
<td><span id="GL_DEPTH"></span><span id="gl_depth"></span><dl> <span data-ttu-id="b8b77-140"><dt><strong>GL_DEPTH</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="b8b77-140"><dt><strong>GL_DEPTH</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="b8b77-141">Les valeurs de profondeur sont lues à partir de la mémoire tampon de profondeur et converties directement en un format à virgule flottante interne avec une précision non spécifiée.</span><span class="sxs-lookup"><span data-stu-id="b8b77-141">Depth values are read from the depth buffer and converted directly to an internal floating-point format with unspecified precision.</span></span> <span data-ttu-id="b8b77-142">La valeur de profondeur à virgule flottante résultante est ensuite multipliée par GL_DEPTH_SCALE et ajoutée à GL_DEPTH_BIAS.</span><span class="sxs-lookup"><span data-stu-id="b8b77-142">The resulting floating-point depth value is then multiplied by GL_DEPTH_SCALE and added to GL_DEPTH_BIAS.</span></span> <span data-ttu-id="b8b77-143">Le résultat est ancré à la plage [0, 1].</span><span class="sxs-lookup"><span data-stu-id="b8b77-143">The result is clamped to the range [0,1].</span></span> <br/> <span data-ttu-id="b8b77-144">Les composants de profondeur résultants sont ensuite convertis en fragments en joignant la couleur de la position raster actuelle ou l’index de couleur et les coordonnées de texture à chaque pixel, puis en affectant les coordonnées de la fenêtre (<em>x</em><sub>r</sub> + i, <em>y</em><sub>r</sub> + <em>j</em>), où (<em>x</em><sub>r</sub> , <em>y</em><sub>r</sub> ) est la position de la <em></em> trame actuelle, et le pixel dans la ligne <em>j</em> .</span><span class="sxs-lookup"><span data-stu-id="b8b77-144">The resulting depth components are then converted to fragments by attaching the current raster position color or color index and texture coordinates to each pixel, then assigning window coordinates (<em>x</em><sub>r</sub> + i, <em>y</em><sub>r</sub> + <em>j</em>), where (<em>x</em><sub>r</sub> , <em>y</em><sub>r</sub> ) is the current raster position, and the pixel was the pixel in the <em>i</em> position in the <em>j</em> row.</span></span> <span data-ttu-id="b8b77-145">Ces fragments de pixels sont ensuite traités comme les fragments générés par la pixellisation des points, des lignes ou des polygones.</span><span class="sxs-lookup"><span data-stu-id="b8b77-145">These pixel fragments are then treated just like the fragments generated by rasterizing points, lines, or polygons.</span></span> <span data-ttu-id="b8b77-146">Le mappage de texture, le brouillard et toutes les opérations de fragment sont appliqués avant que les fragments soient écrits dans le trame.</span><span class="sxs-lookup"><span data-stu-id="b8b77-146">Texture mapping, fog, and all the fragment operations are applied before the fragments are written to the framebuffer.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="GL_STENCIL"></span><span id="gl_stencil"></span><dl> <span data-ttu-id="b8b77-147"><dt><strong>GL_STENCIL</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="b8b77-147"><dt><strong>GL_STENCIL</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="b8b77-148">Les index de stencil sont lus à partir de la mémoire tampon de stencil et convertis en un format à virgule fixe interne avec un nombre non spécifié de bits à droite du point binaire.</span><span class="sxs-lookup"><span data-stu-id="b8b77-148">Stencil indexes are read from the stencil buffer and converted to an internal fixed-point format with an unspecified number of bits to the right of the binary point.</span></span> <span data-ttu-id="b8b77-149">Chaque index à virgule fixe est ensuite déplacé vers la gauche par GL_INDEX_SHIFT bits et ajouté à GL_INDEX_OFFSET.</span><span class="sxs-lookup"><span data-stu-id="b8b77-149">Each fixed-point index is then shifted left by GL_INDEX_SHIFT bits, and added to GL_INDEX_OFFSET.</span></span> <span data-ttu-id="b8b77-150">Si GL_INDEX_SHIFT est négatif, le décalage est à droite.</span><span class="sxs-lookup"><span data-stu-id="b8b77-150">If GL_INDEX_SHIFT is negative, the shift is to the right.</span></span> <span data-ttu-id="b8b77-151">Dans les deux cas, zéro bits remplit les emplacements de bits non spécifiés dans le résultat.</span><span class="sxs-lookup"><span data-stu-id="b8b77-151">In either case, zero bits fill otherwise unspecified bit locations in the result.</span></span> <span data-ttu-id="b8b77-152">Si GL_MAP_STENCIL a la valeur true, l’index est remplacé par la valeur qu’il référence dans la GL_PIXEL_MAP_S_TO_S de la table de recherche.</span><span class="sxs-lookup"><span data-stu-id="b8b77-152">If GL_MAP_STENCIL is true, the index is replaced with the value that it references in lookup table GL_PIXEL_MAP_S_TO_S.</span></span> <span data-ttu-id="b8b77-153">Que le remplacement de la recherche de l’index soit effectué ou non, la partie entière de l’index est ensuite <strong>et</strong>Ed avec 2<sup>b</sup> - 1, où <em>b</em> est le nombre de bits dans la mémoire tampon du stencil.</span><span class="sxs-lookup"><span data-stu-id="b8b77-153">Whether the lookup replacement of the index is done or not, the integer part of the index is then <strong>AND</strong>ed with 2<sup>b</sup> - 1, where <em>b</em> is the number of bits in the stencil buffer.</span></span> <span data-ttu-id="b8b77-154">Les index de stencil qui en résultent sont ensuite écrits dans la mémoire tampon de stencil de telle sorte que l’index lu à partir de l’emplacement <em>i</em> de la ligne <em>j</em> soit écrit dans l’emplacement (<em>x</em><sub>r</sub> + <em>i</em>, <em>y</em><sub>r</sub> + <em>j</em>), où (<em>x</em><sub>r</sub> , <em>y</em><sub>r</sub> ) est la position raster actuelle.</span><span class="sxs-lookup"><span data-stu-id="b8b77-154">The resulting stencil indexes are then written to the stencil buffer such that the index read from the <em>i</em> location of the <em>j</em> row is written to location (<em>x</em><sub>r</sub> + <em>i</em>, <em>y</em><sub>r</sub> + <em>j</em>), where (<em>x</em><sub>r</sub> , <em>y</em><sub>r</sub> ) is the current raster position.</span></span> <span data-ttu-id="b8b77-155">Seul le test de propriété en pixels, le test de ciseaux et le stencil writemask affectent ces écritures.</span><span class="sxs-lookup"><span data-stu-id="b8b77-155">Only the pixel-ownership test, the scissor test, and the stencil writemask affect these writes.</span></span><br/></td>
</tr>
</tbody>
</table>



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b8b77-156">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="b8b77-156">Return value</span></span>

<span data-ttu-id="b8b77-157">Cette fonction ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="b8b77-157">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="b8b77-158">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="b8b77-158">Error codes</span></span>

<span data-ttu-id="b8b77-159">Les codes d’erreur suivants peuvent être récupérés par la fonction [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="b8b77-159">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="b8b77-160">Nom</span><span class="sxs-lookup"><span data-stu-id="b8b77-160">Name</span></span>                                                                                                  | <span data-ttu-id="b8b77-161">Signification</span><span class="sxs-lookup"><span data-stu-id="b8b77-161">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="b8b77-162"><dt>**\_enum GL non valide \_**</dt></span><span class="sxs-lookup"><span data-stu-id="b8b77-162"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="b8b77-163">le *type* n’est pas une valeur acceptée.</span><span class="sxs-lookup"><span data-stu-id="b8b77-163">*type* was not an accepted value.</span></span><br/>                                                                                          |
| <dl> <span data-ttu-id="b8b77-164"><dt>**\_valeur non valide du GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="b8b77-164"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="b8b77-165">La *largeur* ou la hauteur était négative.</span><span class="sxs-lookup"><span data-stu-id="b8b77-165">Either *width* or height was negative.</span></span><br/>                                                                                     |
| <dl> <span data-ttu-id="b8b77-166"><dt>**\_opération non valide du GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="b8b77-166"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="b8b77-167">le *type* était \_ profondeur GL et il n’existait pas de mémoire tampon de profondeur.</span><span class="sxs-lookup"><span data-stu-id="b8b77-167">*type* was GL\_DEPTH and there was no depth buffer.</span></span><br/>                                                                        |
| <dl> <span data-ttu-id="b8b77-168"><dt>**\_opération non valide du GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="b8b77-168"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="b8b77-169">le *type* était \_ stencil GL et il n’existait pas de tampon de stencil.</span><span class="sxs-lookup"><span data-stu-id="b8b77-169">*type* was GL\_STENCIL and there was no stencil buffer.</span></span><br/>                                                                    |
| <dl> <span data-ttu-id="b8b77-170"><dt>**\_opération non valide du GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="b8b77-170"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="b8b77-171">La fonction a été appelée entre un appel à [**glBegin**](glbegin.md) et l’appel correspondant à [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="b8b77-171">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="b8b77-172">Notes</span><span class="sxs-lookup"><span data-stu-id="b8b77-172">Remarks</span></span>

<span data-ttu-id="b8b77-173">La fonction **glCopyPixels** copie un rectangle de pixels aligné à l’écran, de l’emplacement trame spécifié vers une région relative à la position raster actuelle.</span><span class="sxs-lookup"><span data-stu-id="b8b77-173">The **glCopyPixels** function copies a screen-aligned rectangle of pixels from the specified framebuffer location to a region relative to the current raster position.</span></span> <span data-ttu-id="b8b77-174">Son fonctionnement est bien défini uniquement si la région source de pixel entière se trouve dans la partie exposée de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="b8b77-174">Its operation is well defined only if the entire pixel source region is within the exposed portion of the window.</span></span> <span data-ttu-id="b8b77-175">Les résultats des copies en dehors de la fenêtre, ou à partir des régions de la fenêtre qui ne sont pas exposées, sont dépendants du matériel et non définis.</span><span class="sxs-lookup"><span data-stu-id="b8b77-175">Results of copies from outside the window, or from regions of the window that are not exposed, are hardware dependent and undefined.</span></span>

<span data-ttu-id="b8b77-176">Les paramètres *x* et *y* spécifient les coordonnées de la fenêtre du coin inférieur gauche de la zone rectangulaire à copier.</span><span class="sxs-lookup"><span data-stu-id="b8b77-176">The *x* and *y* parameters specify the window coordinates of the lower-left corner of the rectangular region to be copied.</span></span> <span data-ttu-id="b8b77-177">Les paramètres de *largeur* et de *hauteur* spécifient les dimensions de la zone rectangulaire à copier.</span><span class="sxs-lookup"><span data-stu-id="b8b77-177">The *width* and *height* parameters specify the dimensions of the rectangular region to be copied.</span></span> <span data-ttu-id="b8b77-178">La *largeur* et la *hauteur* ne doivent pas être négatives.</span><span class="sxs-lookup"><span data-stu-id="b8b77-178">Both *width* and *height* must be nonnegative.</span></span>

<span data-ttu-id="b8b77-179">Plusieurs paramètres contrôlent le traitement des données de pixels pendant qu’elles sont copiées.</span><span class="sxs-lookup"><span data-stu-id="b8b77-179">Several parameters control the processing of the pixel data while it is being copied.</span></span> <span data-ttu-id="b8b77-180">Ces paramètres sont définis avec trois fonctions : [**glPixelTransfer**](glpixeltransfer.md), [**glPixelMap**](glpixelmap.md)et [**glPixelZoom**](glpixelzoom.md).</span><span class="sxs-lookup"><span data-stu-id="b8b77-180">These parameters are set with three functions: [**glPixelTransfer**](glpixeltransfer.md), [**glPixelMap**](glpixelmap.md), and [**glPixelZoom**](glpixelzoom.md).</span></span> <span data-ttu-id="b8b77-181">Cette rubrique décrit les effets sur les **glCopyPixels** de la plupart des paramètres spécifiés par ces trois fonctions, mais pas tous.</span><span class="sxs-lookup"><span data-stu-id="b8b77-181">This topic describes the effects on **glCopyPixels** of most, but not all, of the parameters specified by these three functions.</span></span>

<span data-ttu-id="b8b77-182">La fonction **glCopyPixels** copie les valeurs de chaque pixel avec l’angle inférieur gauche à (*x*  +  *i*, *y*  +  *j*) pour 0 = *i*  <  *largeur* et 0 =   <  *hauteur* j.</span><span class="sxs-lookup"><span data-stu-id="b8b77-182">The **glCopyPixels** function copies values from each pixel with the lower-left corner at (*x* + *i*, *y* + *j*) for 0 = *i* < *width* and 0 = *j* < *height*.</span></span> <span data-ttu-id="b8b77-183">Ce pixel est considéré comme le pixel *i* de la ligne *j* .</span><span class="sxs-lookup"><span data-stu-id="b8b77-183">This pixel is said to be the *i* pixel in the *j* row.</span></span> <span data-ttu-id="b8b77-184">Les pixels sont copiés dans l’ordre des lignes de la plus petite à la ligne la plus élevée, de gauche à droite dans chaque ligne.</span><span class="sxs-lookup"><span data-stu-id="b8b77-184">Pixels are copied in row order from the lowest to the highest row, left to right in each row.</span></span>

<span data-ttu-id="b8b77-185">Le paramètre de *type* spécifie si les données de couleur, de profondeur ou de gabarit doivent être copiées.</span><span class="sxs-lookup"><span data-stu-id="b8b77-185">The *type* parameter specifies whether color, depth, or stencil data is to be copied.</span></span>

<span data-ttu-id="b8b77-186">La pixellisation décrite jusqu’à présent suppose des facteurs de zoom de pixel de 1,0.</span><span class="sxs-lookup"><span data-stu-id="b8b77-186">The rasterization described thus far assumes pixel zoom factors of 1.0.</span></span> <span data-ttu-id="b8b77-187">Si vous utilisez [**glPixelZoom**](glpixelzoom.md) pour modifier les facteurs de zoom de pixel *x* et *y* , les pixels sont convertis en fragments comme suit.</span><span class="sxs-lookup"><span data-stu-id="b8b77-187">If you use [**glPixelZoom**](glpixelzoom.md) to change the *x* and *y* pixel zoom factors, pixels are converted to fragments as follows.</span></span> <span data-ttu-id="b8b77-188">Si (*x*<sub>r</sub> , *y*<sub>r</sub> ) est la position raster actuelle et qu’un pixel donné se trouve à l’emplacement *i* sur la ligne *j* du rectangle de pixel source, des fragments sont générés pour les pixels dont les centres se trouvent dans le rectangle avec des angles à</span><span class="sxs-lookup"><span data-stu-id="b8b77-188">If (*x*<sub>r</sub> , *y*<sub>r</sub> ) is the current raster position, and a given pixel is in the *i* location in the *j* row of the source pixel rectangle, then fragments are generated for pixels whose centers are in the rectangle with corners at</span></span>

<span data-ttu-id="b8b77-189">(*x*<sub>r</sub>  +  *Zoom*? i, o <sub></sub>  +  *Zoom* r <sub>y</sub> *j*)</span><span class="sxs-lookup"><span data-stu-id="b8b77-189">(*x*<sub>r</sub> + *zoom*? i, y <sub>r</sub> + *zoom*<sub>y</sub> *j*)</span></span>

<span data-ttu-id="b8b77-190">et</span><span class="sxs-lookup"><span data-stu-id="b8b77-190">and</span></span>

<span data-ttu-id="b8b77-191">(*x*<sub>r</sub>  +  *Zoom*?</span><span class="sxs-lookup"><span data-stu-id="b8b77-191">(*x*<sub>r</sub> + *zoom*?</span></span> <span data-ttu-id="b8b77-192">(*i* + 1), *o*<sub>r</sub>  +  *Zoom*<sub>y</sub> (*j* + 1))</span><span class="sxs-lookup"><span data-stu-id="b8b77-192">(*i* + 1), *y*<sub>r</sub> + *zoom*<sub>y</sub> (*j* + 1))</span></span>

<span data-ttu-id="b8b77-193">où *Zoom*? est la valeur de zoom \_ GL \_ X et *Zoom*<sub>y</sub> est la valeur de \_ Zoom GL \_ y.</span><span class="sxs-lookup"><span data-stu-id="b8b77-193">where *zoom*? is the value of GL\_ZOOM\_X and *zoom*<sub>y</sub> is the value of GL\_ZOOM\_Y.</span></span>

<span data-ttu-id="b8b77-194">Les modes spécifiés par [**glPixelStore**](glpixelstore-functions.md) n’ont aucun effet sur l’opération de **glCopyPixels**.</span><span class="sxs-lookup"><span data-stu-id="b8b77-194">Modes specified by [**glPixelStore**](glpixelstore-functions.md) have no effect on the operation of **glCopyPixels**.</span></span>

<span data-ttu-id="b8b77-195">Les fonctions suivantes récupèrent les informations relatives à **glCopyPixels**:</span><span class="sxs-lookup"><span data-stu-id="b8b77-195">The following functions retrieve information related to **glCopyPixels**:</span></span>

<span data-ttu-id="b8b77-196">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) avec argument GL \_ Current \_ Raster \_ position</span><span class="sxs-lookup"><span data-stu-id="b8b77-196">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_CURRENT\_RASTER\_POSITION</span></span>

<span data-ttu-id="b8b77-197">**glGet** avec argument GL \_ Current \_ Raster \_ position \_ valide</span><span class="sxs-lookup"><span data-stu-id="b8b77-197">**glGet** with argument GL\_CURRENT\_RASTER\_POSITION\_VALID</span></span>

<span data-ttu-id="b8b77-198">Pour copier le pixel de couleur dans l’angle inférieur gauche de la fenêtre à la position de pixellisation actuelle, utilisez</span><span class="sxs-lookup"><span data-stu-id="b8b77-198">To copy the color pixel in the lower-left corner of the window to the current raster position, use</span></span>

<span data-ttu-id="b8b77-199">**glCopyPixels**(0, 0, 1, 1, \_ couleur GL);</span><span class="sxs-lookup"><span data-stu-id="b8b77-199">**glCopyPixels**( 0, 0, 1, 1, GL\_COLOR );</span></span>

## <a name="requirements"></a><span data-ttu-id="b8b77-200">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b8b77-200">Requirements</span></span>



| <span data-ttu-id="b8b77-201">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b8b77-201">Requirement</span></span> | <span data-ttu-id="b8b77-202">Valeur</span><span class="sxs-lookup"><span data-stu-id="b8b77-202">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b8b77-203">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b8b77-203">Minimum supported client</span></span><br/> | <span data-ttu-id="b8b77-204">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b8b77-204">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="b8b77-205">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b8b77-205">Minimum supported server</span></span><br/> | <span data-ttu-id="b8b77-206">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b8b77-206">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="b8b77-207">En-tête</span><span class="sxs-lookup"><span data-stu-id="b8b77-207">Header</span></span><br/>                   | <dl> <span data-ttu-id="b8b77-208"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="b8b77-208"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="b8b77-209">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="b8b77-209">Library</span></span><br/>                  | <dl> <span data-ttu-id="b8b77-210"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b8b77-210"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="b8b77-211">DLL</span><span class="sxs-lookup"><span data-stu-id="b8b77-211">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b8b77-212"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b8b77-212"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b8b77-213">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b8b77-213">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b8b77-214">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="b8b77-214">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="b8b77-215">**glDepthFunc**</span><span class="sxs-lookup"><span data-stu-id="b8b77-215">**glDepthFunc**</span></span>](gldepthfunc.md)
</dt> <dt>

[<span data-ttu-id="b8b77-216">**glDrawBuffer**</span><span class="sxs-lookup"><span data-stu-id="b8b77-216">**glDrawBuffer**</span></span>](gldrawbuffer.md)
</dt> <dt>

[<span data-ttu-id="b8b77-217">**glDrawPixels**</span><span class="sxs-lookup"><span data-stu-id="b8b77-217">**glDrawPixels**</span></span>](gldrawpixels.md)
</dt> <dt>

[<span data-ttu-id="b8b77-218">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="b8b77-218">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="b8b77-219">**glGet**</span><span class="sxs-lookup"><span data-stu-id="b8b77-219">**glGet**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[<span data-ttu-id="b8b77-220">**glPixelMap**</span><span class="sxs-lookup"><span data-stu-id="b8b77-220">**glPixelMap**</span></span>](glpixelmap.md)
</dt> <dt>

[<span data-ttu-id="b8b77-221">**glPixelStore**</span><span class="sxs-lookup"><span data-stu-id="b8b77-221">**glPixelStore**</span></span>](glpixelstore-functions.md)
</dt> <dt>

[<span data-ttu-id="b8b77-222">**glPixelTransfer**</span><span class="sxs-lookup"><span data-stu-id="b8b77-222">**glPixelTransfer**</span></span>](glpixeltransfer.md)
</dt> <dt>

[<span data-ttu-id="b8b77-223">**glPixelZoom**</span><span class="sxs-lookup"><span data-stu-id="b8b77-223">**glPixelZoom**</span></span>](glpixelzoom.md)
</dt> <dt>

[<span data-ttu-id="b8b77-224">**glRasterPos**</span><span class="sxs-lookup"><span data-stu-id="b8b77-224">**glRasterPos**</span></span>](glrasterpos-functions.md)
</dt> <dt>

[<span data-ttu-id="b8b77-225">**glReadBuffer**</span><span class="sxs-lookup"><span data-stu-id="b8b77-225">**glReadBuffer**</span></span>](glreadbuffer.md)
</dt> <dt>

[<span data-ttu-id="b8b77-226">**glReadPixels**</span><span class="sxs-lookup"><span data-stu-id="b8b77-226">**glReadPixels**</span></span>](glreadpixels.md)
</dt> <dt>

[<span data-ttu-id="b8b77-227">**glStencilFunc**</span><span class="sxs-lookup"><span data-stu-id="b8b77-227">**glStencilFunc**</span></span>](glstencilfunc.md)
</dt> </dl>

 

 





