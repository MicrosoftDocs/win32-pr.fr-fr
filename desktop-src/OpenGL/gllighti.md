---
title: fonction glLighti (GL. h)
description: La fonction glLighti retourne des valeurs de paramètre de source lumineuse.
ms.assetid: 4fa5e604-d45d-412e-a08c-c38e0836596f
keywords:
- glLighti fonction OpenGL
topic_type:
- apiref
api_name:
- glLighti
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 52225c4db8eaa31c17d12a25590b918cf94b4c3b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843741"
---
# <a name="gllighti-function"></a><span data-ttu-id="cd79b-104">glLighti fonction)</span><span class="sxs-lookup"><span data-stu-id="cd79b-104">glLighti function</span></span>

<span data-ttu-id="cd79b-105">La fonction **glLighti** retourne des valeurs de paramètre de source lumineuse.</span><span class="sxs-lookup"><span data-stu-id="cd79b-105">The **glLighti** function returns light source parameter values.</span></span>

## <a name="syntax"></a><span data-ttu-id="cd79b-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="cd79b-106">Syntax</span></span>


```C++
void WINAPI glLighti(
   GLenum light,
   GLenum pname,
   GLint  param
);
```



## <a name="parameters"></a><span data-ttu-id="cd79b-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="cd79b-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cd79b-108">*light*</span><span class="sxs-lookup"><span data-stu-id="cd79b-108">*light*</span></span> 
</dt> <dd>

<span data-ttu-id="cd79b-109">Identificateur d’une lumière.</span><span class="sxs-lookup"><span data-stu-id="cd79b-109">The identifier of a light.</span></span> <span data-ttu-id="cd79b-110">Le nombre d’éclairages possibles dépend de l’implémentation, mais au moins huit lumières sont prises en charge.</span><span class="sxs-lookup"><span data-stu-id="cd79b-110">The number of possible lights depends on the implementation, but at least eight lights are supported.</span></span> <span data-ttu-id="cd79b-111">Ils sont identifiés par des noms symboliques de la forme livre \_ -lumière *i* , où *i* est une valeur : 0 aux \_ indicateurs Max GL \_ -1.</span><span class="sxs-lookup"><span data-stu-id="cd79b-111">They are identified by symbolic names of the form GL\_LIGHT *i* where *i* is a value: 0 to GL\_MAX\_LIGHTS - 1.</span></span>

</dd> <dt>

<span data-ttu-id="cd79b-112">*pname*</span><span class="sxs-lookup"><span data-stu-id="cd79b-112">*pname*</span></span> 
</dt> <dd>

<span data-ttu-id="cd79b-113">Paramètre de source de lumière à valeur unique pour la *lumière*.</span><span class="sxs-lookup"><span data-stu-id="cd79b-113">A single-valued light source parameter for *light*.</span></span> <span data-ttu-id="cd79b-114">Les noms symboliques suivants sont acceptés.</span><span class="sxs-lookup"><span data-stu-id="cd79b-114">The following symbolic names are accepted.</span></span>



