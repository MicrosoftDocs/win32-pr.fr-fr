---
title: fonction glRasterPos4d (GL. h)
description: Spécifie la position raster pour les opérations de pixel. | fonction glRasterPos4d (GL. h)
ms.assetid: 38327e2d-b9e0-413d-be7e-472cedbdfab9
keywords:
- glRasterPos4d fonction OpenGL
topic_type:
- apiref
api_name:
- glRasterPos4d
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a080782837e9b2e6b7752f2c874530ed072edb58
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "106539821"
---
# <a name="glrasterpos4d-function"></a><span data-ttu-id="7c398-105">glRasterPos4d fonction)</span><span class="sxs-lookup"><span data-stu-id="7c398-105">glRasterPos4d function</span></span>

<span data-ttu-id="7c398-106">Spécifie la position raster pour les opérations de pixel.</span><span class="sxs-lookup"><span data-stu-id="7c398-106">Specifies the raster position for pixel operations.</span></span>

## <a name="syntax"></a><span data-ttu-id="7c398-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7c398-107">Syntax</span></span>


```C++
void WINAPI glRasterPos4d(
   GLdouble x,
   GLdouble y,
   GLdouble z,
   GLdouble w
);
```



## <a name="parameters"></a><span data-ttu-id="7c398-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7c398-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7c398-109">*x*</span><span class="sxs-lookup"><span data-stu-id="7c398-109">*x*</span></span> 
</dt> <dd>

<span data-ttu-id="7c398-110">Spécifie la coordonnée x de la position de la trame actuelle.</span><span class="sxs-lookup"><span data-stu-id="7c398-110">Specifies the x-coordinate for the current raster position.</span></span>

</dd> <dt>

<span data-ttu-id="7c398-111">*y*</span><span class="sxs-lookup"><span data-stu-id="7c398-111">*y*</span></span> 
</dt> <dd>

<span data-ttu-id="7c398-112">Spécifie la coordonnée y de la position raster actuelle.</span><span class="sxs-lookup"><span data-stu-id="7c398-112">Specifies the y-coordinate for the current raster position.</span></span>

</dd> <dt>

<span data-ttu-id="7c398-113">*z*</span><span class="sxs-lookup"><span data-stu-id="7c398-113">*z*</span></span> 
</dt> <dd>

<span data-ttu-id="7c398-114">Spécifie la coordonnée z de la position de la trame actuelle.</span><span class="sxs-lookup"><span data-stu-id="7c398-114">Specifies the z-coordinate for the current raster position.</span></span>

</dd> <dt>

<span data-ttu-id="7c398-115">*w*</span><span class="sxs-lookup"><span data-stu-id="7c398-115">*w*</span></span> 
</dt> <dd>

<span data-ttu-id="7c398-116">Coordonnée w pour la position raster actuelle.</span><span class="sxs-lookup"><span data-stu-id="7c398-116">The w-coordinate for the current raster position.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7c398-117">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="7c398-117">Return value</span></span>

<span data-ttu-id="7c398-118">Cette fonction ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="7c398-118">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="7c398-119">Notes</span><span class="sxs-lookup"><span data-stu-id="7c398-119">Remarks</span></span>

<span data-ttu-id="7c398-120">OpenGL gère une position 3D dans les coordonnées de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="7c398-120">OpenGL maintains a 3-D position in window coordinates.</span></span> <span data-ttu-id="7c398-121">Cette position, appelée position raster, est conservée avec la précision des sous-pixels.</span><span class="sxs-lookup"><span data-stu-id="7c398-121">This position, called the raster position, is maintained with subpixel accuracy.</span></span> <span data-ttu-id="7c398-122">Il est utilisé pour positionner les opérations d’écriture de pixel et de bitmap.</span><span class="sxs-lookup"><span data-stu-id="7c398-122">It is used to position pixel and bitmap write operations.</span></span> <span data-ttu-id="7c398-123">Consultez [**glBitmap**](glbitmap.md), [**glDrawPixels**](gldrawpixels.md)et [**glCopyPixels**](glcopypixels.md).</span><span class="sxs-lookup"><span data-stu-id="7c398-123">See [**glBitmap**](glbitmap.md), [**glDrawPixels**](gldrawpixels.md), and [**glCopyPixels**](glcopypixels.md).</span></span>

