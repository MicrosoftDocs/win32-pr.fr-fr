---
title: fonction glCopyTexSubImage1D (GL. h)
description: La fonction glCopyTexSubImage1D copie une sous-image d’une image de texture unidimensionnelle à partir du trame.
ms.assetid: 718aee8a-6dce-49e1-a441-19beccd89f8d
keywords:
- glCopyTexSubImage1D fonction OpenGL
topic_type:
- apiref
api_name:
- glCopyTexSubImage1D
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 64006f9cec7e5fd2f3ca6f860249e579b16dbf10
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942360"
---
# <a name="glcopytexsubimage1d-function"></a><span data-ttu-id="041f4-104">glCopyTexSubImage1D fonction)</span><span class="sxs-lookup"><span data-stu-id="041f4-104">glCopyTexSubImage1D function</span></span>

<span data-ttu-id="041f4-105">La fonction **glCopyTexSubImage1D** copie une sous-image d’une image de texture unidimensionnelle à partir du trame.</span><span class="sxs-lookup"><span data-stu-id="041f4-105">The **glCopyTexSubImage1D** function copies a sub-image of a one-dimensional texture image from the framebuffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="041f4-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="041f4-106">Syntax</span></span>


```C++
void WINAPI glCopyTexSubImage1D(
   GLenum  target,
   GLint   level,
   GLint   xoffset,
   GLint   x,
   GLint   y,
   GLsizei width
);
```



## <a name="parameters"></a><span data-ttu-id="041f4-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="041f4-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="041f4-108">*cible*</span><span class="sxs-lookup"><span data-stu-id="041f4-108">*target*</span></span> 
</dt> <dd>

<span data-ttu-id="041f4-109">Cible dans laquelle les données de l’image seront modifiées.</span><span class="sxs-lookup"><span data-stu-id="041f4-109">The target to which the image data will be changed.</span></span> <span data-ttu-id="041f4-110">Doit avoir la texture GL \_ valeur \_ 1D.</span><span class="sxs-lookup"><span data-stu-id="041f4-110">Must have the value GL\_TEXTURE\_1D.</span></span>

</dd> <dt>

<span data-ttu-id="041f4-111">*level*</span><span class="sxs-lookup"><span data-stu-id="041f4-111">*level*</span></span> 
</dt> <dd>

<span data-ttu-id="041f4-112">Numéro de niveau de détail.</span><span class="sxs-lookup"><span data-stu-id="041f4-112">The level-of-detail number.</span></span> <span data-ttu-id="041f4-113">Le niveau 0 est l’image de base.</span><span class="sxs-lookup"><span data-stu-id="041f4-113">Level 0 is the base image.</span></span> <span data-ttu-id="041f4-114">Le niveau *n* est la *n* ième image de réduction mipmap.</span><span class="sxs-lookup"><span data-stu-id="041f4-114">Level *n* is the *n* th mipmap reduction image.</span></span>

</dd> <dt>

<span data-ttu-id="041f4-115">*xoffset*</span><span class="sxs-lookup"><span data-stu-id="041f4-115">*xoffset*</span></span> 
</dt> <dd>

<span data-ttu-id="041f4-116">Décalage de Texel dans le tableau de texture.</span><span class="sxs-lookup"><span data-stu-id="041f4-116">The texel offset within the texture array.</span></span>

</dd> <dt>

<span data-ttu-id="041f4-117">*x*</span><span class="sxs-lookup"><span data-stu-id="041f4-117">*x*</span></span> 
</dt> <dd>

<span data-ttu-id="041f4-118">Coordonnée du plan x de la fenêtre du coin inférieur gauche de la ligne de pixels à copier.</span><span class="sxs-lookup"><span data-stu-id="041f4-118">The window x-plane coordinate of the lower-left corner of the row of pixels to be copied.</span></span>

</dd> <dt>

<span data-ttu-id="041f4-119">*y*</span><span class="sxs-lookup"><span data-stu-id="041f4-119">*y*</span></span> 
</dt> <dd>

<span data-ttu-id="041f4-120">Coordonnée du plan y de la fenêtre du coin inférieur gauche de la ligne de pixels à copier.</span><span class="sxs-lookup"><span data-stu-id="041f4-120">The window y-plane coordinate of the lower-left corner of the row of pixels to be copied.</span></span>

</dd> <dt>

<span data-ttu-id="041f4-121">*width*</span><span class="sxs-lookup"><span data-stu-id="041f4-121">*width*</span></span> 
</dt> <dd>

