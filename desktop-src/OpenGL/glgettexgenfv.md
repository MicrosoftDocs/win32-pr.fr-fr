---
title: fonction glGetTexGenfv (GL. h)
description: Les fonctions glGetTexGendv, glGetTexGenfv et glGetTexGeniv retournent des paramètres de génération de coordonnées de texture. | fonction glGetTexGenfv (GL. h)
ms.assetid: 3b5b78a2-6db6-4931-aabb-25624c5af2f6
keywords:
- glGetTexGenfv fonction OpenGL
topic_type:
- apiref
api_name:
- glGetTexGenfv
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e527d0388b8aca7239ba1c51dccdce15de3cd8ee
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104322117"
---
# <a name="glgettexgenfv-function"></a><span data-ttu-id="159d7-105">glGetTexGenfv fonction)</span><span class="sxs-lookup"><span data-stu-id="159d7-105">glGetTexGenfv function</span></span>

<span data-ttu-id="159d7-106">Les fonctions [**glGetTexGendv**](glgettexgendv.md), **glGetTexGenfv** et [**glGetTexGeniv**](glgettexgeniv.md) retournent des paramètres de génération de coordonnées de texture.</span><span class="sxs-lookup"><span data-stu-id="159d7-106">The [**glGetTexGendv**](glgettexgendv.md), **glGetTexGenfv**, and [**glGetTexGeniv**](glgettexgeniv.md) functions return texture coordinate generation parameters.</span></span>

## <a name="syntax"></a><span data-ttu-id="159d7-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="159d7-107">Syntax</span></span>


```C++
void WINAPI glGetTexGenfv(
   GLenum  coord,
   GLenum  pname,
   GLfloat *params
);
```



## <a name="parameters"></a><span data-ttu-id="159d7-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="159d7-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="159d7-109">*coordonnées*</span><span class="sxs-lookup"><span data-stu-id="159d7-109">*coord*</span></span> 
</dt> <dd>

<span data-ttu-id="159d7-110">Coordonnée de texture.</span><span class="sxs-lookup"><span data-stu-id="159d7-110">A texture coordinate.</span></span> <span data-ttu-id="159d7-111">Doit être GL \_ S, GL \_ T, GL \_ R ou GL \_ Q.</span><span class="sxs-lookup"><span data-stu-id="159d7-111">Must be GL\_S, GL\_T, GL\_R, or GL\_Q.</span></span>

</dd> <dt>

<span data-ttu-id="159d7-112">*pname*</span><span class="sxs-lookup"><span data-stu-id="159d7-112">*pname*</span></span> 
</dt> <dd>

<span data-ttu-id="159d7-113">Nom symbolique de la ou des valeurs à retourner.</span><span class="sxs-lookup"><span data-stu-id="159d7-113">The symbolic name of the value(s) to be returned.</span></span> <span data-ttu-id="159d7-114">Il doit s’agir \_ \_ \_ du mode de la génération de texture GL ou du nom de l’une des équations du plan de génération de texture : plan d' \_ objet GL \_ ou \_ plan oculaire GL \_ .</span><span class="sxs-lookup"><span data-stu-id="159d7-114">Must be either GL\_TEXTURE\_GEN\_MODE or the name of one of the texture generation plane equations: GL\_OBJECT\_PLANE or GL\_EYE\_PLANE.</span></span> <span data-ttu-id="159d7-115">Ces valeurs sont les suivantes.</span><span class="sxs-lookup"><span data-stu-id="159d7-115">These values are as follows.</span></span>



| <span data-ttu-id="159d7-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="159d7-116">Value</span></span>                                                                                                                                                                             | <span data-ttu-id="159d7-117">Signification</span><span class="sxs-lookup"><span data-stu-id="159d7-117">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_TEXTURE_GEN_MODE"></span><span id="gl_texture_gen_mode"></span><dl> <span data-ttu-id="159d7-118"><dt>**\_mode de génération de textures GL \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="159d7-118"><dt>**GL\_TEXTURE\_GEN\_MODE**</dt></span></span> </dl> | <span data-ttu-id="159d7-119">Le paramètre *params* retourne la fonction de génération de texture à valeur unique, une constante symbolique.</span><span class="sxs-lookup"><span data-stu-id="159d7-119">The *params* parameter returns the single-valued texture generation function, a symbolic constant.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                            |
| <span id="GL_OBJECT_PLANE"></span><span id="gl_object_plane"></span><dl> <span data-ttu-id="159d7-120"><dt>**\_plan d’objet GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="159d7-120"><dt>**GL\_OBJECT\_PLANE**</dt></span></span> </dl>              | <span data-ttu-id="159d7-121">Le paramètre *params* retourne les quatre coefficients d’équation plan qui spécifient la génération de la coordonnée linéaire de l’objet.</span><span class="sxs-lookup"><span data-stu-id="159d7-121">The *params* parameter returns the four plane equation coefficients that specify object linear-coordinate generation.</span></span> <span data-ttu-id="159d7-122">Les valeurs entières, quand elles sont demandées, sont mappées directement à partir de la représentation à virgule flottante interne.</span><span class="sxs-lookup"><span data-stu-id="159d7-122">Integer values, when requested, are mapped directly from the internal floating-point representation.</span></span><br/>                                                                                                                                                                                                                                    |
| <span id="GL_EYE_PLANE"></span><span id="gl_eye_plane"></span><dl> <span data-ttu-id="159d7-123"><dt>**\_plan oculaire \_ GL**</dt></span><span class="sxs-lookup"><span data-stu-id="159d7-123"><dt>**GL\_EYE\_PLANE**</dt></span></span> </dl>                       | <span data-ttu-id="159d7-124">Le paramètre *params* retourne les quatre coefficients d’équation plan qui spécifient la génération de coordonnées linéaires oculaires.</span><span class="sxs-lookup"><span data-stu-id="159d7-124">The *params* parameter returns the four plane equation coefficients that specify eye linear-coordinate generation.</span></span> <span data-ttu-id="159d7-125">Les valeurs entières, quand elles sont demandées, sont mappées directement à partir de la représentation à virgule flottante interne.</span><span class="sxs-lookup"><span data-stu-id="159d7-125">Integer values, when requested, are mapped directly from the internal floating-point representation.</span></span> <span data-ttu-id="159d7-126">Les valeurs retournées sont celles qui sont gérées en coordonnées oculaires.</span><span class="sxs-lookup"><span data-stu-id="159d7-126">The returned values are those maintained in eye coordinates.</span></span> <span data-ttu-id="159d7-127">Ils ne sont pas égaux aux valeurs spécifiées à l’aide de [**glTexGen**](gltexgen-functions.md), sauf si la matrice modelview a été identifiée au moment de l’appel de **glTexGen** .</span><span class="sxs-lookup"><span data-stu-id="159d7-127">They are not equal to the values specified using [**glTexGen**](gltexgen-functions.md), unless the modelview matrix was identified at the time **glTexGen** was called.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="159d7-128">*params*</span><span class="sxs-lookup"><span data-stu-id="159d7-128">*params*</span></span> 
</dt> <dd>

