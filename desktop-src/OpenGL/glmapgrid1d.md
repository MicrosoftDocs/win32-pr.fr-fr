---
title: fonction glMapGrid1d (GL. h)
description: Définit un maillage unidimensionnel. | fonction glMapGrid1d (GL. h)
ms.assetid: a0bc822e-dd98-4586-a322-2779e11f38ca
keywords:
- glMapGrid1d fonction OpenGL
topic_type:
- apiref
api_name:
- glMapGrid1d
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 30b1900f5597e8c516100504ca7288137ed99ded
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "103869713"
---
# <a name="glmapgrid1d-function"></a><span data-ttu-id="39426-105">glMapGrid1d fonction)</span><span class="sxs-lookup"><span data-stu-id="39426-105">glMapGrid1d function</span></span>

<span data-ttu-id="39426-106">Définit un maillage unidimensionnel.</span><span class="sxs-lookup"><span data-stu-id="39426-106">Defines a one-dimensional mesh.</span></span>

## <a name="syntax"></a><span data-ttu-id="39426-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="39426-107">Syntax</span></span>


```C++
void WINAPI glMapGrid1d(
   GLint    un,
   GLdouble u1,
   GLdouble u2
);
```



## <a name="parameters"></a><span data-ttu-id="39426-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="39426-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="39426-109">*un*</span><span class="sxs-lookup"><span data-stu-id="39426-109">*un*</span></span> 
</dt> <dd>

<span data-ttu-id="39426-110">Nombre de partitions dans l’intervalle de plage de la grille \[ U1, U2 \] .</span><span class="sxs-lookup"><span data-stu-id="39426-110">The number of partitions in the grid range interval \[u1, u2\].</span></span> <span data-ttu-id="39426-111">Cette valeur doit être positive.</span><span class="sxs-lookup"><span data-stu-id="39426-111">This value must be positive.</span></span>

</dd> <dt>

<span data-ttu-id="39426-112">*U1*</span><span class="sxs-lookup"><span data-stu-id="39426-112">*u1*</span></span> 
</dt> <dd>

<span data-ttu-id="39426-113">Valeur utilisée comme mappage de la valeur de domaine de la grille entière i = 0.</span><span class="sxs-lookup"><span data-stu-id="39426-113">A value used as the mapping for integer grid domain value i = 0.</span></span>

</dd> <dt>

<span data-ttu-id="39426-114">*U2*</span><span class="sxs-lookup"><span data-stu-id="39426-114">*u2*</span></span> 
</dt> <dd>

<span data-ttu-id="39426-115">Valeur utilisée comme mappage de la valeur de domaine de la grille entière i = non.</span><span class="sxs-lookup"><span data-stu-id="39426-115">A value used as the mapping for integer grid domain value i = un.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="39426-116">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="39426-116">Return value</span></span>

<span data-ttu-id="39426-117">Cette fonction ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="39426-117">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="39426-118">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="39426-118">Error codes</span></span>

