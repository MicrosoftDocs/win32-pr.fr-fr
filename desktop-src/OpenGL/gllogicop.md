---
title: fonction glLogicOp (GL. h)
description: La fonction glLogicOp spécifie une opération de pixel logique pour le rendu de l’index des couleurs.
ms.assetid: 29edf9bd-f3b8-4de7-9afb-07714f4efd92
keywords:
- glLogicOp fonction OpenGL
topic_type:
- apiref
api_name:
- glLogicOp
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eb29e8f845e99f6d3c988dfd0c0201de129bee69
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104519153"
---
# <a name="gllogicop-function"></a><span data-ttu-id="dad67-104">glLogicOp fonction)</span><span class="sxs-lookup"><span data-stu-id="dad67-104">glLogicOp function</span></span>

<span data-ttu-id="dad67-105">La fonction **glLogicOp** spécifie une opération de pixel logique pour le rendu de l’index des couleurs.</span><span class="sxs-lookup"><span data-stu-id="dad67-105">The **glLogicOp** function specifies a logical pixel operation for color index rendering.</span></span>

## <a name="syntax"></a><span data-ttu-id="dad67-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="dad67-106">Syntax</span></span>


```C++
void WINAPI glLogicOp(
   GLenum opcode
);
```



## <a name="parameters"></a><span data-ttu-id="dad67-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="dad67-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dad67-108">*OpCode*</span><span class="sxs-lookup"><span data-stu-id="dad67-108">*opcode*</span></span> 
</dt> <dd>

<span data-ttu-id="dad67-109">Constante symbolique qui sélectionne une opération logique.</span><span class="sxs-lookup"><span data-stu-id="dad67-109">A symbolic constant that selects a logical operation.</span></span> <span data-ttu-id="dad67-110">Les symboles suivants sont acceptés où s est égal à la valeur du bit source et d correspond à la valeur du bit de destination.</span><span class="sxs-lookup"><span data-stu-id="dad67-110">The following symbols are accepted where s equals the value of the source bit and d is the value of the destination bit.</span></span>