<span data-ttu-id="159d7-129">Retourne les données demandées.</span><span class="sxs-lookup"><span data-stu-id="159d7-129">Returns the requested data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="159d7-130">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="159d7-130">Return value</span></span>

<span data-ttu-id="159d7-131">Cette fonction ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="159d7-131">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="159d7-132">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="159d7-132">Error codes</span></span>

<span data-ttu-id="159d7-133">Les codes d’erreur suivants peuvent être récupérés par la fonction [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="159d7-133">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="159d7-134">Nom</span><span class="sxs-lookup"><span data-stu-id="159d7-134">Name</span></span>                                                                                                  | <span data-ttu-id="159d7-135">Signification</span><span class="sxs-lookup"><span data-stu-id="159d7-135">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="159d7-136"><dt>**\_enum GL non valide \_**</dt></span><span class="sxs-lookup"><span data-stu-id="159d7-136"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="159d7-137">*Coord* ou *pname* n’est pas une valeur acceptée.</span><span class="sxs-lookup"><span data-stu-id="159d7-137">*coord* or *pname* was not an accepted value.</span></span><br/>                                                                              |
| <dl> <span data-ttu-id="159d7-138"><dt>**\_opération non valide du GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="159d7-138"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="159d7-139">La fonction a été appelée entre un appel à [**glBegin**](glbegin.md) et l’appel correspondant à [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="159d7-139">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="159d7-140">Notes</span><span class="sxs-lookup"><span data-stu-id="159d7-140">Remarks</span></span>

<span data-ttu-id="159d7-141">La fonction **glGetTexGen** retourne dans *params* les paramètres sélectionnés d’une fonction de génération de coordonnées de texture que vous avez spécifiée avec **glTexGen**.</span><span class="sxs-lookup"><span data-stu-id="159d7-141">The **glGetTexGen** function returns in *params* selected parameters of a texture-coordinate generation function that you specified with **glTexGen**.</span></span> <span data-ttu-id="159d7-142">Le paramètre *Coord* nomme une des coordonnées de texture (*s*, *t*, *r*, *q*) à l’aide de la constante symbolique GL \_ s, GL \_ t, GL \_ r ou GL \_ q.</span><span class="sxs-lookup"><span data-stu-id="159d7-142">The *coord* parameter names one of the (*s*, *t*, *r*, *q*) texture coordinates, using the symbolic constant GL\_S, GL\_T, GL\_R, or GL\_Q.</span></span>

<span data-ttu-id="159d7-143">Si une erreur est générée, aucune modification n’est apportée au contenu des *paramètres*.</span><span class="sxs-lookup"><span data-stu-id="159d7-143">If an error is generated, no change is made to the contents of *params*.</span></span>

## <a name="requirements"></a><span data-ttu-id="159d7-144">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="159d7-144">Requirements</span></span>



| <span data-ttu-id="159d7-145">Condition requise</span><span class="sxs-lookup"><span data-stu-id="159d7-145">Requirement</span></span> | <span data-ttu-id="159d7-146">Valeur</span><span class="sxs-lookup"><span data-stu-id="159d7-146">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="159d7-147">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="159d7-147">Minimum supported client</span></span><br/> | <span data-ttu-id="159d7-148">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="159d7-148">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="159d7-149">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="159d7-149">Minimum supported server</span></span><br/> | <span data-ttu-id="159d7-150">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="159d7-150">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="159d7-151">En-tête</span><span class="sxs-lookup"><span data-stu-id="159d7-151">Header</span></span><br/>                   | <dl> <span data-ttu-id="159d7-152"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="159d7-152"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="159d7-153">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="159d7-153">Library</span></span><br/>                  | <dl> <span data-ttu-id="159d7-154"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="159d7-154"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="159d7-155">DLL</span><span class="sxs-lookup"><span data-stu-id="159d7-155">DLL</span></span><br/>                      | <dl> <span data-ttu-id="159d7-156"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="159d7-156"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="159d7-157">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="159d7-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="159d7-158">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="159d7-158">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="159d7-159">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="159d7-159">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="159d7-160">**glTexGen**</span><span class="sxs-lookup"><span data-stu-id="159d7-160">**glTexGen**</span></span>](gltexgen-functions.md)
</dt> </dl>

 

 





