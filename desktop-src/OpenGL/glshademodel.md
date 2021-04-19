---
title: fonction glShadeModel (GL. h)
description: La fonction glShadeModel sélectionne un ombrage plat ou lisse.
ms.assetid: 52985ad7-1d6c-48fc-8f1e-4eb2c0324c8e
keywords:
- glShadeModel fonction OpenGL
topic_type:
- apiref
api_name:
- glShadeModel
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 142ac518c91c6378f1606235e25502be8c06dd6a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106510315"
---
# <a name="glshademodel-function"></a><span data-ttu-id="d61cf-104">glShadeModel fonction)</span><span class="sxs-lookup"><span data-stu-id="d61cf-104">glShadeModel function</span></span>

<span data-ttu-id="d61cf-105">La fonction **glShadeModel** sélectionne un ombrage plat ou lisse.</span><span class="sxs-lookup"><span data-stu-id="d61cf-105">The **glShadeModel** function selects flat or smooth shading.</span></span>

## <a name="syntax"></a><span data-ttu-id="d61cf-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d61cf-106">Syntax</span></span>


```C++
void WINAPI glShadeModel(
   GLenum mode
);
```



## <a name="parameters"></a><span data-ttu-id="d61cf-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d61cf-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d61cf-108">*mode*</span><span class="sxs-lookup"><span data-stu-id="d61cf-108">*mode*</span></span> 
</dt> <dd>

<span data-ttu-id="d61cf-109">Valeur symbolique représentant une technique d’ombrage.</span><span class="sxs-lookup"><span data-stu-id="d61cf-109">A symbolic value representing a shading technique.</span></span> <span data-ttu-id="d61cf-110">Les valeurs acceptées sont \_ Flat GL et GL \_ Smooth.</span><span class="sxs-lookup"><span data-stu-id="d61cf-110">Accepted values are GL\_FLAT and GL\_SMOOTH.</span></span> <span data-ttu-id="d61cf-111">La valeur par défaut est lisse du GL \_ .</span><span class="sxs-lookup"><span data-stu-id="d61cf-111">The default is GL\_SMOOTH.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d61cf-112">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="d61cf-112">Return value</span></span>

<span data-ttu-id="d61cf-113">Cette fonction ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="d61cf-113">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="d61cf-114">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="d61cf-114">Error codes</span></span>

