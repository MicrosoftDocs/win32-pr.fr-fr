---
title: fonction glGetTexParameteriv (GL. h)
description: Les fonctions glGetTexParameterfv et glGetTexParameteriv retournent des valeurs de paramètre de texture. | fonction glGetTexParameteriv (GL. h)
ms.assetid: b89d10f1-5e30-4d25-8953-fbd59781fdac
keywords:
- glGetTexParameteriv fonction OpenGL
topic_type:
- apiref
api_name:
- glGetTexParameteriv
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7ca78983594487fd22917c15a5b211c529b6b14d
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "106524826"
---
# <a name="glgettexparameteriv-function"></a><span data-ttu-id="14510-105">glGetTexParameteriv fonction)</span><span class="sxs-lookup"><span data-stu-id="14510-105">glGetTexParameteriv function</span></span>

<span data-ttu-id="14510-106">Les fonctions [**glGetTexParameterfv**](glgettexparameterfv.md) et **glGetTexParameteriv** retournent des valeurs de paramètre de texture.</span><span class="sxs-lookup"><span data-stu-id="14510-106">The [**glGetTexParameterfv**](glgettexparameterfv.md) and **glGetTexParameteriv** functions return texture parameter values.</span></span>

## <a name="syntax"></a><span data-ttu-id="14510-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="14510-107">Syntax</span></span>


```C++
void WINAPI glGetTexParameteriv(
   GLenum target,
   GLenum pname,
   GLint  *params
);
```



## <a name="parameters"></a><span data-ttu-id="14510-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="14510-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="14510-109">*cible*</span><span class="sxs-lookup"><span data-stu-id="14510-109">*target*</span></span> 
</dt> <dd>

<span data-ttu-id="14510-110">Nom symbolique de la texture cible.</span><span class="sxs-lookup"><span data-stu-id="14510-110">The symbolic name of the target texture.</span></span> <span data-ttu-id="14510-111">La \_ texture GL \_ 1D et la \_ texture GL \_ 2D sont acceptées.</span><span class="sxs-lookup"><span data-stu-id="14510-111">GL\_TEXTURE\_1D and GL\_TEXTURE\_2D are accepted.</span></span>

</dd> <dt>

<span data-ttu-id="14510-112">*pname*</span><span class="sxs-lookup"><span data-stu-id="14510-112">*pname*</span></span> 
</dt> <dd>

<span data-ttu-id="14510-113">Nom symbolique d’un paramètre de texture.</span><span class="sxs-lookup"><span data-stu-id="14510-113">The symbolic name of a texture parameter.</span></span> <span data-ttu-id="14510-114">Les valeurs suivantes sont acceptées.</span><span class="sxs-lookup"><span data-stu-id="14510-114">The following values are accepted.</span></span>