| <span data-ttu-id="dad67-111">Valeur</span><span class="sxs-lookup"><span data-stu-id="dad67-111">Value</span></span>                                                                                                                                                                   | <span data-ttu-id="dad67-112">Signification</span><span class="sxs-lookup"><span data-stu-id="dad67-112">Meaning</span></span>              |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------|
| <span id="GL_CLEAR"></span><span id="gl_clear"></span><dl> <span data-ttu-id="dad67-113"><dt>**\_effacement GL**</dt></span><span class="sxs-lookup"><span data-stu-id="dad67-113"><dt>**GL\_CLEAR**</dt></span></span> </dl>                          | <span data-ttu-id="dad67-114">0</span><span class="sxs-lookup"><span data-stu-id="dad67-114">0</span></span><br/>         |
| <span id="GL_SET"></span><span id="gl_set"></span><dl> <span data-ttu-id="dad67-115"><dt>**\_ensemble GL**</dt></span><span class="sxs-lookup"><span data-stu-id="dad67-115"><dt>**GL\_SET**</dt></span></span> </dl>                                | <span data-ttu-id="dad67-116">1</span><span class="sxs-lookup"><span data-stu-id="dad67-116">1</span></span><br/>         |
| <span id="GL_COPY"></span><span id="gl_copy"></span><dl> <span data-ttu-id="dad67-117"><dt>**\_copie GL**</dt></span><span class="sxs-lookup"><span data-stu-id="dad67-117"><dt>**GL\_COPY**</dt></span></span> </dl>                             | <span data-ttu-id="dad67-118">s</span><span class="sxs-lookup"><span data-stu-id="dad67-118">s</span></span><br/>         |
| <span id="GL_COPY_INVERTED"></span><span id="gl_copy_inverted"></span><dl> <span data-ttu-id="dad67-119"><dt>**\_copie GL \_ inversée**</dt></span><span class="sxs-lookup"><span data-stu-id="dad67-119"><dt>**GL\_COPY\_INVERTED**</dt></span></span> </dl> | <span data-ttu-id="dad67-120">! s</span><span class="sxs-lookup"><span data-stu-id="dad67-120">!s</span></span><br/>        |
| <span id="GL_NOOP"></span><span id="gl_noop"></span><dl> <span data-ttu-id="dad67-121"><dt>**GL \_ NOOP**</dt></span><span class="sxs-lookup"><span data-stu-id="dad67-121"><dt>**GL\_NOOP**</dt></span></span> </dl>                             | <span data-ttu-id="dad67-122">d</span><span class="sxs-lookup"><span data-stu-id="dad67-122">d</span></span><br/>         |
| <span id="GL_INVERT"></span><span id="gl_invert"></span><dl> <span data-ttu-id="dad67-123"><dt>**GL \_ inversée**</dt></span><span class="sxs-lookup"><span data-stu-id="dad67-123"><dt>**GL\_INVERT**</dt></span></span> </dl>                       | <span data-ttu-id="dad67-124">! d</span><span class="sxs-lookup"><span data-stu-id="dad67-124">!d</span></span><br/>        |
| <span id="GL_AND"></span><span id="gl_and"></span><dl> <span data-ttu-id="dad67-125"><dt>**GL \_ et**</dt></span><span class="sxs-lookup"><span data-stu-id="dad67-125"><dt>**GL\_AND**</dt></span></span> </dl>                                | <span data-ttu-id="dad67-126">s & d</span><span class="sxs-lookup"><span data-stu-id="dad67-126">s & d</span></span><br/>     |
| <span id="GL_NAND"></span><span id="gl_nand"></span><dl> <span data-ttu-id="dad67-127"><dt>**GL \_ NAND**</dt></span><span class="sxs-lookup"><span data-stu-id="dad67-127"><dt>**GL\_NAND**</dt></span></span> </dl>                             | <span data-ttu-id="dad67-128">! (s & d)</span><span class="sxs-lookup"><span data-stu-id="dad67-128">!(s & d)</span></span><br/>  |
| <span id="GL_OR"></span><span id="gl_or"></span><dl> <span data-ttu-id="dad67-129"><dt>**GL \_ ou**</dt></span><span class="sxs-lookup"><span data-stu-id="dad67-129"><dt>**GL\_OR**</dt></span></span> </dl>                                   | <span data-ttu-id="dad67-130">s \| d</span><span class="sxs-lookup"><span data-stu-id="dad67-130">s \| d</span></span><br/>    |
| <span id="GL_NOR"></span><span id="gl_nor"></span><dl> <span data-ttu-id="dad67-131"><dt>**GL \_ ou**</dt></span><span class="sxs-lookup"><span data-stu-id="dad67-131"><dt>**GL\_NOR**</dt></span></span> </dl>                                | <span data-ttu-id="dad67-132">! (s \| d)</span><span class="sxs-lookup"><span data-stu-id="dad67-132">!(s \| d)</span></span><br/> |
| <span id="GL_XOR"></span><span id="gl_xor"></span><dl> <span data-ttu-id="dad67-133"><dt>**GL \_ Xor**</dt></span><span class="sxs-lookup"><span data-stu-id="dad67-133"><dt>**GL\_XOR**</dt></span></span> </dl>                                | <span data-ttu-id="dad67-134">s ^ d</span><span class="sxs-lookup"><span data-stu-id="dad67-134">s ^ d</span></span><br/>     |
| <span id="GL_EQUIV"></span><span id="gl_equiv"></span><dl> <span data-ttu-id="dad67-135"><dt>**GL \_ EQUIV**</dt></span><span class="sxs-lookup"><span data-stu-id="dad67-135"><dt>**GL\_EQUIV**</dt></span></span> </dl>                          | <span data-ttu-id="dad67-136">! (s ^ d)</span><span class="sxs-lookup"><span data-stu-id="dad67-136">!(s ^ d)</span></span><br/>  |
| <span id="GL_AND_REVERSE"></span><span id="gl_and_reverse"></span><dl> <span data-ttu-id="dad67-137"><dt>**GL \_ et \_ inverse**</dt></span><span class="sxs-lookup"><span data-stu-id="dad67-137"><dt>**GL\_AND\_REVERSE**</dt></span></span> </dl>       | <span data-ttu-id="dad67-138">s & ! d</span><span class="sxs-lookup"><span data-stu-id="dad67-138">s & !d</span></span><br/>    |
| <span id="GL_AND_INVERTED"></span><span id="gl_and_inverted"></span><dl> <span data-ttu-id="dad67-139"><dt>**GL \_ et \_ inversé**</dt></span><span class="sxs-lookup"><span data-stu-id="dad67-139"><dt>**GL\_AND\_INVERTED**</dt></span></span> </dl>    | <span data-ttu-id="dad67-140">! s & d</span><span class="sxs-lookup"><span data-stu-id="dad67-140">!s & d</span></span><br/>    |
| <span id="GL_OR_REVERSE"></span><span id="gl_or_reverse"></span><dl> <span data-ttu-id="dad67-141"><dt>**GL \_ ou \_ inverse**</dt></span><span class="sxs-lookup"><span data-stu-id="dad67-141"><dt>**GL\_OR\_REVERSE**</dt></span></span> </dl>          | <span data-ttu-id="dad67-142">s \| ! d</span><span class="sxs-lookup"><span data-stu-id="dad67-142">s \| !d</span></span><br/>   |
| <span id="GL_OR_INVERTED"></span><span id="gl_or_inverted"></span><dl> <span data-ttu-id="dad67-143"><dt>**GL \_ ou \_ inversé**</dt></span><span class="sxs-lookup"><span data-stu-id="dad67-143"><dt>**GL\_OR\_INVERTED**</dt></span></span> </dl>       | <span data-ttu-id="dad67-144">! s \| d</span><span class="sxs-lookup"><span data-stu-id="dad67-144">!s \| d</span></span><br/>   |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dad67-145">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="dad67-145">Return value</span></span>

