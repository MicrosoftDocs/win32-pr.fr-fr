---
title: fonction glBitmap (GL. h)
description: La fonction glBitmap dessine une bitmap.
ms.assetid: 3cd8e41b-016b-4610-833a-048b5e50ae7c
keywords:
- glBitmap fonction OpenGL
topic_type:
- apiref
api_name:
- glBitmap
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7aeb97bb16a1e3c4c29d1dfb1a5320c02f44404d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032966"
---
# <a name="glbitmap-function"></a><span data-ttu-id="ef96e-104">glBitmap fonction)</span><span class="sxs-lookup"><span data-stu-id="ef96e-104">glBitmap function</span></span>

<span data-ttu-id="ef96e-105">La fonction **glBitmap** dessine une bitmap.</span><span class="sxs-lookup"><span data-stu-id="ef96e-105">The **glBitmap** function draws a bitmap.</span></span>

## <a name="syntax"></a><span data-ttu-id="ef96e-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ef96e-106">Syntax</span></span>


```C++
void WINAPI glBitmap(
         GLSizei width,
         GLSizei height,
         GLfloat xorig,
         GLfloat yorig,
         GLfloat xmove,
         GLfloat ymove,
   const GLubyte *bitmap
);
```



## <a name="parameters"></a><span data-ttu-id="ef96e-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ef96e-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ef96e-108">*width*</span><span class="sxs-lookup"><span data-stu-id="ef96e-108">*width*</span></span> 
</dt> <dd>

<span data-ttu-id="ef96e-109">Largeur en pixels de l’image bitmap.</span><span class="sxs-lookup"><span data-stu-id="ef96e-109">The pixel width of the bitmap image.</span></span>

</dd> <dt>

<span data-ttu-id="ef96e-110">*height*</span><span class="sxs-lookup"><span data-stu-id="ef96e-110">*height*</span></span> 
</dt> <dd>

<span data-ttu-id="ef96e-111">Hauteur en pixels de l’image bitmap.</span><span class="sxs-lookup"><span data-stu-id="ef96e-111">The pixel height of the bitmap image.</span></span>

</dd> <dt>

<span data-ttu-id="ef96e-112">*xorig*</span><span class="sxs-lookup"><span data-stu-id="ef96e-112">*xorig*</span></span> 
</dt> <dd>

<span data-ttu-id="ef96e-113">Emplacement *x* de l’origine dans l’image bitmap.</span><span class="sxs-lookup"><span data-stu-id="ef96e-113">The *x* location of the origin in the bitmap image.</span></span> <span data-ttu-id="ef96e-114">L’origine est mesurée à partir du coin inférieur gauche de la bitmap, avec des directions vers la droite et vers le haut étant les axes positifs.</span><span class="sxs-lookup"><span data-stu-id="ef96e-114">The origin is measured from the lower-left corner of the bitmap, with right and up directions being the positive axes.</span></span>

</dd> <dt>

<span data-ttu-id="ef96e-115">*yorig*</span><span class="sxs-lookup"><span data-stu-id="ef96e-115">*yorig*</span></span> 
</dt> <dd>

<span data-ttu-id="ef96e-116">Emplacement *y* de l’origine dans l’image bitmap.</span><span class="sxs-lookup"><span data-stu-id="ef96e-116">The *y* location of the origin in the bitmap image.</span></span> <span data-ttu-id="ef96e-117">L’origine est mesurée à partir du coin inférieur gauche de la bitmap, avec des directions vers la droite et vers le haut étant les axes positifs.</span><span class="sxs-lookup"><span data-stu-id="ef96e-117">The origin is measured from the lower-left corner of the bitmap, with right and up directions being the positive axes.</span></span>

</dd> <dt>

<span data-ttu-id="ef96e-118">*xmove*</span><span class="sxs-lookup"><span data-stu-id="ef96e-118">*xmove*</span></span> 
</dt> <dd>

<span data-ttu-id="ef96e-119">Décalage *x* à ajouter à la position de la trame actuelle après le dessin de la bitmap.</span><span class="sxs-lookup"><span data-stu-id="ef96e-119">The *x* offset to be added to the current raster position after the bitmap is drawn.</span></span>

