---
title: fonction glRasterPos3dv (GL. h)
description: Spécifie la position raster pour les opérations de pixel. | fonction glRasterPos3dv (GL. h)
ms.assetid: bcf9f5b2-cf17-4451-afa4-28a53415f809
keywords:
- glRasterPos3dv fonction OpenGL
topic_type:
- apiref
api_name:
- glRasterPos3dv
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 503f5d0333fc4213cdcf20a35241c59e6f622a63
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "106524811"
---
# <a name="glrasterpos3dv-function"></a><span data-ttu-id="58a3c-105">glRasterPos3dv fonction)</span><span class="sxs-lookup"><span data-stu-id="58a3c-105">glRasterPos3dv function</span></span>

<span data-ttu-id="58a3c-106">Spécifie la position raster pour les opérations de pixel.</span><span class="sxs-lookup"><span data-stu-id="58a3c-106">Specifies the raster position for pixel operations.</span></span>

## <a name="syntax"></a><span data-ttu-id="58a3c-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="58a3c-107">Syntax</span></span>


```C++
void WINAPI glRasterPos3dv(
   const GLdouble *v
);
```



## <a name="parameters"></a><span data-ttu-id="58a3c-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="58a3c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="58a3c-109">*v*</span><span class="sxs-lookup"><span data-stu-id="58a3c-109">*v*</span></span> 
</dt> <dd>

<span data-ttu-id="58a3c-110">Pointeur vers un tableau de trois éléments, en spécifiant les coordonnées x, y et z pour la position de la trame actuelle.</span><span class="sxs-lookup"><span data-stu-id="58a3c-110">A pointer to an array of three elements, specifying x, y, and z coordinates for the current raster position.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="58a3c-111">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="58a3c-111">Return value</span></span>

<span data-ttu-id="58a3c-112">Cette fonction ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="58a3c-112">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="58a3c-113">Notes</span><span class="sxs-lookup"><span data-stu-id="58a3c-113">Remarks</span></span>

<span data-ttu-id="58a3c-114">OpenGL gère une position 3D dans les coordonnées de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="58a3c-114">OpenGL maintains a 3-D position in window coordinates.</span></span> <span data-ttu-id="58a3c-115">Cette position, appelée position raster, est conservée avec la précision des sous-pixels.</span><span class="sxs-lookup"><span data-stu-id="58a3c-115">This position, called the raster position, is maintained with subpixel accuracy.</span></span> <span data-ttu-id="58a3c-116">Il est utilisé pour positionner les opérations d’écriture de pixel et de bitmap.</span><span class="sxs-lookup"><span data-stu-id="58a3c-116">It is used to position pixel and bitmap write operations.</span></span> <span data-ttu-id="58a3c-117">Consultez [**glBitmap**](glbitmap.md), [**glDrawPixels**](gldrawpixels.md)et [**glCopyPixels**](glcopypixels.md).</span><span class="sxs-lookup"><span data-stu-id="58a3c-117">See [**glBitmap**](glbitmap.md), [**glDrawPixels**](gldrawpixels.md), and [**glCopyPixels**](glcopypixels.md).</span></span>

<span data-ttu-id="58a3c-118">La position actuelle du raster est constituée de trois coordonnées de fenêtre (*x, y, z*), d’une valeur *w* de la coordonnée d’un élément, d’une distance de coordonnée oculaire, d’un bit valide, de données de couleur et de coordonnées de texture associées.</span><span class="sxs-lookup"><span data-stu-id="58a3c-118">The current raster position consists of three window coordinates (*x, y, z*), a clip coordinate *w* value, an eye coordinate distance, a valid bit, and associated color data and texture coordinates.</span></span> <span data-ttu-id="58a3c-119">La coordonnée *w* est une coordonnée de clip, car *w* n’est pas projeté aux coordonnées de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="58a3c-119">The *w* coordinate is a clip coordinate, because *w* is not projected to window coordinates.</span></span> <span data-ttu-id="58a3c-120">La fonction [glRasterPos4](glrasterpos-functions.md) spécifie les coordonnées d’objet *x, y, z* et *w* explicitement.</span><span class="sxs-lookup"><span data-stu-id="58a3c-120">The [glRasterPos4](glrasterpos-functions.md) function specifies object coordinates *x, y, z*, and *w* explicitly.</span></span> <span data-ttu-id="58a3c-121">La fonction glRasterPos3 spécifie les coordonnées d’objet *x, y* et *z* explicitement, tandis que *w* est implicitement défini sur un.</span><span class="sxs-lookup"><span data-stu-id="58a3c-121">The glRasterPos3 function specifies object coordinates *x, y,* and *z* explicitly, while *w* is implicitly set to one.</span></span> <span data-ttu-id="58a3c-122">La fonction glRasterPos2 utilise les valeurs d’argument pour *x* et *y* tout en définissant *z* et *w* de manière implicite sur zéro et un.</span><span class="sxs-lookup"><span data-stu-id="58a3c-122">The glRasterPos2 function uses the argument values for *x* and *y* while implicitly setting *z* and *w* to zero and one.</span></span>

