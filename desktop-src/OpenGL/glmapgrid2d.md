---
title: fonction glMapGrid2d (GL. h)
description: Définit un maillage unidimensionnel. | fonction glMapGrid2d (GL. h)
ms.assetid: 5e5887d1-e137-434b-a1f3-b3f10d462823
keywords:
- glMapGrid2d fonction OpenGL
topic_type:
- apiref
api_name:
- glMapGrid2d
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6992a904528cf961f27335e7241c50fbd14f058b
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "106531773"
---
# <a name="glmapgrid2d-function"></a><span data-ttu-id="d7969-105">glMapGrid2d fonction)</span><span class="sxs-lookup"><span data-stu-id="d7969-105">glMapGrid2d function</span></span>

<span data-ttu-id="d7969-106">Définit un maillage unidimensionnel.</span><span class="sxs-lookup"><span data-stu-id="d7969-106">Defines a one-dimensional mesh.</span></span>

## <a name="syntax"></a><span data-ttu-id="d7969-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d7969-107">Syntax</span></span>


```C++
void WINAPI glMapGrid2d(
   GLint    un,
   GLdouble u1,
   GLdouble u2,
   GLint    vn,
   GLdouble v1,
   GLdouble v2
);
```



## <a name="parameters"></a><span data-ttu-id="d7969-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d7969-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d7969-109">*un*</span><span class="sxs-lookup"><span data-stu-id="d7969-109">*un*</span></span> 
</dt> <dd>

<span data-ttu-id="d7969-110">Nombre de partitions dans l’intervalle de plage de la grille \[ U1, U2 \] .</span><span class="sxs-lookup"><span data-stu-id="d7969-110">The number of partitions in the grid range interval \[u1, u2\].</span></span> <span data-ttu-id="d7969-111">Cette valeur doit être positive.</span><span class="sxs-lookup"><span data-stu-id="d7969-111">This value must be positive.</span></span>

</dd> <dt>

<span data-ttu-id="d7969-112">*U1*</span><span class="sxs-lookup"><span data-stu-id="d7969-112">*u1*</span></span> 
</dt> <dd>

<span data-ttu-id="d7969-113">Valeur utilisée comme mappage de la valeur de domaine de la grille entière i = 0.</span><span class="sxs-lookup"><span data-stu-id="d7969-113">A value used as the mapping for integer grid domain value i = 0.</span></span>

</dd> <dt>

<span data-ttu-id="d7969-114">*U2*</span><span class="sxs-lookup"><span data-stu-id="d7969-114">*u2*</span></span> 
</dt> <dd>

<span data-ttu-id="d7969-115">Valeur utilisée comme mappage de la valeur de domaine de la grille entière i = non.</span><span class="sxs-lookup"><span data-stu-id="d7969-115">A value used as the mapping for integer grid domain value i = un.</span></span>

</dd> <dt>

<span data-ttu-id="d7969-116">*VN*</span><span class="sxs-lookup"><span data-stu-id="d7969-116">*vn*</span></span> 
</dt> <dd>

<span data-ttu-id="d7969-117">Nombre de partitions dans l’intervalle de plage de la grille \[ v1, v2 \] .</span><span class="sxs-lookup"><span data-stu-id="d7969-117">The number of partitions in the grid range interval \[v1, v2\].</span></span>

</dd> <dt>

<span data-ttu-id="d7969-118">*v1*</span><span class="sxs-lookup"><span data-stu-id="d7969-118">*v1*</span></span> 
</dt> <dd>

<span data-ttu-id="d7969-119">Valeur utilisée comme mappage de la valeur de domaine de la grille entière j = 0.</span><span class="sxs-lookup"><span data-stu-id="d7969-119">A value used as the mapping for integer grid domain value j = 0.</span></span>

</dd> <dt>

<span data-ttu-id="d7969-120">*v2*</span><span class="sxs-lookup"><span data-stu-id="d7969-120">*v2*</span></span> 
</dt> <dd>

<span data-ttu-id="d7969-121">Valeur utilisée comme mappage de la valeur de domaine de la grille entière j = VN.</span><span class="sxs-lookup"><span data-stu-id="d7969-121">A value used as the mapping for integer grid domain value j = vn.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d7969-122">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="d7969-122">Return value</span></span>

<span data-ttu-id="d7969-123">Cette fonction ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="d7969-123">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="d7969-124">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="d7969-124">Error codes</span></span>

