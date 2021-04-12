---
title: fonction glCopyTexSubImage2D (GL. h)
description: La fonction glCopyTexSubImage2D copie une sous-image d’une image de texture à deux dimensions à partir du trame.
ms.assetid: cbb644d4-6a23-4d66-8599-5f8b48e9b91f
keywords:
- glCopyTexSubImage2D fonction OpenGL
topic_type:
- apiref
api_name:
- glCopyTexSubImage2D
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0c966d031bb154b59cc54ae2e5d254347aa88d2a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384819"
---
# <a name="glcopytexsubimage2d-function"></a><span data-ttu-id="fa35c-104">glCopyTexSubImage2D fonction)</span><span class="sxs-lookup"><span data-stu-id="fa35c-104">glCopyTexSubImage2D function</span></span>

<span data-ttu-id="fa35c-105">La fonction **glCopyTexSubImage2D** copie une sous-image d’une image de texture à deux dimensions à partir du trame.</span><span class="sxs-lookup"><span data-stu-id="fa35c-105">The **glCopyTexSubImage2D** function copies a sub-image of a two-dimensional texture image from the framebuffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="fa35c-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fa35c-106">Syntax</span></span>


```C++
void WINAPI glCopyTexSubImage2D(
   GLenum  target,
   GLint   level,
   GLint   xoffset,
   GLint   yoffset,
   GLint   x,
   GLint   y,
   GLsizei width,
   GLsizei height
);
```



## <a name="parameters"></a><span data-ttu-id="fa35c-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="fa35c-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fa35c-108">*cible*</span><span class="sxs-lookup"><span data-stu-id="fa35c-108">*target*</span></span> 
</dt> <dd>

<span data-ttu-id="fa35c-109">Cible dans laquelle les données de l’image seront modifiées.</span><span class="sxs-lookup"><span data-stu-id="fa35c-109">The target to which the image data will be changed.</span></span> <span data-ttu-id="fa35c-110">Doit avoir la texture GL de valeur \_ \_ 2D.</span><span class="sxs-lookup"><span data-stu-id="fa35c-110">Must have the value GL\_TEXTURE\_2D.</span></span>

</dd> <dt>

<span data-ttu-id="fa35c-111">*level*</span><span class="sxs-lookup"><span data-stu-id="fa35c-111">*level*</span></span> 
</dt> <dd>

<span data-ttu-id="fa35c-112">Numéro de niveau de détail.</span><span class="sxs-lookup"><span data-stu-id="fa35c-112">The level-of-detail number.</span></span> <span data-ttu-id="fa35c-113">Le niveau 0 est l’image de base.</span><span class="sxs-lookup"><span data-stu-id="fa35c-113">Level 0 is the base image.</span></span> <span data-ttu-id="fa35c-114">Le niveau *n* est la *n* ième image de réduction mipmap.</span><span class="sxs-lookup"><span data-stu-id="fa35c-114">Level *n* is the *n* th mipmap reduction image.</span></span>

</dd> <dt>

<span data-ttu-id="fa35c-115">*xoffset*</span><span class="sxs-lookup"><span data-stu-id="fa35c-115">*xoffset*</span></span> 
</dt> <dd>

<span data-ttu-id="fa35c-116">Décalage de Texel dans la direction *x* dans le tableau de texture.</span><span class="sxs-lookup"><span data-stu-id="fa35c-116">The texel offset in the *x* direction within the texture array.</span></span>

</dd> <dt>

<span data-ttu-id="fa35c-117">*yoffset*</span><span class="sxs-lookup"><span data-stu-id="fa35c-117">*yoffset*</span></span> 
</dt> <dd>

<span data-ttu-id="fa35c-118">Décalage de Texel dans la direction *y* dans le tableau de texture.</span><span class="sxs-lookup"><span data-stu-id="fa35c-118">The texel offset in the *y* direction within the texture array.</span></span>

</dd> <dt>

<span data-ttu-id="fa35c-119">*x*</span><span class="sxs-lookup"><span data-stu-id="fa35c-119">*x*</span></span> 
</dt> <dd>

