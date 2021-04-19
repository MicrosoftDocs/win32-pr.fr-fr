---
title: fonction glDrawBuffer (GL. h)
description: La fonction glDrawBuffer spécifie les mémoires tampons de couleur à dessiner.
ms.assetid: ea625699-303b-4e60-b9aa-771949a8d52d
keywords:
- glDrawBuffer fonction OpenGL
topic_type:
- apiref
api_name:
- glDrawBuffer
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3a99bd2b184766f1621d89b2c8d642902d300e14
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106510947"
---
# <a name="gldrawbuffer-function"></a><span data-ttu-id="8fb30-104">glDrawBuffer fonction)</span><span class="sxs-lookup"><span data-stu-id="8fb30-104">glDrawBuffer function</span></span>

<span data-ttu-id="8fb30-105">La fonction **glDrawBuffer** spécifie les mémoires tampons de couleur à dessiner.</span><span class="sxs-lookup"><span data-stu-id="8fb30-105">The **glDrawBuffer** function specifies which color buffers are to be drawn into.</span></span>

## <a name="syntax"></a><span data-ttu-id="8fb30-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8fb30-106">Syntax</span></span>


```C++
void WINAPI glDrawBuffer(
   GLenum mode
);
```



## <a name="parameters"></a><span data-ttu-id="8fb30-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8fb30-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8fb30-108">*mode*</span><span class="sxs-lookup"><span data-stu-id="8fb30-108">*mode*</span></span> 
</dt> <dd>

<span data-ttu-id="8fb30-109">Spécifie jusqu’à quatre mémoires tampons de couleur à dessiner avec les constantes symboliques acceptées suivantes.</span><span class="sxs-lookup"><span data-stu-id="8fb30-109">Specifies up to four color buffers to be drawn into with the following acceptable symbolic constants.</span></span>