<span data-ttu-id="39426-119">Les codes d’erreur suivants peuvent être récupérés par la fonction [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="39426-119">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="39426-120">Nom</span><span class="sxs-lookup"><span data-stu-id="39426-120">Name</span></span>                                                                                                  | <span data-ttu-id="39426-121">Signification</span><span class="sxs-lookup"><span data-stu-id="39426-121">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="39426-122"><dt>**\_valeur non valide du GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="39426-122"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="39426-123">Un  ou un *VN* n’était pas positif.</span><span class="sxs-lookup"><span data-stu-id="39426-123">Either *un* or *vn* was not positive.</span></span><br/>                                                                                      |
| <dl> <span data-ttu-id="39426-124"><dt>**\_opération non valide du GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="39426-124"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="39426-125">La fonction a été appelée entre un appel à [**glBegin**](glbegin.md) et l’appel correspondant à [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="39426-125">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="39426-126">Notes</span><span class="sxs-lookup"><span data-stu-id="39426-126">Remarks</span></span>

<span data-ttu-id="39426-127">Utilisez les fonctions **glMapGrid** et [glEvalMesh](glevalmesh-functions.md) togetherto pour générer et évaluer efficacement une série de valeurs de domaine de mappage uniformément espacées.</span><span class="sxs-lookup"><span data-stu-id="39426-127">Use the **glMapGrid** and [glEvalMesh](glevalmesh-functions.md) functions togetherto efficiently generate and evaluate a series of evenly spaced map domain values.</span></span> <span data-ttu-id="39426-128">La fonction glEvalMesh effectue un pas à pas dans le domaine entier d’une grille unidimensionnelle ou à deux dimensions, dont la plage est le domaine des mappages d’évaluation spécifiés par [**glMap1**](glmap1.md) et [**glMap2**](glmap2.md).</span><span class="sxs-lookup"><span data-stu-id="39426-128">The glEvalMesh function steps through the integer domain of a one- or two-dimensional grid, whose range is the domain of the evaluation maps specified by [**glMap1**](glmap1.md) and [**glMap2**](glmap2.md).</span></span>

<span data-ttu-id="39426-129">Les fonctions **glMapGrid1** et [**glMapGrid2**](glmapgrid2d.md) spécifient les mappages de grille linéaire entre les coordonnées de la grille entière i (ou i et j) et les coordonnées de la carte d’évaluation à virgule flottante u (ou v et v).</span><span class="sxs-lookup"><span data-stu-id="39426-129">The **glMapGrid1** and [**glMapGrid2**](glmapgrid2d.md) functions specify the linear grid mappings between the i (or i and j) integer grid coordinates, to the u (or u and v) floating-point evaluation map coordinates.</span></span> <span data-ttu-id="39426-130">Pour plus d’informations sur l’évaluation des coordonnées v et v, consultez [**glMap1**](glmap1.md) et [**glMap2**](glmap2.md) .</span><span class="sxs-lookup"><span data-stu-id="39426-130">See [**glMap1**](glmap1.md) and [**glMap2**](glmap2.md) for details of how u and v coordinates are evaluated.</span></span>

<span data-ttu-id="39426-131">La fonction **glMapGrid1** spécifie un mappage linéaire unique, de sorte que la *coordonnée* de grille entière 0 correspond exactement à U1, et que la coordonnée de grille entière n’est pas mappée exactement à *U2*.</span><span class="sxs-lookup"><span data-stu-id="39426-131">The **glMapGrid1** function specifies a single linear mapping such that integer grid coordinate 0 maps exactly to u1, and integer grid coordinate *un* maps exactly to *u2*.</span></span> <span data-ttu-id="39426-132">Toutes les autres coordonnées de grille entières que *je suis* mappées de la façon suivante :</span><span class="sxs-lookup"><span data-stu-id="39426-132">All other integer grid coordinates *i* are mapped such that:</span></span>

<span data-ttu-id="39426-133">*u = i (U2 U1)/un + U1*</span><span class="sxs-lookup"><span data-stu-id="39426-133">*u = i(u2 u1)/un + u1*</span></span>

<span data-ttu-id="39426-134">La fonction [**glMapGrid2**](glmapgrid2d.md) spécifie deux mappages linéaires de ce type.</span><span class="sxs-lookup"><span data-stu-id="39426-134">The [**glMapGrid2**](glmapgrid2d.md) function specifies two such linear mappings.</span></span> <span data-ttu-id="39426-135">L’un mappe la coordonnée de grille entière *i = 0* exactement à *U1*, et la coordonnée de grille entière *i =* non exactement à *U2*.</span><span class="sxs-lookup"><span data-stu-id="39426-135">One maps integer grid coordinate *i = 0* exactly to *u1*, and integer grid coordinate *i = un* exactly to *u2*.</span></span> <span data-ttu-id="39426-136">L’autre mappe la coordonnée de grille entière *j = 0* exactement à *v1*, et la coordonnée de grille entière *j = VN* exactement à *v2*.</span><span class="sxs-lookup"><span data-stu-id="39426-136">The other maps integer grid coordinate *j = 0* exactly to *v1*, and integer grid coordinate *j = vn* exactly to *v2*.</span></span> <span data-ttu-id="39426-137">Les autres coordonnées de grille entière i et j sont mappées de telle sorte que</span><span class="sxs-lookup"><span data-stu-id="39426-137">Other integer grid coordinates i and j are mapped such that</span></span>

<span data-ttu-id="39426-138">*u = i (U2 U1)/un + U1*</span><span class="sxs-lookup"><span data-stu-id="39426-138">*u = i(u2 u1)/un + u1*</span></span>

<span data-ttu-id="39426-139">*v = j (V2 V1)/VN + v1*</span><span class="sxs-lookup"><span data-stu-id="39426-139">*v = j (v2 v1)/vn + v1*</span></span>

<span data-ttu-id="39426-140">Les mappages spécifiés par **glMapGrid** sont utilisés de façon identique par [glEvalMesh](glevalmesh-functions.md) et [**glEvalPoint**](glevalpoint.md).</span><span class="sxs-lookup"><span data-stu-id="39426-140">The mappings specified by **glMapGrid** are used identically by [glEvalMesh](glevalmesh-functions.md) and [**glEvalPoint**](glevalpoint.md).</span></span>

<span data-ttu-id="39426-141">Les fonctions suivantes récupèrent les informations relatives à **glMapGrid**:</span><span class="sxs-lookup"><span data-stu-id="39426-141">The following functions retrieve information related to **glMapGrid**:</span></span>

<dl>

<span data-ttu-id="39426-142">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) avec argument GL \_ Map1 \_ Grid \_ Domain</span><span class="sxs-lookup"><span data-stu-id="39426-142">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_MAP1\_GRID\_DOMAIN</span></span>  
<span data-ttu-id="39426-143">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) avec argument GL \_ map2 \_ Grid \_ Domain</span><span class="sxs-lookup"><span data-stu-id="39426-143">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_MAP2\_GRID\_DOMAIN</span></span>  
<span data-ttu-id="39426-144">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) avec des \_ segments de \_ grille \_ Map1 d’argument GL</span><span class="sxs-lookup"><span data-stu-id="39426-144">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_MAP1\_GRID\_SEGMENTS</span></span>  
<span data-ttu-id="39426-145">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) avec des \_ segments de \_ grille \_ map2 d’argument GL</span><span class="sxs-lookup"><span data-stu-id="39426-145">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_MAP2\_GRID\_SEGMENTS</span></span>  
</dl>

