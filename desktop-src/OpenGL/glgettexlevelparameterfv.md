---
title: fonction glGetTexLevelParameterfv (GL. h)
description: Les fonctions glGetTexLevelParameterfv et glGetTexLevelParameteriv retournent des valeurs de paramètre de texture pour un niveau de détail spécifique. | fonction glGetTexLevelParameterfv (GL. h)
ms.assetid: 5ea91f2e-c0cd-41ee-be95-df096f1c78ef
keywords:
- glGetTexLevelParameterfv fonction OpenGL
topic_type:
- apiref
api_name:
- glGetTexLevelParameterfv
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c92f8b55b41d3538f116241a0401cedf643a5e55
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "106522918"
---
# <a name="glgettexlevelparameterfv-function"></a><span data-ttu-id="a5531-105">glGetTexLevelParameterfv fonction)</span><span class="sxs-lookup"><span data-stu-id="a5531-105">glGetTexLevelParameterfv function</span></span>

<span data-ttu-id="a5531-106">Les fonctions **glGetTexLevelParameterfv** et [**glGetTexLevelParameteriv**](glgettexlevelparameteriv.md) retournent des valeurs de paramètre de texture pour un niveau de détail spécifique.</span><span class="sxs-lookup"><span data-stu-id="a5531-106">The **glGetTexLevelParameterfv** and [**glGetTexLevelParameteriv**](glgettexlevelparameteriv.md) functions return texture parameter values for a specific level of detail.</span></span>

## <a name="syntax"></a><span data-ttu-id="a5531-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a5531-107">Syntax</span></span>


```C++
void WINAPI glGetTexLevelParameterfv(
   GLenum  target,
   GLint   level,
   GLenum  pname,
   GLfloat *params
);
```



## <a name="parameters"></a><span data-ttu-id="a5531-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a5531-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a5531-109">*cible*</span><span class="sxs-lookup"><span data-stu-id="a5531-109">*target*</span></span> 
</dt> <dd>

<span data-ttu-id="a5531-110">Nom symbolique de la texture cible : la texture GL \_ \_ 1D, la texture \_ GL \_ 2D, la \_ texture du proxy GL \_ \_ 1D ou la \_ texture du proxy GL \_ \_ 2D.</span><span class="sxs-lookup"><span data-stu-id="a5531-110">The symbolic name of the target texture: either GL\_TEXTURE\_1D, GL\_TEXTURE\_2D, GL\_PROXY\_TEXTURE\_1D, or GL\_PROXY\_TEXTURE\_2D.</span></span>

</dd> <dt>

<span data-ttu-id="a5531-111">*level*</span><span class="sxs-lookup"><span data-stu-id="a5531-111">*level*</span></span> 
</dt> <dd>

<span data-ttu-id="a5531-112">Numéro de niveau de détail de l’image souhaitée.</span><span class="sxs-lookup"><span data-stu-id="a5531-112">The level-of-detail number of the desired image.</span></span> <span data-ttu-id="a5531-113">Le niveau 0 est le niveau d’image de base.</span><span class="sxs-lookup"><span data-stu-id="a5531-113">Level 0 is the base image level.</span></span> <span data-ttu-id="a5531-114">Le niveau *n* est la *n* ième image de réduction mipmap.</span><span class="sxs-lookup"><span data-stu-id="a5531-114">Level *n* is the *n* th mipmap reduction image.</span></span>

</dd> <dt>

<span data-ttu-id="a5531-115">*pname*</span><span class="sxs-lookup"><span data-stu-id="a5531-115">*pname*</span></span> 
</dt> <dd>

<span data-ttu-id="a5531-116">Nom symbolique d’un paramètre de texture.</span><span class="sxs-lookup"><span data-stu-id="a5531-116">The symbolic name of a texture parameter.</span></span> <span data-ttu-id="a5531-117">Les noms de paramètres suivants sont acceptés.</span><span class="sxs-lookup"><span data-stu-id="a5531-117">The following parameter names are accepted.</span></span>



