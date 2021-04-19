---
title: fonction glStencilOp (GL. h)
description: La fonction glStencilOp définit les actions de test de stencil.
ms.assetid: 16809735-5624-49cf-bfa5-9908d008b234
keywords:
- glStencilOp fonction OpenGL
topic_type:
- apiref
api_name:
- glStencilOp
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8b23162f8606ed68dc90a0cb6debdcc903e0ccd0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106510557"
---
# <a name="glstencilop-function"></a><span data-ttu-id="26828-104">glStencilOp fonction)</span><span class="sxs-lookup"><span data-stu-id="26828-104">glStencilOp function</span></span>

<span data-ttu-id="26828-105">La fonction **glStencilOp** définit les actions de test de stencil.</span><span class="sxs-lookup"><span data-stu-id="26828-105">The **glStencilOp** function sets the stencil test actions.</span></span>

## <a name="syntax"></a><span data-ttu-id="26828-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="26828-106">Syntax</span></span>


```C++
void WINAPI glStencilOp(
   GLenum fail,
   GLenum zfail,
   GLenum zpass
);
```



## <a name="parameters"></a><span data-ttu-id="26828-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="26828-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="26828-108">*incident*</span><span class="sxs-lookup"><span data-stu-id="26828-108">*fail*</span></span> 
</dt> <dd>

<span data-ttu-id="26828-109">Action à effectuer en cas d’échec du test du stencil.</span><span class="sxs-lookup"><span data-stu-id="26828-109">The action to take when the stencil test fails.</span></span> <span data-ttu-id="26828-110">Les six constantes symboliques suivantes sont acceptées.</span><span class="sxs-lookup"><span data-stu-id="26828-110">The following six symbolic constants are accepted.</span></span>