<span data-ttu-id="d7969-125">Les codes d’erreur suivants peuvent être récupérés par la fonction [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="d7969-125">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="d7969-126">Nom</span><span class="sxs-lookup"><span data-stu-id="d7969-126">Name</span></span>                                                                                                  | <span data-ttu-id="d7969-127">Signification</span><span class="sxs-lookup"><span data-stu-id="d7969-127">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="d7969-128"><dt>**\_valeur non valide du GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="d7969-128"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="d7969-129">Un  ou un *VN* n’était pas positif.</span><span class="sxs-lookup"><span data-stu-id="d7969-129">Either *un* or *vn* was not positive.</span></span><br/>                                                                                      |
| <dl> <span data-ttu-id="d7969-130"><dt>**\_opération non valide du GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="d7969-130"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="d7969-131">La fonction a été appelée entre un appel à [**glBegin**](glbegin.md) et l’appel correspondant à [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="d7969-131">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="d7969-132">Notes</span><span class="sxs-lookup"><span data-stu-id="d7969-132">Remarks</span></span>

<span data-ttu-id="d7969-133">Les fonctions **glMapGrid** et [glEvalMesh](glevalmesh-functions.md) sont utilisées en tandem pour générer et évaluer efficacement une série de valeurs de domaine de mappage uniformément espacées.</span><span class="sxs-lookup"><span data-stu-id="d7969-133">The **glMapGrid** and [glEvalMesh](glevalmesh-functions.md) functions are used in tandem to efficiently generate and evaluate a series of evenly spaced map domain values.</span></span> <span data-ttu-id="d7969-134">La fonction glEvalMesh effectue un pas à pas dans le domaine entier d’une grille unidimensionnelle ou à deux dimensions, dont la plage est le domaine des mappages d’évaluation spécifiés par [**glMap1**](glmap1.md) et [**glMap2**](glmap2.md).</span><span class="sxs-lookup"><span data-stu-id="d7969-134">The glEvalMesh function steps through the integer domain of a one- or two-dimensional grid, whose range is the domain of the evaluation maps specified by [**glMap1**](glmap1.md) and [**glMap2**](glmap2.md).</span></span>

<span data-ttu-id="d7969-135">Les fonctions [**glMapGrid1**](glmapgrid1d.md) et **glMapGrid2** spécifient les mappages de grille linéaire entre les coordonnées de la grille entière i (ou i et j) et les coordonnées de la carte d’évaluation à virgule flottante u (ou v et v).</span><span class="sxs-lookup"><span data-stu-id="d7969-135">The [**glMapGrid1**](glmapgrid1d.md) and **glMapGrid2** functions specify the linear grid mappings between the i (or i and j) integer grid coordinates, to the u (or u and v) floating-point evaluation map coordinates.</span></span> <span data-ttu-id="d7969-136">Pour plus d’informations sur l’évaluation des coordonnées v et v, consultez [**glMap1**](glmap1.md) et [**glMap2**](glmap2.md) .</span><span class="sxs-lookup"><span data-stu-id="d7969-136">See [**glMap1**](glmap1.md) and [**glMap2**](glmap2.md) for details of how u and v coordinates are evaluated.</span></span>

<span data-ttu-id="d7969-137">La fonction [**glMapGrid1**](glmapgrid1d.md) spécifie un mappage linéaire unique, de sorte que la *coordonnée* de grille entière 0 correspond exactement à U1, et que la coordonnée de grille entière n’est pas mappée exactement à *U2*.</span><span class="sxs-lookup"><span data-stu-id="d7969-137">The [**glMapGrid1**](glmapgrid1d.md) function specifies a single linear mapping such that integer grid coordinate 0 maps exactly to u1, and integer grid coordinate *un* maps exactly to *u2*.</span></span> <span data-ttu-id="d7969-138">Toutes les autres coordonnées de grille entières que *je suis* mappées de la façon suivante :</span><span class="sxs-lookup"><span data-stu-id="d7969-138">All other integer grid coordinates *i* are mapped such that:</span></span>

<span data-ttu-id="d7969-139">*u = i (U2 U1)/un + U1*</span><span class="sxs-lookup"><span data-stu-id="d7969-139">*u = i(u2 u1)/un + u1*</span></span>

<span data-ttu-id="d7969-140">La fonction **glMapGrid2** spécifie deux mappages linéaires de ce type.</span><span class="sxs-lookup"><span data-stu-id="d7969-140">The **glMapGrid2** function specifies two such linear mappings.</span></span> <span data-ttu-id="d7969-141">L’un mappe la coordonnée de grille entière *i = 0* exactement à *U1*, et la coordonnée de grille entière *i =* non exactement à *U2*.</span><span class="sxs-lookup"><span data-stu-id="d7969-141">One maps integer grid coordinate *i = 0* exactly to *u1*, and integer grid coordinate *i = un* exactly to *u2*.</span></span> <span data-ttu-id="d7969-142">L’autre mappe la coordonnée de grille entière *j = 0* exactement à *v1*, et la coordonnée de grille entière *j = VN* exactement à *v2*.</span><span class="sxs-lookup"><span data-stu-id="d7969-142">The other maps integer grid coordinate *j = 0* exactly to *v1*, and integer grid coordinate *j = vn* exactly to *v2*.</span></span> <span data-ttu-id="d7969-143">Les autres coordonnées de grille entière i et j sont mappées de telle sorte que</span><span class="sxs-lookup"><span data-stu-id="d7969-143">Other integer grid coordinates i and j are mapped such that</span></span>

<span data-ttu-id="d7969-144">*u = i (U2 U1)/un + U1*</span><span class="sxs-lookup"><span data-stu-id="d7969-144">*u = i(u2 u1)/un + u1*</span></span>

<span data-ttu-id="d7969-145">*v = j (V2 V1)/VN + v1*</span><span class="sxs-lookup"><span data-stu-id="d7969-145">*v = j (v2 v1)/vn + v1*</span></span>

<span data-ttu-id="d7969-146">Les mappages spécifiés par [**glMapGrid**](glmapgrid1d.md) sont utilisés de façon identique par [glEvalMesh](glevalmesh-functions.md) et [**glEvalPoint**](glevalpoint.md).</span><span class="sxs-lookup"><span data-stu-id="d7969-146">The mappings specified by [**glMapGrid**](glmapgrid1d.md) are used identically by [glEvalMesh](glevalmesh-functions.md) and [**glEvalPoint**](glevalpoint.md).</span></span>

<span data-ttu-id="d7969-147">Les fonctions suivantes récupèrent les informations relatives à [**glMapGrid**](glmapgrid1d.md):</span><span class="sxs-lookup"><span data-stu-id="d7969-147">The following functions retrieve information related to [**glMapGrid**](glmapgrid1d.md):</span></span>

<dl>

<span data-ttu-id="d7969-148">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) avec argument GL \_ Map1 \_ Grid \_ Domain</span><span class="sxs-lookup"><span data-stu-id="d7969-148">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_MAP1\_GRID\_DOMAIN</span></span>  
<span data-ttu-id="d7969-149">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) avec argument GL \_ map2 \_ Grid \_ Domain</span><span class="sxs-lookup"><span data-stu-id="d7969-149">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_MAP2\_GRID\_DOMAIN</span></span>  
<span data-ttu-id="d7969-150">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) avec des \_ segments de \_ grille \_ Map1 d’argument GL</span><span class="sxs-lookup"><span data-stu-id="d7969-150">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_MAP1\_GRID\_SEGMENTS</span></span>  
<span data-ttu-id="d7969-151">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) avec des \_ segments de \_ grille \_ map2 d’argument GL</span><span class="sxs-lookup"><span data-stu-id="d7969-151">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_MAP2\_GRID\_SEGMENTS</span></span>  
</dl>