| <span data-ttu-id="8fb30-110">Valeur</span><span class="sxs-lookup"><span data-stu-id="8fb30-110">Value</span></span>                                                                                                                                                                       | <span data-ttu-id="8fb30-111">Signification</span><span class="sxs-lookup"><span data-stu-id="8fb30-111">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                      |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_NONE"></span><span id="gl_none"></span><dl> <span data-ttu-id="8fb30-112"><dt>**GL \_ aucun**</dt></span><span class="sxs-lookup"><span data-stu-id="8fb30-112"><dt>**GL\_NONE**</dt></span></span> </dl>                                 | <span data-ttu-id="8fb30-113">Aucune mémoire tampon de couleur n’est écrite.</span><span class="sxs-lookup"><span data-stu-id="8fb30-113">No color buffers are written.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                     |
| <span id="GL_FRONT_LEFT"></span><span id="gl_front_left"></span><dl> <span data-ttu-id="8fb30-114"><dt>**GL \_ avant \_ gauche**</dt></span><span class="sxs-lookup"><span data-stu-id="8fb30-114"><dt>**GL\_FRONT\_LEFT**</dt></span></span> </dl>              | <span data-ttu-id="8fb30-115">Seule la mémoire tampon de couleur frontale est écrite.</span><span class="sxs-lookup"><span data-stu-id="8fb30-115">Only the front-left color buffer is written.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                      |
| <span id="GL_FRONT_RIGHT"></span><span id="gl_front_right"></span><dl> <span data-ttu-id="8fb30-116"><dt>**GL \_ avant \_ droit**</dt></span><span class="sxs-lookup"><span data-stu-id="8fb30-116"><dt>**GL\_FRONT\_RIGHT**</dt></span></span> </dl>           | <span data-ttu-id="8fb30-117">Seule la mémoire tampon de couleur frontale est écrite.</span><span class="sxs-lookup"><span data-stu-id="8fb30-117">Only the front-right color buffer is written.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                     |
| <span id="GL_BACK_LEFT"></span><span id="gl_back_left"></span><dl> <span data-ttu-id="8fb30-118"><dt>**en \_ arrière-plan du GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="8fb30-118"><dt>**GL\_BACK\_LEFT**</dt></span></span> </dl>                 | <span data-ttu-id="8fb30-119">Seule la mémoire tampon de couleur de l’arrière-plan est écrite.</span><span class="sxs-lookup"><span data-stu-id="8fb30-119">Only the back-left color buffer is written.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                       |
| <span id="GL_BACK_RIGHT"></span><span id="gl_back_right"></span><dl> <span data-ttu-id="8fb30-120"><dt>**\_arrière-plan du GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="8fb30-120"><dt>**GL\_BACK\_RIGHT**</dt></span></span> </dl>              | <span data-ttu-id="8fb30-121">Seule la mémoire tampon de couleur de l’arrière-plan est écrite.</span><span class="sxs-lookup"><span data-stu-id="8fb30-121">Only the back-right color buffer is written.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                      |
| <span id="GL_FRONT"></span><span id="gl_front"></span><dl> <span data-ttu-id="8fb30-122"><dt>**GL \_ frontal**</dt></span><span class="sxs-lookup"><span data-stu-id="8fb30-122"><dt>**GL\_FRONT**</dt></span></span> </dl>                              | <span data-ttu-id="8fb30-123">Seules les mémoires tampons de couleur frontale et gauche sont écrites.</span><span class="sxs-lookup"><span data-stu-id="8fb30-123">Only the front-left and front-right color buffers are written.</span></span> <span data-ttu-id="8fb30-124">S’il n’existe pas de mémoire tampon de couleur frontale, seule la mémoire tampon de couleur d’avant-plan est écrite.</span><span class="sxs-lookup"><span data-stu-id="8fb30-124">If there is no front-right color buffer, only the front left-color buffer is written.</span></span><br/>                                                                                                                                                                                                                                              |
| <span id="GL_BACK"></span><span id="gl_back"></span><dl> <span data-ttu-id="8fb30-125"><dt>**Back. du GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="8fb30-125"><dt>**GL\_BACK**</dt></span></span> </dl>                                 | <span data-ttu-id="8fb30-126">Seules les mémoires tampons de couleur de l’arrière-plan et de l’arrière-plan sont écrites.</span><span class="sxs-lookup"><span data-stu-id="8fb30-126">Only the back-left and back-right color buffers are written.</span></span> <span data-ttu-id="8fb30-127">S’il n’existe aucune mémoire tampon de couleur d’arrière-plan, seule la mémoire tampon de couleur d’arrière-plan est écrite.</span><span class="sxs-lookup"><span data-stu-id="8fb30-127">If there is no back-right color buffer, only the back-left color buffer is written.</span></span><br/>                                                                                                                                                                                                                                                  |
| <span id="GL_LEFT"></span><span id="gl_left"></span><dl> <span data-ttu-id="8fb30-128"><dt>**GL \_ gauche**</dt></span><span class="sxs-lookup"><span data-stu-id="8fb30-128"><dt>**GL\_LEFT**</dt></span></span> </dl>                                 | <span data-ttu-id="8fb30-129">Seules les mémoires tampons de couleur d’arrière-plan et de gauche sont écrites.</span><span class="sxs-lookup"><span data-stu-id="8fb30-129">Only the front-left and back-left color buffers are written.</span></span> <span data-ttu-id="8fb30-130">S’il n’y a pas de mémoire tampon de couleur de l’arrière-plan, seule la mémoire tampon de couleur de l’avant-gauche est écrite.</span><span class="sxs-lookup"><span data-stu-id="8fb30-130">If there is no back-left color buffer, only the front-left color buffer is written.</span></span><br/>                                                                                                                                                                                                                                                  |
| <span id="GL_RIGHT"></span><span id="gl_right"></span><dl> <span data-ttu-id="8fb30-131"><dt>**\_droit GL**</dt></span><span class="sxs-lookup"><span data-stu-id="8fb30-131"><dt>**GL\_RIGHT**</dt></span></span> </dl>                              | <span data-ttu-id="8fb30-132">Seules les mémoires tampons de couleur d’avant et de droite sont écrites.</span><span class="sxs-lookup"><span data-stu-id="8fb30-132">Only the front-right and back-right color buffers are written.</span></span> <span data-ttu-id="8fb30-133">S’il n’y a pas de mémoire tampon de couleur de l’arrière-plan, seule la mémoire tampon de couleur de l’avant-droite est écrite.</span><span class="sxs-lookup"><span data-stu-id="8fb30-133">If there is no back-right color buffer, only the front-right color buffer is written.</span></span><br/>                                                                                                                                                                                                                                              |
| <span id="GL_FRONT_AND_BACK"></span><span id="gl_front_and_back"></span><dl> <span data-ttu-id="8fb30-134"><dt>**\_recto \_ et \_ Back GL**</dt></span><span class="sxs-lookup"><span data-stu-id="8fb30-134"><dt>**GL\_FRONT\_AND\_BACK**</dt></span></span> </dl> | <span data-ttu-id="8fb30-135">Toutes les mémoires tampons de couleur de premier plan et d’arrière-plan (avant gauche, avant droit, arrière-plan de gauche, arrière-plan) sont écrites.</span><span class="sxs-lookup"><span data-stu-id="8fb30-135">All the front and back color buffers (front-left, front-right, back-left, back-right) are written.</span></span> <span data-ttu-id="8fb30-136">S’il n’existe aucune mémoire tampon de couleur d’arrière-plan, seuls les tampons de couleur avant gauche et avant droit sont écrits.</span><span class="sxs-lookup"><span data-stu-id="8fb30-136">If there are no back color buffers, only the front-left and front-right color buffers are written.</span></span> <span data-ttu-id="8fb30-137">S’il n’y a pas de mémoire tampon de couleur droite, seules les mémoires tampons de couleur d’arrière-plan et de gauche sont écrites.</span><span class="sxs-lookup"><span data-stu-id="8fb30-137">If there are no right color buffers, only the front-left and back-left color buffers are written.</span></span> <span data-ttu-id="8fb30-138">S’il n’existe pas de mémoire tampon de couleur de droite ou d’arrière-plan, seule la mémoire tampon de couleur frontale est écrite.</span><span class="sxs-lookup"><span data-stu-id="8fb30-138">If there are no right or back color buffers, only the front-left color buffer is written.</span></span><br/> |
| <span id="GL_AUXi"></span><span id="gl_auxi"></span><span id="GL_AUXI"></span><dl> <span data-ttu-id="8fb30-139"><dt>**\_Auxi GL**</dt></span><span class="sxs-lookup"><span data-stu-id="8fb30-139"><dt>**GL\_AUXi**</dt></span></span> </dl>       | <span data-ttu-id="8fb30-140">Seule la mémoire tampon de couleur auxiliaire *i* est écrite ; *i* est compris entre 0 et \_ \_ le GL des tampons au-1.</span><span class="sxs-lookup"><span data-stu-id="8fb30-140">Only the auxiliary color buffer *i* is written; *i* is between 0 and GL\_AUX\_BUFFERS - 1.</span></span> <span data-ttu-id="8fb30-141">(GL \_ \_Les mémoires tampons aux ne sont pas la limite supérieure ; utilisez [**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) pour interroger le nombre de tampons auxiliaires disponibles.)</span><span class="sxs-lookup"><span data-stu-id="8fb30-141">(GL\_AUX\_BUFFERS is not the upper limit; use [**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) to query the number of available auxiliary buffers.)</span></span><br/>                                                                                                                            |



 

