---
title: fonction glColorSubTableEXT (GL. h)
description: La fonction glColorSubTableEXT spécifie une partie de la palette de la texture ciblée à remplacer.
ms.assetid: 21430245-f837-4c7a-944f-b44482254b12
keywords:
- glColorSubTableEXT fonction OpenGL
topic_type:
- apiref
api_name:
- glColorSubTableEXT
api_location:
- Gl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2a0386bda82bf08ae778d20b1be69858698ac7bb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843746"
---
# <a name="glcolorsubtableext-function"></a><span data-ttu-id="8684b-104">glColorSubTableEXT fonction)</span><span class="sxs-lookup"><span data-stu-id="8684b-104">glColorSubTableEXT function</span></span>

<span data-ttu-id="8684b-105">La fonction **glColorSubTableEXT** spécifie une partie de la palette de la texture ciblée à remplacer.</span><span class="sxs-lookup"><span data-stu-id="8684b-105">The **glColorSubTableEXT** function specifies a portion of the targeted texture's palette to be replaced.</span></span>

## <a name="syntax"></a><span data-ttu-id="8684b-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8684b-106">Syntax</span></span>


```C++
void WINAPI glColorSubTableEXT(
         GLenum  target,
         GLsizei start,
         GLsizei count,
         GLenum  format,
         GLenum  type,
   const GLvoid  *data
);
```



## <a name="parameters"></a><span data-ttu-id="8684b-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8684b-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8684b-108">*cible*</span><span class="sxs-lookup"><span data-stu-id="8684b-108">*target*</span></span> 
</dt> <dd>

<span data-ttu-id="8684b-109">Texture de palette cible dont la palette doit être modifiée.</span><span class="sxs-lookup"><span data-stu-id="8684b-109">The target paletted texture that is to have its palette changed.</span></span> <span data-ttu-id="8684b-110">Doit être une TEXTURE \_ 1D ou une texture \_ 2D.</span><span class="sxs-lookup"><span data-stu-id="8684b-110">Must be TEXTURE\_1D or TEXTURE\_2D.</span></span>

</dd> <dt>

<span data-ttu-id="8684b-111">*start*</span><span class="sxs-lookup"><span data-stu-id="8684b-111">*start*</span></span> 
</dt> <dd>

<span data-ttu-id="8684b-112">Entrée d’index de la palette de départ de la palette à modifier.</span><span class="sxs-lookup"><span data-stu-id="8684b-112">The starting palette index entry of the palette to be changed.</span></span>

</dd> <dt>

<span data-ttu-id="8684b-113">*count*</span><span class="sxs-lookup"><span data-stu-id="8684b-113">*count*</span></span> 
</dt> <dd>

<span data-ttu-id="8684b-114">Nombre d’entrées d’index de palette de la palette à modifier à partir du *début*.</span><span class="sxs-lookup"><span data-stu-id="8684b-114">The number of palette index entries of the palette to be changed beginning at *start*.</span></span> <span data-ttu-id="8684b-115">Le paramètre *Count* détermine la plage d’entrées d’index de palette qui sont modifiées.</span><span class="sxs-lookup"><span data-stu-id="8684b-115">The *count* parameter determines the range of palette index entries that are changed.</span></span>

</dd> <dt>

<span data-ttu-id="8684b-116">*format*</span><span class="sxs-lookup"><span data-stu-id="8684b-116">*format*</span></span> 
</dt> <dd>

