---
title: fonction glGetColorTableEXT (GL. h)
description: La fonction glGetColorTableEXT obtient les données de la table des couleurs de la palette de texture ciblée actuelle.
ms.assetid: 9169c4e1-a22e-48fe-bd45-4549c1a10ff0
keywords:
- glGetColorTableEXT fonction OpenGL
topic_type:
- apiref
api_name:
- glGetColorTableEXT
api_location:
- Gl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 811dc53b32c937970fbef8d87fa9a2ef4eb8b978
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106533576"
---
# <a name="glgetcolortableext-function"></a><span data-ttu-id="125a4-104">glGetColorTableEXT fonction)</span><span class="sxs-lookup"><span data-stu-id="125a4-104">glGetColorTableEXT function</span></span>

<span data-ttu-id="125a4-105">La fonction **glGetColorTableEXT** obtient les données de la table des couleurs de la palette de texture ciblée actuelle.</span><span class="sxs-lookup"><span data-stu-id="125a4-105">The **glGetColorTableEXT** function gets the color table data of the current targeted texture palette.</span></span>

## <a name="syntax"></a><span data-ttu-id="125a4-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="125a4-106">Syntax</span></span>


```C++
void WINAPI glGetColorTableEXT(
         GLenum target,
         GLenum format,
         GLenum type,
   const GLvoid *data
);
```



## <a name="parameters"></a><span data-ttu-id="125a4-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="125a4-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="125a4-108">*cible*</span><span class="sxs-lookup"><span data-stu-id="125a4-108">*target*</span></span> 
</dt> <dd>

<span data-ttu-id="125a4-109">Texture cible dont la palette doit être modifiée.</span><span class="sxs-lookup"><span data-stu-id="125a4-109">The target texture that is to have its palette changed.</span></span> <span data-ttu-id="125a4-110">Doit être une TEXTURE \_ 1D ou une texture \_ 2D.</span><span class="sxs-lookup"><span data-stu-id="125a4-110">Must be TEXTURE\_1D or TEXTURE\_2D.</span></span>

</dd> <dt>

<span data-ttu-id="125a4-111">*format*</span><span class="sxs-lookup"><span data-stu-id="125a4-111">*format*</span></span> 
</dt> <dd>