<span data-ttu-id="8fb30-142">La valeur par défaut est \_ recto GL pour les contextes à une seule mise en mémoire tampon, et le GL est \_ de retour pour les contextes de double mise en mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="8fb30-142">The default value is GL\_FRONT for single-buffered contexts, and GL\_BACK for double-buffered contexts.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8fb30-143">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="8fb30-143">Return value</span></span>

<span data-ttu-id="8fb30-144">Cette fonction ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="8fb30-144">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="8fb30-145">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="8fb30-145">Error codes</span></span>

<span data-ttu-id="8fb30-146">Les codes d’erreur suivants peuvent être récupérés par la fonction [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="8fb30-146">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="8fb30-147">Nom</span><span class="sxs-lookup"><span data-stu-id="8fb30-147">Name</span></span>                                                                                                  | <span data-ttu-id="8fb30-148">Signification</span><span class="sxs-lookup"><span data-stu-id="8fb30-148">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="8fb30-149"><dt>**\_enum GL non valide \_**</dt></span><span class="sxs-lookup"><span data-stu-id="8fb30-149"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="8fb30-150">le *mode* n’était pas une valeur acceptée.</span><span class="sxs-lookup"><span data-stu-id="8fb30-150">*mode* was not an accepted value.</span></span><br/>                                                                                          |
| <dl> <span data-ttu-id="8fb30-151"><dt>**\_opération non valide du GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="8fb30-151"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="8fb30-152">Aucune des mémoires tampons indiquées par le *mode* n’existait.</span><span class="sxs-lookup"><span data-stu-id="8fb30-152">None of the buffers indicated by *mode* existed.</span></span><br/>                                                                           |
| <dl> <span data-ttu-id="8fb30-153"><dt>**\_opération non valide du GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="8fb30-153"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="8fb30-154">La fonction a été appelée entre un appel à [**glBegin**](glbegin.md) et l’appel correspondant à [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="8fb30-154">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |


## <a name="remarks"></a><span data-ttu-id="8fb30-155">Notes</span><span class="sxs-lookup"><span data-stu-id="8fb30-155">Remarks</span></span>

<span data-ttu-id="8fb30-156">Lorsque les couleurs sont écrites dans le trame, elles sont écrites dans les tampons de couleurs spécifiés par **glDrawBuffer**.</span><span class="sxs-lookup"><span data-stu-id="8fb30-156">When colors are written to the framebuffer, they are written into the color buffers specified by **glDrawBuffer**.</span></span>

<span data-ttu-id="8fb30-157">Si plus d’une mémoire tampon de couleur est sélectionnée pour le dessin, les opérations de fusion ou logique sont calculées et appliquées indépendamment pour chaque mémoire tampon de couleur et peuvent produire des résultats différents dans chaque mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="8fb30-157">If more than one color buffer is selected for drawing, then blending or logical operations are computed and applied independently for each color buffer and can produce different results in each buffer.</span></span>

<span data-ttu-id="8fb30-158">Les contextes Monoscopic incluent uniquement les mémoires tampons de gauche, tandis que les contextes stéréoscopiques incluent les mémoires tampons de gauche et de droite.</span><span class="sxs-lookup"><span data-stu-id="8fb30-158">Monoscopic contexts include only left buffers, and stereoscopic contexts include both left and right buffers.</span></span> <span data-ttu-id="8fb30-159">De même, les contextes à une seule mémoire tampon incluent uniquement les mémoires tampons d’arrière-plan, et les contextes de double mise en mémoire tampon incluent les mémoires tampons d’arrière-plan et d’arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="8fb30-159">Likewise, single-buffered contexts include only front buffers, and double-buffered contexts include both front and back buffers.</span></span> <span data-ttu-id="8fb30-160">Le contexte est sélectionné lors de l’initialisation OpenGL.</span><span class="sxs-lookup"><span data-stu-id="8fb30-160">The context is selected at OpenGL initialization.</span></span>

<span data-ttu-id="8fb30-161">C’est toujours le cas pour GL \_ des *i* = GL \_ AUX0 + *i*.</span><span class="sxs-lookup"><span data-stu-id="8fb30-161">It is always the case that GL\_AUX *i* = GL\_AUX0 + *i*.</span></span>

<span data-ttu-id="8fb30-162">Les fonctions suivantes récupèrent les informations relatives à la fonction **glDrawBuffer** :</span><span class="sxs-lookup"><span data-stu-id="8fb30-162">The following functions retrieve information related to the **glDrawBuffer** function:</span></span>

<span data-ttu-id="8fb30-163">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) avec argument \_ mémoire tampon de dessin de la comptabilité \_</span><span class="sxs-lookup"><span data-stu-id="8fb30-163">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_DRAW\_BUFFER</span></span>

<span data-ttu-id="8fb30-164">**glGet** avec argument GL \_ aux \_ tampons</span><span class="sxs-lookup"><span data-stu-id="8fb30-164">**glGet** with argument GL\_AUX\_BUFFERS</span></span>

## <a name="requirements"></a><span data-ttu-id="8fb30-165">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8fb30-165">Requirements</span></span>



| <span data-ttu-id="8fb30-166">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8fb30-166">Requirement</span></span> | <span data-ttu-id="8fb30-167">Valeur</span><span class="sxs-lookup"><span data-stu-id="8fb30-167">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8fb30-168">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8fb30-168">Minimum supported client</span></span><br/> | <span data-ttu-id="8fb30-169">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8fb30-169">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="8fb30-170">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8fb30-170">Minimum supported server</span></span><br/> | <span data-ttu-id="8fb30-171">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8fb30-171">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="8fb30-172">En-tête</span><span class="sxs-lookup"><span data-stu-id="8fb30-172">Header</span></span><br/>                   | <dl> <span data-ttu-id="8fb30-173"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="8fb30-173"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="8fb30-174">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="8fb30-174">Library</span></span><br/>                  | <dl> <span data-ttu-id="8fb30-175"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8fb30-175"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="8fb30-176">DLL</span><span class="sxs-lookup"><span data-stu-id="8fb30-176">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8fb30-177"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8fb30-177"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8fb30-178">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8fb30-178">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8fb30-179">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="8fb30-179">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="8fb30-180">**glBlendFunc**</span><span class="sxs-lookup"><span data-stu-id="8fb30-180">**glBlendFunc**</span></span>](glblendfunc.md)
</dt> <dt>

[<span data-ttu-id="8fb30-181">**glColorMask**</span><span class="sxs-lookup"><span data-stu-id="8fb30-181">**glColorMask**</span></span>](glcolormask.md)
</dt> <dt>

[<span data-ttu-id="8fb30-182">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="8fb30-182">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="8fb30-183">**glGet**</span><span class="sxs-lookup"><span data-stu-id="8fb30-183">**glGet**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[<span data-ttu-id="8fb30-184">**glIndexMask**</span><span class="sxs-lookup"><span data-stu-id="8fb30-184">**glIndexMask**</span></span>](glindexmask.md)
</dt> <dt>

[<span data-ttu-id="8fb30-185">**glLogicOp**</span><span class="sxs-lookup"><span data-stu-id="8fb30-185">**glLogicOp**</span></span>](gllogicop.md)
</dt> <dt>

[<span data-ttu-id="8fb30-186">**glReadBuffer**</span><span class="sxs-lookup"><span data-stu-id="8fb30-186">**glReadBuffer**</span></span>](glreadbuffer.md)
</dt> </dl>

 

 