<span data-ttu-id="8684b-117">Format des données de pixels.</span><span class="sxs-lookup"><span data-stu-id="8684b-117">The format of the pixel data.</span></span> <span data-ttu-id="8684b-118">Les constantes symboliques suivantes sont acceptées.</span><span class="sxs-lookup"><span data-stu-id="8684b-118">The following symbolic constants are accepted.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="8684b-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="8684b-119">Value</span></span></th>
<th><span data-ttu-id="8684b-120">Signification</span><span class="sxs-lookup"><span data-stu-id="8684b-120">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="GL_RGBA"></span><span id="gl_rgba"></span><dl> <span data-ttu-id="8684b-121"><dt><strong>GL_RGBA</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="8684b-121"><dt><strong>GL_RGBA</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="8684b-122">Chaque pixel est un groupe de quatre composants dans l’ordre suivant : rouge, vert, bleu, alpha.</span><span class="sxs-lookup"><span data-stu-id="8684b-122">Each pixel is a group of four components in the following order: red, green, blue, alpha.</span></span> <span data-ttu-id="8684b-123">Le format RVBA est déterminé de la façon suivante :</span><span class="sxs-lookup"><span data-stu-id="8684b-123">The RGBA format is determined in this way:</span></span> <br/>
<ol>
<li><span data-ttu-id="8684b-124">La fonction <strong>glColorSubTableEXT</strong> convertit les valeurs à virgule flottante directement en un format interne avec une précision non spécifiée.</span><span class="sxs-lookup"><span data-stu-id="8684b-124">The <strong>glColorSubTableEXT</strong> function converts floating-point values directly to an internal format with unspecified precision.</span></span> <span data-ttu-id="8684b-125">Les valeurs entières signées sont mappées de façon linéaire au format interne, de sorte que la valeur entière représentable la plus positive correspond à 1,0, et la valeur représentable la plus négative correspond à-1,0.</span><span class="sxs-lookup"><span data-stu-id="8684b-125">Signed integer values are mapped linearly to the internal format such that the most positive representable integer value maps to 1.0, and the most negative representable value maps to -1.0.</span></span> <span data-ttu-id="8684b-126">Les données entières non signées sont mappées de la même façon : la plus grande valeur entière correspond à 1,0, et zéro est mappé à 0,0.</span><span class="sxs-lookup"><span data-stu-id="8684b-126">Unsigned integer data is mapped similarly: the largest integer value maps to 1.0, and zero maps to 0.0.</span></span></li>
<li><span data-ttu-id="8684b-127">La fonction <strong>glColorSubTableEXT</strong> multiplie les valeurs de couleur résultantes par GL_c_SCALE et les ajoute à GL_c_BIAS, où <em>c</em> est rouge, vert, bleu et alpha pour les composants de couleur respectifs.</span><span class="sxs-lookup"><span data-stu-id="8684b-127">The <strong>glColorSubTableEXT</strong> function multiplies the resulting color values by GL_c_SCALE and adds them to GL_c_BIAS, where <em>c</em> is RED, GREEN, BLUE, and ALPHA for the respective color components.</span></span> <span data-ttu-id="8684b-128">Les résultats sont ancrés à la plage [0, 1].</span><span class="sxs-lookup"><span data-stu-id="8684b-128">The results are clamped to the range [0,1].</span></span></li>
<li><span data-ttu-id="8684b-129">Si GL_MAP_COLOR a la <strong>valeur true</strong>, <strong>glColorSubTableEXT</strong> met à l’échelle chaque composant de couleur en fonction de la taille de la table de recherche GL_PIXEL_MAP_c_TO_c, puis remplace le composant par la valeur qu’il référence dans cette table. <em>c</em> est R, G, B ou a, respectivement.</span><span class="sxs-lookup"><span data-stu-id="8684b-129">If GL_MAP_COLOR is <strong>TRUE</strong>, <strong>glColorSubTableEXT</strong> scales each color component by the size of lookup table GL_PIXEL_MAP_c_TO_c, then replaces the component by the value that it references in that table; <em>c</em> is R, G, B, or A, respectively.</span></span></li>
<li><span data-ttu-id="8684b-130">La fonction <strong>glColorSubTableEXT</strong> convertit les couleurs RVBA obtenues en fragments en attachant la coordonnée <em>z</em>et la coordonnée de texture de la position raster actuelle à chaque pixel, puis en affectant les coordonnées de la fenêtre <em>x</em> et <em>y</em> au <em>n</em>ième fragment, de telle sorte que<em>x</em>?</span><span class="sxs-lookup"><span data-stu-id="8684b-130">The <strong>glColorSubTableEXT</strong> function converts the resulting RGBA colors to fragments by attaching the current raster position <em>z</em>-coordinate and texture coordinates to each pixel, then assigning <em>x</em> and <em>y</em> window coordinates to the <em>n</em>th fragment such that<em>x</em>?</span></span><span data-ttu-id="8684b-131"> = <em>x</em><sub>r</sub> + <em>n</em> mod <em>largeur</em></span><span class="sxs-lookup"><span data-stu-id="8684b-131"> = <em>x</em><sub>r</sub> + <em>n</em> mod <em>width</em></span></span><br/> <span data-ttu-id="8684b-132"><em>y</em>?</span><span class="sxs-lookup"><span data-stu-id="8684b-132"><em>y</em>?</span></span><span data-ttu-id="8684b-133"> = <em></em><sub>r</sub> +<em>n/largeur</em> o</span><span class="sxs-lookup"><span data-stu-id="8684b-133"> = <em>y</em><sub>r</sub> +<em>n / width</em></span></span><br/> <span data-ttu-id="8684b-134">où (<em>x</em><sub>r</sub> , <em>y</em><sub>r</sub> ) est la position de la trame actuelle.</span><span class="sxs-lookup"><span data-stu-id="8684b-134">where (<em>x</em><sub>r</sub> , <em>y</em><sub>r</sub> ) is the current raster position.</span></span><br/></li>
<li><span data-ttu-id="8684b-135">Ces fragments de pixels sont ensuite traités comme les fragments générés par la pixellisation des points, des lignes ou des polygones.</span><span class="sxs-lookup"><span data-stu-id="8684b-135">These pixel fragments are then treated just like the fragments generated by rasterizing points, lines, or polygons.</span></span> <span data-ttu-id="8684b-136">La fonction <strong>glColorSubTableEXT</strong> applique le mappage de texture, le brouillard et toutes les opérations de fragment avant d’écrire les fragments dans le trame.</span><span class="sxs-lookup"><span data-stu-id="8684b-136">The <strong>glColorSubTableEXT</strong> function applies texture mapping, fog, and all the fragment operations before writing the fragments to the framebuffer.</span></span></li>
</ol></td>
</tr>
<tr class="even">
<td><span id="GL_RED"></span><span id="gl_red"></span><dl> <span data-ttu-id="8684b-137"><dt><strong>GL_RED</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="8684b-137"><dt><strong>GL_RED</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="8684b-138">Chaque pixel est un composant rouge unique.</span><span class="sxs-lookup"><span data-stu-id="8684b-138">Each pixel is a single red component.</span></span><br/> <span data-ttu-id="8684b-139">La fonction <strong>glColorSubTableEXT</strong> convertit ce composant au format interne de la même façon que le composant rouge d’un pixel RVBA est, puis le convertit en pixel RVBA avec le vert et le bleu réglés sur 0,0 et alpha défini sur 1,0.</span><span class="sxs-lookup"><span data-stu-id="8684b-139">The <strong>glColorSubTableEXT</strong> function converts this component to the internal format in the same way that the red component of an RGBA pixel is, then converts it to an RGBA pixel with green and blue set to 0.0, and alpha set to 1.0.</span></span> <span data-ttu-id="8684b-140">Après cette conversion, le pixel est traité comme s’il avait été lu en tant que pixel RVBA.</span><span class="sxs-lookup"><span data-stu-id="8684b-140">After this conversion, the pixel is treated just as if it had been read as an RGBA pixel.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="GL_GREEN"></span><span id="gl_green"></span><dl> <span data-ttu-id="8684b-141"><dt><strong>GL_GREEN</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="8684b-141"><dt><strong>GL_GREEN</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="8684b-142">Chaque pixel est un composant vert unique.</span><span class="sxs-lookup"><span data-stu-id="8684b-142">Each pixel is a single green component.</span></span><br/> <span data-ttu-id="8684b-143">La fonction <strong>glColorSubTableEXT</strong> convertit ce composant au format interne de la même façon que le composant vert d’un pixel RVBA est, puis le convertit en pixel RVBA avec rouge et bleu défini sur 0,0, et alpha défini sur 1,0.</span><span class="sxs-lookup"><span data-stu-id="8684b-143">The <strong>glColorSubTableEXT</strong> function converts this component to the internal format in the same way that the green component of an RGBA pixel is, and then converts it to an RGBA pixel with red and blue set to 0.0, and alpha set to 1.0.</span></span> <span data-ttu-id="8684b-144">Après cette conversion, le pixel est traité comme s’il avait été lu en tant que pixel RVBA.</span><span class="sxs-lookup"><span data-stu-id="8684b-144">After this conversion, the pixel is treated just as if it had been read as an RGBA pixel.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="GL_BLUE"></span><span id="gl_blue"></span><dl> <span data-ttu-id="8684b-145"><dt><strong>GL_BLUE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="8684b-145"><dt><strong>GL_BLUE</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="8684b-146">Chaque pixel est un composant bleu unique.</span><span class="sxs-lookup"><span data-stu-id="8684b-146">Each pixel is a single blue component.</span></span><br/> <span data-ttu-id="8684b-147">La fonction <strong>glColorSubTableEXT</strong> convertit ce composant au format interne de la même façon que le composant bleu d’un pixel RVBA est, puis le convertit en pixel RVBA avec Red et Green défini sur 0,0, et alpha défini sur 1,0.</span><span class="sxs-lookup"><span data-stu-id="8684b-147">The <strong>glColorSubTableEXT</strong> function converts this component to the internal format in the same way that the blue component of an RGBA pixel is, and then converts it to an RGBA pixel with red and green set to 0.0, and alpha set to 1.0.</span></span> <span data-ttu-id="8684b-148">Après cette conversion, le pixel est traité comme s’il avait été lu en tant que pixel RVBA.</span><span class="sxs-lookup"><span data-stu-id="8684b-148">After this conversion, the pixel is treated just as if it had been read as an RGBA pixel.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="GL_ALPHA"></span><span id="gl_alpha"></span><dl> <span data-ttu-id="8684b-149"><dt><strong>GL_ALPHA</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="8684b-149"><dt><strong>GL_ALPHA</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="8684b-150">Chaque pixel est un composant alpha unique.</span><span class="sxs-lookup"><span data-stu-id="8684b-150">Each pixel is a single alpha component.</span></span><br/> <span data-ttu-id="8684b-151">La fonction <strong>glColorSubTableEXT</strong> convertit ce composant au format interne de la même façon que le composant alpha d’un pixel RVBA est, puis le convertit en un pixel RVBA avec rouge, vert et bleu défini sur 0,0.</span><span class="sxs-lookup"><span data-stu-id="8684b-151">The <strong>glColorSubTableEXT</strong> function converts this component to the internal format in the same way that the alpha component of an RGBA pixel is, and then converts it to an RGBA pixel with red, green, and blue set to 0.0.</span></span> <span data-ttu-id="8684b-152">Après cette conversion, le pixel est traité comme s’il avait été lu en tant que pixel RVBA.</span><span class="sxs-lookup"><span data-stu-id="8684b-152">After this conversion, the pixel is treated just as if it had been read as an RGBA pixel.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="GL_RGB"></span><span id="gl_rgb"></span><dl> <span data-ttu-id="8684b-153"><dt><strong>GL_RGB</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="8684b-153"><dt><strong>GL_RGB</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="8684b-154">Chaque pixel est un groupe de trois composants dans cet ordre : rouge, vert, bleu.</span><span class="sxs-lookup"><span data-stu-id="8684b-154">Each pixel is a group of three components in this order: red, green, blue.</span></span><br/> <span data-ttu-id="8684b-155">La fonction <strong>glColorSubTableEXT</strong> convertit chaque composant au format interne de la même façon que les composants rouge, vert et bleu d’un pixel RVBA.</span><span class="sxs-lookup"><span data-stu-id="8684b-155">The <strong>glColorSubTableEXT</strong> function converts each component to the internal format in the same way that the red, green, and blue components of an RGBA pixel are.</span></span> <span data-ttu-id="8684b-156">La triple couleur est convertie en un pixel RVBA avec alpha défini sur 1,0.</span><span class="sxs-lookup"><span data-stu-id="8684b-156">The color triple is converted to an RGBA pixel with alpha set to 1.0.</span></span> <span data-ttu-id="8684b-157">Après cette conversion, le pixel est traité comme s’il avait été lu en tant que pixel RVBA.</span><span class="sxs-lookup"><span data-stu-id="8684b-157">After this conversion, the pixel is treated just as if it had been read as an RGBA pixel.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="GL_BGR_EXT"></span><span id="gl_bgr_ext"></span><dl> <span data-ttu-id="8684b-158"><dt><strong>GL_BGR_EXT</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="8684b-158"><dt><strong>GL_BGR_EXT</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="8684b-159">Chaque pixel est un groupe de trois composants dans cet ordre : bleu, vert, rouge.</span><span class="sxs-lookup"><span data-stu-id="8684b-159">Each pixel is a group of three components in this order: blue, green, red.</span></span><br/> <span data-ttu-id="8684b-160">GL_BGR_EXT fournit un format qui correspond à la disposition mémoire des bitmaps indépendants du périphérique Windows (DIB).</span><span class="sxs-lookup"><span data-stu-id="8684b-160">GL_BGR_EXT provides a format that matches the memory layout of Windows device-independent bitmaps (DIBs).</span></span> <span data-ttu-id="8684b-161">Par conséquent, vos applications peuvent utiliser les mêmes données avec les appels de fonction Windows et les appels de fonction de pixel OpenGL.</span><span class="sxs-lookup"><span data-stu-id="8684b-161">Thus your applications can use the same data with Windows function calls and OpenGL pixel function calls.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="GL_BGRA_EXT"></span><span id="gl_bgra_ext"></span><dl> <span data-ttu-id="8684b-162"><dt><strong>GL_BGRA_EXT</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="8684b-162"><dt><strong>GL_BGRA_EXT</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="8684b-163">Chaque pixel est un groupe de quatre composants dans l’ordre suivant : bleu, vert, rouge, alpha.</span><span class="sxs-lookup"><span data-stu-id="8684b-163">Each pixel is a group of four components in this order: blue, green, red, alpha.</span></span><br/> <span data-ttu-id="8684b-164">GL_BGRA_EXT fournit un format qui correspond à la disposition mémoire des bitmaps indépendants du périphérique Windows (DIB).</span><span class="sxs-lookup"><span data-stu-id="8684b-164">GL_BGRA_EXT provides a format that matches the memory layout of Windows device-independent bitmaps (DIBs).</span></span> <span data-ttu-id="8684b-165">Par conséquent, vos applications peuvent utiliser les mêmes données avec les appels de fonction Windows et les appels de fonction de pixel OpenGL.</span><span class="sxs-lookup"><span data-stu-id="8684b-165">Thus your applications can use the same data with Windows function calls and OpenGL pixel function calls.</span></span><br/></td>
</tr>
</tbody>
</table>



 