| <span data-ttu-id="a5531-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="a5531-118">Value</span></span>                                                                                                                                                                                                  | <span data-ttu-id="a5531-119">Signification</span><span class="sxs-lookup"><span data-stu-id="a5531-119">Meaning</span></span>                                                                                                                                                                                                                                                                                           |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_TEXTURE_WIDTH"></span><span id="gl_texture_width"></span><dl> <span data-ttu-id="a5531-120"><dt>**largeur de la \_ texture GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="a5531-120"><dt>**GL\_TEXTURE\_WIDTH**</dt></span></span> </dl>                                | <span data-ttu-id="a5531-121">Le paramètre *params* retourne une valeur unique contenant la largeur de l’image de texture.</span><span class="sxs-lookup"><span data-stu-id="a5531-121">The *params* parameter returns a single value containing the width of the texture image.</span></span> <span data-ttu-id="a5531-122">Cette valeur comprend la bordure de l’image de texture.</span><span class="sxs-lookup"><span data-stu-id="a5531-122">This value includes the border of the texture image.</span></span><br/>                                                                                                                                          |
| <span id="GL_TEXTURE_HEIGHT"></span><span id="gl_texture_height"></span><dl> <span data-ttu-id="a5531-123"><dt>**hauteur de la \_ texture GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="a5531-123"><dt>**GL\_TEXTURE\_HEIGHT**</dt></span></span> </dl>                             | <span data-ttu-id="a5531-124">Le paramètre *params* retourne une valeur unique contenant la hauteur de l’image de texture.</span><span class="sxs-lookup"><span data-stu-id="a5531-124">The *params* parameter returns a single value containing the height of the texture image.</span></span> <span data-ttu-id="a5531-125">Cette valeur comprend la bordure de l’image de texture.</span><span class="sxs-lookup"><span data-stu-id="a5531-125">This value includes the border of the texture image.</span></span><br/>                                                                                                                                         |
| <span id="GL_TEXTURE_INTERNAL_FORMAT"></span><span id="gl_texture_internal_format"></span><dl> <span data-ttu-id="a5531-126"><dt>**\_ \_ format interne de la texture GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="a5531-126"><dt>**GL\_TEXTURE\_INTERNAL\_FORMAT**</dt></span></span> </dl> | <span data-ttu-id="a5531-127">Le paramètre *params* retourne une valeur unique qui décrit le format Texel de la texture.</span><span class="sxs-lookup"><span data-stu-id="a5531-127">The *params* parameter returns a single value which describes the texel format of the texture.</span></span><br/>                                                                                                                                                                                         |
| <span id="GL_TEXTURE_BORDER"></span><span id="gl_texture_border"></span><dl> <span data-ttu-id="a5531-128"><dt>**bordure de la \_ texture GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="a5531-128"><dt>**GL\_TEXTURE\_BORDER**</dt></span></span> </dl>                             | <span data-ttu-id="a5531-129">Le paramètre *params* retourne une valeur unique : la largeur en pixels de la bordure de l’image de texture.</span><span class="sxs-lookup"><span data-stu-id="a5531-129">The *params* parameter returns a single value: the width in pixels of the border of the texture image.</span></span><br/>                                                                                                                                                                                 |
| <span id="GL_TEXTURE_RED_SIZE"></span><span id="gl_texture_red_size"></span><dl> <span data-ttu-id="a5531-130"><dt>**taille de la texture GL en \_ \_ rouge \_**</dt></span><span class="sxs-lookup"><span data-stu-id="a5531-130"><dt>**GL\_TEXTURE\_RED\_SIZE**</dt></span></span> </dl>                      | <span data-ttu-id="a5531-131">La résolution de stockage interne du composant rouge d’une Texel.</span><span class="sxs-lookup"><span data-stu-id="a5531-131">The internal storage resolution of the red component of a texel.</span></span> <span data-ttu-id="a5531-132">La résolution choisie par OpenGL sera une correspondance proche de la résolution demandée par l’utilisateur avec l’argument Component de [**glTexImage1D**](glteximage1d.md) ou [**glTexImage2D**](glteximage2d.md).</span><span class="sxs-lookup"><span data-stu-id="a5531-132">The resolution chosen by the OpenGL will be a close match for the resolution requested by the user with the component argument of [**glTexImage1D**](glteximage1d.md) or [**glTexImage2D**](glteximage2d.md).</span></span><br/>       |
| <span id="GL_TEXTURE_GREEN_SIZE"></span><span id="gl_texture_green_size"></span><dl> <span data-ttu-id="a5531-133"><dt>**\_ \_ taille verte de la texture GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="a5531-133"><dt>**GL\_TEXTURE\_GREEN\_SIZE**</dt></span></span> </dl>                | <span data-ttu-id="a5531-134">Résolution de stockage interne de la composante verte d’un Texel.</span><span class="sxs-lookup"><span data-stu-id="a5531-134">The internal storage resolution of the green component of a texel.</span></span> <span data-ttu-id="a5531-135">La résolution choisie par OpenGL sera une correspondance proche de la résolution demandée par l’utilisateur avec l’argument Component de [**glTexImage1D**](glteximage1d.md) ou [**glTexImage2D**](glteximage2d.md).</span><span class="sxs-lookup"><span data-stu-id="a5531-135">The resolution chosen by the OpenGL will be a close match for the resolution requested by the user with the component argument of [**glTexImage1D**](glteximage1d.md) or [**glTexImage2D**](glteximage2d.md).</span></span><br/>     |
| <span id="GL_TEXTURE_BLUE_SIZE"></span><span id="gl_texture_blue_size"></span><dl> <span data-ttu-id="a5531-136"><dt>**\_ \_ taille bleue de la texture GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="a5531-136"><dt>**GL\_TEXTURE\_BLUE\_SIZE**</dt></span></span> </dl>                   | <span data-ttu-id="a5531-137">Résolution de stockage interne de la composante bleue d’un Texel.</span><span class="sxs-lookup"><span data-stu-id="a5531-137">The internal storage resolution of the blue component of a texel.</span></span> <span data-ttu-id="a5531-138">La résolution choisie par OpenGL sera une correspondance proche de la résolution demandée par l’utilisateur avec l’argument Component de [**glTexImage1D**](glteximage1d.md) ou [**glTexImage2D**](glteximage2d.md).</span><span class="sxs-lookup"><span data-stu-id="a5531-138">The resolution chosen by the OpenGL will be a close match for the resolution requested by the user with the component argument of [**glTexImage1D**](glteximage1d.md) or [**glTexImage2D**](glteximage2d.md).</span></span><br/>      |
| <span id="GL_TEXTURE_ALPHA_SIZE"></span><span id="gl_texture_alpha_size"></span><dl> <span data-ttu-id="a5531-139"><dt>**\_ \_ taille alpha de la texture GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="a5531-139"><dt>**GL\_TEXTURE\_ALPHA\_SIZE**</dt></span></span> </dl>                | <span data-ttu-id="a5531-140">Résolution de stockage interne du composant alpha d’un Texel.</span><span class="sxs-lookup"><span data-stu-id="a5531-140">The internal storage resolution of the alpha component of a texel.</span></span> <span data-ttu-id="a5531-141">La résolution choisie par OpenGL sera une correspondance proche de la résolution demandée par l’utilisateur avec l’argument Component de [**glTexImage1D**](glteximage1d.md) ou [**glTexImage2D**](glteximage2d.md).</span><span class="sxs-lookup"><span data-stu-id="a5531-141">The resolution chosen by the OpenGL will be a close match for the resolution requested by the user with the component argument of [**glTexImage1D**](glteximage1d.md) or [**glTexImage2D**](glteximage2d.md).</span></span><br/>     |
| <span id="GL_TEXTURE_LUMINANCE_SIZE"></span><span id="gl_texture_luminance_size"></span><dl> <span data-ttu-id="a5531-142"><dt>**taille de luminance de la \_ texture GL \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="a5531-142"><dt>**GL\_TEXTURE\_LUMINANCE\_SIZE**</dt></span></span> </dl>    | <span data-ttu-id="a5531-143">Résolution de stockage interne de la composante luminance d’un Texel.</span><span class="sxs-lookup"><span data-stu-id="a5531-143">The internal storage resolution of the luminance component of a texel.</span></span> <span data-ttu-id="a5531-144">La résolution choisie par OpenGL sera une correspondance proche de la résolution demandée par l’utilisateur avec l’argument Component de [**glTexImage1D**](glteximage1d.md) ou [**glTexImage2D**](glteximage2d.md).</span><span class="sxs-lookup"><span data-stu-id="a5531-144">The resolution chosen by the OpenGL will be a close match for the resolution requested by the user with the component argument of [**glTexImage1D**](glteximage1d.md) or [**glTexImage2D**](glteximage2d.md).</span></span><br/> |
| <span id="GL_TEXTURE_INTENSITY_SIZE"></span><span id="gl_texture_intensity_size"></span><dl> <span data-ttu-id="a5531-145"><dt>**taille d’intensité de la \_ texture GL \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="a5531-145"><dt>**GL\_TEXTURE\_INTENSITY\_SIZE**</dt></span></span> </dl>    | <span data-ttu-id="a5531-146">Résolution de stockage interne du composant d’intensité d’un Texel.</span><span class="sxs-lookup"><span data-stu-id="a5531-146">The internal storage resolution of the intensity component of a texel.</span></span> <span data-ttu-id="a5531-147">La résolution choisie par OpenGL sera une correspondance proche de la résolution demandée par l’utilisateur avec l’argument Component de [**glTexImage1D**](glteximage1d.md) ou [**glTexImage2D**](glteximage2d.md).</span><span class="sxs-lookup"><span data-stu-id="a5531-147">The resolution chosen by the OpenGL will be a close match for the resolution requested by the user with the component argument of [**glTexImage1D**](glteximage1d.md) or [**glTexImage2D**](glteximage2d.md).</span></span><br/> |
| <span id="GL_TEXTURE_COMPONENTS"></span><span id="gl_texture_components"></span><dl> <span data-ttu-id="a5531-148"><dt>**\_composants de texture GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="a5531-148"><dt>**GL\_TEXTURE\_COMPONENTS**</dt></span></span> </dl>                 | <span data-ttu-id="a5531-149">Le paramètre *params* retourne une valeur unique : le nombre de composants dans l’image de texture.</span><span class="sxs-lookup"><span data-stu-id="a5531-149">The *params* parameter returns a single value: the number of components in the texture image.</span></span><br/>                                                                                                                                                                                          |



 

