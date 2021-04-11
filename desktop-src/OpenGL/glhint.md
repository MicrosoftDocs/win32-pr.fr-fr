---
title: fonction glHint (GL. h)
description: La fonction glHint spécifie des indicateurs spécifiques à l’implémentation.
ms.assetid: 6d03e107-321a-45ee-9ce7-25fa9cab32d9
keywords:
- glHint fonction OpenGL
topic_type:
- apiref
api_name:
- glHint
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2772c76868c741660486184e5ab51bd193d3667a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103197"
---
# <a name="glhint-function"></a><span data-ttu-id="b3c9d-104">glHint fonction)</span><span class="sxs-lookup"><span data-stu-id="b3c9d-104">glHint function</span></span>

<span data-ttu-id="b3c9d-105">La fonction **glHint** spécifie des indicateurs spécifiques à l’implémentation.</span><span class="sxs-lookup"><span data-stu-id="b3c9d-105">The **glHint** function specifies implementation-specific hints.</span></span>

## <a name="syntax"></a><span data-ttu-id="b3c9d-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b3c9d-106">Syntax</span></span>


```C++
void WINAPI glHint(
   GLenum target,
   GLenum mode
);
```



## <a name="parameters"></a><span data-ttu-id="b3c9d-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b3c9d-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b3c9d-108">*cible*</span><span class="sxs-lookup"><span data-stu-id="b3c9d-108">*target*</span></span> 
</dt> <dd>

<span data-ttu-id="b3c9d-109">Constante symbolique indiquant le comportement à contrôler.</span><span class="sxs-lookup"><span data-stu-id="b3c9d-109">A symbolic constant indicating the behavior to be controlled.</span></span> <span data-ttu-id="b3c9d-110">Les constantes symboliques suivantes, ainsi que la sémantique suggérée, sont acceptées.</span><span class="sxs-lookup"><span data-stu-id="b3c9d-110">The following symbolic constants, along with suggested semantics, are accepted.</span></span>



| <span data-ttu-id="b3c9d-111">Valeur</span><span class="sxs-lookup"><span data-stu-id="b3c9d-111">Value</span></span>                                                                                                                                                                                                              | <span data-ttu-id="b3c9d-112">Signification</span><span class="sxs-lookup"><span data-stu-id="b3c9d-112">Meaning</span></span>                                                                                                                                                                                                                                                                                                           |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_FOG_HINT"></span><span id="gl_fog_hint"></span><dl> <span data-ttu-id="b3c9d-113"><dt>**\_indicateur de brouillard GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="b3c9d-113"><dt>**GL\_FOG\_HINT**</dt></span></span> </dl>                                                           | <span data-ttu-id="b3c9d-114">Indique l’exactitude du calcul du brouillard.</span><span class="sxs-lookup"><span data-stu-id="b3c9d-114">Indicates the accuracy of fog calculation.</span></span> <span data-ttu-id="b3c9d-115">Si le calcul du brouillard par pixel n’est pas efficacement pris en charge par l’implémentation OpenGL, l’affinement du GL sans \_ \_ souci ou le GL le \_ plus rapide peut entraîner un calcul par vertex des effets de brouillard.</span><span class="sxs-lookup"><span data-stu-id="b3c9d-115">If per-pixel fog calculation is not efficiently supported by the OpenGL implementation, hinting GL\_DONT\_CARE or GL\_FASTEST can result in per-vertex calculation of fog effects.</span></span><br/>                                                                          |
| <span id="GL_LINE_SMOOTH_HINT"></span><span id="gl_line_smooth_hint"></span><dl> <span data-ttu-id="b3c9d-116"><dt>**\_ \_ indicateur lisse de la ligne GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="b3c9d-116"><dt>**GL\_LINE\_SMOOTH\_HINT**</dt></span></span> </dl>                                  | <span data-ttu-id="b3c9d-117">Indique la qualité d’échantillonnage des lignes avec anticrénelage.</span><span class="sxs-lookup"><span data-stu-id="b3c9d-117">Indicates the sampling quality of antialiased lines.</span></span> <span data-ttu-id="b3c9d-118">L’affinement \_ du grand livre peut entraîner la génération d’un plus grand nombre de fragments de pixels au cours de la pixellisation, si une fonction de filtre plus grande est appliquée.</span><span class="sxs-lookup"><span data-stu-id="b3c9d-118">Hinting GL\_NICEST can result in more pixel fragments being generated during rasterization, if a larger filter function is applied.</span></span><br/>                                                                                                               |
| <span id="GL_PERSPECTIVE_CORRECTION_HINT"></span><span id="gl_perspective_correction_hint"></span><dl> <span data-ttu-id="b3c9d-119"><dt>**indicateur de correction de la \_ perspective GL \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="b3c9d-119"><dt>**GL\_PERSPECTIVE\_CORRECTION\_HINT**</dt></span></span> </dl> | <span data-ttu-id="b3c9d-120">Indique la qualité de l’interpolation des coordonnées de couleur et de texture.</span><span class="sxs-lookup"><span data-stu-id="b3c9d-120">Indicates the quality of color and texture coordinate interpolation.</span></span> <span data-ttu-id="b3c9d-121">Si l’interpolation des paramètres corrigés par la perspective n’est pas efficacement prise en charge par l’implémentation OpenGL, l’affinement du GL sans \_ \_ souci ou le GL le \_ plus rapide peut entraîner une interpolation linéaire simple des couleurs et/ou des coordonnées de texture.</span><span class="sxs-lookup"><span data-stu-id="b3c9d-121">If perspective-corrected parameter interpolation is not efficiently supported by the OpenGL implementation, hinting GL\_DONT\_CARE or GL\_FASTEST can result in simple linear interpolation of colors and/or texture coordinates.</span></span><br/> |
| <span id="GL_POINT_SMOOTH_HINT"></span><span id="gl_point_smooth_hint"></span><dl> <span data-ttu-id="b3c9d-122"><dt>**\_indicateur de \_ lissage du point GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="b3c9d-122"><dt>**GL\_POINT\_SMOOTH\_HINT**</dt></span></span> </dl>                               | <span data-ttu-id="b3c9d-123">Indique la qualité d’échantillonnage des points antialiasés.</span><span class="sxs-lookup"><span data-stu-id="b3c9d-123">Indicates the sampling quality of antialiased points.</span></span> <span data-ttu-id="b3c9d-124">L’affinement \_ du grand livre peut entraîner la génération d’un plus grand nombre de fragments de pixels au cours de la pixellisation, si une fonction de filtre plus grande est appliquée.</span><span class="sxs-lookup"><span data-stu-id="b3c9d-124">Hinting GL\_NICEST can result in more pixel fragments being generated during rasterization, if a larger filter function is applied.</span></span><br/>                                                                                                              |
| <span id="GL_POLYGON_SMOOTH_HINT"></span><span id="gl_polygon_smooth_hint"></span><dl> <span data-ttu-id="b3c9d-125"><dt>**\_ \_ indicateur lisse de polygone GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="b3c9d-125"><dt>**GL\_POLYGON\_SMOOTH\_HINT**</dt></span></span> </dl>                         | <span data-ttu-id="b3c9d-126">Indique la qualité d’échantillonnage des polygones avec anticrénelage.</span><span class="sxs-lookup"><span data-stu-id="b3c9d-126">Indicates the sampling quality of antialiased polygons.</span></span> <span data-ttu-id="b3c9d-127">L’affinement \_ du grand livre peut entraîner la génération d’un plus grand nombre de fragments de pixels au cours de la pixellisation, si une fonction de filtre plus grande est appliquée.</span><span class="sxs-lookup"><span data-stu-id="b3c9d-127">Hinting GL\_NICEST can result in more pixel fragments being generated during rasterization, if a larger filter function is applied.</span></span><br/>                                                                                                            |



 

