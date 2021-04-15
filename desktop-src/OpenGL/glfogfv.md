---
title: glFogfv, fonction (Gl.h)
description: La fonction glFogfv spécifie des paramètres de brouillard. | fonction glFogfv (GL. h)
ms.assetid: a2243ff4-4f3a-4b8c-b4fb-ce2cd74815e4
keywords:
- glFogfv fonction OpenGL
topic_type:
- apiref
api_name:
- glFogfv
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b407dd9b9c984a744e903a2c269d21028d32977a
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104211640"
---
# <a name="glfogfv-function"></a><span data-ttu-id="99674-105">glFogfv fonction)</span><span class="sxs-lookup"><span data-stu-id="99674-105">glFogfv function</span></span>

<span data-ttu-id="99674-106">La fonction **glFogfv** spécifie des paramètres de brouillard.</span><span class="sxs-lookup"><span data-stu-id="99674-106">The **glFogfv** function specifies fog parameters.</span></span>

## <a name="syntax"></a><span data-ttu-id="99674-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="99674-107">Syntax</span></span>


```C++
void WINAPI glFogfv(
         GLenum  pname,
   const GLfloat *params
);
```



## <a name="parameters"></a><span data-ttu-id="99674-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="99674-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="99674-109">*pname*</span><span class="sxs-lookup"><span data-stu-id="99674-109">*pname*</span></span> 
</dt> <dd>

<span data-ttu-id="99674-110">Spécifie un paramètre de brouillard.</span><span class="sxs-lookup"><span data-stu-id="99674-110">Specifies a fog parameter.</span></span>

<span data-ttu-id="99674-111">Accepte l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="99674-111">Accepts one of the following values.</span></span>