<span data-ttu-id="fa35c-120">Coordonnées du plan x de la fenêtre du coin inférieur gauche de la ligne de pixels à copier.</span><span class="sxs-lookup"><span data-stu-id="fa35c-120">The window x-plane coordinates of the lower-left corner of the row of pixels to be copied.</span></span>

</dd> <dt>

<span data-ttu-id="fa35c-121">*y*</span><span class="sxs-lookup"><span data-stu-id="fa35c-121">*y*</span></span> 
</dt> <dd>

<span data-ttu-id="fa35c-122">Coordonnées du plan y de la fenêtre du coin inférieur gauche de la ligne de pixels à copier.</span><span class="sxs-lookup"><span data-stu-id="fa35c-122">The window y-plane coordinates of the lower-left corner of the row of pixels to be copied.</span></span>

</dd> <dt>

<span data-ttu-id="fa35c-123">*width*</span><span class="sxs-lookup"><span data-stu-id="fa35c-123">*width*</span></span> 
</dt> <dd>

<span data-ttu-id="fa35c-124">Largeur de la sous-image de l’image de texture.</span><span class="sxs-lookup"><span data-stu-id="fa35c-124">The width of the sub-image of the texture image.</span></span> <span data-ttu-id="fa35c-125">La spécification d’une sous-image de texture avec une largeur nulle n’a aucun effet.</span><span class="sxs-lookup"><span data-stu-id="fa35c-125">Specifying a texture sub-image with zero width has no effect.</span></span>

</dd> <dt>

<span data-ttu-id="fa35c-126">*height*</span><span class="sxs-lookup"><span data-stu-id="fa35c-126">*height*</span></span> 
</dt> <dd>

<span data-ttu-id="fa35c-127">Hauteur de la sous-image de l’image de texture.</span><span class="sxs-lookup"><span data-stu-id="fa35c-127">The height of the sub-image of the texture image.</span></span> <span data-ttu-id="fa35c-128">La spécification d’une sous-image de texture avec une largeur nulle n’a aucun effet.</span><span class="sxs-lookup"><span data-stu-id="fa35c-128">Specifying a texture sub-image with zero width has no effect.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fa35c-129">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="fa35c-129">Return value</span></span>

<span data-ttu-id="fa35c-130">Cette fonction ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="fa35c-130">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="fa35c-131">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="fa35c-131">Error codes</span></span>

