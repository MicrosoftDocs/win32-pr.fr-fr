---
title: fonction glRenderMode (GL. h)
description: La fonction glRenderMode définit le mode de pixellisation.
ms.assetid: bcbc3bba-c552-425b-8284-6cadff0c9f56
keywords:
- glRenderMode fonction OpenGL
topic_type:
- apiref
api_name:
- glRenderMode
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: af07d2492d70f9c0a3a764d767b52b2f71204939
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106198"
---
# <a name="glrendermode-function"></a><span data-ttu-id="34c7b-104">glRenderMode fonction)</span><span class="sxs-lookup"><span data-stu-id="34c7b-104">glRenderMode function</span></span>

<span data-ttu-id="34c7b-105">La fonction **glRenderMode** définit le mode de pixellisation.</span><span class="sxs-lookup"><span data-stu-id="34c7b-105">The **glRenderMode** function sets the rasterization mode.</span></span>

## <a name="syntax"></a><span data-ttu-id="34c7b-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="34c7b-106">Syntax</span></span>


```C++
GLint WINAPI glRenderMode(
   GLenum mode
);
```



## <a name="parameters"></a><span data-ttu-id="34c7b-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="34c7b-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="34c7b-108">*mode*</span><span class="sxs-lookup"><span data-stu-id="34c7b-108">*mode*</span></span> 
</dt> <dd>

<span data-ttu-id="34c7b-109">Mode de pixellisation.</span><span class="sxs-lookup"><span data-stu-id="34c7b-109">The rasterization mode.</span></span> <span data-ttu-id="34c7b-110">Les trois valeurs suivantes sont acceptées.</span><span class="sxs-lookup"><span data-stu-id="34c7b-110">The following three values are accepted.</span></span> <span data-ttu-id="34c7b-111">La valeur par défaut est GL \_ Render.</span><span class="sxs-lookup"><span data-stu-id="34c7b-111">The default value is GL\_RENDER.</span></span>



| <span data-ttu-id="34c7b-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="34c7b-112">Value</span></span>                                                                                                                                                   | <span data-ttu-id="34c7b-113">Signification</span><span class="sxs-lookup"><span data-stu-id="34c7b-113">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_RENDER"></span><span id="gl_render"></span><dl> <span data-ttu-id="34c7b-114"><dt>**\_rendu GL**</dt></span><span class="sxs-lookup"><span data-stu-id="34c7b-114"><dt>**GL\_RENDER**</dt></span></span> </dl>       | <span data-ttu-id="34c7b-115">Mode de rendu.</span><span class="sxs-lookup"><span data-stu-id="34c7b-115">Render mode.</span></span> <span data-ttu-id="34c7b-116">Les primitives sont pixellisées, produisant des fragments de pixels, qui sont écrites dans le trame.</span><span class="sxs-lookup"><span data-stu-id="34c7b-116">Primitives are rasterized, producing pixel fragments, which are written into the framebuffer.</span></span> <span data-ttu-id="34c7b-117">Il s’agit du mode normal et du mode par défaut.</span><span class="sxs-lookup"><span data-stu-id="34c7b-117">This is the normal mode and also the default mode.</span></span><br/>                                                                                                                                                                                                      |
| <span id="GL_SELECT"></span><span id="gl_select"></span><dl> <span data-ttu-id="34c7b-118"><dt>**sélection du GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="34c7b-118"><dt>**GL\_SELECT**</dt></span></span> </dl>       | <span data-ttu-id="34c7b-119">Mode de sélection.</span><span class="sxs-lookup"><span data-stu-id="34c7b-119">Selection mode.</span></span> <span data-ttu-id="34c7b-120">Aucun fragment de pixel n’est produit, et aucune modification du contenu du trame n’est effectuée.</span><span class="sxs-lookup"><span data-stu-id="34c7b-120">No pixel fragments are produced, and no change to the framebuffer contents is made.</span></span> <span data-ttu-id="34c7b-121">Au lieu de cela, un enregistrement des noms des primitives qui auraient été dessinées si le mode de rendu était le \_ rendu GL est retourné dans une mémoire tampon Select, qui doit être créée (voir [**glSelectBuffer**](glselectbuffer.md)) avant que le mode de sélection soit entré.</span><span class="sxs-lookup"><span data-stu-id="34c7b-121">Instead, a record of the names of primitives that would have been drawn if the render mode was GL\_RENDER is returned in a select buffer, which must be created (see [**glSelectBuffer**](glselectbuffer.md)) before selection mode is entered.</span></span><br/>               |
| <span id="GL_FEEDBACK"></span><span id="gl_feedback"></span><dl> <span data-ttu-id="34c7b-122"><dt>**Commentaires sur le GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="34c7b-122"><dt>**GL\_FEEDBACK**</dt></span></span> </dl> | <span data-ttu-id="34c7b-123">Mode commentaires.</span><span class="sxs-lookup"><span data-stu-id="34c7b-123">Feedback mode.</span></span> <span data-ttu-id="34c7b-124">Aucun fragment de pixel n’est produit, et aucune modification du contenu du trame n’est effectuée.</span><span class="sxs-lookup"><span data-stu-id="34c7b-124">No pixel fragments are produced, and no change to the framebuffer contents is made.</span></span> <span data-ttu-id="34c7b-125">Au lieu de cela, les coordonnées et les attributs des vertex qui auraient été dessinés avaient le mode de rendu « GL \_ Render » est retourné dans une mémoire tampon de commentaires, qui doit être créée (voir [**glFeedbackBuffer**](glfeedbackbuffer.md)) avant d’entrer en mode commentaires.</span><span class="sxs-lookup"><span data-stu-id="34c7b-125">Instead, the coordinates and attributes of vertices that would have been drawn had the render mode been GL\_RENDER are returned in a feedback buffer, which must be created (see [**glFeedbackBuffer**](glfeedbackbuffer.md)) before feedback mode is entered.</span></span><br/> |



 