</dd> <dt>

<span data-ttu-id="8684b-166">*type*</span><span class="sxs-lookup"><span data-stu-id="8684b-166">*type*</span></span> 
</dt> <dd>

<span data-ttu-id="8684b-167">Type de données pour les *données*.</span><span class="sxs-lookup"><span data-stu-id="8684b-167">The data type for *data*.</span></span> <span data-ttu-id="8684b-168">Les constantes symboliques suivantes sont acceptées : \_ octet non signé GL \_ , \_ octet GL, GL \_ non signé \_ short, GL \_ short, GL \_ unsigned \_ int, GL \_ int et GL \_ float.</span><span class="sxs-lookup"><span data-stu-id="8684b-168">The following symbolic constants are accepted: GL\_UNSIGNED\_BYTE, GL\_BYTE, GL\_UNSIGNED\_SHORT, GL\_SHORT, GL\_UNSIGNED\_INT, GL\_INT, and GL\_FLOAT.</span></span>

<span data-ttu-id="8684b-169">Le tableau suivant résume la signification des constantes valides pour le paramètre de *type* .</span><span class="sxs-lookup"><span data-stu-id="8684b-169">The following table summarizes the meaning of the valid constants for the *type* parameter.</span></span>



| <span data-ttu-id="8684b-170">Valeur</span><span class="sxs-lookup"><span data-stu-id="8684b-170">Value</span></span>                                                                                                                                                                      | <span data-ttu-id="8684b-171">Signification</span><span class="sxs-lookup"><span data-stu-id="8684b-171">Meaning</span></span>                                          |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------|
| <span id="GL_UNSIGNED_BYTE"></span><span id="gl_unsigned_byte"></span><dl> <span data-ttu-id="8684b-172"><dt>**\_octet non signé GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="8684b-172"><dt>**GL\_UNSIGNED\_BYTE**</dt></span></span> </dl>    | <span data-ttu-id="8684b-173">Entier 8 bits non signé</span><span class="sxs-lookup"><span data-stu-id="8684b-173">Unsigned 8-bit integer</span></span><br/>                |
| <span id="GL_BYTE"></span><span id="gl_byte"></span><dl> <span data-ttu-id="8684b-174"><dt>**\_octet GL**</dt></span><span class="sxs-lookup"><span data-stu-id="8684b-174"><dt>**GL\_BYTE**</dt></span></span> </dl>                                | <span data-ttu-id="8684b-175">Entier 8 bits signé</span><span class="sxs-lookup"><span data-stu-id="8684b-175">Signed 8-bit integer</span></span><br/>                  |
| <span id="GL_UNSIGNED_SHORT"></span><span id="gl_unsigned_short"></span><dl> <span data-ttu-id="8684b-176"><dt>**NON signé dans le GL \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="8684b-176"><dt>**GL\_UNSIGNED\_SHORT**</dt></span></span> </dl> | <span data-ttu-id="8684b-177">Entier 16 bits non signé</span><span class="sxs-lookup"><span data-stu-id="8684b-177">Unsigned 16-bit integer</span></span><br/>               |
| <span id="GL_SHORT"></span><span id="gl_short"></span><dl> <span data-ttu-id="8684b-178"><dt>**\_abrégé GL**</dt></span><span class="sxs-lookup"><span data-stu-id="8684b-178"><dt>**GL\_SHORT**</dt></span></span> </dl>                             | <span data-ttu-id="8684b-179">Entier 16 bits signé</span><span class="sxs-lookup"><span data-stu-id="8684b-179">Signed 16-bit integer</span></span><br/>                 |
| <span id="GL_UNSIGNED_INT"></span><span id="gl_unsigned_int"></span><dl> <span data-ttu-id="8684b-180"><dt>**\_entier non signé GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="8684b-180"><dt>**GL\_UNSIGNED\_INT**</dt></span></span> </dl>       | <span data-ttu-id="8684b-181">Entier 32 bits non signé</span><span class="sxs-lookup"><span data-stu-id="8684b-181">Unsigned 32-bit integer</span></span><br/>               |
| <span id="GL_INT"></span><span id="gl_int"></span><dl> <span data-ttu-id="8684b-182"><dt>**GL \_ int**</dt></span><span class="sxs-lookup"><span data-stu-id="8684b-182"><dt>**GL\_INT**</dt></span></span> </dl>                                   | <span data-ttu-id="8684b-183">Entier de 32 bits</span><span class="sxs-lookup"><span data-stu-id="8684b-183">32-bit integer</span></span><br/>                        |
| <span id="GL_FLOAT"></span><span id="gl_float"></span><dl> <span data-ttu-id="8684b-184"><dt>**valeur \_ float du GL**</dt></span><span class="sxs-lookup"><span data-stu-id="8684b-184"><dt>**GL\_FLOAT**</dt></span></span> </dl>                             | <span data-ttu-id="8684b-185">Valeur à virgule flottante simple précision</span><span class="sxs-lookup"><span data-stu-id="8684b-185">Single-precision floating-point value</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="8684b-186">*data*</span><span class="sxs-lookup"><span data-stu-id="8684b-186">*data*</span></span> 
</dt> <dd>