<span data-ttu-id="58a3c-123">Les coordonnées d’objet présentées par [glRasterPos](glrasterpos-functions.md) sont traitées comme celles d’une commande [glVertex](glvertex-functions.md) .</span><span class="sxs-lookup"><span data-stu-id="58a3c-123">The object coordinates presented by [glRasterPos](glrasterpos-functions.md) are treated just like those of a [glVertex](glvertex-functions.md) command.</span></span> <span data-ttu-id="58a3c-124">Elles sont transformées par les matrices de projection et de modelview actuelles et transmises à l’étape de découpage.</span><span class="sxs-lookup"><span data-stu-id="58a3c-124">They are transformed by the current modelview and projection matrices and passed to the clipping stage.</span></span> <span data-ttu-id="58a3c-125">Si le vertex n’est pas sélectionné, il est projeté et mis à l’échelle sur les coordonnées de la fenêtre, qui devient la nouvelle position de la trame actuelle, et l’indicateur de la position de la \_ trame active du GL \_ \_ \_ est défini.</span><span class="sxs-lookup"><span data-stu-id="58a3c-125">If the vertex is not culled, then it is projected and scaled to window coordinates, which become the new current raster position, and the GL\_CURRENT\_RASTER\_POSITION\_VALID flag is set.</span></span> <span data-ttu-id="58a3c-126">Si le vertex est sélectionné, le bit valide est effacé et la position raster actuelle ainsi que les coordonnées de couleur et de texture associées ne sont pas définies.</span><span class="sxs-lookup"><span data-stu-id="58a3c-126">If the vertex is culled, then the valid bit is cleared and the current raster position and associated color and texture coordinates are undefined.</span></span>

<span data-ttu-id="58a3c-127">La position actuelle du raster comprend également des données de couleur et des coordonnées de texture associées.</span><span class="sxs-lookup"><span data-stu-id="58a3c-127">The current raster position also includes some associated color data and texture coordinates.</span></span> <span data-ttu-id="58a3c-128">Si l’éclairage est activé, la \_ \_ couleur de tramage actuelle de la comptabilité GL \_ , en mode RVBA, ou l' \_ index raster actuel du GL \_ \_ , en mode d’index des couleurs, est définie sur la couleur produite par le calcul de l’éclairage (voir [glLight](gllight-functions.md), [glLightModel](gllightmodel-functions.md)et [**glShadeModel**](glshademodel.md)).</span><span class="sxs-lookup"><span data-stu-id="58a3c-128">If lighting is enabled, then GL\_CURRENT\_RASTER\_COLOR, in RGBA mode, or the GL\_CURRENT\_RASTER\_INDEX, in color-index mode, is set to the color produced by the lighting calculation (see [glLight](gllight-functions.md), [glLightModel](gllightmodel-functions.md), and [**glShadeModel**](glshademodel.md)).</span></span> <span data-ttu-id="58a3c-129">Si l’éclairage est désactivé, la couleur actuelle (en mode RVBA, la couleur actuelle de la comptabilité de la variable d’état \_ \_ ) ou l’index de couleurs (en mode d’index des couleurs, l’index de la valeur de la comptabilité générale de \_ la variable d’état \_ ) est utilisé pour mettre à jour la couleur raster actuelle.</span><span class="sxs-lookup"><span data-stu-id="58a3c-129">If lighting is disabled, current color (in RGBA mode, state variable GL\_CURRENT\_COLOR) or color index (in color-index mode, state variable GL\_CURRENT\_INDEX) is used to update the current raster color.</span></span>