<span data-ttu-id="125a4-112">Format des données de pixels.</span><span class="sxs-lookup"><span data-stu-id="125a4-112">The format of the pixel data.</span></span> <span data-ttu-id="125a4-113">Les constantes symboliques suivantes sont acceptées.</span><span class="sxs-lookup"><span data-stu-id="125a4-113">The following symbolic constants are accepted.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="125a4-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="125a4-114">Value</span></span></th>
<th><span data-ttu-id="125a4-115">Signification</span><span class="sxs-lookup"><span data-stu-id="125a4-115">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="GL_RGBA"></span><span id="gl_rgba"></span><dl> <span data-ttu-id="125a4-116"><dt><strong>GL_RGBA</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="125a4-116"><dt><strong>GL_RGBA</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="125a4-117">Chaque pixel est un groupe de quatre composants dans l’ordre suivant : rouge, vert, bleu, alpha.</span><span class="sxs-lookup"><span data-stu-id="125a4-117">Each pixel is a group of four components in the following order: red, green, blue, alpha.</span></span> <span data-ttu-id="125a4-118">Le format RVBA est déterminé de la façon suivante :</span><span class="sxs-lookup"><span data-stu-id="125a4-118">The RGBA format is determined in this way:</span></span> <br/>
<ol>
<li><span data-ttu-id="125a4-119">La fonction <strong>glGetColorTableEXT</strong> convertit les valeurs à virgule flottante directement en un format interne avec une précision non spécifiée.</span><span class="sxs-lookup"><span data-stu-id="125a4-119">The <strong>glGetColorTableEXT</strong> function converts floating-point values directly to an internal format with unspecified precision.</span></span> <span data-ttu-id="125a4-120">Les valeurs entières signées sont mappées de façon linéaire au format interne de telle sorte que la valeur entière représentable la plus positive corresponde à 1,0, et la valeur entière représentable la plus négative correspond à-1,0.</span><span class="sxs-lookup"><span data-stu-id="125a4-120">Signed integer values are mapped linearly to the internal format such that the most positive representable integer value maps to 1.0, and the most negative representable integer value maps to -1.0.</span></span> <span data-ttu-id="125a4-121">Les données entières non signées sont mappées de la même façon : la plus grande valeur entière correspond à 1,0, et zéro est mappé à 0,0.</span><span class="sxs-lookup"><span data-stu-id="125a4-121">Unsigned integer data is mapped similarly: the largest integer value maps to 1.0, and zero maps to 0.0.</span></span></li>
<li><span data-ttu-id="125a4-122">La fonction <strong>glGetColorTableEXT</strong> multiplie les valeurs de couleur résultantes par GL_c_SCALE et les ajoute à GL_c_BIAS, où <em>c</em> est rouge, vert, bleu et alpha pour les composants de couleur respectifs.</span><span class="sxs-lookup"><span data-stu-id="125a4-122">The <strong>glGetColorTableEXT</strong> function multiplies the resulting color values by GL_c_SCALE and adds them to GL_c_BIAS, where <em>c</em> is RED, GREEN, BLUE, and ALPHA for the respective color components.</span></span> <span data-ttu-id="125a4-123">Les résultats sont ancrés à la plage [0, 1].</span><span class="sxs-lookup"><span data-stu-id="125a4-123">The results are clamped to the range [0,1].</span></span></li>
<li><span data-ttu-id="125a4-124">Si GL_MAP_COLOR a la <strong>valeur true</strong>, <strong>glGetColorTableEXT</strong> met à l’échelle chaque composant de couleur en fonction de la taille de la table de recherche GL_PIXEL_MAP_c_TO_c, puis remplace le composant par la valeur qu’il référence dans cette table. <em>c</em> est R, G, B ou a, respectivement.</span><span class="sxs-lookup"><span data-stu-id="125a4-124">If GL_MAP_COLOR is <strong>TRUE</strong>, <strong>glGetColorTableEXT</strong> scales each color component by the size of lookup table GL_PIXEL_MAP_c_TO_c, then replaces the component by the value that it references in that table; <em>c</em> is R, G, B, or A, respectively.</span></span></li>
<li><span data-ttu-id="125a4-125">La fonction <strong>glGetColorTableEXT</strong> convertit les couleurs RVBA obtenues en fragments en attachant la coordonnée z et la coordonnée de texture de la position raster actuelle à chaque pixel, puis en affectant les coordonnées de la fenêtre <em>x</em> et <em>y</em> au <em>n</em>ième fragment, par exemple <em>x</em>?</span><span class="sxs-lookup"><span data-stu-id="125a4-125">The <strong>glGetColorTableEXT</strong> function converts the resulting RGBA colors to fragments by attaching the current raster position z-coordinate and texture coordinates to each pixel, then assigning <em>x</em> and <em>y</em> window coordinates to the <em>n</em>th fragment, such that <em>x</em>?</span></span><span data-ttu-id="125a4-126"> = <em>x</em><sub>r</sub> + <em>n</em> mod <em>largeur</em></span><span class="sxs-lookup"><span data-stu-id="125a4-126"> = <em>x</em><sub>r</sub> + <em>n</em> mod <em>width</em></span></span><br/> <span data-ttu-id="125a4-127"><em>y</em>?</span><span class="sxs-lookup"><span data-stu-id="125a4-127"><em>y</em>?</span></span><span data-ttu-id="125a4-128"> = <em></em><sub>r</sub> + <em>n/largeur</em> o</span><span class="sxs-lookup"><span data-stu-id="125a4-128"> = <em>y</em><sub>r</sub> + <em>n/width</em></span></span><br/> <span data-ttu-id="125a4-129">où (<em>x</em><sub>r</sub> , <em>y</em><sub>r</sub> ) est la position de la trame actuelle.</span><span class="sxs-lookup"><span data-stu-id="125a4-129">where (<em>x</em><sub>r</sub> , <em>y</em><sub>r</sub> ) is the current raster position.</span></span><br/></li>
<li><span data-ttu-id="125a4-130">Ces fragments de pixels sont ensuite traités comme les fragments générés par la pixellisation des points, des lignes ou des polygones.</span><span class="sxs-lookup"><span data-stu-id="125a4-130">These pixel fragments are then treated just like the fragments generated by rasterizing points, lines, or polygons.</span></span> <span data-ttu-id="125a4-131">La fonction <strong>glGetColorTableEXT</strong> applique le mappage de texture, le brouillard et toutes les opérations de fragment avant d’écrire les fragments dans le trame.</span><span class="sxs-lookup"><span data-stu-id="125a4-131">The <strong>glGetColorTableEXT</strong> function applies texture mapping, fog, and all the fragment operations before writing the fragments to the framebuffer.</span></span></li>
</ol></td>
</tr>
<tr class="even">
<td><span id="GL_RED"></span><span id="gl_red"></span><dl> <span data-ttu-id="125a4-132"><dt><strong>GL_RED</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="125a4-132"><dt><strong>GL_RED</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="125a4-133">Chaque pixel est un composant rouge unique.</span><span class="sxs-lookup"><span data-stu-id="125a4-133">Each pixel is a single red component.</span></span><br/> <span data-ttu-id="125a4-134">La fonction <strong>glGetColorTableEXT</strong> convertit ce composant au format interne de la même façon que le composant rouge d’un pixel RVBA est, puis le convertit en pixel RVBA avec le vert et le bleu réglés sur 0,0 et alpha défini sur 1,0.</span><span class="sxs-lookup"><span data-stu-id="125a4-134">The <strong>glGetColorTableEXT</strong> function converts this component to the internal format in the same way that the red component of an RGBA pixel is, then converts it to an RGBA pixel with green and blue set to 0.0, and alpha set to 1.0.</span></span> <span data-ttu-id="125a4-135">Après cette conversion, le pixel est traité comme s’il avait été lu en tant que pixel RVBA.</span><span class="sxs-lookup"><span data-stu-id="125a4-135">After this conversion, the pixel is treated just as if it had been read as an RGBA pixel.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="GL_GREEN"></span><span id="gl_green"></span><dl> <span data-ttu-id="125a4-136"><dt><strong>GL_GREEN</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="125a4-136"><dt><strong>GL_GREEN</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="125a4-137">Chaque pixel est un composant vert unique.</span><span class="sxs-lookup"><span data-stu-id="125a4-137">Each pixel is a single green component.</span></span><br/> <span data-ttu-id="125a4-138">La fonction <strong>glGetColorTableEXT</strong> convertit ce composant au format interne de la même façon que le composant vert d’un pixel RVBA est, puis le convertit en pixel RVBA avec rouge et bleu défini sur 0,0, et alpha défini sur 1,0.</span><span class="sxs-lookup"><span data-stu-id="125a4-138">The <strong>glGetColorTableEXT</strong> function converts this component to the internal format in the same way that the green component of an RGBA pixel is, and then converts it to an RGBA pixel with red and blue set to 0.0, and alpha set to 1.0.</span></span> <span data-ttu-id="125a4-139">Après cette conversion, le pixel est traité comme s’il avait été lu en tant que pixel RVBA.</span><span class="sxs-lookup"><span data-stu-id="125a4-139">After this conversion, the pixel is treated just as if it had been read as an RGBA pixel.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="GL_BLUE"></span><span id="gl_blue"></span><dl> <span data-ttu-id="125a4-140"><dt><strong>GL_BLUE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="125a4-140"><dt><strong>GL_BLUE</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="125a4-141">Chaque pixel est un composant bleu unique.</span><span class="sxs-lookup"><span data-stu-id="125a4-141">Each pixel is a single blue component.</span></span><br/> <span data-ttu-id="125a4-142">La fonction <strong>glGetColorTableEXT</strong> convertit ce composant au format interne de la même façon que le composant bleu d’un pixel RVBA est, puis le convertit en pixel RVBA avec Red et Green défini sur 0,0, et alpha défini sur 1,0.</span><span class="sxs-lookup"><span data-stu-id="125a4-142">The <strong>glGetColorTableEXT</strong> function converts this component to the internal format in the same way that the blue component of an RGBA pixel is, and then converts it to an RGBA pixel with red and green set to 0.0, and alpha set to 1.0.</span></span> <span data-ttu-id="125a4-143">Après cette conversion, le pixel est traité comme s’il avait été lu en tant que pixel RVBA.</span><span class="sxs-lookup"><span data-stu-id="125a4-143">After this conversion, the pixel is treated just as if it had been read as an RGBA pixel.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="GL_ALPHA"></span><span id="gl_alpha"></span><dl> <span data-ttu-id="125a4-144"><dt><strong>GL_ALPHA</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="125a4-144"><dt><strong>GL_ALPHA</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="125a4-145">Chaque pixel est un composant alpha unique.</span><span class="sxs-lookup"><span data-stu-id="125a4-145">Each pixel is a single alpha component.</span></span><br/> <span data-ttu-id="125a4-146">La fonction <strong>glGetColorTableEXT</strong> convertit ce composant au format interne de la même façon que le composant alpha d’un pixel RVBA est, puis le convertit en un pixel RVBA avec rouge, vert et bleu défini sur 0,0.</span><span class="sxs-lookup"><span data-stu-id="125a4-146">The <strong>glGetColorTableEXT</strong> function converts this component to the internal format in the same way that the alpha component of an RGBA pixel is, and then converts it to an RGBA pixel with red, green, and blue set to 0.0.</span></span> <span data-ttu-id="125a4-147">Après cette conversion, le pixel est traité comme s’il avait été lu en tant que pixel RVBA.</span><span class="sxs-lookup"><span data-stu-id="125a4-147">After this conversion, the pixel is treated just as if it had been read as an RGBA pixel.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="GL_RGB"></span><span id="gl_rgb"></span><dl> <span data-ttu-id="125a4-148"><dt><strong>GL_RGB</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="125a4-148"><dt><strong>GL_RGB</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="125a4-149">Chaque pixel est un groupe de trois composants dans cet ordre : rouge, vert, bleu.</span><span class="sxs-lookup"><span data-stu-id="125a4-149">Each pixel is a group of three components in this order: red, green, blue.</span></span><br/> <span data-ttu-id="125a4-150">La fonction <strong>glGetColorTableEXT</strong> convertit chaque composant au format interne de la même façon que les composants rouge, vert et bleu d’un pixel RVBA.</span><span class="sxs-lookup"><span data-stu-id="125a4-150">The <strong>glGetColorTableEXT</strong> function converts each component to the internal format in the same way that the red, green, and blue components of an RGBA pixel are.</span></span> <span data-ttu-id="125a4-151">La triple couleur est convertie en un pixel RVBA avec alpha défini sur 1,0.</span><span class="sxs-lookup"><span data-stu-id="125a4-151">The color triple is converted to an RGBA pixel with alpha set to 1.0.</span></span> <span data-ttu-id="125a4-152">Après cette conversion, le pixel est traité comme s’il avait été lu en tant que pixel RVBA.</span><span class="sxs-lookup"><span data-stu-id="125a4-152">After this conversion, the pixel is treated just as if it had been read as an RGBA pixel.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="GL_BGR_EXT"></span><span id="gl_bgr_ext"></span><dl> <span data-ttu-id="125a4-153"><dt><strong>GL_BGR_EXT</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="125a4-153"><dt><strong>GL_BGR_EXT</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="125a4-154">Chaque pixel est un groupe de trois composants dans cet ordre : bleu, vert, rouge.</span><span class="sxs-lookup"><span data-stu-id="125a4-154">Each pixel is a group of three components in this order: blue, green, red.</span></span><br/> <span data-ttu-id="125a4-155">GL_BGR_EXT fournit un format qui correspond à la disposition mémoire des bitmaps indépendantes du périphérique (DIB) Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="125a4-155">GL_BGR_EXT provides a format that matches the memory layout of Microsoft Windows device-independent bitmaps (DIBs).</span></span> <span data-ttu-id="125a4-156">Ainsi, vos applications peuvent utiliser les mêmes données avec les appels de fonction Windows et les appels de fonction de pixel OpenGL.</span><span class="sxs-lookup"><span data-stu-id="125a4-156">Thus, your applications can use the same data with Windows function calls and OpenGL pixel function calls.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="GL_BGRA_EXT"></span><span id="gl_bgra_ext"></span><dl> <span data-ttu-id="125a4-157"><dt><strong>GL_BGRA_EXT</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="125a4-157"><dt><strong>GL_BGRA_EXT</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="125a4-158">Chaque pixel est un groupe de quatre composants dans l’ordre suivant : bleu, vert, rouge, alpha.</span><span class="sxs-lookup"><span data-stu-id="125a4-158">Each pixel is a group of four components in this order: blue, green, red, alpha.</span></span><br/> <span data-ttu-id="125a4-159">GL_BGRA_EXT fournit un format qui correspond à la disposition mémoire des bitmaps indépendants du périphérique Windows (DIB).</span><span class="sxs-lookup"><span data-stu-id="125a4-159">GL_BGRA_EXT provides a format that matches the memory layout of Windows device-independent bitmaps (DIBs).</span></span> <span data-ttu-id="125a4-160">Par conséquent, vos applications peuvent utiliser les mêmes données avec les appels de fonction Windows et les appels de fonction de pixel OpenGL.</span><span class="sxs-lookup"><span data-stu-id="125a4-160">Thus your applications can use the same data with Windows function calls and OpenGL pixel function calls.</span></span><br/></td>
</tr>
</tbody>
</table>



 

