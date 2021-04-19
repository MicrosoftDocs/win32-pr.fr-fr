---
title: fonction glAlphaFunc (GL. h)
description: La fonction glAlphaFunc permet à votre application de définir la fonction de test alpha.
ms.assetid: 6c0c06b5-1bad-4590-a262-f134f63f0936
keywords:
- glAlphaFunc fonction OpenGL
topic_type:
- apiref
api_name:
- glAlphaFunc
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6cf96cfe2be0224c9c2e2409fc68805b530ae1f9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106513609"
---
# <a name="glalphafunc-function"></a><span data-ttu-id="1b28b-104">glAlphaFunc fonction)</span><span class="sxs-lookup"><span data-stu-id="1b28b-104">glAlphaFunc function</span></span>

<span data-ttu-id="1b28b-105">La fonction **glAlphaFunc** permet à votre application de définir la fonction de test alpha.</span><span class="sxs-lookup"><span data-stu-id="1b28b-105">The **glAlphaFunc** function enables your application to set the alpha test function.</span></span>

## <a name="syntax"></a><span data-ttu-id="1b28b-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1b28b-106">Syntax</span></span>


```C++
void WINAPI glAlphaFunc(
   GLenum   func,
   GLclampf ref
);
```



## <a name="parameters"></a><span data-ttu-id="1b28b-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1b28b-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1b28b-108">*func*</span><span class="sxs-lookup"><span data-stu-id="1b28b-108">*func*</span></span> 
</dt> <dd>

<span data-ttu-id="1b28b-109">Fonction de comparaison alpha.</span><span class="sxs-lookup"><span data-stu-id="1b28b-109">The alpha comparison function.</span></span> <span data-ttu-id="1b28b-110">Voici les constantes symboliques acceptées et leurs significations.</span><span class="sxs-lookup"><span data-stu-id="1b28b-110">The following are the accepted symbolic constants and their meanings.</span></span>