| <span data-ttu-id="cd79b-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="cd79b-115">Value</span></span>                                                                                                                                                                                                                                                                                                                                               | <span data-ttu-id="cd79b-116">Signification</span><span class="sxs-lookup"><span data-stu-id="cd79b-116">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_SPOT_EXPONENT"></span><span id="gl_spot_exponent"></span><dl> <span data-ttu-id="cd79b-117"><dt>**exposant de point comptable \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="cd79b-117"><dt>**GL\_SPOT\_EXPONENT**</dt></span></span> </dl>                                                                                                                                                                             | <span data-ttu-id="cd79b-118">Le paramètre *param* est une valeur entière unique qui spécifie la distribution d’intensité de la lumière.</span><span class="sxs-lookup"><span data-stu-id="cd79b-118">The *param* parameter is a single integer value that specifies the intensity distribution of the light.</span></span> <span data-ttu-id="cd79b-119">Les valeurs entières et à virgule flottante sont mappées directement.</span><span class="sxs-lookup"><span data-stu-id="cd79b-119">Integer and floating-point values are mapped directly.</span></span> <span data-ttu-id="cd79b-120">Seules les valeurs de la plage \[ 0, 128 \] sont acceptées.</span><span class="sxs-lookup"><span data-stu-id="cd79b-120">Only values in the range \[0, 128\] are accepted.</span></span> <br/> <span data-ttu-id="cd79b-121">L’intensité de la lumière réelle est atténuée par le cosinus de l’angle entre la direction de la lumière et la direction de la lumière jusqu’au sommet qui est éclairé, élevé à la puissance de l’exposant.</span><span class="sxs-lookup"><span data-stu-id="cd79b-121">Effective light intensity is attenuated by the cosine of the angle between the direction of the light and the direction from the light to the vertex being lighted, raised to the power of the spot exponent.</span></span> <span data-ttu-id="cd79b-122">Par conséquent, les exposants de point plus élevés produisent une source de lumière plus ciblée, quel que soit l’angle de coupure des points.</span><span class="sxs-lookup"><span data-stu-id="cd79b-122">Thus, higher spot exponents result in a more focused light source, regardless of the spot cutoff angle.</span></span> <span data-ttu-id="cd79b-123">L’exposant de point par défaut est 0, ce qui entraîne une distribution uniforme de la lumière.</span><span class="sxs-lookup"><span data-stu-id="cd79b-123">The default spot exponent is 0, resulting in uniform light distribution.</span></span><br/> |
| <span id="GL_SPOT_CUTOFF"></span><span id="gl_spot_cutoff"></span><dl> <span data-ttu-id="cd79b-124"><dt>**coupure de l' \_ emplacement GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="cd79b-124"><dt>**GL\_SPOT\_CUTOFF**</dt></span></span> </dl>                                                                                                                                                                                   | <span data-ttu-id="cd79b-125">Le paramètre *param* est une valeur entière unique qui spécifie l’angle d’étalement maximal d’une source de lumière.</span><span class="sxs-lookup"><span data-stu-id="cd79b-125">The *param* parameter is a single integer value that specifies the maximum spread angle of a light source.</span></span> <span data-ttu-id="cd79b-126">Les valeurs entières et à virgule flottante sont mappées directement.</span><span class="sxs-lookup"><span data-stu-id="cd79b-126">Integer and floating-point values are mapped directly.</span></span> <span data-ttu-id="cd79b-127">Seules les valeurs comprises dans la plage \[ 0, 90 \] et la valeur spéciale 180 sont acceptées.</span><span class="sxs-lookup"><span data-stu-id="cd79b-127">Only values in the range \[0, 90\], and the special value 180, are accepted.</span></span> <br/> <span data-ttu-id="cd79b-128">Si l’angle entre la direction de la lumière et la direction de la lumière vers le vertex en clair est supérieur à l’angle de coupure de l’emplacement, la lumière est entièrement masquée.</span><span class="sxs-lookup"><span data-stu-id="cd79b-128">If the angle between the direction of the light and the direction from the light to the vertex being lighted is greater than the spot cutoff angle, then the light is completely masked.</span></span> <span data-ttu-id="cd79b-129">Dans le cas contraire, son intensité est contrôlée par l’exposant ponctuel et les facteurs d’atténuation.</span><span class="sxs-lookup"><span data-stu-id="cd79b-129">Otherwise, its intensity is controlled by the spot exponent and the attenuation factors.</span></span> <span data-ttu-id="cd79b-130">Le point de coupure par défaut est de 180, ce qui aboutit à une distribution de la lumière uniforme.</span><span class="sxs-lookup"><span data-stu-id="cd79b-130">The default spot cutoff is 180, resulting in uniform light distribution.</span></span><br/>       |
| <span id="GL_CONSTANT_ATTENUATION__GL_LINEAR_ATTENUATION__GL_QUADRATIC_ATTENUATION"></span><span id="gl_constant_attenuation__gl_linear_attenuation__gl_quadratic_attenuation"></span><dl> <span data-ttu-id="cd79b-131"><dt>**\_atténuation constante du GL \_ , \_ atténuation linéaire du GL \_ , \_ \_ atténuation quadratique du GL**</dt></span><span class="sxs-lookup"><span data-stu-id="cd79b-131"><dt>**GL\_CONSTANT\_ATTENUATION, GL\_LINEAR\_ATTENUATION, GL\_QUADRATIC\_ATTENUATION**</dt></span></span> </dl> | <span data-ttu-id="cd79b-132">Le paramètre *param* est une valeur entière unique qui spécifie l’un des trois facteurs d’atténuation légère.</span><span class="sxs-lookup"><span data-stu-id="cd79b-132">The *param* parameter is a single integer value that specifies one of the three light attenuation factors.</span></span> <span data-ttu-id="cd79b-133">Les valeurs entières et à virgule flottante sont mappées directement.</span><span class="sxs-lookup"><span data-stu-id="cd79b-133">Integer and floating-point values are mapped directly.</span></span> <span data-ttu-id="cd79b-134">Seules les valeurs non négatives sont acceptées.</span><span class="sxs-lookup"><span data-stu-id="cd79b-134">Only nonnegative values are accepted.</span></span> <br/> <span data-ttu-id="cd79b-135">Si la lumière est positionnelle plutôt que directionnelle, son intensité est atténuée par la réciproque de la somme de : le facteur de constante, le facteur linéaire multiplié par la distance entre la lumière et le vertex qui est éclairé et le facteur quadratique multiplié par le carré de la même distance.</span><span class="sxs-lookup"><span data-stu-id="cd79b-135">If the light is positional, rather than directional, its intensity is attenuated by the reciprocal of the sum of: the constant factor, the linear factor multiplied by the distance between the light and the vertex being lighted, and the quadratic factor multiplied by the square of the same distance.</span></span> <span data-ttu-id="cd79b-136">Les facteurs d’atténuation par défaut sont (1, 0, 0), ce qui n’entraîne aucune atténuation.</span><span class="sxs-lookup"><span data-stu-id="cd79b-136">The default attenuation factors are (1,0,0), resulting in no attenuation.</span></span><br/>                   |



 