</dd> <dt>

<span data-ttu-id="a5531-150">*params*</span><span class="sxs-lookup"><span data-stu-id="a5531-150">*params*</span></span> 
</dt> <dd>

<span data-ttu-id="a5531-151">Retourne les données demandées.</span><span class="sxs-lookup"><span data-stu-id="a5531-151">Returns the requested data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a5531-152">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="a5531-152">Return value</span></span>

<span data-ttu-id="a5531-153">Cette fonction ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="a5531-153">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="a5531-154">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="a5531-154">Error codes</span></span>

<span data-ttu-id="a5531-155">Les codes d’erreur suivants peuvent être récupérés par la fonction [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="a5531-155">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="a5531-156">Nom</span><span class="sxs-lookup"><span data-stu-id="a5531-156">Name</span></span>                                                                                                  | <span data-ttu-id="a5531-157">Signification</span><span class="sxs-lookup"><span data-stu-id="a5531-157">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="a5531-158"><dt>**\_enum GL non valide \_**</dt></span><span class="sxs-lookup"><span data-stu-id="a5531-158"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="a5531-159">*target* ou *pname* n’est pas une valeur acceptée.</span><span class="sxs-lookup"><span data-stu-id="a5531-159">*target* or *pname* was not an accepted value.</span></span><br/>                                                                             |
| <dl> <span data-ttu-id="a5531-160"><dt>**\_valeur non valide du GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="a5531-160"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="a5531-161">le *niveau* est inférieur à zéro ou supérieur au *Journal* 2 *(max)*, où *Max* est la valeur retournée de la taille de \_ texture max GL \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="a5531-161">*level* is less than zero or greater than *log* 2 *(max)*, where *max* is the returned value of GL\_MAX\_TEXTURE\_SIZE.</span></span><br/>      |
| <dl> <span data-ttu-id="a5531-162"><dt>**\_opération non valide du GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="a5531-162"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="a5531-163">La fonction a été appelée entre un appel à [**glBegin**](glbegin.md) et l’appel correspondant à [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="a5531-163">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="a5531-164">Notes</span><span class="sxs-lookup"><span data-stu-id="a5531-164">Remarks</span></span>

<span data-ttu-id="a5531-165">La fonction **glGetTexLevelParameter** retourne les valeurs des paramètres *de texture des paramètres pour* une valeur de niveau de détail spécifique, spécifiée comme *niveau*.</span><span class="sxs-lookup"><span data-stu-id="a5531-165">The **glGetTexLevelParameter** function returns in *params* texture parameter values for a specific level-of-detail value, specified as *level*.</span></span> <span data-ttu-id="a5531-166">Le paramètre *target* définit la texture cible, à savoir la \_ texture GL 1D, la texture \_ GL \_ \_ 2D, la texture du \_ proxy GL \_ \_ 1D ou la \_ \_ texture du proxy GL \_ 2D pour spécifier la texturation unidimensionnelle ou à deux dimensions.</span><span class="sxs-lookup"><span data-stu-id="a5531-166">The *target* parameter defines the target texture, either GL\_TEXTURE\_1D, GL\_TEXTURE\_2D, GL\_PROXY\_TEXTURE\_1D, or GL\_PROXY\_TEXTURE\_2D to specify one-dimensional or two-dimensional texturing.</span></span> <span data-ttu-id="a5531-167">Le paramètre *pname* spécifie le paramètre de texture dont la valeur ou les valeurs seront retournées.</span><span class="sxs-lookup"><span data-stu-id="a5531-167">The *pname* parameter specifies the texture parameter whose value or values will be returned.</span></span>

<span data-ttu-id="a5531-168">Si une erreur est générée, aucune modification n’est apportée au contenu des *paramètres*.</span><span class="sxs-lookup"><span data-stu-id="a5531-168">If an error is generated, no change is made to the contents of *params*.</span></span>

## <a name="requirements"></a><span data-ttu-id="a5531-169">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a5531-169">Requirements</span></span>



| <span data-ttu-id="a5531-170">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a5531-170">Requirement</span></span> | <span data-ttu-id="a5531-171">Valeur</span><span class="sxs-lookup"><span data-stu-id="a5531-171">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a5531-172">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a5531-172">Minimum supported client</span></span><br/> | <span data-ttu-id="a5531-173">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a5531-173">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="a5531-174">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a5531-174">Minimum supported server</span></span><br/> | <span data-ttu-id="a5531-175">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a5531-175">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="a5531-176">En-tête</span><span class="sxs-lookup"><span data-stu-id="a5531-176">Header</span></span><br/>                   | <dl> <span data-ttu-id="a5531-177"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="a5531-177"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="a5531-178">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="a5531-178">Library</span></span><br/>                  | <dl> <span data-ttu-id="a5531-179"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a5531-179"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="a5531-180">DLL</span><span class="sxs-lookup"><span data-stu-id="a5531-180">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a5531-181"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a5531-181"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a5531-182">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a5531-182">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a5531-183">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="a5531-183">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="a5531-184">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="a5531-184">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="a5531-185">**glGetTexParameter**</span><span class="sxs-lookup"><span data-stu-id="a5531-185">**glGetTexParameter**</span></span>](glgettexparameter.md)
</dt> <dt>

[<span data-ttu-id="a5531-186">**glTexImage1D**</span><span class="sxs-lookup"><span data-stu-id="a5531-186">**glTexImage1D**</span></span>](glteximage1d.md)
</dt> <dt>

[<span data-ttu-id="a5531-187">**glTexImage2D**</span><span class="sxs-lookup"><span data-stu-id="a5531-187">**glTexImage2D**</span></span>](glteximage2d.md)
</dt> <dt>

[<span data-ttu-id="a5531-188">**glTexParameter**</span><span class="sxs-lookup"><span data-stu-id="a5531-188">**glTexParameter**</span></span>](gltexparameter-functions.md)
</dt> </dl>

 

 