| <span data-ttu-id="99674-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="99674-112">Value</span></span>                                                                                                                                                             | <span data-ttu-id="99674-113">Signification</span><span class="sxs-lookup"><span data-stu-id="99674-113">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                             |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_FOG_MODE"></span><span id="gl_fog_mode"></span><dl> <span data-ttu-id="99674-114"><dt>**\_mode de brouillard GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="99674-114"><dt>**GL\_FOG\_MODE**</dt></span></span> </dl>          | <span data-ttu-id="99674-115">Le paramètre *params* est une valeur à virgule flottante qui spécifie l’équation à utiliser pour calculer le facteur de mélange de brouillard, *f*.</span><span class="sxs-lookup"><span data-stu-id="99674-115">The *params* parameter is a floating-point value that specifies the equation to be used to compute the fog blend factor, *f*.</span></span> <span data-ttu-id="99674-116">Trois constantes symboliques sont acceptées : GL \_ Linear, GL \_ exp et GL \_ EXP2.</span><span class="sxs-lookup"><span data-stu-id="99674-116">Three symbolic constants are accepted: GL\_LINEAR, GL\_EXP, and GL\_EXP2.</span></span> <span data-ttu-id="99674-117">Les équations correspondant à ces constantes symboliques sont définies dans la section Notes suivante.</span><span class="sxs-lookup"><span data-stu-id="99674-117">The equations corresponding to these symbolic constants are defined in the following Remarks section.</span></span> <span data-ttu-id="99674-118">Le mode de brouillard par défaut est GL \_ exp.</span><span class="sxs-lookup"><span data-stu-id="99674-118">The default fog mode is GL\_EXP.</span></span><br/>                                                                           |
| <span id="GL_FOG_DENSITY"></span><span id="gl_fog_density"></span><dl> <span data-ttu-id="99674-119"><dt>**\_densité de brouillard GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="99674-119"><dt>**GL\_FOG\_DENSITY**</dt></span></span> </dl> | <span data-ttu-id="99674-120">Le paramètre *params* est une valeur à virgule flottante qui spécifie la *densité*, la densité de brouillards utilisée dans les deux équations de brouillard exponentiel.</span><span class="sxs-lookup"><span data-stu-id="99674-120">The *params* parameter is a floating-point value that specifies *density*, the fog density used in both exponential fog equations.</span></span> <span data-ttu-id="99674-121">Seules les densités non négatives sont acceptées.</span><span class="sxs-lookup"><span data-stu-id="99674-121">Only nonnegative densities are accepted.</span></span> <span data-ttu-id="99674-122">La densité de brouillard par défaut est 1,0.</span><span class="sxs-lookup"><span data-stu-id="99674-122">The default fog density is 1.0.</span></span><br/>                                                                                                                                                                                                              |
| <span id="GL_FOG_START"></span><span id="gl_fog_start"></span><dl> <span data-ttu-id="99674-123"><dt>**\_début du brouillard GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="99674-123"><dt>**GL\_FOG\_START**</dt></span></span> </dl>       | <span data-ttu-id="99674-124">Le paramètre *params* est une valeur à virgule flottante qui spécifie *Start*, la distance la plus proche utilisée dans l’équation de brouillard linéaire.</span><span class="sxs-lookup"><span data-stu-id="99674-124">The *params* parameter is a floating-point value that specifies *start*, the near distance used in the linear fog equation.</span></span> <span data-ttu-id="99674-125">La distance proche par défaut est 0,0.</span><span class="sxs-lookup"><span data-stu-id="99674-125">The default near distance is 0.0.</span></span><br/>                                                                                                                                                                                                                                                            |
| <span id="GL_FOG_END"></span><span id="gl_fog_end"></span><dl> <span data-ttu-id="99674-126"><dt>**\_fin du brouillard comptable \_**</dt></span><span class="sxs-lookup"><span data-stu-id="99674-126"><dt>**GL\_FOG\_END**</dt></span></span> </dl>             | <span data-ttu-id="99674-127">Le paramètre *params* est une valeur à virgule flottante qui spécifie *end*, la distance la plus éloignée utilisée dans l’équation de brouillard linéaire.</span><span class="sxs-lookup"><span data-stu-id="99674-127">The *params* parameter is a floating-point value that specifies *end*, the far distance used in the linear fog equation.</span></span> <span data-ttu-id="99674-128">La distance éloignée par défaut est 1,0.</span><span class="sxs-lookup"><span data-stu-id="99674-128">The default far distance is 1.0.</span></span><br/>                                                                                                                                                                                                                                                                |
| <span id="GL_FOG_INDEX"></span><span id="gl_fog_index"></span><dl> <span data-ttu-id="99674-129"><dt>**\_index de brouillard GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="99674-129"><dt>**GL\_FOG\_INDEX**</dt></span></span> </dl>       | <span data-ttu-id="99674-130">Le paramètre *params* est une valeur à virgule flottante qui spécifie *i*<sub>f</sub> , l’index de couleur de brouillard.</span><span class="sxs-lookup"><span data-stu-id="99674-130">The *params* parameter is a floating-point value that specifies *i*<sub>f</sub> , the fog color index.</span></span> <span data-ttu-id="99674-131">L’index de brouillard par défaut est 0,0.</span><span class="sxs-lookup"><span data-stu-id="99674-131">The default fog index is 0.0.</span></span><br/>                                                                                                                                                                                                                                                                                     |
| <span id="GL_FOG_COLOR"></span><span id="gl_fog_color"></span><dl> <span data-ttu-id="99674-132"><dt>**\_couleur de brouillard GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="99674-132"><dt>**GL\_FOG\_COLOR**</dt></span></span> </dl>       | <span data-ttu-id="99674-133">Le paramètre *params* contient quatre valeurs à virgule flottante qui spécifient *C*<sub>f</sub> , la couleur de brouillard.</span><span class="sxs-lookup"><span data-stu-id="99674-133">The *params* parameter contains four floating-point values that specify *C*<sub>f</sub> , the fog color.</span></span> <span data-ttu-id="99674-134">Les valeurs entières sont mappées de façon linéaire de telle sorte que la valeur représentable la plus positive corresponde à 1,0, et la valeur représentable la plus négative correspond à-1,0.</span><span class="sxs-lookup"><span data-stu-id="99674-134">Integer values are mapped linearly such that the most positive representable value maps to 1.0, and the most negative representable value maps to -1.0.</span></span> <span data-ttu-id="99674-135">Les valeurs à virgule flottante sont mappées directement.</span><span class="sxs-lookup"><span data-stu-id="99674-135">Floating-point values are mapped directly.</span></span> <span data-ttu-id="99674-136">Après la conversion, tous les composants de couleur sont ancrés à la plage \[ 0, 1 \] .</span><span class="sxs-lookup"><span data-stu-id="99674-136">After conversion, all color components are clamped to the range \[0,1\].</span></span> <span data-ttu-id="99674-137">La couleur de brouillard par défaut est (0, 0, 0, 0).</span><span class="sxs-lookup"><span data-stu-id="99674-137">The default fog color is (0,0,0,0).</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="99674-138">*params*</span><span class="sxs-lookup"><span data-stu-id="99674-138">*params*</span></span> 
</dt> <dd>

<span data-ttu-id="99674-139">Spécifie la ou les valeurs à assigner à *pname*.</span><span class="sxs-lookup"><span data-stu-id="99674-139">Specifies the value or values to be assigned to *pname*.</span></span> <span data-ttu-id="99674-140">La \_ \_ couleur de brouillard GL requiert un tableau de quatre valeurs.</span><span class="sxs-lookup"><span data-stu-id="99674-140">GL\_FOG\_COLOR requires an array of four values.</span></span> <span data-ttu-id="99674-141">Tous les autres paramètres acceptent un tableau contenant une seule valeur.</span><span class="sxs-lookup"><span data-stu-id="99674-141">All other parameters accept an array containing only a single value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="99674-142">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="99674-142">Return value</span></span>