</dd> </dl>

## <a name="error-codes"></a><span data-ttu-id="34c7b-126">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="34c7b-126">Error codes</span></span>

<span data-ttu-id="34c7b-127">Les codes d’erreur suivants peuvent être récupérés par la fonction [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="34c7b-127">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="34c7b-128">Nom</span><span class="sxs-lookup"><span data-stu-id="34c7b-128">Name</span></span>                                                                                                  | <span data-ttu-id="34c7b-129">Signification</span><span class="sxs-lookup"><span data-stu-id="34c7b-129">Meaning</span></span>                                                                                                                                     |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="34c7b-130"><dt>**\_enum GL non valide \_**</dt></span><span class="sxs-lookup"><span data-stu-id="34c7b-130"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="34c7b-131">le *mode* ne faisait pas partie des trois valeurs acceptées.</span><span class="sxs-lookup"><span data-stu-id="34c7b-131">*mode* was not one of three accepted values.</span></span><br/>                                                                                     |
| <dl> <span data-ttu-id="34c7b-132"><dt>**\_opération non valide du GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="34c7b-132"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="34c7b-133">La fonction a été appelée avec l’argument GL \_ Select avant que [**glSelectBuffer**](glselectbuffer.md) ne soit appelé au moins une fois.</span><span class="sxs-lookup"><span data-stu-id="34c7b-133">The function was called with argument GL\_SELECT before [**glSelectBuffer**](glselectbuffer.md) was called at least once.</span></span><br/>       |
| <dl> <span data-ttu-id="34c7b-134"><dt>**\_opération non valide du GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="34c7b-134"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="34c7b-135">La fonction a été appelée avec l’argument \_ Feedback GL avant que [**glBeedbackBuffer**](glfeedbackbuffer.md) ne soit appelé au moins une fois.</span><span class="sxs-lookup"><span data-stu-id="34c7b-135">The function was called with argument GL\_FEEDBACK before [**glBeedbackBuffer**](glfeedbackbuffer.md) was called at least once.</span></span><br/> |
| <dl> <span data-ttu-id="34c7b-136"><dt>**\_opération non valide du GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="34c7b-136"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="34c7b-137">La fonction a été appelée entre un appel à [**glBegin**](glbegin.md) et l’appel correspondant à [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="34c7b-137">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/>       |



## <a name="remarks"></a><span data-ttu-id="34c7b-138">Notes</span><span class="sxs-lookup"><span data-stu-id="34c7b-138">Remarks</span></span>

<span data-ttu-id="34c7b-139">La fonction **glRenderMode** prend un argument, *mode*, qui peut prendre l’une des trois valeurs prédéfinies ci-dessus.</span><span class="sxs-lookup"><span data-stu-id="34c7b-139">The **glRenderMode** function takes one argument, *mode*, which can assume one of three predefined values above.</span></span>

<span data-ttu-id="34c7b-140">La valeur de retour de la fonction **glRenderMode** est déterminée par le mode de rendu au moment où **glRenderMode** est appelé, plutôt que par *mode*.</span><span class="sxs-lookup"><span data-stu-id="34c7b-140">The return value of the **glRenderMode** function is determined by the render mode at the time **glRenderMode** is called, rather than by *mode*.</span></span> <span data-ttu-id="34c7b-141">Les valeurs retournées pour les trois modes de rendu sont les suivantes.</span><span class="sxs-lookup"><span data-stu-id="34c7b-141">The values returned for the three render modes are as follows.</span></span>



| <span data-ttu-id="34c7b-142">Valeur</span><span class="sxs-lookup"><span data-stu-id="34c7b-142">Value</span></span>        | <span data-ttu-id="34c7b-143">Signification</span><span class="sxs-lookup"><span data-stu-id="34c7b-143">Meaning</span></span>                                                                 |
|--------------|-------------------------------------------------------------------------|
| <span data-ttu-id="34c7b-144">\_rendu GL</span><span class="sxs-lookup"><span data-stu-id="34c7b-144">GL\_RENDER</span></span>   | <span data-ttu-id="34c7b-145">Zéro.</span><span class="sxs-lookup"><span data-stu-id="34c7b-145">Zero.</span></span>                                                                   |
| <span data-ttu-id="34c7b-146">sélection du GL \_</span><span class="sxs-lookup"><span data-stu-id="34c7b-146">GL\_SELECT</span></span>   | <span data-ttu-id="34c7b-147">Nombre d’enregistrements d’accès transférés à la mémoire tampon de sélection.</span><span class="sxs-lookup"><span data-stu-id="34c7b-147">The number of hit records transferred to the select buffer.</span></span>             |
| <span data-ttu-id="34c7b-148">Commentaires sur le GL \_</span><span class="sxs-lookup"><span data-stu-id="34c7b-148">GL\_FEEDBACK</span></span> | <span data-ttu-id="34c7b-149">Nombre de valeurs (pas de vertex) transférées vers la mémoire tampon de commentaires.</span><span class="sxs-lookup"><span data-stu-id="34c7b-149">The number of values (not vertices) transferred to the feedback buffer.</span></span> |



 

<span data-ttu-id="34c7b-150">Pour plus d’informations sur le fonctionnement de la sélection et des commentaires, consultez [**glSelectBuffer**](glselectbuffer.md) et [**glFeedbackBuffer**](glfeedbackbuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="34c7b-150">Refer to [**glSelectBuffer**](glselectbuffer.md) and [**glFeedbackBuffer**](glfeedbackbuffer.md) for more details concerning selection and feedback operation.</span></span>

<span data-ttu-id="34c7b-151">Si une erreur est générée, **glRenderMode** retourne zéro quel que soit le mode de rendu actuel.</span><span class="sxs-lookup"><span data-stu-id="34c7b-151">If an error is generated, **glRenderMode** returns zero regardless of the current render mode.</span></span>

<span data-ttu-id="34c7b-152">La fonction suivante récupère des informations relatives à **glRenderMode**:</span><span class="sxs-lookup"><span data-stu-id="34c7b-152">The following function retrieves information related to **glRenderMode**:</span></span>

<span data-ttu-id="34c7b-153">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) avec argument GL \_ Render \_ mode</span><span class="sxs-lookup"><span data-stu-id="34c7b-153">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_RENDER\_MODE</span></span>

## <a name="requirements"></a><span data-ttu-id="34c7b-154">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="34c7b-154">Requirements</span></span>



| <span data-ttu-id="34c7b-155">Condition requise</span><span class="sxs-lookup"><span data-stu-id="34c7b-155">Requirement</span></span> | <span data-ttu-id="34c7b-156">Valeur</span><span class="sxs-lookup"><span data-stu-id="34c7b-156">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="34c7b-157">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="34c7b-157">Minimum supported client</span></span><br/> | <span data-ttu-id="34c7b-158">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="34c7b-158">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="34c7b-159">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="34c7b-159">Minimum supported server</span></span><br/> | <span data-ttu-id="34c7b-160">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="34c7b-160">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="34c7b-161">En-tête</span><span class="sxs-lookup"><span data-stu-id="34c7b-161">Header</span></span><br/>                   | <dl> <span data-ttu-id="34c7b-162"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="34c7b-162"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="34c7b-163">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="34c7b-163">Library</span></span><br/>                  | <dl> <span data-ttu-id="34c7b-164"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="34c7b-164"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="34c7b-165">DLL</span><span class="sxs-lookup"><span data-stu-id="34c7b-165">DLL</span></span><br/>                      | <dl> <span data-ttu-id="34c7b-166"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="34c7b-166"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="34c7b-167">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="34c7b-167">See also</span></span>

<dl> <dt>

[<span data-ttu-id="34c7b-168">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="34c7b-168">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="34c7b-169">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="34c7b-169">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="34c7b-170">**glFeedbackBuffer**</span><span class="sxs-lookup"><span data-stu-id="34c7b-170">**glFeedbackBuffer**</span></span>](glfeedbackbuffer.md)
</dt> <dt>

[<span data-ttu-id="34c7b-171">**glInitNames**</span><span class="sxs-lookup"><span data-stu-id="34c7b-171">**glInitNames**</span></span>](glinitnames.md)
</dt> <dt>

[<span data-ttu-id="34c7b-172">**glLoadName**</span><span class="sxs-lookup"><span data-stu-id="34c7b-172">**glLoadName**</span></span>](glloadname.md)
</dt> <dt>

[<span data-ttu-id="34c7b-173">**glPassThrough**</span><span class="sxs-lookup"><span data-stu-id="34c7b-173">**glPassThrough**</span></span>](glpassthrough.md)
</dt> <dt>

[<span data-ttu-id="34c7b-174">**glPushName**</span><span class="sxs-lookup"><span data-stu-id="34c7b-174">**glPushName**</span></span>](glpushname.md)
</dt> <dt>

[<span data-ttu-id="34c7b-175">**glSelectBuffer**</span><span class="sxs-lookup"><span data-stu-id="34c7b-175">**glSelectBuffer**</span></span>](glselectbuffer.md)
</dt> </dl>

 

 