</dd> <dt>

<span data-ttu-id="b3c9d-128">*mode*</span><span class="sxs-lookup"><span data-stu-id="b3c9d-128">*mode*</span></span> 
</dt> <dd>

<span data-ttu-id="b3c9d-129">Constante symbolique indiquant le comportement souhaité.</span><span class="sxs-lookup"><span data-stu-id="b3c9d-129">A symbolic constant indicating the desired behavior.</span></span> <span data-ttu-id="b3c9d-130">Les constantes symboliques suivantes sont acceptées.</span><span class="sxs-lookup"><span data-stu-id="b3c9d-130">The following symbolic constants are accepted.</span></span>



| <span data-ttu-id="b3c9d-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="b3c9d-131">Value</span></span>                                                                                                                                                       | <span data-ttu-id="b3c9d-132">Signification</span><span class="sxs-lookup"><span data-stu-id="b3c9d-132">Meaning</span></span>                                                                   |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <span id="GL_FASTEST"></span><span id="gl_fastest"></span><dl> <span data-ttu-id="b3c9d-133"><dt>**GL \_ plus rapide**</dt></span><span class="sxs-lookup"><span data-stu-id="b3c9d-133"><dt>**GL\_FASTEST**</dt></span></span> </dl>        | <span data-ttu-id="b3c9d-134">L’option la plus efficace doit être choisie.</span><span class="sxs-lookup"><span data-stu-id="b3c9d-134">The most efficient option should be chosen.</span></span><br/>                    |
| <span id="GL_NICEST"></span><span id="gl_nicest"></span><dl> <span data-ttu-id="b3c9d-135"><dt>**GL plus \_ agréable**</dt></span><span class="sxs-lookup"><span data-stu-id="b3c9d-135"><dt>**GL\_NICEST**</dt></span></span> </dl>           | <span data-ttu-id="b3c9d-136">L’option la plus correcte, ou la meilleure, doit être choisie.</span><span class="sxs-lookup"><span data-stu-id="b3c9d-136">The most correct, or highest quality, option should be chosen.</span></span><br/> |
| <span id="GL_DONT_CARE"></span><span id="gl_dont_care"></span><dl> <span data-ttu-id="b3c9d-137"><dt>**comptabilité \_ générale \_**</dt></span><span class="sxs-lookup"><span data-stu-id="b3c9d-137"><dt>**GL\_DONT\_CARE**</dt></span></span> </dl> | <span data-ttu-id="b3c9d-138">Le client n’a pas de préférence.</span><span class="sxs-lookup"><span data-stu-id="b3c9d-138">The client doesn't have a preference.</span></span><br/>                          |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b3c9d-139">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="b3c9d-139">Return value</span></span>