<span data-ttu-id="99674-143">Cette fonction ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="99674-143">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="99674-144">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="99674-144">Error codes</span></span>

<span data-ttu-id="99674-145">Les codes d’erreur suivants peuvent être récupérés par la fonction [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="99674-145">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="99674-146">Nom</span><span class="sxs-lookup"><span data-stu-id="99674-146">Name</span></span>                                                                                                  | <span data-ttu-id="99674-147">Signification</span><span class="sxs-lookup"><span data-stu-id="99674-147">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="99674-148"><dt>**\_enum GL non valide \_**</dt></span><span class="sxs-lookup"><span data-stu-id="99674-148"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="99674-149">*pname* n’est pas une valeur acceptée.</span><span class="sxs-lookup"><span data-stu-id="99674-149">*pname* was not an accepted value.</span></span><br/>                                                                                         |
| <dl> <span data-ttu-id="99674-150"><dt>**\_opération non valide du GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="99674-150"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="99674-151">La fonction a été appelée entre un appel à [**glBegin**](glbegin.md) et l’appel correspondant à [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="99674-151">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="99674-152">Notes</span><span class="sxs-lookup"><span data-stu-id="99674-152">Remarks</span></span>

<span data-ttu-id="99674-153">Vous activez et désactivez le brouillard avec [**glEnable**](glenable.md) et [**glDisable**](gldisable.md), à l’aide de l’argument GL \_ Fog.</span><span class="sxs-lookup"><span data-stu-id="99674-153">You enable and disable fog with [**glEnable**](glenable.md) and [**glDisable**](gldisable.md), using the argument GL\_FOG.</span></span> <span data-ttu-id="99674-154">Bien qu’activé, le brouillard affecte les géométries pixellisées, les bitmaps et les blocs de pixels, mais pas les opérations d’effacement de la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="99674-154">While enabled, fog affects rasterized geometry, bitmaps, and pixel blocks, but not buffer-clear operations.</span></span>

<span data-ttu-id="99674-155">La fonction **glFogfv** assigne la ou les *valeurs dans les paramètres au* paramètre de brouillard spécifié par *pname*.</span><span class="sxs-lookup"><span data-stu-id="99674-155">The **glFogfv** function assigns the value or values in *params* to the fog parameter specified by *pname*.</span></span>

<span data-ttu-id="99674-156">Le brouillard fusionne une couleur de brouillard avec chaque couleur de posttexturing du fragment de pixel pixellisé à l’aide d’un facteur de fusion *f*.</span><span class="sxs-lookup"><span data-stu-id="99674-156">Fog blends a fog color with each rasterized pixel fragment's posttexturing color using a blending factor *f*.</span></span> <span data-ttu-id="99674-157">Factor *f* est calculé de l’une des trois façons suivantes, en fonction du mode de brouillard.</span><span class="sxs-lookup"><span data-stu-id="99674-157">Factor *f* is computed in one of three ways, depending on the fog mode.</span></span> <span data-ttu-id="99674-158">Indiquez *z* comme distance en coordonnées oculaires à partir de l’origine jusqu’au fragment à la une.</span><span class="sxs-lookup"><span data-stu-id="99674-158">Let *z* be the distance in eye coordinates from the origin to the fragment being fogged.</span></span> <span data-ttu-id="99674-159">L’équation du \_ brouillard linéaire du GL est la suivante :</span><span class="sxs-lookup"><span data-stu-id="99674-159">The equation for GL\_LINEAR fog is:</span></span>

![Équation qui indique la valeur de GL_LINEAR brouillard.](images/fog01.png)

<span data-ttu-id="99674-161">L’équation du brouillard du GL \_ exp est la suivante :</span><span class="sxs-lookup"><span data-stu-id="99674-161">The equation for GL\_EXP fog is:</span></span>

![Équation représentant la valeur du facteur de fusion en GL_EXP mode de brouillard.](images/fog02.png)

<span data-ttu-id="99674-163">L’équation du \_ brouillard EXP2 GL est la suivante :</span><span class="sxs-lookup"><span data-stu-id="99674-163">The equation for GL\_EXP2 fog is:</span></span>

![Équation représentant la valeur du facteur de fusion en GL_EXP2 mode de brouillard.](images/fog03.png)

<span data-ttu-id="99674-165">Quel que soit le mode de brouillard, *f* est ancré à la plage \[ 0, 1 \] après le calcul.</span><span class="sxs-lookup"><span data-stu-id="99674-165">Regardless of the fog mode, *f* is clamped to the range \[0,1\] after it is computed.</span></span> <span data-ttu-id="99674-166">Ensuite, si OpenGL est en mode de couleurs RVBA, la couleur du fragment *C*<sub>r</sub> est remplacée par</span><span class="sxs-lookup"><span data-stu-id="99674-166">Then, if OpenGL is in RGBA color mode, the fragment's color *C*<sub>r</sub> is replaced by</span></span>

![Équation qui indique la couleur du fragment-brouillard en fonction du facteur de fusion et de la couleur de brouillard.](images/fog04.png)

<span data-ttu-id="99674-168">En mode *d’index des* couleurs, l’index de couleurs du <sub>fragment est remplacé</sub> par</span><span class="sxs-lookup"><span data-stu-id="99674-168">In color-index mode, the fragment's color index *i*<sub>r</sub> is replaced by</span></span>

![Équation représentant l’index de couleurs du fragment à l’échelle du monde en tant que fonction du facteur de fusion et de la couleur indexée.](images/fog05.png)

<span data-ttu-id="99674-170">Les fonctions suivantes récupèrent les informations relatives aux fonctions **glFog** :</span><span class="sxs-lookup"><span data-stu-id="99674-170">The following functions retrieve information related to the **glFog** functions:</span></span>

<span data-ttu-id="99674-171">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) avec argument GL \_ - \_ couleur de brouillard</span><span class="sxs-lookup"><span data-stu-id="99674-171">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_FOG\_COLOR</span></span>

<span data-ttu-id="99674-172">**glGet** avec l' \_ index de brouillard de GL d’argument \_</span><span class="sxs-lookup"><span data-stu-id="99674-172">**glGet** with argument GL\_FOG\_INDEX</span></span>

<span data-ttu-id="99674-173">**glGet** avec argument GL \_ - \_ densité de brouillard</span><span class="sxs-lookup"><span data-stu-id="99674-173">**glGet** with argument GL\_FOG\_DENSITY</span></span>

<span data-ttu-id="99674-174">**glGet** avec argument de \_ début de brouillard GL \_</span><span class="sxs-lookup"><span data-stu-id="99674-174">**glGet** with argument GL\_FOG\_START</span></span>

<span data-ttu-id="99674-175">**glGet** avec argument GL de \_ brouillard de \_ fin</span><span class="sxs-lookup"><span data-stu-id="99674-175">**glGet** with argument GL\_FOG\_END</span></span>

<span data-ttu-id="99674-176">**glGet** avec argument GL de \_ brouillard \_ en mode</span><span class="sxs-lookup"><span data-stu-id="99674-176">**glGet** with argument GL\_FOG\_MODE</span></span>

<span data-ttu-id="99674-177">[**glIsEnabled**](glisenabled.md) avec argument de brouillard de la comptabilité \_</span><span class="sxs-lookup"><span data-stu-id="99674-177">[**glIsEnabled**](glisenabled.md) with argument GL\_FOG</span></span>

## <a name="requirements"></a><span data-ttu-id="99674-178">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="99674-178">Requirements</span></span>



| <span data-ttu-id="99674-179">Condition requise</span><span class="sxs-lookup"><span data-stu-id="99674-179">Requirement</span></span> | <span data-ttu-id="99674-180">Valeur</span><span class="sxs-lookup"><span data-stu-id="99674-180">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="99674-181">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="99674-181">Minimum supported client</span></span><br/> | <span data-ttu-id="99674-182">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="99674-182">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="99674-183">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="99674-183">Minimum supported server</span></span><br/> | <span data-ttu-id="99674-184">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="99674-184">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="99674-185">En-tête</span><span class="sxs-lookup"><span data-stu-id="99674-185">Header</span></span><br/>                   | <dl> <span data-ttu-id="99674-186"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="99674-186"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="99674-187">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="99674-187">Library</span></span><br/>                  | <dl> <span data-ttu-id="99674-188"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="99674-188"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="99674-189">DLL</span><span class="sxs-lookup"><span data-stu-id="99674-189">DLL</span></span><br/>                      | <dl> <span data-ttu-id="99674-190"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="99674-190"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="99674-191">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="99674-191">See also</span></span>

<dl> <dt>

[<span data-ttu-id="99674-192">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="99674-192">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="99674-193">**glDisable**</span><span class="sxs-lookup"><span data-stu-id="99674-193">**glDisable**</span></span>](gldisable.md)
</dt> <dt>

[<span data-ttu-id="99674-194">**glEnable**</span><span class="sxs-lookup"><span data-stu-id="99674-194">**glEnable**</span></span>](glenable.md)
</dt> <dt>

[<span data-ttu-id="99674-195">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="99674-195">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="99674-196">**glGet**</span><span class="sxs-lookup"><span data-stu-id="99674-196">**glGet**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[<span data-ttu-id="99674-197">**glIsEnabled**</span><span class="sxs-lookup"><span data-stu-id="99674-197">**glIsEnabled**</span></span>](glisenabled.md)
</dt> </dl>

 

 





