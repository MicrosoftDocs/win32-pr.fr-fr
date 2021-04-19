---
title: fonction glStencilFunc (GL. h)
description: La fonction glStencilFunc définit la fonction et la valeur de référence pour le test des stencils.
ms.assetid: 6c84415b-4d22-494b-90f2-6243d1406725
keywords:
- glStencilFunc fonction OpenGL
topic_type:
- apiref
api_name:
- glStencilFunc
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cd4f9c0a5ec905ecb061ddb54984bf35ff8edc3d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106518126"
---
# <a name="glstencilfunc-function"></a><span data-ttu-id="31bbd-104">glStencilFunc fonction)</span><span class="sxs-lookup"><span data-stu-id="31bbd-104">glStencilFunc function</span></span>

<span data-ttu-id="31bbd-105">La fonction **glStencilFunc** définit la fonction et la valeur de référence pour le test des stencils.</span><span class="sxs-lookup"><span data-stu-id="31bbd-105">The **glStencilFunc** function sets the function and reference value for stencil testing.</span></span>

## <a name="syntax"></a><span data-ttu-id="31bbd-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="31bbd-106">Syntax</span></span>


```C++
void WINAPI glStencilFunc(
   GLenum func,
   GLint  ref,
   GLuint mask
);
```



## <a name="parameters"></a><span data-ttu-id="31bbd-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="31bbd-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="31bbd-108">*func*</span><span class="sxs-lookup"><span data-stu-id="31bbd-108">*func*</span></span> 
</dt> <dd>

<span data-ttu-id="31bbd-109">Fonction de test.</span><span class="sxs-lookup"><span data-stu-id="31bbd-109">The test function.</span></span> <span data-ttu-id="31bbd-110">Les huit jetons suivants sont valides.</span><span class="sxs-lookup"><span data-stu-id="31bbd-110">The following eight tokens are valid.</span></span>