## <a name="requirements"></a><span data-ttu-id="39426-146">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="39426-146">Requirements</span></span>



| <span data-ttu-id="39426-147">Condition requise</span><span class="sxs-lookup"><span data-stu-id="39426-147">Requirement</span></span> | <span data-ttu-id="39426-148">Valeur</span><span class="sxs-lookup"><span data-stu-id="39426-148">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="39426-149">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="39426-149">Minimum supported client</span></span><br/> | <span data-ttu-id="39426-150">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="39426-150">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="39426-151">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="39426-151">Minimum supported server</span></span><br/> | <span data-ttu-id="39426-152">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="39426-152">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="39426-153">En-tête</span><span class="sxs-lookup"><span data-stu-id="39426-153">Header</span></span><br/>                   | <dl> <span data-ttu-id="39426-154"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="39426-154"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="39426-155">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="39426-155">Library</span></span><br/>                  | <dl> <span data-ttu-id="39426-156"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="39426-156"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="39426-157">DLL</span><span class="sxs-lookup"><span data-stu-id="39426-157">DLL</span></span><br/>                      | <dl> <span data-ttu-id="39426-158"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="39426-158"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="39426-159">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="39426-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="39426-160">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="39426-160">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="39426-161">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="39426-161">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="39426-162">**glEvalCoord**</span><span class="sxs-lookup"><span data-stu-id="39426-162">**glEvalCoord**</span></span>](glevalcoord-functions.md)
</dt> <dt>

[<span data-ttu-id="39426-163">glEvalMesh</span><span class="sxs-lookup"><span data-stu-id="39426-163">glEvalMesh</span></span>](glevalmesh-functions.md)
</dt> <dt>

[<span data-ttu-id="39426-164">**glEvalPoint**</span><span class="sxs-lookup"><span data-stu-id="39426-164">**glEvalPoint**</span></span>](glevalpoint.md)
</dt> <dt>

[<span data-ttu-id="39426-165">**glMap1**</span><span class="sxs-lookup"><span data-stu-id="39426-165">**glMap1**</span></span>](glmap1.md)
</dt> <dt>

[<span data-ttu-id="39426-166">**glMap2**</span><span class="sxs-lookup"><span data-stu-id="39426-166">**glMap2**</span></span>](glmap2.md)
</dt> </dl>

 

 





