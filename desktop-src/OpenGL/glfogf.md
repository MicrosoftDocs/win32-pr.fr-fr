---
title: glFogf, fonction (Gl.h)
description: GlFogf et Function spécifient des paramètres de brouillard.
ms.assetid: 69961d8f-385c-4353-aef3-38fb654c44f8
keywords:
- glFogf fonction OpenGL
topic_type:
- apiref
api_name:
- glFogf
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dfe0509b30e91797752604110068701fcedaa266
ms.sourcegitcommit: 7ef31bf778e76ce4196205d4c4c632fbdc649805
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/05/2021
ms.locfileid: "104042895"
---
# <a name="glfogf-function"></a><span data-ttu-id="f9f9e-104">glFogf fonction)</span><span class="sxs-lookup"><span data-stu-id="f9f9e-104">glFogf function</span></span>

<span data-ttu-id="f9f9e-105">**GlFogf** et Function spécifient des paramètres de brouillard.</span><span class="sxs-lookup"><span data-stu-id="f9f9e-105">The **glFogf** and function specifies fog parameters.</span></span>

## <a name="syntax"></a><span data-ttu-id="f9f9e-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f9f9e-106">Syntax</span></span>


```C++
void WINAPI glFogf(
   GLenum  pname,
   GLfloat param
);
```



## <a name="parameters"></a><span data-ttu-id="f9f9e-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f9f9e-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f9f9e-108">*pname*</span><span class="sxs-lookup"><span data-stu-id="f9f9e-108">*pname*</span></span> 
</dt> <dd>

<span data-ttu-id="f9f9e-109">Spécifie un paramètre de brouillard à valeur unique.</span><span class="sxs-lookup"><span data-stu-id="f9f9e-109">Specifies a single-valued fog parameter.</span></span>

<span data-ttu-id="f9f9e-110">Accepte l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="f9f9e-110">Accepts one of the following values.</span></span>