<span data-ttu-id="fa35c-132">Les codes d’erreur suivants peuvent être récupérés par la fonction [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="fa35c-132">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="fa35c-133">Nom</span><span class="sxs-lookup"><span data-stu-id="fa35c-133">Name</span></span>                                                                                                  | <span data-ttu-id="fa35c-134">Signification</span><span class="sxs-lookup"><span data-stu-id="fa35c-134">Meaning</span></span>                                                                                                                                                                                                                                                                                                                     |
|-------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="fa35c-135"><dt>**\_enum GL non valide \_**</dt></span><span class="sxs-lookup"><span data-stu-id="fa35c-135"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="fa35c-136">la *cible* n’est pas une valeur acceptée.</span><span class="sxs-lookup"><span data-stu-id="fa35c-136">*target* was not an accepted value.</span></span><br/>                                                                                                                                                                                                                                                                              |
| <dl> <span data-ttu-id="fa35c-137"><dt>**\_valeur non valide du GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="fa35c-137"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="fa35c-138">le *niveau* était inférieur à zéro ou supérieur au *Journal* 2 (*Max*), où *Max* est la valeur retournée de la taille de \_ texture max GL \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="fa35c-138">*level* was less than zero or greater than *log* 2 (*max*), where *max* is the returned value of GL\_MAX\_TEXTURE\_SIZE.</span></span><br/>                                                                                                                                                                                          |
| <dl> <span data-ttu-id="fa35c-139"><dt>**\_valeur non valide du GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="fa35c-139"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="fa35c-140">*xoffset* était inférieur à *Border* ou (*xoffset*  +  *Width*) était supérieur à (  +  *Border*), *YOFFSET* était inférieur à *Border*, ou (*YOFFSET*  +  *Height*) était supérieur à (  +  *Border*), où *w* est la \_ largeur de la texture GL et la \_ *bordure* est la bordure de la \_ texture GL \_ .</span><span class="sxs-lookup"><span data-stu-id="fa35c-140">*xoffset* was less than *border* or (*xoffset* + *width*)was greater than (*w* + *border*), *yoffset* was less than *border*, or (*yoffset* + *height*) was greater than (*h* + *border*), where *w* is GL\_TEXTURE\_WIDTH and *border* is GL\_TEXTURE\_BORDER.</span></span> <span data-ttu-id="fa35c-141">Notez que *w* comprend deux fois la largeur de la *bordure* .</span><span class="sxs-lookup"><span data-stu-id="fa35c-141">Note that *w* includes twice the *border* width.</span></span><br/> |
| <dl> <span data-ttu-id="fa35c-142"><dt>**\_valeur non valide du GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="fa35c-142"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="fa35c-143">la *largeur* était inférieure à la *bordure* ou *y* était inférieure à la *bordure*, où *Border* correspond à la largeur de la bordure du tableau de texture.</span><span class="sxs-lookup"><span data-stu-id="fa35c-143">*width* was less than *border* or *y* was less than *border*, where *border* is the border width of the texture array.</span></span><br/>                                                                                                                                                                                           |
| <dl> <span data-ttu-id="fa35c-144"><dt>**\_opération non valide du GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="fa35c-144"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="fa35c-145">Le tableau de texture n’a pas été défini par une opération [**glTexImage1D**](glteximage1d.md) précédente.</span><span class="sxs-lookup"><span data-stu-id="fa35c-145">The texture array was not defined by a previous [**glTexImage1D**](glteximage1d.md) operation.</span></span><br/>                                                                                                                                                                                                                  |
| <dl> <span data-ttu-id="fa35c-146"><dt>**\_opération non valide du GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="fa35c-146"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="fa35c-147">La fonction a été appelée entre un appel à [**glBegin**](glbegin.md) et l’appel correspondant à [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="fa35c-147">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/>                                                                                                                                                                                       |



## <a name="remarks"></a><span data-ttu-id="fa35c-148">Notes</span><span class="sxs-lookup"><span data-stu-id="fa35c-148">Remarks</span></span>

<span data-ttu-id="fa35c-149">La fonction **glCopyTexSubImage2D** remplace une partie rectangulaire d’une image de texture à deux dimensions par des pixels du trame actuel, plutôt qu’à partir de la mémoire principale comme c’est le cas pour [**glTexSubImage2D**](gltexsubimage2d.md).</span><span class="sxs-lookup"><span data-stu-id="fa35c-149">The **glCopyTexSubImage2D** function replaces a rectangular portion of a two-dimensional texture image with pixels from the current framebuffer, rather than from main memory as is the case for [**glTexSubImage2D**](gltexsubimage2d.md).</span></span>

<span data-ttu-id="fa35c-150">Un rectangle de pixels commençant par les coordonnées de fenêtre *x* et *y* et avec la *largeur* et la *hauteur* des dimensions remplace la partie du tableau de texture par les index *xoffset* à *xoffset* + (*Width* -1), les index *YOFFSET* à *YOFFSET* + (*Width* -1) au niveau du mipmap spécifié par *Level*.</span><span class="sxs-lookup"><span data-stu-id="fa35c-150">A rectangle of pixels beginning with the *x* and *y* window coordinates and with the dimensions *width* and *height* replaces the portion of the texture array with the indexes *xoffset* through *xoffset* + (*width* - 1), with the indexes *yoffset* through *yoffset* + (*width* - 1) at the mipmap level specified by *level*.</span></span> <span data-ttu-id="fa35c-151">Le rectangle de destination dans le tableau de texture ne peut pas inclure de texels à l’extérieur du tableau de texture spécifié à l’origine.</span><span class="sxs-lookup"><span data-stu-id="fa35c-151">The destination rectangle in the texture array cannot include any texels outside the originally specified texture array.</span></span>

<span data-ttu-id="fa35c-152">La fonction **glCopyTexSubImage2D** traite les pixels d’une ligne de la même façon que [**glCopyPixels**](glcopypixels.md), sauf qu’avant la conversion finale des pixels, toutes les valeurs de composant de pixel sont ancrées à la plage \[ 0, 1 \] et converties au format interne de la texture pour le stockage dans le tableau de texture.</span><span class="sxs-lookup"><span data-stu-id="fa35c-152">The **glCopyTexSubImage2D** function processes the pixels in a row in the same way as [**glCopyPixels**](glcopypixels.md), except that before the final conversion of the pixels, all pixel component values are clamped to the range \[0,1\] and converted to the texture's internal format for storage in the texture array.</span></span> <span data-ttu-id="fa35c-153">L’ordonnancement des pixels est déterminé par des coordonnées *x* inférieures correspondant à des coordonnées de texture inférieures.</span><span class="sxs-lookup"><span data-stu-id="fa35c-153">Pixel ordering is determined with lower *x* coordinates corresponding to lower texture coordinates.</span></span> <span data-ttu-id="fa35c-154">Si l’un des pixels dans une ligne spécifiée du trame actuel est en dehors de la fenêtre associée au contexte de rendu actuel, ses valeurs ne sont pas définies.</span><span class="sxs-lookup"><span data-stu-id="fa35c-154">If any of the pixels within a specified row of the current framebuffer are outside the window associated with the current rendering context, then their values are undefined.</span></span>

<span data-ttu-id="fa35c-155">Si l’un des pixels du rectangle spécifié du trame actuel est en dehors de la fenêtre de lecture associée au contexte de rendu actuel, les valeurs obtenues pour ces pixels ne sont pas définies.</span><span class="sxs-lookup"><span data-stu-id="fa35c-155">If any of the pixels within the specified rectangle of the current framebuffer are outside the read window associated with the current rendering context, then the values obtained for those pixels are undefined.</span></span> <span data-ttu-id="fa35c-156">Aucune modification n’est apportée au paramètre de *internalFormat*, de *largeur*, de *hauteur* ou de *bordure* du tableau de texture spécifié ou aux valeurs texels en dehors de la sous-image de texture spécifiée.</span><span class="sxs-lookup"><span data-stu-id="fa35c-156">No change is made to the *internalFormat*, *width*, *height*, or *border* parameter of the specified texture array or to texel values outside the specified texture sub-image.</span></span>

<span data-ttu-id="fa35c-157">Vous ne pouvez pas inclure d’appels à **glCopyTexSubImage2D** dans des listes d’affichage.</span><span class="sxs-lookup"><span data-stu-id="fa35c-157">You cannot include calls to **glCopyTexSubImage2D** in display lists.</span></span>

> [!Note]  
> <span data-ttu-id="fa35c-158">La fonction **glCopyTexSubImage2D** est disponible uniquement dans OpenGL version 1,1 ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="fa35c-158">The **glCopyTexSubImage2D** function is only available in OpenGL version 1.1 or later.</span></span>

 

<span data-ttu-id="fa35c-159">La texturation n’a aucun effet dans le mode d’index des couleurs.</span><span class="sxs-lookup"><span data-stu-id="fa35c-159">Texturing has no effect in color-index mode.</span></span> <span data-ttu-id="fa35c-160">Les fonctions [**glPixelStore**](glpixelstore-functions.md) et [**glPixelTransfer**](glpixeltransfer.md) affectent les images de texture exactement comme elles affectent la façon dont les pixels sont dessinés à l’aide de [**glDrawPixels**](gldrawpixels.md).</span><span class="sxs-lookup"><span data-stu-id="fa35c-160">The [**glPixelStore**](glpixelstore-functions.md) and [**glPixelTransfer**](glpixeltransfer.md) functions affect texture images in exactly the way they affect the way pixels are drawn using [**glDrawPixels**](gldrawpixels.md).</span></span>

<span data-ttu-id="fa35c-161">Les fonctions suivantes récupèrent les informations relatives à **glCopyTexSubImage2D**:</span><span class="sxs-lookup"><span data-stu-id="fa35c-161">The following functions retrieve information related to **glCopyTexSubImage2D**:</span></span>

[<span data-ttu-id="fa35c-162">**glGetTexImage**</span><span class="sxs-lookup"><span data-stu-id="fa35c-162">**glGetTexImage**</span></span>](glgetteximage.md)

<span data-ttu-id="fa35c-163">[**glIsEnabled**](glisenabled.md) avec argument GL \_ texture \_ 2D</span><span class="sxs-lookup"><span data-stu-id="fa35c-163">[**glIsEnabled**](glisenabled.md) with argument GL\_TEXTURE\_2D</span></span>

## <a name="requirements"></a><span data-ttu-id="fa35c-164">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="fa35c-164">Requirements</span></span>



| <span data-ttu-id="fa35c-165">Condition requise</span><span class="sxs-lookup"><span data-stu-id="fa35c-165">Requirement</span></span> | <span data-ttu-id="fa35c-166">Valeur</span><span class="sxs-lookup"><span data-stu-id="fa35c-166">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="fa35c-167">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fa35c-167">Minimum supported client</span></span><br/> | <span data-ttu-id="fa35c-168">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="fa35c-168">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="fa35c-169">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fa35c-169">Minimum supported server</span></span><br/> | <span data-ttu-id="fa35c-170">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="fa35c-170">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="fa35c-171">En-tête</span><span class="sxs-lookup"><span data-stu-id="fa35c-171">Header</span></span><br/>                   | <dl> <span data-ttu-id="fa35c-172"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="fa35c-172"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="fa35c-173">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="fa35c-173">Library</span></span><br/>                  | <dl> <span data-ttu-id="fa35c-174"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="fa35c-174"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="fa35c-175">DLL</span><span class="sxs-lookup"><span data-stu-id="fa35c-175">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fa35c-176"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fa35c-176"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fa35c-177">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fa35c-177">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fa35c-178">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="fa35c-178">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="fa35c-179">**glCopyPixels**</span><span class="sxs-lookup"><span data-stu-id="fa35c-179">**glCopyPixels**</span></span>](glcopypixels.md)
</dt> <dt>

[<span data-ttu-id="fa35c-180">**glCopyTexSubImage1D**</span><span class="sxs-lookup"><span data-stu-id="fa35c-180">**glCopyTexSubImage1D**</span></span>](glcopytexsubimage1d.md)
</dt> <dt>

[<span data-ttu-id="fa35c-181">**glDrawPixels**</span><span class="sxs-lookup"><span data-stu-id="fa35c-181">**glDrawPixels**</span></span>](gldrawpixels.md)
</dt> <dt>

[<span data-ttu-id="fa35c-182">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="fa35c-182">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="fa35c-183">**glFog**</span><span class="sxs-lookup"><span data-stu-id="fa35c-183">**glFog**</span></span>](glfog.md)
</dt> <dt>

[<span data-ttu-id="fa35c-184">**glPixelStore**</span><span class="sxs-lookup"><span data-stu-id="fa35c-184">**glPixelStore**</span></span>](glpixelstore-functions.md)
</dt> <dt>

[<span data-ttu-id="fa35c-185">**glPixelTransfer**</span><span class="sxs-lookup"><span data-stu-id="fa35c-185">**glPixelTransfer**</span></span>](glpixeltransfer.md)
</dt> <dt>

[<span data-ttu-id="fa35c-186">**glTexEnv**</span><span class="sxs-lookup"><span data-stu-id="fa35c-186">**glTexEnv**</span></span>](gltexenv-functions.md)
</dt> <dt>

[<span data-ttu-id="fa35c-187">**glTexGen**</span><span class="sxs-lookup"><span data-stu-id="fa35c-187">**glTexGen**</span></span>](gltexgen-functions.md)
</dt> <dt>

[<span data-ttu-id="fa35c-188">**glTexImage2D**</span><span class="sxs-lookup"><span data-stu-id="fa35c-188">**glTexImage2D**</span></span>](glteximage2d.md)
</dt> <dt>

[<span data-ttu-id="fa35c-189">**glTexSubImage2D**</span><span class="sxs-lookup"><span data-stu-id="fa35c-189">**glTexSubImage2D**</span></span>](gltexsubimage2d.md)
</dt> <dt>

[<span data-ttu-id="fa35c-190">**glTexParameter**</span><span class="sxs-lookup"><span data-stu-id="fa35c-190">**glTexParameter**</span></span>](gltexparameter-functions.md)
</dt> </dl>

 

 