## <a name="requirements"></a><span data-ttu-id="d7969-152">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d7969-152">Requirements</span></span>



| <span data-ttu-id="d7969-153">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d7969-153">Requirement</span></span> | <span data-ttu-id="d7969-154">Valeur</span><span class="sxs-lookup"><span data-stu-id="d7969-154">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d7969-155">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d7969-155">Minimum supported client</span></span><br/> | <span data-ttu-id="d7969-156">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d7969-156">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="d7969-157">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d7969-157">Minimum supported server</span></span><br/> | <span data-ttu-id="d7969-158">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d7969-158">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="d7969-159">En-tête</span><span class="sxs-lookup"><span data-stu-id="d7969-159">Header</span></span><br/>                   | <dl> <span data-ttu-id="d7969-160"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="d7969-160"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="d7969-161">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="d7969-161">Library</span></span><br/>                  | <dl> <span data-ttu-id="d7969-162"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d7969-162"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="d7969-163">DLL</span><span class="sxs-lookup"><span data-stu-id="d7969-163">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d7969-164"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d7969-164"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d7969-165">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d7969-165">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d7969-166">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="d7969-166">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="d7969-167">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="d7969-167">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="d7969-168">**glEvalCoord**</span><span class="sxs-lookup"><span data-stu-id="d7969-168">**glEvalCoord**</span></span>](glevalcoord-functions.md)
</dt> <dt>

[<span data-ttu-id="d7969-169">glEvalMesh</span><span class="sxs-lookup"><span data-stu-id="d7969-169">glEvalMesh</span></span>](glevalmesh-functions.md)
</dt> <dt>

[<span data-ttu-id="d7969-170">**glEvalPoint**</span><span class="sxs-lookup"><span data-stu-id="d7969-170">**glEvalPoint**</span></span>](glevalpoint.md)
</dt> <dt>

[<span data-ttu-id="d7969-171">**glMap1**</span><span class="sxs-lookup"><span data-stu-id="d7969-171">**glMap1**</span></span>](glmap1.md)
</dt> <dt>

[<span data-ttu-id="d7969-172">**glMap2**</span><span class="sxs-lookup"><span data-stu-id="d7969-172">**glMap2**</span></span>](glmap2.md)
</dt> </dl>

 

 





