---
title: fonction glAccum (GL. h)
description: La fonction glAccum opère sur la mémoire tampon d’accumulation.
ms.assetid: 3ddd69fe-74fc-4ac0-be8d-bcaa71ac0292
keywords:
- glAccum fonction OpenGL
topic_type:
- apiref
api_name:
- glAccum
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f6d25e02971d07d54567c462708aa4efd87b2d32
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741948"
---
# <a name="glaccum-function"></a><span data-ttu-id="50630-104">glAccum fonction)</span><span class="sxs-lookup"><span data-stu-id="50630-104">glAccum function</span></span>

<span data-ttu-id="50630-105">La fonction **glAccum** opère sur la mémoire tampon d’accumulation.</span><span class="sxs-lookup"><span data-stu-id="50630-105">The **glAccum** function operates on the accumulation buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="50630-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="50630-106">Syntax</span></span>


```C++
void WINAPI glAccum(
   GLenum  op,
   GLfloat value
);
```



## <a name="parameters"></a><span data-ttu-id="50630-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="50630-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="50630-108">*opérationnel*</span><span class="sxs-lookup"><span data-stu-id="50630-108">*op*</span></span> 
</dt> <dd>

<span data-ttu-id="50630-109">Opération de tampon d’accumulation.</span><span class="sxs-lookup"><span data-stu-id="50630-109">The accumulation buffer operation.</span></span> <span data-ttu-id="50630-110">Les constantes symboliques acceptées sont les suivantes.</span><span class="sxs-lookup"><span data-stu-id="50630-110">The accepted symbolic constants are as follows.</span></span>