<span data-ttu-id="7c398-124">La position actuelle du raster est constituée de trois coordonnées de fenêtre (*x, y, z*), d’une valeur *w* de la coordonnée d’un élément, d’une distance de coordonnée oculaire, d’un bit valide, de données de couleur et de coordonnées de texture associées.</span><span class="sxs-lookup"><span data-stu-id="7c398-124">The current raster position consists of three window coordinates (*x, y, z*), a clip coordinate *w* value, an eye coordinate distance, a valid bit, and associated color data and texture coordinates.</span></span> <span data-ttu-id="7c398-125">La coordonnée *w* est une coordonnée de clip, car *w* n’est pas projeté aux coordonnées de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="7c398-125">The *w* coordinate is a clip coordinate, because *w* is not projected to window coordinates.</span></span> <span data-ttu-id="7c398-126">La fonction [glRasterPos4](glrasterpos-functions.md) spécifie les coordonnées d’objet *x, y, z* et *w* explicitement.</span><span class="sxs-lookup"><span data-stu-id="7c398-126">The [glRasterPos4](glrasterpos-functions.md) function specifies object coordinates *x, y, z*, and *w* explicitly.</span></span> <span data-ttu-id="7c398-127">La fonction glRasterPos3 spécifie les coordonnées d’objet *x, y* et *z* explicitement, tandis que *w* est implicitement défini sur un.</span><span class="sxs-lookup"><span data-stu-id="7c398-127">The glRasterPos3 function specifies object coordinates *x, y,* and *z* explicitly, while *w* is implicitly set to one.</span></span> <span data-ttu-id="7c398-128">La fonction glRasterPos2 utilise les valeurs d’argument pour *x* et *y* tout en définissant *z* et *w* de manière implicite sur zéro et un.</span><span class="sxs-lookup"><span data-stu-id="7c398-128">The glRasterPos2 function uses the argument values for *x* and *y* while implicitly setting *z* and *w* to zero and one.</span></span>

<span data-ttu-id="7c398-129">Les coordonnées d’objet présentées par [glRasterPos](glrasterpos-functions.md) sont traitées comme celles d’une commande [glVertex](glvertex-functions.md) .</span><span class="sxs-lookup"><span data-stu-id="7c398-129">The object coordinates presented by [glRasterPos](glrasterpos-functions.md) are treated just like those of a [glVertex](glvertex-functions.md) command.</span></span> <span data-ttu-id="7c398-130">Elles sont transformées par les matrices de projection et de modelview actuelles et transmises à l’étape de découpage.</span><span class="sxs-lookup"><span data-stu-id="7c398-130">They are transformed by the current modelview and projection matrices and passed to the clipping stage.</span></span> <span data-ttu-id="7c398-131">Si le vertex n’est pas sélectionné, il est projeté et mis à l’échelle sur les coordonnées de la fenêtre, qui devient la nouvelle position de la trame actuelle, et l’indicateur de la position de la \_ trame active du GL \_ \_ \_ est défini.</span><span class="sxs-lookup"><span data-stu-id="7c398-131">If the vertex is not culled, then it is projected and scaled to window coordinates, which become the new current raster position, and the GL\_CURRENT\_RASTER\_POSITION\_VALID flag is set.</span></span> <span data-ttu-id="7c398-132">Si le vertex est sélectionné, le bit valide est effacé et la position raster actuelle ainsi que les coordonnées de couleur et de texture associées ne sont pas définies.</span><span class="sxs-lookup"><span data-stu-id="7c398-132">If the vertex is culled, then the valid bit is cleared and the current raster position and associated color and texture coordinates are undefined.</span></span>

<span data-ttu-id="7c398-133">La position actuelle du raster comprend également des données de couleur et des coordonnées de texture associées.</span><span class="sxs-lookup"><span data-stu-id="7c398-133">The current raster position also includes some associated color data and texture coordinates.</span></span> <span data-ttu-id="7c398-134">Si l’éclairage est activé, la \_ \_ couleur de tramage actuelle de la comptabilité GL \_ , en mode RVBA, ou l' \_ index raster actuel du GL \_ \_ , en mode d’index des couleurs, est définie sur la couleur produite par le calcul de l’éclairage (voir [glLight](gllight-functions.md), [glLightModel](gllightmodel-functions.md)et [**glShadeModel**](glshademodel.md)).</span><span class="sxs-lookup"><span data-stu-id="7c398-134">If lighting is enabled, then GL\_CURRENT\_RASTER\_COLOR, in RGBA mode, or the GL\_CURRENT\_RASTER\_INDEX, in color-index mode, is set to the color produced by the lighting calculation (see [glLight](gllight-functions.md), [glLightModel](gllightmodel-functions.md), and [**glShadeModel**](glshademodel.md)).</span></span> <span data-ttu-id="7c398-135">Si l’éclairage est désactivé, la couleur actuelle (en mode RVBA, la couleur actuelle de la comptabilité de la variable d’état \_ \_ ) ou l’index de couleurs (en mode d’index des couleurs, l’index de la valeur de la comptabilité générale de \_ la variable d’état \_ ) est utilisé pour mettre à jour la couleur raster actuelle.</span><span class="sxs-lookup"><span data-stu-id="7c398-135">If lighting is disabled, current color (in RGBA mode, state variable GL\_CURRENT\_COLOR) or color index (in color-index mode, state variable GL\_CURRENT\_INDEX) is used to update the current raster color.</span></span>