| <span data-ttu-id="1b28b-111">Valeur</span><span class="sxs-lookup"><span data-stu-id="1b28b-111">Value</span></span>                                                                                                                                                   | <span data-ttu-id="1b28b-112">Signification</span><span class="sxs-lookup"><span data-stu-id="1b28b-112">Meaning</span></span>                                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| <span id="GL_NEVER"></span><span id="gl_never"></span><dl> <span data-ttu-id="1b28b-113"><dt>**GL \_ jamais**</dt></span><span class="sxs-lookup"><span data-stu-id="1b28b-113"><dt>**GL\_NEVER**</dt></span></span> </dl>          | <span data-ttu-id="1b28b-114">Ne passe jamais.</span><span class="sxs-lookup"><span data-stu-id="1b28b-114">Never passes.</span></span><br/>                                                                       |
| <span id="GL_LESS"></span><span id="gl_less"></span><dl> <span data-ttu-id="1b28b-115"><dt>**GL \_ moins**</dt></span><span class="sxs-lookup"><span data-stu-id="1b28b-115"><dt>**GL\_LESS**</dt></span></span> </dl>             | <span data-ttu-id="1b28b-116">Passe si la valeur alpha entrante est inférieure à la valeur de référence.</span><span class="sxs-lookup"><span data-stu-id="1b28b-116">Passes if the incoming alpha value is less than the reference value.</span></span><br/>                |
| <span id="GL_EQUAL"></span><span id="gl_equal"></span><dl> <span data-ttu-id="1b28b-117"><dt>**GL \_ égal**</dt></span><span class="sxs-lookup"><span data-stu-id="1b28b-117"><dt>**GL\_EQUAL**</dt></span></span> </dl>          | <span data-ttu-id="1b28b-118">Passe si la valeur alpha entrante est égale à la valeur de référence.</span><span class="sxs-lookup"><span data-stu-id="1b28b-118">Passes if the incoming alpha value is equal to the reference value.</span></span><br/>                 |
| <span id="GL_LEQUAL"></span><span id="gl_lequal"></span><dl> <span data-ttu-id="1b28b-119"><dt>**\_LEQUAL GL**</dt></span><span class="sxs-lookup"><span data-stu-id="1b28b-119"><dt>**GL\_LEQUAL**</dt></span></span> </dl>       | <span data-ttu-id="1b28b-120">Passe si la valeur alpha entrante est inférieure ou égale à la valeur de référence.</span><span class="sxs-lookup"><span data-stu-id="1b28b-120">Passes if the incoming alpha value is less than or equal to the reference value.</span></span><br/>    |
| <span id="GL_GREATER"></span><span id="gl_greater"></span><dl> <span data-ttu-id="1b28b-121"><dt>**GL \_ supérieur**</dt></span><span class="sxs-lookup"><span data-stu-id="1b28b-121"><dt>**GL\_GREATER**</dt></span></span> </dl>    | <span data-ttu-id="1b28b-122">Passe si la valeur alpha entrante est supérieure à la valeur de référence.</span><span class="sxs-lookup"><span data-stu-id="1b28b-122">Passes if the incoming alpha value is greater than the reference value.</span></span><br/>             |
| <span id="GL_NOTEQUAL"></span><span id="gl_notequal"></span><dl> <span data-ttu-id="1b28b-123"><dt>**\_NOTEQUAL GL**</dt></span><span class="sxs-lookup"><span data-stu-id="1b28b-123"><dt>**GL\_NOTEQUAL**</dt></span></span> </dl> | <span data-ttu-id="1b28b-124">Passe si la valeur alpha entrante n’est pas égale à la valeur de référence.</span><span class="sxs-lookup"><span data-stu-id="1b28b-124">Passes if the incoming alpha value is not equal to the reference value.</span></span><br/>             |
| <span id="GL_GEQUAL"></span><span id="gl_gequal"></span><dl> <span data-ttu-id="1b28b-125"><dt>**\_GEQUAL GL**</dt></span><span class="sxs-lookup"><span data-stu-id="1b28b-125"><dt>**GL\_GEQUAL**</dt></span></span> </dl>       | <span data-ttu-id="1b28b-126">Passe si la valeur alpha entrante est supérieure ou égale à la valeur de référence.</span><span class="sxs-lookup"><span data-stu-id="1b28b-126">Passes if the incoming alpha value is greater than or equal to the reference value.</span></span><br/> |
| <span id="GL_ALWAYS"></span><span id="gl_always"></span><dl> <span data-ttu-id="1b28b-127"><dt>**\_toujours GL**</dt></span><span class="sxs-lookup"><span data-stu-id="1b28b-127"><dt>**GL\_ALWAYS**</dt></span></span> </dl>       | <span data-ttu-id="1b28b-128">Passe toujours.</span><span class="sxs-lookup"><span data-stu-id="1b28b-128">Always passes.</span></span> <span data-ttu-id="1b28b-129">Il s’agit de la valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="1b28b-129">This is the default.</span></span><br/>                                                 |



 

</dd> <dt>

<span data-ttu-id="1b28b-130">*ref*</span><span class="sxs-lookup"><span data-stu-id="1b28b-130">*ref*</span></span> 
</dt> <dd>

<span data-ttu-id="1b28b-131">Valeur de référence à laquelle les valeurs alpha entrantes sont comparées.</span><span class="sxs-lookup"><span data-stu-id="1b28b-131">The reference value to which incoming alpha values are compared.</span></span> <span data-ttu-id="1b28b-132">Cette valeur est ancrée à la plage de 0 à 1, où 0 représente la valeur alpha la plus basse possible et 1 la valeur la plus élevée possible.</span><span class="sxs-lookup"><span data-stu-id="1b28b-132">This value is clamped to the range 0 through 1, where 0 represents the lowest possible alpha value and 1 the highest possible value.</span></span> <span data-ttu-id="1b28b-133">La référence par défaut est 0.</span><span class="sxs-lookup"><span data-stu-id="1b28b-133">The default reference is 0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1b28b-134">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="1b28b-134">Return value</span></span>

<span data-ttu-id="1b28b-135">Cette fonction ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="1b28b-135">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="1b28b-136">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="1b28b-136">Error codes</span></span>