<span data-ttu-id="58a3c-130">De même, \_ les \_ \_ \_ coordonnées de la texture raster actuelle du GL sont mises à jour en fonction de la mesure de \_ texture actuelle du GL \_ \_ , en fonction de la matrice de texture et des fonctions de génération de texture (voir [glTexGen](gltexgen-functions.md)).</span><span class="sxs-lookup"><span data-stu-id="58a3c-130">Likewise, GL\_CURRENT\_RASTER\_TEXTURE\_COORDS is updated as a function of GL\_CURRENT\_TEXTURE\_COORDS, based on the texture matrix and the texture generation functions (see [glTexGen](gltexgen-functions.md)).</span></span> <span data-ttu-id="58a3c-131">Enfin, la distance entre l’origine du système de coordonnées oculaire et le sommet, telle qu’elle est transformée par la matrice modelview, remplace la distance de la \_ trame actuelle du GL \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="58a3c-131">Finally, the distance from the origin of the eye coordinate system to the vertex, as transformed by only the modelview matrix, replaces GL\_CURRENT\_RASTER\_DISTANCE.</span></span>

<span data-ttu-id="58a3c-132">Au départ, la position du raster actuel est (0, 0, 0, 1), la distance de trame actuelle est 0, le bit valide est défini, la couleur RVBA associée est (1, 1, 1, 1), l’index de couleur associé est 1 et les coordonnées de texture associées sont (0, 0, 0, 1).</span><span class="sxs-lookup"><span data-stu-id="58a3c-132">Initially, the current raster position is (0,0,0,1), the current raster distance is 0, the valid bit is set, the associated RGBA color is (1,1,1,1), the associated color index is 1, and the associated texture coordinates are (0, 0, 0, 1).</span></span> <span data-ttu-id="58a3c-133">En mode RVBA, \_ \_ l’index de tramage actuel de GL \_ est toujours 1 ; dans le mode d’index de couleurs, la couleur RVBA raster actuelle conserve toujours sa valeur initiale.</span><span class="sxs-lookup"><span data-stu-id="58a3c-133">In RGBA mode, GL\_CURRENT\_RASTER\_INDEX is always 1; in color-index mode, the current raster RGBA color always maintains its initial value.</span></span>

> [!Note]  
> <span data-ttu-id="58a3c-134">La position Raster est modifiée à la fois par [glRasterPos](glrasterpos-functions.md) et par [**glBitmap**](glbitmap.md).</span><span class="sxs-lookup"><span data-stu-id="58a3c-134">The raster position is modified both by [glRasterPos](glrasterpos-functions.md) and by [**glBitmap**](glbitmap.md).</span></span>

 

> [!Note]  
> <span data-ttu-id="58a3c-135">Lorsque les coordonnées de la position raster ne sont pas valides, les commandes de dessin basées sur la position raster sont ignorées (c’est-à-dire qu’elles n’entraînent pas de modifications de l’État OpenGL).</span><span class="sxs-lookup"><span data-stu-id="58a3c-135">When the raster position coordinates are invalid, drawing commands that are based on the raster position are ignored (that is, they do not result in changes to the OpenGL state).</span></span>

 

<span data-ttu-id="58a3c-136">Les fonctions suivantes récupèrent les informations relatives à [glRasterPos](glrasterpos-functions.md):</span><span class="sxs-lookup"><span data-stu-id="58a3c-136">The following functions retrieve information related to [glRasterPos](glrasterpos-functions.md):</span></span>

<dl>