<span data-ttu-id="8684b-187">Pointeur vers les données de texture de palette.</span><span class="sxs-lookup"><span data-stu-id="8684b-187">A pointer to the paletted texture data.</span></span> <span data-ttu-id="8684b-188">Les données sont traitées comme des pixels uniques d’une entrée de palette de texture 1D pour une entrée de palette.</span><span class="sxs-lookup"><span data-stu-id="8684b-188">The data is treated as single pixels of a 1-D texture palette entry for a palette entry.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8684b-189">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="8684b-189">Return value</span></span>

<span data-ttu-id="8684b-190">Cette fonction ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="8684b-190">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="8684b-191">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="8684b-191">Error codes</span></span>

<span data-ttu-id="8684b-192">Les codes d’erreur suivants peuvent être récupérés par la fonction [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="8684b-192">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="8684b-193">Nom</span><span class="sxs-lookup"><span data-stu-id="8684b-193">Name</span></span>                                                                                              | <span data-ttu-id="8684b-194">Signification</span><span class="sxs-lookup"><span data-stu-id="8684b-194">Meaning</span></span>                                                                                                                               |
|---------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="8684b-195"><dt>**\_valeur non valide du GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="8684b-195"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl> | <span data-ttu-id="8684b-196">*Start* ou *Count* était un entier non valide.</span><span class="sxs-lookup"><span data-stu-id="8684b-196">*start* or *count* was an invalid integer.</span></span><br/>                                                                                 |
| <dl> <span data-ttu-id="8684b-197"><dt>**\_enum GL non valide \_**</dt></span><span class="sxs-lookup"><span data-stu-id="8684b-197"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>  | <span data-ttu-id="8684b-198">la *cible*, le *format* ou le *type* n’était pas une valeur acceptée.</span><span class="sxs-lookup"><span data-stu-id="8684b-198">*target*, *format*,or *type* was not an accepted value.</span></span><br/>                                                                    |
| <dl> <span data-ttu-id="8684b-199"><dt>**\_valeur non valide du GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="8684b-199"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl> | <span data-ttu-id="8684b-200">La fonction a été appelée entre un appel à [**glBegin**](glbegin.md) et l’appel correspondant à [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="8684b-200">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="8684b-201">Notes</span><span class="sxs-lookup"><span data-stu-id="8684b-201">Remarks</span></span>

<span data-ttu-id="8684b-202">La fonction **glColorSubTableEXT** spécifie des parties de la palette de la texture ciblée actuelle à remplacer.</span><span class="sxs-lookup"><span data-stu-id="8684b-202">The **glColorSubTableEXT** function specifies portions of the current targeted texture's palette to be replaced.</span></span> <span data-ttu-id="8684b-203">Contrairement à [**glColorTableEXT**](glcolortableext.md), vous ne pouvez pas spécifier le paramètre *target* comme une palette de texture de proxy.</span><span class="sxs-lookup"><span data-stu-id="8684b-203">Unlike [**glColorTableEXT**](glcolortableext.md), you cannot specify the *target* parameter to be a proxy texture palette.</span></span>

> [!Note]  
> <span data-ttu-id="8684b-204">La fonction **glColorSubTableEXT** est une fonction d’extension qui ne fait pas partie de la bibliothèque OpenGL standard, mais qui fait partie de l' \_ extension de texture de palette ext GL \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="8684b-204">The **glColorSubTableEXT** function is an extension function that is not part of the standard OpenGL library but is part of the GL\_EXT\_paletted\_texture extension.</span></span> <span data-ttu-id="8684b-205">Pour vérifier si votre implémentation d’OpenGL prend en charge **glColorSubTableEXT**, appelez [**glGetString**](glgetstring.md)( \_ Extensions GL).</span><span class="sxs-lookup"><span data-stu-id="8684b-205">To check whether your implementation of OpenGL supports **glColorSubTableEXT**, call [**glGetString**](glgetstring.md)(GL\_EXTENSIONS).</span></span> <span data-ttu-id="8684b-206">Si elle retourne la \_ \_ texture de palette ext GL \_ , **glColorSubTableEXT** est pris en charge.</span><span class="sxs-lookup"><span data-stu-id="8684b-206">If it returns GL\_EXT\_paletted\_texture, **glColorSubTableEXT** is supported.</span></span> <span data-ttu-id="8684b-207">Pour obtenir l’adresse de fonction d’une fonction d’extension, appelez [**wglGetProcAddress**](/windows/desktop/api/wingdi/nf-wingdi-wglgetprocaddress).</span><span class="sxs-lookup"><span data-stu-id="8684b-207">To obtain the function address of an extension function, call [**wglGetProcAddress**](/windows/desktop/api/wingdi/nf-wingdi-wglgetprocaddress).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="8684b-208">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8684b-208">Requirements</span></span>



| <span data-ttu-id="8684b-209">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8684b-209">Requirement</span></span> | <span data-ttu-id="8684b-210">Valeur</span><span class="sxs-lookup"><span data-stu-id="8684b-210">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="8684b-211">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8684b-211">Minimum supported client</span></span><br/> | <span data-ttu-id="8684b-212">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8684b-212">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                      |
| <span data-ttu-id="8684b-213">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8684b-213">Minimum supported server</span></span><br/> | <span data-ttu-id="8684b-214">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8684b-214">Windows 2000 Server \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="8684b-215">En-tête</span><span class="sxs-lookup"><span data-stu-id="8684b-215">Header</span></span><br/>                   | <dl> <span data-ttu-id="8684b-216"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="8684b-216"><dt>Gl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8684b-217">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8684b-217">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8684b-218">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="8684b-218">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="8684b-219">**glColorTableEXT**</span><span class="sxs-lookup"><span data-stu-id="8684b-219">**glColorTableEXT**</span></span>](glcolortableext.md)
</dt> <dt>

[<span data-ttu-id="8684b-220">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="8684b-220">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="8684b-221">**glGetColorTableEXT**</span><span class="sxs-lookup"><span data-stu-id="8684b-221">**glGetColorTableEXT**</span></span>](glgetcolortableext.md)
</dt> <dt>

[<span data-ttu-id="8684b-222">**glGetColorTableParameterfvEXT**</span><span class="sxs-lookup"><span data-stu-id="8684b-222">**glGetColorTableParameterfvEXT**</span></span>](glgetcolortableparameterfvext.md)
</dt> <dt>

[<span data-ttu-id="8684b-223">**glGetColorTableParameterivEXT**</span><span class="sxs-lookup"><span data-stu-id="8684b-223">**glGetColorTableParameterivEXT**</span></span>](glgetcolortableparameterivext.md)
</dt> <dt>

[<span data-ttu-id="8684b-224">**glGetString**</span><span class="sxs-lookup"><span data-stu-id="8684b-224">**glGetString**</span></span>](glgetstring.md)
</dt> <dt>

[<span data-ttu-id="8684b-225">**wglGetProcAddress**</span><span class="sxs-lookup"><span data-stu-id="8684b-225">**wglGetProcAddress**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-wglgetprocaddress)
</dt> </dl>

 

 