</dd> <dt>

<span data-ttu-id="cd79b-137">*param*</span><span class="sxs-lookup"><span data-stu-id="cd79b-137">*param*</span></span> 
</dt> <dd>

<span data-ttu-id="cd79b-138">Spécifie la valeur affectée au paramètre *pname* de Light source *Light* .</span><span class="sxs-lookup"><span data-stu-id="cd79b-138">Specifies the value that parameter *pname* of light source *light* will be set to.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cd79b-139">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="cd79b-139">Return value</span></span>

<span data-ttu-id="cd79b-140">Cette fonction ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="cd79b-140">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="cd79b-141">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="cd79b-141">Error codes</span></span>

<span data-ttu-id="cd79b-142">Les codes d’erreur suivants peuvent être récupérés par la fonction [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="cd79b-142">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="cd79b-143">Nom</span><span class="sxs-lookup"><span data-stu-id="cd79b-143">Name</span></span>                                                                                                  | <span data-ttu-id="cd79b-144">Signification</span><span class="sxs-lookup"><span data-stu-id="cd79b-144">Meaning</span></span>                                                                                                                                                                                                                   |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="cd79b-145"><dt>**\_enum GL non valide \_**</dt></span><span class="sxs-lookup"><span data-stu-id="cd79b-145"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="cd79b-146">*Light* ou *pname* n’était pas une valeur acceptée.</span><span class="sxs-lookup"><span data-stu-id="cd79b-146">*light* or *pname* was not an accepted value.</span></span><br/>                                                                                                                                                                  |
| <dl> <span data-ttu-id="cd79b-147"><dt>**\_valeur non valide du GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="cd79b-147"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="cd79b-148">Une valeur d’exposant de point a été spécifiée en dehors de la plage \[ 0, 128 \] ou la coupure de place a été spécifiée en dehors de la plage \[ 0, 90 \] (à l’exception de la valeur spéciale 180) ou un facteur d’atténuation négatif a été spécifié.</span><span class="sxs-lookup"><span data-stu-id="cd79b-148">A spot exponent value was specified outside the range \[0, 128\], or spot cutoff was specified outside the range \[0, 90\] (except for the special value 180), or a negative attenuation factor was specified.</span></span><br/> |
| <dl> <span data-ttu-id="cd79b-149"><dt>**\_opération non valide du GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="cd79b-149"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="cd79b-150">La fonction a été appelée entre un appel à [**glBegin**](glbegin.md) et l’appel correspondant à [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="cd79b-150">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/>                                                                                     |



## <a name="remarks"></a><span data-ttu-id="cd79b-151">Notes</span><span class="sxs-lookup"><span data-stu-id="cd79b-151">Remarks</span></span>

<span data-ttu-id="cd79b-152">La fonction **glLighti** définit la valeur ou les valeurs des paramètres de la source lumineuse individuelle.</span><span class="sxs-lookup"><span data-stu-id="cd79b-152">The **glLighti** function sets the value or values of individual light source parameters.</span></span> <span data-ttu-id="cd79b-153">Le paramètre *Light* nomme la lumière et est un nom symbolique de la forme GL \_ Light *i*, où 0 = *i* < \_ lumières Max GL \_ .</span><span class="sxs-lookup"><span data-stu-id="cd79b-153">The *light* parameter names the light and is a symbolic name of the form GL\_LIGHT *i*, where 0 = *i* < GL\_MAX\_LIGHTS.</span></span>

<span data-ttu-id="cd79b-154">Le paramètre *pname* spécifie l’un des paramètres de la source légère, à nouveau par son nom symbolique.</span><span class="sxs-lookup"><span data-stu-id="cd79b-154">The *pname* parameter specifies one of the light source parameters, again by symbolic name.</span></span> <span data-ttu-id="cd79b-155">Le paramètre *param* est soit une valeur unique, soit un pointeur vers un tableau qui contient les nouvelles valeurs.</span><span class="sxs-lookup"><span data-stu-id="cd79b-155">The *param* parameter is either a single value or a pointer to an array that contains the new values.</span></span>

<span data-ttu-id="cd79b-156">Le calcul de l’éclairage est activé et désactivé à l’aide de [**glEnable**](glenable.md) et [**glDisable**](gldisable.md) avec l’éclairage de l’argument GL \_ .</span><span class="sxs-lookup"><span data-stu-id="cd79b-156">Lighting calculation is enabled and disabled using [**glEnable**](glenable.md) and [**glDisable**](gldisable.md) with argument GL\_LIGHTING.</span></span> <span data-ttu-id="cd79b-157">Lorsque l’éclairage est activé, les sources lumineuses activées contribuent au calcul de l’éclairage.</span><span class="sxs-lookup"><span data-stu-id="cd79b-157">When lighting is enabled, light sources that are enabled contribute to the lighting calculation.</span></span> <span data-ttu-id="cd79b-158">Source de lumière *i* est activée et désactivée à l’aide de **glEnable** et **glDisable** avec l’argument GL \_ Light *i*.</span><span class="sxs-lookup"><span data-stu-id="cd79b-158">Light source *i* is enabled and disabled using **glEnable** and **glDisable** with argument GL\_LIGHT *i*.</span></span>

<span data-ttu-id="cd79b-159">C’est toujours le cas que GL \_ Light *i* = GL \_ LIGHT0 + *i*.</span><span class="sxs-lookup"><span data-stu-id="cd79b-159">It is always the case that GL\_LIGHT *i* = GL\_LIGHT0 + *i*.</span></span>

<span data-ttu-id="cd79b-160">Les fonctions suivantes récupèrent les informations relatives à la fonction **glLighti** :</span><span class="sxs-lookup"><span data-stu-id="cd79b-160">The following functions retrieve information related to the **glLighti** function:</span></span>

[<span data-ttu-id="cd79b-161">**glGetLight**</span><span class="sxs-lookup"><span data-stu-id="cd79b-161">**glGetLight**</span></span>](glgetlight.md)

<span data-ttu-id="cd79b-162">[**glIsEnabled**](glisenabled.md) avec argument GL \_ Lighting</span><span class="sxs-lookup"><span data-stu-id="cd79b-162">[**glIsEnabled**](glisenabled.md) with argument GL\_LIGHTING</span></span>

## <a name="requirements"></a><span data-ttu-id="cd79b-163">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="cd79b-163">Requirements</span></span>



| <span data-ttu-id="cd79b-164">Condition requise</span><span class="sxs-lookup"><span data-stu-id="cd79b-164">Requirement</span></span> | <span data-ttu-id="cd79b-165">Valeur</span><span class="sxs-lookup"><span data-stu-id="cd79b-165">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="cd79b-166">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cd79b-166">Minimum supported client</span></span><br/> | <span data-ttu-id="cd79b-167">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="cd79b-167">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="cd79b-168">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cd79b-168">Minimum supported server</span></span><br/> | <span data-ttu-id="cd79b-169">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="cd79b-169">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="cd79b-170">En-tête</span><span class="sxs-lookup"><span data-stu-id="cd79b-170">Header</span></span><br/>                   | <dl> <span data-ttu-id="cd79b-171"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="cd79b-171"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="cd79b-172">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="cd79b-172">Library</span></span><br/>                  | <dl> <span data-ttu-id="cd79b-173"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="cd79b-173"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="cd79b-174">DLL</span><span class="sxs-lookup"><span data-stu-id="cd79b-174">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cd79b-175"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cd79b-175"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cd79b-176">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cd79b-176">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cd79b-177">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="cd79b-177">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="cd79b-178">**glColorMaterial**</span><span class="sxs-lookup"><span data-stu-id="cd79b-178">**glColorMaterial**</span></span>](glcolormaterial.md)
</dt> <dt>

[<span data-ttu-id="cd79b-179">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="cd79b-179">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="cd79b-180">**glLightModel**</span><span class="sxs-lookup"><span data-stu-id="cd79b-180">**glLightModel**</span></span>](gllightmodel-functions.md)
</dt> <dt>

[<span data-ttu-id="cd79b-181">**glMaterial**</span><span class="sxs-lookup"><span data-stu-id="cd79b-181">**glMaterial**</span></span>](glmaterial-functions.md)
</dt> </dl>

 

 