| <span data-ttu-id="f9f9e-111">Valeur</span><span class="sxs-lookup"><span data-stu-id="f9f9e-111">Value</span></span>                                                                                                                                                             | <span data-ttu-id="f9f9e-112">Signification</span><span class="sxs-lookup"><span data-stu-id="f9f9e-112">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                          |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_FOG_MODE"></span><span id="gl_fog_mode"></span><dl> <span data-ttu-id="f9f9e-113"><dt>**\_mode de brouillard GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="f9f9e-113"><dt>**GL\_FOG\_MODE**</dt></span></span> </dl>          | <span data-ttu-id="f9f9e-114">Le paramètre *params* est une valeur à virgule flottante unique qui spécifie l’équation à utiliser pour calculer le facteur de mélange de brouillard, *f*.</span><span class="sxs-lookup"><span data-stu-id="f9f9e-114">The *params* parameter is a single floating-point value that specifies the equation to be used to compute the fog blend factor, *f*.</span></span> <span data-ttu-id="f9f9e-115">Trois constantes symboliques sont acceptées : GL \_ Linear, GL \_ exp et GL \_ EXP2.</span><span class="sxs-lookup"><span data-stu-id="f9f9e-115">Three symbolic constants are accepted: GL\_LINEAR, GL\_EXP, and GL\_EXP2.</span></span> <span data-ttu-id="f9f9e-116">Les équations correspondant à ces constantes symboliques sont définies dans la section Notes suivante.</span><span class="sxs-lookup"><span data-stu-id="f9f9e-116">The equations corresponding to these symbolic constants are defined in the following Remarks section.</span></span> <span data-ttu-id="f9f9e-117">Le mode de brouillard par défaut est GL \_ exp.</span><span class="sxs-lookup"><span data-stu-id="f9f9e-117">The default fog mode is GL\_EXP.</span></span><br/> |
| <span id="GL_FOG_DENSITY"></span><span id="gl_fog_density"></span><dl> <span data-ttu-id="f9f9e-118"><dt>**\_densité de brouillard GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="f9f9e-118"><dt>**GL\_FOG\_DENSITY**</dt></span></span> </dl> | <span data-ttu-id="f9f9e-119">Le paramètre *params* est une valeur à virgule flottante unique qui spécifie la *densité*, la densité de brouillards utilisée dans les deux équations de brouillard exponentiels.</span><span class="sxs-lookup"><span data-stu-id="f9f9e-119">The *params* parameter is a single floating-point value that specifies *density*, the fog density used in both exponential fog equations.</span></span> <span data-ttu-id="f9f9e-120">Seules les densités non négatives sont acceptées.</span><span class="sxs-lookup"><span data-stu-id="f9f9e-120">Only nonnegative densities are accepted.</span></span> <span data-ttu-id="f9f9e-121">La densité de brouillard par défaut est 1,0.</span><span class="sxs-lookup"><span data-stu-id="f9f9e-121">The default fog density is 1.0.</span></span><br/>                                                                                                                                    |
| <span id="GL_FOG_START"></span><span id="gl_fog_start"></span><dl> <span data-ttu-id="f9f9e-122"><dt>**\_début du brouillard GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="f9f9e-122"><dt>**GL\_FOG\_START**</dt></span></span> </dl>       | <span data-ttu-id="f9f9e-123">Le paramètre *params* est une valeur à virgule flottante unique qui spécifie *Start*, la distance la plus proche utilisée dans l’équation de brouillard linéaire.</span><span class="sxs-lookup"><span data-stu-id="f9f9e-123">The *params* parameter is a single floating-point value that specifies *start*, the near distance used in the linear fog equation.</span></span> <span data-ttu-id="f9f9e-124">La distance proche par défaut est 0,0.</span><span class="sxs-lookup"><span data-stu-id="f9f9e-124">The default near distance is 0.0.</span></span><br/>                                                                                                                                                                                  |
| <span id="GL_FOG_END"></span><span id="gl_fog_end"></span><dl> <span data-ttu-id="f9f9e-125"><dt>**\_fin du brouillard comptable \_**</dt></span><span class="sxs-lookup"><span data-stu-id="f9f9e-125"><dt>**GL\_FOG\_END**</dt></span></span> </dl>             | <span data-ttu-id="f9f9e-126">Le paramètre *params* est une valeur à virgule flottante unique qui spécifie *end*, la distance utilisée dans l’équation de brouillard linéaire.</span><span class="sxs-lookup"><span data-stu-id="f9f9e-126">The *params* parameter is a single floating-point value that specifies *end*, the far distance used in the linear fog equation.</span></span> <span data-ttu-id="f9f9e-127">La distance éloignée par défaut est 1,0.</span><span class="sxs-lookup"><span data-stu-id="f9f9e-127">The default far distance is 1.0.</span></span><br/>                                                                                                                                                                                      |
| <span id="GL_FOG_INDEX"></span><span id="gl_fog_index"></span><dl> <span data-ttu-id="f9f9e-128"><dt>**\_index de brouillard GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="f9f9e-128"><dt>**GL\_FOG\_INDEX**</dt></span></span> </dl>       | <span data-ttu-id="f9f9e-129">Le paramètre *params* est une valeur à virgule flottante unique qui spécifie *i*<sub>f</sub> , l’index de couleur de brouillard.</span><span class="sxs-lookup"><span data-stu-id="f9f9e-129">The *params* parameter is a single floating-point value that specifies *i*<sub>f</sub> , the fog color index.</span></span> <span data-ttu-id="f9f9e-130">L’index de brouillard par défaut est 0,0.</span><span class="sxs-lookup"><span data-stu-id="f9f9e-130">The default fog index is 0.0.</span></span><br/>                                                                                                                                                                                                           |



 

</dd> <dt>

<span data-ttu-id="f9f9e-131">*param*</span><span class="sxs-lookup"><span data-stu-id="f9f9e-131">*param*</span></span> 
</dt> <dd>

<span data-ttu-id="f9f9e-132">Spécifie la valeur à laquelle *pname* sera définie.</span><span class="sxs-lookup"><span data-stu-id="f9f9e-132">Specifies the value that *pname* will be set to.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f9f9e-133">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="f9f9e-133">Return value</span></span>

<span data-ttu-id="f9f9e-134">Cette fonction ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="f9f9e-134">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="f9f9e-135">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="f9f9e-135">Error codes</span></span>