<span data-ttu-id="58a3c-137">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) avec argument GL \_ Current \_ Raster \_ position</span><span class="sxs-lookup"><span data-stu-id="58a3c-137">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_CURRENT\_RASTER\_POSITION</span></span>  
<span data-ttu-id="58a3c-138">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) avec argument GL \_ Current \_ Raster \_ position \_ valide</span><span class="sxs-lookup"><span data-stu-id="58a3c-138">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_CURRENT\_RASTER\_POSITION\_VALID</span></span>  
<span data-ttu-id="58a3c-139">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) avec argument GL \_ Current \_ Raster \_ distance</span><span class="sxs-lookup"><span data-stu-id="58a3c-139">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_CURRENT\_RASTER\_DISTANCE</span></span>  
<span data-ttu-id="58a3c-140">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) avec argument GL \_ Current \_ Raster \_ couleur</span><span class="sxs-lookup"><span data-stu-id="58a3c-140">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_CURRENT\_RASTER\_COLOR</span></span>  
<span data-ttu-id="58a3c-141">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) avec argument GL \_ Current \_ Raster \_ index</span><span class="sxs-lookup"><span data-stu-id="58a3c-141">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_CURRENT\_RASTER\_INDEX</span></span>  
<span data-ttu-id="58a3c-142">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) avec argument de \_ la \_ texture de TRAMe actuelle du \_ GL \_</span><span class="sxs-lookup"><span data-stu-id="58a3c-142">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_CURRENT\_RASTER\_TEXTURE\_COORDS</span></span>  
</dl>

## <a name="requirements"></a><span data-ttu-id="58a3c-143">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="58a3c-143">Requirements</span></span>



| <span data-ttu-id="58a3c-144">Condition requise</span><span class="sxs-lookup"><span data-stu-id="58a3c-144">Requirement</span></span> | <span data-ttu-id="58a3c-145">Valeur</span><span class="sxs-lookup"><span data-stu-id="58a3c-145">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="58a3c-146">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="58a3c-146">Minimum supported client</span></span><br/> | <span data-ttu-id="58a3c-147">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="58a3c-147">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="58a3c-148">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="58a3c-148">Minimum supported server</span></span><br/> | <span data-ttu-id="58a3c-149">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="58a3c-149">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="58a3c-150">En-tête</span><span class="sxs-lookup"><span data-stu-id="58a3c-150">Header</span></span><br/>                   | <dl> <span data-ttu-id="58a3c-151"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="58a3c-151"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="58a3c-152">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="58a3c-152">Library</span></span><br/>                  | <dl> <span data-ttu-id="58a3c-153"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="58a3c-153"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="58a3c-154">DLL</span><span class="sxs-lookup"><span data-stu-id="58a3c-154">DLL</span></span><br/>                      | <dl> <span data-ttu-id="58a3c-155"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="58a3c-155"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="58a3c-156">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="58a3c-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="58a3c-157">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="58a3c-157">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="58a3c-158">**glBitmap**</span><span class="sxs-lookup"><span data-stu-id="58a3c-158">**glBitmap**</span></span>](glbitmap.md)
</dt> <dt>

[<span data-ttu-id="58a3c-159">**glCopyPixels**</span><span class="sxs-lookup"><span data-stu-id="58a3c-159">**glCopyPixels**</span></span>](glcopypixels.md)
</dt> <dt>

[<span data-ttu-id="58a3c-160">**glDrawPixels**</span><span class="sxs-lookup"><span data-stu-id="58a3c-160">**glDrawPixels**</span></span>](gldrawpixels.md)
</dt> <dt>

[<span data-ttu-id="58a3c-161">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="58a3c-161">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="58a3c-162">glLight</span><span class="sxs-lookup"><span data-stu-id="58a3c-162">glLight</span></span>](gllight-functions.md)
</dt> <dt>

[<span data-ttu-id="58a3c-163">glLightModel</span><span class="sxs-lookup"><span data-stu-id="58a3c-163">glLightModel</span></span>](gllightmodel-functions.md)
</dt> <dt>

[<span data-ttu-id="58a3c-164">**glShadeModel**</span><span class="sxs-lookup"><span data-stu-id="58a3c-164">**glShadeModel**</span></span>](glshademodel.md)
</dt> <dt>

[<span data-ttu-id="58a3c-165">**glTexCoord**</span><span class="sxs-lookup"><span data-stu-id="58a3c-165">**glTexCoord**</span></span>](gltexcoord-functions.md)
</dt> <dt>

[<span data-ttu-id="58a3c-166">glTexGen</span><span class="sxs-lookup"><span data-stu-id="58a3c-166">glTexGen</span></span>](gltexgen-functions.md)
</dt> <dt>

[<span data-ttu-id="58a3c-167">glVertex</span><span class="sxs-lookup"><span data-stu-id="58a3c-167">glVertex</span></span>](glvertex-functions.md)
</dt> </dl>

 

 