</dd> <dt>

<span data-ttu-id="125a4-161">*type*</span><span class="sxs-lookup"><span data-stu-id="125a4-161">*type*</span></span> 
</dt> <dd>

<span data-ttu-id="125a4-162">Type de données pour les *données*.</span><span class="sxs-lookup"><span data-stu-id="125a4-162">The data type for *data*.</span></span> <span data-ttu-id="125a4-163">Voici les constantes symboliques acceptées et leurs significations.</span><span class="sxs-lookup"><span data-stu-id="125a4-163">The following are the accepted symbolic constants and their meanings.</span></span>



| <span data-ttu-id="125a4-164">Valeur</span><span class="sxs-lookup"><span data-stu-id="125a4-164">Value</span></span>                                                                                                                                                                      | <span data-ttu-id="125a4-165">Signification</span><span class="sxs-lookup"><span data-stu-id="125a4-165">Meaning</span></span>                                          |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------|
| <span id="GL_UNSIGNED_BYTE"></span><span id="gl_unsigned_byte"></span><dl> <span data-ttu-id="125a4-166"><dt>**\_octet non signé GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="125a4-166"><dt>**GL\_UNSIGNED\_BYTE**</dt></span></span> </dl>    | <span data-ttu-id="125a4-167">Entier 8 bits non signé</span><span class="sxs-lookup"><span data-stu-id="125a4-167">Unsigned 8-bit integer</span></span><br/>                |
| <span id="GL_BYTE"></span><span id="gl_byte"></span><dl> <span data-ttu-id="125a4-168"><dt>**\_octet GL**</dt></span><span class="sxs-lookup"><span data-stu-id="125a4-168"><dt>**GL\_BYTE**</dt></span></span> </dl>                                | <span data-ttu-id="125a4-169">Entier 8 bits signé</span><span class="sxs-lookup"><span data-stu-id="125a4-169">Signed 8-bit integer</span></span><br/>                  |
| <span id="GL_UNSIGNED_SHORT"></span><span id="gl_unsigned_short"></span><dl> <span data-ttu-id="125a4-170"><dt>**NON signé dans le GL \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="125a4-170"><dt>**GL\_UNSIGNED\_SHORT**</dt></span></span> </dl> | <span data-ttu-id="125a4-171">Entier 16 bits non signé</span><span class="sxs-lookup"><span data-stu-id="125a4-171">Unsigned 16-bit integer</span></span><br/>               |
| <span id="GL_SHORT"></span><span id="gl_short"></span><dl> <span data-ttu-id="125a4-172"><dt>**\_abrégé GL**</dt></span><span class="sxs-lookup"><span data-stu-id="125a4-172"><dt>**GL\_SHORT**</dt></span></span> </dl>                             | <span data-ttu-id="125a4-173">Entier 16 bits signé</span><span class="sxs-lookup"><span data-stu-id="125a4-173">Signed 16-bit integer</span></span><br/>                 |
| <span id="GL_UNSIGNED_INT"></span><span id="gl_unsigned_int"></span><dl> <span data-ttu-id="125a4-174"><dt>**\_entier non signé GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="125a4-174"><dt>**GL\_UNSIGNED\_INT**</dt></span></span> </dl>       | <span data-ttu-id="125a4-175">Entier 32 bits non signé</span><span class="sxs-lookup"><span data-stu-id="125a4-175">Unsigned 32-bit integer</span></span><br/>               |
| <span id="GL_INT"></span><span id="gl_int"></span><dl> <span data-ttu-id="125a4-176"><dt>**GL \_ int**</dt></span><span class="sxs-lookup"><span data-stu-id="125a4-176"><dt>**GL\_INT**</dt></span></span> </dl>                                   | <span data-ttu-id="125a4-177">Entier de 32 bits</span><span class="sxs-lookup"><span data-stu-id="125a4-177">32-bit integer</span></span><br/>                        |
| <span id="GL_FLOAT"></span><span id="gl_float"></span><dl> <span data-ttu-id="125a4-178"><dt>**valeur \_ float du GL**</dt></span><span class="sxs-lookup"><span data-stu-id="125a4-178"><dt>**GL\_FLOAT**</dt></span></span> </dl>                             | <span data-ttu-id="125a4-179">Valeur à virgule flottante simple précision</span><span class="sxs-lookup"><span data-stu-id="125a4-179">Single-precision floating-point value</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="125a4-180">*data*</span><span class="sxs-lookup"><span data-stu-id="125a4-180">*data*</span></span> 
</dt> <dd>