<span data-ttu-id="f9f9e-136">Les codes d’erreur suivants peuvent être récupérés par la fonction [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="f9f9e-136">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="f9f9e-137">Nom</span><span class="sxs-lookup"><span data-stu-id="f9f9e-137">Name</span></span>                                                                                                  | <span data-ttu-id="f9f9e-138">Signification</span><span class="sxs-lookup"><span data-stu-id="f9f9e-138">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="f9f9e-139"><dt>**\_enum GL non valide \_**</dt></span><span class="sxs-lookup"><span data-stu-id="f9f9e-139"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="f9f9e-140">*pname* n’est pas une valeur acceptée.</span><span class="sxs-lookup"><span data-stu-id="f9f9e-140">*pname* was not an accepted value.</span></span><br/>                                                                                         |
| <dl> <span data-ttu-id="f9f9e-141"><dt>**\_opération non valide du GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="f9f9e-141"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="f9f9e-142">La fonction a été appelée entre un appel à [**glBegin**](glbegin.md) et l’appel correspondant à [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="f9f9e-142">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="f9f9e-143">Notes</span><span class="sxs-lookup"><span data-stu-id="f9f9e-143">Remarks</span></span>

<span data-ttu-id="f9f9e-144">Vous activez et désactivez le brouillard avec [**glEnable**](glenable.md) et [**glDisable**](gldisable.md), à l’aide de l’argument GL \_ Fog.</span><span class="sxs-lookup"><span data-stu-id="f9f9e-144">You enable and disable fog with [**glEnable**](glenable.md) and [**glDisable**](gldisable.md), using the argument GL\_FOG.</span></span> <span data-ttu-id="f9f9e-145">Bien qu’activé, le brouillard affecte les géométries pixellisées, les bitmaps et les blocs de pixels, mais pas les opérations d’effacement de la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="f9f9e-145">While enabled, fog affects rasterized geometry, bitmaps, and pixel blocks, but not buffer-clear operations.</span></span>

<span data-ttu-id="f9f9e-146">La fonction **glFogf** assigne la ou les *valeurs dans les paramètres au* paramètre de brouillard spécifié par *pname*.</span><span class="sxs-lookup"><span data-stu-id="f9f9e-146">The **glFogf** function assigns the value or values in *params* to the fog parameter specified by *pname*.</span></span>

<span data-ttu-id="f9f9e-147">Le brouillard fusionne une couleur de brouillard avec chaque couleur de posttexturing du fragment de pixel pixellisé à l’aide d’un facteur de fusion *f*.</span><span class="sxs-lookup"><span data-stu-id="f9f9e-147">Fog blends a fog color with each rasterized pixel fragment's posttexturing color using a blending factor *f*.</span></span> <span data-ttu-id="f9f9e-148">Factor *f* est calculé de l’une des trois façons suivantes, en fonction du mode de brouillard.</span><span class="sxs-lookup"><span data-stu-id="f9f9e-148">Factor *f* is computed in one of three ways, depending on the fog mode.</span></span> <span data-ttu-id="f9f9e-149">Indiquez *z* comme distance en coordonnées oculaires à partir de l’origine jusqu’au fragment à la une.</span><span class="sxs-lookup"><span data-stu-id="f9f9e-149">Let *z* be the distance in eye coordinates from the origin to the fragment being fogged.</span></span> <span data-ttu-id="f9f9e-150">L’équation du \_ brouillard linéaire du GL est la suivante :</span><span class="sxs-lookup"><span data-stu-id="f9f9e-150">The equation for GL\_LINEAR fog is:</span></span>

![Équation qui indique la valeur de GL_LINEAR brouillard.](images/fog01.png)

<span data-ttu-id="f9f9e-152">L’équation du brouillard du GL \_ exp est la suivante :</span><span class="sxs-lookup"><span data-stu-id="f9f9e-152">The equation for GL\_EXP fog is:</span></span>

![Équation représentant la valeur du facteur de fusion en GL_EXP mode de brouillard.](images/fog02.png)

<span data-ttu-id="f9f9e-154">L’équation du \_ brouillard EXP2 GL est la suivante :</span><span class="sxs-lookup"><span data-stu-id="f9f9e-154">The equation for GL\_EXP2 fog is:</span></span>

![Équation représentant la valeur du facteur de fusion en GL_EXP2 mode de brouillard.](images/fog03.png)

<span data-ttu-id="f9f9e-156">Quel que soit le mode de brouillard, *f* est ancré à la plage \[ 0, 1 \] après le calcul.</span><span class="sxs-lookup"><span data-stu-id="f9f9e-156">Regardless of the fog mode, *f* is clamped to the range \[0,1\] after it is computed.</span></span> <span data-ttu-id="f9f9e-157">Ensuite, si OpenGL est en mode de couleurs RVBA, la couleur du fragment *C*<sub>r</sub> est remplacée par</span><span class="sxs-lookup"><span data-stu-id="f9f9e-157">Then, if OpenGL is in RGBA color mode, the fragment's color *C*<sub>r</sub> is replaced by</span></span>

![Équation qui indique la couleur du fragment-brouillard en fonction du facteur de fusion et de la couleur de brouillard.](images/fog04.png)

<span data-ttu-id="f9f9e-159">En mode *d’index des* couleurs, l’index de couleurs du <sub>fragment est remplacé</sub> par</span><span class="sxs-lookup"><span data-stu-id="f9f9e-159">In color-index mode, the fragment's color index *i*<sub>r</sub> is replaced by</span></span>

![Équation représentant l’index de couleurs du fragment à l’échelle du monde en tant que fonction du facteur de fusion et de la couleur indexée.](images/fog05.png)

<span data-ttu-id="f9f9e-161">Les fonctions suivantes récupèrent les informations relatives aux fonctions **glFog** :</span><span class="sxs-lookup"><span data-stu-id="f9f9e-161">The following functions retrieve information related to the **glFog** functions:</span></span>

<span data-ttu-id="f9f9e-162">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) avec argument GL \_ - \_ couleur de brouillard</span><span class="sxs-lookup"><span data-stu-id="f9f9e-162">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_FOG\_COLOR</span></span>

<span data-ttu-id="f9f9e-163">**glGet** avec l' \_ index de brouillard de GL d’argument \_</span><span class="sxs-lookup"><span data-stu-id="f9f9e-163">**glGet** with argument GL\_FOG\_INDEX</span></span>

<span data-ttu-id="f9f9e-164">**glGet** avec argument GL \_ - \_ densité de brouillard</span><span class="sxs-lookup"><span data-stu-id="f9f9e-164">**glGet** with argument GL\_FOG\_DENSITY</span></span>

<span data-ttu-id="f9f9e-165">**glGet** avec argument de \_ début de brouillard GL \_</span><span class="sxs-lookup"><span data-stu-id="f9f9e-165">**glGet** with argument GL\_FOG\_START</span></span>

<span data-ttu-id="f9f9e-166">**glGet** avec argument GL de \_ brouillard de \_ fin</span><span class="sxs-lookup"><span data-stu-id="f9f9e-166">**glGet** with argument GL\_FOG\_END</span></span>

<span data-ttu-id="f9f9e-167">**glGet** avec argument GL de \_ brouillard \_ en mode</span><span class="sxs-lookup"><span data-stu-id="f9f9e-167">**glGet** with argument GL\_FOG\_MODE</span></span>

<span data-ttu-id="f9f9e-168">[**glIsEnabled**](glisenabled.md) avec argument de brouillard de la comptabilité \_</span><span class="sxs-lookup"><span data-stu-id="f9f9e-168">[**glIsEnabled**](glisenabled.md) with argument GL\_FOG</span></span>

## <a name="requirements"></a><span data-ttu-id="f9f9e-169">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f9f9e-169">Requirements</span></span>



| <span data-ttu-id="f9f9e-170">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f9f9e-170">Requirement</span></span> | <span data-ttu-id="f9f9e-171">Valeur</span><span class="sxs-lookup"><span data-stu-id="f9f9e-171">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f9f9e-172">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f9f9e-172">Minimum supported client</span></span><br/> | <span data-ttu-id="f9f9e-173">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f9f9e-173">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="f9f9e-174">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f9f9e-174">Minimum supported server</span></span><br/> | <span data-ttu-id="f9f9e-175">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f9f9e-175">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="f9f9e-176">En-tête</span><span class="sxs-lookup"><span data-stu-id="f9f9e-176">Header</span></span><br/>                   | <dl> <span data-ttu-id="f9f9e-177"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="f9f9e-177"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="f9f9e-178">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="f9f9e-178">Library</span></span><br/>                  | <dl> <span data-ttu-id="f9f9e-179"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f9f9e-179"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="f9f9e-180">DLL</span><span class="sxs-lookup"><span data-stu-id="f9f9e-180">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f9f9e-181"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f9f9e-181"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f9f9e-182">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f9f9e-182">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f9f9e-183">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="f9f9e-183">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="f9f9e-184">**glDisable**</span><span class="sxs-lookup"><span data-stu-id="f9f9e-184">**glDisable**</span></span>](gldisable.md)
</dt> <dt>

[<span data-ttu-id="f9f9e-185">**glEnable**</span><span class="sxs-lookup"><span data-stu-id="f9f9e-185">**glEnable**</span></span>](glenable.md)
</dt> <dt>

[<span data-ttu-id="f9f9e-186">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="f9f9e-186">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="f9f9e-187">**glGet**</span><span class="sxs-lookup"><span data-stu-id="f9f9e-187">**glGet**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[<span data-ttu-id="f9f9e-188">**glIsEnabled**</span><span class="sxs-lookup"><span data-stu-id="f9f9e-188">**glIsEnabled**</span></span>](glisenabled.md)
</dt> </dl>

 

 