<span data-ttu-id="1b28b-137">Les codes d’erreur suivants peuvent être récupérés par la fonction [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="1b28b-137">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="1b28b-138">Nom</span><span class="sxs-lookup"><span data-stu-id="1b28b-138">Name</span></span>                                                                                                  | <span data-ttu-id="1b28b-139">Signification</span><span class="sxs-lookup"><span data-stu-id="1b28b-139">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="1b28b-140"><dt>**\_enum GL non valide \_**</dt></span><span class="sxs-lookup"><span data-stu-id="1b28b-140"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="1b28b-141">*Func* n’est pas une valeur acceptée.</span><span class="sxs-lookup"><span data-stu-id="1b28b-141">*func* was not an accepted value.</span></span><br/>                                                                                          |
| <dl> <span data-ttu-id="1b28b-142"><dt>**\_opération non valide du GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="1b28b-142"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="1b28b-143">La fonction a été appelée entre un appel à [**glBegin**](glbegin.md) et l’appel correspondant à [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="1b28b-143">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="1b28b-144">Notes</span><span class="sxs-lookup"><span data-stu-id="1b28b-144">Remarks</span></span>

<span data-ttu-id="1b28b-145">Le test alpha ignore les fragments en fonction du résultat d’une comparaison entre les valeurs alpha des fragments entrants et une valeur de référence constante.</span><span class="sxs-lookup"><span data-stu-id="1b28b-145">The alpha test discards fragments depending on the outcome of a comparison between the incoming fragments' alpha values and a constant reference value.</span></span> <span data-ttu-id="1b28b-146">La fonction **glAlphaFunc** spécifie la référence et la fonction de comparaison.</span><span class="sxs-lookup"><span data-stu-id="1b28b-146">The **glAlphaFunc** function specifies the reference and comparison function.</span></span> <span data-ttu-id="1b28b-147">La comparaison est effectuée uniquement si le test alpha est activé.</span><span class="sxs-lookup"><span data-stu-id="1b28b-147">The comparison is performed only if alpha testing is enabled.</span></span> <span data-ttu-id="1b28b-148">(Pour plus d’informations sur GL \_ \_Test alpha, consultez [**glEnable**](glenable.md).)</span><span class="sxs-lookup"><span data-stu-id="1b28b-148">(For more information on GL\_ALPHA\_TEST, see [**glEnable**](glenable.md).)</span></span>

<span data-ttu-id="1b28b-149">Les paramètres *Func* et *ref* spécifient les conditions dans lesquelles le pixel est dessiné.</span><span class="sxs-lookup"><span data-stu-id="1b28b-149">The *func* and *ref* parameters specify the conditions under which the pixel is drawn.</span></span> <span data-ttu-id="1b28b-150">La valeur alpha entrante est comparée à *ref* à l’aide de la fonction spécifiée par *Func*.</span><span class="sxs-lookup"><span data-stu-id="1b28b-150">The incoming alpha value is compared to *ref* using the function specified by *func*.</span></span> <span data-ttu-id="1b28b-151">Si la comparaison réussit, le fragment entrant est dessiné, conditionnel sur les tests du stencil et de la mémoire tampon de profondeur suivants.</span><span class="sxs-lookup"><span data-stu-id="1b28b-151">If the comparison passes, the incoming fragment is drawn, conditional on subsequent stencil and depth-buffer tests.</span></span> <span data-ttu-id="1b28b-152">Si la comparaison échoue, aucune modification n’est apportée au trame à cet emplacement de pixel.</span><span class="sxs-lookup"><span data-stu-id="1b28b-152">If the comparison fails, no change is made to the framebuffer at that pixel location.</span></span>

<span data-ttu-id="1b28b-153">La fonction **glAlphaFunc** fonctionne sur toutes les écritures de pixels, y compris celles résultant de la conversion d’analyse des points, des lignes, des polygones et des bitmaps, et des opérations de dessin et de copie de pixels.</span><span class="sxs-lookup"><span data-stu-id="1b28b-153">The **glAlphaFunc** function operates on all pixel writes, including those resulting from the scan conversion of points, lines, polygons, and bitmaps, and from pixel draw and copy operations.</span></span> <span data-ttu-id="1b28b-154">La fonction **glAlphaFunc** n’affecte pas les opérations d’effacement de l’écran.</span><span class="sxs-lookup"><span data-stu-id="1b28b-154">The **glAlphaFunc** function does not affect screen clear operations.</span></span>

<span data-ttu-id="1b28b-155">Le test alpha est effectué uniquement en mode RVBA.</span><span class="sxs-lookup"><span data-stu-id="1b28b-155">Alpha testing is done only in RGBA mode.</span></span>

<span data-ttu-id="1b28b-156">Les fonctions suivantes récupèrent les informations relatives à la fonction **glAlphaFunc** :</span><span class="sxs-lookup"><span data-stu-id="1b28b-156">The following functions retrieve information related to the **glAlphaFunc** function:</span></span>

<span data-ttu-id="1b28b-157">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) avec l’argument GL \_ alpha de \_ test \_ Func</span><span class="sxs-lookup"><span data-stu-id="1b28b-157">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_ALPHA\_TEST\_FUNC</span></span>

<span data-ttu-id="1b28b-158">**glGet** avec l’argument GL \_ alpha \_ test \_ Ref</span><span class="sxs-lookup"><span data-stu-id="1b28b-158">**glGet** with argument GL\_ALPHA\_TEST\_REF</span></span>

<span data-ttu-id="1b28b-159">[**glIsEnabled**](glisenabled.md) avec l’argument GL \_ alpha \_ test</span><span class="sxs-lookup"><span data-stu-id="1b28b-159">[**glIsEnabled**](glisenabled.md) with argument GL\_ALPHA\_TEST</span></span>

## <a name="requirements"></a><span data-ttu-id="1b28b-160">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1b28b-160">Requirements</span></span>



| <span data-ttu-id="1b28b-161">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1b28b-161">Requirement</span></span> | <span data-ttu-id="1b28b-162">Valeur</span><span class="sxs-lookup"><span data-stu-id="1b28b-162">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1b28b-163">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1b28b-163">Minimum supported client</span></span><br/> | <span data-ttu-id="1b28b-164">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1b28b-164">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="1b28b-165">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1b28b-165">Minimum supported server</span></span><br/> | <span data-ttu-id="1b28b-166">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1b28b-166">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="1b28b-167">En-tête</span><span class="sxs-lookup"><span data-stu-id="1b28b-167">Header</span></span><br/>                   | <dl> <span data-ttu-id="1b28b-168"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="1b28b-168"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="1b28b-169">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="1b28b-169">Library</span></span><br/>                  | <dl> <span data-ttu-id="1b28b-170"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1b28b-170"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="1b28b-171">DLL</span><span class="sxs-lookup"><span data-stu-id="1b28b-171">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1b28b-172"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1b28b-172"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1b28b-173">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1b28b-173">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1b28b-174">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="1b28b-174">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="1b28b-175">**glBlendFunc**</span><span class="sxs-lookup"><span data-stu-id="1b28b-175">**glBlendFunc**</span></span>](glblendfunc.md)
</dt> <dt>