| <span data-ttu-id="14510-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="14510-115">Value</span></span>                                                                                                                                                                                         | <span data-ttu-id="14510-116">Signification</span><span class="sxs-lookup"><span data-stu-id="14510-116">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                      |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_TEXTURE_MAG_FILTER"></span><span id="gl_texture_mag_filter"></span><dl> <span data-ttu-id="14510-117"><dt>**filtre de la \_ texture GL \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="14510-117"><dt>**GL\_TEXTURE\_MAG\_FILTER**</dt></span></span> </dl>       | <span data-ttu-id="14510-118">Retourne le filtre d’agrandissement de texture à valeur unique, une constante symbolique.</span><span class="sxs-lookup"><span data-stu-id="14510-118">Returns the single-valued texture magnification filter, a symbolic constant.</span></span><br/>                                                                                                                                                                                                                                                                                                      |
| <span id="GL_TEXTURE_MIN_FILTER"></span><span id="gl_texture_min_filter"></span><dl> <span data-ttu-id="14510-119"><dt>**filtre de la \_ texture GL \_ min. \_**</dt></span><span class="sxs-lookup"><span data-stu-id="14510-119"><dt>**GL\_TEXTURE\_MIN\_FILTER**</dt></span></span> </dl>       | <span data-ttu-id="14510-120">Retourne le filtre de réduction de la texture à valeur unique, une constante symbolique.</span><span class="sxs-lookup"><span data-stu-id="14510-120">Returns the single-valued texture minification filter, a symbolic constant.</span></span><br/>                                                                                                                                                                                                                                                                                                       |
| <span id="GL_TEXTURE_WRAP_S"></span><span id="gl_texture_wrap_s"></span><dl> <span data-ttu-id="14510-121"><dt>**\_ \_ encapsuler la texture GL \_ S**</dt></span><span class="sxs-lookup"><span data-stu-id="14510-121"><dt>**GL\_TEXTURE\_WRAP\_S**</dt></span></span> </dl>                   | <span data-ttu-id="14510-122">Retourne la fonction d’encapsulation à valeur unique pour les coordonnées de texture *s*, une constante symbolique.</span><span class="sxs-lookup"><span data-stu-id="14510-122">Returns the single-valued wrapping function for texture coordinate *s*, a symbolic constant.</span></span><br/>                                                                                                                                                                                                                                                                                      |
| <span id="GL_TEXTURE_WRAP_T"></span><span id="gl_texture_wrap_t"></span><dl> <span data-ttu-id="14510-123"><dt>**\_enveloppe de \_ la texture GL \_ T**</dt></span><span class="sxs-lookup"><span data-stu-id="14510-123"><dt>**GL\_TEXTURE\_WRAP\_T**</dt></span></span> </dl>                   | <span data-ttu-id="14510-124">Retourne la fonction d’encapsulation à valeur unique pour la coordonnée de texture *t*, une constante symbolique.</span><span class="sxs-lookup"><span data-stu-id="14510-124">Returns the single-valued wrapping function for texture coordinate *t*, a symbolic constant.</span></span><br/>                                                                                                                                                                                                                                                                                      |
| <span id="GL_TEXTURE_BORDER_COLOR"></span><span id="gl_texture_border_color"></span><dl> <span data-ttu-id="14510-125"><dt>**couleur de bordure de la \_ texture GL \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="14510-125"><dt>**GL\_TEXTURE\_BORDER\_COLOR**</dt></span></span> </dl> | <span data-ttu-id="14510-126">Retourne quatre nombres entiers ou à virgule flottante qui composent la couleur RVBA de la bordure de texture.</span><span class="sxs-lookup"><span data-stu-id="14510-126">Returns four integer or floating-point numbers that comprise the RGBA color of the texture border.</span></span> <span data-ttu-id="14510-127">Les valeurs à virgule flottante sont retournées dans la plage \[ 0, 1 \] .</span><span class="sxs-lookup"><span data-stu-id="14510-127">Floating-point values are returned in the range \[0,1\].</span></span> <span data-ttu-id="14510-128">Les valeurs entières sont retournées sous la forme d’un mappage linéaire de la représentation à virgule flottante interne, de sorte que 1,0 correspond à l’entier représentable le plus positif et-1,0 correspond à l’entier pouvant être représenté le plus négatif.</span><span class="sxs-lookup"><span data-stu-id="14510-128">Integer values are returned as a linear mapping of the internal floating-point representation such that 1.0 maps to the most positive representable integer and -1.0 maps to the most negative representable integer.</span></span><br/> |
| <span id="GL_TEXTURE_PRIORITY"></span><span id="gl_texture_priority"></span><dl> <span data-ttu-id="14510-129"><dt>**\_priorité de texture GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="14510-129"><dt>**GL\_TEXTURE\_PRIORITY**</dt></span></span> </dl>              | <span data-ttu-id="14510-130">Retourne la priorité de résidence de la texture cible (ou de la texture nommée qui lui est liée).</span><span class="sxs-lookup"><span data-stu-id="14510-130">Returns the residence priority of the target texture (or the named texture bound to it).</span></span> <span data-ttu-id="14510-131">La valeur initiale est 1.</span><span class="sxs-lookup"><span data-stu-id="14510-131">The initial value is 1.</span></span> <span data-ttu-id="14510-132">Consultez [**glPrioritizeTextures**](glprioritizetextures.md).</span><span class="sxs-lookup"><span data-stu-id="14510-132">See [**glPrioritizeTextures**](glprioritizetextures.md).</span></span><br/>                                                                                                                                                                                                        |
| <span id="GL_TEXTURE_RESIDENT"></span><span id="gl_texture_resident"></span><dl> <span data-ttu-id="14510-133"><dt>**la \_ texture du GL \_ résident**</dt></span><span class="sxs-lookup"><span data-stu-id="14510-133"><dt>**GL\_TEXTURE\_RESIDENT**</dt></span></span> </dl>              | <span data-ttu-id="14510-134">Retourne l’état de résidence de la texture cible.</span><span class="sxs-lookup"><span data-stu-id="14510-134">Returns the residence status of the target texture.</span></span> <span data-ttu-id="14510-135">Si la valeur retournée dans params est définie sur GL \_ true, la texture réside dans la mémoire de texture.</span><span class="sxs-lookup"><span data-stu-id="14510-135">If the value returned in params is GL\_TRUE, the texture is resident in texture memory.</span></span> <span data-ttu-id="14510-136">Consultez [**glAreTexturesResident**](glaretexturesresident.md).</span><span class="sxs-lookup"><span data-stu-id="14510-136">See [**glAreTexturesResident**](glaretexturesresident.md).</span></span><br/>                                                                                                                                                                           |



 