<span data-ttu-id="125a4-181">Pointe vers l’emplacement où les informations de table des couleurs retournées doivent être stockées.</span><span class="sxs-lookup"><span data-stu-id="125a4-181">Points to the location where returned color table information is to be stored.</span></span> <span data-ttu-id="125a4-182">Chaque entrée de table des couleurs est stockée comme s’il s’agissait d’un pixel unique d’une texture 1D.</span><span class="sxs-lookup"><span data-stu-id="125a4-182">Each color table entry is stored as if it was a single pixel of a 1-D texture.</span></span> <span data-ttu-id="125a4-183">Étant donné que toutes les textures ont une palette par défaut, **glGetColorTableEXT** retourne toujours les informations de palette même si les données de texture ne sont pas dans un format de palette.</span><span class="sxs-lookup"><span data-stu-id="125a4-183">Because all textures have a default palette, **glGetColorTableEXT** always returns palette information even if the texture data is not in a paletted format.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="125a4-184">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="125a4-184">Return value</span></span>

<span data-ttu-id="125a4-185">Cette fonction ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="125a4-185">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="125a4-186">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="125a4-186">Error codes</span></span>

<span data-ttu-id="125a4-187">Les codes d’erreur suivants peuvent être récupérés par la fonction [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="125a4-187">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="125a4-188">Nom</span><span class="sxs-lookup"><span data-stu-id="125a4-188">Name</span></span>                                                                                                  | <span data-ttu-id="125a4-189">Signification</span><span class="sxs-lookup"><span data-stu-id="125a4-189">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="125a4-190"><dt>**\_enum GL non valide \_**</dt></span><span class="sxs-lookup"><span data-stu-id="125a4-190"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="125a4-191">la *cible*, le *format* ou le *type* n’était pas une valeur acceptée.</span><span class="sxs-lookup"><span data-stu-id="125a4-191">*target*, *format*, or *type* was not an accepted value.</span></span><br/>                                                                   |
| <dl> <span data-ttu-id="125a4-192"><dt>**\_opération non valide du GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="125a4-192"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="125a4-193">La fonction a été appelée entre un appel à [**glBegin**](glbegin.md) et l’appel correspondant à [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="125a4-193">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="125a4-194">Notes</span><span class="sxs-lookup"><span data-stu-id="125a4-194">Remarks</span></span>

<span data-ttu-id="125a4-195">La fonction **glGetColorTableEXT** obtient les données de la table des couleurs réelles spécifiées par [**glColorTableEXT**](glcolortableext.md) et [**glColorSubTableEXT**](glcolorsubtableext.md).</span><span class="sxs-lookup"><span data-stu-id="125a4-195">The **glGetColorTableEXT** function gets the actual color table data specified by [**glColorTableEXT**](glcolortableext.md) and [**glColorSubTableEXT**](glcolorsubtableext.md).</span></span>

<span data-ttu-id="125a4-196">La fonction **glGetColorTableEXT** est une fonction d’extension qui ne fait pas partie de la bibliothèque OpenGL standard, mais qui fait partie de l' \_ extension de texture de palette ext GL \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="125a4-196">The **glGetColorTableEXT** function is an extension function that is not part of the standard OpenGL library but is part of the GL\_EXT\_paletted\_texture extension.</span></span> <span data-ttu-id="125a4-197">Pour vérifier si votre implémentation d’OpenGL prend en charge **glGetColorTableEXT**, appelez [**glGetString**](glgetstring.md)( \_ Extensions GL).</span><span class="sxs-lookup"><span data-stu-id="125a4-197">To check whether your implementation of OpenGL supports **glGetColorTableEXT**, call [**glGetString**](glgetstring.md)(GL\_EXTENSIONS).</span></span> <span data-ttu-id="125a4-198">Si elle retourne la \_ \_ texture de palette ext GL \_ , **glGetColorTableEXT** est pris en charge.</span><span class="sxs-lookup"><span data-stu-id="125a4-198">If it returns GL\_EXT\_paletted\_texture, **glGetColorTableEXT** is supported.</span></span> <span data-ttu-id="125a4-199">Pour obtenir l’adresse de fonction d’une fonction d’extension, appelez [**wglGetProcAddress**](/windows/desktop/api/wingdi/nf-wingdi-wglgetprocaddress).</span><span class="sxs-lookup"><span data-stu-id="125a4-199">To obtain the function address of an extension function, call [**wglGetProcAddress**](/windows/desktop/api/wingdi/nf-wingdi-wglgetprocaddress).</span></span>

## <a name="requirements"></a><span data-ttu-id="125a4-200">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="125a4-200">Requirements</span></span>



| <span data-ttu-id="125a4-201">Condition requise</span><span class="sxs-lookup"><span data-stu-id="125a4-201">Requirement</span></span> | <span data-ttu-id="125a4-202">Valeur</span><span class="sxs-lookup"><span data-stu-id="125a4-202">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="125a4-203">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="125a4-203">Minimum supported client</span></span><br/> | <span data-ttu-id="125a4-204">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="125a4-204">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                      |
| <span data-ttu-id="125a4-205">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="125a4-205">Minimum supported server</span></span><br/> | <span data-ttu-id="125a4-206">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="125a4-206">Windows 2000 Server \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="125a4-207">En-tête</span><span class="sxs-lookup"><span data-stu-id="125a4-207">Header</span></span><br/>                   | <dl> <span data-ttu-id="125a4-208"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="125a4-208"><dt>Gl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="125a4-209">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="125a4-209">See also</span></span>

<dl> <dt>

[<span data-ttu-id="125a4-210">**glColorSubTableEXT**</span><span class="sxs-lookup"><span data-stu-id="125a4-210">**glColorSubTableEXT**</span></span>](glcolorsubtableext.md)
</dt> <dt>

[<span data-ttu-id="125a4-211">**glColorTableEXT**</span><span class="sxs-lookup"><span data-stu-id="125a4-211">**glColorTableEXT**</span></span>](glcolortableext.md)
</dt> <dt>

[<span data-ttu-id="125a4-212">**glGetColorTableParameterfvEXT**</span><span class="sxs-lookup"><span data-stu-id="125a4-212">**glGetColorTableParameterfvEXT**</span></span>](glgetcolortableparameterfvext.md)
</dt> <dt>

[<span data-ttu-id="125a4-213">**glGetColorTableParameterivEXT**</span><span class="sxs-lookup"><span data-stu-id="125a4-213">**glGetColorTableParameterivEXT**</span></span>](glgetcolortableparameterivext.md)
</dt> <dt>

[<span data-ttu-id="125a4-214">**wglGetProcAddress**</span><span class="sxs-lookup"><span data-stu-id="125a4-214">**wglGetProcAddress**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-wglgetprocaddress)
</dt> </dl>

 

 