| <span data-ttu-id="26828-111">Valeur</span><span class="sxs-lookup"><span data-stu-id="26828-111">Value</span></span>                                                                                                                                                | <span data-ttu-id="26828-112">Signification</span><span class="sxs-lookup"><span data-stu-id="26828-112">Meaning</span></span>                                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| <span id="GL_KEEP"></span><span id="gl_keep"></span><dl> <span data-ttu-id="26828-113"><dt>**conserver le GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="26828-113"><dt>**GL\_KEEP**</dt></span></span> </dl>          | <span data-ttu-id="26828-114">Conserve la valeur actuelle.</span><span class="sxs-lookup"><span data-stu-id="26828-114">Keeps the current value.</span></span><br/>                                                                         |
| <span id="GL_ZERO"></span><span id="gl_zero"></span><dl> <span data-ttu-id="26828-115"><dt>**\_zéro GL**</dt></span><span class="sxs-lookup"><span data-stu-id="26828-115"><dt>**GL\_ZERO**</dt></span></span> </dl>          | <span data-ttu-id="26828-116">Définit la valeur de la mémoire tampon du stencil sur zéro.</span><span class="sxs-lookup"><span data-stu-id="26828-116">Sets the stencil buffer value to zero.</span></span><br/>                                                           |
| <span id="GL_REPLACE"></span><span id="gl_replace"></span><dl> <span data-ttu-id="26828-117"><dt>**remplacement du GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="26828-117"><dt>**GL\_REPLACE**</dt></span></span> </dl> | <span data-ttu-id="26828-118">Définit la valeur de la mémoire tampon du stencil sur *ref*, comme spécifié par **glStencilFunc**.</span><span class="sxs-lookup"><span data-stu-id="26828-118">Sets the stencil buffer value to *ref*, as specified by **glStencilFunc**.</span></span><br/>                       |
| <span id="GL_INCR"></span><span id="gl_incr"></span><dl> <span data-ttu-id="26828-119"><dt>**incrémental du GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="26828-119"><dt>**GL\_INCR**</dt></span></span> </dl>          | <span data-ttu-id="26828-120">Incrémente la valeur de la mémoire tampon du stencil actuelle.</span><span class="sxs-lookup"><span data-stu-id="26828-120">Increments the current stencil buffer value.</span></span> <span data-ttu-id="26828-121">S’attache à la valeur non signée maximale représentable.</span><span class="sxs-lookup"><span data-stu-id="26828-121">Clamps to the maximum representable unsigned value.</span></span><br/> |
| <span id="GL_DECR"></span><span id="gl_decr"></span><dl> <span data-ttu-id="26828-122"><dt>**\_DECR (GL**</dt></span><span class="sxs-lookup"><span data-stu-id="26828-122"><dt>**GL\_DECR**</dt></span></span> </dl>          | <span data-ttu-id="26828-123">Décrémente la valeur de la mémoire tampon du stencil actuelle.</span><span class="sxs-lookup"><span data-stu-id="26828-123">Decrements the current stencil buffer value.</span></span> <span data-ttu-id="26828-124">La valeur de est ancrée à zéro.</span><span class="sxs-lookup"><span data-stu-id="26828-124">Clamps to zero.</span></span><br/>                                     |
| <span id="GL_INVERT"></span><span id="gl_invert"></span><dl> <span data-ttu-id="26828-125"><dt>**GL \_ inversée**</dt></span><span class="sxs-lookup"><span data-stu-id="26828-125"><dt>**GL\_INVERT**</dt></span></span> </dl>    | <span data-ttu-id="26828-126">L’opération de bits inverse la valeur de la mémoire tampon du stencil actuelle.</span><span class="sxs-lookup"><span data-stu-id="26828-126">Bitwise inverts the current stencil buffer value.</span></span><br/>                                                |



 

</dd> <dt>

<span data-ttu-id="26828-127">*zfail*</span><span class="sxs-lookup"><span data-stu-id="26828-127">*zfail*</span></span> 
</dt> <dd>

<span data-ttu-id="26828-128">Action du stencil lorsque le test du stencil réussit, mais le test de profondeur échoue.</span><span class="sxs-lookup"><span data-stu-id="26828-128">Stencil action when the stencil test passes, but the depth test fails.</span></span> <span data-ttu-id="26828-129">Accepte les mêmes constantes symboliques que *Fail.*</span><span class="sxs-lookup"><span data-stu-id="26828-129">Accepts the same symbolic constants as *fail.*</span></span>

</dd> <dt>

<span data-ttu-id="26828-130">*zpass*</span><span class="sxs-lookup"><span data-stu-id="26828-130">*zpass*</span></span> 
</dt> <dd>

<span data-ttu-id="26828-131">Action de stencil lorsque le test de stencil et le test de profondeur réussissent, ou lorsque le test de stencil réussit et qu’il n’y a pas de mémoire tampon de profondeur ou de test de profondeur n’est pas activé.</span><span class="sxs-lookup"><span data-stu-id="26828-131">Stencil action when both the stencil test and the depth test pass, or when the stencil test passes and either there is no depth buffer or depth testing is not enabled.</span></span> <span data-ttu-id="26828-132">Accepte les mêmes constantes symboliques que *Fail*.</span><span class="sxs-lookup"><span data-stu-id="26828-132">Accepts the same symbolic constants as *fail*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="26828-133">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="26828-133">Return value</span></span>

<span data-ttu-id="26828-134">Cette fonction ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="26828-134">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="26828-135">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="26828-135">Error codes</span></span>

<span data-ttu-id="26828-136">Les codes d’erreur suivants peuvent être récupérés par la fonction [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="26828-136">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="26828-137">Nom</span><span class="sxs-lookup"><span data-stu-id="26828-137">Name</span></span>                                                                                                  | <span data-ttu-id="26828-138">Signification</span><span class="sxs-lookup"><span data-stu-id="26828-138">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="26828-139"><dt>**\_enum GL non valide \_**</dt></span><span class="sxs-lookup"><span data-stu-id="26828-139"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="26828-140">*Fail*, *zfail* ou *ZPass* a une valeur autre que les six valeurs constantes définies.</span><span class="sxs-lookup"><span data-stu-id="26828-140">*fail*, *zfail*, or *zpass* was any value other than the six defined constant values.</span></span><br/>                                      |
| <dl> <span data-ttu-id="26828-141"><dt>**\_opération non valide du GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="26828-141"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="26828-142">La fonction a été appelée entre un appel à [**glBegin**](glbegin.md) et l’appel correspondant à [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="26828-142">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="26828-143">Notes</span><span class="sxs-lookup"><span data-stu-id="26828-143">Remarks</span></span>

<span data-ttu-id="26828-144">Le stencil, tel que la mise en mémoire tampon *z*, permet d’activer et de désactiver le dessin par pixel.</span><span class="sxs-lookup"><span data-stu-id="26828-144">Stenciling, like *z*-buffering, enables and disables drawing on a per-pixel basis.</span></span> <span data-ttu-id="26828-145">Vous dessinez dans les plans de stencil à l’aide de primitives de dessin OpenGL, puis vous affichez la géométrie et les images à l’aide des plans de gabarit pour masquer des parties de l’écran.</span><span class="sxs-lookup"><span data-stu-id="26828-145">You draw into the stencil planes using OpenGL drawing primitives, then render geometry and images, using the stencil planes to mask out portions of the screen.</span></span> <span data-ttu-id="26828-146">Le stencil est généralement utilisé dans les algorithmes de rendu multipasses pour obtenir des effets spéciaux, tels que les décalques, le mode plan et le rendu de géométrie solide constructive.</span><span class="sxs-lookup"><span data-stu-id="26828-146">Stenciling is typically used in multipass rendering algorithms to achieve special effects, such as decals, outlining, and constructive solid geometry rendering.</span></span>

<span data-ttu-id="26828-147">Le test de stencil élimine conditionnellement un pixel en fonction du résultat d’une comparaison entre la valeur dans la mémoire tampon de stencil et une valeur de référence.</span><span class="sxs-lookup"><span data-stu-id="26828-147">The stencil test conditionally eliminates a pixel based on the outcome of a comparison between the value in the stencil buffer and a reference value.</span></span> <span data-ttu-id="26828-148">Le test est activé avec des appels [**glEnable**](glenable.md) et [**glDisable**](gldisable.md) avec l’argument de test de stencil de la comptabilité \_ \_ , et contrôlé avec [**glStencilFunc**](glstencilfunc.md).</span><span class="sxs-lookup"><span data-stu-id="26828-148">The test is enabled with [**glEnable**](glenable.md) and [**glDisable**](gldisable.md) calls with argument GL\_STENCIL\_TEST, and controlled with [**glStencilFunc**](glstencilfunc.md).</span></span>

<span data-ttu-id="26828-149">La fonction **glStencilOp** accepte trois arguments qui indiquent ce qui se passe à la valeur du stencil stocké lorsque le stencil est activé.</span><span class="sxs-lookup"><span data-stu-id="26828-149">The **glStencilOp** function takes three arguments that indicate what happens to the stored stencil value while stenciling is enabled.</span></span> <span data-ttu-id="26828-150">Si le test du stencil échoue, aucune modification n’est apportée aux mémoires tampons de couleur ou de profondeur du pixel et l' *échec* spécifie ce qui se passe au contenu de la mémoire tampon du stencil.</span><span class="sxs-lookup"><span data-stu-id="26828-150">If the stencil test fails, no change is made to the pixel's color or depth buffers, and *fail* specifies what happens to the stencil buffer contents.</span></span>

<span data-ttu-id="26828-151">Les valeurs de mémoire tampon de stencil sont traitées comme des entiers non signés.</span><span class="sxs-lookup"><span data-stu-id="26828-151">Stencil buffer values are treated as unsigned integers.</span></span> <span data-ttu-id="26828-152">En cas de incrémentation et de décrémentation, les valeurs sont ancrées à 0 et 2 *n* 1, où *n* est la valeur retournée par l’interrogation des bits du stencil du GL \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="26828-152">When incremented and decremented, values are clamped to 0 and 2 *n* 1, where *n* is the value returned by querying GL\_STENCIL\_BITS.</span></span>

<span data-ttu-id="26828-153">Les deux autres arguments de **glStencilOp** spécifient des actions de tampon de stencil qui réussissent (*ZPass*) ou échouent (*zfail*).</span><span class="sxs-lookup"><span data-stu-id="26828-153">The other two arguments to **glStencilOp** specify stencil buffer actions should subsequent depth buffer tests succeed (*zpass*) or fail (*zfail*).</span></span> <span data-ttu-id="26828-154">(Voir [**glDepthFunc**](gldepthfunc.md).) Elles sont spécifiées à l’aide des six mêmes constantes symboliques que *Fail*.</span><span class="sxs-lookup"><span data-stu-id="26828-154">(See [**glDepthFunc**](gldepthfunc.md).) They are specified using the same six symbolic constants as *fail*.</span></span> <span data-ttu-id="26828-155">Notez que *zfail* est ignoré lorsqu’il n’y a pas de mémoire tampon de profondeur, ou lorsque la mémoire tampon de profondeur n’est pas activée.</span><span class="sxs-lookup"><span data-stu-id="26828-155">Note that *zfail* is ignored when there is no depth buffer, or when the depth buffer is not enabled.</span></span> <span data-ttu-id="26828-156">Dans ces cas, *Fail* et *ZPass* spécifient l’action du stencil lorsque le test du stencil échoue et passe, respectivement.</span><span class="sxs-lookup"><span data-stu-id="26828-156">In these cases, *fail* and *zpass* specify stencil action when the stencil test fails and passes, respectively.</span></span>

<span data-ttu-id="26828-157">Initialement, le test stencil est désactivé.</span><span class="sxs-lookup"><span data-stu-id="26828-157">Initially the stencil test is disabled.</span></span> <span data-ttu-id="26828-158">S’il n’existe pas de mémoire tampon de stencil, aucune modification de stencil ne peut se produire et c’est comme si les tests de stencil réussissent toujours, quel que soit l’appel à **glStencilOp**.</span><span class="sxs-lookup"><span data-stu-id="26828-158">If there is no stencil buffer, no stencil modification can occur and it is as if the stencil tests always pass, regardless of any call to **glStencilOp**.</span></span>

<span data-ttu-id="26828-159">Les fonctions suivantes récupèrent les informations relatives à **glStencilOp**:</span><span class="sxs-lookup"><span data-stu-id="26828-159">The following functions retrieve information related to **glStencilOp**:</span></span>

<span data-ttu-id="26828-160">échec de [**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) avec l’argument du stencil du GL \_ \_</span><span class="sxs-lookup"><span data-stu-id="26828-160">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_STENCIL\_FAIL</span></span>

<span data-ttu-id="26828-161">**glGet** avec argument de la passe de \_ \_ profondeur passe-passe de stencil \_ \_</span><span class="sxs-lookup"><span data-stu-id="26828-161">**glGet** with argument GL\_STENCIL\_PASS\_DEPTH\_PASS</span></span>

<span data-ttu-id="26828-162"> échec de la \_ profondeur de \_ réussite du stencil \_ de glGet avec argument GL \_</span><span class="sxs-lookup"><span data-stu-id="26828-162">**glGet** with argument GL\_STENCIL\_PASS\_DEPTH\_FAIL</span></span>

<span data-ttu-id="26828-163">**glGet** avec arguments de stencil de la comptabilité GL \_ \_</span><span class="sxs-lookup"><span data-stu-id="26828-163">**glGet** with argument GL\_STENCIL\_BITS</span></span>

<span data-ttu-id="26828-164">[**glIsEnabled**](glisenabled.md) avec l’argument \_ test de stencil du GL \_</span><span class="sxs-lookup"><span data-stu-id="26828-164">[**glIsEnabled**](glisenabled.md) with argument GL\_STENCIL\_TEST</span></span>

## <a name="requirements"></a><span data-ttu-id="26828-165">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="26828-165">Requirements</span></span>



| <span data-ttu-id="26828-166">Condition requise</span><span class="sxs-lookup"><span data-stu-id="26828-166">Requirement</span></span> | <span data-ttu-id="26828-167">Valeur</span><span class="sxs-lookup"><span data-stu-id="26828-167">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="26828-168">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="26828-168">Minimum supported client</span></span><br/> | <span data-ttu-id="26828-169">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="26828-169">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="26828-170">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="26828-170">Minimum supported server</span></span><br/> | <span data-ttu-id="26828-171">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="26828-171">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="26828-172">En-tête</span><span class="sxs-lookup"><span data-stu-id="26828-172">Header</span></span><br/>                   | <dl> <span data-ttu-id="26828-173"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="26828-173"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="26828-174">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="26828-174">Library</span></span><br/>                  | <dl> <span data-ttu-id="26828-175"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="26828-175"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="26828-176">DLL</span><span class="sxs-lookup"><span data-stu-id="26828-176">DLL</span></span><br/>                      | <dl> <span data-ttu-id="26828-177"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="26828-177"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="26828-178">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="26828-178">See also</span></span>

<dl> <dt>

[<span data-ttu-id="26828-179">**glAlphaFunc**</span><span class="sxs-lookup"><span data-stu-id="26828-179">**glAlphaFunc**</span></span>](glalphafunc.md)
</dt> <dt>

[<span data-ttu-id="26828-180">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="26828-180">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="26828-181">**glBlendFunc**</span><span class="sxs-lookup"><span data-stu-id="26828-181">**glBlendFunc**</span></span>](glblendfunc.md)
</dt> <dt>

[<span data-ttu-id="26828-182">**glDepthFunc**</span><span class="sxs-lookup"><span data-stu-id="26828-182">**glDepthFunc**</span></span>](gldepthfunc.md)
</dt> <dt>

[<span data-ttu-id="26828-183">**glEnable**</span><span class="sxs-lookup"><span data-stu-id="26828-183">**glEnable**</span></span>](glenable.md)
</dt> <dt>

[<span data-ttu-id="26828-184">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="26828-184">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="26828-185">**glIsEnabled**</span><span class="sxs-lookup"><span data-stu-id="26828-185">**glIsEnabled**</span></span>](glisenabled.md)
</dt> <dt>

[<span data-ttu-id="26828-186">**glLogicOp**</span><span class="sxs-lookup"><span data-stu-id="26828-186">**glLogicOp**</span></span>](gllogicop.md)
</dt> <dt>

[<span data-ttu-id="26828-187">**glStencilFunc**</span><span class="sxs-lookup"><span data-stu-id="26828-187">**glStencilFunc**</span></span>](glstencilfunc.md)
</dt> </dl>

 

 