<span data-ttu-id="b3c9d-140">Cette fonction ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="b3c9d-140">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="b3c9d-141">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="b3c9d-141">Error codes</span></span>

<span data-ttu-id="b3c9d-142">Les codes d’erreur suivants peuvent être récupérés par la fonction [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="b3c9d-142">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="b3c9d-143">Nom</span><span class="sxs-lookup"><span data-stu-id="b3c9d-143">Name</span></span>                                                                                                  | <span data-ttu-id="b3c9d-144">Signification</span><span class="sxs-lookup"><span data-stu-id="b3c9d-144">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="b3c9d-145"><dt>**\_enum GL non valide \_**</dt></span><span class="sxs-lookup"><span data-stu-id="b3c9d-145"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="b3c9d-146">la *cible* ou le *mode* n’était pas une valeur acceptée.</span><span class="sxs-lookup"><span data-stu-id="b3c9d-146">*target* or *mode* was not an accepted value.</span></span><br/>                                                                              |
| <dl> <span data-ttu-id="b3c9d-147"><dt>**\_opération non valide du GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="b3c9d-147"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="b3c9d-148">La fonction a été appelée entre un appel à [**glBegin**](glbegin.md) et l’appel correspondant à [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="b3c9d-148">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="b3c9d-149">Notes</span><span class="sxs-lookup"><span data-stu-id="b3c9d-149">Remarks</span></span>

<span data-ttu-id="b3c9d-150">Lorsqu’il y a de la place pour l’interprétation, vous pouvez contrôler certains aspects du comportement OpenGL avec des indicateurs.</span><span class="sxs-lookup"><span data-stu-id="b3c9d-150">When there is room for interpretation, you can control certain aspects of OpenGL behavior with hints.</span></span> <span data-ttu-id="b3c9d-151">Vous spécifiez un indicateur avec deux arguments.</span><span class="sxs-lookup"><span data-stu-id="b3c9d-151">You specify a hint with two arguments.</span></span> <span data-ttu-id="b3c9d-152">Le paramètre *target* est une constante symbolique indiquant le comportement à contrôler et le *mode* est une autre constante symbolique indiquant le comportement souhaité.</span><span class="sxs-lookup"><span data-stu-id="b3c9d-152">The *target* parameter is a symbolic constant indicating the behavior to be controlled, and *mode* is another symbolic constant indicating the desired behavior.</span></span>

<span data-ttu-id="b3c9d-153">Bien que les aspects d’implémentation qui peuvent être Hints soient bien définis, l’interprétation des indications dépend de l’implémentation.</span><span class="sxs-lookup"><span data-stu-id="b3c9d-153">Though the implementation aspects that can be hinted are well defined, the interpretation of the hints depends on the implementation.</span></span>

<span data-ttu-id="b3c9d-154">La fonction **glHint** peut être ignorée.</span><span class="sxs-lookup"><span data-stu-id="b3c9d-154">The **glHint** function can be ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="b3c9d-155">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b3c9d-155">Requirements</span></span>



| <span data-ttu-id="b3c9d-156">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b3c9d-156">Requirement</span></span> | <span data-ttu-id="b3c9d-157">Valeur</span><span class="sxs-lookup"><span data-stu-id="b3c9d-157">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b3c9d-158">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b3c9d-158">Minimum supported client</span></span><br/> | <span data-ttu-id="b3c9d-159">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b3c9d-159">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="b3c9d-160">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b3c9d-160">Minimum supported server</span></span><br/> | <span data-ttu-id="b3c9d-161">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b3c9d-161">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="b3c9d-162">En-tête</span><span class="sxs-lookup"><span data-stu-id="b3c9d-162">Header</span></span><br/>                   | <dl> <span data-ttu-id="b3c9d-163"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="b3c9d-163"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="b3c9d-164">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="b3c9d-164">Library</span></span><br/>                  | <dl> <span data-ttu-id="b3c9d-165"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b3c9d-165"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="b3c9d-166">DLL</span><span class="sxs-lookup"><span data-stu-id="b3c9d-166">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b3c9d-167"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b3c9d-167"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b3c9d-168">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b3c9d-168">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b3c9d-169">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="b3c9d-169">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="b3c9d-170">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="b3c9d-170">**glEnd**</span></span>](glend.md)
</dt> </dl>

 

 