| <span data-ttu-id="50630-111">Valeur</span><span class="sxs-lookup"><span data-stu-id="50630-111">Value</span></span>                                                                                                                                             | <span data-ttu-id="50630-112">Signification</span><span class="sxs-lookup"><span data-stu-id="50630-112">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_ACCUM"></span><span id="gl_accum"></span><dl> <span data-ttu-id="50630-113"><dt>**\_total amort**</dt></span><span class="sxs-lookup"><span data-stu-id="50630-113"><dt>**GL\_ACCUM**</dt></span></span> </dl>    | <span data-ttu-id="50630-114">Obtient R, G, B et une valeur de la mémoire tampon actuellement sélectionnée pour la lecture (consultez [**glReadBuffer**](glreadbuffer.md)).</span><span class="sxs-lookup"><span data-stu-id="50630-114">Obtains R, G, B, and A values from the buffer currently selected for reading (see [**glReadBuffer**](glreadbuffer.md)).</span></span> <span data-ttu-id="50630-115">Chaque valeur de composant est divisée par 2 *n*  1, où *n* est le nombre de bits alloués à chaque composant de couleur dans la mémoire tampon actuellement sélectionnée.</span><span class="sxs-lookup"><span data-stu-id="50630-115">Each component value is divided by 2 *n*  1, where *n* is the number of bits allocated to each color component in the currently selected buffer.</span></span> <span data-ttu-id="50630-116">Le résultat est une valeur à virgule flottante dans la plage \[ 0, 1 \] , qui est multipliée par *valeur* et ajoutée au composant de pixel correspondant dans la mémoire tampon d’accumulation, ce qui a pour effet de mettre à jour la mémoire tampon d’accumulation.</span><span class="sxs-lookup"><span data-stu-id="50630-116">The result is a floating-point value in the range \[0,1\], which is multiplied by *value* and added to the corresponding pixel component in the accumulation buffer, thereby updating the accumulation buffer.</span></span><br/> |
| <span id="GL_LOAD"></span><span id="gl_load"></span><dl> <span data-ttu-id="50630-117"><dt>**charge du GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="50630-117"><dt>**GL\_LOAD**</dt></span></span> </dl>       | <span data-ttu-id="50630-118">Semblable à la \_ valeur de l’amortissement GL, à la différence que la valeur actuelle de la mémoire tampon d’accumulation n’est pas utilisée dans le calcul de la nouvelle valeur.</span><span class="sxs-lookup"><span data-stu-id="50630-118">Similar to GL\_ACCUM, except that the current value in the accumulation buffer is not used in the calculation of the new value.</span></span> <span data-ttu-id="50630-119">Autrement dit, les valeurs R, G, B et A de la mémoire tampon actuellement sélectionnée sont divisées par 2 *n*  1, multiplié par *valeur*, puis stockées dans la cellule de mémoire tampon d’accumulation correspondante, remplaçant la valeur actuelle.</span><span class="sxs-lookup"><span data-stu-id="50630-119">That is, the R, G, B, and A values from the currently selected buffer are divided by 2 *n*  1, multiplied by *value*, and then stored in the corresponding accumulation buffer cell, overwriting the current value.</span></span><br/>                                                                                                                                      |
| <span id="GL_ADD"></span><span id="gl_add"></span><dl> <span data-ttu-id="50630-120"><dt>**ajout au GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="50630-120"><dt>**GL\_ADD**</dt></span></span> </dl>          | <span data-ttu-id="50630-121">Ajoute la *valeur* à chaque R, G, B et A dans la mémoire tampon d’accumulation.</span><span class="sxs-lookup"><span data-stu-id="50630-121">Adds *value* to each R, G, B, and A in the accumulation buffer.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span id="GL_MULT"></span><span id="gl_mult"></span><dl> <span data-ttu-id="50630-122"><dt>**GL \_ mult**</dt></span><span class="sxs-lookup"><span data-stu-id="50630-122"><dt>**GL\_MULT**</dt></span></span> </dl>       | <span data-ttu-id="50630-123">Multiplie chaque R, G, B et A dans la mémoire tampon d’accumulation par *valeur* et retourne le composant mis à l’échelle à l’emplacement de la mémoire tampon d’accumulation correspondante.</span><span class="sxs-lookup"><span data-stu-id="50630-123">Multiplies each R, G, B, and A in the accumulation buffer by *value* and returns the scaled component to its corresponding accumulation buffer location.</span></span><br/>                                                                                                                                                                                                                                                                                                                                |
| <span id="GL_RETURN"></span><span id="gl_return"></span><dl> <span data-ttu-id="50630-124"><dt>**\_retour GL**</dt></span><span class="sxs-lookup"><span data-stu-id="50630-124"><dt>**GL\_RETURN**</dt></span></span> </dl> | <span data-ttu-id="50630-125">Transfère les valeurs de mémoire tampon de l’accumulation à la mémoire tampon de couleur ou aux mémoires tampons actuellement sélectionnées pour l’écriture.</span><span class="sxs-lookup"><span data-stu-id="50630-125">Transfers accumulation buffer values to the color buffer or buffers currently selected for writing.</span></span> <span data-ttu-id="50630-126">Chaque R, G, B et un composant sont multipliés par la *valeur*, puis multipliés par 2 *n*  1, fixés à la plage \[ 0, 2 *n*  1 \] et stockés dans la cellule de mémoire tampon d’affichage correspondante.</span><span class="sxs-lookup"><span data-stu-id="50630-126">Each R, G, B, and A component is multiplied by *value*, then multiplied by 2 *n*  1, clamped to the range \[0, 2 *n*  1 \], and stored in the corresponding display buffer cell.</span></span> <span data-ttu-id="50630-127">Les seules opérations de fragment appliquées à ce transfert sont la propriété de pixel, la ciseaux, le tramage et la couleur writemasks.</span><span class="sxs-lookup"><span data-stu-id="50630-127">The only fragment operations that are applied to this transfer are pixel ownership, scissor, dithering, and color writemasks.</span></span><br/>                                                                        |



 

</dd> <dt>

<span data-ttu-id="50630-128">*value*</span><span class="sxs-lookup"><span data-stu-id="50630-128">*value*</span></span> 
</dt> <dd>

<span data-ttu-id="50630-129">Valeur à virgule flottante utilisée dans l’opération de tampon d’accumulation.</span><span class="sxs-lookup"><span data-stu-id="50630-129">A floating-point value used in the accumulation buffer operation.</span></span> <span data-ttu-id="50630-130">Le paramètre *op* détermine la façon dont la *valeur* est utilisée.</span><span class="sxs-lookup"><span data-stu-id="50630-130">The *op* parameter determines how *value* is used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="50630-131">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="50630-131">Return value</span></span>