</dd> <dt>

<span data-ttu-id="14510-137">*params*</span><span class="sxs-lookup"><span data-stu-id="14510-137">*params*</span></span> 
</dt> <dd>

<span data-ttu-id="14510-138">Retourne les paramètres de texture.</span><span class="sxs-lookup"><span data-stu-id="14510-138">Returns the texture parameters.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="14510-139">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="14510-139">Return value</span></span>

<span data-ttu-id="14510-140">Cette fonction ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="14510-140">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="14510-141">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="14510-141">Error codes</span></span>

<span data-ttu-id="14510-142">Les codes d’erreur suivants peuvent être récupérés par la fonction [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="14510-142">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="14510-143">Nom</span><span class="sxs-lookup"><span data-stu-id="14510-143">Name</span></span>                                                                                                  | <span data-ttu-id="14510-144">Signification</span><span class="sxs-lookup"><span data-stu-id="14510-144">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="14510-145"><dt>**\_enum GL non valide \_**</dt></span><span class="sxs-lookup"><span data-stu-id="14510-145"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="14510-146">la *cible* ou le *nom* n’était pas une valeur acceptée.</span><span class="sxs-lookup"><span data-stu-id="14510-146">*target* or *name* was not an accepted value.</span></span><br/>                                                                              |
| <dl> <span data-ttu-id="14510-147"><dt>**\_opération non valide du GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="14510-147"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="14510-148">La fonction a été appelée entre un appel à [**glBegin**](glbegin.md) et l’appel correspondant à [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="14510-148">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="14510-149">Notes</span><span class="sxs-lookup"><span data-stu-id="14510-149">Remarks</span></span>

<span data-ttu-id="14510-150">La fonction **glGetTexParameter** *retourne in paramètre* la valeur ou les valeurs du paramètre de texture spécifié comme *pname*.</span><span class="sxs-lookup"><span data-stu-id="14510-150">The **glGetTexParameter** function returns in *params* the value or values of the texture parameter specified as *pname*.</span></span> <span data-ttu-id="14510-151">Le paramètre *target* définit la texture cible, à savoir la texture GL \_ \_ 1D ou la \_ texture GL \_ 2D, pour spécifier une texturation unidimensionnelle ou à deux dimensions.</span><span class="sxs-lookup"><span data-stu-id="14510-151">The *target* parameter defines the target texture, either GL\_TEXTURE\_1D or GL\_TEXTURE\_2D, to specify one-dimensional or two-dimensional texturing.</span></span> <span data-ttu-id="14510-152">Le paramètre *pname* accepte les mêmes symboles que [**glTexParameter**](gltexparameter-functions.md), avec les mêmes interprétations.</span><span class="sxs-lookup"><span data-stu-id="14510-152">The *pname* parameter accepts the same symbols as [**glTexParameter**](gltexparameter-functions.md), with the same interpretations.</span></span>

<span data-ttu-id="14510-153">Si une erreur est générée, aucune modification n’est apportée au contenu des *paramètres*.</span><span class="sxs-lookup"><span data-stu-id="14510-153">If an error is generated, no change is made to the contents of *params*.</span></span>

## <a name="requirements"></a><span data-ttu-id="14510-154">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="14510-154">Requirements</span></span>



| <span data-ttu-id="14510-155">Condition requise</span><span class="sxs-lookup"><span data-stu-id="14510-155">Requirement</span></span> | <span data-ttu-id="14510-156">Valeur</span><span class="sxs-lookup"><span data-stu-id="14510-156">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="14510-157">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="14510-157">Minimum supported client</span></span><br/> | <span data-ttu-id="14510-158">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="14510-158">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="14510-159">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="14510-159">Minimum supported server</span></span><br/> | <span data-ttu-id="14510-160">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="14510-160">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="14510-161">En-tête</span><span class="sxs-lookup"><span data-stu-id="14510-161">Header</span></span><br/>                   | <dl> <span data-ttu-id="14510-162"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="14510-162"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="14510-163">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="14510-163">Library</span></span><br/>                  | <dl> <span data-ttu-id="14510-164"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="14510-164"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="14510-165">DLL</span><span class="sxs-lookup"><span data-stu-id="14510-165">DLL</span></span><br/>                      | <dl> <span data-ttu-id="14510-166"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="14510-166"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="14510-167">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="14510-167">See also</span></span>

<dl> <dt>

[<span data-ttu-id="14510-168">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="14510-168">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="14510-169">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="14510-169">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="14510-170">**glTexParameter**</span><span class="sxs-lookup"><span data-stu-id="14510-170">**glTexParameter**</span></span>](gltexparameter-functions.md)
</dt> </dl>

 

 