| <span data-ttu-id="31bbd-111">Valeur</span><span class="sxs-lookup"><span data-stu-id="31bbd-111">Value</span></span>                                                                                                                                                   | <span data-ttu-id="31bbd-112">Signification</span><span class="sxs-lookup"><span data-stu-id="31bbd-112">Meaning</span></span>                                                          |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| <span id="GL_NEVER"></span><span id="gl_never"></span><dl> <span data-ttu-id="31bbd-113"><dt>**GL \_ jamais**</dt></span><span class="sxs-lookup"><span data-stu-id="31bbd-113"><dt>**GL\_NEVER**</dt></span></span> </dl>          | <span data-ttu-id="31bbd-114">Échoue toujours.</span><span class="sxs-lookup"><span data-stu-id="31bbd-114">Always fails.</span></span><br/>                                         |
| <span id="GL_LESS"></span><span id="gl_less"></span><dl> <span data-ttu-id="31bbd-115"><dt>**GL \_ moins**</dt></span><span class="sxs-lookup"><span data-stu-id="31bbd-115"><dt>**GL\_LESS**</dt></span></span> </dl>             | <span data-ttu-id="31bbd-116">Passe si (  &  *masque* de référence) < (masque de *stencil*  &  ).</span><span class="sxs-lookup"><span data-stu-id="31bbd-116">Passes if (*ref* & *mask*) < (*stencil* & *mask*).</span></span><br/> |
| <span id="GL_LEQUAL"></span><span id="gl_lequal"></span><dl> <span data-ttu-id="31bbd-117"><dt>**\_LEQUAL GL**</dt></span><span class="sxs-lookup"><span data-stu-id="31bbd-117"><dt>**GL\_LEQUAL**</dt></span></span> </dl>       | <span data-ttu-id="31bbd-118">Passe si (  &  *masque* de référence) = (masque de *stencil*  &  ).</span><span class="sxs-lookup"><span data-stu-id="31bbd-118">Passes if (*ref* & *mask*) = (*stencil* & *mask*).</span></span><br/>    |
| <span id="GL_GREATER"></span><span id="gl_greater"></span><dl> <span data-ttu-id="31bbd-119"><dt>**GL \_ supérieur**</dt></span><span class="sxs-lookup"><span data-stu-id="31bbd-119"><dt>**GL\_GREATER**</dt></span></span> </dl>    | <span data-ttu-id="31bbd-120">Passe si (  &  *masque* de référence) > (masque de *stencil*  &  ).</span><span class="sxs-lookup"><span data-stu-id="31bbd-120">Passes if (*ref* & *mask*) > (*stencil* & *mask*).</span></span><br/> |
| <span id="GL_GEQUAL"></span><span id="gl_gequal"></span><dl> <span data-ttu-id="31bbd-121"><dt>**\_GEQUAL GL**</dt></span><span class="sxs-lookup"><span data-stu-id="31bbd-121"><dt>**GL\_GEQUAL**</dt></span></span> </dl>       | <span data-ttu-id="31bbd-122">Passe si (  &  *masque* de référence) = (masque de *stencil*  &  ).</span><span class="sxs-lookup"><span data-stu-id="31bbd-122">Passes if (*ref* & *mask*) = (*stencil* & *mask*).</span></span><br/>    |
| <span id="GL_EQUAL"></span><span id="gl_equal"></span><dl> <span data-ttu-id="31bbd-123"><dt>**GL \_ égal**</dt></span><span class="sxs-lookup"><span data-stu-id="31bbd-123"><dt>**GL\_EQUAL**</dt></span></span> </dl>          | <span data-ttu-id="31bbd-124">Passe si (  &  *masque* de référence) = (masque de *stencil*  &  ).</span><span class="sxs-lookup"><span data-stu-id="31bbd-124">Passes if (*ref* & *mask*) = (*stencil* & *mask*).</span></span><br/>    |
| <span id="GL_NOTEQUAL"></span><span id="gl_notequal"></span><dl> <span data-ttu-id="31bbd-125"><dt>**\_NOTEQUAL GL**</dt></span><span class="sxs-lookup"><span data-stu-id="31bbd-125"><dt>**GL\_NOTEQUAL**</dt></span></span> </dl> | <span data-ttu-id="31bbd-126">Passe si (  &  *masque* de référence) ?</span><span class="sxs-lookup"><span data-stu-id="31bbd-126">Passes if (*ref* & *mask*) ?</span></span> <span data-ttu-id="31bbd-127">(*gabarit*  &  *masque*).</span><span class="sxs-lookup"><span data-stu-id="31bbd-127">(*stencil* & *mask*).</span></span><br/>    |
| <span id="GL_ALWAYS"></span><span id="gl_always"></span><dl> <span data-ttu-id="31bbd-128"><dt>**\_toujours GL**</dt></span><span class="sxs-lookup"><span data-stu-id="31bbd-128"><dt>**GL\_ALWAYS**</dt></span></span> </dl>       | <span data-ttu-id="31bbd-129">Passe toujours.</span><span class="sxs-lookup"><span data-stu-id="31bbd-129">Always passes.</span></span><br/>                                        |



 

</dd> <dt>

<span data-ttu-id="31bbd-130">*ref*</span><span class="sxs-lookup"><span data-stu-id="31bbd-130">*ref*</span></span> 
</dt> <dd>

<span data-ttu-id="31bbd-131">Valeur de référence pour le test de stencil.</span><span class="sxs-lookup"><span data-stu-id="31bbd-131">The reference value for the stencil test.</span></span> <span data-ttu-id="31bbd-132">Le paramètre *ref* est ancré à la plage \[ 0, 2 *n* 1 \] , où *n* est le nombre de bitplanes dans la mémoire tampon du stencil.</span><span class="sxs-lookup"><span data-stu-id="31bbd-132">The *ref* parameter is clamped to the range \[0, 2 *n* 1\], where *n* is the number of bitplanes in the stencil buffer.</span></span>

</dd> <dt>

<span data-ttu-id="31bbd-133">*mask*</span><span class="sxs-lookup"><span data-stu-id="31bbd-133">*mask*</span></span> 
</dt> <dd>