<span data-ttu-id="7c398-136">De même, \_ les \_ \_ \_ coordonnées de la texture raster actuelle du GL sont mises à jour en fonction de la mesure de \_ texture actuelle du GL \_ \_ , en fonction de la matrice de texture et des fonctions de génération de texture (voir [glTexGen](gltexgen-functions.md)).</span><span class="sxs-lookup"><span data-stu-id="7c398-136">Likewise, GL\_CURRENT\_RASTER\_TEXTURE\_COORDS is updated as a function of GL\_CURRENT\_TEXTURE\_COORDS, based on the texture matrix and the texture generation functions (see [glTexGen](gltexgen-functions.md)).</span></span> <span data-ttu-id="7c398-137">Enfin, la distance entre l’origine du système de coordonnées oculaire et le sommet, telle qu’elle est transformée par la matrice modelview, remplace la distance de la \_ trame actuelle du GL \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="7c398-137">Finally, the distance from the origin of the eye coordinate system to the vertex, as transformed by only the modelview matrix, replaces GL\_CURRENT\_RASTER\_DISTANCE.</span></span>

<span data-ttu-id="7c398-138">Au départ, la position du raster actuel est (0, 0, 0, 1), la distance de trame actuelle est 0, le bit valide est défini, la couleur RVBA associée est (1, 1, 1, 1), l’index de couleur associé est 1 et les coordonnées de texture associées sont (0, 0, 0, 1).</span><span class="sxs-lookup"><span data-stu-id="7c398-138">Initially, the current raster position is (0,0,0,1), the current raster distance is 0, the valid bit is set, the associated RGBA color is (1,1,1,1), the associated color index is 1, and the associated texture coordinates are (0, 0, 0, 1).</span></span> <span data-ttu-id="7c398-139">En mode RVBA, \_ \_ l’index de tramage actuel de GL \_ est toujours 1 ; dans le mode d’index de couleurs, la couleur RVBA raster actuelle conserve toujours sa valeur initiale.</span><span class="sxs-lookup"><span data-stu-id="7c398-139">In RGBA mode, GL\_CURRENT\_RASTER\_INDEX is always 1; in color-index mode, the current raster RGBA color always maintains its initial value.</span></span>

> [!Note]  
> <span data-ttu-id="7c398-140">La position Raster est modifiée à la fois par [glRasterPos](glrasterpos-functions.md) et par [**glBitmap**](glbitmap.md).</span><span class="sxs-lookup"><span data-stu-id="7c398-140">The raster position is modified both by [glRasterPos](glrasterpos-functions.md) and by [**glBitmap**](glbitmap.md).</span></span>

 

> [!Note]  
> <span data-ttu-id="7c398-141">Lorsque les coordonnées de la position raster ne sont pas valides, les commandes de dessin basées sur la position raster sont ignorées (c’est-à-dire qu’elles n’entraînent pas de modifications de l’État OpenGL).</span><span class="sxs-lookup"><span data-stu-id="7c398-141">When the raster position coordinates are invalid, drawing commands that are based on the raster position are ignored (that is, they do not result in changes to the OpenGL state).</span></span>

 

<span data-ttu-id="7c398-142">Les fonctions suivantes récupèrent les informations relatives à [glRasterPos](glrasterpos-functions.md):</span><span class="sxs-lookup"><span data-stu-id="7c398-142">The following functions retrieve information related to [glRasterPos](glrasterpos-functions.md):</span></span>

<dl>