<span data-ttu-id="d61cf-115">Les codes d’erreur suivants peuvent être récupérés par la fonction [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="d61cf-115">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="d61cf-116">Nom</span><span class="sxs-lookup"><span data-stu-id="d61cf-116">Name</span></span>                                                                                                  | <span data-ttu-id="d61cf-117">Signification</span><span class="sxs-lookup"><span data-stu-id="d61cf-117">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="d61cf-118"><dt>**\_enum GL non valide \_**</dt></span><span class="sxs-lookup"><span data-stu-id="d61cf-118"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="d61cf-119">le *mode* est une valeur autre que GL \_ glat ou GL \_ Smooth.</span><span class="sxs-lookup"><span data-stu-id="d61cf-119">*mode* was a value other than GL\_GLAT or GL\_SMOOTH.</span></span><br/>                                                                      |
| <dl> <span data-ttu-id="d61cf-120"><dt>**\_opération non valide du GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="d61cf-120"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="d61cf-121">La fonction a été appelée entre un appel à [**glBegin**](glbegin.md) et l’appel correspondant à [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="d61cf-121">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="d61cf-122">Notes</span><span class="sxs-lookup"><span data-stu-id="d61cf-122">Remarks</span></span>

<span data-ttu-id="d61cf-123">Les primitives OpenGL peuvent avoir un ombrage plat ou lissé.</span><span class="sxs-lookup"><span data-stu-id="d61cf-123">OpenGL primitives can have either flat or smooth shading.</span></span> <span data-ttu-id="d61cf-124">L’ombrage lissé, par défaut, entraîne l’interpolation des couleurs calculées des vertex lorsque la primitive est pixellisée, en affectant généralement des couleurs différentes à chaque fragment de pixel résultant.</span><span class="sxs-lookup"><span data-stu-id="d61cf-124">Smooth shading, the default, causes the computed colors of vertices to be interpolated as the primitive is rasterized, typically assigning different colors to each resulting pixel fragment.</span></span> <span data-ttu-id="d61cf-125">L’ombrage plat sélectionne la couleur calculée d’un seul vertex et l’attribue à tous les fragments de pixel générés par la pixellisation d’une seule primitive.</span><span class="sxs-lookup"><span data-stu-id="d61cf-125">Flat shading selects the computed color of just one vertex and assigns it to all the pixel fragments generated by rasterizing a single primitive.</span></span> <span data-ttu-id="d61cf-126">Dans les deux cas, la couleur calculée d’un vertex est le résultat de l’éclairage, si l’éclairage est activé ou s’il s’agit de la couleur actuelle au moment de la spécification du vertex, si l’éclairage est désactivé.</span><span class="sxs-lookup"><span data-stu-id="d61cf-126">In either case, the computed color of a vertex is the result of lighting, if lighting is enabled, or it is the current color at the time the vertex was specified, if lighting is disabled.</span></span>

<span data-ttu-id="d61cf-127">L’ombrage plat et lisse ne peuvent pas être différenciés pour les points.</span><span class="sxs-lookup"><span data-stu-id="d61cf-127">Flat and smooth shading are indistinguishable for points.</span></span> <span data-ttu-id="d61cf-128">En comptant les vertex et les primitives à partir d’un, en commençant à la sortie de [**glBegin**](glbegin.md) , *chaque segment de* ligne à ombrage plat reçoit la couleur calculée du sommet *i* + 1, son deuxième vertex.</span><span class="sxs-lookup"><span data-stu-id="d61cf-128">Counting vertices and primitives from one, starting when [**glBegin**](glbegin.md) is issued, each flat-shaded line segment *i* is given the computed color of vertex *i* + 1, its second vertex.</span></span> <span data-ttu-id="d61cf-129">En comptant de la même manière, chaque polygone à ombrage constant reçoit la couleur calculée du vertex indiqué dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="d61cf-129">Counting similarly from one, each flat-shaded polygon is given the computed color of the vertex listed in the following table.</span></span> <span data-ttu-id="d61cf-130">Il s’agit du dernier vertex pour spécifier le polygone dans tous les cas, à l’exception des polygones simples, où le premier vertex spécifie la couleur ombrée plate.</span><span class="sxs-lookup"><span data-stu-id="d61cf-130">This is the last vertex to specify the polygon in all cases except single polygons, where the first vertex specifies the flat-shaded color.</span></span>



| <span data-ttu-id="d61cf-131">Type primitif de polygone i</span><span class="sxs-lookup"><span data-stu-id="d61cf-131">Primitive type of polygon i</span></span> | <span data-ttu-id="d61cf-132">Sommet</span><span class="sxs-lookup"><span data-stu-id="d61cf-132">Vertex</span></span>   |
|-----------------------------|----------|
| <span data-ttu-id="d61cf-133">Polygone simple (*I*= 1)</span><span class="sxs-lookup"><span data-stu-id="d61cf-133">Single polygon (*I*=1)</span></span>      | <span data-ttu-id="d61cf-134">1</span><span class="sxs-lookup"><span data-stu-id="d61cf-134">1</span></span>        |
| <span data-ttu-id="d61cf-135">Bande triangulaire</span><span class="sxs-lookup"><span data-stu-id="d61cf-135">Triangle strip</span></span>              | <span data-ttu-id="d61cf-136">*i* + 2</span><span class="sxs-lookup"><span data-stu-id="d61cf-136">*i* + 2</span></span>  |
| <span data-ttu-id="d61cf-137">Ventilateur triangulaire</span><span class="sxs-lookup"><span data-stu-id="d61cf-137">Triangle fan</span></span>                | <span data-ttu-id="d61cf-138">*i* + 2</span><span class="sxs-lookup"><span data-stu-id="d61cf-138">*i* + 2</span></span>  |
| <span data-ttu-id="d61cf-139">Triangle indépendant</span><span class="sxs-lookup"><span data-stu-id="d61cf-139">Independent triangle</span></span>        | <span data-ttu-id="d61cf-140">3 *I*</span><span class="sxs-lookup"><span data-stu-id="d61cf-140">3 *I*</span></span>     |
| <span data-ttu-id="d61cf-141">Quadruple bande</span><span class="sxs-lookup"><span data-stu-id="d61cf-141">Quad strip</span></span>                  | <span data-ttu-id="d61cf-142">2 *i* + 2</span><span class="sxs-lookup"><span data-stu-id="d61cf-142">2 *i* + 2</span></span> |
| <span data-ttu-id="d61cf-143">Quad indépendant</span><span class="sxs-lookup"><span data-stu-id="d61cf-143">Independent quad</span></span>            | <span data-ttu-id="d61cf-144">4 *I*</span><span class="sxs-lookup"><span data-stu-id="d61cf-144">4 *I*</span></span>     |



 

<span data-ttu-id="d61cf-145">Les ombrages plats et lisses sont spécifiés par **glShadeModel** avec le *mode* défini sur GL \_ Flat et GL \_ Smooth, respectivement.</span><span class="sxs-lookup"><span data-stu-id="d61cf-145">Flat and smooth shading are specified by **glShadeModel** with *mode* set to GL\_FLAT and GL\_SMOOTH, respectively.</span></span>

<span data-ttu-id="d61cf-146">La fonction suivante récupère des informations relatives à **glShadeModel**:</span><span class="sxs-lookup"><span data-stu-id="d61cf-146">The following function retrieves information related to **glShadeModel**:</span></span>

<span data-ttu-id="d61cf-147">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) avec argument GL \_ Shade Shader \_ Model</span><span class="sxs-lookup"><span data-stu-id="d61cf-147">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_SHADE\_MODEL</span></span>

## <a name="requirements"></a><span data-ttu-id="d61cf-148">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d61cf-148">Requirements</span></span>



| <span data-ttu-id="d61cf-149">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d61cf-149">Requirement</span></span> | <span data-ttu-id="d61cf-150">Valeur</span><span class="sxs-lookup"><span data-stu-id="d61cf-150">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d61cf-151">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d61cf-151">Minimum supported client</span></span><br/> | <span data-ttu-id="d61cf-152">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d61cf-152">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="d61cf-153">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d61cf-153">Minimum supported server</span></span><br/> | <span data-ttu-id="d61cf-154">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d61cf-154">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="d61cf-155">En-tête</span><span class="sxs-lookup"><span data-stu-id="d61cf-155">Header</span></span><br/>                   | <dl> <span data-ttu-id="d61cf-156"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="d61cf-156"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="d61cf-157">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="d61cf-157">Library</span></span><br/>                  | <dl> <span data-ttu-id="d61cf-158"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d61cf-158"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="d61cf-159">DLL</span><span class="sxs-lookup"><span data-stu-id="d61cf-159">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d61cf-160"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d61cf-160"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d61cf-161">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d61cf-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d61cf-162">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="d61cf-162">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="d61cf-163">**glColor**</span><span class="sxs-lookup"><span data-stu-id="d61cf-163">**glColor**</span></span>](glcolor-functions.md)
</dt> <dt>

[<span data-ttu-id="d61cf-164">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="d61cf-164">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="d61cf-165">**glLight**</span><span class="sxs-lookup"><span data-stu-id="d61cf-165">**glLight**</span></span>](gllight-functions.md)
</dt> <dt>

[<span data-ttu-id="d61cf-166">**glLightModel**</span><span class="sxs-lookup"><span data-stu-id="d61cf-166">**glLightModel**</span></span>](gllightmodel-functions.md)
</dt> </dl>

 

 





