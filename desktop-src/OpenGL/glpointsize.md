---
title: fonction glPointSize (GL. h)
description: La fonction glPointSize spécifie le diamètre des points pixellisés.
ms.assetid: efa35fa8-721a-48e5-bf59-d33b9bbe7f73
keywords:
- glPointSize fonction OpenGL
topic_type:
- apiref
api_name:
- glPointSize
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0e6b9525e302cad1eb940184eb5eb83e11744bba
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106512401"
---
# <a name="glpointsize-function"></a><span data-ttu-id="85905-104">glPointSize fonction)</span><span class="sxs-lookup"><span data-stu-id="85905-104">glPointSize function</span></span>

<span data-ttu-id="85905-105">La fonction **glPointSize** spécifie le diamètre des points pixellisés.</span><span class="sxs-lookup"><span data-stu-id="85905-105">The **glPointSize** function specifies the diameter of rasterized points.</span></span>

## <a name="syntax"></a><span data-ttu-id="85905-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="85905-106">Syntax</span></span>


```C++
void WINAPI glPointSize(
   GLfloat size
);
```



## <a name="parameters"></a><span data-ttu-id="85905-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="85905-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="85905-108">*size*</span><span class="sxs-lookup"><span data-stu-id="85905-108">*size*</span></span> 
</dt> <dd>

<span data-ttu-id="85905-109">Diamètre des points pixellisés.</span><span class="sxs-lookup"><span data-stu-id="85905-109">The diameter of rasterized points.</span></span> <span data-ttu-id="85905-110">La valeur par défaut est 1,0.</span><span class="sxs-lookup"><span data-stu-id="85905-110">The default is 1.0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="85905-111">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="85905-111">Return value</span></span>

<span data-ttu-id="85905-112">Cette fonction ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="85905-112">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="85905-113">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="85905-113">Error codes</span></span>