<span data-ttu-id="7c398-143">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) avec argument GL \_ Current \_ Raster \_ position</span><span class="sxs-lookup"><span data-stu-id="7c398-143">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_CURRENT\_RASTER\_POSITION</span></span>  
<span data-ttu-id="7c398-144">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) avec argument GL \_ Current \_ Raster \_ position \_ valide</span><span class="sxs-lookup"><span data-stu-id="7c398-144">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_CURRENT\_RASTER\_POSITION\_VALID</span></span>  
<span data-ttu-id="7c398-145">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) avec argument GL \_ Current \_ Raster \_ distance</span><span class="sxs-lookup"><span data-stu-id="7c398-145">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_CURRENT\_RASTER\_DISTANCE</span></span>  
<span data-ttu-id="7c398-146">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) avec argument GL \_ Current \_ Raster \_ couleur</span><span class="sxs-lookup"><span data-stu-id="7c398-146">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_CURRENT\_RASTER\_COLOR</span></span>  
<span data-ttu-id="7c398-147">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) avec argument GL \_ Current \_ Raster \_ index</span><span class="sxs-lookup"><span data-stu-id="7c398-147">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_CURRENT\_RASTER\_INDEX</span></span>  
<span data-ttu-id="7c398-148">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) avec argument de \_ la \_ texture de TRAMe actuelle du \_ GL \_</span><span class="sxs-lookup"><span data-stu-id="7c398-148">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_CURRENT\_RASTER\_TEXTURE\_COORDS</span></span>  
</dl>

## <a name="requirements"></a><span data-ttu-id="7c398-149">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7c398-149">Requirements</span></span>



| <span data-ttu-id="7c398-150">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7c398-150">Requirement</span></span> | <span data-ttu-id="7c398-151">Valeur</span><span class="sxs-lookup"><span data-stu-id="7c398-151">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7c398-152">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7c398-152">Minimum supported client</span></span><br/> | <span data-ttu-id="7c398-153">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7c398-153">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="7c398-154">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7c398-154">Minimum supported server</span></span><br/> | <span data-ttu-id="7c398-155">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7c398-155">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="7c398-156">En-tête</span><span class="sxs-lookup"><span data-stu-id="7c398-156">Header</span></span><br/>                   | <dl> <span data-ttu-id="7c398-157"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="7c398-157"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="7c398-158">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="7c398-158">Library</span></span><br/>                  | <dl> <span data-ttu-id="7c398-159"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7c398-159"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="7c398-160">DLL</span><span class="sxs-lookup"><span data-stu-id="7c398-160">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7c398-161"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7c398-161"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7c398-162">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7c398-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7c398-163">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="7c398-163">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="7c398-164">**glBitmap**</span><span class="sxs-lookup"><span data-stu-id="7c398-164">**glBitmap**</span></span>](glbitmap.md)
</dt> <dt>

[<span data-ttu-id="7c398-165">**glCopyPixels**</span><span class="sxs-lookup"><span data-stu-id="7c398-165">**glCopyPixels**</span></span>](glcopypixels.md)
</dt> <dt>

[<span data-ttu-id="7c398-166">**glDrawPixels**</span><span class="sxs-lookup"><span data-stu-id="7c398-166">**glDrawPixels**</span></span>](gldrawpixels.md)
</dt> <dt>

[<span data-ttu-id="7c398-167">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="7c398-167">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="7c398-168">glLight</span><span class="sxs-lookup"><span data-stu-id="7c398-168">glLight</span></span>](gllight-functions.md)
</dt> <dt>

[<span data-ttu-id="7c398-169">glLightModel</span><span class="sxs-lookup"><span data-stu-id="7c398-169">glLightModel</span></span>](gllightmodel-functions.md)
</dt> <dt>

[<span data-ttu-id="7c398-170">**glShadeModel**</span><span class="sxs-lookup"><span data-stu-id="7c398-170">**glShadeModel**</span></span>](glshademodel.md)
</dt> <dt>

[<span data-ttu-id="7c398-171">**glTexCoord**</span><span class="sxs-lookup"><span data-stu-id="7c398-171">**glTexCoord**</span></span>](gltexcoord-functions.md)
</dt> <dt>

[<span data-ttu-id="7c398-172">glTexGen</span><span class="sxs-lookup"><span data-stu-id="7c398-172">glTexGen</span></span>](gltexgen-functions.md)
</dt> <dt>

[<span data-ttu-id="7c398-173">glVertex</span><span class="sxs-lookup"><span data-stu-id="7c398-173">glVertex</span></span>](glvertex-functions.md)
</dt> </dl>

 

 