[<span data-ttu-id="1b28b-176">**glClear**</span><span class="sxs-lookup"><span data-stu-id="1b28b-176">**glClear**</span></span>](glclear.md)
</dt> <dt>

[<span data-ttu-id="1b28b-177">**glDepthFunc**</span><span class="sxs-lookup"><span data-stu-id="1b28b-177">**glDepthFunc**</span></span>](gldepthfunc.md)
</dt> <dt>

[<span data-ttu-id="1b28b-178">**glEnable**</span><span class="sxs-lookup"><span data-stu-id="1b28b-178">**glEnable**</span></span>](glenable.md)
</dt> <dt>

[<span data-ttu-id="1b28b-179">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="1b28b-179">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="1b28b-180">**glGet**</span><span class="sxs-lookup"><span data-stu-id="1b28b-180">**glGet**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[<span data-ttu-id="1b28b-181">**glIsEnabled**</span><span class="sxs-lookup"><span data-stu-id="1b28b-181">**glIsEnabled**</span></span>](glisenabled.md)
</dt> <dt>

[<span data-ttu-id="1b28b-182">**glStencilFunc**</span><span class="sxs-lookup"><span data-stu-id="1b28b-182">**glStencilFunc**</span></span>](glstencilfunc.md)
</dt> </dl>

 

 