<span data-ttu-id="85905-114">Les codes d’erreur suivants peuvent être récupérés par la fonction [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="85905-114">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="85905-115">Nom</span><span class="sxs-lookup"><span data-stu-id="85905-115">Name</span></span>                                                                                                  | <span data-ttu-id="85905-116">Signification</span><span class="sxs-lookup"><span data-stu-id="85905-116">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="85905-117"><dt>**\_valeur non valide du GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="85905-117"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="85905-118">la *taille* est inférieure ou égale à zéro.</span><span class="sxs-lookup"><span data-stu-id="85905-118">*size* was less than or equal to zero.</span></span><br/>                                                                                     |
| <dl> <span data-ttu-id="85905-119"><dt>**\_opération non valide du GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="85905-119"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="85905-120">La fonction a été appelée entre un appel à [**glBegin**](glbegin.md) et l’appel correspondant à [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="85905-120">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="85905-121">Notes</span><span class="sxs-lookup"><span data-stu-id="85905-121">Remarks</span></span>

<span data-ttu-id="85905-122">La fonction **glPointSize** spécifie le diamètre pixellisé des points avec et sans alias.</span><span class="sxs-lookup"><span data-stu-id="85905-122">The **glPointSize** function specifies the rasterized diameter of both aliased and antialiased points.</span></span> <span data-ttu-id="85905-123">L’utilisation d’une taille en points autre que 1,0 a des effets différents, selon que l’anticrénelage des points est activé ou non.</span><span class="sxs-lookup"><span data-stu-id="85905-123">Using a point size other than 1.0 has different effects, depending on whether point antialiasing is enabled.</span></span> <span data-ttu-id="85905-124">L’anticrénelage des points est contrôlé en appelant [**glEnable**](glenable.md) et **glDisable** avec l’argument GL \_ point \_ Smooth.</span><span class="sxs-lookup"><span data-stu-id="85905-124">Point antialiasing is controlled by calling [**glEnable**](glenable.md) and **glDisable** with argument GL\_POINT\_SMOOTH.</span></span>

<span data-ttu-id="85905-125">Si l’anticrénelage des points est désactivé, la taille réelle est déterminée en arrondissant la taille fournie à l’entier le plus proche.</span><span class="sxs-lookup"><span data-stu-id="85905-125">If point antialiasing is disabled, the actual size is determined by rounding the supplied size to the nearest integer.</span></span> <span data-ttu-id="85905-126">(Si l’arrondi donne la valeur 0, c’est comme si la taille du point était 1.) Si la taille arrondie est impaire, le point central (*x*,*y*) du fragment de pixel qui représente le point est calculé comme</span><span class="sxs-lookup"><span data-stu-id="85905-126">(If the rounding results in the value 0, it is as if the point size were 1.) If the rounded size is odd, then the center point (*x*,*y*) of the pixel fragment that represents the point is computed as</span></span>

<span data-ttu-id="85905-127">(*x*<sub>w</sub> + 0,5, *y*<sub>w</sub> +. 5)</span><span class="sxs-lookup"><span data-stu-id="85905-127">(*x*<sub>w</sub> + .5, *y*<sub>w</sub> + .5)</span></span>

<span data-ttu-id="85905-128">où les indices *w* indiquent les coordonnées des fenêtres.</span><span class="sxs-lookup"><span data-stu-id="85905-128">where *w* subscripts indicate window coordinates.</span></span> <span data-ttu-id="85905-129">Tous les pixels qui se trouvent dans la grille carrée de la taille arrondie centrée sur (*x*,*y*) composent le fragment.</span><span class="sxs-lookup"><span data-stu-id="85905-129">All pixels that lie within the square grid of the rounded size centered at (*x*,*y*) make up the fragment.</span></span> <span data-ttu-id="85905-130">Si la taille est égale à, le point central est</span><span class="sxs-lookup"><span data-stu-id="85905-130">If the size is even, the center point is</span></span>

<span data-ttu-id="85905-131">(*x*<sub>w</sub> + 0,5, *y*<sub>w</sub> +. 5)</span><span class="sxs-lookup"><span data-stu-id="85905-131">(*x*<sub>w</sub> + .5, *y*<sub>w</sub> + .5)</span></span>

<span data-ttu-id="85905-132">et les centres du fragment pixellisé sont les coordonnées de fenêtre semi-entières dans le carré de la taille arrondie centrée sur (*x*,*y*).</span><span class="sxs-lookup"><span data-stu-id="85905-132">and the rasterized fragment's centers are the half-integer window coordinates within the square of the rounded size centered at (*x*,*y*).</span></span> <span data-ttu-id="85905-133">Tous les fragments de pixel produits pour pixelliser un point de nonantialiased sont affectés aux mêmes données associées. qui du vertex correspond au point.</span><span class="sxs-lookup"><span data-stu-id="85905-133">All pixel fragments produced in rasterizing a nonantialiased point are assigned the same associated data; that of the vertex corresponding to the point.</span></span>

<span data-ttu-id="85905-134">Si l’anticrénelage est activé, la pixellisation des points produit un fragment pour chaque carré de pixel qui croise la région située dans le cercle ayant un diamètre égal à la taille du point actuel et centrée aux points (*x*<sub>w</sub> ,*y*<sub>w</sub> ).</span><span class="sxs-lookup"><span data-stu-id="85905-134">If antialiasing is enabled, then point rasterization produces a fragment for each pixel square that intersects the region lying within the circle having diameter equal to the current point size and centered at the points (*x*<sub>w</sub> ,*y*<sub>w</sub> ).</span></span> <span data-ttu-id="85905-135">La valeur de couverture pour chaque fragment correspond à la zone de coordonnées de la fenêtre de l’intersection de la région circulaire avec le carré de pixel correspondant.</span><span class="sxs-lookup"><span data-stu-id="85905-135">The coverage value for each fragment is the window coordinate area of the intersection of the circular region with the corresponding pixel square.</span></span> <span data-ttu-id="85905-136">Cette valeur est enregistrée et utilisée dans l’étape de pixellisation finale.</span><span class="sxs-lookup"><span data-stu-id="85905-136">This value is saved and used in the final rasterization step.</span></span> <span data-ttu-id="85905-137">Les données associées à chaque fragment sont les données associées au point en cours de pixellisation.</span><span class="sxs-lookup"><span data-stu-id="85905-137">The data associated with each fragment is the data associated with the point being rasterized.</span></span>

<span data-ttu-id="85905-138">Toutes les tailles ne sont pas prises en charge lorsque l’anticrénelage des points est activé.</span><span class="sxs-lookup"><span data-stu-id="85905-138">Not all sizes are supported when point antialiasing is enabled.</span></span> <span data-ttu-id="85905-139">Si une taille non prise en charge est demandée, la taille la plus proche prise en charge est utilisée.</span><span class="sxs-lookup"><span data-stu-id="85905-139">If an unsupported size is requested, the nearest supported size is used.</span></span> <span data-ttu-id="85905-140">Seule la taille 1,0 est garantie pour être prise en charge ; d’autres dépendent de l’implémentation.</span><span class="sxs-lookup"><span data-stu-id="85905-140">Only size 1.0 is guaranteed to be supported; others depend on the implementation.</span></span> <span data-ttu-id="85905-141">Vous pouvez interroger la plage de tailles prises en charge et la différence de taille entre les tailles prises en charge dans la plage en appelant [**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) avec des arguments de granularité de taille de \_ point GL \_ \_ et de \_ \_ granularité de taille de point GL \_ .</span><span class="sxs-lookup"><span data-stu-id="85905-141">The range of supported sizes and the size difference between supported sizes within the range can be queried by calling [**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with arguments GL\_POINT\_SIZE\_RANGE and GL\_POINT\_SIZE\_GRANULARITY.</span></span>

<span data-ttu-id="85905-142">La taille en points spécifiée par **glPointSize** est toujours retournée lorsque la \_ taille du point GL \_ est interrogée.</span><span class="sxs-lookup"><span data-stu-id="85905-142">The point size specified by **glPointSize** is always returned when GL\_POINT\_SIZE is queried.</span></span> <span data-ttu-id="85905-143">Le verrouillage et l’arrondi pour les points avec et sans alias n’ont aucun effet sur la valeur spécifiée.</span><span class="sxs-lookup"><span data-stu-id="85905-143">Clamping and rounding for aliased and antialiased points have no effect on the specified value.</span></span>

<span data-ttu-id="85905-144">La taille du point non anticrénelage peut être ancrée à un maximum dépendant de l’implémentation.</span><span class="sxs-lookup"><span data-stu-id="85905-144">Non-antialiased point size may be clamped to an implementation-dependent maximum.</span></span> <span data-ttu-id="85905-145">Même si ce nombre maximal ne peut pas être interrogé, il ne doit pas être inférieur à la valeur maximale pour les points avec anticrénelage, arrondi à la valeur entière la plus proche.</span><span class="sxs-lookup"><span data-stu-id="85905-145">Although this maximum cannot be queried, it must be no less than the maximum value for antialiased points, rounded to the nearest integer value.</span></span>

<span data-ttu-id="85905-146">Les fonctions suivantes récupèrent les informations relatives à **glPointSize**:</span><span class="sxs-lookup"><span data-stu-id="85905-146">The following functions retrieve information related to **glPointSize**:</span></span>

<span data-ttu-id="85905-147">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) avec l’argument \_ taille du point GL \_</span><span class="sxs-lookup"><span data-stu-id="85905-147">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_POINT\_SIZE</span></span>

<span data-ttu-id="85905-148">**glGet** avec argument GL \_ point \_ taille de la \_ plage</span><span class="sxs-lookup"><span data-stu-id="85905-148">**glGet** with argument GL\_POINT\_SIZE\_RANGE</span></span>

<span data-ttu-id="85905-149">**glGet** avec argument de \_ \_ granularité de taille de point GL \_</span><span class="sxs-lookup"><span data-stu-id="85905-149">**glGet** with argument GL\_POINT\_SIZE\_GRANULARITY</span></span>

<span data-ttu-id="85905-150">[**glIsEnabled**](glisenabled.md) avec argument GL \_ point \_ lisse</span><span class="sxs-lookup"><span data-stu-id="85905-150">[**glIsEnabled**](glisenabled.md) with argument GL\_POINT\_SMOOTH</span></span>

## <a name="requirements"></a><span data-ttu-id="85905-151">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="85905-151">Requirements</span></span>



| <span data-ttu-id="85905-152">Condition requise</span><span class="sxs-lookup"><span data-stu-id="85905-152">Requirement</span></span> | <span data-ttu-id="85905-153">Valeur</span><span class="sxs-lookup"><span data-stu-id="85905-153">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="85905-154">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="85905-154">Minimum supported client</span></span><br/> | <span data-ttu-id="85905-155">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="85905-155">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="85905-156">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="85905-156">Minimum supported server</span></span><br/> | <span data-ttu-id="85905-157">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="85905-157">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="85905-158">En-tête</span><span class="sxs-lookup"><span data-stu-id="85905-158">Header</span></span><br/>                   | <dl> <span data-ttu-id="85905-159"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="85905-159"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="85905-160">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="85905-160">Library</span></span><br/>                  | <dl> <span data-ttu-id="85905-161"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="85905-161"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="85905-162">DLL</span><span class="sxs-lookup"><span data-stu-id="85905-162">DLL</span></span><br/>                      | <dl> <span data-ttu-id="85905-163"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="85905-163"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="85905-164">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="85905-164">See also</span></span>

<dl> <dt>

[<span data-ttu-id="85905-165">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="85905-165">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="85905-166">**glEnable**</span><span class="sxs-lookup"><span data-stu-id="85905-166">**glEnable**</span></span>](glenable.md)
</dt> <dt>

[<span data-ttu-id="85905-167">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="85905-167">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="85905-168">**glIsEnabled**</span><span class="sxs-lookup"><span data-stu-id="85905-168">**glIsEnabled**</span></span>](glisenabled.md)
</dt> </dl>

 

 