<span data-ttu-id="50630-132">Cette fonction ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="50630-132">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="50630-133">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="50630-133">Error codes</span></span>

<span data-ttu-id="50630-134">Les codes d’erreur suivants peuvent être récupérés par la fonction [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="50630-134">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="50630-135">Nom</span><span class="sxs-lookup"><span data-stu-id="50630-135">Name</span></span>                                                                                                  | <span data-ttu-id="50630-136">Signification</span><span class="sxs-lookup"><span data-stu-id="50630-136">Meaning</span></span>                                                                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="50630-137"><dt>**\_enum GL non valide \_**</dt></span><span class="sxs-lookup"><span data-stu-id="50630-137"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="50630-138">*op* n’est pas une valeur acceptée.</span><span class="sxs-lookup"><span data-stu-id="50630-138">*op* was not an accepted value.</span></span><br/>                                                                                                                                            |
| <dl> <span data-ttu-id="50630-139"><dt>**\_opération non valide du GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="50630-139"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="50630-140">Il n’y avait pas de mémoire tampon d’accumulation ou la fonction **glAccum** a été appelée entre un appel à [**glBegin**](glbegin.md) et l’appel correspondant à [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="50630-140">There was no accumulation buffer or the function **glAccum** was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="50630-141">Notes</span><span class="sxs-lookup"><span data-stu-id="50630-141">Remarks</span></span>

<span data-ttu-id="50630-142">La mémoire tampon d’accumulation est une mémoire tampon de plage étendue.</span><span class="sxs-lookup"><span data-stu-id="50630-142">The accumulation buffer is an extended-range color buffer.</span></span> <span data-ttu-id="50630-143">Les images ne sont pas rendues dans celui-ci.</span><span class="sxs-lookup"><span data-stu-id="50630-143">Images are not rendered into it.</span></span> <span data-ttu-id="50630-144">Au lieu de cela, les images rendues dans l’une des mémoires tampons de couleur sont ajoutées au contenu de la mémoire tampon d’accumulation après le rendu.</span><span class="sxs-lookup"><span data-stu-id="50630-144">Rather, images rendered into one of the color buffers are added to the contents of the accumulation buffer after rendering.</span></span> <span data-ttu-id="50630-145">Vous pouvez créer des effets tels que l’anticrénelage (des points, lignes et polygones), le flou directionnel et la profondeur de champ en cumulant les images générées avec des matrices de transformation différentes.</span><span class="sxs-lookup"><span data-stu-id="50630-145">You can create effects such as antialiasing (of points, lines, and polygons), motion blur, and depth of field by accumulating images generated with different transformation matrices.</span></span>

<span data-ttu-id="50630-146">Chaque pixel de la mémoire tampon d’accumulation se compose de valeurs rouge, vert, bleu et alpha.</span><span class="sxs-lookup"><span data-stu-id="50630-146">Each pixel in the accumulation buffer consists of red, green, blue, and alpha values.</span></span> <span data-ttu-id="50630-147">Le nombre de bits par composant dans la mémoire tampon d’accumulation dépend de l’implémentation.</span><span class="sxs-lookup"><span data-stu-id="50630-147">The number of bits per component in the accumulation buffer depends on the implementation.</span></span> <span data-ttu-id="50630-148">Vous pouvez examiner ce nombre en appelant quatre fois [**glGetIntegerv**](glgetintegerv.md) , à l’aide des arguments GL \_ Amort total \_ \_ bits, GL \_ Amort \_ Green \_ bits, GL \_ Amort \_ Blue bits \_ et GL \_ Amort \_ alpha \_ bits, respectivement.</span><span class="sxs-lookup"><span data-stu-id="50630-148">You can examine this number by calling [**glGetIntegerv**](glgetintegerv.md) four times, with the arguments GL\_ACCUM\_RED\_BITS, GL\_ACCUM\_GREEN\_BITS, GL\_ACCUM\_BLUE\_BITS, and GL\_ACCUM\_ALPHA\_BITS, respectively.</span></span> <span data-ttu-id="50630-149">Quel que soit le nombre de bits par composant, toutefois, la plage de valeurs stockées par chaque composant est \[ 1, ? 1 \] .</span><span class="sxs-lookup"><span data-stu-id="50630-149">Regardless of the number of bits per component, however, the range of values stored by each component is \[ 1,?1\].</span></span> <span data-ttu-id="50630-150">Les pixels de la mémoire tampon d’accumulation sont mappés un-à-un avec trame pixels.</span><span class="sxs-lookup"><span data-stu-id="50630-150">The accumulation buffer pixels are mapped one-to-one with framebuffer pixels.</span></span>

<span data-ttu-id="50630-151">La fonction **glAccum** opère sur la mémoire tampon d’accumulation.</span><span class="sxs-lookup"><span data-stu-id="50630-151">The **glAccum** function operates on the accumulation buffer.</span></span> <span data-ttu-id="50630-152">Le premier argument, *op*, est une constante symbolique qui sélectionne une opération de tampon d’accumulation.</span><span class="sxs-lookup"><span data-stu-id="50630-152">The first argument, *op*, is a symbolic constant that selects an accumulation buffer operation.</span></span> <span data-ttu-id="50630-153">Le deuxième argument, *value*, est une valeur à virgule flottante à utiliser dans cette opération.</span><span class="sxs-lookup"><span data-stu-id="50630-153">The second argument, *value*, is a floating-point value to be used in that operation.</span></span> <span data-ttu-id="50630-154">Cinq opérations sont spécifiées : GL \_ Amort, GL \_ Load, GL \_ Add, GL \_ mult et GL \_ Return.</span><span class="sxs-lookup"><span data-stu-id="50630-154">Five operations are specified: GL\_ACCUM, GL\_LOAD, GL\_ADD, GL\_MULT, and GL\_RETURN.</span></span>

<span data-ttu-id="50630-155">Toutes les opérations de mémoire tampon d’accumulation sont limitées à la zone de la zone de ciseaux actuelle et sont appliquées de la même façon que les composants rouge, vert, bleu et alpha de chaque pixel.</span><span class="sxs-lookup"><span data-stu-id="50630-155">All accumulation buffer operations are limited to the area of the current scissor box and are applied identically to the red, green, blue, and alpha components of each pixel.</span></span> <span data-ttu-id="50630-156">Le contenu d’un composant de pixel de mémoire tampon d’accumulation n’est pas défini si l’opération **glAccum** génère une valeur en dehors de la plage \[ 1, 1 \] .</span><span class="sxs-lookup"><span data-stu-id="50630-156">The contents of an accumulation buffer pixel component are undefined if the **glAccum** operation results in a value outside the range \[ 1,1\].</span></span>

<span data-ttu-id="50630-157">Pour effacer la mémoire tampon d’accumulation, utilisez la fonction [**glClearAccum**](glclearaccum.md) pour spécifier R, G, B et une valeur pour la définir, puis émettez une fonction [**glClear**](glclear.md) avec la mémoire tampon d’accumulation activée.</span><span class="sxs-lookup"><span data-stu-id="50630-157">To clear the accumulation buffer, use the [**glClearAccum**](glclearaccum.md) function to specify R, G, B, and A values to set it to, and issue a [**glClear**](glclear.md) function with the accumulation buffer enabled.</span></span>

<span data-ttu-id="50630-158">Seuls les pixels de la zone de ciseaux actuelle sont mis à jour par toute opération **glAccum** .</span><span class="sxs-lookup"><span data-stu-id="50630-158">Only those pixels within the current scissor box are updated by any **glAccum** operation.</span></span>

<span data-ttu-id="50630-159">Les fonctions suivantes récupèrent les informations relatives à la fonction **glAccum** :</span><span class="sxs-lookup"><span data-stu-id="50630-159">The following functions retrieve information related to the **glAccum** function:</span></span>

<span data-ttu-id="50630-160">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) avec argument GL \_ Amort \_ bits en rouge \_</span><span class="sxs-lookup"><span data-stu-id="50630-160">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_ACCUM\_RED\_BITS</span></span>

<span data-ttu-id="50630-161">**glGet** avec argument GL \_ Amort \_ Green \_ bits</span><span class="sxs-lookup"><span data-stu-id="50630-161">**glGet** with argument GL\_ACCUM\_GREEN\_BITS</span></span>

<span data-ttu-id="50630-162">**glGet** avec argument GL \_ Amort \_ Blue \_ bits</span><span class="sxs-lookup"><span data-stu-id="50630-162">**glGet** with argument GL\_ACCUM\_BLUE\_BITS</span></span>

<span data-ttu-id="50630-163">**glGet** avec argument GL \_ Amort \_ alpha \_ bits</span><span class="sxs-lookup"><span data-stu-id="50630-163">**glGet** with argument GL\_ACCUM\_ALPHA\_BITS</span></span>

## <a name="requirements"></a><span data-ttu-id="50630-164">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="50630-164">Requirements</span></span>



| <span data-ttu-id="50630-165">Condition requise</span><span class="sxs-lookup"><span data-stu-id="50630-165">Requirement</span></span> | <span data-ttu-id="50630-166">Valeur</span><span class="sxs-lookup"><span data-stu-id="50630-166">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="50630-167">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="50630-167">Minimum supported client</span></span><br/> | <span data-ttu-id="50630-168">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="50630-168">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="50630-169">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="50630-169">Minimum supported server</span></span><br/> | <span data-ttu-id="50630-170">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="50630-170">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="50630-171">En-tête</span><span class="sxs-lookup"><span data-stu-id="50630-171">Header</span></span><br/>                   | <dl> <span data-ttu-id="50630-172"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="50630-172"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="50630-173">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="50630-173">Library</span></span><br/>                  | <dl> <span data-ttu-id="50630-174"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="50630-174"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="50630-175">DLL</span><span class="sxs-lookup"><span data-stu-id="50630-175">DLL</span></span><br/>                      | <dl> <span data-ttu-id="50630-176"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="50630-176"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="50630-177">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="50630-177">See also</span></span>

<dl> <dt>

[<span data-ttu-id="50630-178">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="50630-178">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="50630-179">**glBlendFunc**</span><span class="sxs-lookup"><span data-stu-id="50630-179">**glBlendFunc**</span></span>](glblendfunc.md)
</dt> <dt>

[<span data-ttu-id="50630-180">**glClear**</span><span class="sxs-lookup"><span data-stu-id="50630-180">**glClear**</span></span>](glclear.md)
</dt> <dt>

[<span data-ttu-id="50630-181">**glClearAccum**</span><span class="sxs-lookup"><span data-stu-id="50630-181">**glClearAccum**</span></span>](glclearaccum.md)
</dt> <dt>

[<span data-ttu-id="50630-182">**glCopyPixels**</span><span class="sxs-lookup"><span data-stu-id="50630-182">**glCopyPixels**</span></span>](glcopypixels.md)
</dt> <dt>

[<span data-ttu-id="50630-183">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="50630-183">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="50630-184">**glGet**</span><span class="sxs-lookup"><span data-stu-id="50630-184">**glGet**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[<span data-ttu-id="50630-185">**glLogicOp**</span><span class="sxs-lookup"><span data-stu-id="50630-185">**glLogicOp**</span></span>](gllogicop.md)
</dt> <dt>

[<span data-ttu-id="50630-186">**glPixelStore**</span><span class="sxs-lookup"><span data-stu-id="50630-186">**glPixelStore**</span></span>](glpixelstore-functions.md)
</dt> <dt>

[<span data-ttu-id="50630-187">**glPixelTransfer**</span><span class="sxs-lookup"><span data-stu-id="50630-187">**glPixelTransfer**</span></span>](glpixeltransfer.md)
</dt> <dt>

[<span data-ttu-id="50630-188">**glReadBuffer**</span><span class="sxs-lookup"><span data-stu-id="50630-188">**glReadBuffer**</span></span>](glreadbuffer.md)
</dt> <dt>

[<span data-ttu-id="50630-189">**glReadPixels**</span><span class="sxs-lookup"><span data-stu-id="50630-189">**glReadPixels**</span></span>](glreadpixels.md)
</dt> <dt>

[<span data-ttu-id="50630-190">**glScissor**</span><span class="sxs-lookup"><span data-stu-id="50630-190">**glScissor**</span></span>](glscissor.md)
</dt> <dt>

[<span data-ttu-id="50630-191">**glStencilOp**</span><span class="sxs-lookup"><span data-stu-id="50630-191">**glStencilOp**</span></span>](glstencilop.md)
</dt> </dl>

 

 