<span data-ttu-id="31bbd-134">Masque qui est **et** Ed avec la valeur de référence et la valeur de stencil stockée lorsque le test est terminé.</span><span class="sxs-lookup"><span data-stu-id="31bbd-134">A mask that is **AND** ed with both the reference value and the stored stencil value when the test is done.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="31bbd-135">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="31bbd-135">Return value</span></span>

<span data-ttu-id="31bbd-136">Cette fonction ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="31bbd-136">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="31bbd-137">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="31bbd-137">Error codes</span></span>

<span data-ttu-id="31bbd-138">Les codes d’erreur suivants peuvent être récupérés par la fonction [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="31bbd-138">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="31bbd-139">Nom</span><span class="sxs-lookup"><span data-stu-id="31bbd-139">Name</span></span>                                                                                                  | <span data-ttu-id="31bbd-140">Signification</span><span class="sxs-lookup"><span data-stu-id="31bbd-140">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="31bbd-141"><dt>**\_enum GL non valide \_**</dt></span><span class="sxs-lookup"><span data-stu-id="31bbd-141"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="31bbd-142">*Func* ne faisait pas partie des huit valeurs acceptées.</span><span class="sxs-lookup"><span data-stu-id="31bbd-142">*func* was not one of the eight accepted values.</span></span><br/>                                                                           |
| <dl> <span data-ttu-id="31bbd-143"><dt>**\_opération non valide du GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="31bbd-143"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="31bbd-144">La fonction a été appelée entre un appel à [**glBegin**](glbegin.md) et l’appel correspondant à [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="31bbd-144">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="31bbd-145">Notes</span><span class="sxs-lookup"><span data-stu-id="31bbd-145">Remarks</span></span>

<span data-ttu-id="31bbd-146">Le stencil, tel que la mise en mémoire tampon *z*, permet d’activer et de désactiver le dessin par pixel.</span><span class="sxs-lookup"><span data-stu-id="31bbd-146">Stenciling, like *z*-buffering, enables and disables drawing on a per-pixel basis.</span></span> <span data-ttu-id="31bbd-147">Vous dessinez dans les plans de stencil à l’aide de primitives de dessin OpenGL, puis vous affichez la géométrie et les images à l’aide des plans de gabarit pour masquer des parties de l’écran.</span><span class="sxs-lookup"><span data-stu-id="31bbd-147">You draw into the stencil planes using OpenGL drawing primitives, then render geometry and images, using the stencil planes to mask out portions of the screen.</span></span> <span data-ttu-id="31bbd-148">Le stencil est généralement utilisé dans les algorithmes de rendu multipasses pour obtenir des effets spéciaux, tels que les décalques, le mode plan et le rendu de géométrie solide constructive.</span><span class="sxs-lookup"><span data-stu-id="31bbd-148">Stenciling is typically used in multipass rendering algorithms to achieve special effects, such as decals, outlining, and constructive solid geometry rendering.</span></span>

<span data-ttu-id="31bbd-149">Le test de stencil élimine conditionnellement un pixel en fonction du résultat d’une comparaison entre la valeur de référence et la valeur dans la mémoire tampon de stencil.</span><span class="sxs-lookup"><span data-stu-id="31bbd-149">The stencil test conditionally eliminates a pixel based on the outcome of a comparison between the reference value and the value in the stencil buffer.</span></span> <span data-ttu-id="31bbd-150">Le test est activé par [**glEnable**](glenable.md) et [**glDisable**](gldisable.md) avec l’argument de test de stencil du GL \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="31bbd-150">The test is enabled by [**glEnable**](glenable.md) and [**glDisable**](gldisable.md) with argument GL\_STENCIL\_TEST.</span></span> <span data-ttu-id="31bbd-151">Les actions effectuées en fonction du résultat du test de stencil sont spécifiées avec [**glStencilOp**](glstencilop.md).</span><span class="sxs-lookup"><span data-stu-id="31bbd-151">Actions taken based on the outcome of the stencil test are specified with [**glStencilOp**](glstencilop.md).</span></span>

<span data-ttu-id="31bbd-152">Le paramètre *Func* est une constante symbolique qui détermine la fonction de comparaison de stencil.</span><span class="sxs-lookup"><span data-stu-id="31bbd-152">The *func* parameter is a symbolic constant that determines the stencil comparison function.</span></span> <span data-ttu-id="31bbd-153">Il accepte l’une des huit valeurs indiquées ci-dessus.</span><span class="sxs-lookup"><span data-stu-id="31bbd-153">It accepts one of the eight values shown above.</span></span> <span data-ttu-id="31bbd-154">Le paramètre *ref* est une valeur de référence entière qui est utilisée dans la comparaison de stencil.</span><span class="sxs-lookup"><span data-stu-id="31bbd-154">The *ref* parameter is an integer reference value that is used in the stencil comparison.</span></span> <span data-ttu-id="31bbd-155">Elle est ancrée dans la plage \[ 0, 2 *n* 1 \] , où *n* est le nombre de bitplanes dans la mémoire tampon du stencil.</span><span class="sxs-lookup"><span data-stu-id="31bbd-155">It is clamped to the range \[0, 2 *n* 1\], where *n* is the number of bitplanes in the stencil buffer.</span></span> <span data-ttu-id="31bbd-156">Le paramètre *Mask* est au niveau du bit **and** Ed avec la valeur de référence et la valeur de stencil stockée, avec les valeurs **et** Ed qui participent à la comparaison.</span><span class="sxs-lookup"><span data-stu-id="31bbd-156">The *mask* parameter is bitwise **AND** ed with both the reference value and the stored stencil value, with the **AND** ed values participating in the comparison.</span></span>

<span data-ttu-id="31bbd-157">Si le *stencil* représente la valeur stockée dans l’emplacement de la mémoire tampon de stencil correspondante, la liste précédente montre l’effet de chaque fonction de comparaison qui peut être spécifiée par *Func*.</span><span class="sxs-lookup"><span data-stu-id="31bbd-157">If *stencil* represents the value stored in the corresponding stencil buffer location, the preceding list shows the effect of each comparison function that can be specified by *func*.</span></span> <span data-ttu-id="31bbd-158">Uniquement si la comparaison réussit est le pixel passé à l’étape suivante du processus de pixellisation (voir [**glStencilOp**](glstencilop.md)).</span><span class="sxs-lookup"><span data-stu-id="31bbd-158">Only if the comparison succeeds is the pixel passed through to the next stage in the rasterization process (see [**glStencilOp**](glstencilop.md)).</span></span> <span data-ttu-id="31bbd-159">Tous les tests considèrent les valeurs de *stencil* comme des entiers non signés dans la plage \[ 0, 2 *n* 1 \] , où *n* est le nombre de bitplanes dans la mémoire tampon de stencil.</span><span class="sxs-lookup"><span data-stu-id="31bbd-159">All tests treat *stencil* values as unsigned integers in the range \[0, 2 *n* 1\], where *n* is the number of bitplanes in the stencil buffer.</span></span>

<span data-ttu-id="31bbd-160">Au départ, le test stencil est désactivé.</span><span class="sxs-lookup"><span data-stu-id="31bbd-160">Initially, the stencil test is disabled.</span></span> <span data-ttu-id="31bbd-161">S’il n’existe pas de mémoire tampon de stencil, aucune modification de stencil ne peut se produire et c’est comme si le test de stencil passe toujours.</span><span class="sxs-lookup"><span data-stu-id="31bbd-161">If there is no stencil buffer, no stencil modification can occur and it is as if the stencil test always passes.</span></span>

<span data-ttu-id="31bbd-162">Les fonctions suivantes récupèrent les informations relatives à **glStencilFunc**:</span><span class="sxs-lookup"><span data-stu-id="31bbd-162">The following functions retrieve information related to **glStencilFunc**:</span></span>

<span data-ttu-id="31bbd-163">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) avec argument GL de \_ stencil \_ Func</span><span class="sxs-lookup"><span data-stu-id="31bbd-163">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_STENCIL\_FUNC</span></span>

<span data-ttu-id="31bbd-164">**glGet** avec argument valeur de stencil du gabarit de GL \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="31bbd-164">**glGet** with argument GL\_STENCIL\_VALUE\_MASK</span></span>

<span data-ttu-id="31bbd-165">**glGet** avec argument de \_ référence de stencil de GL \_</span><span class="sxs-lookup"><span data-stu-id="31bbd-165">**glGet** with argument GL\_STENCIL\_REF</span></span>

<span data-ttu-id="31bbd-166">**glGet** avec arguments de stencil de la comptabilité GL \_ \_</span><span class="sxs-lookup"><span data-stu-id="31bbd-166">**glGet** with argument GL\_STENCIL\_BITS</span></span>

<span data-ttu-id="31bbd-167">[**glIsEnabled**](glisenabled.md) avec l’argument \_ test de stencil du GL \_</span><span class="sxs-lookup"><span data-stu-id="31bbd-167">[**glIsEnabled**](glisenabled.md) with argument GL\_STENCIL\_TEST</span></span>

## <a name="requirements"></a><span data-ttu-id="31bbd-168">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="31bbd-168">Requirements</span></span>



| <span data-ttu-id="31bbd-169">Condition requise</span><span class="sxs-lookup"><span data-stu-id="31bbd-169">Requirement</span></span> | <span data-ttu-id="31bbd-170">Valeur</span><span class="sxs-lookup"><span data-stu-id="31bbd-170">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="31bbd-171">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="31bbd-171">Minimum supported client</span></span><br/> | <span data-ttu-id="31bbd-172">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="31bbd-172">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="31bbd-173">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="31bbd-173">Minimum supported server</span></span><br/> | <span data-ttu-id="31bbd-174">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="31bbd-174">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="31bbd-175">En-tête</span><span class="sxs-lookup"><span data-stu-id="31bbd-175">Header</span></span><br/>                   | <dl> <span data-ttu-id="31bbd-176"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="31bbd-176"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="31bbd-177">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="31bbd-177">Library</span></span><br/>                  | <dl> <span data-ttu-id="31bbd-178"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="31bbd-178"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="31bbd-179">DLL</span><span class="sxs-lookup"><span data-stu-id="31bbd-179">DLL</span></span><br/>                      | <dl> <span data-ttu-id="31bbd-180"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="31bbd-180"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="31bbd-181">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="31bbd-181">See also</span></span>

<dl> <dt>

[<span data-ttu-id="31bbd-182">**glAlphaFunc**</span><span class="sxs-lookup"><span data-stu-id="31bbd-182">**glAlphaFunc**</span></span>](glalphafunc.md)
</dt> <dt>

[<span data-ttu-id="31bbd-183">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="31bbd-183">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="31bbd-184">**glBlendFunc**</span><span class="sxs-lookup"><span data-stu-id="31bbd-184">**glBlendFunc**</span></span>](glblendfunc.md)
</dt> <dt>

[<span data-ttu-id="31bbd-185">**glDepthFunc**</span><span class="sxs-lookup"><span data-stu-id="31bbd-185">**glDepthFunc**</span></span>](gldepthfunc.md)
</dt> <dt>

[<span data-ttu-id="31bbd-186">**glEnable**</span><span class="sxs-lookup"><span data-stu-id="31bbd-186">**glEnable**</span></span>](glenable.md)
</dt> <dt>

[<span data-ttu-id="31bbd-187">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="31bbd-187">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="31bbd-188">**glIsEnabled**</span><span class="sxs-lookup"><span data-stu-id="31bbd-188">**glIsEnabled**</span></span>](glisenabled.md)
</dt> <dt>

[<span data-ttu-id="31bbd-189">**glLogicOp**</span><span class="sxs-lookup"><span data-stu-id="31bbd-189">**glLogicOp**</span></span>](gllogicop.md)
</dt> <dt>

[<span data-ttu-id="31bbd-190">**glStencilOp**</span><span class="sxs-lookup"><span data-stu-id="31bbd-190">**glStencilOp**</span></span>](glstencilop.md)
</dt> </dl>

 

 