<span data-ttu-id="041f4-122">Largeur de la sous-image de l’image de texture.</span><span class="sxs-lookup"><span data-stu-id="041f4-122">The width of the sub-image of the texture image.</span></span> <span data-ttu-id="041f4-123">La spécification d’une sous-image de texture avec une largeur nulle n’a aucun effet.</span><span class="sxs-lookup"><span data-stu-id="041f4-123">Specifying a texture sub-image with zero width has no effect.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="041f4-124">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="041f4-124">Return value</span></span>

<span data-ttu-id="041f4-125">Cette fonction ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="041f4-125">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="041f4-126">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="041f4-126">Error codes</span></span>

<span data-ttu-id="041f4-127">Les codes d’erreur suivants peuvent être récupérés par la fonction [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="041f4-127">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="041f4-128">Nom</span><span class="sxs-lookup"><span data-stu-id="041f4-128">Name</span></span>                                                                                                  | <span data-ttu-id="041f4-129">Signification</span><span class="sxs-lookup"><span data-stu-id="041f4-129">Meaning</span></span>                                                                                                                                                                                                                      |
|-------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="041f4-130"><dt>**\_enum GL non valide \_**</dt></span><span class="sxs-lookup"><span data-stu-id="041f4-130"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="041f4-131">la *cible* n’est pas une valeur acceptée.</span><span class="sxs-lookup"><span data-stu-id="041f4-131">*target* was not an accepted value.</span></span><br/>                                                                                                                                                                               |
| <dl> <span data-ttu-id="041f4-132"><dt>**\_valeur non valide du GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="041f4-132"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="041f4-133">le *niveau* était inférieur à zéro ou le *niveau* est supérieur à *log* 2 (*Max*), où *Max* est la valeur renvoyée de la \_ taille de texture max GL \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="041f4-133">*level* was less than zero or *level* is greater than *log* 2(*max*), where *max* is the returned value of GL\_MAX\_TEXTURE\_SIZE.</span></span><br/>                                                                                 |
| <dl> <span data-ttu-id="041f4-134"><dt>**\_valeur non valide du GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="041f4-134"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="041f4-135">*xoffset* était inférieur à la *bordure* ou(  +  *largeur* xoffset) est supérieur à(  +  *bordure* w), où *w* est la \_ largeur de la texture GL et la \_ *bordure* est la bordure de la texture GL \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="041f4-135">*xoffset* was less than *border* or (*xoffset* + *width*)was greater than (*w* + *border*), where *w* is GL\_TEXTURE\_WIDTH and *border* is GL\_TEXTURE\_BORDER.</span></span> <span data-ttu-id="041f4-136">Notez que *w* comprend deux fois la largeur de la *bordure* .</span><span class="sxs-lookup"><span data-stu-id="041f4-136">Note that *w* includes twice the *border* width.</span></span><br/> |
| <dl> <span data-ttu-id="041f4-137"><dt>**\_valeur non valide du GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="041f4-137"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="041f4-138">la *largeur* était inférieure à la *bordure* ou *y* était inférieure à la *bordure*, où *Border* correspond à la largeur de la bordure du tableau de texture.</span><span class="sxs-lookup"><span data-stu-id="041f4-138">*width* was less than *border* or *y* was less than *border*, where *border* is the border width of the texture array.</span></span><br/>                                                                                            |
| <dl> <span data-ttu-id="041f4-139"><dt>**\_opération non valide du GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="041f4-139"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="041f4-140">Le tableau de texture n’a pas été défini par une opération [**glTexImage1D**](glteximage1d.md) précédente.</span><span class="sxs-lookup"><span data-stu-id="041f4-140">The texture array was not defined by a previous [**glTexImage1D**](glteximage1d.md) operation.</span></span><br/>                                                                                                                   |
| <dl> <span data-ttu-id="041f4-141"><dt>**\_opération non valide du GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="041f4-141"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="041f4-142">La fonction a été appelée entre un appel à [**glBegin**](glbegin.md) et l’appel correspondant à [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="041f4-142">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/>                                                                                        |



## <a name="remarks"></a><span data-ttu-id="041f4-143">Notes</span><span class="sxs-lookup"><span data-stu-id="041f4-143">Remarks</span></span>

<span data-ttu-id="041f4-144">La fonction **glCopyTexSubImage1D** remplace une partie d’une image de texture unidimensionnelle par des pixels du trame actuel, plutôt qu’à partir de la mémoire principale comme c’est le cas pour [**glTexSubImage1D**](gltexsubimage1d.md).</span><span class="sxs-lookup"><span data-stu-id="041f4-144">The **glCopyTexSubImage1D** function replaces a portion of a one-dimensional texture image using pixels from the current framebuffer, rather than from main memory as is the case for [**glTexSubImage1D**](gltexsubimage1d.md).</span></span>

<span data-ttu-id="041f4-145">Une ligne de pixels commençant par les coordonnées de la fenêtre spécifiée par *x* et *y* et avec la *largeur* length remplace la partie du tableau de texture par les index *xoffset* par *xoffset* + (*Width* -1).</span><span class="sxs-lookup"><span data-stu-id="041f4-145">A row of pixels beginning with the window coordinates specified by *x* and *y* and with the length *width* replaces the portion of the texture array with the indexes *xoffset* through *xoffset* + (*width* - 1).</span></span> <span data-ttu-id="041f4-146">La destination dans le tableau de texture ne peut pas inclure de texels à l’extérieur du tableau de texture spécifié à l’origine.</span><span class="sxs-lookup"><span data-stu-id="041f4-146">The destination in the texture array cannot include any texels outside the originally specified texture array.</span></span>

<span data-ttu-id="041f4-147">La fonction **glCopyTexSubImage1D** traite les pixels d’une ligne de la même façon que [**glCopyPixels**](glcopypixels.md) , sauf qu’avant la conversion finale des pixels, toutes les valeurs de composant de pixel sont ancrées à la plage \[ 0, 1 \] et converties au format interne de la texture pour le stockage dans le tableau de texture.</span><span class="sxs-lookup"><span data-stu-id="041f4-147">The **glCopyTexSubImage1D** function processes the pixels in a row in the same way as [**glCopyPixels**](glcopypixels.md) except that before the final conversion of the pixels, all pixel component values are clamped to the range \[0,1\] and converted to the texture's internal format for storage in the texture array.</span></span> <span data-ttu-id="041f4-148">L’ordonnancement des pixels est déterminé par des coordonnées *x* inférieures correspondant à des coordonnées de texture inférieures.</span><span class="sxs-lookup"><span data-stu-id="041f4-148">Pixel ordering is determined with lower *x* coordinates corresponding to lower texture coordinates.</span></span> <span data-ttu-id="041f4-149">Si l’un des pixels dans une ligne spécifiée du trame actuel est en dehors de la fenêtre associée au contexte de rendu actuel, ses valeurs ne sont pas définies.</span><span class="sxs-lookup"><span data-stu-id="041f4-149">If any of the pixels within a specified row of the current framebuffer are outside the window associated with the current rendering context, then their values are undefined.</span></span>

<span data-ttu-id="041f4-150">Aucune modification n’est apportée au paramètre *internalFormat*, *Width* ou *Border* du tableau de texture spécifié ou aux valeurs texels en dehors de la sous-image de texture spécifiée.</span><span class="sxs-lookup"><span data-stu-id="041f4-150">No change is made to the *internalFormat*, *width*, or *border* parameter of the specified texture array or to texel values outside the specified texture sub-image.</span></span>

<span data-ttu-id="041f4-151">Vous ne pouvez pas inclure d’appels à **glCopyTexSubImage1D** dans des listes d’affichage.</span><span class="sxs-lookup"><span data-stu-id="041f4-151">You cannot include calls to **glCopyTexSubImage1D** in display lists.</span></span>

> [!Note]  
> <span data-ttu-id="041f4-152">La fonction **glCopyTexSubImage1D** est disponible uniquement dans OpenGL version 1,1 ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="041f4-152">The **glCopyTexSubImage1D** function is only available in OpenGL version 1.1 or later.</span></span>

 

<span data-ttu-id="041f4-153">La texturation n’a aucun effet dans le mode d’index des couleurs.</span><span class="sxs-lookup"><span data-stu-id="041f4-153">Texturing has no effect in color-index mode.</span></span> <span data-ttu-id="041f4-154">Les fonctions [**glPixelStore**](glpixelstore-functions.md) et [**glPixelTransfer**](glpixeltransfer.md) affectent les images de texture exactement comme elles affectent la façon dont les pixels sont dessinés à l’aide de [**glDrawPixels**](gldrawpixels.md).</span><span class="sxs-lookup"><span data-stu-id="041f4-154">The [**glPixelStore**](glpixelstore-functions.md) and [**glPixelTransfer**](glpixeltransfer.md) functions affect texture images in exactly the way they affect the way pixels are drawn using [**glDrawPixels**](gldrawpixels.md).</span></span>

<span data-ttu-id="041f4-155">Les fonctions suivantes récupèrent les informations relatives à **glCopyTexSubImage1D**:</span><span class="sxs-lookup"><span data-stu-id="041f4-155">The following functions retrieve information related to **glCopyTexSubImage1D**:</span></span>

[<span data-ttu-id="041f4-156">**glGetTexImage**</span><span class="sxs-lookup"><span data-stu-id="041f4-156">**glGetTexImage**</span></span>](glgetteximage.md)

<span data-ttu-id="041f4-157">[**glIsEnabled**](glisenabled.md) avec argument GL \_ texture \_ 1D</span><span class="sxs-lookup"><span data-stu-id="041f4-157">[**glIsEnabled**](glisenabled.md) with argument GL\_TEXTURE\_1D</span></span>

## <a name="requirements"></a><span data-ttu-id="041f4-158">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="041f4-158">Requirements</span></span>



| <span data-ttu-id="041f4-159">Condition requise</span><span class="sxs-lookup"><span data-stu-id="041f4-159">Requirement</span></span> | <span data-ttu-id="041f4-160">Valeur</span><span class="sxs-lookup"><span data-stu-id="041f4-160">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="041f4-161">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="041f4-161">Minimum supported client</span></span><br/> | <span data-ttu-id="041f4-162">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="041f4-162">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="041f4-163">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="041f4-163">Minimum supported server</span></span><br/> | <span data-ttu-id="041f4-164">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="041f4-164">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="041f4-165">En-tête</span><span class="sxs-lookup"><span data-stu-id="041f4-165">Header</span></span><br/>                   | <dl> <span data-ttu-id="041f4-166"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="041f4-166"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="041f4-167">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="041f4-167">Library</span></span><br/>                  | <dl> <span data-ttu-id="041f4-168"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="041f4-168"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="041f4-169">DLL</span><span class="sxs-lookup"><span data-stu-id="041f4-169">DLL</span></span><br/>                      | <dl> <span data-ttu-id="041f4-170"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="041f4-170"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="041f4-171">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="041f4-171">See also</span></span>

<dl> <dt>

[<span data-ttu-id="041f4-172">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="041f4-172">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="041f4-173">**glCopyTexSubImage2D**</span><span class="sxs-lookup"><span data-stu-id="041f4-173">**glCopyTexSubImage2D**</span></span>](glcopytexsubimage2d.md)
</dt> <dt>

[<span data-ttu-id="041f4-174">**glDrawPixels**</span><span class="sxs-lookup"><span data-stu-id="041f4-174">**glDrawPixels**</span></span>](gldrawpixels.md)
</dt> <dt>

[<span data-ttu-id="041f4-175">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="041f4-175">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="041f4-176">**glFog**</span><span class="sxs-lookup"><span data-stu-id="041f4-176">**glFog**</span></span>](glfog.md)
</dt> <dt>

[<span data-ttu-id="041f4-177">**glPixelStore**</span><span class="sxs-lookup"><span data-stu-id="041f4-177">**glPixelStore**</span></span>](glpixelstore-functions.md)
</dt> <dt>

[<span data-ttu-id="041f4-178">**glPixelTransfer**</span><span class="sxs-lookup"><span data-stu-id="041f4-178">**glPixelTransfer**</span></span>](glpixeltransfer.md)
</dt> <dt>

[<span data-ttu-id="041f4-179">**glTexEnv**</span><span class="sxs-lookup"><span data-stu-id="041f4-179">**glTexEnv**</span></span>](gltexenv-functions.md)
</dt> <dt>

[<span data-ttu-id="041f4-180">**glTexGen**</span><span class="sxs-lookup"><span data-stu-id="041f4-180">**glTexGen**</span></span>](gltexgen-functions.md)
</dt> <dt>

[<span data-ttu-id="041f4-181">**glTexImage1D**</span><span class="sxs-lookup"><span data-stu-id="041f4-181">**glTexImage1D**</span></span>](glteximage1d.md)
</dt> <dt>

[<span data-ttu-id="041f4-182">**glTexImage2D**</span><span class="sxs-lookup"><span data-stu-id="041f4-182">**glTexImage2D**</span></span>](glteximage2d.md)
</dt> <dt>

[<span data-ttu-id="041f4-183">**glTexSubImage1D**</span><span class="sxs-lookup"><span data-stu-id="041f4-183">**glTexSubImage1D**</span></span>](gltexsubimage1d.md)
</dt> <dt>

[<span data-ttu-id="041f4-184">**glTexSubImage2D**</span><span class="sxs-lookup"><span data-stu-id="041f4-184">**glTexSubImage2D**</span></span>](gltexsubimage2d.md)
</dt> <dt>

[<span data-ttu-id="041f4-185">**glTexParameter**</span><span class="sxs-lookup"><span data-stu-id="041f4-185">**glTexParameter**</span></span>](gltexparameter-functions.md)
</dt> </dl>

 

 