</dd> <dt>

<span data-ttu-id="ef96e-120">*ymove*</span><span class="sxs-lookup"><span data-stu-id="ef96e-120">*ymove*</span></span> 
</dt> <dd>

<span data-ttu-id="ef96e-121">Décalage *y* à ajouter à la position de la trame actuelle après le dessin de la bitmap.</span><span class="sxs-lookup"><span data-stu-id="ef96e-121">The *y* offset to be added to the current raster position after the bitmap is drawn.</span></span>

</dd> <dt>

<span data-ttu-id="ef96e-122">*bitmap*</span><span class="sxs-lookup"><span data-stu-id="ef96e-122">*bitmap*</span></span> 
</dt> <dd>

<span data-ttu-id="ef96e-123">Adresse de l’image bitmap.</span><span class="sxs-lookup"><span data-stu-id="ef96e-123">The address of the bitmap image.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ef96e-124">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="ef96e-124">Return value</span></span>

<span data-ttu-id="ef96e-125">Cette fonction ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="ef96e-125">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="ef96e-126">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="ef96e-126">Error codes</span></span>

<span data-ttu-id="ef96e-127">Les codes d’erreur suivants peuvent être récupérés par la fonction [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="ef96e-127">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="ef96e-128">Nom</span><span class="sxs-lookup"><span data-stu-id="ef96e-128">Name</span></span>                                                                                                  | <span data-ttu-id="ef96e-129">Signification</span><span class="sxs-lookup"><span data-stu-id="ef96e-129">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="ef96e-130"><dt>**\_valeur non valide du GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="ef96e-130"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="ef96e-131">la *largeur* ou la *hauteur* est négative.</span><span class="sxs-lookup"><span data-stu-id="ef96e-131">*width* or *height* is negative.</span></span><br/>                                                                                           |
| <dl> <span data-ttu-id="ef96e-132"><dt>**\_opération non valide du GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="ef96e-132"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="ef96e-133">La fonction a été appelée entre un appel à [**glBegin**](glbegin.md) et l’appel correspondant à [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="ef96e-133">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="ef96e-134">Notes</span><span class="sxs-lookup"><span data-stu-id="ef96e-134">Remarks</span></span>

<span data-ttu-id="ef96e-135">Une image bitmap est une image binaire.</span><span class="sxs-lookup"><span data-stu-id="ef96e-135">A bitmap is a binary image.</span></span> <span data-ttu-id="ef96e-136">Lorsqu’elle est dessinée, la bitmap est positionnée par rapport à la position actuelle du raster, et trame pixels correspondant aux 1s dans le bitmap sont écrits à l’aide de la couleur ou de l’index raster actuel.</span><span class="sxs-lookup"><span data-stu-id="ef96e-136">When drawn, the bitmap is positioned relative to the current raster position, and framebuffer pixels corresponding to 1s in the bitmap are written using the current raster color or index.</span></span> <span data-ttu-id="ef96e-137">Les pixels de la mémoire tampon de trame correspondant aux zéros dans l’image bitmap ne sont pas modifiés.</span><span class="sxs-lookup"><span data-stu-id="ef96e-137">Frame-buffer pixels corresponding to zeros in the bitmap are not modified.</span></span>

<span data-ttu-id="ef96e-138">L’image bitmap est interprétée comme des données image pour la fonction [**glDrawPixels**](gldrawpixels.md) , avec la *largeur* et la *hauteur* correspondant aux arguments Width et Height de cette fonction, et avec le *type* défini sur bitmap GL \_ et le *format* défini sur l’index de \_ couleurs GL \_ .</span><span class="sxs-lookup"><span data-stu-id="ef96e-138">The bitmap image is interpreted like image data for the [**glDrawPixels**](gldrawpixels.md) function, with *width* and *height* corresponding to the width and height arguments of that function, and with *type* set to GL\_BITMAP and *format* set to GL\_COLOR\_INDEX.</span></span> <span data-ttu-id="ef96e-139">Les modes que vous spécifiez à l’aide de [**glPixelStore**](glpixelstore-functions.md) affectent l’interprétation des données de l’image bitmap ; les modes que vous spécifiez à l’aide de [**glPixelTransfer**](glpixeltransfer.md) ne le sont pas.</span><span class="sxs-lookup"><span data-stu-id="ef96e-139">Modes you specify using [**glPixelStore**](glpixelstore-functions.md) affect the interpretation of bitmap image data; modes you specify using [**glPixelTransfer**](glpixeltransfer.md) do not.</span></span>

<span data-ttu-id="ef96e-140">Si la position raster actuelle n’est pas valide, **glBitmap** est ignoré.</span><span class="sxs-lookup"><span data-stu-id="ef96e-140">If the current raster position is invalid, **glBitmap** is ignored.</span></span> <span data-ttu-id="ef96e-141">Dans le cas contraire, l’angle inférieur gauche de l’image bitmap est positionné aux coordonnées de la fenêtre suivante :</span><span class="sxs-lookup"><span data-stu-id="ef96e-141">Otherwise, the lower-left corner of the bitmap image is positioned at the following window coordinates:</span></span>

<span data-ttu-id="ef96e-142">*x*<sub>w</sub>  =  *x*<sub>r</sub> *x*?</span><span class="sxs-lookup"><span data-stu-id="ef96e-142">*x*<sub>w</sub> = *x*<sub>r</sub> *x*?</span></span>

<span data-ttu-id="ef96e-143">*y*<sub>w</sub>  =  *o*<sub>r</sub> *y*?</span><span class="sxs-lookup"><span data-stu-id="ef96e-143">*y*<sub>w</sub> = *y*<sub>r</sub> *y*?</span></span>

<span data-ttu-id="ef96e-144">Dans ces coordonnées, (*x*<sub>r</sub> , *y*<sub>r</sub> ) est la position raster et (*x*?</span><span class="sxs-lookup"><span data-stu-id="ef96e-144">In these coordinates, (*x*<sub>r</sub> , *y*<sub>r</sub> ) is the raster position, and (*x*?</span></span> <span data-ttu-id="ef96e-145">, *y*?</span><span class="sxs-lookup"><span data-stu-id="ef96e-145">, *y*?</span></span> <span data-ttu-id="ef96e-146">) est l’origine de l’image bitmap.</span><span class="sxs-lookup"><span data-stu-id="ef96e-146">) is the bitmap origin.</span></span> <span data-ttu-id="ef96e-147">Les fragments sont ensuite générés pour chaque pixel correspondant à un 1 dans l’image bitmap.</span><span class="sxs-lookup"><span data-stu-id="ef96e-147">Fragments are then generated for each pixel corresponding to a 1 in the bitmap image.</span></span> <span data-ttu-id="ef96e-148">Ces fragments sont générés à l’aide de la coordonnée *z* de trame actuelle, de l’index de couleur ou de couleur et des coordonnées de texture raster actuelles.</span><span class="sxs-lookup"><span data-stu-id="ef96e-148">These fragments are generated using the current raster *z*-coordinate, color or color index, and current raster texture coordinates.</span></span> <span data-ttu-id="ef96e-149">Ils sont ensuite traités comme s’ils avaient été générés à l’aide d’un point, d’une ligne ou d’un polygone, y compris le mappage de texture, le surlignage et toutes les opérations par fragment, telles que le test alpha et de profondeur.</span><span class="sxs-lookup"><span data-stu-id="ef96e-149">They are then treated just as if they had been generated by a point, line, or polygon, including texture mapping, fogging, and all per-fragment operations such as alpha and depth testing.</span></span>

<span data-ttu-id="ef96e-150">Une fois que l’image bitmap a été dessinée, les coordonnées *x* et *y* de la position raster actuelle sont décalées par *xmove* et *ymove*.</span><span class="sxs-lookup"><span data-stu-id="ef96e-150">After the bitmap has been drawn, the *x* and *y* coordinates of the current raster position are offset by *xmove* and *ymove*.</span></span> <span data-ttu-id="ef96e-151">Aucune modification n’est apportée à la coordonnée *z* de la position du raster actuel ou aux coordonnées de couleur, d’index ou de texture raster actuelles.</span><span class="sxs-lookup"><span data-stu-id="ef96e-151">No change is made to the *z*-coordinate of the current raster position, or to the current raster color, index, or texture coordinates.</span></span>

<span data-ttu-id="ef96e-152">Les fonctions suivantes récupèrent les informations relatives à la fonction **glBitmap** :</span><span class="sxs-lookup"><span data-stu-id="ef96e-152">The following functions retrieve information related to the **glBitmap** function:</span></span>

<span data-ttu-id="ef96e-153">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) avec argument GL \_ Current \_ Raster \_ position</span><span class="sxs-lookup"><span data-stu-id="ef96e-153">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_CURRENT\_RASTER\_POSITION</span></span>

 

<span data-ttu-id="ef96e-154">**glGet** avec argument GL \_ Current \_ Raster \_ couleur</span><span class="sxs-lookup"><span data-stu-id="ef96e-154">**glGet** with argument GL\_CURRENT\_RASTER\_COLOR</span></span>

 

<span data-ttu-id="ef96e-155">**glGet** avec argument GL \_ Current \_ Raster \_ index</span><span class="sxs-lookup"><span data-stu-id="ef96e-155">**glGet** with argument GL\_CURRENT\_RASTER\_INDEX</span></span>

 

<span data-ttu-id="ef96e-156">**glGet** avec argument de \_ la \_ texture de TRAMe actuelle du \_ GL \_</span><span class="sxs-lookup"><span data-stu-id="ef96e-156">**glGet** with argument GL\_CURRENT\_RASTER\_TEXTURE\_COORDS</span></span>

 

<span data-ttu-id="ef96e-157">**glGet** avec argument GL \_ Current \_ Raster \_ position \_ valide</span><span class="sxs-lookup"><span data-stu-id="ef96e-157">**glGet** with argument GL\_CURRENT\_RASTER\_POSITION\_VALID</span></span>

## <a name="requirements"></a><span data-ttu-id="ef96e-158">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ef96e-158">Requirements</span></span>



| <span data-ttu-id="ef96e-159">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ef96e-159">Requirement</span></span> | <span data-ttu-id="ef96e-160">Valeur</span><span class="sxs-lookup"><span data-stu-id="ef96e-160">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ef96e-161">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ef96e-161">Minimum supported client</span></span><br/> | <span data-ttu-id="ef96e-162">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ef96e-162">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="ef96e-163">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ef96e-163">Minimum supported server</span></span><br/> | <span data-ttu-id="ef96e-164">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ef96e-164">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="ef96e-165">En-tête</span><span class="sxs-lookup"><span data-stu-id="ef96e-165">Header</span></span><br/>                   | <dl> <span data-ttu-id="ef96e-166"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="ef96e-166"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="ef96e-167">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="ef96e-167">Library</span></span><br/>                  | <dl> <span data-ttu-id="ef96e-168"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ef96e-168"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="ef96e-169">DLL</span><span class="sxs-lookup"><span data-stu-id="ef96e-169">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ef96e-170"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ef96e-170"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ef96e-171">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ef96e-171">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ef96e-172">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="ef96e-172">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="ef96e-173">**glDrawPixels**</span><span class="sxs-lookup"><span data-stu-id="ef96e-173">**glDrawPixels**</span></span>](gldrawpixels.md)
</dt> <dt>

[<span data-ttu-id="ef96e-174">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="ef96e-174">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="ef96e-175">**glPixelStore**</span><span class="sxs-lookup"><span data-stu-id="ef96e-175">**glPixelStore**</span></span>](glpixelstore-functions.md)
</dt> <dt>

[<span data-ttu-id="ef96e-176">**glPixelTransfer**</span><span class="sxs-lookup"><span data-stu-id="ef96e-176">**glPixelTransfer**</span></span>](glpixeltransfer.md)
</dt> <dt>

[<span data-ttu-id="ef96e-177">**glRasterPos**</span><span class="sxs-lookup"><span data-stu-id="ef96e-177">**glRasterPos**</span></span>](glrasterpos-functions.md)
</dt> </dl>

 

 