<span data-ttu-id="dad67-146">Cette fonction ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="dad67-146">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="dad67-147">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="dad67-147">Error codes</span></span>

<span data-ttu-id="dad67-148">Les codes d’erreur suivants peuvent être récupérés par la fonction [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="dad67-148">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="dad67-149">Nom</span><span class="sxs-lookup"><span data-stu-id="dad67-149">Name</span></span>                                                                                                  | <span data-ttu-id="dad67-150">Signification</span><span class="sxs-lookup"><span data-stu-id="dad67-150">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="dad67-151"><dt>**\_enum GL non valide \_**</dt></span><span class="sxs-lookup"><span data-stu-id="dad67-151"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="dad67-152">l' *opcode* n’était pas une valeur acceptée.</span><span class="sxs-lookup"><span data-stu-id="dad67-152">*opcode* was not an accepted value.</span></span><br/>                                                                                        |
| <dl> <span data-ttu-id="dad67-153"><dt>**\_opération non valide du GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="dad67-153"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="dad67-154">La fonction a été appelée entre un appel à [**glBegin**](glbegin.md) et l’appel correspondant à [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="dad67-154">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="dad67-155">Notes</span><span class="sxs-lookup"><span data-stu-id="dad67-155">Remarks</span></span>

<span data-ttu-id="dad67-156">La fonction **glLogicOp** spécifie une opération logique qui, lorsqu’elle est activée, est appliquée entre l’index de couleur entrant et l’index de couleur à l’emplacement correspondant dans le trame.</span><span class="sxs-lookup"><span data-stu-id="dad67-156">The **glLogicOp** function specifies a logical operation that, when enabled, is applied between the incoming color index and the color index at the corresponding location in the framebuffer.</span></span> <span data-ttu-id="dad67-157">L’opération logique est activée ou désactivée avec [**glEnable**](glenable.md) et **glDisable** à l’aide de la constante symbolique GL \_ Logic \_ op.</span><span class="sxs-lookup"><span data-stu-id="dad67-157">The logical operation is enabled or disabled with [**glEnable**](glenable.md) and **glDisable** using the symbolic constant GL\_LOGIC\_OP.</span></span>

<span data-ttu-id="dad67-158">Le paramètre *opcode* est une constante symbolique choisie dans la liste ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="dad67-158">The *opcode* parameter is a symbolic constant chosen from the list below.</span></span> <span data-ttu-id="dad67-159">Dans l’explication des opérations logiques, *s* représente l’index de couleur entrant et *d* représente l’index dans le trame.</span><span class="sxs-lookup"><span data-stu-id="dad67-159">In the explanation of the logical operations, *s* represents the incoming color index and *d* represents the index in the framebuffer.</span></span> <span data-ttu-id="dad67-160">Les opérateurs langage C standard sont utilisés.</span><span class="sxs-lookup"><span data-stu-id="dad67-160">Standard C-language operators are used.</span></span> <span data-ttu-id="dad67-161">Comme ces opérateurs de bits suggèrent, l’opération logique est appliquée indépendamment à chaque paire de bits des index source et de destination.</span><span class="sxs-lookup"><span data-stu-id="dad67-161">As these bitwise operators suggest, the logical operation is applied independently to each bit pair of the source and destination indexes.</span></span>

<span data-ttu-id="dad67-162">Les opérations de pixels logiques ne sont pas appliquées aux tampons de couleurs RVBA.</span><span class="sxs-lookup"><span data-stu-id="dad67-162">Logical pixel operations are not applied to RGBA color buffers.</span></span>

<span data-ttu-id="dad67-163">Lorsque plusieurs mémoires tampons d’index de couleurs sont activées pour le dessin, les opérations logiques sont effectuées séparément pour chaque mémoire tampon activée, en utilisant le contenu de cette mémoire tampon pour l’index de destination (voir [**glDrawBuffer**](gldrawbuffer.md)).</span><span class="sxs-lookup"><span data-stu-id="dad67-163">When more than one color-index buffer is enabled for drawing, logical operations are done separately for each enabled buffer, using the contents of that buffer for the destination index (see [**glDrawBuffer**](gldrawbuffer.md)).</span></span>

<span data-ttu-id="dad67-164">Le paramètre *opcode* doit être l’une des 16 valeurs acceptées.</span><span class="sxs-lookup"><span data-stu-id="dad67-164">The *opcode* parameter must be one of the 16 accepted values.</span></span> <span data-ttu-id="dad67-165">Les autres valeurs génèrent une erreur.</span><span class="sxs-lookup"><span data-stu-id="dad67-165">Other values result in an error.</span></span>

<span data-ttu-id="dad67-166">Les fonctions suivantes récupèrent les informations relatives à **glLogicOp**:</span><span class="sxs-lookup"><span data-stu-id="dad67-166">The following functions retrieve information related to **glLogicOp**:</span></span>

<span data-ttu-id="dad67-167">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) avec argument GL \_ logique \_ op \_ mode</span><span class="sxs-lookup"><span data-stu-id="dad67-167">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_LOGIC\_OP\_MODE</span></span>

<span data-ttu-id="dad67-168">[**glIsEnabled**](glisenabled.md) avec argument GL \_ Logic \_ op</span><span class="sxs-lookup"><span data-stu-id="dad67-168">[**glIsEnabled**](glisenabled.md) with argument GL\_LOGIC\_OP</span></span>

## <a name="requirements"></a><span data-ttu-id="dad67-169">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="dad67-169">Requirements</span></span>



| <span data-ttu-id="dad67-170">Condition requise</span><span class="sxs-lookup"><span data-stu-id="dad67-170">Requirement</span></span> | <span data-ttu-id="dad67-171">Valeur</span><span class="sxs-lookup"><span data-stu-id="dad67-171">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="dad67-172">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="dad67-172">Minimum supported client</span></span><br/> | <span data-ttu-id="dad67-173">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="dad67-173">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="dad67-174">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="dad67-174">Minimum supported server</span></span><br/> | <span data-ttu-id="dad67-175">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="dad67-175">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="dad67-176">En-tête</span><span class="sxs-lookup"><span data-stu-id="dad67-176">Header</span></span><br/>                   | <dl> <span data-ttu-id="dad67-177"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="dad67-177"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="dad67-178">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="dad67-178">Library</span></span><br/>                  | <dl> <span data-ttu-id="dad67-179"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="dad67-179"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="dad67-180">DLL</span><span class="sxs-lookup"><span data-stu-id="dad67-180">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dad67-181"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dad67-181"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dad67-182">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="dad67-182">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dad67-183">**glAlphaFunc**</span><span class="sxs-lookup"><span data-stu-id="dad67-183">**glAlphaFunc**</span></span>](glalphafunc.md)
</dt> <dt>

[<span data-ttu-id="dad67-184">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="dad67-184">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="dad67-185">**glBlendFunc**</span><span class="sxs-lookup"><span data-stu-id="dad67-185">**glBlendFunc**</span></span>](glblendfunc.md)
</dt> <dt>

[<span data-ttu-id="dad67-186">**glDrawBuffer**</span><span class="sxs-lookup"><span data-stu-id="dad67-186">**glDrawBuffer**</span></span>](gldrawbuffer.md)
</dt> <dt>

[<span data-ttu-id="dad67-187">**glEnable**</span><span class="sxs-lookup"><span data-stu-id="dad67-187">**glEnable**</span></span>](glenable.md)
</dt> <dt>

[<span data-ttu-id="dad67-188">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="dad67-188">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="dad67-189">**glIsEnabled**</span><span class="sxs-lookup"><span data-stu-id="dad67-189">**glIsEnabled**</span></span>](glisenabled.md)
</dt> <dt>

[<span data-ttu-id="dad67-190">**glStencilOp**</span><span class="sxs-lookup"><span data-stu-id="dad67-190">**glStencilOp**</span></span>](glstencilop.md)
</dt> </dl>

 

 





